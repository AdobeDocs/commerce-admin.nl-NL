---
title: CSV-gegevensbestanden
description: In deze video ziet u de structuur die in het CSV-bestand wordt gebruikt om gegevens te importeren en exporteren.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# CSV-gegevensbestanden

De CSV-bestandsindeling (comma-separated-value) wordt gebruikt als basis voor gegevensoverdrachtsbewerkingen en wordt ondersteund door alle spreadsheet- en databasetoepassingen. De volgende bestandstypen worden ondersteund voor importeren en exporteren:

- Importeren: `CSV` en `ZIP` (een gecomprimeerd CSV-bestand)
- Exporteren: `CSV`

>[!IMPORTANT]
>
>U wordt aangeraden een programma te gebruiken dat UTF-8-codering ondersteunt, zoals Kladblok++, om CSV-bestanden te bewerken. Microsoft® Excel voegt extra tekens in de kolomkop van het CSV-bestand in, waardoor de gegevens niet weer naar Commerce kunnen worden geïmporteerd. Als u aan de Mac werkt, kunt u uw gegevens opslaan in de CSV-indeling (Windows).

CSV-bestanden hebben een specifieke structuur die moet overeenkomen met de database. Elke kolomkop komt overeen met de kenmerkcode van het veld dat wordt vertegenwoordigd door de kolom. Om ervoor te zorgen dat de kolomkoppen door Commerce kunnen worden gelezen, moet u de gegevens eerst vanuit uw winkel exporteren als een CSV-bestand. U kunt de gegevens vervolgens bewerken en opnieuw importeren in Commerce.

Als u een geëxporteerd CSV-bestand opent in een teksteditor, ziet u dat waarden worden gescheiden door komma&#39;s en dat meerdere waarden worden ingesloten door dubbele aanhalingstekens. Tijdens het importeren kunt u een aangepast scheidingsteken opgeven, hoewel een komma de standaardinstelling is.

## CSV-structuur product

Een volledige uitvoer van de productdatabase bevat informatie over elk product in de catalogus en de relaties tussen de producten. Elke record heeft een vaste selectie van kolommen die overeenkomt met de kenmerken in de catalogus, hoewel de volgorde van de kenmerken tijdens het importproces wordt genegeerd.

De eerste rij van de tabel bevat de namen van elk kenmerk, dat als kolomkoppen wordt gebruikt. In de overige rijen worden de afzonderlijke productrecords beschreven. Om het even welke rij die met een waarde in de kolom van SKU begint is het begin van een nieuw productverslag. Een enkel product kan meerdere rijen bevatten die informatie bevatten over meerdere afbeeldingen of productopties. De volgende rij die een waarde in de kolom van SKU heeft begint een nieuw product.

De categoriekolom bevat een pad voor elke categorie waaraan het product is toegewezen. Het pad bevat de hoofdcategorie, gevolgd door een slash (`/`) tussen elk niveau. Standaard wordt een komma `,` gebruikt om verschillende categoriepaden van elkaar te scheiden. (U kunt een ander scheidingsteken opgeven met de optie _[!UICONTROL Multiple value separator]_.) Bijvoorbeeld:

`Default Category/Gear,Default Category/Gear/Bags`

Om gegevens in te voeren, moet u slechts SKU en om het even welke kolommen met veranderingen omvatten. Eventuele lege kolommen worden tijdens het importproces genegeerd. Het is niet mogelijk kenmerken toe te voegen tijdens het importproces. U kunt alleen bestaande kenmerken opnemen.

Voor een gedetailleerde beschrijving van elk productattribuut, zie {de Structuur van het Dossier CSV van 0} Product CSV [&#128279;](data-attributes-product.md).

| Kolomnaam | Beschrijving |
| ----------- | ----------- |
| `_<name>` | Kolomkoppen die met een onderstrepingsteken beginnen, bevatten eigenschappen van een servicetechniek of complexe gegevens. Servicekolommen zijn geen productkenmerken. |
| `<attribute_name>` | Kolomkoppen met een kenmerkcode of veldnaam geven de gegevenskolom aan. Een kolom zou een systeemattribuut kunnen vertegenwoordigen, of één die door de opslagbeheerder werd gecreeerd. |

{style="table-layout:auto"}

## CSV-structuur van klant

Het CSV-bestand van klanten bevat klantgegevens uit de database en heeft de volgende structuur:

De eerste rij van de tabel bevat de namen van de kenmerkkolommen (die hetzelfde zijn als kenmerkcodes). Er zijn twee typen kolomnamen, zoals in de volgende tabel wordt getoond. Andere rijen bevatten kenmerkwaarden, servicegegevens en complexe gegevens. Elke rij met niet-lege waarden in de kolommen `email` en `_website` begint de beschrijving van de volgende klant. Elke rij kan klantengegevens met of zonder adresgegevens, of slechts de adresgegevens vertegenwoordigen. Als een rij alleen de adresgegevens bevat, worden waarden in de kolommen die betrekking hebben op het klantprofiel genegeerd en zijn deze mogelijk leeg.

Om meer dan één adres voor een klant toe te voegen of te vervangen, voeg een rij voor elk nieuw adres met lege klantengegevens en de nieuwe of bijgewerkte adresgegevens onder de rij van klantengegevens toe.

Voor een gedetailleerde beschrijving van elk klantenattribuut, zie &lbrace;de Structuur van het Dossier van de Klant CSV [&#128279;](data-attributes-customer.md).

| Kolomnaam | Beschrijving |
| ----------- | ----------- |
| `_<name>` | Kolomkoppen die met een onderstrepingsteken beginnen, bevatten eigenschappen van een servicetechniek of complexe gegevens. Servicekolommen zijn geen klantkenmerken. |
| `<attribute name>` | De namen van de kolommen met waarden van zowel systeem-gecreeerde attributen, als attributen die door de opslagbeheerder worden gecreeerd. |

{style="table-layout:auto"}
