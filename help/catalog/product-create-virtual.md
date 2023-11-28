---
title: Virtueel product
description: Leer hoe u een virtueel product maakt dat een niet-tastbaar item vertegenwoordigt, zoals een lidmaatschap, service, garantie of abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Virtueel product

Virtuele producten, of digitale goederen, vertegenwoordigen niet-tastbare zaken zoals lidmaatschappen, de diensten, de garanties, of abonnementen, en digitale downloads van boeken, muziek, video&#39;s, of andere producten. Virtuele producten kunnen afzonderlijk worden verkocht of als onderdeel van de [Gegroepeerd product](product-create-grouped.md), [Configureerbaar product](product-create-configurable.md), of [Bundel](product-create-bundle.md) productsoorten.

Afgezien van het ontbreken van _[!UICONTROL Weight]_in het veld is het proces voor het maken van een virtueel product en een eenvoudig product hetzelfde. De volgende instructies tonen het proces aan van het maken van een virtueel product met een [productsjabloon](attribute-sets.md), vereiste velden en basisinstellingen. Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

>[!NOTE]
>
>PayPal heeft de ondersteuning voor de verkoop van digitale goederen vervangen via PayPal Express Checkout. Ze raden u aan een van beide te gebruiken [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) of een andere PayPal-betaalgateway om bestellingen te verwerken die virtuele producten bevatten.

![Virtueel product](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Stap 1: Kies het producttype

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Op de _[!UICONTROL Add Product]_( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ) in de rechterbovenhoek, kiest u **[!UICONTROL Virtual Product]**.

   ![Virtueel product toevoegen](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Stap 2: Kies de kenmerkset

Als u de optie [kenmerkset](attribute-sets.md) die als malplaatje voor het product wordt gebruikt, doe één van het volgende:

- Klik in het dialoogvenster **[!UICONTROL Attribute Set]** en voert u de naam van de kenmerkset geheel of gedeeltelijk in.

- Kies in de weergegeven lijst de kenmerkset die u wilt gebruiken.

Het formulier wordt bijgewerkt met de wijziging.

![Kenmerkset kiezen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Stap 3: Voer de vereiste instellingen in

1. Voer de **[!UICONTROL Product Name]**.

1. De standaardinstelling accepteren **[!UICONTROL SKU]** die is gebaseerd op de productnaam of een andere naam invoert.

1. Voer het product in **[!UICONTROL Price]**.

1. Aangezien het product nog niet gereed is om te publiceren, stelt u **[!UICONTROL Enable Product]** tot `No`.

1. Klikken **[!UICONTROL Save]** en doorgaan.

   Wanneer het product wordt opgeslagen, wordt [Winkelweergave](introduction.md#product-scope) wordt in de linkerbovenhoek weergegeven.

1. Kies de optie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![Winkelweergave kiezen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Stap 4: De basisinstellingen voltooien

1. Set **[!UICONTROL Tax Class]** op een van de volgende wijzen:

   - `None`
   - `Taxable Goods`

1. Voer de **[!UICONTROL Quantity]** van het product dat in voorraad is en het volgende doet:

   - De standaardinstelling accepteren **[!UICONTROL Stock Status]** instellen van `In Stock`.

     Omdat een virtueel product niet wordt verzonden, **[!UICONTROL Weight]** wordt niet gebruikt.

   - De standaardinstelling accepteren **[!UICONTROL Visibility]** instellen van `Catalog, Search`.

   >[!NOTE]
   >
   >Als u [Inventory management](../inventory-management/introduction.md), wordt de hoeveelheid in deze sectie ingesteld door handelaren van één bron. De multibronhandelaars voegen bronnen en hoeveelheden in de Bronsectie toe. Zie het volgende _Bronnen en hoeveelheden toewijzen (Inventory management)_ sectie.

1. Om **[!UICONTROL Categories]** voor het product klikt u op de knop **[!UICONTROL Select…]** en voer een van de volgende handelingen uit:

   **Een bestaande categorie kiezen**:

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van de categorie die u wilt toewijzen.

   **Een categorie maken**:

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** en kiest u **[!UICONTROL Parent Category]**, die de positie in de menustructuur bepaalt.

   - Klik op **[!UICONTROL Create Category]**.

   Er kunnen aanvullende individuele kenmerken zijn die het product beschrijven. De selectie varieert per kenmerkset en u kunt deze later voltooien.

### Bronnen en hoeveelheden toewijzen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Stap 5: De productinformatie invullen

Voer de benodigde gegevens in de volgende secties in:

- [Inhoud](product-content.md)
- [Afbeeldingen en video&#39;s](product-images-and-video.md)
- [Optimalisatie zoekmachine](product-search-engine-optimization.md)
- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)
- [Aanpasbare opties](settings-advanced-custom-options.md)
- [Producten op websites](settings-basic-websites.md)
- [Ontwerp](settings-advanced-design.md)
- [Cadeauopties](product-gift-options.md)

>[!NOTE]
>
>De _[!UICONTROL Is this downloadable product?]_is standaard uitgeschakeld. Als u deze functie inschakelt voor een virtueel product, wordt het product [Downloadbaar](product-create-downloadable.md#downloadable-product).

## Stap 6: Het product publiceren

1. Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** tot `Yes`.

1. Voer een van de volgende handelingen uit:

   - **Methode 1:** Opslaan en voorvertonen

      - Klik in de rechterbovenhoek op **[!UICONTROL Save]**.

      - Kies **[!UICONTROL Customer View]** op de _Beheerder_ ( ![Menupijl](../assets/icon-menu-down-arrow-black.png) ).

     De winkel wordt geopend in een nieuw browsertabblad.

     ![Klantenweergave](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Opslaan en sluiten

     Op de _[!UICONTROL Save]_(![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ), kiest u **[!UICONTROL Save & Close]**.

## Te onthouden zaken

- Virtuele producten worden gebruikt voor niet-tastbare producten zoals services, abonnementen en garanties.

- Virtuele producten lijken veel op eenvoudige producten, maar zonder gewicht.

- Verzendopties worden niet weergegeven tijdens het afrekenen, tenzij er een tastbaar product in de winkelwagen zit.
