---
title: Terugkeer configureren
description: Leer hoe u de geretourneerde bedragen voor uw winkel inschakelt en de ondersteunde verzendmethoden configureert.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Terugkeer configureren

{{ee-feature}}

Wanneer toegelaten, kunnen de verzoeken RMA door klanten van de storefront worden voorgelegd. Een RMA kan slechts worden geproduceerd als er een punt in de orde is die voor terugkeer beschikbaar is. Verzoeken om individuele items te retourneren worden beheerd door de _RMA inschakelen_ in elke productrecord. Standaard worden de configuratie-instellingen toegepast op het product (_[!UICONTROL Use Config Settings]_is geselecteerd). Indien_[!UICONTROL Enable RMA]_ is ingesteld op `No`, wordt het product niet weergegeven in de lijst met items die kunnen worden geretourneerd. Als u de _RMA inschakelen_ het is van toepassing op zowel nieuwe als bestaande bestellingen.

## RMA&#39;s inschakelen voor uw winkel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL RMA Settings]** sectie.

   ![RMA-instellingen](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable RMA on Storefront]** tot `Yes`.

   Deze instelling bepaalt of klanten RMA-verzoeken vanuit de winkel kunnen maken en weergeven. RMA&#39;s kunnen worden toegepast op zowel nieuwe als bestaande orders.

1. Set **[!UICONTROL Enable RMA on Product Level]** tot `Yes`.

   Deze instelling bepaalt het gedrag voor de _RMA inschakelen_ kenmerk voor afzonderlijke producten in de winkel:

   - Wanneer [!UICONTROL Enable RMA on Product Level] is ingesteld op `Yes`, kunnen klanten op de winkel alle afzonderlijke producten retourneren. Het omvat beide _[!UICONTROL Enable RMA]_= `Yes` en_[!UICONTROL Enable RMA]_ = `No` productkenmerkwaarden.
   - Wanneer [!UICONTROL Enable RMA on Product Level] is ingesteld op `No`, kunnen klanten op de winkel alleen de producten met een _[!UICONTROL Enable RMA]_= `Yes` productkenmerkwaarde.

1. Set **[!UICONTROL Use Store Address]** op een van de volgende waarden:

   - `Yes` - Teruggestuurde producten naar het adres van de winkel sturen.
   - `No` - Voer een alternatief adres in voor de geretourneerde waarde van het product.

   ![RMA-instellingen met alternatief adres](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Verzendmethoden configureren voor retourzendingen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Breid de sectie voor de drager uit die u voor de terugkeerdienst, zoals wilt gebruiken **[!UICONTROL UPS]**.

   ![RMA-service inschakelen voor carrier](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enabled for RMA]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.

## Toegestane RMA&#39;s op productniveau wijzigen

Als u RMAs voor uw opslag toelaat en uw catalogus sommige producten bevat die niet voor terugkeer zouden moeten worden toegestaan, kunt u het plaatsen op het productniveau wijzigen,

1. Open het product in de bewerkingsmodus.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Autosettings]** sectie.

1. Wis de **[!UICONTROL Use Config Setting]** selectievakje, indien nodig.

1. Schakelen tussen **[!UICONTROL Enable RMA]** instellen op `No`.

   ![RMA uitschakelen voor een product](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.
