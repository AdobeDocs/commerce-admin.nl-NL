---
title: Productsoorten
description: Meer informatie [!DNL Inventory Management] ondersteunt voorraad- en orderbeheer voor alle producttypen van Adobe Commerce en Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Productsoorten

[!DNL Inventory Management] ondersteunt inventarisatie- en orderbeheer voor alle producttypen in Adobe Commerce en Magento Open Source: eenvoudig, configureerbaar, virtueel, downloadbaar, bundel en gegroepeerd. De opties en vereisten kunnen per producttype voor bronnen, voorraden en verzending verschillen.

- [Single-source-handelaren](merchant-sourcing.md#single-source-merchants) productinstellingen en -hoeveelheden maken en bijwerken zonder extra updates nodig te hebben. Alle gemaakte en nieuw geïmporteerde producten worden automatisch toegewezen aan de standaardbron en standaardvoorraad, die direct beschikbaar zijn voor klanten als deze zijn ingeschakeld en in voorraad.

- [Meerbronproducten](merchant-sourcing.md#multi-source-merchants) tijdens of na het maken van het product bronnen, hoeveelheden per bron en instellingen toewijzen. [!DNL Commerce] Hiermee wijst u alle nieuw geïmporteerde producten toe aan de standaardbron, waardoor extra bewerkingen nodig zijn om bronnen en hoeveelheden toe te wijzen.

| Producttype | Algoritme voor verzending en bronselectie |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Gebruikt altijd de SSA aanbeveling. Het systeem voert impliciet het algoritme uit wanneer het facturen creeert, en gebruikt altijd de voorgestelde resultaten.<br/>U kunt deze resultaten niet aanpassen. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Gebruikt altijd de SSA aanbeveling. Het systeem voert impliciet het algoritme uit wanneer het facturen creeert, en gebruikt altijd de voorgestelde resultaten. <br/>U kunt deze resultaten niet aanpassen. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Steunt aanbevelingen SSA en treedt bij het verschepen met voeten. |
