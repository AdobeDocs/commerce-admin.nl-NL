---
title: URL herschrijft
description: Meer informatie over het herschrijven van URL's vindt u met het gereedschap URL herschrijven van Commerce om URL's te wijzigen die zijn gekoppeld aan een product, categorie of CMS-pagina.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# URL herschrijft

Met het gereedschap URL herschrijven kunt u elke URL wijzigen die is gekoppeld aan een product, categorie of CMS-pagina. Wanneer het herschrijven van kracht wordt, worden om het even welke verbindingen die aan vorige URL richten opnieuw gericht aan het nieuwe adres.

>[!NOTE]
>
>Om URL bij te werken herschrijft voor veelvoudige of alle producten gelijktijdig, verwijs naar [ Veelvoudige URL herschrijft ](url-rewrite-product.md#multiple-url-rewrites).

De termijnen _herschrijven_ en _richten_ vaak worden gebruikt onderling verwisselbaar, maar verwijzen naar lichtjes verschillende processen. Een URL wijzigt de manier waarop een URL in de browser wordt weergegeven. Een URL die omleidt werkt URL bij die op de server wordt opgeslagen. Een omleiding van een URL kan tijdelijk of permanent zijn. In uw winkel worden URL-herschriften en omleidingen gebruikt, zodat u gemakkelijk de URL-sleutel van een product, categorie of pagina kunt wijzigen en bestaande koppelingen kunt behouden.

Door gebrek, [ automatische opnieuw richt URL ](url-redirect-product-automatic.md) wordt toegelaten voor uw opslag en **leidt tot Permanent Redirect voor oude URL** checkbox wordt geselecteerd onder het zeer belangrijke gebied URL van elk product.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![ de motoroptimalisering van het Onderzoek - creeer permanent opnieuw richt URL ](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## Canonieke URL&#39;s

In het kader van SEO is het een goed idee dat elk van uw webpagina&#39;s slechts één afzonderlijke URL heeft.

Als u één pagina hebt die toegankelijk is voor meerdere URL&#39;s of verschillende pagina&#39;s met vergelijkbare inhoud, beschouwt Google deze als dubbele versies van dezelfde pagina. Google kiest één URL als canonieke versie en kruipt dat, en alle andere URLs wordt beschouwd als dubbele URLs en minder vaak gekropen.

Als u Google niet uitdrukkelijk vertelt welke URL canonicaal is, maakt het de keus voor u, of zou kunnen hen allebei van gelijk gewicht overwegen. Dit kan leiden tot ongewenst gedrag, en het risico lopen van een ineffectief kruipende begroting en lage verdeelde backkoppels.

Afhankelijk van de manier waarop u uw website instelt, kunnen er meerdere versies van uw site in de index voorkomen, waaronder:

     https://www.example.com 
     https://www.example.com/ 
     http://www.example.com
     https://example.com 
     https://www.example.com/index.html 

Om een canonieke pagina te specificeren, zie {de documentatie van het Onderzoek van 0} Google Centrale [&#128279;](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## URL-herschrijvingen configureren

Het inschakelen van Apache Rewrites voor webservers maakt deel uit van de eerste Commerce-configuratie. Commerce gebruikt gewoonlijk URL herschrijft om de bestandsnaam `index.php` te verwijderen die normaal gesproken in de URL net na de hoofdmap wordt weergegeven. Wanneer Web Server Rewrites wordt toegelaten, herschrijft het systeem elke URL om `index.php` weg te laten. Het herschrijven verwijdert woorden die niets van waarde aan zoekmachines of klanten overbrengen, en heeft geen invloed op prestaties of plaatsrang.

URL zonder herschrijven van webserver

     http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL met herschrijven van webserver

     http://www.yourdomain.com/magento/storeview/url-identifier

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies **[!UICONTROL Web]** in het linkerdeelvenster waar **[!UICONTROL General]** wordt uitgevouwen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

   ![ Algemene configuratie - de optimalisering van de Webonderzoekmachine ](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Use Web Server Rewrites]** in op uw voorkeur.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## URL-herschrijvingen maken

Met het gereedschap URL-herschrijven kunt u product- en categorieherschrijvingen maken en aangepaste herschrijvingen maken voor elke pagina in uw winkel. Wanneer het herschrijven van kracht wordt, worden om het even welke bestaande verbindingen die aan vorige URL richten naadloos opnieuw gericht aan het nieuwe adres.

URL herschrijft kan worden gebruikt om high-value sleutelwoorden toe te voegen om de manier te verbeteren het product door onderzoeksmotoren wordt geïndexeerd. U kunt ook Herschrijvingen gebruiken om extra URL&#39;s te maken voor een tijdelijke seizoenswijziging of permanente wijziging. Herschrijvingen kunnen worden gemaakt voor elk geldig pad, inclusief CMS-inhoudspagina&#39;s. Intern verwijst het systeem altijd naar producten en categorieën op basis van hun id. Hoe vaak de URL verandert, de id blijft ongewijzigd. Hier volgen enkele manieren waarop u URL&#39;s kunt herschrijven:

Systeem-URL

     http://www.example.com/catalog/category/id/6

Oorspronkelijke URL

     http://www.example.com/peripherals/keyboard.html

URL omgeleid product

     http://www.example.com/ergonomic-keyboard.html

Aanvullende categorie-URL&#39;s

     http://www.example.com/all-on-sale.html
     http://www.example.com/save-now/spring-sale 

![ URL herschrijft net ](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce biedt de volgende URL-herschrijftypen aan:

* [Productherschrijvingen](url-rewrite-product.md)
* [Nieuwe categorie](url-rewrite-category.md)
* [CMS Page Rewrites](url-rewrite-cms-page.md)
* [Aangepaste herschrijvingen](url-rewrite-custom.md)

## URL herschrijft demo

Bekijk deze video voor meer informatie over het beheren van herschrijvingen van URL&#39;s:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
