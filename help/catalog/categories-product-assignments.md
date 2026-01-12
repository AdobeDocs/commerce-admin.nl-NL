---
title: Toewijzingen van producten in categorie
description: Leer hoe u de [!UICONTROL Products in Category] -instellingen gebruikt om te bepalen welke producten momenteel aan de categorie zijn toegewezen.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Toewijzingen van producten in categorie

Voor een categorie gebruikt u de sectie _[!UICONTROL Products in Category]_om de producten te bekijken die momenteel aan de categorie zijn toegewezen. De zoekfilters boven aan elke kolom worden gebruikt om producten toe te voegen aan en te verwijderen uit de categorie. U kunt [ categorieregels ](../merchandising-promotions/category-product-rules.md) ( ![ Adobe Commerce ](../assets/adobe-logo.svg) Adobe Commerce slechts) ook gebruiken om de productselectie dynamisch te veranderen wanneer een reeks voorwaarden wordt voldaan aan. Meer leren, zie [ Visuele Merchandiser ](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Tijdens de opstelling van de categorieregel, worden de producten _gesorteerd,_ aangepast _,_ toegewezen _, en_ niet toegewezen _volgens die regel_ slechts **_wanneer deze categorie wordt bewaard._** Om ervoor te zorgen dat een nieuw product volgens de regel wordt toegewezen wanneer u het aan de catalogus toevoegt, moet u **elke categorie** resave die wordt geplaatst om producten door regel aan te passen. Ook, als om het even welke status van de productvoorraad in `In Stock` of `Out of Stock` wordt veranderd en de producten in de categorie _gesorteerd_ volgens de **Automatische het Sorteren** regel, moet u **[!UICONTROL Save Category]** klikken.

![ Producten van de Categorie ](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>De _kolomvertoningen van de Beeld_ beschikbare producthoeveelheid voor _**geselecteerd categoriewerkingsgebied**_ slechts. Wanneer de veelvoudige voorraden voor producten worden beheerd, zou u tussen het overeenkomstige werkingsgebied moeten schakelen om andere _de kolomwaarden van de Beeld_ in het _CategorieProducten_ net te tonen.

## Een categorieregel toepassen

{{ee-feature}}

1. Stel **[!UICONTROL Match products by rule]** in op `Yes` .

   De opties voor automatisch sorteren en voorwaarden worden weergegeven.

   ![ om Producten door Regel ](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"} aan te passen

1. Stel de **[!UICONTROL Automatic Sorting]** volgorde in.

   Deze automatische sortering is gebaseerd op de huidige omstandigheden.

   - `Stock level` - Ga naar boven of onder.
   - `Special price` - Ga naar boven of onder.
   - `New Products` - Nieuwste producten eerst weergeven.
   - `Color` - alfabetisch sorteren op kleur.
   - `Name` - Sorteer in oplopende of aflopende volgorde op Naam.
   - `SKU` - Sorteren in oplopende of aflopende volgorde op SKU
   - `Price` - Sorteer in oplopende of aflopende volgorde op Prijs.

1. Klik op **[!UICONTROL Add Condition]** en voer de volgende handelingen uit:

   - Kies de **[!UICONTROL Attribute]** die de basis van de voorwaarde is.
   - Kies de **[!UICONTROL Operator]** die nodig is om de expressie te vormen.
   - Voer de **[!UICONTROL Value]** in die moet worden aangepast.

   ![ voeg Voorwaarde aan de Regel van de Categorie toe ](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Herhaal dit proces voor elk attribuut dat moet worden gebruikt om de voorwaarden te beschrijven om aan te voldoen. Bijvoorbeeld, om producten aan te passen die van 7 tot 30 dagen geleden werden gecreeerd, doe het volgende:

   - Stel **[!UICONTROL Date Created]** in op `Less than 30` .
   - Stel **[!UICONTROL Logic]** in op `AND` .
   - Stel **[!UICONTROL Date Modified]** in op `Greater than 7` .

1. Klik op **[!UICONTROL Save Category]** als de bewerking is voltooid.

### Paginaopties

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Match products by rule] | Hiermee wordt bepaald of de lijst met producten in de categorie dynamisch wordt gegenereerd door een categorieregel. Opties: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | Hiermee wordt automatisch een sorteervolgorde toegepast op de lijst met categorieproducten. Opties: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Voegt een andere voorwaarde aan de regel toe. |

{style="table-layout:auto"}

### Paginavoorwaarden

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Attribute] | Bepaalt het attribuut dat als basis van de voorwaarde wordt gebruikt. Opties: <br/>**[!UICONTROL Clone Category ID(s)]**- kloont producten dynamisch, zonder sorteren en volgorde, van meerdere categorieën op basis van categorie-id.<br/>**[!UICONTROL Color]** - Bevat producten die op kleur zijn gebaseerd. <br/>**[!UICONTROL Date Created (days ago)]**- Bevat producten op basis van het aantal dagen sinds de producten aan de catalogus zijn toegevoegd.<br/>**[!UICONTROL Date Modified (days ago)]** - Bevat producten op basis van het aantal dagen sinds de producten voor het laatst zijn gewijzigd. <br/>**[!UICONTROL Name]**- Bevat producten op basis van de productnaam.<br/>**[!UICONTROL Price]** - Bevat producten op basis van de prijs. <br/>**[!UICONTROL Quantity]**- Bevat producten op basis van de hoeveelheid in voorraad.<br/>** SKU **- omvat producten die op SKU worden gebaseerd. |
| [!UICONTROL Operator] | Geeft de operator op die op de kenmerkwaarde wordt toegepast om aan de voorwaarde te voldoen. Tenzij een operator is opgegeven, wordt `Equal` als de standaardwaarde gebruikt. Opties: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Geeft de waarde op die het kenmerk aan de voorwaarde moet voldoen. |
| [!UICONTROL Logic] | Wordt gebruikt om meerdere voorwaarden te definiëren en wordt alleen weergegeven wanneer een andere voorwaarde wordt toegevoegd. Opties: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>De hoeveelheid van een configureerbaar product met kindopties wordt berekend door alle aantallen van het kindproduct te combineren. Overweeg een voorbeeld van een configureerbaar product _Tank van de Hulpwaardigheid van de Duur_ met paars, rood, en gele kleurenopties en verschillende hoeveelheden van elk. In dit scenario is de hoofdproducthoeveelheid de gecombineerde hoeveelheid van de paars-, rood- en gele onderliggende producten.

## Besturingselementen


## Paginabesturingselementen

{{ee-feature}}

| Besturing | Beschrijving |
|----------|--------------|
| ![ Mening als lijst ](../assets/icon-view-list.png) | Weergeven als lijst |
| ![ Mening als tegels ](../assets/icon-view-tiles.png) | Weergeven als tegels |
| ![ knevel nr. ](../assets/toggle-no.png) | Op regel afstemmen - Nee |
| ![ Wissel ja ](../assets/toggle-yes.png) | Op regel afstemmen - Ja |
| ![ controlemechanisme van de Beweging ](../assets/icon-move.png) | Met het besturingselement voor slepen en neerzetten kunt u een product vastpakken en naar een andere positie op de huidige pagina van het raster verplaatsen. Meer leren, zie [ Visuele Merchandiser ](../merchandising-promotions/visual-merchandiser.md). |
| ![ controlemechanisme van de Positie ](../assets/control-position.png) | Bepaalt de positie van het product in de lijst. |

{style="table-layout:auto"}

## Paginabesturingselementen

{{ce-feature}}

| Besturing | Beschrijving |
|----------|--------------|
| ![ Geselecteerde checkbox ](../assets/checkbox-selected.png) | Gebruik het selectievakje in de koptekst van de eerste kolom voor het selecteren van alle producten of het wissen van alle selecties. Het besturingselement in de eerste rij bepaalt het type zoekopdracht en kan zo worden ingesteld dat alle records worden opgenomen. U kunt ook alleen de records opnemen die al dan niet zijn toegewezen aan de categorie. Het selectievakje in de eerste kolom van elke rij geeft de producten aan die aan de categorie moeten worden toegevoegd. Opties: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | De filterbesturingselementen boven aan elke kolom kunnen worden gebruikt om specifieke waarden in te voeren die u wilt opnemen in de lijst of uit de lijst wilt verwijderen, afhankelijk van de instelling Alles selecteren. |
| [!UICONTROL Reset Filter] | Wist alle zoekfilters. |
| [!UICONTROL Search] | Hiermee doorzoekt u de catalogus op basis van de filtercriteria en geeft u het resultaat weer. |

{style="table-layout:auto"}
