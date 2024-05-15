---
title: Uitbreidingen van Adobe
description: Informatie bekijken over extensies voor Adobe Commerce en Magento Open Source die door de Adobe zijn uitgebracht.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Uitbreidingen van Adobe

Dit onderwerp verstrekt informatie over uitbreidingen voor Adobe Commerce en Magento Open Source die door Adobe worden vrijgegeven. Met extensies voegt u functies, functionaliteit, services en integratie toe aan Admin en Store. Sommige van deze verlengingen worden ontwikkeld door middel van communautaire bijdragen van de Magento Open Source. Sommige extensies moeten apart worden geïnstalleerd, andere worden standaard geïnstalleerd.

## Geïnstalleerde extensies

Sommige extensies worden automatisch geïnstalleerd met Adobe Commerce of Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) biedt uitgebreid beheer van voorraden en verzendingen op één of meerdere locaties en verkoopkanalen met gelijktijdige algoritmen voor afhandelingsbescherming en -matching. Houd uw voorraad bij, geef klanten nauwkeurige verkoopcijfers en verzend objecten volgens de aanbevelingen of handmatige selecties om uw hele voorraad te beheren. Configureer de beheerinstellingen globaal, per bron en per product.

>[!NOTE]
>
>Deze extensie is ontwikkeld als onderdeel van de [[!DNL Inventory Management]](https://github.com/magento/inventory) (vroeger MSI) project door het Communautaire Programma van de Techniek.

[!DNL Inventory Management] wordt geïnstalleerd met alle functies standaard ingeschakeld. Er zijn geen extra stappen nodig om deze voorraadfuncties in te schakelen. Voor meer informatie over de [!DNL Inventory Management] mogelijkheden, zie [[!DNL Inventory Management] Handboek](../inventory-management/guide-overview.md).

### Braintree

PayPal en Gene Commerce hebben samen de officiële Braintree-extensie voor Commerce 2.4.x-winkels ontwikkeld. De updates zijn uitgerust met een verbeterde afrekenervaring die is ontworpen om de conversie te stimuleren en bevatten PayLater-opties die automatisch relevante PayLater-berichten en -knoppen weergeven aan consumenten tijdens het winkelen en tijdens het afrekenen.

Deze extensie is standaard geïnstalleerd, maar vereist een [Braintree](https://www.braintreepayments.com/) en configuratie in Admin om voor uw opslag worden toegelaten. Als u wilt bepalen welke kosten van toepassing zijn wanneer u Braintree gebruikt om uw transacties te verwerken, controleert u de [Prijsbepaling Braintree](https://www.braintreepayments.com/braintree-pricing).

Voor informatie over de configuratie van de Braintree in Admin, zie [Braintree](../stores-purchase/braintree.md) in het _Handleiding voor verkoop- en aankoopervaring_.

### Google reCAPTCHA

Google reCAPTCHA biedt een hoger beveiligingsniveau voor zowel de storefront als de Admin-gebruikersinterface dan beschikbaar is met de standaard CAPTCHA en biedt u de mogelijkheid om:

- Verifieer wanneer de klanten rekeningen creëren, wachtwoorden terugwinnen, login aan hun rekeningen, of uw bedrijf contacteren.
- Verbeter de beveiliging wanneer Admin-gebruikers zich aanmelden.

Het vermindert potentiële gebruikersfout wanneer het ingaan van een code Captcha en moedigt wortelomzetting aan zonder hindernissen tijdens het afrekenen toe te voegen. [reCAPTCHA inschakelen en configureren](../systems/security-google-recaptcha.md) het gebruik van onzichtbare of interactieve controles om veilige toegang tot [!DNL Commerce] Admin and storefront.

### Twee-factor authentificatie

De [!DNL Commerce] Admin verleent al toegang tot uw opslag, orden, en klantengegevens. [Twee-factor authentificatie](../systems/security-two-factor-authentication.md) (2FA of TFA) verbetert de veiligheid door extra authentificatie te vereisen, voorbij de standaard login naam en het wachtwoord, om tot [!DNL Commerce] Beheer vanaf alle apparaten. De extensie ondersteunt meerdere authenticators, waaronder Google Authenticator, Authy. [!DNL Duo]en U2F-toetsen. Deze verificatie is alleen van toepassing op Admin-gebruikers. Het is niet beschikbaar voor klantenaccounts van winkels.

Deze functies zijn standaard ingeschakeld. Elke Admin-gebruiker moet een van de ondersteunde verificateurs installeren en configureren.

>[!NOTE]
>
>Adobe Commerce-winkels die Adobe Identity Management Services (IMS)-verificatie voor de Admin hebben ingeschakeld, hebben native Commerce 2FA uitgeschakeld. Gebruikers die zich bij de beheerder hebben aangemeld met hun Adobe hoeven niet opnieuw te verifiëren voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [Adobe Identity Management Service (IMS) - Overzicht van integratie](./adobe-ims-integration-overview.md).

## Toe te voegen extensies

De [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) is de globale bron van de eCommerce voor toepassingen en de diensten die uitbreiden [!DNL Commerce] oplossingen met krachtige nieuwe functies en functionaliteit. Adobe geeft verschillende extensies vrij via de [!DNL Marketplace] die kunnen worden geïnstalleerd en geconfigureerd in uw Adobe Commerce- of Magento Open Source-winkel voor verbeterde integratie en mogelijkheden.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Alleen Adobe Commerce

De [!DNL Live Search] Als u de extensie toepast, wordt uw winkel verbonden met de service Live zoeken. Dit is een gratis zoekplatform van Adobe Commerce waarmee verkopers hun klanten naadloos een AI-zoekervaring kunnen bieden. Dankzij de kunstmatige intelligentie van de Adobe helpt Adobe Sensei Intelligent Faceting handelaren meer te doen met minder door het handmatige werk rondom facettering/filteren te verwijderen.

Zie de [Handboek voor live zoeken](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) voor meer informatie .

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Alleen Adobe Commerce

De [!DNL Product Recommendations] De uitbreiding verbindt uw opslag aan de dienst van het Product Recommendations - een krachtig marketing hulpmiddel dat u kunt gebruiken om omzettingen, opbrengst, en betrokkenheid te verhogen. [!DNL Product Recommendations] is gebouwd door Adobe Commerce en wordt aangedreven door de gevechtsteste kunstmatige intelligentie, Adobe Sensei, zodat u op een betrouwbare manier betrokkenheid en conversie kunt stimuleren. Met deze functie verwijdert u het handmatige werk dat nodig is om relevante productaanbevelingen aan elke winkel te doen.

Zie de [[!DNL Product Recommendations] Handboek](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) voor meer informatie .

### [!DNL Catalog Service]

De [!DNL Catalog Service] biedt u de mogelijkheid om klanten een geoptimaliseerde productervaring te bieden en tegelijk de prestaties te verhogen, de schaalbaarheid te verbeteren en de conversies te verhogen. Zie de [[!DNL Catalog Service] Handboek](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) voor meer informatie .

### [!DNL Payment Services]

[!DNL Payment services] voor Adobe Commerce en Magento Open Source is een volledig geïntegreerde betalingsoplossing die het betalingsbeheerproces vereenvoudigt en uw klanten de mogelijkheid biedt om hun geld te betalen. Zorg ervoor dat alle betalings- en transactiegegevens binnen de Adobe Commerce Admin op een veilige manier met elkaar in overeenstemming worden gebracht, zodat u opdrachten en betalingen op één plaats kunt beheren en een naadloze afhandeling kunt uitvoeren. Zie de [[!DNL Payment Services] Handboek](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) voor meer informatie .

### [!DNL Store Fulfillment]

Met de functie Opslagtegoeden voor Adobe Commerce en Magento Open Source kan een superieur online aankopen, de klant van BOPIS (Ophalen in Store) ophalen en de werknemersproductiviteit maximaliseren door een uitgebreide uitvoeringsworkflow te bieden die via een mobiel apparaat wordt ingeschakeld. Zie de [[!DNL Store Fulfillment] Handboek](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) voor meer informatie .

### [!DNL Amazon Sales Channel]

De [!DNL Amazon Sales Channel] voor Adobe Commerce: hiermee kunt u de database met aanbiedingen in Amazon Seller Central integreren met uw [!DNL Commerce] productcatalogus en beheer je Amazon-aanbiedingen en -verkopen in Commerce Admin. Zie de [[!DNL Amazon Sales] Handboek voor handleiding](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) voor meer informatie .

### [!DNL Channel Manager]

[!DNL Channel Manager] biedt u de mogelijkheid om uw verkoop te verhogen, nieuwe klanten te bereiken, bewerkingen te stroomlijnen en tijd te besparen door een Adobe Commerce- of Magento Open Source-productcatalogus te integreren met de Marketplace van Walmart. Nadat u de extensie hebt geïnstalleerd en geconfigureerd, kunnen uw medewerkers aanbiedingen, inventarisaties, bestellingen, geretourneerde bedragen en terugbetalingen van de website van Walmart Marketplace probleemloos beheren [!DNL Commerce Admin]. Zie de [[!DNL Channel Manager] Handboek](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) voor meer informatie .
