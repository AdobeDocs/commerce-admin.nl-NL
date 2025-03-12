---
title: Extensies van Adobe
description: Bekijk de informatie over extensies voor Adobe Commerce en Magento Open Source die door Adobe zijn uitgebracht.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Extensies van Adobe

Dit onderwerp bevat informatie over extensies voor Adobe Commerce en Magento Open Source die door Adobe worden uitgebracht. Met extensies voegt u functies, functionaliteit, services en integratie toe aan Admin en Store. Sommige van deze verlengingen worden ontwikkeld met behulp van de bijdragen van de Gemeenschap van Magento Open Source. Sommige extensies moeten apart worden geïnstalleerd, andere worden standaard geïnstalleerd.

## Geïnstalleerde extensies

Sommige extensies worden automatisch geïnstalleerd met Adobe Commerce of Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) biedt verbeterd beheer van voorraden en verzendingen op één of meerdere locaties en verkoopkanalen met gelijktijdige algoritmen voor afhandelingsbeveiliging en -matching. Houd uw voorraad bij, geef klanten nauwkeurige verkoopcijfers en verzend objecten volgens de aanbevelingen of handmatige selecties om uw hele voorraad te beheren. Configureer de beheerinstellingen globaal, per bron en per product.

>[!NOTE]
>
>Deze uitbreiding werd ontwikkeld als deel van het [[!DNL Inventory Management] ](https://github.com/magento/inventory) (vroeger MSI) project door het Communautaire Programma van de Techniek.

[!DNL Inventory Management] wordt geïnstalleerd met alle functies die standaard zijn ingeschakeld. Er zijn geen extra stappen nodig om deze voorraadfuncties in te schakelen. Voor details over de [!DNL Inventory Management] mogelijkheden, zie de [[!DNL Inventory Management]  Gids van de Gebruiker ](../inventory-management/guide-overview.md).

### Braintree

PayPal en Gene Commerce hebben samen de officiële Braintree-extensie voor Commerce 2.4.x-winkels ontwikkeld. De updates zijn uitgerust met een verbeterde afrekenervaring die is ontworpen om de conversie te stimuleren en bevatten PayLater-opties die automatisch relevante PayLater-berichten en -knoppen weergeven aan consumenten tijdens het winkelen en tijdens het afrekenen.

Deze uitbreiding wordt geïnstalleerd door gebrek, maar vereist de a [ rekening van Braintree ](https://www.braintreepayments.com/) en configuratie in Admin om voor uw opslag worden toegelaten. Om de kosten te bepalen die van toepassing zijn wanneer het gebruiken van Braintree om uw transacties te verwerken, controleer de [ prijs van Braintree ](https://www.braintreepayments.com/braintree-pricing).

Voor informatie over de configuratie van Braintree in Admin, zie het [ Braintree ](../stores-purchase/braintree.md) onderwerp in de _Gids van de Ervaring van de Verkoop en van de Aankoop_.

### Google reCAPTCHA

Google reCAPTCHA biedt een hoger beveiligingsniveau voor zowel de storefront als de Admin-gebruikersinterface dan beschikbaar is met de standaard CAPTCHA en biedt u de mogelijkheid om:

- Verifieer wanneer de klanten rekeningen creëren, wachtwoorden terugwinnen, login aan hun rekeningen, of uw bedrijf contacteren.
- Verbeter de beveiliging wanneer Admin-gebruikers zich aanmelden.

Het vermindert potentiële gebruikersfout wanneer het ingaan van een code Captcha en moedigt wortelomzetting aan zonder hindernissen tijdens het afrekenen toe te voegen. [ laat en vormt reCAPTCHA ](../systems/security-google-recaptcha.md) toe gebruikend onzichtbare of interactieve controles om veilige toegang tot [!DNL Commerce] Admin en storefront te verbeteren.

### Twee-factor authentificatie

De [!DNL Commerce] Admin verleent al toegang tot uw opslag, orden, en klantengegevens. [ two-factor authentificatie ](../systems/security-two-factor-authentication.md) (2FA of TFA) verbetert veiligheid door extra authentificatie, voorbij de standaard login naam en het wachtwoord te vereisen, om tot [!DNL Commerce] Admin van alle apparaten toegang te hebben. De extensie ondersteunt meerdere authenticators, waaronder Google Authenticator, Authy, [!DNL Duo] en U2F. Deze verificatie is alleen van toepassing op Admin-gebruikers. Het is niet beschikbaar voor klantenaccounts van winkels.

Deze functies zijn standaard ingeschakeld. Elke Admin-gebruiker moet een van de ondersteunde verificateurs installeren en configureren.

>[!NOTE]
>
>Adobe Commerce-winkels die Adobe Identity Management Services (IMS)-verificatie voor de Admin hebben ingeschakeld, hebben native Commerce 2FA uitgeschakeld. Gebruikers die zich bij de beheerder hebben aangemeld met hun Adobe-gebruikersgegevens hoeven niet opnieuw te verifiëren voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [ het Overzicht van de Integratie van Adobe Identity Management van de Dienst (IMS) ](./adobe-ims-integration-overview.md).

## Toe te voegen extensies

[[!DNL Commerce Marketplace] ](https://marketplace.magento.com/) is de globale bron van de eCommerce voor toepassingen en de diensten die [!DNL Commerce] oplossingen met krachtige nieuwe eigenschappen en functionaliteit uitbreiden. Adobe geeft via [!DNL Marketplace] verschillende extensies vrij die kunnen worden geïnstalleerd en geconfigureerd in uw Adobe Commerce- of Magento Open Source-winkel voor verbeterde integratie en mogelijkheden.

### [!DNL Live Search]

![ Adobe Commerce ](../assets/adobe-logo.svg) slechts Adobe Commerce

De extensie [!DNL Live Search] verbindt uw winkel met de service Live zoeken. Dit is een gratis zoekplatform van Adobe Commerce dat verkopers naadloos de mogelijkheid biedt om klanten een AI-zoekervaring te bieden. Adobe Sensei, Intelligent Faceting, dat is gebouwd met de kunstmatige intelligentie van Adobe, helpt handelaren meer te doen met minder door het handmatige werk rondom facettering/filteren te verwijderen.

Zie de [ Levende Gids van de Gebruiker van het Onderzoek ](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html) voor meer informatie.

### [!DNL Product Recommendations]

![ Adobe Commerce ](../assets/adobe-logo.svg) slechts Adobe Commerce

De extensie [!DNL Product Recommendations] verbindt uw winkel met de service Productaanbevelingen, een krachtig marketinginstrument waarmee u conversies, inkomsten en betrokkenheid kunt verhogen. [!DNL Product Recommendations] is gebouwd door Adobe Commerce en wordt aangedreven door de in de strijd geteste kunstmatige intelligentie, Adobe Sensei, zodat u op een betrouwbare manier betrokkenheid en conversie kunt stimuleren. Met deze functie verwijdert u het handmatige werk dat nodig is om relevante productaanbevelingen aan elke winkel te doen.

Zie de [[!DNL Product Recommendations]  Gids van de Gebruiker ](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en) voor meer informatie.

### [!DNL Catalog Service]

Met [!DNL Catalog Service] kunt u klanten een geoptimaliseerde productervaring bieden en tegelijk de prestaties verhogen, de schaalbaarheid verbeteren en conversies verhogen. Zie de [[!DNL Catalog Service]  Gids van de Gebruiker ](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html) voor meer informatie.

### [!DNL Payment Services]

[!DNL Payment services] voor Adobe Commerce en Magento Open Source is een volledig geïntegreerde betalingsoplossing die het beheer van betalingen vereenvoudigt en uw klanten de mogelijkheid biedt om hun manier van betalen te betalen. Zorg ervoor dat alle betalings- en transactiegegevens binnen de Adobe Commerce Admin op een veilige manier met elkaar in overeenstemming worden gebracht, zodat u opdrachten en betalingen op één plaats kunt beheren en een naadloze afhandeling kunt uitvoeren. Zie de [[!DNL Payment Services]  Gids van de Gebruiker ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html) voor meer informatie.

### [!DNL Store Fulfillment]

Met Store Fulfillment voor Adobe Commerce en Magento Open Source kan een superieur online kopen, de klant van BOPIS (Ophalen in Store) beleven en de productiviteit van de werknemers maximaliseren door een uitgebreide uitvoeringsworkflow te bieden die via een mobiel apparaat wordt ingeschakeld. Zie de [[!DNL Store Fulfillment]  Gids van de Gebruiker ](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html) voor meer informatie.

### [!DNL Amazon Sales Channel]

Met [!DNL Amazon Sales Channel] voor Adobe Commerce kunt u uw Amazon Seller Central-aanbiedingsdatabase integreren met uw productcatalogus van [!DNL Commerce] en uw Amazon-aanbiedingen en -verkopen beheren in Commerce Admin. Zie de [[!DNL Amazon Sales]  Gids van de Gebruiker van de Gids ](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) voor meer informatie.

### [!DNL Channel Manager]

Met [!DNL Channel Manager] kunt u de verkoop verhogen, nieuwe klanten bereiken, bewerkingen stroomlijnen en tijd besparen door een Adobe Commerce- of Magento Open Source-productcatalogus te integreren met de Walmart Marketplace. Nadat u de extensie hebt geïnstalleerd en geconfigureerd, kunnen uw medewerkers aanbiedingen, inventarisaties, bestellingen, retourneert en terugbetalingen van de [!DNL Commerce Admin] probleemloos beheren. Zie de [[!DNL Channel Manager]  Gids van de Gebruiker ](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) voor meer informatie.
