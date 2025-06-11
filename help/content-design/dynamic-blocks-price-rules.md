---
title: Dynamische blokken in prijsregels
description: Koppel een dynamisch blok aan een promotieprijsregel.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Dynamische blokken in prijsregels

{{ee-feature}}

Om het even welk [ dynamische blok ](dynamic-blocks.md) dat u creeert kan met een bevordering worden geassocieerd. Om de vereniging te maken, moet u zowel het dynamische blok als de [ regel van de catalogusprijs ](../merchandising-promotions/price-rules-catalog.md) of [ de regel van de kartprijs ](../merchandising-promotions/price-rules-cart.md) eerst tot stand brengen. De associatie kan tot stand worden gebracht wanneer wordt gewerkt aan een prijsregel of wanneer wordt gewerkt aan een dynamisch blok.

>[!IMPORTANT]
>
>Nadat u deze vereniging creeert, wordt het dynamische blok getoond **slechts** wanneer de regel in brand steekt. Als de bevordering aan segment A wordt gericht, wordt het blok getoond aan segment A. Als de bevordering niet actief is, wordt het blok niet getoond.

## Een dynamisch blok koppelen aan een prijsregel

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_&#x200B;en kies één van het volgende:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Zoek in het raster de regel die u aan het dynamische blok wilt koppelen en open in de bewerkingsmodus.

1. De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]** uit.

1. Stel in de eerste kolom het filter in op `Any` en klik op **[!UICONTROL Reset Filter]** .

   Het raster bevat nu alle beschikbare dynamische blokken.

1. Schakel het selectievakje in van elk dynamisch blok dat u aan de regel wilt koppelen.

   ![ Toevoegend geselecteerde dynamische blokken ](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Een prijsregel koppelen aan een dynamisch blok

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Zoek het dynamische blok in het raster en open in de bewerkingsmodus.

1. Omlaag schuiven en uitvouwen **[!UICONTROL Related Promotions]** .

   Eventuele prijsregels die op dat moment van toepassing zijn, worden weergegeven in het raster.

1. Voeg een nieuwe bijbehorende regel toe of verwijder een huidige vereniging.

   - Klik op **[!UICONTROL Add Cart Price Rules]** als u een winkelwagentje wilt koppelen.

   - Klik op **[!UICONTROL Add Catalog Price Rules]** als u een productgerelateerde aanbieding wilt koppelen.

1. Selecteer in het raster het selectievakje van elke regel die u aan het dynamische blok wilt koppelen.

1. Klik op **[!UICONTROL Add Selected]**.

   ![ Toevoegend geselecteerde prijsregels aan een dynamisch blok ](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.
