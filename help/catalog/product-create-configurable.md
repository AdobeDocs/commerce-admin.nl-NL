---
title: Configureerbaar product
description: Leer hoe u een configureerbaar product maakt dat kopers verschillende mogelijkheden biedt voor selectie.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '2416'
ht-degree: 0%

---

# Configureerbaar product

Een configureerbaar product ziet er uit als één product met een vervolgkeuzelijst van elke variatie. Elk lijstitem is in feite een afzonderlijk eenvoudig product met een unieke SKU, waardoor het mogelijk is de inventaris voor elke productvariatie bij te houden. U kunt een vergelijkbaar effect bereiken door een eenvoudig product met aangepaste opties te gebruiken, maar zonder dat u de voorraad voor elke variatie kunt bijhouden.

De volgende instructies tonen het proces aan van het creëren van een configureerbaar product gebruikend een [productsjabloon](attribute-sets.md), vereiste velden en basisinstellingen. Elk vereist veld is gemarkeerd met een rood sterretje (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

![Configureerbaar product](./assets/product-configurable.png){width="700" zoomable="yes"}

## Deel 1: Een configureerbaar product maken

Hoewel een configureerbaar product meer SKU&#39;s gebruikt en aanvankelijk iets langer aan opstelling kan nemen, kan het u tijd in het eind besparen. Als u uw zaken wilt kweken, is het configureerbare producttype een goede keus voor producten met veelvoudige opties.

Voordat u begint, bereidt u een [kenmerkset](attribute-sets.md) dat een kenmerk bevat dat is ingesteld op een van de toegestane invoertypen voor elke productvariatie. De kenmerkenset kan bijvoorbeeld vervolgkeuzekenmerken voor kleur en grootte bevatten.

De eigenschappen van elk attribuut dat voor een configureerbare productvariatie wordt gebruikt moeten de volgende montages hebben:

### Eisen inzake kenmerken van productvariatie

| Eigenschap | Instelling |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Het invoertype van een kenmerk dat voor een productwijziging wordt gebruikt, moet een van de volgende zijn: `Dropdown`, `Visual Swatch`, of `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Stap 1: Kies het producttype

1. Op de _Beheerder_ zijbalk, ga naar  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Op de _[!UICONTROL Add Product]_( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ) in de rechterbovenhoek, kiest u **[!UICONTROL Configurable Product]**.

   ![Configureerbaar product toevoegen](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Stap 2: Kies de kenmerkset

De [kenmerkset](attribute-sets.md) Hiermee bepaalt u de selectie van de velden die in het product worden gebruikt. De kenmerkset die in het volgende voorbeeld wordt gebruikt, heeft kenmerken voor kleur en grootte. De naam van de kenmerkset wordt boven aan de pagina aangegeven en wordt aanvankelijk ingesteld op `Default`.

1. Als u de kenmerkset voor het product wilt kiezen, klikt u op het veld boven aan de pagina en voert u een van de volgende handelingen uit:

   - Voor **[!UICONTROL Search]**, voert u de naam in van de kenmerkset.
   - Kies in de lijst de kenmerkset die u wilt gebruiken.

   Het formulier wordt bijgewerkt met de wijziging.

1. Als u nog een kenmerk aan de kenmerkset wilt toevoegen, klikt u op **[!UICONTROL Add Attribute]** en volgt u de instructies in [Een kenmerk toevoegen](product-attributes-add.md).

   ![Sjabloon kiezen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Stap 3: Voer de vereiste instellingen in

1. Voer het product in **[!UICONTROL Product Name]**.

1. De standaardinstelling accepteren **[!UICONTROL SKU]** die is gebaseerd op de productnaam of een andere naam invoert.

1. Voer het product in **[!UICONTROL Price]**.

1. Aangezien het product nog niet gereed is om te publiceren, stelt u **[!UICONTROL Enable Product]** tot `No`.

1. klikken **[!UICONTROL Save]** en doorgaan.

   Wanneer het product wordt opgeslagen, wordt [Winkelweergave](introduction.md#product-scope) wordt in de linkerbovenhoek weergegeven.

1. Kies de optie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![De winkelweergave kiezen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Stap 4: De basisinstellingen voltooien

1. Set **[!UICONTROL Tax Class]** op een van de volgende wijzen:

   - `None`
   - `Taxable Goods`

1. De **[!UICONTROL Quantity]** wordt bepaald door de productvariaties, zodat u het leeg kunt laten.

1. Laat de **[!UICONTROL Stock Status]** zoals ingesteld.

   De voorraadstatus van een configureerbaar product wordt bepaald door elke bijbehorende configuratie. Omdat het product is opgeslagen zonder een hoeveelheid in te voeren, wordt het **[!UICONTROL Stock Status]** is ingesteld op `Out of Stock`.

   >[!NOTE]
   >
   >De **Status van voorraad** van het configureerbare product is een **_halfhandmatig_** gecontroleerde instelling. Het wordt gedeeltelijk gecontroleerd door de voorraadstatus van zijn kinderproducten. Het maakt deel uit van een **_meerdere criteria_** de berekening van de voorraadstatus, die wordt beschreven in de [De voorraadstatus configureren](#configure-the-stock-status) sectie.

1. Voer het product in **[!UICONTROL Weight]**.

>[!NOTE]
>
>Een configureerbaar product moet altijd een gewicht hebben. Als u **[!UICONTROL This item has no weight]** in de vervolgkeuzelijst automatisch gewijzigd in **[!UICONTROL This item has weight]** na het opslaan van het product.

1. De standaardinstelling accepteren **[!UICONTROL Visibility]** instellen van `Catalog, Search`.

1. Het product plaatsen in de lijst met [nieuwe producten](../content-design/widget-new-products-list.md), selecteert u de **[!UICONTROL Set Product as New]** selectievakje.

1. Als u Categorieën aan het product wilt toewijzen, klikt u op de knop **[!UICONTROL Select…]** en voer een van de volgende handelingen uit:

   **Een bestaande categorie kiezen**:

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van de categorie die u wilt toewijzen.

   ![Selecteer een of meer categorieën voor het bundelproduct](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Een categorie maken**:

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** en kiest u **[!UICONTROL Parent Category]**, die de positie in de menustructuur bepaalt.

   s- Klik **[!UICONTROL Create Category]**.

1. Kies de optie **[!UICONTROL Country of Manufacture]**.

   Er kunnen aanvullende kenmerken zijn die worden gebruikt om het product te beschrijven. De selectie varieert per kenmerkset en u kunt deze later voltooien.

### Stap 5: Opslaan en doorgaan

Het is nu een goed moment om uw werk op te slaan. Klik in de rechterbovenhoek op **[!UICONTROL Save]**. In de volgende reeks stappen, zult u opstelling de configuraties voor elke variatie van het product.

## Deel 2: Configuraties toevoegen

In het volgende voorbeeld ziet u hoe u configuraties voor drie kleuren en drie formaten toevoegt. In totaal worden negen eenvoudige producten gemaakt met unieke SKU&#39;s die elke mogelijke combinatie van variaties bestrijken. Standaard zijn de productnaam en SKU voor elke variatie gebaseerd op de kenmerkwaarde en de naam van het bovenliggende product of SKU.

De voortgangsbalk boven aan de pagina geeft aan waar u zich in het proces bevindt en begeleidt u bij elke stap.

### Stap 1: Kies de kenmerken

1. Ga van boven door en schuif omlaag naar de _[!UICONTROL Configurations]_sectie en klik op **[!UICONTROL Create Configurations]**.

   ![Configuraties](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Selecteer checkbox van elk attribuut dat u als configuratie wilt omvatten.

   In dit voorbeeld: `color` en `size` zijn geselecteerd.

   ![Kenmerken selecteren](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   De lijst omvat alle attributen van de kenmerkenreeks die in een configureerbaar product kunnen worden gebruikt.

1. Als u een attribuut wilt toevoegen, klik **[!UICONTROL Create New Attribute]** en voer de volgende handelingen uit:

   - Voltooi de eigenschappen van het kenmerk.

   - Klik op **[!UICONTROL Save Attribute]**.

   - Schakel het selectievakje voor het kenmerk in.

1. Klik in de rechterbovenhoek op **[!UICONTROL Next]**.

### Stap 2: Voer de kenmerkwaarden in

1. Selecteer voor elk kenmerk het selectievakje van de waarden die van toepassing zijn op het product.

   ![Kenmerkwaarden](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Als u de kenmerken opnieuw wilt rangschikken, neemt u de _Opnieuw_ ( ![Pictogram Sorteervolgorde](../assets/icon-sort-order.png) ) en verplaatst u de sectie naar een nieuwe positie.

   De volgorde bepaalt de positie van de vervolgkeuzelijsten op de productpagina.

1. Klik op de voortgangsbalk op **[!UICONTROL Next]**.

### Stap 3: Configureer de afbeeldingen, prijs en hoeveelheid

Deze stap bepaalt de beelden, de tarifering, en de hoeveelheid van elke configuratie. De beschikbare opties zijn voor elke optie gelijk en u kunt slechts één optie kiezen. U kunt het zelfde plaatsen op alle SKUs toepassen, een uniek plaatsen op elke SKU toepassen, of de montages voor nu overslaan.

Kies de configuratieopties die van toepassing zijn.

Gebruik één van de volgende methodes om te vormen **[!UICONTROL images]**:

**Methode 1:** Eén set afbeeldingen toepassen op alle SKU&#39;s

1. Selecteren **[!UICONTROL Apply single set of images to all SKUs]**.

1. Blader naar elke afbeelding die u in de productgalerie wilt opnemen of sleep deze naar het vak.

![Dezelfde afbeeldingen gebruiken voor alle SKU&#39;s](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Methode 2:** Unieke afbeeldingen toepassen voor elke SKU

Aangezien de afbeelding voor het bovenliggende product al is geüpload, kunt u met deze optie een afbeelding van elke kleur uploaden. U kunt een andere afbeelding toevoegen die in het winkelwagentje wordt weergegeven wanneer iemand het artikel in een bepaalde kleur koopt.

1. Selecteren **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Selecteer de **[!UICONTROL Attribute]** dat de afbeeldingen illustreren, zoals `color`.

1. Blader voor elke kenmerkwaarde naar de afbeeldingen die u voor die configuratie wilt gebruiken of sleep ze naar het vak.

   Als u de afbeelding naar een waardevak sleept, wordt deze ook weergegeven in de secties voor de andere waarden. Als u een afbeelding wilt verwijderen, klikt u op de knop _Prullenbak_ (![Prullenbakpictogram](../assets/icon-delete-trashcan-solid.png)).

   ![Unieke afbeeldingen per SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Gebruik één van de volgende methodes om te vormen **[!UICONTROL prices]**:

**Methode 1:** Dezelfde prijs toepassen op alle SKU&#39;s

1. Als de prijs voor alle variaties gelijk is, selecteert u **[!UICONTROL Apply single price to all SKUs]**.

1. Voer de **[!UICONTROL Price]**.

   ![Dezelfde prijs per SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Methode 2:** Een andere prijs toepassen voor elke SKU

1. Als de prijs voor elk product of voor bepaalde variaties verschilt, selecteert u **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Selecteer de **[!UICONTROL Attribute]** dat is de basis van het prijsverschil .

1. Voer de **[!UICONTROL Price]** voor elke kenmerkwaarde.

   In dit voorbeeld kost de XL-grootte meer.

   ![Unieke prijs per SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Gebruik één van de volgende methodes om te vormen **[!UICONTROL Quantity]**:

**Methode 1:** Dezelfde hoeveelheid toepassen op alle SKU&#39;s

Als de hoeveelheid voor alle SKU&#39;s gelijk is, selecteert u **[!UICONTROL Apply single quantity to each SKU]** en de hoeveelheid aangeven.

_Single Source-handelaren_ - Voer de **[!UICONTROL Quantity]**.

_Meerbronhandelaren die [Inventory management](../inventory-management/introduction.md)_ - Bronnen toewijzen en hoeveelheden toevoegen voor alle gegenereerde productvarianten:

1. Selecteer de **[!UICONTROL Apply single quantity to each SKU]** -optie.

1. Klik op **[!UICONTROL Assign Sources]**.

1. Blader naar of zoek naar een bron die u wilt toevoegen. Schakel het selectievakje in naast de bronnen die u voor het product wilt toevoegen.

1. Voer een hoeveelheid voorraad ter plaatse per bron in.

   ![Enkele hoeveelheid voor alle SKU&#39;s, bron toewijzen](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Methode 2:** Verschillende hoeveelheid per kenmerk toepassen

_Single Source-handelaren_ - Voer de **[!UICONTROL Quantity]**.

_Meerbronhandelaren die [Inventory management](../inventory-management/introduction.md)_ - Bronnen toewijzen en hoeveelheden toevoegen voor alle gegenereerde productvarianten:

1. Als de hoeveelheid voor elke SKU verschillend is, selecteert u **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Voer de **[!UICONTROL Quantity]** voor elk.

   ![Verschillende hoeveelheden per kenmerk](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Wanneer de configuratie voor afbeeldingen, prijs en hoeveelheid is voltooid, klikt u op **[!UICONTROL Next]** in de rechterbovenhoek.

### Stap 4: Produceer de productconfiguraties

Wacht tot de lijst met producten wordt weergegeven en voer een van de volgende handelingen uit:

- Als u tevreden bent met de configuraties, klikt u op **[!UICONTROL Generate Products]**.

- Klik op **[!UICONTROL Back]**.

![Overzicht bekijken voordat productwijzigingen worden gegenereerd](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

De huidige productvariaties staan onder aan het dialoogvenster _Configuratie_ sectie.

![Huidige configuraties](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Stap 5: productafbeeldingen toevoegen

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Images and Videos]_sectie.

1. Klik op de knop _Camera_ de tegel en doorbladeren aan het belangrijkste beeld dat u voor het configureerbare product wilt gebruiken.

Zie voor meer informatie [Afbeeldingen en video](product-images-and-video.md).

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

1. Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** tot `Yes` en voer een van de volgende handelingen uit:

   - **Methode 1:** Opslaan en voorvertonen

      - Klik in de rechterbovenhoek op **[!UICONTROL Save]**.

      - Kies **[!UICONTROL Customer View]** op de _Beheerder_ ( ![Menupijl](../assets/icon-menu-down-arrow-black.png) ).

     De winkel wordt geopend in een nieuw browsertabblad.

     ![Klantenweergave](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Opslaan en sluiten

     Op de _[!UICONTROL Save]_( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ), kiest u **[!UICONTROL Save & Close]**.

### Stap 8: De miniaturen van het winkelwagentje configureren

Als u voor elke variatie een andere afbeelding hebt, kunt u de configuratie zo instellen dat de juiste afbeelding wordt gebruikt voor de miniatuur van het winkelwagentje.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Checkout]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Shopping Cart]_sectie.

1. Set **[!UICONTROL Configurable Product Image]** tot `Product Thumbnail Itself`.

1. Klik op **[!UICONTROL Save Config]**.

   ![Winkelwagentje - configureerbare productafbeelding](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## De voorraadstatus configureren

De configureerbare status van de productvoorraad is anders dan de voorraadstatus van het eenvoudige product, waar het een directe weergave is van de beschikbaarheid van het product. Voor een configureerbaar product maakt de voorraadstatus deel uit van een **_meerdere criteria_** berekening van de voorraadstatus.

### Overzicht

De belangrijkste beginselen van de relaties met betrekking tot de status van de voorraden zijn:

- Wanneer u de **[!UICONTROL Stock Status]** van het configureerbare product als `Out of Stock` en klik op **[!UICONTROL Save]** is **_niet gecontroleerd_** door de voorraadstatus van haar kinderproducten. Deze wordt altijd weergegeven als `Out of Stock` in de Admin en op de Storefront.

- Wanneer u de **[!UICONTROL Stock Status]** van het configureerbare product als `In Stock` en klik op **[!UICONTROL Save]** is **_alleen gedeeltelijk gecontroleerd_** door de voorraadstatus van de onderliggende producten, die worden weergegeven in de Admin en op de Storefront.

### Gedetailleerde beschrijving

De _Status van voorraad_ van het configureerbare product gedeeltelijk wordt beheerst door de voorraadstatus van zijn onderliggende producten, en volgens het volgende **_meerdere criteria_** voorraadstatusberekeningen:

#### Alleen met standaardbron/voorraad:

- Als de configureerbare status van de productvoorraad **_handmatig_** instellen op `Out of Stock` door een Admin-gebruiker, bestandsimport of API-aanroep, blijft deze `Out of Stock` op beide **_Beheerder_** en **_Storefront_** totdat  **_handmatig_** gewijzigd in `In stock` door een Admin-gebruiker, bestandsimporteer of API-aanroep. Het kan niet worden gecontroleerd door de voorraadstatus van zijn kinderproducten.

- Als de configureerbare status van de productvoorraad **_handmatig_** instellen op `In Stock` door een Admin-gebruiker, bestandsimport of API-aanroep is de voorraadstatus **_automatisch_** onder de zeggenschap staan van de voorraadstatus van haar onderliggende producten op beide **_Beheerder_** en **_Storefront_**.

>[!NOTE]
>
>Aangepaste voorraden en bronnen maken deel uit van de [Inventory management](../inventory-management/sources-stocks.md) en u wordt ten zeerste aangeraden dit hulpmiddel uitsluitend te gebruiken voor het beheer van de voorraad en de bron. De standaardbron- en voorraadfuncties maken deel uit van de `CatalogInventory` , die nu afgekeurd is.

#### Met ten minste één aangepaste bron/voorraad:

- Als de configureerbare waarde voor de status van de productvoorraad **_handmatig_** instellen op `Out of Stock` door een Admin-gebruiker, bestandsimport of API-aanroep, blijft deze `Out of Stock` op beide **_Beheerder_** en **_Storefront_** totdat **_handmatig_** gewijzigd in `In Stock` door een Admin-gebruiker, bestandsimporteer of API-aanroep. IT **_kan_** worden gecontroleerd door de voorraadstatus van zijn kinderproducten.

- Als de configureerbare waarde voor de status van de productvoorraad **_handmatig_** instellen op `In Stock` door een Admin-gebruiker, bestandsimport of API-aanroep is de voorraadstatus **_automatisch_** die onder de zeggenschap staat van de voorraadstatus van haar onderliggende producten op de **_Storefront_** alleen.

- Als de configureerbare waarde voor de status van de productvoorraad **_handmatig_** instellen op `In Stock` door een Admin-gebruiker, bestandsimport of API-aanroep, blijft deze `In Stock` in de **_Beheerder_** totdat **_handmatig_** gewijzigd in `Out of Stock` door een Admin-gebruiker, bestandsimporteer of API-aanroep. IT **_kan_** worden gecontroleerd door de voorraadstatus van zijn kinderproducten.

## Te onthouden zaken

- Met een configureerbaar product kan de klant opties kiezen uit een keuzelijst, meerdere selecteren, visuele stalen en invoertypen voor tekststalen. Elke optie is een afzonderlijk, eenvoudig product.

- [Status van voorraad](../inventory-management/sources-stocks.md) voor een configureerbaar product is een semi-handbediende instelling. Het is anders dan de voorraadstatus van het eenvoudige product, waar het een directe weergave van de beschikbaarheid van het product is. Voor een configureerbaar product maakt de voorraadstatus deel uit van een voorraadstatusberekening met meerdere criteria.

- Configureerbare onderliggende producten kunnen eenvoudige of virtuele producten zijn **zonder aangepaste opties**. Als u aangepaste onderliggende producten virtueel wilt maken, moet u `Тhis item has no weight` voor de **[!UICONTROL Weight]** voor elk van hen.

- De attributen die voor productvariaties worden gebruikt moeten een globaal werkingsgebied hebben en de klant moet worden vereist om een waarde te kiezen. De attributen van de productvariatie moeten in de kenmerkenreeks worden omvat die als malplaatje voor het configureerbare product wordt gebruikt.

- De kenmerkenreeks die als malplaatje voor een configureerbaar product wordt gebruikt moet de attributen omvatten die de waarden bevatten die voor elke productvariatie nodig zijn.

- De miniatuurafbeelding in het winkelwagentje kan zo worden ingesteld dat de afbeelding wordt weergegeven op basis van de configureerbare productrecord of van de productvariatie.

- [Staalkenmerken](swatches.md#create-swatches-for-products) kan worden geconfigureerd om geen overeenkomende eenvoudige productafbeeldingen weer te geven wanneer het staal wordt geselecteerd door het instellen van de **[!UICONTROL Update Product Preview Image]** optiewaarde voor `No` op de pagina voor kenmerkbewerking in Admin.

- Het thema bepaalt hoe de afbeeldingengalerie zich gedraagt wanneer een gebruiker schakelt tussen productconfiguraties. Het standaardgedrag voor de _Leeg_ thema is de ouder configureerbare productbeelden met de geselecteerde productvariatie met voeten te treden. Voor het thema Luminantie is het standaardgedrag dat de geselecteerde afbeeldingen van productvariaties worden voorafgegaan aan de bovenliggende configureerbare productafbeeldingen.
