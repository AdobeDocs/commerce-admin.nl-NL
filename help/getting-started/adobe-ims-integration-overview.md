---
title: Overzicht van de integratie van Adobe Identity Management Service (IMS)
description: Introduceert de optionele integratie van Adobe Commerce Admin-aanmelding met Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Overzicht van de integratie van Adobe Identity Management Service (IMS)

{{ee-feature}}

Adobe Commerce Admin-gebruikers met een Adobe-account kunnen hun Adobe ID nu gebruiken om zich aan te melden bij Adobe Commerce. Adobe Identity Management Service (IMS) is de op OAuth 2.0 gebaseerde functie voor identiteitsbeheer van de Adobe die verificatie ondersteunt. Het integreren van de authentificatie van Admin van de Handel in de authentificatiewerkschema IMS van het Bedrijfs product van de Adobe kan het authentificatieproces voor gebruikers stroomlijnen die met andere producten van de Adobe werken. Deze integratie is optioneel en wordt per geval ingeschakeld. Alleen de workflows van de Admin-gebruiker worden beïnvloed wanneer deze integratie is ingeschakeld. 

De modules die voor de integratie van Admin IMS van de Handel worden vereist worden verpakt in  `adobe-ims-metapackage`, die wordt meegeleverd bij Adobe Commerce core-releases.

Voor de implementatie van deze integratie raadpleegt u [Vorm de Integratie van Admin van de Handel met IMS](./adobe-ims-config.md).

## Wijzigingen in beheerworkflows en -interface na integratie met IMS

Wanneer deze integratie wordt toegelaten, ervaren de gebruikers van Admin van de Handel veranderingen in de standaard login en authentificatiewerkschema van Admin van de Handel aangezien zij routinetaken in Admin uitvoeren die reauthentication, zoals het creëren van een gebruiker Admin vereisen. Om moduleactivering mogelijk te maken, is tweeledige verificatie (2FA) op het niveau van de Adobe organisatie vereist. De standaard aanmeldingsnaam voor Admin en 2FA zijn uitgeschakeld en de _[!UICONTROL Sign In with Adobe ID]_wordt het standaardformulier Admin vervangen. Rechten worden nog steeds beheerd door de beheerder.

## Hoe de integratie Admin met IMS Commerce wachtwoorden beïnvloedt

Voor handelsplaatsingen die met Adobe IMS zijn geïntegreerd, is een Adobe ID-account vereist met toegang tot de Adobe IMS-organisatie die tijdens het IMS-activeringsproces is geconfigureerd voor de Commerce-toepassing.  Wanneer de IMS-integratie is ingeschakeld, verifiëren beheerders zich via de aanmeldingspagina voor de Adobe met hun Adobe. De handelswachtwoorden en gebruikersnamen voor admin-gebruikers worden niet meer gebruikt voor verificatie zolang de integratie met Adobe IMS is ingeschakeld.

Als de IMS-integratie is uitgeschakeld, moeten gebruikers van beheerders zich opnieuw via Adobe Commerce verifiëren met hun gebruikersnaam en wachtwoord voor Handel. Admin-gebruikers moeten hun Admin-gebruikersgegevens (gebruikersnaam en wachtwoord) en 2FA-gegevens van Commerce opslaan voordat ze deze integratie kunnen inschakelen.

Voor bepaalde back-endcomponenten die bij gebruikersverificatie zijn betrokken, is nog steeds een wachtwoord vereist dat niet gelijk is aan null. Om aan dit vereiste te voldoen, leidt de Handel tot willekeurige wachtwoorden voor pas gecreëerde admin gebruikers in `admin_user` tabel.

De rekeningen van de gebruiker en de roltoestemmingen voor de toepassing van de Handel worden nog beheerd van Admin van de Handel.


## Web API-token genereren met IMS-referenties

Commerce Admin APIs wordt beïnvloed wanneer de authentificatie van Admin met Adobe IMS in een instantie van de Handel wordt toegelaten. De gebruikers Admin kunnen niet meer de geloofsbrieven gebruiken die door de instantie van de Handel worden uitgegeven. Dit zijn de geloofsbrieven die worden vereist om login aan Admin en om toegangstokens te verkrijgen die de diensten kunnen gebruiken om verzoeken aan Admin REST en de APIs van de ZEEP te doen.

Nadat de integratie met Adobe IMS is ingeschakeld, moeten gebruikers van beheerders [Adobe IMS OAuth-tokens](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) voor Adobe Commerce API-eindpunten waarvoor verificatie is vereist. De oplossingen van de cliënt verkrijgen dynamisch de tokens voor Web API gebruik. Dit verificatiemechanisme wordt ingeschakeld voor REST- en SOAP-web-API-gebieden als onderdeel van het configureren van deze integratie.

Zie [Op token gebaseerde verificatie](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) voor een overzicht van hoe Web APIs de toegangstokens van de Handel, met inbegrip van IMS toegangstokens gebruiken.

## Sessiebeheer voor handel en Adobe IMS-toegangstokens

Toegangstokens bevatten zowel gebruikersgegevens als aanmeldingssessiegegevens. Nadat een gebruiker is geverifieerd en een sessie is gestart, worden de volgende twee variabelen aan de gebruikerssessie toegevoegd:

`token_last_check_time`. Hiermee wordt de huidige tijd aangegeven en wordt deze gebruikt door de `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` insteekmodule.

`adobe_access_token` — Identificeert de `ACCESS_TOKEN` tijdens de autorisatie ontvangen waarde.

De `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` insteekmodule controleert of de `token_last_check_time` 10 minuten geleden bijgewerkt. Als de `token_last_check_time` werd tien minuten geleden gecontroleerd, dan maakt het authentificatiewerkschema een API vraag aan IMS om het toegangstoken te bevestigen, en de zitting gaat verder. Als het toegangstoken geldig is, dan `token_last_check_time` waarde wordt bijgewerkt naar de huidige tijd. Als het token niet geldig is, wordt de sessie beëindigd.

## Belangrijke bestanden

`adminAdobeIms` - Biedt een implementatie van de beheerdersaanmelding op basis van de `AdobeImsApi` -module.

`admin_adobe_ims_webapi` - Hiermee wordt een overzicht bijgehouden van alle gevalideerde toegangstokens. Wanneer een token wordt gevalideerd of ongeldig wordt gemaakt, blijft een record van de status ervan in deze tabel behouden.

`adobeIms` - Implementeert alle bedrijfslogica die gerelateerd is aan integratie met Adobe IMS (zodat incompatibiliteiten met oudere versies worden voorkomen).

`adobeImsApi` - Declareert de interfaces die integratie met Adobe IMS steunen.

`adminadobe-ims.log` - Foutlogbestand.

## Integratie inschakelen

Het Adobe IMS-pakket voor metagegevens is geïnstalleerd met Adobe Commerce 2.4.5 en hoger, maar moet zijn geconfigureerd voor gebruik. Het breidt de `AdobeIms` module om de module te steunen die authentificatielogica ( toelaat`AdminAdobeIms`).

Ga voor meer informatie over het inschakelen van de integratie naar [De integratie van Commerce Admin met Adobe IMS configureren](./adobe-ims-config.md).
