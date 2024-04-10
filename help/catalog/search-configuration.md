---
title: Cataloguszoekopdracht configureren
description: Leer hoe u het zoeken naar catalogi voor uw winkel kunt configureren.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Cataloguszoekopdracht configureren

Er zijn twee variaties van de configuratie van het Onderzoek van de Catalogus. De eerste methode beschrijft de beschikbare instellingen wanneer [Live zoeken](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) is geïnstalleerd. De tweede methode beschrijft de configuratie-instellingen voor native Adobe Commerce met [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Methode 1: Adobe Commerce met [!DNL Live Search]

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Search]** sectie.

   ![Catalogus zoeken naar Live zoeken](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [Adobe Commerce met Live zoeken](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) in de _Configuratieverwijzing_.

1. Als u de lengte en het aantal woorden van zoekquerytekst wilt beperken, stelt u een waarde in voor **[!UICONTROL Minimal Query Length]** en **[!UICONTROL Maximum Query Length]**.

1. Als u de hoeveelheid populaire zoekresultaten wilt beperken tot cachegeheugen voor snellere reacties, stelt u een waarde in voor **[!UICONTROL Number of top search results to cache]**.

   De standaardwaarde is `100`. De waarde van `0` Hiermee plaatst u alle zoektermen en resultaten in cache wanneer u een tweede keer invoert.

1. Als u het maximumaantal regels dat beschikbaar is voor geretourneerde regels wilt wijzigen, wordt in het dialoogvenster [pop-up van winkel](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), voert u een andere **[!UICONTROL Autocomplete Limit]** waarde.

   Als u het aantal regels beperkt, worden zoekopdrachten sneller uitgevoerd en wordt de lijst kleiner. De standaardwaarde is `8` lijnen.

## Methode 2: Handel met Elasticsearch

>[!IMPORTANT]
>
>Door de [!DNL Elasticsearch 7] Aankondiging aan het einde van de service voor augustus 2023 wordt aanbevolen dat alle Adobe Commerce-klanten naar de zoekmachine OpenSearch 2.x migreren. Voor informatie over het migreren van uw zoekmachine tijdens productverbetering, zie [Migreren naar OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) in de _Upgradehandleiding_.

### Stap 1: algemene zoekopties configureren

>[!NOTE]
>
>Met Elasticsearch, is er geen out-of-box steun voor onderzoek door het achtervoegsel. Bijvoorbeeld, kan het onderzoek door SKU niet het verwachte resultaat terugkeren als het sleutelwoord slechts het einddeel van SKU bevat.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Search]** sectie.

   ![Instellingen Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Zie voor meer informatie over deze opties [Adobe Commerce met Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) in de _Configuratieverwijzing_.

1. Als u de lengte en het aantal woorden van zoekquerytekst wilt beperken, stelt u een waarde in voor **[!UICONTROL Minimal Query Length]** en **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >De waarde die voor dit minimum en maximumbereik wordt ingesteld, moet compatibel zijn met het corresponderende bereik dat is ingesteld in de configuratie van de zoekmachine voor Elasticsearch. Als u deze waarden bijvoorbeeld instelt op `2` en `300` in Handel, werk de overeenkomstige waarden in uw onderzoeksmotor bij.

1. Als u de hoeveelheid populaire zoekresultaten wilt beperken tot cachegeheugen voor snellere reacties, stelt u een waarde in voor **[!UICONTROL Number of top search results to cache]**.

   De standaardwaarde is `100`. De waarde van `0` Hiermee plaatst u alle zoektermen en resultaten in cache wanneer u een tweede keer invoert.

1. Als u de EAV-indexeerfunctie van het product wilt in- of uitschakelen, stelt u de optie **[!UICONTROL Enable EAV Indexer]**.

   Deze functie verbetert de indexatiesnelheid en beperkt het gebruik van indexen door extensies van derden.

1. Als u het maximumaantal zoekresultaten dat wordt weergegeven voor automatisch aanvullen van zoekopdrachten wilt beperken, stelt u een waarde in voor **[!UICONTROL Autocomplete Limit]**.

   Als u deze hoeveelheid beperkt, worden de zoekresultaten beter en wordt de lijst kleiner. De standaardwaarde is `8`.

### Stap 2: Vorm de verbinding van de Elasticsearch

>[!IMPORTANT]
>
>De **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, en **[!UICONTROL Elasticsearch Server Timeout]** de gebieden werden gevormd toen de Handel werd geïnstalleerd of werd bevorderd. Deze waarden moeten alleen worden gewijzigd wanneer u de Elasticsearch bijwerkt of wijzigt.

1. Voor **[!UICONTROL Search Engine]**, accepteert u de standaardwaarde `Elasticsearch 7`.

   Elasticsearch 7.6.x wordt vereist voor alle installaties van de Handel.

1. Voor **[!UICONTROL Elasticsearch Server Hostname]**, keur de standaardwaarde goed die werd gevormd toen de Handel werd geïnstalleerd.

   In dit voorbeeld is de standaardwaarde `elasticsearch.internal`.

1. Voor **[!UICONTROL Elasticsearch Server Port]**, keur de standaardwaarde goed die werd gevormd toen de Handel werd geïnstalleerd.

   In dit voorbeeld is de standaardwaarde `9200`.

1. Voor **[!UICONTROL Elasticsearch Index Prefix]** Voer een voorvoegsel in om de index van de Elasticsearch te identificeren.

   De standaardwaarde is `magento2`.

1. Om de authentificatie van HTTP te gebruiken om voor een gebruikersbenaming en wachtwoord te vragen om tot de Server van de Elasticsearch toegang te hebben, plaats **[!UICONTROL Enable Elasticsearch HTTP Auth]** tot `Yes`.

1. Voor **[!UICONTROL Elasticsearch Server Timeout]** Voer het aantal seconden in voordat de time-out van het systeem optreedt.

   De standaardwaarde is `15`.

1. Om de configuratie te verifiëren, klik **[!UICONTROL Test Connection]**.

### Stap 3: Configureer suggesties en aanbevelingen

>[!NOTE]
>
>Zoeksuggesties en aanbevelingen kunnen van invloed zijn op de prestaties van de server.

1. Als u aanbevelingen wilt aanbieden, stelt u **[!UICONTROL Enable Search Recommendations]** tot `Yes` en voer de volgende handelingen uit:

   - Voor **[!UICONTROL Search Recommendation Count]**, voert u het aantal aanbevelingen in dat u wilt aanbieden.

   - Om het aantal resultaten te tonen die voor elke aanbeveling worden gevonden, reeks **[!UICONTROL Show Results Count for Each Recommendation]** tot `Yes`.

1. Set **[!UICONTROL Enable Search Suggestions]** tot `Yes` en voer de volgende handelingen uit:

   - Voor **[!UICONTROL Search Suggestions Count]**, geeft u het aantal zoeksuggesties op dat u wilt aanbieden.

   - Om het aantal resultaten te tonen die voor elke suggestie worden gevonden, reeks **[!UICONTROL Show Results for Each Suggestion]** tot `Yes`.

### Stap 4: Minimumvoorwaarden configureren om overeen te komen

Om het minimumaantal termijnen van uw vraag te controleren die de onderzoeksresultaten voor terugkeer zouden moeten aanpassen, specificeer een waarde voor **[!UICONTROL Minimum Terms to Match]**. Als u deze waarde opgeeft, bent u zeker van optimale resultaten voor kopers. Zie voor een lijst met toegestane waarden [minimum_should_match, parameter](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) in de documentatie van de Elasticsearch.

Klik op **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
