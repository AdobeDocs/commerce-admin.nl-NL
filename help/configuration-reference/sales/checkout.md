---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Sales] &gt; [!UICONTROL Checkout] pagina van de Commerce Admin.
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

![Afhandelingsopties](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Winkelweergave | Schakel deze instelling in om niet-geverifieerde gebruikers (winkel- en API&#39;s) de mogelijkheid te geven te vragen of er al een e-mailadres is gekoppeld aan een klantenaccount. Dit kan worden gebruikt om de uitcheckworkflow voor gasten te verbeteren door een aanmeldingsprompt weer te geven als het ingevoerde e-mailadres al is geregistreerd bij een klantenaccount, maar ten koste gaat van het toegankelijk maken van informatie voor niet-geverifieerde gebruikers.  Opties: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Winkelweergave | Hiermee wordt bepaald of [Uitchecken via één pagina](../../stores-purchase/checkout-process.md#checkout-options) Dit is de standaardindeling voor uitchecken. Opties: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Winkelweergave | Hiermee wordt bepaald of gasten door kunnen gaan [afrekenen zonder registratie](../../stores-purchase/checkout-guest.md) voor een account bij je winkel. Opties: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Winkelweergave | Hiermee bepaalt u of klanten akkoord moeten gaan met de [Voorwaarden en bepalingen](../../stores-purchase/terms-and-conditions.md) van de verkoop voordat een aankoop wordt gedaan. Opties: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Winkelweergave | Hiermee bepaalt u de locatie van het factuuradres tijdens het afrekenen. Opties: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Winkelweergave | Hiermee bepaalt u het maximum aantal items dat in het dialoogvenster _Overzicht van bestellingen_ tijdens het afrekenen. De standaardwaarde is `10`. |
| [!UICONTROL Enable Address Search] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (Alleen Adobe Commerce) Hiermee wordt bepaald of klanten deze functie kunnen gebruiken [adreszoekopdracht](../../stores-purchase/checkout-address-search.md) functionaliteit voor verzending en de stappen Controleren en betalen. Als deze optie is ingeschakeld, gebruikt u Limiet voor aantal klantadressen om het aantal opgeslagen adressen in te stellen dat vereist is om deze functie tijdens het uitchecken te activeren. Opties: `Yes` / `No` |
| Limiet voor aantal adressen van klanten | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (Alleen Adobe Commerce) Wanneer zoeken naar adressen is ingeschakeld, bepaalt u het aantal opgeslagen adressen dat is vereist om deze functie te activeren tijdens het uitchecken. Wanneer het aantal opgeslagen adressen van de klant aan dit aantal of overschrijdt, slechts wordt het standaardadres teruggegeven op _Verzending_ en _Reviseren en betalen_ stappen. De klant kan een zoekfunctie gebruiken om het geselecteerde adres te wijzigen. De standaardwaarde is `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Winkelwagentje](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Website | Hiermee bepaalt u de [levensduur van een genoteerde prijs](../../stores-purchase/cart-configuration.md#quote-lifetime), in dagen. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Winkelweergave | Hiermee wordt bepaald of de [winkelwagentje wordt weergegeven](../../stores-purchase/cart-configuration.md#redirect-to-cart) onmiddellijk nadat een product aan het karretje is toegevoegd. Opties: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Winkelweergave | Hiermee bepaalt u het aantal artikelen in het winkelwagentje voordat de pager wordt geactiveerd. Standaardwaarde: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Winkelweergave | Geeft aan of [cross-sell-objecten](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) worden weergegeven in het winkelwagentje, waardoor klanten extra verkoopopties krijgen. Opties: `Yes` (standaardwaarde) / `No` |
| [!UICONTROL Grouped Product Image] | Winkelweergave | Hiermee bepaalt u de [miniatuur](../../stores-purchase/cart-configuration.md#cart-thumbnails) afbeelding die wordt weergegeven voor een [gegroepeerd product](../../catalog/product-create-grouped.md) in het winkelwagentje. Opties: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Winkelweergave | Hiermee bepaalt u de [miniatuur](../../stores-purchase/cart-configuration.md#cart-thumbnails) afbeelding die wordt weergegeven voor een configureerbaar product in het winkelwagentje. Opties: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Winkelweergave | Hiermee bepaalt u de maximumleeftijd van de prijsopgave in minuten bij voorvertoond winkelwagentje. |
| [!UICONTROL Enable Clear Shopping Cart] | Website | Hiermee bepaalt u of in het winkelwagentje de optie wordt weergegeven waarmee gebruikers de inhoud van het winkelwagentje in één handeling kunnen wissen. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Mijn winkelwagentje](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Website | Bepaalt de waarde die tussen haakjes na de koppeling Mijn winkelwagen wordt weergegeven. Opties: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini Cart

![Mini Cart](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Winkelweergave | Hiermee bepaalt u of de miniwinkelwagentje op de winkelpagina&#39;s wordt weergegeven wanneer op het winkelwagentje in de koptekst wordt geklikt. De weergave van de minikaart is afhankelijk van het thema. Opties: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Winkelweergave | Hiermee bepaalt u het aantal items dat in de miniwinkelwagen kan worden weergegeven voordat de schuifbalk wordt geactiveerd. Standaard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Winkelweergave | Hiermee bepaalt u het maximum aantal items dat in de miniwinkelwagen kan worden weergegeven. Standaard: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![Betaling is mislukt](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Winkelweergave | Identificeert de contactpersoon van de winkel die de e-mail met betalingsfout ontvangt. Standaardontvanger: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Winkelweergave | Identificeert de opslagcontactpersoon die wordt weergegeven als de afzender van het bericht Betaling Ontbroken e-mails. Standaardafzender: `General Contact` |
| [!UICONTROL Payment Failed Template] | Winkelweergave | Identificeert de sjabloon die wordt gebruikt voor mislukte e-mails over betalingen. Standaardsjabloon: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Winkelweergave | Verstrekt het e-mailadres van iedereen om een exemplaar van een Ontbroken e-mail van de Betaling te ontvangen. Scheid meerdere adressen met een komma. |
| [!UICONTROL Send Payment Failed Copy Method] | Winkelweergave | Geeft de e-mailmethode aan die wordt gebruikt om de kopie te verzenden. Opties: <br />**`Bcc`**- Verstuurt een blinde hoffelijkheid kopie door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.<br />**`Separate Email`** - Hiermee verzendt u de kopie als een aparte e-mail. |

{style="table-layout:auto"}
