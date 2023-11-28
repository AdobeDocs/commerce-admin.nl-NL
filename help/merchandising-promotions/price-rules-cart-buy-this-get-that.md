---
title: Voorbeeld van de prijsregel voor winkelwagentjes - koop dit object
description: Bekijk een voorbeeld van het gebruik van een winkelprijsegel om een koop-dit-krijgen-die bevordering aan te bieden.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - koop dit object

In dit voorbeeld wordt getoond hoe u een [kartonnen prijsregel](price-rules-cart.md) voor een _Koop dit, krijg het gratis_ bevordering. Het formaat van de korting is als volgt:

_Koop X hoeveelheid product, ontvang gratis Y hoeveelheid_

## Stap 1. Een regel voor een winkelwagenprijs maken

Voltooid [Stap 1](price-rules-cart.md) instructies voor het invullen van de regelgegevens in het kader van de regels voor de kartprijs.

## Stap 2. De voorwaarden definiëren

Voltooid [Stap 2](price-rules-cart.md) van de instructies in het winkelwagentje om de voorwaarden voor de prijsregel te bepalen. Dit is de eerste van twee voorwaarden die aan de regel kunnen worden toegevoegd, en bepaalt wanneer de regel wordt teweeggebracht. Het kan gebaseerd zijn op een combinatie van het volgende:

- Productkenmerken
- Producten
- Kenmerken van winkelwagentje
- ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Klantsegmenten

Als deze optie leeg blijft, wordt de regel geactiveerd voor elk winkelwagentje.

![Wisselkoersregel - voorwaarde](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Stap 3. De acties definiëren

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Actions]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Apply]** tot `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Set **[!UICONTROL Discount Amount]** tot `1`. Dit is het aantal dat de klant gratis ontvangt.

   - Als u het aantal kortingen wilt beperken dat kan worden toegepast wanneer aan de voorwaarde wordt voldaan, voert u het getal in het dialoogvenster **[!UICONTROL Maximum Qty Discount is Applied To]** veld. Dit wordt op basis van deze [formule](#maximum-quantity-discount).

   - Voor **[!UICONTROL Discount Qty Step (Buy X)]**, voert u het aantal in dat de klant moet kopen om in aanmerking te komen voor de korting. In dit voorbeeld moet de klant er drie kopen.

   - Als u wilt voorkomen dat andere kortingen op de aankoop worden toegepast, stelt u **[!UICONTROL Discard subsequent rules]** tot `Yes`.

   ![Regel voor winkelprijzen - koop 3 krijgt 1 gratis](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Als u de regel alleen wilt toepassen op specifieke artikelen in de winkelwagentje, vult u de voorwaarde in om de winkelwagentjes en/of productkenmerken te beschrijven die vereist zijn voor de promotie.

   Het volgende voorbeeld gebruikt SKU om de regel op alle bijbehorende variaties van een configureerbaar product toe te passen.

   ![Winkelprijsregel - voorwaarde voor winkelwagentjes](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Opnemen **[!UICONTROL Free Shipping]**, kiest u `For matching items only`.

1. Klikken **[!UICONTROL Save and Continue Edit]** en de rest van de regel zo nodig voltooien.

## Stap 4. Het label invullen

Voltooid [Stap 4](price-rules-cart.md) van de instructies in het kader van de prijsregel voor winkelwagentjes om het label in te voeren dat tijdens de afhandeling wordt weergegeven.

## Stap 5: Sla de regel op en test deze

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.

1. Test de regel om er zeker van te zijn dat deze correct werkt.

## Variaties

Koop X Gratis ophalen wordt verwerkt als één handeling, met een _rijtotaal_ afhankelijkheid. Alle objecten moeten van dezelfde SKU afkomstig zijn om in aanmerking te komen voor de speciale actie. Bijvoorbeeld:

Koop X-hoeveelheid product van categorie A en ontvang gratis Y-hoeveelheid van hetzelfde product.

Als u het vrije product wilt beperken tot de categorieën A, B en C, stelt u de actie als volgt in:

Als ALLE van deze voorwaarden WAAR zijn: Categorie is één van A, B, C

Als u de gratis items van een categorie (A, B of C) wilt beperken en Y van SKU&#39;s (D123, E123 of F123) wilt ontvangen, stelt u de actie als volgt in:

Als ALLE van deze voorwaarden WAAR zijn: SKU is een van D123, E123, F123

## Maximale korting op hoeveelheid

Gebruik de volgende formule om de correcte waarde voor de Maximale Korting van de Aantal te bepalen:

Formule = `(X+Y) * (M/Y)`
Wanneer
`X` = aantal gekochte artikelen
`Y` = aantal gratis objecten
`M` = Maximaal aantal gratis objecten toegestaan

Bijvoorbeeld:

Koop vijf en krijg twee gratis objecten met maximaal vier gratis objecten toegestaan.

    Wanneer
    X = 5
    Y = 2
    M = 4
    Maximale korting op de hoeveelheid = (5+2)*(4/2)=(7)*(2)=14

Koop vijf en krijg drie gratis objecten met maximaal negen gratis objecten toegestaan.

    Wanneer
    X = 5
    Y = 3
    M = 9
    Maximale korting op de hoeveelheid = (5+3)*(9/3)=24

Koop 20 en ontvang twee gratis objecten met maximaal 20 gratis objecten toegestaan.

    Wanneer
    X = 20
    Y = 2
    M = 20
    Maximale korting op de hoeveelheid = (20+2)*(20/2)=(22)*(10)=220
