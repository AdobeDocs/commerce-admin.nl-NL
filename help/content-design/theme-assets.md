---
title: Themaelementen
description: Leer hoe u uw thema-elementen beheert, zoals CSS-, lettertypen-, afbeeldings- en JavaScript-bestanden.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: e50b85311f4512fb54c7cb29faf6136eaf07eae6
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Themaelementen

De _statische dossiers_ zijn de inzameling van activa, zoals CSS, doopvonten, beelden, en JavaScript die door een thema wordt gebruikt. De plaats van statische dossiers wordt gespecificeerd in de [ Basis URL ](../stores-purchase/store-urls.md) configuratie. U kunt een digitale handtekening toevoegen aan de URL van elk statisch bestand, zodat browsers kunnen detecteren wanneer een nieuwere versie beschikbaar is. De nieuwere versie van het bestand wordt gebruikt als de handtekening afwijkt van de versie die in de cache van de browser is opgeslagen.

Voor een standaardinstallatie worden de elementen die aan een thema zijn gekoppeld, ingedeeld in de map `web` op de volgende locatie onder de [!DNL Commerce] -hoofdmap.

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Een digitale handtekening toevoegen aan statische bestand-URL&#39;s

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Developer]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Static Files Settings]** sectie uit.

   ![ de Statische Montages van Dossiers ](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Stel **[!UICONTROL Sign Static Files]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

| Bestandstype | Beschrijving |
|--- |--- |
| CSS | Hiermee bepaalt u de visuele opmaak die aan de skin is gekoppeld. Voorbeeldlocatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Lettertypen | Geef de lettertypen op die beschikbaar zijn voor gebruik door het thema. Locatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Afbeeldingen | Geef de grafische elementen op die door het thema worden gebruikt, zoals knoppen, achtergrondstructuren, enzovoort. Voorbeeldlocatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Thema-specifieke JavaScript routines en callable functies. Voorbeeldlocatie op de server: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## CSS-bestanden samenvoegen

Als onderdeel van een poging om uw site te optimaliseren en de laadtijd van de pagina te verminderen, kunt u het aantal afzonderlijke CSS-bestanden verminderen door deze samen te voegen tot één gecomprimeerd bestand. Als u een samengevoegd CSS-bestand opent, ziet u één doorlopende tekststroom, waarbij regeleinden zijn verwijderd. U kunt het samengevoegde bestand niet bewerken. U kunt het beste wachten totdat u de ontwikkelingsmodus verlaat en niet meer regelmatig wijzigingen in de CSS aanbrengt.

>[!NOTE]
>
>CSS de dossiers kunnen van het _Admin_ paneel slechts worden samengevoegd wanneer het werken op [ ontwikkelaarwijze ](../systems/developer-tools.md#operation-modes).

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerpaneel, **[!UICONTROL Advanced]** en kies **[!UICONTROL Developer]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL CSS Settings]** sectie uit.

   ![ CSS Montages ](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Voor gedetailleerde beschrijvingen van deze configuratieopties, zie [ CSS Montages ](../configuration-reference/advanced/developer.md#css-settings) in de _Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Merge CSS Files]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## JavaScript-bestanden samenvoegen

Meerdere JavaScript-bestanden kunnen worden samengevoegd tot één, versmald bestand om de laadtijd van de pagina te beperken. Als u een samengevoegd JavaScript-bestand opent, ziet u één doorlopende tekststroom, waarbij regeleinden zijn verwijderd. Als u klaar bent met het ontwikkelingsproces en de code geen fouten bevat, kunt u overwegen de bestanden samen te voegen.

>[!NOTE]
>
>De dossiers van JavaScript kunnen van het _Admin_ paneel slechts worden samengevoegd wanneer het werken op [ Wijze van de Ontwikkelaar ](../systems/developer-tools.md#operation-modes).

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerpaneel, **[!UICONTROL Advanced]** en kies **[!UICONTROL Developer]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL JavaScript Settings]** sectie uit.

   ![ de Montages van JavaScript ](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Voor gedetailleerde beschrijvingen van deze configuratieopties, zie [ de Montages van JavaScript ](../configuration-reference/advanced/developer.md#javascript-settings) in de _Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Merge JavaScript Files]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
