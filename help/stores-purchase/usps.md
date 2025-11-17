---
title: United States Postal Service (USPS)
description: Leer hoe u USPS instelt als een verzendprovider voor uw winkel.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: be8a4e9d7cbcf34452724f8055980007794f525f
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# United States Postal Service (USPS)

De United States Postal Service is de onafhankelijke postdienst van de Amerikaanse overheid, die binnenlandse en internationale scheepvaartdiensten over land en door de lucht aanbiedt.

## Stap 1: Een verzendaccount voor USPS openen

Open a [ rekening van de Hulpmiddelen van het Web van USPS ][1]. Nadat je het registratieproces hebt voltooid, ontvang je je gebruikersnaam en een URL naar de testserver van USPS.

U kunt ook de 1} rekening van de Hulpmiddelen van het Web van a [ USPS {openen. ][1] Nadat je het registratieproces hebt voltooid, ontvang je je gebruikersnaam en een URL naar de testserver van USPS. Meer over de Hulpmiddelen van het Web van USPS leren, zie hun [ Technische Documentatie ][2].

## Stap 2: USPS inschakelen voor uw winkel

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Delivery Methods]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL USPS]** sectie uit.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om de volgende instellingen te wijzigen zoals beschreven.

1. Stel **[!UICONTROL Enabled for Checkout]** in op `Yes` .

1. Stel **[!UICONTROL USPS Type]** in op `USPS Rest APIs` als u de REST-API van USPS gebruikt.

   Als u de API voor webgereedschappen van USPS gebruikt, stelt u **[!UICONTROL USPS Type]** in op `USPS Web Tools API` .

1. Voer indien nodig de **[!UICONTROL Gateway URL]** in om de verzendkosten van USPS te openen.

   Het veld is standaard vooraf ingesteld en hoeft normaal gesproken niet te worden gewijzigd.

1. Voer een **[!UICONTROL Title]** in voor deze verzendmethode die tijdens het uitchecken wordt weergegeven.

1. Gebruik de gegevens die door USPS worden verstrekt om de volgende gebieden in te vullen:

   Als u de USPS Rest-API&#39;s gebruikt, moet u de volgende referenties opgeven:

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   Als u de USPS Web Tools API gebruikt, moet u de volgende geloofsbrieven verstrekken:

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. Stel **[!UICONTROL Mode]** in op een van de volgende opties:

   - `Development` - Voert USPS uit in een testomgeving. Nadat u USPS hebt uitgevoerd in een ontwikkelomgeving, moet u ervoor zorgen dat u later terugkeert en Modus instelt op `Live` .
   - `Live` - Voert USPS uit in een live productieomgeving.

## Stap 3: de verpakkingsbeschrijving invullen

1. Als u wilt bepalen hoe de volgorde wordt beheerd wanneer deze als meerdere pakketten wordt verzonden, stelt u **[!UICONTROL Packages Request Type]** in op een van de volgende opties:

   - `Divide to Equal Weight` - (Eén aanvraag) De verzending van meerdere pakketten kan als één aanvraag worden ingediend als de pakketten worden gedeeld door hetzelfde gewicht.
   - `Use Origin Weight` - (Meerdere aanvragen) Meerdere pakketten moeten als afzonderlijke aanvragen worden ingediend als het oorsprongsgewicht wordt gebruikt als basis voor de berekening van de verzendkosten.

1. Stel **[!UICONTROL Container]** in op het type verpakking dat normaal wordt gebruikt voor het verzenden van producten die voor uw winkel zijn besteld.

1. Stel de **[!UICONTROL Size]** in van het gebruikelijke pakket dat vanuit uw winkel wordt verzonden.

1. Stel **[!UICONTROL Machinable]** in op een van de volgende opties:

   - `Yes` - Als uw standaardpakket door een computer kan worden verwerkt.
   - `No` - Als het gebruikelijke pakket handmatig moet worden verwerkt.

1. Voer de **[!UICONTROL Maximum Package Weight]** in op basis van de vereisten van de provider.

   ![ USPS het Verpakken Montages ](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Stap 4: Afhandelingskosten instellen

De afhandelingskosten zijn optioneel en worden als extra kosten aan de DHL-verzendkosten toegevoegd. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

1. Stel **[!UICONTROL Calculate Handling Fee]** in op een van de volgende methoden:

   - `Fixed`
   - `Percent`

1. Stel **[!UICONTROL Handling Applied]** in op een van de volgende opties om te bepalen hoe de behandelingskosten worden toegepast:

   - `Per Order`
   - `Per Package`

1. Voer het bedrag in van de **[!UICONTROL Handling Fee]** die moet worden geladen.

   Gebruik de decimale notatie als u een percentage wilt invoeren. Voer bijvoorbeeld `0.25` in voor 25%.

   ![ de Behandelingskosten van USPS ](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Stap 5: Geef de toegestane methoden en de toepasselijke landen op

1. Kies voor **[!UICONTROL Allowed Methods]** elke verzendmethode van USPS die beschikbaar is voor uw klanten.

   De methoden worden onder USPS weergegeven tijdens het afrekenen. Als u meerdere methoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Als u a [ Vrij Verschepend ](shipping-free.md) optie door USPS wilt verstrekken, plaats de vrije het verschepen opties:

   - Stel **[!UICONTROL Free Method]** in op de methode die u voor gratis verzending wilt gebruiken. Kies `None` als je geen gratis verzending via USPS wilt aanbieden.

   - Stel **[!UICONTROL Enable Free Shipping Threshold]** in op `Enable` als u een minimale bestelling wilt vereisen die in aanmerking komt voor gratis verzending met USPS. Voer vervolgens de minimumwaarde in **[!UICONTROL Free Shipping Amount Threshold]** in.

1. Wijzig indien nodig de **[!UICONTROL Displayed Error Message]** .

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als USPS niet meer beschikbaar is.

   ![ USPS Toegestane Methoden ](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Ship to Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze leveringsmethode gebruiken.
   - `Specific Countries` - wanneer u deze optie kiest, verschijnt de _Schip aan Specifieke Landen_ lijst. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

   ![ USPS Toepasselijke Landen ](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Show Method if Not Applicable]** in op een van de volgende opties:

   - `Yes` - Vermeldt alle beschikbare verzendmethoden van USPS tijdens het afrekenen, inclusief methoden die niet van toepassing zijn op de verzending.
   - `No` - Vermeldt alleen de verzendmethoden van USPS die van toepassing zijn op de verzending.

1. Als u een logbestand wilt maken met de details van USPS-verzendingen die vanuit uw winkel zijn gemaakt, stelt u **[!UICONTROL Debug]** in op `Yes` .

1. Voer bij **[!UICONTROL Sort Order]** een getal in om te bepalen in welke volgorde USPS wordt weergegeven wanneer deze bij andere leveringsmethoden tijdens het afrekenen wordt vermeld.

   `0` = first, `1` = second, `2` = third, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm

<!-- Last updated from includes: 2025-10-29 05:34:15 -->
