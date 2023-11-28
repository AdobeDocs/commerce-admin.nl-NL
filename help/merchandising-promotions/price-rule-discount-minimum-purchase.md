---
title: Voorbeeld van de prijsregel voor winkelwagentjes - korting met minimumaankoop
description: Bekijk een voorbeeld van het gebruik van een winkelprijsegel om een korting met een minimale aankoop aan te bieden.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - korting met minimumaankoop

De prijsregels voor winkelwagentjes kunnen worden gebruikt om een percentagekorting aan te bieden op basis van een minimumaankoop. In het volgende voorbeeld wordt een korting van 25% toegepast op alle aankopen boven $200,00 in een specifieke categorie. Het formaat van de korting is als volgt:

X% korting op alle Y (categorie) boven $Z dollars

## Stap 1. Een winkelwagentregel maken

Volg de basis [instructies](price-rules-cart.md) om een winkelwagentje te maken.

## Stap 2. De voorwaarden definiëren

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Conditions]** sectie.

1. Klikken _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) en kiest u **[!UICONTROL Product Attribute Combination]**.

   ![Voorwaarde van de prijsregel voor winkelwagentjes - combinatie van productkenmerken](./assets/condition1.png){width="500" zoomable="yes"}

1. Klikken _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) aan het begin van de volgende regel en in de lijst onder **[!UICONTROL Product Attribute]**, kiest u **[!UICONTROL Category]**.

   - Klik op de knop (**...**) _meer_ voor het weergeven van extra opties.

     ![Voorwaarde van de prijsregel voor winkelwagentjes - rubriekopties](./assets/condition3.png){width="600" zoomable="yes"}

   - Klik op de knop _Kiezer_ (![Lijstpictogram](../assets/icon-list-chooser.png)) om de beschikbare categorieën weer te geven. Schakel in de categoriestructuur het selectievakje in van elke categorie die u wilt opnemen. Klik op het controlepictogram om de rubriekselecties te accepteren.

     ![Voorwaarde van de prijsregel voor winkelwagentjes - rubriek](./assets/condition4.png){width="600" zoomable="yes"}

1. Klikken _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) aan het begin van de volgende regel en voer de volgende handelingen uit:

   - In de lijst onder **[!UICONTROL Cart Item Attribute]**, kiest u **[!UICONTROL Price in cart]**.

     ![Voorwaarde van de prijsregel voor winkelwagentjes - kenmerk van winkelwagentje](./assets/condition5.png){width="500"}

   - Klikken **is** en kiest u `equals or greater than`.

   - Klikken **...** en voer het bedrag in dat de prijs in winkelwagentje moet zijn om aan de voorwaarde te voldoen. Voer bijvoorbeeld `30`.

     ![Voorwaarde voor de prijsregel voor winkelwagentjes - prijs in winkelwagentje](./assets/condition6.png){width="500"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

## Stap 3. De acties definiëren

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** en voer de volgende handelingen uit:

   ![Handelingen met prijsregels voor winkelwagentjes](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Apply]** tot `Percent of product price discount`.

   - Voer de **[!UICONTROL Discount Amount]**. Voer bijvoorbeeld `10` voor een korting van 10%.

   - Als u wilt voorkomen dat extra aanbiedingen op de aankoop worden toegepast, stelt u **[!UICONTROL Discard subsequent rules]** tot `Yes`.

1. Klikken **[!UICONTROL Save and Continue Edit]** en vult de regel zo nodig in.

## Stap 4. De labels voltooien

Voltooid [Stap 4](price-rules-cart.md) van de instructies in het kader van de prijsregel voor winkelwagentjes om eventuele labels in te voeren die tijdens de afhandeling worden weergegeven.

## Stap 5: Sla de regel op en test deze

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.

1. Test de regel om er zeker van te zijn dat deze correct werkt.
