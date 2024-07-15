---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Checkout] van Commerce Admin.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![ de Opties van de Controle ](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Winkelweergave | Schakel deze instelling in om niet-geverifieerde gebruikers (winkel- en API&#39;s) de mogelijkheid te geven te vragen of er al een e-mailadres is gekoppeld aan een klantenaccount. Dit kan worden gebruikt om de uitcheckworkflow voor gasten te verbeteren door een aanmeldingsprompt weer te geven als het ingevoerde e-mailadres al is geregistreerd bij een klantenaccount, maar ten koste gaat van het toegankelijk maken van informatie voor niet-geverifieerde gebruikers.  Opties: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Winkelweergave | Bepaalt als [ Één-pagina controle ](../../stores-purchase/checkout-process.md#checkout-options) het standaardcontrolemateriaal is. Opties: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Winkelweergave | Bepaalt als de gasten door [ controle kunnen gaan zonder ](../../stores-purchase/checkout-guest.md) voor een rekening met uw opslag te registreren. Opties: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Winkelweergave | Bepaalt als de klanten worden vereist om met de [ Voorwaarden ](../../stores-purchase/terms-and-conditions.md) van de verkoop in te stemmen alvorens een aankoop te doen. Opties: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Winkelweergave | Hiermee bepaalt u de locatie van het factuuradres tijdens het afrekenen. Opties: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Winkelweergave | Bepaalt het maximumaantal punten die in de _Samenvatting van de Orde_ tijdens controle kunnen verschijnen. De standaardwaarde is `10` . |
| [!UICONTROL Enable Address Search] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de klanten [ functionaliteit van het adresonderzoek ](../../stores-purchase/checkout-address-search.md) voor het verschepen, en de stappen van het Overzicht &amp; van Betalingen kunnen gebruiken. Als deze optie is ingeschakeld, gebruikt u Limiet voor aantal klantadressen om het aantal opgeslagen adressen in te stellen dat vereist is om deze functie tijdens het uitchecken te activeren. Opties: `Yes` / `No` |
| Limiet voor aantal adressen van klanten | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) wanneer het adresonderzoek wordt toegelaten, bepaalt het aantal bewaarde adressen die worden vereist om deze functionaliteit tijdens controle te activeren. Wanneer het aantal van de klant bewaarde adressen samenkomt of dit aantal overschrijdt, slechts wordt het standaardadres teruggegeven op de _Verschepende_ en _Controle &amp; de stappen van de Betalingen_. De klant kan een zoekfunctie gebruiken om het geselecteerde adres te wijzigen. De standaardwaarde is `10` . |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![ Shopping Cart ](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Website | Bepaalt het [ leven van een geciteerde prijs ](../../stores-purchase/cart-configuration.md#quote-lifetime), in dagen. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Winkelweergave | Bepaalt als de [ het winkelen kartpagina ](../../stores-purchase/cart-configuration.md#redirect-to-cart) onmiddellijk verschijnt nadat een product aan de kar wordt toegevoegd. Opties: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Winkelweergave | Hiermee bepaalt u het aantal artikelen in het winkelwagentje voordat de pager wordt geactiveerd. Standaardwaarde: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Winkelweergave | Wijst erop als [ dwars-verkooppunten ](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) in het het winkelwagentje worden getoond, die extra verkoopopties aan klanten verstrekken. Opties: `Yes` (standaardwaarde) / `No` |
| [!UICONTROL Grouped Product Image] | Winkelweergave | Bepaalt het [ duimnagel ](../../stores-purchase/cart-configuration.md#cart-thumbnails) beeld dat voor a [ gegroepeerd product ](../../catalog/product-create-grouped.md) in het het winkelwagentje verschijnt. Opties: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Winkelweergave | Bepaalt het [ duimnagel ](../../stores-purchase/cart-configuration.md#cart-thumbnails) beeld dat voor een configureerbaar product in het winkelwagentje verschijnt. Opties: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Winkelweergave | Hiermee bepaalt u de maximumleeftijd van de prijsopgave in minuten bij voorvertoond winkelwagentje. |
| [!UICONTROL Enable Clear Shopping Cart] | Website | Hiermee bepaalt u of in het winkelwagentje de optie wordt weergegeven waarmee gebruikers de inhoud van het winkelwagentje in één handeling kunnen wissen. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![ Mijn Verbinding van de Kar ](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Website | Bepaalt de waarde die tussen haakjes na de koppeling Mijn winkelwagen wordt weergegeven. Opties: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini Cart

![ Mini Kar ](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Winkelweergave | Hiermee bepaalt u of de miniwinkelwagentje op de winkelpagina&#39;s wordt weergegeven wanneer op het winkelwagentje in de koptekst wordt geklikt. De weergave van de minikaart is afhankelijk van het thema. Opties: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Winkelweergave | Hiermee bepaalt u het aantal items dat in de miniwinkelwagen kan worden weergegeven voordat de schuifbalk wordt geactiveerd. Standaard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Winkelweergave | Hiermee bepaalt u het maximum aantal items dat in de miniwinkelwagen kan worden weergegeven. Standaard: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![ Betaling Ontbroken E-mail ](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Winkelweergave | Identificeert de contactpersoon van de winkel die de e-mail met betalingsfout ontvangt. Standaardontvanger: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Winkelweergave | Identificeert de opslagcontactpersoon die wordt weergegeven als de afzender van het bericht Betaling Ontbroken e-mails. Standaardafzender: `General Contact` |
| [!UICONTROL Payment Failed Template] | Winkelweergave | Identificeert de sjabloon die wordt gebruikt voor mislukte e-mails over betalingen. Standaardsjabloon: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Winkelweergave | Verstrekt het e-mailadres van iedereen om een exemplaar van een Ontbroken e-mail van de Betaling te ontvangen. Scheid meerdere adressen met een komma. |
| [!UICONTROL Send Payment Failed Copy Method] | Winkelweergave | Geeft de e-mailmethode aan die wordt gebruikt om de kopie te verzenden. Opties: <br />**`Bcc`**- hiermee wordt een blinde, hoffelijke kopie verzonden door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.<br />**`Separate Email`** - Verzendt de kopie als een aparte e-mail. |

{style="table-layout:auto"}
