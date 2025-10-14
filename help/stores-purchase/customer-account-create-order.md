---
title: Een bestelling maken
description: Leer hoe u een bestelling voor een klant maakt in Commerce Admin.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 0e2d79f6b716f5d59aa9cd60b096608a6b2dbb98
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 1%

---

# Een bestelling maken

Voor geregistreerde klanten die hulp nodig hebben, kunt u een volledige orde direct van Admin tot stand brengen. Het _[!UICONTROL Create New Order]_-formulier bevat alle informatie die nodig is voor het normale uitcheckproces, met activiteitenoverzichten van het rekeningdashboard van de klant.

![&#x200B; creeer een orde voor een klant &#x200B;](./assets/create-new-order.png){width="700" zoomable="yes"}

## Stap 1: Een bestelling maken

1. Voor _Admin_ sidebar, klik **[!UICONTROL Customers]**.

1. Zoek de klant in het raster.

1. In de _kolom van de Actie_, klik **[!UICONTROL Edit]**.

1. Klik in de koptekst van de werkruimte op **[!UICONTROL Create Order]** .

   ![&#x200B; de kopbal van Workspace &#x200B;](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   U kunt een orde in de [&#x200B; werkruimte van de Orde &#x200B;](orders.md#orders-workspace) ook tot stand brengen door **[!UICONTROL Create New Order]** te klikken.

## Stap 2: Producten toevoegen

Als uw winkel meerdere weergaven heeft, kiest u de winkelweergave waarin de volgorde moet worden geplaatst.

### Producten toevoegen uit de zijbalk [!UICONTROL Customer's Activities]

U kunt items naar het winkelwagentje overbrengen van de verlanglijst van een klant of van onlangs bekeken, vergeleken of geordende items.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) één van de volgende secties uit:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Schakel het selectievakje van elk product in het linkerdeelvenster in.

1. Schuif omlaag en klik op **[!UICONTROL Update Changes]** .

   Het item wordt weergegeven in het bestelformulier.

   ![&#x200B; toevoegen aan Kar &#x200B;](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Producten toevoegen uit de catalogus

1. Klik op **[!UICONTROL Add Products]**.

   ![&#x200B; voeg Producten &#x200B;](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"} toe

1. Selecteer in het raster het selectievakje van elk product dat aan de winkelwagentje moet worden toegevoegd en voer de **[!UICONTROL Qty]** in die u wilt kopen.

   ![&#x200B; Uitgezochte Producten &#x200B;](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >In het productselectieraster worden altijd reguliere basisprijzen voor producten weergegeven, zonder kortingen en de toegepaste regels voor de kartel- of groepsprijs. De uiteindelijke prijs van het product wordt alleen berekend wanneer het product aan een bestelling/karretje wordt toegevoegd.

1. Beschikbare productopties configureren:

   - Klik op **[!UICONTROL Configure]**.

   - Vul de gewenste opties in.

   - Klik op **[!UICONTROL OK]**.

   - Klik op **[!UICONTROL Add Selected Product(s) to Order]** om het winkelwagentje bij te werken.

1. Als een product voor [&#x200B; giftopties &#x200B;](../catalog/product-gift-options.md) wordt gevormd, plaats de opties zoals nodig.

1. Overschrijf indien nodig de prijs van een object:

   - Schakel het selectievakje **[!UICONTROL Custom Price]** in en voer in het onderstaande vak de nieuwe prijs in.

   - Klik op **[!UICONTROL Update Items and Quantities]** om de totaal van de winkelwagentjes bij te werken.

   ![&#x200B; Aangepaste Prijs &#x200B;](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Vul de volgende secties in die u nodig hebt voor de bestelling:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]
   - [[!UICONTROL [kenmerken van aangepaste volgorde]]](../stores-purchase/order-processing.md#custom-order-attributes)

>[!NOTE]
>
>Zie de [&#x200B; Gids van de Diensten van de Betaling &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce/payment-services/guide-overview) voor meer informatie over betalingsmethodes om deze functionaliteit te steunen wanneer de uitbreiding van de Diensten van de Betaling geïnstalleerd en gevormd is.

## Stap 3: De bestelling verzenden

Klik op **[!UICONTROL Submit Order]**.

Er wordt een bevestiging verzonden naar de klant en de klant kan de bestelgegevens van zijn account bekijken.
