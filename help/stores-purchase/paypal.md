---
title: PayPal-betalingsoplossingen
description: Meer informatie over de integratie van de PayPal-betalingsoplossing die beschikbaar is voor je winkel.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# PayPal-betalingsoplossingen

PayPal is een wereldwijde marktleider op het gebied van online betalingen en een snelle en veilige manier voor uw klanten om online te betalen. De keuze van beschikbare PayPal-oplossingen varieert per bedrijfslocatie. PayPal Express Checkout en PayPal Payments Standard kunnen overal ter wereld worden gebruikt. Zie voor meer informatie [PayPal-oplossingen per land](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2 Eisen:** <br/>
>Vanaf 14 september 2019 kunnen Europese banken betalingen afbouwen die niet voldoen [PSD 2](../getting-started/compliance-payment-services-directive.md) eisen. Voor de meeste PayPal-oplossingen is geen actie vereist om aan PSD2 te voldoen, omdat deze vereisten door PayPal worden afgehandeld.

## PayPal-zakelijke account

Als je PayPal als betalingsmethode in je winkel wilt aanbieden, moet je een PayPal-rekening hebben [zakelijke account][1] of een [PayPal Payflow-rekening][2]. De accountvereisten worden opgegeven in de beschrijving van elke PayPal-oplossing. Je PayPal Merchant-account wordt ook gebruikt voor het beheren van [fraudefilters](#paypal-fraud-management-filters) die worden toegepast op aankopen die worden gedaan in je winkel.

Klanten die PayPal Express Checkout of Express Checkout gebruiken voor Payflow Pro, moeten een PayPal-kopersaccount hebben. PayPal Payments Standard (in sommige landen de betalingsstandaard van de website) kan rechtstreeks of via een kopersaccount worden gebruikt wanneer de handelaar _PayPal-account optioneel_. Deze parameter is standaard ingeschakeld, zodat klanten hun creditcardgegevens kunnen invoeren of een kopersaccount kunnen maken met PayPal. Als deze optie is uitgeschakeld, moeten klanten eerst een PayPal-kopersaccount maken voordat ze een aankoop doen.

Voor Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway en Payflow Link moeten klanten creditcardgegevens invoeren tijdens het afrekenen.

## PayPal-creditering en PayPalLater

PayPal PayPal biedt uw klanten snel toegang tot financiering, zodat ze nu kunnen kopen en op tijd kunnen betalen, zonder extra kosten voor u. Er wordt geen bedrag in rekening gebracht wanneer klanten PayPal-kredietopties kiezen en alleen de normale PayPal-transactiekosten betalen. Zie voor meer informatie de [PayPal-website][3].

Geef je verkoop een boost wanneer je adverteert met financiering. Met PayPal kun je browsers omzetten in kopers met financiering via PayPal PayPal Later. Uw klanten kunnen in de loop der tijd betalen, terwijl u vooraf betaald wordt, zonder extra kosten voor u. Gebruik gratis PayPal-banneradvertenties om PayPal-financiering als betalingsoptie te adverteren wanneer uw klanten zich afmelden met PayPal. Het PayPal-advertentieprogramma heeft extra aankopen laten genereren en de gemiddelde aankoopgrootte met 15% of meer doen toenemen.

U kunt eenvoudig gratis, kant-en-klare banneradvertenties toevoegen aan pagina&#39;s van uw site en de _PayPal-creditering_ op uw winkelwagentje tijdens de afhandeling om uw klanten eraan te herinneren dat financiering direct beschikbaar is.

>[!NOTE]
>
>Vanaf de release 2.4.3 wordt PayPal PayLater ondersteund in implementaties die PayPal bevatten. Met deze functie kunnen kopers een bestelling in tweewekelijkse termijnen betalen in plaats van het volledige bedrag op het moment van aankoop te betalen. De PayPal-ervaring is afgekeurd.

Voor Amerikaanse handelaren is PayPal-krediet standaard ingeschakeld voor de [PayPal Express-afhandeling](paypal-express-checkout.md) betalingsoptie. Als u deze voor deze betalingsmethode wilt uitschakelen, raadpleegt u de _Functies_ deel van [PayPal Express-betalingsconfiguratie](paypal-express-checkout.md#features).

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

![PayPal alles-in-één betalingsoplossingen](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

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

![PayPal-betaalgateways instellen](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## Paypal-filters voor fraudebeheer

Met PayPal-filters voor fraudebeheer is het gemakkelijker om frauduleuze transacties op te sporen en erop te reageren. Deze filters kunnen worden geconfigureerd om risicovollere betalingen te markeren, te bewaren voor controle of te weigeren. Handelingen in verband met de handel [orderstatus](order-status.md) de waarden worden gewijzigd op basis van de instellingen van het fraudefilter:

| Handeling | Resultaat |
| --- | --- |
| [!UICONTROL Review] | De verdachte opdracht krijgt de status _Betaalcontrole_ wanneer de volgorde is geplaatst. U kunt de bestelling bekijken en goedkeuren of de betaling annuleren in de beheerfunctie of op de PayPal-zijde. Wanneer u op **[!UICONTROL Accept Payment]** of **[!UICONTROL Deny Payment]** Er worden geen nieuwe transacties voor de bestelling gemaakt. <br/><br/>Als u de status van de transactie op de PayPal-site wijzigt, moet u klikken op **[!UICONTROL Get Payment Update]** op de pagina Volgorde van de beheerder om de wijzigingen toe te passen. Als u op **[!UICONTROL Accept Payment]** of **[!UICONTROL Deny Payment]**, worden de wijzigingen toegepast die op de Paypal-site zijn aangebracht. |
| [!UICONTROL Deny] | De verdachte bestelling kan niet door de klant worden geplaatst, omdat de bijbehorende transactie door PayPal wordt geweigerd. <br/><br/>Als u de betaling van de beheerder wilt weigeren, klikt u op **[!UICONTROL Deny Payment]** rechtsboven op de pagina. De orderstatus verandert in `Canceled`, wordt de transactie teruggedraaid en worden middelen op de klantenrekening vrijgegeven. De bijbehorende informatie wordt toegevoegd in het gedeelte _[!UICONTROL Comments History]_van de ordeweergave. |
| [!UICONTROL Flag] | De verdachte bestelling krijgt de status `Processing` wanneer het wordt geplaatst. De corresponderende transactie wordt gemarkeerd met een vlag in de lijst van handelstransacties. |

{style="table-layout:auto"}

## PayPal-oplossingen per land

| Land | PayPal-betalingsoplossing |
|--- |--- |
| Australië | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Canada | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inclusief Express Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Frankrijk | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Duitsland | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Hongkong SAR China | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italië | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japan | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Nieuw-Zeeland | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Spanje | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Verenigd Koninkrijk | [!DNL PayPal Payments Pro Hosted Solution] (inclusief Express Checkout)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Verenigde Staten | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (inclusief Express Checkout)<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (inclusief Express Checkout)<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (inclusief Express Checkout)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inclusief Express Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

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
