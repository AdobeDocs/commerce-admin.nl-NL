---
title: voorraadhoeveelheden beheren
description: Leer hoe u bronnen en hoeveelheden kunt toewijzen voor nieuwe producten of bestaande producten kunt wijzigen.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# voorraadhoeveelheden beheren

De volgende informatie geeft aan hoe u bronnen en hoeveelheden voor nieuwe producten kunt toewijzen of bestaande producten kunt wijzigen.

Wijs bij het maken van producten bronnen en hoeveelheden toe tijdens het maken van producten. Zie [Een product maken](../catalog/product-create.md) voor volledige instructies. Deze pagina&#39;s bevatten informatie uit één bron en uit meerdere bronnen voor bronnen en hoeveelheden per bron.

Wanneer u voor het eerst een upgrade opent [!DNL Commerce] with [!DNL Inventory Management], worden alle producten en hoeveelheden toegewezen aan de standaardbron. Wanneer het invoeren van nieuwe producten via.csv- dossier, worden zij ook toegewezen aan de Standaardbron.

Single- en multi-source-handelaren kunnen bronnen, inventarishoeveelheden en drempelwaarden per product of in bulk bijwerken.

- Single-source-handelaren kunnen producthoeveelheden bijwerken voor de standaardbron. Deze hoeveelheid is het totale aantal te koop aangeboden producten.

- Meerbronhandelaren kunnen meerdere bronnen en hoeveelheden per product toewijzen voor elke locatie (opslagplaatsen, winkels, verlader, enzovoort). We raden u aan bronnen toe te voegen voordat u de hoeveelheden voor de productvoorraad instelt.

Wanneer u bronnen en hoeveelheden aan uw producten toevoegt, kunt u de hoeveelheden via het productraster bekijken. Als u een groot aantal bronnen hebt, houdt u de muisaanwijzer boven de _[!UICONTROL Quantity per Source]_om de volledige, schuifbare lijst met bronnen met de huidige hoeveelheden te zien.

![Producthoeveelheden per bron](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

U hebt de volgende opties om voorraad aan producten toe te wijzen:

- [Bronnen toewijzen per product](sources-assign-per-product.md) - Wijs handmatig bronnen toe per product in uw catalogus.

- [Hoeveelheden per product toewijzen](quantities-assign-per-product.md) - Voeg voorraden aan uw producten toe per bron. Deze informatie is specifiek voor multi-source handelaren.

- [Bulk toewijzen en toewijzing van bronnen opheffen](bulk-assignment.md) - Bronnen toewijzen aan geselecteerde producten als een massale actie. Gebruik de [Overdracht inventarisatie naar bron](inventory-transfer.md) als u de voorraad wilt overbrengen en de bron wilt verwijderen.

- [Overdracht van voorraad naar bron](inventory-transfer.md) - breng alle voorraden over van een bron van oorsprong naar een bron van bestemming.

- [Hoeveelheden importeren en exporteren](inventory-import-export.md) - Met import- en exportfuncties kunt u meerdere SKU&#39;s voor producten bijwerken met bronnen en inventarishoeveelheden.
