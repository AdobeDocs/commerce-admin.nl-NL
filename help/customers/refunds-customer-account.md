---
title: Terugbetalingen op het dashboard voor de klantenaccount
description: Winkelklanten kunnen de terugbetalingsgegevens van de bestelling bekijken in hun accountdashboard.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Terugbetalingen op het dashboard voor de klantenaccount

{{ee-feature}}

Als een terugbetaling voor een bestelling is verleend, kunnen klanten de terugbetalingsinformatie die aan de orde in hun rekeningdashboard wordt geassocieerd bekijken. Als u [!UICONTROL _de Geschiedenis van het Krediet van de Opslag aan Klanten_] optie voor [&#x200B; de configuratie van het Krediet van de Opslag &#x200B;](../customers/credit-configure.md) hebt toegelaten, kunnen de klanten tot hun [&#x200B; Krediet van de Opslag &#x200B;](../customers/store-credit.md) geschiedenis ook toegang hebben.

## Restitutie bekijken op de winkel

1. Vanaf de storefront meldt de klant zich aan bij zijn account.

1. Hiermee zoekt u de volgorde op een van de volgende manieren:

   * Het vinden van de orde in de lijst van **Recente Orden** en het klikken **[!UICONTROL View]**.
   * Kies **[!UICONTROL My Orders]** in het linkerdeelvenster. Zoek vervolgens de volgorde in de lijst en klik op **[!UICONTROL View]** .

1. De klant klikt op het tabblad **[!UICONTROL Refunds]** om de details van de terugbetaling weer te geven.

   ![&#x200B; detail van de Terugbetaling op de storefront &#x200B;](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Het creditsaldo en de geschiedenis van de winkel weergeven

Methode 1: **van het dashboard van de klantenrekening**

1. Van de opslag, logt de klant aan rekening binnen.

1. Als de restitutie is toegepast voor het opslaan van krediet, kiest u **[!UICONTROL Store Credit]** in het linkervenster.

1. Het bedrag dat aan hun winkelkrediet wordt terugbetaald verschijnt in de lijst met de datum en de tijd van de actie.

   ![&#x200B; Bedrag teruggegeven om krediet op te slaan &#x200B;](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >De pagina van het Krediet van de Opslag verstrekt ook een verbinding voor de klant om a [&#x200B; geschenkkaart &#x200B;](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card) in te wisselen.

Methode 2: **van de _Overzicht &amp; van Betalingen_ pagina**

1. De klant voegt een product toe aan het winkelwagentje.

2. Verwerkt aan de _Afhandelings_ pagina.

3. Geeft de stap **[!UICONTROL Shipping]** door.

4. Als opslagkrediet beschikbaar is, klikt de klant **[!UICONTROL Use Store Credit]**.

   ![&#x200B; Krediet van de Opslag van Overzicht &amp; van Betalingen pagina &#x200B;](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Als de klant hun mening over het gebruiken van de opslagkredieten verandert, klikt **[!UICONTROL Remove]** in de _Samenvatting van de Orde_ sectie.

## Betalingsacties in de beheerder

U kunt betalingsacties voor uw specifieke [&#x200B; Methode van de Betaling vormen &#x200B;](../configuration-reference/sales/payment-methods.md). Elke betalingsmethode heeft een andere reeks betalingsacties.

| Betalingsactie | Beschrijving |
|--- |---|
| [!UICONTROL Capture Online] | Wanneer de factuur wordt verzonden, vangt het systeem de betaling van de betalingsgateway van de derde. Een Admin-gebruiker kan vervolgens een creditnota maken en de factuur annuleren. |
| [!UICONTROL Capture Offline] | Wanneer de factuur wordt ingediend, wordt de betaling niet in het systeem opgenomen. Aangenomen wordt dat de betaling rechtstreeks via de gateway wordt vastgelegd en de betaling niet via Adobe Commerce kan worden vastgelegd. Een Admin-gebruiker kan vervolgens een creditnota maken, maar de factuur kan niet worden geannuleerd. (Hoewel de bestelling een online betaling gebruikte, is de factuur in wezen een offline factuur.) |
| [!UICONTROL Not Capture] | Wanneer de factuur wordt ingediend, wordt de betaling niet in het systeem opgenomen. Aangenomen wordt dat de betaling later via Adobe Commerce wordt vastgelegd. Er is a [!UICONTROL _vangt_] knoop in de voltooide factuur. Voordat u gaat vastleggen, kunt u de factuur annuleren. Na het vastleggen kunt u een creditmemo maken en de factuur annuleren. |

{style="table-layout:auto"}

>[!WARNING]
>
>Selecteer [!UICONTROL _niet vangen_] optie tenzij u zeker bent dat u de betaling door Adobe Commerce later zult vangen. U kunt geen creditnota tot stand brengen tot de betaling gebruikend [!UICONTROL _gevangen is gevangen Vangst_] knoop.
