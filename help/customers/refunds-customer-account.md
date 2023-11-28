---
title: Terugbetalingen op het dashboard voor de klantenaccount
description: Winkelklanten kunnen de terugbetalingsgegevens van de bestelling bekijken in hun accountdashboard.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Terugbetalingen op het dashboard voor de klantenaccount

{{ee-feature}}

Als een terugbetaling voor een bestelling is verleend, kunnen klanten de terugbetalingsinformatie die aan de orde in hun rekeningdashboard wordt geassocieerd bekijken. Als u de optie [!UICONTROL _Winkelcreditatiegeschiedenis aan klanten tonen_] optie voor [Winkelcrediteringsconfiguratie](../customers/credit-configure.md), kunnen klanten ook toegang krijgen tot [Winkelkrediet](../customers/store-credit.md) geschiedenis.

## Restitutie bekijken op de winkel

1. Vanaf de storefront meldt de klant zich aan bij zijn account.

1. Hiermee zoekt u de volgorde op een van de volgende manieren:

   * De volgorde zoeken in de lijst met **Recente bestellingen** en klikken **[!UICONTROL View]**.
   * Kies in het linkerdeelvenster de optie **[!UICONTROL My Orders]**. Zoek vervolgens de volgorde in de lijst en klik op **[!UICONTROL View]**.

1. De klant klikt op de knop **[!UICONTROL Refunds]** om de details van de restitutie te bekijken.

   ![Restitutiedetails on the storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Het creditsaldo en de geschiedenis van de winkel weergeven

Methode 1: **Van het dashboard van de klantenrekening**

1. Van de opslag, logt de klant aan rekening binnen.

1. Als de restitutie is toegepast voor de opslag van krediet, kiest u **[!UICONTROL Store Credit]** in het linkerdeelvenster.

1. Het bedrag dat aan hun winkelkrediet wordt terugbetaald verschijnt in de lijst met de datum en de tijd van de actie.

   ![Bedrag dat is terugbetaald om krediet op te slaan](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >De pagina Winkelcreditering bevat ook een koppeling waarmee de klant een [cadeaukaart](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Methode 2: **Van de _Reviseren en betalen_ page**

1. De klant voegt een product toe aan het winkelwagentje.

2. Verwerkt naar de _Afhandeling_ pagina.

3. Hiermee geeft u de **[!UICONTROL Shipping]** stap.

4. Als opslagkrediet beschikbaar is, klikt de klant **[!UICONTROL Use Store Credit]**.

   ![Creditering opslaan op de pagina Bekijken en betalen](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Als de klant van mening verandert over het gebruik van het winkelkrediet, klikt u **[!UICONTROL Remove]** in de _Overzicht van bestellingen_ sectie.

## Betalingsacties in de beheerder

U kunt betalingsacties configureren voor uw specifieke [Betalingsmethode](../configuration-reference/sales/payment-methods.md). Elke betalingsmethode heeft een andere reeks betalingsacties.

| Betalingsactie | Beschrijving |
|--- |---|
| [!UICONTROL Capture Online] | Wanneer de factuur wordt verzonden, vangt het systeem de betaling van de betalingsgateway van de derde. Een Admin-gebruiker kan vervolgens een creditnota maken en de factuur annuleren. |
| [!UICONTROL Capture Offline] | Wanneer de factuur wordt ingediend, wordt de betaling niet in het systeem opgenomen. Aangenomen wordt dat de betaling rechtstreeks via de gateway wordt vastgelegd en de betaling niet via Adobe Commerce kan worden vastgelegd. Een Admin-gebruiker kan vervolgens een creditnota maken, maar de factuur kan niet worden geannuleerd. (Hoewel de bestelling een online betaling gebruikte, is de factuur in wezen een offline factuur.) |
| [!UICONTROL Not Capture] | Wanneer de factuur wordt ingediend, wordt de betaling niet in het systeem opgenomen. Aangenomen wordt dat de betaling later via Adobe Commerce wordt vastgelegd. Er is een [!UICONTROL _Vastleggen_] in de ingevulde factuur. Voordat u gaat vastleggen, kunt u de factuur annuleren. Na het vastleggen kunt u een creditmemo maken en de factuur annuleren. |

{style="table-layout:auto"}

>[!WARNING]
>
>Selecteer de [!UICONTROL _Niet vastleggen_] tenzij u zeker weet dat u de betaling later via Adobe Commerce gaat vastleggen. U kunt pas een creditmemo maken nadat de betaling is vastgelegd met de [!UICONTROL _Vastleggen_] knop.
