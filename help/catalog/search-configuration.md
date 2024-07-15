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

Er zijn twee variaties van de configuratie van het Onderzoek van de Catalogus. De eerste methode beschrijft de beschikbare montages wanneer [ Levend Onderzoek ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) geïnstalleerd is. De tweede methode beschrijft de configuratiemontages voor inheemse Adobe Commerce met [ Elasticsearch ][1] {:target= &quot;_blank&quot;}.

## Methode 1: Adobe Commerce met [!DNL Live Search]

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Search]** sectie uit.

   ![ het Onderzoek van de Catalogus naar Levend Onderzoek ](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [ Adobe Commerce met Levend Onderzoek ](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) in de _Verwijzing van de Configuratie_.

1. Stel een waarde in voor **[!UICONTROL Minimal Query Length]** en **[!UICONTROL Maximum Query Length]** om de lengte en het aantal woorden van zoekquerytekst te beperken.

1. Als u de hoeveelheid populaire zoekresultaten wilt beperken tot cachegeheugen voor snellere reacties, stelt u een waarde in voor **[!UICONTROL Number of top search results to cache]** .

   De standaardwaarde is `100` . Als u de waarde `0` invoert, worden alle zoektermen en resultaten in cache opgeslagen wanneer u de tweede keer invoert.

1. Om het maximumaantal lijnen te veranderen die voor teruggekeerde resultaten in [ storefront pop over ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) beschikbaar zijn, ga een verschillende **[!UICONTROL Autocomplete Limit]** waarde in.

   Als u het aantal regels beperkt, worden zoekopdrachten sneller uitgevoerd en wordt de lijst kleiner. De standaardwaarde is `8` regels.

## Methode 2: Commerce met Elasticsearch

>[!IMPORTANT]
>
>Vanwege de aankondiging van het einde van de [!DNL Elasticsearch 7] -service voor augustus 2023 wordt aanbevolen dat alle Adobe Commerce-klanten naar de OpenSearch 2.x-zoekfunctie migreren. Voor informatie over het migreren van uw onderzoeksmotor tijdens productverbetering, zie [ Migrerend aan OpenSearch ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) in de _Gids van de Verbetering_.

### Stap 1: algemene zoekopties configureren

>[!NOTE]
>
>Met Elasticsearch, is er geen out-of-box steun voor onderzoek door het achtervoegsel. Bijvoorbeeld, kan het onderzoek door SKU niet het verwachte resultaat terugkeren als het sleutelwoord slechts het einddeel van SKU bevat.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Search]** sectie uit.

   ![ de Montages van de Elasticsearch ](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Voor meer informatie over deze opties, zie [ Adobe Commerce met Elasticsearch ](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) in de _Verwijzing van de Configuratie_.

1. Stel een waarde in voor **[!UICONTROL Minimal Query Length]** en **[!UICONTROL Maximum Query Length]** om de lengte en het aantal woorden van zoekquerytekst te beperken.

   >[!IMPORTANT]
   >
   >De waarde die voor dit minimum en maximumbereik wordt ingesteld, moet compatibel zijn met het corresponderende bereik dat is ingesteld in de configuratie van de zoekmachine voor Elasticsearch. Als u deze waarden bijvoorbeeld instelt op `2` en `300` in Commerce, werkt u de bijbehorende waarden bij in uw zoekprogramma.

1. Als u de hoeveelheid populaire zoekresultaten wilt beperken tot cachegeheugen voor snellere reacties, stelt u een waarde in voor **[!UICONTROL Number of top search results to cache]** .

   De standaardwaarde is `100` . Als u de waarde `0` invoert, worden alle zoektermen en resultaten in cache opgeslagen wanneer u de tweede keer invoert.

1. Stel de **[!UICONTROL Enable EAV Indexer]** in als u de product EAV-index wilt in- of uitschakelen.

   Deze functie verbetert de indexatiesnelheid en beperkt het gebruik van indexen door extensies van derden.

1. Stel een waarde in voor **[!UICONTROL Autocomplete Limit]** om het maximumaantal zoekresultaten dat wordt weergegeven voor automatisch aanvullen van zoekopdrachten te beperken.

   Als u deze hoeveelheid beperkt, worden de zoekresultaten beter en wordt de lijst kleiner. De standaardwaarde is `8` .

### Stap 2: Vorm de verbinding van de Elasticsearch

>[!IMPORTANT]
>
>De velden **[!UICONTROL Search Engine]** , **[!UICONTROL Elasticsearch Server Hostname]** , **[!UICONTROL Elasticsearch Server Port]** , **[!UICONTROL Elasticsearch Index Prefix]** , **[!UICONTROL Enable Elasticsearch HTTP Auth]** en **[!UICONTROL Elasticsearch Server Timeout]** zijn geconfigureerd toen Commerce werd geïnstalleerd of bijgewerkt. Deze waarden moeten alleen worden gewijzigd wanneer u de Elasticsearch bijwerkt of wijzigt.

1. Accepteer de standaardwaarde `Elasticsearch 7` voor **[!UICONTROL Search Engine]** .

   Elasticsearch 7.6.x is vereist voor alle Commerce-installaties.

1. Accepteer voor **[!UICONTROL Elasticsearch Server Hostname]** de standaardwaarde die was geconfigureerd toen Commerce werd geïnstalleerd.

   In dit voorbeeld is de standaardwaarde `elasticsearch.internal` .

1. Accepteer voor **[!UICONTROL Elasticsearch Server Port]** de standaardwaarde die was geconfigureerd toen Commerce werd geïnstalleerd.

   In dit voorbeeld is de standaardwaarde `9200` .

1. Voer bij **[!UICONTROL Elasticsearch Index Prefix]** een voorvoegsel in om de index van de Elasticsearch te identificeren.

   De standaardwaarde is `magento2` .

1. Stel **[!UICONTROL Enable Elasticsearch HTTP Auth]** in op `Yes` als u HTTP-verificatie wilt gebruiken om te vragen of er een gebruikersnaam en wachtwoord zijn voor toegang tot Elasticsearch Server.

1. Voer bij **[!UICONTROL Elasticsearch Server Timeout]** het aantal seconden in voordat de time-out van het systeem optreedt.

   De standaardwaarde is `15` .

1. Klik op **[!UICONTROL Test Connection]** om de configuratie te controleren.

### Stap 3: Configureer suggesties en aanbevelingen

>[!NOTE]
>
>Zoeksuggesties en aanbevelingen kunnen van invloed zijn op de prestaties van de server.

1. Als u aanbevelingen wilt doen, stelt u **[!UICONTROL Enable Search Recommendations]** in op `Yes` en voert u de volgende handelingen uit:

   - Voer bij **[!UICONTROL Search Recommendation Count]** het aantal aanbevelingen in dat u wilt aanbieden.

   - Stel **[!UICONTROL Show Results Count for Each Recommendation]** in op `Yes` om het aantal resultaten voor elke aanbeveling weer te geven.

1. Stel **[!UICONTROL Enable Search Suggestions]** in op `Yes` en voer de volgende handelingen uit:

   - Voer bij **[!UICONTROL Search Suggestions Count]** het aantal zoeksuggesties in dat u wilt aanbieden.

   - Stel **[!UICONTROL Show Results for Each Suggestion]** in op `Yes` om het aantal resultaten voor elke suggestie weer te geven.

### Stap 4: Minimumvoorwaarden configureren om overeen te komen

Geef een waarde op voor **[!UICONTROL Minimum Terms to Match]** als u wilt bepalen hoeveel termen de zoekopdracht minimaal moet retourneren. Als u deze waarde opgeeft, bent u zeker van optimale resultaten voor kopers. Voor een lijst van toegelaten waarden, zie [ minimum_should_match parameter ](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) in de documentatie van de Elasticsearch.

Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
