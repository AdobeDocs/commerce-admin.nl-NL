---
title: Gebruiksscenario's en workflows voor offertesjablonen
description: Maak een offertsjabloon op basis van een bestaand citaat om de offerteonderhandeling voor terugkerende bestellingen te stroomlijnen.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Gebruik hoofdletters en kleine letters voor offertesjablonen en workflows

Met de mogelijkheid Offertesjabloon kunnen kopers en verkopers het offerteproces stroomlijnen door herbruikbare en aanpasbare offertjablonen te maken.

- **Aanpasbare Citaten** - de Kopers kunnen verbonden citaten van een vooraf goedgekeurd malplaatje produceren, dat voor aanpassing binnen gespecificeerde parameters zoals lijn-punt hoeveelheden en selecties toestaat.
- **de Drempels van de Orde** - de verkopers kunnen minimum en maximumorderverplichtingen bepalen, die ervoor zorgen dat de kopers aan overeengekomen koopgevolumes naleven.
- **Vervaldatums** - de Malplaatjes kunnen geldigheidsperioden hebben, die ervoor zorgen dat de termijnen slechts binnen een gespecificeerd tijdkader van toepassing zijn.
- **Kortingen en het Tarief** - de verkopers kunnen het zelfde lijn-punt, citaat-niveau, en de mogelijkheden van de verschepende prijskorting gebruiken beschikbaar met citaten om kortingen voor terugkerende orden te plaatsen, die het onderhandelingsproces vereenvoudigen.
- **het Volgen en het Melden** - het systeem volgt het aantal verbonden citaten die van het malplaatje worden geproduceerd en met succes voltooide orden om inzichten in de voltooiing van overeengekomen op orderquota te verstrekken.

## Hoofdletters gebruiken

Een bedrijfkoper kan een prijsverhogingsmalplaatje gebruiken om een specifieke reeks producten over een periode te bestellen. De koper configureert de volgende opties van het citaatmalplaatje om het het citeren proces efficiënter, consistenter, en gericht aan strategische koopovereenkomsten te maken.

- Besteldrempel om het minimum- en maximumaantal bestellingen te specificeren dat in aanmerking komt voor overeengekomen prijsstelling. This can be used to apply and track order quotas specified in contract agreements.

- Quantity thresholds (minimum/maximum quantities) The template specifies a quantity threshold to set the minimum and maximum quantity that can be purchased for each order, ensuring that the seller can manage stock levels effectively while providing the buyer with the flexibility to adjust quantities as needed.

## Quote template workflow

Quote templates can be initiated by the buyer or the seller.

**Stap 1: De creatie van het malplaatje van het citaat (Nieuw)**

- **de Koper leidt tot het citaatmalplaatje**

  Wanneer de koper een bestaande prijsverhogingsmalplaatje controleert, besluit dat het bedrijf veelvoudige orden in het volgende jaar moet indienen en extra kortingen wil vragen die op herhaalde zaken worden gebaseerd. Ze maken een aanhalingstekensjabloon met de handeling *[!UICONTROL Create quote template]* voor het aanhalingsteken. Vervolgens beginnen ze de onderhandelingen door de nieuwe template ter controle naar de verkoper te sturen.

  Kopers kunnen ook rechtstreeks via de pagina *[!UICONTROL My Quote Templates]** op de winkel een aanhalingsteken maken.

- **Verkoper** - een Vertegenwoordiger kan een citaatmalplaatje van Admin namens een specifieke bedrijfkoper creëren. De verkoper kan de offertesjabloon in de beheerder maken op basis van een bestaande offerte of op basis van het [!UICONTROL Quote Templates] -raster en deze opslaan als een `draft` of de sjabloon naar de koper sturen om de onderhandelingen te starten. In de conceptstatus is de offerte alleen zichtbaar voor de verkoper. Nadat de offerte is verzonden, is de status `Submitted` . De verkoper kan de wijziging pas aanbrengen nadat de koper de wijziging heeft teruggestuurd.

  ![ Verkoper die een koperscitaat van het net van Citaten in Admin in werking stelt ](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**Stap 2: De overzicht en de onderhandeling van het citaat (Overzicht)**

Het bekijken van of onderhandelen over een prijsopgavesjabloon kan onder meer bestaan uit het wijzigen van hoeveelheden, het verwijderen van objecten, het toevoegen van commentaar op lijstitems, het toepassen van kortingen op lijstitems of noteringen (verkoper) en het toevoegen van een verzendadres (koper).

- **de meningsverzoek van de verkoper en verzendt reactie** - in Admin, bekijkt de verkoper het citaatmalplaatje van het *[!UICONTROL Quote Templates]* * net of opent het van de verbinding in het e-mailbericht. In de winkel verandert de status van de offerte in `Pending` en kan de koper geen wijzigingen aanbrengen. Na het zelfde proces voor [ citaatonderhandeling ](quote-price-negotiation.md), antwoordt de verkoper door prijskortingen aan te bieden en hoeveelheden en punten aan te passen zoals nodig, gaat een commentaar in, en stuurt het citaat terug naar de koper. De koper en de verkoopvertegenwoordiger worden per e-mail op de hoogte gesteld van het feit dat de verkoper heeft gereageerd.

- **de vertoningen van de koper citaatmalplaatje van verkoper en verzendt reactie** - de koper klikt de verbinding in het e-mailbericht om het citaatmalplaatje te openen, of opent het citaat van de _Mijn pagina van de Malplaatjes van het Citaat_ van het accountdashboard. De koper kan opmerkingen aan de verkoper overlaten op het regel- of offerteniveau, hoeveelheden wijzigen en objecten verwijderen.

De koper en de verkoper zetten het onderhandelingsproces voort totdat een overeenkomst is bereikt of totdat de verkoper de offertesjabloon afwijst. Als de koper wijzigingen aanbrengt in de offerte (door producten toe te voegen of te verwijderen of door producthoeveelheden te wijzigen), moet de offerte ter controle worden teruggestuurd naar de verkoper.

- **de Koper voegt een het verschepen adres** toe - de koper moet een het verschepen adres aan het citaatmalplaatje toevoegen als het niet heeft. After the buyer adds the address, the seller can provide shipping and delivery options. De weergegeven verzendmethoden zijn afhankelijk van de configuratie Storefront.

If the buyer adds a shipping address, the negotiation agreement has to be reviewed, and the seller can continue the negotiation process until an agreement is reached, or the seller declines the quote template.

****

The buyer accepts the negotiated terms in the template. After the quote template is accepted, the buyer can use it to generate pre-approved, linked quotes that can be used to submit orders without requiring further negotiation.

Verzendopties zijn vergrendeld bij afhandeling.

### Een aanhalingsteken weergeven

1. Klik in de kolom **[!UICONTROL Actions]** voor een record op **[!UICONTROL View]** .

1. Om aan het klantenverzoek te antwoorden, volg de instructies en begin het zelfde [ proces van de prijsonderhandeling ](quote-price-negotiation.md) dat aan onderhandelingscitaten wordt gebruikt.

### Sjabloonactiviteit voor aanhalingstekens weergeven

Bekijk de tijdlijn van de onderhandelingen, de communicatie en andere offerteactiviteiten in de [!UICONTROL Comments] en [!UICONTROL History Log] - informatie omvat statuswijzigingen, updates van klant- en verzendgegevens, item- en prijsupdates en andere belangrijke informatie.

1. Open een offertsjabloon.

1. Bekijk opmerkingen over de offerteonderhandelingen en de geschiedenis door naar **[!UICONTROL Negotiation]** te schuiven en **[!UICONTROL Comments]** en **[!UICONTROL History Log]** te selecteren.

   ![ Geschiedenis van de Mening ](./assets/quote-view-history.png){width="400"}

1. De geschiedenis wordt ook bijgehouden op het niveau van het lijnpunt.

   ![ de Geschiedenis van het Punt van de Lijn van de Mening ](./assets/quote-view-line-item-history.png){width="400"}


### Een aanhalingstekensjabloon afwijzen

Alleen aanhalingstekensjablonen met de status `In Review` kunnen worden geweigerd.

1. *[!UICONTROL Quote Templates]*

1. **[!UICONTROL Decline]**

1. **[!UICONTROL Confirm]**
