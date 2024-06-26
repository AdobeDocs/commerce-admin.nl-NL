---
title: Storefront-orderbeheer
description: Leer hoe klanten hun ordergeschiedenis kunnen bekijken en beheren op de Commerce-winkel.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: c13a4b730ed70ed4829cc20b13c2723137dcbb3a
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Storefront-orderbeheer

Klanten hebben toegang tot al hun bestellingen via hun account. Bestellingen kunnen als nieuwe bestellingen worden weergegeven, gefilterd, bijgehouden en opnieuw worden verzonden. Afhankelijk van de status van de bestelling kunnen klanten hun bestellingen, facturen, verzendingen en terugbetalingsgegevens afdrukken.

## Filterorders

{{b2b-feature}}

Uw eerste _[!UICONTROL My Orders]_resultaten bevatten ook overeenkomende opdrachten van ondergeschikte gebruikers van alle websites in de instantie commerce. Een klant die aan een bedrijfrekening wordt geassocieerd kan de orderlijst filtreren om verslagen binnen de resultaten snel te vinden. Om de filteropties te tonen, klikt de klant **[!UICONTROL Filter]**en klikken **[!UICONTROL Close]**de filters verbergen.

![Mijn bestellingen](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| Filter | Beschrijving |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | Voer een SKU- of productnaam in. |
| [!UICONTROL Order Number] | Kan een geheel of gedeeltelijk ordernummer zijn. |
| [!UICONTROL Order Status] | Hiermee kiest u een waarde uit de vervolgkeuzelijst om te filteren op status. |
| [!UICONTROL Invoice Number] | Voer een volledig of gedeeltelijk factuurnummer in. |
| [!UICONTROL Order Date] | Hiermee stelt u een of beide datumvelden in die op de orderdatum moeten worden gefilterd. |
| [!UICONTROL Created by] | Hiermee filtert u de orders van het bedrijf door de maker van de order. |
| [!UICONTROL Order Total] | Hiermee stelt u de waarden min, max of beide in op filteren op totaal van volgorde. |

## Een bestelling weergeven

Een klant vindt de orde in de lijst en klikt **[!UICONTROL View Order]**. Vanuit de open volgorde kunnen ze een van de volgende handelingen uitvoeren:

![Volgorde weergeven](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Onlangs bestelde producten weergeven

De **[!UICONTROL Recent Orders]** blok wordt weergegeven in de zijbalk en op de **[!UICONTROL My Account]** pagina voor klanten die na het plaatsen van een bestelling zijn aangemeld. Er worden vijf producten weergegeven vanaf de laatste aankoop.

De klant kan producten aan de kar lezen door de producten te selecteren en te klikken **[!UICONTROL Add to Cart]**. Ze kunnen ook de laatste volgorde weergeven door op **[!UICONTROL View all]**, die wordt doorgestuurd naar de _[!UICONTROL My Account]_en de **[!UICONTROL Recent Orders]**blokkeren.

### Afdrukvolgorde

1. De klant klikt **[!UICONTROL Print Order]**.

1. Volg de instructies in het dialoogvenster Afdrukken om het afdrukken te voltooien.

### Facturen afdrukken

1. Op de **[!UICONTROL Invoices]** tabblad klikt de klant op een van de volgende opties:

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Facturen](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Gebruikt het dialoogvenster Afdrukken om het afdrukken te voltooien.

### Afdrukken

1. Op de **[!UICONTROL Order Shipments]** tabblad klikt de klant op een van de volgende opties:

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Alle verzendingen afdrukken](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Gebruikt het dialoogvenster Afdrukken om het afdrukken te voltooien.

### Een verzending volgen

1. Op de **[!UICONTROL Order Shipments]** tabblad, klikt u op **[!UICONTROL Track this Shipment]**.

   Alle beschikbare trackinggegevens worden weergegeven in een pop-upvenster.

1. Wanneer klaar, klikt de klant **[!UICONTROL Close Window]**.

### Afdrukrestituties

1. Op de **Restituties** tabblad klikt de klant op een van de volgende opties:

   - **Alle restituties afdrukken**

   - **Terugbetaling afdrukken**

   ![Restituties](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Gebruikt het dialoogvenster Afdrukken om het afdrukken te voltooien.

Herschikkingen zijn beschikbaar voor klanten wanneer de [_Opnieuw ordenen toestaan_](reorders-allow.md) configuratieoptie is ingeschakeld.

Een klant kan de functionaliteit voor opnieuw ordenen voor een specifieke volgorde op twee pagina&#39;s starten:

- Pagina Mijn bestellingen
- Weergavepagina Volgorde

## Herschikkingen

De _[!UICONTROL Reorder]_de verbinding wordt getoond in de lijst met orden dichtbij_[!UICONTROL View]_ koppeling.

![Koppeling opnieuw ordenen op de pagina Mijn bestelling](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Zaak 1.** Alle producten van de bestelling kunnen opnieuw worden geordend

De klant wordt omgeleid naar het winkelwagentje en alle producten worden aan het winkelwagentje toegevoegd.

**Zaak 2.** Enkele/alle producten van de bestelling zijn niet beschikbaar voor herschikking

>[!NOTE]
>
>Het is mogelijk de volgorde te wijzigen `Not Visible Individually` producten.

De _[!UICONTROL Reorder]_de koppeling wordt niet weergegeven op het tabblad_[!UICONTROL My Orders]_ en _[!UICONTROL View Order]_pagina&#39;s.

![Pagina Mijn bestelling](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Als het winkelwagentje niet leeg is en de klant klikt **[!UICONTROL Reorder]** (van de [!UICONTROL My Orders] of [!UICONTROL Order View] pagina), blijven de bestaande producten in het winkelwagentje met de toegevoegde producten van de herschikking.

## Bestellingen annuleren

Annuleren is beschikbaar voor klanten wanneer de [_Annuleren toestaan_](cancel-allow.md) configuratieoptie is ingeschakeld.

Een klant kan de functie voor annuleren voor een specifieke bestelling starten op drie pagina&#39;s:

- Pagina Mijn bestellingen
- Weergavepagina Volgorde
- Pagina Mijn account

De _[!UICONTROL Cancel Order]_de koppeling wordt weergegeven bij de_[!UICONTROL Reorder]_ koppeling. Als de volgorde niet kan worden geannuleerd, wordt de koppeling niet weergegeven.

![Koppeling op de pagina Mijn bestelling annuleren](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

Om annuleren uit te voeren, annuleert de klant:

1. Klikken **[!UICONTROL Cancel Order]**

1. Verstrekt een annuleringsreden

   ![Opdrachten annuleren](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   U kunt de annuleringsredenen aanpassen in het dialoogvenster [_Annuleren toestaan_](cancel-allow.md) pagina.

1. Klikken **[!UICONTROL Confirm]**

   ![Annuleren op de pagina Mijn bestelling](./assets/cancel-order.png){width="700" zoomable="yes"}

   Na de annulering waren de bestellingen in _[!UICONTROL Pending]_status, wijzigen in_[!UICONTROL Canceled]_ status, de bestellingen in _[!UICONTROL Processing]_status, wijzigen in_[!UICONTROL Closed]_ status en terugbetaling worden verwerkt.

   Wanneer de annulering is voltooid, wordt een e-mail verzonden naar de klant.

   ![E-mail bestellen annuleren](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   De annuleringsinformatie wordt toegevoegd aan de ordergeschiedenis van de klant. Deze wordt weergegeven in de notities bij de volgorde en op het tabblad Overzicht van opmerkingen.

   ![Bestelnotities annuleren](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![Opmerkingen annuleren](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   Als de bestelling om een of andere reden is gewijzigd in een status die niet kan worden geannuleerd en de klant de pagina niet heeft vernieuwd, wordt de koppeling om de bestelling te annuleren nog steeds weergegeven. Wanneer ze echter proberen te annuleren, wordt een foutbericht weergegeven.

   ![Foutbericht voor bestelling annuleren](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   Nadat u de pagina hebt vernieuwd, ziet u dat de volgorde al is voltooid. Daarom werkt de annulering niet.

   ![Bestelling annuleren na vernieuwen](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
