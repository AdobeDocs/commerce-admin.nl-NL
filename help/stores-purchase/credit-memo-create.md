---
title: Een creditmemo uitgeven
description: Leer hoe u een creditmemo voor een gefactureerde bestelling genereert en afdrukt.
exl-id: 84ec72ba-7f72-4fa1-a9bf-91c17f43a3a7
feature: Orders, Invoices
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2132'
ht-degree: 0%

---

# Een creditmemo uitgeven

Alvorens een creditmemo kan worden gedrukt, moet het eerst voor een [ gefactureerde orde ](invoices.md#create-an-invoice) worden geproduceerd. Afhankelijk van de betalingsmethode kunt u zowel online als offline terugbetalingen (gedeeltelijk of volledig) uitvoeren vanuit een open creditnota.

- ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Terugbetalingen kunnen worden toegepast om krediet op te slaan.
- ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) Terugbetalingen kan op bedrijfskrediet worden toegepast.
- Aankopen met een creditcard kunnen online of offline worden terugbetaald.
- Aankopen via cheque of postwissel moeten offline worden terugbetaald.

Om het even welk creditmemo met een [ open status ](order-status.md) heeft een opmerkelijke verschuldigde terugbetaling.

Met creditmemo&#39;s kunt u:

- Het volledige factuurbedrag terugbetalen.
- Een deel van een factuur terugbetalen.
- Meerdere gedeeltelijke factuurbedragen terugbetalen.
- Terugbetaling van meerdere facturen per bestelling, waarbij het totale orderbedrag niet mag worden overschreden.
- Een deel van de hoeveelheid voor één lijnitem terugbetalen, zoals drie van de vijf overhemden in een bestelling.

Zie [ een factuur ](invoices.md#create-an-invoice) voor meer informatie creëren.

## Instelling betalingsactie

Het terugbetalingswerkschema voor orden die door creditcard worden betaald wordt bepaald door [ het plaatsen van de Actie van de Betaling ](../configuration-reference/sales/payment-methods.md#payment-actions) in de configuratie voor elke beschikbare betalingsmethode. Terugbetalingen kunnen pas worden verricht nadat de transactie is afgewikkeld.

![ het plaatsen van de Actie van de Betaling ](./assets/payment-action-setting.png){width="600" zoomable="yes"}

- Als de betalingsactie voor de geconfigureerde betalingsmethode is ingesteld op `Authorize` , moet u eerst de factuur genereren via de beheerder voordat een creditcard kan worden gemaakt.
- Als de betalingsactie voor de geconfigureerde betalingsmethode is ingesteld op `Authorize and Capture`, is de factuur al gegenereerd door de betalingsprocessor, maar zijn de geldmiddelen pas beschikbaar wanneer de transactie is afgewikkeld. Deze korte wachttijd wordt door veel betalingsverwerkers als een beveiligingsmaatregel aanbevolen en kan doorgaans automatisch worden afgehandeld. Transacties kunnen ook handmatig worden afgewikkeld via uw zakelijke rekening bij de betalingsprocessor.
- ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) als u een creditnota voor een orde creeert die cadeauopties omvat, verschijnt de terugbetaling voor het cadeau verpakken en/of de gedrukte kaart in de sectie van de Totalen van de Terugbetaling van het creditmemo. Als u deze kosten wilt uitsluiten van het terug te betalen bedrag, voert u het bedrag in als een aanpassingsvergoeding. Als er meerdere creditnota&#39;s voor dezelfde bestelling worden uitgegeven, wordt de terugbetaling voor cadeauopties alleen in de eerste creditnota weergegeven.

## Een creditmemo maken

Bepaal het type van teruggave dat u wilt uitgeven-voor a [ kredietaankoop ](#issue-a-refund-for-a-credit-purchase) of voor [ controle of geldorde ](#issue-an-offline-refund-for-check-or-money-order)-en produceren het creditnota en geven een teruggave uit.

### Een terugbetaling voor een aankoop van een krediet uitgeven

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

   ![ het net van Orden ](./assets/orders-grid.png){width="700" zoomable="yes"}

1. Zoek de volgorde in het raster en klik op **[!UICONTROL View]** .

1. Als de knop _[!UICONTROL Credit Memo]_&#x200B;zichtbaar is in de knopbalk, voert u een van de volgende handelingen uit:

   - Ga naar stap 6 als u een `offline` restitutie wilt uitgeven.
   - Ga verder met stap 4 als u een `online` restitutie wilt uitgeven.

   Zie [ Memo&#39;s van het Krediet ](credit-memos.md) voor meer informatie over off-line en online terugbetalingen.

1. Klik op **[!UICONTROL Invoices]** in het linkerdeelvenster.

1. Zoek de factuur in het raster en klik op **[!UICONTROL View]** .

   ![ het net van Facturen ](./assets/order-invoices-grid.png){width="700" zoomable="yes"}

1. Blader omlaag naar de sectie **[!UICONTROL Invoice Totals]** van de factuur, controleer of de factuur is ingesteld op `Capture Online` en klik op **[!UICONTROL Submit Invoice]** .

   ![ Vangst online ](./assets/order-invoice-capture-online.png){width="600" zoomable="yes"}

   Als deze optie niet beschikbaar is, wordt de factuur al gemaakt. Ga verder met de volgende stap.

1. Klik op **[!UICONTROL Credit Memo]** in de knopbalk boven aan de factuur.

1. Controleer de gegevens in de sectie **[!UICONTROL Items to Refund]** en voer de volgende handelingen uit, indien van toepassing:

   - Schakel het selectievakje **[!UICONTROL Return to Stock]** in als u het product weer wilt inventariseren.

     Het product keert automatisch terug naar voorraad als _de Opties van de Voorraad van het Product_ aan `Automatically Return Credit Memo Item to Stock` wordt geplaatst. Met [ toegelaten Inventory management ](../inventory-management/enable.md), keert het punt aan de bron terug die de verzending verzond.

   - Werk **[!UICONTROL Qty to Refund]** bij en klik op **[!UICONTROL Update Qty's]** .

     ![ Punten aan Terugbetaling ](./assets/invoice-credit-memo-items-to-refund.png){width="600" zoomable="yes"}

1. Werk de sectie **[!UICONTROL Refunds Totals]** als volgt bij:

   - Voer voor **[!UICONTROL Refund Shipping]** een bedrag in dat moet worden terugbetaald van de verzendkosten.

     In dit veld wordt eerst het totale verzendbedrag weergegeven van de bestelling die kan worden terugbetaald. Het is gelijk aan het volledige verzendbedrag van de bestelling, na aftrek van het verzendbedrag dat al is terugbetaald. Net als de hoeveelheid kan de hoeveelheid worden verlaagd, maar niet worden verhoogd.

   - Voer voor **[!UICONTROL Adjustment Refund]** een waarde in die moet worden toegevoegd aan het totale bedrag dat wordt terugbetaald als een extra terugbetaling die niet van toepassing is op een bepaald deel van de bestelling (verzending, objecten of belasting). Deze kan ook worden gebruikt voor gedeeltelijke terugbetaling met virtueel geld, zoals een cadeaukaart, wanneer een beheerder eerst een niet-virtuele betalingsmethode wil terugbetalen.

     Het opgegeven bedrag kan de totale restitutie niet hoger doen uitkomen dan het betaalde bedrag.

   - Voer bij **[!UICONTROL Adjustment Fee]** een waarde in die van het totale terugbetaalde bedrag moet worden afgetrokken.

     Dit bedrag wordt niet afgetrokken van een specifiek gedeelte van de bestelling, zoals verzending, objecten of belasting.

1. Als u een opmerking wilt toevoegen, voert u de tekst in het vak **[!UICONTROL Credit Memo Comments]** in.

   - Als u een e-mailbericht naar de klant wilt verzenden, schakelt u het selectievakje **[!UICONTROL Email Copy of Credit Memo]** in.

1. Klik op **[!UICONTROL Update Totals]**.

1. Voer de volgende handelingen uit, indien van toepassing:

   - ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) om het bedrag aan het de opslagkrediet van de klant terug te betalen, selecteer **[!UICONTROL Refund to Store Credit]** checkbox.

   - ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) om het bedrag aan het bedrijfskrediet van de klant terug te betalen, selecteer **[!UICONTROL Refund to Company Credit]** checkbox.

   - Klik op **[!UICONTROL Refund Offline]** om een offline restitutie uit te geven.

   - Klik op **[!UICONTROL Refund]** om een onlinerestitutie uit te voeren.

   - ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) als de aankoop met bedrijfskrediet werd betaald, klik **[!UICONTROL Refund to Company Credit]**.

   Zie [ Memo&#39;s van het Krediet ](credit-memos.md) voor meer informatie over off-line en online terugbetalingen.

   ![ totale teruggave van de Orde ](./assets/credit-memo-order-total-refund.png){width="600" zoomable="yes"}

### Een offline terugbetaling voor cheque of postwissel afgeven

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de voltooide volgorde in het raster en open de volgorde door op de koppeling **[!UICONTROL View]** te klikken.

1. Klik op **[!UICONTROL Invoice]** in de knopbalk boven aan de pagina.

1. Schuif omlaag naar de onderkant van de pagina en klik op **[!UICONTROL Submit Invoice]** .

1. Klik op **[!UICONTROL Credit Memo]** in de knopbalk boven aan de factuur.

   ![ creeer creditmemo ](./assets/order-invoice-info-company.png){width="600" zoomable="yes"}

1. Controleer de gegevens in de sectie **[!UICONTROL Items to Refund]** en voer de volgende handelingen uit, indien van toepassing:

   ![ Punten aan Terugbetaling ](./assets/credit-memo-items-to-refund.png){width="600" zoomable="yes"}

   - Schakel het selectievakje **[!UICONTROL Return to Stock]** in als u het geretourneerde product wilt retourneren aan de voorraad.

     Als Inventory management is ingeschakeld, wordt de voorraadhoeveelheid geretourneerd naar de bron die de verzending heeft verzonden. Het product keert automatisch terug naar voorraad als [ de Opties van de Voorraad van het Product ](../inventory-management/enable.md) aan `Automatically Return Credit Memo Item to Stock` wordt geplaatst.

   - Werk **[!UICONTROL Qty to Refund]** bij en klik **[!UICONTROL Update Qty's]**.

     Het bedrag dat moet worden gecrediteerd, mag niet hoger zijn dan het maximumbedrag dat voor restitutie beschikbaar is.

1. Werk de sectie **[!UICONTROL Refunds Totals]** naar wens bij:

   - Voer voor **[!UICONTROL Refund Shipping]** een bedrag in dat moet worden terugbetaald van de verzendkosten.

     In dit veld wordt aanvankelijk het totale verzendbedrag weergegeven van de bestelling die kan worden terugbetaald. Het is gelijk aan het volledige verzendbedrag van de bestelling, na aftrek van het verzendbedrag dat al is terugbetaald. Net als de hoeveelheid kan de hoeveelheid worden verlaagd, maar niet worden verhoogd.

   - Voer voor **[!UICONTROL Adjustment Refund]** een waarde in die moet worden toegevoegd aan het totale bedrag dat wordt terugbetaald als een extra terugbetaling die niet van toepassing is op een bepaald deel van de bestelling (verzending, objecten of belasting). Deze kan ook worden gebruikt voor gedeeltelijke terugbetaling met virtueel geld, zoals een cadeaukaart, wanneer een beheerder eerst een niet-virtuele betalingsmethode wil terugbetalen.

     Het opgegeven bedrag kan de totale restitutie niet hoger doen uitkomen dan het betaalde bedrag.

   - Voer bij **[!UICONTROL Adjustment Fee]** een waarde in die van het totale terugbetaalde bedrag moet worden afgetrokken.

     Dit bedrag wordt niet afgetrokken van een specifiek gedeelte van de bestelling, zoals verzending, objecten of belasting.

   - Als de aankoop is betaald met winkelkrediet, schakelt u het selectievakje **[!UICONTROL Refund to Store Credit]** in om het bedrag te crediteren naar het saldo van de klantenrekening.

1. Als u een opmerking wilt toevoegen, voert u de tekst in het vak **[!UICONTROL Credit Memo Comments]** in en voert u de volgende handelingen uit:

   - Als u een e-mailbericht naar de klant wilt verzenden, schakelt u het selectievakje **[!UICONTROL Email Copy of Credit Memo]** in.

   - Schakel het selectievakje **[!UICONTROL Append Comments]** in om de opmerkingen die u in de e-mail hebt ingevoerd, op te nemen.

     De status van een kennisgeving van een creditnota wordt weergegeven in de voltooide creditnota naast het nummer van de creditnota.

     ![ Terugbetaalde Totalen ](./assets/credit-memo-order-totals.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Refund Offline]** om het proces te voltooien en de restitutie uit te geven.

## Veldomschrijvingen

### [!UICONTROL Order & Account Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Order Number] | Het orderaantal verschijnt in de _Orde &amp; Informatie van de Rekening_, die door een nota wordt gevolgd die erop wijst als bevestigingse-mail werd verzonden. |
| [!UICONTROL Order Date] | De datum en tijd waarop de bestelling is geplaatst. |
| [!UICONTROL Order Status] | Geeft de orderstatus aan als `Complete` . |
| [!UICONTROL Purchased From] | Geeft de website-, opslag- en opslagweergave aan waarin de volgorde is geplaatst. |
| [!UICONTROL Placed from IP] | Wijst op het IP adres van de computer waarvan de orde werd geplaatst. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Customer Name] | De naam van de klant of koper die de bestelling heeft geplaatst. De naam van de klant is gekoppeld aan het profiel van de klant. |
| [!UICONTROL Email] | Het e-mailadres van de klant of koper. Het e-mailadres is gekoppeld aan een nieuw e-mailbericht. |
| [!UICONTROL Customer Group] | De naam van de klantengroep of gedeelde catalogus waaraan de klant is toegewezen. |
| [!UICONTROL Company Name] | ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) De naam van het bedrijf verbonden aan de koper, en namens wie de orde wordt geplaatst. De bedrijfsnaam is gekoppeld aan het bedrijfsprofiel. |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Billing Address] | De naam van de klant of de koper die de orde plaatste, die door het het factureren adres, telefoonnummer, en [ BTW ](vat.md) wordt gevolgd, als toepasselijk. Het telefoonnummer is gekoppeld aan een autowijzerplaat op een mobiel apparaat. |
| [!UICONTROL Shipping Address] | De naam van de persoon onder wiens aandacht de bestelling moet worden verzonden, gevolgd door het verzendadres en telefoonnummer. Het telefoonnummer is gekoppeld aan een autowijzerplaat op een mobiel apparaat. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Payment Information] | De wijze van betaling die voor de order moet worden gebruikt, en het inkoopordernummer, indien van toepassing, gevolgd door de valuta die voor de order is gebruikt. Als de orde aan bedrijfskrediet gebruikend [ Betaling op Rekening ](../b2b/enable-basic-features.md#configure-payment-on-account) in rekening wordt gebracht, wordt het bedrag dat aan de rekening in rekening wordt gebracht vermeld. |
| [!UICONTROL Shipping & Handling Information] | De te gebruiken verzendmethode en eventuele verpakkingskosten. |

{style="table-layout:auto"}

### [!UICONTROL Items to Refund]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Product] | De productnaam, SKU en opties (indien van toepassing). |
| [!UICONTROL Price] | De aankoopprijs van het object. Voor Adobe Commerce B2B geeft deze waarde eventuele kortingen weer die op het item uit de gedeelde catalogus zijn toegepast, indien van toepassing. |
| [!UICONTROL Qty] | De bestelde hoeveelheid. |
| [!UICONTROL Return to Stock] | Selectievakje dat aangeeft of het geretourneerde item moet worden geretourneerd naar voorraad. |
| [!UICONTROL Qty to Refund] | Geeft het aantal geretourneerde eenheden van het product aan. |
| [!UICONTROL Subtotal] | Het subtotaal is de aankoopprijs vermenigvuldigd met de hoeveelheid geretourneerde producteenheden. |
| [!UICONTROL Tax Amount] | Het bedrag aan belasting dat op het teruggekeerde punt als decimale waarde van toepassing is. |
| [!UICONTROL Tax Percent] | Het percentage aan belasting dat op het geretourneerde object wordt toegepast als een percentage. |
| [!UICONTROL Discount Amount] | Alle kortingen die van toepassing zijn op het geretourneerde object. |
| [!UICONTROL Row Total] | Het totaal van de posten, inclusief toepasselijke belastingen die verschuldigd zijn voor het niveau van het geretourneerde product, minus kortingen. |
| _orde totaal_ |  |

{style="table-layout:auto"}

### [!UICONTROL Credit Memo Comments]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Comment Text] | Een tekstvak dat wordt gebruikt om een opmerking over het creditmemo aan de klant toe te voegen. |

{style="table-layout:auto"}

### [!UICONTROL Refund Totals]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Refund Shipping] | Het verzendbedrag dat moet worden terugbetaald. |
| [!UICONTROL Adjustment Refund] | Een bedrag dat wordt toegevoegd aan het totale bedrag dat wordt terugbetaald als een extra terugbetaling die niet van toepassing is op een bepaald deel van de bestelling, zoals verzending, objecten of belasting. Het ingevoerde bedrag kan de totale restitutie niet hoger doen uitkomen dan het betaalde bedrag. |
| [!UICONTROL Adjustment Fee] | Een bedrag dat wordt afgetrokken van het totale terugbetaalde bedrag, zoals een hervoorraadkosten, of een bedrag dat verband houdt met cadeauverpakking of cadeauopties. |
| [!UICONTROL Grand Total] | Totaal terug te betalen bedrag |
| [!UICONTROL Append Comments] | Selectievakje dat bepaalt of opmerkingen in de creditnota worden opgenomen. |
| [!UICONTROL Email Copy of Credit Memo] | Selectievakje dat bepaalt of een kopie van het creditmemo per e-mail wordt verzonden. |
| [!UICONTROL Refund to Store Credit] | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Checkbox die bepaalt als het totaal aan [ opslagkrediet ](../customers/store-credit-using.md) moet worden terugbetaald. |
| [!UICONTROL Subtotal] | ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) het totaal van alle lijnpunten die moeten worden terugbetaald. |

{style="table-layout:auto"}

### Terugbetalingsknoppen

De betalingsmethode die voor de bestelling wordt gebruikt, bepaalt de terugbetalingsknoppen die beschikbaar zijn voor een creditnota.

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Refund]** | Als de oorspronkelijke aankoop via een creditcard is betaald via een betaalgateway, wordt het restitutiebedrag beheerd door de betalingsverwerker. Raadpleeg de documentatie van uw betalingsprovider voor informatie over het beheer van terugbetalingen. |
| **[!UICONTROL Refund Offline]** | Als de oorspronkelijke aankoop per cheque of postwissel is betaald, wordt de terugbetaling rechtstreeks aan de klant betaald door een cheque, cadeaukaart of contant geld uit te geven als u een baksteen- en mortierwinkel hebt. De creditnota dient als een overzicht van de offlinetransactie. |
| **[!UICONTROL Refund to Company Credit]** | ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) als de aankoop aan bedrijfskrediet in rekening werd gebracht, is de teruggave teruggekeerd aan de [ Rekening van het Bedrijf ](../b2b/credit-company.md). |

{style="table-layout:auto"}

## Een creditmemo afdrukken

Als u het ingevulde creditmemo wilt afdrukken of bekijken, moet er een PDF-lezer zijn geïnstalleerd. U kunt [ Adobe Reader ][1] zonder last downloaden.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Credit Memos]**.

1. Gebruik een van de volgende methoden om het creditmemo af te drukken:

### Methode 1: Huidige creditnota afdrukken

1. Open de creditnota in het raster.

1. Klik op **[!UICONTROL Print]**.

   ![ Druk het creditmemo ](./assets/credit-memo-print.png){width="600" zoomable="yes"}

### Methode 2: Meerdere creditnota&#39;s afdrukken

1. Schakel in de lijst het selectievakje in van elk creditmemo dat u wilt afdrukken.

1. Stel het besturingselement **[!UICONTROL Actions]** in op `PDF Credit Memos` en klik op **[!UICONTROL Submit]** .

   ![ Druk geselecteerde creditnota&#39;s ](./assets/credit-memos-print.png){width="600" zoomable="yes"} af

1. Voer een van de volgende handelingen uit wanneer u hierom wordt gevraagd:

   - Als u het document wilt opslaan, klikt u op **[!UICONTROL Save]** en volgt u de aanwijzingen om het bestand op uw computer op te slaan. Wanneer het downloaden is voltooid, opent u de PDF in Adobe Reader en drukt u het document af.

   - Klik op **[!UICONTROL Open]** om het document weer te geven. De gedrukte PDF creditnota wordt geopend in Adobe Reader. Vanaf hier kunt u het creditmemo afdrukken of opslaan op uw computer.


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader ophalen"
