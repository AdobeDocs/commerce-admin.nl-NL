---
title: Bovenste navigatie
description: Leer hoe u het hoofdmenu van een winkel definieert. Dit werkt als een map voor de verschillende afdelingen.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Bovenste navigatie

Het hoofdmenu van uw winkel is vergelijkbaar met een directory naar de verschillende afdelingen in uw winkel. Elke optie vertegenwoordigt een andere categorie producten. De positie en presentatie van de bovenste navigatie kunnen per thema verschillen, maar de manier waarop deze werkt, is in wezen hetzelfde.

![Bovenste navigatie](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

De categoriestructuur van uw catalogus kan van invloed zijn op hoe goed uw site wordt geïndexeerd door zoekprogramma&#39;s. Hoe dieper een categorie genest, hoe minder waarschijnlijk het is dat deze grondig geïndexeerd wordt. Over het algemeen is het gebruik van een tot drie zichtbare niveaus het meest effectief. De [hoofdcategorie](category-root.md) telt als het eerste niveau, hoewel het niet in het menu verschijnt. Het maximumaantal niveaus dat beschikbaar is in de hoogste navigatie wordt bepaald door de configuratie. Bovendien kan er een limiet zijn voor het aantal menuniveaus dat door uw winkelthema wordt ondersteund. Het voorbeeldthema Luma ondersteunt bijvoorbeeld maximaal vijf niveaus, inclusief de hoofdmap.

## Maniveaus tellen

| Item | Beschrijving |
|--- |--- |
| Niveau 1 | Het eerste niveau is de hoofdcategorie, die in de voorbeeldgegevens &#39;&#39;Standaardcategorie&#39;&#39; wordt genoemd. De hoofdmap is een container voor het menu en de naam ervan wordt niet als een optie in het menu weergegeven. |
| Niveau 2 | Op een desktopscherm is de bovenste navigatie het hoofdmenu dat boven aan de pagina wordt weergegeven. Op een mobiel apparaat wordt het hoofdmenu doorgaans weergegeven als een vlieg-uitmenu met opties. De opties op het tweede niveau in de Luminawinkel zijn _Nieuwe functies_, _Vrouwen_, _Mannen_, _Tandwiel_, _Training_, en _Verkoop_. |
| Niveau 3 | Het derde niveau wordt onder elke hoofdmenuoptie weergegeven. Bijvoorbeeld onder _Vrouwen_ zijn de opties op het derde niveau _Tops_ en _Bottoms_. |
| Niveau 4 | De opties op het vierde niveau zijn subcategorieën die uit een optie op het derde niveau vliegen. Bijvoorbeeld onder _Tops_ De menuopties op het vierde niveau zijn: _Jasjes_, _Hoodies en overhemden_, _Tees_, en _Bramen en tanks_. |

{style="table-layout:auto"}

## Bovenste navigatie instellen

Voer de volgende stappen uit om een categorie in de bovenste navigatie van een winkel weer te geven:

### Stap 1: Een categorie maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Een **[!UICONTROL Store View]** om te bepalen waar de nieuwe categorie beschikbaar moet zijn.

1. Selecteer in de categoriestructuur de bovenliggende categorie van de nieuwe categorie.

   Als u zonder gegevens vanaf het begin begint, zijn er mogelijk slechts twee categorieën in de lijst: _Standaardcategorie_, dat de basis vormt, en _Voorbeeldcategorie_.

1. Klik op **[!UICONTROL Add Subcategory]**.

1. Voltooi de basisgegevens met de volgende instellingen:

   - **[!UICONTROL Enable Category]** instellen op `Yes`
   - **[!UICONTROL Include in Menu]** instellen op `Yes`

1. In weergaveset **[!UICONTROL Anchor]** tot `Yes`.

1. Alle overige vereiste gegevens invullen [categorieinstellingen](category-create.md).

1. Klik op **[!UICONTROL Save]**.

Voor een installatie met meerdere opslagruimten kan een ander hoofdmenu worden toegewezen als de [hoofdcategorie](category-root.md) voor elke [winkel](../stores-purchase/stores.md#add-stores).

### Stap 2: De diepte van de bovenste navigatie instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Vouw de sectie **[!UICONTROL Category Top Navigation]** uit.

   ![Bovenste categorie navigatie](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Omdat de diepte van de bovenste navigatie een algemene waarde heeft [configuratiebereik](../getting-started/websites-stores-views.md#scope-settings), is het plaatsen op alle websites, opslag van toepassing, en opslagmeningen in de installatie van de Handel. De _[!UICONTROL Category Top Navigation]_configuratiesectie is alleen beschikbaar als_[!UICONTROL Store View]_ in de linkerbovenhoek is ingesteld op `Default Config`.

   Voor een gedetailleerde lijst van deze opties, zie [Bovenste categorie navigatie](../configuration-reference/catalog/catalog.md#layered-navigation) in de _Configuratieverwijzing_.

1. Als u het aantal subcategorieën in de bovenste navigatie wilt beperken, voert u het getal in voor **[!UICONTROL Maximal Depth]**.

   De standaardwaarde is `0`, waarin geen beperking wordt gesteld aan het aantal niveaus van subcategorieën.

1. Klik op **[!UICONTROL Save Config]**.
