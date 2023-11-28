---
title: Geplande orderactiviteiten
description: Leer meer over de geplande bestelbewerkingen en bestellingen die deze functionaliteit ondersteunen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Geplande orderactiviteiten

Gebruiken [Cron](../systems/cron.md) taken om de volgende taken voor orderverwerking te plannen:

![Raster voor bestellingen](./assets/orders-grid.png){width="700" zoomable="yes"}

## Levensduur betalingsopdracht instellen

De looptijd van orders met lopende betalingen wordt bepaald door de _Instellingen voor het uitsnijden van bestellingen_ configuratie. De standaardwaarde is 480 minuten, namelijk 8 uur.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Orders Cron Settings]** sectie.

   ![Instellingen voor het uitsnijden van bestellingen](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Voor **[!UICONTROL Pending Payment Order Lifetime (minutes)]** Voer het aantal minuten in voordat een betaling in behandeling verloopt.

1. Klik op **[!UICONTROL Save Config]**.

## Updates en opnieuw indexeren van het geplande raster inschakelen

De de configuratieschema&#39;s van de Montages van het Net werken aan de volgende ordebeheernetten bij, en herdexeert de gegevens zoals gepland door [Cron](../systems/cron.md):

- [Orders](orders.md#orders-workspace)
- [Facturen](invoices.md)
- [Overbrengingen](shipments.md)
- [Creditnota&#39;s](credit-memos.md)

Door deze taken te plannen, kunt u de sloten vermijden die voorkomen wanneer het gegeven wordt bewaard en verwerkingstijd verminderen. Wanneer deze optie is ingeschakeld, vinden updates alleen plaats tijdens de geplande uitsnijdtaak. Voor beste resultaten, zou het Gewas moeten worden gevormd om eens per minuut in werking te stellen.

**_De updates en opnieuw indexeren inschakelen:_**

Wanneer [Productiemodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (de standaardmodus die wordt gebruikt in Adobe Commerce op de cloudinfrastructuur) wordt ingeschakeld, voert u de volgende opdracht uit:

``bin/magento config:set dev/grid/async_indexing 1``

Wanneer [Standaardmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) is ingeschakeld, voert u de volgende stappen uit:

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Developer]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Grid Settings]** sectie.

1. Set **[!UICONTROL Asynchronous Indexing]** tot `Enable`.

   ![Rasterinstellingen](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
