---
title: Productvideo's toevoegen
description: Leer hoe u productvideo's voor uw winkel kunt configureren. Hiervoor is een YouTube API-sleutel van een Google-account vereist en u voegt een videokoppeling voor een product toe.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Productvideo&#39;s toevoegen

Als u een productvideo wilt toevoegen, moet u eerst een API-sleutel verkrijgen van uw Google-account en deze invoeren in de configuratie van uw winkel. Vervolgens kunt u een koppeling maken naar de video van het product.

## Stap 1: De YouTube API-sleutel ophalen

1. Login aan uw rekening van Google en bezoek de [ Console van de Ontwikkelaars van Google ][1].

1. Typ `YouTube Data API v3` in het zoekveld bovenaan en klik op het zoekpictogram.

1. Zorg dat de API-pagina is ingeschakeld wanneer deze wordt weergegeven.

1. Kies **[!UICONTROL Credentials]** in het linkerdeelvenster.

1. Afhankelijk van of u geloofsbrieven hebt of niet, doe één van het volgende:

   - Als u reeds de vereiste geloofsbrieven hebt, kopieer de sleutel in de _API sleutels_ lijst.

   - Als u nog geen gegevens voor deze API hebt, klikt u op **[!UICONTROL Create Credentials]** boven aan het scherm en volgt u de aanwijzingen om de benodigde gegevens te maken. Onder _krijg uw geloofsbrieven_, kopieer de API sleutel en klik **[!UICONTROL Done]**.

1. Kopieer de API-sleutel naar het klembord.

1. Klik op het pictogram Bewerken aan de rechterkant en stel de beperkingen in om ervoor te zorgen dat de API-sleutel beperkt is tot de juiste referenties.

1. Wacht even terwijl de sleutel wordt geproduceerd en kopieer dan de sleutel aan het klembord.

   In de volgende stap plakt u de sleutel in de configuratie van uw winkel.

## Stap 2: De sleutel configureren in Commerce

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de _[!UICONTROL Product Video]_sectie uit en kleef uw **[!UICONTROL YouTube API key]**.

   ![ de Videoconfiguratie van het Product ](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Vernieuw de cache wanneer daarom wordt gevraagd.

## Stap 3: Koppeling naar de video

1. Open een product in de bewerkingsmodus.

1. Blader naar de sectie _[!UICONTROL Images and Videos]_en vouw deze uit.

   ![ Beelden en Video&#39;s ](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Add Video]** .

   Als u de YouTube API-sleutel nog niet hebt geconfigureerd, klikt u op **[!UICONTROL OK]** om door te gaan. U kunt geen koppeling maken naar een YouTube-video, maar u kunt wel het proces doorlopen.

1. Voer bij **[!UICONTROL Url]** de URL in van de YouTube- of Vimeo-video.

   ![ Nieuwe video voor product ](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Klik buiten het veld en wacht op feedback op de API-sleutel of -video.

   Als alles uitcheckt, verschaft YouTube basisinformatie van de video

1. Voer de **[!UICONTROL Title]** en **[!UICONTROL Description]** van de video in.

1. Als u een **[!UICONTROL Preview Image]** wilt uploaden, bladert u naar de afbeelding en selecteert u het bestand.

   >[!NOTE]
   >
   >Na het uploaden wordt de weergegeven voorvertoning automatisch gegenereerd door een extern videoservicebureau. U kunt de afbeelding niet bewerken via Adobe Commerce Admin.

1. Klik op **[!UICONTROL Get Video Information]** als u liever de metagegevens van de video wilt gebruiken.

1. Als u wilt bepalen hoe de video wordt gebruikt in de winkel, schakelt u het selectievakje in van elke video die van toepassing is: **[!UICONTROL Role]**

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   >[!NOTE]
   >
   >Als de configuratieoptie _[!UICONTROL Autostart base video]_is ingesteld op `Yes` maar de video niet automatisch begint af te spelen, kan dit worden veroorzaakt door het automatisch afspeelbeleid dat door de browser wordt afgedwongen en dat niet door Adobe Commerce kan worden beheerd. Elke ondersteunde browser heeft een eigen beleid voor automatisch afspelen dat in de loop der tijd kan worden gewijzigd en de video wordt in de toekomst mogelijk niet automatisch afgespeeld. Als geadviseerde beste praktijken, zou u niet op autoplay voor bedrijfskritieke functionaliteit moeten vertrouwen en zou het videogedrag in uw opslag met elke gesteunde browser moeten testen.

## API-toegang behouden

Volgens de de ontwikkelaar van Google [ Algemene Voorwaarden ], kan YouTube API toegang voor rekeningen onbruikbaar maken die meer dan 90 dagen inactief zijn geweest. Dit kan ertoe leiden dat uw video&#39;s niet worden weergegeven. Als u de API-toegang up-to-date wilt houden, gebruikt u een snijtaak om de API regelmatig te pingelen:

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## Veldverwijzing

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL URL] | De URL van de gekoppelde video. |
| [!UICONTROL Title] | De titel van de video. |
| [!UICONTROL Description] | De videobeschrijving. |
| [!UICONTROL Preview Image] | Een geüploade afbeelding die wordt gebruikt als voorvertoning van de video in uw winkel. |
| [!UICONTROL Get Video Information] | Hiermee worden de metagegevens van de video opgehaald die op de hostserver zijn opgeslagen. U kunt de oorspronkelijke gegevens gebruiken of zo nodig bijwerken. |
| [!UICONTROL Role] | Hiermee bepaalt u hoe de voorvertoning wordt gebruikt in de winkel. U kunt een willekeurige combinatie van opties kiezen: `Base Image` , `Small Image` , `Thumbnail` , `Swatch Image` , `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[Voorwaarden en bepalingen]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
