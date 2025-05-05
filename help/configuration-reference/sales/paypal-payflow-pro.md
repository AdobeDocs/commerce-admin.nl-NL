---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt;  [!UICONTROL PayPal Payflow Pro]'
description: Controleer de configuratie-instellingen in de sectie [!UICONTROL PayPal Payflow Pro] op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] van Commerce Admin.
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2 Vereisten:** <br/>
>Vanaf 14 september 2019, zouden de Europese banken betalingen kunnen verminderen die niet [ PSD2 ](../../getting-started/compliance-payment-services-directive.md) vereisten voldoen. [!DNL PayPal Payflow Pro] moet zijn geïntegreerd met [!DNL Cardinal Commerce] om te voldoen aan PSD2. Meer leren, zie [ 3-D Veilig voor Payflow ](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![ Vereiste Montages ](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Website | (Optioneel) Alle e-mailadressen die aan uw PayPal-zakelijke account zijn gekoppeld. E-mailadressen zijn hoofdlettergevoelig en moeten exact overeenkomen met de adressen in uw account. |
| [!UICONTROL Partner] | Website | Uw PayPal Partner-id, indien van toepassing. |
| [!UICONTROL Vendor] | Website | De gebruikersnaam van uw PayPal-gebruikersaanmelding. |
| Gebruiker | Website | De id van een andere gebruiker op je PayPal-rekening. |
| [!UICONTROL Password] | Website | Het wachtwoord dat aan uw PayPal-handelsaccount is gekoppeld. |
| [!UICONTROL Test Mode] | Website | Als deze optie is ingeschakeld, wordt PayPal Payflow Pro uitgevoerd in een testomgeving. Schakel de testmodus uit als u in de productiemodus &quot;live&quot; wilt gaan. Opties: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Website | Een proxy kan worden gebruikt om verkeer om te leiden wanneer de serverfirewall directe toegang tot de PayPal-server voorkomt. Indien van toepassing, identificeert de proxyserver die wordt gebruikt om verbinding te maken met de PayPal-server. Opties: `Yes` / `No` <br/><br/> Indien ingeschakeld, stelt u de proxyopties in: <br/>**`Proxy Host`**- Het IP-adres van de proxyhost.<br/>**`Proxy Port`** - Het nummer van de proxypoort. |
| [!UICONTROL Enable this Solution] | Website | Hiermee bepaalt u of PayPal Payflow Pro voor uw klanten beschikbaar is als betalingsmethode. |
| [!UICONTROL Enable PayPal Credit] | Website | Hiermee wordt bepaald of PayPal-krediet beschikbaar is voor uw klanten als betalingsoptie. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![ Adverteer PayPal Krediet ](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Website | De uitgevers-id die aan uw PayPal-creditaccount is gekoppeld. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Hiermee wordt uw uitgevers-id opgehaald uit PayPal. |
| [!UICONTROL Home Page] | Website | Bepaalt de positie en de grootte van de [!DNL PayPal Credit] -banner op de startpagina. Opties: <br/>**`Display`**- bepaalt of een [!DNL PayPal Credit] banner op de homepage van uw opslag wordt getoond. Opties: `Yes` / `No`<br/>**`Position`** - Hiermee bepaalt u de positie van de [!DNL PayPal Credit] banner op de startpagina. Opties: Koptekst (midden) / Zijbalk (rechts) <br/>**`Size`**- Hiermee bepaalt u de grootte van de [!DNL PayPal Credit] -banner op de startpagina. Opties: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Website | Bepaalt de positie en grootte van de banner [!DNL PayPal Credit] op categoriepagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Website | Bepaalt de positie en de grootte van de [!DNL PayPal Credit] -banner op productpagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Website | Hiermee bepaalt u de positie en grootte van de [!DNL PayPal Credit] -banner op de winkelwagentpagina. Opties: (gelijk aan voor [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![ Basismontages ](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Title] | Winkelweergave | Een naam die PayPal Payflow Pro identificeert als een betalingsmethode tijdens de afhandeling. |
| [!UICONTROL Sort Order] | Winkelweergave | Een getal dat de volgorde bepaalt waarin PayPal Payflow Pro wordt weergegeven wanneer het bij andere betalingsmethoden wordt aangeboden tijdens het afrekenen. |
| [!UICONTROL Payment Action] | Website | Bepaalt welke actie PayPal onderneemt wanneer een bestelling wordt verzonden. Opties: <br/>**`Authorization`**- hiermee gaat u akkoord met de aankoop, maar u houdt de middelen in de wacht. De hoeveelheid wordt pas opgevraagd wanneer deze door de handelaar wordt &quot;gevangen&quot;.<br/>**`Sale`** - Het bedrag van de aankoop wordt geautoriseerd en onmiddellijk van de rekening van de klant teruggetrokken. |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Website | Bepaalt welke creditcards beschikbaar zijn voor klanten tijdens het afrekenen. Selecteer elke ondersteunde kaart. Opties: `American Express` (hiervoor is een extra overeenkomst vereist) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![ Geavanceerde Montages ](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| Weergeven bij winkelwagentje | Winkelweergave | Hiermee wordt bepaald of PayPal Express Checkout wordt weergegeven als een betalingsoptie in het winkelwagentje. Opties: Ja (aanbevolen) / Nee |
| [!UICONTROL Payment Action Applicable From] | Website | Hiermee bepaalt u het bereik van de toepasselijke landselectie. Opties: alle toegestane landen / specifieke landen |
| [!UICONTROL Countries Payment Applicable From] | Website | Identificeert elk land van waaruit betaling wordt geaccepteerd. Alleen klanten met een factuuradres in een geselecteerd land kunnen aankopen doen met deze betalingsmethode. |
| [!UICONTROL Debug Mode] | Website | Hiermee worden berichten die tussen je winkel en het PayPal-betalingssysteem zijn verzonden, in een logbestand vastgelegd. Opties: `Yes` / `No` <br/><br/>**_Nota:_**&#x200B;het logboekdossier wordt opgeslagen op de server en is toegankelijk slechts voor ontwikkelaars. In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier. |
| [!UICONTROL Enable SSL Verification] | Website | Schakelt verificatie van het beveiligingscertificaat van de host in. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Geeft een volledig overzicht weer van de lijstitems van het winkelwagentje van de klant op de Paypal-site. Opties: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Website | Hiermee bepaalt u of klanten de transactie kunnen voltooien vanaf de PayPal-site of dat ze naar uw winkel moeten terugkeren en de stap Bestelrevisie moeten voltooien voordat ze de bestelling verzenden. Opties: `Yes` / `No` |

{style="table-layout:auto"}
