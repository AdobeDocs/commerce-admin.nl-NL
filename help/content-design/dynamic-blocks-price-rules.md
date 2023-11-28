---
title: Dynamische blokken in prijsregels
description: Koppel een dynamisch blok aan een promotieprijsregel.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamische blokken in prijsregels

{{ee-feature}}

Alle [dynamisch blok](dynamic-blocks.md) die je maakt, kan worden gekoppeld aan een speciale actie. Als u de koppeling wilt maken, moet u eerst zowel het dynamische blok als het [catalogusprijsregel](../merchandising-promotions/price-rules-catalog.md) of [kartonnen prijsregel](../merchandising-promotions/price-rules-cart.md). De associatie kan tot stand worden gebracht wanneer wordt gewerkt aan een prijsregel of wanneer wordt gewerkt aan een dynamisch blok.

>[!IMPORTANT]
>
>Nadat u deze koppeling hebt gemaakt, wordt het dynamische blok weergegeven **alleen** wanneer de regel in brand staat. Als de bevordering aan segment A wordt gericht, wordt het blok getoond aan segment A. Als de bevordering niet actief is, wordt het blok niet getoond.

## Een dynamisch blok koppelen aan een prijsregel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_en kiest u een van de volgende opties:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Zoek in het raster de regel die u aan het dynamische blok wilt koppelen en open in de bewerkingsmodus.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. Stel in de eerste kolom het filter in op `Any` en klik op **[!UICONTROL Reset Filter]**.

   Het raster bevat nu alle beschikbare dynamische blokken.

1. Schakel het selectievakje in van elk dynamisch blok dat u aan de regel wilt koppelen.

   ![Geselecteerde dynamische blokken toevoegen](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

## Een prijsregel koppelen aan een dynamisch blok

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Zoek het dynamische blok in het raster en open in de bewerkingsmodus.

1. Omlaag schuiven en uitbreiden **[!UICONTROL Related Promotions]**.

   Eventuele prijsregels die op dat moment van toepassing zijn, worden weergegeven in het raster.

1. Voeg een nieuwe bijbehorende regel toe of verwijder een huidige vereniging.

   - Als u een winkelwagentje wilt koppelen, klikt u op **[!UICONTROL Add Cart Price Rules]**.

   - Als u een productgerelateerde aanbieding wilt koppelen, klikt u op **[!UICONTROL Add Catalog Price Rules]**.

1. Selecteer in het raster het selectievakje van elke regel die u aan het dynamische blok wilt koppelen.

1. Klik op **[!UICONTROL Add Selected]**.

   ![Geselecteerde prijsregels toevoegen aan een dynamisch blok](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.
