---
title: "[!DNL Audience Activation]"
description: Leer hoe u het Real-Time CDP-publiek in Adobe Commerce activeert om personalisatie in uw winkel te stimuleren.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: aacba21dc4472b04e87b0a3c5e722b3ecd52770d
workflow-type: tm+mt
source-wordcount: '1457'
ht-degree: 0%

---

# [!DNL Audience Activation]

De [!DNL Audience Activation] Met deze extensie kunt u Real-Time CDP-publiek in Adobe Commerce activeren om unieke aanbiedingen in de winkelwagen te maken. Deze aanbiedingen en prikkels omvatten gemeenschappelijke technieken voor elektronische handel, zoals _koop 2 krijg 1 gratis_, hoofdbanners gericht op die klant, en gewijzigde productprijzen door diverse aanbiedingen. Het publiek dat in Real-Time CDP is samengesteld, is gebaseerd op gegevens van verschillende bedrijfssystemen, zoals Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), verkooppunten en marketingsystemen. Omdat de informatie van het klantensegment constant wordt verfrist, kunnen de klanten van een segment worden geassocieerd en worden losgemaakt aangezien zij in uw opslag winkelen.

U kunt een publiek activeren in een Luma-winkel of [krankzinnig](#headless-support) storefront. In een Luma-winkel wordt de publieksinformatie (segmentlidmaatschap) opgeslagen in een cookie aan de Commerce-zijde. In een koploze winkel wordt de publieksinformatie doorgegeven in de GraphQL API-header als een parameter met de naam: `aep-segments-membership`.

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

![Repareren](../assets/fix.svg) - De [Real-Time CDP-dashboard Soorten publiek](#real-time-cdp-audiences-dashboard) om het filteren te vereenvoudigen.

_27 juni 2023_

![Repareren](../assets/fix.svg) - Toegevoegde ondersteuning voor PHP 8.2 in de `magento/module-data-services-graphql` pakket.

_30 mei 2023_

![Nieuw](../assets/new.svg) - De [Real-Time CDP-dashboard Soorten publiek](#real-time-cdp-audiences-dashboard) om het actieve publiek in uw Adobe Commerce-instantie te sorteren, te zoeken en te filteren.

+++

### 2.1.1.

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_4 april 2024_

![Nieuw](../assets/new.svg) - Toegevoegde ondersteuning voor PHP 8.3.

### 2.2.0-bèta1

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_16 februari 2024_

![Nieuw](../assets/new.svg) - Als u deelneemt aan de bètaversie, zorg er dan voor dat u `composer.json` bestand heeft het volgende op hoofdniveau: ` "minimum-stability": "beta"`.
![Nieuw](../assets/new.svg) - (**Beta**) Toegevoegde mogelijkheid om te maken [verwante productregels](../merchandising-promotions/product-related-rule-create.md) door het publiek geïnformeerd.

### 2.1.0.

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_24 januari 2024_

![Nieuw](../assets/new.svg) - De [Real-Time CDP-dashboard Soorten publiek](#real-time-cdp-audiences-dashboard) de websites met het publiek op te nemen en te specificeren welke dynamische blokken en regels voor de kartprijs zijn geconfigureerd om dat publiek te gebruiken.

### 2.0.1.

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_16 november 2023_

![Repareren](../assets/fix.svg) - Verbeterde stabiliteit.

### 2.0.0.

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_10 oktober 2023_

![Nieuw](../assets/new.svg) - Toegevoegde ondersteuning voor OAuth 2.0 wanneer u [vormen](#configure-the-extension) de extensie Audience Activation.
![Repareren](../assets/fix.svg) - Verbeterde stabiliteit.

### 1.2.0.

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

_15 augustus 2023_

![Repareren](../assets/fix.svg) - De versie van de UI-componenten is bijgewerkt.

### 1.1.0.

_30 mei 2023_

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

![Nieuw](../assets/new.svg) - Toegevoegde ondersteuning voor [dynamische blokken](#headless-support) in een koploze winkel.

### 1.0.1.

_11 mei 2023_

[!BADGE Compatibiliteit]{type=Informative tooltip="Compatibiliteit"}

![Repareren](../assets/fix.svg) - Probleem verholpen waarbij een dynamisch blok- of winkelprijscriterium niet werd toegepast.
![Repareren](../assets/fix.svg) - Probleem verholpen waarbij een niet-geconfigureerde installatie van de extensie Audience Activation een fout veroorzaakte wanneer een handelaar probeerde een dynamisch blok te maken of bij te werken.

### 1.0.0.

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

Nadat u de [!DNL Audience Activation] -extensie, dient u zich aan te melden bij uw Commerce Admin en het volgende in te vullen:

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Aanmelden](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) naar uw Adobe-account en selecteer uw organisatie-id.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. In de **[!UICONTROL Datastream ID]** veld, plak de id van de gegevensstroom die u hebt gemaakt toen u [geactiveerd](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce als bestemming in Real-Time CDP.

   Deze gegevensstroom verzendt gegevens van uw Commerce-website naar Real-Time CDP om te bepalen of een klant tot een publiek behoort. Als u nog geen gegevensstroom hebt gemaakt, [maken](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) één in Experience Platform, [toevoegen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) het naar de bestemming Commerce in Real-Time CDP en naar de [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) extensie in het beheerprogramma.

   >[!NOTE]
   >
   >Wanneer u een gegevensstroom-id opgeeft, kunt u [koppelen aan een specifieke website](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) in de [!DNL Data Connection] extensie. Als uw Commerce-winkel meerdere websites heeft, [een doel maken](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) voor elke website in Real-Time CDP en gebruik voor elke website een andere gegevensstroom-id.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Uitbreiden **[!UICONTROL Services]** en selecteert u **[!UICONTROL [!DNL Data Connection]]**.

1. [Toevoegen](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) serviceaccount en referentiedetails.

## Waar kan het Real-Time CDP-publiek in Commerce worden gebruikt?

Met de [!DNL Audience Activation] extensie ingeschakeld, kunt u:

- [Een regel voor een winkelwagenprijs maken](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) geïnformeerd door het publiek
- [Een dynamisch blok maken](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) geïnformeerd door het publiek
- [(**Beta**) Een regel voor een verwant product maken](../merchandising-promotions/product-related-rule-create.md) geïnformeerd door het publiek

Voor een volledige gebruiksscenario van begin tot eind over hoe te om uit te voeren [!DNL Commerce] gegevens naar Real-Time CDP, maak een publiek en activeer dat publiek vervolgens naar [!DNL Commerce], zie [Een publiek maken in Real-Time CDP met [!DNL Commerce] gebeurtenisgegevens](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience).

## Real-Time CDP-doeldashboard

U kunt alle [actief](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) publiek dat binnen uw Adobe Commerce-instantie kan worden gepersonaliseerd met behulp van de **Real-Time CDP-publiek** dashboard.

Als u toegang wilt krijgen tot **Real-Time CDP-publiek** dashboard, ga naar _Beheerder_ zijbalk, ga vervolgens naar **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP-dashboard Soorten publiek](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Het dashboard bevat de volgende velden:

| Kolom | Beschrijving |
|--- |--- |
| `Hide filters` | Hiermee kunt u alle filters tonen of verbergen die u op het dashboard kunt toepassen. U kunt momenteel alleen het filter toepassen `Last updated`. Met dit filter kunt u een datumbereik voor soorten publiek selecteren op basis van het tijdstip waarop ze voor het laatst zijn bijgewerkt. |
| `Search` | Hiermee kunt u zoeken naar actief publiek in uw Commerce-exemplaar. |
| `Name` | Naam gegeven aan het publiek in Real-Time CDP. |
| `Origin` | Geeft aan waar het publiek vandaan komt, zoals `Experience Platform`. |
| `Websites` | Geeft aan welke websites zijn geconfigureerd om het publiek te gebruiken. |
| `Dynamic Blocks` | Geeft aan welke dynamische blokken zijn geconfigureerd om het publiek te gebruiken. |
| `Cart Price Rules` | Geeft aan welke regels voor de winkelwagenprijs zijn geconfigureerd om het publiek te gebruiken. |
| `Last updated` | Geeft aan wanneer het publiek is gewijzigd in Real-Time CDP. |
| `Sync now` | Hiermee haalt u nieuwe of bijgewerkte soorten publiek op uit Real-Time CDP. |
| `Customize table` | Hiermee kunt u de `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules`, en `Last updated` kolommen. |

{style="table-layout:auto"}

## Hoofdondersteuning

U kunt het publiek in een Adobe Commerce-instantie zonder kop, zoals AEM en PWA, activeren om regels voor de winkelwagenprijs, verwante productregels of dynamische blokken weer te geven die zijn gebaseerd op het publiek.

### Cart price rules and related product rules

Voor de regels betreffende de kartprijs en de desbetreffende productregels geeft een koploze winkel het Experience Platform via de [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Het framework biedt een server-side API die met GraphQL is geïmplementeerd. De informatie van het publiek, zoals het segment van een verkoopster, gaat tot Commerce door een kopbalparameter van GraphQL genoemd over: `aep-segments-membership`.

De architectuur ziet er als volgt uit:

![Gegevens verzenden van Headless Storefront naar Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Na u [installeren](#install-the-extension) en [vormen](#configure-the-extension) Voor de uitbreiding, bevat het Web SDK van het Experience Platform de publieksinformatie in de vorm van segmentlidmaatschap.

Om die segmentlidmaatschappen van SDK te vangen, zie dit [codefragment](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Nadat u de segmenten hebt opgehaald, kunt u deze in de GraphQL-koptekst doorgeven aan Commerce. Bijvoorbeeld:

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

U kunt een Real-Time CDP-publiek ophalen met de Adobe Experience Platform Mobile SDK.

1. [Installeren](#install-the-extension) de extensie Audience Activation.
1. [De SDK voor uw mobiele Commerce-site installeren en configureren](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

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

Nadat de gegevens zijn opgehaald, kunt u deze gebruiken om op de doelgroep gebaseerde gegevens te maken [regels betreffende de kartonprijs](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [dynamische blokken](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) en  [verwante productregels](../merchandising-promotions/product-related-rule-create.md) in de Commerce-app.

## Soorten publiek wordt niet weergegeven in Commerce

Als Real-Time CDP-publiek niet wordt weergegeven in Commerce, kan dit worden veroorzaakt door:

- Onjuist verificatietype geselecteerd in het dialoogvenster **Gegevensverbinding** configuratiepagina
- Onvoldoende rechten voor gegenereerd token

De volgende twee secties beschrijven hoe te om één van beide geval problemen op te lossen.

### Onjuist verificatietype geselecteerd in configuratie

1. Open uw Commerce-exemplaar.
1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Uitbreiden **[!UICONTROL Services]** en selecteert u **[!UICONTROL [!DNL Data Connection]]**.
1. Verzeker de server-aan-server vergunningsmethode die u in specificeerde **[!UICONTROL Authentication Type]** is correct. Adobe raadt u aan **OAuth**. JWT is vervangen. [Meer informatie](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Onvoldoende rechten voor gegenereerd token

Dit probleem kan worden veroorzaakt door onvoldoende API-bevoegdheden voor het gegenereerde token. Om ervoor te zorgen dat het token de juiste rechten heeft:

1. Identificeer de systeembeheerder voor Adobe Experience Platform in uw organisatie.
1. Zoek het project en de geloofsbrieven die u zult gebruiken.
1. Identificeer de e-mail van de technische rekening, bijvoorbeeld: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Laat de systeembeheerder Adobe Experience Platform starten en ga naar **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Zoek met behulp van de e-mail over de technische account van boven naar de referenties die u wilt wijzigen.
1. Open de referenties en selecteer **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. De rol toevoegen die **[!UICONTROL Manage destinations]** toestemming.
1. Klik op **[!UICONTROL Save]**.
1. [Regenereren](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) het toegangstoken in Console.
1. Controleer of het token een geldige reactie biedt met de functie [API voor doelverbindingen](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
