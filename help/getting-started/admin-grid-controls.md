---
title: Besturingselementen voor beheerraster
description: Leer hoe u kunt werken op beheerpagina's die gegevens beheren en een verzameling records in een raster weergeven.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Besturingselementen voor beheerraster

Op beheerpagina&#39;s die gegevens beheren, wordt een verzameling records in een raster weergegeven. U kunt de gegevens sorteren met de besturingselementen boven aan elke kolom. De huidige sorteervolgorde wordt aangegeven met een oplopende of aflopende pijl in de kolomkop. U kunt opgeven welke kolommen in het raster worden weergegeven en deze naar verschillende posities slepen. U kunt ook verschillende kolomregelingen opslaan als weergaven die u later kunt gebruiken. In de kolom **[!UICONTROL Action]** worden bewerkingen weergegeven die op een afzonderlijke record kunnen worden toegepast. Bovendien kan de datum van de huidige mening van de meeste netten aan a [ CSV ](../systems/data-csv.md) of dossier van XML worden uitgevoerd.

![ de pagina van Orden - netvertoning ](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## De lijst sorteren

1. Klik op een kolomkop.

   De pijl geeft de huidige volgorde aan als oplopend of aflopend.

1. Gebruik de pagineringsbesturingselementen om extra pagina&#39;s in de verzameling weer te geven.

   ![ de vertoning van het Net - paginacontroles ](./assets/pagination-controls.png){width="300"}

## De lijst pagineren

1. Stel het besturingselement **[!UICONTROL Pagination]** in op het aantal records dat u per pagina wilt weergeven.

1. Klik op **[!UICONTROL Next]** en **[!UICONTROL Previous]** om door de lijst te bladeren of voer een specifieke **[!UICONTROL Page Number]** in.

## De lijst filteren

1. Klik op **[!UICONTROL Filters]**.

1. Voer zoveel filters in als nodig zijn om de record te beschrijven die u wilt zoeken.

1. Klik op **[!UICONTROL Apply Filters]**.

   ![ de lijst van Orden - filtercontroles ](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Gegevens exporteren

1. Selecteer de records die u wilt exporteren.

   >[!NOTE]
   >
   >Productgegevens kunnen niet uit het raster worden geëxporteerd. Meer leren, zie [ Uitvoer ](../systems/data-export.md).

1. Op de _Uitvoer_ (![ selecteur van het Menu ](../assets/icon-export.png)) menu in de hoger-juiste hoek, kies één van de volgende dossierformaten:

   - `CSV`
   - `Excel XML`

   ![ lijst van Orden - de uitvoeropties ](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Export]**.

1. Zoek het gedownloade bestand met geëxporteerde gegevens op de locatie die door uw browser wordt gebruikt voor downloads.

## Rasterlay-out

De selectie van kolommen en hun orde in het net kunnen volgens uw voorkeur worden veranderd, en als a _mening_ worden bewaard. U kunt bepalen welke kenmerken in het raster worden weergegeven onder de afzonderlijke kenmerkconfiguratie. Veel kenmerken die in het productraster worden weergegeven, kunnen van invloed zijn op de laadtijd en prestaties van de beheerder.

![ de Kolommen van het Net van de Orde ](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### De selectie van kolommen wijzigen

1. In de hoger-juiste hoek, klik de _controle van Kolommen_ (![ controle van Kolommen ](../assets/icon-columns.png)).

1. Wijzig de kolomselecties:

   - Schakel het selectievakje in van de kolommen die u aan het raster wilt toevoegen.
   - Schakel het selectievakje uit van elke kolom die u uit het raster wilt verwijderen.
   - Klik op **[!UICONTROL Reset]** om de standaardrasterweergave te herstellen.

Schuif omlaag om alle beschikbare kolommen weer te geven.

### Een kolom verplaatsen

1. Klik op de kolomkop en houd de muisknop ingedrukt.

1. Sleep de kolom naar de nieuwe positie en laat deze los.

### Een rasterweergave opslaan

1. Klik de _controle van de Mening_ (![ controle van de Mening ](../assets/icon-view-eye.png)).

1. Klik op **[!UICONTROL Save Current View]**.

1. Voer een **[!UICONTROL name]** in voor de weergave.

1. Om alle veranderingen te bewaren, klik de _Pijl_ (![ sparen alle veranderingen ](../assets/icon-arrow-save.png)).

   De naam van de weergave wordt nu weergegeven als de huidige weergave.

### De rasterweergave wijzigen

1. Klik de _controle van de Mening_ (![ het pictogram van de Mening ](../assets/icon-view-eye.png)).

1. Voer een van de volgende handelingen uit:

   - Klik op de naam van de weergave als u een andere weergave wilt gebruiken.
   - Om de naam van een mening te veranderen, klik _uitgeven_ (![ geef pictogram ](../assets/icon-edit-pencil.png)) pictogram uit en werk de naam bij.
   - Om een mening te schrappen, klik _uitgeven_ (![ geef pictogram ](../assets/icon-edit-pencil.png) uit) pictogram en klik dan _Schrapping_ (![ pictogram van de Schrapping ](../assets/icon-delete-trashcan-solid.png)) pictogram.
