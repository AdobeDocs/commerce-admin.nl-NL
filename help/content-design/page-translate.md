---
title: Een inhoudspagina vertalen
description: Leer hoe u een vertaalde versie van elke pagina maakt die beschikbaar is in de specifieke winkelweergave.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Een inhoudspagina vertalen

Als uw winkel meerdere weergaven heeft in verschillende [talen](../stores-purchase/store-localize.md)en u hebt de landinstelling voor elke weergave ingesteld op een andere taal, is het resultaat een gedeeltelijk vertaalde site. De volgende stap bestaat uit het maken van een vertaalde versie van elke pagina die beschikbaar is in de specifieke winkelweergave. De [!UICONTROL Store View] kolom van de _[!UICONTROL Manage Pages]_wordt elke weergave weergegeven die een vertaalde versie van de pagina heeft.

Als u een inhoudspagina wilt vertalen, moet u een andere pagina maken die dezelfde URL-sleutel heeft als het origineel, maar die is toegewezen aan de specifieke opslagweergave. Werk vervolgens de pagina voor de specifieke weergave bij met de vertaalde tekst. In het volgende voorbeeld wordt getoond hoe u een vertaalde versie van het dialoogvenster _Over ons_ pagina voor de weergave van de Spaanse winkel.

## Stap 1: Kopieer de URL-sleutel voor de pagina die moet worden vertaald

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Zoek in het raster de pagina die u wilt vertalen en open in _bewerken_ -modus.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** en kopieer de **[!UICONTROL URL Key]** naar het klembord.

1. Als u wilt terugkeren naar de _[!UICONTROL Pages]_raster, klikken **[!UICONTROL Back]**in de bovenste knopbalk.

## Stap 2: Een pagina toevoegen voor de vertaalde inhoud

1. Klik op **[!UICONTROL Add New Page]**.

1. Voer de vertaalde gegevens in **[!UICONTROL Page Title]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Content]** en vult de vertaalde tekst voor de pagina in.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** en voer de volgende handelingen uit:

   - Plak de **[!UICONTROL URL Key]** die u van de originele pagina hebt gekopieerd.

   - Voer de vertaalde tekst in voor de **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, en **[!UICONTROL Meta Description]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Page in Websites]** sectie en set **[!UICONTROL Store View]** naar de winkelweergave waar de pagina beschikbaar moet zijn.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Design]** en stel de kolom in **[!UICONTROL Layout]** van de pagina.

1. Klik op **[!UICONTROL Save]**.

1. Vernieuw bij de aanwijzing alle ongeldige [caches](../systems/cache-management.md).

## Stap 3: De vertaling verifiëren

Ga naar de winkel en gebruik de taalkiezer om de winkelweergave te wijzigen om de vertaling te verifiëren.

Er zijn nog enkele elementen op de pagina die moeten worden vertaald, waaronder de voettekstkoppelingen van het bedrijf [blok](block-add.md)de [welkomstbericht](../getting-started/storefront-branding.md#change-the-welcome-message), en [productinformatie](../stores-purchase/store-localize.md#localize-products).
