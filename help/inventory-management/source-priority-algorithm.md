---
title: Het Source Priority Algorithm configureren
description: Leer hoe te om de bronprioriteit te vormen die voor de orde van toegewezen bronnen in uw voorraad wordt gebruikt om aanbevelingen te doen.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Het Source Priority Algorithm configureren

Aangepaste voorraden bevatten een lijst met bronnen die via je winkel kunnen worden verkocht en geleverd. Dit algoritme gebruikt de orde van toegewezen bronnen in uw voorraad om aanbevelingen te doen.

Bij uitvoering, het algoritme:

- Werkt door de gevormde orde van bronnen op het voorraadniveau die bij de bovenkant beginnen

- beveelt een hoeveelheid aan om per product te verzenden en te leveren op basis van de volgorde in de lijst, de beschikbare hoeveelheid en de bestelde hoeveelheid

- Hiermee gaat u door met de lijst totdat de order is geladen

- Hiermee slaat u uitgeschakelde bronnen over als deze in de lijst worden gevonden

Om te vormen, schik die bronnen van bovenkant tot bodem in prioriteit voor het vervullen van orden. Het Source Selection Algorithm (SSA) biedt een algoritme Priority die deze volgorde gebruikt bij het bepalen van aftrekkingen voor verzending en inventaris. Zie [&#x200B; Prioritizing Bronnen voor een Voorraad &#x200B;](stocks-prioritize-sources.md).

## De prioriteit van bronnen configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Open een bestand in de bewerkingsmodus en ga naar het _[!UICONTROL Sources]_-gebied.

1. Klik op **[!UICONTROL Assign Sources]**.

1. Selecteer in de weergave _[!UICONTROL Assign Sources]_&#x200B;het selectievakje voor de vereiste bron en klik vervolgens op **[!UICONTROL Done]**&#x200B;om een bron aan het bestand toe te wijzen.

>[!NOTE]
>
>Wanneer het gebruiken van het [&#128279;](distance-priority-algorithm.md) algoritme van de Prioriteit van de Afstand  voor het verschepen, als de routes en de gegevens niet voor de geselecteerde [&#x200B; wijze van de Berekening &#x200B;](distance-priority-algorithm.md) (het drijven, het fietsen, of het lopen) voor een lading terugkeren, blijft SSA aan het gebruiken van de Prioriteit van Source in gebreke.

![&#x200B; orde van Source na prioritering &#x200B;](assets/inventory-stock-priority-after.png)

| pictogrammen | Beschrijving |
|----------------------------------------------|----------------------------------------------------------------|
| ![&#x200B; belemmering en laat vallen het pictogram om prioriteit &#x200B;](assets/icon-drag-and-drop-action.png) te plaatsen | Gebruik deze optie om bronnen te slepen en neer te zetten op basis van prioriteit. |
| ![&#x200B; klik pictogram aan unassign een bron &#x200B;](assets/icon-delete-action.png) | De toewijzing van een bron aan een bestand opheffen. |
