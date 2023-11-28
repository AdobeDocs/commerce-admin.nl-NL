---
title: Uitchecken op nul subtotaal
description: Leer hoe u een subtotaal van nul instelt als een offline betalingsmethode in uw winkel.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Uitchecken op nul subtotaal

_Uitchecken op nul subtotaal_ kan worden gebruikt voor orders met een subtotaal van nul die worden belast nadat een korting is toegepast. Het subtotaal van nul kan bijvoorbeeld in de volgende situaties worden gebruikt:

- Een korting geldt voor de volledige aankoopprijs, zonder extra verzendkosten.

- De klant voegt een [downloadbaar](../catalog/product-create-downloadable.md) of [virtueel](../catalog/product-create-virtual.md) op het winkelwagentje, en de prijs is gelijk aan nul.

- De prijs van een [eenvoudig](../catalog/product-create-simple.md) het product is nul en het [gratis verzending](shipping-free.md) is beschikbaar.

- A [couponcode](../merchandising-promotions/price-rules-cart-coupon.md) dekt de volledige prijs van producten en verzendingen.

Om tijd te besparen, kunnen de geen bevelen van het subtotaal aan automatisch factuur worden geplaatst.

**_Om nul subtotal checkout te vormen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Payment Methods]**.

1. Onder _[!UICONTROL Other Payment Methods]_, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Zero Subtotal Checkout]**sectie.

   ![Afhandeling nul subtotaal](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Indien nodig eerst de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze instellingen te wijzigen.

1. Als u het uitchecken van het subtotaal nul wilt activeren, stelt u **[!UICONTROL Enabled]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die de methode Subtotaal nul aangeeft tijdens het afrekenen.

1. Als de orden typisch op goedkeuring wachten, keur het gebrek goed **[!UICONTROL New Order Status]** als `Pending"` totdat de order is goedgekeurd.

   U kunt desgewenst de opdracht `Processing` of `Suspected Fraud` status voor nieuwe orders met deze betalingsmethode.

1. Set **[!UICONTROL Automatically Invoice All Items]** tot `Yes` als je automatisch alle objecten met een saldo van nul wilt factureren.

   Deze optie is alleen beschikbaar als **[!UICONTROL New Order Status]** optie is ingesteld op `Processing`.

   >[!NOTE]
   >
   >Indien _[!UICONTROL New Order Status]_is ingesteld op `Processing` en_[!UICONTROL Automatically Invoice All Items]_ is ingesteld op `No`, moet u ook **[!UICONTROL Order Status]** = `Processing` voor de **[!UICONTROL Order State]** = `Pending` en **[!UICONTROL Default Status]** = `No` het toewijzen van [Status van bestelling](order-status.md#custom-order-status) pagina.

1. Set **[!UICONTROL Payment from Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) Deze betalingsmethode kan worden gebruikt.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, _[!UICONTROL Payment from Specific Countries]_wordt weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in dat de positie van dit object bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = eerst, `1` = seconde, `2` = derde, enzovoort.)

1. Klik op **[!UICONTROL Save Config]**.
