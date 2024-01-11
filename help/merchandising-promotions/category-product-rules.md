---
title: Categorievoorschriften voor handelsdoeleinden
description: Leer hoe u regels maakt om de productselecties op dynamische wijze aan te passen aan een aantal voorwaarden.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
source-git-commit: 50951e5aae51067cdba2d8b50c1e530c7f79007a
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---

# Categorievoorschriften voor handelsdoeleinden

{{ee-feature}}

Met Categorieregels wordt de productselectie dynamisch gewijzigd volgens een aantal voorwaarden. Elke categorie kan slechts één categorieregel hebben, hoewel de enige regel meerdere voorwaarden kan hebben. U kunt bijvoorbeeld een categorieregel maken voor een bepaald merk. Producten van hetzelfde merk worden automatisch aan de lijst toegevoegd, zelfs als ze niet aan dezelfde categorie zijn toegewezen. U kunt zoveel voorwaarden aan de expressie toevoegen als u nodig hebt om de producten te beschrijven die u wilt opnemen.

>[!TIP]
>
>Tijdens de opstelling van categorieregels zijn de producten _gesorteerd_, _gematcht_, _toegewezen_, en _ongeplaatst_ volgens die regel **_alleen_** als deze rubriek is opgeslagen. Als u bijvoorbeeld een product aan de catalogus toevoegt en het volgens de regel wilt toewijzen, **moet elke categorie opnieuw opslaan** dat wordt geplaatst om producten door regel aan te passen. Als de status van een productvoorraad wordt gewijzigd in `In Stock` of `Out of Stock` en producten in de categorie _gesorteerd_ volgens de **[!UICONTROL Automatic Sorting]** regel, u moet klikken **[!UICONTROL Save Category]**.

Elke voorwaarde bestaat uit een attribuut, waarde, en logische exploitant. Alleen kenmerken met de _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_eigenschap ingesteld op `Yes` kan worden gebruikt in categorieregels. U moet deze eigenschap instellen voor het kenmerk als u een kenmerk wilt gebruiken dat niet in productlijsten is opgenomen. Hoewel de attributen van de Datum niet worden gesteund, kunt u de Gemaakt Datum of Gewijzigde attributen gebruiken om een datum, of een waaier van data te bepalen. Als u bijvoorbeeld alleen producten wilt opnemen die in de afgelopen week zijn gemaakt, stelt u &#39;Aanmaakdatum&#39; in op de waarde `<7`.

>[!NOTE]
>
>Zorg ervoor om elk attribuut te vormen dat in de regel als a wordt gebruikt [_slim_ attribute](smart-attributes-configure.md).

![Productregel voor categorie](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

De productregels van de categorie kunnen het proces versnellen om specifieke producten aan categorieën toe te wijzen, die op voorwaarden worden gebaseerd die bepalen welke producten in de categorie verschijnen. De &quot;slimme&quot; kenmerken die kunnen worden gebruikt met de regels voor categorieproducten worden gespecificeerd in de [Visual Merchandiser](visual-merchandiser.md) configuratie.

>[!NOTE]
>
>Wees voorzichtig bij het toepassen van een regel voor een categorieproduct, omdat alle producten die niet aan de voorwaarde voldoen, uit de categorie worden verwijderd. Als u bijvoorbeeld een regel maakt die alleen paarse tankdoppen bevat, worden alle andere tanktoppen uit de categorie verwijderd.

## Stap 1: Vorm _slim_ attributes

1. Voor elk attribuut dat in de regel moet worden gebruikt, zorg ervoor dat [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) storefront, eigenschap is ingesteld op `Yes`.

   >[!NOTE]
   >
   >Zorg ervoor dat het kenmerk dat u selecteert GEEN multiselect is _[!UICONTROL Input Type]_.

1. Voltooi de [configuratie](smart-attributes-configure.md) om elk _slim_ attributen die met Visuele Merchandiser moeten worden gebruikt.

## Stap 2: De categorieregel maken

1. Open in de categoriestructuur de categorie die u wilt bewerken.

1. In de **[!UICONTROL Products in Category]** sectie, set **[!UICONTROL Match products by rule]** tot `Yes`.

   De opties voor automatisch sorteren en voorwaarden worden weergegeven.

1. Klik op **[!UICONTROL Add Condition]**.

1. Kies de optie **[!UICONTROL Attribute]** dat is de basis van de voorwaarde .

1. Set **[!UICONTROL Operator]** op een van de volgende wijzen:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Voer de **[!UICONTROL Value]** dat moet worden nagekomen .

   ![Voorwaarde toevoegen aan categorieregel](../catalog/assets/category-rule-create.png){width="500"}

1. Herhaal dit proces voor elk kenmerk dat nodig is om de voorwaarden te beschrijven waaraan moet worden voldaan.

   Bijvoorbeeld, om producten aan te passen die tussen zeven tot 30 dagen geleden werden gecreeerd, doe het volgende:

   - Set **[!UICONTROL Date Created]** tot `Less than 30`.

   - Set **[!UICONTROL Logic]** tot `AND`.

     >[!NOTE]
     >
     >Wanneer u `AND`, is de regel van toepassing op producten die aan alle voorwaarden voldoen. Kies `OR`, is zij van toepassing op producten waaraan ten minste één voorwaarde is voldaan.

   - Set **[!UICONTROL Date Modified]** tot `Greater than 7`.

1. Als u automatisch een sorteervolgorde wilt toepassen op de lijst met dynamisch gegenereerde producten, stelt u **[!UICONTROL Automatic Sorting]**.

   ![Automatisch sorteren](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Sorteervolgordeopties worden globaal gedefinieerd en worden toegepast op basis van de huidige omstandigheden. U kunt geen andere sorteervolgorde instellen voor het weergaveniveau van de website, opslag of opslag.

   | Sorteren, optie | Beschrijving |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Sorteren op basis van voorraad, van boven of beneden: `Move low stock to top` of `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Sorteren op prijs, van boven of beneden: `Special price to top` of `Special price to bottom` |
   | [!UICONTROL New Products] | Nieuwste producten weergeven: `Newest products first` |
   | [!UICONTROL Color] | Alfabet sorteren op kleur: `Sort by color` |
   | [!UICONTROL Product Names] | Sorteren op naam in oplopende of aflopende volgorde: `Name A - Z` of `Name Z -A` |
   | [!UICONTROL SKU] | Sorteren op SKU in oplopende of aflopende volgorde: `SKU: Ascending` of `SKU: Descending` |
   | [!UICONTROL Price] | Sorteren op prijs in oplopende of aflopende volgorde: `Price: High to low` of `Price: Low to high` |

   {style="table-layout:auto"}

1. Klik op **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Wanneer u een categorieregel instelt, worden de producten bijgesneden en aan de regel toegewezen wanneer de categorie wordt opgeslagen. Als u een product aan de catalogus toevoegt en het in de regel wilt omvatten, moet u elke categorie opnieuw opslaan die wordt geplaatst om producten door regel aan te passen. Dit zorgt ervoor dat het nieuwe product wordt opgenomen.

### Menuopties

- **[!UICONTROL Match products by rule]** - Hiermee wordt bepaald of de lijst van producten in de categorie dynamisch wordt gegenereerd door een categorieregel. Opties: `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** - Hiermee wordt automatisch een sorteervolgorde toegepast op de lijst met categorieproducten. Opties: `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low`, en `Price: Low to High`

  >[!NOTE]
  >
  >Als u een configureerbaar product met kindproducten hebt, wordt de voorraad van het ouderproduct berekend gebaseerd op het gecombineerde totaal van de voorraden van het kindproduct. Overweeg een voorbeeld waar u configureerbaar product hebt _Proteus Fitness Shirt_ met oranje, rode en gele kinderproducten met verschillende voorraadhoeveelheden van elk. De voorraad van het bovenliggende product wordt berekend op basis van het gecombineerde totaal van de voorraad van oranje, rode en gele onderliggende producten. Met de `Move low stock to top` , wordt de voorraad van de ouderproducten berekend door al zijn verkoopbare kindproducten voorraad te combineren en dienovereenkomstig te sorteren.

- **[!UICONTROL Add Condition]** - Voegt een andere voorwaarde aan de regel toe.

- **[!UICONTROL Attribute]** - Bepaalt het attribuut dat als basis van de voorwaarde wordt gebruikt. Opties:

  | Optie | Beschrijving |
  | ------ | ----------- |
  | `Clone Category ID(s)` | Producten dynamisch klonen, zonder sortering en volgorde, van meerdere categorieën op basis van categorie-id. |
  | `Color` | Omvat producten die op kleur worden gebaseerd. |
  | `Date Created (days ago)` | Omvat producten op basis van het aantal dagen sinds de producten aan de catalogus zijn toegevoegd. |
  | `Date Modified (days ago)` | Omvat producten op basis van het aantal dagen sinds de laatste wijziging van de producten. |
  | `Name` | Omvat producten op basis van de productnaam. |
  | `Price` | Omvat op prijs gebaseerde producten. Deze eigenschap is niet van toepassing op configureerbare producten omdat zij hun eigen prijs niet hebben. |
  | `Quantity` | Omvat producten op basis van de hoeveelheid in voorraad. |
  | `SKU` | Omvat op SKU gebaseerde producten. |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >De hoeveelheid van een configureerbaar product met kindopties wordt berekend door alle verkoopbare aantallen van het kindproduct te combineren. Overweeg een voorbeeld waar u een configureerbaar product hebt _Standaard fitnesstank_ met opties voor paarse, rode en gele kleur en verschillende hoeveelheden van beide. In dit geval is de hoeveelheid van het bovenliggende product (Basic Fitness Tank) de gecombineerde verkoopbare hoeveelheid van de onderliggende producten van paarse, rode en gele kleur.

- **[!UICONTROL Operator]** - Geeft de operator op die op de kenmerkwaarde wordt toegepast om aan de voorwaarde te voldoen. Tenzij een operator is opgegeven, `Equal` wordt gebruikt als standaard. Opties: `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to`, en `Contains`

- **[!UICONTROL Value]** - Geeft de waarde op die het kenmerk aan de voorwaarde moet voldoen.

- **[!UICONTROL Logic]** - De kolom Logica wordt gebruikt om meerdere voorwaarden te definiëren en wordt alleen weergegeven wanneer een andere voorwaarde wordt toegevoegd. De operatoren volgen de prioriteitsregels voor MySQL [booleaanse operatoren](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). Opties: `AND` / `OR`
