---
title: Gratis verzending
description: Leer hoe je een optie voor gratis verzending instelt voor je winkel.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Gratis verzending

_het Vrij verschepen_ is één van de meest efficiënte bevorderingen die u kunt aanbieden. Het kan op een minimumaankoop worden gebaseerd, of opstelling als regel van de a [ kartprijs ](../merchandising-promotions/price-rules-cart.md) die wordt toegepast wanneer een reeks voorwaarden wordt voldaan. Als beide op de zelfde orde van toepassing zijn, neemt het configuratie plaatsen belangrijkheid over de wortelregel.

>[!NOTE]
>
>Controleer de configuratie van de verzendende provider voor eventuele aanvullende instellingen die vereist zijn voor gratis verzending.

## Stap 1: Vrije verzending configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Delivery Methods]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Free Shipping]** sectie uit.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om de volgende instellingen te wijzigen zoals beschreven.

1. Stel **[!UICONTROL Enabled]** in op `Yes` .

1. Voer bij **[!UICONTROL Title]** een titel in die de methode voor het gratis verzenden van objecten tijdens het afrekenen aangeeft en een **[!UICONTROL Method Name]** die deze methode beschrijft.

1. Voer bij **[!UICONTROL Minimum Order Amount]** de minimale totale waarde in die in aanmerking komt voor gratis verzending.

   >[!TIP]
   >
   >Om het vrije verschepen met [ lijsttarieven ](shipping-table-rate.md) te gebruiken, maak _[!UICONTROL Minimum Order Amount]_&#x200B;zo hoog dat het nooit wordt ontmoet. Als je deze hoge waarde gebruikt, wordt de gratis verzending niet van kracht, tenzij deze wordt geactiveerd door een prijsregel.

1. Instellen **[!UICONTROL Include Tax to Amount]** :

   - `Yes` - Hiermee wordt belasting opgenomen bij het berekenen van het minimumbedrag voor bestellingen (Subtotaal + BTW - Korting).
   - `No` - Neemt geen belasting op bij de berekening van het minimumbedrag van de order (Subtotaal - Korting).

   ![ Vrij die ](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"} verscheept

1. Voer bij **[!UICONTROL Displayed Error Message]** het bericht in dat wordt weergegeven als de gratis verzending niet langer beschikbaar is.

1. Instellen **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - de Klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen vrije verzending gebruiken.

   - `Specific Countries` - Nadat u deze waarde hebt gekozen, wordt de lijst _[!UICONTROL Ship to Specific Countries]_&#x200B;weergegeven. Selecteer elk land in de lijst waar gratis verzending kan worden gebruikt.

1. Instellen **[!UICONTROL Show Method if Not Applicable]** :

   - `Yes` - Geeft altijd de methode voor gratis verzending weer, zelfs als deze niet van toepassing is.
   - `No` - Geeft de methode voor gratis verzending alleen weer wanneer deze van toepassing is.

1. Voer bij **[!UICONTROL Sort Order]** het getal in dat de positie van de gratis verzending bepaalt in de lijst met leveringsmethoden tijdens het afrekenen.

   `0` = first, `1` = second, `2` = third, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

## Stap 2: Laat het vrije verschepen in de dragerconfiguratie toe

Zorg ervoor om het even welke configuratie te voltooien die voor elke drager wordt vereist die u voor vrije verzending van plan bent te gebruiken. Bijvoorbeeld, als uw [ configuratie van UPS ](ups.md) anders volledig is, werk de volgende montages bij om vrije verzending toe te laten en te vormen.

1. In de _[!UICONTROL Delivery Methods]_&#x200B;configuratie, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL UPS]**&#x200B;sectie.

1. Stel **[!UICONTROL Free Method]** in op `UPS Ground` of een ander type dat u wilt toewijzen voor gratis verzending.

1. Als u een minimale bestelling voor gratis verzending wilt vereisen, stelt u **[!UICONTROL Enable Free Shipping Threshold]** in op `Enable` .

   Als u een minimumvolgorde wilt gebruiken, voert u de vereiste hoeveelheid voor **[!UICONTROL Free Shipping Amount Threshold]** in.

1. Klik op **[!UICONTROL Save Config]**.
