---
title: Referentiehandleiding voor configuratie
description: Bekijk beschrijvende informatie voor alle configuratie-instellingen van de Commerce Admin Store die zijn geordend op de configuratietabbladen, pagina's en secties.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: dbc0057f02bddf681d769bdaebfaf6b526c8dbd2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Referentiehandleiding voor configuratie

Deze handleiding is bedoeld voor handelaren en systeembeheerders die in Adobe Commerce of Magento Open Source Admin werken. Het verstrekt verwijzingsinformatie voor alle montages van de opslagconfiguratie die van _worden betreden Admin_ sidebar bij **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

De sectie heeft geen betrekking op details over de mogelijkheden van Adobe Commerce en Magento Open Source of procedures voor de configuratie van winkels.

Deze gids wordt georganiseerd volgens de configuratie linkernavigatie:

| Tabblad Configuratie | Onderliggende tabbladen |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/> de _[!UICONTROL General]_&#x200B;configuratiesecties bepalen opslagparameters, URLs, thema, munt, e-mailadressen, opslagcontacten, redacteur, en dashboardrapport. | - [[!UICONTROL General]](./general/general.md)<br> - [[!UICONTROL B2B Features]](./general/b2b-features.md)<br> - [[!UICONTROL Web]](./general/web.md)<br> - [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br> - [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br> - [[!UICONTROL Contacts]](./general/contacts.md)<br> - [[!UICONTROL Reports]](./general/reports.md)<br> - [[!UICONTROL Content Management]](./general/content-management.md)<br> - [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br> - [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/> de _[!UICONTROL Catalog]_&#x200B;configuratiemontages bepalen het product en de inventarismontages, controle sitemap en RSS voedergeneratie, en specificeren het e-mailmalplaatje dat wordt gebruikt om producten met vrienden te delen. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br> - [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br> - [[!UICONTROL Inventory]](./catalog/inventory.md)<br> - [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br> - [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br> - [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/> _[!UICONTROL Security]_&#x200B;de controle van de configuratiemontages opslagveiligheid, bifactorauthentificatie, en de Google reCAPTCHA eigenschap. | - [[!UICONTROL 2FA]](./security/2fa.md)<br> - [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br> - [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br> - [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/> _[!UICONTROL Customers]_&#x200B;de configuratiemontages vestigen basisklantenrekening en login opties, nieuwsbrief montages, verlanglijst, en het formaat van auto-geproduceerde couponcodes. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br> - [[!UICONTROL Newsletter]](./customers/newsletter.md)<br> - [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br> - [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br> - [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br> - [[!UICONTROL Wish List]](./customers/wishlist.md)<br> - [[!UICONTROL Invitations]](./customers/invitations.md)<br> - [[!UICONTROL Reward Points]](./customers/reward-points.md)<br> - [[!UICONTROL Promotions]](./customers/promotions.md)<br> - [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br> - [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/> _[!UICONTROL Sales]_&#x200B;de configuratiemontages bepalen checkout en belasting montages, betaling en verschepende opties, verkoop e-mail en PDF druk-outs, en Google API montages. | - [[!UICONTROL Sales]](./sales/sales.md)<br> - [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br> - [[!UICONTROL Quotes]](./sales/quotes.md)<br> - [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br> - [[!UICONTROL Tax]](./sales/tax.md)<br> - [[!UICONTROL Checkout]](./sales/checkout.md)<br> - [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br> - [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br> - [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br> - [[!UICONTROL Google API]](./sales/google-api.md)<br> - [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br> - [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br> - [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/> Wanneer de [!DNL Amazon Sales Channel] extensie wordt geïnstalleerd, beheren de _[!UICONTROL Sales Channels]_-instellingen geautomatiseerde integratiebewerkingen met uw Amazon-winkel. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/> de _[!UICONTROL Services]_&#x200B;configuratie montages bepalen de integratie van Commerce API montages, met inbegrip van SOAP en OAuth. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br> - [[!UICONTROL Commerce Services]](./services/saas.md)<br> - [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/> de _[!UICONTROL Advanced]_&#x200B;configuratiemontages bepalen standaard montages Admin, diverse montages van de systeemconfiguratie, geavanceerde modulecontroles, en ontwikkelaarshulpmiddelen. | - [[!UICONTROL Admin]](./advanced/admin.md)<br> - [[!UICONTROL System]](./advanced/system.md)<br> - [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

De sectie heeft geen betrekking op details over de mogelijkheden van Adobe Commerce en Magento Open Source of procedures voor de configuratie van winkels.

## Beschikbare documentatie

{{docs-links}}
