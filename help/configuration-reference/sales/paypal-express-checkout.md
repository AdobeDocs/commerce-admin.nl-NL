---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Express Checkout]'
description: Controleer de configuratie-instellingen in de sectie [!UICONTROL PayPal Express Checkout] op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] van Commerce Admin.
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1702'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**PSD2 Vereisten:** <br/>
>Vanaf 14 september 2019, zouden de Europese banken betalingen kunnen verminderen die niet [&#x200B; PSD2 &#x200B;](../../getting-started/compliance-payment-services-directive.md) vereisten voldoen. Er is geen actie nodig om PayPal Express Checkout te laten voldoen aan PSD2 omdat alle vereisten door PayPal worden afgehandeld.

{{config}}

## [!UICONTROL Required PayPal Settings]

![&#x200B; Uitdrukkelijke de Afhandeling van PayPal Vereiste Montages &#x200B;](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable this Solution] | Website | Activeert [!DNL PayPal Express Checkout] als een betalingsmethode die beschikbaar is voor uw klanten. Opties: `Yes` / `No` |
| [!UICONTROL Enable In-Context Checkout Experience] | Website | Hiermee activeert u gestroomlijnde PayPal In-Context Checkout als een betalingsmethode die beschikbaar is voor uw klanten. Opties: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit] | Website | Hiermee activeert u PayPal-krediet zodat klanten nu kunnen kopen, maar later kunnen betalen. Je krijgt vooraf betaald, maar klanten hebben meer tijd om te betalen. Opties: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Express Checkout]

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Website | Hier geeft u het e-mailadres op dat u hebt opgegeven bij de oprichting van uw PayPal-handelsaccount. Het e-mailadres is hoofdlettergevoelig en moet precies overeenkomen met uw e-mailadres in het PayPal-systeem. |
| [!UICONTROL API Authentication Methods] | Website | Bepaalt welke methode wordt gebruikt voor API-verificatie. Opties: <br/>**`API Signature`**- geeft het veld _[!UICONTROL API Signature]_&#x200B;in het formulier weer.<br/>**`API Certificate`**- Hiermee geeft u het veld&#x200B;_[!UICONTROL API Certificate]_ in het formulier weer. |
| [!UICONTROL API Username] | Website | De API-gebruikersnaam die is gekoppeld aan uw PayPal Merchant-account. |
| [!UICONTROL API Password] | Website | Het API-wachtwoord dat aan uw PayPal-zakelijke account is gekoppeld. |
| [!UICONTROL API Signature] | Website | De API-handtekening die is gekoppeld aan uw PayPal Merchant-account. |
| [!UICONTROL API Certificate] | Website | Blader om uw API-certificaat te uploaden. |
| [!UICONTROL Get Credentials from PayPal] |  | Hiermee worden uw API-referenties opgehaald van PayPal. |
| [!UICONTROL Sandbox Credentials] |  | Hiermee worden uw sandboxreferenties opgehaald van PayPal. |
| [!UICONTROL Sandbox Mode] | Website | Als u PayPal Express Checkout wilt uitvoeren in een testomgeving, voert u uw API-referenties voor de sandbox in en stelt u deze in op `Yes` . Opties: `Yes` / `No` |
| [!UICONTROL API Uses Proxy] | Website | Als uw systeem een proxyserver gebruikt om de verbinding tussen Commerce en het PayPal-systeem tot stand te brengen, stelt u deze in op `Yes` . Opties: `Yes` / `No` |
| [!UICONTROL Proxy Host] | Website | Als de API proxy gebruikt, geeft dit het IP-adres van de proxyhost op. |
| [!UICONTROL Proxy Port] | Website | Als de API proxy gebruikt, geeft dit de poort op die door de proxyhost wordt gebruikt. |

{style="table-layout:auto"}

### [!UICONTROL Advertise PayPal Credit]

![&#x200B; Adverteer PayPal Krediet &#x200B;](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Website | De uitgevers-id die aan uw PayPal-creditaccount is gekoppeld. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Hiermee wordt uw uitgevers-id opgehaald uit PayPal. |
| [!UICONTROL Home Page] | Website | Bepaalt de positie en de grootte van de [!DNL PayPal Credit] -banner op de startpagina. Opties: <br/>**Vertoning** - toont a [!DNL PayPal Credit] banner op de homepage van uw opslag. Opties: `Yes` / `No` <br/>**Positie** - bepaalt de positie van de [!DNL PayPal Credit] banner op de homepage. Opties: Kopbal (centrum) / Zijbalk (recht) <br/>**Grootte** - bepaalt de grootte van de [!DNL PayPal Credit] banner op de homepage. Opties: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Website | Bepaalt de positie en grootte van de banner [!DNL PayPal Credit] op categoriepagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Website | Bepaalt de positie en de grootte van de [!DNL PayPal Credit] -banner op productpagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Website | Hiermee bepaalt u de positie en grootte van de [!DNL PayPal Credit] -banner op de winkelwagentpagina. Opties: (gelijk aan voor [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![&#x200B; Basismontages &#x200B;](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Title] | Winkelweergave | Een naam die de PayPal Express-betalingsmethode voor afhandeling tijdens de afhandeling aangeeft. |
| [!UICONTROL Sort Order] | Winkelweergave | Een getal dat de volgorde bepaalt waarin PayPal Express Checkout wordt weergegeven bij aanbiedingen met andere betalingsmethoden tijdens het afrekenen. Voer `0` in voor de bovenkant van de lijst. |
| [!UICONTROL Payment Action] | Website | Bepaalt welke actie PayPal onderneemt wanneer het een bestelling ontvangt. Opties: <br/>**`Authorization`**- hiermee gaat u akkoord met de aankoop, maar u houdt de middelen in de wacht. De hoeveelheid wordt pas opgevraagd wanneer deze door de handelaar wordt &quot;gevangen&quot;.<br/>**`Sale`** - Het bedrag van de aankoop wordt geautoriseerd en onmiddellijk van de rekening van de klant teruggetrokken. <br/>**`Order`**- Vertegenwoordigt een overeenkomst met PayPal die de handelaar toestaat om één of meerdere bedragen tot het geordende totaal van de kopersrekening van de klant, binnen een bepaalde tijdspanne te vangen. Dit kan tot 29 dagen zijn. Een of meer facturen moeten door de Commerce Admin worden gegenereerd om de middelen te kunnen opnemen. |
| [!UICONTROL Display on Product Details Page] | Winkelweergave | Hiermee wordt bepaald of de knop Afhandeling met PayPal op productpagina&#39;s wordt weergegeven. De volgende opties zijn beschikbaar: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![&#x200B; Geavanceerde Montages &#x200B;](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Winkelweergave | Hiermee wordt bepaald of PayPal Express Checkout wordt weergegeven als een betalingsoptie in het winkelwagentje. Opties: `Yes` (PayPal aanbevolen) / `No` |
| [!UICONTROL Payment Action Applicable From] | Website | Hiermee bepaalt u het bereik van de toepasselijke landselectie. Opties: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Website | Identificeert elk land van waaruit betaling wordt geaccepteerd. Alleen klanten met een factuuradres in een geselecteerd land kunnen aankopen doen met deze betalingsmethode. |
| [!UICONTROL Debug Mode] | Website | Registreert berichten die tussen uw winkel en het betalingssysteem worden verzonden in een logbestand. Opties: `Yes` / `No` <br/><br/>**_Nota:_**&#x200B;het logboekdossier wordt opgeslagen op de server en is toegankelijk slechts voor ontwikkelaars. In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier. |
| [!UICONTROL Enable SSL Verification] | Website | Schakelt verificatie van het beveiligingscertificaat van de host in. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Geeft een volledig overzicht weer van de lijstitems van het winkelwagentje van de klant op de Paypal-site. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Website | Bevat maximaal tien verzendopties op de PayPal-site. Opties: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Winkelweergave | Hiermee bepaalt u het type afbeelding dat wordt gebruikt voor de PayPal-acceptatieknop. Opties: <br/>**`Dynamic`**- (aanbevolen) Hiermee geeft u een afbeelding weer die dynamisch kan worden gewijzigd van de PayPal-server.<br/>**`Static`** - Geeft een statische afbeelding weer die niet dynamisch kan worden gewijzigd. |
| [!UICONTROL Enable PayPal Guest Checkout] | Website | Klanten die geen PayPal-rekening hebben, kunnen aankopen doen met PayPal Express Checkout. Opties: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Website | Hiermee bepaalt u of het factuuradres van de klant is vereist. Opties: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Website | Bepaalt als de klanten in a [&#x200B; het factureren overeenkomst &#x200B;](../../stores-purchase/paypal-billing-agreements.md) met uw opslag kunnen ingaan. Opties: <br/>**`Auto`**- de klant kan zich aanmelden voor een factureringsovereenkomst tijdens Express Checkout.<br/>**`Ask Customer`** - De klant wordt gevraagd of hij of zij zich wil aanmelden voor een factureringsovereenkomst. <br/>**`Never`**- Klanten kunnen zich niet aanmelden voor een factureringsovereenkomst. |
| [!UICONTROL Skip Order Review Step] | Website | Hiermee bepaalt u of klanten de transactie kunnen voltooien vanaf de PayPal-site of dat ze naar uw winkel moeten terugkeren en de stap Bestelrevisie moeten voltooien voordat ze de bestelling verzenden. Opties: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Billing Agreement Settings]

![&#x200B; het Factureren de Montages van de Overeenkomst &#x200B;](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Als factureringsovereenkomsten ingeschakeld zijn, worden deze tijdens het afrekenen als een betalingsoptie weergegeven. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | Het label voor de optie voor de PayPal-factureringsovereenkomst dat tijdens het afrekenen als een betalingsoptie wordt weergegeven. |
| [!UICONTROL Sort Order] | Winkelweergave | Hiermee bepaalt u de volgorde waarin factureringsovereenkomsten tijdens het afrekenen met andere betalingsmethoden worden weergegeven. |
| [!UICONTROL Payment Action] | Website | Bepaalt hoe PayPal de transactie beheert: Opties: <br/>**Vergunning** - keurt de aankoop goed, maar zet een greep op de middelen. De hoeveelheid wordt pas opgevraagd wanneer deze door de handelaar wordt &quot;gevangen&quot;. <br/>**Verkoop** - het bedrag van de aankoop wordt geautoriseerd en onmiddellijk teruggetrokken van de rekening van de klant. |
| [!UICONTROL Payment Applicable From] | Website | Hiermee bepaalt u het bereik van de toepasselijke landselectie. Opties: alle toegestane landen / specifieke landen |
| [!UICONTROL Countries Payment Applicable From] | Website | Identificeert elk land van waaruit betaling wordt geaccepteerd. Alleen klanten met een factuuradres in een geselecteerd land kunnen aankopen doen met deze betalingsmethode. |
| [!UICONTROL Debug Mode] | Website | Registreert communicatie met het betalingssysteem in een logboekdossier. Opties: `Yes` / `No` <br/><br/>**_Nota:_**&#x200B;het logboekdossier wordt opgeslagen op de server en is toegankelijk slechts voor ontwikkelaars. In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier. |
| [!UICONTROL Enable SSL Verification] | Website | Hiermee schakelt u een verificatiestap in die ervoor zorgt dat de transactie plaatsvindt via een gecodeerd SSL-kanaal. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Als deze optie is ingeschakeld, wordt een overzicht weergegeven van de regelobjecten in het winkelwagentje op de PayPal-betalingspagina. Opties: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Website | Wanneer deze optie is ingeschakeld, kunnen klanten een factureringsovereenkomst starten vanaf het dashboard van hun klantenaccount. |

{style="table-layout:auto"}

### [!UICONTROL Settlement Report Settings]

![&#x200B; de Montages van het Rapport van de Oplossing &#x200B;](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Website | Uw gebruikersnaam die is vereist om u aan te melden bij de Secure FTP-server van PayPal. |
| [!UICONTROL Password] | Website | Uw wachtwoord dat is vereist om u aan te melden bij de Secure FTP-server van PayPal. |
| [!UICONTROL Sandbox Mode] | Website | Wanneer toegelaten, looppas rapporten in een testmilieu alvorens &quot;levend&quot;in het productiemilieu te gaan. Opties: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Website | De URL waar afwikkelingsrapporten worden beheerd. Standaardwaarde: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Website | Het pad waar afwikkelingsrapporten op uw server worden opgeslagen. Standaardwaarde: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Website | Als deze optie is ingeschakeld, worden afwikkelingsrapporten automatisch volgens schema opgehaald. Opties: `Yes` / `No` |
| [!UICONTROL Schedule] | Website | Hiermee bepaalt u hoe vaak afwikkelingsrapporten worden gegenereerd door PayPal. Opties: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Website | Bepaalt het uur, de minuut en de seconde dat afwikkelingsrapporten worden gegenereerd. |

{style="table-layout:auto"}

### [!UICONTROL Frontend Experience Settings]

![&#x200B; de Montages van de Voorwaartse Ervaring - de Verkoopbare Stijl van Pagina&#39;s van PayPal &#x200B;](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Winkelweergave | Hiermee bepaalt u het PayPal-logo dat in uw winkel wordt weergegeven. Er zijn vier basisstijlen in twee formaten. Opties: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | Winkelweergave | Hiermee bepaalt u de weergave van de handelspagina van PayPal. Toegestane waarden: **`paypal`** - Gebruikt de paginastijl van PayPal. <br/>**`primary`**- Gebruikt de paginastijl die u hebt geïdentificeerd als de &quot;primaire&quot; stijl in uw accountprofiel.<br/>**`your_custom_value`** - Gebruikt een aangepaste paginastijl voor betalingen, die in uw accountprofiel is opgegeven. |
| [!UICONTROL Header Image URL] | Winkelweergave | De URL van de afbeelding die in de linkerbovenhoek van de uitcheckpagina wordt weergegeven. De maximale grootte is 750 x 90 pixels. <br/><br/>**_Nota:_**&#x200B;PayPal adviseert dat het beeld op een veilige (https) server wordt opgeslagen. Anders kan de browser van de klant waarschuwen dat de pagina zowel beveiligde als niet-beveiligde items bevat. |
| [!UICONTROL Header Image Background Color] | Winkelweergave | De zes karakter [&#x200B; hexadecimale kleur &#x200B;](https://en.wikipedia.org/wiki/Web_colors) code voor de achtergrondkleur van de kopbal op de controlepagina. U kunt de code invoeren in hoofdletters en kleine letters. |
| [!UICONTROL Header Image Border Color] | Winkelweergave | De zes karakter [&#x200B; hexadecimale kleur &#x200B;](https://en.wikipedia.org/wiki/Web_colors) code voor de twee-pixelgrens rond de kopbal. |
| [!UICONTROL Page Background Color] | Winkelweergave | De zes karakter [&#x200B; hexadecimale kleur &#x200B;](https://en.wikipedia.org/wiki/Web_colors) code voor de achtergrondkleur van de controlepagina die achter de kopbal en betalingsvorm verschijnt. |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![&#x200B; de Montages van de Begaring van de Voorkant - pas Slimme Knopen &#x200B;](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom --> aan

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Customize Button] | Winkelweergave | Hiermee bepaalt u of de slimme PayPal-knoppen kunnen worden aangepast aan de indeling en het thema van uw winkel. U kunt deze wijzigingen afzonderlijk toepassen op de pagina Afhandeling, op productpagina&#39;s, op de pagina Winkelwagentje en in de miniwagentje. |
| [!UICONTROL Label] | Winkelweergave | De tekst die PayPal weergeeft op de knop Slimme betaling. Opties: <br/>**`Checkout`**(wordt weergegeven als &quot;PayPal-kassa&quot;)<br/>**`Pay`** (wordt weergegeven als &quot;PayPal&quot;) <br/>**`Buy Now`**(wordt weergegeven als &quot;Nu kopen met PayPal&quot;)<br/>**`PayPal`** (wordt weergegeven als &quot;PayPal&quot;) <br/>**`Installment`**(wordt weergegeven als &quot;PayPal&quot;)<br/>**`Credit`** (wordt weergegeven als &quot;PayPal CREDIT&quot;) |
| [!UICONTROL Layout] | Winkelweergave | Bepaalt of slimme PayPal-knoppen verticaal of horizontaal moeten worden weergegeven. Opties: <br/>**`Vertical`**- De koper moet zich aanmelden bij PayPal of een PayPal-rekening maken, ongeacht of &quot;Uitchecken door gasten inschakelen&quot; is geselecteerd.<br/>**`Horizontal`** - Wanneer &quot;Uitchecken door gasten inschakelen&quot; is geselecteerd, wordt de knop **`Pay with Debit Card or Credit Card`** weergegeven in het pop-upvenster van PayPal. Anders moet de koper zich aanmelden bij PayPal of een PayPal-rekening maken. |
| [!UICONTROL Size] | Winkelweergave | Hiermee stelt u de grootte van de knop Slimme betaling in. Opties: <br/>**`Medium`**- 250 pixels bij 35 pixels<br/>**`Large`** - 350 pixels bij 40 pixels <br/>**`Responsive`**- (standaardinstelling) Hiermee past u de breedte van de container aan. De minimale breedte is 100 pixels en de maximale breedte is 500 pixels. De hoogte wordt dynamisch aangepast op basis van de breedte. |
| [!UICONTROL Shape] | Winkelweergave | Hiermee geeft u de vorm van de knop Slimme betaling op. Opties: `Pill` (standaardwaarde) / `Rectangle` |
| [!UICONTROL Color] | Winkelweergave | Stel de kleur van de knop Slim betalen in. Opties: `Gold` (standaardwaarde) / `Blue` / `Silver` / `Black` |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Features)]

![&#x200B; de Montages van de Begaring van de Voorkant - pas Slimme Knopen (Eigenschappen) aan &#x200B;](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Disable Funding Options] | Winkelweergave | Hiermee bepaalt u welke andere PayPal-financieringsopties worden weergegeven op de pagina Uitchecken. De geselecteerde opties worden nooit weergegeven op de pagina Uitchecken. Niet-geselecteerde opties worden alleen weergegeven als PayPal de valuta van de winkel en de locatie van de koper ondersteunt. Opties: `PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV` |

{style="table-layout:auto"}
