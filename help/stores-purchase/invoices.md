---
title: Facturen
description: Leer hoe u facturen maakt en afdrukt ter ondersteuning van bestelverwerking en klantenservice.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# Facturen

Een factuur is een overzicht van de betalingsgegevens van een bestelling. De veelvoudige facturen kunnen [ ](#create-an-invoice) voor één enkele orde worden gecreeerd, en elk kunnen zo vele of zo weinig van de gekochte producten omvatten die u specificeert. U kunt [ druk-klaar PDF facturen ](#print-invoices) als verkoopdocumenten voor uw klanten ook tot stand brengen.

Op _Admin_ sidebar, ga naar **[!UICONTROL Sales]** > _Verrichtingen_ > **Facturen** om het _8} net van Facturen {te openen en tot uw gecreeerde facturen toegang te hebben._

![ het net van Facturen ](./assets/invoices.png){width="700" zoomable="yes"}

## Kolombeschrijvingen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Schakel de selectievakjes in voor de aanhalingstekens die aan een handeling moeten worden onderworpen of gebruik het selectiegereedschap in de kolomkop. Opties: `Select All` / `Deselect All` |
| [!UICONTROL Invoice] | Een unieke numerieke id die wordt toegewezen wanneer een factuur wordt verzonden door de beheerder. Wanneer u de factuurdetails weergeeft, wordt dit nummer boven aan de pagina weergegeven in plaats van de naam van het citaat. |
| [!UICONTROL Invoice Date] | De datum en het tijdstip waarop de beheerder de factuur voor het eerst heeft verzonden. |
| [!UICONTROL Order#] | Een unieke numerieke id die wordt toegewezen wanneer een bestelling door een koper wordt geplaatst. Wanneer u de factuurgegevens weergeeft, wordt dit nummer als een koppeling weergegeven in het vak Order &amp; Account Information. |
| [!UICONTROL Order Date] | De datum en tijd waarop de klant een bestelling voor het eerst heeft geplaatst. |
| [!UICONTROL Bill-to Name] | De naam van de persoon die verantwoordelijk is voor de betaling van de beschikking. |
| [!UICONTROL Status] | Geeft de huidige status van een factuur aan. De status kan alleen worden gewijzigd door actie van de koper of de verkoper. |
| [!UICONTROL Grand Total (Base)] | De totale prijs van de te kopen producten. Het totale bedrag wordt weergegeven in de basisvaluta van de website en in de valuta van de opslagplaats. |
| [!UICONTROL Grand Total (purchase)] | Het totaal-generaal aan producten die in de bestelling zijn aangeschaft. Het totale bedrag wordt weergegeven in de basisvaluta van de website en in de valuta van de opslagplaats. |
| [!UICONTROL Purchased From] | De website/winkel/winkel-weergave waaruit de factuur is gemaakt. |
| [!UICONTROL Billing Address] | Het factureringsadres van de klant die de orde plaatste. |
| [!UICONTROL Shipping Address] | Het adres waar de bestelling moet worden verzonden. |
| [!UICONTROL Customer Name] | De voornaam en achternaam van de klant die de factuur ontvangt. |
| [!UICONTROL Email] | Het e-mailadres van de klant die de factuur ontvangt. |
| [!UICONTROL Customer Group] | De klantgroep die is toegewezen aan de klant die de factuur ontvangt. |
| [!UICONTROL Payment Method] | De wijze van betaling die voor de betaling moet worden gebruikt. |
| [!UICONTROL Shipping Information] | De methode die moet worden gebruikt om de bestelling te verzenden. |
| [!UICONTROL Subtotal] | Het subtotaal van de bestelling, zonder verzending en belasting. |
| [!UICONTROL Shipping and Handling] | Het bedrag dat in rekening wordt gebracht voor verzending. |
| [!UICONTROL Action] | **[!UICONTROL View]** - hiermee wordt de factuur geopend in de bewerkingsmodus. |

{style="table-layout:auto"}

## Een factuur maken

Als u een factuur voor een bestelling maakt, wordt deze verplaatst naar een staat waarin deze niet kan worden geannuleerd of gewijzigd. Een nieuwe factuurpagina ziet er ongeveer hetzelfde uit als een voltooide bestelling, met enkele extra velden. Elke activiteit die verband houdt met een bestelling wordt vermeld in de sectie Opmerkingen van de factuur.

Gewoonlijk worden bestellingen gefactureerd en vastgelegd wanneer het verzendproces start. Als de methode van betaling een kooporder is, of als de [ betalingsactie ](../configuration-reference/sales/payment-methods.md#payment-actions) aan `Authorize and Capture` wordt geplaatst, wordt de orde gefactureerd en de betaling wordt gevangen tijdens controle. U kunt een factuur genereren met een pakbon en ook verzendlabels afdrukken van uw transportaccount. Eén bestelling kan worden opgesplitst in gedeeltelijke overbrengingen, die indien nodig afzonderlijk worden gefactureerd.

Wanneer de staat van nieuwe orden aan `Processing` wordt geplaatst, wordt de optie _automatisch Alle Punten van de Factuur_ beschikbaar in de configuratie. Sommige methodes van de creditcardbetaling voltooien de het factureren stap als deel van het proces wanneer de [ betalingsactie ](../configuration-reference/sales/payment-methods.md#payment-actions) aan `Authorize and Capture` wordt geplaatst. In dat geval wordt de knop Factuur niet weergegeven en kan de bestelling worden verzonden.

>[!NOTE]
>
>Facturen worden niet automatisch gemaakt voor orders die worden geplaatst met `Gift Card` , `Store Credit` , `Reward Points` of andere methoden voor offlinebetalingen.

Er moet een factuur voor de bestelling worden gegenereerd voordat deze kan worden afgedrukt. Om de PDF te bekijken of te drukken, eerst download en installeer een lezer van de PDF zoals [ Adobe Acrobat Reader ][1].

**_om een orde te factureren:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Zoek de verkooporder met de status `Processing` in het raster. Voer vervolgens de volgende handelingen uit:

1. In de _kolom van de Actie_, klik **[!UICONTROL View]**.

1. Kies in de koptekst van de verkooporder de optie **[!UICONTROL Invoice]** .

   >[!NOTE]
   >
   >De _[!UICONTROL Invoice]_optie verschijnt niet wanneer de [ betalingsactie ](../configuration-reference/sales/payment-methods.md#payment-actions) voor uw specifieke [ betalingsmethode ](../configuration-reference/sales/payment-methods.md) aan `Authorize and Capture` wordt geplaatst, die auto-produceert een factuur. Dit is ook het geval als de bestelling wordt geplaatst en de betalingsactie voor uw betalingsmethode is ingesteld op `Authorize` en de bestelling wordt gefactureerd.

   ![ de Orde van de Verkoop van de Factuur ](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   De nieuwe factuurpagina ziet er ongeveer hetzelfde uit als een pagina met voltooide bestellingen, met extra velden die kunnen worden bewerkt.

1. Als de objecten klaar zijn om te worden verzonden, genereert u een pakbon voor de verzending op het moment dat u de factuur maakt:

   - In de _Verzendinformatie_ sectie, klik **[!UICONTROL Create Shipment]** checkbox om het te selecteren.

     De ladingslijst wordt gecreeerd tezelfdertijd dat de factuur wordt geproduceerd.

   - Een trackingnummer opnemen:

      - Klik op **[!UICONTROL Add Tracking Number]**.
      - Voer de volgende gegevens in: _[!UICONTROL Carrier]_,_[!UICONTROL Title]_ en _[!UICONTROL Number]_

     ![ creeer een verzending van de Verkoop ](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - U kunt desgewenst een gedeeltelijke factuur genereren:

      - In de _Punten aan de sectie van de Factuur_, werk de **[!UICONTROL Qty to Invoice]** kolom bij om slechts specifieke punten op de factuur te omvatten.
      - Klik vervolgens op **[!UICONTROL Update Qty's]** .

        ![ Punten aan Factuur ](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. Als een online betalingsmethode is gebruikt voor de bestelling, stelt u **[!UICONTROL Amount]** in op de juiste optie.

1. Ga als volgt te werk om klanten via e-mail op de hoogte te stellen wanneer de factuur wordt gegenereerd:

   - Schakel het selectievakje **[!UICONTROL Email Copy of Invoice]** in.

   - Voer een **[!UICONTROL Invoice Comments]** in. Als u de opmerkingen wilt opnemen in de e-mailmelding, schakelt u het selectievakje **[!UICONTROL Append Comments]** in.

1. Klik na afloop op **[!UICONTROL Submit Invoice]** onder aan de pagina.

   **_Online betalingsmethode:_**

   ![ leg Factuur - online betalingsmethode voor ](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_Offline betalingsmethode:_**

   ![ leg Factuur voor - off-line betalingsmethode) ](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   De status van de volgorde verandert van `Pending` in `Complete` .

   ![ Voltooide factuursamenvatting ](./assets/invoice-complete.png){width="600" zoomable="yes"}

## Facturen afdrukken

Facturen kunnen afzonderlijk of als een batch worden afgedrukt. Voordat een factuur kan worden afgedrukt, moet deze echter eerst voor de bestelling worden gegenereerd. U kunt een high-resolution embleem voor een druk-klaar PDF factuur uploaden, en [ identiteitskaart van de Orde ](../stores-purchase/sales-documents.md#add-reference-ids) in de kopbal omvatten. Om het factuurmalplaatje met uw embleem en adres aan te passen, zie {de Vereisten van het Logo van 0} PDF ](../stores-purchase/sales-documents.md#image-formats).[

>[!NOTE]
>
>Als u de PDF wilt weergeven of afdrukken, hebt u een PDF-lezer nodig. U kunt [ Adobe Reader ][1] zonder last downloaden.

### Eén factuur afdrukken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. In het _[!UICONTROL Invoices]_net, bepaal de plaats van de factuur en klik **[!UICONTROL View]**in de_ kolom van de Actie _.

1. Klik boven aan de factuur op **[!UICONTROL Print]** om een PDF van de factuur te genereren.

1. Sla de gegenereerde PDF op in een bestand of druk het af.

### Meerdere facturen afdrukken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Selecteer in het raster _[!UICONTROL Invoices]_het selectievakje voor elke factuur die u wilt afdrukken.

1. Stel het besturingselement **[!UICONTROL Actions]** in op `PDF Invoices` .

   ![ Druk veelvoudige facturen ](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

De facturen worden opgeslagen in één PDF-bestand dat naar een printer kan worden verzonden of dat kan worden opgeslagen.

## Bronnen voor probleemoplossing

Voor hulp bij het oplossen van problemenfactuurkwesties, zie de volgende _artikelen van de Kennisbank van de Steun van 0} Commerce:_

- [ kan geen de bundelproducten virtuele en eenvoudige ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-30889-magento-patch-can-t-invoice-bundle-products-virtual-and-simple.html) factureren
- [ Factuur zonder de informatie van de opslagkrediet ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31150-magento-patch-invoice-without-store-credit-info.html)
- [ Belasting verschijnt op factuur met 100% korting ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-22/mdva-35773-tax-appears-on-invoice-with-100-discount.html)
- [ de facturen van de Orde verzenden automatisch niet ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-13/mdva-32545-magento-patch-order-invoices-don-t-send-automatically.html)


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader ophalen"
