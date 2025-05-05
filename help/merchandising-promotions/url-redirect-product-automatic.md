---
title: Automatische omleidingen
description: Leer hoe u automatische omleidingen configureert die worden gegenereerd wanneer de URL-sleutel van een product of categorie wordt gewijzigd in uw Commerce-winkel.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Automatische omleidingen

Uw winkel kan zo worden geconfigureerd dat automatisch een permanente omleiding wordt gegenereerd wanneer de URL-sleutel van een product of categorie verandert. In de sectie van de Optimalisering van de Motor van het Onderzoek, checkbox onder de sleutel URL wijst op als de permanente omleidingen worden toegelaten. Als uw winkel al is geconfigureerd om catalogus-URL&#39;s automatisch om te leiden, is omleiding een eenvoudige update van de URL-sleutel. Het proces voor het maken van automatische omleiding is hetzelfde voor zowel producten als categorieën.

>[!NOTE]
>
>Wanneer automatische omleidingen zijn ingeschakeld en u een categorie opslaat, worden alle product- en categorieherschrijvingen in real-time gegenereerd en standaard in databasetabellen opgeslagen. Dit kan leiden tot aanzienlijke prestatieproblemen voor categorieën met veel toegewezen producten. De oplossing is om deze standaard te wijzigen en het genereren van een categorie/producten-URL voor herschrijvingen van producten op de categorie Opslaan over te slaan. In dit geval worden herschrijfbewerkingen van het product alleen gegenereerd voor de URL van het canonieke product.

## Automatische omleidingen instellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

   ![ configuratie van de Catalogus - de optimalisering van de onderzoeksmotor ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.


>[!NOTE]
>
> URL herschrijft kan voor de archiefmening of het websitewerkingsgebied worden geproduceerd. Stel het bereik voor het herschrijven van de URL in via Beheer op **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Selecteer het bereik in het veld&#x200B;_[!UICONTROL Product URL Rewrite Scope]_ .

## product-URL&#39;s automatisch doorsturen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek het product in de lijst en klik om de record te openen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

   ![ de optimalisering van het het onderzoekscentrum van het Product - permanent opnieuw richt ](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Voer voor **[!UICONTROL URL Key]** de volgende handelingen uit:

   - Controleer of het selectievakje **[!UICONTROL Create Permanent Redirect for old URL]** is ingeschakeld. Als niet, volg de instructies om [ toe te laten automatisch opnieuw richt ](url-rewrite.md#configure-url-rewrites).

   - Werk **[!UICONTROL URL Key]** zo nodig bij met kleine letters en niet-afbreekstreepjes tussen deze tekens in plaats van spaties.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, volg de verbindingen in het bericht bij de bovenkant van de werkruimte.

   De permanente omleiding is nu van kracht voor het product en om het even welke bijbehorende categorie URLs.

## Categorie-URL&#39;s automatisch doorsturen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Zoek de categorie in de structuur en klik om de record te openen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

1. Voer voor **[!UICONTROL URL Key]** de volgende handelingen uit:

   - Controleer of het selectievakje **[!UICONTROL Create Permanent Redirect for old URL]** is ingeschakeld. Als niet, volg de instructies om [ toe te laten automatisch opnieuw richt ](url-rewrite.md#configure-url-rewrites).

   - Werk **[!UICONTROL URL Key]** zo nodig bij met kleine letters en niet-afbreekstreepjes tussen deze tekens in plaats van spaties.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, volg de verbindingen in het bericht bij de bovenkant van de werkruimte.

   De permanente omleiding is nu van kracht voor de categorie en alle bijbehorende product-URL&#39;s.

## Genereren van product-URL herschrijft voor opslaan van categorie overslaan {#skip-rewrite}

>[!WARNING]
>
>Als u de URL voor het automatisch genereren van categorieën/producten uitschakelt, wordt de bestaande URL voor de categorie/het producttype permanent verwijderd. Deze URL kan niet worden hersteld. Dit kan mogelijk leiden tot onopgeloste URL-conflicten tussen categorieën/producttypen waarvoor een handmatige update van de URL-sleutel nodig is om deze op te lossen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

1. Stel **[!UICONTROL Generate "category/product" URL Rewrites]** in op `No` .

1. Klik in het bevestigingsdialoogvenster op **[!UICONTROL OK]** om de wijziging te bevestigen en de bestaande URL te verwijderen.

   ![ Draai van categorie/productURL herschrijft - bevestigt ](./assets/seo-rewrite-off.png){width="350"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
