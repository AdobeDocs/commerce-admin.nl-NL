---
title: Maak aansprekende, persoonlijke ervaringen op schaal
description: Leer welke functies in Adobe zijn [!DNL Commerce] Hiermee kunt u een persoonlijke ervaring voor kopers maken.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 1a63af10d76cb9d17a992e8822e99d50bcdfa84e
workflow-type: tm+mt
source-wordcount: '1630'
ht-degree: 0%

---

# Maak aansprekende, persoonlijke ervaringen op schaal

Adobe [!DNL Commerce] biedt u een krachtige toolkit om elk aanraakpunt van klanten aan te passen, waardoor de betrokkenheid van klanten, conversie en omzet wordt verhoogd.

In dit artikel leert u:

- Wat is personalisatie?
- Welke gegevens heb ik nodig om personalisatie te bereiken?
- Hoe werkt Adobe? [!DNL Commerce] personalisatie ontgrendelen?
- Beschikbare gebruiksgevallen voor personalisatie

## Wat is personalisatie?

Personalisatie betekent dat aspecten van de koopervaring van elke klant worden aangepast aan hun unieke behoeften, context en voorkeuren. Personalisatie is niet beperkt tot inhoud op de site of het aanbevelen van best-fit producten, maar omvat alle aanraakpunten over de reis van de klant, met inbegrip van:

- **Campagnes en communicatie** - relevante en consistente berichtgeving via campagnes en communicatie
- **Productdetectie** - De juiste producten op de juiste momenten aan de juiste klanten tonen
- **Aanbiedingen en aanbiedingen** - Promoties en aanbiedingen richten om elke klant te stimuleren om te converteren
- **Ervaringen met inhoud** - Inhoud van de website aanpassen om hyper-relevant voor elke klant en zijn reis te voelen

![Typen personalisatie](assets/types-personalization.png){width="700" zoomable="yes"}

Terwijl deze soorten gepersonaliseerde ervaringen voor een kleine ondergroep van klanten haalbaar kunnen schijnen, die aan schaal voor duizenden of miljoenen klanten over elk aanraakpunt en kanaal aanpassen, kunnen allen in real time zich onmogelijk voelen. In de volgende secties leert u hoe Adobe [!DNL Commerce] en Adobe Experience Cloud kan helpen.

## Welke gegevens heb ik nodig om personalisatie te bereiken?

De efficiënte verpersoonlijking vereist context of signalen die informatie over klanten verstrekken die dan kunnen worden gebruikt om hun ervaring te wijzigen. De volgende tabel bevat de verschillende gegevenstypen en de rol die Adobe [!DNL Commerce] speelt bij het ondersteunen van het verzamelen en activeren van die gegevens.

| Gegevenstypen | Storefront-gegevens (gedragsgebeurtenissen) | Back Office-gegevens (server-side gebeurtenissen) | Klantprofiel en segmentgegevens |
|---|---|---|---|
| **Definitie** | Klik of acties die klanten op uw site uitvoeren. | Informatie over de levenscyclus en details van elke bestelling (verleden en huidig). | Wie zijn de kopers en voor welke segmenten komen ze in aanmerking? |
| **Gebeurtenissen vastgelegd door Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Status van bestelling**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnsInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Orderhistorie**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Naam, Prijshoeveelheid, Korting<br>- Productcategorie<br>- Betalingsbedrag, type, valuta<br>- Verzendmethode en -bedrag<br>- Terugbetaling-ID, Bedrag, Valuta<br>- Reden van terugkeer, Voorwaarde, Resolutie<br>- Adres<br>- E-mail | [**Profielrecord**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Naam, Geslacht, Adres, Loyalty Status, Telefoonnummer, E-mailadres)<br>**Accountstatus**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDelted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Met al deze rijke, eerstepartijenlijst [!DNL Commerce] gegevens, bent u klaar om de ervaring van elke verkoopster te richten en te personaliseren. In de volgende sectie leert u hoe [!DNL Commerce] en Adobe Experience Cloud helpen u om persoonlijke ervaringen en gebruiksgevallen te maken die u kunt activeren.

## Hoe werkt Adobe? [!DNL Commerce] personalisatie kracht bijzetten?

Adobe [!DNL Commerce] Met gegevensuitwisseling kunt u de gegevenstypen in de vorige tabel verzamelen en delen met andere Adobe Experience Cloud-producten, zodat u uniforme profielen en doelgroepen van klanten, gepersonaliseerde campagnes en rijke analyses en inzichten kunt gebruiken.

![De gegevensstroom naar de rand van het Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Het delen van gegevens omvat twee zeer belangrijke componenten:

1. [Gegevensverbinding](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): Deel storefront, achterkantoor en klantprofielgegevens van Adobe [!DNL Commerce] naar het Adobe Experience Platform edge-netwerk voor gebruik in Adobe Experience Cloud-toepassingen, waaronder:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): De gegevens van de klanten van de Stitch van over bronnen (ERP, CRM, POS) in verenigde profielen en leiden op regel-gebaseerde of op AI-Gebaseerde segmenten.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): Geppersonaliseerde e-mailreizen starten, waaronder e-mailcampagnes, SMS, pushmeldingen en nog veel meer.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) en [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): Verbeter inzichten in de klant en de zaken.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Inhoud, aanbevolen producten, aanbiedingen, navigatie en meer testen en optimaliseren.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Gebruik [!DNL Real-Time CDP] publiek om dynamische inhoudblokken, promoties en verwante productregels op uw Adobe aan te passen [!DNL Commerce] site.

### Buiten-de-doos Personalisatie: Ga aan de slag met inheemse Adobe [!DNL Commerce] functies

Adobe [!DNL Commerce] biedt krachtige personalisatie met de native out-of-the-box mogelijkheden. De volgende tabel beschrijft [!DNL Commerce] functies die u direct kunt activeren om aan de slag te gaan met uw persoonlijke voorkeur.

| Categorie | Functies |
|---|---|
| Persoonlijke productdetectie | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): Pas de zoekresultaten aan en optimaliseer ze op basis van de acties en affiniteiten die een winkelier op locatie uitvoert met de zoekfunctie van AI.<br>[Intelligente handel in categorieën](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): Op categoriepagina&#39;s wordt een door AI aangedreven productclassificatie gebaseerd op de acties en affiniteiten van een verkoopster ter plaatse.<br>[Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): Op AI gebaseerde productaanbevelingen op basis van gedrag, trends en affiniteiten van winkels.<br>[Regels voor verwante producten](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): Definieer aangepaste regels om producten uit uw catalogus weer te geven om cross-and-up-sell te stimuleren. |
| Persoonlijke site-inhoud | [Dynamische-inhoudblokken](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Geef gepersonaliseerde inhoudsblokken weer, bijvoorbeeld banners, op basis van klantsegmenten in Adobe Commerce. |
| Persoonlijke aanbiedingen en aanbiedingen | [Lijnen met winkelprijzen](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Pas kortingen toe op artikelen in het winkelwagentje op basis van een aantal voorwaarden, waaronder klantsegmenten in de Adobe [!DNL Commerce]. |
| Inzichten en meting | [Adobe [!DNL Commerce] Intelligentie](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Begrijp hoe uw verpersoonlijkingsstrategieën werken en verbeteren in de loop van de tijd. |

## Gebruiksscenario&#39;s voor topverpersoonlijking

Adobe [!DNL Commerce] klanten gebruiken out-of-the-box mogelijkheden en delen gegevens aan Adobe Experience Cloud voor een verscheidenheid van gebruiksgevallen. In de volgende secties worden de meest gebruikte gevallen beschreven en wordt beschreven hoe deze met Adobe zijn geïmplementeerd [!DNL Commerce] Alleen of [!DNL Commerce] plus Experience Cloud-apps.

### Persoonlijke campagnes en communicatie

| Hoofdletters en kleine letters | Oplossing |
|---|---|
| **Verlaten Kart en Bladeren** - Een persoonlijke e-mail of melding over een nieuwe service leveren wanneer een klant zijn winkelwagentje of bladersessie afsluit nadat een hoge service is aangetoond | **Adobe [!DNL Commerce] Alleen**:<br>[E-mailherinneringen](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] met Adobe Journey Optimizer**:<br>[!DNL Commerce] gegevens dienen als de aanzet tot een omni-channel-verlaten reis. Personaliseer die reis die op klantenattributen, wordt gebaseerd wat zij, ander het winkelgedrag, en vroegere aankopen verlieten.<br>Commerce met Adobe Journey Optimizer en Real-Time CDP: Tailor-opruimingscampagnes gebaseerd op verenigde klantprofielen en centraal beheerde doelgroepen, bijvoorbeeld door een hoog percentage gebruikers voor het verlaten van het bedrijf te creëren. |
| **Gecentraliseerde publiek maken** - Maak op regels gebaseerd of door AI aangedreven publiek op basis van onsite gedrag, aankopen in het verleden, profielkenmerken, categorie-affiniteiten, loyaliteitsstatus, klantwaarde en meer | **Adobe [!DNL Commerce] Alleen**:<br>Klantprofielgegevens verzamelen wanneer [!DNL Commerce] klanten maken accounts. Op regels gebaseerd maken [klantsegmenten](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) en klantgroepen om inhoud en promoties aan te passen.<br>**Adobe [!DNL Commerce] met Adobe Real-Time CDP**:<br> [Verenigde profielen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) van verschillende gegevensbronnen en kanalen; op regels gebaseerd of door AI aangedreven publiek. |
| **Aanbieding via persoonlijke e-mail/SMS op basis van gedrag van koper** - Verstuur persoonlijke aanbiedingen naar klanten via e-mail op basis van eerdere aankopen en winkelgedrag, bijvoorbeeld verzend voorstellen voor producten of categorieën die klanten hebben bekeken of gebruikt. | **Adobe [!DNL Commerce] Alleen**:<br>Gegevens exporteren voor gebruik met oplossingen voor marketingautomatisering.<br>**Adobe [!DNL Commerce] met Adobe Journey Optimizer en Real-Time CDP**:<br>[!DNL Commerce] gegevens fungeren als de trigger voor e-mail- of SMS-aanbiedingen en bieden signalen (gedrag van winkels) die u kunt aanpassen. Real-Time CDP is niet verplicht, maar deze aanbiedingen en campagnes worden over het algemeen rond het publiek opgezet, dat binnen Real-Time CDP zou worden gecreëerd en beheerd. |
| **Compatibele producten/merken voor meerdere of verbeterde objecten** - Als een klant één product of merk koopt dat compatibel is of dat een hoge affiniteit voor een ander product of merk vertoont, stuurt u een campagne (e-mail/sms) om de omzetting van producten tussen verschillende producten te stimuleren. | **Adobe [!DNL Commerce] Alleen**:<br>Adobe gebruiken [!DNL Commerce] [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) om specifieke producten op de plaats aan te bevelen. U kunt ook [Regels voor verwante producten](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) andere producten voor te stellen.<br>**[!DNL Commerce] with [!DNL Target]**:<br>Adobe [!DNL Target] beschikt ook over een ingebouwde productaanbeveling-engine met krachtige mogelijkheden, zoals de affiniteit van categorieën. Dit kan voor dwars of upsell worden gebruikt.<br>**[!DNL Commerce] met Adobe Journey Optimizer**:<br>Gebruiken [!DNL Target] of [!DNL Commerce] om producten te bepalen die moeten worden aanbevolen, dan leveren via Adobe Journey Optimizer. |

### Persoonlijke ervaringen met sites

| Hoofdletters en kleine letters | Oplossing |
|---|---|
| **Persoonlijke site-inhoud** - Websitebanners en andere pagina-inhoud aanpassen op basis van winkelacties, zoals bladeren door producten en categorie-affiniteiten. Stel best-geschikte inhoud op die op resultaten van tests A/B of bedrijfsdoelstellingen wordt gebaseerd. | **Adobe [!DNL Commerce] Alleen**:<br>Segmentspecifiek implementeren [dynamische inhoudblokken](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] met Real-Time CDP **:<br>Gebruiken [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) om publiek-specifieke dynamische inhoudsblokken op te stellen die aan acties in real time en verenigde gegevens van het klantenprofiel antwoorden, terwijl het centraal beheren van profielen en publiek in Real-Time CDP.<br>**[!DNL Commerce] with[!DNL Target]**:<br>Pas elk deel van de site-ervaring aan, inclusief inhoud, navigatie-items, volledige paginalay-outs en meer met Adobe [!DNL Commerce] gegevens in Adobe [!DNL Target]. A/B testinhoud, selecteert en implementeert automatisch winnende inhoud voor elke klant.<br>**[!DNL Commerce] met AEM Assets **:<br>Sla al je inhoud op in Adobe Experience Manager Assets. U hebt vanuit Adobe Commerce native toegang tot die inhoud. Met GenAI kunt u inhoudvariaties maken die u kunt aanpassen aan verschillende segmenten of soorten publiek. |
| **Persoonlijke onsite aanbieding op basis van gedrag** - Promoties aanpassen op basis van acties van winkels, zoals bladeren door producten en rubriekaffiniteiten. Implementeer de volgende beste aanbieding op basis van de resultaten van A/B-tests of bedrijfsdoelstellingen. | **Adobe [!DNL Commerce] Alleen**:<br>Segmentspecifieke catalogus implementeren en [regels betreffende de kartonprijs](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] met Real-Time CDP**:<br>Gebruiken [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) om publiekspecifieke aanbiedingen te implementeren en tegelijkertijd profielen/publiek centraal te beheren in Real-Time CDP.<br>**Commerce met[!DNL Target]**: De offer decisioning van het gebruik om te bepalen welke aanbieding om op te stellen, test A/B of vastgestelde bedrijfsdoelstellingen om aanbiedingen te begeleiden die in Adobe Commerce worden opgesteld. |

### Analyses en inzichten

| Hoofdletters en kleine letters | Oplossing |
|---|---|
| **Gedrag van de klant per kanaal** - Begrijp de nuances van hoe klanten in elk kanaal (Web, in-persoon, app, andere) aan invloed op marketing strategieën voor elk kanaal; begrijp de verkooptrechter en de zwakheden in de klantenervaring. | **Adobe [!DNL Commerce] Alleen**:<br>[Adobe [!DNL Commerce] Intelligentie](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) biedt uitgebreide analysemogelijkheden voor de digitale [!DNL Commerce] kanaal, maar niet over kanalen of bredere stukken van de klantenreis.<br>**Adobe [!DNL Commerce] met Customer Journey Analytics**:<br>[!DNL Commerce] gegevens voeren gegevensdashboards voor volledig rijke detail op alle stadia van de klantenervaring (over kanalen) uit. Begrijp elk aanraakpunt en de bredere trechter om zwakke punten in de klantenreis te identificeren waar de klanten van kunnen vallen. |
| **Aankooptrends** - inzicht in het aankoopgedrag gedurende een specifiek tijdsbestek (bijvoorbeeld analyse van winkelmandjes, productanalyse) om trends, seizoensgebondenheid en optimalisering van de marketing op basis van historische aankooppatronen te identificeren. | **Adobe [!DNL Commerce] Alleen**:<br>[Adobe [!DNL Commerce] Intelligentie](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) biedt uitgebreide analysemogelijkheden voor de digitale [!DNL Commerce] kanaal, maar niet over kanalen of bredere stukken van de klantenreis.<br>**Adobe [!DNL Commerce] met Customer Journey Analytics**:<br>[!DNL Commerce] gegevens voeren gegevensdashboards voor volledig rijke detail op alle stadia van de klantenervaring (over kanalen) uit. Begrijp elk aanraakpunt en de bredere trechter om zwakke punten in de klantenreis te identificeren waar de klanten van kunnen vallen. |

## Voorbeeld van gebruik-hoofdletters

Meer informatie over hoe je Adobe Journey Optimizer kunt gebruiken voor [een e-mail met een verlaten winkelwagentje verzenden](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
