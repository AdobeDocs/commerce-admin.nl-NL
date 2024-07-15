---
title: Voorbeeld van de prijsregel voor winkelwagentjes - korting met minimumaankoop
description: Bekijk een voorbeeld van het gebruik van een winkelprijsegel om een korting met een minimale aankoop aan te bieden.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - korting met minimumaankoop

De prijsregels voor winkelwagentjes kunnen worden gebruikt om een percentagekorting aan te bieden op basis van een minimumaankoop. In het volgende voorbeeld wordt een korting van 25% toegepast op alle aankopen boven $200,00 in een specifieke categorie. Het formaat van de korting is als volgt:

X% korting op alle Y (categorie) boven $Z dollars

## Stap 1. Een winkelwagentregel maken

Volg de basis [ instructies ](price-rules-cart.md) om een wortelregel tot stand te brengen.

## Stap 2. De voorwaarden definiëren

1. De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Conditions]** sectie.

1. Klik _toevoegen_ (![ voeg pictogram ](../assets/icon-add-green-circle.png) toe) en kies **[!UICONTROL Product Attribute Combination]**.

   ![ de voorwaarde van de prijsregel van de Kar - de combinatie van productattributen ](./assets/condition1.png){width="500" zoomable="yes"}

1. Klik _toevoegen_ (![ voeg pictogram ](../assets/icon-add-green-circle.png) toe) aan het begin van de volgende lijn en in de lijst onder **[!UICONTROL Product Attribute]**, kies **[!UICONTROL Category]**.

   - Klik (**..**) _meer_ verbinding om extra opties te tonen.

     ![ voorwaarde van de prijsregel van de Kar - categorieopties ](./assets/condition3.png){width="600" zoomable="yes"}

   - Klik het _pictogram van de Kiezer_ (![ pictogram van de Lijst ](../assets/icon-list-chooser.png)) om de beschikbare categorieën te zien. Schakel in de categoriestructuur het selectievakje in van elke categorie die u wilt opnemen. Klik op het controlepictogram om de rubriekselecties te accepteren.

     ![ voorwaarde van de prijsregel van de Kar - categorie ](./assets/condition4.png){width="600" zoomable="yes"}

1. Klik _toevoegen_ (![ voeg pictogram ](../assets/icon-add-green-circle.png) toe) aan het begin van de volgende lijn en doe het volgende:

   - Kies in de lijst onder **[!UICONTROL Cart Item Attribute]** de optie **[!UICONTROL Price in cart]** .

     ![ de voorwaarde van de prijsregel van de Kar - het attribuut van het wortelpunt ](./assets/condition5.png){width="500"}

   - Klik **is** en kies `equals or greater than`.

   - Klik op **..** en voer het bedrag in dat de prijs in winkelwagentje moet hebben om aan de voorwaarde te voldoen. Voer bijvoorbeeld `30` in.

     ![ voorwaarde van de prijsregel van de Kar - prijs in kar ](./assets/condition6.png){width="500"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

## Stap 3. De acties definiëren

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** sectie uit en doe het volgende:

   ![ de acties van de prijsregel van de Kar ](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Apply]** in op `Percent of product price discount` .

   - Voer de **[!UICONTROL Discount Amount]** in. Voer bijvoorbeeld `10` in voor een korting van 10%.

   - Stel **[!UICONTROL Discard subsequent rules]** in op `Yes` als u wilt voorkomen dat extra promoties op de aankoop worden toegepast.

1. Klik op **[!UICONTROL Save and Continue Edit]** en voer de gewenste regel in.

## Stap 4. De labels voltooien

Voltooi [ Stap 4 ](price-rules-cart.md) van de de regelinstructies van de kartprijs om het even welke etiketten in te gaan die tijdens controle verschijnen.

## Stap 5: Sla de regel op en test deze

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.

1. Test de regel om er zeker van te zijn dat deze correct werkt.
