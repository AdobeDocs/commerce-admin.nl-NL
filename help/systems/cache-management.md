---
title: Cachebeheer
description: Leer hoe u de tools voor cachebeheer gebruikt, die een eenvoudige manier zijn om de prestaties van uw site te verbeteren.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%

---

# Cachebeheer

Het cachebeheersysteem van Adobe Commerce en Magento Open Source biedt een eenvoudige manier om de prestaties van uw site te verbeteren. Wanneer een cache moet worden vernieuwd, wordt een melding weergegeven met een koppeling naar de [!UICONTROL Cache Management] -pagina om de vernieuwing te voltooien.

![ sparen productattribuut - update geheim voorgeheugenbericht ](./assets/product-attribute-save-msg-update-cache.png){width="500"}

Op de pagina _[!UICONTROL Cache Management]_&#x200B;ziet u de status van elke primaire cache en de bijbehorende tag. De grote knopen in de hoger-juiste hoek kunnen worden gebruikt om het geheime voorgeheugen, of de alle-inclusieve Opslag van het Geheime voorgeheugen te spoelen. Onder aan de pagina kunt u met extra knoppen de cache voor productafbeeldingen in de catalogus en de JavaScript/CSS-cache leegmaken.

>[!IMPORTANT]
>
>Wanneer entiteiten uit een catalogus worden gewijzigd, kan dit van invloed zijn op andere pagina&#39;s en meerdere cache tegelijk ongeldig maken. Wanneer u de pagina van het geheim voorgeheugenbeheer herziet, kon u ongeldige punten zien die vereisen verfrissen toen zij _&#x200B;**niet direct**&#x200B;_ werden uitgegeven. Deze validatie treedt bijvoorbeeld op wanneer u een product in de catalogus bewerkt dat aan een categorie is toegewezen, of wanneer u een regel voor een verwant product wijzigt.

Nadat u een cache hebt gewist, vernieuwt u altijd de browser om te controleren of u de meest recente bestanden kunt zien. Als u de Commerce-cache wist, wordt de cache van uw webbrowser niet gewist. Mogelijk moet u de cache van de browser wissen om de bijgewerkte inhoud te kunnen zien.

De extra technische informatie over Adobe Commerce caching is beschikbaar van het [ overzicht van het Geheime voorgeheugen ](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target="_blank"} in de _Gids van de Ontwikkeling van Commerce Frontend_.

Ga op een van de volgende manieren te werk om de pagina _[!UICONTROL Cache Management]_&#x200B;te openen:

- Klik op de koppeling **[!UICONTROL Cache Management]** in het bericht boven de werkruimte.
- Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![ het beheer van het Geheime voorgeheugen ](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Aanbevolen procedures voor het in cache plaatsen

Het opnieuw indexeren en in cache plaatsen heeft verschillende doeleinden in Commerce. [ indexen ](index-management.md) de informatie van het spoorgegevensbestand voor verhoogde onderzoeksprestaties, snellere gegevensherwinning voor opslagefronts, en meer. In cache worden geladen gegevens, afbeeldingen, indelingen en dergelijke opgeslagen voor betere prestaties bij het laden en openen van de opslagruimte.

- Maak de cache altijd leeg nadat u extensies/modules hebt geïnstalleerd. U kunt een of meer extensies installeren en vervolgens de cache leegmaken.
- Maak de cache leeg nadat u Commerce hebt geïnstalleerd. Voor nieuwe installaties moet u ook opnieuw indexeren.
- Maak de cache leeg nadat u de upgrade hebt uitgevoerd van de ene versie van Open Source of Commerce naar de andere.
- Houd bij het spoelen rekening met het type cache en het plannen van het spoelen tijdens perioden zonder pieken. Kies bijvoorbeeld een tijdstip waarop weinig klanten de site gebruiken, zoals &#39;s nachts of &#39;s morgens. Het wissen van cachetypen tijdens piekvraag kan de belasting van de beheerder verhogen en de site doen afnemen totdat de bewerking is voltooid.
- Wanneer [ het opnieuw indexeren ](index-management.md), moet u niet het geheime voorgeheugen ontruimen.

## Bronnen voor Cachebeheer

U kunt toegang tot specifieke acties van het geheim voorgeheugenonderhoud aan gebruikers door rol, met inbegrip van opties aan mening, knevel, en spoelgeheime voorgeheugens toewijzen. Adobe raadt u aan alleen handelingen op het niveau van beheerders uit te schakelen. Het bieden van toegang tot alle functies voor cachebeheer kan van invloed zijn op de prestaties van uw winkel.

![ de middelen van de Rol - geheim voorgeheugenbeheer ](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Voor informatie over het toewijzen van middelen om toegang voor Admin gebruikersrekeningen te verlenen, zie {de middelen van de Rol 0} [&#128279;](permissions-user-roles.md#role-resources).  De volgende middelen controleren toegang tot de hulpmiddelen van het geheim voorgeheugenbeheer:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Specifieke cache vernieuwen

1. Voor elke cache die moet worden vernieuwd, schakelt u het selectievakje aan het begin van de rij in.

1. Stel **[!UICONTROL Actions]** in op `Refresh` en klik op **[!UICONTROL Submit]** .

## Vernieuwen van massaactie uitvoeren

1. Als u een groep caches wilt selecteren, stelt u **[!UICONTROL Mass Actions]** in op een van de volgende opties:

   - `Select All`
   - `Select Visible`

1. Schakel het selectievakje in voor elke cache die u wilt vernieuwen.

1. Stel **[!UICONTROL Actions]** in op `Refresh` en klik op **[!UICONTROL Submit]** .

## De cache van de productafbeelding leegmaken

1. Klik onder _[!UICONTROL Additional Cache Management]_&#x200B;op **[!UICONTROL Flush Catalog Images Cache]**&#x200B;om vooraf gegenereerde afbeeldingsbestanden voor het product te wissen.

   Het `Image cache was cleaned` -bericht wordt boven in de werkruimte weergegeven.

1. Wis de cache van uw browser.

## De JavaScript/CSS-cache leegmaken

1. Wis onder _[!UICONTROL Additional Cache Management]_&#x200B;Javascript- en CSS-bestanden die zijn samengevoegd tot één bestand door op **[!UICONTROL Flush JavaScript/CSS Cache]**&#x200B;te klikken.

   Het `The JavaScript/CSS cache has been cleaned` -bericht wordt boven in de werkruimte weergegeven.

1. Wis de cache van uw browser.

## Uitlijnen met gebruik van de opdrachtregel

Systeembeheerders en -ontwikkelaars met toegang tot de Commerce-toepassingsserver kunnen de cache- en cachemonfiguratie ook vanaf de opdrachtregel beheren met behulp van de Commerce CLI. Zie [ het geheime voorgeheugen ](https://experienceleague.adobe.com/nl/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target="_blank"} in de _Gids van de Configuratie_ leiden.

## Besturingselementen

| Besturing | Beschrijving |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Selecteert checkbox van veelvoudige geheime voorgeheugens. Opties: <br/>**[!UICONTROL Select All]**— Selecteert het selectievakje van alle cache.<br/>**&#x200B; Unselect allen &#x200B;**— ontruimt checkbox van alle geheime voorgeheugens.<br/>**[!UICONTROL Select Visible]** — Selecteert het selectievakje van alle zichtbare cache. <br/>**[!UICONTROL Unselect Visible]**— Wist het selectievakje van alle zichtbare cache. |
| [!UICONTROL Actions] | Hiermee bepaalt u de actie die op alle geselecteerde caches moet worden toegepast. Opties: <br/>**[!UICONTROL Enable]**— Hiermee schakelt u alle geselecteerde caches in.<br/>**[!UICONTROL Disable]** — Schakelt alle geselecteerde caches uit. <br/>**[!UICONTROL Refresh]**— Hiermee vernieuwt u alle geselecteerde caches. |
| [!UICONTROL Submit] | Hiermee past u de handeling toe op alle geselecteerde caches. |

{style="table-layout:auto"}

### Knoppen

| Knop | Beschrijving |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Hiermee worden alle items in de standaard Commerce-cache (`var/cache`) verwijderd volgens de bijbehorende Commerce-tags. |
| [!UICONTROL Flush Cache Storage] | Hiermee worden alle items uit het cachegeheugen verwijderd, ongeacht de Commerce-tag. Als uw systeem een alternatieve cachelocatie gebruikt, worden alle cachebestanden die door andere toepassingen worden gebruikt, tijdens het proces verwijderd. |
| [!UICONTROL Flush Catalog Images Cache] | Hiermee verwijdert u alle automatisch gewijzigde en van een watermerk voorziene catalogusafbeeldingen die zijn opgeslagen in `media/catalog/product/cache` . Als onlangs geüploade afbeeldingen niet in de catalogus worden weergegeven, probeert u de catalogus te spoelen en de browser te vernieuwen. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Hiermee verwijdert u de samengevoegde kopie van JavaScript- en CSS-bestanden uit de cache. Als recente wijzigingen in de stijlpagina of JavaScript niet worden doorgevoerd in de winkel, probeert u de JavaScript/CSS-cache te leegmaken en de browser te vernieuwen. |
| [!UICONTROL Flush Static Files Cache] | Verwijdert vooraf verwerkte meningsdossiers en statische dossiers. |

{style="table-layout:auto"}

### Cursussen

De pagina [!UICONTROL Cache Management] bevat een lijst met de cachetypen die u kunt beheren vanuit de beheerder met hun huidige status. In deze sectie worden de standaardcachetypen beschreven die door Adobe Commerce worden ondersteund. De _Cachetag van het Geheime voorgeheugen_ en _identiteitskaart van het Geheime voorgeheugen_ kolommen beschrijven waarden die in de de toepassingscode van Commerce worden gebruikt:

- `cache_type_id` definieert de unieke id voor een cachetype.

- `%CACHE_TYPE_TAG%` definieert de unieke tag die moet worden gebruikt in cache-typeschema.

Ontwikkelaars en systeemintegrators gebruiken deze waarden om caching te configureren en te beheren tijdens het aanpassen of integreren met Adobe Commerce, bijvoorbeeld bij het ontwikkelen van integratie met GraphQL API&#39;s.

[!BADGE &#x200B; PaaS slechts &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} `cache_type_id` wordt ook gebruikt voor geheim voorgeheugenbeheer van de lijn van het het bevelbevel van de toepassingsserver gebruikend Commerce CLI. ` bin/magento cache:status config` geeft bijvoorbeeld de huidige status van de configuratiecache weer.

>[!NOTE]
>
>Ontwikkelaars en systeemintegrators kunnen het Commerce-cachebeheersysteem aanpassen en uitbreiden om aangepaste modules en integratie te ondersteunen. Voor details, zie [ Caching ](https://experienceleague.adobe.com/nl/docs/commerce-operations/configuration-guide/cache/caching-overview) in het voorgeheugen onderbrengen in de _Gids van de Configuratie van Adobe Commerce_.

<!-- prettier-ignore -->

#### Cachelijst met details

| Cache | Beschrijving | Cachetag | Cache-id |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce verzamelt de configuratie van XML van alle modules, voegt het samen, en bewaart het samengevoegde resultaat aan het geheime voorgeheugen.<br>**[!UICONTROL System]**- `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br> Deze cache bevat ook opslagspecifieke instellingen die zijn opgeslagen in het bestandssysteem en de database. Reinig of verwijder dit cachetype na het wijzigen van configuratiedossiers. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Gecompileerde paginalay-outs, dat wil zeggen de lay-outcomponenten van alle componenten. Reinig of verwijder dit cachetype na het wijzigen van lay-outbestanden. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | HTML-paginafragmenten per blok. Reinig of verwijder dit cachetype na het wijzigen van de meningslaag. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Gegevensbestanden van de inzameling die de resultaten van gegevensbestandvragen opslaan. Indien nodig, ontruimt Commerce automatisch dit geheime voorgeheugen, maar de derdeontwikkelaars kunnen om het even welk segment van het geheime voorgeheugen plaatsen. Reinig of verwijder dit cachetype als in uw aangepaste module logica wordt gebruikt die cachemarangen oplevert die Commerce niet kan opschonen. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Wist de weerspiegelingsgegevens van de API interface, die typisch tijdens runtime wordt geproduceerd. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Databaseschema Indien nodig, ontruimt Commerce automatisch dit geheime voorgeheugen, maar de derdeontwikkelaars kunnen om het even welk segment van het geheime voorgeheugen plaatsen. Reinig of verwijder dit cachetype nadat u douaneveranderingen in het gegevensbestandschema aanbrengt. (Dit zijn dus updates die Commerce niet zelf maakt.) Één manier om het gegevensbestandschema automatisch bij te werken gebruikt magento opstelling :db-schema: verbeteringsbevel. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Resultaten van codecompilatie. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Hiermee worden reacties op webhaakaanvragen vastgezet. Voor meer informatie, zie de [ Gids van Webhooks ](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) in de de ontwikkelaarsdocumentatie van Commerce. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Hiermee wordt de declaratie van entiteitstypen in de cache opgenomen voor metagegevens die betrekking hebben op kenmerken van kenmerk Entiteit Attribute Value (EAV). Kenmerken zijn winkellabels, koppelingen naar gerelateerde PHP-code, kenmerkrendering, zoekinstellingen enzovoort. U hoeft dit type cache gewoonlijk niet op te schonen of te leegmaken. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Tijdelijke meldingen die worden weergegeven in de gebruikersinterface. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Caches the results from GraphQL query resolvers for customer, CMS page, CMS block, and product media gallery entities. Laat deze cache ingeschakeld om de GraphQL-prestaties te verbeteren. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Integratieconfiguratiebestand. Maak deze cache leeg of maak deze leeg nadat u integraties hebt gewijzigd of toegevoegd. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Configuratie van gecompileerde integratie-API&#39;s voor winkelintegratie. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | Kies deze optie om aanpassingen door te voeren bij de beheerder. Zie [ Configuratie Admin en het testen ](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) in de _Gids van Admin UI van SDK_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Volledige pagina in cache plaatsen. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Index van doelregel | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | De Web API-structuur in cache plaatsen. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Vertaalbestanden. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## In cache plaatsen van volledige pagina&#39;s

Adobe Commerce en Magento Open Source maken gebruik van caching op de server van volledige pagina&#39;s om snel categorie-, product- en CMS-pagina&#39;s weer te geven. Het in cache plaatsen van volledige pagina&#39;s verbetert de responstijd en vermindert de belasting op de server. Zonder caching, zou elke pagina blokken van code moeten in werking stellen en informatie van het gegevensbestand terugwinnen. Als plaatsing op een volledige pagina is ingeschakeld, kan een volledig gegenereerde pagina echter rechtstreeks vanuit de cache worden gelezen.

>[!NOTE]
>
>Het wordt geadviseerd dat [ het Geheime voorgeheugen van de Varnish ](https://varnish-cache.org/){:target="_blank"} slechts in een productiemilieu wordt gebruikt.

Inhoud in cache kan worden gebruikt om de aanvragen van vergelijkbare typen bezoeken te verwerken. Hierdoor kunnen pagina&#39;s die aan een bezoeker worden getoond afwijken van pagina&#39;s die aan een klant worden getoond. Voor het in cache plaatsen is elk bezoek een van de volgende drie soorten:

- `Non-sessioned` - Tijdens een niet-sessioned bezoek, bekijkt de verkoopster pagina&#39;s, maar wisselt niet met de opslag. Het systeem plaatst de inhoud van elke weergegeven pagina in cache en levert deze aan andere niet-sessioned kopers.
- `Sessioned` - Tijdens een sessiebezoek wordt aan kopers die met de winkel werken, een sessie-id toegewezen. Interacties omvatten activiteiten zoals het vergelijken van producten of het toevoegen van producten aan het winkelwagentje. Pagina&#39;s in de cache die tijdens de sessie worden gegenereerd, worden tijdens de sessie alleen door die winkelier gebruikt.
- `Customer` - Er worden klantsessies gemaakt voor klanten die zich met hun geregistreerde account aanmelden en winkelen. Tijdens de sessie kunnen klanten speciale aanbiedingen, promoties en prijzen krijgen op basis van hun toegewezen klantengroep.

Voor technische informatie, zie [ vormen en gebruiken Vervagen ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html?lang=nl-NL){:target="_blank"} en [ Gebruik Redis voor de pagina van Commerce en het gebrek geheime voorgeheugen ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html?lang=nl-NL){:target="_blank"} in de _Gids van de Configuratie_.

**_om het full-page geheime voorgeheugen te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Full Page Cache]** sectie uit.

   ![ Geavanceerde configuratie - volledig paginacache ](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Caching Application]** in op een van de volgende opties:

   - `Built-in Application`
   - `Varnish Caching`

1. Voer de **[!UICONTROL TTL for public content]** in om de time-out voor de paginacache in te stellen. (De standaardwaarde is `86400` )

1. Om het maximumaantal [ lay-outhandvatten ](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) te specificeren om op het [`{BASE-URL}/page_cache/block/esi` ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html?lang=nl-NL) eindpunt van HTTP te verwerken, ga **[!UICONTROL Handles param size]** in. Het beperken van de grootte kan de veiligheid en de prestaties verbeteren. (De standaardwaarde is `100` )

1. Als u Varnish gebruikt, voert u de sectie **[!UICONTROL Varnish Configuration]** als volgt in:

   - **[!UICONTROL Access list]** - ga de IP adressen in die de configuratie van Varnish kunnen zuiveren om een config dossier te produceren. Scheid meerdere items met een komma. De standaardwaarde is `localhost` .

   - **[!UICONTROL Backend host]** - ga het IP adres van de achterste deelgastheer in die config dossiers produceert. De standaardwaarde is `localhost` .

   - **[!UICONTROL Backend port]** - Identificeer de achterste haven die wordt gebruikt om configuratiedossiers te produceren. De standaardwaarde is: `8080` .

   - **[!UICONTROL Grace period]** - Geef het aantal seconden op dat u als respijtperiode wilt gebruiken om configuratiebestanden te genereren. Zie [ Geavanceerde configuratie van Varnish ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html?lang=nl-NL) in de _Gids van de Configuratie_.

   - Als u de configuratie als een `varnish.vcl` -bestand wilt exporteren, klikt u op de knop voor de versie van Vaag die u gebruikt.

   ![ Geavanceerde configuratie - de volledige vernis van het paginacachegeheugen ](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
