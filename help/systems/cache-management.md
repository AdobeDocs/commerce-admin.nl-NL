---
title: Cachebeheer
description: Leer hoe u de tools voor cachebeheer gebruikt, die een eenvoudige manier zijn om de prestaties van uw site te verbeteren.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# Cachebeheer

Het cachebeheersysteem van Adobe Commerce en Magento Open Source biedt een eenvoudige manier om de prestaties van uw site te verbeteren. Wanneer een cache moet worden vernieuwd, verschijnt boven in de werkruimte een bericht om u door het proces te begeleiden. Volg de verbinding aan het Beheer van het Geheime voorgeheugen en vernieuw de ongeldige caches.

![Productkenmerk opslaan - cachebericht bijwerken](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>Wanneer entiteiten uit een catalogus worden gewijzigd, kan dit van invloed zijn op andere pagina&#39;s en meerdere cache tegelijk ongeldig maken. Wanneer u de pagina van het geheim voorgeheugenbeheer bekijkt, kon u ongeldige punten zien die vereisen verfrist zich toen zij waren _**niet rechtstreeks bewerkt**_. Deze validatie treedt bijvoorbeeld op wanneer u een product in de catalogus bewerkt en het wordt toegewezen aan een categorie of wanneer u een regel voor een verwant product wijzigt.

De _[!UICONTROL Cache Management]_op de pagina worden de status van elke primaire cache en de bijbehorende tag weergegeven. De grote knopen in de hoger-juiste hoek kunnen worden gebruikt om het geheime voorgeheugen, of de alle-inclusieve Opslag van het Geheime voorgeheugen te spoelen. Onder aan de pagina vindt u extra knoppen om de cache van de catalogusproductafbeeldingen en de JavaScript/CSS-cache te leegmaken.

Nadat u een cache hebt gewist, vernieuwt u altijd de browser om te controleren of u de meest recente bestanden kunt zien. Als u de cache van de Handel wist, wordt de cache van uw webbrowser niet gewist. Mogelijk moet u de browsercache wissen om de bijgewerkte inhoud te kunnen zien.

Zie voor aanvullende technische informatie [Overzicht van cache](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} in het dialoogvenster _Handleiding voor de ontwikkeling van de handelsfront_.

Toegang krijgen tot de _[!UICONTROL Cache Management]_pagina door een van de volgende handelingen uit te voeren:

- Klik op de knop **[!UICONTROL Cache Management]** in het bericht boven de werkruimte.
- Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Cachebeheer](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Aanbevolen procedures voor het in cache plaatsen

Bij de Handel hebben opnieuw indexeren en in cache plaatsen verschillende doeleinden. [Indexen](index-management.md) traceer databasegegevens voor betere zoekprestaties, snellere gegevensophaling voor winkelcentra en nog veel meer. In cache worden geladen gegevens, afbeeldingen, indelingen en dergelijke opgeslagen voor betere prestaties bij het laden en openen van de opslagruimte.

- Maak de cache altijd leeg nadat u extensies/modules hebt geïnstalleerd. U kunt een of meer extensies installeren en vervolgens de cache leegmaken.
- Maak het cachegeheugen leeg nadat u Commerce hebt geïnstalleerd. Voor nieuwe installaties moet u ook opnieuw indexeren.
- Maak de cache leeg nadat u de upgrade hebt uitgevoerd van de ene versie van Open Source of Commerce naar de andere.
- Houd bij het spoelen rekening met het type cache en het plannen van het spoelen tijdens perioden zonder pieken. Kies bijvoorbeeld een tijdstip waarop weinig klanten toegang hebben tot de site, bijvoorbeeld &#39;s nachts of &#39;s morgens. Het wissen van bepaalde cachetypen tijdens piektijden leidt tot een hoge belasting van de Admin en kan resulteren in een downsite tot voltooiing.
- Wanneer [herindexering](index-management.md)hoeft u niet ook een uitlijncache uit te voeren.

## Bronnen voor Cachebeheer

De toegang tot specifieke acties van het geheim voorgeheugenonderhoud kan aan gebruikers door rol, met inbegrip van opties aan mening worden toegewezen, knevel, en spoelgeheime voorgeheugens. Adobe raadt u aan alleen handelingen op het niveau van beheerders uit te voeren. Het bieden van toegang tot alle functies voor cachebeheer kan van invloed zijn op de prestaties van uw winkel.

![Rolresources - cachebeheer](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Voor informatie over het toewijzen van middelen om toegang voor Admin gebruikersrekeningen te verlenen, zie [Rolresources](permissions-user-roles.md#role-resources). De volgende middelen controleren toegang tot de hulpmiddelen van het geheim voorgeheugenbeheer:

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

1. Set **[!UICONTROL Actions]** tot `Refresh` en klik op **[!UICONTROL Submit]**.

## Vernieuwen van massaactie uitvoeren

1. Als u een groep caches wilt selecteren, stelt u **[!UICONTROL Mass Actions]** op een van de volgende wijzen:

   - `Select All`
   - `Select Visible`

1. Schakel het selectievakje in van elke cache die door de handeling als doel moet worden ingesteld.

1. Set **[!UICONTROL Actions]** tot `Refresh` en klik op **[!UICONTROL Submit]**.

## De cache van de productafbeelding leegmaken

1. Onder _[!UICONTROL Additional Cache Management]_, klikt u op **[!UICONTROL Flush Catalog Images Cache]**om vooraf gegenereerde afbeeldingsbestanden voor het product te wissen.

   De `Image cache was cleaned` verschijnt boven aan de werkruimte.

1. Wis de cache van uw browser.

## De JavaScript/CSS-cache leegmaken

1. Onder _[!UICONTROL Additional Cache Management]_, klikt u op **[!UICONTROL Flush JavaScript/CSS Cache]**om JavaScript- en CSS-bestanden te wissen die in één bestand zijn samengevoegd.

   De `The JavaScript/CSS cache has been cleaned` verschijnt boven aan de werkruimte.

1. Wis de cache van uw browser.

## Uitlijnen met gebruik van de opdrachtregel

De handel verstrekt extra flush geheim voorgeheugenopties gebruikend de bevellijn. Voor deze opties is mogelijk ondersteuning voor ontwikkelaars vereist. Voor volledige details en bevelopties, zie [De cache beheren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){:target=&quot;_blank&quot;} in het dialoogvenster _Configuratiegids_.

## Besturingselementen

| Besturing | Beschrijving |
|--- |--- |
| [!UICONTROL Mass Actions] | Selecteert checkbox van veelvoudige geheime voorgeheugens. Opties: <br/>**[!UICONTROL Select All]**— Selecteert checkbox van alle geheime voorgeheugens.<br/>** Alle selecties opheffen **— Wist het selectievakje van alle cache.<br/>**[!UICONTROL Select Visible]** — Selecteert checkbox van alle zichtbare geheime voorgeheugens. <br/>**[!UICONTROL Unselect Visible]**— Wist het selectievakje van alle zichtbare cache. |
| [!UICONTROL Actions] | Hiermee bepaalt u de actie die op alle geselecteerde caches moet worden toegepast. Opties: <br/>**[!UICONTROL Enable]**— Schakelt alle geselecteerde caches in.<br/>**[!UICONTROL Disable]** — Schakelt alle geselecteerde caches uit. <br/>**[!UICONTROL Refresh]**— Verfrist alle geselecteerde geheime voorgeheugens. |
| [!UICONTROL Submit] | Hiermee past u de handeling toe op alle geselecteerde caches. |

{style="table-layout:auto"}

### Knoppen

| Knop | Beschrijving |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | Hiermee worden alle items in de standaardhandelscache verwijderd (`var/cache`), op basis van de bijbehorende tags Commerce. |
| [!UICONTROL Flush Cache Storage] | Hiermee verwijdert u alle items uit het cachegeheugen, ongeacht de tag Commerce. Als uw systeem een alternatieve cachelocatie gebruikt, worden alle cachebestanden die door andere toepassingen worden gebruikt, tijdens het proces verwijderd. |
| [!UICONTROL Flush Catalog Images Cache] | Hiermee verwijdert u alle automatisch gewijzigde en van een watermerk voorziene catalogusafbeeldingen die zijn opgeslagen in `media/catalog/product/cache`. Als onlangs geüploade afbeeldingen niet in de catalogus worden weergegeven, probeert u de catalogus te spoelen en de browser te vernieuwen. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Hiermee verwijdert u de samengevoegde kopie van JavaScript- en CSS-bestanden uit de cache. Als recente wijzigingen in de stijlpagina of JavaScript niet in de winkel worden weergegeven, probeert u de JavaScript/CSS-cache te leegmaken en de browser te vernieuwen. |
| [!UICONTROL Flush Static Files Cache] | Verwijdert vooraf verwerkte meningsdossiers en statische dossiers. |

{style="table-layout:auto"}

### Cursussen

| Cache | Beschrijving | Gekoppelde tag |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | Diverse configuraties van XML die over modules werden verzameld en werden samengevoegd.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | Instructies voor het samenstellen van lay-outs. | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | HTML van paginablokken. | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | Gegevensbestanden verzameling. | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | Wist de weerspiegelingsgegevens van de API interface, die typisch tijdens runtime wordt geproduceerd. | `REFLECTION` |
| [!UICONTROL Database DDL operations] | Resultaten van vraag DDL, zoals beschrijvend lijsten of indexen. | `DB_DDL` |
| [!UICONTROL Compiled Config] | Resultaten van codecompilatie. | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | Declaratiecache voor entiteitstypen. | `EAV` |
| [!UICONTROL Customer Notification] | Tijdelijke meldingen die worden weergegeven in de gebruikersinterface. | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | Integratieconfiguratiebestand. | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | Integrations API configuration file. | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | Volledige pagina in cache plaatsen. | `FPC` |
| [!UICONTROL Translations] | Vertaalbestanden. | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | REST- en SOAP-configuraties, gegenereerd WSDL-bestand. | `WEBSERVICE` |
| [!UICONTROL Target Rule] | Index van doelregel | `TARGET_RULE` |

{style="table-layout:auto"}

## In cache plaatsen van volledige pagina&#39;s

Adobe Commerce en Magento Open Source maken gebruik van caching op de server van volledige pagina&#39;s om snel categorie-, product- en CMS-pagina&#39;s weer te geven. Het in cache plaatsen van volledige pagina&#39;s verbetert de responstijd en vermindert de belasting op de server. Zonder caching, zou elke pagina blokken van code moeten in werking stellen en informatie van het gegevensbestand terugwinnen. Als plaatsing op een volledige pagina is ingeschakeld, kan een volledig gegenereerde pagina echter rechtstreeks vanuit de cache worden gelezen.

>[!NOTE]
>
>Het wordt aanbevolen [Varnish Cache](https://varnish-cache.org/){:target=&quot;_blank&quot;} alleen gebruiken in een productieomgeving.

Inhoud in cache kan worden gebruikt om de aanvragen van vergelijkbare typen bezoeken te verwerken. Hierdoor kunnen pagina&#39;s die aan een bezoeker worden getoond afwijken van de pagina&#39;s die aan een klant worden getoond. Voor het in cache plaatsen is elk bezoek een van de volgende drie soorten:

- `Non-sessioned` - Tijdens een niet-sessioneel bezoek bekijken de winkelpagina&#39;s, maar communiceren ze niet met de winkel. Het systeem plaatst de inhoud van elke weergegeven pagina in cache en levert deze aan andere niet-sessioned kopers.
- `Sessioned` - Tijdens een sessioneel bezoek wordt een sessie-ID toegekend aan kopers die met de winkel communiceren, bijvoorbeeld door producten te vergelijken of producten aan de winkelwagentje toe te voegen. Pagina&#39;s in de cache die tijdens de sessie worden gegenereerd, worden tijdens de sessie alleen door die winkelier gebruikt.
- `Customer` - Er worden klantsessies gemaakt voor gebruikers die zich voor een account bij uw winkel en winkel hebben geregistreerd terwijl ze zich bij hun account hebben aangemeld. Tijdens de sessie kunnen klanten speciale aanbiedingen, promoties en prijzen krijgen die zijn gebaseerd op hun toegewezen klantengroep.

Voor technische informatie, zie [Varnish configureren en gebruiken](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} en [Redis gebruiken voor de pagina Commerce en de standaardcache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} in het dialoogvenster _Configuratiegids_.

**_Om het full-page geheime voorgeheugen te vormen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Full Page Cache]** sectie.

   ![Geavanceerde configuratie - volledige paginacache](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Caching Application]** op een van de volgende wijzen:

   - `Built-in Application`
   - `Varnish Caching`

1. Als u de time-out voor de paginacache wilt instellen, voert u de **[!UICONTROL TTL for public content]**. (De standaardwaarde is `86400`)

1. Als u Varnish gebruikt, voltooit u de **[!UICONTROL Varnish Configuration]** als volgt:

   - **[!UICONTROL Access list]** - Ga de IP adressen in die de Varnish configuratie kunnen zuiveren om een config dossier te produceren. Scheid meerdere items met een komma. De standaardwaarde is `localhost`.

   - **[!UICONTROL Backend host]** - Ga het IP adres van de achterste deelgastheer in die config dossiers produceert. De standaardwaarde is `localhost`.

   - **[!UICONTROL Backend port]** - Identificeer de achterste haven die wordt gebruikt om configuratiedossiers te produceren. De standaardwaarde is: `8080`.

   - **[!UICONTROL Grace period]** - Geef het aantal seconden op dat als respijtperiode moet worden gebruikt om configuratiebestanden te genereren. Zie [Geavanceerde Varnish-configuratie](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) in de _Configuratiegids_.

   - De configuratie exporteren als een `varnish.vcl` Klik op de knop voor de versie van Varnish die u gebruikt.

   ![Geavanceerde configuratie - vernis met volledige paginacache](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
