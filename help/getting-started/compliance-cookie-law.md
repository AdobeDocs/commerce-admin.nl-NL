---
title: Naleving van Cookie-recht
description: Om gelijke tred te houden met de wetgeving in veel landen inzake het gebruik van cookies, bieden Adobe Commerce en Magento Open Source handelaren een keuze aan methoden om toestemming van klanten te verkrijgen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: abdd70f63ce9ce49ea7e6552951c644480f6024f
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# Naleving van Cookie-recht

Cookies zijn kleine bestanden die worden opgeslagen op de computer van elke bezoeker van uw site en die worden gebruikt als tijdelijke opslagplaatsen ter informatie. Informatie die in cookies wordt opgeslagen, wordt gebruikt om de winkelervaring te personaliseren, bezoekers te koppelen aan hun winkelwagentjes, verkeerspatronen te meten en de doeltreffendheid van promoties te verbeteren. Om gelijke tred te houden met de wetgeving in veel landen inzake het gebruik van cookies, bieden Adobe Commerce en Magento Open Source handelaren een keuze aan methoden om toestemming van klanten te verkrijgen. Voor een lijst van de standaardkoekjes in Adobe Commerce en Magento Open Source, de [ Verwijzing van het Koekje ](#default-cookies).

>[!NOTE]
>
>Als u het gebrek [ de privacymontages van Google ](../merchandising-promotions/google-tools.md#google-privacy-settings) wijzigt om aan de [ Algemene Verordening van de Bescherming van Gegevens ](compliance-gdpr.md) te voldoen, is het niet noodzakelijk om gebruikerstoestemming voor het gebruik van de koekjes van Google Analytics te verkrijgen.

## Modus Koekjesbeperking

Wanneer de beperkingsmodus voor cookies is ingeschakeld, krijgen bezoekers van de winkel een melding dat cookies vereist zijn voor bewerkingen met alle functies. Afhankelijk van uw thema kan het bericht boven de koptekst, onder de voettekst of ergens anders op de pagina worden weergegeven. Het bericht verwijst naar uw privacybeleid voor meer informatie en moedigt bezoekers aan op de knop Toestaan te klikken om toestemming te verlenen. Nadat de toestemming wordt verleend, verdwijnt het bericht.

Uw [ privacybeleid ](privacy-policy.md)) zou de naam van uw opslag en contactinformatie moeten omvatten, en het doel van elk koekje verklaren dat door uw opslag wordt gebruikt. Meer leren, zie [&#128279;](#default-cookies) Referentie van het 0&rbrace; Koekje.

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

1. Wanneer u wordt gevraagd de cache bij te werken, klikt u op de koppeling **[!UICONTROL Cache Management]** in het systeembericht en vernieuwt u elke ongeldige cache.

### Stap 2: Je privacybeleid bijwerken

Werk uw [ privacybeleid ](privacy-policy.md) bij zodat het op de informatie wijst die uw bedrijf verzamelt en hoe het wordt gebruikt.

## Standaardcookies

De standaardkoekjes in Adobe Commerce en Magento Open Source worden geclassificeerd als Vrijgesteld/niet-Vrijgesteld om handelaars te helpen aan de vereisten van privacyverordeningen zoals [ GDPR ](compliance-gdpr.md) voldoen. Handelaren dienen deze informatie als leidraad te gebruiken en juridische adviseurs te raadplegen om hun privacy- en cookiebeleid bij te werken als onderdeel van een uitgebreide nalevingsstrategie voor privacyregelgeving.

De volgende cookies worden door [!DNL Commerce] &#39;out of the box&#39; gebruikt voor installaties op locatie en in de cloud. Deze cookies zijn mogelijk vereist door functionaliteit die expliciet wordt aangevraagd door de klant. Meer over het leven van zittingskoekjes leren, zie [ Levensduur van de Zitting ](../customers/customer-online-options.md).

Sommige van deze cookies kunnen configuratieopties bieden, waaronder, indien nodig, in-/uitschakelen.

### Cookies met aangevraagde functionaliteit (vrijgesteld)

#### `add_to_cart`

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) vangt het product SKU, de naam, de prijs, en de hoeveelheid die uit het karretje wordt verwijderd. Hiermee kan Google Analytics weten wanneer een product aan een winkelwagen is toegevoegd.

#### `guest-view`

Koppelt een gastorder aan een gast (omdat er geen account voor de gast is).

#### `login_redirect`

Slaat omleiding URL aan routegebruiker op als succesvol login en gebruikersregistratie. Hiermee slaat u de pagina op die een gebruiker vóór het aanmelden had (om de locatie te bepalen waarnaar de gebruiker na het aanmelden teruggaat).

#### `mage-banners-cache-storage`

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) slaat bannerinhoud plaatselijk op om prestaties te verbeteren. De inhoud van de banner is om het even welke inhoud die een handelaar op hun website zou tonen.

#### `mage-messages`

Tracks foutberichten en andere meldingen die aan de gebruiker worden getoond, zoals het bevestigingsbericht van het cookie en diverse foutberichten. Het bericht wordt verwijderd uit het cookie nadat het aan de gebruiker is getoond. Er is geen optie om deze cookie uit te schakelen. Zo wordt eenmalig informatie doorgegeven aan de gebruiker, zoals foutberichten.

#### `product_data_storage` (lokale opslag)

Hiermee slaat u de configuratie op voor productgegevens die worden gebruikt voor de functies &quot;Recent bekeken&quot; en &quot;Producten vergelijken&quot;. Hiermee worden de specifieke instellingen van een gebruiker opgeslagen (bijvoorbeeld als deze onlangs een product heeft bekeken of producten heeft vergeleken).

#### `recently_compared_product` (lokale opslag)

Hiermee slaat u product-id&#39;s op van producten die onlangs zijn vergeleken.

#### `recently_compared_product_previous` (lokale opslag)

Hiermee slaat u product-id&#39;s van eerder vergeleken producten op voor eenvoudige navigatie.

#### `recently_viewed_product` (lokale opslag)

Hiermee slaat u product-id&#39;s van onlangs bekeken producten op voor eenvoudige navigatie.

#### `recently_viewed_product_previous` (lokale opslag)

Hiermee slaat u product-id&#39;s van onlangs bekeken producten op voor eenvoudige navigatie.

#### `remove_from_cart`

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) staat Google Analytics toe om te weten wanneer een product uit een kar is verwijderd.

#### `stf`

Verslagen de tijdberichten worden verzonden door SendFriend ([ e-mail een Vriend ](../stores-purchase/email-a-friend.md)) module. Wanneer een winkelier een koppeling naar een product verzendt, wordt in dit cookie een tijdstempel vastgelegd en wordt een telling bijgehouden.

#### `X-Magento-Vary`

Geeft aan wanneer een nieuwe versie van een pagina moet worden verzonden vanuit de cache. Ondersteunt de prestaties van websites.

#### `form_key`

Een veiligheidsmechanisme dat een willekeurig geproduceerde waarde houdt om de aanvallen van de smeedmachine van het Verzoek van de Cross-Site te verhinderen (CSRF) door te helpen bepalen of een verzoek uit een echte bron of een slechte actor kwam. Dit is een industriestandaard praktijk om aanvallen van CSRF te verhinderen.

#### `mage-cache-sessid`

Nuttig om te bepalen wanneer lokale opslag in de browser moet worden schoongemaakt na het verstrijken van de sessie. Dit wordt gebruikt om te bepalen of lokale opslag moet worden schoongemaakt. Door het ontbreken van deze cookie wordt de lokale opslag opgeschoond.

#### `mage-cache-storage`

Lokale opslag van bezoekersspecifieke inhoud die e-commercefuncties toelaat. Niet gebruikt door gebrek, maar wanneer het wordt gebruikt, wordt het gebruikt om afhandeling te versnellen zodat de basisgebruikersinformatie beschikbaar is wanneer iemand verlaat en terugkeert.

#### `mage-cache-storage-section-invalidation`

Hiermee slaat u informatie op over welke secties van de pagina ongeldig moeten worden gemaakt en verwijderd.

#### `persistent_shopping_cart`

Hiermee slaat u de sleutel-id van een permanente winkelwagen op, zodat de winkelwagen voor een anonieme winkelier kan worden hersteld.

#### `private_content_version`

Voegt een willekeurig, uniek aantal en tijd aan pagina&#39;s met klanteninhoud toe om hen te verhinderen in het voorgeheugen ondergebracht op de server worden. Het wordt op meerdere plaatsen ingesteld: in PHP, in JavaScript als een cookie en in JavaScript als een lokale opslaglocatie.

#### `section_data_ids`

Hiermee slaat u klantspecifieke informatie op over acties die door winkels worden geïnitieerd, zoals weergave van wensenlijsten en afhandelingsgegevens.

#### `store`

Volgt de specifieke opslagweergave/landinstelling die door de winkelier is geselecteerd.

#### `mage-banners-cache-storage`

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Lokale opslag voor de functionaliteit van de Banner. De banner betekent algemene website activa om het even welke informatie die aan een verkoopster wordt getoond.

#### `PHPSESSID`

Houdt gebruikerszittingen op de winkel bij. Dit zijn de kopers die de eindproducten gebruiken.

#### `admin`

Houdt gebruikerszittingen op de Admin kant bij.

#### `loggedOutReasonCode`

Instellen wanneer een Admin-gebruiker wordt vergrendeld nadat een bepaald aantal mislukte wachtwoorden is geprobeerd.

#### `section_data_clean`

Instellen wanneer een gebruikerswisselaar de weergave opslaat. De aanwezigheid van deze cookie zorgt ervoor dat JavaScript bepaalde secties op de pagina opnieuw laadt om de juiste winkelweergave te weerspiegelen.

#### `lang`

Deze optie wordt indirect ingesteld door de module Admin Analytics. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `s_fid`

Deze optie wordt indirect ingesteld door de module Admin Analytics. Unieke tijd-/datumstempel van bezoekersidentiteitskaart afwisselen. Hiermee wordt een unieke bezoeker geïdentificeerd als de standaard `s_vi` -cookie niet beschikbaar is vanwege cookie-beperkingen van derden. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `s_cc`

Deze optie wordt indirect ingesteld door de module Admin Analytics. Deze wordt ingesteld en gelezen door de JavaScript-code om te bepalen of cookies zijn ingeschakeld. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `apt.sid`

Wordt ingesteld door de Gainsight PX-bibliotheek die indirect wordt gebruikt door de beheermodule Analytics. Het doel van dit cookie is het bijhouden van een permanente sessie-id toe te staan onder het domein op hoofdniveau van het product en wordt gebruikt als referentie-id voor de actieve sessie. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `apt.uid`

Wordt ingesteld door de Gainsight PX-bibliotheek die indirect wordt gebruikt door de beheermodule Analytics. Het doel van dit cookie is het permanent bijhouden van id&#39;s toe te staan onder het domein op hoofdniveau van het product en wordt gebruikt als referentie-id voor de gebruikersentiteit. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `s_sq`

Deze optie wordt indirect ingesteld door de module Admin Analytics. Wordt gebruikt door de ClickMap-functie die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. Hiermee slaat u gegevens van elke klik op. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `pagebuilder_modal_dismissed`

Door de Module van de Bouwer van de Pagina worden geplaatst. Bevat een vlag die verdere herinneringen verhindert die een beheerder vragen om een bepaalde actie te bevestigen openen als de beheerder hen uitdrukkelijk verwierp alvorens. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `pagebuilder_template_apply_confirm`

Door de Module van de Bouwer van de Pagina worden geplaatst. Bevat een vlag die verdere herinneringen verhindert die een beheerder vragen om een bepaalde actie te bevestigen openen als de beheerder hen uitdrukkelijk verwierp alvorens. Wordt alleen gebruikt in een administratieve ruimte van een winkel. Niet van toepassing op kopers.

#### `accordion-&lbrace;VARIABLE&rbrace;-&lbrace;VARIABLE&rbrace;`

Wordt alleen gebruikt als onderdeel van de implementatie van de tabfunctionaliteit in een beheergebied van een winkel. Niet van toepassing op kopers.

## Cookies met productaanbevelingen

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) de volgende koekjes worden gebruikt door de Aanbevelingen van het Product voor de klanten van Adobe Commerce. Deze koekjes worden geïnstalleerd met de [ module DataServices ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg_dnt`: Staat u toe [ om de gegevensinzameling van Adobe Commerce ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/developer/setting-cookie) te beperken als u douanecode hebt om koekjestoestemming op uw plaats te beheren.
- `user_allowed_save_cookie`: Gebruikt voor [ wijze van de koekjesbeperking ](#cookie-restriction-mode).
- `authentication_flag`: geeft aan of een klant zich heeft aangemeld of zich heeft afgemeld. Deze cookie wordt tegelijk met het `dataservices_customer_id` cookie bijgewerkt.
- `dataservices_customer_id`: geeft aan of een klant zich heeft aangemeld of zich heeft afgemeld. Dit cookie bevat de unieke id van de klant in het systeem.
- `dataservices_customer_group`: geeft de groep van een klant aan. Dit koekje wordt opgeslagen als [ sha1 ](https://en.wikipedia.org/wiki/SHA-1) controlesom van de de groepsidentiteitskaart van de klant.
- `dataservices_cart_id`: identificeert de winkelwagentacties. Dit cookie bevat de unieke kaart-id van de klant in het systeem.
- `dataservices_product_context`: identificeert de productinteracties van een klant. Dit cookie bevat de unieke aanhalings-id van de klant in het systeem.

## Aanvullende cookies

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) de volgende koekjes worden geplaatst voor klanten van Adobe Commerce. Deze koekjes worden geïnstalleerd met de [ module DataServices ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg`: wordt ingesteld door Snowplow JavaScript-tracker. Meer informatie kan in de [ documentatie van de Snowplow ](https://docs.snowplow.io/docs/sources/trackers/javascript-trackers/web-tracker/tracker-setup/initialization-options/) worden gevonden.
- `com.adobe.alloy.getTld`: Op basis van de hostnaam van de huidige webpagina is dit het bovenste domein dat geen &quot;openbaar achtervoegsel&quot; is zoals beschreven in https://publicsuffix.org. In principe is dit het bovenste domein dat cookies kan accepteren. Dit koekje maakt deel uit van [ het Web SDK ](https://github.com/adobe/alloy) van de Legering.

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
