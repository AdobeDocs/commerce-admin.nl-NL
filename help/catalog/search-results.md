---
title: Zoekresultaten
description: Leer hoe u kunt configureren hoe uw producten voldoen aan de zoekcriteria die zijn ingevoerd in het vak Snel zoeken of het formulier Geavanceerd zoeken.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Zoekresultaten

>[!NOTE]
>
>Deze pagina beschrijft standaardonderzoeksfunctionaliteit die van [&#x200B; Levend Onderzoek &#x200B;](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=nl-NL) zou kunnen verschillen.

De _lijst van de Resultaten van het Onderzoek_ omvat alle producten die de onderzoekscriteria ingegaan in het Snelle vakje van het Onderzoek of de Geavanceerde vorm van het Onderzoek aanpassen. Elke productlijst in de catalogus heeft in wezen dezelfde besturingselementen. Het enige verschil is dat één het resultaat van een onderzoeksvraag is, en het andere verschil is het resultaat van [&#x200B; navigatie &#x200B;](navigation.md).

De resultaten kunnen als of net of lijst worden geformatteerd en door een selectie van attributen worden gesorteerd. Besturingselementen voor paginering worden weergegeven als er meer producten zijn dan op de pagina passen. Gebruik deze besturingselementen om van de ene pagina naar de andere te gaan. Het aantal records per pagina wordt bepaald door de configuratie Voorkant catalogus. Voor meer informatie, zie [&#x200B; Lijsten van het Product &#x200B;](navigation-product-listings.md).

Met **Elasticsearch**:

- Er is geen out-of-box steun voor onderzoek door het achtervoegsel. Bijvoorbeeld, kan het onderzoek door SKU niet het verwachte resultaat terugkeren als het sleutelwoord slechts het einddeel van SKU bevat.
- Ondersteuning voor zoeken op voorvoegsel (gedeeltelijk zoeken op trefwoorden) buiten de box alleen voor `name` - en `sku` -productkenmerken. Alle andere productkenmerken worden doorzocht door het hele trefwoord, met de exacte overeenkomst.
- Zoekresultaten voor `name` - en `sku` -productkenmerken zijn gebaseerd op de relevantie, niet op exacte overeenkomst. De meest relevante gelijken, zoals precies overtroffen _Naam van het Product_ of _SKU_, zijn eerst vermeld. Om naar een nauwkeurige gelijke te zoeken, kan de klant dubbele citaten in de onderzoeksvraag gebruiken. Een zoekquery van `WSH12-32-Red` kan bijvoorbeeld meerdere producten retourneren, gesorteerd op relevantie. Maar een `"WSH12-32-Red"` onderzoeksvraag keert slechts één product met **_exact_** aangepast `sku` terug.

![&#x200B; resultaten van het Onderzoek met pagineringscontroles &#x200B;](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Gezien de aankondiging van het einde van Elasticsearch 7 voor augustus 2023 wordt aanbevolen dat alle Adobe Commerce-klanten naar de OpenSearch 2.x zoekmachine migreren. Voor informatie over het migreren van uw onderzoeksmotor tijdens productverbetering, zie [&#x200B; Migrerend aan OpenSearch &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=nl-NL) in de _Gids van de Verbetering_.

## Trefwoordtoewijzing om zoekresultaten uit te breiden

Deze techniek gebruikt een attribuut om een op sleutelwoord-gebaseerde vereniging tussen twee producten tot stand te brengen zodat een onderzoek naar één van beide producten resultaten voor beide producten terugkeert. U kunt trefwoordtoewijzing gebruiken om een product te promoten in zoekresultaten als dit anders niet het geval zou zijn.

![&#x200B; resultaten van het Onderzoek met sleutelwoordafbeelding &#x200B;](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

Het volgende voorbeeld gebruikt sleutelwoordafbeelding die op SKU wordt gebaseerd. Wanneer één van beide SKU in het onderzoeksvakje is ingegaan, verschijnen beide producten in de resultaten. De SKUs van de volgende configureerbare producten worden in kaart gebracht, eerder dan SKUs van productvariaties:

- Montana Wind Jacket (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Stap 1: Een kenmerk maken

1. Open in de lijst _[!UICONTROL Products]_&#x200B;de bewerkingsmodus van `Montana Wind Jacket` (MJ03).
1. Klik in de rechterbovenhoek op **[!UICONTROL Add Attribute]** .
1. Voor de _Uitgezochte pagina van Attributen_, klik **[!UICONTROL Create New Attribute]**.
1. Vul de eigenschappen van het kenmerk als volgt in:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (standaardwaarde)
   - [!UICONTROL Use in Filter Options] - `Yes` (standaardwaarde)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.

   Het kenmerk wordt toegevoegd aan het kenmerk dat voor het product is ingesteld.

### Stap 2: Wijs het eerste product toe

1. Schuif omlaag op de pagina met productinstellingen en vouw de sectie _[!UICONTROL Attributes]_&#x200B;uit.
1. Voer in het veld **[!UICONTROL Search Keywords]** de SKU `MH01` in die aan dit product moet worden toegewezen.

   U kunt meerdere SKU&#39;s invoeren die door een spatie worden gescheiden in het veld Trefwoorden zoeken. In dit voorbeeld wordt slechts één item ingevoerd.

   ![&#x200B; sectie van Attributen met onderzoekssleutelwoord &#x200B;](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.
1. Ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;en vernieuw de **[!UICONTROL Page Cache]**.

### Stap 3: Het tweede product toewijzen

1. Open in de lijst _[!UICONTROL Products]_&#x200B;de `Chaz Kangaroo Hoodie` (MH01) in de bewerkingsmodus.
1. Schuif omlaag en vouw de sectie **[!UICONTROL Attributes]** uit.
1. Voer in het veld **[!UICONTROL Search Keywords]** de SKU voor het andere product in, `MJ03` .
1. Klik op **[!UICONTROL Save]**.
1. Ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;en vernieuw de **[!UICONTROL Page Cache]**.

### Stap 4: Test het in de winkel

1. Ga naar de storefront en ga `MJ03` in het _Snelle vakje van het Onderzoek_ in.
1. Controleer of beide producten worden geretourneerd in de lijst met zoekresultaten.

## Gewogen zoekopdracht

Aan productkenmerken die zijn ingeschakeld voor zoeken in een catalogus, kan een gewicht worden toegewezen, zodat ze een hogere waarde krijgen in de zoekresultaten. Kenmerken met een groter gewicht worden geretourneerd vóór kenmerken met een lager gewicht. Bijvoorbeeld, als er twee attributen in het systeem zijn, _kleur_ met een onderzoeksgewicht van 3 en _beschrijving_ met een onderzoeksgewicht van 1. Een onderzoek naar het woord _rood_ keert een lijst van producten met een waarde van kleurenattributen van `red` bij de bovenkant van de onderzoeksresultaten terug en keert producten met beschrijvingen terug die het woord _rood_ bij de bodem van de onderzoeksresultaten bevatten. In dit voorbeeld heeft het kenmerk `color` een grotere gedefinieerde dikte dan het kenmerk `description` .

>[!IMPORTANT]
>
>Het sorteren door relevantie wordt beïnvloed door **_veelvoudige_** criteria en verhoudingen tussen hen **_tezelfdertijd_**. [!UICONTROL Search Weight] is slechts een van deze criteria. Dit betekent dat kenmerken met een lager zoekgewicht soms nog relevanter zijn dan kenmerken met een hoger zoekgewicht. Andere criteria kunnen het aantal overeenkomsten in een bepaald kenmerk, de positie van de gevonden zoekterm en de algemene tekststructuur vóór en na een zoekterm zijn.

**_om de eigenschappen van het onderzoeksgewicht van een attribuut te plaatsen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Zoek het kenmerk in de lijst en open in de bewerkingsmodus.

1. Kies **[!UICONTROL Storefront Properties]** in het linkerdeelvenster en voer de volgende handelingen uit:

   - Stel **[!UICONTROL Use in Search]** in op `Yes` als u het kenmerk in zoekquery&#39;s wilt opnemen.

   - Als u de zoekwaarde van het kenmerk wilt bepalen, stelt u **[!UICONTROL Search Weight]** in op een getal tussen 1 en 10, waarbij `10` de hoogste prioriteit heeft. Als er geen waarde wordt ingevoerd, worden alle kenmerken standaard ingesteld op een zoekgewicht van `1` .

   ![&#x200B; Gewicht van het Onderzoek &#x200B;](./assets/search-weight.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.
