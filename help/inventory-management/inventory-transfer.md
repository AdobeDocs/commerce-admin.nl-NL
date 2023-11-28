---
title: Inventarisatie naar bron overbrengen
description: Leer hoe leveranciers met meerdere leveranciers hun productvoorraad van de ene bronlocatie naar de andere kunnen overbrengen.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Inventarisatie naar bron overbrengen

Afhankelijk van de bedrijfsbehoeften en de status van locatie, brengen leveranciers uit meerdere bronnen vaak de productvoorraad over van de ene bronlocatie naar de andere. U kunt bijvoorbeeld een opslaglocatie sluiten of niet langer specifieke producten van een locatie verzenden en alle bewerkingen voor die producten naar een nieuwe locatie verplaatsen.

Met deze optie kunt u een of meer producten selecteren, de bron van waaruit de voorraad wordt overgedragen en de doelbron waarop de hoeveelheden worden ontvangen:

- De hoeveelheden van de voorraad, de status van de bronpost (in voorraad/uit voorraad) en de hoeveelheid van de kennisgeving voor de geselecteerde bron worden per product verplaatst.

- Als een product die bron niet heeft, wordt het overgeslagen.

- Alle productvoorraad voor de bron wordt verplaatst. U kunt een gedeeltelijk aantal niet overdragen.

>[!NOTE]
>
>Indien de oorsprong en de bestemmingsbronnen zich in verschillende voorraden bevinden, heeft dit gevolgen voor de geaggregeerde verkoopbare hoeveelheid en de reserveringen voor lopende orders.

U kunt de toewijzing van de bron ook ongedaan maken wanneer u inventarishoeveelheden overdraagt.

{{$include /help/_includes/unassign-source.md}}

![Overdracht van voorraad naar andere bron](assets/inventory-bulk-transfer-source.gif)

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer de producten waarvoor u bronnen wilt wijzigen.

   Blader of zoek naar producten en selecteer selectievakjes voor overdracht.

1. Klik op de knop **[!UICONTROL Actions]** bovenaan en kies **[!UICONTROL Transfer Inventory to Source]**.

1. Klikken **[!UICONTROL OK]** in het bevestigingsdialoogvenster.

1. Als u producten naar een nieuwe bestemming wilt overbrengen, selecteert u de oorsprong (_[!UICONTROL from]_).

1. om producten naar een nieuwe bestemming over te brengen, selecteer de bestemming (_[!UICONTROL to]_).

1. Als u de bron uit de producten wilt verwijderen, schakelt u het optionele selectievakje in **[!UICONTROL Unassign from origin source after transfer]**.

   ![Oorsprong en bestemming voor overdracht selecteren](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Transfer Inventory]**.

   Alle producthoeveelheden worden van de oorsprong afgetrokken en aan de bestemmingsbron toegevoegd. De hoeveelheid en het verkoopbare aantal worden automatisch bijgewerkt.
