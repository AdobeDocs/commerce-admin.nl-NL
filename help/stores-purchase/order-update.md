---
title: Een bestelling bijwerken
description: Leer hoe u de bestelling van een klant bijwerkt in Admin.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Een bestelling bijwerken

Wanneer u een klant helpt die een bestelling heeft geplaatst, moet u de status van de bestelling bepalen. De beschikbare opties voor een `Pending` -volgorde verschillen van de opties voor een `Processing` -volgorde. Voor meer informatie, zie [ Proces een orde ](order-processing.md).

## Bestellingen in behandeling

Nadat een klant een bestelling heeft geplaatst, maar voordat de betaling is ontvangen, is de bestelling in de status `Pending` . U kunt de volgorde bewerken, in de wachtstand zetten of volledig annuleren. De knopbalk van een bestelling in behandeling geeft een overzicht van de beschikbare handelingen voor een bestelling.

![ In afwachting van de Opties van de Orde ](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Als u wezenlijke delen van een orde wijzigt, wordt de originele orde geannuleerd en een nieuwe orde wordt geproduceerd. U kunt de facturering of het verzendadres echter wijzigen zonder een nieuwe bestelling te genereren.

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Hiermee gaat u terug naar de pagina Bestellingen zonder wijzigingen op te slaan. |
| **[!UICONTROL Login as Customer]** | Staat een admin gebruiker toe om klanten met hun orden bij te staan. |
| **[!UICONTROL Cancel]** | Annuleert de in behandeling zijnde bestelling. |
| **[!UICONTROL Send Email]** | Stuur een e-mail over de bestelling die in behandeling is naar de klant. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Wijzigt de status van de in behandeling zijnde bestelling in `On Hold` . Kies _[!UICONTROL Unhold]_als u de muisknop wilt loslaten. |
| **[!UICONTROL Invoice]** | Creeert een [ factuur ](invoices.md#create-an-invoice) van de hangende orde door de orde in een factuur om te zetten, en verandert de ordestatus in `processing`. |
| **[!UICONTROL Ship]** | Creeert a [ lading ](shipments.md#create-a-shipment) verslag voor de orde. |
| **[!UICONTROL Reorder]** | Hiermee maakt u een nieuwe volgorde in behandeling die een duplicaat is van de huidige volgorde in behandeling. |
| **[!UICONTROL Edit]** | Hiermee wordt een volgorde geopend die in behandeling is in de bewerkingsmodus. De Edit knoop is slechts beschikbaar voor hangende orden, of voor orden die op onderhandelde [ citaten ](../b2b/quotes.md) worden gebaseerd. |

{style="table-layout:auto"}

## Verwerkingsopdrachten

Een volgorde voert de status `Processing` in wanneer:

* De betaling voor een bestelling wordt ontvangen/vastgelegd en de factuur wordt gegenereerd—wanneer de betalingsactie op `Authorize and Capture` is ingesteld.
* Een ordertransactie is geautoriseerd, maar de betaling wordt nog niet vastgelegd—wanneer de betalingsactie is ingesteld op `Authorize` .

De [ configuratie van de betalingsactie ](../configuration-reference/sales/payment-methods.md#payment-actions) bepaalt welke ordeacties beschikbaar zijn nadat een orde wordt gecreeerd.

U kunt een bestelling van `Processing` niet ingrijpend wijzigen, maar u kunt wel het factuuradres en het verzendadres bewerken.

![ Opties van de Orde van de Verwerking ](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wanneer de betalingsactie van de betalingsmethode is ingesteld op `Authorize and Capture` , wordt automatisch een factuur gemaakt wanneer de klant een bestelling plaatst. In deze omstandigheid, kunt u middelen terugbetalen gebruikend a [ creditnota ](credit-memo-create.md), maar kan [ niet ](#cancel-a-pending-order) annuleren of [ nietig ](#void-a-processing-order) de orde.

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Hiermee gaat u terug naar de pagina Bestellingen zonder wijzigingen op te slaan. |
| **[!UICONTROL Send Email]** | Stuur een e-mail over de bestelling naar de klant. |
| **[!UICONTROL Void]** | [ Voids ](#void-a-processing-order) een ordetransactie, of een gedeeltelijke ordetransactie. |
| **[!UICONTROL Credit Memo]** | Initieert het proces om a [ creditnota ](credit-memo-create.md) tot stand te brengen. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Hiermee wijzigt u de status van de verkooporder in `On Hold` . Kies _[!UICONTROL Unhold]_om de greep op de verkooporder vrij te geven. |
| **[!UICONTROL Reorder]** | Hiermee maakt u een nieuwe volgorde in behandeling op basis van de huidige volgorde. |
| **[!UICONTROL Create Returns]** | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) initieert het proces aan [ terugkeer ](returns.md) één of meerdere punten van de orde. |

{style="table-layout:auto"}

## Void een verwerkingsopdracht uit

Wanneer een bestelling nog steeds de status `Processing` heeft en de integratie van de betaling is ingesteld op `Authorize` (niet `Authorize and Capture` ), kunt u alleen een transactie annuleren of een bestelling annuleren. [ het Kantelen van een orde ](#cancel-a-pending-order) verbiedt ook de vergunning.

Wanneer een bestelling wordt geplaatst met een betalingsmethode waarbij de betalingsactie is ingesteld op `Authorize and Capture` , kunt u de geldmiddelen via het creditcard terugbetalen, maar u kunt de bestelling niet annuleren omdat de bestelling wordt gefactureerd en de betaling wordt vastgelegd.

Je betalingsmethode bepaalt de beschikbare betalingsacties. Zie [ de acties van de Betaling ](../configuration-reference/sales/payment-methods.md#payment-actions) voor meer informatie.

**_om een orde te verwerpen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klik in de kolom **[!UICONTROL Action]** voor de volgorde die u wilt bewerken op **[!UICONTROL View]** .

1. Klik op **[!UICONTROL Void]** om de volgorde te wissen.

1. Klik op **[!UICONTROL OK]** als u hierom wordt gevraagd.

U kunt om het even welke noodzakelijke terugbetalingen uitgeven gebruikend a [ creditnota ](credit-memo-create.md) nadat de middelen zijn gevangen. U kunt a [ terugkeer ook tot handelsvergunning (RMA) ](returns.md) leiden die voor productwinst wordt uitgegeven. Meer leren, zie [ Verwerking een Orde ](order-processing.md).

## Een bestelling in behandeling bewerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klik in de kolom **[!UICONTROL Action]** voor de volgorde die u wilt bewerken op **[!UICONTROL View]** .

1. Klik op **[!UICONTROL Edit]**.

   ![ geef Orde ](./assets/order-edit.png){width="600" zoomable="yes"} uit

1. Klik op **[!UICONTROL OK]** als u wordt gevraagd door te gaan met bewerken.

1. Werk de volgorde naar wens bij.

1. Pas uw wijzigingen toe:
   * Klik op **[!UICONTROL Save]** als u de wijzigingen in het facturerings- of verzendadres wilt opslaan.
   * Klik op **[!UICONTROL Submit Order]** om de wijzigingen in lijnitems op te slaan en de volgorde opnieuw te verwerken.

## Een bestelling in de wachtstand zetten

Als de voorkeursmethode van de klant niet beschikbaar is of als het object tijdelijk buiten voorraad is, kunt u de bestelling in de wacht zetten.

1. In het _bevel_ net, vind de `Pending` orde die u op greep wilt plaatsen.

1. In de _kolom van de Actie_, klik **[!UICONTROL View]**.

1. Klik op **[!UICONTROL Hold]** om de volgorde in de wachtstand te zetten.

Als u de greep van een bestelling wilt verwijderen, bewerkt u de volgorde opnieuw en klikt u op **[!UICONTROL Unhold]** .

## Een lopende order annuleren

Als u een bestelling annuleert, wordt de status van de bestelling gewijzigd van `Pending` in `Canceled` .

1. Zoek in het _[!UICONTROL Orders]_-raster naar de volgorde die in behandeling is en die moet worden geannuleerd.

1. Klik in de kolom _[!UICONTROL Action]_op **[!UICONTROL View]**.

1. Klik op **[!UICONTROL Cancel]** om de bestelling te annuleren.

De status van de volgorde is nu `Canceled` .
