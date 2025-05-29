---
title: Zoekmachine optimaliseren
description: Meer informatie over SEO-gereedschappen (Search Engine Optimization, optimalisatie van zoekprogramma's) voor Commerce-sites en tips en trucs voor optimale SEO.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Overzicht van SEO

_de motoroptimalisering van het Onderzoek_ (SEO) is de praktijk van het verfijnen van de inhoud en de presentatie van een plaats om de manier te verbeteren de pagina&#39;s door onderzoeksmotoren worden geïndexeerd. Commerce bevat verschillende functies die uw huidige SEO-inspanningen ondersteunen.

>[!TIP]
>
>Voor Adobe Commerce as a Cloud Service, zie de [ richtlijnen van SEO ](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) in de documentatie van de Storefront van Commerce

## Metagegevens

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

Leer meer over het toevoegen van en het verbeteren van sleutelwoord-rijke [ meta-gegevens ](meta-data.md) voor uw plaats en opslag.

## Een sitemap gebruiken

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

A [ plaatskaart ](sitemap-xml.md) verbetert de manier dat uw opslag door onderzoeksmotoren wordt geïndexeerd, en ontworpen om pagina&#39;s te vinden die door Webkruiplers zouden kunnen worden over het hoofd gezien. U kunt een site-overzicht configureren om alle pagina&#39;s en afbeeldingen te indexeren.

## URL herschrijft

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

[ URL herschrijft ](url-rewrite.md) hulpmiddel laat u om het even welke URL veranderen die met een product, een categorie, of een pagina van CMS wordt geassocieerd.

## Zoekmachine-robots

De Commerce-configuratie bevat instellingen voor het genereren en beheren van instructies voor webcrawlers en bots die uw site indexeren. Als de aanvraag voor `robots.txt` Commerce bereikt (in plaats van een fysiek bestand), wordt deze dynamisch gerouteerd naar de robots-controller. De instructies zijn richtlijnen die door de meeste zoekmachines worden erkend en gevolgd.

Standaard bevat het bestand robots.txt dat door Commerce wordt gegenereerd, instructies voor webcrawler om te voorkomen dat bepaalde delen van de site worden geïndexeerd die bestanden bevatten die intern door het systeem worden gebruikt. U kunt de standaardinstellingen gebruiken of uw eigen aangepaste instructies definiëren voor iedereen of voor specifieke zoekprogramma&#39;s. Er zijn veel online artikelen die het onderwerp in detail onderzoeken.

### Voorbeeld van aangepaste instructies

**staat Volledige Toegang** toe

     gebruiker-agent:* 
     verlaat:

**ontkent Toegang tot Alle Omslagen**

     gebruiker-agent:* 
     Ontoegestaan: /

**StandaardInstructies**

     gebruiker-agent: *
     Ontoegestaan: /index.php/
     Ontoegestaan: /*?
     Ontoegestaan: /checkout/
     Ontoegestaan: /app/
     Ontoegestaan: /lib/
     Ontoegestaan: /*.php$ 
     Ontoegestaan: /pkginfo/
     Ontoegestaan: /report/
     Ontoegestaan: /var/
     Ontoegestaan: /catalog/
     Ontoegestaan: /customer/
     Afwijzen: /sendvriend/ 
     Ontoegestaan: /review/
     Ontoegestaan: /*SID= 

### Configureren `robots.txt`

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de **[!UICONTROL Global]** -configuratie in de eerste rij van het raster en klik op **[!UICONTROL Edit]** .

   ![ Globale ontwerpconfiguratie ](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Search Engine Robots]** sectie en doet het volgende:

   ![ configuratie van het Ontwerp - de robots van de onderzoeksmotor ](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Default Robots]** in op een van de volgende opties:

     | Optie | Beschrijving |
     |------|------------|
     | `INDEX, FOLLOW` | Instrueert webcrawlers de site te indexeren en later te controleren op wijzigingen. |
     | `NOINDEX, FOLLOW` | Hiermee geeft u webcrawlers de opdracht om de site niet te indexeren, maar om later te controleren op wijzigingen. |
     | `INDEX, NOFOLLOW` | Geeft webcrawlers de opdracht de site één keer te indexeren, maar later niet te controleren op wijzigingen. |
     | `NOINDEX, NOFOLLOW` | Geeft webcrawlers de opdracht te voorkomen dat de site wordt geïndexeerd en later niet opnieuw te controleren op wijzigingen. |

     {style="table-layout:auto"}

   - Voer zo nodig aangepaste instructies in het vak **[!UICONTROL Edit Custom instruction of robots.txt file]** in. Als een site bijvoorbeeld in ontwikkeling is, wilt u mogelijk de toegang tot alle mappen weigeren.

   - Klik op **[!UICONTROL Reset to Default]** om de standaardinstructies te herstellen.

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.
