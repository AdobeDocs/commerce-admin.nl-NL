---
title: Geplande orderactiviteiten
description: Leer meer over de geplande bestelbewerkingen en bestellingen die deze functionaliteit ondersteunen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Geplande orderactiviteiten

De banen van het gebruik [ Gewas ](../systems/cron.md) om de volgende taken van de ordeverwerking te plannen:

![ het net van Orden ](./assets/orders-grid.png){width="700" zoomable="yes"}

## Levensduur betalingsopdracht instellen

Het leven van orden met hangende betalingen wordt bepaald door de _configuratie van de Montages van het Gewas van 0&rbrace; Orden &lbrace;._ De standaardwaarde is 480 minuten, namelijk 8 uur.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de sectie **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Orders Cron Settings]** sectie uit.

   ![ orden de Montages van het Gewas ](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Voer voor **[!UICONTROL Pending Payment Order Lifetime (minutes)]** het aantal minuten in voordat een in behandeling zijnde betaling verloopt.

1. Klik op **[!UICONTROL Save Config]**.

## Updates en opnieuw indexeren van het geplande raster inschakelen

De de configuratieschema&#39;s van de Montages van het Net werken aan de volgende ordebeheernetten bij, en herdexeert de gegevens zoals die door [ Gewas ](../systems/cron.md) worden gepland:

- [Orders](orders.md#orders-workspace)
- [Facturen](invoices.md)
- [Overbrengingen](shipments.md)
- [Creditnota&#39;s](credit-memos.md)

Door deze taken te plannen, kunt u de sloten vermijden die voorkomen wanneer het gegeven wordt bewaard en verwerkingstijd verminderen. Wanneer deze optie is ingeschakeld, vinden updates alleen plaats tijdens de geplande uitsnijdtaak. Voor beste resultaten, zou het Gewas moeten worden gevormd om eens per minuut in werking te stellen.

**_om de updates en het opnieuw indexeren toe te laten:_**

Wanneer [ de wijze van de Productie ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=nl-NL#production-mode) (de standaardwijze die in Adobe Commerce op wolkeninfrastructuur wordt gebruikt) wordt toegelaten, stel het volgende bevel in werking:

``bin/magento config:set dev/grid/async_indexing 1``

Wanneer [ Standaardwijze ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=nl-NL#default-mode) wordt toegelaten, voltooi de volgende stappen:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de sectie **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Developer]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Grid Settings]** sectie uit.

1. Stel **[!UICONTROL Asynchronous Indexing]** in op `Enable` .

   ![ de Montages van het Net ](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
