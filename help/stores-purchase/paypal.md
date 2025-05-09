---
title: PayPal-betalingsoplossingen
description: Meer informatie over de integratie van de PayPal-betalingsoplossing die beschikbaar is voor je winkel.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# PayPal-betalingsoplossingen

PayPal is een wereldwijde marktleider op het gebied van online betalingen en een snelle en veilige manier voor uw klanten om online te betalen. De keuze van beschikbare PayPal-oplossingen varieert per bedrijfslocatie. PayPal Express Checkout en PayPal Payments Standard kunnen overal ter wereld worden gebruikt. Meer leren, zie [ oplossingen PayPal door land ](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2 Vereisten:** <br/>
>Vanaf 14 september 2019, kunnen Europese banken betalingen dalen die niet aan [ PSD2 ](../getting-started/compliance-payment-services-directive.md) vereisten voldoen. Voor de meeste PayPal-oplossingen is geen actie vereist om aan PSD2 te voldoen, omdat deze vereisten door PayPal worden afgehandeld.

## PayPal-zakelijke account

Om PayPal als betalingsmethode in uw opslag aan te bieden, moet u een PayPal [ bedrijfsrekening ][1] en/of a [ PayPal rekening van de Betalingsstroom hebben ][2]. De accountvereisten worden opgegeven in de beschrijving van elke PayPal-oplossing. Uw PayPal handelsrekening wordt ook gebruikt om het even welke [ fraudefilters ](#paypal-fraud-management-filters) te beheren die op aankopen worden toegepast die van uw opslag worden gemaakt.

Klanten die PayPal Express Checkout of Express Checkout gebruiken voor Payflow Pro, moeten een PayPal-kopersaccount hebben. De Betalingsstandaard van PayPal (de Norm van de Betalingen van de Website in sommige landen) kan direct of door een kopersrekening worden gebruikt wanneer dat de handelaar _Facultatieve Rekening van PayPal_ toelaat. Deze parameter is standaard ingeschakeld, zodat klanten hun creditcardgegevens kunnen invoeren of een kopersaccount kunnen maken met PayPal. Als deze optie is uitgeschakeld, moeten klanten eerst een PayPal-kopersaccount maken voordat ze een aankoop doen.

Voor Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway en Payflow Link moeten klanten creditcardgegevens invoeren tijdens het afrekenen.

## PayPal-creditering en PayPalLater

PayPal PayPal biedt uw klanten snel toegang tot financiering, zodat ze nu kunnen kopen en op tijd kunnen betalen, zonder extra kosten voor u. Er wordt geen bedrag in rekening gebracht wanneer klanten PayPal-kredietopties kiezen en alleen de normale PayPal-transactiekosten betalen. Meer leren, zie de [ website PayPal ][3].

Geef je verkoop een boost wanneer je adverteert met financiering. Met PayPal kun je browsers omzetten in kopers met financiering via PayPal PayPal Later. Uw klanten kunnen in de loop der tijd betalen, terwijl u vooraf betaald wordt, zonder extra kosten voor u. Gebruik gratis PayPal-banneradvertenties om PayPal-financiering als betalingsoptie te adverteren wanneer uw klanten zich afmelden met PayPal. Het is aangetoond dat het PayPal Advertising-programma extra aankopen genereert en de gemiddelde aankoopgrootte met 15% of meer verhoogt.

U kunt vrije, kant-en-klare banneradvertenties aan pagina&#39;s van uw plaats en de _Krediet van PayPal_ knoop aan uw winkelwagentje tijdens controle gemakkelijk toevoegen om uw klanten eraan te herinneren dat de financiering gemakkelijk beschikbaar is.

>[!NOTE]
>
>Vanaf de release 2.4.3 wordt PayPal PayLater ondersteund in implementaties die PayPal bevatten. Met deze functie kunnen kopers een bestelling in tweewekelijkse termijnen betalen in plaats van het volledige bedrag op het moment van aankoop te betalen. De PayPal-ervaring is afgekeurd.

Voor de handelaren van de V.S., wordt het Krediet van PayPal toegelaten door gebrek voor de [&#128279;](paypal-express-checkout.md) betalingsoptie van de Uitdrukkelijke Afhandeling van PayPal . Om het voor deze betalingsmethode onbruikbaar te maken, zie de _sectie van Eigenschappen_ van [ Uitdrukkelijke configuratie van de Controle van PayPal ](paypal-express-checkout.md#features).

PayPal-krediet is standaard uitgeschakeld voor de andere PayPal-betalingsoplossingen, maar kan in de configuratie van de betalingsmethode worden ingeschakeld voor ondersteunende oplossingen:

- [Betalingen geavanceerd](paypal-payments-advanced.md)
- [Betalingen Pro](paypal-payments-pro.md)
- [Betalingsstandaard](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Payflow-koppeling](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Voordat u PayPal-creditering of PayPal PayPal PayPal Later configureert voor uw winkel, moet u controleren of dit is ingeschakeld in uw PayPal-handelsaccount.

## Geïntegreerde PayPal-oplossingen

Met PayPal en Adobe Commerce kun je betalingen accepteren van alle grote incasso- en creditcards. PayPal biedt extra gebruiksgemak, omdat zelfs uw klanten die geen PayPal-rekening hebben voor hun aankopen met PayPal kunnen betalen.

>[!NOTE]
>
>Je kunt niet meer dan één PayPal-methode tegelijk in je winkel laten gebruiken, behalve voor PayPal Express Checkout. PayPal Express Checkout kan worden gebruikt met andere PayPal-betalingsmethoden, behalve PayPal Payments Standard. Als u betalingsoplossingen wijzigt, is de vorige methode uitgeschakeld.

### PayPal Express-afhandeling

[PayPal Express-afhandeling](paypal-express-checkout.md)

### PayPal All-in-One betalingsoplossingen

In de Verenigde Staten biedt PayPal de volgende PCI-compatibele oplossingen om aan de behoeften van uw groeiende bedrijf te voldoen.

- [PayPal-betalingen geavanceerd](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

![ PayPal alle-in-één betalingsoplossingen ](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### PayPal-betalingsgateways

Een betaalgateway is een commerciële dienst die wordt verleend door een dienstverlener die e-commerce toepassingen verleent die creditcard of verwerking van directe betalingen toestaat. Zij werken als tussenpersonen tussen klanten en banken.

Betalingsgateways zijn beschikbaar in online- en offline-omgevingen. Betalingen kunnen worden geaccepteerd via de telefoon, online of via een mobiele app. De transactie wordt naar het verwerkingssysteem van de dienstverlener verzonden en vervolgens ter verificatie en bevestiging naar de bank van de klant gestuurd. Indien geverifieerd, ontvangt de handelaar de betaling zonder rechtstreeks contact te hebben met de bankrekening van de klant.

Er zijn twee soorten betalingsgateways-direct en ontvangen.

- Met Direct betaalgateways kunnen gebruikers hun kaartgegevens invoeren op de website van de winkel.
- Gehoste betaalgateways leiden gebruikers om naar een gehoste betalingspagina, buiten de website van de winkel.

De betaalgateway biedt beveiliging en bescherming voor alle partijen die bij een transactie betrokken zijn.

PayPal biedt een keuze uit twee betaalgatewayoplossingen voor uw bedrijf. U kunt PayPal als host voor uw afhandeling kiezen op de beveiligde betalingssite of u kunt de volledige betalingservaring beheren met een aanpasbare oplossing.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow Link](paypal-payflow-link.md)

![ de betaalgateways van de Opstelling PayPal ](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## Paypal-filters voor fraudebeheer

Met PayPal-filters voor fraudebeheer is het gemakkelijker om frauduleuze transacties op te sporen en erop te reageren. Deze filters kunnen worden geconfigureerd om risicovollere betalingen te markeren, te bewaren voor controle of te weigeren. De acties met betrekking tot de status van de Commerce [ orde ](order-status.md) waarden veranderden volgens de montages van de fraudefilter:

| Handeling | Resultaat |
| --- | --- |
| [!UICONTROL Review] | De verdachte orde ontvangt de status _Controle van de Betaling_ wanneer de orde wordt geplaatst. U kunt de bestelling bekijken en goedkeuren of de betaling annuleren in de beheerfunctie of op de PayPal-zijde. Wanneer u op **[!UICONTROL Accept Payment]** of **[!UICONTROL Deny Payment]** klikt, worden er geen nieuwe transacties voor de volgorde gemaakt. <br/><br/> als u de status van de transactie op de plaats PayPal verandert, moet u **[!UICONTROL Get Payment Update]** in de pagina van de Orde van Admin klikken om de veranderingen toe te passen. Als u op **[!UICONTROL Accept Payment]** of **[!UICONTROL Deny Payment]** klikt, worden de wijzigingen toegepast die op de Paypal-site zijn aangebracht. |
| [!UICONTROL Deny] | De verdachte bestelling kan niet door de klant worden geplaatst, omdat de bijbehorende transactie door PayPal wordt geweigerd. <br/><br/> om de betaling van Admin te ontkennen, klik **[!UICONTROL Deny Payment]** in de hoger-juiste hoek van de pagina. De orderstatus verandert in `Canceled` , de transactie wordt teruggedraaid en er worden middelen vrijgemaakt op de klantenaccount. De bijbehorende informatie wordt toegevoegd in de sectie _[!UICONTROL Comments History]_&#x200B;van de ordeweergave. |
| [!UICONTROL Flag] | De vermoedelijke volgorde krijgt de status `Processing` wanneer deze wordt geplaatst. De corresponderende transactie wordt gemarkeerd met een vlag in de lijst van handelstransacties. |

{style="table-layout:auto"}

## PayPal-oplossingen per land

| Land | PayPal-betalingsoplossing |
|--- |--- |
| Australië | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Canada | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inclusief Express Checkout) <br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Frankrijk | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Duitsland | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Hongkong SAR China | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italië | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japan | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Nieuw-Zeeland | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Spanje | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Verenigd Koninkrijk | [!DNL PayPal Payments Pro Hosted Solution] (inclusief Express Checkout) <br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Verenigde Staten | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (omvat Uitdrukkelijke Controle) <br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (omvat Uitdrukkelijke Controle) <br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (omvat Uitdrukkelijke Controle) <br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (omvat Uitdrukkelijke Controle) <br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### Overige landen

PayPal Express Checkout en PayPal Website Payments Standard zijn beschikbaar in de volgende landen:

- Argentinië
- Oostenrijk
- België
- Brazilië
- Bulgarije
- Chili
- Costa Rica
- Cyprus
- Tsjechië
- Denemarken
- Dominicaanse Republiek
- Ecuador
- Estland
- Finland
- Frans-Guyana
- Gibraltar
- Griekenland
- Guadeloupe
- Hongarije
- IJsland
- India
- Indonesië
- Ierland
- Israël
- Jamaica
- Letland
- Liechtenstein
- Litouwen
- Luxemburg
- Maleisië
- Malta
- Martinique
- Mexico
- Nederland
- Noorwegen
- Filipijnen
- Polen
- Portugal
- Réunion
- Roemenië
- San Marino
- Singapore
- Slowakije
- Slovenië
- Zuid-Afrika
- Zuid-Korea
- Zweden
- Zwitserland
- Taiwan
- Thailand
- Turkije
- Verenigde Arabische Emiraten
- Uruguay
- Venezuela
- Vietnam


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
