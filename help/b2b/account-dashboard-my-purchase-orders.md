---
title: "[!UICONTROL My Purchase Orders]"
description: Meer informatie over inkooporders en hoe bedrijven deze kunnen gebruiken om hun aankopen te beheren.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Wanneer inkooporders [toegelaten voor een bedrijf](purchase-order-flow.md), wordt elke bestelling voor een klant die is aangemeld bij een bedrijfsgebruikersaccount automatisch gemaakt als een inkooporder (inkooporder). De gebruikers van het bedrijf met de vereiste toestemmingen kunnen tot stand brengen, uitgeven en POs schrappen die zij, samen met POs leiden die door ondergeschikte gebruikers worden gecreeerd.

![Mijn inkooporders](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Inkooporders maken een _opname_ van objectprijzen, kortingen en verzendprijzen op het moment dat de bestelling werd gemaakt. Als de prijs van een item verandert nadat de inkooporder is gemaakt, wordt de oorspronkelijke prijs gebruikt.

## Aankooporders beheren

Van de _Inkooporder weergeven_ pagina, kan de klant PO, afhankelijk van hun beheren [rolmachtigingen](account-company-roles-permissions.md).

- Klik op **[!UICONTROL View]**.
- Om om het even welke commentaren over PO te zien, klik **[!UICONTROL Comments]** tab.
- Als u een volledige ordergeschiedenis wilt weergeven, klikt u op de knop **[!UICONTROL History Log]** tab.

>[!IMPORTANT]
>
>Als een item in een inkooporder uit voorraad is of als er onvoldoende hoeveelheid beschikbaar is, treedt er een fout op wanneer de inkooporder wordt omgezet in een werkelijke order. Als backorders worden ingeschakeld, wordt de volgorde op de normale wijze verwerkt.

## Nieuwe inkooporder van bestaande kooporder

Als de klant een bestaande inkooporder heeft en nieuwe items wilt toevoegen, kunnen deze een dubbele inkooporder genereren met nieuwe producten die aan de nieuwe inkooporder zijn toegevoegd. De klant voert de volgende stappen uit:

1. Op de _Mijn inkooporder_ pagina, zoekt de klant naar de kooporder en klikt op de **[!UICONTROL View]** koppeling.

1. De klant klikt **[!UICONTROL Add Items to Shopping Cart]**.

   De pagina Winkelwagentje wordt geopend met alle vermelde items.

1. Hiermee brengt u toevoegingen of wijzigingen aan.

1. (Optioneel) Gebruikt de **[!UICONTROL Custom Reference Number]** om een intern Factuur/Inkooporderaantal aan de orde toe te voegen.

1. Volg de normale uitcheckworkflow en klik op **[!UICONTROL Place Purchase Order]**.

Als ze artikelen in hun winkelwagentje hebben wanneer ze op _[!UICONTROL Add Items to Shopping Cart]_wordt een dialoogvenster weergegeven. In dit dialoogvenster kunnen ze kiezen tussen het samenvoegen van de winkelwagentjes met de nieuwe artikelen of het vervangen van de artikelen in het winkelwagentje door de artikelen in de inkooporder.

De oorspronkelijke kooporder kan worden gesloten als deze niet meer nodig is.

## Goedkeuring van inkooporders

Voor een klant die als fiatteur op bedrijfsstructuur of toegewezen bedrijfrol wordt aangewezen, _[!UICONTROL My Purchase Orders]_op de dashboardpagina wordt de **[!UICONTROL Requires My Approval]**tab. De klant klikt dit lusje om POs te herzien die op hun goedkeuring wachten. De teller toont hoeveel orden op goedkeuring wachten.

Na klikken **[!UICONTROL View]** voor een inkooporder en het bekijken van de details, kan de fiatteur klikken op **[!UICONTROL Approve]** of **[!UICONTROL Reject]**.

### Goedkeuring/afkeuring van een lamp

Vanaf Adobe Commerce 2.4.1 kunnen fiatteurs meerdere inkooporders tegelijk goedkeuren of afwijzen.

1. Op de _[!UICONTROL My Purchase Order]_pagina, klikt u op de knop **[!UICONTROL Requires My Approval]**tab.

1. Schakel het selectievakje in voor elke inkooporder die moet worden goedgekeurd of geweigerd.

1. Klikken **[!UICONTROL Approve Selected]** of **[!UICONTROL Reject Selected]**.

Een klant kan alleen de inkooporders selecteren met een status die een handeling toestaat. Bedrijfsbeheerders kunnen bulkgoedkeuringen of afwijzingen maken voor alle actieve inkooporders in hun bedrijf.
