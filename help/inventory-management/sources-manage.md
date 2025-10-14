---
title: voorraadbronnen beheren
description: Leer bronnen en hoe ze de fysieke locaties definiëren waar de productvoorraad wordt beheerd en verzonden voor bestelling, of waar services beschikbaar zijn.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Bronnen beheren

De bronnen zijn de fysieke plaatsen waar de productinventaris wordt beheerd en voor bestelling wordt verscheept, of waar de diensten beschikbaar zijn. Deze locaties kunnen opslagplaatsen, baksteen- en mortierwinkels, distributiecentra, ophaallocaties en neerslagbevrachters omvatten. U wijst voorraadhoeveelheden toe aan deze bronnen, en [!DNL Commerce] voegt automatisch de totale verkoopbare producten voor uw voorraden samen. Voor grote bedrijven voegt u meerdere bronnen toe voor al uw locaties: in verschillende geografische locaties per land en continent, locaties in een stad op basis van het type inventaris, zelfs op basis van services.

U wordt aangeraden specifieke fysieke geografische locaties op te geven wanneer u een bron maakt. Dat staat het _Prioritaire Algoritme van de Afstand_ toe om de plaats van het verschepende bestemmingsadres met de beschikbare bronplaatsen te vergelijken om de dichtstbijzijnde bron te bepalen om verzendingen te vervullen. U kunt Google Maps of offlineberekeningen gebruiken, die geocodes gebruiken. Voor meer informatie over dit _Prioritair Algorithm van de Afstand_, zie [&#x200B; het Prioritaire Algoritme van de Afstand &#x200B;](distance-priority-algorithm.md) vormen.

Begin met a _Standaard Source_ dat u kunt bijwerken maar niet onbruikbaar maken. Deze bron wordt gebruikt door single-source handelaren en voor productmigratie. U hebt altijd een standaardbron nodig.

- **Informatie van de Plaats** - Elke bron omvat de naam, het land, het fysieke adres van de plaats, en een punt van contact.
- **toelatend Middelen** - u kunt bronnen toelaten en onbruikbaar maken zoals nodig. Schakel een bron alleen in als deze opdrachten en achtergronden accepteert en vervult.
- **Beschikbare Inventaris** - wijs en werk inventarishoeveelheden voor elke bron door de productpagina toe. De inventarishoeveelheden worden berekend, geleverd en gereserveerd via de bron- en voorraadtoewijzing.

In het volgende diagram ziet u de bronnen van een winkelhandelaar in fietsen die een mountainbikes verkoopt, die beschikbaar is voor voorraden en toegankelijk is voor de VS voor verzendingen.

![&#x200B; Bronsdiagram van het Voorbeeld &#x200B;](assets/diagram-sources.png){width="600" zoomable="yes"}

Alle winkels beginnen met een standaard Source die ingeschakeld moet blijven:

- Voor alle nieuwe producten die in [!DNL Commerce] worden geïmporteerd, is een bron en een voorraad vereist die automatisch worden toegewezen voor directe toegang tot [!DNL Inventory Management] .
- Single-source-handelaren gebruiken de Default Source als enig punt voor de inventarislocatie en -verzending.

## Bronnen bewerken

U kunt de naam, het adres, de GPS-locatie en de contactgegevens bijwerken. De broncode is een beschermde waarde, die als unieke identiteitskaart dienst doet die de bron met uw producthoeveelheden en voorraden associeert.

Als u de standaard Source bewerkt, kunt u alle configuraties bewerken, behalve de naam en de code. Aanbevolen wordt dat single-source-handelaren informatie toevoegen die overeenkomt met hun locatie.

De pagina _[!UICONTROL Manage Sources]_&#x200B;bevat een lijst met alle beschikbare inventarislocaties en uitvoeringsfaciliteiten. U kunt nieuwe inventarisbronnen toevoegen en bestaande locaties bewerken.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Om een inventarisplaats toe te voegen, zie [&#x200B; Toevoegend een Nieuwe Source &#x200B;](sources-add.md).

1. Vind de inventarisbron en open het op _geeft_ wijze uit.

1. Werk de gegevens bij en sla de wijzigingen op.

   ![&#x200B; beheert Bronnen &#x200B;](assets/inventory-sources.png){width="600" zoomable="yes"}

## Knopbalk

| Knop | Beschrijving |
|--|--|
| [!UICONTROL Add New Source] | Hiermee opent u het nieuwe Source-formulier dat wordt gebruikt om een nieuwe inventarisbron, uitvoeringsfaciliteit of locatie in te voeren. |

## Bronkolombeschrijvingen beheren

| Kolom | Beschrijving |
|--|--|
| [!UICONTROL Code] | Een unieke alfanumerieke code die door het systeem wordt gebruikt om de inventarisbron te identificeren. |
| [!UICONTROL Name] | Een unieke naam die de inventarisbron voor Admin-gebruikers identificeert. |
| [!UICONTROL Is Enabled] | Hiermee wordt aangegeven of de inventarisbron actief is en beschikbaar voor gebruik. |
| [!UICONTROL Pickup Location] | Wijst erop als de bron actief als bestelwagenplaats voor [&#x200B; in-opslaglevering &#x200B;](../stores-purchase/shipping-in-store-delivery.md) is. |
| [!UICONTROL Action] | Klik op **[!UICONTROL Edit]** om de inventarisbronrecord te openen in de bewerkingsmodus. |

## Andere kolommen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Latitude] | Hiermee geeft u de breedtecoördinaat van de inventarisbron voor GPS op. Voer de waarde in als een getal, voorafgegaan door een plusteken of minteken. Het gradensymbool en de letters zijn niet toegestaan. Bijvoorbeeld: `32.7555` |
| [!UICONTROL State/Province] | De staat of provincie waar de bron zich bevindt. |
| [!UICONTROL Postcode] | De postcode van de bron. |
| [!UICONTROL Email] | De e-mail van de primaire contactpersoon. |
| [!UICONTROL Longitude] | Hiermee geeft u de lengtecoördinaat van de inventarisbron voor GPS op. Voer de waarde in als een getal, voorafgegaan door een plusteken of minteken. Het gradensymbool en de letters zijn niet toegestaan. Bijvoorbeeld: Longitude -97.3308 |
| [!UICONTROL City] | De stad waar de bron zich bevindt. |
| [!UICONTROL Phone] | Het telefoonnummer van de primaire contactpersoon. |
| [!UICONTROL Country] | Het land waar de bron zich bevindt. |
| [!UICONTROL Street] | Het adres van de bron. |
| [!UICONTROL Fax] | De netnummer en het faxnummer van de primaire contactpersoon. |
