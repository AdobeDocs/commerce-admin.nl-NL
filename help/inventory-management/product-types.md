---
title: Productsoorten
description: Leer hoe  [!DNL Inventory Management]  inventaris en ordebeheer voor alle Adobe Commerce en Magento Open Source producttypes steunt.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Productsoorten

[!DNL Inventory Management] ondersteunt inventarisatie- en orderbeheer voor alle producttypen in Adobe Commerce en Magento Open Source: eenvoudig, configureerbaar, virtueel, downloadbaar, bundel en gegroepeerd. De opties en vereisten kunnen per producttype voor bronnen, voorraden en verzending verschillen.

- [ Single-source handelaars ](merchant-sourcing.md#single-source-merchants) creeer en werk productmontages en hoeveelheden bij zonder extra updates te vereisen. Alle gemaakte en nieuw geïmporteerde producten worden automatisch toegewezen aan de standaard-Source en de standaardvoorraad, die direct beschikbaar zijn voor klanten als deze zijn ingeschakeld en in voorraad.

- [ Multisource handelaren ](merchant-sourcing.md#multi-source-merchants) wijzen bronnen, hoeveelheden per bron, en montages tijdens of na productverwezenlijking toe. [!DNL Commerce] wijst alle nieuw geïmporteerde producten toe aan de standaard-Source, waardoor extra bewerkingen nodig zijn om bronnen en hoeveelheden toe te wijzen.

| Producttype | Algoritme voor verzending en Source-selectie |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Gebruikt altijd de SSA aanbeveling. Het systeem voert impliciet het algoritme uit wanneer het facturen creeert, en gebruikt altijd de voorgestelde resultaten.<br/> u kunt niet deze resultaten aanpassen. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Gebruikt altijd de SSA aanbeveling. Het systeem voert impliciet het algoritme uit wanneer het facturen creeert, en gebruikt altijd de voorgestelde resultaten. <br/> u kunt niet deze resultaten aanpassen. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
