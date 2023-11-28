---
title: Een winkelwagentje beheren
description: Leer hoe u een klant rechtstreeks via de beheerder kunt helpen met zijn winkelwagentje.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 1%

---

# Een winkelwagentje beheren

{{ee-feature}}

Als u een sessie voor ondersteund winkelen wilt starten, moet de klant bij de winkel zijn aangemeld bij de klant om de informatie beschikbaar te stellen. Als de klant geen account heeft, kunt u [één maken](../customers/account-create.md).

![Winkelwagentje in de klantenaccount](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Handelingencontrole

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Remove] | Hiermee verwijdert u items uit het huidige winkelwagentje |
| [!UICONTROL Move to Wish List] | Hiermee verplaatst u items naar de geselecteerde wenslijst van klanten |

{style="table-layout:auto"}

## Besturingsknoppen

| Knop | Beschrijving |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Wist het huidige winkelwagentje van alle producten. |
| [!UICONTROL Update Items and Quantities|]Voer de vereiste hoeveelheid in het dialoogvenster **[!UICONTROL Qty]** het aantal artikelen in het winkelwagentje bij te werken. |
| [!UICONTROL Add selections to my cart] | Hiermee voegt u producten van alle secties toe aan het winkelwagentje. |

{style="table-layout:auto"}

## Controleren of de klant is aangemeld

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Alle bezoekers van de winkel en aangemelde klanten worden in de lijst weergegeven.

   ![Klanten nu online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Bied assistentie bij winkelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Open in de lijst de klantrecord in de bewerkingsmodus.

   >[!TIP]
   >
   >Als u snel de gegevens van de klant wilt vinden, gebruikt u de [Filters](../getting-started/admin-grid-controls.md) controle.

   In het klantenprofiel onder _[!UICONTROL Personal Information]_de_[!UICONTROL Last Logged In]_ datum en tijd geven aan dat de klant online is.

   ![Klantprofiel van een online klant](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Als u de modus voor ondersteund winkelen wilt inschakelen, klikt u op **[!UICONTROL Manage Shopping Cart]** in de bovenste knopbalk.

   ![Assistent-winkelmodus](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Producten aan winkelwagentje per kenmerk toevoegen

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Products]** sectie.

1. Een product zoeken met een van de filters boven aan elke kolom.

1. Klik op **[!UICONTROL Search]**.

1. Gebruik een van de volgende stappen volgens het producttype:

### Een eenvoudig product toevoegen

1. Klik op het product dat u wilt bestellen.

   Met deze handeling wordt de record geselecteerd en ingesteld **[!UICONTROL Quantity]** op de standaardwaarde van `1`.

1. Werk indien nodig de geordende hoeveelheid bij.

1. Klik links boven het raster op **[!UICONTROL Add selections to my cart]**.

   ![Product toevoegen aan winkelwagentje](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   Het regelitem wordt boven aan de pagina toegevoegd aan het winkelwagentje.

   ![Winkelwagentje bijgewerkt](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Een product met configuratie toevoegen

Er zijn drie soorten producten die moeten worden gevormd alvorens aan de kar toe te voegen: `Bundle Product`, `Configurable Product`, en `Grouped Product`.

1. Klik in het raster op **[!UICONTROL Configure]** naast de productnaam.

   ![Het product configureren](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. In de _Bijbehorende producten_ , kiest u elke productoptie om het item te beschrijven dat u wilt bestellen, voert u de optie **[!UICONTROL Quantity]** en klik op **[!UICONTROL OK]**.

   Het product wordt geselecteerd met een vinkje en de geordende hoeveelheid wordt weergegeven in het raster.

1. Als u het product aan het winkelwagentje wilt toevoegen, klikt u op **[!UICONTROL Add selections to my cart]**.

   ![Configureerbaar product in de kar](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Werk zo nodig de productopties in het winkelwagentje bij:

   - Klik op **[!UICONTROL Configure]**.

   - Werk de opties bij en klik vervolgens op **[!UICONTROL OK]**.

## Product toevoegen door SKU

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Add to Shopping Cart by SKU]** sectie.

1. Producten afzonderlijk toevoegen door **[!UICONTROL SKU]** of voeg producten toe door een CSV-bestand te uploaden.

### Items afzonderlijk toevoegen door SKU

1. Voer de **[!UICONTROL SKU]** en **[!UICONTROL Qty]** van het te bestellen item.

1. Als u een ander product wilt bestellen, klikt u op **[!UICONTROL Add another]**.

   ![Producten toevoegen door SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Add selections to my cart]**.

1. Als het item een configureerbaar product is, kiest u de productopties wanneer u hierom wordt gevraagd en klikt u op **[!UICONTROL Add to Shopping Cart]**.

### Producten toevoegen door een CSV-bestand te uploaden

1. Een [csv-bestand](../systems/data-csv.md) met de items die aan het winkelwagentje moeten worden toegevoegd.

   Het bestand mag slechts twee kolommen bevatten, met `sku` en `qty` in de koptekst.

1. Upload het voorbereide bestand:

   - Klik op **[!UICONTROL Choose File]**.

   - Selecteer het bestand dat u wilt uploaden in de map.

## Een item overbrengen

U kunt objecten naar het winkelwagentje overbrengen vanuit de verlanglijst van een klant en onlangs bekeken, vergeleken of geordende objecten. Het aantal items in elke sectie wordt tussen haakjes achter de sectiekop weergegeven.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) een van de volgende secties:

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Selecteer in het raster elk product dat u wilt bestellen en voer de **[!UICONTROL Quantity]**.

1. Als u de opties voor een configureerbaar product wilt invoeren, klikt u op **[!UICONTROL Configure]** en stelt de productopties zo nodig in.

1. Klik op **[!UICONTROL Add selections to my cart]**.

1. Pas een couponcode toe, indien beschikbaar:

   - Voor **[!UICONTROL Apply Coupon Code]** Voer een geldige waardeboncode in.

   - Klik op de knop _Toepassen_ ( ![Pijlpictogram](../assets/icon-apply-arrow.png) ).

1. Pas de geordende hoeveelheid naar wens aan:

   - In de **[!UICONTROL Qty]** vermeld het juiste bedrag in de kolom van het aan te passen product.

   - Klik op **[!UICONTROL Update Items and Quantities]**.

## De volgorde maken

1. Klik op **[!UICONTROL Create Order]**.

   De _[!UICONTROL Create New Order]_op de pagina worden de objecten in het winkelwagentje weergegeven, gevolgd door de verzend- en betalingsgegevens.

1. Voltooi de verzend- en betalingsgegevens.

1. Klik op **[!UICONTROL Submit Order]**.

Zie voor meer informatie [Een bestelling maken](customer-account-create-order.md).
