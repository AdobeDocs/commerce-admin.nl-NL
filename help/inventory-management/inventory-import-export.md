---
title: Invoer- en uitvoervoorraad
description: Gebruik de inheemse invoer en de uitvoereigenschappen met uitgebreide  [!DNL Inventory Management]  opties om bronnen en hoeveelheden door SKU bij te werken.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Invoer- en uitvoervoorraad

Voor catalogi met veel producten gebruikt u de native import- en exportfuncties met uitgebreide [!DNL Inventory Management] -opties om bronnen en hoeveelheden per SKU bij te werken. Met deze opties kunt u nieuwe bronnen toevoegen en inventarishoeveelheden bijwerken voor alle bronnen of een specifieke bron. U kunt bijvoorbeeld producten exporteren voor een bron in Duitsland zonder dat dit van invloed is op de productinformatie voor bronnen in Frankrijk, Engeland of de VS.

- [!DNL Commerce] wijst de Standaard Source automatisch toe aan uw producten wanneer u een upgrade uitvoert van [!DNL Commerce] of nieuwe producten importeert. Als u producten importeert waaraan een aangepaste bron is toegewezen, wordt de standaard-Source nog steeds toegevoegd met een hoeveelheid van 0. Gebruik deze importinstructies om bronnen en hoeveelheden bij te werken.

- Single-source-handelaren gebruiken import om alleen producthoeveelheden bij te werken. Alle bestaande en toegevoegde producten worden toegewezen aan Standaard Source.

- Multisource-handelaren gebruiken import om meerdere bronnen en hoeveelheden per rij per SKU toe te voegen.

Als u updates wilt importeren, exporteert u eerst een CSV-bestand voor een bepaalde of alle bronnen. Bewerk het CSV-bestand en voeg een rij per SKU toe voor elke bron en hoeveelheid. U hebt de code van de bron nodig wanneer u een bron toevoegt en hoeveelheden voorraad toevoegt. U kunt geen voorraden toevoegen of bijwerken met functies voor importeren en exporteren.

## CSV-bestandsinhoud

Het export-import bestand bevat de volgende informatie, afhankelijk van de bron:

- `source_code` - De code voor bronnen in [!DNL Commerce] . Er is een rij voor elke bron en SKU.
- `sku` - De SKU voor het product in [!DNL Commerce]. De SKU moet overeenkomen met een product in uw winkel om [!DNL Inventory Management] -gegevens correct bij te werken.
- `status` - 0 voor Uit voorraad. 1 voor In voorraad. Deze waarde moet 1 zijn om voorraad van deze bron aan te schaffen.
- `quantity` - De totale hoeveelheid voorraad beschikbaar voor deze SKU en bron.

Gebruik een CSV-bestand om snel meerdere producten en toegewezen bronnen bij te werken en eventuele onnauwkeurigheden in de voorraadadministratie te corrigeren in plaats van één voor één via de toepassingsinterface. Exporteer voor een basisbestand eerst en werk het bestand zo nodig bij.

![&#x200B; Csv- dossier van het Voorbeeld voor de invoer - de gegevens van de de uitvoervoorraad &#x200B;](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Productgegevens exporteren voor alle bronnen

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Kies `Stock Sources` bij **[!UICONTROL Entity Type]** .

   De uitvoer haalt slechts gegevens voor producten met een SKU uit.

1. Klik op **[!UICONTROL Continue]**.

   Het bestand wordt gegenereerd en gedownload om te openen en te bewerken.

Importeer het bestand weer in [!DNL Commerce] nadat u de voorraad en de productgegevens hebt bijgewerkt.

![&#x200B; de voorraadbronnen van de Uitvoer voor productgegevens en bronnen &#x200B;](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Productgegevens exporteren voor een specifieke bron

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Kies `Stock Sources` bij **[!UICONTROL Entity Type]** .

   De uitvoer haalt slechts gegevens voor producten met een SKU uit.

1. Gebruik **[!UICONTROL Entity Attributes]** om de geëxporteerde producten voor een bepaalde bron te filteren.

   Voer bij `source_code` de code voor de bron in het filterveld in.

1. Klik op **[!UICONTROL Continue]**.

   Het bestand wordt gegenereerd en gedownload om te openen en te bewerken.

Importeer het bestand weer in [!DNL Commerce] nadat u de voorraad en de productgegevens hebt bijgewerkt.

## Productgegevens importeren

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Kies `Stock Sources` bij **[!UICONTROL Entity Type]** .

   De uitvoer haalt slechts gegevens voor producten met een SKU uit.

1. Selecteer configuraties voor de **[!UICONTROL Import Behavior]** .

1. Selecteer het CSV-bestand dat u wilt importeren.

1. Klik op **[!UICONTROL Check Data]** en voltooi het importeren.

![&#x200B; de productgegevens en bronnen van de Invoer &#x200B;](assets/inventory-import-sources.png){width="600" zoomable="yes"}
