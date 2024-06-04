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

Voordat een creditmemo kan worden afgedrukt, moet deze eerst worden gegenereerd voor een [gefactureerde bestelling](invoices.md#create-an-invoice). Afhankelijk van de betalingsmethode kunt u zowel online als offline terugbetalingen (gedeeltelijk of volledig) uitvoeren vanuit een open creditnota.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Restituties kunnen worden toegepast voor winkelkrediet.
- ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar bij Adobe Commerce B2B) Restituties kunnen worden toegepast op bedrijfskrediet.
- Aankopen met een creditcard kunnen online of offline worden terugbetaald.
- Aankopen via cheque of postwissel moeten offline worden terugbetaald.

Elke creditnota met een [open status](order-status.md) heeft een te betalen terugbetaling.

Met creditmemo&#39;s kunt u:

- Het volledige factuurbedrag terugbetalen.
- Een deel van een factuur terugbetalen.
- Meerdere gedeeltelijke factuurbedragen terugbetalen.
- Terugbetaling van meerdere facturen per bestelling, waarbij het totale orderbedrag niet mag worden overschreden.
- Een deel van de hoeveelheid voor één lijnitem terugbetalen, zoals drie van de vijf overhemden in een bestelling.

Zie [Een factuur maken](invoices.md#create-an-invoice) voor meer informatie .

## Instelling betalingsactie

De terugbetalingsworkflow voor via creditcard betaalde orders wordt bepaald door [Instelling betalingsactie](../configuration-reference/sales/payment-methods.md#payment-actions) in de configuratie voor elke beschikbare betalingsmethode. Terugbetalingen kunnen pas worden verricht nadat de transactie is afgewikkeld.

![Instelling betalingsactie](./assets/payment-action-setting.png){width="600" zoomable="yes"}

- Als de betalingsactie voor de geconfigureerde betalingsmethode is ingesteld op `Authorize`, moet u eerst de factuur genereren van de beheerder voordat een creditnota kan worden gemaakt.
- Als Betalingsactie voor de geconfigureerde betalingsmethode is ingesteld op `Authorize and Capture`De factuur is al gegenereerd door de betalingsverwerker, maar de gelden zijn pas beschikbaar als de transactie is afgewikkeld. Deze korte wachttijd wordt door veel betalingsverwerkers als een beveiligingsmaatregel aanbevolen en kan doorgaans automatisch worden afgehandeld. Transacties kunnen ook handmatig worden afgewikkeld via uw zakelijke rekening bij de betalingsprocessor.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Als u een creditmemo maakt voor een bestelling die cadeauopties bevat, wordt de terugbetaling voor de cadeauverpakking en/of afgedrukte kaart weergegeven in het gedeelte Retoucheren van de creditcard. Als u deze kosten wilt uitsluiten van het terug te betalen bedrag, voert u het bedrag in als een aanpassingsvergoeding. Als er meerdere creditnota&#39;s voor dezelfde bestelling worden uitgegeven, wordt de terugbetaling voor cadeauopties alleen in de eerste creditnota weergegeven.

## Een creditmemo maken

Bepaal het type restitutie dat u wilt uitgeven—voor een [kredietaankoop](#issue-a-refund-for-a-credit-purchase) of voor [cheque of postwissel](#issue-an-offline-refund-for-check-or-money-order)—en genereren de creditnota en geven een terugbetaling af.

### Een terugbetaling voor een aankoop van een krediet uitgeven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

   ![Raster voor bestellingen](./assets/orders-grid.png){width="700" zoomable="yes"}

1. Zoek de volgorde in het raster en klik op **[!UICONTROL View]**.

1. Als de _[!UICONTROL Credit Memo]_in de knopbalk zichtbaar is, voert u een van de volgende handelingen uit:

   - Als u een `offline` restitutie, ga naar stap 6.
   - Als u een `online` restitutie, doorgaan met stap 4.

   Zie [Creditnota&#39;s](credit-memos.md) voor meer informatie over offline en online terugbetalingen.

1. Klikken **[!UICONTROL Invoices]** in het linkerdeelvenster.

1. Zoek de factuur in het raster en klik op **[!UICONTROL View]**.

   ![Raster facturen](./assets/order-invoices-grid.png){width="700" zoomable="yes"}

1. Omlaag schuiven naar de **[!UICONTROL Invoice Totals]** van de factuur, controleren of de factuur is ingesteld op `Capture Online`en klik op **[!UICONTROL Submit Invoice]**.

   ![Online vastleggen](./assets/order-invoice-capture-online.png){width="600" zoomable="yes"}

   Als deze optie niet beschikbaar is, wordt de factuur al gemaakt. Ga verder met de volgende stap.

1. Klik op de knopbalk boven aan de factuur op **[!UICONTROL Credit Memo]**.

1. Controleer de gegevens in het dialoogvenster **[!UICONTROL Items to Refund]** en doet het volgende, indien van toepassing:

   - Als u het product wilt terugbrengen naar de voorraad, selecteert u de **[!UICONTROL Return to Stock]** selectievakje.

     Als het product automatisch weer opslaat _Opties voor productvoorraad_ is ingesteld op `Automatically Return Credit Memo Item to Stock`. Met [Inventory management ingeschakeld](../inventory-management/enable.md), retourneert het item naar de bron die de verzending heeft verzonden.

   - Werk de **[!UICONTROL Qty to Refund]** en klik op **[!UICONTROL Update Qty's]**.

     ![Te restitueren objecten](./assets/invoice-credit-memo-items-to-refund.png){width="600" zoomable="yes"}

1. Werk de **[!UICONTROL Refunds Totals]** als volgt:

   - Voor **[!UICONTROL Refund Shipping]** Voer een bedrag in dat moet worden terugbetaald van de verzendkosten.

     In dit veld wordt eerst het totale verzendbedrag weergegeven van de bestelling die kan worden terugbetaald. Het is gelijk aan het volledige verzendbedrag van de bestelling, na aftrek van het verzendbedrag dat al is terugbetaald. Net als de hoeveelheid kan de hoeveelheid worden verlaagd, maar niet worden verhoogd.

   - Voor **[!UICONTROL Adjustment Refund]** Voer een waarde in die bij het totale terugbetaalde bedrag moet worden opgeteld als een extra terugbetaling die niet van toepassing is op een bepaald deel van de bestelling (verzending, objecten of belasting). Deze kan ook worden gebruikt voor gedeeltelijke terugbetaling met virtueel geld, zoals een cadeaukaart, wanneer een beheerder eerst een niet-virtuele betalingsmethode wil terugbetalen.

     Het opgegeven bedrag kan de totale restitutie niet hoger doen uitkomen dan het betaalde bedrag.

   - Voor **[!UICONTROL Adjustment Fee]** Voer een waarde in die van het totale terugbetaalde bedrag moet worden afgetrokken.

     Dit bedrag wordt niet afgetrokken van een specifiek gedeelte van de bestelling, zoals verzending, objecten of belasting.

1. Als u een opmerking wilt toevoegen, voert u de tekst in het dialoogvenster **[!UICONTROL Credit Memo Comments]** doos.

   - Als u een e-mailbericht naar de klant wilt verzenden, selecteert u de optie **[!UICONTROL Email Copy of Credit Memo]** selectievakje.

1. Klik op **[!UICONTROL Update Totals]**.

1. Voer de volgende handelingen uit, indien van toepassing:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Als u het bedrag wilt terugbetalen naar het winkelkrediet van de klant, selecteert u de optie **[!UICONTROL Refund to Store Credit]** selectievakje.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar bij Adobe Commerce B2B) Als u het bedrag wilt terugbetalen naar het bedrijfskrediet van de klant, selecteert u de optie **[!UICONTROL Refund to Company Credit]** selectievakje.

   - Klik op **[!UICONTROL Refund Offline]**.

   - Klik op **[!UICONTROL Refund]**.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar bij Adobe Commerce B2B) Klik op **[!UICONTROL Refund to Company Credit]**.

   Zie [Creditnota&#39;s](credit-memos.md) voor meer informatie over offline en online terugbetalingen.

   ![Totale restitutie bestellen](./assets/credit-memo-order-total-refund.png){width="600" zoomable="yes"}

### Een offline terugbetaling voor cheque of postwissel afgeven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. De voltooide volgorde in het raster zoeken en openen door op de knop **[!UICONTROL View]** koppeling.

1. Klik op de knopbalk boven aan de pagina op **[!UICONTROL Invoice]**.

1. Omlaag schuiven naar de onderkant van de pagina en klikken **[!UICONTROL Submit Invoice]**.

1. Klik op de knopbalk boven aan de factuur op **[!UICONTROL Credit Memo]**.

   ![Creditmemo maken](./assets/order-invoice-info-company.png){width="600" zoomable="yes"}

1. Controleer de gegevens in het dialoogvenster **[!UICONTROL Items to Refund]** en doet het volgende, indien van toepassing:

   ![Te restitueren objecten](./assets/credit-memo-items-to-refund.png){width="600" zoomable="yes"}

   - Selecteer de **[!UICONTROL Return to Stock]** Schakel het selectievakje in als u het geretourneerde product wilt terugbrengen naar de voorraad.

     Als Inventory management is ingeschakeld, wordt de voorraadhoeveelheid geretourneerd naar de bron die de verzending heeft verzonden. Als het product automatisch weer opslaat [Opties voor productvoorraad](../inventory-management/enable.md) is ingesteld op `Automatically Return Credit Memo Item to Stock`.

   - Werk de **[!UICONTROL Qty to Refund]** en klik op **[!UICONTROL Update Qty's]**.

     Het bedrag dat moet worden gecrediteerd, mag niet hoger zijn dan het maximumbedrag dat voor restitutie beschikbaar is.

1. Werk de **[!UICONTROL Refunds Totals]** in voorkomend geval:

   - Voor **[!UICONTROL Refund Shipping]** Voer een bedrag in dat moet worden terugbetaald van de verzendkosten.

     In dit veld wordt aanvankelijk het totale verzendbedrag weergegeven van de bestelling die kan worden terugbetaald. Het is gelijk aan het volledige verzendbedrag van de bestelling, na aftrek van het verzendbedrag dat al is terugbetaald. Net als de hoeveelheid kan de hoeveelheid worden verlaagd, maar niet worden verhoogd.

   - Voor **[!UICONTROL Adjustment Refund]** Voer een waarde in die bij het totale terugbetaalde bedrag moet worden opgeteld als een extra terugbetaling die niet van toepassing is op een bepaald deel van de bestelling (verzending, objecten of belasting). Deze kan ook worden gebruikt voor gedeeltelijke terugbetaling met virtueel geld, zoals een cadeaukaart, wanneer een beheerder eerst een niet-virtuele betalingsmethode wil terugbetalen.

     Het opgegeven bedrag kan de totale restitutie niet hoger doen uitkomen dan het betaalde bedrag.

   - Voor **[!UICONTROL Adjustment Fee]** Voer een waarde in die van het totale terugbetaalde bedrag moet worden afgetrokken.

     Dit bedrag wordt niet afgetrokken van een specifiek gedeelte van de bestelling, zoals verzending, objecten of belasting.

   - Als de aankoop is betaald met winkelkrediet, selecteert u de optie **[!UICONTROL Refund to Store Credit]** Schakel het selectievakje in om het bedrag te crediteren naar het saldo van de klantenrekening.

1. Als u een opmerking wilt toevoegen, voert u de tekst in het dialoogvenster **[!UICONTROL Credit Memo Comments]** en voer de volgende handelingen uit:

   - Als u een e-mailbericht naar de klant wilt verzenden, selecteert u de optie **[!UICONTROL Email Copy of Credit Memo]** selectievakje.

   - Als u de opmerkingen die u in de e-mail hebt ingevoerd, wilt opnemen, selecteert u de optie **[!UICONTROL Append Comments]** selectievakje.

     De status van een kennisgeving van een creditnota wordt weergegeven in de voltooide creditnota naast het nummer van de creditnota.

     ![Totaal terugbetalen](./assets/credit-memo-order-totals.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Refund Offline]**.

## Veldomschrijvingen

### [!UICONTROL Order & Account Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Order Number] | Het volgnummer wordt weergegeven in het dialoogvenster _Bestellen en accountgegevens_, gevolgd door een opmerking die aangeeft of het bevestigingsbericht is verzonden. |
| [!UICONTROL Order Date] | De datum en tijd waarop de bestelling is geplaatst. |
| [!UICONTROL Order Status] | Geeft de status van de volgorde aan als `Complete`. |
| [!UICONTROL Purchased From] | Geeft de website-, opslag- en opslagweergave aan waarin de volgorde is geplaatst. |
| [!UICONTROL Placed from IP] | Wijst op het IP adres van de computer waarvan de orde werd geplaatst. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Customer Name] | De naam van de klant of koper die de bestelling heeft geplaatst. De naam van de klant is gekoppeld aan het profiel van de klant. |
| [!UICONTROL Email] | Het e-mailadres van de klant of koper. Het e-mailadres is gekoppeld aan een nieuw e-mailbericht. |
| [!UICONTROL Customer Group] | De naam van de klantengroep of gedeelde catalogus waaraan de klant is toegewezen. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar bij Adobe Commerce B2B) De naam van de met de koper verbonden onderneming en namens wie de order wordt geplaatst. De bedrijfsnaam is gekoppeld aan het bedrijfsprofiel. |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Billing Address] | De naam van de klant of de koper die de bestelling heeft geplaatst, gevolgd door het factuuradres, het telefoonnummer en [BTW](vat.md), indien van toepassing. Het telefoonnummer is gekoppeld aan een autowijzerplaat op een mobiel apparaat. |
| [!UICONTROL Shipping Address] | De naam van de persoon onder wiens aandacht de bestelling moet worden verzonden, gevolgd door het verzendadres en telefoonnummer. Het telefoonnummer is gekoppeld aan een autowijzerplaat op een mobiel apparaat. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Payment Information] | De wijze van betaling die voor de order moet worden gebruikt, en het inkoopordernummer, indien van toepassing, gevolgd door de valuta die voor de order is gebruikt. Als het bedrijfskrediet van de bestelling wordt afgeschreven met behulp van [Betaling op rekening](../b2b/enable-basic-features.md#configure-payment-on-account), wordt het op de rekening in rekening gebrachte bedrag vermeld. |
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
| _ordertotaal_ |  |

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
| [!UICONTROL Refund to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Selectievakje dat bepaalt of het totaal moet worden terugbetaald [winkelkrediet](../customers/store-credit-using.md). |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar bij Adobe Commerce B2B) Het totaal van alle lijnitems die moeten worden terugbetaald. |

{style="table-layout:auto"}

### Terugbetalingsknoppen

De betalingsmethode die voor de bestelling wordt gebruikt, bepaalt de terugbetalingsknoppen die beschikbaar zijn voor een creditnota.

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Refund]** | Als de oorspronkelijke aankoop via een creditcard is betaald via een betaalgateway, wordt het restitutiebedrag beheerd door de betalingsverwerker. Raadpleeg de documentatie van uw betalingsprovider voor informatie over het beheer van terugbetalingen. |
| **[!UICONTROL Refund Offline]** | Als de oorspronkelijke aankoop per cheque of postwissel is betaald, wordt de terugbetaling rechtstreeks aan de klant betaald door een cheque, cadeaukaart of contant geld uit te geven als u een baksteen- en mortierwinkel hebt. De creditnota dient als een overzicht van de offlinetransactie. |
| **[!UICONTROL Refund to Company Credit]** | ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar bij Adobe Commerce B2B) Als de aankoop op bedrijfskrediet werd afgeschreven, wordt de terugbetaling aan de [Zakelijke account](../b2b/credit-company.md). |

{style="table-layout:auto"}

## Een creditmemo afdrukken

Als u het ingevulde creditmemo wilt afdrukken of bekijken, moet er een PDF-lezer zijn geïnstalleerd. U kunt downloaden [Adobe Reader][1] zonder kosten.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Credit Memos]**.

1. Gebruik een van de volgende methoden om het creditmemo af te drukken:

### Methode 1: Huidige creditnota afdrukken

1. Open de creditnota in het raster.

1. Klik op **[!UICONTROL Print]**.

   ![Het creditmemo afdrukken](./assets/credit-memo-print.png){width="600" zoomable="yes"}

### Methode 2: Meerdere creditnota&#39;s afdrukken

1. Schakel in de lijst het selectievakje in van elk creditmemo dat u wilt afdrukken.

1. Stel de **[!UICONTROL Actions]** controle op `PDF Credit Memos` en klik op **[!UICONTROL Submit]**.

   ![Geselecteerde creditmemo&#39;s afdrukken](./assets/credit-memos-print.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit wanneer u hierom wordt gevraagd:

   - Klik op **[!UICONTROL Save]** en volgt u de aanwijzingen om het bestand op uw computer op te slaan. Wanneer het downloaden is voltooid, opent u de PDF in Adobe Reader en drukt u het document af.

   - Klik op **[!UICONTROL Open]**. De gedrukte PDF creditnota wordt geopend in Adobe Reader. Vanaf hier kunt u het creditmemo afdrukken of opslaan op uw computer.


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader ophalen"
