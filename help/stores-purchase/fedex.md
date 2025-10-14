---
title: FedEx
description: Leer hoe u FedEx instelt als een verzender voor je winkel.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: ad5da1d77b63bf6bcc0227a5c467e369b7bb8d89
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# FedEx

FedEx is een van &#39;s werelds grootste scheepvaartmaatschappijen die lucht-, vracht- en grondvaartdiensten met verschillende prioriteitsniveaus aanbieden.

![&#x200B; Verzendopties FedEx bij Afhandeling &#x200B;](./assets/storefront-checkout-shipping-fedex.png)

>[!NOTE]
>
>FedEx kan [&#x200B; dimensionaal gewicht &#x200B;](carriers.md#dimensional-weight) gebruiken om sommige het verschepen tarieven te bepalen. Adobe Commerce en Magento Open Source ondersteunen echter alleen berekening van verzendkosten op basis van gewicht.

## Stap 1: Register voor de Productie van de Diensten van het Web FedEx

Een FedEx handelaarrekening en registratie voor de Toegang van de Productie van de Diensten van het Web FedEx wordt vereist. Na het creëren van een rekening FedEx, lees door de pagina van de informatie van de productierekening, dan klik _verkrijg de Sleutel van de Productie_ verbinding bij de bodem van de pagina om een sleutel te registreren en te verkrijgen.

>[!NOTE]
>
>Zorg ervoor om de authentificatiesleutel te kopiëren of te schrijven. Het is vereist om FedEx in te stellen in je verzendinstellingen voor Commerce.

## Stap 2: FedEx inschakelen voor je winkel

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Delivery Methods]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL FedEx]** sectie uit.

1. Stel **[!UICONTROL Enabled for Checkout]** in op `Yes` .

1. Voer bij **[!UICONTROL Title]** een titel in die de verzendmethode van FedEx tijdens het afrekenen aangeeft.

1. Voer de volgende gegevens in van uw FedEx-account:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Als u afzonderlijke volgAPI-referenties hebt, schakelt u de volgende configuratie in:

   - **[!UICONTROL Enable Tracking API credentials]**

1. Voer de volgende gegevens in van uw FedEx-account:

   - **[!UICONTROL Tracking API Key]**
   - **[!UICONTROL Tracking API Secret Key]**

1. Stel **[!UICONTROL Sandbox Mode]** in op `Yes` als u een FedEx-sandbox hebt ingesteld en wilt werken in de testomgeving.

   >[!NOTE]
   >
   >Stel de sandboxmodus in op `No` wanneer u FedEx als verzendmethode aan uw klanten wilt aanbieden.

   ![&#x200B; de Montages van de Rekening FedEx &#x200B;](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png)

## Stap 3: Verpakkings- en verpakkingskosten

1. Stel **[!UICONTROL Pickup Type]** in op de ophaalmethode die wordt gebruikt voor verzendingen.

   - `DropOff at Fedex Location` - (Standaard) Geeft aan dat u verzendingen op uw lokale FedEx-station neerzet.
   - `Contact Fedex to Schedule` - Geeft aan dat u contact opneemt met FedEx om een afhaalbewerking aan te vragen.
   - `Use Scheduled Pickup` - Geeft aan dat de verzending wordt opgehaald als onderdeel van een normale geplande ophaling.
   - `On Call` - Geeft aan dat het ophalen is gepland door FedEx aan te roepen.
   - `Package Return Program` - Geeft aan dat de verzending is opgehaald door het FedEx Ground Package Returns Program.
   - `Regular Stop` - Geeft aan dat de verzending wordt opgehaald volgens het normale ophaalschema.
   - `Tag` - Geeft aan dat het ophalen van de verzending specifiek is voor een aanvraag voor het ophalen van de tag Express of grondaanroep. Dit is alleen van toepassing op verzendlabel voor retourzending.

1. Selecteer voor **[!UICONTROL Packages Request Type]** het aanvraagtype dat het beste uw voorkeur beschrijft bij het splitsen van een bestelling in meerdere verzendingen:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Selecteer voor **[!UICONTROL Packaging]** het type FedEx-pakket dat u doorgaans gebruikt om producten uit uw winkel te verzenden.

1. Stel **[!UICONTROL Weight Unit]** in op de maateenheid die in uw landinstelling wordt gebruikt.

   - `Pounds`
   - `Kilograms`

1. Voer de **[!UICONTROL Maximum Package Weight]** in die is toegestaan voor FedEx-verzendingen.

   Het standaard FedEx maximumgewicht is 150 lbs. Raadpleeg uw verzendende maatschappij voor meer informatie. De standaardwaarde wordt aanbevolen, tenzij u speciale regelingen hebt getroffen met FedEx. Zie [&#x200B; Afmetingen gewicht &#x200B;](carriers.md#dimensional-weight) voor meer informatie.

   ![&#x200B; de Montages van het Pakket FedEx &#x200B;](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png)

1. Configureer de opties voor de behandelingskosten naar wens.

   De verpakkingskosten zijn optioneel en zijn niet zichtbaar tijdens het afrekenen. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

   - Instellen **[!UICONTROL Calculate Handling Fee]** :

      - `Fixed Fee`
      - `Percentage`

   - Kies bij **[!UICONTROL Handling Applied]** een van de volgende methoden voor het beheer van afhandelingskosten:

      - `Per Order`
      - `Per Package`

   - Voer de **[!UICONTROL Handling Fee]** in als een `fixed` bedrag of `percentage` , afhankelijk van de berekeningsmethode.

1. Stel **[!UICONTROL Residential Delivery]** in op een van de volgende opties, afhankelijk van het feit of u Business-to-Consumer (B2C) of Business-to-Business (B2B) verkoopt.

   - `Yes` - Voor B2C-residentiële leveringen.
   - `No` - Voor B2B-residentiële leveringen.

   ![&#x200B; FedEx die de Montages van de Vergoeding &#x200B;](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png) behandelt

## Stap 4: Toegestane methoden en toepasselijke landen

1. Stel **[!UICONTROL Allowed Methods]** in op elke verzendmethode die u wilt aanbieden.

   Houd bij het kiezen van methoden rekening met uw FedEx-account, de frequentie en de grootte van uw verzendingen en als u internationale verzendingen toestaat. U kunt zo veel of zo weinig methoden aanbieden als u wilt, zoals:

   - Eerste prioriteit Europa
   - Opties voor de leveringsdag: 1-daagse vracht, 2-daagse vracht, 2-daagse, 2-daagse AM, 3-daagse vracht
   - Binnenlandse opties — Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Internationale opties - Internationale economie, binnenlandse economie, goederenvervoer, internationale eerste, internationale grond, internationaal, prioritair
   - Prioriteitsopties - Vracht, Prioriteit overnight
   - Slim post-als het aanbieden van de Slimme methode van Post (ga **identiteitskaart van de Hub** in)
   - Goederenopties — Vracht, nationaal goederenvervoer

1. Als u a [&#x200B; Vrij Verschepend &#x200B;](shipping-free.md) optie door FedEx wilt verstrekken, plaats de vrije het verschepen opties.

   - Stel **[!UICONTROL Free Method]** in op de methode die u voor gratis verzending wilt gebruiken. Kies `None` als je geen gratis verzending via FedEx wilt aanbieden.

   - Stel **[!UICONTROL Enable Free Shipping Threshold]** in op `Enable` als u een minimale bestelling wilt vereisen die in aanmerking komt voor gratis verzending met FedEx. Voer vervolgens de minimumwaarde in **[!UICONTROL Free Shipping Amount Threshold]** in.

   Deze instelling is vergelijkbaar met de instelling voor de standaardmethode voor gratis verzending, maar wordt tijdens het uitchecken weergegeven in de sectie FedEx, zodat klanten weten welke methode wordt gebruikt voor hun bestelling.

1. Wijzig indien nodig de **[!UICONTROL Displayed Error Message]** .

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als FedEx niet beschikbaar is.

   ![&#x200B; FedEx Toegestane Methoden van de Levering &#x200B;](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png)

1. Instellen **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - de klanten van alle [&#x200B; landen &#x200B;](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze leveringsmethode gebruiken.

   - `Specific Countries` - wanneer u deze optie kiest, verschijnt de _Schip aan Specifieke Landen_ lijst. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Stel **[!UICONTROL Debug]** in op `Yes` als u een logboek wilt bijhouden van alle communicatie tussen uw winkel en het FedEx-systeem.

1. Instellen **[!UICONTROL Show Method if Not Applicable]** :

   - `Yes` - Toont alle verzendmethoden van FedEx aan klanten, ongeacht hun beschikbaarheid.
   - `No` - Geeft alleen de verzendmethoden van FedEx weer die van toepassing zijn op de bestelling.

1. Voer bij **[!UICONTROL Sort Order]** een getal in om te bepalen in welke volgorde FedEx wordt weergegeven wanneer deze bij andere leveringsmethoden wordt vermeld tijdens het afrekenen.

   `0` = first, `1` = second, `2` = third, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

   ![&#x200B; FedEx Toepasselijke Landen &#x200B;](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png)

>[!NOTE]
>
>Commerce declareert altijd de volledige bestellingsprijs aan FedEx bij het berekenen van verzendkosten. Dit gedrag kan niet worden gewijzigd.
