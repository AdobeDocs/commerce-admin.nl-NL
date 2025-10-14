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

![&#x200B; In-store Methode van de Levering bij Controle &#x200B;](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Tijdens het afrekenen op de winkel:

1. De klant klikt op **[!UICONTROL Pick In Store]** of selecteert de verzendmethode _[!UICONTROL In-Store Pickup Delivery]_.
1. Het tabblad _[!UICONTROL Pick In Store]_&#x200B;Uitchecken wordt geopend.

Wanneer de klant een adres heeft of het formulier voor het verzendadres heeft ingevuld voordat de klant naar het tabblad _[!UICONTROL Pick In Store]_&#x200B;gaat:

- De dichtstbijzijnde bron aan het klantenadres binnen de gevormde straal wordt automatisch vooraf geselecteerd als ophaalopslag.
- Wanneer de klant op **[!UICONTROL Select Other]** klikt, wordt het zoekformulier van _[!UICONTROL Select Store]_&#x200B;geopend. Alleen opslagruimten binnen de geconfigureerde afstand (straal) tot de vooraf geselecteerde opslagruimte worden in de lijst weergegeven. Alle opslagruimten in de lijst worden gesorteerd op de afstand tot de vooraf geselecteerde opslagplaats.
- Wanneer de klant een postcode of plaatsnaam in het onderzoeksgebied ingaat, slechts worden de opslag binnen de gevormde afstand (straal) aan de gezochte plaats getoond in de lijst. Alle opslagruimten in de lijst worden gesorteerd op de afstand tot de gezochte locatie.
- Wanneer de klant de postcode of plaatsnaam van het onderzoeksgebied ontruimt, worden alle ophaalwinkels die aan de producten in het winkelwagentje worden toegewezen getoond aan de klant. Alle opslagruimten in de lijst worden in oplopende volgorde van de broncodes gesorteerd zonder beperking van de afstand (straal).

Als de klant geen adres heeft of het formulier voor het verzendadres niet eerder heeft ingevuld voordat wordt overgeschakeld op het tabblad _[!UICONTROL Pick In Store]_:

- De pagina toont _wij konden oppikken geen op beschikbare informatie_ bericht worden gebaseerd die op bestelplaats vooraf selecteren.
- Wanneer de klant op **[!UICONTROL Select Store]** klikt, wordt het zoekformulier van _[!UICONTROL Select Store]_&#x200B;geopend.
- Alle ophaalwinkels die aan de producten in het winkelwagentje zijn toegewezen, worden in oplopende volgorde van de broncodes weergegeven zonder beperking van de afstand (straal).
- Wanneer de klant een postcode of plaatsnaam in het onderzoeksgebied ingaat, slechts worden de opslag binnen de gevormde afstand (straal) aan de gezochte plaats getoond in de lijst. Alle opslagruimten in de lijst worden gesorteerd op de afstand tot de gezochte locatie.

## Voor installatie

- Zorg ervoor u een non-default voorraad en een bron hebt. Voor meer informatie over hoe te om een bron als bestelwagenplaats te vormen, zie [&#x200B; een bron &#x200B;](../inventory-management/sources-add.md) toevoegen.
- Zorg ervoor u een Prioritair Algorithm van de Afstand hebt gevormd. Voor meer informatie, zie [&#x200B; het Prioritaire Algoritme van de Afstand &#x200B;](../inventory-management/distance-priority-algorithm.md) vormen.
- Zorg ervoor u [&#128279;](../inventory-management/cli.md#import-geocodes) alle noodzakelijke geocodes voor off-line berekening hebt gedownload en ingevoerd.
- Zorg ervoor u [&#x200B; de montages van de Berekening van de StandaardBelastingbestemming &#x200B;](../configuration-reference/sales/tax.md#default-tax-destination-calculation) hebt gevormd.

>[!IMPORTANT]
>
>**in de storefront, worden de onderzoeksresultaten gefiltreerd door afstand (straal) om relevante resultaten te tonen:**<br><br>
>Als de klant een het verschepen adres heeft, wordt de basisplaats om de afstand (straal) te berekenen genomen van het het verschepen adres.<br><br>
>Als de klant geen verschepend adres heeft, wordt de basisplaats om de afstand te berekenen genomen van de [&#128279;](../configuration-reference/sales/tax.md#default-tax-destination-calculation) montages van de Berekening van de StandaardBTW van de Bestemming . Deze montages worden geplaatst per archiefmening en u moet de montages van de Berekening van de StandaardBelastingbestemming vormen om ervoor te zorgen dat het onderzoek van de ophaalwinkel behoorlijk werkt.

## In-store levering instellen

Eerst, controleer dat de levering in-store wordt toegelaten.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Delivery Methods]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL In-Store Delivery]** sectie uit.

   ![&#x200B; In-store Levering &#x200B;](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enabled]** in op `Yes` .

   >[!NOTE]
   >
   >Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om de standaardinstelling voor een veld te wijzigen.

1. Voer de **[!UICONTROL Method Name]** in die de berekeningsmethode beschrijft die wordt gebruikt om een verzendschatting te maken.

   De naam van de methode staat naast de berekende geschatte snelheid in het winkelwagentje.

1. Ga **[!UICONTROL Title]** in die u voor _in-Opslag de sectie van de Levering_ tijdens controle wilt verschijnen.

   De standaardtitel is `In-Store Pickup Delivery` .

1. Als u klanten kosten wilt aanrekenen voor de service voor het ophalen in de winkel, voert u de kosten in het veld **[!UICONTROL Price]** in.

1. Voer de **[!UICONTROL Search Radius]** in kilometers in voor het zoeken naar de locatie van de ophaalservice bij het uitchecken van winkels.

1. Voer bij **[!UICONTROL Displayed Error Message]** het bericht in dat wordt weergegeven als de levering in de winkel niet meer beschikbaar is.

   Het standaardbericht is `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Klik op **[!UICONTROL Save Config]**.
