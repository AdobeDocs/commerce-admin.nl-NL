---
title: Toewijzing en toewijzing van voorraden in bulk
description: Leer hoe te om het Assign hulpmiddel van Bronnen te gebruiken om brontaken voor producten te beheren.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Bulkbrontoewijzing en -toewijzing

Gebruik _toewijzen Bronnen_ hulpmiddel om één of meerdere bronnen aan uw producten toe te voegen. Het hulpmiddel helpt wanneer het creëren van en het toewijzen van douanebronnen aan uw StandaardVoorraad of douanevoorraden en het voorbereiden van nieuwe plaatsen en inventaris.

Na het toevoegen van nieuwe douanebronnen, kunt u [ inventarishoeveelheden per product ](quantities-assign-per-product.md) of voor veelvoudige producten door Admin toevoegen of de [ invoereigenschap ](inventory-import-export.md) gebruiken.

![ voeg inventarisbronnen voor geselecteerde producten ](assets/inventory-bulk-assign-sources.gif) toe

## Bronnen en hoeveelheden toewijzen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer de producten waarvoor u de bronnen wilt wijzigen.

   Blader of zoek naar de producten en selecteer de selectievakjes.

1. Klik op het menu **[!UICONTROL Actions]** bovenaan en kies **[!UICONTROL Assign Inventory Source]** .

1. Klik op **[!UICONTROL OK]** in het bevestigingsdialoogvenster.

1. Voor alle bronnen die u aan de producten wilt toevoegen, selecteer checkboxes.

1. Klik op **[!UICONTROL Assign Sources]**.

   ![ Uitgezochte producten om bronnen toe te voegen ](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

De bronnen worden toegevoegd aan de producten met een inventarishoeveelheid van 0. U kunt [ inventarishoeveelheden ](quantities-assign-per-product.md) per bron toevoegen.

## Toewijzing van bronnen en hoeveelheden ongedaan maken

Wanneer u de toewijzing van een bron uit een product ongedaan maakt, geeft u aan dat het product niet langer op die locatie is opgeslagen. Dit proces ontruimt volledig alle inventarisgegevens voor bron momenteel die aan het product wordt toegewezen. Als u de bestaande inventaris naar een nieuwe plaats wilt verplaatsen, denk na gebruikend de _inventarisoptie van de Overdracht_.

{{$include /help/_includes/unassign-source.md}}

Het wordt ten zeerste aanbevolen alle bestellingen en verzendingen voor deze producten in te vullen voordat de bron wordt verwijderd.

![ wijst bronnen voor geselecteerde producten ](assets/inventory-bulk-unassign-sources.gif) unassign

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer de producten waarvoor u bronnen wilt wijzigen.

   Blader of zoek naar de producten en selecteer de selectievakjes.

1. Klik op het menu **[!UICONTROL Actions]** bovenaan en kies **[!UICONTROL Unassign Inventory Source]** .

1. Klik op **[!UICONTROL OK]** in het bevestigingsdialoogvenster.

1. Selecteer de bron die u uit de producten wilt verwijderen.

   Op de pagina wordt een waarschuwing weergegeven dat bij het verwijderen van de toewijzing alle specifieke bron- en kwantiteitsgegevens uit het product worden verwijderd.

1. Klik op **[!UICONTROL Unassign Sources]**.

   ![ verwijdert bronnen uit geselecteerde producten ](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
