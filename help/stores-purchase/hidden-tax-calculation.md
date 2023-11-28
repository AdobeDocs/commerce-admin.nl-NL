---
title: Verborgen belastingberekening
description: Leer hoe u een verborgen belastingberekening configureert wanneer er een korting is waarin belasting is ingesloten.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Verborgen belastingberekening

_Verborgen belasting_ is het btw-bedrag dat een disconteringsbedrag heeft. De waarde is niet gelijk aan nul wanneer aan al deze voorwaarden wordt voldaan:

- Catalogusprijzen inclusief belasting
- Het BTW-tarief is niet nul
- Er is een korting aanwezig

Wanneer er een korting is waarin belasting is ingebed, berekent de Handel een _verborgen belasting_ dat wordt opgeteld voor de berekening van de gedisconteerde prijs.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Voorbeeld

1. Volledige prijs van object, inclusief btw: $100
1. BTW op: 20%
1. Korting van 10% toegepast op objectprijs exclusief belastingen:

### Ongeldig verwacht resultaat

- Objectprijs na belasting zonder korting=100 USD
- Objectprijs vóór belasting zonder korting=100/1.2=83,33 USD
- Korting=83.33 \ *0.1=8.33 USD
- Tax=(83.33-8.33) \ *0.2=**15 USD (ongeldig)**
- Totaal van bestellingen exclusief belastingen=83.33-8.33=**75 USD (ongeldig)**
- Totaal van bestelling inclusief btw=75+15=**90 USD (ongeldig)**

### Geldig daadwerkelijk resultaat in winkelwagen

![Verborgen BTW-berekening in winkelwagen](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Geldige berekeningen

1. Volledige prijs van het object zonder belasting is: $100 / 1,2 = **$ 83,33**

1. Het BTW-bedrag op de volledige objectprijs is: $100 - $83,33 = $16,67

   _Kan ook worden berekend als: $100 \ * (1 - 1/1.2)._

1. Korting van 10% op $83,33 is: **$ 8,33** (als je geen korting op BTW toepast)

1. Korte prijs van object met belasting is: $100 - $8,33 = $91,67

   >[!NOTE]
   >
   >Deze vergelijking illustreert de perceptie van de klant van hoe de kortingen worden toegepast.

1. Korte prijs van het object zonder belasting is: $91,67 / 1,2 = $76,39

1. Het BTW-bedrag op de verlaagde prijs is: $ 91,67 - $ 76,39 = **$ 15,28 (geldig)**

   _Kan ook worden berekend als: $91,67 \ * (1 - 1/1.2)._

1. Verborgen belasting of _Belastingcompensatie voor korting_ is het verschil tussen het BTW-bedrag van de volledige prijs en de verlaagde prijs: $ 16,67 - $ 15,28 = **$ 1,39**

   _Een andere manier om ernaar te kijken: verborgen belasting is het BTW-bedrag dat binnen de korting van 8,33 dollar wordt gedragen: $8,33 \* (1 - 1/1.2)._

1. Hoe de klant gewoonlijk de gedisconteerde prijs (het Totaal van de Orde) begrijpt:

   _Volledige prijs van het object inclusief belastingen **minder**de korting: $100 - $8,33 = $91,67_

1. **Hoe de Handel de verdisconteerde prijs berekent** (zie eerder voor formule):

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
