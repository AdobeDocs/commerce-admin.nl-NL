---
title: Gegevens over belastingtarieven bijwerken
description: Leer hoe u met export- en importbewerkingen de belastingtarieven voor je winkel kunt bijwerken.
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Gegevens over belastingtarieven bijwerken

Als je zaken doet in verschillende landen en een groot aantal producten verzendt, kan het erg tijdrovend zijn om handmatig belastingtarieven in te voeren. Het is sneller en efficiënter om belastingtarieven te downloaden per postcode en deze in de handel te brengen. In het volgende voorbeeld ziet u hoe u een set staatspecifieke belastingtarieven importeert die u van een vertrouwde bron hebt gedownload. Avalara verstrekt [tabellen met belastingtarieven](https://www.avalara.com/taxrates/en/download-tax-tables.html), die je gratis kunt downloaden voor elke postcode in de Verenigde Staten.

>[!NOTE]
>
>Als je geïnteresseerd bent in het automatiseren van je verkoopactiviteiten en het toepassen van belastingregels en -rapportage, kun je naar de optie Vertrouwd op de verkoper gaan [Partners in de handel](https://solutionpartners.adobe.com/s/directory/?solution=commerce) site.

## Stap 1: Exporteer de gegevens over het belastingtarief voor de handel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Klik op **[!UICONTROL Export Tax Rates]**.

1. Zoek het bestand op de downloadlocatie voor uw webbrowser.

1. Sla het bestand op en open het in een spreadsheet.

   Dit voorbeeld gebruikt [!DNL OpenOffice Calc].

   De geëxporteerde gegevens over het belastingtarief voor handel omvatten de volgende kolommen:
   - Code
   - Land
   - Staat
   - Postcode
   - Snelheid
   - Bereik van
   - Bereik tot
   - Een kolom voor elke archiefweergave

   ![Geëxporteerde gegevens - belastingtarieven](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. Open de nieuwe gegevens over het belastingtarief in een tweede instantie van het spreadsheet, zodat kunt u hen naast elkaar zien.

1. Houd bij de nieuwe gegevens over het belastingtarief rekening met eventuele aanvullende gegevens over het belastingtarief die u in uw winkel moet instellen voordat de gegevens worden geïmporteerd.

   De gegevens over het belastingtarief voor Californië omvatten bijvoorbeeld ook:

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   Als u meer wilt importeren [belastingzones en belastingtarieven](../stores-purchase/tax-zones-rates.md), moet u deze eerst definiëren via de beheerder van uw winkel en de [belastingregels](../stores-purchase/tax-rules.md) indien nodig. Exporteer vervolgens de gegevens en open het bestand in een teksteditor, zodat het ter referentie kan worden gebruikt. Om dit voorbeeld eenvoudig te houden, importeren we echter alleen de kolommen met het standaardbelastingtarief.

## Stap 2: De importgegevens voorbereiden

Er zijn twee spreadsheets geopend, naast elkaar. De ene bevat de structuur van het exportbestand Commerce en de andere bevat de nieuwe gegevens over het belastingtarief die u wilt importeren.

1. Om een plaats tot stand te brengen om in spreadsheet met de nieuwe gegevens van het belastingtarief te werken, neem zo vele lege kolommen bij uiterst rechts zonodig op om gegevens van het de uitvoerdossier van de Handel toe te voegen. Gebruik cut-and-paste om de gegevens toe te voegen en dan de kolommen opnieuw te rangschikken zodat passen zij de orde van het de uitvoergegevensbestand van de Handel.

1. Wijzig de naam van de kolomkoppen zodat deze overeenkomen met de exportgegevens van Handel.

1. Verwijder alle kolommen zonder gegevens.

   Anders moet de structuur van het importbestand overeenkomen met de oorspronkelijke exportgegevens van Handel.

1. Blader omlaag voordat u het bestand opslaat en controleer of de kolommen met belastingtarieven alleen numerieke gegevens bevatten.

   Alle tekst die in een kolom met belastingtarieven wordt gevonden, voorkomt dat de gegevens worden geïmporteerd.

1. Sla de voorbereide gegevens op als een CSV-bestand.

   Controleer bij de aanwijzing of een komma wordt gebruikt als een veldscheidingsteken en dubbele aanhalingstekens als het tekstscheidingsteken. Klik vervolgens op **[!UICONTROL OK]**.

## Stap 3: Invoer van de belastingtarieven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Klikken **[!UICONTROL Choose File]** en kiest u het CSV-bestand met belastingtarieven dat u wilt importeren.

1. Klik op **[!UICONTROL Import Tax Rates]**.

   Het importeren van de gegevens kan enkele minuten duren. Wanneer het proces is voltooid, wordt `The tax rate has been imported` wordt weergegeven. Als er een foutbericht verschijnt, verhelpt u het probleem in de gegevens en probeert u het opnieuw.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   De geïmporteerde snelheden worden weergegeven in de lijst.

1. Gebruik de paginacontroles om de nieuwe belastingtarieven te bekijken.

   ![Belastingtarieven voor invoer van gegevens](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. Voer een aantal testtransacties uit in uw winkel met klanten van verschillende ZIP-codes om ervoor te zorgen dat de nieuwe belastingtarieven correct werken.
