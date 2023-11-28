---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt;  [!UICONTROL PayPal Payflow Pro]'
description: Controleer de configuratie-instellingen in het dialoogvenster [!UICONTROL PayPal Payflow Pro] de [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] pagina van de Commerce Admin.
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2 Eisen:** <br/>
>Vanaf 14 september 2019 zouden Europese banken betalingen kunnen terugdringen die niet voldoen aan [PSD 2](../../getting-started/compliance-payment-services-directive.md) eisen. Om te voldoen aan PSD2 [!DNL PayPal Payflow Pro] moet worden geïntegreerd met [!DNL Cardinal Commerce]. Zie voor meer informatie [3-D veilig voor Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Vereiste instellingen](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Website | (Optioneel) Alle e-mailadressen die aan uw PayPal-zakelijke account zijn gekoppeld. E-mailadressen zijn hoofdlettergevoelig en moeten exact overeenkomen met de adressen in uw account. |
| [!UICONTROL Partner] | Website | Uw PayPal Partner-id, indien van toepassing. |
| [!UICONTROL Vendor] | Website | De gebruikersnaam van uw PayPal-gebruikersaanmelding. |
| Gebruiker | Website | De id van een andere gebruiker op je PayPal-rekening. |
| [!UICONTROL Password] | Website | Het wachtwoord dat aan uw PayPal-handelsaccount is gekoppeld. |
| [!UICONTROL Test Mode] | Website | Als deze optie is ingeschakeld, wordt PayPal Payflow Pro uitgevoerd in een testomgeving. Schakel de testmodus uit als u in de productiemodus &quot;live&quot; wilt gaan. Opties: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Website | Een proxy kan worden gebruikt om verkeer om te leiden wanneer de serverfirewall directe toegang tot de PayPal-server voorkomt. Indien van toepassing, identificeert de proxyserver die wordt gebruikt om verbinding te maken met de PayPal-server. Opties: `Yes` / `No` <br/><br/>Indien ingeschakeld, stelt u de proxyopties in: <br/>**`Proxy Host`**- Het IP-adres van de proxyhost.<br/>**`Proxy Port`** - Het nummer van de proxypoort. |
| [!UICONTROL Enable this Solution] | Website | Hiermee bepaalt u of PayPal Payflow Pro voor uw klanten beschikbaar is als betalingsmethode. |
| [!UICONTROL Enable PayPal Credit] | Website | Hiermee wordt bepaald of PayPal-krediet beschikbaar is voor uw klanten als betalingsoptie. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advertise PayPal Credit]

![PayPal-krediet adverteren](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Website | De uitgevers-id die aan uw PayPal-creditaccount is gekoppeld. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Hiermee wordt uw uitgevers-id opgehaald uit PayPal. |
| [!UICONTROL Home Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op de startpagina. Opties: <br/>**`Display`**- Hiermee wordt bepaald of een[!DNL PayPal Credit] banner wordt weergegeven op de homepage van uw winkel. Opties: `Yes` / `No`<br/>**`Position`** - Bepaalt de positie van [!DNL PayPal Credit] banner op de startpagina. Opties: Koptekst (midden) / Zijbalk (rechts) <br/>**`Size`**- Hiermee bepaalt u de grootte van de [!DNL PayPal Credit] banner op de startpagina. Opties: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op categoriepagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op productpagina&#39;s. Opties: (gelijk aan voor [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Website | Hiermee bepaalt u de positie en de grootte van de [!DNL PayPal Credit] banner op winkelwagentje. Opties: (gelijk aan voor [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![Basisinstellingen](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Title] | Winkelweergave | Een naam die PayPal Payflow Pro identificeert als een betalingsmethode tijdens de afhandeling. |
| [!UICONTROL Sort Order] | Winkelweergave | Een getal dat de volgorde bepaalt waarin PayPal Payflow Pro wordt weergegeven wanneer het bij andere betalingsmethoden wordt aangeboden tijdens het afrekenen. |
| [!UICONTROL Payment Action] | Website | Bepaalt welke actie PayPal onderneemt wanneer een bestelling wordt verzonden. Opties: <br/>**`Authorization`**- Goedkeuring van de aankoop, maar blokkeert de middelen. De hoeveelheid wordt pas opgevraagd wanneer deze door de handelaar wordt &quot;gevangen&quot;.<br/>**`Sale`** - Het bedrag van de aankoop wordt toegestaan en onmiddellijk van de rekening van de klant teruggetrokken. |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Website | Bepaalt welke creditcards beschikbaar zijn voor klanten tijdens het afrekenen. Selecteer elke ondersteunde kaart. Opties: `American Express` (hiervoor is een extra overeenkomst vereist) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![Geavanceerde instellingen](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| Weergeven bij winkelwagentje | Winkelweergave | Hiermee wordt bepaald of PayPal Express Checkout wordt weergegeven als een betalingsoptie in het winkelwagentje. Opties: Ja (aanbevolen) / Nee |
| [!UICONTROL Payment Action Applicable From] | Website | Hiermee bepaalt u het bereik van de toepasselijke landselectie. Opties: alle toegestane landen / specifieke landen |
| [!UICONTROL Countries Payment Applicable From] | Website | Identificeert elk land van waaruit betaling wordt geaccepteerd. Alleen klanten met een factuuradres in een geselecteerd land kunnen aankopen doen met deze betalingsmethode. |
| [!UICONTROL Debug Mode] | Website | Hiermee worden berichten die tussen je winkel en het PayPal-betalingssysteem zijn verzonden, in een logbestand vastgelegd. Opties: `Yes` / `No` <br/><br/>**_Opmerking:_**Het logbestand wordt opgeslagen op de server en is alleen toegankelijk voor ontwikkelaars. In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier. |
| [!UICONTROL Enable SSL Verification] | Website | Schakelt verificatie van het beveiligingscertificaat van de host in. Opties: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Geeft een volledig overzicht weer van de lijstitems van het winkelwagentje van de klant op de Paypal-site. Opties: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Website | Hiermee bepaalt u of klanten de transactie kunnen voltooien vanaf de PayPal-site of dat ze naar uw winkel moeten terugkeren en de stap Bestelrevisie moeten voltooien voordat ze de bestelling verzenden. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
