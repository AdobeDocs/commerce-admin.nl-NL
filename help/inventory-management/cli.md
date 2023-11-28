---
title: '''[!DNL Inventory Management] CLI-verwijzing"'
description: Meer informatie over de opdrachten van de [!DNL Inventory Management] -module voor het beheren van inventarisgegevens en configuratie-instellingen.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI-verwijzing

[!DNL Inventory Management] verstrekt bevelen om inventarisgegevens en configuratiemontages te beheren.

Deze opdrachten zijn:

- Controle en oplossing van inconsistenties in de reserveringen die gevolgen hebben voor de verkoopbare hoeveelheid
- Geocodes toevoegen voor het algoritme Afstandprioriteit

## Onverenigbaarheden van voorbehouden oplossen

Met reserveringen wordt een verkoopbare hoeveelheid aangehouden voor SKU&#39;s per voorraad. Wanneer u producten verzendt, toevoegt, een bestelling annuleert of terugbetaalt, worden er compensatiereserveringen ingevoerd om deze bezittingen te plaatsen of te wissen.

[!DNL Inventory Management] verstrekt twee bevelen om reserveringsinconsistenties te controleren en op te lossen:

- [Verhaal:reservation:list-inconsistenties&quot;](#list-inconsistencies-command)
- [Verhaal:reservation:creëren van compensaties&quot;](#create-compensations-command)

### Oorzaken van inconsistenties in het voorbehoud

[!DNL Inventory Management] genereert reserveringen voor toetsgebeurtenissen:

- Plaatsing van bestellingen (eerste reservering)
- Overlading van orders (reservering van vergoedingen)
- Terugbetalingsopdracht of creditmemo uitgeven (reservering van vergoeding)
- Opzegging van het bevel (boeking van schadevergoeding)

Voorbehoud-inconsistenties kunnen optreden wanneer:

- [!DNL Inventory Management] De oorspronkelijke reservering verliest en voert te veel reserveringstoeslagen in (overcompensatie en onsamenhangende bedragen)
- [!DNL Inventory Management] het oorspronkelijke voorbehoud correct wordt geplaatst, maar er worden geen compenserende voorbehouden gemaakt.

U kunt reserveringen handmatig bekijken en controleren in het dialoogvenster `inventory_reservation` tabel.

De volgende configuraties en gebeurtenissen kunnen inconsistenties in de reserveringen veroorzaken:

- **Voer een upgrade uit naar 2.3.x met bestellingen die zich niet in de uiteindelijke status bevinden (Voltooid, Geannuleerd of Gesloten).** [!DNL Inventory Management] tot compenserende reserveringen voor deze bestellingen leidt, maar de bestelling voert niet de oorspronkelijke boeking in die op de verkoopbare hoeveelheid in mindering wordt gebracht. Het wordt aanbevolen deze opdrachten te gebruiken nadat u een upgrade hebt uitgevoerd naar Adobe Commerce of Magento Open Source v2.3.x vanuit 2.1.x of 2.2.x. Als u bestellingen in behandeling hebt, werken de opdrachten het verkoopbare aantal en de reserveringen voor verkoop en bestelling correct bij.
- **U beheert de voorraad niet en wijzigt deze configuratie later niet.** U kunt 2.3.x beginnen te gebruiken met **[!UICONTROL Manage Stock]** instellen op `No` in de configuratie. [!DNL Commerce] maakt geen voorbehoud bij plaatsen van orders en verzendingen. Als u later **[!UICONTROL Manage Stock]** configuratie en sommige orden worden gecreeerd, zou de Salable Qty met compensatiereserve worden bedorven wanneer u behandelt en die orde vervult.
- **U wijst de voorraad voor een website toe terwijl bestellingen worden verzonden naar die website**. De oorspronkelijke boeking vermeldt voor de oorspronkelijke voorraad en alle reserveringen voor de vergoeding worden opgenomen in de nieuwe voorraad.
- **Het totaal van alle voorbehouden kan niet worden opgelost voor `0`.** Alle voorbehouden in het kader van een bestelling in de definitieve staat (Voltooid, Geannuleerd, Gesloten) moeten worden opgelost om `0`, waarbij alle verkochte hoeveelheden worden verruimd.

### Inconsistenties weergeven, opdracht

De `list-inconsistencies` alle inconsistenties in de reservering worden gedetecteerd en vermeld. Gebruik de opdrachtopties om alleen voltooide of onvolledige bestellingen of alle opdrachten te controleren.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opdrachtopties:

- `-c`, `--complete-orders` - Geeft inconsistenties voor voltooide orders. Onjuiste reserveringen kunnen nog steeds worden aangehouden voor voltooide orders.
- `-i`, `--incomplete-orders` - Geeft inconsistenties voor incomplete orders (gedeeltelijk verzonden, niet verzonden). Onjuiste reserveringen kunnen te veel of onvoldoende verkoopbare hoeveelheid voor de bestellingen bevatten.
- `-b`, `--bunch-size` - Hiermee definieert u het aantal orders dat in één keer moet worden geladen.
- `-r`, `--raw` - Onbewerkte uitvoer.

Reacties met `-r` return in `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` indeling:

- Order-id geeft het bereik van de inconsistentie aan.
- SKU geeft het product aan met de inconsistentie.
- De hoeveelheid bepaalt het bedrag dat voor de reserveringscompensatie moet worden ingevoerd.
- De voorraad-id definieert de omvang van de voorraad, waarbij de reserveringen worden gebruikt om de verkoopbare hoeveelheid te berekenen.

Voorbeelden:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Als er geen problemen worden gevonden, wordt dit bericht geretourneerd: er zijn geen inconsistenties in de volgorde gevonden.

### Vergoedingen maken, opdracht

De `create-compensations` bevel leidt tot compensatiebedenkingen. Afhankelijk van het probleem worden nieuwe reserveringen gemaakt om een hoeveelheid te plaatsen of vrij te geven.

Om reserveringen te creëren, verstrek compensaties gebruikend het formaat `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` zoals `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Optie Opdracht:

- `-r`, `--raw` - Retourneert onbewerkte uitvoer.

Als de indeling van de aanvraag onjuist is, wordt het volgende bericht weergegeven:

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Aangezien het bevel reserves creeert, toont het berichten die op de updates door SKU, orde, en voorraad wijzen.

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Als de SKU voor een compensatie-item spaties bevat, plaatst u de SKU tussen aanhalingstekens.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Inconsistenties opsporen en compensaties creëren

U kunt inconsistenties detecteren en onmiddellijk compensaties maken door een pijp te gebruiken om beide opties uit te voeren `list-inconsistencies` en `create-compensations`. Gebruik de `-r` opdrachtoptie voor het genereren en verzenden van de onbewerkte gegevens naar `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Voorbeeld van reactie:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Nadat de updates voltooid zijn, voer het lijstbevel uit om te verifiëren:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

U kunt de opdrachten ook gebruiken om inconsistenties op te sporen en om alleen onvolledige compensaties te maken (`-i`) of complete (`-c`) bestellingen.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Geocodes importeren

[!DNL Inventory Management] verstrekt [algoritme voor afstandprioriteit](distance-priority-algorithm.md), waarmee u de beste optie kunt bepalen voor het verzenden van een volledige of gedeeltelijke bestelling. Het algoritme gebruikt GPS-informatie of geocodes om de afstand tussen de bron (een pakhuis of andere fysieke locatie) van elk item in een bestelling en het verzendadres te berekenen. Op basis van die resultaten raadt het algoritme aan welke bron moet worden gebruikt om elk item in de volgorde te verzenden.

De handelaar selecteert de leverancier van de GPS- of geocodegegevens die nodig zijn om afstanden te berekenen:

- **GOOGLE MAP** gebruik [Google Maps-platform](https://mapsplatform.google.com/) services om de afstand en tijd tussen het verzendadres en de bronlocatie te berekenen. Voor deze optie is een factureringsplan voor Google vereist en mogelijk worden kosten in rekening gebracht via Google.

- **Offlineberekening** berekent de afstand met behulp van gegevens die zijn gedownload van [geonames.org](https://www.geonames.org/) en geïmporteerd in de handel met een opdracht. Deze optie is gratis.

geocodes importeren voor offlineberekening:

Voer de volgende opdracht in met een door spaties gescheiden lijst van [ISO-3166 alpha2-landcodes](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Bijvoorbeeld:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Het systeem downloadt en importeert de geocodes gegevens naar uw database en geeft vervolgens het bericht weer  `Importing <country code>: OK`.
