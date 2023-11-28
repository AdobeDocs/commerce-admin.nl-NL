---
title: Bankoverschrijvingen
description: Leer hoe je bankoverschrijvingen kunt instellen als een offline betalingsmethode in je winkel.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Bankoverschrijvingen

Met Adobe Commerce en Magento Open Source kun je betalingen accepteren die van een bankrekening van een klant zijn overgemaakt en op je zakelijke bankrekening zijn gedeponeerd.

**_Betalingen via overschrijving configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Payment Methods]**.

1. Onder _Andere betalingsmethoden_, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Bank Transfer Payment]** sectie.

   ![Bankoverschrijving](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Indien nodig eerst de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze instellingen te wijzigen.

1. Als je bankoverschrijvingen wilt activeren, stelt u **[!UICONTROL Enabled]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die de betalingsmethode voor overschrijvingen tijdens het afrekenen aangeeft.

1. Set **[!UICONTROL New Order Status]** tot `Pending` totdat de betaling is toegestaan.

1. Set **[!UICONTROL Payment from Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) Deze betalingsmethode kan worden gebruikt.

   - `Specific Countries` - Nadat u deze optie hebt gekozen, _[!UICONTROL Payment from Specific Countries]_wordt weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voer de **[!UICONTROL Instructions]** dat uw klanten moeten volgen om een overschrijving in te stellen.

   Afhankelijk van het land waar uw bank is gevestigd en de vereisten van de bank, kunt u de volgende informatie opnemen:

   - Bankrekeningnaam
   - Bankrekeningnummer
   - Bankcode
   - Banknaam
   - Bankadres

1. Set **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** de bedragen die nodig zijn om voor deze betalingsmethode in aanmerking te komen.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in dat de positie van dit object bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = eerst, `1` = seconde, `2` = derde, enzovoort.)

1. Klik op **[!UICONTROL Save Config]**.
