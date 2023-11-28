---
title: voorraadbronnen beheren
description: Leer bronnen en hoe ze de fysieke locaties definiëren waar de productvoorraad wordt beheerd en verzonden voor bestelling, of waar services beschikbaar zijn.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Bronnen beheren

De bronnen zijn de fysieke plaatsen waar de productinventaris wordt beheerd en voor bestelling wordt verscheept, of waar de diensten beschikbaar zijn. Deze locaties kunnen opslagplaatsen, baksteen- en mortierwinkels, distributiecentra, ophaallocaties en neerslagbevrachters omvatten. U wijst inventarishoeveelheden toe aan deze bronnen, en [!DNL Commerce] Hiermee worden de totale verkoopbare producten voor uw voorraden automatisch samengevoegd. Voor grote bedrijven voegt u meerdere bronnen toe voor al uw locaties: in verschillende geografische locaties per land en continent, locaties in een stad op basis van het type inventaris, zelfs op basis van services.

U wordt aangeraden specifieke fysieke geografische locaties op te geven wanneer u een bron maakt. Dat maakt het mogelijk _Algoritme voor afstandprioriteit_ om de locatie van het verzendadres te vergelijken met de beschikbare bronlocaties om de dichtstbijzijnde bron voor de verzending te bepalen. U kunt Google Maps of offlineberekeningen gebruiken, die geocodes gebruiken. Meer informatie hierover _Algoritme voor afstandprioriteit_, zie [Algoritme voor afstandprioriteit configureren](distance-priority-algorithm.md).

Beginnen met een _Standaardbron_ dat u kunt bijwerken maar niet onbruikbaar maken. Deze bron wordt gebruikt door single-source handelaren en voor productmigratie. U hebt altijd een standaardbron nodig.

- **Locatiegegevens** - Elke bron bevat de naam, het land, het fysieke adres van de locatie en een contactpunt.
- **Bronnen inschakelen** - U kunt bronnen naar wens in- en uitschakelen. Schakel een bron alleen in als deze opdrachten en achtergronden accepteert en vervult.
- **Beschikbare voorraad** - Wijs en werk inventarishoeveelheden voor elke bron door de productpagina bij. De inventarishoeveelheden worden berekend, geleverd en gereserveerd via de bron- en voorraadtoewijzing.

In het volgende diagram ziet u de bronnen van een winkelhandelaar in fietsen die een mountainbikes verkoopt, die beschikbaar is voor voorraden en toegankelijk is voor de VS voor verzendingen.

![Voorbeeld van brondiagram](assets/diagram-sources.png){width="600" zoomable="yes"}

Alle opslag begint met een Standaard Bron die moet worden toegelaten:

- Alle nieuwe producten die in [!DNL Commerce] een bron en voorraad vereisen die automatisch worden toegewezen voor directe toegang tot [!DNL Inventory Management].
- Single-source-handelaren gebruiken de standaardbron als hun enige voorraadlocatie en verzendingen.

## Bronnen bewerken

U kunt de naam, het adres, de GPS-locatie en de contactgegevens bijwerken. De broncode is een beschermde waarde, die als unieke identiteitskaart dienst doet die de bron met uw producthoeveelheden en voorraden associeert.

Als u de standaardbron bewerkt, kunt u alle configuraties bewerken, behalve de naam en de code. Aanbevolen wordt dat single-source-handelaren informatie toevoegen die overeenkomt met hun locatie.

De _[!UICONTROL Manage Sources]_op de pagina worden alle beschikbare inventarislocaties en uitvoeringsfaciliteiten vermeld. U kunt nieuwe inventarisbronnen toevoegen en bestaande locaties bewerken.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Als u een inventarislocatie wilt toevoegen, raadpleegt u [Een nieuwe bron toevoegen](sources-add.md).

1. De inventarisbron zoeken en openen in _Bewerken_ -modus.

1. Werk de gegevens bij en sla de wijzigingen op.

   ![Bronnen beheren](assets/inventory-sources.png){width="600" zoomable="yes"}

## Knopbalk

| Knop | Beschrijving |
|--|--|
| [!UICONTROL Add New Source] | Opent de Nieuwe Bronvorm die wordt gebruikt om een nieuwe inventarisbron, een uitvoeringsfaciliteit, of een plaats in te gaan. |

## Bronkolombeschrijvingen beheren

| Kolom | Beschrijving |
|--|--|
| [!UICONTROL Code] | Een unieke alfanumerieke code die door het systeem wordt gebruikt om de inventarisbron te identificeren. |
| [!UICONTROL Name] | Een unieke naam die de inventarisbron voor Admin-gebruikers identificeert. |
| [!UICONTROL Is Enabled] | Hiermee wordt aangegeven of de inventarisbron actief is en beschikbaar voor gebruik. |
| [!UICONTROL Pickup Location] | Geeft aan of de bron actief is als een oppiklocatie voor [levering in de winkel](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Klikken **[!UICONTROL Edit]** Hiermee opent u de inventarisbronrecord in de bewerkingsmodus. |

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
