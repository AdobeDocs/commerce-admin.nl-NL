---
title: FedEx
description: Leer hoe u FedEx instelt als een verzender voor je winkel.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# FedEx

FedEx is een van &#39;s werelds grootste scheepvaartmaatschappijen die lucht-, vracht- en grondvaartdiensten met verschillende prioriteitsniveaus aanbieden.

![Verzendopties FedEx bij afhandeling](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx kan gebruiken [dimensionaal gewicht](carriers.md#dimensional-weight) om bepaalde verzendkosten te bepalen. Adobe Commerce en Magento Open Source ondersteunen echter alleen de berekening van verzendkosten op basis van gewicht.

## Stap 1: Register voor de Productie van de Diensten van het Web FedEx

A [FedEx-zakelijke account][1] en registratie voor de Toegang van de Productie van de Diensten van het Web FedEx wordt vereist. Nadat u een FedEx-account hebt gemaakt, leest u de pagina met informatie over de productieaccount en klikt u op de knop _productiesleutel verkrijgen_ een koppeling onder aan de pagina om een sleutel te registreren en te verkrijgen.

>[!NOTE]
>
>Zorg ervoor om de authentificatiesleutel te kopiëren of te schrijven. Je moet FedEx instellen in je verzendinstellingen voor Handel.

## Stap 2: FedEx inschakelen voor je winkel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL FedEx]** sectie.

1. Set **[!UICONTROL Enabled for Checkout]** tot `Yes`.

1. Voor **[!UICONTROL Title]**, voert u een titel in die de verzendmethode van FedEx tijdens het afrekenen aangeeft.

1. Voer de volgende gegevens in van uw FedEx-account:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Als u een FedEx-sandbox hebt ingesteld en wilt werken in de testomgeving, stelt u **[!UICONTROL Sandbox Mode]** tot `Yes`.

   >[!NOTE]
   >
   >Sandboxmodus instellen op `No` als u klaar bent om FedEx als verzendmethode aan uw klanten aan te bieden.

   ![FedEx-accountinstellingen](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Stap 3: Verpakkings- en verpakkingskosten

1. Set **[!UICONTROL Pickup Type]** op de ophaalmethode die wordt gebruikt voor overbrengingen.

   - `DropOff at Fedex Location` - (Standaard) Geeft aan dat u verzendingen op uw lokale FedEx-station neerzet.
   - `Contact Fedex to Schedule` - Geeft aan dat u contact opneemt met FedEx om een afhaalbewerking aan te vragen.
   - `Use Scheduled Pickup` - Geeft aan dat de zending wordt opgehaald als onderdeel van een normale geplande ophaling.
   - `On Call` - Wijst erop dat de bestelwagen door FedEx wordt gepland te roepen.
   - `Package Return Program` - Geeft aan dat de verzending wordt opgehaald door het FedEx Ground Package Returns Program.
   - `Regular Stop` - Geeft aan dat de verzending wordt opgehaald volgens het normale ophaalschema.
   - `Tag` - Geeft aan dat het ophalen van de lading specifiek is voor een aanvraag van de tag Express of grondaanroep. Dit is alleen van toepassing op verzendlabel voor retourzending.

1. Voor **[!UICONTROL Packages Request Type]** Selecteer het aanvraagtype dat het beste uw voorkeur beschrijft wanneer u een bestelling opsplitst in meerdere verzendingen:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Voor **[!UICONTROL Packaging]** selecteert u het type FedEx-verpakking dat u doorgaans gebruikt om producten uit uw winkel te verzenden.

1. Set **[!UICONTROL Weight Unit]** aan de maateenheid die wordt gebruikt in uw landinstelling.

   - `Pounds`
   - `Kilograms`

1. Voer de **[!UICONTROL Maximum Package Weight]** toegestaan voor FedEx-verzendingen.

   Het standaard FedEx maximumgewicht is 150 lbs. Raadpleeg uw verzendende maatschappij voor meer informatie. De standaardwaarde wordt aanbevolen, tenzij u speciale regelingen hebt getroffen met FedEx. Zie [Afmetingen](carriers.md#dimensional-weight) voor meer informatie .

   ![FedEx-pakketinstellingen](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configureer de opties voor de behandelingskosten naar wens.

   De verpakkingskosten zijn optioneel en zijn niet zichtbaar tijdens het afrekenen. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

   - Set **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Voor **[!UICONTROL Handling Applied]** kiest u een van de volgende methoden voor het beheer van afhandelingskosten:

      - `Per Order`
      - `Per Package`

   - Voer de **[!UICONTROL Handling Fee]** als `fixed` bedrag of `percentage`, afhankelijk van de berekeningsmethode.

1. Set **[!UICONTROL Residential Delivery]** op een van de volgende manieren, afhankelijk van het feit of u Business-to-Consumer (B2C) of Business-to-Business (B2B) verkoopt.

   - `Yes` - voor leveringen van B2C-woningen.
   - `No` - voor B2B-leveringen.

   ![FedEx-instellingen voor afhandelingskosten](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Stap 4: Toegestane methoden en toepasselijke landen

1. Set **[!UICONTROL Allowed Methods]** aan elke verzendmethode die u wilt aanbieden.

   Houd bij het kiezen van methoden rekening met uw FedEx-account, de frequentie en de grootte van uw verzendingen en als u internationale verzendingen toestaat. U kunt zo veel of zo weinig methoden aanbieden als u wilt, zoals:

   - Eerste prioriteit Europa
   - Opties voor de leveringsdag: 1-daagse vracht, 2-daagse vracht, 2-daagse, 2-daagse AM, 3-daagse vracht
   - Binnenlandse opties — Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Internationale opties - Internationale economie, binnenlandse economie, goederenvervoer, internationale eerste, internationale grond, internationaal, prioritair
   - Prioriteitsopties - Vracht, Prioriteit overnight
   - Smart Post-if die de methode Smart Post aanbiedt (ga in **Hub-id**)
   - Goederenopties — Vracht, nationaal goederenvervoer

1. Als u een [Gratis verzending](shipping-free.md) Stel de opties voor gratis verzending in via FedEx.

   - Set **[!UICONTROL Free Method]** op de methode die je wilt gebruiken voor gratis verzending. Kies `None`.

   - Als u een minimale bestelling wilt vereisen die in aanmerking komt voor gratis verzending met FedEx, stelt u **[!UICONTROL Enable Free Shipping Threshold]** tot `Enable`. Voer vervolgens de minimumwaarde in **[!UICONTROL Free Shipping Amount Threshold]**.

   Deze instelling is vergelijkbaar met de instelling voor de standaardmethode voor gratis verzending, maar wordt tijdens het uitchecken weergegeven in de sectie FedEx, zodat klanten weten welke methode wordt gebruikt voor hun bestelling.

1. Wijzig, indien nodig, de **[!UICONTROL Displayed Error Message]**.

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als FedEx niet beschikbaar is.

   ![Toegestane leveringsmethoden FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) gespecificeerd in uw archiefconfiguratie kan deze leveringsmethode gebruiken.

   - `Specific Countries` - Als u deze optie kiest, _Schip naar specifieke landen_ wordt weergegeven. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Als u een logboek van al mededeling tussen uw opslag en het systeem wilt houden FedEx, plaats **[!UICONTROL Debug]** tot `Yes`.

1. Set **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Geeft alle verzendmethoden van FedEx aan klanten weer, ongeacht hun beschikbaarheid.
   - `No` - Geeft alleen de verzendmethoden van FedEx weer die van toepassing zijn op de bestelling.

1. Voor **[!UICONTROL Sort Order]** voert u een getal in om de volgorde te bepalen waarin FedEx wordt weergegeven bij andere leveringsmethoden tijdens het afrekenen.

   `0` = eerst, `1` = seconde, `2` = derde, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

   ![FedEx-landen](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>De handel verklaart altijd de volledige bestellingsprijs aan FedEx wanneer het berekenen van verzendkosten. Dit gedrag kan niet worden gewijzigd.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
