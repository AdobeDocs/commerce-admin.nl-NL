---
title: Hoofdcategorie en hiërarchie
description: Leer meer over de categoriehiërarchie en de hoofdcategorie, die fungeert als container voor het hoofdmenu in de categoriestructuur.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Hoofdcategorie en hiërarchie

De producten in het belangrijkste menu worden bepaald door de wortelcategorie die aan de [&#x200B; opslag &#x200B;](../stores-purchase/stores.md#add-stores) wordt toegewezen. De hoofdcategorie is in feite een container voor het hoofdmenu in de categoriestructuur. U kunt een wortelcategorie met een volledig nieuwe reeks producten tot stand brengen of producten van een bestaande wortelcategorie kopiëren. De hoofdcategorie kan worden toegewezen aan de huidige winkel of aan elke andere winkel op dezelfde website.

![&#x200B; de hiërarchiediagram van de Catalogus &#x200B;](./assets/catalog-hierarchy-scope.svg){width="550"}

Vanuit Beheer is de categoriestructuur vergelijkbaar met een ondersteboven liggende structuur, met bovenaan het basiselement. De wortel heeft een naam, maar geen sleutel URL, en verschijnt niet in de [&#x200B; hoogste navigatie &#x200B;](navigation-top.md) van de opslag. Alle andere categorieën in het menu worden onder het hoofdknooppunt genest. Aangezien de hoofdcategorie het hoogste niveau van de catalogus is, kan in uw winkel slechts één hoofdcategorie tegelijk actief zijn. U kunt echter extra hoofdcategorieën maken voor alternatieve catalogusstructuren en verschillende winkels.

In het volgende voorbeeld ziet u hoe u een hoofdcategorie maakt en deze toewijst aan een andere winkel.

## Stap 1: Een hoofdcategorie maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Klik links op **[!UICONTROL Add Root Category]** .

   ![&#x200B; Nieuwe wortelcategorie &#x200B;](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Category Name]** in.

   De naam die u kiest, wordt in eerste instantie toegewezen aan alle weergaven van de winkel.

1. Ga als volgt te werk als u producten uit de huidige catalogus wilt toevoegen aan de catalogus:

   - Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de _Producten in Categorie_ sectie.

   - Gebruik de [&#x200B; onderzoeksfilters &#x200B;](../getting-started/admin-grid-controls.md) om de producten te vinden u en checkbox voor elk product wilt selecteren dat u in de nieuwe catalogus wilt kopiëren.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Stap 2: Het hoofdmenu maken

1. Selecteer links de nieuwe hoofdcategorie die u in de vorige stap hebt gemaakt.

1. Om de [&#x200B; categoriestructuur &#x200B;](category-create.md) voor het belangrijkste menu tot stand te brengen, klik **[!UICONTROL Add Subcategory]** en volg de instructies.

## Stap 3: Wijs de wortelcategorie aan de opslag toe

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. In de _kolom van Slaat_ van het net op, klik de opslag die u de nieuwe catalogus wilt toewijzen.

1. Stel **[!UICONTROL Root Category]** in op de nieuwe hoofdcategorie die u hebt gemaakt.

1. Controleer of er een **[!UICONTROL Default Store View]** aan de winkel is toegewezen.

   De opslag moet minstens één [&#x200B; opslagmening &#x200B;](../stores-purchase/store-views.md) hebben.

1. Klik op **[!UICONTROL Save Store]** als de bewerking is voltooid.

1. Ga als volgt te werk om te controleren of de winkel een nieuwe catalogus heeft:

   - Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Producten die naar de nieuwe catalogus zijn gekopieerd, worden in het raster weergegeven.

   - Ga naar de winkel om te controleren of de nieuwe catalogus en het hoofdmenu goed werken.
