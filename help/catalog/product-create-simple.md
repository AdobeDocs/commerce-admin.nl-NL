---
title: Eenvoudig product
description: Leer hoe u een eenvoudig product maakt dat afzonderlijk of als onderdeel van een gegroepeerd, configureerbaar of gebundeld product kan worden verkocht.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Eenvoudig product

Een van de sleutels tot het benutten van de kracht van producttypen is het leren wanneer een eenvoudig, zelfstandig product moet worden gebruikt. Een eenvoudig product kan afzonderlijk of als deel van een gegroepeerd, configureerbaar, of bundelproduct worden verkocht. Een eenvoudig product met aangepaste opties wordt soms ook wel een _samengesteld product_.

De volgende instructies tonen het proces aan van het maken van een eenvoudig product met een [productsjabloon](attribute-sets.md), vereiste velden en basisinstellingen. Elk vereist veld is gemarkeerd met een rood sterretje (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

![Eenvoudig product](./assets/product-simple.png){width="700" zoomable="yes"}

## Stap 1: Kies het producttype

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Op de _[!UICONTROL Add Product]_( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ) in de rechterbovenhoek, kiest u **[!UICONTROL Simple Product]**.

   ![Eenvoudig product toevoegen](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Stap 2: Kies de kenmerkset

Als u de optie [kenmerkset](attribute-sets.md) die als template voor het product wordt gebruikt:

- Klik in het dialoogvenster **[!UICONTROL Attribute Set]** en voert u de volledige of gedeeltelijke naam van de kenmerkset in.

- Kies in de weergegeven lijst de kenmerkset die u wilt gebruiken.

Het formulier wordt bijgewerkt met de wijziging.

![Kenmerkset kiezen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Stap 3: Voer de vereiste instellingen in

1. Voer de **[!UICONTROL Product Name]**.

1. De standaardinstelling accepteren **[!UICONTROL SKU]** die is gebaseerd op de productnaam of een andere naam invoert.

1. Voer het product in **[!UICONTROL Price]**.

1. Stel de optie **[!UICONTROL Enable Product]** optie voor `No`.

1. klikken **[!UICONTROL Save]** en doorgaan.

   Wanneer het product wordt opgeslagen, wordt [Winkelweergave](introduction.md#product-scope) wordt in de linkerbovenhoek weergegeven.

1. Kies de optie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![De winkelweergave kiezen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Stap 4: De basisinstellingen voltooien

1. Set **[!UICONTROL Tax Class]** op een van de volgende wijzen:

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Voer de **[!UICONTROL Quantity]** van het product dat in voorraad is.

   Standaard, **[!UICONTROL Stock Status]** is ingesteld op `In Stock`.

   >[!NOTE]
   >
   >Als u [Inventory management](../inventory-management/introduction.md), wordt de hoeveelheid in deze sectie ingesteld door Single Source-handelaren. De multi-Bron handelaars voegen bronnen en hoeveelheden in de Bronsectie toe. Zie het volgende _Bronnen en hoeveelheden toewijzen (Inventory management)_ sectie.

1. Voer de **[!UICONTROL Weight]** van het product.

1. De standaardinstelling accepteren **[!UICONTROL Visibility]** instellen van `Catalog, Search`.

1. Om _[!UICONTROL Categories]_voor het product klikt u op de knop **[!UICONTROL Select…]**en voer een van de volgende handelingen uit:

   **Een bestaande categorie kiezen**:

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van elke categorie die u wilt toewijzen.

   **Een categorie maken**:

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** en kiest u **[!UICONTROL Parent Category]**, die de positie in de menustructuur bepaalt.

   - Klik op **[!UICONTROL Create Category]**.

1. Het product plaatsen in de lijst met [nieuwe producten](../content-design/widget-new-products-list.md), selecteert u de **[!UICONTROL Set Product as New]** selectievakje.

1. Kies de optie **[!UICONTROL Country of Manufacture]**.

Er kunnen aanvullende individuele kenmerken zijn die het product beschrijven. De selectie varieert per kenmerkset en u kunt deze later voltooien.

### Bronnen en hoeveelheden toewijzen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Stap 5: De productinformatie invullen

Schuif omlaag en voltooi indien nodig de informatie in de volgende secties:

- [Inhoud](product-content.md)
- [Afbeeldingen en video&#39;s](product-images-and-video.md)
- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)
- [Optimalisatie zoekmachine](product-search-engine-optimization.md)
- [Aanpasbare opties](settings-advanced-custom-options.md)
- [Producten op websites](settings-basic-websites.md)
- [Ontwerp](settings-advanced-design.md)
- [Cadeauopties](product-gift-options.md)

## Stap 6: Het product publiceren

1. Als u het product wilt publiceren in de catalogus, stelt u de optie **[!UICONTROL Enable Product]** schakelen naar `Yes`.

1. Voer een van de volgende handelingen uit:

   - **Methode 1:** Opslaan en voorvertonen

      - Klik in de rechterbovenhoek op **[!UICONTROL Save]**.

      - Kies **[!UICONTROL Customer View]** op de _Beheerder_ (![Menupijl](../assets/icon-menu-down-arrow-black.png)).

     De winkel wordt geopend in een nieuw browsertabblad.

     ![Klantenweergave](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Opslaan en sluiten

     Op de _[!UICONTROL Save]_ ( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ), kiest u **[!UICONTROL Save & Close]**.

## Te onthouden zaken

- Eenvoudige producten kunnen worden opgenomen in configureerbare, bundel- en gegroepeerde producttypen.

- De eenvoudige productconfiguratie treedt configureerbare productconfiguraties voor een specifiek product met voeten.

- Een eenvoudig product kan aangepaste opties hebben met verschillende typen invoer, waardoor het mogelijk is om veel productvariaties van één SKU te verkopen.
