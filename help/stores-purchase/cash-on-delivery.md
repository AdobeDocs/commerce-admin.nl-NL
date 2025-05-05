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

Adobe Commerce en de Magento Open Source staan u toe om _geld op levering_ (COD) betalingen voor aankopen goed te keuren. U kunt de betaling van COD slechts van specifieke landen goedkeuren, en u kunt de configuratie met minimum en maximum totale grenzen van de orde verfijnen.

De verzendende vervoerder ontvangt de betaling van de klant op het tijdstip van levering, die vervolgens aan u wordt overgedragen. Je kunt een correctie aanbrengen voor alle kosten die de vervoerder in rekening brengt in de verzendkosten.

**_aan opstellingscontanten op leveringsbetalingen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Onder _Andere Wijzen van de Betaling_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Cash On Delivery Payment]** sectie uit.

   ![ Betaling Onder rembours ](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Betaling Onder rembours ](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) in de _Gids van de Verwijzing van de Configuratie_.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

1. Als u contant geld wilt activeren bij het betalen, stelt u **[!UICONTROL Enabled]** in op `Yes` .

1. Voer voor **[!UICONTROL Title]** een titel in die de betalingsmethode voor Onder rembours aangeeft tijdens het afrekenen.

1. Stel **[!UICONTROL New Order Status]** in op `Pending` totdat de ontvangst van de betaling is bevestigd.

   U kunt desgewenst de status `Processing` of `Suspected Fraud` gebruiken voor nieuwe bestellingen met deze betalingsmethode.

1. Stel **[!UICONTROL Payment from Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_&#x200B;weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voer de **[!UICONTROL Instructions]** in voor het accepteren van de levering van een COD-bestelling.

1. Stel **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** in op de orderbedragen die nodig zijn om in aanmerking te komen voor COD-betaling.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of gelijken, het minimum of maximumordertotaal is.

1. Voer bij **[!UICONTROL Sort Order]** een getal in dat de positie van dit item bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
