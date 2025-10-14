---
title: Volgorde voor uitchecktotalen sorteren
description: Leer over het getoonde checkout totaal en hoe te om de orde van de de totalen van de controle in het ordesamenvatting te vormen.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Volgorde voor uitchecktotalen sorteren

Tijdens de controle van de bestelling wordt het totaal onder aan de bestelling weergegeven, met eventuele aanpassingen voor kortingen, verzendkosten, winkelkrediet en belasting. De orde van elk punt bepaalt de opeenvolging van de berekeningen, en in de configuratie door een aantal geplaatst dat aan elk punt wordt toegewezen. Het subtotaal is bijvoorbeeld het eerste item in de sectie en krijgt de waarde 10. Het Eindtotaal wordt als laatste weergegeven en krijgt de waarde 100 toegewezen. Aan alle andere items in de totalen wordt een waarde tussen deze waarden toegewezen.

![&#x200B; Samenvatting van de Orde toont het checkout totaal &#x200B;](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_om de de sorteervolgorde van de controletotalen te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de sectie **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Totals Sort Order]** sectie uit.

   ![&#x200B; de totalen van de Controle genummerde opties om de soortorde te bepalen &#x200B;](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie {de Volumes van de Controle 1} de Orde van de Soort in de _Gids van de Verwijzing van de Configuratie_.[&#128279;](../configuration-reference/sales/sales.md#checkout-totals-sort-order)

1. Als het plaatsen voor een specifieke opslagmening is, [&#x200B; kies de opslagmening &#x200B;](../configuration-reference/scope-change.md#set-the-scope) waar de configuratie van toepassing is.

   Klik op **[!UICONTROL OK]** als u daarom wordt gevraagd om door te gaan.

1. Om de orde in de _Totalen_ sectie te bepalen, verander het aantal dat aan elk punt wordt toegewezen.

   Hoe lager de waarde, hoe eerder de waarde in de lijst wordt geplaatst. In de standaardconfiguratie, is Subtotal (`10`) het eerste en Eindtotaal (`100`) het laatste.

   Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om deze wijzigingen te voltooien.

1. Klik op **[!UICONTROL Save Config]**.
