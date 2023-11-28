---
title: Voorbeeld van de prijsregel voor winkelwagentjes - gratis verzendpromotie
description: Bekijk een voorbeeld van het gebruik van een regel voor winkelprijzen voor gratis verzending.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - gratis verzendpromotie

Gratis verzending kan worden aangeboden als speciale actie, met of zonder [coupon](price-rules-cart-coupon.md). Een gratis coupon (of voucher) kan ook worden toegepast op ophaalopdrachten van klanten, zodat de bestelling kan worden gefactureerd en verzonden om de [werkstroom](../stores-purchase/order-processing.md#order-workflow-and-processing).

Sommige configuraties van verzenddragers bieden u de mogelijkheid om gratis verzending aan te bieden op basis van een minimumbestelling. Om op dit basisvermogen uit te breiden, kunt u het winkelen de prijsregels van het karretje gebruiken om complexe voorwaarden tot stand te brengen die op veelvoudige productattributen, kartinhoud, en klantengroepen worden gebaseerd.

## Stap 1. Gratis verzending toestaan

1. Inschakelen [gratis verzending](../stores-purchase/shipping-free.md) in uw winkelconfiguratie.

1. Vul de instellingen voor gratis verzending in voor alle [transportdienst](../stores-purchase/carriers.md) die je wilt gebruiken voor gratis verzending.

## Stap 2. Een regel voor een winkelwagenprijs maken

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Voer de onderstaande stappen uit om het type gratis verzendpromotie in te stellen dat je wilt aanbieden.

### Voorbeeld 1: gratis verzending voor elke bestelling

1. Voltooi de **[!UICONTROL Rule Information]** als volgt:

   - Voer een **[!UICONTROL Rule Name]** voor interne referentie.
   - Voer een korte beschrijving in **[!UICONTROL Description]** om de regel te beschrijven.
   - Set **[!UICONTROL Active]** tot `Yes`.
   - In de **[!UICONTROL Websites]** selecteert u elke site waar de gratis coupon beschikbaar is.
   - Selecteer de **[!UICONTROL Customer Groups]** waarop de regel van toepassing is.
   - Set **[!UICONTROL Coupon]** op een van de volgende wijzen:
      - Als je gratis verzendpromotie wilt aanbieden zonder coupon, accepteer je de standaardwaarde (`No Coupon`) instellen.
      - Als u een coupon wilt gebruiken met de prijsregel, selecteert u `Specific Coupon`. Indien nodig, voltooi de instructies om een [coupon](price-rules-cart-coupon.md).

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Apply]** tot `Percent of product price discount`.
   - Set **[!UICONTROL Apply to Shipping Amount]** tot `Yes`.
   - Set **[!UICONTROL Free Shipping]** tot `For matching items only`.

   ![Winkelprijsregel - Handelingen voor gratis verzending](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Voorbeeld 2: Gratis verzending voor bestellingen van meer dan $

1. Voltooi de **[!UICONTROL General Information]** instellingen zoals beschreven in het vorige voorbeeld.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Conditions]** sectie.

1. Klikken _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) om een voorwaarde in te voegen en het volgende te doen:

   - In de lijst onder **[!UICONTROL Cart Attribute]**, kiest u `Subtotal`.
   - Klikken **[!UICONTROL is]** en kiest u `equals or greater than`.
   - Klikken **...** en voer een drempelwaarde in voor het subtotaal, zoals `100`, om de voorwaarde te voltooien.

   ![Wisselkoersregel - voorwaarde](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Indien nodig uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Apply]** tot `Percent of product price discount`.
   - Set **[!UICONTROL Apply to Shipping Amount]** tot `Yes`.
   - Set **[!UICONTROL Free Shipping]** tot `For matching items only`.

## Stap 3. De labels voltooien

Voltooid [Stap 4](price-rules-cart.md) van de instructies in het kader van de prijsregel voor winkelwagentjes om eventuele labels in te voeren die tijdens de afhandeling worden weergegeven.

## Stap 4. De regel opslaan en testen

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.

1. Test de regel om er zeker van te zijn dat deze correct werkt.
