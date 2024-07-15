---
title: Klantsegmenten
description: De segmenten van de klant staan u toe om inhoud en bevorderingen aan specifieke klanten dynamisch te tonen.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Klantensegmenten

De segmenten van klanten staan u toe om inhoud en bevorderingen aan specifieke klanten dynamisch te tonen, die op diverse eigenschappen worden gebaseerd. Sommige voorbeelden zijn het adres van de klant, de ordergeschiedenis en de inhoud van het winkelwagentje. U kunt marketinginitiatieven optimaliseren op basis van doelsegmenten met winkelwagenprijsregels. U kunt ook rapporten genereren en de lijst met beoogde klanten exporteren. Omdat de informatie van het klantensegment constant wordt verfrist, kunnen de klanten van een segment worden geassocieerd en worden losgemaakt aangezien zij in uw opslag winkelen.

Om het verschil tussen [ klantengroepen ](../customers/customer-groups.md) en klantensegmenten beter te begrijpen, neem nota waar zij worden gebruikt:

|  | Klantsegment | Klantgroep |
|--- |--- |--- |
| Catalogusprijsregel |  | ✔️ |
| Winkelprijsregel | ✔️ | ✔️ |
| Tier-prijs |  | ✔️ |
| Verwante productregel | ✔️ |  |
| Dynamisch blok | ✔️ |  |
| Wisselkoersen |  | ✔️ |
| Categoriemachtigingen |  | ✔️ |
| Uitnodigingen |  | ✔️ |

{style="table-layout:auto"}

## Clientsegmentkenmerken

De het segmentattributen van klanten worden bepaald op een manier gelijkend op winkelwagentje en catalogusprijsregels. Voor een attribuut dat in een voorwaarde van het klantensegment moet worden gebruikt, moet het _[!UICONTROL Use in Customer Segment]_[ bezit ](attribute-properties.md#) aan `Yes` worden geplaatst. De de segmentvoorwaarden van de klant kunnen de volgende types van attributen omvatten:

| Kenmerk | Beschrijving |
|---|---|
| `Customer Address Fields` | U kunt elk adresveld definiëren, zoals plaats of land. Om het even welk adres in het adresboek van een klant kan deze voorwaarden voor de klant aanpassen. U kunt ook opgeven dat alleen het standaardfacturerings- of verzendadres kan worden gebruikt om overeen te komen met een klant. Adreskenmerken van de klant zijn alleen beschikbaar voor klanten die zijn aangemeld bij hun accounts. |
| `Customer Information Fields` | Er kunnen diverse klantgegevens worden gedefinieerd, zoals de klantgroep, de naam, het e-mailadres, de abonnementsstatus voor nieuwsbrieven en het saldo voor creditering van winkels. Klantgegevens zijn alleen beschikbaar voor klanten die zich bij hun accounts hebben aangemeld. |
| `Cart Fields` | De eigenschappen van winkelwagentjes kunnen worden gebaseerd op het aantal (regelobjecten of het totale aantal) of de waarde (zoals het totaal-generaal, de belasting en de cadeaukaart) van de inhoud van het winkelwagentje. |
| `Products` | U kunt verwijzen naar producten die zich momenteel in het winkelwagentje of op de verlanglijst bevinden, of die eerder zijn bekeken of besteld. U kunt ook een datumbereik instellen waarin de gebeurtenis heeft plaatsgevonden. De producten worden gedefinieerd met behulp van productkenmerken. |
| `Order Fields` | Orderkenmerken voor bestellingen uit het verleden kunnen worden gedefinieerd op basis van het factuuradres/verzendadres in de bestelling, het totale (of gemiddelde) bedrag of de hoeveelheid van de bestellingen, of het totale aantal bestellingen. U kunt ook een datumbereik instellen voor het tijdstip waarop de bewerking heeft plaatsgevonden en de status van de volgorde van de bestellingen die aan deze voorwaarden voldoen. Alleen beschikbaar voor klanten die zijn aangemeld. Voorwaarden die zijn ingesteld voor kopers die niet zijn aangemeld, werken niet meer wanneer ze zich aanmelden. |

{style="table-layout:auto"}

Zie [ klantensegmenten ](../customers/customer-segment-create.md) voor meer informatie tot stand brengen en schrappen over het bepalen van klantensegmenten.

## eBooks

- **segmentatie van de Klant** — Krijg [ eBook ](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) leren hoe te om winsten en algemene klantentevredenheid te verhogen.
- **de tactiek van de Segmentatie** - krijg [ eBook ](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html) om het richten van uw berichten en bevorderingen te verbeteren om betekenisvolle gesprekken met uw klanten tot stand te brengen.
