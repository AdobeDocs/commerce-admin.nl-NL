---
title: Productinstellingen - [!UICONTROL Search Engine Optimization]
description: Voor een product stellen de [!UICONTROL Search Engine Optimization] -instellingen de URL-sleutel en metagegevens in die door zoekprogramma's worden gebruikt om het product te indexeren.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Productinstellingen - [!UICONTROL Search Engine Optimization]

_de motoroptimalisering van het Onderzoek_ (SEO) is de praktijk van het verfijnen van de inhoud en de presentatie van een plaats om de manier te verbeteren de pagina&#39;s door onderzoeksmotoren worden geïndexeerd.

De _[!UICONTROL Search Engine Optimization]_montages voor een product specificeren de [ Sleutel URL ](catalog-urls.md) en [ meta- gegevens ](../merchandising-promotions/meta-data.md) gebieden die door onderzoeksmotoren worden gebruikt om het product te indexeren. Hoewel sommige zoekprogramma&#39;s metatrefwoorden negeren, blijven andere zoekprogramma&#39;s deze gebruiken. De huidige [ beste praktijken van SEO ](../merchandising-promotions/seo-overview.md) moet high-value sleutelwoorden in zowel de metattitel als meta beschrijving opnemen.

De standaardwaarde voor elk metagegevensveld kan automatisch worden gegenereerd op basis van de waarden die in de configuratie zijn opgegeven. Elk veld bevat een tijdelijke aanduiding die wordt vervangen door een werkelijke waarde. Voor meer informatie, zie {de gebieden van het 0} Product auto-Generatie ](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).[

## De SEO-velden invullen

1. Open het product in de bewerkingsmodus.

1. De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de _[!UICONTROL Search Engine Optimization]_sectie.

![ Optimalisering van de Motor van het Onderzoek ](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Voer de **[!UICONTROL URL Key]** (optioneel) in.

   De standaard-URL-sleutel is gebaseerd op de productnaam. U kunt de standaardinstelling gebruiken of deze desgewenst wijzigen. Voor meer informatie, zie [ Catalogus URLs ](catalog-urls.md).

1. Voer de **[!UICONTROL Meta Title]** (optioneel) in.

   De metatitel is de tekst die boven in het browservenster wordt weergegeven. U kunt de standaardinstelling gebruiken, die is gebaseerd op de productnaam, of deze desgewenst wijzigen.

1. Voeg de lus **[!UICONTROL Meta Keywords]** (optioneel) toe.

   De metatrefwoorden worden door sommige zoekmachines meer gebruikt dan door andere. U kunt het beste een paar zeer waardevolle trefwoorden invoeren om het product zichtbaarder te maken.

1. Voer de **[!UICONTROL Meta Description]** in.

   De meta-beschrijving is de tekst die in de lijsten van onderzoeksresultaten verschijnt. Voor het beste resultaat voert u een beschrijving in die tussen 150 en 160 tekens lang is.

## Veldverwijzing

| Veld | [ Reikwijdte ](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Winkelweergave | Bepaalt het online adres van het product. De URL-sleutel wordt toegevoegd aan de basis-URL van de winkel en wordt weergegeven in de adresbalk van een browser. Commerce creeert aanvankelijk a _onderzoekmachine-vriendschappelijke_ URL die op de productnaam gebaseerd is. De URL-sleutel moet bestaan uit kleine letters, met niet-afbreekstreepjes tussen deze tekens in plaats van spaties. Neem geen achtervoegsel zoals `.html` op in de URL-sleutel, omdat dit wordt beheerd in de configuratie. |
| [!UICONTROL Meta Title] | Winkelweergave | De titel wordt weergegeven in de titelbalk en het tabblad van uw browser en wordt ook gebruikt als de titel op de resultatenpagina van een zoekmachine (SERP). De titel van de meta zou uniek aan de pagina en minder dan 70 karakters in lengte moeten zijn. Automatisch gegenereerde waarde: `{{name}}` |
| [!UICONTROL Meta Keywords] | Winkelweergave | Relevante trefwoorden voor het product. Overweeg trefwoorden te gebruiken die klanten kunnen gebruiken om het product te zoeken. Automatisch gegenereerde waarde: `{{name}}` |
| [!UICONTROL Meta Description] | Winkelweergave | De meta-beschrijving geeft een kort overzicht van de pagina voor aanbiedingen met zoekresultaten. De ideale lengte ligt tussen 150 en 160 tekens, met een maximum van 255 tekens. Hoewel de klant dit niet kan zien, bevatten sommige zoekprogramma&#39;s de metagegevens op de pagina met zoekresultaten. Automatisch gegenereerde waarde: `{{name}} {{description}}` |

{style="table-layout:auto"}
