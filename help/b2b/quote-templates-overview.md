---
title: Gebruiksscenario's en workflows voor het Citatesjabloon
description: Creeer een citaatmalplaatje van een bestaand citaat om citaatonderhandeling voor terugkomende orden te stroomlijnen.
feature: B2B, Quotes
exl-id: 7d1e7a3d-6c50-416a-b490-0a083e1c06b4
source-git-commit: 6fe8a356ab517fc5dd169c4a6f7ef52937f705c4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Gebruik hoofdletters en workflows voor prijssjablonen

Met de mogelijkheid Offertesjabloon kunnen kopers en verkopers het prijsverhogingsproces stroomlijnen door herbruikbare en aanpasbare prijsquotasjablonen te maken.

- **Aanpasbare Citaten** - de Kopers kunnen verbonden citaten van een vooraf goedgekeurd malplaatje produceren, dat voor aanpassing binnen gespecificeerde parameters zoals lijn-punt hoeveelheden en selecties toestaat.
- **de Drempelwaarden van de Orde** - Verkopers kunnen minimum en maximumorderverplichtingen plaatsen, die ervoor zorgen dat de kopers aan overeengekomen-op koopgevolume naleven. Nadat de koper de prijsverhogingsmalplaatje goedkeurt, stijgt de telling van de ordedrempel telkens als een verbonden citaat wordt geproduceerd. Als het gekoppelde citaat wordt gesloten zonder in een orde worden omgezet, wordt de orde afgetrokken van de drempeltelling. Wanneer aan de maximumorderdrempel wordt voldaan, verloopt het citaatmalplaatje.
- **Vervaldata** - de Malplaatjes kunnen geldigheidsperioden (*[!UICONTROL Valid Until]*) hebben, die ervoor zorgen dat de termijnen slechts binnen een gespecificeerd tijdkader van toepassing zijn. Bij het verlopen wordt de sjabloon gesloten en worden alle gekoppelde aanhalingstekens gesloten.
- **Kortingen en het Tarief** - de verkopers kunnen het zelfde lijn-punt, citaat-niveau, en het verschepen mogelijkheden van de prijskorting gebruiken beschikbaar met citaten om kortingen voor terugkomende orden te plaatsen, die het onderhandelingsproces vereenvoudigen.
- **het Volgen en het Melden** - het systeem volgt het aantal verbonden citaten die van het malplaatje worden geproduceerd en met succes voltooide orden om inzichten in de naleving van overeengekomen op orderquota te verstrekken.
- **Verbindingen van het Document van de Verwijzing** - zowel kunnen de kopers als de verkopers externe documentverbindingen (zoals DocuSign, het Teken van Adobe, of andere online diensten) aan het citaatmalplaatje toevoegen, uitgeven en beheren. Dit maakt gemakkelijke toegang tot verwante contracten en overeenkomsten tijdens het proces van het citaatmalplaatje mogelijk.

## Hoofdletters gebruiken

Een bedrijfkoper kan een prijsverhogingsmalplaatje gebruiken om een specifieke reeks producten over een periode te bestellen. De koper configureert de volgende opties van het citaatmalplaatje om het het citeren proces efficiënter, consistenter, en gericht aan strategische koopovereenkomsten te maken.

- Besteldrempel om het minimum- en maximumaantal bestellingen te specificeren dat in aanmerking komt voor overeengekomen prijsstelling. Dit kan worden gebruikt voor de toepassing en het volgen van in contractovereenkomsten bepaalde quota&#39;s.

- Hoeveelheden (minimum-/maximumhoeveelheden) In de template wordt een drempel voor de hoeveelheid vastgesteld die minimaal en maximaal kan worden aangekocht voor elke bestelling, zodat de verkoper de voorraadniveaus doeltreffend kan beheren en de koper de flexibiliteit krijgt om de hoeveelheden naar behoefte aan te passen.

- Referentiedocument is gekoppeld om verbindingen te onderhouden met externe contracten en overeenkomsten, waardoor het makkelijker wordt om tijdens het prijsaanvraagproces toegang te krijgen tot gerelateerde documentatie.

## Workflow voor prijssjabloon

Offertesjablonen kunnen worden geïnitieerd door de koper of de verkoper.

**Stap 1: De creatie van het malplaatje van het citaat (Nieuw)**

- **de Koper leidt tot het citaatmalplaatje**

  Wanneer de koper een bestaande prijsopgave bekijkt, besluit hij dat het bedrijf in het komende jaar meerdere bestellingen moet indienen en wil hij extra kortingen aanvragen op basis van herhaalde transacties. Ze maken een aanhalingstekensjabloon met de handeling *[!UICONTROL Create quote template]* voor het aanhalingsteken. De koper kan met behulp van het besturingselement *[!UICONTROL Add]* in de sectie met referentiedocumenten koppelingen naar externe contracten of overeenkomsten toevoegen. Vervolgens beginnen ze met onderhandelen door de prijsopgave ter controle naar de verkoper te sturen.

  Kopers kunnen ook een prijsopmaaksjabloon aanvragen door producten die ze regelmatig willen kopen toe te voegen aan het winkelwagentje. Vervolgens vraagt u om een prijsopgave en vermeldt u in de opmerkingen hoe vaak de aankoop moet worden herhaald.

- **Verkoper** — Een Vertegenwoordiger kan een citaatmalplaatje van Admin namens een specifieke bedrijfkoper tot stand brengen. De verkoper kan de prijsverhogingsmalplaatje in Admin van een bestaand citaat of van het [!UICONTROL Quote Templates] net tot stand brengen en het opslaan als `draft` of het verzenden naar de koper om de onderhandeling te beginnen. In de conceptversie is de prijsopgave alleen zichtbaar voor de verkoper. Nadat het aanhalingsteken is verzonden, is de status `Submitted` . Deze kan pas door de verkoper worden gewijzigd nadat de koper de transactie heeft teruggestuurd.

  ![&#x200B; Verkoper die een koperscitaat van het net van Citaten in Admin in werking stelt &#x200B;](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

  Wanneer de verkoper de aanhalingstekensjabloon maakt, wordt de vervaldatum ([!UICONTROL Valid until] datumveld) standaard ingesteld op 180 dagen. Als de koper de template heeft gemaakt, is de vervaldatum leeg.  De koper moet de vervaldatum instellen voordat de template ter controle naar de koper wordt teruggestuurd.

  Wanneer de verkoper de aanhalingstekensjabloon maakt, wordt de vervaldatum (*[!UICONTROL Valid until]* datumveld) standaard ingesteld op 180 dagen. Als de koper de template heeft gemaakt, is de vervaldatum leeg.  De koper moet de vervaldatum instellen voordat de template ter controle naar de koper wordt teruggestuurd.

**Stap 2: De overzicht en de onderhandeling van het citaat (Overzicht)**

Het bekijken van of onderhandelen over een prijsopgavesjabloon kan onder meer bestaan uit het wijzigen van hoeveelheden, het verwijderen van objecten, het toevoegen van commentaar op regelobjecten, het toepassen van kortingen op regelobjecten of prijsopgaven (verkoper), het toevoegen van een verzendadres (koper) en het beheren van koppelingen naar referentiedocumenten.

- **de meningsverzoek van de Verkoper en verzendt reactie** - in Admin, bekijkt de verkoper het citaatmalplaatje van het *[!UICONTROL Quote Templates]** net of opent het van de verbinding in het e-mailbericht. In de winkel verandert de status van de prijsopgave in `Pending` en kan de koper geen wijzigingen aanbrengen. Na het zelfde proces voor [&#x200B; citaat onderhandeling &#x200B;](quote-price-negotiation.md), antwoordt de verkoper door prijskortingen aan te bieden en hoeveelheden en punten aan te passen zoals nodig, gaat een commentaar in, en verzendt het citaatmalplaatje terug naar de koper. De verkoper kan tijdens dit proces ook koppelingen naar referentiedocumenten toevoegen, bewerken of verwijderen. De koper en de verkoper worden per e-mail op de hoogte gesteld dat de verkoper heeft gereageerd.

- **de meningen van de koper citeren malplaatje van verkoper en verzendt reactie** - de koper klikt de verbinding in het e-mailbericht om het citaatmalplaatje te openen, of opent het van de _Mijn pagina van de Malplaatjes van het Citaat_ van het rekeningsdashboard. De koper kan opmerkingen aan de verkoper overlaten op het regel- of prijsniveau, hoeveelheden wijzigen, objecten verwijderen en koppelingen naar referentiedocumenten beheren.

De koper en verkoper gaan verder met de onderhandelingsprocedure totdat een overeenkomst is bereikt of de verkoper de prijsopgave afwijst. Als de koper wijzigingen aanbrengt in de prijsopgave (door producten toe te voegen of te verwijderen, door de producthoeveelheden te wijzigen of door het referentiedocument te wijzigen), moet de aanhaling ter controle worden teruggestuurd naar de verkoper.

- **de Koper voegt een het verschepen adres** toe - de koper moet een het verschepen adres aan het citaatmalplaatje toevoegen als het niet heeft. Nadat de koper het adres heeft toegevoegd, kan de verkoper verzend- en leveringsopties opgeven. De weergegeven verzendmethoden zijn afhankelijk van de configuratie Storefront.

Als de koper een verzendadres toevoegt, moet de onderhandelingsovereenkomst worden herzien en kan de verkoper het onderhandelingsproces voortzetten totdat een overeenkomst is bereikt of de verkoper de prijsopmaaksjabloon afwijst.

**Stap 3: De koper keurt citaatmalplaatje** goed

De koper accepteert de onderhandelde voorwaarden in de template. Nadat het citaatmalplaatje wordt goedgekeurd, kan de koper het gebruiken aan [&#x200B; vooraf goedgekeurde, verbonden citaten &#x200B;](account-dashboard-my-quote-templates.md#generate-a-linked-quote) produceren die kunnen worden gebruikt om orden voor te leggen zonder verdere onderhandeling te vereisen.

Verzendopties zijn vergrendeld bij afhandeling.

Offertesjablonen blijven actief totdat deze verlopen, geannuleerd of gesloten zijn of totdat de maximumorderdrempel voor de koper is bereikt.

### Een aanhalingsteken weergeven

1. Klik in de kolom **[!UICONTROL Actions]** voor een record op **[!UICONTROL View]** .

1. Om aan het klantenverzoek te antwoorden, volg de instructies en begin het zelfde [&#x200B; proces van de prijsonderhandeling &#x200B;](quote-price-negotiation.md) dat aan onderhandelingscitaten wordt gebruikt.

### Sjabloonactiviteit voor aanhalingstekens weergeven

Bekijk de tijdlijn van de onderhandeling, de communicatie, en andere activiteit van het citaatmalplaatje van [!UICONTROL Comments] en [!UICONTROL History Log] - de informatie omvat statusveranderingen, updates aan klant en verschepende informatie, punt en prijsupdates, en andere belangrijke informatie.

1. Open een aanhalingsteken.

1. Opmerkingen bij de onderhandeling en de geschiedenis van aanhalingstekens weergeven door naar **[!UICONTROL Negotiation]** te schuiven en **[!UICONTROL Comments]** en **[!UICONTROL History Log]** te selecteren.

   ![&#x200B; Geschiedenis van de Mening &#x200B;](./assets/quote-view-history.png){width="400" zoomable="yes"}

1. De geschiedenis wordt ook bijgehouden op het niveau van het lijnpunt.

   ![&#x200B; de Geschiedenis van het Punt van de Lijn van de Mening &#x200B;](./assets/quote-view-line-item-history.png){width="400" zoomable="yes"}

### Een aanhalingstekensjabloon afwijzen

Alleen aanhalingstekensjablonen met de status `In Review` kunnen worden geweigerd.

1. Open in het *[!UICONTROL Quote Templates]* -raster de aanhalingstekensjabloon die u wilt afwijzen.

1. Voor het citaatmalplaatje, klik **[!UICONTROL Decline]**.

1. Voer de reden in waarom het aanhalingsteken is afgewezen en klik op **[!UICONTROL Confirm]** .
