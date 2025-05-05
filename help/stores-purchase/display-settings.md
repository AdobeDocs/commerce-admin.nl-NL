---
title: Instellingen voor prijsweergave
description: In deze video ziet u meer informatie over de weergave van belastingen in de catalogus, winkelwagentje, bestellingen, facturen en creditnota's die de aankoop van klanten ondersteunen.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Instellingen voor prijsweergave

De instellingen voor prijsweergave bepalen of de prijs van het product en de verzendkosten belasting bevatten of uitsluiten, of twee versies van de prijs weergeven: één met en de andere zonder belasting.

Als de productprijs ook belasting bevat, wordt de belasting alleen weergegeven als er een belastingregel is die overeenkomt met de fiscale oorsprong of als het adres van een klant overeenkomt met de belastingregel. Gebeurtenissen die een overeenkomst kunnen activeren, zijn onder meer wanneer een klant een account maakt, zich aanmeldt of een taxatie en verzendkosten genereert vanuit het winkelwagentje.

>[!IMPORTANT]
>
>Het kan verwarrend zijn voor de klant om prijzen weer te geven die belasting omvatten en uitsluiten. Vermijd het teweegbrengen van een waarschuwingsbericht, zie de [ richtlijnen ](international-tax-guidelines.md) voor uw land en [ geadviseerde montages ](taxes.md#warning-messages) om waarschuwingsberichten te vermijden.

![ de Montages van de Vertoning van de Prijs ](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie {de Montages van de Vertoning van de 0} Prijs [&#128279;](../configuration-reference/sales/tax.md#price-display-settings) in de _Gids van de Verwijzing van de Configuratie_.

## Prijsweergave-instellingen configureren

Wanneer de configuratie van berekening voor belastingen, tarieven, en klassen wordt gebeëindigd, worden de belastingen berekend volgens die montages. De weergave van belastingen in de catalogus, winkelwagentje, bestellingen, facturen en creditnota&#39;s moet echter ook worden geconfigureerd om de gebruikerservaring op de winkel te ondersteunen.

Het is aan te raden om prijzen weer te geven met de bijbehorende belastingen (inclusief belastingen of zowel inclusief belastingen als exclusief belastingen), zodat klanten weten hoe deze berekeningen worden toegepast voordat ze een order plaatsen.

### Stap 1: Weergave-instellingen voor catalogusprijzen configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Tax]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Price Display Settings]** sectie uit.

1. Kies bij **[!UICONTROL Display Product Prices in Catalog]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Als u deze optie instelt op `Including Tax` , wordt de belasting alleen weergegeven als er een belastingregel is die overeenkomt met de fiscale oorsprong of als er een klantadres is dat overeenkomt met de belastingregel. Gebeurtenissen die een overeenkomst kunnen activeren, zijn onder andere het aanmaken van een klantenaccount, aanmelding of het gebruik van het taxatieprogramma BTW en verzendkosten in het winkelwagentje.

1. Kies bij **[!UICONTROL Display Shipping Prices]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Als u ervoor kiest om beide prijzen (met en zonder belasting) weer te geven, ziet de winkel er ongeveer als volgt uit:

![ Voorbeeld van prijsvertoning met inbegrip van belastingen op de storefront ](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Stap 2: De weergave-instellingen voor winkelwagentjes configureren

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Shopping Cart Display Settings]** sectie uit.

   ![ het Shopping de Montages van de Vertoning van de Kar ](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Kies bij **[!UICONTROL Display Prices]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Kies bij **[!UICONTROL Display Subtotal]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Kies bij **[!UICONTROL Display Shipping Amount]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) voor **[!UICONTROL Display Gift Wrapping Prices]**, kies één van het volgende:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) voor **[!UICONTROL Display Printed Card Prices]**, kies één van het volgende:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Voor elk van deze resterende opties schakelt u naar `Yes` of `No` volgens uw voorkeur:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Stap 3: De weergave-instellingen voor bestellingen, facturen en creditnota&#39;s configureren

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** sectie uit.

   ![ Orders, Facturen, de Montages van de Vertoning van de Memo&#39;s van Kredieten ](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Kies bij **[!UICONTROL Display Prices]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Kies bij **[!UICONTROL Display Subtotal]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Kies bij **[!UICONTROL Display Shipping Amount]** een van de volgende opties:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) voor **[!UICONTROL Display Gift Wrapping Prices]**, kies één van het volgende:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) voor **[!UICONTROL Display Printed Card Prices]**, kies één van het volgende:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Voor elk van deze resterende opties schakelt u naar `Yes` of `No` volgens uw voorkeur:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
