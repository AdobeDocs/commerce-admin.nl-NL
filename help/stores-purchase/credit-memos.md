---
title: Creditmemo's
description: Meer informatie over creditnota's en hoe deze worden gebruikt om een gedeeltelijke of volledige terugbetaling uit te geven.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Creditmemo&#39;s

A _creditnota_ is een document waarin het bedrag wordt weergegeven dat de klant verschuldigd is voor een volledige of gedeeltelijke terugbetaling. Het bedrag kan op een aankoop worden toegepast of aan de klant worden terugbetaald. U kunt een creditnota voor één enkele orde, of voor veelvoudige orden als partij drukken. Voordat een creditnota kan worden afgedrukt, moet deze eerst voor de bestelling worden gegenereerd. De _Creditnota&#39;s_ Deze pagina bevat een overzicht van de creditmemo&#39;s die aan klanten zijn uitgegeven.

![Creditnota&#39;s](./assets/credit-memos.png){width="700" zoomable="yes"}

## Restitutiemethode

De [betalingsmethode](payments.md) voor de volgorde bepaalt in zekere mate de methode waarmee u een bestelling terugbetaalt.

U kunt bestellingen op drie manieren terugbetalen:

- Creditering account - Betalingen met een creditrekening kunnen worden terugbetaald als een creditering van de rekening:
   - ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) [Winkelkrediet](../customers/store-credit-using.md)
   - ![B2B voor Adobe Commerce](../assets/b2b.svg) (Beschikbaar bij B2B voor Adobe Commerce) [Betaling op rekening](../b2b/enable-basic-features.md#configure-payment-on-account) (offlinemethode)
   - ![B2B voor Adobe Commerce](../assets/b2b.svg) (Beschikbaar bij B2B voor Adobe Commerce) [Bedrijfskrediet](../b2b/credit-company.md)
- [Online restitutie](payments.md#online-payment-methods)—Bestellingen die via een creditcard worden betaald via een betaalgateway, zoals PayPal of Braintree, worden online terugbetaald via de betalingsprocessor.
- [Offline restitutie](payments.md#offline-payment-methods)—Bestellingen die onder rembours worden betaald ([COD](cash-on-delivery.md)) of door [cheque of postwissel](check-money-order.md) worden offline terugbetaald.

U kunt voor elke betalingsmethode een offlinerestitutie of een creditering van de account (indien ingeschakeld) uitgeven.

Een bestelling die onder rembours is betaald ([COD](cash-on-delivery.md)) of door [cheque of postwissel](check-money-order.md) wordt offline terugbetaald.

## Terugbetalingsworkflow

1. **Betalingsactie** - Als de [Betalingsactie](credit-memo-create.md#payment-action-setting) configuratie is ingesteld op `Authorize`, moet u een factuur genereren voordat u een creditcard maakt. Ga verder met stap 2. Indien ingesteld op `Authorize and Capture`, er is al een factuur gegenereerd. Ga verder met stap 3.

1. **Factuur genereren** - [Een factuur maken](invoices.md#create-an-invoice) voor de bestelling, zodat u de klant een terugbetaling kunt sturen via creditnota.

1. **Creditnota maken** - [Een creditmemo uitgeven](credit-memo-create.md) in de Admin [kredietaankoop](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)of een [cheque of postwissel](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Kolombeschrijvingen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Schakel de selectievakjes in voor de onderdelen van het creditnota die aan een handeling moeten worden onderworpen, of gebruik het selectiegereedschap in de kolomkop. Opties: `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Een unieke numerieke id die wordt toegewezen wanneer een aanvraag voor een creditnota wordt ingediend. |
| [!UICONTROL Created] | De datum en het tijdstip waarop de koper de aanvraag voor een creditcard voor het eerst heeft ingediend. |
| [!UICONTROL Order#] | Order-id van de bestelling waarvan de producten worden geretourneerd. |
| [!UICONTROL Order Date] | De datum en het tijdstip waarop de koper een bestelling heeft geplaatst. |
| [!UICONTROL Bill-to Name] | De naam van de persoon die verantwoordelijk is voor de betaling van de beschikking. |
| [!UICONTROL Status] | Geeft de huidige status van een aanvraag voor een creditcard aan. |
| [!UICONTROL Refunded] | Het totale bedrag dat van de orde wordt terugbetaald. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Opent het verzoek om een creditnota en houdt een overzicht bij van de onderhandelingen tussen koper en verkoper. |
| [!UICONTROL Order Status] | Hiermee wordt de status van de volgorde aangegeven. |
| [!UICONTROL Purchased From] | Geeft de website-, opslag- en opslagweergave aan waarin de volgorde is geplaatst. |
| [!UICONTROL Billing Address] | Het factureringsadres van de klant die de orde plaatste. |
| [!UICONTROL Shipping Address] | Het adres waar de bestelling moet worden verzonden. |
| [!UICONTROL Customer Name] | De voornaam en achternaam van de klant die de bestelling heeft geplaatst. |
| [!UICONTROL Email] | Het e-mailadres van de persoon die de bestelling heeft geplaatst. |
| [!UICONTROL Customer Group] | De klantengroep waaraan de klant wordt toegewezen. |
| [!UICONTROL Payment Method] | De wijze van betaling die voor de betaling moet worden gebruikt. |
| [!UICONTROL Shipping Information] | De methode die moet worden gebruikt om de bestelling te verzenden. |
| [!UICONTROL Subtotal] | Het subtotaal van de bestelling, zonder verzending en belasting. |
| [!UICONTROL Shipping & Handling] | Het bedrag dat in rekening wordt gebracht voor verzending. |
| [!UICONTROL Adjustment Refund] | Het bedrag dat wordt opgeteld bij het totale bedrag dat wordt terugbetaald als extra restitutie. |
| [!UICONTROL Adjustment Fee] | Het bedrag dat wordt afgetrokken van het totale terugbetaalde bedrag. |
| [!UICONTROL Grand Total] | Het totaal van de bestelling. |

{style="table-layout:auto"}
