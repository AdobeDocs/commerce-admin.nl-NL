---
title: Automatische omleidingen
description: Meer informatie over het configureren van automatische omleidingen die worden gegenereerd wanneer de URL-sleutel van een product of categorie wordt gewijzigd in uw Commerce-winkel.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Automatische omleidingen

Je winkel kan worden geconfigureerd om automatisch een permanente omleiding te genereren wanneer de URL-sleutel van een product of categorie verandert. In het gedeelte Zoekmachineoptimalisatie geeft het selectievakje onder de URL-sleutel aan of permanente omleidingen zijn ingeschakeld. Als uw winkel al is geconfigureerd om catalogus-URL&#39;s automatisch om te leiden, is omleiding een eenvoudige update van de URL-sleutel. Het proces voor het maken van een automatische omleiding is hetzelfde voor zowel producten als categorieën.

>[!NOTE]
>
>Wanneer automatische omleidingen zijn ingeschakeld en u een categorie opslaat, worden alle herschrijvingen van producten en categorieën in realtime gegenereerd en standaard opgeslagen in databasetabellen. Dit kan leiden tot aanzienlijke prestatieproblemen voor categorieën waaraan veel producten zijn toegewezen. De oplossing is om deze standaard te wijzigen en het genereren van URL-herschrijvingen van categorieën/producten voor producten op categorie Save over te slaan. In dit geval worden productherschrijvingen alleen gegenereerd voor de canonieke product-URL.

## Automatische omleidingen instellen

1. Ga in de _zijbalk voor beheerders_ naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

   ![ configuratie van de Catalogus - de optimalisering van de onderzoeksmotor ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.


>[!NOTE]
>
> URL herschrijft kan voor de archiefmening of het websitewerkingsgebied worden geproduceerd. Stel het bereik voor het herschrijven van de URL in via Beheer op **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Selecteer het bereik in het veld_[!UICONTROL Product URL Rewrite Scope]_ .

## product-URL&#39;s automatisch doorsturen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek het product in de lijst en klik om de record te openen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit.

   ![Productzoekmachineoptimalisatie - permanente redirect](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Ga als **[!UICONTROL URL Key]** volgt te werk:

   - Zorg ervoor dat het **[!UICONTROL Create Permanent Redirect for old URL]** selectievakje is ingeschakeld. Als dit niet het geval is, volgt u de instructies om automatische omleidingen](url-rewrite.md#configure-url-rewrites) in te [schakelen.

   - Werk **[!UICONTROL URL Key]** zo nodig bij met kleine letters en niet-afbreekstreepjes tussen deze tekens in plaats van spaties.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

1. Wanneer u wordt gevraagd om de cache te vernieuwen, volgt u de koppelingen in het bericht boven aan de werkruimte.

   De permanente omleiding is nu van kracht voor het product en alle bijbehorende categorie-URL&#39;s.

## Categorie-URL&#39;s automatisch omleiden

1. Ga in de _zijbalk voor beheerders_ naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Zoek de categorie in de boom en klik om het record te openen.

1. Vouw de uitbreidingskiezer de](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]** sectie uit![.

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

1. Vouw de uitbreidingskiezer de](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]** sectie uit![.

1. Stel in **[!UICONTROL Generate "category/product" URL Rewrites]** op `No`.

1. Klik in het bevestigingsvenster om **[!UICONTROL OK]** de wijziging en de verwijdering van bestaande URL-herschrijvingen te bevestigen.

   ![ Draai van categorie/productURL herschrijft - bevestigt ](./assets/seo-rewrite-off.png){width="350"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
