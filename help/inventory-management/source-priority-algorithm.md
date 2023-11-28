---
title: Het algoritme voor bronprioriteit configureren
description: Leer hoe te om de bronprioriteit te vormen die voor de orde van toegewezen bronnen in uw voorraad wordt gebruikt om aanbevelingen te doen.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Het algoritme voor bronprioriteit configureren

Aangepaste voorraden bevatten een lijst met bronnen die via je winkel kunnen worden verkocht en geleverd. Dit algoritme gebruikt de orde van toegewezen bronnen in uw voorraad om aanbevelingen te doen.

Bij uitvoering, het algoritme:

- Werkt door de gevormde orde van bronnen op het voorraadniveau die bij de bovenkant beginnen

- beveelt een hoeveelheid aan om per product te verzenden en te leveren op basis van de volgorde in de lijst, de beschikbare hoeveelheid en de bestelde hoeveelheid

- Hiermee gaat u door met de lijst totdat de order is geladen

- Hiermee slaat u uitgeschakelde bronnen over als deze in de lijst worden gevonden

Om te vormen, schik die bronnen van bovenkant tot bodem in prioriteit voor het vervullen van orden. Het algoritme van de Selectie Bron (SSA) verstrekt een algoritme Prioriteit gebruikend deze orde wanneer het bepalen van verzending en inventarisaftrek. Zie [Prioritaire bronnen voor een bestand](stocks-prioritize-sources.md).

## De prioriteit van bronnen configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Een bestand openen in de bewerkingsmodus en naar de _[!UICONTROL Sources]_gebied.

1. Klik op **[!UICONTROL Assign Sources]**.

1. In de _[!UICONTROL Assign Sources]_de mening, selecteert checkbox voor de vereiste bron, en klikt dan **[!UICONTROL Done]**om een bron aan het bestand toe te wijzen.

>[!NOTE]
>
>Wanneer u de opdracht [Prioriteit afstand](distance-priority-algorithm.md) algoritme voor verzending als routes en gegevens niet worden geretourneerd voor de geselecteerde [Rekenmodus](distance-priority-algorithm.md) (het besturen, het fietsen, of het lopen) voor een lading, blijft SSA aan het gebruiken van de Prioriteit Bron in gebreke.

![Bronvolgorde na prioritering](assets/inventory-stock-priority-after.png)

| pictogrammen | Beschrijving |
|----------------------------------------------|----------------------------------------------------------------|
| ![het pictogram slepen en neerzetten om prioriteit in te stellen](assets/icon-drag-and-drop-action.png) | Gebruik deze optie om bronnen te slepen en neer te zetten op basis van prioriteit. |
| ![Klik op het pictogram om de toewijzing van een bron ongedaan te maken](assets/icon-delete-action.png) | De toewijzing van een bron aan een bestand opheffen. |
