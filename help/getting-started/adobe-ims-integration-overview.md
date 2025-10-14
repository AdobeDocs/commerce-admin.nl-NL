---
title: Overzicht van de integratie van Adobe Identity Management Service (IMS)
description: Introduceert de optionele integratie van Adobe Commerce Admin-aanmelding met Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Overzicht van de integratie van Adobe Identity Management Service (IMS)

{{ee-feature}}

Adobe Commerce Admin-gebruikers met een Adobe-account kunnen hun Adobe ID nu gebruiken om zich aan te melden bij Adobe Commerce. Adobe Identity Management Service (IMS) is een op Adobe 2.0 gebaseerde functie voor identiteitsbeheer die verificatie ondersteunt. Door de Commerce Admin-verificatie te integreren in de IMS-verificatieworkflow van Adobe Business Product kan het verificatieproces worden gestroomlijnd voor gebruikers die met andere Adobe-producten werken. Deze integratie is optioneel en wordt per geval ingeschakeld. Alleen de workflows van de Admin-gebruiker worden beïnvloed wanneer deze integratie is ingeschakeld. 

De modules die vereist zijn voor de integratie van Commerce Admin IMS worden verpakt in `adobe-ims-metapackage` , dat wordt meegeleverd bij Adobe Commerce core-releases.

Om deze integratie uit te voeren, zie [&#x200B; de Integratie van Admin van Commerce met IMS &#x200B;](./adobe-ims-config.md) vormen.

## Wijzigingen in beheerworkflows en -interface na integratie met IMS

Als deze integratie is ingeschakeld, ervaren Commerce Admin-gebruikers wijzigingen in de standaard Commerce Admin-aanmeldings- en verificatieworkflow terwijl ze routinetaken in Admin uitvoeren waarvoor verificatie vereist is, zoals het maken van een Admin-gebruiker. Om moduleactivering mogelijk te maken, is tweeledige verificatie (2FA) op het niveau van de Adobe-organisatie vereist. De standaardaanmelding voor beheer en 2FA zijn uitgeschakeld en de knop _[!UICONTROL Sign In with Adobe ID]_&#x200B;vervangt het standaardaanmeldingsformulier voor beheer. Rechten worden nog steeds beheerd door de beheerder.

## Hoe de integratie van Admin met IMS Commerce wachtwoorden beïnvloedt

Voor Commerce-implementaties die met Adobe IMS zijn geïntegreerd, is een Adobe ID-account vereist met toegang tot de Adobe IMS-organisatie die tijdens het IMS-activeringsproces is geconfigureerd voor de Commerce-toepassing.  Wanneer de IMS-integratie is ingeschakeld, verifiëren beheerders zich via de Adobe-aanmeldpagina met hun Adobe-gegevens. De Commerce-wachtwoorden en -gebruikersnamen voor beheerders worden niet meer gebruikt voor verificatie zolang de integratie met Adobe IMS is ingeschakeld.

Als de IMS-integratie is uitgeschakeld, moeten beheerders de verificatie via Adobe Commerce opnieuw uitvoeren met hun Commerce-gebruikersnaam en -wachtwoord. Admin-gebruikers moeten hun Commerce Admin-gegevens (gebruikersnaam en wachtwoord) en 2FA-gegevens opslaan voordat ze deze integratie kunnen inschakelen.

Voor bepaalde back-endcomponenten die bij gebruikersverificatie zijn betrokken, is nog steeds een wachtwoord vereist dat niet gelijk is aan null. Om aan deze vereiste te voldoen, maakt Commerce willekeurige wachtwoorden voor nieuwe beheerders in de tabel `admin_user` .

Gebruikersaccounts en rolmachtigingen voor de Commerce-toepassing worden nog steeds beheerd via Commerce Admin.


## Web API-token genereren met IMS-referenties

Commerce Admin API&#39;s worden beïnvloed wanneer Admin-verificatie met Adobe IMS is ingeschakeld in een Commerce-instantie. Admin-gebruikers kunnen de gegevens die door het Commerce-exemplaar worden verstrekt, niet meer gebruiken. Dit zijn de gegevens die vereist zijn om u aan te melden bij Admin en om toegangstokens te verkrijgen waarmee services aanvragen kunnen indienen bij de API&#39;s van Admin REST en SOAP.

Nadat de integratie van Adobe IMS wordt toegelaten, moeten de admin gebruikers [&#x200B; de tokens van IMS van Adobe &#x200B;](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) voor Adobe Commerce API gebruiken eindpunten die authentificatie vereisen. De oplossingen van de cliënt verkrijgen dynamisch de tokens voor Web API gebruik. Dit verificatiemechanisme is ingeschakeld voor REST- en SOAP Web API-gebieden als onderdeel van het configureren van deze integratie.

Zie [&#x200B; op token-gebaseerde authentificatie &#x200B;](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) voor een overzicht van hoe het Web APIs de toegangstokens van Commerce, met inbegrip van IMS toegangstokens gebruikt.

## Commerce-sessiebeheer en Adobe IMS-toegangstokens

Toegangstokens bevatten zowel gebruikersgegevens als aanmeldingssessiegegevens. Nadat een gebruiker is geverifieerd en een sessie is gestart, worden de volgende twee variabelen aan de gebruikerssessie toegevoegd:

`token_last_check_time`. Hiermee wordt de huidige tijd aangegeven en wordt deze gebruikt door de `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` -plug-in.

`adobe_access_token` — Identificeert de `ACCESS_TOKEN` -waarde die tijdens de autorisatie is ontvangen.

De `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` -insteekmodule controleert of de `token_last_check_time` tien minuten geleden is bijgewerkt. Als de `token_last_check_time` tien minuten geleden is gecontroleerd, wordt in de verificatieworkflow een API-aanroep naar IMS uitgevoerd om het toegangstoken te valideren en gaat de sessie verder. Als het toegangstoken geldig is, dan wordt de `token_last_check_time` waarde bijgewerkt aan de huidige tijd. Als het token niet geldig is, wordt de sessie beëindigd.

## Belangrijke bestanden

`adminAdobeIms` - Biedt een implementatie van de aanmeldingsgegevens voor Admin op basis van de module `AdobeImsApi` .

`admin_adobe_ims_webapi` - Hiermee wordt een record bijgehouden met alle gevalideerde toegangstokens. Wanneer een token wordt gevalideerd of ongeldig wordt gemaakt, blijft een record van de status ervan in deze tabel behouden.

`adobeIms` - Implementeert alle bedrijfslogica die gerelateerd is aan integratie met Adobe IMS (zodat incompatibiliteiten met oudere versies worden voorkomen).

`adobeImsApi` - Declareert de interfaces die integratie met Adobe IMS steunen.

`adminadobe-ims.log` - Foutlogbestand.

## Integratie inschakelen

Het Adobe IMS-pakket voor metagegevens is geïnstalleerd met Adobe Commerce 2.4.5 en hoger, maar moet zijn geconfigureerd voor gebruik. Het breidt de `AdobeIms` module uit om de module te steunen die authentificatielogica (`AdminAdobeIms`) toelaat.

Voor meer informatie over het toelaten van de integratie, zie [&#x200B; de Integratie van Admin van Commerce met Adobe IMS &#x200B;](./adobe-ims-config.md) vormen.
