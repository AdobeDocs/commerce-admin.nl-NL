---
title: "[!DNL Audience Activation]"
description: Leer hoe u het Real-Time CDP-publiek in Adobe Commerce activeert om personalisatie in uw winkel te stimuleren.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: 9f351ab659b21377310f8327fef5bc29cc9f7c89
workflow-type: tm+mt
source-wordcount: '1516'
ht-degree: 0%

---

# [!DNL Audience Activation]

Met de extensie [!DNL Audience Activation] kunt u het Real-Time CDP-publiek in Adobe Commerce activeren en unieke aanbiedingen in het winkelwagentje maken. Deze aanbiedingen en de prikkels omvatten gemeenschappelijke e-handel die technieken, zoals _koopt 2 krijgt 1 vrije_, heldenbanners die op die klant worden gericht, en gewijzigde productprijs door diverse aanbiedingen. Het publiek dat in Real-Time CDP is samengesteld, is gebaseerd op gegevens van verschillende bedrijfssystemen, zoals Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), verkooppunten en marketingsystemen. Omdat de informatie van het klantensegment constant wordt verfrist, kunnen de klanten van een segment worden geassocieerd en worden losgemaakt aangezien zij in uw opslag winkelen.

U kunt publiek in een Luma storefront of [ zonder kop ](#headless-support) storefront activeren. In een Luma-winkel wordt de publieksinformatie (segmentlidmaatschap) opgeslagen in een cookie aan de Commerce-zijde. In een koploze winkel wordt publieksinformatie doorgegeven in de GraphQL API-header als een parameter met de naam: `aep-segments-membership` .

## Opmerkingen bij de release

Deze sectie bevat informatie over updates voor de extensie Audience Activation en bevat:

![ Nieuw ](../assets/new.svg) - Nieuwe eigenschappen
![ Repareren ](../assets/fix.svg) - Oplossingen en verbeteringen
![ Bug ](../assets/bug.svg) - Bekende kwesties

Zie [ Komende Versies ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) om over versieschema&#39;s en steun te leren.

Zie de ontwikkelaarsdocumentatie aan [ over productverenigbaarheid ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) leren.

## Ondersteunde service-updates

In deze releaseopmerkingen worden wijzigingen in de functies en correcties beschreven die betrekking hebben op extensies die door het Audience Activation worden gebruikt.

+++Ondersteunde service-updates

_Augustus 15, 2023_

![ Repareren ](../assets/fix.svg) - werkte het [ dashboard van het Soorten Soorten publiek van Real-Time CDP ](#real-time-cdp-audiences-dashboard) bij om het filtreren te vereenvoudigen.

_Juni 27, 2023_

![ Repareren ](../assets/fix.svg) - Toegevoegde steun voor PHP 8.2 in het `magento/module-data-services-graphql` pakket.

_30 Mei, 2023_

![ Nieuw ](../assets/new.svg) - Bijgewerkt het [ dashboard van het Soorten Soorten publiek van Real-Time CDP ](#real-time-cdp-audiences-dashboard) om de capaciteit te omvatten, het actieve publiek binnen uw instantie van Adobe Commerce te sorteren, te zoeken en te filtreren.

+++

### 2.2.0.

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_12 Juni, 2024_

![ Nieuw ](../assets/new.svg) - de versie van GA voor [ verwante productregels ](../merchandising-promotions/product-related-rule-create.md) die door publiek worden geïnformeerd.

### 2.1.1.

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_4 April, 2024_

![ Nieuw ](../assets/new.svg) - Toegevoegde steun voor PHP 8.3.

### 2.2.0-bèta1

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_16 februari 2024_

![ Nieuw ](../assets/new.svg) - als u aan bèta deelneemt, zorg ervoor uw `composer.json` dossier het volgende op het wortelniveau heeft: ` "minimum-stability": "beta"`.
![ Nieuw ](../assets/new.svg) - (**Beta**) toegevoegde capaciteit om [ verwante productregels ](../merchandising-promotions/product-related-rule-create.md) tot stand te brengen die door publiek worden geïnformeerd.

### 2.1.0.

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_Januari 24, 2024_

![ Nieuw ](../assets/new.svg) - Bijgewerkt het [ dashboard van het Soorten Soorten publiek van Real-Time CDP ](#real-time-cdp-audiences-dashboard) om de websites te omvatten die het publiek bevatten en specificeren welke dynamische blokken en de regels van de kartprijs worden gevormd om die soorten publiek te gebruiken.

### 2.0.1.

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_16 november 2023_

![ Repareren ](../assets/fix.svg) - Verbeterde stabiliteit.

### 2.0.0.

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_10 oktober, 2023_

![ Nieuw ](../assets/new.svg) - Toegevoegde steun voor OAuth 2.0 wanneer u [ ](#configure-the-extension) de uitbreiding van het Audience Activation vormt.
![ Repareren ](../assets/fix.svg) - Verbeterde stabiliteit.

### 1.2.0.

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

_Augustus 15, 2023_

![ Repareren ](../assets/fix.svg) - werkte de UI componentenversie bij.

### 1.1.0.

_30 Mei, 2023_

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

![ Nieuw ](../assets/new.svg) - Toegevoegde steun voor [ dynamische blokken ](#headless-support) in een headless storefront.

### 1.0.1.

_Mei 11, 2023_

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

![ bevestig ](../assets/fix.svg) - Vaste een kwestie waar een dynamisch blok of de regel van de kartprijs niet op de storefront werd toegepast.
![ Bevestig ](../assets/fix.svg) - Vloedigde een kwestie waar een niet gevormde installatie van de uitbreiding van het Audience Activation een fout veroorzaakte wanneer een handelaar probeerde om een dynamisch blok tot stand te brengen of bij te werken.

### 1.0.0.

_Maart 31, 2023_

[!BADGE  Verenigbaarheid ]{type=Informative tooltip="Compatibiliteit"}

![ Nieuw ](../assets/new.svg) - Algemene beschikbaarheidsversie

## Implementatie

De volgende taken zijn van toepassing op zowel de uitvoeringen van het Luma als van het hoofdloze winkelcentrum. Als u het publiek in Adobe Commerce wilt activeren, moet u:

- Adobe Commerce versie 2.4.4 of hoger installeren
- [ activeer ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce als bestemming in Real-Time CDP
- [ installeer ](#install-the-extension) de [!DNL Audience Activation] uitbreiding in Admin
- [ vorm ](#configure-the-extension) de [!DNL Audience Activation] uitbreiding in Admin

### De extensie installeren

Installeer de [!DNL Audience Activation] uitbreiding van [ marktPlace ](https://commercemarketplace.adobe.com/magento-audiences.html), of stel het volgende bevel in werking:

```bash
composer require magento/audiences
```

### De extensie configureren

Nadat u de extensie [!DNL Audience Activation] hebt geïnstalleerd, moet u zich aanmelden bij uw Commerce-beheerder en het volgende invullen:

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [ Teken binnen ](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) aan uw rekening van de Adobe en selecteer uw organisatieidentiteitskaart

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. Op het **[!UICONTROL Datastream ID]** gebied, kleef identiteitskaart van de gegevensstroom die u creeerde toen u [ ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce als bestemming in Real-Time CDP activeerde.

   Deze gegevensstroom verzendt gegevens van uw Commerce-website naar Real-Time CDP om te bepalen of een klant tot een publiek behoort. Als u nog geen gegevensstroom hebt gecreeerd, [ creeer ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) in Experience Platform, [ voeg ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) het aan de bestemming van Commerce in Real-Time CDP toe, en aan de [[!DNL Data Connection] ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) uitbreiding in Admin.

   >[!NOTE]
   >
   >Wanneer u een gegevensstroomidentiteitskaart specificeert, associeert u [ het aan een specifieke website ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) in de [!DNL Data Connection] uitbreiding. Als uw opslag van Commerce veelvoudige websites heeft, [ creeer een bestemming ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) voor elke website in Real-Time CDP en gebruik verschillende gegevensstroom identiteitskaart voor elk.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw **[!UICONTROL Services]** uit en selecteer **[!UICONTROL [!DNL Data Connection]]** .

1. [ voeg ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) de dienstrekening en credentiedetails toe.

## Waar kan het Real-Time CDP-publiek in Commerce worden gebruikt?

Als de extensie [!DNL Audience Activation] is ingeschakeld, kunt u:

- [ creeer een regel van de kartprijs ](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) die door publiek wordt geïnformeerd
- [ creeer een dynamisch blok ](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) dat door publiek wordt geïnformeerd
- [ creeer een verwante productregel ](../merchandising-promotions/product-related-rule-create.md) die door publiek wordt geïnformeerd

>[!TIP]
>
>Voor een volledig gebruiksgeval van begin tot eind over hoe te om [!DNL Commerce] gegevens naar Real-Time CDP uit te voeren, bouwt een publiek, dan activeert dat publiek aan [!DNL Commerce], zie [ een publiek in Real-Time CDP creëren gebruikend  [!DNL Commerce]  gebeurtenisgegevens ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience).

## Real-Time CDP-doeldashboard

U kunt alle [ actieve ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) publiek bekijken dat beschikbaar is om binnen uw instantie van Adobe Commerce te personaliseren gebruikend het **3} dashboard van het Soorten publiek van Real-Time CDP {.**

Om tot het **publiek van Real-Time CDP** dashboard toegang te hebben, ga naar _Admin_ sidebar, dan ga **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![ het Dashboard van het Soorten Soorten publiek van Real-Time CDP ](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Het dashboard bevat de volgende velden:

| Kolom | Beschrijving |
|--- |--- |
| `Hide filters` | Hiermee kunt u alle filters tonen of verbergen die u op het dashboard kunt toepassen. Het enige filter dat u op dit moment kunt toepassen, is `Last updated` . Met dit filter kunt u een datumbereik voor soorten publiek selecteren op basis van het tijdstip waarop ze voor het laatst zijn bijgewerkt. |
| `Search` | Hiermee kunt u zoeken naar actief publiek in uw Commerce-exemplaar. |
| `Name` | Naam gegeven aan het publiek in Real-Time CDP. |
| `Origin` | Geeft aan waar het publiek vandaan kwam, zoals `Experience Platform` . |
| `Websites` | Geeft aan welke websites zijn geconfigureerd om het publiek te gebruiken. |
| `Dynamic Blocks` | Geeft aan welke dynamische blokken zijn geconfigureerd om het publiek te gebruiken. |
| `Cart Price Rules` | Geeft aan welke regels voor de winkelwagenprijs zijn geconfigureerd om het publiek te gebruiken. |
| `Related Product Rules` | Geeft aan welke gerelateerde productregels zijn geconfigureerd om het publiek te gebruiken. |
| `Last updated` | Geeft aan wanneer het publiek is gewijzigd in Real-Time CDP. |
| `Sync now` | Hiermee haalt u nieuwe of bijgewerkte soorten publiek op uit Real-Time CDP. |
| `Customize table` | Hiermee kunt u de kolommen `Origin` , `Websites` , `Dynamic Blocks` , `Cart Price Rules` en `Last updated` weergeven of verbergen. |

{style="table-layout:auto"}

## Hoofdondersteuning

U kunt het publiek in een Adobe Commerce-instantie zonder kop, zoals AEM en PWA, activeren om regels voor de winkelwagenprijs, verwante productregels of dynamische blokken weer te geven die zijn gebaseerd op het publiek.

### Cart price rules and related product rules

Voor de regels van de kartprijs en verwante productregels, communiceert een headless storefront aan het Experience Platform door het [ Commerce integration framework (CIF) ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Het framework biedt een server-side API die met GraphQL is geïmplementeerd. Publiek-informatie, zoals het segment van een klant, gaat naar Commerce via een GraphQL-headerparameter genaamd: `aep-segments-membership` .

De architectuur ziet er als volgt uit:

![ verzendend Gegevens van Hoofdloze Storefront aan Achtergrond ](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Nadat u [ ](#install-the-extension) installeert en [ ](#configure-the-extension) de uitbreiding vormt, bevat het Web SDK van het Experience Platform de publieksinformatie in de vorm van segmentlidmaatschap.

Om die segmentlidmaatschap van SDK te vangen, zie dit [ codefragment ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Nadat u de segmenten hebt opgehaald, kunt u deze in de GraphQL-koptekst doorgeven aan Commerce. Bijvoorbeeld:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamische blokken

Voor dynamische blokken kunnen GraphQL `dynamicBlocks` -query&#39;s het invoerkenmerk `audience_id` bevatten. Als u een of meer `audience_id` -waarden opgeeft in een `dynamicBlocks` -query, wordt een lijst met dynamische blokken geretourneerd die aan dat publiek zijn toegewezen.

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

Leer meer over de `dynamicBlocks` vraag van GraphQL in de [ ontwikkelaardocumentatie ](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Soorten publiek ophalen met de Adobe Experience Platform Mobile SDK

U kunt een Real-Time CDP-publiek ophalen met de Adobe Experience Platform Mobile SDK.

1. [ installeer ](#install-the-extension) de uitbreiding van het Audience Activation.
1. [ installeer en vorm SDK voor uw mobiele plaats van Commerce ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

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

Nadat het gegeven wordt teruggewonnen, kunt u het gebruiken om publiek-geïnformeerde [ regels van de wortelprijs ](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) tot stand te brengen, [ dynamische blokken ](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) en [ verwante productregels ](../merchandising-promotions/product-related-rule-create.md) in Commerce app.

## Soorten publiek wordt niet weergegeven in Commerce

Als Real-Time CDP-publiek niet wordt weergegeven in Commerce, kan dit worden veroorzaakt door:

- Ongeldige verbinding
- Onjuist die authentificatietype in de **configuratiepagina van de Verbinding van 0} wordt geselecteerd**
- Onvoldoende rechten voor gegenereerd token

In de volgende secties wordt beschreven hoe u deze problemen kunt oplossen.

### De verbinding valideren

Voer de volgende opdracht uit om de referenties en het antwoord van Adobe Experience Platform te valideren:

```bash
bin/magento audiences:config:status
```

Dit bevel keert de verbindingsstatus terug. Voeg de markering `-v` toe voor extra breedtegraad:

```
./bin/magento audiences:config:status -v  
```

Bijvoorbeeld:

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### Onjuist verificatietype geselecteerd in configuratie

1. Open uw Commerce-exemplaar.
1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Vouw **[!UICONTROL Services]** uit en selecteer **[!UICONTROL [!DNL Data Connection]]** .
1. Controleer of de machtigingsmethode van server naar server die u in het veld **[!UICONTROL Authentication Type]** hebt opgegeven correct is. Adobe adviseert gebruikend **OAuth**. JWT is vervangen. [ leer meer ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Onvoldoende rechten voor gegenereerd token

Dit probleem kan worden veroorzaakt door onvoldoende API-bevoegdheden voor het gegenereerde token. Om ervoor te zorgen dat het token de juiste rechten heeft:

1. Identificeer de systeembeheerder voor Adobe Experience Platform in uw organisatie.
1. Zoek het project en de geloofsbrieven die u zult gebruiken.
1. Identificeer de e-mail naar de technische account, bijvoorbeeld: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com` .
1. Laat de systeembeheerder Adobe Experience Platform starten en ga naar **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]** .
1. Zoek met behulp van de e-mail over de technische account van boven naar de referenties die u wilt wijzigen.
1. Open de referenties en selecteer vervolgens **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]** .
1. Voeg de rol toe die **[!UICONTROL Manage destinations]** toestemming bevat.
1. Klik op **[!UICONTROL Save]**.
1. [ Regenereer ](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) het toegangstoken in Console.
1. Verifieer dat het teken een geldige reactie gebruikend [ Verbinding API van het Doel ](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections) verstrekt.
