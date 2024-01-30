---
title: Zoektermen beheren
description: Leer hoe u de zoektermen voor uw winkel beheert om klanten om te leiden met verkeerd gespelde of alternatieve termen.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 3851258543ba829a4bdbfdb5d3d053ec4627184a
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Zoektermen beheren

De [landingspagina](../content-design/pages.md) voor een zoekterm kan dit een inhoudspagina, een categoriepagina, een pagina met productdetails of zelfs een pagina op een andere site zijn.

Gebruik zoektermen om veelvoorkomende spelfouten vast te leggen en deze om te leiden naar de juiste pagina. Als je bijvoorbeeld ijzergeduldig meubilair verkoopt, weet je dat veel mensen de term verkeerd spellen als _gietijzer_, of zelfs _rotijzer_. U kunt elk verkeerd gespeld woord invoeren als zoekterm en deze synoniemen maken voor _ruw ijzer_. Hoewel het woord verkeerd is gespeld, wordt de zoekopdracht naar de pagina gestuurd voor ruw ijzer.

U kunt ook leren wat uw klanten zoeken door de zoektermen te bekijken die zij gebruiken om producten in uw winkel te zoeken. Als er voldoende mensen zijn die op zoek zijn naar een product dat niet in uw catalogus staat, kan dit wijzen op een verkoopmogelijkheid. In plaats van ze leeg te laten, kunt u ze nu doorsturen naar een ander product in uw catalogus.

## Zoektermen toevoegen

Terwijl u nieuwe woorden leert die mensen gebruiken om in uw winkel te zoeken, kunt u deze toevoegen aan de lijst met zoektermen om mensen naar de meest overeenkomende producten in uw catalogus te leiden.

![Het raster Zoektermen](./assets/search-terms.png){width="700" zoomable="yes"}

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Search Query] | De query die wordt gebruikt om de zoekopdracht uit te voeren. |
| [!UICONTROL Store] | De winkel waarop de zoekquery is toegepast. |
| [!UICONTROL Results] | Aantal resultaten gevonden door query. |
| [!UICONTROL Uses] | Aantal toepassingen. |
| [!UICONTROL Redirect URL] | URL van de doelpagina waarop de gebruiker na het uitvoeren van de zoekopdracht is omgeleid. |
| [!UICONTROL Suggested Terms] | Bepaalt als het vraagresultaat voorgestelde termijnen toont. |
| [!UICONTROL Actions] | Opent het product in Edit wijze. |

{style="table-layout:auto"}

>[!NOTE]
>
>Het aantal resultaten wordt bijgewerkt telkens wanneer een winkelier een zoekopdracht uitvoert met deze zoekquery. Deze wordt niet bijgewerkt als een van de producten wordt gewijzigd of verwijderd.

### Een zoekterm toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Klik op **[!UICONTROL Add New Search Term]**.

   ![Algemene informatie over termen zoeken](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. Onder _[!UICONTROL General Information]_in de **[!UICONTROL Search Query]**voert u het woord of de woordgroep in die u als een nieuwe zoekterm wilt toevoegen.

1. Als uw winkel in meerdere talen beschikbaar is, kiest u de optie **[!UICONTROL Store]** weergeven.

1. Als u de zoekresultaten wilt doorsturen naar een andere pagina in uw winkel of naar een andere website, voert u de volledige URL van de doelpagina in het dialoogvenster **[!UICONTROL Redirect URL]** veld.

1. Als u wilt dat deze term beschikbaar is voor gebruik als suggestie wanneer een zoekopdracht geen resultaten oplevert, stelt u **[!UICONTROL Display in Suggested Terms]** tot `Yes`.

1. Klik op **[!UICONTROL Save Search]**.

## Een zoekterm bewerken

1. In de _[!UICONTROL Search Terms]_, klikt u op de rij van records om de zoekterm in de bewerkingsmodus te openen.

1. Breng de gewenste wijzigingen aan.

1. Klik op **[!UICONTROL Save Search]**.

## Een zoekterm verwijderen

Er zijn twee methoden om een zoekterm te verwijderen: uit het raster en op de bewerkingspagina.

**Methode 1:** In de _[!UICONTROL Search Terms]_raster

1. Selecteer in de lijst het selectievakje van de term die u wilt verwijderen.

1. In de linkerbovenhoek van de lijst stelt u **[!UICONTROL Actions]** tot `Delete`.

1. Klik op **[!UICONTROL Submit]**.

**Methode 2:** Op de _[!UICONTROL Edit a Search Term]_page

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Zoek de zoekterm die u wilt verwijderen en open deze in de bewerkingsmodus.

1. Klik op **[!UICONTROL Delete Search]**.

1. Klik op **[!UICONTROL OK]**.

## Populaire zoektermen

De _Zoekvoorwaarden_ de koppeling in de voettekst van uw winkel geeft de zoektermen weer die bezoekers gebruiken in uw winkel, gerangschikt op populariteit. Zoektermen worden weergegeven in een _tagcloud_ opmaak, waarbij de grootte van de tekst de populariteit van de term aangeeft.

Standaard zijn de algemene zoektermen ingeschakeld als een gereedschap voor optimalisatie van zoekprogramma&#39;s, maar er is geen directe verbinding met het zoekproces van de catalogus. Omdat de pagina Zoekvoorwaarden wordt geïndexeerd door zoekmachines, kunnen termen op de pagina de positie van je zoekmachine en de zichtbaarheid van je winkel verbeteren. De URL van de pagina Populaire zoektermen is: `mystore.com/search/term/popular/`

![Voorbeeld van een winkel - populaire zoektermen](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_Veelgebruikte zoektermen configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie.

   ![Catalogusconfiguratie - optimalisatie zoekprogramma](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [Optimalisatie zoekmachine](../configuration-reference/catalog/catalog.md#search-engine-optimization) in de _Configuratieverwijzing_.

1. Set **[!UICONTROL Popular Search Terms]** indien nodig.

   Wis indien nodig de **[!UICONTROL Use system value]** Schakel dit selectievakje in om deze instelling te wijzigen.

1. Klik op **[!UICONTROL Save Config]**.

>[!NOTE]
>
>U kunt het in cache plaatsen van populaire [cataloguszoekopdrachten](search-configuration.md).

## Synoniemen zoeken

Een manier om de doeltreffendheid van [cataloguszoekopdracht](search-configuration.md) moet verschillende termen bevatten die mensen kunnen gebruiken om hetzelfde item te beschrijven. Je wilt een uitverkoop niet verliezen alleen omdat iemand op zoek is naar een _sofa_ en je product wordt aangeboden als een _bank_. U kunt een breder bereik van zoektermen vastleggen door de zoektermen in te voeren _sofa_, _davenport_, en _lovesisch_ als synoniemen voor _bank_ en stuurt ze naar dezelfde landingspagina.

Adobe Commerce ondersteunt twee verschillende oplossingen voor synoniem beheer:

- Live zoeken [Synoniemen](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) is beschikbaar voor Adobe Commerce-installaties waarop Live Search is geïnstalleerd.
- De standaardfunctie Synonyms zoeken (die in deze pagina wordt beschreven) is beschikbaar in alle Adobe Commerce-installaties.

>[!NOTE]
>
>De standaardfunctie Synonyms zoeken biedt ondersteuning voor de box `name` en `sku` productkenmerken **_alleen_**.

>[!IMPORTANT]
>
>De zoeksynoniemenfunctie gebruikt alleen een zoekmethode met volledige tekst die overeenkomt.

![Voorbeeld van storefront - zoekresultaten met synoniemen](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Een synoniem maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   De _[!UICONTROL Search Synonyms]_wordt weergegeven. Als het de eerste keer is dat u zoeksynoniemen hebt gebruikt, is het raster leeg.

   ![Synoniemenraster zoeken](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL New Synonym Group]**.

   ![Nieuwe groep met zoeksynoniemen](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Set **[!UICONTROL Scope]** op de opslagweergaven waarop de synoniemen van toepassing zijn.

1. Voer elk synoniem in de groep in, gescheiden door komma&#39;s. Kies woorden die mensen kunnen gebruiken als zoekcriteria. Bijvoorbeeld:

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Als u deze synoniemen wilt samenvoegen in een groep met andere synoniemen met hetzelfde bereik, selecteert u de optie **[!UICONTROL Merge existing synonyms]** selectievakje.

1. Klik op **[!UICONTROL Save Synonym Group]**.

### Een synoniem-groep bewerken

1. In de _[!UICONTROL Search Synonyms]_, klikt u op de rij van records om de synoniem groep te openen in de bewerkingsmodus.

1. Breng de gewenste wijzigingen aan.

1. Klik op **[!UICONTROL Save Synonym Group]**.

### Een synoniem-groep verwijderen

Er zijn twee methoden voor het verwijderen van een synoniemengroep: uit het raster en op de bewerkingspagina.

**Methode 1:** In het raster Synoniemen zoeken

1. In de _[!UICONTROL Search Synonyms]_, schakelt u het selectievakje in van de groep die u wilt verwijderen.

1. In de linkerbovenhoek van de lijst stelt u **[!UICONTROL Actions]** tot `Delete`.

1. Klik op **[!UICONTROL Submit]**.

**Methode 2:** Op de pagina Een symboolgroep bewerken

1. Klik in het raster Synoniemen zoeken op de rij met alle records om de synoniem groep te openen in de bewerkingsmodus.

1. Klik op **[!UICONTROL Delete Synonym Group]**.

1. Bevestig desgevraagd of de groep is verwijderd.

## Rapport met zoektermen

Het rapport Zoektermen toont het aantal resultaten voor elke term en het aantal keren dat de term is gebruikt. De rapportgegevens kunnen op termijn, opslag, resultaten, en klusjes worden gefiltreerd, en voor verdere analyse worden uitgevoerd.

### Het rapport weergeven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Gebruik de besturingselementen om het rapport naar wens te filteren.

   ![Rapport met zoektermen](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Het rapport exporteren

1. Voor **[!UICONTROL Export to]** kiest u een exportindeling:

   - `CSV` - Een bestand met door komma&#39;s gescheiden waarden dat normale tekstgegevens bevat
   - `Excel XML` - Een op XML gebaseerde indeling voor spreadsheetgegevens

1. Klik op **[!UICONTROL Export]**.

   Het gegenereerde bestand wordt automatisch voor downloads opgeslagen in de door u aangewezen map.

### Kolommen rapporteren

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Unieke, numerieke id gegenereerd voor het zoekterm-item |
| [!UICONTROL Search Query] | De query die wordt gebruikt om de zoekopdracht uit te voeren |
| [!UICONTROL Store] | De winkel waar de zoekquery is toegepast |
| [!UICONTROL Results] | Aantal resultaten |
| [!UICONTROL Hits] | Aantal toepassingen |

{style="table-layout:auto"}
