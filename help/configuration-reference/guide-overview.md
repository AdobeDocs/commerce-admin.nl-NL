---
title: Referentiehandleiding voor configuratie
description: De beschrijvende informatie van het overzicht voor alle de opslagconfiguratiemontages van Admin van de Handel die door de configuratielusjes, pagina's, en secties worden georganiseerd.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Referentiehandleiding voor configuratie

Deze handleiding is bedoeld voor handelaren en systeembeheerders die in Adobe Commerce of Magento Open Source werken. Het verstrekt verwijzingsinformatie voor alle montages van de opslagconfiguratie die van worden betreden _Beheerder_ zijbalk op **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

Het omvat geen details over de mogelijkheden van Adobe Commerce en Magento Open Source of procedures voor winkelconfiguratie.

Deze gids wordt georganiseerd volgens de configuratie linkernavigatie:

| Tabblad Configuratie | Onderliggende tabbladen |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/>De _[!UICONTROL General]_configuratiesecties bepalen opslagparameters, URLs, thema, munt, e-mailadressen, opslagcontacten, redacteur, en dashboardrapport. | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/>De _[!UICONTROL Catalog]_De configuratiemontages bepalen het product en de inventarismontages, de productie van de controlesitemap en van het voer RSS, en specificeren het e-mailmalplaatje dat wordt gebruikt om producten met vrienden te delen. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/>De _[!UICONTROL Security]_configuratiemontages bewaren veiligheid, bifactorauthentificatie, en de Google reCAPTCHA eigenschap. | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/>De _[!UICONTROL Customers]_configuratie-instellingen bepalen de basisopties voor klantenaccounts en aanmelding, nieuwsbrief-instellingen, wensenlijst en de indeling van automatisch gegenereerde couponcodes. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/>De _[!UICONTROL Sales]_De configuratie-instellingen bepalen de instellingen voor kassa en belasting, betalings- en verzendopties, de instellingen voor e-mail- en PDF-afdrukken en Google API. | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>Wanneer de [!DNL Amazon Sales Channel] -extensie is geïnstalleerd, de _[!UICONTROL Sales Channels]_Met instellingen beheert u geautomatiseerde integratiebewerkingen met uw Amazon-winkel. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/>De _[!UICONTROL Services]_configuratie-instellingen bepalen de integratie-instellingen voor de Commerce API, waaronder SOAP en OAuth. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/>De _[!UICONTROL Advanced]_De configuratiemontages bepalen standaard montages Admin, diverse montages van de systeemconfiguratie, geavanceerde modulecontroles, en ontwikkelaarshulpmiddelen. | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

Het omvat geen details over de mogelijkheden van Adobe Commerce en Magento Open Source of procedures voor winkelconfiguratie.

## Beschikbare documentatie

{{docs-links}}
