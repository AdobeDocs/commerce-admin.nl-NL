---
title: Het algoritme voor prioriteitsafstand configureren
description: Stel de configuratie in voor het vergelijken van de locatie van het verzendadres met de bronlocaties om de dichtstbijzijnde bron voor het uitvoeren van verzendingen te bepalen.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Het algoritme voor prioriteitsafstand configureren

Het algoritme van de Prioriteit van de Afstand vergelijkt de plaats van het verzendende bestemmingsadres met bronplaatsen om de dichtstbijzijnde bron te bepalen om verzendingen te vervullen. De afstand kan worden bepaald door fysieke afstand of tijd die wordt doorgebracht van de ene naar de andere locatie, met behulp van databasegegevens of het rijden, lopen of fietsen. Gebruik deze [Algoritme voor bronselectie](selection-reservations.md) om de dichtstbijzijnde bron aan de verzendende bestemmingsadressen aan te bevelen.

>[!NOTE]
>
>Als u het algoritme van de Prioriteit van de Afstand gebruikt, ga het volledige straatadres en GPS coördinaten voor uw [bronnen](sources-add.md) wordt aanbevolen.

U hebt twee opties om de afstand en de tijd te berekenen om de dichtstbijzijnde bron voor verzending te vinden:

- **GOOGLE MAP** - Gebruik [Google Maps-platform][1] services om de afstand en tijd tussen het verzendadres en de bronlocatie te berekenen. Bij deze optie worden de GPS-coördinaten (Latitude and Longitude) van de bron gebruikt en kan het adres van de straat worden gebruikt, afhankelijk van de berekeningsmodus. Een Google API-sleutel is vereist voor [Geocoding-API][2] en [Distance Matrix API][3] ingeschakeld en je kunt kosten betalen via Google.

- **Offlineberekening** - Berekent de afstand aan de hand van gedownloade en geïmporteerde geocodegegevens met behulp van postcodes en GPS-coördinaten om de dichtstbijzijnde bron voor het verzendende doeladres te bepalen. Als u deze optie wilt configureren, hebt u mogelijk hulp van ontwikkelaars nodig om geocodes in eerste instantie te downloaden en importeren aan de hand van opdrachtregelinstructies.

>[!NOTE]
>
>Voor multi-store website met verscheidene landen, vorm [standaardbelastingbestemming](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} voor elk land.

## Google-kaarten gebruiken

U hebt geen Google-account nodig om aan de slag te gaan. Het proces omvat Google-account en het maken van projecten, indien nodig. Deze optie vereist dat er een factureringsaccount en betalingsmethode aan uw Google-account worden toegevoegd om de configuratie te voltooien en het algoritme te gebruiken.
Google MAP op afstand gebaseerd algoritme wordt echter aanbevolen als geavanceerder en nauwkeuriger in vergelijking met Offlineberekening.

### Stap 1: De Google API-sleutel maken

De toets is afkomstig van de [Google Maps-platform][1] en moet [Geocoding-API][2] en [Distance Matrix API][3] ingeschakeld. Zie voor meer informatie [Algorithm Distance Priority configureren](distance-priority-algorithm.md).

1. Bezoek [Google Maps-platform][1] en klik op **[!UICONTROL Get Started]**.

1. Selecteer **[!UICONTROL Maps, Routes, and Places]** en klik op **[!UICONTROL Continue]**.

   ![Google Maps Platform voor uw Sleutel](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Meld u aan met een Google-account of maak een account.

1. Een project instellen:

   - Selecteer een project of ga een nieuwe projectnaam in.

   - Selecteer `Yes`.

   - Klik op **[!UICONTROL Next]**.

1. Voer een factureringsaccount in of maak er een. U kunt een factureringsaccount later overslaan en toevoegen.

   U hebt een factureringsaccount nodig om deze service te kunnen gebruiken.

1. Als u de opties voor het Google Cloud Platform wilt openen en configureren, klikt u op **[!UICONTROL Console]**.

   - Open uw project.

   - Het menu uitvouwen en klikken **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Google API Services](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - Zoeken naar [Geocoding-API][2] en [Distance Matrix API][3]. Selecteer en laat elke dienst toe.

1. Vouw het menu uit en klik op **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]** en kopieer de Google API-sleutel.

   ![Google API Key Copy](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### Stap 2: De Google MAP-provider configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Inventory]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Distance Provider for Distance Based SSA]_sectie en set **[!UICONTROL Provider]**tot `Google MAP`.

   ![Leveranciers voor op afstand-Gebaseerde SSA](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Google Distance Provider]_de instellingen te configureren:

   - Voor **[!UICONTROL Google API Key]**, voert u de uit uw Google-account gekopieerde sleutel in.

   - Voor **[!UICONTROL Computation mode]** selecteert u een configuratie.

     >[!NOTE]
     >
     >Wanneer het gebruiken van dit algoritme voor het verschepen, als de routes en de gegevens niet voor de geselecteerde wijze van de Berekening (het besturen, het fietsen, of het lopen) voor een lading terugkeren, blijft SSA aan het gebruiken van de Prioriteit Bron in gebreke. De instelling van [prioriteit voor bronnen per bestand](stocks-prioritize-sources.md) wordt aanbevolen.

     | Optie | Beschrijving |
     | ----- | ----- |
     | `Driving` | (Standaard) Vereist standaard rijrichtingen die het wegennet gebruiken. |
     | `Walking` | Verzoekt lopende richtingen met gebruik van voetgangerspaden en zijkanten (indien beschikbaar). |
     | `Bicycling` | Verzoekt fietsrichtingen met fietspaden en de voorkeurstraten (indien beschikbaar). De [service Afstandsmatrix][4] is alleen beschikbaar in de VS en sommige Canadese steden. |

   - Voor **[!UICONTROL Value]** selecteert u een waardetype:

     | Optie | Beschrijving |
     | ----- | ----- |
     | `Distance` | (Standaard) Geeft de afstand tussen punten in metriek (kilometers en meters) of imperial (mijlen en voeten). |
     | `Time to Destination` | Retourneert de tijd die nodig is om van de bronlocaties naar het verzendadres te gaan in uren en minuten. |

   ![Google Distance Provider](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Offline berekening gebruiken

Offlineberekeningen gebruiken landcodes om de afstand tussen de verzendbestemming en de bronadressen te bepalen. Voor deze optie is mogelijk hulp van ontwikkelaars nodig bij het configureren. Een [!DNL Inventory Management] CLI-opdracht om gegevens te downloaden en importeren van [geonames.org][5].

>[!NOTE]
>
>Geocodes importeren van [geonames.org][5] hebben beperkingen voor sommige landen, zoals Canada en Ierland. Zie [GeoNames Postal Code-bestanden][6] voor meer informatie .

### Stap 1: geocodes downloaden en importeren

Volledige bevel-lijn configuratie om geocodes landen te downloaden en in te voeren om te verzenden naar en bronplaatsen in te hebben. Voor deze stap is mogelijk hulp van de ontwikkelaar nodig bij het uitvoeren van opdrachtregeltaken. Zie [Geocodes importeren](cli.md#import-geocodes).

Vul deze opdrachten altijd in als u meer geocodes wilt toevoegen.

### Stap 2: De berekening instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Inventory]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Distance Provider for Distance Based SSA]_sectie.

1. Hef de selectie van **[!UICONTROL Use system value]** selectievakje en set **[!UICONTROL Provider]** tot `Offline Calculation`.

   ![Leveranciers van afstand voor Op afstand gebaseerde SSA](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
