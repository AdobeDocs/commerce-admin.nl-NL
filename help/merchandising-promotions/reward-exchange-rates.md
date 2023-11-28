---
title: Wisselkoersen
description: Leer hoe u de bonuswisselkoersen instelt die het aantal beloningspunten bepalen dat wordt verdiend.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Wisselkoersen

{{ee-feature}}

Wisselkoersen met terugwerkende kracht bepalen het aantal punten dat wordt verdiend op basis van het orderbedrag en de waarde van de verdiende punten. Verschillende wisselkoersen kunnen worden toegepast op verschillende websites en verschillende klantengroepen. Als meerdere wisselkoersen van verschillende websites en klantgroepen van toepassing zijn op dezelfde klant, gelden de volgende prioriteitsregels:

## Wisselkoersprioriteit

**1**: Van toepassing op specifieke website en specifieke klantengroep.

**2**: Van toepassing op alle websites en een specifieke klantengroep.

**3**: van toepassing op een specifieke website en alle klantengroepen.

**4**: van toepassing op alle websites en alle klantengroepen.

Bij het omzetten van een valuta in punten kan het aantal punten niet worden gedeeld. De rest van de valuta wordt naar beneden afgerond. Als $2.00 bijvoorbeeld wordt omgezet in tien punten, worden punten verdiend in groepen van $2.00. Daarom zou een orde $7.00 30 punten verdienen, en de resterende $1.00 zou naar beneden worden afgerond. Het geldelijke bedrag van de order wordt gedefinieerd als het bedrag dat de handelaar ontvangt, of het totaal-generaal minus verzendkosten, belastingen, kortingen, winkelkredieten en cadeaukaarten. De punten worden verdiend op het moment dat er geen niet-gefactureerde items in de bestelling staan (alle items worden betaald of geannuleerd). Als een Admin-gebruiker klanten niet wil toestaan om Punten terug te verdienen voor geannuleerde bestellingen, kunnen deze punten handmatig van de pagina Manage Customers worden afgetrokken.

## Wisselkoersen instellen

![Wisselkoersen](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Rate]**.

1. In de **[!UICONTROL Reward Exchange Rate Information]** Ga als volgt te werk:

   ![Wisselkoersen met wederinkoopverplichting - informatie](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Website]** op de plaatsen waar de wisselkoers van toepassing is.

   - Set **[!UICONTROL Customer Group]** voor de groepen waarvoor de wisselkoers geldt.

   - Set **[!UICONTROL Direction]** op een van de volgende wijzen:

      - `Points to Currency`
      - `Currency to Points`

   Bij elke instelling voor Richting wordt het bedrag weergegeven in de basisvaluta van de website.

1. Voer de **[!UICONTROL Rate]** waarden volgens de _[!UICONTROL Direction]_instellen.

   | Richting | Snelheidinstellingen |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | In het eerste _[!UICONTROL Rate]_voert u het aantal punten in. In de tweede_[!UICONTROL Rate]_ Voer de monetaire waarde van de punten in. |
   | [!UICONTROL Currency to Points] | In het eerste  _[!UICONTROL Rate]_Voer de monetaire waarde in. In de tweede_[!UICONTROL Rate]_ Voer het aantal punten in dat door de monetaire waarde wordt vertegenwoordigd. |

   Bij de conversie van punten naar valuta kan het aantal punten niet worden gedeeld. Als tien punten bijvoorbeeld worden omgezet in $2,00, moeten punten worden ingewisseld in groepen van tien. Daarom zouden 25 punten worden terugbetaald voor $4,00, waarbij 5 punten in het saldo van de klant overblijven.

   Het wordt aanbevolen een conversie in te stellen voor beide `Points to Currency` en `Currency to Points`.

1. Klik op **[!UICONTROL Save]**.

## Een omrekeningskoers verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Zoek de wisselkoers die moet worden verwijderd en open deze in de bewerkingsmodus.

1. Klik in de menubalk op **[!UICONTROL Delete]**.

1. Klik op **[!UICONTROL OK]**.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Website] | De websites waarop de bonustarieven van toepassing zijn. |
| [!UICONTROL Customer Group] | De klantengroepen waarop de beloningsrente van toepassing is. |
| [!UICONTROL Direction] | Bepaalt welk type transactie de wisselkoers bepaalt. Opties: <br/>**[!UICONTROL Points to Currency]**- Definieert het aantal punten dat als krediet op het bedrag van een bestelling kan worden toegepast. In het eerste _[!UICONTROL Rate]_voert u het aantal punten in. In de tweede_[!UICONTROL Rate]_ Voer de monetaire waarde van de punten in.<br/>**[!UICONTROL Currency to Points]** - Hiermee bepaalt u het bedrag van een bestelling dat de punten van de klant kan verdienen. In het eerste  _[!UICONTROL Rate]_Voer de monetaire waarde in. In de tweede_[!UICONTROL Rate]_ Voer het aantal punten in dat door de monetaire waarde wordt vertegenwoordigd. |
