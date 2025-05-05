---
title: Prioriteit geven aan inventarisbronnen voor een bestand
description: Leer hoe u prioritair bronnen van boven naar beneden rangschikt, die worden gebruikt voor het bepalen van verzendingen en voorraadaftrekkingen.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Prioriteit geven aan bronnen voor een bestand

Na het toevoegen van [ bronnen ](sources-manage.md) aan de [ voorraad ](stocks-manage.md), rangschik die bronnen van boven tot onder in prioriteit voor het vervullen van orden. Het Source Selection Algorithm (SSA) biedt een algoritme Priority die deze volgorde gebruikt bij het bepalen van aftrekkingen voor verzending en inventaris.

De bronprioriteit voor voorraden heeft geen invloed op toegewezen bronnen bij het bewerken van productinventarissen.

In dit voorbeeld heeft het Britse Stock bronnen toegewezen die zijn toegewezen aan een winkel en twee opslagplaatsen in Londen en een pakhuis in Berlijn.

![ orde van Source alvorens voorrang te geven ](assets/inventory-priority-before.png){width="350" zoomable="yes"}

De handelaar geeft er de voorkeur aan dat de overbrengingen voorrang krijgen op het grotere Berlijnse pakhuis, het Londense entrepot, de overlooplocatie Londen en ten slotte de winkel in Londen. Om de volgorde te wijzigen, worden items gesleept en in de gewenste volgorde neergezet.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Open de voorraad op _geeft_ wijze uit.

1. Vouw indien nodig de tab _[!UICONTROL Sources]_&#x200B;uit.

1. Het pictogram van de Soort van het gebruik ![&#128279;](assets/icon-sort.png) om de bronnen in een prioriteit van bovenkant (eerst) aan bodem (laatste) te slepen en te laten vallen.

   Deze bestelling is belangrijk bij verzendopdrachten. SSA beveelt aan dat zendingen worden uitgevoerd op basis van de volgorde van bronnen

1. Klik op **[!UICONTROL Save & Continue]** om de wijzigingen op te slaan.

![ orde van Source na prioritering ](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
