---
title: Inventarisatie naar bron overbrengen
description: Leer hoe leveranciers met meerdere leveranciers hun productvoorraad van de ene bronlocatie naar de andere kunnen overbrengen.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Inventarisatie naar bron overbrengen

Afhankelijk van de bedrijfsbehoeften en de status van locatie, brengen leveranciers uit meerdere bronnen vaak de productvoorraad over van de ene bronlocatie naar de andere. U kunt bijvoorbeeld een opslaglocatie sluiten of niet langer specifieke producten van een locatie verzenden en alle bewerkingen voor die producten naar een nieuwe locatie verplaatsen.

Met deze optie kunt u een of meer producten selecteren, de bron van waaruit de voorraad wordt overgedragen en de doelbron waarop de hoeveelheden worden ontvangen:

- De hoeveelheden van de voorraad, de status van Source-objecten (in voorraad/uit voorraad) en de hoeveelheid van de geselecteerde bron melden worden per product verplaatst.

- Als een product die bron niet heeft, wordt het overgeslagen.

- Alle productvoorraad voor de bron wordt verplaatst. U kunt een gedeeltelijk aantal niet overdragen.

>[!NOTE]
>
>Indien de oorsprong en de bestemmingsbronnen zich in verschillende voorraden bevinden, heeft dit gevolgen voor de geaggregeerde verkoopbare hoeveelheid en de reserveringen voor lopende orders.

U kunt de toewijzing van de bron ook ongedaan maken wanneer u inventarishoeveelheden overdraagt.

{{$include /help/_includes/unassign-source.md}}

![ voorraad van de Overdracht aan een andere bron ](assets/inventory-bulk-transfer-source.gif)

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer de producten waarvoor u bronnen wilt wijzigen.

   Blader of zoek naar producten en selecteer selectievakjes voor overdracht.

1. Klik op het menu **[!UICONTROL Actions]** bovenaan en kies **[!UICONTROL Transfer Inventory to Source]** .

1. Klik op **[!UICONTROL OK]** in het bevestigingsdialoogvenster.

1. Om producten naar een nieuwe bestemming over te brengen, selecteer de oorsprong (_[!UICONTROL from]_) bron.

1. om producten naar een nieuwe bestemming over te brengen, selecteer de bestemmingsbron (_[!UICONTROL to]_).

1. Als u de bron uit de producten wilt verwijderen, schakelt u het optionele selectievakje **[!UICONTROL Unassign from origin source after transfer]** in.

   ![ Uitgezochte oorsprong en bestemming voor overdracht ](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Transfer Inventory]**.

   Alle producthoeveelheden worden van de oorsprong afgetrokken en aan de bestemmingsbron toegevoegd. De hoeveelheid en het verkoopbare aantal worden automatisch bijgewerkt.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
