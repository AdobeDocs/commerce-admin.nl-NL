---
title: Categorieën - Inhoud-instellingen
description: Leer hoe u de [!UICONTROL Content] -instellingen gebruikt om aanvullende inhoud te definiëren die op de categoriepagina wordt weergegeven.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Categorieën - Inhoud-instellingen

De _[!UICONTROL Content]_-instellingen bepalen of er aanvullende inhoud op de categoriepagina wordt weergegeven. Naast de lijst met categorieproducten kan de pagina een afbeelding, beschrijving en CMS-blok bevatten. U kunt de inhoudsgereedschappen van [[!DNL Page Builder]](../page-builder/introduction.md) gebruiken om de categoriebeschrijving te definiëren.

## Categoriebeschrijving toevoegen in [!DNL Page Builder]

1. Open de categorie in de bewerkingsmodus.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Content]** sectie.

   ![&#x200B; inhoud van de Categorie &#x200B;](./assets/category-content.png){width="600" zoomable="yes"}

1. Klik rechtsboven in het **[!UICONTROL Description]** -gebied op **[!UICONTROL Edit with Page Builder]** .

1. Gebruik de [[!DNL Page Builder]](../page-builder/introduction.md) inhoudshulpmiddelen [&#x200B; om het even welke bestaande tekst &#x200B;](../page-builder/text.md) uit te geven en andere inhoud (indien nodig) toe te voegen.

## [!DNL Page Builder] voorvertoning

Wanneer u de _sectie van de Inhoud_ voor een bestaande categorie uitbreidt waar er inhoud die met [!DNL Page Builder] wordt gecreeerd is, toont het een voorproef van de **[!UICONTROL Description]** inhoud zoals het in de categoriepagina zou verschijnen. Als u op het inhoudsgebied klikt, wordt de [!DNL Page Builder] -werkruimte geopend waarin u de benodigde updates kunt uitvoeren.

![&#x200B; de voorproef van de Beschrijving &#x200B;](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Deze voorvertoning van inhoud is standaard ingeschakeld voor de product- en categorieformulieren. Als de prestaties te lijden hebben aan het laden van de voorproef, kunt u de voorproef in de [&#x200B; configuratie van het Beheer van de Inhoud &#x200B;](../configuration-reference/general/content-management.md#advanced-content-tools) montages onbruikbaar maken.

## Categoriebeschrijving toevoegen in editor

Typ alleen normale ASCII-tekens in het tekstvak. Als u tekst plakt van een tekstverwerker, slaat u deze eerst op als een gewoon TXT-bestand om onzichtbare besturingstekens te verwijderen.

Voor meer informatie, zie [&#x200B; redacteur WYSIWYG &#x200B;](../content-design/editor.md).

1. Open de categorie in de bewerkingsmodus.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Content]** sectie.

   ![&#x200B; inhoud van de Categorie &#x200B;](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Ga de categorie **[!UICONTROL Description]** in en gebruik de [&#x200B; redacteurstoolbar &#x200B;](../content-design/editor.md) om te formatteren zoals nodig.

   U kunt de rechterbenedenhoek slepen om de hoogte van het tekstvak te wijzigen.

## Een CMS-blok toevoegen aan de categoriepagina

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de categorie die u wilt bewerken.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie uit.

1. Selecteer bij **[!UICONTROL Add the CMS block]** een blok dat u wilt toevoegen.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Display Settings]** sectie uit.

1. Stel de **[!UICONTROL Display Mode]** in op een van de volgende opties:

   - `Static block only`
   - `Static block and products`

1. Klik na voltooiing op **[!UICONTROL Save]** en bekijk de blokweergave in de winkel (de cache moet worden vernieuwd).

## Content settings reference

| Instelling | [&#x200B; Reikwijdte &#x200B;](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Category Image] | Winkelweergave | Hiermee geeft u een afbeelding op die boven aan de categoriepagina wordt weergegeven. Methoden: <br/><br/>**[!UICONTROL Upload]**- Uploadt een afbeeldingsbestand van uw lokale computer naar de galerie en gebruikt dit als de categorieafbeelding.<br/><br/>**[!UICONTROL Select from Gallery]** - Hiermee wordt u gevraagd een bestaande afbeelding in de galerie te kiezen. <br/><br/>![&#x200B; het camerapictogram van de Bouwer van de Pagina &#x200B;](../assets/icon-camera.png) - of sleep een beelddossier aan de camerategel of doorblader aan het beeld en selecteer het van uw lokaal dossiersysteem. |
| [!UICONTROL Description] | Winkelweergave | Hiermee geeft u een beschrijving op die op de categoriepagina wordt weergegeven. <br/><br/>**[!UICONTROL Edit with Page Builder]**- opent de [[!DNL Page Builder]  werkruimte &#x200B;](../page-builder/workspace.md), waar u de beschrijving kunt uitgeven.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Hiermee schakelt u de weergave tussen de WYSIWYG-editor en de HTML-modus. |
| [!UICONTROL Add CMS Block] | Winkelweergave | Voegt een bestaand [&#x200B; blok CMS &#x200B;](../content-design/blocks.md) aan de categoriepagina toe. |

{style="table-layout:auto"}
