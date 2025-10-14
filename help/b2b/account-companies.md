---
title: Bedrijfsrekeningen
description: Ontdek hoe bedrijfsaccounts die in je Adobe Commerce-winkel worden beheerd, het mogelijk maken om meerdere kopers die tot hetzelfde bedrijf behoren, tot één bedrijfsaccount te laten samenvoegen.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Bedrijfsrekeningen

Wanneer u B2B bedrijfsrekeningen in uw opslag opneemt, kunt u de collectieve het winkelen ervaring vereenvoudigen door bedrijven toe te laten om veelvoudige subaccounts met flexibele toestemmingen tot stand te brengen die op gebruikersrollen in hun organisatie worden gebaseerd.

Depending on the company, a store administrator can adjust promotions and prices to suit their needs, and create highly customized offers that cater to the shoppers&#39; demands and increase orders.

Het toevoegen van een vereniging van de bedrijfrekening aan een standaard [&#x200B; individu &#x200B;](../customers/account-create.md) staat de klant toe om de specifieke die koopgewerkschema&#39;s te gebruiken voor het bedrijf worden bepaald.

Voordelen van een bedrijfsaccount:

- Biedt onbeperkte [&#x200B; bedrijfgebruikers &#x200B;](account-company-users.md) en de verwezenlijking van extra rekeningen aan, die collectieve aankopen vereenvoudigt.

- Omvat steun voor de hiërarchie van de a _slimme_ bedrijfrekening met verschillende [&#x200B; rollen en toestemmingen &#x200B;](account-company-roles-permissions.md) voor het plaatsen van orden.

- Verstrekt een mechanisme voor handelaren om inkomen te verhogen door [&#x200B; bedrijfsleekrediet &#x200B;](credit-company.md) als betalingsmethode aan te bieden.

- [&#128279;](account-company-manage.md)

## View company accounts

__ [&#128279;](account-company-create.md) [&#128279;](account-company-manage.md) Use the standard grid controls to filter the list, and adjust the column layout. __[&#128279;](account-company-manage.md)

Customers can create a company account from the storefront, or a merchant can create one from the Admin. By default, the ability to create company accounts from the storefront is enabled. If allowed by the configuration, a visitor to the store can request to open a company account. After the company account is approved, the company administrator can set up the company structure and users with various levels of permission.

__&#x200B;**[!UICONTROL Customers]**&#x200B;**[!UICONTROL Companies]**

![](./assets/companies-grid.png){width="700" zoomable="yes"}

[!UICONTROL Companies] [&#128279;](manage-company-hierarchy.md) [&#128279;](/help/b2b/account-company-manage.md#company-options-and-columns) [&#128279;](../getting-started/admin-grid-controls.md)

## Bedrijfsleider

Het volgende voorbeeld toont het _netwerk van Klanten_ met de aanvankelijke rekeningen van de bedrijfbeheerder.

![&#x200B; het net van Klanten met de rekening van de bedrijfbeheerder &#x200B;](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Elke onderneming heeft één enkele bedrijfbeheerder die door het rekening e-mailadres en de eerste en achternaam van de beheerder wordt geïdentificeerd. The administrator can be assigned to other companies as a user, but they can be an administrator for only one company.

[&#128279;](account-company-structure.md) [&#128279;](account-company-users.md) [&#128279;](account-company-roles-permissions.md)

### Wachtwoord voor bedrijfsbeheerder instellen voor eerste aanmelding

1. De bedrijfbeheerder vindt een welkome e-mail van de opslag.

   ![&#x200B; E-mail van het Welkome E-mail van het Voorbeeld &#x200B;](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >De e-mailadresdoelstellingen en de inhoud van e-mail worden bepaald door de opties die in de [&#x200B; bedrijf e-mailopties &#x200B;](email-company-configuration.md) configuratie worden gespecificeerd.

1. Volgt de instructies en klikt [!UICONTROL **verbinding**] om hun wachtwoord te plaatsen.

1. Keert a [!UICONTROL **Nieuw Wachtwoord**] en wachtwoordbevestiging voor hun rekening in.

   The password must include at least three of the following character types:

   - Lowercase characters (abc...)
   - Uppercase characters (ABC...)
   - Numbers (1234567890)
   - Special characters (!@#$...)

1. [!UICONTROL **&#x200B;**]

   ![](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. [!UICONTROL Customer Login][!UICONTROL **&#x200B;**][!UICONTROL **&#x200B;**]

1. [!UICONTROL **&#x200B;**]

   ![](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Bedrijfsstructuur

Een bedrijfsrekening kan worden opgezet om de structuur van de onderneming te weerspiegelen. Aanvankelijk, omvat de bedrijfsstructuur slechts de bedrijfbeheerder, maar kan worden uitgebreid om teams van gebruikers te omvatten. De gebruikers kunnen met teams worden geassocieerd of binnen een hiërarchie van afdelingen en onderverdelingen binnen het bedrijf worden georganiseerd. De structuur wordt ontworpen om het gebruik van [&#x200B; goedkeuringsregels &#x200B;](account-dashboard-approval-rules.md) voor [&#x200B; kooporden &#x200B;](purchase-order-flow.md) (POs) te steunen verbonden aan de bedrijfrekening.

![](./assets/company-structure-diagram.svg){width="450"}

In the company administrator&#39;s account dashboard, the company structure is represented as a tree and initially consists of only the company administrator.

![&#x200B; Structuur van het Bedrijf met de Beheerder van het Bedrijf &#x200B;](./assets/company-structure-tree-admin.png){width="600"}

When the account is created, the company administrator can use the company email address or be assigned a different email address.

In the following example, the initial company structure includes the company administrator plus an individual user account in the name of the company administrator. But company administrator functions (such as company structure and approval rules) are available only when they are logged in to the user account that is designated as the company administrator.

![](./assets/company-structure-tree-admin-user.png){width="600"}
