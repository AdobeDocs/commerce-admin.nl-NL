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

**_om bankoverschrijvingsbetalingen te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Onder _Andere Wijzen van de Betaling_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Bank Transfer Payment]** sectie uit.

   ![ Betaling van de Overdracht van de Bank ](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

1. Als u bankoverschrijvingen wilt activeren, stelt u **[!UICONTROL Enabled]** in op `Yes` .

1. Voer voor **[!UICONTROL Title]** een titel in die de betalingsmethode voor overschrijvingen tijdens het afrekenen identificeert.

1. Stel **[!UICONTROL New Order Status]** in op `Pending` totdat de betaling is geautoriseerd.

1. Stel **[!UICONTROL Payment from Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.

   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_&#x200B;weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voer de **[!UICONTROL Instructions]** in die uw klanten moeten volgen om een overschrijving in te stellen.

   Afhankelijk van het land waar uw bank is gevestigd en de vereisten van de bank, kunt u de volgende informatie opnemen:

   - Bankrekeningnaam
   - Bankrekeningnummer
   - Bankcode
   - Banknaam
   - Bankadres

1. Stel **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** in op de bedragen die nodig zijn om in aanmerking te komen voor deze betalingsmethode.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voer bij **[!UICONTROL Sort Order]** een getal in dat de positie van dit item bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
