---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL General] &gt; [!UICONTROL Web] pagina van de Commerce Admin.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1795'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Algemene opties](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Veld | Toepassingsgebied | Beschrijving |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Algemeen | Als de Server van het Web Herschrijft wordt toegelaten, neemt de Code van de Opslag van de huidige mening in URL op. Opties: `Yes` / `No`. <br />Wanneer dit veld is ingesteld op `Yes`, moet u opslagcodes opnemen in de URL&#39;s van uw browser om ervoor te zorgen dat herschrijvingen van URL&#39;s correct worden toegewezen en dat alle pagina&#39;s correct worden geopend. Dit vermijdt _404 pagina niet gevonden_ fouten. |
| [!UICONTROL Auto-redirect to Base URL] | Winkelweergave | (Voor instellingen in één winkel) Als er een verbroken koppeling op uw site staat, stuurt u het verkeer door naar de basis-URL in plaats van naar een pagina met het bericht &#39;404 Pagina niet gevonden&#39;. Opties:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Belangrijk:_**Gebruik geen automatische omleiding naar basis-URL voor instellingen in meerdere winkels. |
| [!UICONTROL Catalog media URL format] | Algemeen | Definieert de [URL-indeling](../../catalog/catalog-urls.md) aan producten en categorieën worden toegewezen. Opties: unieke hash per afbeeldingsvariant (modus Verouderd) definieert omgezette bestandsnaam als een unieke hash-waarde. De optimalisering van het beeld die op vraagparameters wordt gebaseerd bepaalt [optimalisering van afbeeldingen](../../content-design/media-gallery-image-optimization.md) proces afhankelijk van vraagparameters. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > Optimalisatie van zoekmachines](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://docs.magento.com/user-guide/marketing/url-rewrite.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Winkelweergave | Op PHP gebaseerde systemen bevatten doorgaans een bestand dat een naam krijgt `index.php` in de hoofdmap. Standaard wordt de bestandsnaam in de URL net na de naam van de hoofdmap weergegeven. Als deze optie is ingeschakeld, wordt het systeem weggelaten `index.php` via de URL. Deze bruikbaarheids beste praktijken maken elke URL beknopter, en hebben geen invloed op prestaties of plaatscijfer. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > Basis-URL&#39;s](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Base URL] | Winkelweergave | Het volledige adres van de de wortelomslag van de Handel die niet over een gecodeerd (SSL) kanaal loopt. De URL moet eindigen met een slash. |
| [!UICONTROL Base Link URL] | Winkelweergave | Een opmaakcode die wordt gebruikt als plaatsaanduiding voor de basis-URL. |
| [!UICONTROL Base URL for Static View Files] | Winkelweergave | Een pad dat wijst naar de locatie van statische bestanden die door het thema worden gebruikt, zoals css, fonts, afbeeldingen en JavaScript. Een tijdelijke aanduiding wordt gebruikt om de basis-URL weer te geven. Als uw installatie van de Handel veelvoudige plaatsen met de zelfde omslagstructuur heeft, kunt u een verschillende omslag voor elke plaats hebben. Stel het configuratiebereik in op de juiste site voordat u de basis-URL voor statische weergavebestanden invoert. U kunt ook een map buiten de installatie van Commerce opgeven. |
| [!UICONTROL Base URL for User Media Files] | Winkelweergave | Een pad dat wijst naar de locatie van catalogusafbeeldingen en andere mediabestanden. Een tijdelijke aanduiding wordt gebruikt om de basis-URL weer te geven. Als uw installatie van de Handel veelvoudige plaatsen met de zelfde omslagstructuur heeft, kunt u een verschillende media omslag voor elk hebben. Hierdoor kunt u een back-up maken van elke mediamap en deze afzonderlijk terugdraaien. U kunt ook een mediamap buiten de installatie van de Commerce opgeven. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > Basis-URL&#39;s (veilig)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Winkelweergave | Het volledige adres van de de wortelomslag van de Handel die met gecodeerd veilig (SSL/TLS) protocol wordt geleverd. De URL moet eindigen met een slash. |
| [!UICONTROL Secure Base Link URL] | Winkelweergave | Een opmaakcode die wordt gebruikt als plaatsaanduiding voor de basis-URL die via een beveiligd kanaal wordt uitgevoerd. |
| [!UICONTROL Secure Base URL for Static View Files] | Winkelweergave | Een opmaakcode die verwijst naar de locatie van statische bestanden, zoals CSS, lettertypen, afbeeldingen en JavaScript, die door het thema worden gebruikt. De bestanden kunnen zich op een onbeveiligd of beveiligd kanaal bevinden. Als uw installatie van de Handel veelvoudige plaatsen met de zelfde omslagstructuur heeft, kunt u een verschillende omslag voor elke plaats hebben. Stel het configuratiebereik in op de juiste site voordat u de basis-URL voor statische weergavebestanden invoert. U kunt ook een map buiten de installatie van Commerce opgeven. |
| [!UICONTROL Secure Base URL for User Media Files] | Winkelweergave | Een pad dat wijst naar de locatie van catalogusafbeeldingen en andere mediabestanden. De bestanden kunnen zich op een onbeveiligd of beveiligd kanaal bevinden. Een tijdelijke aanduiding wordt gebruikt om de basis-URL weer te geven. Als uw installatie van de Handel veelvoudige plaatsen met de zelfde omslagstructuur heeft, kunt u een verschillende media omslag voor elk hebben. Hierdoor kunt u een back-up maken van elke mediamap en deze afzonderlijk terugdraaien. U kunt ook een mediamap buiten de installatie van de Commerce opgeven. |
| [!UICONTROL Use Secure URLs on Storefront] | Winkelweergave | Als uw domein een veiligheidscertificaat heeft, kunt u verkiezen om de storefront, met of zonder SSL encryptie in werking te stellen. Opties:<br />**`Yes`**- URL&#39;s opslaan begint met `https` om aan te geven dat de pagina wordt geleverd met een gecodeerd, beveiligd protocol.<br />**`No`** - URL&#39;s opslaan begint met `http` om aan te geven dat de pagina zonder beveiligd protocol wordt geleverd. |
| [!UICONTROL Use Secure URLs in Admin] | Algemeen | Als uw domein een beveiligingscertificaat heeft, kunt u de opslagbeheerder uitvoeren, met of zonder SSL-codering. Opties: <br />**`Yes`**- URL&#39;s voor beheer beginnen met `https` om aan te geven dat de pagina wordt geleverd met een gecodeerd, beveiligd protocol.<br />**`No`** - URL&#39;s voor beheer beginnen met `http` om aan te geven dat de pagina zonder beveiligd protocol wordt geleverd.<br /> Wanneer beveiligde URL&#39;s zijn ingeschakeld voor zowel de winkel als de beheerder, worden twee extra velden weergegeven om in te schakelen en te configureren `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Winkelweergave | Indien ingeschakeld, [`HSTS`][1] biedt een mate van beveiliging tegen aanvallen van &#39;man in het midden&#39; en voorkomt dat gebruikers het bericht &#39;invalid certificate&#39; overschrijven. Opties: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Winkelweergave | Indien ingeschakeld, wordt onbeveiligd geconverteerd (`HTTP`) van de browser ontvangen verzoeken aan de beveiligde (`HTTPS`). Opties: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Algemeen | Hiermee geeft u de `offloader_header` waarde in uw serverconfiguratie om het protocol tussen de client en het taakverdelingsmechanisme te identificeren. De meeste installaties van de Handel gebruiken de standaardwaarde, `X-Forwarded-Proto` (XFP) om het protocol als één van beide te identificeren `HTTP` of `HTTPS`. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > Standaardpagina&#39;s](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://docs.magento.com/user-guide/cms/pages-default.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Winkelweergave | Geeft de bestemmingspagina aan die aan de basis-URL is gekoppeld. Deze wordt standaard ingesteld op &quot;cms&quot; om een pagina van het CMS (Commerce Content Management System) aan te geven. U kunt ook een ander type bestemmingspagina gebruiken, zoals een blog. Als bijvoorbeeld een blog op de server is geïnstalleerd op `magento/blog`, kunt u de naam van de map &quot;blog&quot; invoeren als een relatief pad naar de paginaselectie. |
| [!UICONTROL CMS Home Page] | Winkelweergave | Als u de homepage voor de winkel wilt kiezen, selecteert u gewoon de CMS-pagina in de lijst. Standaard wordt op de CMS-startpagina de volledige selectie van CMS-pagina&#39;s weergegeven die beschikbaar zijn voor uw winkel. |
| [!UICONTROL Default No-route URL] | Winkelweergave | Bevat de URL van de standaardpagina die u wilt weergeven als een `404 Page not Found` fout treedt op. De standaardwaarde is `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Winkelweergave | Hiermee wordt een specifieke CMS-pagina aangegeven die moet worden weergegeven wanneer een fout van 404 pagina niet gevonden optreedt. De standaardpagina is 404 Niet gevonden. |
| [!UICONTROL CMS No Cookies Page] | Winkelweergave | Hiermee wordt een specifieke CMS-pagina aangegeven die wordt weergegeven wanneer cookies niet zijn ingeschakeld voor de browser. Op de pagina wordt uitgelegd waarom cookies worden gebruikt en hoe u deze voor elke browser inschakelt. De standaardpagina is Enable Cookies. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Winkelweergave | Hiermee wordt bepaald of een breedbandtrail op alle CMS-pagina&#39;s in de catalogus wordt weergegeven. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Standaardindelingen](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://docs.magento.com/user-guide/design/page-layout.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Algemeen | Hiermee bepaalt u de [layout](../../content-design/page-layout.md) die standaard wordt gebruikt voor productpagina&#39;s. Opties: <br/>**`No layout updates`**- Standaard zijn lay-outupdates niet beschikbaar voor productpagina&#39;s.<br/>**`Empty`** - Standaard wordt een lege indeling gebruikt voor productpagina&#39;s. <br/>**`1 column`**- Standaard wordt voor productpagina&#39;s één kolomindeling gebruikt.<br/>**`2 columns with left bar`** - Standaard wordt voor productpagina&#39;s een lay-out van twee kolommen gebruikt, waarbij de zijbalk aan de linkerkant wordt weergegeven. <br/>**`2 columns with right bar`**- Voor productpagina&#39;s wordt standaard een lay-out van twee kolommen gebruikt, met de zijbalk aan de rechterkant.<br/>**`3 columns`** - Standaard wordt voor productpagina&#39;s een lay-out van drie kolommen gebruikt met zijbalken links en rechts.<br/>**`Page -- Full Width`**- (Vereist [!DNL Page Builder]) Standaard wordt de indeling Pagina — volledige breedte gebruikt voor productpagina&#39;s.<br/>**`Category - Full Width`** - (Vereist [!DNL Page Builder]) Standaard wordt de indeling Categorie - Volledige breedte gebruikt voor productpagina&#39;s. <br/>**`Product - Full Width`**- (Vereist [!DNL Page Builder]) Standaard wordt de indeling Product - Volledige breedte gebruikt voor productpagina&#39;s. |
| [!UICONTROL Default Category Layout] | Algemeen | Hiermee bepaalt u de [layout](../../content-design/page-layout.md) die standaard wordt gebruikt voor categoriepagina&#39;s. Opties: <br/>**`No layout updates`**- Standaard zijn indelingsupdates niet beschikbaar voor categoriepagina&#39;s.<br/>**`Empty`** - Standaard wordt een lege indeling gebruikt voor categoriepagina&#39;s. <br/>**`1 column`**- Standaard wordt voor categoriepagina&#39;s één kolomindeling gebruikt.<br/>**`2 columns with left bar`** - Voor categoriepagina&#39;s wordt standaard een lay-out van twee kolommen gebruikt, waarbij de zijbalk aan de linkerkant wordt weergegeven. <br/>**`2 columns with right bar`**- Voor categoriepagina&#39;s wordt standaard een lay-out van twee kolommen gebruikt, waarbij de zijbalk aan de rechterkant is ingeschakeld.<br/>**`3 columns`** - Standaard wordt een indeling met drie kolommen gebruikt met zijbalken links en rechts voor categoriepagina&#39;s.<br/>**`Page - Full Width`**- (Vereist [!DNL Page Builder]) Standaard wordt de indeling Pagina - volledige breedte gebruikt voor categoriepagina&#39;s.<br/>**`Category - Full Width`** - (Vereist [!DNL Page Builder]) Standaard wordt de indeling Categorie - Volledige breedte gebruikt voor categoriepagina&#39;s. <br/>**`Product - Full Width`**- (Vereist [!DNL Page Builder]) Standaard wordt de indeling Product - Volledige breedte gebruikt voor categoriepagina&#39;s. |
| Standaardpagina-indeling | Algemeen | Hiermee bepaalt u de [layout](../../content-design/page-layout.md) die standaard wordt gebruikt voor CMS-pagina&#39;s. Opties: <br/>**`No layout updates`**- Standaard zijn lay-outupdates niet beschikbaar voor CMS-pagina&#39;s.<br/>**`Empty`** - Voor CMS-pagina&#39;s wordt standaard een lege indeling gebruikt. <br/>**`1 column`**- Standaard wordt voor CMS-pagina&#39;s één kolomindeling gebruikt.<br/>**`2 columns with left bar`** - Voor CMS-pagina&#39;s wordt standaard een lay-out van twee kolommen gebruikt met de zijbalk links.<br/>**`2 columns with right bar`**- Voor CMS-pagina&#39;s wordt standaard een lay-out van twee kolommen gebruikt met de zijbalk rechts.<br/>**`3 columns`** - Voor CMS-pagina&#39;s wordt standaard een lay-out van drie kolommen gebruikt met zijbalken links en rechts.<br/>**`Page - Full Width`**- (Vereist [!UICONTROL Page Builder]) Standaard wordt de indeling Pagina - volledige breedte gebruikt voor CMS-pagina&#39;s.<br/>**`Category - Full Width`** - (Vereist [!UICONTROL Page Builder]) Standaard wordt de indeling Categorie - volledige breedte gebruikt voor CMS-pagina&#39;s. <br/>**`Product - Full Width`**- (Vereist [!DNL Page Builder]) Standaard wordt de indeling Product - Volledige breedte gebruikt voor CMS-pagina&#39;s. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > Standaardinstellingen voor cookie](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://docs.magento.com/user-guide/stores/compliance-cookie-law.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Winkelweergave | Hiermee bepaalt u hoe lang een cookie kan bestaan voordat deze automatisch wordt verwijderd. Standaardwaarde is 3600 seconden (1 uur) |
| [!UICONTROL Cookie Path] | Winkelweergave | Hiermee geeft u de mappen op de server op waarin de cookies van de Handel kunnen worden gebruikt. Als u de cookies van de Handel overal in de installatie beschikbaar wilt maken, stelt u het Koekjespad in op één schuine streep: `/`. Deze waarde kan alleen het cookiepad bevatten, en **_kan_** bevat andere cookieparameters. |
| [!UICONTROL Cookie Domain] | Winkelweergave | Hiermee bepaalt u of de cookies van de Handel beschikbaar zijn voor subdomeinen. Bijvoorbeeld om `mysubdomain`.domain.com, ga de naam van uw domein met een periode aan het begin in, zoals `.domain.com`. Deze waarde kan alleen het cookiedomein bevatten, en **_kan_** bevat andere cookieparameters. |
| [!UICONTROL Use HTTP Only] | Winkelweergave | Bepaalt of de Koekjes van de Handel slechts over een onbeveiligd kanaal (http) kunnen worden gebruikt, of kunnen ook over een gecodeerd kanaal (https) worden gebruikt. Opties: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Website | Hiermee wordt bepaald of de beperkingsmodus voor cookies is ingeschakeld. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > Sessievalidering](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://docs.magento.com/user-guide/stores/security-session-validation.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Algemeen | Verifieert dat het IP Adres van een verzoek aanpast `$_SESSION` gegevens. De sessie wordt beëindigd als een ander IP-adres wordt gedetecteerd. Opties: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Algemeen | Verifieert inkomende volmachtsgegevens en controleert dat het volmachtsadres van een verzoek aanpast `$_SESSION` gegevens. De sessie wordt beëindigd als een ander proxyadres wordt gevonden. Opties: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Algemeen | Verifieert uitgaande volmachtsgegevens en controleert dat door:sturen-voor adres van een verzoek aanpast  `$_SESSION` gegevens. De sessie wordt beëindigd als een ander doorgestuurd adres wordt gedetecteerd. Opties: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Algemeen | `USER_AGENT` verwijst naar de browser of het apparaat dat wordt gebruikt om toegang te krijgen tot de website. Hierbij wordt gecontroleerd of de naam en versie van de browser en het besturingssysteem overeenkomen met `$_SESSION` gegevens. De sessie wordt beëindigd als een andere gebruikersagent wordt gedetecteerd tussen aanvragen in dezelfde sessie. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > Detectie van browsermogelijkheden](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://docs.magento.com/user-guide/stores/security-browser-capabilities-detection.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Winkelweergave | Als cookies door de browser worden uitgeschakeld, wordt deze automatisch doorgestuurd naar de pagina CMS No Cookies. Opties: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Winkelweergave | Als JavaScript door de browser is uitgeschakeld, wordt een bericht weergegeven waarin de gebruiker wordt gevraagd om JavaScript-opties in te schakelen: `Yes` / `No` (kan worden uitgeschakeld) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Winkelweergave | Hiermee wordt een bericht weergegeven als de lokale cache is uitgeschakeld. Opties: `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
