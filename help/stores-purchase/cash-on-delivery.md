---
title: Onder rembours
description: Leer hoe u contant geld bij levering instelt als een offline betalingsmethode in uw winkel.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Onder rembours

Met Adobe Commerce en Magento Open Source kun je accepteren _Onder rembours_ (COD) betalingen voor aankopen. U kunt de betaling van COD slechts van specifieke landen goedkeuren, en u kunt de configuratie met minimum en maximum totale grenzen van de orde verfijnen.

De verzendende vervoerder ontvangt de betaling van de klant op het tijdstip van levering, die vervolgens aan u wordt overgedragen. Je kunt een correctie aanbrengen voor alle kosten die de vervoerder in rekening brengt in de verzendkosten.

**_Contant betalen bij levering instellen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Payment Methods]**.

1. Onder _Andere betalingsmethoden_, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Cash On Delivery Payment]** sectie.

   ![Onder rembours](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [Onder rembours](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) in de _Referentiehandleiding voor configuratie_.

   >[!NOTE]
   >
   >Indien nodig eerst de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze instellingen te wijzigen.

1. Als je de betaling via contant geld wilt activeren, moet je **[!UICONTROL Enabled]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die de betalingsmethode voor Onder rembours aangeeft tijdens het afrekenen.

1. Set **[!UICONTROL New Order Status]** tot `Pending` totdat de ontvangst van de betaling is bevestigd.

   U kunt desgewenst de opdracht `Processing` of `Suspected Fraud` status voor nieuwe orders met deze betalingsmethode.

1. Set **[!UICONTROL Payment from Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) Deze betalingsmethode kan worden gebruikt.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, _[!UICONTROL Payment from Specific Countries]_wordt weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voer de **[!UICONTROL Instructions]** voor het accepteren van levering van een COD-bestelling.

1. Set **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** op de orderbedragen die nodig zijn om in aanmerking te komen voor CZV-betaling.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of gelijken, het minimum of maximumordertotaal is.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in dat de positie van dit object bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = eerst, `1` = seconde, `2` = derde, enzovoort.)

1. Klik op **[!UICONTROL Save Config]**.
