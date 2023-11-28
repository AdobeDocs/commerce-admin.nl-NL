---
title: Vaste verzendkosten
description: Leer hoe je een optie voor vaste verzendkosten instelt voor je winkel.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Vaste verzendkosten

_Plat tarief_ is een vaste, vooraf gedefinieerde vergoeding die per artikel of per zending kan worden toegepast. Vlak tarief is een eenvoudige verzendoplossing, vooral wanneer gebruikt met de vlakke verpakking die van sommige vervoerders beschikbaar is. Indien ingeschakeld, _Platte snelheid_ wordt weergegeven als een optie tijdens het uitchecken. Omdat geen specifieke drager wordt gespecificeerd, kunt u een drager van uw keus gebruiken.

## Vaste verzendkosten instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **Platte snelheid** sectie.

   ![Platte snelheid](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [Platte snelheid](../configuration-reference/sales/delivery-methods.md#flat-rate) in de _Referentiehandleiding voor configuratie_.

1. Set **[!UICONTROL Enabled]** tot `Yes`.

   De vaste prijs wordt weergegeven als een optie in het gedeelte Schatting van verzendkosten en belasting van het winkelwagentje en ook in het gedeelte Verzending tijdens het afrekenen.

1. Voer een beschrijving in **[!UICONTROL Title]** voor de methode met vaste snelheid.

1. Voer een **Naam methode** naast het berekende tarief in het winkelwagentje.

   De standaardnaam van de methode is `Fixed`. Als je kosten in rekening brengt, kun je deze tekst wijzigen in `Plus Handling`of iets anders dat geschikt is.

1. Als u wilt beschrijven hoe vaste verzendkosten kunnen worden gebruikt, stelt u **Type** op een van de volgende wijzen:

   - `None` - Hiermee schakelt u het betalingstype uit. De optie Vlakke snelheid wordt weergegeven in de winkelwagentje, maar met een snelheid van nul. Dit is hetzelfde als gratis verzending.
   - `Per Order` - Hiermee wordt één vast tarief in rekening gebracht voor de gehele bestelling.
   - `Per Item` - Hiermee wordt voor elk object één vast tarief in rekening gebracht. Het tarief wordt vermenigvuldigd met het aantal artikelen in het karretje, ongeacht of er meerdere hoeveelheden van dezelfde of van verschillende posten zijn.

1. Voer de **Prijs** die je in rekening wilt brengen voor vaste verzendkosten.

1. Configureer de opties voor de behandelingskosten naar wens.

   De verpakkingskosten zijn optioneel en worden weergegeven als extra kosten die bij de verzendkosten worden opgeteld. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

   - Voor **Verhandelingskosten berekenen** selecteert u de methode die u wilt gebruiken voor het berekenen van afhandelingskosten:

      - `Fixed`
      - `Percent`

   - Voor **Verhandelingskosten** Voer het bedrag in dat moet worden aangerekend op basis van de methode die u hebt gekozen voor de berekening van het bedrag.

     Als de vergoeding bijvoorbeeld is gebaseerd op een vaste vergoeding, voert u het bedrag in als een decimaal, zoals `4.90`. Als de verpakkingskosten echter zijn gebaseerd op een percentage van de verzendkosten, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de verzendkosten in rekening brengt, voert u de waarde in als `6`.

1. Wijzig, indien nodig, de **Foutbericht weergeven**.

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als Vaste verzending niet beschikbaar is.

1. Set **Schip naar landen van toepassing**:

   - `All Allowed Countries` - Klanten van iedereen [landen](../getting-started/store-details.md#country-options) gespecificeerd in uw archiefconfiguratie kan deze leveringsmethode gebruiken.
   - `Specific Countries` - Als u deze optie kiest, _Schip naar specifieke landen_ wordt weergegeven. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Set **Methode tonen indien niet van toepassing**:

   - `Yes` - Geeft altijd de methode met vaste snelheid weer, zelfs als deze niet van toepassing is.
   - `No` - Geeft de methode met vaste snelheid alleen weer wanneer deze van toepassing is.

1. Voor **[!UICONTROL Sort Order]**, voert u een getal in om de volgorde te bepalen waarin Vaste verzending wordt weergegeven bij andere leveringsmethoden tijdens het afrekenen.

   `0` = eerst, `1` = seconde, `2` = derde, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.
