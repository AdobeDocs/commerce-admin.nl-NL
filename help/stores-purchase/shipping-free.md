---
title: Gratis verzending
description: Leer hoe je een optie voor gratis verzending instelt voor je winkel.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Gratis verzending

_Gratis verzending_ is een van de meest effectieve aanbiedingen die je kunt aanbieden. Deze kan gebaseerd zijn op een minimale aankoop of worden ingesteld als een [kartonnen prijsregel](../merchandising-promotions/price-rules-cart.md) die wordt toegepast wanneer aan een reeks voorwaarden wordt voldaan. Als beide op de zelfde orde van toepassing zijn, neemt het configuratie plaatsen belangrijkheid over de wortelregel.

>[!NOTE]
>
>Controleer de configuratie van de verzendende provider voor eventuele aanvullende instellingen die vereist zijn voor gratis verzending.

## Stap 1: Vrije verzending configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Free Shipping]** sectie.

   >[!NOTE]
   >
   >Schakel indien nodig eerst de optie **[!UICONTROL Use system value]** Schakel het selectievakje in om de volgende instellingen te wijzigen zoals beschreven.

1. Set **[!UICONTROL Enabled]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die de methode voor gratis verzending tijdens het afrekenen aangeeft en een **[!UICONTROL Method Name]** om het te beschrijven.

1. Voor **[!UICONTROL Minimum Order Amount]** Voer de minimale totale waarde in die in aanmerking komt voor gratis verzending.

   >[!TIP]
   >
   >Voor gratis verzending met [tabeltarieven](shipping-table-rate.md)de _[!UICONTROL Minimum Order Amount]_zo hoog dat het nooit wordt gehaald. Als je deze hoge waarde gebruikt, wordt de gratis verzending niet van kracht, tenzij deze wordt geactiveerd door een prijsregel.

1. Set **[!UICONTROL Include Tax to Amount]**:

   - `Yes` - Omvat belasting bij de berekening van het minimumbestelbedrag (Subtotaal + Belasting - Korting).
   - `No` - Omvat geen belasting bij de berekening van het minimumorderbedrag (Subtotaal - Korting).

   ![Gratis verzending](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Voor **[!UICONTROL Displayed Error Message]**, voer het bericht in dat wordt weergegeven als de gratis verzending niet beschikbaar is.

1. Set **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) Je kunt gratis verzending gebruiken die in je winkelconfiguratie is opgegeven.

   - `Specific Countries` - Nadat u deze waarde hebt gekozen, _[!UICONTROL Ship to Specific Countries]_wordt weergegeven. Selecteer elk land in de lijst waar gratis verzending kan worden gebruikt.

1. Set **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Altijd de methode voor gratis verzending weergeven, zelfs als deze niet van toepassing is.
   - `No` - Geeft alleen de methode voor gratis verzending weer wanneer van toepassing.

1. Voor **[!UICONTROL Sort Order]**, voert u het getal in dat de positie van de gratis verzending bepaalt in de lijst met leveringsmethoden tijdens het afrekenen.

   `0` = eerst, `1` = seconde, `2` = derde, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

## Stap 2: Laat het vrije verschepen in de dragerconfiguratie toe

Zorg ervoor om het even welke configuratie te voltooien die voor elke drager wordt vereist die u voor vrije verzending van plan bent te gebruiken. Als uw [UPS-configuratie](ups.md) is anders volledig, werk de volgende montages bij om vrije verzending toe te laten en te vormen.

1. In de _[!UICONTROL Delivery Methods]_configuratie, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL UPS]**sectie.

1. Set **[!UICONTROL Free Method]** tot `UPS Ground` of een ander type dat je wilt aanwijzen voor gratis verzending.

1. Als je een minimale bestelling voor gratis verzending wilt vereisen, stelt u **[!UICONTROL Enable Free Shipping Threshold]** tot `Enable`.

   Als u een minimumvolgorde kiest, voert u het vereiste bedrag in voor **[!UICONTROL Free Shipping Amount Threshold]**.

1. Klik op **[!UICONTROL Save Config]**.
