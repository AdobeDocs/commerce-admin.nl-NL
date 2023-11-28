---
title: Productvideo's toevoegen
description: Leer hoe u productvideo's voor uw winkel kunt configureren. Hiervoor is een YouTube API-sleutel van een Google-account vereist en u voegt een videokoppeling voor een product toe.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Productvideo&#39;s toevoegen

Als u een productvideo wilt toevoegen, moet u eerst een API-sleutel verkrijgen van uw Google-account en deze invoeren in de configuratie van uw winkel. Vervolgens kunt u een koppeling maken naar de video van het product.

## Stap 1: De YouTube API-sleutel ophalen

1. Meld u aan bij uw Google-account en ga naar [Google Developers Console][1].

1. Typ in het zoekveld bovenaan `YouTube Data API v3` en klik op het zoekpictogram.

1. Zorg dat de API-pagina is ingeschakeld wanneer deze wordt weergegeven.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Credentials]**.

1. Afhankelijk van of u geloofsbrieven hebt of niet, doe één van het volgende:

   - Als u al over de vereiste gegevens beschikt, kopieert u de sleutel in het dialoogvenster _API-sleutels_ tabel.

   - Als u nog geen gegevens voor deze API hebt, klikt u op **[!UICONTROL Create Credentials]**  bovenaan en volgt u de aanwijzingen om de vereiste referenties te maken. Onder _Uw referenties ophalen_, kopieer de API-sleutel en klik op **[!UICONTROL Done]**.

1. Kopieer de API-sleutel naar het klembord.

1. Klik op het pictogram Bewerken aan de rechterkant en stel de beperkingen in om ervoor te zorgen dat de API-sleutel beperkt is tot de juiste referenties.

1. Wacht even terwijl de sleutel wordt geproduceerd en kopieer dan de sleutel aan het klembord.

   In de volgende stap plakt u de sleutel in de configuratie van uw winkel.

## Stap 2: Vorm de sleutel in Handel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Product Video]_sectie en plak uw **[!UICONTROL YouTube API key]**.

   ![Productvideoconfiguratie](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

1. Vernieuw de cache wanneer daarom wordt gevraagd.

## Stap 3: Koppeling naar de video

1. Open een product in de bewerkingsmodus.

1. Naar de _[!UICONTROL Images and Videos]_sectie.

   ![Afbeeldingen en video&#39;s](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. klikken **[!UICONTROL Add Video]**.

   Als u de YouTube API-sleutel nog niet hebt geconfigureerd, klikt u op **[!UICONTROL OK]** om door te gaan. U kunt geen koppeling maken naar een YouTube-video, maar u kunt wel het proces doorlopen.

1. Voor **[!UICONTROL Url]** Voer de URL van de YouTube- of Vimeo-video in.

   ![Nieuwe video voor product](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Klik buiten het veld en wacht op feedback op de API-sleutel of -video.

   Als alles uitcheckt, verschaft YouTube basisinformatie van de video

1. Voer de **[!UICONTROL Title]** en **[!UICONTROL Description]** van de video.

1. Als u een **[!UICONTROL Preview Image]**, bladert u naar de afbeelding en selecteert u het bestand.

   >[!NOTE]
   >
   >Na het uploaden wordt de weergegeven voorvertoning automatisch gegenereerd door een extern videoservicebureau. U kunt de afbeelding niet bewerken via Adobe Commerce Admin.

1. Als u liever de metagegevens van de video wilt gebruiken, klikt u op **[!UICONTROL Get Video Information]**.

1. Om te bepalen hoe de video in de opslag wordt gebruikt, selecteer checkbox van elk **[!UICONTROL Role]** dat geldt voor:

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. Klik op **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Als de _[!UICONTROL Autostart base video]_configuratieoptie is ingesteld op `Yes` maar de video wordt niet automatisch afgespeeld, dit kan het gevolg zijn van het automatisch afspeelbeleid dat wordt afgedwongen door de browser en dat niet kan worden beheerd door Adobe Commerce. Elke ondersteunde browser heeft een eigen beleid voor automatisch afspelen dat in de loop der tijd kan worden gewijzigd en de video wordt in de toekomst mogelijk niet automatisch afgespeeld. Als geadviseerde beste praktijken, zou u niet op autoplay voor bedrijfskritieke functionaliteit moeten vertrouwen en zou het videogedrag in uw opslag met elke gesteunde browser moeten testen.

## API-toegang behouden

Volgens de Google-ontwikkelaar [Voorwaarden en bepalingen], kan YouTube API-toegang uitschakelen voor accounts die langer dan 90 dagen inactief zijn geweest. Dit kan ertoe leiden dat uw video&#39;s niet worden weergegeven. Als u de API-toegang up-to-date wilt houden, gebruikt u een snijtaak om de API regelmatig te pingelen:

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
| [!UICONTROL Role] | Hiermee bepaalt u hoe de voorvertoning wordt gebruikt in de winkel. U kunt een willekeurige combinatie van opties kiezen: `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[Voorwaarden en bepalingen]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
