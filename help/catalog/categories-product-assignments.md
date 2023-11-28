---
title: Toewijzingen van producten in categorie
description: Meer informatie over het gebruik van de [!UICONTROL Products in Category] instellingen om te bepalen welke producten momenteel aan de categorie worden toegewezen.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Toewijzingen van producten in categorie

Voor een categorie gebruikt u de _[!UICONTROL Products in Category]_om de producten te bekijken die momenteel aan de categorie zijn toegewezen. De zoekfilters boven aan elke kolom worden gebruikt om producten toe te voegen aan en te verwijderen uit de categorie. U kunt ook [categorieregels](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) om de productselectie dynamisch te wijzigen als aan een aantal voorwaarden wordt voldaan. Zie voor meer informatie [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Tijdens de opstelling van categorieregels zijn de producten _gesorteerd_, _gematcht_, _toegewezen_, en _ongeplaatst_ volgens die regel **_alleen_** als deze rubriek is opgeslagen. Om ervoor te zorgen dat een nieuw product volgens de regel wordt toegewezen wanneer u het aan de catalogus toevoegt, **moet elke categorie opnieuw opslaan** dat wordt geplaatst om producten door regel aan te passen. Als de status van een productvoorraad wordt gewijzigd in `In Stock` of `Out of Stock` en producten in de categorie _gesorteerd_ volgens de **Automatisch sorteren** regel, u moet klikken **[!UICONTROL Save Category]**.

![Categorieproducten](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Op de categoriepagina&#39;s: `Out of stock` producten worden altijd weergegeven **_na_** `In Stock` producten in de productlijst met alle sorteertypen.

>[!NOTE]
>
>De _Voorraad_ kolom geeft verkoopbare producthoeveelheid weer voor _**bereik van geselecteerde categorie**_ alleen. Wanneer de veelvoudige voorraden voor producten worden beheerd, zou u tussen het overeenkomstige werkingsgebied moeten schakelen om andere te tonen _Voorraad_ kolomwaarden in het dialoogvenster _Categorieproducten_ raster.

## Een categorieregel toepassen

{{ee-feature}}

1. Set **[!UICONTROL Match products by rule]** tot `Yes`.

   De opties voor automatisch sorteren en voorwaarden worden weergegeven.

   ![Producten op regel afstemmen](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Stel de **[!UICONTROL Automatic Sorting]** bestelling.

   Deze automatische sortering is gebaseerd op de huidige omstandigheden.

   - `Stock level` - Naar boven of onder.
   - `Special price` - Naar boven of onder.
   - `New Products` - Nieuwste producten eerst aanbieden.
   - `Color` - alfabetisch sorteren op kleur.
   - `Name` - Sorteren in oplopende of aflopende volgorde op naam.
   - `SKU` - Sorteren in oplopende of aflopende volgorde op SKU
   - `Price` - Sorteren in oplopende of aflopende volgorde op prijs.

1. Klikken **[!UICONTROL Add Condition]** en voer de volgende handelingen uit:

   - Kies de optie **[!UICONTROL Attribute]** dat is de basis van de voorwaarde .
   - Kies de optie **[!UICONTROL Operator]** vereist om de expressie te vormen.
   - Voer de **[!UICONTROL Value]** dat moet worden nagekomen .

   ![Voorwaarde toevoegen aan categorieregel](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Herhaal dit proces voor elk attribuut dat moet worden gebruikt om de voorwaarden te beschrijven om aan te voldoen. Bijvoorbeeld, om producten aan te passen die van 7 tot 30 dagen geleden werden gecreeerd, doe het volgende:

   - Set **[!UICONTROL Date Created]** tot `Less than 30`.
   - Set **[!UICONTROL Logic]** tot `AND`.
   - Set **[!UICONTROL Date Modified]** tot `Greater than 7`.

1. Klik op **[!UICONTROL Save Category]**.

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
| [!UICONTROL Attribute] | Bepaalt het attribuut dat als basis van de voorwaarde wordt gebruikt. Opties: <br/>**[!UICONTROL Clone Category ID(s)]**- Producten dynamisch klonen, zonder sortering en volgorde, uit meerdere categorieën op basis van categorie-id.<br/>**[!UICONTROL Color]** - Omvat producten op basis van kleur. <br/>**[!UICONTROL Date Created (days ago)]**- Omvat producten op basis van het aantal dagen sinds de producten aan de catalogus zijn toegevoegd.<br/>**[!UICONTROL Date Modified (days ago)]** - Omvat producten op basis van het aantal dagen sinds de laatste wijziging van de producten. <br/>**[!UICONTROL Name]**- Omvat producten op basis van de productnaam.<br/>**[!UICONTROL Price]** - Omvat producten op basis van de prijs. <br/>**[!UICONTROL Quantity]**- Omvat producten op basis van de hoeveelheid in voorraad.<br/>** SKU **- Omvat producten op basis van SKU. |
| [!UICONTROL Operator] | Geeft de operator op die op de kenmerkwaarde wordt toegepast om aan de voorwaarde te voldoen. Tenzij een operator is opgegeven, `Equal` wordt gebruikt als standaard. Opties: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Geeft de waarde op die het kenmerk aan de voorwaarde moet voldoen. |
| [!UICONTROL Logic] | Wordt gebruikt om meerdere voorwaarden te definiëren en wordt alleen weergegeven wanneer een andere voorwaarde wordt toegevoegd. Opties: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>De hoeveelheid van een configureerbaar product met kindopties wordt berekend door alle verkoopbare aantallen van het kindproduct te combineren. Overweeg een voorbeeld van een configureerbaar product _Duurzaamheid, tank_ met opties voor paarse, rode en gele kleur en verschillende hoeveelheden van beide. In dit scenario is de hoeveelheid van het bovenliggende product de gecombineerde verkoopbare hoeveelheid van de onderliggende producten van paarse, rode en gele kleuren.

## Besturingselementen


## Paginabesturingselementen

{{ee-feature}}

| Besturing | Beschrijving |
|----------|--------------|
| ![Weergeven als lijst](../assets/icon-view-list.png) | Weergeven als lijst |
| ![Weergeven als tegels](../assets/icon-view-tiles.png) | Weergeven als tegels |
| ![Niet in-/uitschakelen](../assets/toggle-no.png) | Op regel afstemmen - Nee |
| ![Ja in-/uitschakelen](../assets/toggle-yes.png) | Op regel afstemmen - Ja |
| ![Bediening verplaatsen](../assets/icon-move.png) | Met het besturingselement voor slepen en neerzetten kunt u een product vastpakken en naar een andere positie op de huidige pagina van het raster verplaatsen. Zie voor meer informatie [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Positiecontrole](../assets/control-position.png) | Bepaalt de positie van het product in de lijst. |

{style="table-layout:auto"}

## Paginabesturingselementen

{{ce-feature}}

| Besturing | Beschrijving |
|----------|--------------|
| ![Selectievakje](../assets/checkbox-selected.png) | Gebruik het selectievakje in de koptekst van de eerste kolom voor het selecteren van alle producten of het wissen van alle selecties. Het besturingselement in de eerste rij bepaalt het type zoekopdracht en kan zo worden ingesteld dat alle records worden opgenomen. U kunt ook alleen de records opnemen die al dan niet zijn toegewezen aan de categorie. Het selectievakje in de eerste kolom van elke rij geeft de producten aan die aan de categorie moeten worden toegevoegd. Opties: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | De filterbesturingselementen boven aan elke kolom kunnen worden gebruikt om specifieke waarden in te voeren die u wilt opnemen in de lijst of uit de lijst wilt verwijderen, afhankelijk van de instelling Alles selecteren. |
| [!UICONTROL Reset Filter] | Wist alle zoekfilters. |
| [!UICONTROL Search] | Hiermee doorzoekt u de catalogus op basis van de filtercriteria en geeft u het resultaat weer. |

{style="table-layout:auto"}
