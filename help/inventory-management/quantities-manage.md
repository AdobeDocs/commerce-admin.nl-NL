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

Wijs bij het maken van producten bronnen en hoeveelheden toe tijdens het maken van producten. Zie [ een product ](../catalog/product-create.md) voor volledige instructies creëren. Deze pagina&#39;s bevatten informatie uit één bron en uit meerdere bronnen voor bronnen en hoeveelheden per bron.

Wanneer u een upgrade van [!DNL Commerce] met [!DNL Inventory Management] opent, worden alle producten en hoeveelheden toegewezen aan de standaard-Source. Wanneer u nieuwe producten importeert via het CSV-bestand, worden deze ook toegewezen aan de Standaard Source.

Single- en multi-source-handelaren kunnen bronnen, inventarishoeveelheden en drempelwaarden per product of in bulk bijwerken.

- Single-source-handelaren kunnen producthoeveelheden bijwerken voor de standaard Source. Deze hoeveelheid is het totale aantal te koop aangeboden producten.

- Meerbronhandelaren kunnen meerdere bronnen en hoeveelheden per product toewijzen voor elke locatie (opslagplaatsen, winkels, verlader, enzovoort). We raden u aan bronnen toe te voegen voordat u de hoeveelheden voor de productvoorraad instelt.

Wanneer u bronnen en hoeveelheden aan uw producten toevoegt, kunt u de hoeveelheden via het productraster bekijken. Als u een groot aantal bronnen hebt, houdt u de muisaanwijzer boven _[!UICONTROL Quantity per Source]_om de volledige, schuifbare lijst met bronnen met de huidige hoeveelheden weer te geven.

![ de hoeveelheden van het Product per bron ](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

U hebt de volgende opties om voorraad aan producten toe te wijzen:

- [ Toewijzend Bronnen per Product ](sources-assign-per-product.md) - wijs manueel bronnen per product in uw catalogus toe.

- [ Toewijzend Hoeveelheden per Product ](quantities-assign-per-product.md) - voeg voorraad aan uw producten per bron toe. Deze informatie is specifiek voor multi-source handelaren.

- [ Bulk die en Bronnen ](bulk-assignment.md) toewijzen Unassigning - wijst bronnen aan geselecteerde producten als massaactie toe. Gebruik de [ optie van de Inventaris van de Overdracht aan Source ](inventory-transfer.md) als u inventaris wilt overbrengen en de bron verwijderen.

- [ Overbrengend Inventaris aan Source ](inventory-transfer.md) - breng alle inventaris van één oorsprong naar een bestemmingsbron over.

- [ het Invoeren en het Uitvoeren Hoeveelheden ](inventory-import-export.md) - de invoer en de uitvoereigenschappen van het gebruik om veelvoudige product SKUs met bronnen en inventarishoeveelheden bij te werken.
