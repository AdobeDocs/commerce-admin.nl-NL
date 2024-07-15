---
title: Gegevens over belastingtarieven bijwerken
description: Leer hoe u met export- en importbewerkingen de belastingtarieven voor je winkel kunt bijwerken.
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Gegevens over belastingtarieven bijwerken

Als je zaken doet in verschillende landen en een groot aantal producten verzendt, kan het erg tijdrovend zijn om handmatig belastingtarieven in te voeren. Het is sneller en efficiënter om belastingtarieven te downloaden per postcode en deze in Commerce te importeren. In het volgende voorbeeld ziet u hoe u een set staatspecifieke belastingtarieven importeert die u van een vertrouwde bron hebt gedownload. Avalara verstrekt [ lijsten van het belastingtarief ](https://www.avalara.com/taxrates/en/download-tax-tables.html), dat u zonder kosten, voor elke code van het ZIP in de Verenigde Staten kunt downloaden.

>[!NOTE]
>
>Als u in het automatiseren van uw verkoop geinteresseerd bent en belastingnaleving en rapportering gebruikt, kunt u Commerce-vertrouwde op opties op de ](https://solutionpartners.adobe.com/s/directory/?solution=commerce) plaats van de Partners van Commerce 0} vinden {.[

## Stap 1: De gegevens over het Commerce-belastingtarief exporteren

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Klik op **[!UICONTROL Export Tax Rates]** .

1. Zoek het bestand op de downloadlocatie voor uw webbrowser.

1. Sla het bestand op en open het in een spreadsheet.

   In dit voorbeeld wordt [!DNL OpenOffice Calc] gebruikt.

   De geëxporteerde gegevens over het Commerce-belastingtarief bevatten de volgende kolommen:
   - Code
   - Land
   - Staat
   - Postcode/Post
   - Snelheid
   - Bereik van
   - Bereik tot
   - Een kolom voor elke archiefweergave

   ![ Uitgevoerde gegevens - belastingtarieven ](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. Open de nieuwe gegevens over het belastingtarief in een tweede instantie van het spreadsheet, zodat kunt u hen naast elkaar zien.

1. Houd bij de nieuwe gegevens over het belastingtarief rekening met eventuele aanvullende gegevens over het belastingtarief die u in uw winkel moet instellen voordat de gegevens worden geïmporteerd.

   De gegevens over het belastingtarief voor Californië omvatten bijvoorbeeld ook:

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   Als u extra [ belastingstreken en tarieven ](../stores-purchase/tax-zones-rates.md) moet invoeren, moet u hen van Admin van uw opslag eerst bepalen en de [ belastingregels ](../stores-purchase/tax-rules.md) bijwerken zoals nodig. Exporteer vervolgens de gegevens en open het bestand in een teksteditor, zodat het ter referentie kan worden gebruikt. Om dit voorbeeld eenvoudig te houden, importeren we echter alleen de kolommen met het standaardbelastingtarief.

## Stap 2: De importgegevens voorbereiden

Er zijn twee spreadsheets geopend, naast elkaar. Het ene bestand bevat de structuur van het Commerce-exportbestand en het andere bevat de nieuwe gegevens over het belastingtarief die u wilt importeren.

1. Als u een werkplek in het werkblad wilt maken met de nieuwe gegevens over belastingtarieven, voegt u zoveel lege kolommen helemaal rechts in als nodig is om gegevens uit het Commerce-exportbestand toe te voegen. Gebruik cut-and-paste om de gegevens toe te voegen en dan de kolommen opnieuw te rangschikken zodat zij de orde van het de uitvoergegevensbestand van Commerce aanpassen.

1. Wijzig de naam van de kolomkoppen in overeenstemming met de Commerce-exportgegevens.

1. Verwijder alle kolommen zonder gegevens.

   Anders moet de structuur van het importbestand overeenkomen met de oorspronkelijke Commerce-exportgegevens.

1. Blader omlaag voordat u het bestand opslaat en controleer of de kolommen met belastingtarieven alleen numerieke gegevens bevatten.

   Alle tekst die in een kolom met belastingtarieven wordt gevonden, voorkomt dat de gegevens worden geïmporteerd.

1. Sla de voorbereide gegevens op als een CSV-bestand.

   Controleer bij de aanwijzing of een komma wordt gebruikt als een veldscheidingsteken en dubbele aanhalingstekens als het tekstscheidingsteken. Klik vervolgens op **[!UICONTROL OK]** .

## Stap 3: Invoer van de belastingtarieven

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Klik op **[!UICONTROL Choose File]** en kies het CSV-bestand met belastingtarieven dat u wilt importeren.

1. Klik op **[!UICONTROL Import Tax Rates]**.

   Het importeren van de gegevens kan enkele minuten duren. Wanneer het proces is voltooid, wordt het bericht `The tax rate has been imported` weergegeven. Als er een foutbericht verschijnt, verhelpt u het probleem in de gegevens en probeert u het opnieuw.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   De geïmporteerde snelheden worden weergegeven in de lijst.

1. Gebruik de paginacontroles om de nieuwe belastingtarieven te bekijken.

   ![ de belastingtarieven van de de invoer van Gegevens ](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. Voer een aantal testtransacties uit in uw winkel met klanten van verschillende ZIP-codes om ervoor te zorgen dat de nieuwe belastingtarieven correct werken.
