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

Met Adobe Commerce en Magento Open Source kun je betalingen per cheque of postwissel accepteren. De _betalingsmethode van de Controle/van de Geld_ wordt van de Controle &lbrace;toegelaten voor uw opslag door gebrek. U kunt controles en postorders slechts van specifieke landen goedkeuren, en u kunt de configuratie met minimum en maximum totale grenzen van de orde verfijnen.

**_om betaling door controle of postorde te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Onder _[!UICONTROL Other Payment Methods]_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Check / Money Order]**&#x200B;sectie.

   ![ Controle/Geldorde ](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Controle/Geldorde ](../configuration-reference/sales/payment-methods.md#check--money-order) in de _Gids van de Verwijzing van de Configuratie_.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

1. Als u betaling via cheque of postwissel wilt accepteren, stelt u **[!UICONTROL Enabled]** in op `Yes` .

1. Voer bij **[!UICONTROL Title]** een titel in die de betalingsmethode voor de cheque/postwissel tijdens het afrekenen aangeeft.

1. Als orders doorgaans wachten op goedkeuring, accepteert u de standaardwaarde **[!UICONTROL New Order Status]** als `Pending"` totdat deze wordt goedgekeurd.

   U kunt desgewenst de status `Processing` of `Suspected Fraud` gebruiken voor nieuwe bestellingen met deze betalingsmethode.

1. Stel **[!UICONTROL Payment from Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_&#x200B;weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Voer bij **[!UICONTROL Make Check Payable To]** de naam in van de partij aan wie de cheque moet worden betaald.

1. Voer bij **[!UICONTROL Send Check To]** het adres of postvak van de straat in waar de controles zijn gemaild.

1. Stel **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** in op de orderbedragen die nodig zijn om in aanmerking te komen voor deze betalingsmethode.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voer bij **[!UICONTROL Sort Order]** een getal in dat de positie van dit item bepaalt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
