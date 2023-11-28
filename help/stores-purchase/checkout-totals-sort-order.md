---
title: Volgorde voor uitchecktotalen sorteren
description: Leer over het getoonde checkout totaal en hoe te om de orde van de de totalen van de controle in het ordesamenvatting te vormen.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Volgorde voor uitchecktotalen sorteren

Tijdens de controle van de bestelling wordt het totaal onder aan de bestelling weergegeven, met eventuele aanpassingen voor kortingen, verzendkosten, winkelkrediet en belasting. De orde van elk punt bepaalt de opeenvolging van de berekeningen, en in de configuratie door een aantal geplaatst dat aan elk punt wordt toegewezen. Het subtotaal is bijvoorbeeld het eerste item in de sectie en krijgt de waarde 10. Het Eindtotaal wordt als laatste weergegeven en krijgt de waarde 100 toegewezen. Aan alle andere items in de totalen wordt een waarde tussen deze waarden toegewezen.

![Overzicht van bestellingen geeft het totaal van het afrekenen weer](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_De sorteervolgorde voor de totalen van de kassa configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Totals Sort Order]** sectie.

   ![Opties voor het uitchecken van totalen worden genummerd om de sorteervolgorde te bepalen](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [Afhandelingstotalen Sorteervolgorde](../configuration-reference/sales/sales.md#checkout-totals-sort-order) in de _Referentiehandleiding voor configuratie_.

1. Als de instelling geldt voor een specifieke winkelweergave, [kiezen in de winkelweergave](../configuration-reference/scope-change.md#set-the-scope) waar de configuratie van toepassing is.

   Klik op **[!UICONTROL OK]** om door te gaan.

1. De volgorde bepalen in het dialoogvenster _Totalen_ , wijzigt u het nummer dat aan elk item is toegewezen.

   Hoe lager de waarde, hoe eerder de waarde in de lijst wordt geplaatst. In de standaardconfiguratie, Subtotal (`10`) is het eerste en het hoogste totaal (`100`) is de laatste.

   Indien nodig de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze wijzigingen te voltooien.

1. Klik op **[!UICONTROL Save Config]**.
