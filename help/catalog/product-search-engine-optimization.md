---
title: Productinstellingen - [!UICONTROL Search Engine Optimization]
description: Voor een product geldt het [!UICONTROL Search Engine Optimization] Met instellingen worden de URL-sleutel- en metagegevens ingesteld die door zoekprogramma's worden gebruikt om het product te indexeren.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Productinstellingen - [!UICONTROL Search Engine Optimization]

_Zoekmachine optimaliseren_ (SEO) is de praktijk om de inhoud en presentatie van een site te verfijnen om de manier waarop de pagina&#39;s door zoekmachines worden geïndexeerd te verbeteren.

De _[!UICONTROL Search Engine Optimization]_instellingen voor een product opgeven [URL-sleutel](catalog-urls.md) en [metagegevens](../merchandising-promotions/meta-data.md) velden die door zoekprogramma&#39;s worden gebruikt om het product te indexeren. Hoewel sommige zoekprogramma&#39;s metatrefwoorden negeren, blijven andere zoekprogramma&#39;s deze gebruiken. De huidige [Best practices voor SEO](../merchandising-promotions/seo-overview.md) moet hoogwaardetrefwoorden in zowel de metattitel als de meta- beschrijving opnemen.

De standaardwaarde voor elk metagegevensveld kan automatisch worden gegenereerd op basis van de waarden die in de configuratie zijn opgegeven. Elk veld bevat een tijdelijke aanduiding die wordt vervangen door een werkelijke waarde. Zie voor meer informatie [Productvelden automatisch genereren](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

## De SEO-velden invullen

1. Open het product in de bewerkingsmodus.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Search Engine Optimization]_sectie.

![Optimalisatie zoekmachine](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Voer de **[!UICONTROL URL Key]** (optioneel).

   De standaard-URL-sleutel is gebaseerd op de productnaam. U kunt de standaardinstelling gebruiken of deze desgewenst wijzigen. Zie voor meer informatie [Catalogus-URL&#39;s](catalog-urls.md).

1. Voer de **[!UICONTROL Meta Title]** (optioneel).

   De metatitel is de tekst die boven in het browservenster wordt weergegeven. U kunt de standaardinstelling gebruiken, die is gebaseerd op de productnaam, of deze desgewenst wijzigen.

1. Voeg de **[!UICONTROL Meta Keywords]** (optioneel).

   De metatrefwoorden worden door sommige zoekmachines meer gebruikt dan door andere. U kunt het beste een paar zeer waardevolle trefwoorden invoeren om het product zichtbaarder te maken.

1. Voer de **[!UICONTROL Meta Description]**.

   De meta-beschrijving is de tekst die in de lijsten van onderzoeksresultaten verschijnt. Voor het beste resultaat voert u een beschrijving in die tussen 150 en 160 tekens lang is.

## Veldverwijzing

| Veld | [Toepassingsgebied](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Winkelweergave | Bepaalt het online adres van het product. De URL-sleutel wordt toegevoegd aan de basis-URL van de winkel en wordt weergegeven in de adresbalk van een browser. De handel leidt aanvankelijk tot een _zoekmachinevriendelijk_ URL die is gebaseerd op de productnaam. De URL-sleutel moet bestaan uit kleine letters, met niet-afbreekstreepjes tussen deze tekens in plaats van spaties. Geen achtervoegsel zoals `.html` in de Sleutel URL, omdat het in de configuratie wordt beheerd. |
| [!UICONTROL Meta Title] | Winkelweergave | De titel wordt weergegeven in de titelbalk en het tabblad van uw browser en wordt ook gebruikt als de titel op de resultatenpagina van een zoekmachine (SERP). De titel van de meta zou uniek aan de pagina en minder dan 70 karakters in lengte moeten zijn. Automatisch gegenereerde waarde: `{{name}}` |
| [!UICONTROL Meta Keywords] | Winkelweergave | Relevante trefwoorden voor het product. Overweeg trefwoorden te gebruiken die klanten kunnen gebruiken om het product te zoeken. Automatisch gegenereerde waarde: `{{name}}` |
| [!UICONTROL Meta Description] | Winkelweergave | De meta-beschrijving geeft een kort overzicht van de pagina voor aanbiedingen met zoekresultaten. De ideale lengte ligt tussen 150 en 160 tekens, met een maximum van 255 tekens. Hoewel de klant dit niet kan zien, bevatten sommige zoekprogramma&#39;s de metagegevens op de pagina met zoekresultaten. Automatisch gegenereerde waarde: `{{name}} {{description}}` |

{style="table-layout:auto"}
