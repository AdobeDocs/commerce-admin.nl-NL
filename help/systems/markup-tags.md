---
title: Opmaaktags
description: Leer meer over opmaakcodes die codefragmenten bevatten waarmee u naar een object in uw winkel kunt verwijzen.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Opmaaktags

Een markeringsmarkering is een richtlijn die codefragment met een relatieve verwijzing naar een voorwerp in uw opslag zoals een variabele, URL, beeld, of blok bevat. De markeringen van de prijsverhoging kunnen overal worden gebruikt de redacteur beschikbaar is en in HTML van [ e-mail ](email-templates.md) en [ nieuwsbrief ](../merchandising-promotions/newsletter-template.md) malplaatjes, evenals andere soorten [ inhoud ](../content-design/introduction.md#content) wordt opgenomen.

Markeringstags worden ingesloten door dubbele accolades en kunnen worden gegenereerd met het gereedschap Widget of rechtstreeks in HTML-inhoud worden getypt. In plaats van het volledige pad naar een pagina te coderen met de code, kunt u bijvoorbeeld een opmaakcode gebruiken voor de URL van de winkel. De opmaakcodes in de volgende voorbeelden zijn:

{{$include /help/_includes/directives-caution.md}}

## Aangepaste variabele

De veranderlijke prijsverhogingsmarkering kan worden gebruikt om a [ douanevariabele ](variables-custom.md) in een e-mailmalplaatje, blokken, nieuwsbrieven, en inhoudspagina&#39;s op te nemen.

\{\{CustomVar code= &quot;my_custom_variable&quot;}

## URL van winkel

De opmaaktag URL opslaan vertegenwoordigt de basis-URL van uw website en wordt gebruikt als vervanging voor het eerste deel van een volledige URL, inclusief de domeinnaam. Er zijn twee versies van deze prijsverhogingsmarkering: één die rechtstreeks naar uw opslag gaat, en andere met een voorwaartse schuine streep (`/`) aan het eind die wordt gebruikt wanneer een weg wordt toegevoegd.

\{\{store url=&#39;apparel/schoenen/womens&#39;}

## Media-URL

De markering voor dynamische media-URL vertegenwoordigt de locatie en bestandsnaam van een afbeelding die is opgeslagen op een CDN (Content Delivery Network). De tag kan worden gebruikt om een afbeelding op een pagina, blok, banner of e-mailsjabloon te plaatsen.

\{\{media url=&#39;shoe-sale.jpg&#39;}

## Blok-id

De markering Blok-id is een van de gemakkelijkste manieren om een blok-id te gebruiken en kan worden gebruikt om een blok rechtstreeks op een CMS-pagina te plaatsen, of zelfs in een ander blok te nesten. U kunt deze techniek gebruiken om een blok voor verschillende promoties of talen te wijzigen. De markering Blok-id verwijst naar een blok met de id.

\{\{block id=&#39;block-id&#39;}

## Sjabloonlabel

Een sjabloontag verwijst naar een PHTML-sjabloonbestand en kan worden gebruikt om het blok weer te geven op een CMS-pagina of statisch blok. De code in het volgende voorbeeld kan aan een pagina of een blok worden toegevoegd om het formulier Contact met ons te tonen.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}

De code in het volgende voorbeeld kan aan een pagina of een blok worden toegevoegd om een lijst van producten in een specifieke categorie, door categorie ID te tonen.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}

## Widget-code

Met het gereedschap Widget kunt u lijsten met producten weergeven of complexe koppelingen invoegen, zoals koppelingen naar een specifieke productpagina, op basis van product-id. De code die wordt geproduceerd omvat de blokverwijzing, plaats van de codemodule, en het overeenkomstige malplaatje PHTML. Nadat de code is gegenereerd, kunt u deze van de ene naar de andere locatie kopiëren en plakken.

De code in het volgende voorbeeld kan aan een pagina of een blok worden toegevoegd om de lijst van nieuwe producten te tonen.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}

De code in het volgende voorbeeld kan aan een pagina of een blok worden toegevoegd om een verbinding aan een specifiek product, door product identiteitskaart te tonen.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;Mijn productkoppeling&quot; title=&quot;Mijn productkoppeling&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}

## Markeringstags gebruiken in koppelingen

U kunt opmaaktags gebruiken met HTML-ankertags en rechtstreeks koppelen aan een willekeurige pagina in uw winkel. De koppeling kan worden opgenomen in inhoudspagina&#39;s, blokken of sjablonen voor e-mail en nieuwsbrief. U kunt deze techniek ook gebruiken om een afbeelding aan een specifieke pagina te koppelen.

### Stap 1. De doel-URL identificeren

Blader, indien mogelijk, naar de pagina waarnaar u wilt koppelen en kopieer de volledige URL van de adresbalk van uw browser. Het deel van de URL dat u nodig hebt, komt na de `.com/` . Als dat niet het geval is, kopieert u de URL-sleutel van de CMS-pagina die u als doel voor de koppeling wilt gebruiken.

#### Volledige URL naar categoriepagina

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### Volledige URL naar productpagina

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### Volledige URL naar CMS-pagina

`https://mystore.com/about-us`

### Stap 2. De markering toevoegen aan de URL

De tag Store URL vertegenwoordigt de basis-URL van uw website en wordt gebruikt als vervanging voor het HTTP-adresgedeelte van de winkel-URL, inclusief de domeinnaam en `.com` . Er zijn twee versies van de tag, die u kunt gebruiken, afhankelijk van de resultaten die u wilt bereiken.

`store direct_url` - Koppelingen rechtstreeks naar een pagina.

`store url` - Hiermee plaatst u een slash aan het einde, zodat extra verwijzingen kunnen worden toegevoegd als een pad.

In de volgende voorbeelden wordt de URL-sleutel tussen enkele aanhalingstekens geplaatst en wordt de volledige opmaaktag tussen dubbele accolades geplaatst. Wanneer de markering wordt gebruikt met een ankertag, wordt deze binnen de dubbele aanhalingstekens van het anker geplaatst. U voorkomt verwarring door enkele en dubbele aanhalingstekens te gebruiken voor elke geneste set aanhalingstekens.

Als u begint met een volledige URL, verwijdert u het HTTP-adres (`http://` of `https://` ) deel van de URL, tot en met `.com/` . Voer in plaats daarvan de opmaaktag URL van winkel in, tot en met het eerste enkele aanhalingsteken.

#### Tag voor URL-markering opslaan

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

Anders voert u het eerste deel van de opmaaktag Store URL in en plakt u de URL-sleutel of het pad dat u eerder hebt gekopieerd.

### Tag voor URL-markering opslaan met URL-sleutel

`{{store url=`

Voer de afsluitende dubbele aanhalingstekens en accolades in om de markering te voltooien.

`{{store url='apparel/shoes/womens'}}`

### Stap 3. De ankertag voltooien

Plaats de voltooide opmaakcode binnen een ankertag met de opmaaktag in plaats van de doel-URL. Voeg vervolgens de koppelingstekst en de afsluitende ankertag toe.

#### Opmaak in ankertag

\&lt;a href=&quot;\{\{markup tag goes here}&quot;>

Plak de voltooide ankertag in de code van een CMS-pagina, -blok, -banner of -e-mailsjabloon, waar u de koppeling wilt weergeven.

### Koppeling met markering voltooien

\&lt;a href=&quot;\{\{store url=&#39;apparel/schoenen&#39;}&quot;>Schoonverkoop\&lt;/a>

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
