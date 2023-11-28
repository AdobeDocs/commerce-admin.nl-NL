---
title: Controles en postwissels
description: Leer hoe u cheque en postwissel kunt instellen als een offline betalingsmethode in uw winkel.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Controles en postwissels

Met Adobe Commerce en Magento Open Source kun je betalingen per cheque of postwissel accepteren. De _Cheque/postwissel_ De betalingsmethode is standaard ingeschakeld voor je winkel. U kunt controles en postorders slechts van specifieke landen goedkeuren, en u kunt de configuratie met minimum en maximum totale grenzen van de orde verfijnen.

**_Om betaling via cheque of postwissel te configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Payment Methods]**.

1. Onder _[!UICONTROL Other Payment Methods]_, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Check / Money Order]**sectie.

   ![Cheque/postwissel](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [Cheque/postwissel](../configuration-reference/sales/payment-methods.md#check--money-order) in de _Referentiehandleiding voor configuratie_.

   >[!NOTE]
   >
   >Indien nodig eerst de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze instellingen te wijzigen.

1. Als u betaling wilt accepteren via cheque of postwissel, stelt u **[!UICONTROL Enabled]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die de betalingsmethode voor de cheque/postwissel tijdens de afhandeling aangeeft.

1. Als de orden typisch op goedkeuring wachten, keur het gebrek goed **[!UICONTROL New Order Status]** als `Pending"` totdat het is goedgekeurd.

   U kunt desgewenst de opdracht `Processing` of `Suspected Fraud` status voor nieuwe orders met deze betalingsmethode.

1. Set **[!UICONTROL Payment from Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) Deze betalingsmethode kan worden gebruikt.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, _[!UICONTROL Payment from Specific Countries]_wordt weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voor **[!UICONTROL Make Check Payable To]** wordt de naam van de partij vermeld aan wie de controle verschuldigd is.

1. Voor **[!UICONTROL Send Check To]** Voer het adres of postvak in van de straat waar de controles zijn verzonden.

1. Set **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** de bedragen van de bestelling die nodig zijn om voor deze betalingsmethode in aanmerking te komen.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in dat de positie van dit object bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = eerst, `1` = seconde, `2` = derde, enzovoort.)

1. Klik op **[!UICONTROL Save Config]**.
