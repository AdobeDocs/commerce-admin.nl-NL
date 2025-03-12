---
title: Maak aansprekende, persoonlijke ervaringen op schaal
description: Leer welke eigenschappen in Adobe  [!DNL Commerce]  u toestaan om een gepersonaliseerde ervaring voor uw kopers tot stand te brengen.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Maak aansprekende, persoonlijke ervaringen op schaal

Adobe [!DNL Commerce] biedt u een krachtige toolkit waarmee u elke klant een persoonlijk tintje kunt geven en waarmee u uw betrokkenheid, conversie en omzet van klanten kunt verhogen.

In dit artikel leert u:

- Wat is personalisatie?
- Welke gegevens heb ik nodig om personalisatie te bereiken?
- Hoe ontgrendelt Adobe [!DNL Commerce] personalisatie?
- Beschikbare gebruiksgevallen voor personalisatie

## Wat is personalisatie?

Personalization betekent dat aspecten van de koopervaring van elke klant worden aangepast aan hun unieke behoeften, context en voorkeuren. Personalization is niet beperkt tot de inhoud van de site of het aanbevelen van best-fit producten, maar omvat alle touchpoints over de reis van de klant, waaronder:

- **Campagnes en Mededelingen** - leverend relevant en verenigbaar overseinen via campagnes en mededelingen
- **Ontdekking van het Product** - tonend de juiste producten aan de juiste klanten op enkel de juiste momenten
- **Bevorderingen en Aanbiedingen** - het richten van bevorderingen en aanbiedingen om elke klant te drijven om te zetten
- **Ervaringen van de Inhoud** - het Kentelen van plaatsinhoud om hyper-relevant voor elke klant en hun reis te voelen

![ Types van Personalization ](assets/types-personalization.png){width="700" zoomable="yes"}

Terwijl deze soorten gepersonaliseerde ervaringen voor een kleine ondergroep van klanten haalbaar kunnen schijnen, die aan schaal voor duizenden of miljoenen klanten over elk aanraakpunt en kanaal aanpassen, kunnen allen in real time zich onmogelijk voelen. In de volgende secties leert u hoe Adobe [!DNL Commerce] en Adobe Experience Cloud kunnen helpen.

## Welke gegevens heb ik nodig om personalisatie te bereiken?

De efficiënte verpersoonlijking vereist context of signalen die informatie over klanten verstrekken die dan kunnen worden gebruikt om hun ervaring te wijzigen. De volgende tabel bevat de verschillende gegevenstypen en de rol die Adobe [!DNL Commerce] speelt bij het ondersteunen van het verzamelen en activeren van die gegevens.

| Gegevenstypen | Storefront-gegevens (gedragsgebeurtenissen) | Back Office-gegevens (server-side gebeurtenissen) | Klantprofiel en segmentgegevens |
|---|---|---|---|
| **Definitie** | Klik of acties die klanten op uw site uitvoeren. | Informatie over de levenscyclus en details van elke bestelling (verleden en huidig). | Wie zijn de kopers en voor welke segmenten komen ze in aanmerking? |
| **Gebeurtenissen die door Adobe Commerce** worden gevangen | [ pageView ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#pageview) <br>[ productPageView ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events) <br>[ searchRequestSent ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchrequestsent) <br>[ searchResponseReceived ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived) <br>[ addToCart ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtocart) <br>[ openCart ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#opencart) <br>[ signIn ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signin) <br>[ signOut ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signout) <br>[ ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#startcheckout) startCheckout <br>[ completeCheckout ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#completecheckout) <br>[ createRequisitionList ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist) <br>[ addToRequisitionList ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist) <br>[ removeFromRequisitionList ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **de status van de Orde**:<br>[ orderPlaced ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced) <br>[ orderItemsReturnInitiated ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated) <br>[ orderItemsShipped ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped) <br>[ orderCanceled ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled) <br>[**geschiedenis van de Orde** ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data):<br> - SKU, Naam, Kwantiteit, Korting <br> - Product Categorie <br> - het Bedrag van de Betaling, Type, Valuta <br> - Verzendmethode en Bedrag <br> - teruggegeven identiteitskaart, Bedrag, Valuta <br> - Terugkeer Reden, Voorwaarde, Resolutie <br> - Adres <br> - E-mail | [**het verslag van het Profiel** ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-profilerecord): (Naam, Geslacht, Adres, de Status van de Loyalty, Aantal van de Telefoon, E-mailAdres) <br>**de status van de Rekening**:<br>[ accountCreated ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated) <br>[ accountUpdated ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated) <br>[ accountDelette ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Met al deze rijke, eersteklas [!DNL Commerce] gegevens bent u klaar om de ervaring van elke klant te richten en aan te passen. In de volgende sectie leert u hoe u met [!DNL Commerce] en Adobe Experience Cloud persoonlijke ervaringen en gebruiksscenario&#39;s kunt maken die u kunt activeren.

## Hoe versterkt Adobe [!DNL Commerce] personalisatie?

Met Adobe [!DNL Commerce] Data Sharing kunt u de gegevenstypen in de vorige tabel verzamelen en delen met andere Adobe Experience Cloud-producten, zodat uniforme profielen en doelgroepen van klanten, gepersonaliseerde campagnes en rijke analyses en inzichten van gebruikers van kracht worden.

![ hoe de gegevens aan de rand van Experience Platform ](assets/commerce-edge.png){width="700" zoomable="yes"} stromen

Adobe [!DNL Commerce] Data Sharing bevat twee belangrijke componenten:

1. [ Verbinding van Gegevens ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview): De opslagruimte van het aandeel, achterkantoor, en gegevens van het klantenprofiel van Adobe [!DNL Commerce] aan het de randnetwerk van Adobe Experience Platform voor gebruik over de toepassingen van Adobe Experience Cloud, die omvatten:

   - [ Adobe  [!DNL Real-Time CDP] ](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): De gegevens van de steunen klant van over bronnen (ERP, CRM, POS) in verenigde profielen en creeer op regel-gebaseerde of op AI-Gebaseerde segmenten.
   - [ Adobe  [!DNL Journey Optimizer] ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): De gepersonaliseerde reis in het midden-kanaal van de lancering, met inbegrip van e-mailcampagnes, SMS, dupberichten, en meer.
   - [ Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) en [ Adobe  [!DNL Analytics] ](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): De inzichten van de winst in de klant en de zaken.
   - [ Adobe  [!DNL Target] ](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Test en optimaliseer inhoud, geadviseerde producten, aanbiedingen, navigatie, en meer.

1. [[!DNL Audience Activation] ](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): gebruik [!DNL Real-Time CDP] soorten publiek om dynamische inhoudblokken, promoties en gerelateerde productregels op uw Adobe [!DNL Commerce] -site aan te passen.

### Persoonlijke ervaring met winkelprestaties over elk kanaal, op schaal

Adobe [!DNL Commerce] kan uit voordeel halen van een krachtige opslag, genoemd [ Edge Delivery Services ](https://experienceleague.adobe.com/developer/commerce/storefront/), om gepersonaliseerde ervaringen over al uw kanalen, met AI mogelijkheden bij de kern, en snelheid als stichting te leveren.

Met Edge Delivery Services kunt u:

- **creeerde gepersonaliseerde inhoud**: Op document-gebaseerde het gebruik creatie, inheemse experimentatie met Generatieve AI tekst &amp; beeldvariaties voor het personaliseren van de ervaring bij schaal. Met Assets en Generative AI-inhoud kunt u op grote schaal product- en marketingafbeeldingen maken.

- **produceer variaties**: Staat inhoudsauteurs toe om Generatieve AI te gebruiken om grote volumes van gepersonaliseerde AI-gedreven [ tekstinhoud en beeldvariaties ](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) met Adobe Firefly tot stand te brengen.

- **opstellen via Edge Delivery Services Storefront**: Inhoud op de mogelijkheden van Edge en Commerce die door drop-in componenten worden aangedreven, om op maat gesneden shoppable ervaringen voor uw publiek tot stand te brengen.

- **Commerce en Adobe Experience Manager Assets**: De generatieve verwezenlijking van de het productactiva van AI en variaties bij schaal. Maak, lever en controleer de levering van inhoud via elk kanaal.

![ drop-ins: De Pagina van het Detail van het Product ](assets/drop-in.png){width="700" zoomable="yes"}

### Personalization: aan de slag met systeemeigen Adobe [!DNL Commerce] -functies

Adobe [!DNL Commerce] biedt krachtige personalisatie met de native out-of-the-box mogelijkheden. In de volgende tabel worden de [!DNL Commerce] -functies beschreven die u direct kunt activeren om aan de slag te gaan met uw persoonlijke voorkeur.

| Categorie | Functies |
|---|---|
| Persoonlijke productdetectie | [[!DNL Live Search] ](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview): Personaliseer en optimaliseer onderzoeksresultaten die op het gedrag van een verkoopster onsite worden gebaseerd en affiniteiten met AI-aangedreven onderzoek.<br>[ Intelligente Merchandising van de Categorie ](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/category-merch): AI-gedreven productrangschikking op categoriepagina&#39;s die op het gedrag van een verkoopster onsite acties en affiniteiten worden gebaseerd.{de Aanbevelingen van het 0} Product ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview): AI-Gerichte productaanbevelingen die op verkoopgedrag, tendensen, en affiniteiten worden gebaseerd.<br>[<br>[ Verwante Regels van het Product ](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): Bepaal douaneregels om producten van uw catalogus te tonen om dwars en omhoog-verkopen te drijven. |
| Persoonlijke site-inhoud | [ de Dynamische Blokken van de Inhoud ](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Vertoning gepersonaliseerde inhoudsblokken, bijvoorbeeld, banners, die op klantensegmenten in Adobe Commerce worden gebaseerd. |
| Persoonlijke aanbiedingen en aanbiedingen | [ Regels van de Prijs van de Kar ](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Pas kortingen op punten in het het winkelwagentje toe dat op een reeks voorwaarden, met inbegrip van klantensegmenten in Adobe [!DNL Commerce] wordt gebaseerd. |
| Inzichten en meting |  [!DNL Commerce]  Intelligentie van Adobe [ ](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Begrijp hoe uw verpersoonlijkingsstrategieën in tijd werken en verbeteren. |

## Gebruiksscenario&#39;s voor topverpersoonlijking

Adobe [!DNL Commerce]-klanten gebruiken de mogelijkheid om gegevens uit de verpakking te halen en delen deze naar Adobe Experience Cloud voor verschillende gebruiksscenario&#39;s. In de volgende secties worden de meest gebruikte toepassingen beschreven en wordt beschreven hoe deze worden geïmplementeerd met Adobe [!DNL Commerce] Only of [!DNL Commerce] plus Experience Cloud-toepassingen.

### Persoonlijke campagnes en communicatie

| Hoofdletters en kleine letters | Oplossing |
|---|---|
| **Verlaten Kar en doorbladeren** - Lever een gepersonaliseerde re-overeenkomst e-mail of bericht wanneer een klant hun kar of doorbladerzitting na het aantonen van hoge overeenkomst verlaat | **Adobe [!DNL Commerce] slechts**:<br>[ E-mailherinneringen ](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules) <br>**Adobe [!DNL Commerce] met Adobe Journey Optimizer**:<br>[!DNL Commerce] de gegevens dienen als trekker voor een omni-channel beëindigingsreis. Personaliseer die reis die op klantenattributen, wordt gebaseerd wat zij, ander het winkelgedrag, en vroegere aankopen verlieten.<br> Commerce met Adobe Journey Optimizer en Real-Time CDP: De opruimingscampagnes van de dageraad die op verenigde klantenprofielen en centraal geleid publiek worden gebaseerd, bijvoorbeeld tot het creëren van een hoog percentage van het voortijdig verlaten. |
| **Gecentraliseerde Maken van het Publiek** - creeer op regel-gebaseerde of op AI-Gerichte soorten publiek dat op onsite gedrag, verleden-aankopen, profielattributen, categoriesaffiniteiten, loyaliteitsstatus, klantenwaarde en meer wordt gebaseerd | **Adobe [!DNL Commerce] slechts**:<br> verzamel de informatie van het klantenprofiel wanneer [!DNL Commerce] klanten rekeningen creëren. Creeer op regel-gebaseerde [ klantensegmenten ](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) en klantengroepen om inhoud en bevorderingen te personaliseren.<br>**Adobe [!DNL Commerce] met Adobe Real-Time CDP**:<br> [ Verenigde profielen ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) van over gegevensbronnen en kanalen; op regels-gebaseerd of op AI-Gebaseerd publiek. |
| **Gepersonaliseerde die Aanbieding E-mail/SMS op Gedrag van de Schopper** wordt gebaseerd - verzend gepersonaliseerde aanbiedingen aan klanten via gerichte e-mail op vroegere aankopen en verkoopgedrag, bijvoorbeeld, verzend aanbieding voor producten of categorieën klanten hebben bekeken of met geëngageerd. | **Adobe [!DNL Commerce] slechts**:<br> de gegevens van de Uitvoer voor gebruik met de oplossingen van de marketing automatisering.<br>**Adobe [!DNL Commerce] met Adobe Journey Optimizer en Real-Time CDP**:<br>[!DNL Commerce] de gegevens dienen als trekker voor e-mail of de aanbiedingen van SMS en verstrekt signalen (verkoopgedrag) om zich te personaliseren gebaseerd op. Real-Time CDP is niet verplicht, maar deze aanbiedingen en campagnes worden over het algemeen rond het publiek opgezet, dat binnen Real-Time CDP zou worden gecreëerd en beheerd. |
| **dwars of Upsell Compatibele Producten/Merken** - als een klant één product of merk koopt dat compatibel is of hoge affiniteit aan een ander product of een merk wijst, verzend een campagne (e-mail/SMS) om dwars-verkoopomzetting te drijven. | **Adobe [!DNL Commerce] slechts**:<br> Gebruik Adobe [!DNL Commerce] [ Aanbevelingen van het Product ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) om specifieke producten op de plaats aan te bevelen. U kunt [ Verwante Regels van het Product ](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) ook gebruiken om andere producten voor te stellen.<br>**[!DNL Commerce] met [!DNL Target]**:<br> Adobe [!DNL Target] heeft ook een ingebouwde motor van de productaanbeveling met krachtige mogelijkheden zoals categorieaffiniteit. Dit kan voor dwars of upsell worden gebruikt.<br>**[!DNL Commerce] met Adobe Journey Optimizer**:<br> Gebruik [!DNL Target] of [!DNL Commerce] om producten te bepalen om te adviseren, dan te leveren via Adobe Journey Optimizer. |

### Persoonlijke ervaringen met sites

| Hoofdletters en kleine letters | Oplossing |
|---|---|
| **Gepersonaliseerde Inhoud van de Plaats** - Personaliseer plaatsbanners en andere paginainhoud die op winkelacties, zoals product het doorbladeren en categoriereigenschappen wordt gebaseerd. Stel best-geschikte inhoud op die op resultaten van tests A/B of bedrijfsdoelstellingen wordt gebaseerd. | **Adobe [!DNL Commerce] slechts**:<br> stel segment-specifieke [ dynamische inhoudsblokken ](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) op.<br>**[!DNL Commerce] met Real-Time CDP **:<br> Gebruik [ Audience Activation ](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) om publiek-specifieke dynamische inhoudsblokken op te stellen die aan acties in real time en verenigde gegevens van het klantenprofiel antwoorden, terwijl centraal het beheren van profielen en publiek in Real-Time CDP.<br>**[!DNL Commerce] met[!DNL Target]**:<br> pas elk deel van de plaatservaring aan, met inbegrip van inhoud, navigatie punten, volledige paginalay-outs en meer gebruikend Adobe [!DNL Commerce] gegevens in Adobe [!DNL Target]. A/B testinhoud, selecteert en implementeert automatisch winnende inhoud voor elke klant.<br>**[!DNL Commerce] met AEM Assets **:<br> sla al uw inhoud in Adobe Experience Manager Assets op. U hebt vanuit Adobe Commerce native toegang tot die inhoud. Gebruik Generatieve AI om inhoudvariaties te maken die u kunt aanpassen aan verschillende segmenten of soorten publiek. |
| **Gepersonaliseerde Onsite die Aanbieding op Gedrag** wordt gebaseerd - Personaliseer bevorderingen die op verkoopacties, zoals product het doorbladeren en categoriereigenschappen worden gebaseerd. Implementeer de volgende beste aanbieding op basis van de resultaten van A/B-tests of bedrijfsdoelstellingen. | **Adobe [!DNL Commerce] slechts**:<br> stel segment-specifieke catalogus en [ de regels van de kartprijs ](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) op.<br>**Adobe [!DNL Commerce] met Real-Time CDP**:<br> Gebruik [ Audience Activation ](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) om publiek-specifieke aanbiedingen op te stellen, terwijl centraal het beheren van profielen/publiek in Real-Time CDP.<br>**Commerce met[!DNL Target]**: Het aanbiedingsbesluit van het gebruik om te bepalen welke aanbieding om op te stellen, A/B test of vastgestelde bedrijfsdoelstellingen om aanbiedingen te begeleiden die in Adobe Commerce worden opgesteld. |

### Analyses en inzichten

| Hoofdletters en kleine letters | Oplossing |
|---|---|
| **Gedrag van de Klant door Kanaal** - begrijp de nuances van hoe de klanten in elk kanaal (Web, in-persoon, app, andere) aan effect marketingstrategieën voor elk kanaal in dienst nemen; begrijp de verkooptrechter en de zwakheden in de klantenervaring. | **Adobe [!DNL Commerce] slechts**:<br>[ Adobe  [!DNL Commerce]  Intelligentie ](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) verstrekt rijke analyses op het digitale [!DNL Commerce] kanaal, maar niet over kanalen of bredere stukken van de klantenreis.<br>**Adobe [!DNL Commerce] met Customer Journey Analytics**:<br>[!DNL Commerce] de gegevensvoer gegevensdashboards voor volledig rijk detail op alle stadia van de klantenervaring (over kanalen). Begrijp elk aanraakpunt en de bredere trechter om zwakke punten in de klantenreis te identificeren waar de klanten van kunnen vallen. |
| **Trends van de Aankoop** - begrijp aankoopgedrag over een specifiek tijdskader (bijvoorbeeld, de analyse van de winkelmand, productanalyse) om tendensen, seizoensgebondenheid te identificeren, en marketing te optimaliseren die op historische aankooppatronen wordt gebaseerd. | **Adobe [!DNL Commerce] slechts**:<br>[ Adobe  [!DNL Commerce]  Intelligentie ](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) verstrekt rijke analyses op het digitale [!DNL Commerce] kanaal, maar niet over kanalen of bredere stukken van de klantenreis.<br>**Adobe [!DNL Commerce] met Customer Journey Analytics**:<br>[!DNL Commerce] de gegevensvoer gegevensdashboards voor volledig rijk detail op alle stadia van de klantenervaring (over kanalen). Begrijp elk aanraakpunt en de bredere trechter om zwakke punten in de klantenreis te identificeren waar de klanten van kunnen vallen. |

## Voorbeeld van gebruik-hoofdletters

- Leer hoe u Adobe Journey Optimizer kunt gebruiken om [ een verlaten kart e-mail ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/using-ajo) te verzenden.
- Leer hoe te [ om een publiek in Real-Time CDP ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience) tot stand te brengen om een regel van de kartprijs in Adobe [!DNL Commerce] te informeren.
