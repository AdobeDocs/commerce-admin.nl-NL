---
title: Bedrijfsrekeningen
description: Ontdek hoe bedrijfsaccounts die in je Adobe Commerce-winkel worden beheerd, het mogelijk maken om meerdere kopers die tot hetzelfde bedrijf behoren, tot één bedrijfsaccount te laten samenvoegen.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Bedrijfsrekeningen

Wanneer u B2B bedrijfsrekeningen in uw opslag opneemt, kunt u de collectieve het winkelen ervaring vereenvoudigen door bedrijven toe te laten om veelvoudige subaccounts met flexibele toestemmingen tot stand te brengen die op gebruikersrollen in hun organisatie worden gebaseerd. Afhankelijk van het bedrijf, kan een opslagbeheerder bevorderingen en prijzen aanpassen om hun behoeften aan te passen, en hoogst aangepaste aanbiedingen tot stand brengen die aan de eisen van de kopers voldoen en orden verhogen. Het toevoegen van een vereniging van de bedrijfrekening aan een standaard [ individu ](../customers/account-create.md) staat de klant toe om de specifieke die koopgewerkschema&#39;s te gebruiken voor het bedrijf worden bepaald.

Voordelen van een bedrijfsaccount:

- Biedt onbeperkte [ bedrijfgebruikers ](account-company-users.md) en de verwezenlijking van extra rekeningen aan, die collectieve aankopen vereenvoudigt.

- Omvat steun voor de hiërarchie van de a _slimme_ bedrijfrekening met verschillende [ rollen en toestemmingen ](account-company-roles-permissions.md) voor het plaatsen van orden.

- Verstrekt een mechanisme voor handelaren om inkomen te verhogen door [ bedrijfsleekrediet ](credit-company.md) als betalingsmethode aan te bieden.

- Steunt het [ beheer ](account-company-manage.md) van alle bedrijfrekeningen in Admin.

## Zakelijke accounts weergeven

Het _net van bedrijven van 0} {{maakt een lijst van alle actieve bedrijfrekeningen en hangende verzoeken, ongeacht status het plaatsen._ Het verstrekt ook de hulpmiddelen voor [ het creëren van ](account-company-create.md) en [ het leiden ](account-company-manage.md) bedrijfsrekeningen. Gebruik de standaardrasterbesturingselementen om de lijst te filteren en de kolomlay-out aan te passen. Voor een lijst van kolombeschrijvingen, zie de _sectie van de Beschrijvingen van de Kolom_ in [ het Leiden de Rekeningen van het Bedrijf ](account-company-manage.md).

Klanten kunnen een bedrijfsaccount maken op basis van de winkel of een handelaar kan een account maken op basis van de beheerder. Door gebrek, wordt de capaciteit om bedrijfrekeningen van de opslag tot stand te brengen toegelaten. Als de configuratie dit toestaat, kan een bezoeker van de winkel een aanvraag indienen om een bedrijfsaccount te openen. Nadat de bedrijfsrekening wordt goedgekeurd, kan de bedrijfbeheerder de bedrijfstructuur en gebruikers met diverse niveaus van toestemming opstelling.

In _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![ het Net van Bedrijven ](./assets/companies-grid.png){width="700" zoomable="yes"}

In het raster [!UICONTROL Companies] worden alle bedrijven weergegeven, ongeacht hun status. In het weergegeven voorbeeld ziet u de accounts van twee bedrijven: het ACME-bedrijf en het Vandelay-bedrijf.

## Bedrijfsleider

Het volgende voorbeeld toont het _netwerk van Klanten_ met de aanvankelijke rekeningen van de bedrijfbeheerder.

![ het net van Klanten met de rekening van de bedrijfbeheerder ](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Het is mogelijk dat de persoon die als bedrijfbeheerder dienst heeft veelvoudige rollen binnen het bedrijf heeft. Als een afzonderlijk e-mailadres voor de bedrijfbeheerder is ingegaan, omvat de aanvankelijke bedrijfstructuur de bedrijfbeheerder plus een individuele gebruikersrekening in de naam van de bedrijfbeheerder. In dat geval kan de beheerder van het bedrijf zich aanmelden bij de account als bedrijf of als individuele gebruiker.

Na het creëren van de rekening, bepaalt de bedrijfbeheerder de bedrijfstructuur van [ teams ](account-company-structure.md), plaatst - omhoog de [ bedrijfgebruikers ](account-company-users.md), en vestigt [ rollen en toestemmingen ](account-company-roles-permissions.md) voor elk.

### Wachtwoord voor bedrijfsbeheerder instellen voor eerste aanmelding

1. De bedrijfbeheerder vindt een welkome e-mail van de opslag.

   ![ E-mail van het Welkome E-mail van het Voorbeeld ](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >De e-mailadresdoelstellingen en de inhoud van e-mail worden bepaald door de opties die in de [ bedrijf e-mailopties ](email-company-configuration.md) configuratie worden gespecificeerd.

1. Volgt de instructies en klikt [!UICONTROL **verbinding**] om hun wachtwoord te plaatsen.

1. Keert a [!UICONTROL **Nieuw Wachtwoord**] voor hun rekening en opnieuw in om te bevestigen.

   Het wachtwoord moet ten minste drie van de volgende tekentypen bevatten:

   - Kleine letters (abc...)
   - Hoofdletters (ABC...)
   - Getallen (1234567890)
   - Speciale tekens (!@#$...)

1. Klik [!UICONTROL **plaatsen een Nieuw Wachtwoord**].

   ![ Login van de Klant - bedrijf admin ](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Wanneer de [!UICONTROL Customer Login] pagina verschijnt, gaat de klant hun [!UICONTROL **E-mail**] en [!UICONTROL **Wachtwoord**] in.

1. Klik [!UICONTROL **binnen Teken**] om tot hun rekeningsdashboard toegang te hebben.

   ![ Dashboard van de Rekening - bedrijf ](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Bedrijfsstructuur

Een bedrijfsrekening kan worden opgezet om de structuur van de onderneming te weerspiegelen. Aanvankelijk, omvat de bedrijfsstructuur slechts de bedrijfbeheerder, maar kan worden uitgebreid om teams van gebruikers te omvatten. De gebruikers kunnen met teams worden geassocieerd of binnen een hiërarchie van afdelingen en onderverdelingen binnen het bedrijf worden georganiseerd. De structuur wordt ontworpen om het gebruik van [ goedkeuringsregels ](account-dashboard-approval-rules.md) voor [ kooporden ](purchase-order-flow.md) (POs) te steunen verbonden aan de bedrijfrekening.

![ Structuur van het Bedrijf met Afdelingen ](./assets/company-structure-diagram.svg){width="450"}

In het de rekeningsdashboard van de bedrijfbeheerder, wordt de bedrijfstructuur vertegenwoordigd als boom en bestaat aanvankelijk uit slechts de bedrijfbeheerder.

![ Structuur van het Bedrijf met de Beheerder van het Bedrijf ](./assets/company-structure-tree-admin.png){width="600"}

Wanneer de account is gemaakt, kan de bedrijfsbeheerder het e-mailadres van het bedrijf gebruiken of een ander e-mailadres krijgen toegewezen.

In het volgende voorbeeld bevat de initiële bedrijfsstructuur de bedrijfsbeheerder plus een individuele gebruikersaccount in de naam van de bedrijfsbeheerder. Maar de functies van de bedrijfbeheerder (zoals bedrijfsstructuur en goedkeuringsregels) zijn beschikbaar slechts wanneer zij aan de gebruikersrekening worden het programma geopend die als bedrijfbeheerder wordt aangewezen.

![ Structuur van het Bedrijf met Beheerder en Rekening van de Gebruiker ](./assets/company-structure-tree-admin-user.png){width="600"}
