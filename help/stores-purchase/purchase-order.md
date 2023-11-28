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

A _inkooporder_ (PO) biedt commerciële klanten de mogelijkheid om voor goedgekeurde aankopen te betalen door naar het inkoopordernummer te verwijzen. De kooporder wordt vooraf goedgekeurd en uitgegeven door de onderneming die de aankoop doet. Tijdens het afrekenen kiest de klant Inkooporder als betalingsmethode. Na ontvangst van de factuur verwerkt het bedrijf de betaling in het systeem van te betalen rekeningen en betaalt het de aankoop.

Voordat betaling per kooporder wordt geaccepteerd, moet altijd de kredietwaardigheid van de commerciële klant worden vastgesteld.

**_U kunt als volgt de betaling per inkooporder configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Payment Methods]**.

1. Onder _[!UICONTROL Other Payment Methods]_, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Purchase Order]**sectie.

   ![Inkooporder](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [Inkooporder](../configuration-reference/sales/payment-methods.md#purchase-order) in de _Referentiehandleiding voor configuratie_.

   >[!NOTE]
   >
   >Indien nodig eerst de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze instellingen te wijzigen.

1. Als u deze betalingsmethode wilt activeren, stelt u **[!UICONTROL Enabled]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die deze betalingsmethode identificeert tijdens het afrekenen.

1. Set **[!UICONTROL New Order Status]** tot `Pending` totdat de betaling is toegestaan.

1. Set **[!UICONTROL Payment from Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) Deze betalingsmethode kan worden gebruikt.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, _[!UICONTROL Payment from Specific Countries]_wordt weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Set **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** de bedragen die nodig zijn om voor deze betalingsmethode in aanmerking te komen.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in dat de positie van dit object bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = eerst, `1` = seconde, `2` = derde, enzovoort.)

1. Klik op **[!UICONTROL Save Config]**.
