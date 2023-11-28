---
title: voorraadvoorraad beheren
description: Leer hoe voorraad wordt gebruikt om een virtuele, geaggregeerde inventaris van producten voor bronnen van uw verkoopkanalen te vertegenwoordigen.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Voorraad beheren

De voorraad vertegenwoordigt een virtuele, geaggregeerde inventaris van producten voor bronnen van uw verkoopkanalen (websites). Afhankelijk van uw siteconfiguratie, kan de voorraad aan één of meerdere verkoopkanalen worden toegewezen. Aan elk verkoopkanaal kan slechts één voorraad worden toegewezen en aan meerdere verkoopkanalen kan één voorraad worden toegewezen. Door de voorraad kunt u de prioritering wijzigen van bronnen die worden gebruikt terwijl orders via een verkoopkanaal komen.

U begint met een standaardvoorraad die niet kan worden verwijderd of uitgeschakeld. U kunt alleen extra verkoopkanalen aan de voorraad toevoegen. De enige toegewezen bron is Standaardbron. Deze voorraad wordt gebruikt door single-source-handelaren, integraties van derden en geïmporteerde producten.

Sales Channel vertegenwoordigen entiteiten die je voorraad verkopen. Standaard, [!DNL Commerce] biedt uw winkelwebsites als verkoopkanalen. De verkoopkanalen kunnen worden uitgebreid om extra kanalen zoals B2B klantengroepen en opslagmeningen te steunen. Elk verkoopkanaal kan aan slechts één Voorraad worden geassocieerd.

- **Ondersteuning voor Sales Channel** - Verkoopkanalen bevatten momenteel websites die niet in de handel zijn. U kunt verkoopkanalen uitbreiden om douaneopties zoals B2B klantengroepen en opslagmeningen te omvatten. Aan elk verkoopkanaal kan slechts één voorraad worden toegewezen. Eén voorraad kan aan meerdere verkoopkanalen worden toegewezen.
- **Toewijzen aan bronnen** - Aan elk bestand kunnen een of meer in- of uitgeschakeld bronnen worden toegewezen, waarbij de virtuele geaggregeerde inventaris per product wordt berekend.
- **Afhandeling van prioriteitsvolgorde** - Het uit-van-de-doos Prioriteitsalgoritme voor het Algoritme van de Selectie van de Bron gebruikt de bronlijst van de voorraad van boven aan onder wanneer het vervullen van orden.

Het volgende diagram helpt bepalen hoe een Voorraad met betrekking tot Bronnen en Sales Channel voor een handelaar van de Winkel van de Bicycle werkt.

![Diagram van bijvoorbeeld voorraden voor een winkel](assets/diagram-stock.png){width="600" zoomable="yes"}

## Voorbeelden van een bergfiets en -winkel

Alle winkels beginnen met een standaardvoorraad. Het moet blijven `Enabled` om de volgende redenen:

- Het wordt gebruikt bij het invoeren van nieuwe producten, automatisch toewijzend producten aan de standaardbron en voorraad voor directe toegang tot [!DNL Inventory Management].
- U kunt geen extra bronnen buiten de Standaardbron aan dit bestand toevoegen.
- Deze is vereist en wordt gebruikt door eenbronhandelaren, bundelproducten en gegroepeerde producten.

Voor producten met meerdere leveranciers maakt en configureert u voorraden die het best passen bij uw winkels en bestellingen. Wanneer u nieuwe voorraad aan een verkoopkanaal toewijst, wordt om het even welke reeds bestaande voorraad in dat verkoopkanaal unassigned.

Voor een installatie in meerdere opslagruimten wordt de standaardvoorraad aanvankelijk toegewezen aan de [Hoofdwebsite](../stores-purchase/stores.md#add-websites){target="_blank"} en de standaardopslag. De juiste voorraad en hoeveelheden worden weergegeven voor ingeschakelde en uitgeschakelde producten in de **[!UICONTROL Products]** rasterweergave.

![Stock beheren](assets/inventory-stock.png){width="600" zoomable="yes"}

## Knopbalk

| Knop | Beschrijving |
|--|--|
| [!UICONTROL Add New Stock] | Hiermee opent u de _[!UICONTROL New Stock]_formulier dat wordt gebruikt om een nieuw voorraadbestand in te voeren voor de toewijzing van voorraad aan verkoopkanaal. |

## Beschrijvingen van voorraadkolommen beheren

| Kolom | Beschrijving |
|--|--|
| [!UICONTROL ID] | Unieke, numerieke id die is gegenereerd voor het voorraaditem. |
| [!UICONTROL Name] | Unieke naam die de inventarisvoorraad identificeert. |
| [!UICONTROL Sales Channels] | Hiermee definieert u het bereik van de voorraad door de voorraad toe te wijzen aan specifieke websites als _verkoopkanalen_. |
| [!UICONTROL Assigned sources] | Bronnen die zijn toegewezen aan de voorraad die alle producthoeveelheden levert. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Hiermee opent u de voorraadrecord in de bewerkingsmodus. |
