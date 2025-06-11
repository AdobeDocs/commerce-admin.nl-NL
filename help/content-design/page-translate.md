---
title: Een inhoudspagina vertalen
description: Leer hoe u een vertaalde versie van elke pagina maakt die beschikbaar is in de specifieke winkelweergave.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Een inhoudspagina vertalen

Als uw opslag veelvoudige meningen in verschillende [ talen ](../stores-purchase/store-localize.md) heeft, en u hebt de scène voor elke mening aan een verschillende taal geplaatst, is het resultaat een gedeeltelijk vertaalde plaats. De volgende stap bestaat uit het maken van een vertaalde versie van elke pagina die beschikbaar is in de specifieke winkelweergave. De kolom [!UICONTROL Store View] van de lijst _[!UICONTROL Manage Pages]_&#x200B;toont elke mening die een vertaalde versie van de pagina heeft.

Als u een inhoudspagina wilt vertalen, moet u een andere pagina maken die dezelfde URL-sleutel heeft als het origineel, maar die is toegewezen aan de specifieke opslagweergave. Werk vervolgens de pagina voor de specifieke weergave bij met de vertaalde tekst. Het volgende voorbeeld toont hoe te om tot een vertaalde versie van _Ongeveer de pagina van ons_ voor de Spaanse opslagmening te leiden.

## Stap 1: Kopieer de URL-sleutel voor de pagina die moet worden vertaald

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. In het net, vind de pagina die moet worden vertaald en open op _uitgeven_ wijze.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit en kopieer **[!UICONTROL URL Key]** aan het klembord.

1. Als u wilt terugkeren naar het _[!UICONTROL Pages]_-raster, klikt u op **[!UICONTROL Back]**&#x200B;in de bovenste knopbalk.

## Stap 2: Een pagina toevoegen voor de vertaalde inhoud

1. Klik op **[!UICONTROL Add New Page]**.

1. Voer de vertaalde **[!UICONTROL Page Title]** in.

1. Vouw ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie uit en voltooi de vertaalde tekst voor de pagina.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** sectie uit en doe het volgende:

   - Plak de **[!UICONTROL URL Key]** die u van de oorspronkelijke pagina hebt gekopieerd.

   - Voer de vertaalde tekst in voor de kolommen **[!UICONTROL Meta Title]** , **[!UICONTROL Meta Keywords]** en **[!UICONTROL Meta Description]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Page in Websites]** sectie uit en reeks **[!UICONTROL Store View]** aan de opslagmening waar de pagina beschikbaar moet zijn.

1. Vouw ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Design]** sectie uit en plaats de kolom **[!UICONTROL Layout]** van de pagina.

1. Klik op **[!UICONTROL Save]**.

1. Wanneer ertoe aangezet, vernieuw om het even welke ongeldige [ geheime voorgeheugens ](../systems/cache-management.md).

## Stap 3: De vertaling verifiëren

Ga naar de winkel en gebruik de taalkiezer om de winkelweergave te wijzigen om de vertaling te verifiëren.

Bericht dat er nog sommige elementen op de pagina zijn die zouden moeten worden vertaald, met inbegrip van de verbindingen van het bedrijffooter [ blok ](block-add.md), het [ welkome bericht ](../getting-started/storefront-branding.md#change-the-welcome-message), en [ productinformatie ](../stores-purchase/store-localize.md#localize-products).
