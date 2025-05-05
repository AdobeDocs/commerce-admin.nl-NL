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

Na het toevoegen van [ bronnen ](sources-assign-per-product.md), werk de inventarishoeveelheden voor uw product bij. Deze waarden volgen de beschikbare voorraden aan de hand.

Als u de voorraad van een bron wilt verbergen voor verzendingen zonder de bron te verwijderen, stelt u _[!UICONTROL Source Item Status]_&#x200B;in op `Out of Stock` . De SSA en de verzendopties hebben alleen toegang tot bronnen die als `In Stock` met beschikbare inventarishoeveelheid worden vermeld.

Alle bijgewerkte hoeveelheden en bronnen worden weergegeven in het productraster.

## Hoeveelheden bijwerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek en open een product in de bewerkingsmodus.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** sectie uit.

1. Stel **[!UICONTROL Source Item Status]** in op `In Stock` .

1. Voer een bedrag in voor **[!UICONTROL Qty]** als u de hoeveelheid voor de voorraad wilt bijwerken.

1. Voer een van de volgende handelingen uit om een melding voor inventarishoeveelheden in te stellen:

   - Aangepast aantal berichten - Schakel het selectievakje **[!UICONTROL Use Default]** uit en voer een bedrag in **[!UICONTROL Notify Qty]** in.
   - Standaardwaarde voor Hoeveelheid waarschuwen - Schakel het selectievakje **[!UICONTROL Use Default]** in. [!DNL Commerce] controleert en gebruikt de instelling in _[!UICONTROL Advanced Inventory]_&#x200B;of algemene winkelconfiguratie.

   ![ de Hoeveelheden van het Product van de Update per Source ](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Voer een van de volgende handelingen uit om op te slaan:

   - Klik op **[!UICONTROL Save]**.

   - Voor **[!UICONTROL Save]** (![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png)) menu, kies **[!UICONTROL Save & Close]**.


Het productraster wordt bijgewerkt met een lijst met alle bronnen en gerelateerde hoeveelheden. Voor producten met meer dan vijf toegewezen bronnen houdt u de muisaanwijzer boven de kolom _[!UICONTROL Quantity per Source]_&#x200B;om de volledige lijst weer te geven.

![ de hoeveelheden van het Product per bron ](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
