---
title: Personalisatie op schaal
description: Leer welke functies je in Adobe Commerce kunt gebruiken om een persoonlijke ervaring voor je kopers te maken.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5f40c98324c3033cdeb8a11e89a71497ced890b8
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Personalisatie op schaal

&#x200B; Personalisatie op schaal staat ondernemingen toe om de het winkelen ervaring voor elk klantenaanraakpunt te personaliseren dat op directe context en eerder waargenomen gedrag wordt gebaseerd. Het doel is om telkens de meest relevante en gepersonaliseerde ervaring te presenteren.

Als u de voordelen van een persoonlijke winkelervaring wilt begrijpen, downloadt u de [_Aan de slag met personalisatie op schaal_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) verslag.

Om een gepersonaliseerde het winkelen ervaring te creëren vereist u om over het type van gegevens te leren nodig om de klantencontext te begrijpen. Van daaruit leert u over Adobe Commerce-functies die deze gegevens gebruiken om de inzichten van de klant te ontsluiten die u nodig hebt om de persoonlijke winkelervaring te creëren.

In de volgende afbeelding ziet u de concepten die u nodig hebt voor het aanpassen van de winkelervaring:

![Een personalisatiepijplijn maken](assets/personalization-journey.png){width="700" zoomable="yes"}

In dit artikel worden de bovenstaande concepten gedetailleerder besproken.

## Hoe maak je een persoonlijk tintje op de boodschappenbeleving?

Succesvolle verpersoonlijking begint met klantencontext. In deze sectie, leert u over de gegevenstypes die beschikbaar zijn om u te helpen de klantencontext bouwen.

### Storefront-gegevens

Storefront-gegevens, ook wel gedrags- of browsergegevens genoemd, kunnen inzicht geven in de manier waarop kopers met uw site communiceren. Bijvoorbeeld:

- Welke producten en categorieën zijn mijn kopers het meest geïnteresseerd?
- Wat voor soort zoekquery&#39;s zijn mijn kopers het meest betrokken?
- Zijn mijn kopers producten aan het winkelwagentje toevoegen en het dan verlaten?
- Gebruiken mijn kopers een desktopcomputer of een mobiele browser?

De volgende storefront gebeurtenissen vangen gegevens die u kunnen helpen deze vragen beantwoorden:

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Gegevens voor back-office

De gegevens van het achterkantoor, ook genoemd server-zijgegevens, kunnen inzichten in de cyclus van het ordeleven openbaren. Bijvoorbeeld:

- Zijn er producten die vaker op basis van het seizoen worden aangekocht?
- Retourneert mijn winkels producten?
- Hoe kan ik de waarde van levenslange klanten berekenen?

De volgende gebeurtenissen van het achterkantoor vangen gegevens die u kunnen helpen deze vragen beantwoorden:

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnsInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Klantprofiel en segmentgegevens

Klantprofielgegevens kunnen inzicht geven in wie uw klanten zijn en voor welke segmenten zij in aanmerking komen. Bijvoorbeeld:

- Naam
- Geslacht
- Adres
- Loyalstatus
- Telefoonnummer
- E-mailadres
- Loyalstatus
- Telefoonnummer
- E-mailadres
- Geschiktheid voor upgrades
- Kopers tussen kanalen
- Vooruitzichten voor nieuwe producten
- Goud-, zilver- of bronzen loyaliteitsleden

De volgende profielgebeurtenissen leggen gegevens vast die u kunnen helpen deze vragen te beantwoorden:

- [Profielrecord](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDelted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

Storefront-, back-office- en profielgegevens vormen de basis van de Commerce-context voor klanten en bestellingen, zodat u weet welke producten uw klanten bekijken en uiteindelijk kopen. Je kunt dan hun belangen bepalen en hun ervaring personaliseren. In de volgende sectie leert u welke soorten persoonlijke ervaringen u kunt gebruiken met uw klanten.

## Typen persoonlijke ervaringen

De klant en de gegevens van de ordecontext in Commerce bevorderen de volgende soorten gepersonaliseerde ervaringen:

| Ervaring | Beschrijving |
|---|---|
| **Productdetectie** | Bevat merchandising-services die [geïmplementeerd als SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Dit zijn functies waarmee u gedragsgegevens, productkenmerken en inventarisniveaus kunt gebruiken om productdetectie automatisch aan te passen aan de verschillende zoekresultaten, productaanbevelingen en bladerpagina&#39;s. Deze functies gebruiken allemaal [ADOBE SENSEI AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Site-inhoud** | Verwijst naar de capaciteit om gepersonaliseerde dynamische inhoudsblokken op te stellen die op de huidige klant worden gebaseerd die uw plaats doorbladert. |
| **Aanbiedingen en campagnes** | Hiermee kunt u gepersonaliseerde promotionele inhoud implementeren op basis van segmentgegevens. |
| **Meting** | Gebruikt gegevensintelligentie om uw zaken met inbegrip van opbrengst, kanaal en koopwaar prestaties, bevorderingen, etc. beter te begrijpen. |

In de volgende twee secties leert u hoe u deze gegevens kunt gebruiken om persoonlijke ervaringen te creëren in [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) en in [native Commerce-functies](#using-commerce-data-in-native-commerce-features).

## Commerce-gegevens gebruiken in Adobe Experience Platform

Als u een persoonlijke ervaring voor uw klanten op alle kanalen wilt creëren, stuurt u uw Commerce-gegevens naar de Edge Network van het Experience Platform met de [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) extensie.

![De gegevensstroom naar de rand van het Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

In de bovenstaande afbeelding worden de gegevens van uw winkel, back office en klantprofiel naar de rand van het Experience Platform verzonden met behulp van een SDK, API en een bronaansluiting. U hoeft niet volledig te begrijpen hoe deze onderdelen werken als de extensie de complexiteit voor het delen van gegevens voor u behandelt. Wanneer de gebeurtenisgegevens zich aan de rand bevinden, kunt u die gegevens in andere Experience Platforms toepassingen opnemen.

In de volgende tabel worden enkele van de beschikbare Experience Platforms-toepassingen gemarkeerd en wordt aangegeven hoe deze toepassingen uw Commerce-gegevens gebruiken.

| Ervaring | Toepassing | Hoe Commerce Data wordt gebruikt |
|---|---|---|
| **Site-inhoud** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerce-gegevens leveren geharmoniseerde klantprofielen op, waarbij Real-Time CDP gegevens uit verschillende bronnen (ERP, CRM, CMS, POS) onderbrengt in afzonderlijke profielen. Real-Time CDP kan zowel op regels-gebaseerde als op AI-Gebaseerde segmenten tot stand brengen om dan over uw geplaatste marketing oplossing te gebruiken. U kunt Real-Time CDP-publiek ook gebruiken om inhoudsblokken, promoties en gerelateerde productregels aan te passen. Zie [[!DNL Audience Activation]](../customers/audience-activation.md) voor meer informatie. &#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerce-gegevens kunnen in Adobe worden geactiveerd [!DNL Target] voor het testen, optimaliseren en maken van dynamische bestemmingspagina&#39;s. U kunt de volgorde aanpassen waarin inhoud op een pagina wordt weergegeven, zoals beschrijvingen, specificaties, revisies en aanbevolen producten op basis van de verzonden Commerce-gegevens. |
| **Aanbiedingen en campagnes** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Adobe Commerce-gedrags- en back-office gegevens kunnen worden gebruikt als een aansporing voor gepersonaliseerde omni-kanaalreizen, zoals e-mailcampagnes, SMS, pushmeldingen en nog veel meer. &#x200B; |
| **Meting** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) en [Klant [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce stuurt zowel gegevens van de winkel als van de back-office naar de klant [!DNL Journey Analytics] (en alleen gegevens opslaan naar Adobe [!DNL Analytics]) om een rijkere analyse mogelijk te maken die verder gaat dan de elementaire maatstaven van Adobe Commerce Intelligence, zoals inkomsten, handelswaar en promoties. &#x200B; |

Ga voor meer informatie over hoe je Commerce-gegevens naar het Experience Platform kunt verzenden naar [Gegevensverbinding](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Commerce-gegevens gebruiken in systeemeigen Commerce-functies

In de volgende sectie leert u hoe u native Commerce-functies, zoals Product Recommendations en Live Search, kunt gebruiken om een persoonlijke winkelervaring te creëren. U zult ook over een eigenschap leren genoemd [!DNL Audience Activation], die gegevens gebruikt van een product dat beschikbaar is in de Experience Platform met de naam Real-Time CDP, zoals vermeld [voorheen](#using-commerce-data-in-adobe-experience-platform). Hoewel Real-Time CDP niet in Commerce is opgenomen, kan de informatie in Commerce via de [[!DNL Audience Activation]](../customers/audience-activation.md) extensie.

In de volgende tabel worden de Commerce-functies beschreven die beschikbaar zijn om de Commerce-klanten en ordercontextgegevens om te zetten in inzichten die uitvoerbaar zijn.

| Ervaring | Functie | Beschrijving |
|---|---|---|
| **Productdetectie** | [Live zoeken](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Gebruikt AI rangschikkingsalgoritmen om onderzoeksresultaten te personaliseren en te optimaliseren die op de acties van het het gedrag van een verkoopster ter plaatse worden gebaseerd, die onderzoeksrelevantie en omzetting bevorderen. |
|  | [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Hier worden productaanbevelingen weergegeven die zijn gebaseerd op winkelgedrag, trends, productgelijkenis en meer. Als de productaanbevelingen worden gecombineerd met uw Adobe Commerce-catalogus, bieden ze een zeer aantrekkelijke, relevante en persoonlijke ervaring. |
|  | [Categorieverhandeling](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Vanuit Live Search Admin is de categorie Handchandising benaderd met AI om de reeks producten op elke categoriepagina automatisch opnieuw te genereren en zo de relevantie en conversie voor elke winkel te verbeteren. U kunt op AI-Gebaseerde regels tot stand brengen en leiden om product het rangschikken op categoriepagina&#39;s volgens winkelacties en affiniteiten automatisch te herleiden. |
| **Site-inhoud** | [Dynamische blokken die worden geïnformeerd door native Commerce-functies](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Staat u toe om gepersonaliseerde plaatsinhoud te leveren die op logica wordt gebaseerd die in prijsregels en klantensegmenten wordt gevormd. |
|  | [Dynamische blokken, geïnformeerd door Real-Time CDP-publiek](../customers/audience-activation.md) | Laat verkopers toe om gepersonaliseerde plaatsinhoud te leveren die op publiek wordt gebaseerd dat in Real-Time CDP wordt gevormd. |
| **Aanbiedingen en campagnes** | [Prijsregels voor winkelwagentjes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Hiermee kunt u op basis van een aantal voorwaarden kortingen toepassen op objecten in het winkelwagentje. |
|  | [Dynamische blokken die worden geïnformeerd door native Commerce-functies](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Staat u toe om gepersonaliseerde bannerbevorderingen te tonen die op klantensegmenten worden gebaseerd die in Commerce worden gevormd. |
|  | [Dynamische blokken, geïnformeerd door Real-Time CDP-publiek](../customers/audience-activation.md) | Staat u toe om gepersonaliseerde bevorderingen te tonen die op publiek in Real-Time CDP wordt gevormd. |
| **Meting** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (Vroeger bekend als Magento Business Intelligence) is een wolkenplatform dat inzicht in best practices biedt om u te helpen gegevensgestuurde beslissingen te nemen en duidelijke en geïnformeerde acties te ondernemen. Adobe Commerce Intelligence kan uw gegevens analyseren om u te helpen vragen te beantwoorden over de groei van bestellingen, het gedrag van klanten en de doeltreffendheid van promotiestrategieën. |
