---
title: Cataloguszoekopdracht configureren
description: Leer hoe u het zoeken naar catalogi voor uw winkel kunt configureren.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# Cataloguszoekopdracht configureren

Er zijn twee variaties van de configuratie van het Onderzoek van de Catalogus. De eerste methode beschrijft de beschikbare montages wanneer [&#x200B; Levend Onderzoek &#x200B;](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=nl-NL) geïnstalleerd is. De tweede methode beschrijft de configuratiemontages voor inheemse Adobe Commerce met [&#x200B; OpenSearch &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html?lang=nl-NL) {:target="_blank"}.

>[!NOTE]
>
>Voor de projecten van de wolkeninfrastructuur, zie extra instructies in [_Commerce op de Gids van de Infrastructuur van de Wolk_ &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce-cloud-service/user-guide/configure/service/opensearch).

## Methode 1: Adobe Commerce met [!DNL Live Search]

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Search]** sectie uit.

   ![&#x200B; het Onderzoek van de Catalogus naar Levend Onderzoek &#x200B;](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [&#x200B; Adobe Commerce met Levend Onderzoek &#x200B;](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) in de _Verwijzing van de Configuratie_.

1. Stel een waarde in voor **[!UICONTROL Minimal Query Length]** en **[!UICONTROL Maximum Query Length]** om de lengte en het aantal woorden van zoekquerytekst te beperken.

1. Als u de hoeveelheid populaire zoekresultaten wilt beperken tot cachegeheugen voor snellere reacties, stelt u een waarde in voor **[!UICONTROL Number of top search results to cache]** .

   De standaardwaarde is `100` . Als u de waarde `0` invoert, worden alle zoektermen en resultaten in cache opgeslagen wanneer u de tweede keer invoert.

1. Om het maximumaantal lijnen te veranderen die voor teruggekeerde resultaten in [&#x200B; storefront pop over &#x200B;](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-storefront/quick-tour.html?lang=nl-NL) beschikbaar zijn, ga een verschillende **[!UICONTROL Autocomplete Limit]** waarde in.

   Als u het aantal regels beperkt, worden zoekopdrachten sneller uitgevoerd en wordt de lijst kleiner. De standaardwaarde is `8` regels.

## Methode 2: Commerce met OpenSearch

>[!IMPORTANT]
>
>- Vanwege de aankondiging van het einde van de [!DNL Elasticsearch 7] -service voor augustus 2023 wordt aanbevolen dat alle Adobe Commerce-klanten naar de OpenSearch 2.x-zoekfunctie migreren. Voor informatie over het migreren van uw onderzoeksmotor tijdens productverbetering, zie [&#x200B; Migrerend aan OpenSearch &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=nl-NL) in de _Gids van de Verbetering_.
>- In versies 2.4.4 en 2.4.3-p2 zijn alle velden met het label Elasticsearch ook van toepassing op OpenSearch. Toen de steun voor Elasticsearch 8.x in versie 2.4.6 werd geïntroduceerd, werden de nieuwe etiketten gecreeerd om tussen Elasticsearch en configuraties te onderscheiden OpenSearch. De configuratieopties voor beide zijn echter gelijk.

### Stap 1: algemene zoekopties configureren

>[!NOTE]
>
>Met OpenSearch en Elasticsearch is er geen ondersteuning buiten de box voor zoeken op het achtervoegsel. Bijvoorbeeld, kan het onderzoek door SKU niet het verwachte resultaat terugkeren als het sleutelwoord slechts het einddeel van SKU bevat.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Search]** sectie uit.

   ![&#x200B; de motormontages van het Onderzoek &#x200B;](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   Voor meer informatie over deze opties, zie [&#x200B; Adobe Commerce met inheems onderzoek &#x200B;](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search) in de _Verwijzing van de Configuratie_.

1. Stel een waarde in voor **[!UICONTROL Minimal Query Length]** en **[!UICONTROL Maximum Query Length]** om de lengte en het aantal woorden van zoekquerytekst te beperken.

   >[!IMPORTANT]
   >
   >De waarde die voor dit minimum- en maximumbereik is ingesteld, moet compatibel zijn met het corresponderende bereik dat is ingesteld in de configuratie van de zoekmachine. Als u deze waarden bijvoorbeeld instelt op `2` en `300` in Commerce, werkt u de bijbehorende waarden bij in uw zoekprogramma.

1. Als u de hoeveelheid populaire zoekresultaten wilt beperken tot cachegeheugen voor snellere reacties, stelt u een waarde in voor **[!UICONTROL Number of top search results to cache]** .

   De standaardwaarde is `100` . Als u de waarde `0` invoert, worden alle zoektermen en resultaten in cache opgeslagen wanneer u de tweede keer invoert.

1. Stel de **[!UICONTROL Enable EAV Indexer]** in als u de product EAV-index wilt in- of uitschakelen.

   Deze functie verbetert de indexatiesnelheid en beperkt het gebruik van indexen door extensies van derden.

1. Stel een waarde in voor **[!UICONTROL Autocomplete Limit]** om het maximumaantal zoekresultaten dat wordt weergegeven voor automatisch aanvullen van zoekopdrachten te beperken.

   Als u deze hoeveelheid beperkt, worden de zoekresultaten beter en wordt de lijst kleiner. De standaardwaarde is `8` .

### Stap 2: De OpenSearch-verbinding configureren

>[!IMPORTANT]
>
>De velden **[!UICONTROL Search Engine]** , **[!UICONTROL OpenSearch Server Hostname]** , **[!UICONTROL OpenSearch Server Port]** , **[!UICONTROL OpenSearch Index Prefix]** , **[!UICONTROL Enable OpenSearch HTTP Auth]** en **[!UICONTROL OpenSearch Server Timeout]** zijn geconfigureerd toen Commerce werd geïnstalleerd of bijgewerkt. Deze waarden moeten alleen worden gewijzigd wanneer u een upgrade uitvoert of OpenSearch wijzigt.

1. Selecteer `OpenSearch` bij **[!UICONTROL Search Engine]** .

1. Accepteer voor **[!UICONTROL OpenSearch Server Hostname]** de standaardwaarde die was geconfigureerd toen Commerce werd geïnstalleerd.

1. Accepteer voor **[!UICONTROL OpenSearch Server Port]** de standaardwaarde die was geconfigureerd toen Commerce werd geïnstalleerd.

   In dit voorbeeld is de standaardwaarde `9200` .

1. Voer bij **[!UICONTROL OpenSearch Index Prefix]** een voorvoegsel in om de Elasticsearch-index te identificeren.

   De standaardwaarde is `magento2` .

1. Stel **[!UICONTROL Enable OpenSearch HTTP Auth]** in op `Yes` als u HTTP-verificatie wilt gebruiken om te vragen of een gebruikersnaam en wachtwoord toegang hebben tot de OpenSearch-server.

1. Voer bij **[!UICONTROL OpenSearch Server Timeout]** het aantal seconden in voordat de time-out van het systeem optreedt.

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

Geef een waarde op voor **[!UICONTROL Minimum Terms to Match]** als u wilt bepalen hoeveel termen de zoekopdracht minimaal moet retourneren. Als u deze waarde opgeeft, bent u zeker van optimale resultaten voor kopers. Voor een lijst van toegelaten waarden, zie [&#x200B; minimum_should_match parameter &#x200B;](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) in de documentatie OpenSearch.

Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
