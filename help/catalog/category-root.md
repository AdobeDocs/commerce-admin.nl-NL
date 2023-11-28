---
title: Hoofdcategorie en hiërarchie
description: Leer meer over de categoriehiërarchie en de hoofdcategorie, die fungeert als container voor het hoofdmenu in de categoriestructuur.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Hoofdcategorie en hiërarchie

De producten in het hoofdmenu worden bepaald door de hoofdcategorie die is toegewezen aan de [winkel](../stores-purchase/stores.md#add-stores). De hoofdcategorie is in feite een container voor het hoofdmenu in de categoriestructuur. U kunt een wortelcategorie met een volledig nieuwe reeks producten tot stand brengen of producten van een bestaande wortelcategorie kopiëren. De hoofdcategorie kan worden toegewezen aan de huidige winkel of aan elke andere winkel op dezelfde website.

![Hiërarchiediagram van catalogus](./assets/catalog-hierarchy-scope.svg){width="550"}

Vanuit Beheer is de categoriestructuur vergelijkbaar met een ondersteboven liggende structuur, met bovenaan het basiselement. De hoofdmap heeft een naam, maar geen URL-sleutel en wordt niet weergegeven in de [topnavigatie](navigation-top.md) van de winkel. Alle andere categorieën in het menu worden onder het hoofdknooppunt genest. Aangezien de hoofdcategorie het hoogste niveau van de catalogus is, kan in uw winkel slechts één hoofdcategorie tegelijk actief zijn. U kunt echter extra hoofdcategorieën maken voor alternatieve catalogusstructuren en verschillende winkels.

In het volgende voorbeeld ziet u hoe u een hoofdcategorie maakt en deze toewijst aan een andere winkel.

## Stap 1: Een hoofdcategorie maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Klik links op **[!UICONTROL Add Root Category]**.

   ![Nieuwe hoofdcategorie](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Category Name]**.

   De naam die u kiest, wordt in eerste instantie toegewezen aan alle weergaven van de winkel.

1. Ga als volgt te werk als u producten uit de huidige catalogus wilt toevoegen aan de catalogus:

   - Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _Producten in categorie_ sectie.

   - Gebruik de [zoekfilters](../getting-started/admin-grid-controls.md) om de gewenste producten te zoeken en schakel het selectievakje in voor elk product dat u naar de nieuwe catalogus wilt kopiëren.

1. Klik op **[!UICONTROL Save]**.

## Stap 2: Het hoofdmenu maken

1. Selecteer links de nieuwe hoofdcategorie die u in de vorige stap hebt gemaakt.

1. Als u de opdracht [categoriestructuur](category-create.md) voor het hoofdmenu klikt u op **[!UICONTROL Add Subcategory]** en volgt u de instructies.

## Stap 3: Wijs de wortelcategorie aan de opslag toe

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. In de _Winkels_ klikt u op de opslagplaats die u wilt toewijzen aan de nieuwe catalogus.

1. Set **[!UICONTROL Root Category]** naar de nieuwe hoofdcategorie die u hebt gemaakt.

1. Zorg ervoor dat de winkel een **[!UICONTROL Default Store View]** toegewezen.

   De winkel moet ten minste één [winkelweergave](../stores-purchase/store-views.md).

1. Klik op **[!UICONTROL Save Store]**.

1. Ga als volgt te werk om te controleren of de winkel een nieuwe catalogus heeft:

   - Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Producten die naar de nieuwe catalogus zijn gekopieerd, worden in het raster weergegeven.

   - Ga naar de winkel om te controleren of de nieuwe catalogus en het hoofdmenu goed werken.
