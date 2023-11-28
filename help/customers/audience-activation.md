---
title: "[!DNL Audience Activation]"
description: Leer hoe u het Real-Time CDP-publiek in Adobe Commerce activeert om personalisatie in uw winkel te stimuleren.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: f7b8e47aa5a8113fac768b8086ace3bf673193c5
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# [!DNL Audience Activation]

De [!DNL Audience Activation] Met deze extensie kunt u Real-Time CDP-publiek in Adobe Commerce activeren om unieke aanbiedingen in de winkelwagen te maken. Deze aanbiedingen en prikkels omvatten gemeenschappelijke technieken voor elektronische handel, zoals _koop 2 krijg 1 gratis_, hoofdbanners gericht op die klant, en gewijzigde productprijzen door diverse aanbiedingen. Het publiek dat in Real-Time CDP is samengesteld, is gebaseerd op gegevens van verschillende bedrijfssystemen, zoals Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), verkooppunten en marketingsystemen. Omdat de informatie van het klantensegment constant wordt verfrist, kunnen de klanten van een segment worden geassocieerd en worden losgemaakt aangezien zij in uw opslag winkelen.

U kunt een publiek activeren in een Luma-winkel of [krankzinnig](#headless-support) storefront. In een Luma-winkel wordt de publieksinformatie (segmentlidmaatschap) opgeslagen in een cookie aan de kant van de Handel. In een koploze winkel wordt de publieksinformatie doorgegeven in de GraphQL API-header als een parameter met de naam: `aep-segments-membership`.

## Opmerkingen bij de release

Deze sectie bevat informatie over updates voor de extensie Audience Activation en bevat:

![Nieuw](../assets/new.svg) - Nieuwe functies
![Repareren](../assets/fix.svg) - Oplossingen en verbeteringen
![Bug](../assets/bug.svg) - Bekende problemen

Zie [Volgende releases](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) om over versieschema&#39;s en steun te leren.

Zie de documentatie voor ontwikkelaars op [informatie over productcompatibiliteit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Ondersteunde service-updates

In deze releaseopmerkingen worden wijzigingen in de functies en correcties beschreven die betrekking hebben op extensies die door het Audience Activation worden gebruikt.

+++Ondersteunde service-updates

_15 augustus 2023_

![Repareren](../assets/new.svg) - De [Real-Time CDP-dashboard Soorten publiek](#real-time-cdp-audiences-dashboard) om het filteren te vereenvoudigen.

_27 juni 2023_

![Repareren](../assets/fix.svg) - Toegevoegde ondersteuning voor PHP 8.2 in de `magento/module-data-services-graphql` pakket.

_30 mei 2023_

![Nieuw](../assets/new.svg) - De [Real-Time CDP-dashboard Soorten publiek](#real-time-cdp-audiences-dashboard) om het actieve publiek in uw Adobe Commerce-instantie te sorteren, te zoeken en te filteren.

+++

### 2.0.0

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_10 oktober 2023_

![Nieuw](../assets/new.svg) - Toegevoegde ondersteuning voor OAuth 2.0 wanneer u [vormen](#configure-the-extension) de extensie Audience Activation.
![Repareren](../assets/fix.svg) - Verbeterde stabiliteit.

### 1.2.0

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_15 augustus 2023_

![Repareren](../assets/fix.svg) - De versie van de UI-componenten is bijgewerkt.

### 1.1.0

_30 mei 2023_

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

![Nieuw](../assets/new.svg) - Toegevoegde ondersteuning voor [dynamische blokken](#headless-support) in een koploze winkel.

### 1.0.1

_11 mei 2023_

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

![Repareren](../assets/fix.svg) - Probleem verholpen waarbij een dynamisch blok- of winkelprijscriterium niet werd toegepast.
![Repareren](../assets/fix.svg) - Probleem verholpen waarbij een niet-geconfigureerde installatie van de extensie Audience Activation een fout veroorzaakte wanneer een handelaar probeerde een dynamisch blok te maken of bij te werken.

### 1.0.0

_31 maart 2023_

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

![Nieuw](../assets/new.svg) - Algemene beschikbaarheidsrelease

## Implementatie

De volgende taken zijn van toepassing op zowel de uitvoeringen van het Luma als van het hoofdloze winkelcentrum. Als u het publiek in Adobe Commerce wilt activeren, moet u:

- Adobe Commerce versie 2.4.4 of hoger installeren
- [Activeren](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce als bestemming in Real-Time CDP
- [Installeren](#install-the-extension) de [!DNL Audience Activation] extensie in Admin
- [Configureren](#configure-the-extension) de [!DNL Audience Activation] extensie in Admin

### De extensie installeren

Installeer de [!DNL Audience Activation] van de [marktplaats](https://commercemarketplace.adobe.com/magento-audiences.html)of voer de volgende opdracht uit:

```bash
composer require magento/audiences
```

### De extensie configureren

Nadat u de [!DNL Audience Activation] extensie, moet u zich aanmelden bij uw Commerce Admin en het volgende voltooien:

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Aanmelden](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) naar uw Adobe-account en selecteer uw organisatie-id.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. In de **[!UICONTROL Datastream ID]** veld, plak de id van de gegevensstroom die u hebt gemaakt toen u [geactiveerd](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce als bestemming in Real-Time CDP.

   Deze gegevensstroom verzendt gegevens van uw website van de Handel naar Real-Time CDP om te bepalen of een verkoopster tot een publiek behoort. Als u nog geen gegevensstroom hebt gemaakt, [maken](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) één in Experience Platform, [toevoegen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) het naar de plaats van bestemming Handel in Real-Time CDP en naar de [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) extensie in het beheerprogramma.

   >[!NOTE]
   >
   >Wanneer u een gegevensstroom-id opgeeft, kunt u [koppelen aan een specifieke website](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) in de [!DNL Data Connection] extensie. Als uw winkel van de Handel veelvoudige websites heeft, [een doel maken](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) voor elke website in Real-Time CDP en gebruik voor elke website een andere gegevensstroom-id.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Uitbreiden **[!UICONTROL Services]** en selecteert u **[!UICONTROL [!DNL Data Connection]]**.

1. In de [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#send-historical-order-data) Volg stap 1 voor deze handleiding: **Een project maken in Adobe Developer Console** en 2: **Configuratiebestand downloaden**. Het resultaat is een bestand dat u kopieert en plakt in de **[!UICONTROL [!DNL Data Connection]]** configuratiepagina

   ![Configuratie Real-Time CDP Audience Admin](./assets/epc-admin-config.png){width="700" zoomable="yes"}

1. Klikken **Config opslaan**.

Als het publiek is geactiveerd voor uw Adobe Commerce-instantie, kunt u:

- [Een regel voor een winkelwagenprijs maken](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) geïnformeerd door het publiek
- [Een dynamisch blok maken](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) geïnformeerd door het publiek

## Real-Time CDP-doeldashboard

U kunt alle actieve soorten publiek weergeven die binnen uw Adobe Commerce-instantie kunnen worden gepersonaliseerd met de opdracht **Real-Time CDP-publiek** dashboard. Willekeurig publiek [geactiveerd](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) in de Adobe Commerce-bestemming in Real-Time CDP wordt in dit dashboard weergegeven.

Als u toegang wilt krijgen tot **Real-Time CDP-publiek** dashboard, ga naar _Beheerder_ zijbalk, ga vervolgens naar **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

Het dashboard bevat de volgende velden:

| Kolom | Beschrijving |
|--- |--- |
| `Hide filters` | Hiermee kunt u alle filters tonen of verbergen die u op het dashboard kunt toepassen. U kunt momenteel alleen het filter toepassen `Last updated`. Met dit filter kunt u een datumbereik voor soorten publiek selecteren op basis van het tijdstip waarop ze voor het laatst zijn bijgewerkt. |
| `Search` | Hiermee kunt u zoeken naar actief publiek in uw instantie Commerce. |
| `Name` | Naam gegeven aan het publiek in Real-Time CDP. |
| `Origin` | Geeft aan waar het publiek vandaan komt, zoals `Experience Platform`. |
| `Last updated` | Geeft aan wanneer het publiek is gewijzigd in Real-Time CDP. |
| `Sync now` | Hiermee haalt u nieuwe of bijgewerkte soorten publiek op uit Real-Time CDP. |
| `Customize table` | Hiermee kunt u de `Origin` en `Last updated` kolommen. |

{style="table-layout:auto"}

## Hoofdondersteuning

U kunt het publiek in een Adobe Commerce-instantie zonder kop, zoals AEM en PWA, activeren om regels voor de prijs van winkelwagentjes of dynamische blokken weer te geven op basis van het publiek.

### Prijsregels voor winkelwagentjes

Voor de regels voor de kartprijs geeft een koploze winkel het Experience Platform via de [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Het framework biedt een server-side API die met GraphQL is geïmplementeerd. De informatie van het publiek, zoals het segment van een verkoopster, gaat tot Handel door een GraphQL kopbalparameter over genoemd: `aep-segments-membership`.

De architectuur ziet er als volgt uit:

![Gegevens verzenden van Headless Storefront naar Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Na u [installeren](#install-the-extension) en [vormen](#configure-the-extension) Voor de uitbreiding, bevat het Web SDK van het Experience Platform de publieksinformatie in de vorm van segmentlidmaatschap.

Om die segmentlidmaatschappen van SDK te vangen, zie dit [codefragment](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Nadat het wordt teruggewonnen, kunt u die segmenten tot Handel binnen de kopbal van GraphQL overgaan. Bijvoorbeeld:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamische blokken

Voor dynamische blokken, GraphQL `dynamicBlocks` query&#39;s kunnen de `audience_id` invoerkenmerk. Als u een of meer `audience_id` waarden in a `dynamicBlocks` query, geeft het een lijst met dynamische blokken die aan dat publiek zijn toegewezen.

#### Voorbeeldgebruik

De volgende vraag keert alle dynamische blokken verbonden aan veelvoudige publiek IDs terug.

**Verzoek:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Reactie:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

Meer informatie over de `dynamicBlocks` GraphQL-query in het dialoogvenster [ontwikkelaarsdocumentatie](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Soorten publiek ophalen met de Adobe Experience Platform Mobile SDK

Voordat u het Real-Time CDP-publiek kunt ophalen met de Adobe Experience Platform Mobile SDK, moet u [De SDK voor uw site voor mobiele handel installeren en configureren](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>De Adobe Experience Platform Mobile SDK voor iOS ondersteunt iOS 11 of hoger.

Nadat u de configuratie hebt voltooid, gebruikt u mobiele SDK-bewerkingen om de publieksgegevens op te halen. Bijvoorbeeld:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

Nadat de gegevens zijn opgehaald, kunt u deze gebruiken om op de doelgroep gebaseerde gegevens te maken [regels betreffende de kartonprijs](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) en [dynamische blokken](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) in de Commerce-app.
