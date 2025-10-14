---
title: Verborgen belastingberekening
description: Leer hoe u een verborgen belastingberekening configureert wanneer er een korting is waarin belasting is ingesloten.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Verborgen belastingberekening

_Verborgen Belasting_ is het bedrag van BTW dat een kortingsbedrag heeft. De waarde is niet gelijk aan nul wanneer aan al deze voorwaarden wordt voldaan:

- Catalogusprijzen inclusief belasting
- Het BTW-tarief is niet nul
- Er is een korting aanwezig

Wanneer er een korting is die belasting ingebed in het heeft, berekent Commerce a _verborgen belasting_ die terug voor het berekenen van de verdisconteerde prijs wordt toegevoegd.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Voorbeeld

1. Volledige prijs van object, inclusief btw: $100
1. BTW op: 20%
1. Korting van 10% toegepast op objectprijs exclusief belastingen:

### Ongeldig verwacht resultaat

- Objectprijs na belasting zonder korting=100 USD
- Objectprijs vóór belasting zonder korting=100/1.2=83,33 USD
- Korting=83.33 \ *0.1=8.33 USD
- Tax= (83.33-8.33) \ *0.2= **15 USD (ongeldig)**
- De Totaal van de orde exclusief Tax=83.33-8.33= **75 USD (ongeldig)**
- Het Totaal van de orde met inbegrip van Tax=75+15= **90 USD (ongeldig)**

### Geldig daadwerkelijk resultaat in winkelwagen

![&#x200B; Verborgen Berekening van de Belastingbelasting in Kart &#x200B;](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Geldige berekeningen

1. Volledige prijs van het item zonder belasting is: $100 / 1.2 = **$83.33**

1. Het BTW-bedrag op de volledige objectprijs is: $100 - $83,33 = $16,67

   _kan ook als worden berekend: $100 \ * (1 - 1/1.2)._

1. Korting van 10% op $83.33 is: **$8.33** (wanneer u geen kortingsbelasting)

1. Korte prijs van object met belasting is: $100 - $8,33 = $91,67

   >[!NOTE]
   >
   >Deze vergelijking illustreert de perceptie van de klant van hoe de kortingen worden toegepast.

1. Korte prijs van het object zonder belasting is: $91,67 / 1,2 = $76,39

1. Het BTW-bedrag op de verlaagde prijs is: $91,67 - $76,39 = **$15.28 (geldig)**

   _kan ook als worden berekend: $91.67 \ * (1 - 1/1.2)._

1. De verborgen belasting of _Compensatie van de Belasting van de Korting_ is het verschil tussen het BTW bedrag van de volledige prijs tegenover disconteerde prijs: $16.67 - $15.28 = **$1.39**

   _een andere manier om het te bekijken: de verborgen belasting is het BTW bedrag dat binnen $8.33 korting wordt gedragen: $8.33 \* (1 - 1/1.2)._

1. Hoe de klant gewoonlijk de gedisconteerde prijs (het Totaal van de Orde) begrijpt:

   _Volledige prijs van punt met inbegrip van belastingen **minder**&#x200B;het disconteringsbedrag: $100 - $8.33 = $91.67_

1. **hoe Commerce de gedisconteerde prijs** berekent (zie vroeger voor formule):

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
