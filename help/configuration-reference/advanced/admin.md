---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Advanced] &gt; [!UICONTROL Admin] van Commerce Admin.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Geavanceerd > Beheer

{{config}}

## [!UICONTROL Admin User Emails]

![&#x200B; Emails van de Gebruiker Admin &#x200B;](./assets/admin-admin-user-emails.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [&#x200B; Gevergeten wachtwoord en terugstellen e-mail &#x200B;](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Algemeen | Identificeert het e-mailmalplaatje dat voor het bericht wordt gebruikt dat wordt verzonden wanneer een gebruiker Admin zijn wachtwoord vergeet. Standaardsjabloon: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Algemeen | Identificeert het opslagcontact dat als afzender van het _vergeten Wachtwoord_ e-mail verschijnt. Standaardafzender: `General Contact`<br/> Andere afzenderopties: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Algemeen | Bepaalt de e-mailsjabloon die als standaard wordt gebruikt voor beheerdersmeldingen. Standaardsjabloon: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![&#x200B; Opstartpagina &#x200B;](./assets/admin-startup-page.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [&#x200B; de startpagina &#x200B;](../../getting-started/admin-dashboard.md#change-the-startup-page) in _Begonnen Gids_ veranderen.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Algemeen | Bepaalt de bestemmingspagina Admin die na u login verschijnt. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] opties

| Gebied |                                                                                                                                                                                                                                                                                                                                                                           | Optie |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![&#x200B; Adobe Commerce B2B &#x200B;](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![&#x200B; Adobe Commerce B2B &#x200B;](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![&#x200B; Adobe Commerce B2B &#x200B;](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg)<br /> | [&#x200B; Dashboard &#x200B;](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool` &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html?lang=nl-NL) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=nl-NL#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![&#x200B; Admin Basis URL &#x200B;](./assets/admin-admin-base-url.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie [&#x200B; basis URL &#x200B;](../../stores-purchase/store-urls.md#configure-the-base-url) in de _Gids van de Opslag en van de Ervaring van de Aankoop_ vormen.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Algemeen | Hiermee wordt bepaald of een aangepaste URL wordt gebruikt voor toegang tot de beheerder. Opties: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Algemeen | Hier geeft u een aangepaste URL op voor toegang tot de beheerder. Standaard is de URL voor het beheer gelijk aan de basis-URL.<br/>**Belangrijk:** Admin URL moet in de zelfde installatie van Commerce zijn, en de zelfde documentwortel hebben zoals de storefront. |
| [!UICONTROL Use Custom Admin Path] | Algemeen | Hiermee wordt bepaald of een aangepast pad wordt gebruikt voor toegang tot de beheerder. Het standaardpad is `admin` . Opties: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Algemeen | Wijzigt de naam van het standaardbeheerpad naar iets wat moeilijk te raden is. Voer de naam van het aangepaste pad in kleine letters in. Bijvoorbeeld: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![&#x200B; Veiligheid &#x200B;](./assets/admin-security.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie [&#x200B; veiligheid Admin &#x200B;](../../systems/security-admin.md) in de _Gids van Systemen Admin_ vormen.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Winkelweergave | Hiermee wordt bepaald of een Admin-gebruiker gelijktijdig vanaf verschillende apparaten kan worden aangemeld bij hetzelfde account. Opties: <br/>**`Yes`**- Hiermee worden meerdere actieve sessies van hetzelfde beheerdersaccount toegestaan.<br/>**`No`** - Hiermee wordt slechts één actieve sessie per beheerdersaccount toegestaan. |
| [!UICONTROL Password Reset Protection Type] | Winkelweergave | Bepaalt de methode die wordt gebruikt om verzoeken om het terugstellen van het wachtwoord te beheren. Opties: <br/>**`By IP and Email`**- Het wachtwoord kan online opnieuw worden ingesteld nadat een antwoord is ontvangen van het bericht is verzonden naar het e-mailadres dat is gekoppeld aan het beheerdersaccount.<br/>**`By IP`** - U kunt het wachtwoord online opnieuw instellen zonder extra bevestiging. <br/>**`By Email`**- Het wachtwoord kan alleen opnieuw worden ingesteld door te reageren per e-mail naar het bericht dat is verzonden naar het e-mailadres dat is gekoppeld aan het beheerdersaccount.<br/>**`None`** - Het wachtwoord kan slechts door de archiefbeheerder worden teruggesteld. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Algemeen | Bepaalt het aantal uren een verbinding van de wachtwoordterugwinning geldig blijft. |
| [!UICONTROL Max Number of Password Reset Requests] | Winkelweergave | Bepaalt het maximumaantal wachtwoordverzoeken dat per uur kan worden ingediend. |
| [!UICONTROL Min Time Between Password Reset Requests] | Winkelweergave | Hiermee bepaalt u het minimale aantal minuten tussen verzoeken om opnieuw instellen van wachtwoord. |
| [!UICONTROL Add Secret Key to URLs] | Algemeen | Als deze optie is ingeschakeld, wordt een geheime sleutel aan de URL van de beheerder toegevoegd als voorzorgsmaatregel tegen explosies. Opties: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Algemeen | Hiermee wordt bepaald of de aanmeldingsgegevens die een gebruiker heeft ingevoerd, moeten overeenkomen met de gegevens die zijn opgeslagen. Opties: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Algemeen | Hiermee bepaalt u de lengte van een beheersessie in seconden. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Algemeen | Hiermee bepaalt u hoe vaak Admin-gebruikers zich kunnen aanmelden voordat hun accounts zijn vergrendeld. Als het veld leeg is, wordt geen minimum ingesteld. Standaardwaarde: `6` |
| [!UICONTROL Lockout Time (minutes)] | Algemeen | Hiermee bepaalt u het aantal minuten dat een beheerdersaccount is vergrendeld voordat de gebruiker zich opnieuw kan aanmelden. Standaardwaarde: `30` |
| [!UICONTROL Password Lifetime (days)] | Algemeen | Hiermee bepaalt u het aantal dagen voordat een beheerderswachtwoord verloopt. Als het veld leeg is, wordt geen levensduur ingesteld. Standaardwaarde: `90` |
| [!UICONTROL Password Change] | Algemeen | Hiermee bepaalt u of Admin-gebruikers hun wachtwoorden moeten wijzigen. Opties: <br/>**`Forced`**- vereist dat Admin-gebruikers hun wachtwoorden wijzigen nadat de account is ingesteld.<br/>**`Recommended`** - raadt gebruikers van Admin aan hun wachtwoorden te wijzigen nadat de account is ingesteld. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![&#x200B; Dashboard &#x200B;](./assets/admin-dashboard.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie [&#x200B; Admin dashboard &#x200B;](../../getting-started/admin-dashboard.md) in de _Begonnen Gids_.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Algemeen | Hiermee wordt bepaald of het dashboard een grafiek bevat die wordt gegenereerd op basis van de huidige verkoopgegevens. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![&#x200B; Admin Rasters &#x200B;](./assets/admin-admin-grids.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie [&#x200B; productvertoning van de Beperking &#x200B;](../../catalog/products-list.md#limit-product-display) in de _Gids van het Beheer van de Catalogus_.

>[!NOTE]
>
>Als u de prestaties van grote catalogi wilt verbeteren, kunt u het beste het aantal producten beperken dat in het raster wordt weergegeven.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Algemeen | Hiermee wordt bepaald of het aantal weergegeven producten in het raster wordt beperkt tot de waarde _[!UICONTROL Records Limit]_. Opties: `Yes` / `No` |
| [!UICONTROL Records Limit] | Algemeen | Hiermee stelt u de maximale hoeveelheid producten in het productraster in. De standaardwaarde voor de minimumwaarde is `20000` . |

## [!UICONTROL CAPTCHA]

![&#x200B; CAPTCHA &#x200B;](./assets/admin-captcha.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie [&#x200B; CAPTCHA &#x200B;](../../systems/security-captcha.md) in de _Gids van Systemen Admin_.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Algemeen | Hiermee schakelt u CAPTCHA in voor de aanmelding bij Admin. Opties: `Yes` / `No` |
| [!UICONTROL Font] | Algemeen | Bepaalt het lettertype dat wordt gebruikt om de CAPTCHA weer te geven. Als u uw eigen lettertype wilt toevoegen, plaatst u het lettertypebestand in dezelfde map als de Commerce-instantie en voegt u de declaratie toe aan het bestand config.xml in het standaardlettertype `app/code/Magento/Captcha/etc` :` LinLibertine` |
| [!UICONTROL Forms] | Algemeen | Hiermee bepaalt u de formulieren waarin CAPTCHA wordt gebruikt. Opties: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Algemeen | Hiermee bepaalt u wanneer de CAPTCHA wordt weergegeven. Opties: <br/>**`Always`**- CAPTCHA is altijd vereist om u aan te melden.<br/>**`After number of attempts to login`** - Geeft het veld [!UICONTROL Number of Unsuccessful Attempts to Login] weer. Voer het aantal toegestane aanmeldpogingen in. De waarde 0 (nul) komt overeen met het instellen van Weergavemodus op Altijd. Deze optie geldt niet voor de formulieren Wachtwoord vergeten en Gebruiker maken. Als CAPTCHA is ingeschakeld en is ingesteld op verschijnen, wordt deze altijd opgenomen in het formulier.<br />**Nota**: Om het aantal mislukte login pogingen te volgen, wordt elke poging aan login onder één e-mailadres en van één IP-adres geteld. Het maximumaantal login pogingen die van het zelfde IP-adres worden toegestaan is 1.000. Deze beperking is alleen van toepassing wanneer CAPTCHA is ingeschakeld. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Algemeen | Hiermee bepaalt u het aantal keren dat een persoon kan proberen zich aan te melden voordat de account is vergrendeld. Om het aantal mislukte login pogingen te volgen, volgt het systeem de pogingen van één e-mailadres van één enkel IP-adres. Het maximumaantal pogingen dat van het zelfde IP adres wordt toegestaan is 1.000. Deze beperking is alleen van toepassing als CAPTCHA is ingeschakeld. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Algemeen | Bepaalt de levensduur van de huidige CAPTCHA. Wanneer de CAPTCHA verloopt, moet de gebruiker de pagina opnieuw laden. |
| [!UICONTROL Number of Symbols] | Algemeen | Hiermee bepaalt u het aantal symbolen dat in de CAPTCHA wordt gebruikt. De maximaal toegestane waarde is `8` . U kunt ook een bereik opgeven, bijvoorbeeld `5-8` . |
| [!UICONTROL Symbols Used in CAPTCHA] | Algemeen | Hiermee bepaalt u welke symbolen worden gebruikt in de CAPTCHA. Alleen letters (a-z en A-Z) en getallen (0-9) zijn toegestaan. De standaardset symbolen die in het veld wordt voorgesteld, sluit gelijkende symbolen zoals i, l of 1 uit. Als deze symbolen in CAPTCHA worden weergegeven, neemt de kans af dat een gebruiker CAPTCHA correct herkent. |
| [!UICONTROL Case Sensitive] | Algemeen | Hiermee wordt bepaald of de tekens in de CAPTCHA hoofdlettergevoelig zijn. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![&#x200B; Logging van Acties Admin &#x200B;](./assets/admin-actions-logging.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie {het archiveren van het 0} logboek van de Actie [&#x200B; in de &#x200B;](../../systems/action-log-archive.md) Gids van Systemen Admin _._

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Algemeen | Schakelt actielogboekregistratie in voor elk van de geselecteerde acties: <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` {2111 <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites`} <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![&#x200B; Gebruik Admin &#x200B;](./assets/admin-usage.png)<!-- zoom -->

Voor meer informatie over het plaatsen van deze opties, zie {de gegevensinzameling van het 0} Gebruik [&#x200B; in &#x200B;](../../getting-started/admin.md#usage-data-collection) Begonnen Gids _krijgen._

| Veld | Toepassingsgebied | Beschrijving |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Algemeen | Verleent toestemming voor Adobe om Admin gebruiksgegevens te verzamelen om de ervaring te verbeteren van het gebruiken van _Admin_, en verwante producten en de diensten. Het toestaan van gegevensinzameling laat ook _Begeleiding in-Product_ toe die wordt ontworpen om interactieve inhoud zoals hulp, hulpmiddeluiteinden, looppas-door gidsen, op het instappen informatie, eigenschapaankondigingen, en meer aan _Admin_ te brengen. Individuele beheerders worden niet geïdentificeerd in gebruiksgegevens. Opties:<br />**`Yes`**- staat gegevensinzameling toe en laat _Begeleiding in-product_ toe.<br />**`No`** - staat gegevensinzameling niet toe noch laat _Begeleiding in-product_ toe. |

{style="table-layout:auto"}
