---
title: '[!DNL Adobe Commerce Marketplace]'
description: Meer informatie over de [!DNL Commerce Marketplace], die verkopers een gekromde selectie van oplossingen aanbiedt, en gekwalificeerde ontwikkelaars de hulpmiddelen, het platform, en de eerste plaats verstrekt om een het gedijen zaken te bouwen.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 02e7c71fc47e6850371bfbdc1be50f65ec8015e9
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] is de toepassingsopslag die verkopers een gebogen selectie van oplossingen aanbiedt, en gekwalificeerde ontwikkelaars de hulpmiddelen, het platform, en de primaire plaats verstrekt om een het gedijen zaken te bouwen. [!DNL Commerce Marketplace] biedt een selectie van extensies die gratis beschikbaar zijn en andere extensies die te koop zijn. Aankopen kunnen per creditcard worden betaald of [PayPal][2].

Alle extensies die beschikbaar zijn op [!DNL Commerce Marketplace] hebben een uitgebreide revisie goedgekeurd. De [Extension Quality Program][3] (MKN) [!DNL Commerce] deskundigheid, ontwikkelings richtlijnen, en controlehulpmiddelen om ervoor te zorgen dat alle uitbreidingen op Commerce Marketplace aan coderingsnormen en beste praktijken voldoen. Het revisieproces omvat zowel een automatische controle als een handmatige kwaliteitscontrole. Tijdens het proces worden de structuur en de code van elke extensie onderzocht en getest op tekenen van besmetting met virussen/malware, en op aanwijzingen voor plagiaat. De evaluatie omvat een grondige technische controle en een grondige controle van de hygiëne door een [!DNL Commerce] engineer, met nadruk op documentatie, coderingsstructuur, prestaties, schaalbaarheid, beveiliging en compatibiliteit met de [!DNL Commerce] kern.

Hoewel u extensies kunt kopen van andere bronnen, zijn alleen de extensies beschikbaar op [!DNL Commerce Marketplace] worden gecontroleerd door middel van uitgebreide technische en marketingevaluatie in het kader van het Extension Quality Programme.

## App-bronnen

Ontwikkelaars hebben van oudsher PHP gebruikt om &#39;in-process&#39; extensies te maken die functies, functionaliteit, services en integratie toevoegen aan Adobe Commerce. Door toepassingen te maken die niet langer procesextensies maar uitbreidbaar zijn, kunt u compatibiliteitsproblemen voorkomen.

De volgende bronnen bieden een beginpunt voor nieuwe gebruikers om vertrouwd te raken met apps:

### Commerce-bronnen

- [I/O-gebeurtenissen instellen voor Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Gebeurtenissen configureren voor Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [De SDK van de beheerdersinterface instellen](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Een extensie converteren naar een app](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Bronnen voor App Builder

- [Overzicht van Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [API-net instellen voor Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [App Builder-apps gebruiken](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD voor App Builder-apps](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Aan de slag met App Builder/Developer Console
   - [Aan de slag met App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Projecten en werkruimten](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] geloofsbrieven

Voordat u een extensie kunt installeren die u hebt aangeschaft van [!DNL Commerce Marketplace], meld u aan bij uw [!DNL Commerce] account en controleer of u een actieve toegangssleutel hebt. U kunt zich aanmelden bij uw [!DNL Commerce] account van de header van [[!DNL Marketplace]][1] of [Magento.com][6].

Uw toegangssleutel is een reeks openbare en privé sleutels die wordt gebruikt om uw [!DNL Commerce] installeren met uw [!DNL Commerce] account en verifieer uw gegevens. Nadat uw account is gesynchroniseerd, moet u telkens uw persoonlijke sleutel invoeren wanneer u een extensie of module installeert vanuit de Commerce Marketplace of wanneer u een upgrade uitvoert van uw account [!DNL Commerce] installatie.

U kunt meerdere toegangstoetsen maken voor verschillende doeleinden en deze naar wens in- of uitschakelen. U moet echter dezelfde toegangssleutel gebruiken die is gebruikt voor de installatie van de [!DNL Commerce] software. U kunt bijvoorbeeld geen toegangssleutel voor Magento Open Sourcen gebruiken om Adobe Commerce bij te werken of bij te werken, of omgekeerd. U kunt ook geen toegangstoets gebruiken die bij een andere gebruiker hoort of die afkomstig is van een [gedeelde account](commerce-account-share.md).

### Een toegangstoets maken

1. Aanmelden bij uw [!DNL Commerce] account.

1. Op de _[!UICONTROL My Account]_pagina, kiest u de **[!UICONTROL Marketplace]**tab.

1. Klik in de rechterbovenhoek naast uw naam op de pijl omlaag en kies **[!UICONTROL My Profile]**.

   ![Uw [!DNL Marketplace] profiel](./assets/marketplace-profile.png){width="600"}

1. Op de _[!UICONTROL Marketplace]_tab onder_[!UICONTROL My Products]_, klikt u op **[!UICONTROL Access Keys]** en voer vervolgens een van de volgende twee handelingen uit:

   - Controleer of je al een set toegangstoetsen hebt voor je aankopen op Marketplace. U kunt meerdere sets toegangstoetsen maken voor verschillende doeleinden.

   ![Toegangssleutels](./assets/access-keys.png){width="600"}

   - Klik op **[!UICONTROL Create a New Access Key]**. Voer een naam in voor het nieuwe sleutelpaar en klik op **[!UICONTROL OK]**. Geldige tekens zijn hoofdletters en kleine letters en koppeltekens in plaats van spaties.

1. Klik op **[!UICONTROL OK]**.

   De nieuwe toegangssleutel wordt toegelaten en verschijnt in de lijst.

   Let op: _Kopiëren_ koppeling na elke openbare en persoonlijke sleutel. In de volgende stap kopieert en plakt u deze waarden om de winkel te synchroniseren met de Commerce Marketplace.

## Installatieproces

>[!IMPORTANT]
>
>Beginnend met Adobe Commerce en Magento Open Source 2.4.0, wordt de Tovenaar van de Opstelling van het Web verwijderd, en u moet de bevellijn gebruiken aan [installeren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) of [upgrade](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) uw exemplaar. Deze eis omvat ook [modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) en [extensions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Het installatieproces voor [!DNL Marketplace] aankopen zijn anders voor _op locatie_ installaties van Commerce dan voor installaties die worden gehost op [de Adobe Cloud Architecture][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Ondersteuning

Als u hulp bij het installeren of met het gebruiken van een uitbreiding nodig hebt, kijk eerst in de documentatie die de uitbreiding vergezelt. Als u het antwoord op uw vraag niet kunt vinden, gebruikt u de contactgegevens in de lijst met extensies om rechtstreeks contact op te nemen met de ontwikkelaar. Als wat u op Marketplace koopt niet aan uw behoeften voldoet, kunt u [om terugbetaling verzoeken](#refund-requests) binnen 25 dagen na de datum van aankoop. De Adobe herziet alle terugbetalingsverzoeken en geeft (indien goedgekeurd) de juiste terugbetaling uit. Raadpleeg voor ondersteuning van problemen met betrekking tot Commerce Marketplace de [[!DNL Marketplace] Help Center][5].

### Afhandelingsproblemen

De adresvelden in uw accountprofiel moeten worden ingevuld voor verificatiedoeleinden in het aankoopsysteem voor Markttoegang.

1. Voeg de adresvelden toe aan uw Marketplace-accountprofiel.
1. Sla het bijgewerkte profiel op.
1. Ga door met het afrekenen.

### Aanmeldingsproblemen

Aanmeldingsproblemen hebben doorgaans betrekking op een onjuiste combinatie van uw MAGEID en e-mailadres in de accountdatabase. Neem contact op met de ondersteuning van de marktplaats.

>[!INFO]
>
>Aankopen van apps en extensies kunnen niet worden uitgevoerd [overgedragen](#purchase-transfers) naar een nieuwe account.

### Bronvragen openen

Het marktondersteuningsteam verhelpt problemen met betrekking tot het [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) en [commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/) alleen sites. Gelieve vragen over de Magento Open Source aan de [Forum van de Gemeenschap](https://community.magento.com/) of [contact opnemen met een partner](https://business.adobe.com/products/magento/partners.html) die hulp kunnen bieden bij Magento Open Source.

### Terugbetalingsaanvragen

Als u een terugbetaling wilt aanvragen voor een aankoop op een Marketplace, meldt u zich aan bij uw account en voert u de volgende stappen uit:

1. Klikken [!UICONTROL **Mijn profiel**] > [!UICONTROL **Aankoopgeschiedenis**].
1. Zoek de aankoop en klik op [!UICONTROL **Terugbetaling aanvragen**].
1. Vul het formulier voor de terugbetalingsopdracht in.

Marketplace Support vraagt om informatie nadat het verzoek om terugbetaling is gegenereerd. De terugbetalingsoptie is 25 dagen na de aankoopdatum beschikbaar. Zie de [Overeenkomst voor klant van Marktplaats](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Facturen bestellen

U kunt facturen voor bestellingen downloaden van de [!UICONTROL **Aankoopgeschiedenis**] in uw Marketplace account. De factuur levert de BTW of het adres van de verkoper niet, omdat dit momenteel geen marktverplichting is.

Als u een bestelfactuur wilt downloaden voor een aankoop in een handelsplaats, meldt u zich aan bij uw Marketplace-account en voert u de volgende stappen uit:

1. Klikken [!UICONTROL **Mijn profiel**] > [!UICONTROL **Aankoopgeschiedenis**].
1. Zoek de aankoop.
1. Klik op het printerpictogram in de rechterbovenhoek van de volgorde.

### Inkoopoverdrachten

Het marktondersteuningsteam heeft niet de mogelijkheid om aankopen naar een andere account over te dragen. U moet alle apps en extensies aanschaffen op de primaire Commerce-account om installatie- en implementatieproblemen te voorkomen. Adobe Commerce heeft recht op één unieke identificatiecode. Aangezien Composer wordt gebruikt voor de installatie, wordt slechts één set [toegangstoets](#create-an-access-key) kan worden gebruikt. De enige beschikbare oplossing is: [om terugbetaling verzoeken](#refund-requests) op de aankooprekening van de Marketplace (indien toegestaan door het terugbetalingsbeleid van Adobe Commerce).

U kunt [delen](commerce-account-share.md) een Commerce-exemplaar via de primaire account. Gedeelde toegang verleent speciale toestemmingen aan een ondergeschikte rekening van een primaire rekening. Het gedeelde toegangspunt wordt gegenereerd van de primaire account. De primaire account kan de Commerce-account, de hoofdzakelijke account of een account zijn die binnen een organisatie wordt gedeeld.

Deze speciale machtigingen verlenen Adobe Commerce hetzelfde toegangsniveau als de primaire rechten, maar ze worden niet overgedragen naar Adobe Commerce Marketplace of Developer Portal. Dit betekent dat het kopen van een extensie van een ondergeschikte rekening op de Marketplace niet kan worden gedeeld met de primaire account. Gedeelde toegang is een eenrichtingsweg (primair account dat ondergeschikt is). Het werkt niet wanneer een ondergeschikte account probeert terug te delen naar de primaire account.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
