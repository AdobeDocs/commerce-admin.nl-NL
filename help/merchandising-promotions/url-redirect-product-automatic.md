---
title: Automatische omleidingen
description: Leer hoe u automatische omleidingen configureert die moeten worden gegenereerd wanneer de URL-sleutel van een product of categorie wordt gewijzigd in uw winkel Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Automatische omleidingen

Uw winkel kan zo worden geconfigureerd dat automatisch een permanente omleiding wordt gegenereerd wanneer de URL-sleutel van een product of categorie verandert. In de sectie van de Optimalisering van de Motor van het Onderzoek, checkbox onder de sleutel URL wijst op als de permanente omleidingen worden toegelaten. Als uw winkel al is geconfigureerd om catalogus-URL&#39;s automatisch om te leiden, is omleiding een eenvoudige update van de URL-sleutel. Het proces voor het maken van automatische omleiding is hetzelfde voor zowel producten als categorieën.

>[!NOTE]
>
>Wanneer automatische omleidingen zijn ingeschakeld en u een categorie opslaat, worden alle product- en categorieherschrijvingen in real-time gegenereerd en standaard in databasetabellen opgeslagen. Dit kan leiden tot aanzienlijke prestatieproblemen voor categorieën met veel toegewezen producten. De oplossing is om deze standaard te wijzigen en het genereren van een categorie/producten-URL voor herschrijvingen van producten op de categorie Opslaan over te slaan. In dit geval worden herschrijfbewerkingen van het product alleen gegenereerd voor de URL van het canonieke product.

## Automatische omleidingen instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie.

   ![Catalogusconfiguratie - optimalisatie zoekprogramma](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.

## product-URL&#39;s automatisch doorsturen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek het product in de lijst en klik om de record te openen.

1. Uitbreiden ![Expansiekiezer ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie.

   ![Optimalisatie van zoekmachines voor producten - permanent omleiden](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Voor **[!UICONTROL URL Key]** Ga als volgt te werk:

   - Zorg ervoor dat de **[!UICONTROL Create Permanent Redirect for old URL]** selectievakje is ingeschakeld. Indien niet, volg de instructies op [automatische omleidingen inschakelen](url-rewrite.md#configure-url-rewrites).

   - Werk de **[!UICONTROL URL Key]** indien nodig, met kleine letters en niet-afbreekstreepjes tussen deze tekens in plaats van spaties.

1. Klik op **[!UICONTROL Save]**.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, volg de verbindingen in het bericht bij de bovenkant van de werkruimte.

   De permanente omleiding is nu van kracht voor het product en om het even welke bijbehorende categorie URLs.

## Categorie-URL&#39;s automatisch doorsturen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Zoek de categorie in de structuur en klik om de record te openen.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie.

1. Voor **[!UICONTROL URL Key]** Ga als volgt te werk:

   - Zorg ervoor dat de **[!UICONTROL Create Permanent Redirect for old URL]** selectievakje is ingeschakeld. Indien niet, volg de instructies op [automatische omleidingen inschakelen](url-rewrite.md#configure-url-rewrites).

   - Werk de **[!UICONTROL URL Key]** indien nodig, met kleine letters en niet-afbreekstreepjes tussen deze tekens in plaats van spaties.

1. Klik op **[!UICONTROL Save]**.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, volg de verbindingen in het bericht bij de bovenkant van de werkruimte.

   De permanente omleiding is nu van kracht voor de categorie en alle bijbehorende product-URL&#39;s.

## Genereren van product-URL herschrijft voor opslaan van categorie overslaan {#skip-rewrite}

>[!WARNING]
>
>Als u de URL voor het automatisch genereren van categorieën/producten uitschakelt, wordt de bestaande URL voor de categorie/het producttype permanent verwijderd. Deze URL kan niet worden hersteld. Dit kan mogelijk leiden tot onopgeloste URL-conflicten tussen categorieën/producttypen waarvoor een handmatige update van de URL-sleutel nodig is om deze op te lossen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie.

1. Set **[!UICONTROL Generate "category/product" URL Rewrites]** tot `No`.

1. Klik in het bevestigingsdialoogvenster op **[!UICONTROL OK]** om de wijziging en verwijdering van bestaande URL te bevestigen.

   ![Herschrijvingen van categorie/product-URL uitschakelen - bevestigen](./assets/seo-rewrite-off.png){width="350"}

1. Klik op **[!UICONTROL Save Config]**.
