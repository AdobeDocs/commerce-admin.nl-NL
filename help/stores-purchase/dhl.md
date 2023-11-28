---
title: DHL
description: Leer hoe u DHL instelt als een transportbedrijf voor uw winkel.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# DHL

DHL biedt geïntegreerde internationale diensten en op maat gesneden, klantgerichte oplossingen voor het beheren en vervoeren van brieven, goederen en informatie.

## Stap 1: DHL inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL DHL]** sectie.

   >[!NOTE]
   >
   >Indien nodig eerst de **[!UICONTROL Use system value]** Schakel het selectievakje in om de volgende instellingen te wijzigen zoals beschreven.

1. Set **[!UICONTROL Enabled for Checkout]** tot `Yes`.

1. Gewoonlijk kunt u de standaardinstelling accepteren **[!UICONTROL Gateway URL]**.

   Als DHL u een alternatieve URL heeft gegeven, ga die waarde op dit gebied in.

1. Gebruik de geloofsbrieven die door DHL worden verstrekt om de volgende gebieden te voltooien:

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![Instellingen DHL-account](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Stap 2; Voer de pakketbeschrijving en de verpakkingskosten in

1. In de **[!UICONTROL Content Type]** Selecteer de optie die het beste het type pakket beschrijft dat u verzendt:

   - `Documents`
   - `Non documents`

1. Configureer de opties voor de behandelingskosten naar wens.

   De afhandelingskosten zijn optioneel en worden als extra kosten aan de DHL-verzendkosten toegevoegd. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

   - Voor **[!UICONTROL Calculate Handling Fee]** selecteert u de methode die u wilt gebruiken voor het berekenen van afhandelingskosten:

      - `Fixed`
      - `Percentage`

   - Voor **[!UICONTROL Handling Applied]**, selecteer hoe u de afhandelingskosten wilt toepassen:

      - `Per Order`
      - `Per Package`

   - Voor **[!UICONTROL Handling Fee]** Voer het bedrag in dat moet worden aangerekend op basis van de methode die u hebt gekozen voor de berekening van het bedrag.

     Als de vergoeding bijvoorbeeld is gebaseerd op een vaste vergoeding, voert u het bedrag in als een decimaal, zoals `4.90`. Als de behandelingskosten echter zijn gebaseerd op een percentage van de bestelling, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de bestelling in rekening brengt, voert u de waarde in als `.06`.

   - Om ervoor te zorgen dat het totale gewicht van de bestelling kan worden opgesplitst voor een correcte berekening van de verzendkosten, stelt u **[!UICONTROL Divide Order Weight]** tot `Yes`.

   - Stel de **[!UICONTROL Weight Unit]** van de verpakking:

      - `Pounds`
      - `Kilograms`

   - Stel de **[!UICONTROL Size]** van een typische verpakking:

      - `Regular`
      - `Specific`

     Als u `Specific`, voert u de **[!UICONTROL Height]**, **[!UICONTROL Depth]**, en **[!UICONTROL Width]** van de verpakking in centimeter.

   ![Instellingen DHL-pakket](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Stap 3: Geef toegestane leveringsmethoden op

1. Voor **[!UICONTROL Allowed Methods]** kiest u elke methode die u beschikbaar wilt maken voor klanten.

   Als u meerdere methoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   Om de correcte lijst van leveringsmethodes te tonen, moet u eerst specificeren [Land van oorsprong](../configuration-reference/sales/shipping-settings.md).

1. Voor **[!UICONTROL Ready Time]** Voer het aantal uren in nadat een bestelling is verzonden dat een pakket klaar is om te worden verzonden.

1. Bewerk de **[!UICONTROL Displayed Error Message]** indien nodig.

   Dit bericht wordt weergegeven wanneer een geselecteerde methode niet beschikbaar is.

1. Als u een [Gratis verzending](shipping-free.md) via DHL de opties voor gratis verzending instellen.

   - Voor **[!UICONTROL Free Method]**, kiest u de methode die u voor gratis verzending wilt gebruiken.

   - Set **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - Als je Gratis verzending met minimumbestelling aanbiedt, voer je de **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - Geen gratis DHL-scheepvaart op bestellingen.

     Deze instelling is vergelijkbaar met de standaardinstelling _Gratis verzending_ methode, maar verschijnt in de sectie van DHL zodat weten de klanten welke methode voor hun orde wordt gebruikt.

   - Voor **[!UICONTROL Free Shipping Amount Threshold]** Voer het minimumbedrag in voor een bestelling die in aanmerking komt voor gratis verzending.

     ![Toegestane methoden van DHL](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Stap 4: Geef de landen aan die van toepassing zijn

1. Set **[!UICONTROL Ship to Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries`
   - `Specific Countries`

   Als u objecten naar bepaalde landen verzendt, selecteert u elk land in het **[!UICONTROL Ship to Specific Countries]** lijst.

1. Set **[!UICONTROL Show Method if Not Applicable]**:

   `Yes` - Geeft DHL weer als een verzendmethode tijdens de afhandeling, zelfs als dit niet van toepassing is op de bestelling.

   `No` - Geeft DHL alleen als verzendmethode tijdens de afhandeling weer, indien van toepassing.

1. Als u een logbestand wilt maken met de details van DHL-verzendingen die vanuit uw winkel zijn gemaakt, stelt u **[!UICONTROL Debug]** tot `Yes`.

1. Voor **[!UICONTROL Sort Order]** Voer een getal in om de volgorde te bepalen waarin DHL wordt weergegeven bij andere leveringsmethoden tijdens het uitchecken.

   `0` = eerst, `1` = seconde, `2` = derde, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

   ![Toepasselijke landen van DHL](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
