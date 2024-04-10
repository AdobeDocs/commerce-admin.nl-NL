---
title: Wat is de winkel?
description: Meer informatie over de pagina's en functionele elementen die uw winkel kan bieden ter ondersteuning van de winkelervaring voor uw klanten.
exl-id: 1c64888f-2bc0-4e2e-b7da-0e7182ea67e0
feature: Storefront
source-git-commit: 3b359ed43e81a2771a372c8e3c7557853b3eecad
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Wat is de winkel?

In uw Adobe Commerce- of Magento Open Source-implementatie is de winkel het externe, openbare gedeelte van uw winkel. Het biedt de inhoud en functionele componenten die uw klanten gebruiken om te winkelen en aan te schaffen.

Het pad dat klanten naar een verkoop nemen, wordt soms ook wel _pad naar aankoop_ en uw winkel bevat de componenten waarmee klanten dit pad kunnen voltooien. In de volgende secties vindt u een overzicht van de basispaginatypen die een strategische waarde bieden. De plaatsen waar klanten gewoonlijk bezoeken tijdens het winkelen in uw winkel. Terwijl u ze bekijkt, moet u rekening houden met verschillende opslagfuncties die in elk stadium van de reis van de klant kunnen worden gebruikt.

## Homepage

Wist u dat de meeste mensen slechts een paar seconden op een pagina doorbrengen voordat ze besluiten om ergens anders te blijven of te gaan? Het is niet lang om een indruk te maken. Studies tonen aan dat mensen ook van foto&#39;s houden, vooral van andere mensen. Welk ontwerp u ook kiest, alles op uw homepage zou bezoekers naar de volgende stap in het verkoopproces moeten bewegen. Het is de bedoeling dat zij hun aandacht in een samenhangende stroom van het ene punt van belang naar het andere vestigen.

![Voorbeeld van homepage van winkel](./assets/storefront-homepage-full.png){width="700"}

## Cataloguspagina

Aanbiedingen op cataloguspagina&#39;s hebben doorgaans kleine productafbeeldingen en korte beschrijvingen en kunnen worden opgemaakt als een lijst of als een raster. U kunt blokken, video&#39;s en beschrijvingen met veel trefwoorden toevoegen en ook speciale ontwerpen maken voor een speciale aanbieding of seizoen. U kunt een speciale categorie maken voor een levensstijl of merk die een curated collectie producten uit verschillende categorieën bevat.

De oorspronkelijke productbeschrijving geeft kopers meestal genoeg informatie om er beter uit te zien. Mensen die weten wat ze willen, kunnen het product aan hun winkelwagentjes toevoegen en gaan. Klanten die winkelen terwijl ze zich aanmelden bij hun account, genieten van een persoonlijke winkelervaring.

![Verzamelingspagina op de winkelpagina](./assets/storefront-collection-page.png){width="700"}

## Zoekresultaten

Wist u dat mensen die zoeken bijna twee keer zo vaak een aankoop doen als mensen die alleen op navigatie vertrouwen? Je zou kunnen denken dat deze kopers _vooraf gekwalificeerd_.

### [!DNL Live Search]

Met [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) voor Adobe Commerce biedt uw winkel een snelle, superrelevante en intuïtieve zoekervaring en is gratis beschikbaar voor Adobe Commerce.

![Voorbeeld van Live zoeken - zoeken terwijl u typt](./assets/storefront-search-as-you-type.png){width="700"}

### Standaardcataloguszoekopdracht

Met [standaardcataloguszoekopdracht](../catalog/search.md), bevat uw winkel een zoekvak in de rechterbovenhoek en een koppeling naar Geavanceerd zoeken in de voettekst. Alle zoektermen die kopers verzenden, worden opgeslagen, zodat je precies kunt zien wat ze zoeken. U kunt suggesties aanbieden, en synoniemen en gemeenschappelijke misspellingen ingaan. Geef vervolgens een specifieke pagina weer wanneer een zoekterm wordt ingevoerd.

![Voorbeeld van standaard zoekresultaten in een catalogus](./assets/storefront-search-results-page-full.png){width="700"}

## Productpagina

De productpagina gaat veel verder! Het eerste wat uw ogen op de productpagina raakt, is de hoofdafbeelding met een zoomgalerie met hoge resolutie en een miniatuurgalerie. Naast de prijs en beschikbaarheid is er een gedeelte met tabbladen met meer informatie en een lijst met verwante producten.

![Voorbeeld van productpagina van winkel](./assets/storefront-product-page-full-m.png){width="700"}

## Winkelwagentje

In het winkelwagentje kan het ordertotaal worden bepaald, samen met kortingsbonnen en geschatte verzendkosten en belastingen, en een geweldige plaats om je vertrouwensbadges en zegels weer te geven. Het is ook een ideale gelegenheid om nog een laatste punt aan te bieden. Als een cross-sell-object kunt u bepaalde objecten selecteren die als een impulsaankoop moeten worden aangeboden wanneer een bepaald object in het winkelwagentje wordt weergegeven.

![Voorbeeld winkelwagentje](./assets/storefront-cart-full.png){width="700"}

## Afhandelingspagina

Afhandelingsproces bestaat uit twee stappen:

1. Verzendgegevens

   De eerste stap van het afrekenproces is dat de klant de verzendadresgegevens invult en de verzendmethode kiest. Als de klant een account heeft, wordt het verzendadres automatisch ingevoerd, maar kan het indien nodig worden gewijzigd.
Als een gastklant een e-mailadres invoert dat als eerder geregistreerd wordt erkend, wordt de aanmeldingsprompt weergegeven als [!UICONTROL Enable Guest Checkout Login] veld in de opslagconfiguratie is ingesteld op `Yes` (zie [[!UICONTROL Checkout Options]](../configuration-reference/sales/checkout.md#checkout-options) in de _Referentiehandleiding voor configuratie_). Nochtans, kan dit het plaatsen klanteninformatie aan niet voor authentiek verklaarde gebruikers blootstellen.

   ![Voorbeeld van uitcheckpagina voor winkel](./assets/storefront-checkout-shipping-full.png){width="700"}

1. Gegevens bekijken en betalen

   De tweede stap van het afrekeningsproces is dat de klant de betalingsmethode kiest en eventueel een kortingscode toepast.

   >[!NOTE]
   >
   >Hoewel [!DNL Commerce] met de configuratie van meerdere couponcodes kan een klant slechts één couponcode op de kaart toepassen. (Zie de [Couponcodes](../merchandising-promotions/price-rules-cart-coupon.md#coupon-codes) voor meer informatie .)

   ![Voorbeeld van uitcheckpagina voor winkel](./assets/storefront-checkout-payment-full.png){width="700"}

De voortgangsbalk boven aan de pagina volgt elke stap van het uitcheckproces en de _Overzicht van bestellingen_ toont de informatie die tot dit punt is ingegaan.

>[!NOTE]
>
>De uitzondering op een controle in twee stappen is van toepassing op virtuele en/of downloadbare producten. Als het winkelwagentje alleen dergelijke producten bevat, wordt de afhandeling automatisch omgezet in één stap, omdat de verzendgegevens niet vereist zijn.
