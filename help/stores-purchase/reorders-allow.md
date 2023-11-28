---
title: Herstellingen toestaan
description: Leer hoe u mogelijkheden voor het opnieuw ordenen van uw klanten kunt bieden.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Herstellingen toestaan

Als deze optie is ingeschakeld, kunt u de volgorde direct vanaf de klantenaccount of vanaf de oorspronkelijke volgorde in de _Beheerder_. Herstellingen zijn standaard ingeschakeld.

![Koppeling voor opnieuw ordenen van klant in Admin](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Criteria voor het inschakelen van de volgorde van een bestelling

- De _Opnieuw ordenen toestaan_ De configuratieoptie moet worden ingeschakeld.

- Als de volgorde in `Hold` of in `Payment Review` status, is de optie voor opnieuw ordenen uitgeschakeld.

- Als een van de items in de volgorde niet beschikbaar, uit voorraad of uitgeschakeld is, is de optie voor opnieuw ordenen uitgeschakeld in de winkel.

- An _Beheerder_ kan de volgorde wijzigen, zelfs als een van de items uit voorraad is of is uitgeschakeld.

## Configureren om klantherschikkingen toe te staan

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Reorder]** sectie.

   ![Opties voor opnieuw ordenen](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Allow Reorder]** tot `Yes`.

   Met deze instelling wordt functionaliteit voor opnieuw ordenen ingeschakeld vanaf de klantenaccount in de winkel of in de lijst met bestellingen in de beheerder.

1. Klik op **[!UICONTROL Save Config]**.

## Opnieuw ordenen vanuit de winkel

Een klant kan de functionaliteit voor opnieuw ordenen voor een specifieke volgorde op twee pagina&#39;s starten:

- _Mijn bestellingen_ page

- _Weergave bestelling_ page

### Mijn bestellingen

De _Opnieuw_ Deze knop wordt altijd weergegeven in de lijst met bestellingen (zelfs als niet alle producten in de bestelling opnieuw kunnen worden geordend).

![Voorbeeld van winkel - pagina Mijn bestellingen](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Zaak 1.** Alle producten van de orde zijn **beschikbaar** voor herschikking

De gebruiker wordt omgeleid naar de kar en alle producten worden toegevoegd aan de kar

![Winkelwagentje](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Zaak 2.** Enkele/alle producten uit de bestelling zijn **niet beschikbaar** voor herschikking

>[!NOTE]
>
>Het is mogelijk de volgorde te wijzigen `Not Visible Individually` producten.

De _Opnieuw_ wordt niet weergegeven op de knop _Mijn bestellingen_ en _Volgorde weergeven_ pagina&#39;s.

![Pagina met Mijn bestellingen 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Weergavepagina Volgorde

**Zaak 1.** Alle producten van de bestelling kunnen opnieuw worden geordend

De gebruiker wordt omgeleid naar de kar en alle producten worden toegevoegd aan de kar

**Zaak 2.** Enkele/alle producten uit de bestelling zijn **niet beschikbaar** voor herschikking

>[!NOTE]
>
>Het is mogelijk de volgorde te wijzigen `Not Visible Individually` producten.

De _Opnieuw_ wordt niet weergegeven op de knop _Mijn bestellingen_ en _Volgorde weergeven_ pagina&#39;s.

![Pagina met bestelgegevens](./assets/order-view-page.png){width="700" zoomable="yes"}

### Winkelwagentje is niet leeg

Als het winkelwagentje niet leeg is en de gebruiker klikt **[!UICONTROL Reorder]** (van de _Mijn bestellingen_  of _Weergave bestelling_ pagina), blijven de bestaande producten in het winkelwagentje met de toegevoegde producten van de herschikking.

![Items opnieuw ordenen](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Opnieuw ordenen via de beheerder

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde en open deze in **[!UICONTROL View]** -modus.

1. Klikken **[!UICONTROL Reorder]** die wordt weergegeven in de bovenste knopbalk.

   ![Bestelgegevens in de beheerder](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Nadat u op **[!UICONTROL Reorder]** de _Nieuwe volgorde maken_ De pagina wordt geopend met producten opnieuw ordenen.

   ![Opnieuw ordenen](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Vul alle vereiste velden naar wens in.

1. Als u de volgorde wilt verzenden, klikt u op **[!UICONTROL Submit Order]**.
