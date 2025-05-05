---
title: Platte catalogi
description: Meer informatie over het maken van een platte catalogus, waarbij elke rij alle benodigde gegevens over een product of categorie bevat.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Platte catalogi

>[!IMPORTANT]
>
>Het gebruik van een platte catalogus wordt niet langer aanbevolen als beste praktijk. Het is bekend dat voortdurend gebruik van deze functie prestatievermindering en andere indexeringsproblemen kan veroorzaken. Een gedetailleerde beschrijving en de oplossing zijn beschikbaar in het [ Centrum van de Hulp ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html?lang=nl-NL).<br/><br/> beïnvloede versies omvatten: <br/> - Adobe Commerce op wolkeninfrastructuur, 2.3.x en boven <br/> - Adobe Commerce (op-Premise), 2.3.x en boven <br/> - Magento Open Source, 2.3.x en boven <br/><br/> op om het even welke versieversie, werken sommige uitbreidingen slechts met vlakke lijsten, zo creërend een risico als u vlakke lijsten onbruikbaar maakt. Als u weet dat u extensies hebt die gebruikmaken van Platte catalogusindexen, moet u rekening houden met dit risico wanneer u deze waarden instelt op `No` .

Commerce slaat catalogusgegevens doorgaans op in meerdere tabellen, op basis van het model Entiteit-Attribute-Value (EAV). Omdat productkenmerken in veel tabellen worden opgeslagen, zijn SQL-query&#39;s soms lang en complex.

Een platte catalogus maakt daarentegen direct tabellen, waarin elke rij alle benodigde gegevens over een product of categorie bevat. Een platte catalogus wordt automatisch bijgewerkt, elke minuut of op basis van de snijtaak. Met een platte catalogusindexering kan ook de verwerking van de regels voor de catalogusprijs en de kartprijs worden versneld. Een catalogus met maximaal 500.000 SKU&#39;s kan snel worden geïndexeerd als een platte catalogus.

>[!NOTE]
>
>Voordat u een platte catalogus voor een live winkel inschakelt, moet u de configuratie in een ontwikkelomgeving testen.

## Stap 1: De vlakke catalogus inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid de _sectie Storefront_ uit en doe het volgende:

   - Stel **[!UICONTROL Use Flat Catalog Category]** in op `Yes` . (Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit.)

   - Stel **[!UICONTROL Use Flat Catalog Product]** in op `Yes` .

   ![ Vlakke catalogusconfiguratie ](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Wanneer u wordt gevraagd de cache bij te werken, klikt u op **[!UICONTROL Cache Management]** in het systeembericht en volgt u de instructies om de cache te vernieuwen.

## Stap 2: Verifieer de resultaten

U kunt de resultaten op twee manieren controleren.

### Methode 1: De resultaten voor één product verifiëren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de bewerkingsmodus.

1. Voeg bij **[!UICONTROL Name]** de tekst `_TEST` toe aan het einde van de productnaam.

1. Klik op **[!UICONTROL Save]**.

1. Navigeer op een nieuw browsertabblad naar de homepage van uw winkel en voer de volgende handelingen uit:

   - Zoeken naar het product dat u hebt bewerkt.

   - Gebruik de navigatie om naar het product onder zijn toegewezen categorie te bladeren.

     Vernieuw indien nodig de pagina om de resultaten te zien. De verandering verschijnt binnen de minuut of volgens uw [ Gewas ](../systems/cron.md) programma.

   ![ Storefront met Platte Catalogus ](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Methode 2: De resultaten voor een categorie verifiëren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Controleer in de linkerbovenhoek of **[!UICONTROL Store View]** is ingesteld op `All Store Views` .

   Klik desgevraagd op **[!UICONTROL OK]** om te bevestigen.

1. Selecteer een bestaande categorie in de categoriestructuur, klik op **[!UICONTROL Add Subcategory]** en voer de volgende handelingen uit:

   - Voer bij **[!UICONTROL Category Name]** `Test Category` in.

   - Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

     ![ subcategory van de Test ](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Products in Category]** sectie uit en klik **[!UICONTROL Reset Filter]** om alle producten te tonen.

   - Schakel het selectievakje in van verschillende producten die aan de nieuwe categorie moeten worden toegevoegd.

   - Klik op **[!UICONTROL Save]** .

   ![ de categorieproducten van de Test ](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. Navigeer op een nieuw browsertabblad naar de homepage van uw winkel en gebruik de winkelnavigatie om naar de categorie te bladeren die u hebt gemaakt.

   Vernieuw indien nodig de pagina om de resultaten te zien. De wijziging wordt binnen de minuut of volgens het uitsnijdschema weergegeven.

## Stap 3: De testgegevens verwijderen

Ga als volgt te werk om de testgegevens te verwijderen en de oorspronkelijke productnaam en catalogusconfiguratie te herstellen.

### De testcategorie verwijderen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de testsubcategorie die u hebt gemaakt.

1. Klik in de rechterbovenhoek op **[!UICONTROL Delete]** .

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

   Als u deze categorie verwijdert, worden de producten die aan de categorie zijn toegewezen, niet verwijderd.

### De oorspronkelijke productnaam herstellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Open het testproduct in de bewerkingsmodus.

1. Verwijder de `_TEST` tekst die u aan **[!UICONTROL Product Name]** hebt toegevoegd.

1. Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

### De oorspronkelijke catalogusconfiguratie herstellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid de _sectie Storefront_ uit en doe het volgende:

   - Stel **[!UICONTROL Use Flat Catalog Category]** in op `No` .

   - Stel **[!UICONTROL Use Flat Catalog Product]** in op `No` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Vernieuw de cache wanneer daarom wordt gevraagd.
