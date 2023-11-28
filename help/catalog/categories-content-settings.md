---
title: Categorieën - Inhoud-instellingen
description: Meer informatie over het gebruik van de [!UICONTROL Content] instellingen om aanvullende inhoud te definiëren die op de categoriepagina wordt weergegeven.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Categorieën - Inhoud-instellingen

De _[!UICONTROL Content]_bepalen de instellingen of er aanvullende inhoud op de categoriepagina wordt weergegeven. Naast de lijst met categorieproducten kan de pagina een afbeelding, beschrijving en CMS-blok bevatten. U kunt de [[!DNL Page Builder]](../page-builder/introduction.md) inhoudsgereedschappen om de categoriebeschrijving te definiëren.

## Voeg de categoriebeschrijving toe in [!DNL Page Builder]

1. Open de categorie in de bewerkingsmodus.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie.

   ![Categorie-inhoud](./assets/category-content.png){width="600" zoomable="yes"}

1. Rechtsboven in het dialoogvenster **[!UICONTROL Description]** gebied, klikken **[!UICONTROL Edit with Page Builder]**.

1. Gebruik de [[!DNL Page Builder]](../page-builder/introduction.md) inhoudsgereedschappen naar [bestaande tekst bewerken](../page-builder/text.md) en voeg andere inhoud toe (indien nodig).

## [!DNL Page Builder] voorvertoning

Wanneer u de _Inhoud_ sectie voor een bestaande categorie waarin inhoud is gemaakt met [!DNL Page Builder]wordt een voorvertoning van de **[!UICONTROL Description]** inhoud zoals deze op de categoriepagina wordt weergegeven. Als u op het inhoudsgebied klikt, wordt het dialoogvenster [!DNL Page Builder] waar u de benodigde updates kunt uitvoeren.

![Voorvertoning van beschrijving](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Deze voorvertoning van inhoud is standaard ingeschakeld voor de product- en categorieformulieren. Als de prestaties achterblijven bij het laden van de voorvertoning, kunt u de voorvertoning uitschakelen in het dialoogvenster [Configuratie van inhoudsbeheer](../configuration-reference/general/content-management.md#advanced-content-tools) instellingen.

## Categoriebeschrijving toevoegen in editor

Typ alleen normale ASCII-tekens in het tekstvak. Als u tekst plakt van een tekstverwerker, slaat u deze eerst op als een gewoon TXT-bestand om onzichtbare besturingstekens te verwijderen.

Zie voor meer informatie [WYSIWYG-editor](../content-design/editor.md).

1. Open de categorie in de bewerkingsmodus.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie.

   ![Categorie-inhoud](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Voer de categorie in **[!UICONTROL Description]** en gebruiken de [editor-werkbalk](../content-design/editor.md) naar wens op te maken.

   U kunt de rechterbenedenhoek slepen om de hoogte van het tekstvak te wijzigen.

## Een CMS-blok toevoegen aan de categoriepagina

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de categorie die u wilt bewerken.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie.

1. Voor **[!UICONTROL Add the CMS block]** selecteert u een blok dat u wilt toevoegen.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Display Settings]** sectie.

1. Stel de **[!UICONTROL Display Mode]** op een van de volgende wijzen:

   - `Static block only`
   - `Static block and products`

1. Klik op **[!UICONTROL Save]** en bekijk de blokweergave op de winkel (cache moet worden vernieuwd).

## Content settings reference

| Instelling | [Toepassingsgebied](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Category Image] | Winkelweergave | Hiermee geeft u een afbeelding op die boven aan de categoriepagina wordt weergegeven. Methoden: <br/><br/>**[!UICONTROL Upload]**- Uploadt een afbeeldingsbestand van uw lokale computer naar de galerie en gebruikt dit als de categorieafbeelding.<br/><br/>**[!UICONTROL Select from Gallery]** - Hiermee wordt u gevraagd een bestaande afbeelding in de galerie te kiezen. <br/><br/>![Page Builder-camerapictogram](../assets/icon-camera.png) - Sleep een afbeeldingsbestand naar het camerablok of blader naar de afbeelding en selecteer deze in het lokale bestandssysteem. |
| [!UICONTROL Description] | Winkelweergave | Hiermee geeft u een beschrijving op die op de categoriepagina wordt weergegeven. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Opent de [[!DNL Page Builder] werkruimte](../page-builder/workspace.md), waar u de beschrijving kunt bewerken.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Hiermee schakelt u de weergave tussen de modi WYSIWYG Editor en HTML in. |
| [!UICONTROL Add CMS Block] | Winkelweergave | Hiermee voegt u een bestaande [CMS-blok](../content-design/blocks.md) op de rubriekpagina. |

{style="table-layout:auto"}
