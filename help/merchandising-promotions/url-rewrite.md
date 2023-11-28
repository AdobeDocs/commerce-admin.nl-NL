---
title: URL herschrijft
description: Meer informatie over URL-herschriften en het herschrijfgereedschap voor de handels-URL gebruiken om URL's te wijzigen die aan een product, categorie of CMS-pagina zijn gekoppeld.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL herschrijft

Met het gereedschap URL herschrijven kunt u elke URL wijzigen die is gekoppeld aan een product, categorie of CMS-pagina. Wanneer het herschrijven van kracht wordt, worden om het even welke verbindingen die aan vorige URL richten opnieuw gericht aan het nieuwe adres.

>[!NOTE]
>
>Als u URL-herschrijvingen voor meerdere of alle producten tegelijk wilt bijwerken, raadpleegt u [Meerdere URL&#39;s worden herschreven](url-rewrite-product.md#multiple-url-rewrites).

De voorwaarden _herschrijven_ en _omleiden_ worden vaak onderling verwisselbaar gebruikt, maar hebben betrekking op enigszins verschillende processen. Een URL wijzigt de manier waarop een URL in de browser wordt weergegeven. Een URL die omleidt werkt URL bij die op de server wordt opgeslagen. Een omleiding van een URL kan tijdelijk of permanent zijn. In uw winkel worden URL-herschriften en omleidingen gebruikt, zodat u gemakkelijk de URL-sleutel van een product, categorie of pagina kunt wijzigen en bestaande koppelingen kunt behouden.

Standaard, [automatische URL-omleidingen](url-redirect-product-automatic.md) zijn ingeschakeld voor uw winkel en de **Permanente omleiding maken voor oude URL** Schakel het selectievakje in onder het veld URL-sleutel van elk product.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Zoekmachine optimaliseren - permanente omleiding voor URL maken](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

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

Als u een canonieke pagina wilt opgeven, raadpleegt u [Google Search Central-documentatie](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## URL-herschrijvingen configureren

Het toelaten van de Server Apache van het Web maakt deel uit van de aanvankelijke opstelling van de Handel. De handel gebruikt routinematig URL herschrijft om het dossier te verwijderen - naam `index.php` die normaal gesproken in de URL net na de hoofdmap wordt weergegeven. Wanneer Herschrijvingen van de Server van het Web worden toegelaten, herschrijft het systeem elke URL om weg te gaan `index.php`. Het herschrijven verwijdert woorden die niets van waarde aan zoekmachines of klanten overbrengen, en heeft geen invloed op prestaties of plaatsrang.

URL zonder herschrijven van webserver

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL met herschrijven van webserver

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster waar **[!UICONTROL General]** wordt uitgebreid, kiest u **[!UICONTROL Web]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie.

   ![Algemene configuratie - optimalisatie van zoekprogramma&#39;s voor het web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Use Web Server Rewrites]** naar uw voorkeur.

1. Klik op **[!UICONTROL Save Config]**.

## URL-herschrijvingen maken

Met het gereedschap URL-herschrijven kunt u product- en categorieherschrijvingen maken en aangepaste herschrijvingen maken voor elke pagina in uw winkel. Wanneer het herschrijven van kracht wordt, worden om het even welke bestaande verbindingen die aan vorige URL richten naadloos opnieuw gericht aan het nieuwe adres.

URL herschrijft kan worden gebruikt om high-value sleutelwoorden toe te voegen om de manier te verbeteren het product door onderzoeksmotoren wordt geïndexeerd. U kunt ook Herschrijvingen gebruiken om extra URL&#39;s te maken voor een tijdelijke seizoenswijziging of permanente wijziging. Herschrijvingen kunnen worden gemaakt voor elk geldig pad, inclusief pagina&#39;s met CMS-inhoud. Intern verwijst het systeem altijd naar producten en categorieën op basis van hun id. Hoe vaak de URL verandert, de id blijft ongewijzigd. Hier volgen enkele manieren waarop u URL&#39;s kunt herschrijven:

Systeem-URL

    http://www.example.com/catalog/category/id/6

Oorspronkelijke URL

    http://www.example.com/peripherals/keyboard.html

URL omgeleid product

    http://www.example.com/ergonomic-keyboard.html

Aanvullende categorie-URL&#39;s

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL herschrijft raster](./assets/url-rewrites.png){width="700" zoomable="yes"}

De handel biedt deze URL aan herschrijft types:

* [Productherschrijvingen](url-rewrite-product.md)
* [Nieuwe categorie](url-rewrite-category.md)
* [CMS-pagina herschrijft](url-rewrite-cms-page.md)
* [Aangepaste herschrijvingen](url-rewrite-custom.md)

## URL herschrijft demo

Bekijk deze video voor meer informatie over het beheren van herschrijvingen van URL&#39;s:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
