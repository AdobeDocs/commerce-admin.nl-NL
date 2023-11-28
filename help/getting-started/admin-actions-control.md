---
title: Handelingencontrole
description: Leer over het gebruiken van de controle van Acties om een verrichting op één of meerdere verslagen in Admin toe te passen.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Handelingencontrole

Wanneer u met een verzameling records in het raster werkt, kunt u met het besturingselement Handelingen een bewerking toepassen op een of meer records. De controle van Acties maakt een lijst van elke verrichting die voor het specifieke type van gegevens beschikbaar is. U kunt bijvoorbeeld het besturingselement Handelingen gebruiken om de kenmerken van geselecteerde producten bij te werken en de status te wijzigen van `Disabled` tot `Enabled`of om records uit de database te verwijderen.

U kunt zoveel wijzigingen aanbrengen als nodig zijn en de records vervolgens in één stap bijwerken. Het is veel efficiënter dan de montages individueel voor elk product te veranderen. Het toepassen van bewerkingen op een batch records is een asynchrone bewerking die op de achtergrond wordt uitgevoerd, zodat u in de beheerfunctie kunt blijven werken zonder te wachten tot de bewerking is voltooid. Het systeem geeft een bericht weer wanneer de taak is voltooid.

De selectie van beschikbare acties varieert per lijst en er kunnen aanvullende opties worden weergegeven, afhankelijk van de geselecteerde actie. Wanneer u bijvoorbeeld de status van een groep records wijzigt, kunt u _[!UICONTROL Status]_wordt naast het besturingselement Handelingen weergegeven met extra opties.

## Stap 1: records selecteren

Het selectievakje in de eerste kolom van de lijst geeft elke record aan die een doel voor de actie is. De [filterbesturingselementen](admin-grid-controls.md) U kunt de lijst beperken tot de records waarop u de actie wilt toepassen.

1. Indien nodig, plaats de filters bij de bovenkant van elke kolom om slechts de verslagen te tonen die u wilt omvatten.

1. Schakel het selectievakje in van elke record die een doel is voor de handeling of gebruik de kolomkiezer om een bulkselectie te kiezen.

![Alles of alles op pagina selecteren of deselecteren](./assets/action-change-selection.png){width="500"}

## Stap 2: Een handeling toepassen op geselecteerde records

1. Stel de **[!UICONTROL Actions]** besturingselement voor de bewerking die u wilt toepassen.

   **_Voorbeeld:_** Kenmerken bijwerken

   - Selecteer in de lijst het selectievakje van elke record die moet worden bijgewerkt.

   - Stel de **[!UICONTROL Actions]** controle op `Update Attributes`.

     ![Selecteer de actie Kenmerken bijwerken](./assets/action-select.png){width="450"}

   - Klik op **[!UICONTROL Submit]**.

     De pagina Kenmerken bijwerken bevat een lijst met alle beschikbare kenmerken, ingedeeld per groep in het deelvenster aan de linkerkant.

     ![Pagina Kenmerken bijwerken](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - Selecteer de **[!UICONTROL Change]** Schakel het selectievakje naast elk kenmerk in en breng de benodigde wijzigingen aan.

   - Klikken **[!UICONTROL Save]** om de kenmerken voor de groep geselecteerde records bij te werken.

1. Klik op **[!UICONTROL Submit]**.

## Handelingen Selectievakje

| Handeling | Beschrijving |
|--- |--- |
| [!UICONTROL Select All] | Selecteert checkbox van alle verslagen in de lijst. |
| [!UICONTROL Unselect All] | Wist het selectievakje van alle records in de lijst. |
| [!UICONTROL Select All on This Page] | Selecteert checkbox van verslagen die op de huidige pagina worden getoond. |
| [!UICONTROL Deselect All on This Page] | Hiermee wist u het selectievakje met records die op de huidige pagina worden weergegeven. |

{style="table-layout:auto"}
