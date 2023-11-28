---
title: Producten toevoegen aan een gedeelde catalogus
description: Leer hoe u producten aan een gedeelde catalogus toevoegt, afzonderlijk of in groepen per categorie.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Producten toevoegen aan een gedeelde catalogus

Producten kunnen afzonderlijk of in groepen van meerdere producten per categorie worden toegevoegd aan een gedeelde catalogus.

Een complex product (zoals bundel, gegroepeerd of configureerbaar) kan alleen zichtbaar zijn vanuit de winkel in een gedeelde catalogus als aan de volgende vereisten is voldaan:

- Alles [verwante producten](../catalog/product-configurations.md) en moeten opties worden toegewezen aan dezelfde gedeelde catalogus en worden ingeschakeld in de primaire catalogus.
- Voor [configureerbaar](../catalog/product-create-configurable.md) en [gegroepeerd](../catalog/product-create-grouped.md) alleen de ingeschakelde gekoppelde producten zijn zichtbaar.
- Voor een [bundelen](../catalog/product-create-bundle.md) , moeten alle opties worden opgenomen in de gedeelde catalogus.

  ![Producten voor catalogus selecteren](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Methode 1: Eén product toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ga voor het product in het raster dat u wilt toevoegen naar het _[!UICONTROL Action]_kolom en klik op **[!UICONTROL Edit]**.

1. Omlaag schuiven, uitvouwen ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Product in Shared Catalogs]_en voer de volgende handelingen uit:

   - Schakel het selectievakje in van elke gedeelde catalogus waarin het product moet worden weergegeven. Als u alle catalogi wilt kiezen, klikt u op **[!UICONTROL Select all]**.

     ![Product in gedeelde catalogi](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     De naam van elke geselecteerde catalogus wordt weergegeven in het dialoogvenster _[!UICONTROL Shared Catalogs]_veld.

     ![Gedeelde toegewezen catalogi](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Klikken **[!UICONTROL Done]** om de instellingen op te slaan.

1. Klik op **[!UICONTROL Save]**.

## Methode 2: Meerdere producten toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus in het raster naar _[!UICONTROL Action]_kolom en selecteer **[!UICONTROL Set Pricing and Structure]**.

1. Voer in de categoriestructuur een van de volgende handelingen uit:

   - Klik op **[!UICONTROL Select all]** of selecteer het selectievakje van de bovenliggende categorie.
   - Als u bepaalde productcategorieën wilt opnemen, schakelt u het selectievakje in van elke categorie die u wilt opnemen.
   - Als u een afzonderlijk product wilt opnemen of uitsluiten, schakelt u het selectievakje van het product in of uit.

   De notatie onder elke categorie in de structuur geeft het aantal producten van de categorie weer dat momenteel is opgenomen in de gedeelde catalogus. De notatie onder de [hoofdcategorie](../catalog/category-root.md) Hier wordt het totale aantal producten uit alle categorieën weergegeven die momenteel zijn geselecteerd voor de gedeelde catalogus.

1. Als u categorieproducten in het raster wilt weergeven, klikt u op de naam van de categorie in de boomstructuur.

   Wanneer een categorie wordt geselecteerd, komt het volgende voor:

   - De schakeloptie in de eerste kolom van het raster is ingesteld op `On` voor elk geselecteerd product.
   - Als een product aan meerdere categorieën wordt toegewezen en in een van deze categorieën wordt weggelaten, blijft het beschikbaar via de andere categorieën en via [cataloguszoekopdracht](../catalog/search.md).
   - Het systeem wordt automatisch ingesteld [Categoriemachtigingen](../catalog/category-permissions.md) tot `Allow` voor de geselecteerde producten.
