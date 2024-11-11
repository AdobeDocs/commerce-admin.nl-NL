---
title: Bedrijfsaccounts beheren
description: Leer bedrijfsaccounts voor je Adobe Commerce-winkel beheren met behulp van de pagina Companies en de tools die beschikbaar zijn in het raster.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: d930c2294f0313cfa36d81c8a153b3cb35183f85
workflow-type: tm+mt
source-wordcount: '2726'
ht-degree: 0%

---

# Bedrijfsaccounts beheren

De pagina _[!UICONTROL Companies]_bevat een lijst met alle huidige bedrijfsaccounts, ongeacht de status. Eventuele lopende goedkeuringsaanvragen staan boven aan de lijst.

![ het Net van Bedrijven ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Gebruik het besturingselement *[!UICONTROL Columns]* om de kolommen in het raster aan te passen. Pas de bedrijven aan die in de weergave worden weergegeven met de zoek- en filtermogelijkheden.

- Vind bedrijven in het **Bedrijven** net door _[!UICONTROL Search]_te gebruiken. Het onderzoek indexeert de **Naam van het Bedrijf**en **ouder**kolommen.

- Pas de weergave aan om records op te nemen die aan specifieke criteria voldoen met de [!UICONTROL Filter] . Bijvoorbeeld, als de B2B plaats wordt gevormd om zowel enige bedrijfrekeningen als [ bedrijfhiërarchieën ](manage-companies.md) te beheren, kunt u filtreren door `[!UICONTROL Company Type - Company]` om slechts enige bedrijven te tonen, of door `[!UICONTROL Company Type - Parent]` om slechts het ouderbedrijf voor elke hiërarchie te tonen.

Pas een actie op veelvoudige bedrijfverslagen toe door de _[!UICONTROL Actions]_controle boven het net te gebruiken. In plaats van bijvoorbeeld elk afzonderlijk bedrijfsverzoek goed te keuren, kunt u meerdere verzoeken selecteren om de accounts in één handeling te activeren. De beschikbare acties hangen van de [ toestemmingen ](../systems/permissions.md) voor de rol af die aan uw Admin gebruikersrekening wordt toegewezen.

## Bronnen voor bedrijfsrollen

De [ montages van de Middelen van de Rol ](../systems/permissions-user-roles.md#role-resources) bepalen de capaciteit om:

- Een bedrijf toevoegen
- Een bedrijf verwijderen
- Saldo-terugbetaling toepassen
- Bedrijven weergeven

Deze rolmiddelen moeten voor de [ Rol van de Gebruiker ](../systems/permissions-user-roles.md) worden geplaatst die aan de Admin gebruikersrekening wordt toegewezen.

## Bedrijfsaccounts beheren via het raster Bedrijven

U kunt de gebruikersaccounts van bedrijven weergeven en beheren in het menu Beheer door **[!UICONTROL Customers]** > **[!UICONTROL Companies]** te selecteren om de pagina *[!UICONTROL Companies]* te openen.

U kunt accounts afzonderlijk of in groepen beheren.

- U kunt configuratie-instellingen voor een individuele bedrijfsaccount weergeven of wijzigen door **[!UICONTROL Edit]** te selecteren in de kolom **[!UICONTROL Action]** voor de accountrecord van het bedrijf.

  ![ Uitgezochte actie om op geselecteerde bedrijven van toepassing te zijn ](assets/companies-change-settings-edit-selection.png){width="675" zoomable="yes"}

- U kunt een groep geselecteerde bedrijfsaccounts weergeven of wijzigen met behulp van de opties in het besturingselement [!UICONTROL Actions]** boven het raster.

  ![ Uitgezochte actie om op geselecteerde bedrijven van toepassing te zijn ](assets/companies-change-settings-mass-action-selection.png){width="675" zoomable="yes"}

Zie de volgende secties voor instructies om elke actie toe te passen.

### Bedrijfsaccounts activeren

1. Selecteer **[!UICONTROL Set Active]** in het besturingselement **[!UICONTROL Actions]** .

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

### Actief/inactief instellen

Klanten met inactieve accounts kunnen zich niet aanmelden bij of aankopen doen bij hun accounts. Er zijn twee methoden om een klantenaccount in te stellen als actief of inactief:

Methode 1: **van het net van Klanten**

1. Op _Admin_ sidebar, ga [!UICONTROL **Klanten**] > [!UICONTROL **Alle Klanten**].

1. Selecteer in het menu **[!UICONTROL Actions]** een van de volgende opties:

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. Selecteer **[!UICONTROL OK]** wanneer u daarom wordt gevraagd om de wijziging toe te passen.

Methode 2: **van de rekening geeft pagina** uit

1. Op _Admin_ sidebar, ga [!UICONTROL **Klanten**] > [!UICONTROL **Alle Klanten**].

1. Zoek in het raster het klantrecord dat u wilt bewerken.

1. In de _kolom van Acties_ op uiterst rechts, uitgezocht [!UICONTROL **geef**] uit.

1. Selecteer het [!UICONTROL **lusje van de Informatie van de Rekening**].

1. Plaats [!UICONTROL **Actieve Klant**] aan `Yes` of `No`.

1. Klik [!UICONTROL **sparen Klant**].

### Zakelijke accounts blokkeren

Gebruikers die zijn gekoppeld aan een geblokkeerd bedrijfsaccount kunnen zich aanmelden en toegang krijgen tot de catalogus, maar kunnen geen aankopen doen. Een bedrijf met een rekening die niet in goede staat is kan tijdelijk worden geblokkeerd totdat de kwestie is opgelost.

1. Selecteer **[!UICONTROL Block]** in het besturingselement **[!UICONTROL Actions]** .

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

### Bedrijfsaccounts verwijderen

Verwijderde bedrijfsaccounts kunnen niet worden hersteld. De status van gebruikersaccounts die aan het bedrijf zijn gekoppeld, is ingesteld op `Inactive` en de bedrijfs-id wordt verwijderd uit de profielen van gebruikersaccounts. Informatie over bedrijfsactiviteiten en transacties wordt in het systeem bewaard.

1. Selecteer **[!UICONTROL Delete]** in het besturingselement **[!UICONTROL Actions]** .

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

### Bedrijfsinstellingen wijzigen

Werk de [ Geavanceerde configuratie van Montages ](account-company-create.md#advanced-settings) bij om de zelfde montages op veelvoudige bedrijven toe te passen die op het *net van Bedrijven* worden geselecteerd.

>[!NOTE]
>
>Beheer de geavanceerde montageconfiguratie voor een bedrijforganisatie met een ouder en bijbehorende kindbedrijven van de [ mening van de Hiërarchie van het Bedrijf ](manage-company-hierarchy.md#change-company-settings).

1. Selecteer **[!UICONTROL Change company settings]** in het besturingselement **[!UICONTROL Actions]** .

   In het *[!UICONTROL Change company settings]* -formulier worden de initiële configuratie-instellingen ingesteld op de standaardwaarden.

1. Voor elke configuratie die moet worden gewijzigd, schakelt u het selectievakje **[!UICONTROL Change]** in om de instelling in te schakelen. Werk de instelling vervolgens naar wens bij.

   ![ bedrijfmontages van de Verandering voor veelvoudige bedrijven ](assets/companies-change-advanced-settings-action.png){width="675" zoomable="yes"}

1. Selecteer **[!UICONTROL Apply Changes]** nadat u de configuratie-instellingen hebt bijgewerkt.

1. Wanneer ertoe aangezet, selecteer **[!UICONTROL Change settings]** om de configuratie voor de geselecteerde bedrijven bij te werken.

>[!TIP]
>
>U kunt de geavanceerde montageconfiguratie voor één enkel bedrijf veranderen door **[!UICONTROL Edit]** in de **[!UICONTROL Action]** kolom voor het verslag van de bedrijfrekening te selecteren.

### De creditvaluta converteren

Het krediet in de rekeningen van geselecteerde ondernemingen wordt omgezet in de actuele koers van de geselecteerde valuta.

1. Selecteer **[!UICONTROL Convert Currency]** in het besturingselement **[!UICONTROL Actions]** .

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

1. Kies de **[!UICONTROL Credit Currency]** die voor de geselecteerde bedrijfsaccounts moet worden gebruikt.

   De bedragen worden herberekend volgens de huidige omrekeningskoersen, indien beschikbaar. Als deze optie niet beschikbaar is, kunt u handmatig aangepaste conversiesnelheden invoeren. Het systeem geeft zoveel conversieberekeningen weer als nodig zijn voor de creditvaluta die door de geselecteerde bedrijven wordt gebruikt.

1. Klik op **[!UICONTROL Proceed]** om de conversie te voltooien.

## Een bedrijfsaccount bewerken

Methode 1: **Snelle geeft uit**

1. Selecteer in de eerste kolom het selectievakje van de bedrijfsaccount die u wilt bewerken.

1. Selecteer **[!UICONTROL Edit]** in het besturingselement **[!UICONTROL Actions]** .

   Elke waarde die kan worden bijgewerkt, verschijnt in een tekstvak.

   ![ Snel geeft voor een bedrijfrekening ](./assets/companies-grid-quick-edit.png){width="675" zoomable="yes"} uit

1. Werk een van de volgende waarden naar wens bij:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Klik op **[!UICONTROL Save]**.

Methode 2: **Volledige geeft uit**

1. Zoek in het raster het bedrijfsrecord dat moet worden bewerkt.

1. Selecteer **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Breng de benodigde wijzigingen aan in de bedrijfsinformatie.

   Voor gebiedsbeschrijvingen, zie [ een bedrijfrekening ](account-company-create.md) creëren.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Een vertegenwoordiger toewijzen

De verkoopvertegenwoordiger is een [ gebruiker Admin ](../systems/permissions.md) die als punt van contact voor een bedrijfrekening wordt toegewezen en alle geautomatiseerde [ e-mailberichten ](../b2b/enable-basic-features.md#configure-company-email-options) met betrekking tot het bedrijf ontvangt. Per bedrijfsrekening kan slechts één vertegenwoordiger worden aangesteld, maar één enkele vertegenwoordiger kan meerdere bedrijfsrekeningen beheren. De standaardgebruikersaccount voor Admin wordt toegewezen als de vertegenwoordiger van de verkoper, tenzij een andere Admin-gebruiker wordt toegewezen.

De naam en het e-mailadres van de toegewezen vertegenwoordiger zijn voor de leden van het bedrijf zichtbaar vanaf de pagina met bedrijfsaccounts en aanhalingstekens.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek het bedrijf in het raster en open de bewerkingsmodus.

1. Stel **[!UICONTROL Sales Representative]** in op de Admin-gebruiker die u wilt toewijzen als contactpunt voor het bedrijf.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   De toegewezen verkoper ontvangt een e-mailmelding van de toewijzing.

## Een bedrijfsprofiel bijwerken

Het bedrijfsprofiel kan van de winkel door de bedrijfbeheerder, en ook van Admin door een opslagbeheerder worden gehandhaafd.

](./assets/company-update.png){width="700" zoomable="yes"} Profiel van 0} Bedrijf![

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek het bedrijf in het raster en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Werk de veldwaarden in elke sectie zo nodig bij met de veldbeschrijvingen ter referentie.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Bedrijfsaccountdemo

U kunt meer leren over het beheren van bedrijfsaccounts door naar deze video te kijken:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Bedrijfsbeheer

Nadat een bedrijf is gemaakt, kunnen Admin-gebruikers met de juiste machtigingen de sectie [!UICONTROL Company Hierarchy] gebruiken om een organisatie van het moederbedrijf te maken door het aangewezen moederbedrijf te bewerken en verwante bedrijven toe te wijzen.

Als een bedrijf aan een hiërarchie is toegevoegd, toont het [!UICONTROL Company Hierarchy] net het moederbedrijf en alle toegewezen bedrijven in het net.

Zie [ bedrijfshiërarchie ](manage-company-hierarchy.md) voor meer informatie beheren.

## Bedrijfsopties en -kolommen

In de volgende secties vindt u een verwijzing naar de beschikbare acties, opties en weergegeven informatie die beschikbaar is voor het beheer van bedrijfsaccounts.

### Handelingenbesturingsopties

| Optie | Beschrijving |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Hiermee wordt de status van alle geselecteerde bedrijfsrecords ingesteld op `Active` . De beheerders van het bedrijf ontvangen instructies om hun wachtwoorden te plaatsen zodat kunnen zij tot hun rekeningen toegang hebben en hun bedrijven van de winkel beheren. |
| [!UICONTROL Block] | Beperkt bedrijfsrekeningen die niet in goede staat zijn, terwijl het bewaren van de rekening. De leden van het bedrijf kunnen login en tot de catalogus toegang hebben, maar zij kunnen geen orden namens het bedrijf plaatsen. |
| [!UICONTROL Delete] | Hiermee verwijdert u geselecteerde bedrijfsaccounts. De status van gebruikersaccounts die aan een verwijderd bedrijf zijn gekoppeld, is ingesteld op `Inactive` en de bedrijfs-id wordt verwijderd uit de profielen van gebruikersaccounts. Informatie over bedrijfsactiviteiten en transacties wordt in het systeem bewaard. |
| [!UICONTROL Edit] | Hiermee kunnen bepaalde waarden van het geselecteerde bedrijfsrecord worden bewerkt in het raster. Standaard zijn de waarden Bedrijfsnaam, E-mail van het bedrijf en Telefoonnummer beschikbaar voor een snelle bewerking. |
| [!UICONTROL Change company settings] | Opent de *bedrijfmontages van de Verandering* vorm om de [ Geavanceerde montages ](account-company-create.md#advanced-settings) configuratie bij te werken en de veranderingen op de geselecteerde bedrijven toe te passen. |
| [!UICONTROL Convert Credit] | Hiermee wordt het krediet voor de geselecteerde ondernemingen geconverteerd naar de koers van de opgegeven valuta. |

{style="table-layout:auto"}

### Kolombeschrijvingen


#### Standaardkolomindeling

| Kolom | Beschrijving |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Schakel selectievakjes in om bedrijfsrecords te selecteren die het onderwerp van een handeling moeten zijn of gebruik het selectiegereedschap in de kolomkop om alles in of uit te schakelen. |
| [!UICONTROL ID] | Een unieke numerieke id die wordt toegewezen wanneer het verzoek om een bedrijf te maken wordt ingediend. |
| [!UICONTROL Company Name] | De bedrijfsnaam wordt ingevoerd wanneer het bedrijfsaccount voor het eerst wordt gemaakt en kan een verkorte versie van de volledige juridische naam zijn. |
| [!UICONTROL Company Type] | Het type van [ bedrijf ](manage-companies.md). Opties: <br/>**[!UICONTROL Company]**- Nieuwe bedrijven worden standaard als afzonderlijke bedrijven gemaakt.<br/>**[!UICONTROL Parent]** - Het bedrijf is een moedermaatschappij van andere bedrijven. <br/>**[!UICONTROL Child]**- Dit bedrijf is verbonden met een moedermaatschappij. |
| [!UICONTROL Parent] | Toont het moederbedrijf voor deze specifieke bedrijfslijn. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Phone Number] | Het primaire telefoonnummer van het bedrijf. |
| [!UICONTROL Country] | Het land waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL State Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL City] | De stad waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL Group/Shared Catalog] | De kolomnaam hangt af van of de Gedeelde Catalogus in de configuratie wordt toegelaten. Opties: <br/>**[!UICONTROL Customer Group]**- als de Gedeelde Catalogus niet in de configuratie wordt toegelaten, specificeert de naam van de [ klantengroep ](../customers/customer-groups.md) waartot het bedrijf behoort.<br/>**[!UICONTROL Shared Catalog]** - Als Gedeelde Catalogus in de configuratie wordt toegelaten, specificeert de naam van de gedeelde catalogus die aan de klant wordt toegewezen. |
| [!UICONTROL Outstanding Balance] | Het uitstaande saldo op de bedrijfsrekening. de kolom is leeg als de onderneming geen kredietgeschiedenis heeft en haar kredietlimiet nul is. |
| [!UICONTROL Company Admin] | De voornaam en achternaam van de bedrijfsbeheerder. |
| [!UICONTROL Job Title] | De functie van de bedrijfbeheerder. |
| [!UICONTROL Work Phone Number] | Het aantal van de het werktelefoon van de bedrijfbeheerder. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfsbeheerder. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Opent het bedrijfsaccount in de bewerkingsmodus. |

{style="table-layout:auto"}

#### Aanvullende kolommen

De volgende kolommen zijn beschikbaar door de [ kolomlay-out ](../getting-started/admin-grid-controls.md) van het net te veranderen.

| Kolom | Beschrijving |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | De volledige wettelijke naam van de onderneming. |
| [!UICONTROL Street Address] | Het adres van de straat waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL ZIP] | De postcode of postcode waar de onderneming geregistreerd is om zaken te doen. |
| [!UICONTROL Reseller ID] | Het wederverkoopnummer dat aan de onderneming wordt toegekend voor belastingverslagleggingsdoeleinden. |
| [!UICONTROL VAT/TAX ID] | Het [ waarde-toegevoegde belasting ](../stores-purchase/vat.md) aantal dat aan het bedrijf door sommige jurisdicties voor belastingrapporteringsdoeleinden wordt toegewezen. Om de klant BTW/identiteitskaart van de BELASTING te vormen om in de storefront te verschijnen, zie [ Nieuwe Opties van de Rekening ](../configuration-reference/customers/customer-configuration.md) creëren. |
| [!UICONTROL Credit Limit] | De kredietlimiet die tot de bedrijfsrekening wordt uitgebreid. |
| [!UICONTROL Credit Currency] | De valuta die door de winkel wordt geaccepteerd voor aankopen op bedrijfskrediet. |
| [!UICONTROL Status] | Wijst op de [ status ](account-company-approve.md) van de bedrijfrekening. Opties: <br/>**[!UICONTROL Active]**- Het bedrijfsaccount wordt goedgekeurd door de beheerder van de winkel. De bedrijfsbeheerder en geassocieerde leden kunnen zich bij de winkel aanmelden en aankopen doen.<br/>**[!UICONTROL Pending Approval]** - Er is een verzoek ingediend om een bedrijfsaccount te openen, maar dit is nog niet goedgekeurd door de beheerder van de winkel. <br/>**[!UICONTROL Rejected]**- Een verzoek om een bedrijfsaccount te openen is ingediend, maar niet goedgekeurd door de beheerder van de winkel. De initiële aanmeldingsgegevens die zijn gebruikt om het verzoek in te dienen, worden geblokkeerd.<br/>**[!UICONTROL Blocked]** - Bedrijfsleden kunnen zich aanmelden en toegang krijgen tot de catalogus, maar kunnen geen aankopen doen. De opslagbeheerder zou een bedrijfrekening kunnen blokkeren die niet in goede staat is. Het blok op de rekening kan door de opslagbeheerder op elk ogenblik worden verwijderd. |
| [!UICONTROL Gender] | Het geslacht van de bedrijfsbeheerder. Opties: Mannelijk / Vrouwelijk / Niet opgegeven |
| [!UICONTROL Comment] | Opmerkingen over de bedrijfsaccount ter referentie en zijn alleen zichtbaar vanuit de beheerder. |

{style="table-layout:auto"}

### Knopbalk

| Knop | Beschrijving |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Companies zonder de wijzigingen op te slaan. |
| [!DNL Delete Company] | Hiermee verwijdert u het bedrijfsaccount. De status van gebruikersaccounts die aan het bedrijf zijn gekoppeld, is ingesteld op `Inactive` en de bedrijfs-id wordt verwijderd uit de profielen van gebruikersaccounts. Informatie over bedrijfsactiviteiten en transacties wordt in het systeem bewaard. |
| [!DNL Reset] | Hiermee herstelt u de oorspronkelijke waarden in alle velden met niet-opgeslagen wijzigingen. |
| [!DNL Reimburse Balance] | Staat de beheerder toe om het saldo van opslagkrediet terug te betalen, dat door het aantal van de PO wordt van verwijzingen voorzien. |
| [!DNL Save] | Hiermee slaat u wijzigingen op in het bedrijf en houdt u het profiel open. |
| [!UICONTROL Save & Close] | Hiermee slaat u wijzigingen op in het bedrijf en sluit u het profiel. |

{style="table-layout:auto"}

### Veldomschrijvingen

| Veld | Beschrijving |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | De bedrijfsnaam wordt ingevoerd wanneer het bedrijfsaccount voor het eerst wordt gemaakt en kan een verkorte versie van de volledige juridische naam zijn. |
| [!UICONTROL Status] | Wijst op de [ status ](account-company-approve.md) van de bedrijfrekening. Opties: <br/>**[!UICONTROL Active]**- Het bedrijfsaccount wordt goedgekeurd door de beheerder van de winkel. De bedrijfsbeheerder en geassocieerde leden kunnen zich bij de winkel aanmelden en aankopen doen.<br/>**[!UICONTROL Pending Approval]** - Er is een verzoek ingediend om een bedrijfsaccount te openen, maar dit is nog niet goedgekeurd door de beheerder van de winkel. <br/>**[!UICONTROL Rejected]**- Een verzoek om een bedrijfsaccount te openen is ingediend, maar niet goedgekeurd door de beheerder van de winkel. De initiële aanmeldingsgegevens die zijn gebruikt om het verzoek in te dienen, worden geblokkeerd.<br/>**[!UICONTROL Blocked]** - Bedrijfsleden kunnen zich aanmelden en toegang krijgen tot de catalogus, maar kunnen geen aankopen doen. De opslagbeheerder zou een bedrijfrekening kunnen blokkeren die niet in goede staat is. Het blok op de rekening kan door de opslagbeheerder op elk ogenblik worden verwijderd. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Sales Representative] | De Admin-gebruiker die de primaire contactpersoon voor het bedrijfsaccount is. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Veld | Beschrijving |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | De volledige wettelijke naam van de onderneming. |
| [!UICONTROL VAT / TAX ID] | De belasting of [ toegevoegde belasting ](../stores-purchase/vat.md) aantal dat aan het bedrijf voor belasting meldende doeleinden wordt toegewezen. |
| [!UICONTROL Reseller ID] | Het wederverkoopnummer dat aan de onderneming wordt toegekend voor belastingverslagleggingsdoeleinden. |
| [!UICONTROL Comment] | Deze opmerkingen over de bedrijfsaccount zijn ter referentie en zijn alleen zichtbaar vanuit de beheerder. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Kolommen | Beschrijving |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Het ID-nummer van het bedrijf. |
| [!UICONTROL Company Name] | De volledige naam van de onderneming. <br/> A `current company indicator` verschijnt in de bedrijflijn die wordt uitgegeven. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Phone Number] | Het primaire telefoonnummer van het bedrijf. |
| [!UICONTROL State/Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL City] | De stad waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL Customer Group] | (Admin slechts) wijst op de [ klantengroep ](../customers/customer-groups.md) of [ gedeelde catalogus ](catalog-shared.md) die aan het bedrijf wordt toegewezen. |
| [!UICONTROL Company Admin] | De volledige naam van de bedrijfbeheerder. |
| [!UICONTROL Action] | De lijst van mogelijke acties voor die bedrijfslijn. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| Kolommen | Beschrijving |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Het adres van de straat waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL City] | De stad waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL Country] | Het land waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL State/Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL ZIP/Postal Code] | De postcode of postcode waar de onderneming geregistreerd is om zaken te doen. |
| [!UICONTROL Phone Number] | Het primaire telefoonnummer van het bedrijf. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Veld | Beschrijving |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Plaats het [ websitewerkingsgebied ](../getting-started/websites-stores-views.md) voor de bedrijfrekening. Wordt standaard ingesteld op *[!UICONTROL Main Website]* . |
| [!UICONTROL Job Title] | De titel van de bedrijfsbeheerder die de bedrijfsaccount beheert. |
| [!UICONTROL Work Phone Number] | Het telefoonaantal van de bedrijfbeheerder die de bedrijfrekening beheert. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfsbeheerder kan hetzelfde zijn als het e-mailadres van het bedrijf. Als u een ander e-mailadres opgeeft, wordt naast het bedrijfsaccount een aparte account voor de beheerder van het bedrijf gemaakt. |
| [!UICONTROL Prefix] | Indien van toepassing, het voorvoegsel dat is gekoppeld aan de naam van de bedrijfsbeheerder (bijvoorbeeld `Mr.` , `Ms.` , `Mrs.` of `Dr.` ). Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL First Name] | De voornaam van de bedrijfbeheerder. |
| [!UICONTROL Middle Name/Initial] | De middelste naam of de aanvankelijke naam van de bedrijfbeheerder. |
| [!UICONTROL Last Name] | De achternaam van de bedrijfsbeheerder. |
| [!UICONTROL Suffix] | Indien van toepassing, het achtervoegsel dat aan de naam van de bedrijfbeheerder (zoals `Jr.`, `Sr.`, of `III`) wordt geassocieerd. Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL Gender] | Het geslacht van de bedrijfsbeheerder. Opties: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | Stel de storeview in die u wilt gebruiken wanneer u de welkomstmail naar de nieuwe bedrijfsbeheerder verzendt als u de *[!UICONTROL Default Store View]* niet wilt gebruiken. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Veld | Beschrijving |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | De valuta die door de winkel wordt geaccepteerd voor aankopen op bedrijfskrediet. |
| [!UICONTROL Credit Limit] | De kredietlimiet die tot de bedrijfsrekening wordt uitgebreid. |
| [!UICONTROL Allow to Exceed Credit Limit] | Geeft aan of de onderneming toestemming heeft om de kredietlimiet te overschrijden. Opties: Ja/Nee |
| [!UICONTROL Reason for Change] | Een toelichting waarin de omstandigheden worden toegelicht waarin de onderneming de kredietlimiet al dan niet kan overschrijden. Dit veld is alleen actief als de toestemming om de kredietlimiet te overschrijden wordt gewijzigd. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Veld | Beschrijving |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Wijst op de [ klantengroep ](../customers/customer-groups.md) of [ gedeelde catalogus ](catalog-shared.md) die aan het bedrijf wordt toegewezen. |
| [!UICONTROL Allow Quotes] | Hiermee wordt bepaald of leden van het bedrijf namens de onderneming verhandelbare noteringen kunnen opstellen en indienen. |
| [!UICONTROL Enable Purchase Orders] | Hiermee wordt bepaald of inkooporders zijn toegestaan voor het bedrijf. Voor kooporders om voor de rekeningen van het bedrijflid te functioneren, moet de bedrijfbeheerder deze eigenschap op de opslagplaats ook toelaten. |
| [!UICONTROL Applicable Payment Methods] | Geeft de betalingsmethoden aan die beschikbaar zijn voor aankopen door bedrijven. Opties: `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Alleen beheerder) Wordt actief als specifieke betalingsmethoden worden aangegeven. Als u meerdere betalingsmethoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie. |

{style="table-layout:auto"}
