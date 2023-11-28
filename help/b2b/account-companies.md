---
title: Bedrijfsrekeningen
description: Ontdek hoe bedrijfsaccounts die in je Adobe Commerce-winkel worden beheerd, het mogelijk maken om meerdere kopers die tot hetzelfde bedrijf behoren, tot één bedrijfsaccount te laten samenvoegen.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Bedrijfsrekeningen

Wanneer u B2B bedrijfsrekeningen in uw opslag opneemt, kunt u de collectieve het winkelen ervaring vereenvoudigen door bedrijven toe te laten om veelvoudige subaccounts met flexibele toestemmingen tot stand te brengen die op gebruikersrollen in hun organisatie worden gebaseerd. Afhankelijk van het bedrijf, kan een opslagbeheerder bevorderingen en prijzen aanpassen om hun behoeften aan te passen, en hoogst aangepaste aanbiedingen tot stand brengen die aan de eisen van de kopers voldoen en orden verhogen. Een bedrijfsaccountvereniging aan een standaard toevoegen [individueel](../customers/account-create.md) staat de klant toe om de specifieke koopgewerkschema&#39;s te gebruiken die voor het bedrijf worden bepaald.

Voordelen van een bedrijfsaccount:

- Aanbiedingen onbeperkt [bedrijfsgebruikers](account-company-users.md) en het aanmaken van extra rekeningen, waardoor aankopen door bedrijven worden vereenvoudigd.

- Bevat ondersteuning voor een _slim_ hiërarchie van bedrijfsaccounts met verschillende [rollen en machtigingen](account-company-roles-permissions.md) voor het plaatsen van orders.

- Verstrekt een mechanisme voor handelaren om inkomen te verhogen door aan te bieden [bedrijfslabel](credit-company.md) als betalingsmethode.

- Ondersteunt de [management](account-company-manage.md) van alle bedrijfsrekeningen in de Admin.

## Zakelijke accounts weergeven

De _Bedrijven_ het net maakt een lijst van alle actieve bedrijfsrekeningen en hangende verzoeken, ongeacht status het plaatsen. Het verstrekt ook de hulpmiddelen voor [maken](account-company-create.md) en [beheren](account-company-manage.md) bedrijfsrekeningen. Gebruik de standaardrasterbesturingselementen om de lijst te filteren en de kolomlay-out aan te passen. Voor een lijst met kolombeschrijvingen raadpleegt u de _Kolombeschrijvingen_ sectie in [Bedrijfsaccounts beheren](account-company-manage.md).

Klanten kunnen een bedrijfsaccount maken op basis van de winkel of een handelaar kan een account maken op basis van de beheerder. Door gebrek, wordt de capaciteit om bedrijfrekeningen van de opslag tot stand te brengen toegelaten. Als de configuratie dit toestaat, kan een bezoeker van de winkel een aanvraag indienen om een bedrijfsaccount te openen. Nadat de bedrijfsrekening wordt goedgekeurd, kan de bedrijfbeheerder de bedrijfstructuur en gebruikers met diverse niveaus van toestemming opstelling.

In de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Companies Grid](./assets/companies-grid.png){width="700" zoomable="yes"}

De [!UICONTROL Companies] in het raster worden alle bedrijven vermeld , ongeacht hun status . In het weergegeven voorbeeld ziet u de accounts van twee bedrijven: het ACME-bedrijf en het Vandelay-bedrijf.

## Bedrijfsleider

In het volgende voorbeeld wordt het _Klanten_ net met de aanvankelijke rekeningen van de bedrijfbeheerder.

![Het net van klanten met de rekening van de bedrijfbeheerder](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Het is mogelijk dat de persoon die als bedrijfbeheerder dienst heeft veelvoudige rollen binnen het bedrijf heeft. Als een afzonderlijk e-mailadres voor de bedrijfbeheerder is ingegaan, omvat de aanvankelijke bedrijfstructuur de bedrijfbeheerder plus een individuele gebruikersrekening in de naam van de bedrijfbeheerder. In dat geval kan de beheerder van het bedrijf zich aanmelden bij de account als bedrijf of als individuele gebruiker.

Na het creëren van de rekening, bepaalt de bedrijfbeheerder de bedrijfstructuur van [teams](account-company-structure.md), stelt de [bedrijfsgebruikers](account-company-users.md)en [rollen en machtigingen](account-company-roles-permissions.md) voor elk.

### Wachtwoord voor bedrijfsbeheerder instellen voor eerste aanmelding

1. De bedrijfbeheerder vindt een welkome e-mail van de opslag.

   ![Welkom-e-mail](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >De e-mailadresdoelstellingen en de inhoud van het e-mailbericht worden bepaald door de opties die in het dialoogvenster [e-mailopties voor bedrijven](email-company-configuration.md) configuratie.

1. Volg de instructies en klik op [!UICONTROL **link**] om hun wachtwoord in te stellen.

1. Voert een [!UICONTROL **Nieuw wachtwoord**] ter bevestiging van hun account.

   Het wachtwoord moet ten minste drie van de volgende tekentypen bevatten:

   - Kleine letters (abc...)
   - Hoofdletters (ABC...)
   - Getallen (1234567890)
   - Speciale tekens (!@#$...)

1. Klikken [!UICONTROL **Een nieuw wachtwoord instellen**].

   ![Aanmelden bij klant - bedrijfsbeheerder](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Wanneer de [!UICONTROL Customer Login] pagina wordt weergegeven, voert de klant zijn of haar [!UICONTROL **E-mail**] en [!UICONTROL **Wachtwoord**].

1. Klikken [!UICONTROL **Aanmelden**] om hun accountdashboard te openen.

   ![Accountdashboard - bedrijf](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Bedrijfsstructuur

Een bedrijfsrekening kan worden opgezet om de structuur van de onderneming te weerspiegelen. Aanvankelijk, omvat de bedrijfsstructuur slechts de bedrijfbeheerder, maar kan worden uitgebreid om teams van gebruikers te omvatten. De gebruikers kunnen met teams worden geassocieerd of binnen een hiërarchie van afdelingen en onderverdelingen binnen het bedrijf worden georganiseerd. De structuur is ontworpen om het gebruik van [goedkeuringsregels](account-dashboard-approval-rules.md) for [inkooporders](purchase-order-flow.md) (POs) verbonden aan de bedrijfsrekening.

![Bedrijfsstructuur met afdelingen](./assets/company-structure-diagram.svg){width="450"}

In het de rekeningsdashboard van de bedrijfbeheerder, wordt de bedrijfstructuur vertegenwoordigd als boom en bestaat aanvankelijk uit slechts de bedrijfbeheerder.

![Bedrijfsstructuur met bedrijfsbeheerder](./assets/company-structure-tree-admin.png){width="600"}

Wanneer de account is gemaakt, kan de bedrijfsbeheerder het e-mailadres van het bedrijf gebruiken of een ander e-mailadres krijgen toegewezen.

In het volgende voorbeeld bevat de initiële bedrijfsstructuur de bedrijfsbeheerder plus een individuele gebruikersaccount in de naam van de bedrijfsbeheerder. Maar de functies van de bedrijfbeheerder (zoals bedrijfsstructuur en goedkeuringsregels) zijn beschikbaar slechts wanneer zij aan de gebruikersrekening worden het programma geopend die als bedrijfbeheerder wordt aangewezen.

![Bedrijfsstructuur met Beheerder- en gebruikersaccount](./assets/company-structure-tree-admin-user.png){width="600"}
