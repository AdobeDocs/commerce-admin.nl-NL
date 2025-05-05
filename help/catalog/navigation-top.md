---
title: Bovenste navigatie
description: Leer hoe u het hoofdmenu van een winkel definieert. Dit werkt als een map voor de verschillende afdelingen.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Bovenste navigatie

Het hoofdmenu van uw winkel is vergelijkbaar met een directory naar de verschillende afdelingen in uw winkel. Elke optie vertegenwoordigt een andere categorie producten. De positie en presentatie van de bovenste navigatie kunnen per thema verschillen, maar de manier waarop deze werkt, is in wezen hetzelfde.

![ Hoogste Navigatie ](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

De categoriestructuur van uw catalogus kan van invloed zijn op hoe goed uw site wordt geïndexeerd door zoekprogramma&#39;s. Hoe dieper een categorie genest, hoe minder waarschijnlijk het is dat deze grondig geïndexeerd wordt. Over het algemeen is het gebruik van een tot drie zichtbare niveaus het meest effectief. De [ wortelcategorie ](category-root.md) telt als eerste niveau, hoewel het niet in het menu verschijnt. Het maximumaantal niveaus dat beschikbaar is in de hoogste navigatie wordt bepaald door de configuratie. Bovendien kan er een limiet zijn voor het aantal menuniveaus dat door uw winkelthema wordt ondersteund. Het voorbeeldthema Luma ondersteunt bijvoorbeeld maximaal vijf niveaus, inclusief de hoofdmap.

## Maniveaus tellen

| Item | Beschrijving |
|--- |--- |
| Niveau 1 | Het eerste niveau is de hoofdcategorie, die in de voorbeeldgegevens &#39;&#39;Standaardcategorie&#39;&#39; wordt genoemd. De hoofdmap is een container voor het menu en de naam ervan wordt niet als een optie in het menu weergegeven. |
| Niveau 2 | Op een desktopscherm is de bovenste navigatie het hoofdmenu dat boven aan de pagina wordt weergegeven. Op een mobiel apparaat wordt het hoofdmenu doorgaans weergegeven als een vlieg-uitmenu met opties. De opties op het tweede niveau in de opslag van de Luma zijn _wat_, _Vrouwen_, _Mannen_, _Gear_, _Opleiding_, en _Verkoop_ Nieuw is. |
| Niveau 3 | Het derde niveau wordt onder elke hoofdmenuoptie weergegeven. Bijvoorbeeld, onder _Vrouwen_, zijn de opties op het derde niveau _Tops_ en _Bottoms_. |
| Niveau 4 | De opties op het vierde niveau zijn subcategorieën die uit een optie op het derde niveau vliegen. Bijvoorbeeld, onder _Tops_, zijn de opties van het vierde niveaumenu _Jasjes_, _Hoodies &amp; Sweatshirts_, _Tees_, en _Borden &amp; Tanks_. |

{style="table-layout:auto"}

## Bovenste navigatie instellen

Voer de volgende stappen uit om een categorie in de bovenste navigatie van een winkel weer te geven:

### Stap 1: Een categorie maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Stel een **[!UICONTROL Store View]** in om te bepalen waar de nieuwe categorie beschikbaar moet zijn.

1. Selecteer in de categoriestructuur de bovenliggende categorie van de nieuwe categorie.

   Als u van het begin zonder om het even welke gegevens begint, zouden er slechts twee categorieën in de lijst kunnen zijn: _Standaard Categorie_, die de wortel, en een _categorie van het Voorbeeld_ is.

1. Klik op **[!UICONTROL Add Subcategory]**.

1. Voltooi de basisgegevens met de volgende instellingen:

   - **[!UICONTROL Enable Category]** ingesteld op `Yes`
   - **[!UICONTROL Include in Menu]** ingesteld op `Yes`

1. In Weergave-instelling ingesteld op **[!UICONTROL Anchor]** op `Yes` .

1. Voltooi om het even welke andere vereiste [ categoriemontages ](category-create.md).

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

Voor een multistore installatie, kan een verschillend hoofdmenu als [ wortelcategorie ](category-root.md) voor elke [ opslag ](../stores-purchase/stores.md#add-stores) worden toegewezen.

### Stap 2: De diepte van de bovenste navigatie instellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Vouw de sectie **[!UICONTROL Category Top Navigation]** uit.

   ![&#128279;](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"} de Top Navigatie van de Categorie 0&rbrace; &lbrace;

   Omdat de diepte van de hoogste navigatie een globaal [ configuratiewerkingsgebied ](../getting-started/websites-stores-views.md#scope-settings) heeft, is het plaatsen van toepassing op alle websites, opslag, en opslagmeningen in de installatie van Commerce. De configuratiesectie _[!UICONTROL Category Top Navigation]_&#x200B;is alleen beschikbaar als&#x200B;_[!UICONTROL Store View]_ in de linkerbovenhoek is ingesteld op `Default Config` .

   Voor een gedetailleerde lijst van deze opties, zie {de Top Navigatie van de Categorie 0} [&#128279;](../configuration-reference/catalog/catalog.md#layered-navigation) in de _Verwijzing van de Configuratie_.

1. Als u het aantal subcategorieën in de bovenste navigatie wilt beperken, voert u het getal voor **[!UICONTROL Maximal Depth]** in.

   De standaardwaarde is `0` , waarbij geen limiet wordt ingesteld voor het aantal subcategorieniveaus.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
