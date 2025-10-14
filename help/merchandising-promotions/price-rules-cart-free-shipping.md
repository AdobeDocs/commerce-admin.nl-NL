---
title: Voorbeeld van de prijsregel voor winkelwagentjes - gratis verzendpromotie
description: Bekijk een voorbeeld van het gebruik van een regel voor winkelprijzen voor gratis verzending.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - gratis verzendpromotie

Het vrije verschepen kan als bevordering, of met, of zonder a [&#x200B; coupon &#x200B;](price-rules-cart-coupon.md) worden aangeboden. Een vrije het verschepen coupon, of bon, kan ook op klant ophaalorden worden toegepast, zodat kan de orde worden gefactureerd en worden verscheept om het [&#x200B; werkschema &#x200B;](../stores-purchase/order-processing.md#order-workflow-and-processing) te voltooien.

Sommige configuraties van verzenddragers bieden u de mogelijkheid om gratis verzending aan te bieden op basis van een minimumbestelling. Om op dit basisvermogen uit te breiden, kunt u het winkelen de prijsregels van het karretje gebruiken om complexe voorwaarden tot stand te brengen die op veelvoudige productattributen, kartinhoud, en klantengroepen worden gebaseerd.

## Stap 1. Gratis verzending toestaan

1. Laat [&#x200B; vrije verzending &#x200B;](../stores-purchase/shipping-free.md) in uw opslagconfiguratie toe.

1. Voltooi de vrije het verschepen montages voor om het even welke [&#x200B; dragerdienst &#x200B;](../stores-purchase/carriers.md) die u voor het vrije verschepen wilt gebruiken.

## Stap 2. Een regel voor een winkelwagenprijs maken

Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Voer de onderstaande stappen uit om het type gratis verzendpromotie in te stellen dat je wilt aanbieden.

### Voorbeeld 1: gratis verzending voor elke bestelling

1. Voltooi **[!UICONTROL Rule Information]** als volgt:

   - Voer een **[!UICONTROL Rule Name]** in voor interne referentie.
   - Voer een korte beschrijving **[!UICONTROL Description]** in om de regel te beschrijven.
   - Stel **[!UICONTROL Active]** in op `Yes` .
   - Selecteer in het vak **[!UICONTROL Websites]** elke site waar de gratis coupon beschikbaar moet zijn.
   - Selecteer de **[!UICONTROL Customer Groups]** waarop de regel van toepassing is.
   - Stel **[!UICONTROL Coupon]** in op een van de volgende opties:
      - Accepteer de standaardinstelling (`No Coupon`) als u een speciale aanbieding voor verzending zonder coupon wilt aanbieden.
      - Selecteer `Specific Coupon` als u een coupon met de prijsregel wilt gebruiken. Indien nodig, voltooi de instructies aan opstelling a [&#x200B; coupon &#x200B;](price-rules-cart-coupon.md).

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Actions]** sectie en doet het volgende:

   - Stel **[!UICONTROL Apply]** in op `Percent of product price discount` .
   - Stel **[!UICONTROL Apply to Shipping Amount]** in op `Yes` .
   - Stel **[!UICONTROL Free Shipping]** in op `For matching items only` .

   ![&#x200B; de prijsregel van de Kar - het vrije verschepen acties &#x200B;](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Voorbeeld 2: Gratis verzending voor bestellingen van meer dan $

1. Voltooi de **[!UICONTROL General Information]** -instellingen zoals in het vorige voorbeeld wordt beschreven.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Conditions]** sectie.

1. Klik _toevoegen_ (![&#x200B; voeg pictogram &#x200B;](../assets/icon-add-green-circle.png) toe) om een voorwaarde op te nemen en het volgende te doen:

   - Kies in de lijst onder **[!UICONTROL Cart Attribute]** de optie `Subtotal` .
   - Klik op **[!UICONTROL is]** en kies `equals or greater than` .
   - Klik **..** en ga een drempelwaarde voor Subtotal, zoals `100` in, om de voorwaarde te voltooien.

   ![&#x200B; de prijsregel van de Kar - voorwaarde &#x200B;](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Indien noodzakelijk, breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** sectie uit en doe het volgende:

   - Stel **[!UICONTROL Apply]** in op `Percent of product price discount` .
   - Stel **[!UICONTROL Apply to Shipping Amount]** in op `Yes` .
   - Stel **[!UICONTROL Free Shipping]** in op `For matching items only` .

## Stap 3. De labels voltooien

Voltooi [&#x200B; Stap 4 &#x200B;](price-rules-cart.md) van de de regelinstructies van de kartprijs om het even welke etiketten in te gaan die tijdens controle verschijnen.

## Stap 4. De regel opslaan en testen

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.

1. Test de regel om er zeker van te zijn dat deze correct werkt.
