---
title: Gebruikersrollen
description: Leer hoe u gebruikersrollen en de bijbehorende machtigingen maakt om de toegang tot Admin-functies te beheren.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Gebruikersrollen

Om iemand beperkte toegang tot Admin te geven, moet de eerste stap een rol tot stand brengen die het aangewezen niveau van toestemmingen heeft. Nadat de rol wordt bewaard, kunt u nieuwe gebruikers toevoegen en de beperkte rol toewijzen om hen beperkte toegang tot Admin te verlenen.

![Admin - gebruikersrollen](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Een rol definiëren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Role]**.

1. Voer de stappen uit om de rol te definiëren:

### Stap 1: Voeg de rolnaam toe

1. Onder _[!UICONTROL Role Information]_, voert u een beschrijving in **[!UICONTROL Role Name]**.

1. Onder _[!UICONTROL Current User Identity Verification]_, voer uw wachtwoord in.

   ![Systeemmachtigingen - rolgegevens](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Stap 2: Bronnen toewijzen

>[!IMPORTANT]
>
>Wanneer het toewijzen van middelen, ben zeker om toegang tot het hulpmiddel van Toestemmingen onbruikbaar te maken als u toegang voor een bepaalde rol beperkt. Anders kunnen gebruikers hun eigen machtigingen wijzigen.

1. Set **[!UICONTROL Role Scopes]** op een van de volgende wijzen:

   - `All`
   - `Custom`

   Indien ingesteld op `Custom` voor een installatie met meerdere sites selecteert u het selectievakje van de website en slaat u de locatie op waar de rol moet worden gebruikt.

   ![Bronnen voor gebruikersrollen - aangepast bereik](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Gebruikers met een `Custom` rolwerkingsgebied kan geen websites en categorieën tot stand brengen, producten aan categorieën toewijzen, of producten uitgeven bij _[!UICONTROL All Store Views]_werkingsgebied wanneer zij aan beperkte opslag worden toegewezen. Deze gebruikers kunnen ook geen andere_ globaal _handelingen die van invloed zijn op het bereik wanneer ze geen toegang hebben.

1. Onder _[!UICONTROL Roles Resources]_, set **[!UICONTROL Resource Access]**tot `Custom`.

1. In de **[!UICONTROL Resource]** boomstructuur, selecteer checkbox van elk vermogen Admin dat de rol kan toegang hebben.

   Als u een beheerdersrol wilt maken met toegang tot belastinginstellingen, kiest u zowel de BTW- als de systeembronnen. Als u een website instelt voor een gebied dat afwijkt van uw standaard [verzendpunt van oorsprong](../stores-purchase/shipping-settings.md#point-of-origin), moet u toegang tot de middelen van het Systeem/Verzending voor de rol verlenen. De verzendinstellingen bepalen het BTW-tarief voor de winkel dat wordt gebruikt voor catalogusprijzen.

   ![Toegewezen gebruikersrolbronnen](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   De lijst met beschikbare machtigingen kan aanvullende opties voor gebundelde en geïnstalleerde extensies bevatten. Door de hoogste toestemming voor elke eigenschap te selecteren, wijst u alle toestemmingen toe beschikbaar voor de gebruiker.

   >[!NOTE]
   >
   >Een Admin-gebruiker moet **[!UICONTROL Sales / Archive]** machtigingen voor hun rolbereik om de _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_, en _[!UICONTROL Shipments]_bestellen [tabs](../stores-purchase/order-processing.md).

1. Klik op **[!UICONTROL Save Role]**.

   De rol wordt nu weergegeven in het raster en kan worden toegewezen aan gebruikersaccounts.

## Rollen toewijzen aan gebruikers

1. Van de _[!UICONTROL Roles]_, opent u de record in de bewerkingsmodus.

1. Onder _[!UICONTROL Current User Identity Verification]_, voer het wachtwoord voor uw gebruikersaccount in.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Role Users]**.

   De _[!UICONTROL Role Users]_wordt alleen weergegeven nadat een nieuwe rol is opgeslagen.

   ![Gebruikersaccounts toegewezen aan de rol](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Ga als volgt te werk om te zoeken naar een specifieke gebruikersrecord:

   - Voer de waarde in het zoekfilter boven aan een kolom in en druk op **Enter**.

   - Wanneer u klaar bent om naar de volledige lijst terug te keren, klikt u op **[!UICONTROL Reset Filter]**.

1. Schakel het selectievakje in van de gebruikers die aan de rol moeten worden toegewezen.

1. Klik op **[!UICONTROL Save Role]**.

## Een rol bewerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Zoek de rol met filters boven het raster en klik op de naam van de rol.

1. Breng de gewenste wijzigingen aan.

   Controleer de stappen voor het maken van een gebruikersrol voor informatie over de rolinstellingen.

1. Voer desgevraagd uw wachtwoord in om uw identiteit te bevestigen.

1. Klik op de knop **[!UICONTROL Save Role]**.

## Een rol verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Zoek de rol met behulp van filters boven het raster en open de bewerkingsmodus.

1. Klik in de rechterbovenhoek op **[!UICONTROL Delete Role]**.

1. Klik op **[!UICONTROL OK]**.

## demo gebruikersrollen

Bekijk deze video voor meer informatie over het beheren van gebruikersrollen:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## Rolresources

De toegang tot de volgende middelen kan aan een douanerol worden toegewezen. Zie de gekoppelde pagina voor meer informatie over de mogelijkheden die aan elke bron zijn gekoppeld.

![Adobe Commerce](../assets/adobe-logo.svg) - Alleen Adobe Commerce

![Adobe Commerce B2B](../assets/b2b.svg) - Alleen beschikbaar bij Adobe Commerce B2B

| Bron |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Inhoud stapelen](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
