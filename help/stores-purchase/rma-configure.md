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

Wanneer toegelaten, kunnen de verzoeken RMA door klanten van de storefront worden voorgelegd. Een RMA kan slechts worden geproduceerd als er een punt in de orde is die voor terugkeer beschikbaar is. De verzoeken om individuele punten terug te keren worden beheerd door _laat 1&rbrace; attributen RMA in elk productverslag toe._ Door gebrek, worden de configuratiemontages toegepast op het product (_[!UICONTROL Use Config Settings]_&#x200B;wordt geselecteerd). Als&#x200B;_[!UICONTROL Enable RMA]_ is ingesteld op `No` , wordt het product niet weergegeven in de lijst met items die kunnen worden geretourneerd. Als u _verandert laat RMA_ plaatsen toe, is het op zowel nieuwe als bestaande orden van toepassing.

## RMA&#39;s inschakelen voor uw winkel

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL RMA Settings]** sectie uit.

   ![&#x200B; Montages RMA &#x200B;](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable RMA on Storefront]** in op `Yes` .

   Deze instelling bepaalt of klanten RMA-verzoeken vanuit de winkel kunnen maken en weergeven. RMA&#39;s kunnen worden toegepast op zowel nieuwe als bestaande orders.

1. Stel **[!UICONTROL Enable RMA on Product Level]** in op `Yes` .

   Dit het plaatsen bepaalt het gedrag voor _laat 1&rbrace; attributen RMA voor individuele producten op storefront toe:_

   - Wanneer [!UICONTROL Enable RMA on Product Level] is ingesteld op `Yes` , kunnen klanten in de winkel alle afzonderlijke producten retourneren. Deze bevat zowel _[!UICONTROL Enable RMA]_= `Yes` als&#x200B;_[!UICONTROL Enable RMA]_ = `No` productkenmerkwaarden.
   - Wanneer [!UICONTROL Enable RMA on Product Level] is ingesteld op `No` , kunnen klanten in de winkel alleen de producten retourneren met de waarde van het productkenmerk _[!UICONTROL Enable RMA]_= `Yes` .

1. Stel **[!UICONTROL Use Store Address]** in op een van de volgende waarden:

   - `Yes` - Verstuur de geretourneerde producten naar het adres van de winkel.
   - `No` - Voer een alternatief adres in voor de geretourneerde waarde van het product.

   ![&#x200B; Montages RMA met afwisselend adres &#x200B;](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Verzendmethoden configureren voor retourzendingen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Delivery Methods]** .

1. Vouw de sectie uit voor de carrier die u wilt gebruiken voor de retourservice, zoals **[!UICONTROL UPS]** .

   ![&#x200B; laat de dienst RMA voor drager &#x200B;](./assets/rma-delivery-method.png){width="600" zoomable="yes"} toe

1. Stel **[!UICONTROL Enabled for RMA]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]**.

## Toegestane RMA&#39;s op productniveau wijzigen

Als u RMAs voor uw opslag toelaat en uw catalogus sommige producten bevat die niet voor terugkeer zouden moeten worden toegestaan, kunt u het plaatsen op het productniveau wijzigen,

1. Open het product in de bewerkingsmodus.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Autosettings]** sectie.

1. Schakel indien nodig het selectievakje **[!UICONTROL Use Config Setting]** uit.

1. Schakel de instelling **[!UICONTROL Enable RMA]** in op `No` .

   ![&#x200B; maak RMA voor een product &#x200B;](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"} onbruikbaar

1. Klik op **[!UICONTROL Save]**.
