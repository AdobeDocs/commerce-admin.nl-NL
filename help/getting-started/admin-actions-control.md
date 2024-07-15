---
title: Handelingencontrole
description: Leer over het gebruiken van de controle van Acties om een verrichting op één of meerdere verslagen in Admin toe te passen.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Handelingencontrole

Wanneer u met een verzameling records in het raster werkt, kunt u met het besturingselement Handelingen een bewerking toepassen op een of meer records. De controle van Acties maakt een lijst van elke verrichting die voor het specifieke type van gegevens beschikbaar is. Met het besturingselement Handelingen kunt u bijvoorbeeld de kenmerken van geselecteerde producten bijwerken, de status wijzigen van `Disabled` in `Enabled` of records uit de database verwijderen.

U kunt zoveel wijzigingen aanbrengen als nodig zijn en de records vervolgens in één stap bijwerken. Het is veel efficiënter dan de montages individueel voor elk product te veranderen. Het toepassen van bewerkingen op een batch records is een asynchrone bewerking die op de achtergrond wordt uitgevoerd, zodat u in de beheerfunctie kunt blijven werken zonder te wachten tot de bewerking is voltooid. Het systeem geeft een bericht weer wanneer de taak is voltooid.

De selectie van beschikbare acties varieert per lijst en er kunnen aanvullende opties worden weergegeven, afhankelijk van de geselecteerde actie. Wanneer u bijvoorbeeld de status van een groep records wijzigt, wordt naast het besturingselement Handelingen een vak _[!UICONTROL Status]_weergegeven met extra opties.

## Stap 1: records selecteren

Het selectievakje in de eerste kolom van de lijst geeft elke record aan die een doel voor de actie is. De [ filtercontroles ](admin-grid-controls.md) kunnen worden gebruikt om de lijst aan de verslagen te beperken u voor de actie wilt richten.

1. Indien nodig, plaats de filters bij de bovenkant van elke kolom om slechts de verslagen te tonen die u wilt omvatten.

1. Schakel het selectievakje in van elke record die een doel is voor de handeling of gebruik de kolomkiezer om een bulkselectie te kiezen.

![ Uitgezocht of deselecteer allen of allen op pagina ](./assets/action-change-selection.png){width="500"}

## Stap 2: Een handeling toepassen op geselecteerde records

1. Stel het besturingselement **[!UICONTROL Actions]** in op de bewerking die u wilt toepassen.

   **_Voorbeeld:_** attributen van de Update

   - Selecteer in de lijst het selectievakje van elke record die moet worden bijgewerkt.

   - Stel het besturingselement **[!UICONTROL Actions]** in op `Update Attributes` .

     ![ selecteer de actie van Attributen van de Update ](./assets/action-select.png){width="450"}

   - Klik op **[!UICONTROL Submit]**.

     De pagina Kenmerken bijwerken bevat een lijst met alle beschikbare kenmerken, ingedeeld per groep in het deelvenster aan de linkerkant.

     ![ pagina van Attributen van de Update ](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - Schakel het selectievakje **[!UICONTROL Change]** naast elk kenmerk in en breng de benodigde wijzigingen aan.

   - Klik op **[!UICONTROL Save]** om de kenmerken voor de groep geselecteerde records bij te werken.

1. Klik op **[!UICONTROL Submit]** als de bewerking is voltooid.

## Handelingen Selectievakje

| Handeling | Beschrijving |
|--- |--- |
| [!UICONTROL Select All] | Selecteert checkbox van alle verslagen in de lijst. |
| [!UICONTROL Unselect All] | Wist het selectievakje van alle records in de lijst. |
| [!UICONTROL Select All on This Page] | Selecteert checkbox van verslagen die op de huidige pagina worden getoond. |
| [!UICONTROL Deselect All on This Page] | Hiermee wist u het selectievakje met records die op de huidige pagina worden weergegeven. |

{style="table-layout:auto"}
