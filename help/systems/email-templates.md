---
title: E-mailsjablonen
description: Leer over e-mailmalplaatjes en hoe u hen kunt gebruiken om mededelingen aan uw klanten te steunen en uw merk te versterken.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# E-mailsjablonen

Met e-mailsjablonen definieert u de indeling, inhoud en opmaak van geautomatiseerde berichten die vanuit uw winkel worden verzonden. Ze worden transactiee-mails genoemd omdat elke e-mail is gekoppeld aan een specifiek type transactie of gebeurtenis.

Commerce bevat een reeks responsieve e-mailsjablonen die worden geactiveerd door verschillende gebeurtenissen die plaatsvinden tijdens het gebruik van uw winkel. Elke sjabloon is geoptimaliseerd voor elke schermgrootte en kan worden weergegeven vanaf het bureaublad en op tablets en mobiele apparaten. Er zijn diverse voorbereide e-mailsjablonen met betrekking tot klantactiviteiten, verkoop, productwaarschuwingen, beheeracties en systeemberichten die u kunt gebruiken [aanpassen](email-template-custom.md) om uw merk te weerspiegelen.

E-mailberichten van Commerce kunnen worden weergegeven door e-mailclients met HTML- en normale tekst. De manier waarop e-mailberichten worden weergegeven, kan per client verschillen.

## Uw e-maillogo voorbereiden

Logo&#39;s kunnen worden opgeslagen als een van de volgende bestandstypen. Logo&#39;s met een transparante achtergrond kunnen worden opgeslagen als .GIF- of .PNG-bestanden.

- JPG/JPEG
- GIF
- PNG

Er zijn afmetingen opgegeven in de koptekstsjabloon. Om ervoor te zorgen dat uw logo echter goed wordt weergegeven op apparaten met hoge resolutie, moet de geüploade afbeelding drie keer zo groot zijn. Originele logo-illustraties worden meestal gemaakt als vectorafbeeldingen, zodat deze kunnen worden vergroot zonder dat de resolutie verloren gaat. De afbeelding kan vervolgens worden opgeslagen in een van de ondersteunde indelingen voor bitmapafbeeldingen.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

Als u wilt profiteren van de beperkte verticale ruimte in de koptekst, snijdt u de afbeelding uit om te voorkomen dat er ruimte aan de boven- of onderkant verloren gaat. Wanneer u de afbeelding bewerkt, moet u de hoogte-breedteverhouding van het logo behouden, zodat de hoogte- en breedteverhouding proportioneel worden aangepast.

Doorgaans kunt u een afbeelding kleiner maken dan het origineel, maar niet groter zonder dat de resolutie verloren gaat. Als u een kleine afbeelding maakt en deze in een fotoeditor schaalt, verlaagt u de resolutie van de afbeelding. Als de weergavedrempel van het logo bijvoorbeeld 168 pixels breed en 48 pixels hoog is in de koptekstsjabloon, moet de geüploade afbeelding 504 pixels breed en 144 pixels hoog zijn.

| Logo-Dimensionen | 1 x (schermgrootte) | 3 x (afbeeldingsgrootte) |
|----------|----|----|
| Breedte: | 168 px | 504 px |
| Hoogte: | 48 px | 144 px |

{style="table-layout:auto"}

## E-mailsjablonen configureren

De configuratie bepaalt het logo dat in het standaardkopbalmalplaatje verschijnt, en om het even welke douane [header](email-template-custom.md#header-template) en [voettekst](email-template-custom.md#footer-template) sjablonen die u wilt gebruiken voor transactiee-mailberichten die vanuit uw winkels worden verzonden.

![Transactioneel e-mailontwerp](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

Voor een gedetailleerde lijst van de configuratiemontages, zie [_Transactiee-mails_](../content-design/configuration.md) in de _Inhoud- en ontwerphandleiding_.

## Stap 1. Uw logo uploaden

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de archiefmening die u wilt vormen en klikken **[!UICONTROL Edit]** in de _[!UICONTROL Action]_kolom.

1. Onder _[!UICONTROL Other Settings]_, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Transactional Emails]**sectie.

1. Uw voorbereid uploaden **[!UICONTROL Logo Image]**, klikt u op **[!UICONTROL Upload]** en selecteer het bestand op uw systeem.

1. Voor **[!UICONTROL Logo Image Alt]** Voer alternatieve tekst in om de afbeelding te identificeren.

1. Voer de **[!UICONTROL Logo Width]** en **[!UICONTROL Logo Height]** in pixels.

   Voer elke waarde in als een getal, zonder de `px` afkorting. Deze waarden hebben betrekking op de weergavegrootten van het logo in de koptekst en niet op de werkelijke grootte van de afbeelding.

## Stap 2. De kop- en voettekstsjablonen kiezen

Als u aangepaste kop- en voettekstsjablonen hebt voor uw winkel of voor verschillende winkels, kunt u opgeven welke sjablonen voor elke sjabloon worden gebruikt, afhankelijk van de [bereik](../getting-started/websites-stores-views.md#scope-settings) van de configuratie. Anders worden de standaardsjablonen gebruikt. Zie voor meer informatie [E-mailsjablonen aanpassen](email-template-custom.md).

1. Kies de optie **[!UICONTROL Header Template]** te gebruiken voor alle transactie-e-mailberichten.

1. Kies de optie **[!UICONTROL Footer Template]** te gebruiken voor alle transactie-e-mailberichten.

1. Klik op **[!UICONTROL Save Config]**.

## E-mailsjabloonlijst

De lijst met e-mailsjablonen is alfabetisch geordend op module.

### [!DNL Amazon_Payment]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Hard-declined Authorization` | nvt |
| `Soft-declined Authorization` | nvt |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Payment Failed` | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**Sectie:** [!UICONTROL Payment Failed Emails]<br/>**Veld:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (Alleen beschikbaar bij Adobe Commerce B2B)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Assign Company Admin` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails]<br/>**Veld:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **Pagina:** [!UICONTROL Customers] > [Bedrijfsconfiguratie ](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails] <br/>**Veld:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails]<br/>**Veld:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails]<br/>**Veld:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | nvt |
| `Company Registration Request` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Email Options - Company Registration]<br/>**Veld:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Status Change]<br/>**Veld:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Status Change]<br/>**Veld:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Status Change]<br/>**Veld:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Status Change]<br/>**Veld:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Status Change]<br/>**Veld:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails]<br/>**Veld:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails]<br/>**Veld:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Customer-Related Emails]<br/>**Veld:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (Alleen beschikbaar bij Adobe Commerce B2B)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Credit Limit Allocated` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Credit]<br/>**Veld:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Credit]<br/>**Veld:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Credit]<br/>**Veld:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Credit]<br/>**Veld:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sectie:** [!UICONTROL Company Credit]<br/>**Veld:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Contact Form` | **Pagina:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**Sectie:** [!UICONTROL Email Options]<br/>**Veld:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Change Email` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Account Information Options]<br/>**Veld:** [!UICONTROL Change Email Template] |
| E-mail en wachtwoord wijzigen | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Account Information Options]<br/>**Veld:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Password Options]<br/>**Veld:** E-mailsjabloon vergeten |
| `New Account` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Create New Account Options]<br/>**Veld:** Standaard-welkomste-mail |
| `New Account (Magento/luma)` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Create New Account Options]<br/>**Veld:** Standaard-welkomste-mail |
| `New Account Confirmation Key` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Create New Account Options]<br/>**Veld:** E-mailadres voor bevestiging |
| `New Account Confirmed` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Create New Account Options]<br/>**Veld:** Welkom-e-mail |
| `New Account Without Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Create New Account Options]<br/>**Veld:** Standaard welkomstbericht zonder wachtwoord |
| `Remind Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Password Options]<br/>**Veld:** E-mailsjabloon onthouden |
| `Reset Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Password Options] <br/>**Veld:** Wachtwoordsjabloon opnieuw instellen |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Store Credit Update` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sectie:** [!UICONTROL Store Credit Options]<br/>**Veld:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Currency Update Warnings` | **Pagina:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**Sectie:** [!UICONTROL Scheduled Import Settings]<br/>**Veld:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Footer` | nvt |
| `Footer (Magento/luma)` | nvt |
| `Header` | nvt |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Gift Card(s) Purchase` | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Sectie:** [!UICONTROL Gift Card Email Settings]<br/>**Veld:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Gift Card Code/Balance` | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Sectie:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**Veld:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Sjabloon | Configuratiepad |
|--- |--- |
| `New Registry` | **Pagina:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sectie:** [!UICONTROL Owner Notification]<br/>**Veld:** [!UICONTROL Email Template] |
| `Registry Sharing` | **Pagina:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sectie:** [!UICONTROL Gift Registry Sharing]<br/>**Veld:** [!UICONTROL Email Template] |
| `Registry Update` | **Pagina:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sectie:** [!UICONTROL Gift Registry Update]<br/>**Veld:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Order is Ready for Pickup` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Veld:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Veld:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Customer Invitation` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**Sectie:** [!UICONTROL Email]<br/>**Veld:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (Alleen beschikbaar bij Adobe Commerce B2B)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Declined Quote` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL Expiration Date Reset] | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Quote]<br/>**Veld:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Subscription Confirmation` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sectie:** [!UICONTROL  Subscription Options]<br/>**Veld:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sectie:** [!UICONTROL  Subscription Options]<br/>**Veld:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sectie:** [!UICONTROL  Subscription Options]<br/>**Veld:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Cron Error Warning` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sectie:** [!UICONTROL Product Alerts Run Settings]<br/>**Veld:** [!UICONTROL Error Email Template] |
| `Price Alert` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sectie:** [!UICONTROL Product Alerts]<br/>**Veld:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sectie:** [!UICONTROL Product Alerts]<br/>**Veld:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Approved Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL Purchase Order Approval]<br/>**Veld:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Promotion Notification/Reminder` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**Sectie:** [!UICONTROL Automated Email Reminder Rules]<br/>**Veld:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Balance Update` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Sectie:** [!UICONTROL Email Notification Settings]<br/>**Veld:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Sectie:** [!UICONTROL Email Notification Settings]<br/>**Veld:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

| Sjabloon | Configuratiepad |
|--- |--- |
| `New RMA` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL  RMA]<br/>**Veld:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL  RMA]<br/>**Veld:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL  RMA Admin Comments]<br/>**Veld:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL  RMA Admin Comments]<br/>**Veld:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL  RMA Authorization]<br/>**Veld:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL  RMA Authorization]<br/>**Veld:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sectie:** [!UICONTROL RMA Customer Comments]<br/>**Veld:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Credit Memo Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo Contents]<br/>**Veld:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo Comments]<br/>**Veld:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo Comments]<br/>**Veld:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo Comments]<br/>**Veld:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice Comments]<br/>**Veld:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice Comments]<br/>**Veld:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice Comments]<br/>**Veld:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice Comments]<br/>**Veld:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo]<br/>**Veld:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo]<br/>**Veld:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo]<br/>**Veld:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Credit Memo]<br/>**Veld:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice]<br/>**Veld:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice]<br/>**Veld:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice]<br/>**Veld:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Invoice]<br/>**Veld:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order]<br/>**Veld:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order]<br/>**Veld:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order]<br/>**Veld:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order]<br/>**Veld:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment]<br/>**Veld:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment]<br/>**Veld:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment]<br/>**Veld:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment]<br/>**Veld:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order Comments]<br/>**Veld:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order Comments]<br/>**Veld:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order Comments]<br/>**Veld:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Order Comments]<br/>**Veld:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment Comments]<br/>**Veld:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment Comments]<br/>**Veld:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment Comments]<br/>**Veld:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sectie:** [!UICONTROL Shipment Comments]<br/>**Veld:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

| Sjabloon | Configuratiepad |
|--- |--- |
| `Export Failed` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sectie:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Veld:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sectie:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Veld:** [!UICONTROL Error Email Template] |
| `Import Failed` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sectie:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Veld:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Send Product Link to Friend` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**Sectie:** [!UICONTROL Email Templates]<br/>**Veld:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Sitemap Generation Settings` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**Sectie:** [!UICONTROL Generation Settings]<br/>**Veld:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Sjabloon | Configuratiepad |
|--- |--- |
| `2FA Configuration Required by User` | nvt |
| `2FA Configuration Required for the Application` | nvt |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Forgot Admin Password` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sectie:** [!UICONTROL Admin User Emails]<br/>**Veld:** E-mailsjabloon wachtwoord vergeten |
| `User Notification` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sectie:** [!UICONTROL Admin User Emails]<br/>**Veld:** Sjabloon voor gebruikersmeldingen |
| `New User Notification` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sectie:** [!UICONTROL Admin User Emails]<br/>**Veld:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Sjabloon | Configuratiepad |
|--- |--- |
| `Magento Wish List Sharing` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**Sectie:** [!UICONTROL Share Options]<br/>**Veld:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
