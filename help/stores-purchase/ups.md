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
>UPS kan [ dimensionaal gewicht ](carriers.md#dimensional-weight) gebruiken om sommige het verschepen tarieven te bepalen. Adobe Commerce ondersteunt echter alleen berekening van verzendkosten op basis van gewicht.

## Stap 1: Een UPS-verzendaccount openen

Als u deze verzendmethode aan uw klanten wilt aanbieden, moet u eerst een account bij UPS openen.

## Stap 2: UPS inschakelen voor uw winkel

1. Voor _Admin sidebar_, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder **[!UICONTROL Sales]** de optie **[!UICONTROL Delivery Methods]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL UPS]** sectie uit.

1. Stel **[!UICONTROL Enabled for Checkout]** in op `Yes` .

1. Ga als volgt te werk voor een UPS REST-account (standaardwaarde):

   - Voer uw UPS-gebruikersgegevens in: UPS ClientID als **[!UICONTROL User ID]**, UPS Client Secret als **[!UICONTROL Password]**

   - Stel **[!UICONTROL Mode]** in op `Live` om gegevens via een veilige verbinding naar het UPS-verzendsysteem te verzenden. (In de ontwikkelingsmodus worden geen gegevens verzonden via een beveiligde verbinding.)

   - Controleer **[!UICONTROL Gateway URL]** die nodig is om aanvragen te verzenden. Gebruik een sandbox-URL voor de testmodus en een productie-URL voor liveaanvragen.

   - Controleer **[!UICONTROL Tracking URL]** die nodig is voor het ophalen van trackinggegevens. Gebruik een sandbox-URL voor de testmodus en een productie-URL voor liveaanvragen.

   - Stel **[!UICONTROL Origin of the Shipment]** in op het gebied waar de verzending vandaan komt.

   - Als u speciale tarieven met UPS hebt, plaats **[!UICONTROL Enable Negotiated Rates]** aan `Yes` en ga zes-cijfer **[!UICONTROL Shipper Number]** in die aan u door UPS wordt toegewezen.

   - Stel **[!UICONTROL Live Account]** in op een van de volgende opties:

      - `Yes` - Voert UPS uit in de productiemodus en biedt UPS als verzendmethode aan uw klanten.
      - `No` - Voert UPS in een testmodus uit.

   >[!NOTE]
   >
   >Het standaard United Parcel Service-type is gepland voor afschrijving. Voor nieuwe configuraties gebruikt u het standaardtype `United Parcel Service REST` . Het REST type wordt ook vereist om [ verschepende etiketten ](shipping-labels.md) te produceren.<br/>
   >Voor de release 2.4.7 wordt **[!UICONTROL UPS Type]** verwijderd omdat de typen `UPS` en `UPS XML` gepland zijn voor afschrijving en `UPS REST` de standaardwaarde is. De API&#39;s van de United Parcel Service (UPS) die door de native Adobe Commerce-integratie worden gebruikt, zijn tijdelijk vervangen omdat deze momenteel geen ondersteuning bieden voor het OAuth 2.0-beveiligingsmodel.

   >[!IMPORTANT]
   >
   >UPS stopt de ondersteuning van HTTP, dat wordt gebruikt in de huidige standaardwaarde (systeemwaarde). Schakel het selectievakje **[!UICONTROL Use system value]** uit en wijzig de URL om HTTPS te gebruiken. Voorbeeld: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Voer bij **[!UICONTROL Title]** de naam van deze verzendoptie in zoals u deze tijdens het afrekenen wilt weergeven.

   Dit veld is standaard ingesteld op `United Parcel Service` .

   ![ laat UPS ](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"} toe

## Stap 3: Voer de beschrijving van de container in

1. Stel **[!UICONTROL Packages Request Type]** in op een van de volgende opties:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Geef bij **[!UICONTROL Container]** het typische pakkettype op dat wordt gebruikt voor verzending:

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

1. Stel **[!UICONTROL Weight Unit]** in op het systeem dat u gebruikt om het productgewicht te meten.

   Het gewichtsysteem dat door UPS wordt ondersteund, verschilt per land. Vraag UPS in geval van twijfel welk gewichtssysteem u moet gebruiken. U kunt onder andere de volgende opties kiezen:

   - `LBS`
   - `KGS`

1. Stel **[!UICONTROL Destination Type]** in op een van de volgende opties:

   - `Residential` - De meeste van uw verzendingen zijn zakelijk voor consumenten (B2C).
   - `Commercial` - De meeste van uw verzendingen zijn zakelijk (B2B).

1. Voer de **[!UICONTROL Maximum Package Weight]** in die de vervoerder toestaat.

1. Stel **[!UICONTROL Pickup Method]** in op een van de volgende opties:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Voer de **[!UICONTROL Minimum Package Weight]** in die de vervoerder toestaat.

   ![ Beschrijving van de Container ](./assets/ups2.png){width="600" zoomable="yes"}

## Stap 4: Afhandelingskosten instellen

De verpakkingskosten zijn optioneel en worden weergegeven als extra kosten die bij de verzendkosten van de UPS worden opgeteld. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

1. Stel **[!UICONTROL Calculate Handling Fee]** in op een van de volgende methoden:

   - `Fixed`
   - `Percent`

1. Stel **[!UICONTROL Handling Applied]** in op een van de volgende opties om te bepalen hoe de behandelingskosten worden toegepast:

   - `Per Order`
   - `Per Package`

1. Voer het bedrag in van de **[!UICONTROL Handling Fee]** die moet worden geladen.

   Gebruik de decimale notatie als u een percentage wilt invoeren. Voer bijvoorbeeld `0.25` in voor 25%.

   ![ Behandelingskosten ](./assets/ups3.png){width="600" zoomable="yes"}

## Stap 5: Geef de toegestane methoden en de toepasselijke landen op

1. Kies voor **[!UICONTROL Allowed Methods]** elke UPS-verzendmethode die beschikbaar is voor uw klanten.

   De methoden worden onder UPS weergegeven tijdens het uitchecken. Als u meerdere methoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Als u a [ Vrij Verschepend ](shipping-free.md) optie door UPS wilt verstrekken, plaats de vrije het verschepen opties:

   - Stel **[!UICONTROL Free Method]** in op de methode die u voor gratis verzending wilt gebruiken. Kies `None` als je geen gratis verzending via UPS wilt aanbieden.

   - Stel **[!UICONTROL Enable Free Shipping Threshold]** in op `Enable` als u een minimale bestelling wilt vereisen die in aanmerking komt voor gratis verzending met UPS. Voer vervolgens de minimumwaarde in **[!UICONTROL Free Shipping Amount Threshold]** in.

1. Wijzig indien nodig de **[!UICONTROL Displayed Error Message]** .

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als UPS niet meer beschikbaar is.

   ![ Toegestane Methoden ](./assets/ups4.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Ship to Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze leveringsmethode gebruiken.
   - `Specific Countries` - wanneer u deze optie kiest, verschijnt de _Schip aan Specifieke Landen_ lijst. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Stel **[!UICONTROL Show Method if Not Applicable]** in op een van de volgende opties:

   - `Yes` - Vermeldt alle beschikbare verzendmethoden voor UPS tijdens het afrekenen, inclusief methoden die niet van toepassing zijn op de verzending.
   - `No` - Hier worden alleen de UPS-verzendmethoden vermeld die van toepassing zijn op de verzending.

   ![ Toepasselijke Landen ](./assets/ups5.png){width="600" zoomable="yes"}

1. Als u een logbestand wilt maken met de details van UPS-verzendingen die vanuit uw winkel worden gemaakt, stelt u **[!UICONTROL Debug]** in op `Yes` .

1. Voer bij **[!UICONTROL Sort Order]** een getal in om te bepalen in welke volgorde UPS wordt weergegeven wanneer deze bij andere leveringsmethoden tijdens het afrekenen wordt vermeld.

   `0` = first, `1` = second, `2` = third, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

## Stap 6: Stel het adres van de verzendoorsprong in

1. Zorg ervoor dat uw [ Informatie van de Opslag ](../getting-started/store-details.md#store-information) volledig is.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en selecteer **[!UICONTROL Shipping Settings]** .

1. Vouw ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Origin]** op de pagina uit en vorm het verschepende oorsprongadres.

   ![ de configuratie van de Verkoop - verschepende oorsprong adresopties ](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce declareert de volledige bestellingsprijs niet aan UPS bij het berekenen van verzendkosten. Dit gedrag kan niet worden gewijzigd.
