---
title: Storefront-orderbeheer
description: Leer hoe klanten hun ordergeschiedenis op de Commerce-winkel kunnen bekijken en beheren.
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

Uw initiële _[!UICONTROL My Orders]_resultaten bevatten ook overeenkomende opdrachten van ondergeschikte gebruikers van alle websites in de instantie commerce. Een klant die aan een bedrijfrekening wordt geassocieerd kan de orderlijst filtreren om verslagen binnen de resultaten snel te vinden. Om de filteropties te tonen, klikt de klant **[!UICONTROL Filter]**, en klikt **[!UICONTROL Close]**om de filters te verbergen.

![ Mijn Orden ](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

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

Een klant zoekt de volgorde in de lijst en klikt op **[!UICONTROL View Order]** . Vanuit de open volgorde kunnen ze een van de volgende handelingen uitvoeren:

![ de Orde van de Mening ](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Onlangs bestelde producten weergeven

Het blok **[!UICONTROL Recent Orders]** wordt weergegeven op de zijbalk en op de pagina **[!UICONTROL My Account]** voor klanten die zich na het plaatsen van een bestelling hebben aangemeld. Er worden vijf producten weergegeven vanaf de laatste aankoop.

De klant kan producten aan de kar lezen door de producten te selecteren en **[!UICONTROL Add to Cart]** te klikken. Ze kunnen ook de laatste volgorde weergeven door op **[!UICONTROL View all]** te klikken. Hiermee wordt doorgegaan naar de pagina _[!UICONTROL My Account]_en het blok **[!UICONTROL Recent Orders]**.

### Afdrukvolgorde

1. De klant klikt op **[!UICONTROL Print Order]** .

1. Volg de instructies in het dialoogvenster Afdrukken om het afdrukken te voltooien.

### Facturen afdrukken

1. Op het tabblad **[!UICONTROL Invoices]** klikt de klant op een van de volgende opties:

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![ Facturen ](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Gebruikt het dialoogvenster Afdrukken om het afdrukken te voltooien.

### Afdrukken

1. Op het tabblad **[!UICONTROL Order Shipments]** klikt de klant op een van de volgende opties:

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![ Druk Alle Verzendingen ](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Gebruikt het dialoogvenster Afdrukken om het afdrukken te voltooien.

### Een verzending volgen

1. Klik op het tabblad **[!UICONTROL Order Shipments]** op **[!UICONTROL Track this Shipment]** .

   Alle beschikbare trackinggegevens worden weergegeven in een pop-upvenster.

1. Wanneer deze gereed is, klikt de klant op **[!UICONTROL Close Window]** .

### Afdrukrestituties

1. Op **terugkeert** lusje terug, klikt de klant één van het volgende:

   - **Druk Alle Terugbetalingen**

   - **Terugbetaling van de Druk**

   ![ Terugbetalingen ](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Gebruikt het dialoogvenster Afdrukken om het afdrukken te voltooien.

Reorders zijn beschikbaar aan klanten wanneer [_toestaat opnieuw rangschikt_](reorders-allow.md) configuratieoptie wordt toegelaten.

Een klant kan de functionaliteit voor opnieuw ordenen voor een specifieke volgorde op twee pagina&#39;s starten:

- Pagina Mijn bestellingen
- Weergavepagina Volgorde

## Herschikkingen

De koppeling _[!UICONTROL Reorder]_wordt weergegeven in de lijst met bestellingen bij de koppeling_[!UICONTROL View]_ .

![ herordent verbinding op de Mijn pagina van de Orde ](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Geval 1.** Alle producten van de bestelling zijn beschikbaar voor herschikking

De klant wordt omgeleid naar het winkelwagentje en alle producten worden aan het winkelwagentje toegevoegd.

**Geval 2.** Sommige/alle producten van de bestelling zijn niet beschikbaar voor herschikking

>[!NOTE]
>
>Het is mogelijk om `Not Visible Individually` -producten opnieuw te ordenen.

De koppeling _[!UICONTROL Reorder]_wordt niet weergegeven op de pagina&#39;s_[!UICONTROL My Orders]_ en _[!UICONTROL View Order]_.

![ Mijn pagina van de Orde ](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Als het winkelwagentje niet leeg is en de klant op **[!UICONTROL Reorder]** klikt (vanaf de pagina [!UICONTROL My Orders] of [!UICONTROL Order View] ), blijven de bestaande producten in het winkelwagentje met de toegevoegde producten voor opnieuw ordenen.

## Bestellingen annuleren

Annuleren is beschikbaar aan klanten wanneer [_toestaat annuleer_](cancel-allow.md) configuratieoptie wordt toegelaten.

Een klant kan de functie voor annuleren voor een specifieke bestelling starten op drie pagina&#39;s:

- Pagina Mijn bestellingen
- Weergavepagina Volgorde
- Pagina Mijn account

De koppeling _[!UICONTROL Cancel Order]_wordt weergegeven bij de koppeling_[!UICONTROL Reorder]_ . Als de volgorde niet kan worden geannuleerd, wordt de koppeling niet weergegeven.

![ annuleert verbinding op de Mijn pagina van de Orde ](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

Om annuleren uit te voeren, annuleert de klant:

1. Klikken **[!UICONTROL Cancel Order]**

1. Verstrekt een annuleringsreden

   ![ annuleert orderedenen ](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   U kunt de annuleringsredenen op [_aanpassen toestaat annuleert_](cancel-allow.md) pagina.

1. Klikken **[!UICONTROL Confirm]**

   ![ annuleert op de Mijn pagina van de Orde ](./assets/cancel-order.png){width="700" zoomable="yes"}

   Na de annulering worden de bestellingen die de status _[!UICONTROL Pending]_hadden, gewijzigd in_[!UICONTROL Canceled]_ status, de bestellingen die de status _[!UICONTROL Processing]_hadden, gewijzigd in_[!UICONTROL Closed]_ status en terugbetaald.

   Wanneer de annulering is voltooid, wordt een e-mail verzonden naar de klant.

   ![ annuleer orde e-mail ](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   De annuleringsinformatie wordt toegevoegd aan de ordergeschiedenis van de klant. Deze wordt weergegeven in de notities bij de volgorde en op het tabblad Overzicht van opmerkingen.

   ![ annuleer ordentnota&#39;s ](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![ annuleer commentaargeschiedenis ](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   Als de bestelling om een of andere reden is gewijzigd in een status die niet kan worden geannuleerd en de klant de pagina niet heeft vernieuwd, wordt de koppeling om de bestelling te annuleren nog steeds weergegeven. Wanneer ze echter proberen te annuleren, wordt een foutbericht weergegeven.

   ![ annuleer het bericht van de ordefout ](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   Nadat u de pagina hebt vernieuwd, ziet u dat de volgorde al is voltooid. Daarom werkt de annulering niet.

   ![ annuleer orde na verfrissen ](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
