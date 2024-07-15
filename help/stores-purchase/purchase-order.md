---
title: Aankooporders
description: Leer hoe u inkooporders instelt als een offline betalingsmethode in uw winkel.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Aankooporders

A _kooporder_ (PO) staat commerciële klanten toe om voor erkende aankopen te betalen door het aantal van Inkooporder van verwijzingen te voorzien. De kooporder wordt vooraf goedgekeurd en uitgegeven door de onderneming die de aankoop doet. Tijdens het afrekenen kiest de klant Inkooporder als betalingsmethode. Na ontvangst van de factuur verwerkt het bedrijf de betaling in het systeem van te betalen rekeningen en betaalt het de aankoop.

Voordat betaling per kooporder wordt geaccepteerd, moet altijd de kredietwaardigheid van de commerciële klant worden vastgesteld.

**_om betaling door kooporder te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Onder _[!UICONTROL Other Payment Methods]_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Purchase Order]**sectie.

   ![ Inkooporder ](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ de Orde van de Aankoop ](../configuration-reference/sales/payment-methods.md#purchase-order) in de _Gids van de Verwijzing van de Configuratie_.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

1. Als u deze betalingsmethode wilt activeren, stelt u **[!UICONTROL Enabled]** in op `Yes` .

1. Voer bij **[!UICONTROL Title]** een titel in die deze betalingsmethode identificeert tijdens het afrekenen.

1. Stel **[!UICONTROL New Order Status]** in op `Pending` totdat de betaling is geautoriseerd.

1. Stel **[!UICONTROL Payment from Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Stel **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** in op de bedragen die nodig zijn om in aanmerking te komen voor deze betalingsmethode.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voer bij **[!UICONTROL Sort Order]** een getal in dat de positie van dit item bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
