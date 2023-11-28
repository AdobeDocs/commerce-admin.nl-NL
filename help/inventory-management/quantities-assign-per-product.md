---
title: Overbodige hoeveelheden per product toewijzen
description: Leer hoe u de inventarishoeveelheden voor uw product kunt bijwerken en de beschikbare voorraad kunt bijhouden.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Hoeveelheden per product toewijzen

Na toevoegen [bronnen](sources-assign-per-product.md), werkt u de inventarishoeveelheden voor uw product bij. Deze waarden volgen de beschikbare voorraden aan de hand.

Als u de voorraad van een bron wilt verbergen voor verzendingen zonder de bron te verwijderen, stelt u _[!UICONTROL Source Item Status]_tot `Out of Stock`. De veiligheidscontrole en de verzendingsopties hebben alleen toegang tot bronnen die zijn vermeld als `In Stock` met beschikbare inventarishoeveelheid.

Alle bijgewerkte hoeveelheden en bronnen worden weergegeven in het productraster.

## Hoeveelheden bijwerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek en open een product in de bewerkingsmodus.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** sectie.

1. Set **[!UICONTROL Source Item Status]** tot `In Stock`.

1. om de hoeveelheid voor de voorraad aan te passen, een bedrag in te voeren voor **[!UICONTROL Qty]**.

1. Voer een van de volgende handelingen uit om een melding voor inventarishoeveelheden in te stellen:

   - Aangepast aantal berichten - Schakel het selectievakje **[!UICONTROL Use Default]** selectievakje en voer een bedrag in **[!UICONTROL Notify Qty]**.
   - Standaardaantal meldingen - Selecteer de optie **[!UICONTROL Use Default]** selectievakje. [!DNL Commerce] controleert en gebruikt de instelling in _[!UICONTROL Advanced Inventory]_of globale winkelconfiguratie.

   ![Producthoeveelheden per bron bijwerken](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Voer een van de volgende handelingen uit om op te slaan:

   - Klik op **[!UICONTROL Save]**.

   - Op de **[!UICONTROL Save]** (![Menupijl](../assets/icon-menu-down-arrow-red.png)), kiest u **[!UICONTROL Save & Close]**.


Het productraster wordt bijgewerkt met een lijst met alle bronnen en gerelateerde hoeveelheden. Voor producten met meer dan vijf toegewezen bronnen, houdt u de muisaanwijzer boven de _[!UICONTROL Quantity per Source]_om de volledige lijst weer te geven.

![Producthoeveelheden per bron](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
