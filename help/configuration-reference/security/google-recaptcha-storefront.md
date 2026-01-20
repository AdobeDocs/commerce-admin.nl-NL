---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] van Commerce Admin.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '1444'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Voordat Google reCAPTCHA kan worden geconfigureerd, moet u ervoor zorgen dat uw `PHP.ini` -bestand de volgende instelling bevat: `allow_url_fopen = 1` . Hiervoor kan hulp van ontwikkelaars nodig zijn. Zie [ PHP Montages ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) in de _Gids van de Installatie_.

{{config}}

Voor meer informatie over het gebruiken van Google reCAPTCHA om uw opslag te beveiligen, zie Google [ reCAPTCHA ](../../systems/security-google-recaptcha.md) in de _Gids van Systemen Admin_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![ reCAPTCHA v2 (&quot;ik ben geen robot&quot;) ](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--|--|--|
| [!UICONTROL Google API Website Key] | Website | De websitecode die wordt gemaakt wanneer u uw Google reCAPTCHA-account registreert. |
| [!UICONTROL Google API Secret Key] | Website | De geheime sleutel die aan uw Google reCAPTCHA-account is gekoppeld. |
| [!UICONTROL Size] | Website | De grootte van het Google reCAPTCHA-vak dat wordt weergegeven wanneer een klant zich aanmeldt bij zijn of haar account. Opties: `Normal` (standaardwaarde) / `Compact` |
| [!UICONTROL Theme] | Website | Bepaalt de stijl van het vak Google reCAPTCHA. Opties: `Light Theme` (standaardwaarde) / `Dark Theme` |
| [!UICONTROL Language Code] | Winkelweergave | De [ twee-karakter code ](https://developers.google.com/recaptcha/docs/language) die de taal specificeert die voor de tekst en het overseinen van Google reCAPTCHA wordt gebruikt. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![ reCAPTCHA v2 Onzichtbaar ](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--|--|--|
| [!UICONTROL Google API Website Key] | Website | De websitecode die wordt gemaakt wanneer u uw Google reCAPTCHA-account registreert. |
| [!UICONTROL Google API Secret Key] | Website | De geheime sleutel die aan uw Google reCAPTCHA-account is gekoppeld. |
| [!UICONTROL Invisible Badge Position] | Website | De positie van de onzichtbare reCAPTCHA-badge op elke pagina. Opties: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Algemeen | Bepaalt de stijl van het vak Google reCAPTCHA. Opties: `Light Theme` (standaardwaarde) / `Dark Theme` |
| [!UICONTROL Language Code] | Winkelweergave | A [ twee-karakter code ](https://developers.google.com/recaptcha/docs/language) die de taal specificeert die voor de tekst en het overseinen van Google reCAPTCHA wordt gebruikt. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![ reCAPTCHA v3 Onzichtbaar ](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--|--|--|
| [!UICONTROL Google API Website Key] | Website | De websitecode die wordt gemaakt wanneer u uw Google reCAPTCHA-account registreert. |
| [!UICONTROL Google API Secret Key] | Website | De geheime sleutel die aan uw Google reCAPTCHA-account is gekoppeld. |
| [!UICONTROL Minimum Score Threshold] | Algemeen | De minimumscore die een gebruikersinteractie als potentieel risico identificeert, waar 1.0 een typische gebruikersinteractie is, en 0.0 waarschijnlijk is een bot. Standaard: `0.5` |
| [!UICONTROL Invisible Badge Position] | Website | De positie van de onzichtbare reCAPTCHA-badge op elke pagina. Opties: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Website | Bepaalt de stijl van het vak Google reCAPTCHA. Opties: `Light Theme` (standaardwaarde) / `Dark Theme` |
| [!UICONTROL Language Code] | Winkelweergave | A [ twee-karakter code ](https://developers.google.com/recaptcha/docs/language) die de taal specificeert die voor de tekst en het overseinen van Google reCAPTCHA wordt gebruikt. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

[!BADGE  slechts SaaS ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service-projecten (door Adobe beheerde SaaS-infrastructuur)."}

![ reCAPTCHA v3 Onderneming ](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--|--|--|
| [!UICONTROL Site Key] | Website | De sitecode die wordt gemaakt wanneer u uw Google reCAPTCHA Enterprise-account registreert. |
| [!UICONTROL Google Cloud Project ID] | Website | Projectidentiteitskaart wordt getoond in de **info van het Project** sectie op het dashboard van het project. |
| [!UICONTROL Service Account JSON] | Website | Download de sleutel van de de dienstrekening van de Google Cloud console en plak zijn inhoud in dit gebied. |
| [!UICONTROL Minimum Score Threshold] | Website | De minimumscore die een gebruikersinteractie als potentieel risico identificeert, waar 1.0 een typische gebruikersinteractie is, en 0.0 waarschijnlijk is een bot. Standaard: `0.5` |
| [!UICONTROL Badge Position] | Website | De positie van de onzichtbare reCAPTCHA-badge op elke pagina. Opties: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Website | Bepaalt de stijl van het vak Google reCAPTCHA. Opties: `Light Theme` (standaardwaarde) / `Dark Theme` |
| [!UICONTROL Language Code] | Winkelweergave | A [ twee-karakter code ](https://developers.google.com/recaptcha/docs/language) die de taal specificeert die voor de tekst en het overseinen van Google reCAPTCHA wordt gebruikt. Laat het veld leeg om de standaardtaal van de browser van de gebruiker te gebruiken. |
| [!UICONTROL Validation Failure Message] | Winkelweergave | Een bericht dat wordt weergegeven wanneer validatie mislukt. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![ de berichten van de Mislukking ](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Winkelweergave | Het bericht dat in de opslagruimte wordt weergegeven als de verificatie mislukt. Standaardtekst: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Winkelweergave | Het bericht dat in de storefront wordt getoond als reCAPTCHA er niet in slaagt om een controleresultaat terug te keren. Standaardtekst: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![ Storefront ](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Het reCAPTCHA-type dat u kiest, moet overeenkomen met het type dat is gekoppeld aan de API-sleutel van uw Google reCAPTCHA-account.

>[!WARNING]
>
>Wanneer u reCAPTCHA versie 3 gebruikt, kan een echte gebruiker met een lage score niet doorgaan. Voor versie 2 ontvangt een echte gebruiker met een lage score een uitdaging. Overweeg zorgvuldig of echte gebruikers met een lage score de kans moeten hebben om een uitdaging (versie 2) op te lossen of geblokkeerd te worden (versie 3).

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten [ binnen ](../../customers/customer-sign-in.md) aan hun rekeningen ondertekenen. Opties:<br/>**`No`**- (gebrek) bevestigt niet het login verzoek.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Forgot Password] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten om het terugstellen van het a [ wachtwoord ](../../customers/password-reset.md) verzoeken. Opties:<br/>**`No`**- (gebrek) bevestigt niet het verzoek van het wachtwoordterugstellen.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Create New Customer Account] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klant omhoog voor a [ nieuwe rekening ](../../customers/account-create.md) ondertekent. Opties:<br/>**`No`**- (gebrek) bevestigt niet het rekeningsverzoek.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Edit Customer Account] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klant hun [ rekeningsinformatie ](../../customers/account-dashboard-account-information.md) verandert. Opties:<br/>**`No`**- (gebrek) bevestigt niet het rekeningsverzoek.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Create New Company Account] | Website | ![ Adobe Commerce B2B ](../../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B slechts) specificeert het type van reCAPTCHA dat wordt gebruikt wanneer een nieuwe [ bedrijfrekening ](../../b2b/account-company-create.md) wordt gecreeerd. Opties:<br/>**`No`**- (gebrek) bevestigt niet het rekeningsverzoek.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Contact Us] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt om een bericht van de [ pagina van het Contact van ons ](../../getting-started/store-details.md#contact-us-form) van uw opslag te verzenden. Opties:<br/>**`No`**- (gebrek) bevestigt niet het berichtverzoek.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Product Review] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten a [ productoverzicht ](../../merchandising-promotions/product-reviews.md) voorleggen. Opties:<br/>**`No`**- (gebrek) bevestigt niet het verzoek van het productoverzicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Newsletter Subscription] | Website | Specificeert het type van onzichtbare reCAPTCHA die wordt gebruikt wanneer de klanten omhoog voor het abonnement van de a [ nieuwsbrief ](../../merchandising-promotions/newsletter-subscribers.md) ondertekenen. Opties:<br/>**`No`**- (gebrek) bevestigt niet het verzoek van het nieuwsbrief abonnement.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Gift Card] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten a [ cadeaukaart ](../../catalog/product-gift-card-create.md) code ingaan. Opties:<br/>**`No`**- (gebrek) bevestigt niet de indiening van de cadeau kaartcode.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder dat interactie op basis van de score vereist is.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Invitation Create Account] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten een van de rekeningsverwezenlijking [ uitnodigings ](../../merchandising-promotions/invitations.md) code verzenden. Opties:<br/>**`No`**- (gebrek) bevestigt niet de uitnodigings e-mailvoorlegging.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder dat interactie op basis van de score vereist is.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Send to Friend] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten [ een product ](../../stores-purchase/email-a-friend.md) met een vriend delen. Opties:<br/>**`No`**- (gebrek) bevestigt niet de e-mailvoorlegging.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Wishlist Sharing] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten [ een verlanglijst ](../../stores-purchase/wishlist-storefront.md#share-the-wish-list) delen. Opties:<br/>**`No`**- (gebrek) bevestigt niet het bericht en e-mailvoorlegging.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder dat interactie op basis van de score vereist is.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for Coupon Codes] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten a [ couponcode ](../../merchandising-promotions/price-rules-cart-coupon.md) ingaan. Opties:<br/>**`No`**- (standaardwaarde) valideert de verzending van de couponcode niet.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder dat interactie op basis van de score vereist is.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Website | Specificeert het type van reCAPTCHA dat wordt gebruikt wanneer de klanten voor een aankoop met [ PayPal Payflow Pro ](../../stores-purchase/paypal-payflow-pro.md) betalen. Opties:<br/>**`No`**- (gebrek) bevestigt niet het verzoek van het wachtwoordterugstellen.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Vereist de gebruiker om _te selecteren I ben geen robot_ checkbox.<br />**`Invisible reCAPTCHA v2`**- Valideert het gedrag van de gebruiker op de achtergrond zonder interactie op basis van de score te vereisen.<br/>**`Invisible reCAPTCHA v3`** - (Aanbevolen) Hiermee wordt het gebruikersgedrag op de achtergrond gevalideerd op basis van de interactiescore. |

{style="table-layout:auto"}
