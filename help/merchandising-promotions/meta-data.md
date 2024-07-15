---
title: Metagegevens
description: Leer hoe u trefwoordrijke metagegevens kunt invoeren om de manier te verbeteren waarop zoekprogramma's uw Commerce-site indexeren.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Metagegevens

Uw winkel wordt geladen met plaatsen waar u trefwoordrijke metagegevens kunt invoeren om de manier te verbeteren waarop zoekprogramma&#39;s uw site indexeren. Tijdens het instellen van de winkel kunt u voorlopige metagegevens invoeren, met de bedoeling deze later af te ronden. In de loop der tijd kunt u de metagegevens afstemmen op de aankooppatronen en -voorkeuren van uw klanten.

![ montages van het Product - de optimalisering van de onderzoeksmotor ](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Meta-titel

De titel van de meta wordt weergegeven in de titelbalk en op het tabblad van uw browser en in aanbiedingen met zoekresultaten. De titel van de meta zou uniek aan de pagina moeten zijn, en minder dan 70 karakters in lengte.

![ storefront van het Voorbeeld - metattitle ](./assets/storefront-home-page-meta-title.png){width="600"}

## Meta-trefwoorden

Hoewel sommige zoekprogramma&#39;s metatrefwoorden negeren, blijven andere deze gebruiken. De huidige beste praktijken moeten high-value sleutelwoorden in de metattitel en meta beschrijving opnemen.

![ browser van het Web onderzoek - metatrefwoorden ](./assets/storefront-meta-description.png){width="500"}

## Meta-beschrijving

Meta-beschrijvingen bieden een kort overzicht van de pagina voor aanbiedingen met zoekresultaten. In het ideale geval moet een metabeschrijving tussen 150 en 160 tekens lang zijn, hoewel het veld maximaal 255 tekens accepteert.

## Rijke fragmenten

Rich snippets bieden gedetailleerde informatie voor zoekresultaten en andere toepassingen. Door gebrek, wordt de gestructureerde gegevensprijsverhoging die op de {][1] norm 0} schema.org wordt gebaseerd toegevoegd aan het productmalplaatje van uw opslag. [ Dientengevolge, is meer informatie beschikbaar voor onderzoeksmotoren om als _rijke fragmenten_ in productlijsten te omvatten.

## Canonical meta tag

Sommige zoekprogramma&#39;s bestraffen websites met meerdere URL&#39;s die naar dezelfde inhoud verwijzen. De canonieke meta-tag vertelt zoekprogramma&#39;s welke pagina ze moeten indexeren wanneer meerdere URL&#39;s dezelfde of vergelijkbare inhoud hebben. Met de canonieke metatag kunt u de positie van uw site en de weergave van geaggregeerde pagina&#39;s verbeteren. De canonieke meta-tag wordt in het `<head>` -blok van een product- of categoriepagina geplaatst. Het bevat een koppeling naar uw voorkeursURL, zodat zoekprogramma&#39;s er meer gewicht aan toekennen.

### Voorbeeld 1: categoriepad maakt dubbele URL&#39;s

Als uw catalogus bijvoorbeeld is geconfigureerd om het categoriepad op te nemen in product-URL&#39;s, genereert uw winkel meerdere URL&#39;s die naar dezelfde productpagina verwijzen.

     http://mystore.com/gear/bags/driven-backpack.html
     http://mystore.com/driven-backpack.html 

### Voorbeeld 2: volledige URL voor categoriepagina

Wanneer canonieke metatags voor categorieën zijn ingeschakeld, bevat de categoriepagina van uw winkel een canonieke URL naar de volledige categorie-URL:

     http://mystore.com/gear/bags/

### Voorbeeld 3: volledige URL van productpagina

Wanneer canonieke metatags voor producten zijn ingeschakeld, bevat de productpagina een canonieke URL naar de domeinnaam/product-url-sleutel, omdat de URL-sleutels van het product wereldwijd uniek zijn.

     http://mystore.com/driven-backpack.html

Als u ook het categoriepad opneemt in product-URL&#39;s, blijft de canonieke URL domeinnaam/product-url-sleutel. Het product is echter ook toegankelijk via de volledige URL, die de categorie bevat. Als de product-URL bijvoorbeeld `driven-backpack` is en is toegewezen aan de categorie Gear > Bags, kunt u het product openen via een van beide URL&#39;s.

U kunt voorkomen dat zoekmachines worden gestraft door de categorie weg te laten van de URL of door de canonieke metatag te gebruiken om zoekprogramma&#39;s te laten indexeren op product of categorie. U kunt het beste kanonische metatags inschakelen voor zowel categorieën als producten.

### De canonieke meta-tag inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **sectie van de Optimalisering van de Motor van het Onderzoek**.

   Om om het even welke gebiedswaarden te veranderen, moet u het **checkbox van de systeemwaarde van het 0} Gebruik na elk gebied eerst ontruimen.**

   ![ configuratie van de Catalogus - de optimalisering van de onderzoeksmotor ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Als u wilt dat zoekprogramma&#39;s alleen categoriepagina&#39;s indexeren met het volledige categoriepad, doet u het volgende:

   - Plaats **Markering van Meta van de Verbinding van het Gebruik Canonical voor Categorieën** aan `Yes`.

   - Plaats **de Canonieke markering van Meta van de Verbinding van het Gebruik voor Producten** aan `No`.

1. Als u wilt dat zoekprogramma&#39;s productpagina&#39;s alleen indexeren met de indeling domeinnaam/product-URL-sleutel, doet u het volgende:

   - Plaats **de Canonieke markering van Meta van de Verbinding van het Gebruik voor Producten** aan `Yes`.

   - Plaats **Markering van Meta van de Verbinding van het Gebruik Canonical voor Categorieën** aan `No`.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Meta-gegevensdemo

Bekijk deze video voor meer informatie over het beheer van SEO-metagegevens:

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12)

[1]: https://schema.org/
