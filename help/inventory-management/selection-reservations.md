---
title: Source-algoritmen en -reserveringen
description: Meer informatie over de Source Selection Algorithm and Reservations-systemen die op de achtergrond worden uitgevoerd om uw verkoopbare hoeveelheden bij te werken.
exl-id: dcd63322-fb4c-4448-b6e7-0c54350905d7
feature: Inventory, Shipping/Delivery
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '2196'
ht-degree: 0%

---

# Source-algoritmen en -reserveringen

De kern van [!DNL Inventory Management] houdt vrijwel en on-hand elk beschikbaar product in uw pakhuizen en winkels bij. De systemen van het Algoritme en van Reservations van de Selectie van Source lopen op de achtergrond, die uw verkoopbare hoeveelheden bijgewerkt houdt, controle vrij van botsingen, en bepleite verzendopties.

>[!NOTE]
>
>Verwijs naar de [ ontwikkelaardocumentatie ](https://developer.adobe.com/commerce/php/development/framework/inventory-management/) voor informatie over het werken met het [!DNL Inventory Management] systeem programmatically.

## Algoritme voor Source-selectie

Het algoritme van de Selectie van Source (SSA) analyseert en bepaalt de beste gelijke voor bronnen en het verschepen gebruikend de prioritaire orde van bronnen die in een voorraad worden gevormd. Tijdens de verzending van orders bevat het algoritme een aanbevolen lijst met bronnen, beschikbare hoeveelheden en bedragen die op basis van het geselecteerde algoritme moeten worden afgetrokken. [!DNL Inventory Management] biedt een algoritme met prioriteit en ondersteunt extensies voor nieuwe opties.

Met meerdere bronlocaties, klanten over de hele wereld en vervoerders met verschillende verzendopties en -kosten kan het lastig zijn om te weten wat uw actuele beschikbare voorraad is en de beste verzendoptie te vinden. SSA doet het werk voor u van het volgen van inventaris verkoopbare hoeveelheden over alle bronnen aan het berekenen en het doen van aanbevelingen voor verzendingen.

**Inventaris van het Spoor** - Gebruikend voorraden en bronnen, controleert SSA het verkoopkanaal van inkomende productverzoeken en bepaalt beschikbare inventaris:

- Berekent de geaggregeerde virtuele verkoopbare hoeveelheid van alle toegewezen bronnen per voorraad: geaggregeerde hoeveelheid - Drempel voor onvoldoende voorraad per bron
- Hiermee trekt u het uit-van-voorraad drempelbedrag af van de verkoopbare hoeveelheid om te beschermen tegen oververkoop
- Reserves inventarishoeveelheden op bestelling, in mindering gebracht op voorraden bij de verwerking van orders en bij de verzending
- Ondersteunt backorders met verbeterde opties voor negatieve drempelwaarden

**beheert Verzendingen** - de algoritmehulp wanneer u en bestellingen verwerkt. U kunt het algoritme in werking stellen om aanbevelingen op de beste bronnen voor het verschepen van het product te krijgen of de selecties met voeten te treden aan:

- Gedeeltelijke verzendingen verzenden, slechts een paar producten van specifieke locaties verzenden en de volledige bestelling later voltooien
- De volledige bestelling van één bron verzenden
- De verzendingen in verschillende hoeveelheden over meerdere bronnen verdelen, waarbij een evenwichtige voorraad in alle opslagplaatsen en opslagplaatsen wordt bewaard

SSA is verlengbaar voor derdesteun en douanealgoritmen voor het adviseren van rendabele verzendingen.

>[!NOTE]
>
>SSA functioneert verschillend voor Virtuele en Downloadbare producten, die geen verzendkosten kunnen maken. In deze gevallen voert het systeem impliciet het algoritme uit wanneer het facturen creeert, en gebruikt altijd de voorgestelde resultaten. U kunt deze resultaten niet aanpassen voor virtuele en downloadbare producten.

### Source Priority Algorithm

Aangepaste voorraden bevatten een lijst met bronnen die via je winkel kunnen worden verkocht en geleverd. Het Prioriteitsalgoritme van Source gebruikt de orde van toegewezen bronnen in de voorraad om productaftrek per bron aan te bevelen wanneer het factureren en het verschepen van de orde.

Bij uitvoering, het algoritme:

- Werkt door de gevormde orde van bronnen op het voorraadniveau die bij de bovenkant beginnen
- beveelt een hoeveelheid aan om per product te verzenden en te leveren op basis van de volgorde in de lijst, de beschikbare hoeveelheid en de bestelde hoeveelheid
- Hiermee gaat u door met de lijst totdat de order is geladen
- Hiermee slaat u uitgeschakelde bronnen over als deze in de lijst worden gevonden

Om, bronnen aan een douanevoorraad te vormen toe te wijzen en opdracht te geven. Zie [ Prioritizing Bronnen voor een Voorraad ](stocks-prioritize-sources.md).

In het volgende voorbeeld worden de toegewezen bronnen op volgorde, de beschikbare hoeveelheid en de aanbevolen bron en het bedrag dat moet worden afgetrokken en het schip. De belangrijkste bron is een Drop Shipper in het Verenigd Koninkrijk met een beschikbare hoeveelheid van 240.

![ aanbevelingen van het Voorbeeld SSA voor een bergfiets ](assets/ssa-sources-example.png){width="600" zoomable="yes"}

### Algoritme voor afstandprioriteit

Het algoritme van de Prioriteit van de Afstand vergelijkt de plaats van het verzendende bestemmingsadres met bronplaatsen om de dichtstbijzijnde bron te bepalen om verzendingen te vervullen. De afstand kan worden bepaald door fysieke afstand of tijd die wordt doorgebracht van de ene naar de andere locatie, met behulp van geïmporteerde databaselocaties of Google-richtingen (rijden, lopen of fietsen).

U hebt twee opties om de afstand en de tijd te berekenen om de dichtstbijzijnde bron voor verzending te vinden:

- **MAP van Google** - gebruikt [ de Diensten van het Platform van de Kaarten van Google ][1] om de afstand en de tijd tussen het verschepende bestemmingsadres en bronplaatsen (adres en GPS coördinaten) te berekenen. Bij deze optie worden de Latitude en Lengtegraad van de bron gebruikt. Een sleutel van Google API wordt vereist met [ Geocoding API ][2] en [ toegelaten de Matrijs van de Afstand API ][3]. Voor deze optie is een factureringsplan voor Google vereist en mogelijk worden kosten in rekening gebracht via Google.

- **Offline Berekening** - berekent de afstand gebruikend gedownloade en ingevoerde geocode gegevens om de dichtste bron aan het verschepende bestemmingsadres te bepalen. Bij deze optie worden de landcodes van het verzendadres en de bron gebruikt. Als u deze optie wilt configureren, hebt u mogelijk hulp van ontwikkelaars nodig om geocodes in eerste instantie te downloaden en importeren via een opdrachtregel.

Selecteer configuraties en voer aanvullende stappen uit, zoals de Google API-sleutel of het downloaden van verzendgegevens. Zie [ het Prioritaire Algoritme van de Afstand ](distance-priority-algorithm.md) vormen.

### Aangepaste algoritmen

[!DNL Commerce] ondersteunt aangepaste ontwikkeling en extensies waarmee u alternatieve algoritmen kunt toevoegen om de prioriteit van bronnen te bepalen. Bijvoorbeeld, kunt u één prioritair algoritme hebben dat op geografie wordt gebaseerd en een andere die op uitgave van voorraad of een klantenattribuut wordt gebaseerd. Wanneer de voorraadkosten veranderen, kan uw implementatie algoritmen gemakkelijk veranderen om de laagste kosten te verzekeren.

## Voorbehouden

In plaats van onmiddellijk de hoeveelheden van de productvoorraad af te trekken of toe te voegen, houden reserveringen inventarisbedragen aan totdat orders worden verzonden of geannuleerd. Reserveringen werken volledig op de achtergrond om uw verkoopbare hoeveelheid automatisch bij te werken op voorraadniveau.

>[!NOTE]
>
>[!BADGE  PaaS slechts ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} het reservatiecapaciteit vereist de `inventory.reservations.updateSalabilityStatus` consument van de berichtrij om onophoudelijk te lopen. Gebruik de opdracht `bin/magento queue:consumers:list` om te controleren of de bewerking wordt uitgevoerd. Als de consument in de wachtrij niet wordt vermeld, start u deze: `bin/magento queue:consumers:start inventory.reservations.updateSalabilityStatus` .

### Bevoegdheid

De reserves houden de voorraden aan die bij de indiening van een bestelling op de verkoopbare hoeveelheid in mindering zijn gebracht. De reserveringen zijn op voorraadniveau, waarbij de hoeveelheden in aanmerking worden genomen totdat de bestelling wordt gefactureerd en verzonden, geannuleerd enzovoort. Bij het verzenden van de bestelling kunt u de SSA-aanbevelingen gebruiken of handmatig aftrekposten per bron invoeren. Bij verzending worden de reserveringen automatisch gewist en de hoeveelheid afgetrokken. De verkoopbare hoeveelheid wordt opnieuw berekend voor de voorraad met een bijgewerkte hoeveelheid en de eventuele in het systeem resterende bedragen.

Het volgende diagram helpt het proces van reserveringen tijdens een orde en door aan verzending bepalen.

![ Voorbehouden van orde aan levering ](assets/diagram-quantity.png){width="600" zoomable="yes"}

Een klant dient een bestelling in. [!DNL Commerce] controleert de huidige hoeveelheid die in de voorraad kan worden verkocht. Indien op het voorraadniveau voldoende voorraden beschikbaar zijn, wordt een reservering opgenomen om een tijdelijk opslagplaats voor het SKU-product (voor dat bestand) te plaatsen en wordt de verkoopbare hoeveelheid opnieuw berekend.

Nadat u de bestelling hebt gefactureerd, bepaalt u de bedragen van het product die u van uw bronnen wilt aftrekken en verzenden. De verzending wordt verwerkt en vanuit een of meer geselecteerde bronnen naar de klant verzonden. De hoeveelheden worden automatisch in mindering gebracht op de hoeveelheid van de bronvoorraad en de vastgestelde reserveringen. Voor volledige details en voorbeelden, zie [ Ongeveer de Status van de Orde en Reserveringen ](order-status.md).

## Reserveringsberekeningen

Het systeem maakt een reservering voor elk product wanneer de volgende gebeurtenissen optreden:

- Een klant of handelaar plaatst een bestelling.
- Een klant of handelaar annuleert een bestelling geheel of gedeeltelijk.
- De handelaar leidt tot een lading voor een fysiek product.
- De verkoper maakt een factuur voor een virtueel of downloadbaar product.
- De verkoper geeft een creditnota uit.

Reserveringen zijn bewerkingen met alleen de toevoeging, vergelijkbaar met een logboek met gebeurtenissen. De oorspronkelijke reservering krijgt een negatieve waarde voor het aantal toegewezen. Alle volgende voorbehouden die tijdens de verwerking van de volgorde worden gemaakt, zijn positieve waarden. Wanneer de bestelling is voltooid, is de som van alle reserveringen voor het product 0.

Voordat het systeem een reservering kan geven als reactie op een nieuwe bestelling, bepaalt het of er voldoende verkoopbare items zijn om aan de bestelling te voldoen. De volgende grootheden die in de berekening worden meegenomen:

- **StockItem hoeveelheid**. De StockItem-hoeveelheid is de geaggregeerde voorraad van alle fysieke bronnen voor het huidige verkoopkanaal. Neem bijvoorbeeld een voorbeeld waarbij de Baltimore-bron 20 eenheden van een product heeft, de Austin-bron 25 eenheden van hetzelfde product heeft en de Reno-bron 10. Wanneer al deze bronnen aan voorraad A zijn gekoppeld, is het StockItem voor dit product 55 (20 + 25 + 10). (Wanneer objecten worden verzonden, werkt de inventarisindex de beschikbare hoeveelheden bij elke bron.)

- **Uitstaand reserve**. Het systeem omvat alle initiële voorbehouden die niet zijn gecompenseerd. Dit getal is altijd negatief. Als klant A een reservering heeft voor tien objecten en klant B een reservering 5 heeft voor objecten, dan zijn er nog openstaande reserveringen voor het product in totaal -15.

Daarom kan de handelaar een inkomende orde vervullen zolang de klant minder dan 40 (55 + -15) eenheden orden.

Wanneer u een bestelling hebt verwerkt (Voltooid, Geannuleerd, Gesloten), moeten alle reserveringen in het bereik van die bestelling worden omgezet in `0` . Hierdoor worden alle verkoopbare voorraden gewist.

>[!NOTE]
>
>De achterorden (met Drempels uit-van-voorraad) en de Notitie voor Hoeveelheid onder de montages beïnvloeden ook de berekening van verkoopbare hoeveelheden, maar zij zijn buiten het werkingsgebied van dit onderwerp. Voor meer informatie over deze montages, zie [ het Vormen  [!DNL Inventory Management]](./configuration.md).

## Reserveringsobjecten

Een reservering bevat de volgende informatie:

| Parameter | Gegevenstype | Beschrijving |
| --- | --- | --- |
| `reservation_id` | Geheel | Een door het systeem gegenereerde id |
| `stock_id` | Geheel | De id van de voorraad waaraan het product is toegewezen |
| `sku` | String | De SKU van het product |
| `quantity` | Float | Het aantal objecten in dit voorbehoud |
| `metadata` | String | Het gebeurtenistype, het objecttype en de object-id voor deze reservering. Bijvoorbeeld: `{"event_type":"order_placed","object_type":"order",| "object_id":"8"}` |

{style="table-layout:auto"}

De metagegevens `event_type` kunnen de volgende waarden hebben:

- `order_placed`
- `order_canceled`
- `shipment_created`
- `creditmemo_created`
- `invoice_created`

Het objecttype voor metagegevens moet momenteel `order` zijn en de object-id moet de volgorde-id zijn.

In toekomstige versies kan het mogelijk zijn een reservering te maken wanneer een klant een artikel aan een winkelwagentje toevoegt. Elk object kan voor een vaste tijd worden gereserveerd, bijvoorbeeld 15 minuten, zodat de klant objecten kan reserveren terwijl hij doorgaat met winkelen. Wanneer dit type reservering is ingeschakeld, kunnen de metagegevens aanvullende soorten informatie bevatten.

## Levenscyclus reservering

In het volgende voorbeeld ziet u de volgorde van reserveringen die voor een eenvoudige volgorde zijn gegenereerd.

1. De klant maakt een inkooporder voor 25 eenheden product `SKU-1`. Het voorbehoud bevat de volgende informatie:

   ```text
   reservation_id = 1
   stock_id = 1
   sku = SKU-1
   quantity = -25
   event_type = order_placed
   ```

1. De klant stuurt een factuur voor 20 objecten, waardoor 5 van de bestelde eenheden worden geannuleerd.

   ```text
   reservation_id = 2
   stock_id = 1
   sku = SKU-1
   quantity = 5
   event_type = order_canceled
   ```

1. De handelaar verzendt de aangekochte 20 eenheden.

   ```text
   reservation_id = 3
   stock_id = 1
   sku = `SKU-1`
   quantity = 20
   event_type = shipment_created
   ```

De drie `quantity` -waarden lopen op tot 0 (-25 + 5 + 20). Het systeem wijzigt geen bestaande bedenkingen.

## Verwijdering van verwerkte voorbehouden

De `inventory_cleanup_reservations` -cron-taak voert SQL-query&#39;s uit om de databasetabel met reserveringen te wissen. Door gebrek, loopt het dagelijks bij middernacht, maar u kunt de tijden en de frequentie vormen. Bij de uitsnijdtaak wordt een script uitgevoerd waarmee de database wordt opgezocht naar volledige reserveringsreeksen waarin de som van de kwantitatieve waarden 0 is. Wanneer alle reserveringen voor een bepaald product die op de zelfde dag (of andere gevormde tijd) voortkwamen zijn gecompenseerd, schrapt de cron baan de reserveringen allen in één keer.

De `inventory_reservations_cleanup` cron-taak is niet hetzelfde als de `inventory.reservations.cleanup` message queue consumer. De consument schrapt asynchroon reserveringen door product SKU nadat een product is verwijderd, terwijl de kroonbaan de volledige reserveringstabel ontruimt. De consument wordt vereist wanneer u [**synchroniseert met de voorraadoptie van de Catalogus**](../configuration-reference/catalog/inventory.md) in de opslagconfiguratie toelaat. Zie [ berichtrijen ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) beheren in de _Gids van de Configuratie_.

Vaak kunnen de eerste voorbehouden die op één dag zijn gemaakt, niet op dezelfde dag worden gecompenseerd. Deze situatie kan zich voordoen wanneer een klant een bestelling plaatst vlak voordat de bouwtaak begint of de aankoop uitvoert met een methode voor offline betaling, zoals een bankoverschrijving. De gecompenseerde reserveringsreeksen blijven in de database totdat ze allemaal gecompenseerd worden. Deze praktijk interfereert niet met reserveringsberekeningen, omdat het totaal voor elke reservering 0 is.

>[!NOTE]
>
>Er zijn CLI bevelen die u kunt gebruiken om reserveringsinconsistenties (zie de [[!DNL Inventory Management]  CLI Verwijzing ](cli.md)) te ontdekken en te beheren.

### Reserveringsupdates

Wanneer de wijzigingen in bestellingen en productbedragen zijn voltooid, voert [!DNL Commerce] automatisch reserveringsvergoedingen in. U hoeft geen compensaties in te voeren via de Admin of de code om deze wachtwoorden bij te werken of te wissen. De voorbehouden worden alleen aangetast door de aangevoerde voorbehouden om een hoeveelheid vast te houden of een bedrag in de reserve vrij te maken (ter compensatie van de voorbehouden).

Zo werken ze:

- **Voorgelegde Orde** - wanneer een orde voor verscheidene producten wordt voorgelegd, gaat een reserve voor dat bedrag in. Als u bijvoorbeeld vijf rugzak bestelt van een Amerikaanse website, voert u een reservering in van `-5` voor die SKU en die voorraad. De verkoopbare hoeveelheid wordt met 5 verlaagd.

- **Geannuleerde Bestelling** - wanneer een orde (geheel of gedeeltelijk) wordt geannuleerd, gaat een compensatiereserve in om dat bedrag te ontruimen. Als u bijvoorbeeld drie backpackages annuleert, wordt een +3-reservering voor die SKU en voorraad ingevoerd en wordt de greep gewist. De verkoopbare hoeveelheid wordt met 3 verhoogd.

- **Verzonden Bestelling** - wanneer een orde (geheel of gedeeltelijk) schepen, een compensatiereserve ingaat om dat bedrag te ontruimen. Bijvoorbeeld, het verschepen van twee backpackages gaat een +2 reserve voor dat SKU en voorraad in, die de greep ontruimen. De hoeveelheid van het product wordt voor de verzending direct met 2 verlaagd. De berekende verkoopbare hoeveelheid wordt ook bijgewerkt voor het verlaagde voorraadbedrag, maar wordt niet langer beïnvloed door het voorbehoud.

![ de updates van de Voorbehoud ](assets/diagram-reservation.png){width="600" zoomable="yes"}

Alle voorbehouden moeten worden vereffend door middel van compensaties wanneer de bestellingen volledig worden uitgevoerd, producten worden geannuleerd, kredietkaarten worden uitgegeven, enzovoort. Als de compensaties geen voorbehoud maken, zouden de hoeveelheden in staat van opslag kunnen zijn (niet beschikbaar voor verkoop en nooit voor verzending).

>[!NOTE]
>
>Als u reserveringen wilt controleren, is een reeks bevel-lijn opties beschikbaar. U kunt reserveringen slechts door een bevel-lijn interface herzien. Het gebruiken van bevelen CLI kan ontwikkelaarhulp vereisen. Zie [[!DNL Inventory Management]  CLI Verwijzing ](cli.md).

Als u alle bronnen uit een product verwijdert voor een voorraad met lopende bestellingen, hebt u mogelijk een voorbehoud gemaakt.

{{$include /help/_includes/unassign-source.md}}

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
