---
title: voorraadvoorraad beheren
description: Leer hoe voorraad wordt gebruikt om een virtuele, geaggregeerde inventaris van producten voor bronnen van uw verkoopkanalen te vertegenwoordigen.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Voorraad beheren

De voorraad vertegenwoordigt een virtuele, geaggregeerde inventaris van producten voor bronnen van uw verkoopkanalen (websites). Afhankelijk van uw siteconfiguratie, kan de voorraad aan één of meerdere verkoopkanalen worden toegewezen. Aan elk verkoopkanaal kan slechts één voorraad worden toegewezen en aan meerdere verkoopkanalen kan één voorraad worden toegewezen. Door de voorraad kunt u de prioritering wijzigen van bronnen die worden gebruikt terwijl orders via een verkoopkanaal komen.

U begint met een standaardvoorraad die niet kan worden verwijderd of uitgeschakeld. U kunt alleen extra verkoopkanalen aan de voorraad toevoegen. De enige toegewezen bron is Default Source. Deze voorraad wordt gebruikt door single-source-handelaren, integraties van derden en geïmporteerde producten.

Sales Channel vertegenwoordigen entiteiten die je voorraad verkopen. Standaard biedt [!DNL Commerce] uw winkelwebsites als verkoopkanalen. De verkoopkanalen kunnen worden uitgebreid om extra kanalen zoals B2B klantengroepen en opslagmeningen te steunen. Elk verkoopkanaal kan aan slechts één Voorraad worden geassocieerd.

- **de Steun van de Sales Channel** - de verkoopkanalen omvatten momenteel websites uit-van-de-doos. U kunt verkoopkanalen uitbreiden om douaneopties zoals B2B klantengroepen en opslagmeningen te omvatten. Aan elk verkoopkanaal kan slechts één voorraad worden toegewezen. Eén voorraad kan aan meerdere verkoopkanalen worden toegewezen.
- **Kaart aan Bronnen** - Elk dossier kan één of meerdere toegelaten of gehandicapte toegewezen bronnen hebben, die de virtuele bijeengevoegde inventaris per product berekenen.
- **Prioritaire Volgorde 1&rbrace; - het uit-van-de-doos algoritme van de Prioriteit voor het Algoritme van de Selectie van Source gebruikt de bron van de voorraad van boven tot onder wanneer het vervullen van orden.**

Het volgende diagram helpt bepalen hoe een Voorraad met betrekking tot Bronnen en Sales Channel voor een handelaar van de Winkel van de Bicycle werkt.

![ Diagram voor bijvoorbeeld voorraden voor een opslag ](assets/diagram-stock.png){width="600" zoomable="yes"}

## Voorbeelden van een bergfiets en -winkel

Alle winkels beginnen met een standaardvoorraad. Deze moet `Enabled` blijven om de volgende redenen:

- Deze wordt gebruikt bij het importeren van nieuwe producten, waarbij producten automatisch worden toegewezen aan de standaardbron en voorraad voor directe toegang tot [!DNL Inventory Management] .
- U kunt geen extra bronnen buiten de standaard-Source aan dit bestand toevoegen.
- Deze is vereist en wordt gebruikt door eenbronhandelaren, bundelproducten en gegroepeerde producten.

Voor producten met meerdere leveranciers maakt en configureert u voorraden die het best passen bij uw winkels en bestellingen. Wanneer u nieuwe voorraad aan een verkoopkanaal toewijst, wordt om het even welke reeds bestaande voorraad in dat verkoopkanaal unassigned.

Voor een multi-opslaginstallatie, wordt de StandaardBeeld aanvankelijk toegewezen aan de [ Belangrijkste Website ](../stores-purchase/stores.md#add-websites){target="_blank"} en standaardopslag. Correcte hoeveelheden en voorraden worden weergegeven voor in- en uitgeschakeld producten in de rasterweergave van **[!UICONTROL Products]** .

![ beheer Voorraad ](assets/inventory-stock.png){width="600" zoomable="yes"}

## Knopbalk

| Knop | Beschrijving |
|--|--|
| [!UICONTROL Add New Stock] | Hiermee opent u het _[!UICONTROL New Stock]_-formulier dat wordt gebruikt voor het invoeren van een nieuw voorraad voor het toewijzen van voorraad aan verkoopkanaal. |

## Beschrijvingen van voorraadkolommen beheren

| Kolom | Beschrijving |
|--|--|
| [!UICONTROL ID] | Unieke, numerieke id die is gegenereerd voor het voorraaditem. |
| [!UICONTROL Name] | Unieke naam die de inventarisvoorraad identificeert. |
| [!UICONTROL Sales Channels] | Bepaalt het werkingsgebied van de voorraad door de voorraad aan specifieke websites als _verkoopkanalen_ toe te wijzen. |
| [!UICONTROL Assigned sources] | Bronnen die zijn toegewezen aan de voorraad die alle producthoeveelheden levert. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Opent de voorraadrecord in de bewerkingsmodus. |
