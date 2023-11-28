---
title: Naleving van Cookie-recht
description: Om gelijke tred te houden met de wetgeving in veel landen inzake het gebruik van cookies, bieden Adobe Commerce en Magento Open Source handelaren een keuze aan methoden om toestemming van klanten te verkrijgen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Naleving van Cookie-recht

Cookies zijn kleine bestanden die worden opgeslagen op de computer van elke bezoeker van uw site en die worden gebruikt als tijdelijke opslagplaatsen ter informatie. Informatie die in cookies wordt opgeslagen, wordt gebruikt om de winkelervaring te personaliseren, bezoekers te koppelen aan hun winkelwagentjes, verkeerspatronen te meten en de doeltreffendheid van promoties te verbeteren. Om gelijke tred te houden met de wetgeving in veel landen inzake het gebruik van cookies, bieden Adobe Commerce en Magento Open Source handelaren een keuze aan methoden om toestemming van klanten te verkrijgen. Voor een lijst met de standaardcookies in Adobe Commerce en Magento Open Source, [Referentie cookie](#default-cookies).

>[!NOTE]
>
>Als u de standaardinstelling wijzigt [Google-privacyinstellingen](../merchandising-promotions/google-tools.md#google-privacy-settings) om aan de [Algemene verordening inzake gegevensbescherming](compliance-gdpr.md), is het niet nodig toestemming van de gebruiker te verkrijgen voor het gebruik van cookies van Googles Analytics.

## Methode 1: Impliciete toestemming

Impliciete toestemming houdt in dat bezoekers van uw winkel duidelijk begrijpen dat cookies een noodzakelijk onderdeel van de activiteiten zijn en door uw site te gebruiken indirect toestemming hebben gegeven om ze te gebruiken. De sleutel tot het verkrijgen van impliciete toestemming is het verstrekken van voldoende informatie voor een bezoeker om een geïnformeerde beslissing te nemen. Veel winkels geven boven aan alle standaardpagina&#39;s een bericht weer met een kort overzicht van het gebruik van cookies, met een koppeling naar het privacybeleid van de winkel. Het privacybeleid moet het type informatie beschrijven dat uw winkel verzamelt en hoe deze wordt gebruikt.

## Methode 2: Uitdrukkelijke toestemming

Uw winkel gebruiken in _cookie-beperkingsmodus_ bezoekers moeten hun toestemming geven voordat cookies op hun computer kunnen worden opgeslagen. Veel functies van je winkel zijn niet beschikbaar, tenzij er toestemming is verleend. Als er bijvoorbeeld Googles Analytics beschikbaar zijn voor uw winkel, kan deze alleen worden aangeroepen nadat de bezoeker toestemming heeft gegeven cookies te gebruiken.

## Modus Koekjesbeperking

Wanneer de beperkingsmodus voor cookies is ingeschakeld, krijgen bezoekers van de winkel een melding dat cookies vereist zijn voor bewerkingen met alle functies. Afhankelijk van uw thema kan het bericht boven de koptekst, onder de voettekst of ergens anders op de pagina worden weergegeven. Het bericht verwijst naar uw privacybeleid voor meer informatie en moedigt bezoekers aan op de knop Toestaan te klikken om toestemming te verlenen. Nadat de toestemming wordt verleend, verdwijnt het bericht.

Uw [privacybeleid](privacy-policy.md)) moet de naam van uw winkel en contactgegevens bevatten en het doel van elke cookie die door uw winkel wordt gebruikt, toelichten. Zie voor meer informatie [Referentie cookie](#default-cookies).

>[!NOTE]
>
>Als u de URL-sleutel van het privacybeleid wijzigt, moet u ook een aangepaste URL maken om het verkeer om te leiden naar de nieuwe URL-sleutel. Anders, keert de verbinding in het bericht van de Wijze van de Beperking van het Koken terug `404 Page Not Found`.

![Voorbeeld van storefront - kennisgeving van cookie-beperking](./assets/storefront-cookie-restriction-message.png){width="600"}

### Stap 1: de beperkingsmodus voor cookies inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkernavigatievenster onder **[!UICONTROL General]**, kiest u **[!UICONTROL Web]**.

1. Breid uit **[!UICONTROL Default Cookie Settings]** en voer de volgende handelingen uit:

   ![Webconfiguratie - standaardinstellingen voor cookies](./assets/web-default-cookie-settings.png){width="600"}

   - Voer de **[!UICONTROL Cookie Lifetime]** in seconden.

   - Als u cookies beschikbaar wilt maken voor andere mappen, voert u de **[!UICONTROL Cookie Path]**. Als u de cookies overal op de site beschikbaar wilt maken, voert u een slash in (`/`). Deze waarde kan alleen het cookiepad bevatten, en **_kan_** bevat andere cookieparameters.

   - Als u de cookies beschikbaar wilt maken voor een subdomein, voert u de subdomeinnaam in het dialoogvenster **[!UICONTROL Cookie Domain]** field (`subdomain.yourdomain.com`). Als u cookies beschikbaar wilt maken voor alle subdomeinen, voert u de domeinnaam in die wordt voorafgegaan door een punt (`.yourdomain.com`). Deze waarde kan alleen het cookiedomein bevatten, en **_kan_** bevat andere cookieparameters.

   - Als u wilt voorkomen dat scripttalen, zoals JavaScript, toegang krijgen tot cookies, controleert u of **Alleen HTTP gebruiken** is ingesteld op `Yes`.

   - Set **[!UICONTROL Cookie Restriction Mode]** tot `Yes`.

     Wis indien nodig het selectievakje en klik op **[!UICONTROL OK]** om werkingsgebiedomschakeling te bevestigen.

1. Klik op **[!UICONTROL Save Config]**.

1. Klik op de knop **[!UICONTROL Cache Management]** koppeling in het systeembericht. Vernieuw vervolgens elke ongeldige cache.

### Stap 2: Je privacybeleid bijwerken

Werk uw [privacybeleid](privacy-policy.md) zodat het de informatie weerspiegelt die uw bedrijf verzamelt en hoe het wordt gebruikt.

## Standaardcookies

De standaardcookies in Adobe Commerce en Magento Open Source worden ingedeeld als Vrijgesteld/Niet-Vrijgesteld om handelaren te helpen voldoen aan de vereisten van privacyregels zoals de [GDPR](compliance-gdpr.md). Handelaren dienen deze informatie als leidraad te gebruiken en juridische adviseurs te raadplegen om hun privacy- en cookiebeleid bij te werken als onderdeel van een uitgebreide nalevingsstrategie voor privacyregelgeving.

De volgende cookies worden gebruikt door [!DNL Commerce] &quot;out of the box&quot; voor installaties in de bedrijfsruimte en in de cloud. Deze cookies zijn mogelijk vereist door functionaliteit die expliciet wordt aangevraagd door de klant. Voor meer informatie over de levensduur van sessiecookies raadpleegt u [Sessielevensduur](../customers/customer-online-options.md).

Sommige van deze cookies kunnen configuratieopties bieden, waaronder, indien nodig, in-/uitschakelen.

### Cookies met aangevraagde functionaliteit (vrijgesteld)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Wordt gebruikt door Google-tagbeheer. Hiermee legt u de SKU van het product vast, de naam, de prijs en de hoeveelheid die uit het winkelwagentje zijn verwijderd, en maakt u de informatie beschikbaar voor toekomstige integratie door scripts van derden.

#### `guest-view`

Hiermee slaat u de bestellings-id op die bezoekers gebruiken om de status van hun bestelling op te halen. Weergave Gastbestellingen. Gebruikt in _[!DNL Orders and Returns]_widgets.

- Is veilig? Nee
- Alleen HTTP: Ja
- Vervalbeleid: sessie
- Module: `Magento_Sales`

#### `login_redirect`

Behoudt de bestemmingspagina die alvorens de klant aan login werd geleid laadde. Een login wordt omleiding gebruikt met de minikaart voor aangemelde klanten als [Min. winkelwagentje weergeven](../stores-purchase/cart-configuration.md#mini-cart) configuratieoptie is ingesteld op `Yes`.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: sessie
- Module: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Hiermee slaat u bannerinhoud lokaal op om de prestaties te verbeteren.

#### `mage-messages`

Tracks foutberichten en andere meldingen die aan de gebruiker worden getoond, zoals het bevestigingsbericht van het cookie en diverse foutberichten. Het bericht wordt verwijderd uit het cookie nadat het aan de gebruiker is getoond.

Er is geen optie om deze cookie uit te schakelen.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: duur 1 jaar. Vooraan verschoven wanneer het bericht aan de gebruiker wordt getoond.
- Module: `Magento_Theme`

#### `mage-translation-storage` (lokale opslag)

Vertaalde inhoud wordt opgeslagen op verzoek van de winkelier. Wordt gebruikt wanneer [Vertaalstrategie](../configuration-reference/advanced/developer.md) wordt gevormd als &quot;Woordenboek (Vertaling aan de kant van Storefront)&quot;.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Translation`

#### `mage-translation-file-version` (lokale opslag)

Tracks the version of translations in local storage. Wordt gebruikt wanneer [Vertaalstrategie](../configuration-reference/advanced/developer.md) is geconfigureerd als `Dictionary (Translation on Storefront side)`.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Translation`

#### `product_data_storage` (lokale opslag)

Hiermee slaat u de configuratie op voor productgegevens die betrekking hebben op onlangs bekeken/vergeleken producten.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Catalog`

#### `recently_compared_product` (lokale opslag)

Hiermee slaat u product-id&#39;s op van producten die onlangs zijn vergeleken.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Catalog`

#### `recently_compared_product_previous` (lokale opslag)

Hiermee slaat u product-id&#39;s van eerder vergeleken producten op voor eenvoudige navigatie.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Catalog`

#### `recently_viewed_product` (lokale opslag)

Hiermee slaat u product-id&#39;s van onlangs bekeken producten op voor eenvoudige navigatie.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Catalog`

#### `recently_viewed_product_previous` (lokale opslag)

Hiermee slaat u product-id&#39;s van onlangs bekeken producten op voor eenvoudige navigatie.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Gebruikt door [Google-tagbeheer](../merchandising-promotions/google-tag-manager.md). Hiermee legt u de SKU, naam, prijs en hoeveelheid van het product vast die aan het winkelwagentje is toegevoegd, en stelt u de informatie beschikbaar voor toekomstige integratie door scripts van derden.

#### `stf`

Registreert de tijdberichten worden verzonden door SendFriend ([Een vriend e-mailen](../stores-purchase/email-a-friend.md)).

- Is veilig? Ja
- Alleen HTTP: Ja
- Vervalbeleid: sessie
- Module: `Magento_SendFriend`

#### `X-Magento-Vary`

Configuratie die de prestaties verbetert wanneer het gebruiken van Statische inhoud het in cache plaatsen van Varnish.

- Is veilig? Ja
- Alleen HTTP: Ja
- Vervalbeleid: gebaseerd op PHP setting session.cookie_life
- Module: `Magento_PageCache`

#### `form_key`

Een beveiligingsmaatregel die een willekeurige tekenreeks toevoegt aan alle formulierverzendingen om de gegevens te beschermen tegen de zogeheten Cross-Site Request-vervalsing (CSRF).

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid:
   - PHP: Gebaseerd op PHP setting session.cookie_life
   - JS: sessie
- Module: Paginacache

#### `mage-cache-sessid`

De waarde van dit cookie zorgt voor het opschonen van de lokale cacheopslag. Wanneer de cookie wordt verwijderd door de back-endtoepassing, schoont Admin de lokale opslag op en stelt de cookie-waarde in op `true`.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: sessie
- Module: `Magento_Customer`

#### `mage-cache-storage`

Lokale opslag van bezoekersspecifieke inhoud die functies voor e-commerce inschakelt.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: sessie
- Module: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (lokale opslag)

Lokale opslag van bezoekersspecifieke inhoud die functies voor e-commerce inschakelt.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: sessie
- Module: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (lokale opslag)

Hiermee wordt lokale opslag van specifieke inhoudsgedeelten geforceerd die ongeldig moeten worden gemaakt.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: per lokale opslag
- Module: `Magento_Customer`

#### `persistent_shopping_cart`

Hiermee slaat u de sleutel (ID) van een blijvende winkelwagen op om het mogelijk te maken de winkelwagen te herstellen voor een anonieme winkelier.

- Is veilig? Ja
- Alleen HTTP: Ja
- Vervalbeleid: gebaseerd op [Blijvende winkelwagentje](../stores-purchase/cart-persistent.md) - Configuratie van levensonderhoud (seconden)
- Module: `Magento_Persistent`

#### `private_content_version`

Voegt een willekeurig, uniek aantal en tijd aan pagina&#39;s met klanteninhoud toe om hen te verhinderen in het voorgeheugen ondergebracht op de server worden.

Deze wordt op meerdere plaatsen ingesteld: in PHP, in JavaScript als een cookie en in JavaScript op lokale opslag.

Alleen voor HTTP=`Yes` (gebaseerd op verzoek) betekent dit dat de cookie beveiligd is als deze tijdens een HTTPS-aanvraag wordt ingesteld en onveilig als deze tijdens een HTTP-aanvraag wordt ingesteld.

- Is veilig? `Yes` (op verzoek), `No`
- Alleen HTTP: `No`
- Vervalbeleid: gebaseerd op [Blijvende winkelwagentje](../stores-purchase/cart-persistent.md) - Configuratie van levensonderhoud (seconden)
   - PHP: `1` jaar / `315360000s` (tien jaar)
   - JS: `1` dag
   - JS lokale opslag: volgens lokale opslagregels (altijd)
- Module: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Hiermee slaat u klantspecifieke informatie op over acties die door winkels worden geïnitieerd, zoals weergave van wensenlijsten en afhandelingsgegevens.

- Is veilig? `No`
- Alleen HTTP: `No`
- Vervalbeleid: `Session`
- Module: `Magento_Customer`

#### `store`

Volgt de specifieke winkelweergave/-landinstelling die door de winkelier is geselecteerd.

- Is veilig? `No`
- Alleen HTTP: `Yes`
- Vervalbeleid: `1` jaar
- Module: `Magento_Store`

#### `mage-banners-cache-storage` - lokale opslag

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Lokale opslag voor de Bannerfunctionaliteit.

- Is veilig? `No`
- Alleen HTTP: `No`
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Banner`

## Cookies Googles Analytics

De volgende cookies worden gebruikt wanneer [Googles Analytics](../merchandising-promotions/google-analytics.md) of Google Universal Analytics is volledig ingeschakeld voor uw installatie. Als u deze cookies wilt uitschakelen zodat de privacyregels worden nageleefd, raadpleegt u [Google Privacy-instellingen](../merchandising-promotions/google-tools.md#google-privacy-settings). Zie voor meer informatie [Gebruik van Googles Analytics cookie op websites][1].

### Google Universal Analytics cookies - niet vrijgesteld

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) JavaScript-bibliotheken: `gtag.js` en `analytics.js`

- `_ga`: Hiermee verdeelt u bezoekers van uw site.
- `_gid`: Hiermee verdeelt u bezoekers van uw site.
- `gat`: Wordt gebruikt om de aanvraagsnelheid te vertragen.
- `dc_gtm_<property-id>`: Het verzoektarief van Throttles wanneer de Googles Analytics met worden opgesteld [Google-tagbeheer](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: Bevat een token dat kan worden gebruikt om een client-id op te halen van de AMP Client ID-service. Andere mogelijke waarden zijn opt-out, inflight-aanvraag of een fout bij het ophalen van een client-id van de AMP Client ID-service.
- `_gac_<property-id>`: Bevat informatie over de campagne voor de gebruiker. Google AdWords-conversietags lezen dit cookie als Googles Analytics zijn gekoppeld aan uw [AdWords][2] account.

### Cookies van Googles Analytics - niet-vrijgesteld

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) JavaScript-bibliotheek: `ga.js`

- `__utma`: Hiermee maakt u onderscheid tussen winkels en sessies. Dit cookie wordt gemaakt wanneer de JavaScript-bibliotheek wordt uitgevoerd en er geen bestaand cookie is. `__utma` cookie. Het cookie wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.
- `__utmt`: Wordt gebruikt om de aanvraagsnelheid te vertragen.
- `__utmb`: Bepaalt nieuwe sessies/bezoeken. Dit cookie wordt gemaakt wanneer de JavaScript-bibliotheek wordt uitgevoerd en er geen bestaand cookie is. `__utmb` cookie. Het cookie wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.
- `_utmz`: Hiermee slaat u de verkeersbron of campagne op waarin wordt uitgelegd hoe de gebruiker uw site heeft bereikt. Het cookie wordt gemaakt wanneer de JavaScript-bibliotheek wordt uitgevoerd en wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.
- `__utmv`: Hiermee slaat u aangepaste variabele gegevens op bezoekersniveau op. Deze cookie wordt gemaakt wanneer een ontwikkelaar de functie `_setCustomVar` methode met een aangepaste variabele op bezoekersniveau. Dit cookie wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.

## Product Recommendations cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) De volgende cookies worden door Product Recommendations gebruikt voor klanten van Adobe Commerce. Deze cookies worden geïnstalleerd met de [De module DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: Hiermee kunt u [Adobe Commerce-gegevensverzameling beperken](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) als u aangepaste code hebt voor het beheer van cookie-toestemming op uw site.
- `user_allowed_save_cookie`: Gebruikt voor [cookie-beperkingsmodus](#cookie-restriction-mode).
- `authentication_flag`: Geeft aan of een winkelier zich heeft aangemeld of zich heeft afgemeld. Deze cookie wordt tegelijk bijgewerkt met de `dataservices_customer_id` cookie.
- `dataservices_customer_id`: Geeft aan of een winkelier zich heeft aangemeld of zich heeft afgemeld. Dit cookie bevat de unieke id van de klant in het systeem.
- `dataservices_customer_group`: Geeft de groep van een klant aan. Deze cookie wordt opgeslagen als [sha1](https://en.wikipedia.org/wiki/SHA-1) controlesom van de groep-id van de klant.
- `dataservices_cart_id`: Identificeert de winkelwagentacties. Dit cookie bevat de unieke kaart-id van de klant in het systeem.
- `dataservices_product_context`: Identificeert de productinteracties van een klant. Dit cookie bevat de unieke aanhalings-id van de klant in het systeem.

## Aanvullende cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) De volgende cookies worden ingesteld voor Adobe Commerce-klanten. Deze cookies worden geïnstalleerd met de [De module DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: Ingesteld door JavaScript-tracker Snowplow. Meer informatie vindt u in de [Documentatie over gloed](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: Op basis van de hostnaam van de huidige webpagina is dit het bovenste domein dat geen &quot;openbaar achtervoegsel&quot; is zoals beschreven in https://publicsuffix.org. In principe is dit het bovenste domein dat cookies kan accepteren. Deze cookie maakt deel uit van de [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
