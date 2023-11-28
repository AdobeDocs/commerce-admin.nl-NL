---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Standard]'
description: Controleer de configuratie-instellingen in het dialoogvenster [!UICONTROL PayPal Payments Standard] de [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] pagina van de Commerce Admin.
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**PSD2 Eisen:**<br/>
>Vanaf 14 september 2019 zouden Europese banken betalingen kunnen terugdringen die niet voldoen aan [PSD 2](../../getting-started/compliance-payment-services-directive.md) eisen. Er is geen actie nodig voor [!DNL PayPal Payments Standard] om te voldoen aan PSD2, omdat alle vereisten worden afgehandeld door PayPal.

{{config}}

## [!UICONTROL Required Settings]

![Vereiste instellingen](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Website | (Optioneel) Alle e-mailadressen die aan uw PayPal-zakelijke account zijn gekoppeld. E-mailadressen zijn hoofdlettergevoelig en moeten exact overeenkomen met de adressen in uw account. |
| [!UICONTROL Partner] | Website | Uw PayPal Partner-id, indien van toepassing. |
| [!UICONTROL Vendor] | Website | De gebruikersnaam van uw PayPal-gebruikersaanmelding. |
| Gebruiker | Website | De id van een andere gebruiker op je PayPal-rekening. |
| [!UICONTROL Password] | Website | Het wachtwoord dat aan uw PayPal-handelsaccount is gekoppeld. |
| [!UICONTROL Test Mode] | Website | Als deze optie is ingeschakeld, wordt PayPal Payments Pro uitgevoerd in een testomgeving. Schakel de testmodus uit als u in de productiemodus &quot;live&quot; wilt gaan. Opties: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Website | Een proxy kan worden gebruikt om verkeer om te leiden wanneer de serverfirewall directe toegang tot de PayPal-server voorkomt. Indien van toepassing, identificeert de proxyserver die wordt gebruikt om verbinding te maken met de PayPal-server. Opties: `Yes` / `No` <br/><br/>Indien ingeschakeld, stelt u de opties in: <br/>**`Proxy Host`**- Het IP-adres van de proxyhost.<br/>**`Proxy Port`** - Het nummer van de proxypoort. |
| [!UICONTROL Enable this Solution] | Website | Hiermee bepaalt u of PayPal Payments Pro beschikbaar is voor uw klanten als betalingsmethode. |
| [!UICONTROL Enable PayPal Credit] | Website | Hiermee wordt bepaald of PayPal-krediet beschikbaar is voor uw klanten als betalingsoptie. |

{:style=&quot;table-layout:auto&quot;}

## PayPal-krediet adverteren

![PayPal-krediet adverteren](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Website | De uitgevers-id die aan uw PayPal-creditaccount is gekoppeld. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Hiermee wordt uw uitgevers-id opgehaald uit PayPal. |
| [!UICONTROL Home Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op de startpagina. Opties: <br/>**`Display`**- Hiermee wordt bepaald of een [!DNL PayPal Credit] banner wordt weergegeven op de homepage van uw winkel. Opties: `Yes` / `No`<br/>**`Position`** - Bepaalt de positie van [!DNL PayPal Credit] banner op de startpagina. Opties: `Header (center)` / `Sidebar (right)` <br/>**`Size`**- Hiermee bepaalt u de grootte van de [!DNL PayPal Credit] banner op de startpagina. Opties: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op categoriepagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op productpagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op winkelwagentje. Opties: (gelijk aan voor [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![Basisinstellingen](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Title] | Winkelweergave | Een naam die PayPal Payments Pro identificeert als betalingsmethode tijdens het afrekenen. |
| [!UICONTROL Sort Order] | Winkelweergave | Een getal dat de volgorde bepaalt waarin PayPal Payments Pro wordt weergegeven wanneer het bij andere betalingsmethoden wordt aangeboden tijdens het afrekenen. |
| [!UICONTROL Payment Action] | Website | Bepaalt welke actie PayPal onderneemt wanneer een bestelling wordt verzonden. Opties: <br/>**`Authorization`**- Goedkeuring van de aankoop, maar blokkeert de middelen. De hoeveelheid wordt pas opgevraagd wanneer deze door de handelaar wordt &quot;gevangen&quot;.<br/>**`Sale`** - Het bedrag van de aankoop wordt toegestaan en onmiddellijk van de rekening van de klant teruggetrokken. |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Website | Bepaalt welke creditcards beschikbaar zijn voor klanten tijdens het afrekenen. Selecteer elke ondersteunde kaart. Opties: `American Express` (hiervoor is een extra overeenkomst vereist) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![Geavanceerde instellingen](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Winkelweergave | Hiermee wordt bepaald of PayPal Express Checkout wordt weergegeven als een betalingsoptie in het winkelwagentje. Opties: `Yes` (aanbevolen) / `No` |
| [!UICONTROL Payment Action Applicable From] | Website | Hiermee bepaalt u het bereik van de toepasselijke landselectie. Opties: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Website | Identificeert elk land van waaruit betaling wordt geaccepteerd. Alleen klanten met een factuuradres in een geselecteerd land kunnen aankopen doen met deze betalingsmethode. |
| [!UICONTROL Debug Mode] | Website | Hiermee worden berichten die tussen je winkel en het PayPal-betalingssysteem zijn verzonden, in een logbestand vastgelegd. Opties: `Yes` / `No` <br/><br/>**_Opmerking:_**Het logbestand wordt opgeslagen op de server en is alleen toegankelijk voor ontwikkelaars. In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier. |
| [!UICONTROL Enable SSL Verification] | Website | Schakelt verificatie van het beveiligingscertificaat van de host in. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Geeft een volledig overzicht weer van de lijstitems van het winkelwagentje van de klant op de Paypal-site. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Website | Bevat maximaal tien verzendopties op de PayPal-site. Opties: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Winkelweergave | Hiermee bepaalt u het type afbeelding dat wordt gebruikt voor de PayPal-acceptatieknop. Opties: <br/>**`Dynamic`**- (Aanbevolen) Hiermee wordt een afbeelding weergegeven die dynamisch kan worden gewijzigd van de PayPal-server.<br/>**`Static`** - Geeft een statische afbeelding weer die niet dynamisch kan worden gewijzigd. |
| [!UICONTROL Enable PayPal Guest Checkout] | Website | Klanten die geen PayPal-rekening hebben, kunnen aankopen doen met PayPal Express Checkout. Opties: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Website | Hiermee bepaalt u of het factuuradres van de klant is vereist. Opties: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Website | Hiermee bepaalt u of klanten een [factureringsovereenkomst](../../stores-purchase/paypal-billing-agreements.md) met uw winkel. Opties: <br/>**`Auto`**- De klant kan zich aanmelden voor een factureringsovereenkomst tijdens de Express Checkout.<br/>**`Ask Customer`** - De klant wordt gevraagd of hij zich wil aanmelden voor een factureringsovereenkomst. <br/>**`Never`**- Klanten kunnen zich niet aanmelden voor een factureringsovereenkomst. |
| [!UICONTROL Skip Order Review Step] | Website | Hiermee bepaalt u of klanten de transactie kunnen voltooien vanaf de PayPal-site of dat ze naar uw winkel moeten terugkeren en de stap Bestelrevisie moeten voltooien voordat ze de bestelling verzenden. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Billing Agreement Setting]

![Instellingen factureringsovereenkomst](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Als factureringsovereenkomsten ingeschakeld zijn, worden deze tijdens het afrekenen als een betalingsoptie weergegeven. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | Het label voor de optie voor de PayPal-factureringsovereenkomst dat tijdens het afrekenen als een betalingsoptie wordt weergegeven. |
| [!UICONTROL Sort Order] | Winkelweergave | Hiermee bepaalt u de volgorde waarin factureringsovereenkomsten tijdens het afrekenen met andere betalingsmethoden worden weergegeven. |
| [!UICONTROL Payment Action] | Website | Bepaalt hoe PayPal de transactie beheert: Opties: <br/>**`Authorization`**- Goedkeuring van de aankoop, maar blokkeert de middelen. De hoeveelheid wordt pas opgevraagd wanneer deze door de handelaar wordt &quot;gevangen&quot;.<br/>**`Sale`** - Het bedrag van de aankoop wordt toegestaan en onmiddellijk van de rekening van de klant teruggetrokken. |
| [!UICONTROL Payment Applicable From] | Website | Hiermee bepaalt u het bereik van de toepasselijke landselectie. Opties: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Website | Identificeert elk land van waaruit betaling wordt geaccepteerd. Alleen klanten met een factuuradres in een geselecteerd land kunnen aankopen doen met deze betalingsmethode. |
| [!UICONTROL Debug Mode] | Website | Registreert communicatie met het betalingssysteem in een logboekdossier. Opties: `Yes` / `No` <br/><br/>**_Opmerking:_**Het logbestand wordt opgeslagen op de server en is alleen toegankelijk voor ontwikkelaars. In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier. |
| [!UICONTROL Enable SSL Verification] | Website | Hiermee schakelt u een verificatiestap in die ervoor zorgt dat de transactie plaatsvindt via een gecodeerd SSL-kanaal. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Als deze optie is ingeschakeld, wordt een overzicht weergegeven van de regelobjecten in het winkelwagentje op de PayPal-betalingspagina. Opties: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Website | Wanneer deze optie is ingeschakeld, kunnen klanten een factureringsovereenkomst starten vanaf het dashboard van hun klantenaccount. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Settlement Report Settings]

![Instellingen voor afwikkelingsrapport](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Login] | Website | Uw gebruikersnaam die is vereist om u aan te melden bij de Secure FTP-server van PayPal. |
| [!UICONTROL Password] | Website | Uw wachtwoord dat is vereist om u aan te melden bij de Secure FTP-server van PayPal. |
| [!UICONTROL Sandbox Mode] | Website | Wanneer toegelaten, looppas rapporten in een testmilieu alvorens &quot;levend&quot;in het productiemilieu te gaan. Opties: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Website | De URL waar afwikkelingsrapporten worden beheerd. Standaardwaarde: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Website | Het pad waar afwikkelingsrapporten op uw server worden opgeslagen. Standaardwaarde: `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | Website | Als deze optie is ingeschakeld, worden afwikkelingsrapporten automatisch volgens schema opgehaald. Opties: `Yes` / `No` |
| [!UICONTROL Schedule] | Algemeen | Hiermee bepaalt u hoe vaak afwikkelingsrapporten worden gegenereerd door PayPal. Opties: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Algemeen | Bepaalt het uur, de minuut en de seconde dat afwikkelingsrapporten worden gegenereerd. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Frontend Experience Settings]

![Instellingen voor voorvertoning](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Winkelweergave | Hiermee bepaalt u het PayPal-logo dat in uw winkel wordt weergegeven. Er zijn vier basisstijlen in twee formaten. Opties: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | Winkelweergave | Hiermee bepaalt u de weergave van de handelspagina van PayPal. Toegestane waarden: <br/>**`paypal`**- Gebruikt de paginastijl van PayPal.<br/>**`primary`** - Gebruikt de paginastijl die u hebt geïdentificeerd als de &quot;primaire&quot; stijl in uw accountprofiel. <br/>**`your_custom_value`**- Hiermee gebruikt u een aangepaste paginastijl voor betalingen, die in uw accountprofiel is opgegeven. |
| [!UICONTROL Header Image URL] | Winkelweergave | De URL van de afbeelding die in de linkerbovenhoek van de uitcheckpagina wordt weergegeven. De maximale grootte is 750 x 90 pixels. <br/><br/>**_Opmerking:_**PayPal raadt aan de afbeelding op een beveiligde server (https) op te slaan. Anders kan de browser van de klant waarschuwen dat de pagina zowel beveiligde als niet-beveiligde items bevat. |
| [!UICONTROL Header Image Background Color] | Winkelweergave | Het zesteken [hexadecimale kleur](https://en.wikipedia.org/wiki/Web_colors) code voor de achtergrondkleur van de koptekst op de uitcheckpagina. U kunt de code invoeren in hoofdletters en kleine letters. |
| [!UICONTROL Header Image Border Color] | Winkelweergave | De hexadecimale kleurcode van zes tekens voor de rand van twee pixels rond de koptekst. |
| [!UICONTROL Page Background Color] | Winkelweergave | De hexadecimale kleurcode van zes tekens voor de achtergrondkleur van de uitcheckpagina die achter het koptekst- en betalingsformulier wordt weergegeven. |

{:style=&quot;table-layout:auto&quot;}
