---
title: Bedrijfsaccounts beheren
description: Leer bedrijfsaccounts voor je Adobe Commerce-winkel beheren met behulp van de pagina Companies en de tools die beschikbaar zijn in het raster.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '2706'
ht-degree: 0%

---

# Bedrijfsaccounts beheren

De pagina _[!UICONTROL Companies]_bevat een lijst met alle huidige bedrijfsaccounts, ongeacht de status. Eventuele lopende goedkeuringsaanvragen staan boven aan de lijst.

![](./assets/companies-grid-view.png){width="700" zoomable="yes"}

*[!UICONTROL Columns]* Customize the companies displayed in the view using the search and filter capabilities.

- ****_[!UICONTROL Search]_********

- [!UICONTROL Filter] [](manage-companies.md)`[!UICONTROL Company Type - Company]``[!UICONTROL Company Type - Parent]`

_[!UICONTROL Actions]_For example, rather than approving each individual company request, you can select multiple requests to activate the accounts in a single action. [](../systems/permissions.md)

## Bronnen voor bedrijfsrollen

De [ montages van de Middelen van de Rol ](../systems/permissions-user-roles.md#role-resources) bepalen de capaciteit om:

- Een bedrijf toevoegen
- Een bedrijf verwijderen
- Saldo-terugbetaling toepassen
- View companies

[](../systems/permissions-user-roles.md)

## Manage company accounts from the Companies grid

**[!UICONTROL Customers]****[!UICONTROL Companies]***[!UICONTROL Companies]*

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

Deleted company accounts cannot be restored. `Inactive` Information about company activity and transactions is retained in the system.

1. **[!UICONTROL Actions]****[!UICONTROL Delete]**

1. **[!UICONTROL OK]**

### Change company settings

[](account-company-create.md#advanced-settings)**

>[!NOTE]
>
>[](manage-company-hierarchy.md#change-company-settings)

1. **[!UICONTROL Actions]****[!UICONTROL Change company settings]**

   *[!UICONTROL Change company settings]*

1. **[!UICONTROL Change]** Then, update the setting as needed.

   ![ bedrijfmontages van de Verandering voor veelvoudige bedrijven ](assets/companies-change-advanced-settings-action.png){width="675" zoomable="yes"}

1. Selecteer **[!UICONTROL Apply Changes]** nadat u de configuratie-instellingen hebt bijgewerkt.

1. Wanneer ertoe aangezet, selecteer **[!UICONTROL Change settings]** om de configuratie voor de geselecteerde bedrijven bij te werken.

>[!TIP]
>
>U kunt de geavanceerde montageconfiguratie voor één enkel bedrijf veranderen door **[!UICONTROL Edit]** in de **[!UICONTROL Action]** kolom voor het verslag van de bedrijfrekening te selecteren.

### De creditvaluta converteren

Het krediet in de rekeningen van geselecteerde ondernemingen wordt omgezet in de actuele koers van de geselecteerde valuta.

1. Selecteer **[!UICONTROL Convert Currency]** in het besturingselement **[!UICONTROL Actions]** .

1. **[!UICONTROL OK]**

1. **[!UICONTROL Credit Currency]**

   The amounts are recalculated according to the current conversion rates, if available. If not available, you can manually enter custom conversion rates. The system displays as many conversion calculations are needed for the credit currency that is used by the selected companies.

1. **[!UICONTROL Proceed]**

## Edit a company account

Methode 1: **Snelle geeft uit**

1. Selecteer in de eerste kolom het selectievakje van de bedrijfsaccount die u wilt bewerken.

1. Selecteer **[!UICONTROL Edit]** in het besturingselement **[!UICONTROL Actions]** .

   Elke waarde die kan worden bijgewerkt, verschijnt in een tekstvak.

   ![ Snel geeft voor een bedrijfrekening ](./assets/companies-grid-quick-edit.png){width="675" zoomable="yes"} uit

1. Update any of the following values as needed:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Klik op **[!UICONTROL Save]**.

****

1. In the grid, find the company record to be edited.

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

1. Update the field values in each section as needed using the field descriptions for reference.

1. **[!UICONTROL Save]**

## Company account demo

You can learn about managing company accounts by watching this video:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Company management

Nadat een bedrijf is gemaakt, kunnen Admin-gebruikers met de juiste machtigingen de sectie [!UICONTROL Company Hierarchy] gebruiken om een organisatie van het moederbedrijf te maken door het aangewezen moederbedrijf te bewerken en verwante bedrijven toe te wijzen.

Als een bedrijf aan een hiërarchie is toegevoegd, toont het [!UICONTROL Company Hierarchy] net het moederbedrijf en alle toegewezen bedrijven in het net.

[](manage-company-hierarchy.md)

## Company options and columns

The following sections provide a reference for the available actions, options, and displayed information available for managing company accounts.

### Actions control options

| Option | Description |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | `Active` Company administrators receive instructions to set their passwords so they can access their accounts and manage their companies from the storefront. |
| [!UICONTROL Block] | Restricts company accounts that are not in good standing, while preserving the account. Company members can log in and access the catalog, but they cannot place orders on behalf of the company. |
| [!UICONTROL Delete] | Deletes selected company accounts. `Inactive` Information about company activity and transactions is retained in the system. |
| [!UICONTROL Edit] | Allows some values of the selected company record to be edited from the grid. By default, the Company Name, Company Email, and Phone Number values are available for a quick edit. |
| [!UICONTROL Change company settings] | **[](account-company-create.md#advanced-settings) |
| [!UICONTROL Convert Credit] | Hiermee wordt het krediet voor de geselecteerde ondernemingen geconverteerd naar de koers van de opgegeven valuta. |

{style="table-layout:auto"}

### Kolombeschrijvingen


#### Standaardkolomindeling

| Kolom | Beschrijving |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Schakel selectievakjes in om bedrijfsrecords te selecteren die het onderwerp van een handeling moeten zijn of gebruik het selectiegereedschap in de kolomkop om alles in of uit te schakelen. |
| [!UICONTROL ID] | A unique numeric identifier that is assigned when the request to create a company is submitted. |
| [!UICONTROL Company Name] | The company name is entered when the company account is first created, and can be a shortened version of the full legal name. |
| [!UICONTROL Company Type] | [](manage-companies.md) <br/>**[!UICONTROL Company]**<br/>**[!UICONTROL Parent]** <br/>**[!UICONTROL Child]** |
| [!UICONTROL Parent] | Shows the parent company for this specific company line. |
| [!UICONTROL Company Email] | The email address that is associated with the company account. |
| [!UICONTROL Phone Number] | The primary phone number of the company. |
| [!UICONTROL Country] | Het land waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL State Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL City] | De stad waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL Group/Shared Catalog] | The column name depends on whether Shared Catalog is enabled in the configuration. <br/>**[!UICONTROL Customer Group]**[](../customers/customer-groups.md)<br/>**[!UICONTROL Shared Catalog]** |
| [!UICONTROL Outstanding Balance] | The outstanding balance on the company account. the column is blank if the company does not have a credit history, and its credit limit is zero. |
| [!UICONTROL Company Admin] | The first and last name of the company administrator. |
| [!UICONTROL Job Title] | The job title of the company administrator. |
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
| [!UICONTROL Status] | Wijst op de [ status ](account-company-approve.md) van de bedrijfrekening. Opties: <br/>**[!UICONTROL Active]**- Het bedrijfsaccount wordt goedgekeurd door de beheerder van de winkel. De bedrijfsbeheerder en geassocieerde leden kunnen zich bij de winkel aanmelden en aankopen doen.<br/>**[!UICONTROL Pending Approval]** - Er is een verzoek ingediend om een bedrijfsaccount te openen, maar dit is nog niet goedgekeurd door de beheerder van de winkel. <br/>**[!UICONTROL Rejected]**- Een verzoek om een bedrijfsaccount te openen is ingediend, maar niet goedgekeurd door de beheerder van de winkel. De initiële aanmeldingsgegevens die zijn gebruikt om het verzoek in te dienen, worden geblokkeerd.<br/>**[!UICONTROL Blocked]** - Bedrijfsleden kunnen zich aanmelden en toegang krijgen tot de catalogus, maar kunnen geen aankopen doen. The store administrator might block a company account that is not in good standing. The block on the account can be removed by the store administrator at any time. |
| [!UICONTROL Gender] | The gender of the company administrator. Options: Male / Female / Not Specified |
| [!UICONTROL Comment] | Notes about the company account for reference and visible only from the Admin. |

{style="table-layout:auto"}

### Button bar

| Knop | Beschrijving |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Companies zonder de wijzigingen op te slaan. |
| [!DNL Delete Company] | Deletes the company account. De status van gebruikersaccounts die aan het bedrijf zijn gekoppeld, is ingesteld op `Inactive` en de bedrijfs-id wordt verwijderd uit de profielen van gebruikersaccounts. Information about company activity and transactions is retained in the system. |
| [!DNL Reset] | Restores the original values to any fields with unsaved changes. |
| [!DNL Reimburse Balance] | Allows the administrator to reimburse the balance from store credit, referenced by PO number. |
| [!DNL Save] | Saves changes to the company and keeps the profile open. |
| [!UICONTROL Save & Close] | Saves changes to the company and closes the profile. |

{style="table-layout:auto"}

### Field descriptions

| Veld | Description |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | The company name is entered when the company account is first created, and can be a shortened version of the full legal name. |
| [!UICONTROL Status] | [](account-company-approve.md) <br/>**[!UICONTROL Active]**The company administrator and associated members can log in the account from the storefront and make purchases.<br/>**[!UICONTROL Pending Approval]** <br/>**[!UICONTROL Rejected]**The initial login credentials that were used to submit the request are blocked.<br/>**[!UICONTROL Blocked]** De opslagbeheerder zou een bedrijfrekening kunnen blokkeren die niet in goede staat is. Het blok op de rekening kan door de opslagbeheerder op elk ogenblik worden verwijderd. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Sales Representative] | De Admin-gebruiker die de primaire contactpersoon voor het bedrijfsaccount is. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Veld | Beschrijving |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | The full legal name of the company. |
| [!UICONTROL VAT / TAX ID] | [](../stores-purchase/vat.md) |
| [!UICONTROL Reseller ID] | The resale number that is assigned to the company for tax reporting purposes. |
| [!UICONTROL Comment] | These notes about the company account are for reference and visible only from the Admin. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Columns | Description |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | The ID number of the company. |
| [!UICONTROL Company Name] | The full name of the company. <br/> A `current company indicator` verschijnt in de bedrijflijn die wordt uitgegeven. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Phone Number] | Het primaire telefoonnummer van het bedrijf. |
| [!UICONTROL State/Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL City] | The city where the company is registered to conduct business. |
| [!UICONTROL Customer Group] | [](../customers/customer-groups.md)[](catalog-shared.md) |
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
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Plaats het [ websitewerkingsgebied ](../getting-started/websites-stores-views.md) voor de bedrijfrekening. Wordt standaard ingesteld op *[!UICONTROL Main Website]* . |
| [!UICONTROL Job Title] | De titel van de bedrijfsbeheerder die de bedrijfsaccount beheert. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfsbeheerder kan hetzelfde zijn als het e-mailadres van het bedrijf. Als u een ander e-mailadres opgeeft, wordt naast het bedrijfsaccount een aparte account voor de beheerder van het bedrijf gemaakt. |
| [!UICONTROL Prefix] | Indien van toepassing, het voorvoegsel dat is gekoppeld aan de naam van de bedrijfsbeheerder (bijvoorbeeld `Mr.` , `Ms.` , `Mrs.` of `Dr.` ). Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL First Name] | De voornaam van de bedrijfbeheerder. |
| [!UICONTROL Middle Name/Initial] | De middelste naam of de aanvankelijke naam van de bedrijfbeheerder. |
| [!UICONTROL Last Name] | The last name of the company administrator. |
| [!UICONTROL Suffix] | `Jr.``Sr.``III` Depending on the configuration, the input field might be a text field or list. |
| [!UICONTROL Gender] | The gender of the company administrator. `Male``Female``Not Specified` |
| [!UICONTROL Send Welcome Email From] | *[!UICONTROL Default Store View]* |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Field | Beschrijving |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | De valuta die door de winkel wordt geaccepteerd voor aankopen op bedrijfskrediet. |
| [!UICONTROL Credit Limit] | De kredietlimiet die tot de bedrijfsrekening wordt uitgebreid. |
| [!UICONTROL Allow to Exceed Credit Limit] | Geeft aan of de onderneming toestemming heeft om de kredietlimiet te overschrijden. Options: Yes / No |
| [!UICONTROL Reason for Change] | A note that explains the circumstances when the company can or cannot exceed the credit limit. This field is active only if the permission to exceed the credit limit changes. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Field | Description |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | [](../customers/customer-groups.md)[](catalog-shared.md) |
| [!UICONTROL Allow Quotes] | Determines if company members can prepare and submit negotiable quotes on behalf of the company. |
| [!UICONTROL Enable Purchase Orders] | Determines if Purchase Orders are permitted for the company. For purchase orders to function for company member accounts, the company administrator must also enable this feature on the storefront. |
| [!UICONTROL Applicable Payment Methods] | Indicates the payment methods that are available for company purchases. `B2B Payment Methods``All Enabled Payment Methods``Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Admin Only) Becomes active if specific payment methods are indicated. To select multiple payment methods, hold down the Ctrl key (PC) or the Command key (Mac) and click each option. |

{style="table-layout:auto"}
