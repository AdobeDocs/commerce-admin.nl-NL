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

_Vlak tarief_ is een vaste, vooraf bepaalde lading die per punt, of per lading kan worden toegepast. Vlak tarief is een eenvoudige verzendoplossing, vooral wanneer gebruikt met de vlakke verpakking die van sommige vervoerders beschikbaar is. Wanneer toegelaten, _Flat Tarief_ verschijnt als optie tijdens controle. Omdat geen specifieke drager wordt gespecificeerd, kunt u een drager van uw keus gebruiken.

## Vaste verzendkosten instellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Delivery Methods]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **Vlakke sectie van het Tarief**.

   ![ Vlak Tarief ](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Vlak Tarief ](../configuration-reference/sales/delivery-methods.md#flat-rate) in de _Gids van de Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Enabled]** in op `Yes` .

   De vaste prijs wordt weergegeven als een optie in het gedeelte Schatting van verzendkosten en belasting van het winkelwagentje en ook in het gedeelte Verzending tijdens het afrekenen.

1. Voer een beschrijvende **[!UICONTROL Title]** waarde in voor de methode Snelheid.

1. Ga de Naam van de a **Methode** in om naast het berekende tarief in het het winkelwagentje te verschijnen.

   De standaardnaam van de methode is `Fixed` . Als u kosten in rekening brengt, kunt u deze tekst wijzigen in `Plus Handling` of iets anders dat geschikt is.

1. Om te beschrijven hoe de vlakke tarief verschepen kan worden gebruikt, plaats **Type** aan één van het volgende:

   - `None` - Hiermee schakelt u het betalingstype uit. De optie Vlakke snelheid wordt weergegeven in de winkelwagentje, maar met een snelheid van nul. Dit is hetzelfde als gratis verzending.
   - `Per Order` - Hiermee wordt één vaste snelheid in rekening gebracht voor de volledige bestelling.
   - `Per Item` - Hiermee wordt één vaste prijs berekend voor elk item. Het tarief wordt vermenigvuldigd met het aantal artikelen in het karretje, ongeacht of er meerdere hoeveelheden van dezelfde of van verschillende posten zijn.

1. Ga de **Prijs** in die u voor het vlakke tarief verschepen wilt in rekening brengen.

1. Configureer de opties voor de behandelingskosten naar wens.

   De verpakkingskosten zijn optioneel en worden weergegeven als extra kosten die bij de verzendkosten worden opgeteld. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

   - Voor **berekent Behandelingskosten**, selecteer de methode u wilt gebruiken om behandelende kosten te berekenen:

      - `Fixed`
      - `Percent`

   - Voor **Behandelende Tarief**, ga het te laden bedrag in, dat op de methode wordt gebaseerd u hebt gekozen om het bedrag te berekenen.

     Als de kosten bijvoorbeeld zijn gebaseerd op een vaste vergoeding, voert u het bedrag in als een decimaal, bijvoorbeeld `4.90` . Als de verpakkingskosten echter zijn gebaseerd op een percentage van de verzendkosten, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de verzendkosten in rekening brengt, voert u de waarde in als `6` .

1. Indien nodig, verander het **Weergegeven Bericht van de Fout**.

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als Vaste verzending niet beschikbaar is.

1. Plaats **Schip aan Toepasselijke Landen**:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze leveringsmethode gebruiken.
   - `Specific Countries` - wanneer u deze optie kiest, verschijnt de _Schip aan Specifieke Landen_ lijst. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Plaats **tonen Methode als niet van toepassing**:

   - `Yes` - Geeft altijd de methode met vaste snelheid weer, zelfs als deze niet van toepassing is.
   - `No` - Geeft de methode met vaste snelheid alleen weer wanneer deze van toepassing is.

1. Voer bij **[!UICONTROL Sort Order]** een getal in om de volgorde te bepalen waarin verzending met vaste kosten wordt weergegeven wanneer deze bij andere leveringsmethoden tijdens het afrekenen wordt vermeld.

   `0` = first, `1` = second, `2` = third, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.
