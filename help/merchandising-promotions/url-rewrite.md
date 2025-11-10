---
title: URL herschrijft
description: Meer informatie over het herschrijven van URL's vindt u met het gereedschap URL herschrijven van Commerce om URL's te wijzigen die zijn gekoppeld aan een product, categorie of CMS-pagina.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 2f2db4926ff92adfa27692eeca872c1765fd31d6
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# URL herschrijft

>[!TIP]
>
>Voor Adobe Commerce as a Cloud Service, zie de [ richtlijnen van SEO ](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) in de documentatie van de Storefront van Commerce

Met het gereedschap URL herschrijven kunt u elke URL wijzigen die is gekoppeld aan een product, categorie of CMS-pagina. Wanneer u een URL herschrijft, maakt Commerce automatisch een permanente omleiding (301), zodat koppelingen die naar de oude URL verwijzen, naar het nieuwe adres worden omgeleid.

>[!NOTE]
>
>Om URL bij te werken herschrijft voor veelvoudige of alle producten gelijktijdig, verwijs naar [ Veelvoudige URL herschrijft ](url-rewrite-product.md#multiple-url-rewrites).

>[!BEGINSHADEBOX  &quot;Het begrip herschrijft en herleidt&quot;]

De termijnen _herschrijven_ en _richten_ vaak worden gebruikt onderling verwisselbaar, maar zij zijn verschillende verrichtingen:

* **URL herschrijft** — Een server-zijproces dat intern één URL aan een andere in kaart brengt zonder te veranderen wat in de browser adresbar verschijnt. Wanneer een bezoeker een URL aanvraagt, verwerkt de server deze als een andere URL achter de scènes, maar de browser blijft de oorspronkelijke URL weergeven.

* **Redirect URL** - verzendt een reactie van HTTP naar browser die het opdraagt om aan een verschillende URL te navigeren. De adresbalk van de browser wordt bijgewerkt met de nieuwe URL. Omleidingen kunnen tijdelijk (302) of permanent (301) zijn.

>[!ENDSHADEBOX]

## De werking van het gereedschap Opnieuw schrijven

In Adobe Commerce wordt met het gereedschap URL herschrijven standaard een permanente omleiding (301) gemaakt om de waarde SEO te behouden wanneer u de URL-sleutel van een product, categorie of pagina wijzigt. Dit gedrag zorgt ervoor dat de bestaande verbindingen blijven werken en de rangschikkingen van de onderzoeksmotor worden gehandhaafd.

Door gebrek, [ automatische opnieuw richt URL ](url-redirect-product-automatic.md) wordt toegelaten voor uw opslag en **leidt tot Permanent Redirect voor oude URL** checkbox wordt geselecteerd onder het zeer belangrijke gebied URL van elk product.

{{url-rewrite-skip}}

![ de motoroptimalisering van het Onderzoek - creeer permanent opnieuw richt URL ](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## URL herschrijft demo

Bekijk de volgende video voor meer informatie over het beheren van herschrijvingen van URL&#39;s:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

## URL-herschrijvingen maken

Gebruik het gereedschap URL herschrijven om omleidingen voor producten en categorieën te maken en om aangepaste omleidingen voor elke pagina in uw winkel te maken. Wanneer de configuratie voor het herschrijven van URL wordt toegepast, worden bestaande koppelingen die naar de vorige URL verwijzen, naadloos omgeleid naar het nieuwe adres.

U kunt URL-herschrijvingen maken naar:

* Voeg hoogwaardige trefwoorden toe om de manier waarop het product wordt geïndexeerd door zoekprogramma&#39;s te verbeteren.

* Voeg aanvullende URL&#39;s toe voor een tijdelijke seizoenswijziging of een permanente wijziging.

* Voeg een geldig pad toe voor een pagina, inclusief CMS-inhoudspagina&#39;s. U kunt bijvoorbeeld een URL maken om een gebruikersvriendelijkere of SEO-vriendelijkere URL te maken op een systeem dat altijd naar producten en categorieën verwijst op basis van hun interne id.

De URL die u maakt, kan worden omgeleid naar bestaande categorieën of aangepaste pagina&#39;s zonder de sitestructuur te wijzigen. Hierdoor kunt u gemakkelijk memorabele URL&#39;s voor marketingcampagnes maken.

![ URL herschrijft net ](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce biedt de volgende URL-herschrijftypen aan:

* [Productherschrijvingen](url-rewrite-product.md)
* [Nieuwe categorie](url-rewrite-category.md)
* [CMS Page Rewrites](url-rewrite-cms-page.md)
* [Aangepaste herschrijvingen](url-rewrite-custom.md)

### Gebruik voorbeelden en gevallen

URL herschrijft wordt algemeen gebruikt in deze scenario&#39;s:

#### Een interne systeem-URL wijzigen in een SEO-vriendelijke URL

Commerce gebruikt intern op id gebaseerde URL&#39;s, maar u kunt SEO-vriendelijke URL&#39;s voor klanten maken:

**systeem URL (intern):**

     http://www.example.com/catalog/category/id/6

**Klantgerichte URL:**

     http://www.example.com/peripherals/keyboard.html

#### Productherbranding of URL-optimalisatie

Wanneer u de naam van een product wijzigt of de URL voor SEO wilt verbeteren, maakt u een omleiding om bestaande koppelingen te behouden:

**Oorspronkelijke URL:**

     http://www.example.com/peripherals/keyboard.html

**Nieuwe geoptimaliseerde URL:**

     http://www.example.com/ergonomic-keyboard.html

Met het gereedschap Herschrijven wordt automatisch een omleiding van 301 van de oude naar de nieuwe URL gemaakt, zodat klanten en zoekprogramma&#39;s naadloos naar de juiste pagina worden geleid.

#### Reclamepagina&#39;s

Maak tijdelijke of permanente aangepaste URL&#39;s voor marketingcampagnes:

**Promotional URLs:**

     http://www.example.com/all-on-sale.html
     http://www.example.com/save-now/spring-sale 

## Aanvullende configuratie voor URL-beheer

De volgende secties beschrijven hoe te om de Server van het Web te vormen herschrijft en canonieke URLs voor Commerce.

### Herschrijvingen webserver configureren

>[!NOTE]
>
>In deze sectie wordt het herschrijven van URL&#39;s op serverniveau beschreven. Dit wijkt af van de functie voor het herschrijven van URL&#39;s. Webserver herschrijft technische URL-opmaak (zoals verwijderen `index.php` ), terwijl het gereedschap URL herschrijven omleidingen voor inhoudswijzigingen beheert.

Het toelaten van de Server van het Web herschrijft maakt deel uit van de aanvankelijke opstelling van Commerce en typisch gevormd tijdens installatie. Wanneer deze optie is ingeschakeld, verwijdert de webserver (Apache of Nginx) automatisch de bestandsnaam `index.php` van URL&#39;s, waardoor er helderdere, meer SEO-vriendelijke adressen ontstaan.
In het volgende voorbeeld wordt getoond hoe URL&#39;s worden weergegeven met en zonder dat herschrijven van webservers is ingeschakeld:

**URL zonder de Server van het Web herschrijft**

     http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**URL met de Server van het Web herschrijft**

     http://www.yourdomain.com/magento/storeview/url-identifier

#### Herschrijvingen webserver in- of uitschakelen:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies **[!UICONTROL General]** in het linkerdeelvenster waar **[!UICONTROL Web]** wordt uitgevouwen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

   ![ Algemene configuratie - de optimalisering van de Webonderzoekmachine ](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Use Web Server Rewrites]** in op uw voorkeur.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Canonieke URL&#39;s opgeven

Voor SEO-doeleinden mag elke webpagina slechts één afzonderlijke URL hebben.

Als u één pagina hebt die toegankelijk is voor meerdere URL&#39;s of verschillende pagina&#39;s met vergelijkbare inhoud, beschouwt Google deze als dubbele versies van dezelfde pagina. Google kiest één URL als canonieke versie en kruipt dat, en alle andere URLs wordt beschouwd als dubbele URLs en minder vaak gekropen.

Als u Google niet uitdrukkelijk vertelt welke URL canonicaal is, maakt het de keus voor u, of zou kunnen hen allebei van gelijk gewicht overwegen. Dit kan leiden tot ongewenst gedrag en het risico bestaat dat de begroting ineffectief wordt verhoogd en dat er weinig zwarte vlekken worden gedistribueerd.

Afhankelijk van de manier waarop u uw website instelt, kunnen er meerdere versies van uw site in de index voorkomen, bijvoorbeeld:

     https://www.example.com 
     https://www.example.com/ 
     http://www.example.com
     https://example.com 
     https://www.example.com/index.html 

Om een canonieke pagina te specificeren, zie {de documentatie van het Onderzoek van 0} Google Centrale [.](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)
