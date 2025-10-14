---
title: Prijsbepaling en structuur van gedeelde catalogus instellen
description: In Adobe Commerce B2B leert u meer over het instellen van de prijs en de structuur van een gedeelde catalogus.
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# Prijsbepaling en structuur van gedeelde catalogus instellen

Het instellen van de prijs en de structuur van een gedeelde catalogus bestaat uit twee stappen. De huidige plaats in het proces wordt gemarkeerd met een getal in de voortgangsbalk boven aan de pagina. U kunt de andere stap in het proces op elk gewenst moment weergeven door op de voortgangsbalk te klikken. Als u bijvoorbeeld werkt aan aangepaste prijzen, kunt u ter referentie terugkeren naar de pagina met productselectie. Klik gewoon op **[!UICONTROL Products]** in de voortgangsbalk boven aan de pagina en klik vervolgens op **[!UICONTROL Pricing]** om terug te keren naar de aangepaste prijspagina. Uw werk gaat hierbij niet verloren.

![&#x200B; Producten in Catalogus &#x200B;](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

In de standaardcategorieboom, is de wortelcategorie de hoogste container en wordt bedoeld als _StandaardCategorie_ in de steekproefgegevens. Nochtans, wanneer de gedeelde catalogi worden toegelaten, heeft de categorieboom een buitencontainer genoemd _Catalogus van de Wortel_. De basiscatalogus omvat alle andere categoriefstructuren die in het systeem bestaan. Voor meer informatie, zie [&#x200B; Reikwijdte van de Catalogus &#x200B;](../catalog/introduction.md#catalog-scope).

## Stap 1: Open de gedeelde catalogusprijs en structuurconfiguratie

1. Op _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. Ga voor de gedeelde catalogus in het raster naar de kolom _[!UICONTROL Action]_&#x200B;en klik op **[!UICONTROL Set Pricing and Structure]**.

   ![&#x200B; Vastgestelde tarifering en structuur voor gedeelde catalogus &#x200B;](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. De eerste keer dat de gedeelde catalogus wordt geconfigureerd, klikt u op **[!UICONTROL Configure]** om door te gaan met de volgende stappen.

## Stap 2: Kies de producten

De eerste stap in het proces is de producten te kiezen die u in de gedeelde catalogus wilt omvatten. De pagina van de productselectie kenmerkt de [&#x200B; categorieboom &#x200B;](../catalog/category-create.md) op de linkerzijde, en een gesynchroniseerd productnet op het recht. Als u op een categorie in de boomstructuur klikt, worden de producten in de categorie in het raster weergegeven.

Slechts verschijnen de categorieën met geselecteerde producten in de [&#x200B; hoogste navigatie &#x200B;](../catalog/navigation-top.md) wanneer de gedeelde catalogus van de storefront wordt bekeken. Standaard worden alleen de eerste drie categorieniveaus opgenomen in de storefront-navigatie, exclusief de hoofdcategorie.

1. Gebruik de **verkiesster van de Opslag** om het [&#x200B; werkingsgebied &#x200B;](../catalog/introduction.md#product-scope) van de configuratie te plaatsen.

   Het bereik van de configuratie kan alleen worden ingesteld voordat de gedeelde catalogus voor het eerst wordt opgeslagen. Als u de productselectie later bewerkt, is de winkelkiezer niet beschikbaar.

   ![&#x200B; kies Opslag &#x200B;](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. Voer in de categoriestructuur een van de volgende handelingen uit:

   - Als u alle producten wilt opnemen, klikt u op **[!UICONTROL Select all]** of selecteert u het selectievakje van de bovenliggende categorie.
   - Als u bepaalde productcategorieën wilt opnemen, schakelt u het selectievakje in van elke categorie die u wilt opnemen.
   - Als u een afzonderlijk product wilt opnemen of uitsluiten, schakelt u het selectievakje van het product in of uit.

   De notatie onder elke categorie in de structuur geeft het aantal producten van de categorie weer dat momenteel is opgenomen in de gedeelde catalogus. De aantekening onder de [&#x200B; wortelcategorie &#x200B;](../catalog/category-root.md) toont het totale aantal producten van alle categorieën die momenteel voor de gedeelde catalogus worden geselecteerd.

1. Als u categorieproducten in het raster wilt weergeven, klikt u op de naam van de categorie in de boomstructuur. Wanneer een categorie wordt geselecteerd, komt het volgende voor:

   - De knevel in de eerste kolom van het net wordt geplaatst aan groene __ positie voor elk geselecteerd product.
   - Als een product aan veelvoudige categorieën wordt toegewezen en niet in één van hen wordt geselecteerd, blijft het beschikbaar door de andere categorieën, en ook wanneer het gebruiken van [&#x200B; catalogusonderzoek &#x200B;](../catalog/search.md).
   - Het systeem plaatst automatisch [&#x200B; Toestemmingen van de Categorie &#x200B;](../catalog/category-permissions.md) aan `Allow` voor de geselecteerde producten.

1. Gebruik indien nodig de filters en andere rasterbesturingselementen om de producten te zoeken die u wilt opnemen in de gedeelde catalogus.

   U kunt afzonderlijke producten afzonderlijk selecteren of weglaten door op de schakeloptie in de eerste kolom te klikken.

   Als u een categorie selecteert die geen producten heeft, maar die is gekoppeld aan CMS-inhoud of een externe koppeling, wordt deze weergegeven in de bovenste navigatie in de winkel.

   De categoriemontages die u maakt worden niet permanent geregistreerd in het gegevensbestand tot de configuratie wordt bewaard. Ze worden echter tijdelijk opgeslagen terwijl u werkt aan de structuur en de prijs.

1. Klik op **[!UICONTROL Next]**.

   ![&#x200B; Uitgezochte Producten voor Catalogus &#x200B;](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Stap 3: Aangepaste prijzen instellen

U kunt aangepaste prijzen voor elk product afzonderlijk instellen of de _[!UICONTROL Action]_-controle gebruiken om aangepaste prijzen in te stellen als een vast bedrag of percentage voor meerdere productrecords.

- **[!UICONTROL Fixed]** - Geeft de uiteindelijke productprijs op. Als u bijvoorbeeld een vaste prijs van € 10,00 invoert, is de prijs in de winkel voor het desbetreffende bedrijf $10,00.

  >[!NOTE]
  >
  >De minimumwaarde tussen de basisprijs en de ingevoerde vaste waarde wordt gebruikt als de uiteindelijke productprijs.

  >[!NOTE]
  >
  >_&#x200B;**product Aanpasbare Opties van de Prijs van de Vaste Prijs**&#x200B;_ &lbrace;worden _niet_ beïnvloed door de Prijs van de Groep, de Prijs van de Rij, de Speciale Prijs, of de regels van de Prijs van de Catalogus.

- **[!UICONTROL Percentage]**: hiermee wordt de aangepaste prijs bepaald op basis van het kortingspercentage. Als u bijvoorbeeld een korting van 10 procent wilt aanbieden, stelt u het aangepaste prijstype in op `Percentage` en voert u `10` in. De verdisconteerde aangepaste prijs is 90 procent van de oorspronkelijke productprijs.

Als u de korting wilt instellen op een vast bedrag of een percentage voor de volgende producttypen, gebruikt u de kolom _[!UICONTROL Custom Price]_&#x200B;in het raster:

- [&#x200B; Eenvoudig &#x200B;](../catalog/product-create-simple.md) (met inbegrip van configureerbare productvariaties)
- [Bundel](../catalog/product-create-bundle.md)
- [Downloadbaar](../catalog/product-create-downloadable.md)
- [Virtueel](../catalog/product-create-virtual.md)

De kolom van de Prijs van de Douane is leeg voor [&#x200B; configureerbare &#x200B;](../catalog/product-create-configurable.md) en [&#x200B; gegroepeerde &#x200B;](../catalog/product-create-grouped.md) producttypes en voor [&#x200B; giftekaarten &#x200B;](../catalog/product-gift-card-create.md).

De selectie van producten in het net kan niet van de _pagina van de Prijzen van de Douane worden veranderd_. U kunt echter de voortgangsindicator boven aan de pagina gebruiken om terug te keren naar de vorige stap en de selectie van producten te wijzigen.

![&#x200B; Uitgezochte Producten voor Catalogus &#x200B;](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### Een aangepaste prijs toepassen

1. Voor een installatie op meerdere sites stelt u **[!UICONTROL Website]** in op de website waarop de aangepaste prijzen van toepassing zijn.

   ![&#x200B; kies Website &#x200B;](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Gebruik een van de volgende methoden om de producten te selecteren waarop de aangepaste prijs van toepassing is.

   - Gebruik de categoriestructuur om alle producten in een specifieke categorie te selecteren.
   - Stel het besturingselement _[!UICONTROL Mass Actions]_&#x200B;in de koptekst in op `Select All` .
   - Schakel het selectievakje voor afzonderlijke producten in.

   In het raster worden de producten in de momenteel geselecteerde categorieën weergegeven en u kunt de standaardbesturingselementen gebruiken om producten te zoeken en de lijst te filteren.

   ![&#x200B; Uitgezocht allen &#x200B;](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Actions]** in op een van de volgende opties:

   - `Set Discount` - Hiermee past u een kortingspercentage toe op alle geselecteerde producten. Elke beïnvloede productprijs wordt getoond als a **_verdisconteerde_** prijs.
   - `Adjust Fixed Price` - Hiermee past u een korting op de vaste prijs toe op alle geselecteerde producten. Elke beïnvloede productprijs wordt getoond als **_aangepaste vaste_** prijs.

   ![&#x200B; Controle van Acties - de Reeks Korting &#x200B;](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. Voer desgevraagd de korting of de prijsaanpassing in en klik op **[!UICONTROL Apply]** .

   ![&#x200B; plaats Korting &#x200B;](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![&#x200B; Adjust Vaste Prijs &#x200B;](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   De korting wordt toegepast op alle geselecteerde producten, en de _kolom van de Prijs van de Douane_ wijst op het type van toegepaste korting en bedrag.

   ![&#x200B; Kolom van de Aangepaste Prijs met Korting &#x200B;](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### Laagprijs toepassen

[&#x200B; de tarifering van de Rij &#x200B;](../catalog/product-price-tier.md) laat u een kwantitatieve korting voor producten in de gedeelde catalogus aanbieden. De _kolom van de Prijs van de Rij_ van het net bevat een verbinding aan _Geavanceerde het Prijsmaken_ opties die specifiek op de gedeelde catalogus van toepassing zijn. Als het product reeds rijtarifering omvat, verschijnt het aantal bestaande rijen tussen haakjes na de verbinding.

De volgende instructies laten zien hoe u de prijzen op lagen kunt toepassen op één product. Om rij het tarief op veelvoudige producten toe te passen, verwijs naar [&#x200B; de laagprijzen van de Invoer &#x200B;](../systems/data-import-price-tier.md).

1. Voor het product in het net, ga naar de _kolom van de Prijs van de Rij_ en klik **[!UICONTROL Configure]**.

   ![&#x200B; vorm de Prijs van de Rij &#x200B;](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. Voor de _Geavanceerde Prijsverhoging_ pagina, klik **[!UICONTROL Add Price]** en doe het volgende:

   ![&#x200B; Catalogus en de Prijs van de Rij &#x200B;](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Website]** in op de website waarop de laagprijs van toepassing is.
   - Voer de hoeveelheid product in die u moet kopen om de korting te ontvangen.
   - Stel **[!UICONTROL Price]** in op een van de volgende kortingstypen:
      - `Fixed`
      - `Discount`
   - Voer het bedrag van de korting in.
   - Om een andere rij in te gaan, klik **Add Prijs** en herhaal het proces om de volgende rij te bepalen.

   ![&#x200B; Veelvoudige Prijzen van de Rij &#x200B;](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Done]** als de bewerking is voltooid.

   In het raster wordt het aantal lagen tussen haakjes weergegeven in de kolom _[!UICONTROL Tier Price]_.

   ![&#x200B; Veelvoudige Lagen &#x200B;](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## Structuur en prijzen opslaan

Wanneer de aangepaste prijs is voltooid, klikt u op **[!UICONTROL Generate Catalog]** en **[!UICONTROL Save]** .

De gedeelde catalogus wordt nu opgeslagen in de database. De naam ervan wordt weergegeven in de kolom _[!UICONTROL Shared Catalog]_&#x200B;van het&#x200B;_[!UICONTROL Products]_ -raster. De volgende stap moet [&#x200B; de gedeelde catalogus aan een bedrijf &#x200B;](./catalog-shared-assign-companies.md) toewijzen.
