---
title: Configureerbaar product
description: Leer hoe u een configureerbaar product maakt dat kopers verschillende mogelijkheden biedt voor selectie.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 0cb594144a03eda985be3a86e45c93452281e9d5
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 0%

---

# Configureerbaar product

Een configureerbaar product ziet er uit als één product met een vervolgkeuzelijst van elke variatie. Elk lijstitem is in feite een afzonderlijk eenvoudig product met een unieke SKU, waardoor het mogelijk is de inventaris voor elke productvariatie bij te houden. U kunt een vergelijkbaar effect bereiken door een eenvoudig product met aangepaste opties te gebruiken, maar zonder dat u de voorraad voor elke variatie kunt bijhouden.

De volgende instructies tonen het proces aan om een configureerbaar product te creëren gebruikend a [ productmalplaatje ](attribute-sets.md), vereiste gebieden, en basismontages. Elk vereist gebied is duidelijk met een rode asterisk (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

![ Configureerbaar product ](./assets/product-configurable.png){width="700" zoomable="yes"}

## Deel 1: Een configureerbaar product maken

Hoewel een configureerbaar product meer SKU&#39;s gebruikt en aanvankelijk iets langer aan opstelling kan nemen, kan het u tijd in het eind besparen. Als u uw zaken wilt kweken, is het configureerbare producttype een goede keus voor producten met veelvoudige opties.

Alvorens u begint, bereidt een [ geplaatste attributen ](attribute-sets.md) voor die een attribuut omvat dat aan één van de toelaatbare inputtypes voor elke productvariatie wordt geplaatst. De kenmerkenset kan bijvoorbeeld vervolgkeuzekenmerken voor kleur en grootte bevatten.

De eigenschappen van elk attribuut dat voor een configureerbare productvariatie wordt gebruikt moeten de volgende montages hebben:

### Eisen inzake kenmerken van productvariatie

| Eigenschap | Instelling |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Het invoertype van een kenmerk dat wordt gebruikt voor een productvariatie, moet een van de volgende waarden zijn: `Dropdown`, `Visual Swatch` of `Text Swatch` . |
| [!UICONTROL Values Required] | `Yes` |
| [!UICONTROL Use for Promo Rule Conditions] | `Yes` |

{style="table-layout:auto"}

### Stap 1: Kies het producttype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Voor _[!UICONTROL Add Product]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu bij de hoger-juiste hoek, kies **[!UICONTROL Configurable Product]**.

   ![ voeg configureerbaar product ](./assets/product-add-configurable.png){width="700" zoomable="yes"} toe

### Stap 2: Kies de kenmerkset

De [ geplaatste attributen ](attribute-sets.md) bepaalt de selectie van gebieden die in het product worden gebruikt. De kenmerkset die in het volgende voorbeeld wordt gebruikt, heeft kenmerken voor kleur en grootte. De naam van de kenmerkset wordt boven aan de pagina aangegeven en wordt aanvankelijk ingesteld op `Default` .

1. Als u de kenmerkset voor het product wilt kiezen, klikt u op het veld boven aan de pagina en voert u een van de volgende handelingen uit:

   - Voer bij **[!UICONTROL Search]** de naam in van de kenmerkset.
   - Kies in de lijst de kenmerkset die u wilt gebruiken.

   Het formulier wordt bijgewerkt met de wijziging.

1. Als u een ander attribuut aan de kenmerkenreeks wilt toevoegen, klik **[!UICONTROL Add Attribute]** en volg de instructies in [ Toevoegend een Attribuut ](product-attributes-add.md).

   ![ kies malplaatje ](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Stap 3: Voer de vereiste instellingen in

1. Voer het product **[!UICONTROL Product Name]** in.

1. Accepteer de standaardwaarde **[!UICONTROL SKU]** die is gebaseerd op de productnaam of voer een andere naam in.

1. Voer het product **[!UICONTROL Price]** in.

1. Stel **[!UICONTROL Enable Product]** in op `No` omdat het product nog niet kan worden gepubliceerd.

1. Klik op **[!UICONTROL Save]** en ga verder.

   Wanneer het product wordt bewaard, verschijnt de [ verkiesster van de Mening van de Opslag ](introduction.md#product-scope) in de upper-left hoek.

1. Kies de locatie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![ kies de opslagmening ](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Stap 4: De basisinstellingen voltooien

1. Stel **[!UICONTROL Tax Class]** in op een van de volgende opties:

   - `None`
   - `Taxable Goods`

1. **[!UICONTROL Quantity]** wordt bepaald door de productvariaties, zodat u het leeg kunt laten.

1. Laat **[!UICONTROL Stock Status]** staan zoals ingesteld.

   De voorraadstatus van een configureerbaar product wordt bepaald door elke bijbehorende configuratie. Omdat het product is opgeslagen zonder een hoeveelheid in te voeren, is de waarde **[!UICONTROL Stock Status]** ingesteld op `Out of Stock` .

   >[!NOTE]
   >
   >De **Status van de Beeld** van het configureerbare product is a **_half-manueel_** gecontroleerd plaatsen. Het wordt gedeeltelijk gecontroleerd door de voorraadstatus van zijn kinderproducten. Het is een deel van de berekening van de a **_multi-criteria_** voorraadstatus, die in [ wordt beschreven vormt de 3&rbrace; sectie van de Status van de Voorraad &lbrace;.](#configure-the-stock-status)

1. Voer het product **[!UICONTROL Weight]** in.

>[!NOTE]
>
>Een configureerbaar product moet altijd een gewicht hebben. Als u **[!UICONTROL This item has no weight]** selecteert in de vervolgkeuzelijst, wordt deze automatisch gewijzigd in **[!UICONTROL This item has weight]** nadat u het product hebt opgeslagen.

1. Accepteer de standaardinstelling **[!UICONTROL Visibility]** van `Catalog, Search` .

1. Om het product in de lijst van [ nieuwe producten ](../content-design/widget-new-products-list.md) te voorzien, selecteer **[!UICONTROL Set Product as New]** checkbox.

1. Als u Categorieën aan het product wilt toewijzen, klikt u op het vak **[!UICONTROL Select…]** en voert u een van de volgende handelingen uit:

   **kies een bestaande categorie**:

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van de categorie die u wilt toewijzen.

   ![ selecteer één of meerdere categorieën voor het bundelproduct ](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **creeer een categorie**:

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** in en kies de **[!UICONTROL Parent Category]** die de positie in de menustructuur bepaalt.

   s- Klik op **[!UICONTROL Create Category]** .

1. Kies de **[!UICONTROL Country of Manufacture]** .

   Er kunnen aanvullende kenmerken zijn die worden gebruikt om het product te beschrijven. De selectie varieert per kenmerkset en u kunt deze later voltooien.

### Stap 5: Opslaan en doorgaan

Het is nu een goed moment om uw werk op te slaan. Klik in de rechterbovenhoek op **[!UICONTROL Save]** . In de volgende reeks stappen, zult u opstelling de configuraties voor elke variatie van het product.

## Deel 2: Configuraties toevoegen

In het volgende voorbeeld ziet u hoe u configuraties voor drie kleuren en drie formaten toevoegt. In totaal worden negen eenvoudige producten gemaakt met unieke SKU&#39;s die elke mogelijke combinatie van variaties bestrijken. Standaard zijn de productnaam en SKU voor elke variatie gebaseerd op de kenmerkwaarde en de naam van het bovenliggende product of SKU.

De voortgangsbalk boven aan de pagina geeft aan waar u zich in het proces bevindt en begeleidt u bij elke stap.

### Stap 1: Kies de kenmerken

1. Blader vanaf boven naar de sectie _[!UICONTROL Configurations]_&#x200B;en klik op **[!UICONTROL Create Configurations]**.

   ![ Configuraties ](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Selecteer checkbox van elk attribuut dat u als configuratie wilt omvatten.

   In dit voorbeeld zijn `color` en `size` geselecteerd.

   ![ Uitgezochte Attributen ](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   De lijst omvat alle attributen van de kenmerkenreeks die in een configureerbaar product kunnen worden gebruikt.

1. Als u een kenmerk wilt toevoegen, klikt u op **[!UICONTROL Create New Attribute]** en gaat u als volgt te werk:

   - Voltooi de eigenschappen van het kenmerk.

   - Klik op **[!UICONTROL Save Attribute]**.

   - Schakel het selectievakje voor het kenmerk in.

1. Klik in de rechterbovenhoek op **[!UICONTROL Next]** .

### Stap 2: Voer de kenmerkwaarden in

1. Selecteer voor elk kenmerk het selectievakje van de waarden die van toepassing zijn op het product.

   ![ waarden van Attributen ](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Om de attributen opnieuw te rangschikken, greep _opnieuw rangschikt_ ( ![ het pictogram van de Orde van de Sortering ](../assets/icon-sort-order.png) ) en beweeg de sectie naar een nieuwe positie.

   De volgorde bepaalt de positie van de vervolgkeuzelijsten op de productpagina.

1. Klik op **[!UICONTROL Next]** in de voortgangsbalk.

### Stap 3: Configureer de afbeeldingen, prijs en hoeveelheid

Deze stap bepaalt de beelden, de tarifering, en de hoeveelheid van elke configuratie. De beschikbare opties zijn voor elke optie gelijk en u kunt slechts één optie kiezen. U kunt het zelfde plaatsen op alle SKUs toepassen, een uniek plaatsen op elke SKU toepassen, of de montages voor nu overslaan.

Kies de configuratieopties die van toepassing zijn.

Gebruik een van de volgende methoden om de **[!UICONTROL images]** te configureren:

**Methode 1:** pas één enkele reeks beelden op alle SKUs toe

1. Selecteer **[!UICONTROL Apply single set of images to all SKUs]** .

1. Blader naar elke afbeelding die u in de productgalerie wilt opnemen of sleep deze naar het vak.

![ Gebruik zelfde beelden voor alle SKUs ](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Methode 2:** pas unieke beelden voor elke SKU toe

Aangezien de afbeelding voor het bovenliggende product al is geüpload, kunt u met deze optie een afbeelding van elke kleur uploaden. U kunt een andere afbeelding toevoegen die in het winkelwagentje wordt weergegeven wanneer iemand het artikel in een bepaalde kleur koopt.

1. Selecteer **[!UICONTROL Apply unique images by attribute to each SKU]** .

1. Selecteer de **[!UICONTROL Attribute]** die de afbeeldingen illustreren, zoals `color` .

1. Blader voor elke kenmerkwaarde naar de afbeeldingen die u voor die configuratie wilt gebruiken of sleep ze naar het vak.

   Als u de afbeelding naar een waardevak sleept, wordt deze ook weergegeven in de secties voor de andere waarden. Als u een beeld wilt schrappen, klik het _Prullenbak_ (![ pictogram van het Afval ](../assets/icon-delete-trashcan-solid.png)) pictogram.

   ![ Unieke beelden per SKU ](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Gebruik een van de volgende methoden om de **[!UICONTROL prices]** te configureren:

>[!NOTE]
>
>Een configureerbaar product heeft geen eigen prijs in de catalogus. De configureerbare productprijs wordt afgeleid van de onderliggende [!UICONTROL In Stock] producten.

**Methode 1:** pas de zelfde prijs op alle SKUs toe

1. Als de prijs voor alle variaties gelijk is, selecteert u **[!UICONTROL Apply single price to all SKUs]** .

1. Voer de **[!UICONTROL Price]** in.

   ![ Zelfde prijs per SKU ](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Methode 2:** pas een verschillende prijs voor elke SKU toe

1. Selecteer **[!UICONTROL Apply unique prices by attribute to each SKU]** als de prijs voor elk product of voor bepaalde variaties verschilt.

1. Selecteer **[!UICONTROL Attribute]** die de basis van het prijsverschil is.

1. Voer de **[!UICONTROL Price]** in voor elke kenmerkwaarde.

   In dit voorbeeld kost de XL-grootte meer.

   ![ Unieke prijs per SKU ](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Gebruik een van de volgende methoden om de **[!UICONTROL Quantity]** te configureren:

**Methode 1:** pas het zelfde aantal op alle SKUs toe

Als de hoeveelheid voor alle SKU&#39;s gelijk is, selecteert u **[!UICONTROL Apply single quantity to each SKU]** en geeft u de hoeveelheid op.

_Enige bronverkopers_ - ga **[!UICONTROL Quantity]** in.

_MultiSource handelaars die [ Inventory management](../inventory-management/introduction.md)_ gebruiken - wijs bronnen toe en voeg hoeveelheden voor alle geproduceerde productvarianten toe:

1. Selecteer de optie **[!UICONTROL Apply single quantity to each SKU]** .

1. Klik op **[!UICONTROL Assign Sources]** om een bron toe te voegen.

1. Blader naar of zoek naar een bron die u wilt toevoegen. Schakel het selectievakje in naast de bronnen die u voor het product wilt toevoegen.

1. Voer een hoeveelheid voorraad ter plaatse per bron in.

   ![ Enige Aantal voor Alle SKUs, wijs bron ](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"} toe

**Methode 2:** pas verschillende hoeveelheid door attribuut toe

_Enige bronverkopers_ - ga **[!UICONTROL Quantity]** in.

_MultiSource handelaars die [ Inventory management](../inventory-management/introduction.md)_ gebruiken - wijs bronnen toe en voeg hoeveelheden voor alle geproduceerde productvarianten toe:

1. Selecteer **[!UICONTROL Apply unique quantity by attribute to each SKU]** als het aantal voor elke SKU anders is.

1. Voer de waarde **[!UICONTROL Quantity]** voor elke waarde in.

   ![ Verschillende hoeveelheden per attribuut ](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Wanneer de configuratie voor afbeeldingen, prijs en aantal is voltooid, klikt u op **[!UICONTROL Next]** in de rechterbovenhoek.

### Stap 4: Produceer de productconfiguraties

Wacht tot de lijst met producten wordt weergegeven en voer een van de volgende handelingen uit:

- Klik op **[!UICONTROL Generate Products]** als u tevreden bent met de configuraties.

- Klik op **[!UICONTROL Back]** om correcties aan te brengen.

![ samenvatting van het Overzicht alvorens productvariaties ](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"} te produceren

De huidige productvariaties verschijnen bij de bodem van de _sectie van de Configuratie_.

![ Huidige Configuraties ](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Stap 5: productafbeeldingen toevoegen

1. De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de _[!UICONTROL Images and Videos]_&#x200B;sectie.

1. Klik de _tegel van de Camera_ en doorblader aan het belangrijkste beeld dat u voor het configureerbare product wilt gebruiken.

Voor meer informatie, zie [ Beelden en Video ](product-images-and-video.md).

### Stap 6: De productinformatie invullen

Schuif omlaag en voltooi indien nodig de informatie in de volgende secties:

- [Inhoud](product-content.md)

- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)

- [Optimalisatie zoekmachine](product-search-engine-optimization.md)

- [Aanpasbare opties](settings-advanced-custom-options.md)

- [Producten op websites](settings-basic-websites.md)

- [Ontwerp](settings-advanced-design.md)

- [Cadeauopties](product-gift-options.md)

### Stap 7: Het product publiceren

1. Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** in op `Yes` en voert u een van de volgende handelingen uit:

   - **Methode 1:** sparen en voorproef

      - Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

      - Om het product in uw opslag te bekijken, verkies **[!UICONTROL Customer View]** op _Admin_ ( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-black.png)) menu.

     De winkel wordt geopend in een nieuw browsertabblad.

     ![ Mening van de Klant ](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** sparen en sluit

     Voor _[!UICONTROL Save]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu, kies **[!UICONTROL Save & Close]**.

### Stap 8: De miniaturen van het winkelwagentje configureren

Als u voor elke variatie een andere afbeelding hebt, kunt u de configuratie zo instellen dat de juiste afbeelding wordt gebruikt voor de miniatuur van het winkelwagentje.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de _[!UICONTROL Shopping Cart]_&#x200B;sectie uit.

1. Stel **[!UICONTROL Configurable Product Image]** in op `Product Thumbnail Itself` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

   ![ het Schepen kart - configureerbaar productbeeld ](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## De voorraadstatus configureren

De configureerbare status van de productvoorraad is anders dan de voorraadstatus van het eenvoudige product, waar het een directe weergave is van de beschikbaarheid van het product. Voor een configureerbaar product, is de voorraadstatus een deel van a **_multi-criteria_** de berekening van de voorraadstatus.

### Overzicht

De belangrijkste beginselen van de relaties met betrekking tot de status van de voorraden zijn:

- Wanneer u **[!UICONTROL Stock Status]** van het configureerbare product als `Out of Stock` verandert en **[!UICONTROL Save]** klikt, wordt het **_niet gecontroleerd_** door de voorraadstatussen van zijn kindproducten. Deze wordt altijd als `Out of Stock` weergegeven in de beheerdersinterface en in de winkelruimte.

- Wanneer u **[!UICONTROL Stock Status]** van het configureerbare product als `In Stock` plaatst en **[!UICONTROL Save]** klikt, wordt het **_slechts gedeeltelijk gecontroleerd_** door de voorraadstatussen van zijn kindproducten, die in Admin en op Storefront worden weerspiegeld.

### Gedetailleerde beschrijving

De _Status van de Voorraad_ van het configureerbare product wordt gedeeltelijk gecontroleerd door de Status van de Voorraad van zijn kindproducten, en volgens de volgende **_multi-criteria_** berekeningen van de voorraadstatus:

#### Alleen met standaardbron/voorraad:

- Als de configureerbare Status van de productvoorraad **_manueel_** wordt geplaatst aan `Out of Stock` door een Admin gebruiker, dossierinvoer, of API vraag, blijft het als `Out of Stock` op zowel **_Admin_** en **_Storefront_** tot het **_manueel_** wordt veranderd in `In stock` door een gebruiker Admin, dossierinvoer, of API vraag. Het kan niet worden gecontroleerd door de voorraadstatus van zijn kinderproducten.

- Als de configureerbare Status van het productdossier **_manueel_** wordt geplaatst aan `In Stock` door een Admin gebruiker, dossier de invoer, of API vraag, is zijn voorraadstatus **__** automatisch gecontroleerd door de voorraadstatus van zijn kindproducten op zowel **_Admin_** en **_Storefront_**.

>[!NOTE]
>
>De aandelen en de bronnen van de douane maken deel uit van de [ Inventory management ](../inventory-management/sources-stocks.md) uitbreiding en het wordt hoogst geadviseerd dat u dit hulpmiddel uitsluitend voor het beheren van voorraad en bron gebruikt. De standaardbron- en voorraadfuncties maken deel uit van de module `CatalogInventory` , die nu is afgekeurd.

#### Met ten minste één aangepaste bron/voorraad:

- Als de configureerbare waarde van de Status van de productvoorraad **_manueel_** wordt geplaatst aan `Out of Stock` door een Admin gebruiker, dossierinvoer, of API vraag, blijft het als `Out of Stock` op zowel **_Admin_** en **_Storefront_** tot het **_manueel_** wordt veranderd in `In Stock` door een gebruiker Admin, dossierinvoer, of API vraag. Het **_kan_** niet door de voorraadstatus van zijn kindproducten worden gecontroleerd.

- Als de configureerbare waarde van de Status van de productvoorraad **_manueel_** wordt geplaatst aan `In Stock` door een Admin gebruiker, dossierinvoer, of API vraag, is zijn voorraadstatus **__** automatisch gecontroleerd door de voorraadstatus van zijn kindproducten op **_Storefront_** slechts.

- Als de configureerbare waarde van de Status van de productvoorraad **_manueel_** wordt geplaatst aan `In Stock` door een Admin gebruiker, dossierinvoer, of API vraag, blijft het als `In Stock` in **_Admin_** tot het **_manueel_** wordt veranderd in `Out of Stock` door een Admin gebruiker, dossierinvoer, of API vraag. Het **_kan_** niet door de voorraadstatus van zijn kindproducten worden gecontroleerd.

## Te onthouden zaken

- Met een configureerbaar product kan de klant opties kiezen uit een keuzelijst, meerdere selecteren, visuele stalen en invoertypen voor tekststalen. Elke optie is een afzonderlijk, eenvoudig product.

- [ Status van de Voorraad ](../inventory-management/sources-stocks.md) voor een configureerbaar product is een semi-manueel gecontroleerd plaatsen. Het is anders dan de voorraadstatus van het eenvoudige product, waar het een directe weergave van de beschikbaarheid van het product is. Voor een configureerbaar product maakt de voorraadstatus deel uit van een voorraadstatusberekening met meerdere criteria.

- De configureerbare kindproducten kunnen eenvoudige of virtuele producten **zonder douaneopties** zijn. Als u aangepaste onderliggende producten virtueel wilt maken, moet u voor elk product de instelling **[!UICONTROL Weight]** `Тhis item has no weight` selecteren.

- Alle kindproducten worden toegewezen en unassigned van het configureerbare product **_globaal_** voor alle websites, opslag, en opslagmeningen tezelfdertijd.

- Een configureerbaar product heeft geen eigen prijs in de catalogus. De configureerbare productprijs wordt afgeleid van de onderliggende [!UICONTROL In Stock] producten.

- De attributen die voor productvariaties worden gebruikt moeten een globaal werkingsgebied hebben en de klant moet worden vereist om een waarde te kiezen. De attributen van de productvariatie moeten in de kenmerkenreeks worden omvat die als malplaatje voor het configureerbare product wordt gebruikt.

- De kenmerkenreeks die als malplaatje voor een configureerbaar product wordt gebruikt moet de attributen omvatten die de waarden bevatten die voor elke productvariatie nodig zijn.

- De miniatuurafbeelding in het winkelwagentje kan zo worden ingesteld dat de afbeelding wordt weergegeven op basis van de configureerbare productrecord of van de productvariatie.

- [ de attributen van het Monster ](swatches.md#create-swatches-for-products) kunnen worden gevormd om overeenkomstige eenvoudige productbeelden niet te tonen wanneer het monster door de **[!UICONTROL Update Product Preview Image]** optiewaarde aan `No` bij de attributen te plaatsen uitgeeft pagina in Admin wordt geselecteerd.

- Het thema bepaalt hoe de afbeeldingengalerie zich gedraagt wanneer een gebruiker schakelt tussen productconfiguraties. Het standaardgedrag voor het _Lege_ thema moet de ouder configureerbare productbeelden met de geselecteerde productvariatie met voeten treden. Voor het thema Luminantie is het standaardgedrag dat de geselecteerde afbeeldingen van productvariaties worden voorafgegaan aan de bovenliggende configureerbare productafbeeldingen.
