---
title: '[!DNL Inventory Management] CLI-verwijzing'
description: Leer over de bevelen die door de  [!DNL Inventory Management]  module worden verstrekt om inventarisgegevens en configuratiemontages te beheren.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI-verwijzing

[!DNL Inventory Management] bevat opdrachten voor het beheer van inventarisgegevens en configuratie-instellingen.

Deze opdrachten zijn:

- Controle en oplossing van inconsistenties in de reserveringen die gevolgen hebben voor de verkoopbare hoeveelheid
- Geocodes toevoegen voor het algoritme Afstandprioriteit

## Onverenigbaarheden van voorbehouden oplossen

Met reserveringen wordt een verkoopbare hoeveelheid aangehouden voor SKU&#39;s per voorraad. Wanneer u producten verzendt, toevoegt, een bestelling annuleert of terugbetaalt, worden er compensatiereserveringen ingevoerd om deze bezittingen te plaatsen of te wissen.

[!DNL Inventory Management] biedt twee opdrachten om inconsistenties in de reserveringen te controleren en op te lossen:

- [` inventariseren :reservation: lijst-inconsistenties `](#list-inconsistencies-command)
- [` voorraad :reservation: creeer-compensaties `](#create-compensations-command)

### Oorzaken van inconsistenties in het voorbehoud

[!DNL Inventory Management] genereert reserveringen voor toetsgebeurtenissen:

- Plaatsing van bestellingen (eerste reservering)
- Overlading van orders (reservering van vergoedingen)
- Terugbetalingsopdracht of creditmemo uitgeven (reservering van vergoeding)
- Opzegging van het bevel (boeking van schadevergoeding)

Voorbehoud-inconsistenties kunnen optreden wanneer:

- [!DNL Inventory Management] verliest de oorspronkelijke reservering en voert te veel reserveringsvergoedingen in (overcompensatie en leidt tot inconsistente bedragen)
- [!DNL Inventory Management] plaatst de oorspronkelijke reservering correct, maar verliest compenserende reserveringen.

U kunt reserveringen handmatig controleren en controleren in de tabel `inventory_reservation` .

De volgende configuraties en gebeurtenissen kunnen inconsistenties in de reserveringen veroorzaken:

- **Verbetering aan 2.3.x met orden niet in een definitieve staat (Voltooid, Geannuleerd, of Gesloten).** [!DNL Inventory Management] maakt compenserende reserveringen voor deze bestellingen, maar het voert niet de oorspronkelijke reservering in of heeft deze die van de verkoopbare hoeveelheid wordt afgetrokken. Het wordt aanbevolen deze opdrachten te gebruiken nadat u een upgrade hebt uitgevoerd naar Adobe Commerce of Magento Open Source v2.3.x vanuit 2.1.x of 2.2.x. Als u bestellingen in behandeling hebt, werken de opdrachten het verkoopbare aantal en de reserveringen voor verkoop en bestelling correct bij.
- **u beheert geen voorraad dan verandert later deze configuratie.** U kunt 2.3.x beginnen te gebruiken terwijl **[!UICONTROL Manage Stock]** is ingesteld op `No` in de configuratie. [!DNL Commerce] plaatst geen reserveringen bij de plaatsing van orders en verzendgebeurtenissen. Als u later de configuratie van **[!UICONTROL Manage Stock]** inschakelt en sommige bestellingen worden gemaakt, is de Salable Qty beschadigd met de reservering voor compensatie wanneer u die bestelling afhandelt en uitvoert.
- **u wijst de Beeld voor een Website toe terwijl de orden aan die website** voorleggen. De oorspronkelijke boeking vermeldt voor de oorspronkelijke voorraad en alle reserveringen voor de vergoeding worden opgenomen in de nieuwe voorraad.
- **het totaal van alle reserveringen kan niet aan `0` oplossen.** Alle reserveringen in het bereik van een bestelling in de uiteindelijke status (Voltooid, Geannuleerd, Gesloten) moeten worden omgezet in `0` , waarbij alle aanhoudingen voor de verkoopbare hoeveelheid worden gewist.

### Inconsistenties weergeven, opdracht

De opdracht `list-inconsistencies` detecteert alle inconsistenties in de reservering en geeft deze weer. Gebruik de opdrachtopties om alleen voltooide of onvolledige bestellingen of alle opdrachten te controleren.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opdrachtopties:

- `-c`, `--complete-orders` - Geeft inconsistenties voor voltooide orders. Onjuiste reserveringen kunnen nog steeds worden aangehouden voor voltooide orders.
- `-i`, `--incomplete-orders` - Geeft inconsistenties voor incomplete bestellingen (gedeeltelijk verzonden, niet verzonden). Onjuiste reserveringen kunnen te veel of onvoldoende verkoopbare hoeveelheid voor de bestellingen bevatten.
- `-b` , `--bunch-size` - Hiermee definieert u hoeveel bestellingen tegelijkertijd moeten worden geladen.
- `-r` , `--raw` - Onbewerkte uitvoer.

Reacties met `-r` return in `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` -indeling:

- Order-id geeft het bereik van de inconsistentie aan.
- SKU geeft het product aan met de inconsistentie.
- De hoeveelheid bepaalt het bedrag dat voor de reserveringscompensatie moet worden ingevoerd.
- De voorraad-id definieert de omvang van de voorraad, waarbij de reserveringen worden gebruikt om de verkoopbare hoeveelheid te berekenen.

Voorbeelden:

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Als er geen problemen worden gevonden, wordt dit bericht geretourneerd: er zijn geen inconsistenties in de volgorde gevonden.

### Vergoedingen maken, opdracht

Met de opdracht `create-compensations` maakt u compensatiereserveringen. Afhankelijk van het probleem worden nieuwe reserveringen gemaakt om een hoeveelheid te plaatsen of vrij te geven.

Als u reserveringen wilt maken, biedt u compensaties met de indeling `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` , zoals `172:bike-123:+2.000000:1` .

```bash
bin/magento inventory:reservation:create-compensations
```

Optie Opdracht:

- `-r` , `--raw` - Geeft onbewerkte uitvoer.

Als de indeling van de aanvraag onjuist is, wordt het volgende bericht weergegeven:

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Aangezien het bevel reserves creeert, toont het berichten die op de updates door SKU, orde, en voorraad wijzen.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Als de SKU voor een compensatie-item spaties bevat, plaatst u de SKU tussen aanhalingstekens.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Inconsistenties opsporen en compensaties creëren

U kunt inconsistenties detecteren en direct compensaties maken door met behulp van een pijp zowel de `list-inconsistencies` als de `create-compensations` uit te voeren. Gebruik de opdrachtoptie `-r` om de onbewerkte gegevens te genereren en naar `create-compensations` te verzenden.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Voorbeeld van reactie:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Nadat de updates voltooid zijn, voer het lijstbevel uit om te verifiëren:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

U kunt de bevelen ook leiden om inconsistenties te ontdekken en compensaties voor slechts onvolledige (`-i`) tot stand te brengen of (`-c`) te voltooien orden.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Geocodes importeren

[!DNL Inventory Management] verstrekt het [ Prioriteitsalgoritme van de Afstand ](distance-priority-algorithm.md), dat de hulp de beste optie voor het verschepen van een volledige of gedeeltelijke orde bepaalt. Het algoritme gebruikt GPS-informatie of geocodes om de afstand tussen de bron (een pakhuis of andere fysieke locatie) van elk item in een bestelling en het verzendadres te berekenen. Op basis van die resultaten raadt het algoritme aan welke bron moet worden gebruikt om elk item in de volgorde te verzenden.

De handelaar selecteert de leverancier van de GPS- of geocodegegevens die nodig zijn om afstanden te berekenen:

- **MAP van Google** gebruikt [ de Diensten van het Platform van de Kaarten van Google ](https://mapsplatform.google.com/) om de afstand en de tijd tussen het verschepende bestemmingsadres en bronplaatsen te berekenen. Voor deze optie is een factureringsplan voor Google vereist en mogelijk worden kosten in rekening gebracht via Google.

- **Offline berekening** berekent de afstand gebruikend gegevens die van [ geonames.org ](https://www.geonames.org/) worden gedownload en in Commerce met een bevel worden ingevoerd. Deze optie is gratis.

geocodes importeren voor offlineberekening:

Ga het volgende bevel met een spatie-gescheiden lijst van [ ISO-3166 alpha2 landcodes ](https://www.geonames.org/countries/) in:

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Bijvoorbeeld:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Het systeem downloadt en importeert de geocodes gegevens naar uw database en geeft vervolgens het bericht `Importing <country code>: OK` weer.
