---
title: Herstellingen toestaan
description: Leer hoe u mogelijkheden voor het opnieuw ordenen van uw klanten kunt bieden.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Herstellingen toestaan

Wanneer toegelaten, kan reorders direct van de klantenrekening of van de originele orde in _Admin_ worden gemaakt. Herstellingen zijn standaard ingeschakeld.

![&#x200B; Klante reorder verbinding in Admin &#x200B;](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Criteria voor het inschakelen van de volgorde van een bestelling

- De _staat Reorder_ configuratieoptie toe moet worden toegelaten.

- Als de volgorde in de status `Hold` of `Payment Review` staat, is de optie voor opnieuw ordenen uitgeschakeld.

- Als een van de items in de volgorde niet beschikbaar, uit voorraad of uitgeschakeld is, is de optie voor opnieuw ordenen uitgeschakeld in de winkel.

- Een _Admin_ kan reorder zelfs als om het even welke punten uit voorraad of onbruikbaar gemaakt zijn.

## Configureren om klantherschikkingen toe te staan

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Reorder]** sectie uit.

   ![&#x200B; herschikt opties &#x200B;](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Allow Reorder]** in op `Yes` .

   Met deze instelling wordt functionaliteit voor opnieuw ordenen ingeschakeld vanaf de klantenaccount in de winkel of in de lijst met bestellingen in de beheerder.

1. Klik op **[!UICONTROL Save Config]**.

## Opnieuw ordenen vanuit de winkel

Een klant kan de functionaliteit voor opnieuw ordenen voor een specifieke volgorde op twee pagina&#39;s starten:

- _Mijn Orden_ pagina

- _de Mening van de Orde_ pagina

### Mijn bestellingen

De _herschikt_ knoop wordt altijd getoond in de lijst met Worden (zelfs als alle producten van de orde niet beschikbaar voor reorder zijn).

![&#x200B; storefront van het Voorbeeld - Mijn pagina van Orden &#x200B;](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Geval 1.** Alle producten van de orde zijn **beschikbaar** voor reorder

De gebruiker wordt omgeleid naar de kar en alle producten worden toegevoegd aan de kar

![&#x200B; Shopping kar &#x200B;](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Geval 2.** Sommige/alle producten van de orde zijn **niet beschikbaar** voor reorder

>[!NOTE]
>
>Het is mogelijk om `Not Visible Individually` -producten opnieuw te ordenen.

De _herschikt_ knoop verschijnt niet op _Mijn Orden_ en _Volgorde van de Mening_ pagina&#39;s.

![&#x200B; Mijn Orden pagina 1 &#x200B;](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Weergavepagina Volgorde

**Geval 1.** Alle producten van de bestelling zijn beschikbaar voor herschikking

De gebruiker wordt omgeleid naar de kar en alle producten worden toegevoegd aan de kar

**Geval 2.** Sommige/alle producten van de orde zijn **niet beschikbaar** voor reorder

>[!NOTE]
>
>Het is mogelijk om `Not Visible Individually` -producten opnieuw te ordenen.

De _herschikt_ knoop verschijnt niet op _Mijn Orden_ en _Volgorde van de Mening_ pagina&#39;s.

![&#x200B; de detailpagina van de Orde &#x200B;](./assets/order-view-page.png){width="700" zoomable="yes"}

### Winkelwagentje is niet leeg

Als het karretje niet leeg is en de gebruiker **[!UICONTROL Reorder]** klikt (van _Mijn Orden_ of _de pagina van de Mening van de Orde_), blijven de bestaande producten in het karretje met toegevoegde reorder producten.

![&#x200B; opnieuw rangschikt punten &#x200B;](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Opnieuw ordenen via de beheerder

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde en open in de modus **[!UICONTROL View]** .

1. Klik op **[!UICONTROL Reorder]** dat wordt weergegeven in de bovenste knopbalk.

   ![&#x200B; de details van de Orde in Admin &#x200B;](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Nadat u **[!UICONTROL Reorder]** klikt, _creeer Nieuwe Orde_ pagina met reorder producten opent.

   ![&#x200B; creeer reorder &#x200B;](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Vul alle vereiste velden naar wens in.

1. Klik op **[!UICONTROL Submit Order]** om de volgorde te verzenden.
