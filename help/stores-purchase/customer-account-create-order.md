---
title: Een bestelling maken
description: Leer hoe u een bestelling voor een klant maakt in Commerce Admin.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Een bestelling maken

Voor geregistreerde klanten die hulp nodig hebben, kunt u een volledige orde direct van Admin tot stand brengen. De _[!UICONTROL Create New Order]_het formulier bevat alle informatie die nodig is voor het normale afrekenproces, met activiteitenoverzichten van het rekeningdashboard van de klant.

![Een bestelling voor een klant maken](./assets/create-new-order.png){width="700" zoomable="yes"}

## Stap 1: Een bestelling maken

1. Op de _Beheerder_ zijbalk, klikken **[!UICONTROL Customers]**.

1. Zoek de klant in het raster.

1. In de _Handeling_ kolom, klik **[!UICONTROL Edit]**.

1. Klik in de koptekst van de werkruimte op **[!UICONTROL Create Order]**.

   ![Werkruimtekop](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   U kunt ook een volgorde maken in het dialoogvenster [Werkruimte Bestellen](orders.md#orders-workspace) door te klikken **[!UICONTROL Create New Order]**.

## Stap 2: Producten toevoegen

Als uw winkel meerdere weergaven heeft, kiest u de winkelweergave waarin de volgorde moet worden geplaatst.

### Producten toevoegen uit de [!UICONTROL Customer's Activities] zijbalk

U kunt items naar het winkelwagentje overbrengen van de verlanglijst van een klant of van onlangs bekeken, vergeleken of geordende items.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) een van de volgende secties:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Schakel het selectievakje van elk product in het linkerdeelvenster in.

1. Omlaag schuiven en klikken **[!UICONTROL Update Changes]**.

   Het item wordt weergegeven in het bestelformulier.

   ![Toevoegen aan winkelwagentje](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Producten toevoegen uit de catalogus

1. Klik op **[!UICONTROL Add Products]**.

   ![Producten toevoegen](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. Schakel in het raster het selectievakje in van elk product dat aan het winkelwagentje moet worden toegevoegd en typ de optie **[!UICONTROL Qty]** te kopen.

   ![Producten selecteren](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >In het productselectieraster worden altijd reguliere basisprijzen voor producten weergegeven, zonder kortingen en de toegepaste regels voor de kartel- of groepsprijs. De uiteindelijke prijs van het product wordt alleen berekend wanneer het product aan een bestelling/karretje wordt toegevoegd.

1. Beschikbare productopties configureren:

   - Klik op **[!UICONTROL Configure]**.

   - Vul de gewenste opties in.

   - Klik op **[!UICONTROL OK]**.

   - Klikken **[!UICONTROL Add Selected Product(s) to Order]** de winkelwagen bijwerken.

1. Als een product is geconfigureerd voor [cadeauopties](../catalog/product-gift-options.md)stelt u de gewenste opties in.

1. Overschrijf indien nodig de prijs van een object:

   - Selecteer de **[!UICONTROL Custom Price]** en voer in onderstaand vak de nieuwe prijs in.

   - Klik op **[!UICONTROL Update Items and Quantities]**.

   ![Aangepaste prijs](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Vul de volgende secties in die u nodig hebt voor de bestelling:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>Zie de [Handleiding voor betalingsservices](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) voor meer informatie over betalingsmethoden om deze functionaliteit te ondersteunen wanneer de extensie Betalingsservices is geïnstalleerd en geconfigureerd.

## Stap 3: De bestelling verzenden

Klik op **[!UICONTROL Submit Order]**.

Er wordt een bevestiging verzonden naar de klant en de klant kan de bestelgegevens van zijn account bekijken.
