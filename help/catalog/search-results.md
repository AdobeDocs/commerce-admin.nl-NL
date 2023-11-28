---
title: Zoekresultaten
description: Leer hoe u kunt configureren hoe uw producten voldoen aan de zoekcriteria die zijn ingevoerd in het vak Snel zoeken of het formulier Geavanceerd zoeken.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# Zoekresultaten

>[!NOTE]
>
>Deze pagina beschrijft de standaardzoekfunctionaliteit die kan verschillen van [Live zoeken](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

De _Zoekresultaten_ bevat alle producten die voldoen aan de zoekcriteria die zijn ingevoerd in het vak Snel zoeken of het formulier Geavanceerd zoeken. Elke productlijst in de catalogus heeft in wezen dezelfde besturingselementen. Het enige verschil is dat één het resultaat van een onderzoeksvraag is, en het andere verschil is het resultaat van [navigatie](navigation.md).

De resultaten kunnen als of net of lijst worden geformatteerd en door een selectie van attributen worden gesorteerd. Besturingselementen voor paginering worden weergegeven als er meer producten zijn dan op de pagina passen. Gebruik deze besturingselementen om van de ene pagina naar de andere te gaan. Het aantal records per pagina wordt bepaald door de configuratie Voorkant catalogus. Zie voor meer informatie [Productaanbiedingen](navigation-product-listings.md).

Met **Elasticsearch**:

- Er is geen out-of-box steun voor onderzoek door het achtervoegsel. Bijvoorbeeld, kan het onderzoek door SKU niet het verwachte resultaat terugkeren als het sleutelwoord slechts het einddeel van SKU bevat.
- Er is out-of-box steun voor onderzoek door prefix (gedeeltelijke sleutelwoordonderzoek) voor `name` en `sku` alleen productkenmerken. Alle andere productkenmerken worden doorzocht door het hele trefwoord, met de exacte overeenkomst.
- Zoekresultaten voor `name` en `sku` productkenmerken zijn gebaseerd op de relevantie, niet op exacte overeenkomst. De meest relevante overeenkomsten, zoals een exact overeenkomende _Productnaam_ of _SKU_, worden als eerste vermeld. Om naar een nauwkeurige gelijke te zoeken, kan de klant dubbele citaten in de onderzoeksvraag gebruiken. Bijvoorbeeld een `WSH12-32-Red` zoekquery kan meerdere producten retourneren, gesorteerd op relevantie. Maar een `"WSH12-32-Red"` zoekquery retourneert slechts één product met **_exact_** gematcht `sku`.

![Zoekresultaten met pagineringselementen](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Gezien de Elasticsearch 7 eindeaankondiging voor augustus 2023, wordt aanbevolen dat alle Adobe Commerce-klanten naar de OpenSearch 2.x zoekmachine migreren. Voor informatie over het migreren van uw zoekmachine tijdens productverbetering, zie [Migreren naar OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) in de _Upgradehandleiding_.

## Trefwoordtoewijzing om zoekresultaten uit te breiden

Deze techniek gebruikt een attribuut om een op sleutelwoord-gebaseerde vereniging tussen twee producten tot stand te brengen zodat een onderzoek naar één van beide producten resultaten voor beide producten terugkeert. U kunt trefwoordtoewijzing gebruiken om een product te promoten in zoekresultaten als dit anders niet het geval zou zijn.

![Zoekresultaten met trefwoordtoewijzing](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

Het volgende voorbeeld gebruikt sleutelwoordafbeelding die op SKU wordt gebaseerd. Wanneer één van beide SKU in het onderzoeksvakje is ingegaan, verschijnen beide producten in de resultaten. De SKUs van de volgende configureerbare producten worden in kaart gebracht, eerder dan SKUs van productvariaties:

- Montana Wind Jacket (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Stap 1: Een kenmerk maken

1. In de _[!UICONTROL Products]_lijst, opent u de `Montana Wind Jacket` (MJ03) in bewerkingsmodus.
1. Klik in de rechterbovenhoek op **[!UICONTROL Add Attribute]**.
1. Op de _Kenmerk selecteren_ pagina, klikt u **[!UICONTROL Create New Attribute]**.
1. Vul de eigenschappen van het kenmerk als volgt in:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label]  - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (standaard)
   - [!UICONTROL Use in Filter Options] - `Yes` (standaard)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Klik op **[!UICONTROL Save Attribute]**.

   Het kenmerk wordt toegevoegd aan het kenmerk dat voor het product is ingesteld.

### Stap 2: Wijs het eerste product toe

1. Schuif omlaag en vouw de _[!UICONTROL Attributes]_sectie.
1. In de **[!UICONTROL Search Keywords]** veld, voert u de SKU in `MH01` dat aan dit product moet worden toegewezen.

   U kunt meerdere SKU&#39;s invoeren die door een spatie worden gescheiden in het veld Trefwoorden zoeken. In dit voorbeeld wordt slechts één item ingevoerd.

   ![Sectie Kenmerken met trefwoord zoeken](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.
1. Ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**en vernieuw de **[!UICONTROL Page Cache]**.

### Stap 3: Het tweede product toewijzen

1. In de _[!UICONTROL Products]_lijst, opent u de `Chaz Kangaroo Hoodie` (MH01) in bewerkingsmodus.
1. Omlaag schuiven en de **[!UICONTROL Attributes]** sectie.
1. In de **[!UICONTROL Search Keywords]** veld, de SKU voor het andere product invullen; `MJ03`.
1. Klik op **[!UICONTROL Save]**.
1. Ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**en vernieuw de **[!UICONTROL Page Cache]**.

### Stap 4: Test het in de winkel

1. Ga naar de winkel en voer `MJ03` in de _Snel zoeken_ doos.
1. Controleer of beide producten worden geretourneerd in de lijst met zoekresultaten.

## Gewogen zoekopdracht

Aan productkenmerken die zijn ingeschakeld voor zoeken in een catalogus, kan een gewicht worden toegewezen, zodat ze een hogere waarde krijgen in de zoekresultaten. Kenmerken met een groter gewicht worden geretourneerd vóór kenmerken met een lager gewicht. Als het systeem bijvoorbeeld twee kenmerken bevat, _kleur_ met een zoekgewicht van 3 en _beschrijving_ met een zoekgewicht van 1. Een zoekopdracht naar het woord _rood_ retourneert een lijst met producten met een waarde voor kleurkenmerken van `red` boven aan de zoekresultaten en retourneert producten met beschrijvingen die het woord bevatten _rood_ onder aan de zoekresultaten. In dit voorbeeld wordt `color` kenmerk heeft een groter gedefinieerd gewicht dan `description` kenmerk.

**_De eigenschappen voor de zoekdikte van een kenmerk instellen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Zoek het kenmerk in de lijst en open in de bewerkingsmodus.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Storefront Properties]** en voer de volgende handelingen uit:

   - Om de attributen in onderzoeksvragen te omvatten, plaats **[!UICONTROL Use in Search]** tot `Yes`.

   - Om de onderzoekswaarde van de attributen te vestigen, plaats **[!UICONTROL Search Weight]** naar een getal van 1 tot en met 10, waarbij `10` heeft de hoogste prioriteit. Als er geen waarde wordt ingevoerd, worden alle kenmerken standaard ingesteld op een zoekgewicht van `1`.

   ![Zoekdikte](./assets/search-weight.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Attribute]**.
