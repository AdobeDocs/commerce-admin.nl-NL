---
title: Onderhandelingen over een offerte
description: Meer informatie over workflows voor prijsonderhandeling en over hoe u met kopers kunt werken voor aankopen.
exl-id: 93efbc9d-da4d-4ff8-95c1-13848b68bc38
feature: B2B, Quotes
source-git-commit: ec00288f33af2abb785d1b37dd67aaf1ebe35c06
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 0%

---

# Onderhandelingen over een offerte

Als [&#x200B; B2B de Citaten &#x200B;](configure-quotes.md) in de configuratie worden toegelaten, kan de prijsonderhandeling door een erkende koper van een bedrijf of een verkoopvertegenwoordiger worden in werking gesteld.

De kopers stellen het proces van de prijsonderhandeling door [&#x200B; in werking verzoekend om een citaat &#x200B;](quote-request.md) van het winkelwagentje. De Vertegenwoordigers van de verkoop kunnen onderhandeling door [&#x200B; in werking stellen creërend een ontwerp citaat voor een koper &#x200B;](sales-rep-initiates-quote.md), die het citaat met de aanvankelijke orde punten en de tarifering bijwerkt, en het verzenden naar de koper.

Wanneer de prijsonderhandeling begint, worden de citaten vermeld in het [&#x200B; Citaten &#x200B;](quotes.md) net. Alle onderhandelingen tussen de koper en de verkoper vinden plaats per e-mail en worden gestart en bijgehouden vanuit de gedetailleerde weergave van de prijsopgave.

Tijdens het onderhandelingsproces kan de verkoper het volgende doen via de beheerder:

- Producten toevoegen of verwijderen
- Het aantal wijzigen
- Een korting toepassen op regelitems of op het volledige aanhalingsteken
- Verzendmethode toevoegen of wijzigen
- Opmerkingen toevoegen
- De bijgewerkte prijsopgave naar de koper sturen of opslaan als concept

Kopers beheren het onderhandelingsproces voor aanhalingstekens vanuit de winkel met [[!UICONTROL My Quotes]](account-dashboard-my-quotes.md) . Hoewel het aanhalingsteken kan worden gecontroleerd, is de status op de account van de koper ingesteld op `Pending` . De koper kan de prijsopgave wijzigen en opnieuw verzenden, zelfs als deze is afgewezen of verlopen is.

## Stap 1: De aanvraag weergeven

1. Ga op de zijbalk Beheerder naar **[!UICONTROL Sales]** > **[!UICONTROL Quotes]** .

   De nieuwe aanvraag wordt weergegeven in het raster van _[!UICONTROL Quotes]_.

1. In de _kolom van Acties_, klik **[!UICONTROL View]**.

   ![&#x200B; Nieuwe Citaat &#x200B;](./assets/quote-grid-new.png){width="700" zoomable="yes"}

## Stap 2: Het aanhalingsteken wijzigen

1. Onder _[!UICONTROL Quote & Account Information]_, klik het_ Kalender _(![&#x200B; pictogram van de Kalender &#x200B;](../assets/icon-calendar.png)) pictogram.

   ![&#x200B; Citaat en rekeningsinformatie &#x200B;](./assets/quote-details-account-information.png){width="575" zoomable="yes"}

1. Kies een **[!UICONTROL Expiration Date]** voor de offerte.

1. Blader omlaag naar de sectie _[!UICONTROL Quote Totals]_&#x200B;en werk de **[!UICONTROL Negotiated Price]**&#x200B;zo nodig bij.

   ![&#x200B; Update Onderhandelde Prijs &#x200B;](./assets/quote-change-update-negotiated-price.png){width="600" zoomable="yes"}

   Als de koper de hoeveelheid in de prijsopgave vermelde items wijzigt, wordt boven aan de prijsopgave een bericht weergegeven waarin wordt aangegeven dat de lijst met artikelen is gewijzigd en dat de prijs van de overeenkomst moet worden bijgewerkt.

   ![&#x200B; Bericht van de Verandering van het Citaat &#x200B;](./assets/quote-change-notice.png){width="600" zoomable="yes"}

### Nieuwe producten aan de prijsopgave toevoegen

1. Klik op **[!UICONTROL Add Products by SKU]**.

1. Voer de **[!UICONTROL SKU]** en **[!UICONTROL Qty]** in die u wilt toevoegen.

   ![&#x200B; voeg aan Citaat door SKU &#x200B;](./assets/quote-details-add-by-sku.png){width="600" zoomable="yes"} toe

### Regelitemupdates toepassen

Pas indien nodig wijzigingen van regelitems toe in de sectie _[!UICONTROL Items Quoted]_.

![&#x200B; pas de updates van het lijnpunt toe &#x200B;](./assets/quote-apply-line-item-operations.png){width="600" zoomable="yes"}

- Wijzig de **[!UICONTROL Quantity]** die u voor de voorgestelde prijs moet kopen.

- Selecteer **[!UICONTROL Configure]** en wijzig de productopties.

  De optie [!UICONTROL Configure] is alleen beschikbaar op een regelitem voor een configureerbaar product

- Selecteer in het menu **[!UICONTROL Action]** een handeling om het item bij te werken:
   - **punt van de Korting** om een korting als percentage, vast bedrag, of aangewezen tarifering toe te passen.
U kunt desgewenst het kortingsbedrag vergrendelen om verdere kortingen te voorkomen. Als de korting niet vergrendeld is,
zowel de korting op het regelartikel als de korting op het prijsniveau worden toegepast op de productprijs.
   - **verlaat een nota aan koper** om de koper van extra informatie over een punt te voorzien
   - **verwijder** om een punt uit het citaat te verwijderen.

### Wijzigingen toepassen en bijwerken

- Klik op **[!UICONTROL Add to Quote]** om wijzigingen toe te passen.

- Klik op **[!UICONTROL Recalculate the Quote]** om het aanhalingsteken bij te werken.

- Als u de wijzigingen wilt toepassen en het aanhalingsteken wilt bijwerken naar de gedeelde catalogus en prijsregels, klikt u op **[!UICONTROL Update Prices]** en vervolgens op **[!UICONTROL Proceed]** om de update te bevestigen.

  ![&#x200B; Gepoteerde Punten &#x200B;](./assets/quote-detail-items-quoted.png){width="600" zoomable="yes"}

### Verzendgegevens bijwerken

1. Als de koper a _Verzenden aan_ adres in het citaat omvat, klik **[!UICONTROL Get shipping methods and rates]**.

1. Kies een verzendmethode uit de beschikbare opties.

1. Voer een **[!UICONTROL Proposed Shipping Price]** in.

   _[!UICONTROL Quote Totals]_&#x200B;wordt bijgewerkt om de voorgestelde verzendprijs weer te geven.

### Voeg een ondersteunend document bij

1. Onder _voeg uw commentaar_ doos toe, klik **[!UICONTROL Attach file]**.

   Door gebrek, [&#x200B; in bijlage dossiers &#x200B;](../configuration-reference/sales/quotes.md) kan tot 2 MB in om het even welke volgende dossierformaten zijn: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG of JPEG, PNG.

1. Kies het bestand in de map.

## Stap 3: Werk citaat-vlakke informatie bij, en verzend uw antwoord

1. Voer in de sectie _[!UICONTROL Negotiation]_&#x200B;op het tabblad&#x200B;_[!UICONTROL Comments]_ uw antwoord in de sectie **[!UICONTROL Add your comment]** in.

1. Als u een ondersteunend document wilt opnemen, klikt u op **[!UICONTROL Attach file]** en selecteert u het bestand in de directory.

   De maximale bestandsgrootte voor bijlagen is 2 MB.

1. Een korting toepassen op het citaat:

   - Kies onder _[!UICONTROL Quote Totals]_&#x200B;in de sectie&#x200B;_[!UICONTROL Negotiated Price]_ een van de volgende kortingstypen:

      - `Percentage Discount`: Met een percentagekorting verlaagt u de oorspronkelijke prijs met een bepaald percentage.
      - `Amount Discount`: Met een korting op het bedrag wordt een vaste prijsverlaging toegepast.
      - `Proposed Price`: Een voorgestelde prijskorting stelt de uiteindelijke prijs in op een bepaald bedrag, ongeacht de oorspronkelijke prijs.

   - Voer het bedrag in als een percentage of een vaste prijs.

     ![&#x200B; Commentaren van de Onderhandeling &#x200B;](./assets/quote-detail-negotiation-comments.png){width="600" zoomable="yes"}

   - U kunt kortingen op elk lijnpunt of het citaat als geheel toepassen:

      - **het puntkortingen van de Lijn**: De het puntkortingen van de Lijn worden toegepast op individuele punten in de kar. De korting kan een `percentage`, een specifieke `amount` of een `proposed price` zijn.
      - **Kart-vlakke kortingen**: De kunst-vlakke kortingen worden toegepast op het volledige het winkelwagentje. De korting kan een `percentage` of een specifieke `amount` zijn en wordt toegepast op de totale waarde van het winkelwagentje.
      - **Combinatie van Kortingen van het Punt van de Kar en van het Punt van de Lijn**: In sommige gevallen, kunnen de kortingen op zowel de kar als de niveaus van het lijnpunt worden toegepast. De korting op het regelitem wordt eerst toegepast, gevolgd door de korting op het winkelwagenniveau op het resterende totaal.

1. De offerte verzenden of opslaan:

   - Klik op **[!UICONTROL Send]** als het aanhalingsteken klaar is om naar de koper te worden teruggestuurd.

   - Klik op **[!UICONTROL Save as Draft]** als u het aanhalingsteken later wilt blijven gebruiken.

>[!NOTE]
>
> Tijdens de citaatonderhandelingen, kunnen de kortingen worden gesloten om verdere veranderingen te verhinderen. Zodra een citaat wordt gesloten, noch kan het kortingstype noch het bedrag worden veranderd zonder het citaat eerst te ontgrendelen. Dit vergrendelingsmechanisme zorgt ervoor dat de tussen de verkoper en de koper overeengekomen voorwaarden worden gehandhaafd.

## Stap 4: Follow-up van een prijsopgave

Wanneer u een prijsopgave verzendt, brengt het systeem zowel de koper als de verkoper op de hoogte die het bedrijfsaccount beheren. Het e-mailbericht bevat een koppeling naar de prijsopgave op de rekening van de koper en de vervaldatum van de prijsopgave. Op elk moment in de onderhandeling kan de koper het volgende doen:

- Accepteer de onderhandelde prijsopgave en voltooi de aankoop.
- Stuur een antwoord met een tegenaanbod en ga verder met de onderhandelingen.
- Beëindig de onderhandelingen.

Controleer uw e-mail en de status van het aanhalingsteken in het raster om de positie in de workflow te controleren. U kunt het onderhandelingsproces zo lang als nodig voortzetten.

## Knopbalk

| Knop | Beschrijving |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Hiermee gaat u terug naar de _[!UICONTROL Quotes]_-pagina zonder wijzigingen op te slaan. |
| [!UICONTROL Print] | Verzendt het aanhalingsteken naar een printer of slaat het op als een PDF-bestand. |
| [!UICONTROL Create Copy] | Hiermee maakt en opent u een kopie van het huidige aanhalingsteken, waarbij `(copy)` aan de oorspronkelijke naam wordt toegevoegd. Wijzig de naam van het nieuwe aanhalingsteken door het veld [!UICONTROL Name] te bewerken. Verwerk het nieuwe aanhalingsteken door het als concept op te slaan of te verzenden naar de klant. |
| Sjabloon maken | Creeer een citaatmalplaatje dat op het huidige citaat wordt gebaseerd. Offertesjablonen stroomlijnen de prijsonderhandeling door kopers en verkopers in staat te stellen overeenstemming te bereiken over contractvoorwaarden en prijsvoorwaarden die op meerdere offertes kunnen worden toegepast. . Na overeenstemming kan de koper een vooraf goedgekeurd, gekoppeld citaat uit de template genereren voor volgende orders in plaats van het aanvraagproces (RFQ) opnieuw te starten. |
| [!UICONTROL Save as Draft] | Sla eventuele wijzigingen in de prijsopgave op, maar verzend deze niet naar de koper. |
| [!UICONTROL Decline] | Het verzoek om over prijzen te onderhandelen wordt afgewezen, hetzij op het eerste onderzoek, hetzij tijdens lopende onderhandelingen. Wanneer een prijsopgave wordt afgewezen, moet de verkoper een opmerking toevoegen om de beslissing toe te lichten. Wanneer een prijsopgave wordt afgewezen, worden alle onderhandelde prijzen weer op de oorspronkelijke waarden ingesteld. Deze knop is uitgeschakeld terwijl de verkoper wacht op een antwoord van de koper. |
| [!UICONTROL Send] | Verstuurt het bijgewerkte prijsopgave als antwoord op de vraag van de koper. Deze knop is uitgeschakeld als de verkoper wacht op een antwoord van de koper. |

{style="table-layout:auto"}

## Veldomschrijvingen

De informatie van het citaat en de functies in Admin worden georganiseerd in de volgende secties.

### [!UICONTROL Quote & Account Information]

| Veld | Beschrijving |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | De naam die aan een citaatverzoek door de [&#x200B; koper &#x200B;](account-company-roles-permissions.md) wordt toegewezen. |
| [!UICONTROL Status] | Geeft de huidige status van het aanhalingsteken aan. De status van een prijsopgave kan alleen worden gewijzigd door actie van de koper of de verkoper. Zie ook de [&#x200B; montages van de Status &#x200B;](quotes.md) van Admin en de [&#x200B; rekening van de koper &#x200B;](account-dashboard-my-quotes.md). |
| [!UICONTROL Created] | De datum en het tijdstip waarop de koper de aanvraag voor een prijsopgave voor het eerst heeft ingediend. |
| [!UICONTROL Created By] | De voornaam en achternaam van de koper van de onderneming die het prijsverzoek heeft ingediend. |
| [!UICONTROL Expiration Date] | Geeft de laatste dag aan dat het huidige aanhalingsteken geldig is. De standaardvervaldatum wordt in de configuratie ingesteld op 30 dagen nadat een koper een aanvraag voor een prijsopgave heeft ingediend. <br/><br/> de verkoper kan de standaardvervaldatum met voeten treden door een verschillende datum (MMM DD JJJJ) in te gaan of de datum van de kalender te kiezen. Het aanhalingsteken verloopt nooit als het veld leeg blijft. <br/><br/> voor open citaten, ontvangt de verkoper een [&#x200B; e-mailbericht &#x200B;](../systems/email-templates.md) 48 uur alvorens het citaat gepland is te verlopen. Kopers krijgen een melding 24 uur vóór de vervaldatum. <br/><br/> de status van het citaat verandert in _Verlopen_ en de koper kan geen verdere veranderingen in het citaat aanbrengen. De voorgestelde prijzen in het citaat keren terug naar de oorspronkelijke waarden uit de catalogus. <br/><br/> als een citaat voor overzicht door de verkoper open is wanneer het citaat wordt geplaatst om te verlopen, wordt de vervaldatum teruggesteld volgens de waaier die in de configuratie wordt geplaatst. <br/><br/> de Datum van de Vervalsing is het enige gebied in de _Citaat &amp; sectie van de Rekening_ die tijdens het overzichtsproces kan worden uitgegeven. |
| [!UICONTROL Company] | De wettelijke naam van het [&#x200B; bedrijf &#x200B;](account-companies.md) dat de koper vertegenwoordigt. |
| [!UICONTROL Company Admin Email] | Het e-mailadres van de [&#x200B; bedrijfbeheerder &#x200B;](account-company-admin.md). |
| [!UICONTROL Sales Rep] | De [&#x200B; verkoopvertegenwoordiger &#x200B;](account-company-manage.md) die voor de verkoper werkt, en is het primaire contact dat aan de bedrijfrekening wordt toegewezen. |
| [!UICONTROL Shared Catalog (or Customer Group)] | De [&#x200B; gedeelde catalogus &#x200B;](catalog-shared.md) of [&#x200B; klantengroep &#x200B;](account-company-customer-group.md) waaraan het bedrijf wordt toegewezen. Het citaat zou douaneprijzen van de gedeelde catalogus kunnen omvatten die aan het bedrijf wordt toegewezen. |

{style="table-layout:auto"}

### [!UICONTROL Add to Quote by SKU]

| Veld | Beschrijving |
|---------------------------|-----------------------------------------------------------|
| [!UICONTROL Enter SKU] | De SKU van het product dat aan het citaat moet worden toegevoegd. |
| [!UICONTROL Qty] | Het aantal punten van dit SKU dat aan het citaat moet worden toegevoegd. |
| [!UICONTROL Add to Quote] | Hiermee voegt u de hoeveelheid van het opgegeven product toe aan de prijsopgave. |

{style="table-layout:auto"}

### [!UICONTROL Items Quoted]

| Veld | Beschrijving |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name & SKU] | De gekoppelde productnaam en de voorraadeenheid (SKU). |
| [!UICONTROL Stock] | Het aantal producten onder deze SKU die momenteel voor verkoop beschikbaar zijn. |
| [!UICONTROL Cost] | Het bedrag dat de verkoper heeft betaald om het product te kopen. |
| [!UICONTROL Catalog Price] | De prijs van het product in de catalogus van de koper, op basis van de klantengroep of gedeelde catalogus die aan het bedrijf van de koper is toegewezen. |
| [!UICONTROL Cart Price] | De oorspronkelijke prijs van het artikel in het winkelwagentje, na aftrek van eventuele kortingen op het winkelwagentje. De prijs van het winkelwagentje kan afwijken van de catalogusprijs als er kortingen of winkelregels gelden voor de klantengroep van de koper. |
| [!UICONTROL Discount] | De korting op regelitems die op het item wordt toegepast. De waarde kan een percentage, een vast bedrag of een voorgestelde prijs zijn. |
| [!UICONTROL Qty] | Het aantal eenheden in deze SKU dat de basis vormt voor de genoteerde prijs. Er kan alleen een positief getal worden ingevoerd dat groter is dan nul. Als u het aantal wilt veranderen in nul, schrap het lijnpunt van het citaat. |
| [!UICONTROL Subtotal] | De voorgestelde prijs vermenigvuldigd met de hoeveelheid bestelde artikelen. |
| [!UICONTROL Estimated Tax] | Het bedrag aan belasting dat voor dit lijnpunt, volgens de configuratie wordt geschat. Afhankelijk van de instellingen voor belastingberekening kan de geschatte belasting worden gebaseerd op een van de volgende elementen: Eenheidsprijs / Totaal rij / Totaal |
| [!UICONTROL Subtotal (Incl./Excl. Tax)] | Afhankelijk van de configuratie, kan deze kolom subtotal met of zonder geschatte belastingen tonen. |
| [!UICONTROL Action] | Selectiemenu van bewerkingen die op een lijstitem kunnen worden toegepast:<ul><li>**[!UICONTROL Discount item]**</li><li>**[!UICONTROL Leave a note to Buyer]**</li><li>**[!UICONTROL Remove an item from the quote]**</li></ul>. |
| [!UICONTROL Configure] | Hiermee kunt u de productopties voor een configureerbaar product wijzigen. |
| [!UICONTROL Update Prices] | Werkt het citaat met de recentste veranderingen van de gedeelde catalogus en prijsregels bij. |
| [!UICONTROL Recalculate Quote] | Hiermee herberekent u alle prijsopgaven, de regels voor de winkelwagenprijs en de belasting om de wijzigingen in de prijsopgave te weerspiegelen. |

{style="table-layout:auto"}

### [!UICONTROL Shipping Information]

| Veld | Beschrijving |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Shipping Address] | Hier wordt het verzendadres weergegeven dat is opgegeven in de account van de koper. Het verzendadres is leeg als de koper geen adres heeft opgegeven voordat hij de aanvraag indient. |
| [!UICONTROL Shipping Method & Price] | De Get Verzendmethodes en de verbinding van Tarieven verschijnt als de koper a _Verzenden aan_ adres in het citaat omvat. |

{style="table-layout:auto"}

### [!UICONTROL Negotiation]

| Veld | Beschrijving |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Comments] | Het tabblad Opmerkingen van de sectie Onderhandeling wordt gebruikt om een bericht aan de koper over de prijsopgave in te voeren. <br/>**[!UICONTROL Add your comment]**- De opmerkingen worden gebruikt om tijdens het onderhandelingsproces met de koper te communiceren. Gebruik de opmerkingen om eventuele kortingen in het citaat uit te leggen, of de reden waarom een prijsaanvraag wordt afgewezen.<br/>**[!UICONTROL Attach file]** - de maximumdossiergrootte en de gesteunde dossiertypes voor [&#x200B; in bijlage dossiers &#x200B;](configure-quotes.md) worden bepaald door de configuratie. Een bijgevoegd bestand kan standaard maximaal 2 MB en een van de volgende bestandstypen hebben: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG of JPEG, PNG. |
| [!UICONTROL History Log] | Op dit tabblad wordt een volledige historie van het aanhalingsteken weergegeven met datums, aanhalingstekenstatus en opmerkingen. |

{style="table-layout:auto"}

### [!UICONTROL Quote Totals]

| Veld | Beschrijving |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Total Cost] | De totale kosten voor de verkoper van de objecten die in de prijsopgave zijn opgenomen. |
| [!UICONTROL Catalog Total Price  (Incl./Excl. Tax)] | De totale prijs van de items in het citaat zonder belasting, volgens de prijzen in de gedeelde catalogus of de primaire catalogus die als basis voor het citaat wordt gebruikt. Breid de sectie uit om de waarden te tonen die in de berekening, afhankelijk van [&#x200B; Subtotaal van de Vertoning &#x200B;](../configuration-reference/sales/tax.md) het plaatsen in de configuratie worden gebruikt. Opties: <br/>**[!UICONTROL Subtotal (Excl. Tax)]**- De totale catalogusprijs zonder geschatte belasting.<br/>**[!UICONTROL Subtotal (Incl. Tax)]** - De totale catalogusprijs zonder geschatte belasting. <br/>**[!UICONTROL Estimated Tax]**- Het belastingbedrag dat naar schatting wordt toegepast op de totale catalogusprijs. |
| Onderhandelde prijs | De korting die aan de koper wordt aangeboden, kan op elk van de volgende manieren worden gebaseerd: <br/>**[!UICONTROL Percentage Discount]**- De korting als een percentage.<br/>**[!UICONTROL Amount Discount]** - De korting als een vast bedrag. <br/>**[!UICONTROL Proposed Price]**- De prijs die door de verkoper wordt voorgesteld.<p>Als alle items in het citaat een vergrendelde itemkorting hebben, is de sectie [!UICONTROL Negotiated Price] uitgeschakeld omdat er geen verdere korting kan worden toegepast.</p><p>Als een product een korting op regelitems heeft die niet is vergrendeld, worden zowel de korting op regelitem als de korting op het prijsniveau toegepast op de productprijs.</p> |
| [!UICONTROL Quote Subtotal (Incl./Excl. Tax)] | De totale voorgestelde prijs van elk lijnpunt in het citaat, of met of zonder belasting, afhankelijk van de [&#x200B; montages van de belastingberekening &#x200B;](../configuration-reference/sales/tax.md) in de configuratie. |
| [!UICONTROL Shipping & Handling] | Het bedrag dat de verkoper heeft ingevoerd in het veld Voorgestelde verzendprijs in het gedeelte Verzendgegevens van de prijsopgave. Als dat veld leeg is, wordt het bedrag gebaseerd op de geselecteerde verzendmethode. |
| [!UICONTROL Estimated Tax] | De hoeveelheid belasting die om, zoals gespecificeerd in de configuratie [&#x200B; vertoningsmontages &#x200B;](../configuration-reference/sales/tax.md) wordt geschat te zijn. |
| [!UICONTROL Quote Grand Total (Incl. Tax)] | Het uiteindelijke totaal onder aan de prijsopgave, inclusief de onderhandelingsprijs, de geschatte belasting en de voorgestelde verzending. |

{style="table-layout:auto"}
