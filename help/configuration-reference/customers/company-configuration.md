---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Company Configuration]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Customers] &gt; [!UICONTROL Company Configuration] van Commerce Admin.
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Met de installatie en activering van Adobe Commerce B2B kan de koopervaring worden gepersonaliseerd met bedrijfsspecifieke functies. Adobe Commerce B2B is een geïntegreerde oplossing die zowel B2B- als B2C-modellen ondersteunt. Voor meer informatie over de eigenschappen B2B, zie de [ Gids van de Gebruiker van Adobe Commerce B2B ](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

>[!NOTE]
>
>De toegang tot deze configuratieopties voor B2B eigenschappen wordt gecontroleerd door de [ rolmiddelen ](../../systems/permissions-user-roles.md#role-resources). Deze rolmiddelen moeten voor de gebruikersrol worden geplaatst die aan de gebruiker Admin wordt toegewezen.

Voor meer informatie over het vormen van deze montages, zie [ Basiseigenschappen B2B ](../../b2b/enable-basic-features.md) toelaten in de _Gids van de Gebruiker van Adobe Commerce B2B_.

## [!UICONTROL General]

![ Algemeen ](./assets/company-general.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | Website | Bepaalt als de bezoekers aan uw opslag de keus hebben om [ ](../../customers/customer-sign-in.md) voor een bedrijfrekening of een individuele rekening te registreren. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![ E-mailopties - de Registratie van het Bedrijf ](./assets/company-email-options-company-registration.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | Winkelweergave | De contactpersoon van de winkel die op de hoogte wordt gesteld wanneer een registratieverzoek van het bedrijf wordt ingediend bij de winkel. Opties: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | Winkelweergave | Het e-mailadres van elke persoon die een kopie van de registratiekennisgeving moet ontvangen. Scheid meerdere e-mailadressen met een komma. |
| [!UICONTROL Send Email Copy Method] | Winkelweergave | De e-mailmethode die wordt gebruikt om de kopie van de registratie-e-mail te verzenden. Opties: `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt voor het bedrijfsregistratiebericht. Standaardsjabloon: `Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![ klant-Verwante E-mail ](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer een verkoper wordt toegewezen aan een bedrijfsaccount. Dit e-mailbericht wordt verzonden naar de vertegenwoordiger en de beheerder van het bedrijf. Standaardsjabloon: `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer een individuele klantenrekening aan een bedrijfrekening wordt toegewezen. Dit e-mailbericht wordt alleen naar de klant verzonden. Standaardsjabloon: `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | Winkelweergave | Het e-mailmalplaatje dat wordt gebruikt wanneer een bedrijfbeheerder aan een bedrijf wordt toegewezen. Dit e-mailbericht wordt verzonden naar de vertegenwoordiger en de beheerder van het bedrijf. Standaardsjabloon: `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer de status van de persoon die als bedrijfbeheerder dienst doet in &quot;Inactief&quot;wordt veranderd. Het systeem verzendt e-mailbericht van de verandering naar de nieuwe en vroegere bedrijfbeheerders. Standaardsjabloon: `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer de vroegere bedrijfbeheerder een bedrijflid wordt. Het e-mailbericht wordt alleen naar het lid van het bedrijf verzonden. Standaardsjabloon: `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer de status van een klant actief wordt. Dit e-mailbericht wordt alleen naar de klant verzonden. Standaardsjabloon: `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer de status van een klant inactief wordt. Dit e-mailbericht wordt alleen naar de klant verzonden. Standaardsjabloon: `Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![ Verandering van de Status van het Bedrijf ](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | Winkelweergave | Het opslagcontact dat wordt meegedeeld wanneer de status van een bedrijf verandert. Opties: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | Winkelweergave | Het e-mailadres van elke persoon die een kopie van het bericht over de wijziging van de bedrijfsstatus moet ontvangen. Scheid meerdere e-mailadressen met een komma. |
| [!UICONTROL Send Email Copy Method] | Winkelweergave | De e-mailmethode die wordt gebruikt om de kopie van het bericht voor statuswijziging te verzenden. Opties: `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | Winkelweergave | Het e-mailmalplaatje dat wordt gebruikt wanneer het statuut van een bedrijf van _in afwachting van Goedkeuring_ aan _Actieve_ verandert. Standaardsjabloon: `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer het statuut van een bedrijf van _Afgewezen_ of _Geblokkeerd_ aan _Actief_ verandert. Standaardsjabloon: `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer het statuut van een bedrijf in _Geweigerd_ verandert. Standaardsjabloon: `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer het statuut van een bedrijf in _Geblokkeerd_ verandert. Standaardsjabloon: `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer het statuut van een bedrijf in _in afwachting van Goedkeuring_ verandert. Standaardsjabloon: `Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![ Krediet van het Bedrijf ](./assets/company-email-options-company-credit.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | Winkelweergave | De contactpersoon van de winkel die op de hoogte wordt gesteld wanneer er een wijziging optreedt in het krediet van een bedrijf. Opties: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | Winkelweergave | Het e-mailadres van elke persoon die een kopie van de kennisgeving van wijziging van het bedrijfskrediet moet ontvangen. Scheid meerdere e-mailadressen met een komma. |
| [!UICONTROL Send Email Copy Method] | Winkelweergave | De e-mailmethode die wordt gebruikt om de kopie van het bericht over de wijziging van het creditcard te verzenden. Opties: `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer bedrijfskrediet wordt toegewezen. Deze e-mail wordt verzonden naar de bedrijfbeheerder. Standaardsjabloon: `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer de kredietlimiet van een bedrijf wordt bijgewerkt. Deze e-mail wordt verzonden naar de bedrijfbeheerder. Standaardsjabloon: `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | Winkelweergave | Het e-mailmalplaatje dat door gebrek wordt gebruikt wanneer a [ terugbetaling ](../../b2b/credit-company.md#apply-a-payment-to-a-company-account) aan bedrijfskrediet wordt gemaakt. Deze e-mail wordt verzonden naar de bedrijfbeheerder. Standaardsjabloon: `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer een bedrag uit een bestelling wordt terugbetaald aan bedrijfskrediet. Deze e-mail wordt verzonden naar de bedrijfbeheerder. Standaardsjabloon: `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | Winkelweergave | De e-mailsjabloon die standaard wordt gebruikt wanneer een bestelling wordt teruggezet naar bedrijfskrediet. Deze e-mail wordt verzonden naar de bedrijfbeheerder. Standaardsjabloon: `Order Reverted to Company Credit` |

{style="table-layout:auto"}
