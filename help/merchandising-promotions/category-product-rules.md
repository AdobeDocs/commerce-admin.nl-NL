---
title: Categorievoorschriften voor handelsdoeleinden
description: Leer hoe u regels maakt om de productselecties op dynamische wijze aan te passen aan een aantal voorwaarden.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# Categorievoorschriften voor handelsdoeleinden

{{ee-feature}}

Met Categorieregels wordt de productselectie dynamisch gewijzigd volgens een aantal voorwaarden. Elke categorie kan slechts één categorieregel hebben, hoewel de enige regel meerdere voorwaarden kan hebben. U kunt bijvoorbeeld een categorieregel maken voor een bepaald merk. Producten van hetzelfde merk worden automatisch aan de lijst toegevoegd, zelfs als ze niet aan dezelfde categorie zijn toegewezen. U kunt zoveel voorwaarden aan de expressie toevoegen als u nodig hebt om de producten te beschrijven die u wilt opnemen.

>[!TIP]
>
>Tijdens de opstelling van de categorieregel, worden de producten _gesorteerd,_ aangepast _,_ toegewezen _, en_ niet toegewezen _volgens die regel **_slechts_**&#x200B;wanneer deze categorie wordt bewaard._ Bijvoorbeeld, als u een product aan de catalogus toevoegt en het volgens de regel wilt toewijzen, moet u **elke categorie** opnieuw opslaan die wordt geplaatst om producten door regel aan te passen. Ook, als om het even welke status van de productvoorraad in `In Stock` of `Out of Stock` wordt veranderd en de producten in de categorie _zouden moeten worden gesorteerd_ volgens de **[!UICONTROL Automatic Sorting]** regel, moet u **[!UICONTROL Save Category]** klikken.

Elke voorwaarde bestaat uit een attribuut, waarde, en logische exploitant. In categorieregels kunnen alleen kenmerken worden gebruikt waarvoor de eigenschap _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_is ingesteld op `Yes` . U moet deze eigenschap instellen voor het kenmerk als u een kenmerk wilt gebruiken dat niet in productlijsten is opgenomen. Hoewel de attributen van de Datum niet worden gesteund, kunt u de Gemaakt Datum of Gewijzigde attributen gebruiken om een datum, of een waaier van data te bepalen. Als u bijvoorbeeld alleen producten wilt opnemen die in de afgelopen week zijn gemaakt, stelt u Aanmaakdatum in op de waarde `<7` .

>[!NOTE]
>
>Zorg ervoor om elk attribuut te vormen dat in de regel als a [_slimme_ attributen &#x200B;](smart-attributes-configure.md) wordt gebruikt.

![&#x200B; Regel van het Product van de Categorie &#x200B;](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

De productregels van de categorie kunnen het proces versnellen om specifieke producten aan categorieën toe te wijzen, die op voorwaarden worden gebaseerd die bepalen welke producten in de categorie verschijnen. De &quot;slimme&quot;attributen die met de regels van het categorieproduct kunnen worden gebruikt worden gespecificeerd in [&#x200B; Visuele Merchandiser &#x200B;](visual-merchandiser.md) configuratie.

>[!NOTE]
>
>Wees voorzichtig bij het toepassen van een regel voor een categorieproduct, omdat alle producten die niet aan de voorwaarde voldoen, uit de categorie worden verwijderd. Als u bijvoorbeeld een regel maakt die alleen paarse tankdoppen bevat, worden alle andere tanktoppen uit de categorie verwijderd.

## Stap 1: Vorm de _slimme_ attributen

1. Voor elk attribuut dat in de regel moet worden gebruikt, zorg ervoor dat het [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) storefront bezit aan `Yes` wordt geplaatst.

   >[!NOTE]
   >
   >Zorg ervoor dat het kenmerk dat u selecteert GEEN multiselect _[!UICONTROL Input Type]_&#x200B;is.

1. Voltooi de [&#x200B; configuratie &#x200B;](smart-attributes-configure.md) om elk _slimme_ attribuut te identificeren dat met Visuele Merchandiser moet worden gebruikt.

## Stap 2: De categorieregel maken

1. Open in de categoriestructuur de categorie die u wilt bewerken.

1. Stel **[!UICONTROL Match products by rule]** in op `Yes` in de sectie **[!UICONTROL Products in Category]** .

   De opties voor automatisch sorteren en voorwaarden worden weergegeven.

1. Klik op **[!UICONTROL Add Condition]**.

1. Kies de **[!UICONTROL Attribute]** die de basis van de voorwaarde is.

1. Stel **[!UICONTROL Operator]** in op een van de volgende opties:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Voer de **[!UICONTROL Value]** in die moet worden aangepast.

   ![&#x200B; voeg Voorwaarde aan de Regel van de Categorie toe &#x200B;](../catalog/assets/category-rule-create.png){width="500"}

1. Herhaal dit proces voor elk kenmerk dat nodig is om de voorwaarden te beschrijven waaraan moet worden voldaan.

   Bijvoorbeeld, om producten aan te passen die tussen zeven tot 30 dagen geleden werden gecreeerd, doe het volgende:

   - Stel **[!UICONTROL Date Created]** in op `Less than 30` .

   - Stel **[!UICONTROL Logic]** in op `AND` .

     >[!NOTE]
     >
     >Wanneer u `AND` kiest, is de regel van toepassing op producten waar aan alle voorwaarden wordt voldaan. Wanneer u `OR` kiest, is deze van toepassing op producten waaraan ten minste één voorwaarde is voldaan.

   - Stel **[!UICONTROL Date Modified]** in op `Greater than 7` .

1. Stel **[!UICONTROL Automatic Sorting]** in als u automatisch een sorteervolgorde wilt toepassen op de lijst met dynamisch gegenereerde producten.

   ![&#x200B; Automatisch Sorteren &#x200B;](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Sorteervolgordeopties worden globaal gedefinieerd en worden toegepast op basis van de huidige omstandigheden. U kunt geen andere sorteervolgorde instellen voor het weergaveniveau van de website, opslag of opslag.

   | Sorteren, optie | Beschrijving |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Sorteren op basis van voorraad, van boven of onder: `Move low stock to top` of `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Sorteren op prijs, van boven naar beneden: `Special price to top` of `Special price to bottom` |
   | [!UICONTROL New Products] | Nieuwste producten weergeven: `Newest products first` |
   | [!UICONTROL Color] | Alfabet sorteren op kleur: `Sort by color` |
   | [!UICONTROL Product Names] | Sorteren op naam in oplopende of aflopende volgorde: `Name A - Z` of `Name Z -A` |
   | [!UICONTROL SKU] | Sorteren op SKU in oplopende of aflopende volgorde: `SKU: Ascending` of `SKU: Descending` |
   | [!UICONTROL Price] | Sorteren op prijs in oplopende of aflopende volgorde: `Price: High to low` of `Price: Low to high` |

   {style="table-layout:auto"}

1. Klik op **[!UICONTROL Save Category]** als de bewerking is voltooid.

>[!NOTE]
>
>Wanneer u een categorieregel instelt, worden de producten bijgesneden en aan de regel toegewezen wanneer de categorie wordt opgeslagen. Als u een product aan de catalogus toevoegt en het in de regel wilt omvatten, moet u elke categorie opnieuw opslaan die wordt geplaatst om producten door regel aan te passen. Dit zorgt ervoor dat het nieuwe product wordt opgenomen.

### Menuopties

- **[!UICONTROL Match products by rule]** - Hiermee wordt bepaald of de lijst met producten in de categorie dynamisch wordt gegenereerd door een categorieregel. Opties: `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** - Hiermee wordt automatisch een sorteervolgorde toegepast op de lijst met categorieproducten. Opties: `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low` en `Price: Low to High`

  >[!NOTE]
  >
  >Als u een configureerbaar product met kindproducten hebt, wordt de voorraad van het ouderproduct berekend gebaseerd op het gecombineerde totaal van de voorraden van het kindproduct. Overweeg een voorbeeld waar u configureerbaar product _ProteusZitter van de Eiwitheid_ met oranje, rode, en gele kindproducten met verschillende voorraadhoeveelheden van elk hebt. De voorraad van het bovenliggende product wordt berekend op basis van het gecombineerde totaal van de voorraad van oranje, rode en gele onderliggende producten. Met de optie `Move low stock to top` wordt de voorraad van bovenliggende producten berekend door alle verkochte onderliggende producten te combineren en dienovereenkomstig te sorteren.

- **[!UICONTROL Add Condition]** - Voegt een andere voorwaarde aan de regel toe.

- **[!UICONTROL Attribute]** - Bepaalt het kenmerk dat wordt gebruikt als basis voor de voorwaarde. Opties:

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
  >De hoeveelheid van een configureerbaar product met kindopties wordt berekend door alle verkoopbare aantallen van het kindproduct te combineren. Overweeg een voorbeeld waar u een configureerbaar product _BasisSteek van de Fantasiteit_ met paarse, rode, en gele kleurenopties en verschillende hoeveelheden van elk hebt. In dit geval is de hoeveelheid van het bovenliggende product (Basic Fitness Tank) de gecombineerde verkoopbare hoeveelheid van de onderliggende producten van paarse, rode en gele kleur.

- **[!UICONTROL Operator]** - Geeft de operator op die wordt toegepast op de kenmerkwaarde om aan de voorwaarde te voldoen. Tenzij een operator is opgegeven, wordt `Equal` als de standaardwaarde gebruikt. Opties: `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to` en `Contains`

- **[!UICONTROL Value]** - Geeft de waarde op die het kenmerk aan de voorwaarde moet voldoen.

- **[!UICONTROL Logic]** - De kolom Logica wordt gebruikt om meerdere voorwaarden te definiëren en wordt alleen weergegeven wanneer een andere voorwaarde wordt toegevoegd. De exploitanten volgen de regels van belangrijkheid voor MySQL [&#x200B; booleaanse exploitanten &#x200B;](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). Opties: `AND` / `OR`
