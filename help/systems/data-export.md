---
title: Gegevens exporteren
description: Meer informatie over filters en kenmerken voor het exporteren van gegevens en over het exporteren van gegevens uit uw winkel.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Gegevens exporteren

De beste manier om vertrouwd te raken met de structuur van uw database is de gegevens te exporteren en deze in een spreadsheet te openen. Nadat u met het proces vertrouwd bent geworden, kunt u het als efficiënte manier gebruiken om grote hoeveelheden informatie te beheren.

Speciale tekens, zoals het gelijkteken, groter en kleiner dan symbolen, enkele en dubbele aanhalingstekens, backslash, pipe en en en ampersand-symbolen, kunnen problemen veroorzaken tijdens de gegevensoverdracht. Om ervoor te zorgen dat dergelijke speciale karakters correct worden geïnterpreteerd, kunnen zij als _vluchtopeenvolging_ worden gemerkt. Als de gegevens bijvoorbeeld een tekenreeks `code="str"`, `code="str2"` bevatten en de tekst tussen dubbele aanhalingstekens wordt geplaatst, weet u zeker dat de oorspronkelijke dubbele aanhalingstekens deel uitmaken van de gegevens: `"code="str""` . Wanneer het systeem een dubbele reeks dubbele citaten ontmoet, begrijpt het dat de buitenste reeks dubbele citaten de daadwerkelijke gegevens omsluit.

Het exporteren van gegevens is een asynchrone bewerking die op de achtergrond wordt uitgevoerd, zodat u kunt blijven werken in Beheer zonder te wachten tot de bewerking is voltooid. Het systeem geeft een bericht weer wanneer de taak is voltooid.

## Uitvoercriteria

Exportfilters worden gebruikt om de gegevens op te geven die u in het exportbestand wilt opnemen op basis van de kenmerkwaarde. Daarnaast kunt u opgeven welke kenmerkgegevens u wilt opnemen in of uitsluiten van de exportbewerking.

![ de uitvoercriteria van Gegevens ](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Exportfilters

U kunt filters gebruiken om te bepalen welke SKUs in het de uitvoerdossier inbegrepen zijn. Als u bijvoorbeeld een waarde invoert in het filter Land van vervaardiging, bevat het geëxporteerde CSV-bestand alleen producten die in dat land zijn gemaakt.

Het type filter komt overeen met het gegevenstype. Voor datumgebieden, kunt u de datum van het pictogram van de Kalender ![ kiezen Kalender ](../assets/icon-calendar.png). Zie {de Types van Invoer van 0} Attributen ](../catalog/attributes-input-types.md) voor meer informatie.[

Het formaat van de datum wordt bepaald door de [ scène ](../getting-started/store-details.md#locale-options).

Als u alleen records met een specifieke waarde wilt opnemen, zoals een SKU, voert u de waarde in het veld Filter in. Sommige velden, zoals Prijs, Dikte en Product instellen als Nieuw, hebben een waardebereik van/tot.

### Kenmerken uitsluiten

Het selectievakje in de eerste kolom wordt gebruikt om kenmerken uit te sluiten van het exportbestand. Als een attribuut wordt uitgesloten, is de bijbehorende kolom in de uitvoergegevens inbegrepen, maar leeg.

| Uitsluiten | Filter | Resultaat |
|--- |--- |--- |
| ![ Cleared checkbox ](../assets/checkbox-clear.png) | Nee | Het geëxporteerde bestand bevat elk kenmerk voor alle bestaande records. |
| ![ Cleared checkbox ](../assets/checkbox-clear.png) | Ja | Het exportbestand bevat elk kenmerk met alleen de records die door het filter zijn toegestaan. |
| ![ Geselecteerde checkbox ](../assets/checkbox-selected.png) | Nee | Het exportbestand bevat niet de kolom voor het uitgesloten kenmerk, maar wel alle bestaande records. |
| ![ Geselecteerde checkbox ](../assets/checkbox-selected.png) | Ja | Het exportbestand bevat niet de kolom voor het uitgesloten kenmerk en bevat alleen de records die door het filter zijn toegestaan. |

{style="table-layout:auto"}

## Gegevens exporteren

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. In de _sectie van de Montages van de Uitvoer_, plaats **[!UICONTROL Entity Type]** aan één van het volgende:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![ de uitvoermontages van Gegevens ](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Accepteer de standaardwaarde **[!UICONTROL Export File Format]** van CSV.

1. Als u om het even welke speciale karakters wilt insluiten die in de gegevens als _vluchtopeenvolging_ zouden kunnen worden gevonden, selecteer **[!UICONTROL Fields Enclosure]** checkbox.

1. Wijzig zo nodig de weergave van de entiteitskenmerken.

   Standaard worden in de sectie Entiteitskenmerken alle beschikbare kenmerken in alfabetische volgorde weergegeven. U kunt de standaard [ lijstcontroles ](../getting-started/admin-grid-controls.md) gebruiken om naar specifieke attributen te zoeken en de lijst te sorteren. Met de besturingselementen Filter Zoeken en Herstellen bepaalt u de weergave van de lijst, maar dit heeft geen invloed op de selectie van de kenmerken die moeten worden opgenomen in het exportbestand.

   ![ de uitvoer gefilterde entiteitattributen van Gegevens ](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Ga als volgt te werk om de geëxporteerde gegevens te filteren op basis van de kenmerkwaarde:

   - Als u alleen records met specifieke kenmerkwaarden wilt exporteren, voert u de vereiste waarde in de kolom **[!UICONTROL Filter]** in. In het volgende voorbeeld wordt alleen een specifieke SKU geëxporteerd.

   - Als u een kenmerk wilt weglaten bij het exporteren, schakelt u het selectievakje **[!UICONTROL Exclude]** aan het begin van de rij in. Als u bijvoorbeeld alleen de kolommen `sku` en `image` wilt exporteren, schakelt u het selectievakje van elk ander kenmerk in. De kolom wordt weergegeven in het exportbestand, maar zonder waarden.

1. Schuif omlaag en klik op **[!UICONTROL Continue]** in de rechterbenedenhoek van de pagina.

   Na voltooiing van de taak wordt het bestand verwerkt via een wachtrij met berichten (zorg ervoor dat de uitsnijdtaak wordt uitgevoerd). Het geëxporteerde bestand wordt opgeslagen in de `var/export/ folder` . Voor meer informatie over de berichtrij, zie [ berichtrijen ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) beheren in de _Gids van de Configuratie_.

   U kunt het geëxporteerde CSV-bestand opslaan of openen als spreadsheet, de gegevens vervolgens bewerken en weer importeren in uw winkel.

   >[!NOTE]
   >
   >Standaard bevinden alle geëxporteerde bestanden zich in de map `<Magento-root-directory>/var/export` . Als de externe opslagmodule is ingeschakeld, bevinden alle geëxporteerde bestanden zich in de map `<remote-storage-root-directory>/import_export/export` .

## Bronnen voor probleemoplossing

Raadpleeg de volgende artikelen in de Commerce Support Knowledge Base voor hulp bij het oplossen van problemen met het exporteren van gegevens:

- [ Uitgevoerde producten.csv- dossier verschijnt niet ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [ de uitvoerdossier van het Product tonen niet in Admin ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [ Uitgave in het uitvoeren van orden in formaat CSV ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
