---
title: United States Postal Service (USPS)
description: Leer hoe u USPS instelt als een verzendprovider voor uw winkel.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# United States Postal Service (USPS)

De United States Postal Service is de onafhankelijke postdienst van de Amerikaanse overheid, die binnenlandse en internationale scheepvaartdiensten over land en door de lucht aanbiedt.

## Stap 1: Een verzendaccount voor USPS openen

Een [USPS-webgereedschappen][1] account. Nadat je het registratieproces hebt voltooid, ontvang je je gebruikersnaam en een URL naar de testserver van USPS.

U kunt ook een [USPS-webgereedschappen][1] account. Nadat je het registratieproces hebt voltooid, ontvang je je gebruikersnaam en een URL naar de testserver van USPS. Voor meer informatie over de Webhulpmiddelen van USPS, zie hun [Technische documentatie][2].

## Stap 2: USPS inschakelen voor uw winkel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL USPS]** sectie.

   >[!NOTE]
   >
   >Schakel indien nodig eerst de optie **[!UICONTROL Use system value]** Schakel het selectievakje in om de volgende instellingen te wijzigen zoals beschreven.

1. Set **[!UICONTROL Enabled for Checkout]** tot `Yes`.

1. Voer zo nodig de **[!UICONTROL Gateway URL]** voor toegang tot verzendkosten van USPS.

   >[!IMPORTANT]
   >
   >Vanaf 24 juni 2021 verwijdert USPS Web Tools de ondersteuning voor alle onveilige HTTP-eindpunten. Na deze verandering, zullen alle hulpmiddelen API van het Web verzoeken dat aan een onbeveiligd eindpunt van HTTP zal ontbreken. Zorg ervoor dat uw **[!UICONTROL Gateway URL]** gebruikt het veilige eindpunt HTTPS.

   Het veld is standaard vooraf ingesteld en hoeft normaal gesproken niet te worden gewijzigd.

1. Voer een **[!UICONTROL Title]** voor deze verzendmethode die tijdens het afrekenen wordt weergegeven.

1. Voer de **[!UICONTROL User ID]** en **[!UICONTROL Password]** voor uw USPS-account.

1. Set **[!UICONTROL Mode]** op een van de volgende wijzen:

   - `Development` - Voert USPS uit in een testomgeving. Nadat u USPS hebt uitgevoerd in een ontwikkelomgeving, moet u ervoor zorgen dat u later terugkeert en Modus instelt op `Live`.
   - `Live` - Voert USPS uit in een live productieomgeving.

## Stap 3: de verpakkingsbeschrijving invullen

1. Om te bepalen hoe de orde wordt beheerd als verzonden als veelvoudige pakketten, plaats **[!UICONTROL Packages Request Type]** op een van de volgende wijzen:

   - `Divide to Equal Weight` - (Eén aanvraag) De verzending van meerdere verpakkingen kan als één aanvraag worden ingediend indien de verpakkingen worden gedeeld door hetzelfde gewicht.
   - `Use Origin Weight` - (Meerdere verzoeken) Meerdere pakketten moeten als afzonderlijke aanvragen worden ingediend als het oorsprongsgewicht wordt gebruikt als basis voor de berekening van de verzendkosten.

1. Set **[!UICONTROL Container]** op het soort verpakking dat gewoonlijk wordt gebruikt voor het verzenden van producten die voor uw winkel zijn besteld.

1. Stel de **[!UICONTROL Size]** van het gebruikelijke pakket dat vanuit uw winkel wordt verzonden.

1. Set **[!UICONTROL Machinable]** op een van de volgende wijzen:

   - `Yes` - Als uw typische verpakking door een machine kan worden verwerkt.
   - `No` - Als de gebruikelijke verpakking handmatig moet worden verwerkt.

1. Voer de **[!UICONTROL Maximum Package Weight]** volgens de eisen van de vervoerder.

   ![Verpakkingsinstellingen USPS](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Stap 4: Afhandelingskosten instellen

De afhandelingskosten zijn optioneel en worden als extra kosten aan de DHL-verzendkosten toegevoegd. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

1. Set **[!UICONTROL Calculate Handling Fee]** op een van de volgende wijzen:

   - `Fixed`
   - `Percent`

1. Om te bepalen hoe de behandelingskosten worden toegepast, stelt u **[!UICONTROL Handling Applied]** op een van de volgende wijzen:

   - `Per Order`
   - `Per Package`

1. Voer de hoeveelheid van de **[!UICONTROL Handling Fee]** in rekening te brengen.

   Gebruik de decimale notatie als u een percentage wilt invoeren. Voer bijvoorbeeld `0.25` voor 25%.

   ![Verzendkosten voor USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Stap 5: Geef de toegestane methoden en de toepasselijke landen op

1. Voor **[!UICONTROL Allowed Methods]**, kiest u elke verzendmethode van USPS die beschikbaar is voor uw klanten.

   De methoden worden onder USPS weergegeven tijdens het afrekenen. Als u meerdere methoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Als u een [Gratis verzending](shipping-free.md) Stel de opties voor gratis verzending in via USPS:

   - Set **[!UICONTROL Free Method]** op de methode die je wilt gebruiken voor gratis verzending. Kies `None`.

   - Als u een minimale bestelling wilt vereisen die in aanmerking komt voor gratis verzending met USPS, stelt u **[!UICONTROL Enable Free Shipping Threshold]** tot `Enable`. Voer vervolgens de minimumwaarde in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Wijzig, indien nodig, de **[!UICONTROL Displayed Error Message]**.

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als USPS niet meer beschikbaar is.

   ![Toegestane USPS-methoden](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Ship to Applicable Countries]** op een van de volgende wijzen:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) gespecificeerd in uw archiefconfiguratie kan deze leveringsmethode gebruiken.
   - `Specific Countries` - Als u deze optie kiest, _Schip naar specifieke landen_ wordt weergegeven. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

   ![Toepasselijke landen van USPS](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Show Method if Not Applicable]** op een van de volgende wijzen:

   - `Yes` - Vermeldt alle beschikbare verzendmethoden van USPS tijdens het afrekenen, inclusief methoden die niet van toepassing zijn op de verzending.
   - `No` - Vermeldt alleen de verzendmethoden van USPS die van toepassing zijn op de verzending.

1. Als u een logbestand wilt maken met de details van USPS-verzendingen die vanuit uw winkel zijn gemaakt, stelt u **[!UICONTROL Debug]** tot `Yes`.

1. Voor **[!UICONTROL Sort Order]** voert u een getal in om de volgorde te bepalen waarin USPS wordt weergegeven bij andere leveringsmethoden tijdens het afrekenen.

   `0` = eerst, `1` = seconde, `2` = derde, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
