---
title: Platte catalogi
description: Meer informatie over het maken van een platte catalogus, waarbij elke rij alle benodigde gegevens over een product of categorie bevat.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Platte catalogi

>[!IMPORTANT]
>
>Het gebruik van een platte catalogus wordt niet langer aanbevolen als beste praktijk. Het is bekend dat voortdurend gebruik van deze functie prestatievermindering en andere indexeringsproblemen kan veroorzaken. Een gedetailleerde beschrijving en oplossing zijn beschikbaar in de [Help Center](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>Betrokken versies zijn onder meer: <br/>- Adobe Commerce op cloudinfrastructuur, 2.3.x en hoger<br/>- Adobe Commerce (op locatie), 2.3.x en hoger<br/>- Magento Open Source, 2.3.x en hoger <br/><br/>Bij elke releaseversie werken sommige extensies alleen met platte tabellen, wat een risico oplevert als u platte tabellen uitschakelt. Als u weet dat u extensies hebt die gebruikmaken van Platte catalogusindexen, moet u op de hoogte zijn van dit risico wanneer u deze waarden instelt op `No`.

De handel slaat typisch catalogusgegevens in veelvoudige lijsten op, die op het entiteit-Attribuut-Waarde (EAV) model worden gebaseerd. Omdat productkenmerken in veel tabellen worden opgeslagen, zijn SQL-query&#39;s soms lang en complex.

Een platte catalogus maakt daarentegen direct tabellen, waarin elke rij alle benodigde gegevens over een product of categorie bevat. Een platte catalogus wordt automatisch bijgewerkt, elke minuut of op basis van de snijtaak. Met een platte catalogusindexering kan ook de verwerking van de regels voor de catalogusprijs en de kartprijs worden versneld. Een catalogus met maximaal 500.000 SKU&#39;s kan snel worden geïndexeerd als een platte catalogus.

>[!NOTE]
>
>Voordat u een platte catalogus voor een live winkel inschakelt, moet u de configuratie in een ontwikkelomgeving testen.

## Stap 1: De vlakke catalogus inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Breid uit _Storefront_ en voer de volgende handelingen uit:

   - Set **[!UICONTROL Use Flat Catalog Category]** tot `Yes`. (Schakel indien nodig de optie **[!UICONTROL Use system value]** selectievakje.)

   - Set **[!UICONTROL Use Flat Catalog Product]** tot `Yes`.

   ![Vlakke catalogusconfiguratie](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

1. Klik wanneer u wordt gevraagd de cache bij te werken op **[!UICONTROL Cache Management]** in het systeembericht en volg de instructies om de cache te vernieuwen.

## Stap 2: Verifieer de resultaten

U kunt de resultaten op twee manieren controleren.

### Methode 1: De resultaten voor één product verifiëren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de bewerkingsmodus.

1. Voor **[!UICONTROL Name]**, voeg de tekst toe `_TEST` aan het einde van de productnaam.

1. Klik op **[!UICONTROL Save]**.

1. Navigeer op een nieuw browsertabblad naar de homepage van uw winkel en voer de volgende handelingen uit:

   - Zoeken naar het product dat u hebt bewerkt.

   - Gebruik de navigatie om naar het product onder zijn toegewezen categorie te bladeren.

     Vernieuw indien nodig de pagina om de resultaten te zien. De wijziging wordt binnen de minuut of volgens uw [Cron](../systems/cron.md) schema.

   ![Storefront met platte catalogus](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Methode 2: De resultaten voor een categorie verifiëren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Controleer in de linkerbovenhoek of **[!UICONTROL Store View]** is ingesteld op `All Store Views`.

   Klik desgevraagd op **[!UICONTROL OK]** ter bevestiging.

1. Selecteer een bestaande categorie in de categoriestructuur en klik op **[!UICONTROL Add Subcategory]** en voer de volgende handelingen uit:

   - Voor **[!UICONTROL Category Name]**, enter `Test Category`.

   - Klik op **[!UICONTROL Save]**.

     ![Testsubcategorie](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Products in Category]** sectie en klik op **[!UICONTROL Reset Filter]** om alle producten weer te geven.

   - Schakel het selectievakje in van verschillende producten die aan de nieuwe categorie moeten worden toegevoegd.

   - klikken **[!UICONTROL Save]**.

   ![Producten van testcategorieën](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. Navigeer op een nieuw browsertabblad naar de homepage van uw winkel en gebruik de winkelnavigatie om naar de categorie te bladeren die u hebt gemaakt.

   Vernieuw indien nodig de pagina om de resultaten te zien. De wijziging wordt binnen de minuut of volgens het uitsnijdschema weergegeven.

## Stap 3: De testgegevens verwijderen

Ga als volgt te werk om de testgegevens te verwijderen en de oorspronkelijke productnaam en catalogusconfiguratie te herstellen.

### De testcategorie verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de testsubcategorie die u hebt gemaakt.

1. Klik in de rechterbovenhoek op **[!UICONTROL Delete]**.

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.

   Als u deze categorie verwijdert, worden de producten die aan de categorie zijn toegewezen, niet verwijderd.

### De oorspronkelijke productnaam herstellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Open het testproduct in de bewerkingsmodus.

1. Verwijder de `_TEST` tekst die u hebt toegevoegd aan de **[!UICONTROL Product Name]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Save]**.

### De oorspronkelijke catalogusconfiguratie herstellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Breid uit _Storefront_ en voer de volgende handelingen uit:

   - Set **[!UICONTROL Use Flat Catalog Category]** tot `No`.

   - Set **[!UICONTROL Use Flat Catalog Product]** tot `No`.

1. Klik op **[!UICONTROL Save Config]**.

1. Vernieuw de cache wanneer daarom wordt gevraagd.
