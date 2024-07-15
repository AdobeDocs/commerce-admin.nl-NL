---
title: Onderhandelbare aanhalingstekens
description: Meer informatie over workflows met prijsopgave en hoe u deze service kunt aanbieden aan uw bedrijfsaccounts.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Onderhandelbare aanhalingstekens

Kopers en verkopers gebruiken Aanhalingstekens om het onderhandelingsproces voor een orde-toevoegende punten te beheren, hoeveelheden bij te werken, om kortingen te verzoeken en toe te passen, etc.-tot zij overeenstemming bereiken. Het onderhandelingsproces voor de prijsopgave kan worden geïnitieerd door een geautoriseerde koper van een onderneming of door een vertegenwoordiger van een onderneming.

Aanhalingstekens kunnen worden geopend door een erkende koper van een onderneming of door een vertegenwoordiger van een verkoopmaatschappij. Nadat de prijsopgave is gemaakt, begint het onderhandelingsproces wanneer de koper of verkoper de prijsopgave ter controle indient. Het _Citaten_ net dat van elk ontvangen citaat een lijst maakt en een geschiedenis van de communicatie tussen koper en verkoper handhaaft. Gebruik de standaard [ werkplekcontroles ](../getting-started/admin-workspace.md) om de lijst te filtreren, de kolomlay-out te veranderen, meningen, en de uitvoergegevens te bewaren.

- In de winkel, leggen de kopers het citaat als a [ verzoek voor om ](quote-price-negotiation.md) de prijs van het het winkelwagentje te bespreken. Bij het maken van de prijsaanvraag kan een koper de prijsopgave opslaan als concept of deze rechtstreeks naar de verkoper verzenden.

- In Admin, kunnen de Vertegenwoordigers van de Verkoop prijsnoteringen namens de bedrijfkoper tot stand brengen. Bij het maken van de prijsopgave kan de verkoper de prijsopgave opslaan als concept of deze rechtstreeks naar de koper verzenden om het onderhandelingsproces te starten.

Tijdens het onderhandelingsproces kan het citaat alleen worden bijgewerkt door de persoon die de voorwaarden voor verdere onderhandelingen herziet en voorstelt.

## Vereisten

Negotiable quotes zijn beschikbaar slechts als Adobe Commerce de volgende configuratiemontages heeft:

- [De Adobe Commerce B2B-extensie is geïnstalleerd](install.md)
- [Vormde B2B-functies](enable-basic-features.md)
   - Bedrijfsaccounts inschakelen
   - B2B-aanhalingsteken inschakelen

## Offerteworkflow

Aanbiedingen kunnen worden geïnitieerd door de koper of de verkoper.

**Stap 1: De verwezenlijking van het citaat**

- **de verzoeken van de Koper citeren** - de koper [ vraagt een citaat ](quote-request.md) van het winkelwagentje. Het verzoek verschijnt in de _Mijn Citaten_ lijst in het rekeningsdashboard van de koper en e-mailbericht wordt verzonden naar de verkoopvertegenwoordiger die aan de bedrijfrekening wordt toegewezen. In Admin, verschijnt het verzoek in het _Citaten_ net, met een status van `New`. Een prijsaanvraag kan door de koper worden gewijzigd totdat de verkoper het heeft geopend.

  ![ Citaten ](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}


- **de vertegenwoordiger van de Verkoop** — Een Vertegenwoordiger kan [ een citaat ](sales-rep-initiates-quote.md) van Admin namens een specifieke bedrijfkoper tot stand brengen. De verkoper moet de prijsopgave bijwerken om producten en andere informatie zoals kortingen en opmerkingen aan de koper toe te voegen. De Vertegenwoordiging van de Verkoop kan het citaat als `draft` bewaren of het verzenden naar de koper om de onderhandeling te beginnen. In de conceptversie is de prijsopgave alleen zichtbaar voor de verkoper. Nadat het aanhalingsteken is verzonden, is de status `Submitted` . Deze kan pas door de verkoper worden gewijzigd nadat de koper de transactie heeft teruggestuurd.

  ![ Verkoper die een koperscitaat van het net van Citaten in Admin in werking stelt ](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}


**Stap 2: Het overzicht en de onderhandeling van het citaat**

**de meningsverzoek van de verkoper en verzendt reactie** - in Admin, bekijkt de verkoper het verzoek om een citaat. De status van het aanhalingsteken verandert in `Pending` en de koper kan geen wijzigingen aanbrengen. De [ verkoper antwoordt ](quote-price-negotiation.md) door verdisconteerde tarifering voor de producten in het citaat aan te bieden, gaat een commentaar in, en verzendt het citaat terug naar de koper. De koper en de verkoper worden per e-mail op de hoogte gesteld dat de verkoper heeft gereageerd.

**de meningscitaat van de koper van verkoper en verzendt reactie** - de koper klikt de verbinding in het e-mailbericht om het citaat te openen, of opent het citaat van de _Mijn Citaten_ pagina van het rekeningsdashboard. De koper kan opmerkingen aan de verkoper op het regel- of prijsniveau laten en objecten verwijderen.

De koper en verkoper kunnen het onderhandelingsproces voortzetten totdat een overeenkomst is bereikt of de verkoper de prijsopgave afwijst. Als de koper wijzigingen aanbrengt in de prijsopgave (door producten toe te voegen of te verwijderen of door producthoeveelheden te wijzigen), moet de prijsopgave ter controle worden teruggestuurd naar de verkoper.

**Stap 4: De koper keurt citaat** goed - de koper keurt de voorgestelde prijs goed en blijft afrekenen. Er kunnen geen extra kortingen aan het onderhandelde prijsopgave worden toegevoegd.

## B2B-rolbronnen voor winkeloffertes

De opties van de configuratie voor citaten worden gecontroleerd gebruikend de [ rolmiddelen ](../systems/permissions-user-roles.md#role-resources). Deze rolmiddelen moeten voor de Admin gebruikersrol worden geplaatst die aan de opslagbeheerder wordt toegewezen.

Om toegang tot citaatfuncties in Admin te verlenen, ga **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selecteer de rol, en navigeer aan [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] in de_ Bron van de Rol _boom.

## Een handeling toepassen

In Admin, kunnen de Beheerders B2B en de Verkopers citaten van het Net van het Citaat beheren door het [!UICONTROL Actions] menu te gebruiken.

![ Citaten ](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. Selecteer in de eerste kolom van het raster het selectievakje voor elke record waarop u de handeling wilt toepassen.

1. Selecteer in **[!UICONTROL Actions]** de actie die u wilt toepassen.

### Een aanhalingsteken weergeven

1. Klik in de kolom **[!UICONTROL Actions]** voor een record op **[!UICONTROL View]** .

1. Om aan het klantenverzoek te antwoorden, volg de instructies en begin het [ proces van de prijsonderhandeling ](quote-price-negotiation.md).

### Aanhalingsactiviteit weergeven

Bekijk de onderhandelingstijdlijn, de communicatie, en andere citaatactiviteit van [!UICONTROL Comments] en [!UICONTROL History Log] - de informatie omvat statusveranderingen, updates aan klant en verschepende informatie, punt en prijsupdates, en andere belangrijke informatie.

1. Open een offerte.

1. Opmerkingen bij de onderhandeling en de geschiedenis van aanhalingstekens weergeven door naar **[!UICONTROL Negotiation]** te schuiven en **[!UICONTROL Comments]** en **[!UICONTROL History Log]** te selecteren.

   ![ Geschiedenis van de Mening ](./assets/quote-view-history.png){width="400"}

1. De geschiedenis wordt ook bijgehouden op het niveau van het lijnpunt.

   ![ de Geschiedenis van het Punt van de Lijn van de Mening ](./assets/quote-view-line-item-history.png){width="400"}


### Een aanvraag voor een prijsopgave afwijzen

Alleen aanhalingsaanvragen met de status `Open` kunnen worden afgewezen.

1. Selecteer elk open citaatverzoek dat u wilt verwerpen.

1. Stel het besturingselement _[!UICONTROL Actions]_in op `Declined` .

1. Voer de reden in waarom het aanhalingsteken is afgewezen en klik op **[!UICONTROL Confirm]** .

   ![ Weigeren Citaat?](./assets/quote-decline-confirm.png){width="400"}


## Kolombeschrijvingen

| Kolom | Beschrijving |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Als u de aanhalingstekens wilt selecteren waarop een handeling moet worden uitgevoerd, schakelt u het selectievakje in of gebruikt u het selectiegereedschap in de kolomkop. Opties: Alles selecteren / Alles deselecteren |
| [!UICONTROL ID] | Een unieke numerieke id die wordt toegewezen wanneer een prijsaanvraag wordt ingediend via het winkelwagentje van een koper. Wanneer het bekijken van het citaatdetail verschijnt identiteitskaart bij de bovenkant van de pagina, in plaats van de citaatnaam. |
| [!UICONTROL Name] | De naam die door de koper aan een prijsaanvraag is toegewezen. |
| [!UICONTROL Created Date] | De datum en het tijdstip waarop de koper de aanvraag voor een prijsopgave voor het eerst heeft ingediend. |
| [!UICONTROL Company] | De naam van de onderneming waarvoor een koper een prijsaanvraag indient. |
| [!UICONTROL Submitted By] | De voornaam en achternaam van de koper van de onderneming die een prijsaanvraag indient. |
| [!UICONTROL Last Updated] | De datum en het tijdstip van de laatste communicatie tussen koper en verkoper over de prijsopgave. |
| [!UICONTROL Sales Rep] | De voornaam en achternaam van de verkoper die de rekening van de koper beheert. |
| [!UICONTROL Quote Total (Base)] | De totale prijs van de te kopen producten op basis van de oorspronkelijke offerte. Het totale bedrag wordt weergegeven in de basisvaluta van de website en in de valuta van de opslagplaats. |
| [!UICONTROL Quote Total (Negotiated)] | De totale prijs van de te kopen producten op basis van de overeengekomen prijsopgave. Dit totaal wordt automatisch berekend door het systeem en omvat alle kortingen op regelniveau of op prijsniveau die door de verkoper worden toegepast. Het totale bedrag wordt weergegeven in de basisvaluta van de website en in de valuta van de opslagplaats. |
| [!UICONTROL Status] | Geeft de huidige status van een aanhalingsverzoek aan. De status van een prijsopgave kan alleen worden gewijzigd door actie van de koper of de verkoper. Zie ook de montages van de Status van de [ rekening van de koper ](account-dashboard-my-quotes.md).<ul><li>**[!UICONTROL New]** - De koper heeft een prijsaanvraag ingediend, maar deze is niet door de verkoper bekeken. De aanvraag kan door de koper worden bijgewerkt totdat de verkoper het heeft geopend.</li><li>**[!UICONTROL Draft]** - De verkoper maakt een conceptprijsopgave voor een koper. De prijsopgave is pas zichtbaar voor de koper nadat de verkoper de aanbiedingsgegevens (objecten, aantal, korting, enzovoort) heeft toegevoegd en de prijsopgave bij de koper heeft ingediend.</li> <li>**[!UICONTROL Open]** - De verkoper heeft het verzoek geopend en is bezig het te bekijken en een reactie voor te bereiden. </li><li>**[!UICONTROL Submitted]** - De verkoper heeft een reactie gestuurd naar de koper. Het citaatrecord kan niet worden bewerkt tijdens het onderhandelingsproces.</li><li>**[!UICONTROL Client Reviewed]** - De koper heeft de reactie van de verkoper bekeken en bereidt een antwoord voor.</li><li>**[!UICONTROL Updated]** - De koper heeft een reactie verzonden, maar deze is niet door de verkoper bekeken.</li><li>**[!UICONTROL Ordered]** - De koper heeft de bestelling ingediend op basis van de onderhandelde prijsopgave.</li><li>**[!UICONTROL Closed]** - De koper heeft de prijsaanvraag geannuleerd.</li><li>**[!UICONTROL Declined]** - De verkoper heeft de aanvraag voor een prijsopgave afgewezen. Aangepaste prijzen worden uit het aanhalingsteken verwijderd en de record is vergrendeld voor verdere bewerkingen.</li><li>**[!UICONTROL Expired]** - De koper heeft niet binnen de opgegeven termijn gereageerd op het antwoord van de verkoper en het prijsopgave is niet langer geldig.</li></ul> |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Opent het verzoek om een prijsopgave en houdt een overzicht bij van de onderhandelingen tussen koper en verkoper. |

{style="table-layout:auto"}

## Knopbalk

| Knop | Beschrijving |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Send] | Verstuurt het bijgewerkte prijsopgave als antwoord op de vraag van de koper. Deze knop is uitgeschakeld als de verkoper wacht op een antwoord van de koper. |
| [!UICONTROL Back] | Keert aan de _Citaten_ pagina terug zonder veranderingen te bewaren. |
| [!UICONTROL Create Copy] | [!BADGE  1.5.0-bètamogelijkheden ] {type=Informative url=&quot;/help/b2b/release-notes.md&quot;tooltip=&quot;Beschikbaar slechts voor de programmadeelnemers van Beta&quot;} creeer een nieuw citaat van het huidige citaat door het te kopiëren en anders te noemen. Wanneer het nieuwe aanhalingsteken wordt geopend, is de standaardnaam `<original quote name> (copy)`. Wijzig de naam door de waarde in het veld [!UICONTROL Name] te bewerken en het aanhalingsteken op te slaan als concept. |
| [!UICONTROL Print] | Verzendt het aanhalingsteken naar een printer of slaat het op als een PDF-bestand. |
| [!UICONTROL Create a copy] | Maakt een kopie van het aanhalingsteken met de naam `<original quote name> (copy)` en opent deze. Wijzig de naam van het nieuwe aanhalingsteken en werk het bij voordat u het opslaat als concept of naar de koper verzendt. |
| [!UICONTROL Save as Draft] | Hiermee slaat u eventuele wijzigingen in de prijsopgave op, maar niet terugsturen naar de koper. |
| [!UICONTROL Decline] | Het verzoek om over prijzen te onderhandelen wordt afgewezen, hetzij op het eerste onderzoek, hetzij tijdens lopende onderhandelingen. Wanneer een prijsopgave wordt afgewezen, moet de verkoper een opmerking toevoegen om de beslissing toe te lichten. Wanneer een prijsopgave wordt afgewezen, worden alle onderhandelde prijzen weer op de oorspronkelijke waarden ingesteld. Deze knop is uitgeschakeld terwijl de verkoper wacht op een antwoord van de koper. |

{style="table-layout:auto"}

## Voorbeeld van citaat

In de volgende afbeelding ziet u een voorbeeld van de weergave met citaatdetails in de beheerfunctie waarvoor bepaalde instellingen zijn geconfigureerd.

![ citaat van het Voorbeeld ](./assets/quote-full.png){width="700" zoomable="yes"}


>[!NOTE]
>
>[!BADGE  1.5.0-bètamogelijkheden ]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor Beta-programmadeelnemers"}
