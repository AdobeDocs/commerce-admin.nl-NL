---
title: Themaelementen
description: Leer hoe u thema-elementen, zoals CSS-, lettertypen-, afbeeldingen- en JavaScript-bestanden, beheert.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Themaelementen

De _statische bestanden_ Dit zijn de verzameling elementen, zoals CSS, lettertypen, afbeeldingen en JavaScript die door een thema worden gebruikt. De locatie van statische bestanden wordt opgegeven in het dialoogvenster [Basis-URL](../stores-purchase/store-urls.md) configuratie. U kunt een digitale handtekening toevoegen aan de URL van elk statisch bestand, zodat browsers kunnen detecteren wanneer een nieuwere versie beschikbaar is. De nieuwere versie van het bestand wordt gebruikt als de handtekening afwijkt van de versie die in de cache van de browser is opgeslagen.

Voor een standaardinstallatie worden de elementen die aan een thema zijn gekoppeld, ingedeeld in de categorie `web` map op de volgende locatie onder de [!DNL Commerce] hoofdmap.

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Een digitale handtekening toevoegen aan statische bestand-URL&#39;s

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Developer]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Static Files Settings]** sectie.

   ![Instellingen Statische bestanden](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Set **[!UICONTROL Sign Static Files]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.

| Bestandstype | Beschrijving |
|--- |--- |
| CSS | Hiermee bepaalt u de visuele opmaak die aan de skin is gekoppeld. Voorbeeldlocatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Lettertypen | Geef de lettertypen op die beschikbaar zijn voor gebruik door het thema. Locatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Afbeeldingen | Geef de grafische elementen op die door het thema worden gebruikt, zoals knoppen, achtergrondstructuren, enzovoort. Voorbeeldlocatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Themaspecifieke JavaScript-routines en aanroepbare functies. Voorbeeldlocatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## CSS-bestanden samenvoegen

Als onderdeel van een poging om uw site te optimaliseren en de laadtijd van de pagina te verminderen, kunt u het aantal afzonderlijke CSS-bestanden verminderen door deze samen te voegen tot één gecomprimeerd bestand. Als u een samengevoegd CSS-bestand opent, ziet u één doorlopende tekststroom, waarbij regeleinden zijn verwijderd. U kunt het samengevoegde bestand niet bewerken. U kunt het beste wachten totdat u de ontwikkelingsmodus verlaat en niet meer regelmatig wijzigingen in de CSS aanbrengt.

>[!NOTE]
>
>CSS-bestanden kunnen worden samengevoegd vanuit de _Beheerder_ alleen in het deelvenster [ontwikkelmodus](../systems/developer-tools.md#operation-modes).

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerpaneel, **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Developer]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL CSS Settings]** sectie.

   ![CSS-instellingen](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Voor gedetailleerde beschrijvingen van deze configuratieopties, zie [CSS-instellingen](../configuration-reference/advanced/developer.md#css-settings) in de _Configuratieverwijzing_.

1. Set **[!UICONTROL Merge CSS Files]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.

## JavaScript-bestanden samenvoegen

U kunt meerdere JavaScript-bestanden samenvoegen tot één verkort bestand om de laadtijd van de pagina te beperken. Als u een samengevoegd JavaScript-bestand opent, ziet u één doorlopende tekststroom, waarbij regeleinden zijn verwijderd. Als u klaar bent met het ontwikkelingsproces en de code geen fouten bevat, kunt u overwegen de bestanden samen te voegen.

>[!NOTE]
>
>JavaScript-bestanden kunnen worden samengevoegd vanuit de _Beheerder_ alleen in het deelvenster [Modus voor ontwikkelaars](../systems/developer-tools.md#operation-modes).

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerpaneel, **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Developer]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL JavaScript Settings]** sectie.

   ![JavaScript-instellingen](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Voor gedetailleerde beschrijvingen van deze configuratieopties, zie [JavaScript-instellingen](../configuration-reference/advanced/developer.md#javascript-settings) in de _Configuratieverwijzing_.

1. Set **[!UICONTROL Merge JavaScript Files]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.
