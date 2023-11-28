---
title: URL's van catalogi en producten
description: Leer over de formaattypes URL voor uw catalogusproducten, en hoe te om hen te vormen.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# URL&#39;s van catalogi en producten

De URL&#39;s die u toewijst aan producten en categorieën spelen een belangrijke rol bij het bepalen hoe goed uw site wordt geïndexeerd door zoekprogramma&#39;s. Overweeg de beschikbare opties voordat u de catalogus gaat samenstellen. Als u de huidige URL-indeling wilt weergeven, gaat u naar de winkel en navigeert u naar een willekeurig product in de catalogus. De indeling van de URL is afhankelijk van de huidige configuratie-instellingen en de methode die u gebruikt om de pagina te zoeken.

## URL-indelingen

### Dynamische URL

Er wordt een dynamische URL gemaakt _op de vlucht_ en bevat mogelijk een queryreeks met variabelen voor de product-id, de sorteervolgorde en de pagina waar de aanvraag is ingediend. Wanneer een klant naar een product in uw winkel zoekt, kan de resulterende URL er ongeveer als volgt uitzien:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### Statische URL

Een statische URL is een vast adres voor een specifieke pagina. Een statische URL kan worden weergegeven in een indeling die geschikt is voor zoekprogramma&#39;s of in een indeling die verwijst naar producten en categorieën op ID. Deze URL&#39;s bevatten woorden die mensen kunnen gebruiken om naar een product te zoeken en waarvoor herschrijvingen van webservers moeten worden ingeschakeld. Bestanden met statische URL&#39;s worden doorgaans gebruikt voor product- en categoriepagina&#39;s, inhoudspagina&#39;s en [thema-elementen](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## URL-componenten

### URL-sleutel

De URL-sleutel is het deel van een statische URL dat het product of de categorie beschrijft. Wanneer u een product of categorie maakt, wordt automatisch een eerste URL-sleutel gegenereerd op basis van de naam. Als u de URL-sleutel wilt wijzigen, raadpleegt u de [Optimalisatie zoekmachine](product-search-engine-optimization.md) in de productinformatie.

>[!NOTE]
>
>Speciale tekens met accent worden automatisch vervangen door de normale versie zonder accent in de URL-sleutel. Bijvoorbeeld: `ñ` wordt automatisch vervangen door `n`.

De URL-sleutel moet bestaan uit kleine letters met niet-afbreekstreepjes tussen deze tekens om woorden van elkaar te scheiden. Afbreekstreepjes zijn niet toegestaan aan het begin of aan het einde van de URL-sleutel. Een goed ontworpen URL-sleutel die &#39;geschikt is voor zoekprogramma&#39;s&#39; kan de productnaam en trefwoorden bevatten om de manier waarop deze wordt geïndexeerd door zoekprogramma&#39;s te verbeteren. De URL-sleutel kan worden geconfigureerd om een automatische omleiding te maken als de URL-sleutel verandert.

>[!NOTE]
>
>Zie voor meer informatie over URL-aanpassingen, zoals gelokaliseerde URL&#39;s [URL herschrijft](../merchandising-promotions/url-rewrite.md) voor meer informatie .

### achtervoegsel HTML

Uw catalogus kan worden geconfigureerd om het achtervoegsel als onderdeel van categorie- en product-URL&#39;s op te nemen of uit te sluiten. Er zijn verschillende redenen waarom mensen zouden kunnen kiezen om het achtervoegsel te gebruiken of weg te laten. Sommigen zijn van mening dat het achtervoegsel geen nut meer heeft en dat pagina&#39;s zonder achtervoegsel effectiever worden geïndexeerd door zoekmachines. Uw bedrijf kan echter een gestandaardiseerde indeling voor URL&#39;s hebben waarvoor een achtervoegsel is vereist.

Omdat het achtervoegsel door de systeemconfiguratie wordt gecontroleerd, zou u het niet direct in de sleutel URL van een categorie of een product moeten typen. (Als u dit doet, wordt een dubbel achtervoegsel weergegeven aan het einde van de URL.) Of u nu besluit het achtervoegsel te gebruiken of niet, wees consistent en gebruik dezelfde instelling voor al uw product- en categoriepagina&#39;s. Hier volgen voorbeelden van URL&#39;s met en zonder achtervoegsel.

#### URL met achtervoegsel HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL zonder achtervoegsel HTML

- `http://mystore.com/helena-hooded-fleece`

### Categoriepad

U kunt de URL zodanig configureren dat het categoriepad wordt opgenomen of uitgesloten. Standaard wordt het categoriepad opgenomen in alle categorieën en productpagina&#39;s. In de volgende voorbeelden ziet u dezelfde product-URL met en zonder het categoriepad.

#### URL met categoriepad

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL zonder categoriepad

- `http://mystore.com/helena-hooded-fleece.html`

Als u wilt voorkomen dat zoekprogramma&#39;s meerdere URL&#39;s indexeren die tot dezelfde inhoud leiden, kunt u het categoriepad uitsluiten van de URL. Een andere methode is het gebruik van een canonicale metatag om zoekprogramma&#39;s te laten weten welke URL&#39;s moeten worden geïndexeerd en welke moeten worden genegeerd. Standaard wordt bij Handel het categoriepad niet opgenomen in product-URL&#39;s.

## Catalogus-URL&#39;s configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimizations]** en stel de opties in:

   - Set **[!UICONTROL Product URL Suffix]** tot `html` of `htm`. Voer het achtervoegsel zonder een punt in, omdat dit automatisch wordt toegepast.

   - Set **[!UICONTROL Category URL Suffix]** tot `html` of `htm`. Voer het achtervoegsel zonder een punt in, omdat dit automatisch wordt toegepast.

   - Set **[!UICONTROL Use Categories Path for Product URLs]** naar uw voorkeur.

   ![Optimalisatie zoekmachine](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [Optimalisatie zoekmachine](../configuration-reference/catalog/catalog.md#search-engine-optimization) in de _Configuratieverwijzing_.

1. Klik op **[!UICONTROL Save Config]**.

1. Klik op de knop **[!UICONTROL Cache Management]** koppeling in het systeembericht en vernieuw de ongeldige cache.

   ![Cache vernieuwen](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Zie voor meer informatie over deze opties [caches vernieuwen](../systems/cache-management.md#refresh-specific-caches).

## De URL-indeling van catalogusmedia configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL General]** en kiest u **[!UICONTROL Web]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Url Options]** en stel de opties in:

![Web > Algemene opties](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Veld | [Toepassingsgebied](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Algemeen | Als rewrites van de Webserver worden toegelaten, neemt het toelaten van deze het plaatsen de Code van de Opslag van de huidige mening in URL op. Opties: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Algemeen | (Voor Single-store-instellingen) Als er een verbroken koppeling op uw site staat, wordt het verkeer omgeleid naar de basis-URL in plaats van naar een pagina met het bericht &quot;404 Pagina niet gevonden&quot;. Opties: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Belangrijk!_**Gebruik geen automatische omleiding naar basis-URL voor instellingen in meerdere winkels. |
| [!UICONTROL Catalog media URL format] | Algemeen | Hiermee definieert u de URL-indeling die is toegewezen aan producten en categorieën. Opties: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definieert omgezette bestandsnaam als een unieke hash-waarde.<br />**[!UICONTROL Image optimization based on query parameters]** - Definities [optimalisering van afbeeldingen](../content-design/media-gallery-image-optimization.md) proces afhankelijk van vraagparameters. |

{style="table-layout:auto"}
