---
title: United Parcel Service (UPS)
description: Leer hoe u UPS instelt als een verzendprovider voor uw winkel.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) biedt binnenlandse en internationale scheepvaartdiensten over land en door de lucht aan naar meer dan 220 landen.

{{ups-api}}

>[!NOTE]
>
>UPS kan [dimensionaal gewicht](carriers.md#dimensional-weight) om bepaalde verzendkosten te bepalen. Adobe Commerce ondersteunt echter alleen berekening van verzendkosten op basis van gewicht.

## Stap 1: Een UPS-verzendaccount openen

Als u deze verzendmethode aan uw klanten wilt aanbieden, moet u eerst een account bij UPS openen.

## Stap 2: UPS inschakelen voor uw winkel

1. Op de _Admin sidebar_, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het deelvenster aan de linkerkant, onder **[!UICONTROL Sales]**, kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL UPS]** sectie.

1. Set **[!UICONTROL Enabled for Checkout]** tot `Yes`.

1. Ga als volgt te werk voor een UPS REST-account (standaardwaarde):

   - Voer uw UPS-gebruikersgegevens in: UPS ClientID als **[!UICONTROL User ID]**, UPS-clientgeheim als **[!UICONTROL Password]**

   - Set **[!UICONTROL Mode]** tot `Live` gegevens naar het UPS-verzendsysteem verzenden via een beveiligde verbinding. (In de ontwikkelingsmodus worden geen gegevens verzonden via een beveiligde verbinding.)

   - Controleer de **[!UICONTROL Gateway URL]** dat nodig is om verzoeken te verzenden. Gebruik een sandbox-URL voor de testmodus en een productie-URL voor liveaanvragen.

   - Controleer de **[!UICONTROL Tracking URL]** is vereist voor het ophalen van trackinggegevens. Gebruik een sandbox-URL voor de testmodus en een productie-URL voor liveaanvragen.

   - Set **[!UICONTROL Origin of the Shipment]** naar de regio waar de overbrenging haar oorsprong heeft.

   - Als u speciale tarieven met UPS hebt, plaats **[!UICONTROL Enable Negotiated Rates]** tot `Yes` en voert u het zescijferige **[!UICONTROL Shipper Number]** toegewezen aan u door UPS.

   - Set **[!UICONTROL Live Account]** op een van de volgende wijzen:

      - `Yes` - UPS wordt in de productiemodus uitgevoerd en UPS wordt als verzendmethode aan uw klanten aangeboden.
      - `No` - UPS wordt in een testmodus uitgevoerd.

   >[!NOTE]
   >
   >Het standaard United Parcel Service-type is gepland voor afschrijving. Voor nieuwe configuraties, gebruik het gebrek `United Parcel Service REST` type. Het REST-type is ook vereist om [verzendlabels](shipping-labels.md).<br/>
   >Voor de release van 2.4.7 **[!UICONTROL UPS Type]**  is verwijderd omdat `UPS` en `UPS XML` typen zijn gepland voor afgekeurd en `UPS REST` is de standaardwaarde. De API&#39;s van de United Parcel Service (UPS) die door de native Adobe Commerce-integratie worden gebruikt, zijn tijdelijk vervangen omdat deze momenteel geen ondersteuning bieden voor het OAuth 2.0-beveiligingsmodel.

   >[!IMPORTANT]
   >
   >UPS stopt de ondersteuning van HTTP, dat wordt gebruikt in de huidige standaardwaarde (systeemwaarde). Wis de **[!UICONTROL Use system value]** Schakel het selectievakje in en wijzig de URL om HTTPS te gebruiken. Voorbeeld: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Voor **[!UICONTROL Title]**, voert u de naam van deze verzendoptie in zoals u deze tijdens het afrekenen wilt weergeven.

   Dit veld is standaard ingesteld op `United Parcel Service`.

   ![UPS inschakelen](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Stap 3: Voer de beschrijving van de container in

1. Set **[!UICONTROL Packages Request Type]** op een van de volgende wijzen:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Voor **[!UICONTROL Container]**, het typische verpakkingstype specificeren dat voor verzending wordt gebruikt:

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Set **[!UICONTROL Weight Unit]** op het systeem dat u gebruikt om het productgewicht te meten.

   Het gewichtsysteem dat door UPS wordt ondersteund, verschilt per land. Vraag UPS in geval van twijfel welk gewichtssysteem u moet gebruiken. U kunt onder andere de volgende opties kiezen:

   - `LBS`
   - `KGS`

1. Set **[!UICONTROL Destination Type]** op een van de volgende wijzen:

   - `Residential` - De meeste van uw verzendingen zijn zakelijk voor de consument (B2C).
   - `Commercial` - De meeste verzendingen zijn zakelijk (B2B).

1. Voer de **[!UICONTROL Maximum Package Weight]** toegestaan door de vervoerder.

1. Set **[!UICONTROL Pickup Method]** op een van de volgende wijzen:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Voer de **[!UICONTROL Minimum Package Weight]** toegestaan door de vervoerder.

   ![Containerbeschrijving](./assets/ups2.png){width="600" zoomable="yes"}

## Stap 4: Afhandelingskosten instellen

De verpakkingskosten zijn optioneel en worden weergegeven als extra kosten die bij de verzendkosten van de UPS worden opgeteld. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

1. Set **[!UICONTROL Calculate Handling Fee]** op een van de volgende wijzen:

   - `Fixed`
   - `Percent`

1. Om te bepalen hoe de behandelingskosten worden toegepast, stelt u **[!UICONTROL Handling Applied]** op een van de volgende wijzen:

   - `Per Order`
   - `Per Package`

1. Voer de hoeveelheid van de **[!UICONTROL Handling Fee]** in rekening te brengen.

   Gebruik de decimale notatie als u een percentage wilt invoeren. Voer bijvoorbeeld `0.25` voor 25%.

   ![Verhandelingskosten](./assets/ups3.png){width="600" zoomable="yes"}

## Stap 5: Geef de toegestane methoden en de toepasselijke landen op

1. Voor **[!UICONTROL Allowed Methods]**, kiest u elke UPS-verzendmethode die beschikbaar is voor uw klanten.

   De methoden worden onder UPS weergegeven tijdens het uitchecken. Als u meerdere methoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Als u een [Gratis verzending](shipping-free.md) Stel de opties voor gratis verzending in via UPS:

   - Set **[!UICONTROL Free Method]** op de methode die je wilt gebruiken voor gratis verzending. Kies `None`.

   - Als u een minimale bestelling wilt vereisen die in aanmerking komt voor gratis verzending met UPS, stelt u **[!UICONTROL Enable Free Shipping Threshold]** tot `Enable`. Voer vervolgens de minimumwaarde in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Wijzig, indien nodig, de **[!UICONTROL Displayed Error Message]**.

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als UPS niet meer beschikbaar is.

   ![Toegestane methoden](./assets/ups4.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Ship to Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) gespecificeerd in uw archiefconfiguratie kan deze leveringsmethode gebruiken.
   - `Specific Countries` - Als u deze optie kiest, _Schip naar specifieke landen_ wordt weergegeven. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Set **[!UICONTROL Show Method if Not Applicable]** op een van de volgende wijzen:

   - `Yes` - Vermeldt alle beschikbare UPS-verzendmethoden tijdens het afrekenen, inclusief methoden die niet van toepassing zijn op de verzending.
   - `No` - Vermeldt alleen de UPS-verzendmethoden die van toepassing zijn op de verzending.

   ![Toepasselijke landen](./assets/ups5.png){width="600" zoomable="yes"}

1. Als u een logbestand wilt maken met de details van UPS-verzendingen die vanuit uw winkel zijn gemaakt, stelt u **[!UICONTROL Debug]** tot `Yes`.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in om de volgorde te bepalen waarin UPS wordt weergegeven bij andere leveringsmethoden tijdens het afrekenen.

   `0` = eerst, `1` = seconde, `2` = derde, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

## Stap 6: Stel het adres van de verzendoorsprong in

1. Zorg ervoor dat uw [Opslaggegevens](../getting-started/store-details.md#store-information) is voltooid.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en selecteert u **[!UICONTROL Shipping Settings]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Origin]** op de pagina en het adres van de verzendoorsprong configureren.

   ![Verkoopconfiguratie - Adresopties voor oorsprong van verzending](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Bij de berekening van de verzendkosten wordt de volledige bestellingsprijs niet aan UPS aangegeven. Dit gedrag kan niet worden gewijzigd.
