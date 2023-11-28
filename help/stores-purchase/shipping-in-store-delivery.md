---
title: Levering in de winkel
description: Leer hoe u een leveringsoptie in de winkel instelt voor uw winkel.
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Levering in de winkel

Met de in-store leveringsmethode, kan de klant een bron selecteren die als oppiklocatie tijdens het uitrekenen moet worden gebruikt.

![In-store leveringsmethode bij afhandeling](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Tijdens het afrekenen op de winkel:

1. De klant klikt **[!UICONTROL Pick In Store]** of selecteert u de _[!UICONTROL In-Store Pickup Delivery]_verzendmethode.
1. De _[!UICONTROL Pick In Store]_uitchecken wordt geopend.

Wanneer de klant een adres heeft of het formulier voor het verzendadres heeft ingevuld voordat de klant naar de _[!UICONTROL Pick In Store]_tab:

- De dichtstbijzijnde bron aan het klantenadres binnen de gevormde straal wordt automatisch vooraf geselecteerd als ophaalopslag.
- Wanneer de klant klikt **[!UICONTROL Select Other]** de _[!UICONTROL Select Store]_zoekformulier wordt geopend. Alleen opslagruimten binnen de geconfigureerde afstand (straal) tot de vooraf geselecteerde opslagruimte worden in de lijst weergegeven. Alle opslagruimten in de lijst worden gesorteerd op de afstand tot de vooraf geselecteerde opslagplaats.
- Wanneer de klant een postcode of plaatsnaam in het onderzoeksgebied ingaat, slechts worden de opslag binnen de gevormde afstand (straal) aan de gezochte plaats getoond in de lijst. Alle opslagruimten in de lijst worden gesorteerd op de afstand tot de gezochte locatie.
- Wanneer de klant de postcode of plaatsnaam van het onderzoeksgebied ontruimt, worden alle ophaalwinkels die aan de producten in het winkelwagentje worden toegewezen getoond aan de klant. Alle opslagruimten in de lijst worden in oplopende volgorde van de broncodes gesorteerd zonder beperking van de afstand (straal).

Als de klant geen adres heeft of het formulier voor het verzendadres niet eerder heeft ingevuld voordat de klant naar de _[!UICONTROL Pick In Store]_tab:

- Op de pagina worden de _We kunnen de locatie voor het ophalen niet vooraf selecteren op basis van de beschikbare gegevens_ bericht.
- Wanneer de klant klikt **[!UICONTROL Select Store]** de _[!UICONTROL Select Store]_zoekformulier wordt geopend.
- Alle ophaalwinkels die aan de producten in het winkelwagentje zijn toegewezen, worden in oplopende volgorde van de broncodes weergegeven zonder beperking van de afstand (straal).
- Wanneer de klant een postcode of plaatsnaam in het onderzoeksgebied ingaat, slechts worden de opslag binnen de gevormde afstand (straal) aan de gezochte plaats getoond in de lijst. Alle opslagruimten in de lijst worden gesorteerd op de afstand tot de gezochte locatie.

## Voor installatie

- Zorg ervoor u een non-default voorraad en een bron hebt. Voor meer informatie over hoe te om een bron als bestelwagenplaats te vormen, zie [Een bron toevoegen](../inventory-management/sources-add.md).
- Zorg ervoor u een Prioritair Algorithm van de Afstand hebt gevormd. Zie voor meer informatie [Het algoritme voor prioriteitsafstand configureren](../inventory-management/distance-priority-algorithm.md).
- Zorg ervoor dat u [gedownload en geïmporteerd](../inventory-management/cli.md#import-geocodes) alle vereiste geocodes voor offlineberekening.
- Zorg ervoor u hebt gevormd [Berekening standaardbelastingbestemming](../configuration-reference/sales/tax.md#default-tax-destination-calculation) instellingen.

>[!IMPORTANT]
>
>**In de winkel worden de zoekresultaten gefilterd op afstand (straal) om de relevante resultaten weer te geven:**<br><br>
>Als de klant een verzendadres heeft, wordt de basislocatie voor het berekenen van de afstand (straal) overgenomen van het verzendadres.<br><br>
>Als de klant geen verzendadres heeft, wordt de basislocatie voor het berekenen van de afstand overgenomen van [Berekening standaardbelastingbestemming](../configuration-reference/sales/tax.md#default-tax-destination-calculation) instellingen. Deze montages worden geplaatst per archiefmening en u moet de montages van de Berekening van de StandaardBelastingbestemming vormen om ervoor te zorgen dat het onderzoek van de ophaalwinkel behoorlijk werkt.

## In-store levering instellen

Eerst, controleer dat de levering in-store wordt toegelaten.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL In-Store Delivery]** sectie.

   ![Levering in de winkel](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enabled]** tot `Yes`.

   >[!NOTE]
   >
   >Wis indien nodig de **[!UICONTROL Use system value]** Schakel het selectievakje in om de standaardinstelling voor een veld te wijzigen.

1. Voer de **[!UICONTROL Method Name]** een beschrijving van de berekeningsmethode die wordt gebruikt om een schatting van de verzendkosten te maken.

   De naam van de methode staat naast de berekende geschatte snelheid in het winkelwagentje.

1. Voer de **[!UICONTROL Title]** waarvoor u wilt verschijnen _In-Store levering_ -sectie tijdens het afrekenen.

   De standaardtitel is `In-Store Pickup Delivery`.

1. Als u klanten kosten wilt aanrekenen voor de service voor het ophalen in de winkel, voert u de kosten in het dialoogvenster **[!UICONTROL Price]** veld.

1. Voer de **[!UICONTROL Search Radius]** in kilometers voor zoekopdrachten naar locatie van winkel bij winkeluitchecken.

1. Voor **[!UICONTROL Displayed Error Message]** Voer het bericht in dat wordt weergegeven als de levering in de winkel niet meer beschikbaar is.

   Het standaardbericht is `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Klik op **[!UICONTROL Save Config]**.
