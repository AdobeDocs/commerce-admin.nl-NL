---
title: URL's van catalogi en producten
description: Leer over de formaattypes URL voor uw catalogusproducten, en hoe te om hen te vormen.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# URL&#39;s van catalogi en producten

De URL&#39;s die u toewijst aan producten en categorieën spelen een belangrijke rol bij het bepalen hoe goed uw site wordt geïndexeerd door zoekprogramma&#39;s. Overweeg de beschikbare opties voordat u de catalogus gaat samenstellen. Als u de huidige URL-indeling wilt weergeven, gaat u naar de winkel en navigeert u naar een willekeurig product in de catalogus. De indeling van de URL is afhankelijk van de huidige configuratie-instellingen en de methode die u gebruikt om de pagina te zoeken.

## URL-indelingen

### Dynamische URL

Een dynamische URL wordt gecreeerd _op de vlucht_ en zou een vraagkoord met variabelen voor productidentiteitskaart, soortorde, en de pagina kunnen omvatten waar het verzoek werd gemaakt. Wanneer een klant naar een product in uw winkel zoekt, kan de resulterende URL er ongeveer als volgt uitzien:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### Statische URL

Een statische URL is een vast adres voor een specifieke pagina. Een statische URL kan worden weergegeven in een indeling die geschikt is voor zoekprogramma&#39;s of in een indeling die verwijst naar producten en categorieën op ID. Deze URL&#39;s bevatten woorden die mensen kunnen gebruiken om naar een product te zoeken en waarvoor herschrijvingen van webservers moeten worden ingeschakeld. De dossiers met statische URLs worden algemeen gebruikt voor product en categoriepagina&#39;s, inhoudspagina&#39;s, en [ themaactiva ](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## URL-componenten

### URL-sleutel

De URL-sleutel is het deel van een statische URL dat het product of de categorie beschrijft. Wanneer u een product of categorie maakt, wordt automatisch een eerste URL-sleutel gegenereerd op basis van de naam. Om de sleutel te veranderen URL, zie de [&#128279;](product-search-engine-optimization.md) sectie van de Optimalisering van de Motor van het Onderzoek  van de productinformatie.

>[!NOTE]
>
>Standaard worden speciale tekens met accent automatisch vervangen door de normale versie zonder accent in de URL-sleutel. `ñ` wordt bijvoorbeeld automatisch vervangen door `n` . Dit gedrag kan worden uitgeschakeld door de configuratieoptie _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;in te stellen op `No` . Zie [ catalogus URLs ](#configure-catalog-urls) vormen.

De URL-sleutel moet bestaan uit kleine letters met niet-afbreekstreepjes tussen deze tekens om woorden van elkaar te scheiden. Afbreekstreepjes zijn niet toegestaan aan het begin of aan het einde van de URL-sleutel. Een goed ontworpen URL-sleutel die &#39;geschikt is voor zoekprogramma&#39;s&#39; kan de productnaam en trefwoorden bevatten om de manier waarop deze wordt geïndexeerd door zoekprogramma&#39;s te verbeteren. De URL-sleutel kan worden geconfigureerd om een automatische omleiding te maken als de URL-sleutel verandert.

>[!NOTE]
>
>Om aanpassingen URL, zoals gelokaliseerde URLs uit te breiden, zie [ URL herschrijft ](../merchandising-promotions/url-rewrite.md) voor meer informatie.

### HTML-achtervoegsel

Uw catalogus kan worden geconfigureerd om het achtervoegsel als onderdeel van categorie- en product-URL&#39;s op te nemen of uit te sluiten. Er zijn verschillende redenen waarom mensen zouden kunnen kiezen om het achtervoegsel te gebruiken of weg te laten. Sommigen zijn van mening dat het achtervoegsel geen nut meer heeft en dat pagina&#39;s zonder achtervoegsel effectiever worden geïndexeerd door zoekmachines. Uw bedrijf kan echter een gestandaardiseerde indeling voor URL&#39;s hebben waarvoor een achtervoegsel is vereist.

Omdat het achtervoegsel door de systeemconfiguratie wordt gecontroleerd, zou u het niet direct in de sleutel URL van een categorie of een product moeten typen. (Als u dit doet, wordt een dubbel achtervoegsel weergegeven aan het einde van de URL.) Of u nu besluit het achtervoegsel te gebruiken of niet, wees consistent en gebruik dezelfde instelling voor al uw product- en categoriepagina&#39;s. Hier volgen voorbeelden van URL&#39;s met en zonder achtervoegsel.

#### URL met achtervoegsel HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL zonder HTML-achtervoegsel

- `http://mystore.com/helena-hooded-fleece`

### Categoriepad

U kunt de product-URL&#39;s zodanig configureren dat het categoriepad wordt opgenomen of uitgesloten op basis van uw voorkeuren. Standaard is het categoriepad niet opgenomen in product-URL&#39;s. Bij geneste categorieën wordt echter altijd het volledige categoriepad weergegeven in de URL&#39;s, zodat de categorienavigatie duidelijk en consistent is. In de volgende voorbeelden ziet u dezelfde product-URL met en zonder het categoriepad.

#### Product-URL met categoriepad

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL van product zonder categoriepad

- `http://mystore.com/helena-hooded-fleece.html`

Als u wilt voorkomen dat zoekprogramma&#39;s meerdere URL&#39;s indexeren die tot dezelfde inhoud leiden, kunt u het categoriepad uitsluiten van de URL. Een andere methode is het gebruik van een canonicale metatag om zoekprogramma&#39;s te laten weten welke URL&#39;s moeten worden geïndexeerd en welke moeten worden genegeerd. Commerce neemt standaard het categoriepad niet op in product-URL&#39;s.

## Catalogus-URL&#39;s configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimizations]** sectie uit en plaats de opties:

   - Stel **[!UICONTROL Product URL Suffix]** in op `html` of `htm` . Voer het achtervoegsel zonder een punt in, omdat dit automatisch wordt toegepast.

   - Stel **[!UICONTROL Category URL Suffix]** in op `html` of `htm` . Voer het achtervoegsel zonder een punt in, omdat dit automatisch wordt toegepast.

   - Stel **[!UICONTROL Use Categories Path for Product URLs]** in op uw voorkeur.

   ![ Optimalisering van de Motor van het Onderzoek ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie {de Optimalisering van de Motor van het 0} Onderzoek [&#128279;](../configuration-reference/catalog/catalog.md#search-engine-optimization) in de _Verwijzing van de Configuratie_.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Klik op de koppeling **[!UICONTROL Cache Management]** in het systeembericht als daarom wordt gevraagd en vernieuw de ongeldige cache.

   ![ verfrist Geheime voorgeheugen ](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Voor meer informatie over deze opties, zie [ geheime voorgeheugens ](../systems/cache-management.md#refresh-specific-caches) verfrissen.

## De URL-indeling van catalogusmedia configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL General]** uit en kies **[!UICONTROL Web]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Url Options]** sectie uit en plaats de opties:

![ Web > Algemene Opties ](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Veld | [ Reikwijdte ](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Algemeen | Als rewrites van de Webserver worden toegelaten, neemt het toelaten van deze het plaatsen de Code van de Opslag van de huidige mening in URL op. Opties: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Algemeen | (Voor Single-store-instellingen) Als er een verbroken koppeling op uw site staat, wordt het verkeer omgeleid naar de basis-URL in plaats van naar een pagina met het bericht &quot;404 Pagina niet gevonden&quot;. Opties: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Belangrijk!_**&#x200B;Gebruik geen automatische omleiding naar de basis-URL voor instellingen in meerdere winkels. |
| [!UICONTROL Catalog media URL format] | Algemeen | Hiermee definieert u de URL-indeling die is toegewezen aan producten en categorieën. Opties: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definieert omgezette bestandsnaam als een unieke hash-waarde.<br />**[!UICONTROL Image optimization based on query parameters]** - bepaalt [ beeld optimaliseert ](../content-design/media-gallery-image-optimization.md) proces afhankelijk van vraagparameters. |

{style="table-layout:auto"}
