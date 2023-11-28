---
title: Widgets maken en beheren
description: Leer hoe u widgets maakt en beheert die automatisch inhoud in uw winkel bijwerken.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Widgets maken en beheren

Widgets zijn herbruikbare componenten. U kunt eenvoudig widgets maken en bestaande widgets wijzigen om inhoud in uw winkel automatisch bij te werken. U kunt ook widgets verwijderen die niet meer in gebruik zijn.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Een widget maken

Het proces voor het maken van een widget is vrijwel hetzelfde voor elke widget [widgettype](widgets.md#widget-types). U kunt het eerste deel van de instructies volgen en vervolgens het laatste deel voor het specifieke type widget voltooien.

### Stap 1: Kies het type

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik op **[!UICONTROL Add Widget]**.

1. In de _[!UICONTROL Settings]_sectie:

   - Set **[!UICONTROL Type]** op het widgettype dat u wilt maken.

   - Controleer of de **[!UICONTROL Design Theme]** wordt ingesteld op het huidige thema.

     ![Widget-instellingen](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Continue]**.

### Stap 2: Eigenschappen en lay-out van storefront opgeven

1. In de _[!UICONTROL Storefront Properties]_sectie:

   - Voor **[!UICONTROL Widget Title]**, voert u een beschrijvende titel in voor de widget.

     Deze titel is alleen zichtbaar vanuit de beheerder.

   - Voor **[!UICONTROL Assign to Store Views]** selecteert u de winkelweergaven waarin u de widget zichtbaar wilt maken.

     U kunt een specifieke winkelweergave selecteren, of `All Store Views`. Als u meerdere weergaven wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   - (Optioneel) Voor **[!UICONTROL Sort Order]** Voer een getal in om de volgorde te bepalen waarin dit item wordt weergegeven met andere items op hetzelfde deel van de pagina. (`0` = eerst, `1` = seconde, `3` = derde, enzovoort.)

     ![Eigenschappen van Storefront](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. In de _[!UICONTROL Layout Updates]_sectie, klikken **[!UICONTROL Add Layout Update]**.

1. Set **[!UICONTROL Display On]** op het paginatype waar het moet verschijnen.

1. In de **[!UICONTROL Container]** kiest u het gebied van de paginalay-out waar u de pagina wilt plaatsen.

   ![Layout-updates](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Als de widget een koppeling is, stelt u **[!UICONTROL Template]** op een van de volgende wijzen:

   - `Block Template` - Hiermee wordt de inhoud opgemaakt, zodat deze als zelfstandige eenheid op de pagina kan worden geplaatst.
   - `Inline Template` - Maakt de inhoud op, zodat deze in andere inhoud kan worden geplaatst. Bijvoorbeeld een koppeling die zich in een alinea met tekst bevindt.

### Stap 3: Voltooi de widgetopties

De opties voor elk widgettype variëren enigszins, maar het proces is in wezen hetzelfde. In het volgende voorbeeld wordt de productlijst voor een specifieke categorie weergegeven, met pagineringsbesturingselementen.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Widget Options]**.

1. Klik op **[!UICONTROL Select Block]**.

1. Voer een **[!UICONTROL Title]** boven de lijst weergeven, zoals `Featured Products`.

1. Voor pagineringsbesturingselementen stelt u **[!UICONTROL Display Page Control]** tot `Yes`  en voer de volgende handelingen uit:

   - Voer de **[!UICONTROL Number of Products per Page]**.

   - Voer het totaal in **[!UICONTROL Number of Products to Display]**.

   - Set **[!UICONTROL Condition]** op de categorie producten die moet worden vermeld.

     Het proces is hetzelfde als het instellen van een voorwaarde voor een [prijsregel](../merchandising-promotions/price-rules-catalog.md).

### Stap 4: Het resultaat opslaan en controleren

1. Klik op **[!UICONTROL Save]**.

1. Volg desgevraagd de instructies boven aan de werkruimte om de cache zo nodig bij te werken.

1. Ga terug naar uw winkel om te controleren of de widget correct werkt.

   Als u de widget naar een andere locatie wilt verplaatsen, kunt u de widget opnieuw openen en een andere pagina of blokverwijzing proberen.

## Demo voor maken van widget

Bekijk deze video voor meer informatie over het maken van widgets:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## Een widget bewerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Zoek de widget met behulp van de filters boven het raster en klik op de naam van de widget.

1. Breng de gewenste wijzigingen aan.

   Controleer de stappen voor het maken van een widget voor informatie over de widgetopties.

1. Klik op de knop **[!UICONTROL Save]**.

## Een widget verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Zoek de widgets met behulp van de filters boven het raster en schakel vervolgens het selectievakje in van de widgets die u wilt verwijderen.

1. In de linkerbovenhoek van de lijst stelt u **[!UICONTROL Actions]** tot `Delete`.

1. Klik op **[!UICONTROL Submit]**.

1. Klik op **[!UICONTROL OK]**.
