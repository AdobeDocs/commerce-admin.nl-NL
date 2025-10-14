---
title: '[!UICONTROL My Purchase Orders]'
description: Meer informatie over inkooporders en hoe bedrijven deze kunnen gebruiken om hun aankopen te beheren.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Wanneer de kooporders [&#x200B; voor een bedrijf &#x200B;](purchase-order-flow.md) worden toegelaten, wordt om het even welke orde voor een klant die in een rekening van de bedrijfgebruiker wordt ondertekend automatisch gecreeerd als kooporder (PO). De gebruikers van het bedrijf met de vereiste toestemmingen kunnen tot stand brengen, uitgeven en POs schrappen die zij, samen met POs leiden die door ondergeschikte gebruikers worden gecreeerd.

![&#x200B; Mijn orden van de Aankoop &#x200B;](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>De Orden van de aankoop leiden a _momentopname_ van puntprijzen, kortingen, en verschepende prijzen op het tijdstip dat de orde werd gecreeerd. Als de prijs van een item verandert nadat de inkooporder is gemaakt, wordt de oorspronkelijke prijs gebruikt.

## Aankooporders beheren

Van de _pagina van de Inkooporder van de Mening_, kan de klant PO, afhankelijk van hun [&#x200B; roltoestemmingen &#x200B;](account-company-roles-permissions.md) beheren.

- Klik op **[!UICONTROL View]** om de inkooporder weer te geven.
- Als u opmerkingen over de inkooporder wilt zien, klikt u op de tab **[!UICONTROL Comments]** .
- Klik op het tabblad **[!UICONTROL History Log]** om de geschiedenis van de volledige volgorde weer te geven.

>[!IMPORTANT]
>
>Als een item in een inkooporder uit voorraad is of als er onvoldoende hoeveelheid beschikbaar is, treedt er een fout op wanneer de inkooporder wordt omgezet in een werkelijke order. Als backorders worden ingeschakeld, wordt de volgorde op de normale wijze verwerkt.

## Nieuwe inkooporder van bestaande kooporder

Als de klant een bestaande inkooporder heeft en nieuwe items wilt toevoegen, kunnen deze een dubbele inkooporder genereren met nieuwe producten die aan de nieuwe inkooporder zijn toegevoegd. De klant voert de volgende stappen uit:

1. Op de _Mijn pagina van de Inkooporder_, de klantenplaats van de aankooporde en klikt de **[!UICONTROL View]** verbinding.

1. De klant klikt op **[!UICONTROL Add Items to Shopping Cart]** .

   De pagina Winkelwagentje wordt geopend met alle vermelde items.

1. Hiermee brengt u toevoegingen of wijzigingen aan.

1. (Optioneel) Hiermee wordt de **[!UICONTROL Custom Reference Number]** gebruikt om een intern Factuur-/inkoopordernummer aan de bestelling toe te voegen.

1. Volg de normale uitcheckworkflow en klik op **[!UICONTROL Place Purchase Order]** .

Als ze artikelen in hun winkelwagentje hebben wanneer ze op _[!UICONTROL Add Items to Shopping Cart]_&#x200B;klikken, wordt er een dialoogvenster weergegeven. In dit dialoogvenster kunnen ze kiezen tussen het samenvoegen van de winkelwagentjes met de nieuwe artikelen of het vervangen van de artikelen in het winkelwagentje door de artikelen in de inkooporder.

De oorspronkelijke kooporder kan worden gesloten als deze niet meer nodig is.

## Goedkeuring van inkooporders

Voor een klant die is aangewezen als fiatteur op basis van de bedrijfsstructuur of de toegewezen bedrijfsrol, wordt op de _[!UICONTROL My Purchase Orders]_-dashboardpagina het tabblad **[!UICONTROL Requires My Approval]**&#x200B;weergegeven. De klant klikt dit lusje om POs te herzien die op hun goedkeuring wachten. De teller toont hoeveel orden op goedkeuring wachten.

Nadat u op **[!UICONTROL View]** voor een inkooporder hebt geklikt en de details hebt bekeken, kan de fiatteur op **[!UICONTROL Approve]** of **[!UICONTROL Reject]** klikken.

### Goedkeuring/afkeuring van een lamp

Vanaf Adobe Commerce 2.4.1 kunnen fiatteurs meerdere inkooporders tegelijk goedkeuren of afwijzen.

1. Klik op de pagina _[!UICONTROL My Purchase Order]_&#x200B;op de tab **[!UICONTROL Requires My Approval]**.

1. Schakel het selectievakje in voor elke inkooporder die moet worden goedgekeurd of geweigerd.

1. Klik op **[!UICONTROL Approve Selected]** of **[!UICONTROL Reject Selected]** .

Een klant kan alleen de inkooporders selecteren met een status die een handeling toestaat. Bedrijfsbeheerders kunnen bulkgoedkeuringen of afwijzingen maken voor alle actieve inkooporders in hun bedrijf.
