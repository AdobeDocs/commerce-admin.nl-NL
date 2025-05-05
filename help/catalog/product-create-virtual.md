---
title: Virtueel product
description: Leer hoe u een virtueel product maakt dat een niet-tastbaar item vertegenwoordigt, zoals een lidmaatschap, service, garantie of abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Virtueel product

Virtuele producten, of digitale goederen, vertegenwoordigen niet-tastbare zaken zoals lidmaatschappen, de diensten, de garanties, of abonnementen, en digitale downloads van boeken, muziek, video&#39;s, of andere producten. De virtuele producten kunnen individueel of inbegrepen als deel van het [ Gegroepeerde Product ](product-create-grouped.md), [ Configureerbaar Product ](product-create-configurable.md), of [ Bundel de producttypes van het Product ](product-create-bundle.md) worden verkocht.

Behalve de afwezigheid van het veld _[!UICONTROL Weight]_&#x200B;is het proces voor het maken van een virtueel product en een eenvoudig product hetzelfde. De volgende instructies tonen het proces aan om een virtueel product te creëren gebruikend a [ productmalplaatje ](attribute-sets.md), vereiste gebieden, en basismontages. Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

>[!NOTE]
>
>PayPal heeft de ondersteuning voor de verkoop van digitale goederen vervangen via PayPal Express Checkout. Zij adviseren dat u of [ de Norm van Betalingen van PayPal ](../stores-purchase/paypal-payments-standard.md) of een andere PayPal betaalgateway gebruikt om het even welke orde te verwerken die virtuele producten omvat.

![ Virtueel Product ](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Stap 1: Kies het producttype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Voor _[!UICONTROL Add Product]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu bij de hoger-juiste hoek, kies **[!UICONTROL Virtual Product]**.

   ![ voeg Virtueel Product ](./assets/product-add-virtual.png){width="700" zoomable="yes"} toe

## Stap 2: Kies de kenmerkset

Om de [ geplaatste attributen ](attribute-sets.md) te kiezen die als malplaatje voor het product wordt gebruikt, doe één van het volgende:

- Klik in het veld **[!UICONTROL Attribute Set]** en voer de naam van de kenmerkset geheel of gedeeltelijk in.

- Kies in de weergegeven lijst de kenmerkset die u wilt gebruiken.

Het formulier wordt bijgewerkt met de wijziging.

![ kies Vastgestelde Attributen ](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Stap 3: Voer de vereiste instellingen in

1. Voer de **[!UICONTROL Product Name]** in.

1. Accepteer de standaardwaarde **[!UICONTROL SKU]** die is gebaseerd op de productnaam of voer een andere naam in.

1. Voer het product **[!UICONTROL Price]** in.

1. Stel **[!UICONTROL Enable Product]** in op `No` omdat het product nog niet kan worden gepubliceerd.

1. Klik op **[!UICONTROL Save]** en ga verder.

   Wanneer het product wordt bewaard, verschijnt de [ verkiesster van de Mening van de Opslag ](introduction.md#product-scope) in de upper-left hoek.

1. Kies de locatie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![ kies de Mening van de Opslag ](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Stap 4: De basisinstellingen voltooien

1. Stel **[!UICONTROL Tax Class]** in op een van de volgende opties:

   - `None`
   - `Taxable Goods`

1. Voer de **[!UICONTROL Quantity]** in van het product dat in voorraad is en voer de volgende handelingen uit:

   - Accepteer de standaardinstelling **[!UICONTROL Stock Status]** van `In Stock` .

     Omdat een virtueel product niet wordt verzonden, wordt het veld **[!UICONTROL Weight]** niet gebruikt.

   - Accepteer de standaardinstelling **[!UICONTROL Visibility]** van `Catalog, Search` .

   >[!NOTE]
   >
   >Als u [ Inventory management ](../inventory-management/introduction.md) toelaat, plaatsen enige bronverkopers de hoeveelheid in deze sectie. De multibronhandelaars voegen bronnen en hoeveelheden in de Bronsectie toe. Zie het volgende _toewijzen Bronnen en Hoeveelheden (Inventory management)_ sectie.

1. Als u **[!UICONTROL Categories]** aan het product wilt toewijzen, klikt u op het vak **[!UICONTROL Select…]** en voert u een van de volgende handelingen uit:

   **kies een bestaande categorie**:

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van de categorie die u wilt toewijzen.

   **creeer een categorie**:

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** in en kies de **[!UICONTROL Parent Category]** die de positie in de menustructuur bepaalt.

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
>De optie _[!UICONTROL Is this downloadable product?]_&#x200B;is standaard uitgeschakeld. Het toelaten van deze eigenschap voor een virtueel product maakt het product [ Downloadbaar ](product-create-downloadable.md#downloadable-product).

## Stap 6: Publish het product

1. Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** in op `Yes` .

1. Voer een van de volgende handelingen uit:

   - **Methode 1:** sparen en voorproef

      - Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

      - Om het product in uw opslag te bekijken, verkies **[!UICONTROL Customer View]** op _Admin_ ( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-black.png)) menu.

     De winkel wordt geopend in een nieuw browsertabblad.

     ![ Mening van de Klant ](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** sparen en sluit

     Voor _[!UICONTROL Save]_(![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu, kies **[!UICONTROL Save & Close]**.

## Te onthouden zaken

- Virtuele producten worden gebruikt voor niet-tastbare producten zoals services, abonnementen en garanties.

- Virtuele producten lijken veel op eenvoudige producten, maar zonder gewicht.

- Verzendopties worden niet weergegeven tijdens het afrekenen, tenzij er een tastbaar product in de winkelwagen zit.
