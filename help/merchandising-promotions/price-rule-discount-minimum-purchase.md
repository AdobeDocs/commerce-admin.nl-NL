---
title: Voorbeeld van de prijsregel voor winkelwagentjes - korting op de minimumprijs van het product
description: Bekijk een voorbeeld van het gebruik van een winkelprijsegel om een korting aan te bieden met een minimale productprijs.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 1a784e894e02090cfa3bc9edc47149b35d935e8e
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - korting op de minimumprijs van het product

De prijsregels voor winkelwagentjes kunnen worden gebruikt om een korting op basis van een minimumprijs in het winkelwagentje aan te bieden. In het volgende voorbeeld wordt een korting van 10% toegepast op alle producten in het hele winkelwagentje wanneer ten minste één product met een prijs van meer dan € 30,00 uit een bepaalde categorie aan het winkelwagentje wordt toegevoegd. Het formaat van de korting is als volgt:

X% hele kar korting wanneer ten minste 1 product van de Y-categorie komt en de prijs ervan meer dan $Z dollar bedraagt.

## Stap 1. Een winkelwagentregel maken

Volg de basis [&#x200B; instructies &#x200B;](price-rules-cart.md) om een wortelregel tot stand te brengen.

## Stap 2. De voorwaarden definiëren

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Conditions]** sectie.

1. Klik _toevoegen_ (![&#x200B; voeg pictogram &#x200B;](../assets/icon-add-green-circle.png) toe) en kies **[!UICONTROL Product Attribute Combination]**.

   ![&#x200B; de voorwaarde van de prijsregel van de Kar - de combinatie van productattributen &#x200B;](./assets/condition1.png){width="500" zoomable="yes"}

1. Klik _toevoegen_ (![&#x200B; voeg pictogram &#x200B;](../assets/icon-add-green-circle.png) toe) aan het begin van de volgende lijn en in de lijst onder **[!UICONTROL Product Attribute]**, kies **[!UICONTROL Category]**.

   - Klik (**..**) _meer_ verbinding om extra opties te tonen.

     ![&#x200B; voorwaarde van de prijsregel van de Kar - categorieopties &#x200B;](./assets/condition3.png){width="600" zoomable="yes"}

   - Klik het _pictogram van de Kiezer_ (![&#x200B; pictogram van de Lijst &#x200B;](../assets/icon-list-chooser.png)) om de beschikbare categorieën te zien. Schakel in de categoriestructuur het selectievakje in van elke categorie die u wilt opnemen. Klik op het controlepictogram om de rubriekselecties te accepteren.

     ![&#x200B; voorwaarde van de prijsregel van de Kar - categorie &#x200B;](./assets/condition4.png){width="600" zoomable="yes"}

1. Klik _toevoegen_ (![&#x200B; voeg pictogram &#x200B;](../assets/icon-add-green-circle.png) toe) aan het begin van de volgende lijn en doe het volgende:

   - Kies in de lijst onder **[!UICONTROL Cart Item Attribute]** de optie **[!UICONTROL Price in cart]** .

     ![&#x200B; de voorwaarde van de prijsregel van de Kar - het attribuut van het wortelpunt &#x200B;](./assets/condition5.png){width="500"}

   - Klik **is** en kies `equals or greater than`.

   - Klik op **..** en voer het bedrag in dat de prijs in winkelwagentje moet hebben om aan de voorwaarde te voldoen. Voer bijvoorbeeld `30` in.

     ![&#x200B; voorwaarde van de prijsregel van de Kar - prijs in kar &#x200B;](./assets/condition6.png){width="500"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

## Stap 3. De acties definiëren

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** sectie uit en doe het volgende:

   ![&#x200B; de acties van de prijsregel van de Kar &#x200B;](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Apply]** in op `Percent of product price discount` .

   - Voer de **[!UICONTROL Discount Amount]** in. Voer bijvoorbeeld `10` in voor een korting van 10%.

   - Stel **[!UICONTROL Discard subsequent rules]** in op `Yes` als u wilt voorkomen dat extra promoties op de aankoop worden toegepast.

1. Klik op **[!UICONTROL Save and Continue Edit]** en voer de gewenste regel in.

## Stap 4. De labels voltooien

Voltooi [&#x200B; Stap 4 &#x200B;](price-rules-cart.md) van de de regelinstructies van de kartprijs om het even welke etiketten in te gaan die tijdens controle verschijnen.

## Stap 5: Sla de regel op en test deze

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.
1. Test de regel om er zeker van te zijn dat deze correct werkt.
