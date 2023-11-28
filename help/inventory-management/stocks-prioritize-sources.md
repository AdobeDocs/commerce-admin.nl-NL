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

Na toevoegen [bronnen](sources-manage.md) aan de [voorraad](stocks-manage.md)rangschikt u deze bronnen in de eerste plaats van boven naar beneden om aan orders te voldoen. Het algoritme van de Selectie Bron (SSA) verstrekt een algoritme Prioriteit gebruikend deze orde wanneer het bepalen van verzending en inventarisaftrek.

De bronprioriteit voor voorraden heeft geen invloed op toegewezen bronnen bij het bewerken van productinventarissen.

In dit voorbeeld heeft het Britse Stock bronnen toegewezen die zijn toegewezen aan een winkel en twee opslagplaatsen in Londen en een pakhuis in Berlijn.

![Bronvolgorde vóór prioritering](assets/inventory-priority-before.png){width="350" zoomable="yes"}

De handelaar geeft er de voorkeur aan dat de overbrengingen voorrang krijgen op het grotere Berlijnse pakhuis, het Londense entrepot, de overlooplocatie Londen en ten slotte de winkel in Londen. Om de volgorde te wijzigen, worden items gesleept en in de gewenste volgorde neergezet.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. De voorraad openen in het dialoogvenster _Bewerken_ -modus.

1. Breid uit _[!UICONTROL Sources]_indien nodig.

1. Gebruiken ![Pictogram Sorteren](assets/icon-sort.png) om de bronnen naar een prioriteit van boven (eerste) naar onder (laatste) te slepen.

   Deze bestelling is belangrijk bij verzendopdrachten. SSA beveelt aan dat zendingen worden uitgevoerd op basis van de volgorde van bronnen

1. Klikken **[!UICONTROL Save & Continue]** om de wijzigingen op te slaan

![Bronvolgorde na prioritering](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
