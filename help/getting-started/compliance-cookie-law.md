---
title: Naleving van Cookie-recht
description: Om gelijke tred te houden met de wetgeving in veel landen inzake het gebruik van cookies, bieden Adobe Commerce en Magento Open Source handelaren een keuze aan methoden om toestemming van klanten te verkrijgen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Naleving van Cookie-recht

Cookies zijn kleine bestanden die worden opgeslagen op de computer van elke bezoeker van uw site en die worden gebruikt als tijdelijke opslagplaatsen ter informatie. Informatie die in cookies wordt opgeslagen, wordt gebruikt om de winkelervaring te personaliseren, bezoekers te koppelen aan hun winkelwagentjes, verkeerspatronen te meten en de doeltreffendheid van promoties te verbeteren. Om gelijke tred te houden met de wetgeving in veel landen inzake het gebruik van cookies, bieden Adobe Commerce en Magento Open Source handelaren een keuze aan methoden om toestemming van klanten te verkrijgen. Voor een lijst van de standaardkoekjes in Adobe Commerce en Magento Open Source, de [ Verwijzing van het Koekje ](#default-cookies).

>[!NOTE]
>
>Als u het gebrek [ de privacymontages van Google ](../merchandising-promotions/google-tools.md#google-privacy-settings) wijzigt om aan de [ Algemene Verordening van de Bescherming van Gegevens ](compliance-gdpr.md) te voldoen, is het niet noodzakelijk om gebruikerstoestemming voor het gebruik van de koekjes van Googles Analytics te verkrijgen.

## Methode 1: Impliciete toestemming

Impliciete toestemming houdt in dat bezoekers van uw winkel duidelijk begrijpen dat cookies een noodzakelijk onderdeel van de activiteiten zijn en door uw site te gebruiken indirect toestemming hebben gegeven om ze te gebruiken. De sleutel tot het verkrijgen van impliciete toestemming is het verstrekken van voldoende informatie voor een bezoeker om een geïnformeerde beslissing te nemen. Veel winkels geven boven aan alle standaardpagina&#39;s een bericht weer met een kort overzicht van het gebruik van cookies, met een koppeling naar het privacybeleid van de winkel. Het privacybeleid moet het type informatie beschrijven dat uw winkel verzamelt en hoe deze wordt gebruikt.

## Methode 2: Uitdrukkelijke toestemming

Het in werking stellen van uw opslag op _wijze van de koekjesbeperking_ vereist bezoekers om hun toestemming uit te drukken alvorens om het even welke koekjes aan hun computers kunnen worden bewaard. Veel functies van je winkel zijn niet beschikbaar, tenzij er toestemming is verleend. Als er bijvoorbeeld Googles Analytics beschikbaar zijn voor uw winkel, kan deze alleen worden aangeroepen nadat de bezoeker toestemming heeft gegeven cookies te gebruiken.

## Modus Koekjesbeperking

Wanneer de beperkingsmodus voor cookies is ingeschakeld, krijgen bezoekers van de winkel een melding dat cookies vereist zijn voor bewerkingen met alle functies. Afhankelijk van uw thema kan het bericht boven de koptekst, onder de voettekst of ergens anders op de pagina worden weergegeven. Het bericht verwijst naar uw privacybeleid voor meer informatie en moedigt bezoekers aan op de knop Toestaan te klikken om toestemming te verlenen. Nadat de toestemming wordt verleend, verdwijnt het bericht.

Uw [ privacybeleid ](privacy-policy.md)) zou de naam van uw opslag en contactinformatie moeten omvatten, en het doel van elk koekje verklaren dat door uw opslag wordt gebruikt. Meer leren, zie ](#default-cookies) Referentie van het 0} Koekje.[

>[!NOTE]
>
>Als u de URL-sleutel van het privacybeleid wijzigt, moet u ook een aangepaste URL maken om het verkeer om te leiden naar de nieuwe URL-sleutel. Anders retourneert de koppeling in het bericht Cookie Restriction Mode `404 Page Not Found` .

![ storefront van het Voorbeeld - de mededeling van de koekjesbeperking ](./assets/storefront-cookie-restriction-message.png){width="600"}

### Stap 1: de beperkingsmodus voor cookies inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies **[!UICONTROL Web]** onder **[!UICONTROL General]** in het linkernavigatievenster.

1. Vouw de sectie **[!UICONTROL Default Cookie Settings]** uit en voer de volgende handelingen uit:

   ![ configuratie van het Web - standaard koekjesmontages ](./assets/web-default-cookie-settings.png){width="600"}

   - Voer de **[!UICONTROL Cookie Lifetime]** in seconden in.

   - Als u cookies beschikbaar wilt maken voor andere mappen, voert u de **[!UICONTROL Cookie Path]** in. Voer een slash (`/`) in om de cookies overal op de site beschikbaar te maken. Deze waarde kan slechts de koekjesweg bevatten, en **_kan_** geen andere koekjesparameters bevatten.

   - Als u de cookies beschikbaar wilt maken voor een subdomein, voert u de subdomeinnaam in het veld **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com` ) in. Als u cookies beschikbaar wilt maken voor alle subdomeinen, voert u de domeinnaam in die wordt voorafgegaan door een punt (`.yourdomain.com`). Deze waarde kan slechts het koekjesdomein bevatten, en **_kan_** geen andere koekjesparameters bevatten.

   - Om scripting talen, zoals JavaScript te verhinderen, toegang tot koekjes te verkrijgen, zorg ervoor dat **slechts HTTP van het Gebruik** aan `Yes` wordt geplaatst.

   - Stel **[!UICONTROL Cookie Restriction Mode]** in op `Yes` .

     Schakel indien nodig het selectievakje uit en klik op **[!UICONTROL OK]** om het schakelen tussen bereik en bereik te bevestigen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Klik op de koppeling **[!UICONTROL Cache Management]** in het systeembericht wanneer u wordt gevraagd de cache bij te werken. Vernieuw vervolgens elke ongeldige cache.

### Stap 2: Je privacybeleid bijwerken

Werk uw [ privacybeleid ](privacy-policy.md) bij zodat het op de informatie wijst die uw bedrijf verzamelt en hoe het wordt gebruikt.

## Standaardcookies

De standaardkoekjes in Adobe Commerce en de Magento Open Source worden geclassificeerd als Vrijgesteld/niet-Vrijgesteld om handelaars te helpen aan de vereisten van privacyverordeningen zoals [ GDPR ](compliance-gdpr.md) voldoen. Handelaren dienen deze informatie als leidraad te gebruiken en juridische adviseurs te raadplegen om hun privacy- en cookiebeleid bij te werken als onderdeel van een uitgebreide nalevingsstrategie voor privacyregelgeving.

De volgende cookies worden door [!DNL Commerce] &#39;out of the box&#39; gebruikt voor installaties op locatie en in de cloud. Deze cookies zijn mogelijk vereist door functionaliteit die expliciet wordt aangevraagd door de klant. Om over het leven van zittingskoekjes te leren, zie [ Levensduur van de Zitting ](../customers/customer-online-options.md).

Sommige van deze cookies kunnen configuratieopties bieden, waaronder, indien nodig, in-/uitschakelen.

### Cookies met aangevraagde functionaliteit (vrijgesteld)


#### `add_to_cart`

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) die door de Manager van de Markering van Google wordt gebruikt. Hiermee legt u de SKU van het product vast, de naam, de prijs en de hoeveelheid die uit het winkelwagentje zijn verwijderd, en maakt u de informatie beschikbaar voor toekomstige integratie door scripts van derden.

#### `guest-view`

Hiermee slaat u de bestellings-id op die bezoekers gebruiken om de status van hun bestelling op te halen. Weergave Gastbestellingen. Wordt gebruikt in _[!DNL Orders and Returns]_-widgets.

- Is veilig? Nee
- Alleen HTTP: Ja
- Vervalbeleid: sessie
- Module: `Magento_Sales`

#### `login_redirect`

Behoudt de bestemmingspagina die alvorens de klant aan login werd geleid laadde. Login wordt omleiding gebruikt met de mini kart voor het programma geopende klanten als de ](../stores-purchase/cart-configuration.md#mini-cart) configuratieoptie van de Min van de Vertoning [ {aan `Yes` wordt geplaatst.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: sessie
- Module: `Magento_Customer`

#### `mage-banners-cache-storage`

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) slaat bannerinhoud plaatselijk op om prestaties te verbeteren.

#### `mage-messages`

Tracks foutberichten en andere meldingen die aan de gebruiker worden getoond, zoals het bevestigingsbericht van het cookie en diverse foutberichten. Het bericht wordt verwijderd uit het cookie nadat het aan de gebruiker is getoond.

Er is geen optie om deze cookie uit te schakelen.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: duur 1 jaar. Vooraan verschoven wanneer het bericht aan de gebruiker wordt getoond.
- Module: `Magento_Theme`

#### `mage-translation-storage` (lokale opslag)

Vertaalde inhoud wordt opgeslagen op verzoek van de winkelier. Gebruikt wanneer [ Vertaalstrategie ](../configuration-reference/advanced/developer.md) als &quot;Woordenboek (Vertaling op kant Storefront)&quot;wordt gevormd.

- Is veilig? Nee
- Alleen HTTP: Nee
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Translation`

#### `mage-translation-file-version` (lokale opslag)

Tracks the version of translations in local storage. Gebruikt wanneer [ Vertaalstrategie ](../configuration-reference/advanced/developer.md) als `Dictionary (Translation on Storefront side)` wordt gevormd.

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

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) die door [ wordt gebruikt de Manager van de Markering van Google ](../merchandising-promotions/google-tag-manager.md). Hiermee legt u de SKU, naam, prijs en hoeveelheid van het product vast die aan het winkelwagentje is toegevoegd, en stelt u de informatie beschikbaar voor toekomstige integratie door scripts van derden.

#### `stf`

Verslagen de tijdberichten worden verzonden door SendFriend ([ e-mail een Vriend ](../stores-purchase/email-a-friend.md)) module.

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

De waarde van dit cookie zorgt voor het opschonen van de lokale cacheopslag. Wanneer de cookie wordt verwijderd door de back-endtoepassing, schoont Admin de lokale opslag op en stelt de cookiewaarde in op `true` .

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
- Het Beleid van de vervalsing: Gebaseerd op [ het Persistent Shopping Cart ](../stores-purchase/cart-persistent.md) - de configuratie van het Levensduur van de persistentie (seconden)
- Module: `Magento_Persistent`

#### `private_content_version`

Voegt een willekeurig, uniek aantal en tijd aan pagina&#39;s met klanteninhoud toe om hen te verhinderen in het voorgeheugen ondergebracht op de server worden.

Het wordt op meerdere plaatsen ingesteld: in PHP, in JavaScript als een cookie en in JavaScript als een lokale opslaglocatie.

Voor HTTP Only= `Yes` (die op verzoek wordt gebaseerd), betekent het dat het koekje veilig is indien geplaatst tijdens HTTPS verzoek en onveilig indien geplaatst tijdens HTTP- verzoek.

- Is veilig? `Yes` (gebaseerd op verzoek), `No`
- Alleen HTTP: `No`
- Het Beleid van de vervalsing: Gebaseerd op [ het Persistent Shopping Cart ](../stores-purchase/cart-persistent.md) - de configuratie van het Levensduur van de persistentie (seconden)
   - PHP: `1` year / `315360000s` (10 jaar)
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

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Lokale opslag voor de functionaliteit van de Banner.

- Is veilig? `No`
- Alleen HTTP: `No`
- Vervalbeleid: volgens de regels voor lokale opslag
- Module: `Magento_Banner`

## Cookies Googles Analytics

De volgende koekjes worden gebruikt wanneer [ Googles Analytics ](../merchandising-promotions/google-analytics.md) of de Universele Analytics van Google volledig voor uw installatie wordt toegelaten. Om deze koekjes voor naleving van de privacyregeling onbruikbaar te maken, zie [ de Montages van de Privacy van Google ](../merchandising-promotions/google-tools.md#google-privacy-settings). Meer leren, zie {het Gebruik van de Koekjeskolom 0} Googles Analytics op Websites ][1].[

### Google Universal Analytics cookies - niet vrijgesteld

![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce) de Bibliotheken van JavaScript: `gtag.js` en `analytics.js`

- `_ga`: hiermee verdeelt u bezoekers van uw site.
- `_gid`: hiermee verdeelt u bezoekers van uw site.
- `gat`: wordt gebruikt om de aanvraagsnelheid te vertragen.
- `dc_gtm_<property-id>`: Het verzoektarief van schroeven wanneer de Googles Analytics met [ de Manager van de Markering van Google ](../merchandising-promotions/google-tag-manager.md) worden opgesteld.
- `AMP_TOKEN`: Bevat een token dat kan worden gebruikt om een client-id op te halen van de AMP Client ID-service. Andere mogelijke waarden zijn opt-out, inflight-aanvraag of een fout bij het ophalen van een client-id van de AMP Client ID-service.
- `_gac_<property-id>`: bevat campagnegerelateerde informatie voor de gebruiker. De omzettingsmarkeringen van Google AdWords lezen dit koekje als de Googles Analytics met uw [ AdWords ][2] rekening verbonden zijn.

### Cookies van Googles Analytics - niet-vrijgesteld

![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce) de Bibliotheek van JavaScript: `ga.js`

- `__utma`: onderscheidt gebruikers en sessies. Dit cookie wordt gemaakt wanneer de JavaScript-bibliotheek wordt uitgevoerd en er is geen bestaand `__utma` cookie. Het cookie wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.
- `__utmt`: wordt gebruikt om de aanvraagsnelheid te vertragen.
- `__utmb`: bepaalt nieuwe sessies/bezoeken. Dit cookie wordt gemaakt wanneer de JavaScript-bibliotheek wordt uitgevoerd en er is geen bestaand `__utmb` cookie. Het cookie wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.
- `_utmz`: hiermee slaat u de verkeersbron of campagne op waarin wordt uitgelegd hoe de gebruiker uw site heeft bereikt. Het cookie wordt gemaakt wanneer de JavaScript-bibliotheek wordt uitgevoerd en wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.
- `__utmv`: slaat aangepaste variabele gegevens op bezoekersniveau op. Dit cookie wordt gemaakt wanneer een ontwikkelaar de methode `_setCustomVar` gebruikt met een aangepaste variabele op bezoekersniveau. Dit cookie wordt bijgewerkt telkens wanneer gegevens naar Googles Analytics worden verzonden.

## Product Recommendations cookies

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) de volgende koekjes worden gebruikt door Product Recommendations voor de klanten van Adobe Commerce. Deze koekjes worden geïnstalleerd met de [ module DataServices ](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: Staat u toe [ om de gegevensinzameling van Adobe Commerce ](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) te beperken als u douanecode hebt om koekjestoestemming op uw plaats te beheren.
- `user_allowed_save_cookie`: Gebruikt voor [ wijze van de koekjesbeperking ](#cookie-restriction-mode).
- `authentication_flag`: geeft aan of een klant zich heeft aangemeld of zich heeft afgemeld. Deze cookie wordt tegelijk met het `dataservices_customer_id` cookie bijgewerkt.
- `dataservices_customer_id`: geeft aan of een klant zich heeft aangemeld of zich heeft afgemeld. Dit cookie bevat de unieke id van de klant in het systeem.
- `dataservices_customer_group`: geeft de groep van een klant aan. Dit koekje wordt opgeslagen als [ sha1 ](https://en.wikipedia.org/wiki/SHA-1) controlesom van de de groepsidentiteitskaart van de klant.
- `dataservices_cart_id`: identificeert de winkelwagentacties. Dit cookie bevat de unieke kaart-id van de klant in het systeem.
- `dataservices_product_context`: identificeert de productinteracties van een klant. Dit cookie bevat de unieke aanhalings-id van de klant in het systeem.

## Aanvullende cookies

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) de volgende koekjes worden geplaatst voor klanten van Adobe Commerce. Deze koekjes worden geïnstalleerd met de [ module DataServices ](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: wordt ingesteld door Snowplow JavaScript-tracker. Meer informatie kan in de [ documentatie van de Snowplow ](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options) worden gevonden.
- `com.adobe.alloy.getTld`: Op basis van de hostnaam van de huidige webpagina is dit het bovenste domein dat geen &quot;openbaar achtervoegsel&quot; is zoals beschreven in https://publicsuffix.org. In principe is dit het bovenste domein dat cookies kan accepteren. Dit koekje maakt deel uit van [ het Web SDK van de Legering ](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
