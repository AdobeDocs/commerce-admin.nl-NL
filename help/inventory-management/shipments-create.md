---
title: Multibronzendingen maken
description: Leer hoe leveranciers met meerdere leveranciers verzendingen kunnen maken en verzenden.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Multibronzendingen maken

Met [!DNL Inventory Management], verzendt u een of meer verzendingen terwijl u een voorraad hebt. Herhaal deze instructies met de aanbevolen of handmatig ingevoerde hoeveelheden en bronnen om zo nodig extra verzendingen te genereren. In deze instructies wordt gedetailleerd beschreven hoe leveranciers uit meerdere bronnen zendingen verzenden. Single-source-handelaren verzenden zendingen zonder deze extra stappen (zie [Een verzending maken](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} in de basisgebruikershandleiding).

Wanneer het creëren van verzendingen, gebruik het Algoritme Bron van de Selectie voor berekende aanbevelingen. Volg en gebruik deze aanbevelingen of stel de bedragen per bron in, die douaneverzendingen produceren. U beheert de uitgaande voorraad voor elke bestelling, waarbij u de af te trekken bedragen instelt, een of meer verzendingen verzendt en de voorraad en de achterstand instelt terwijl de voorraad beschikbaar is. Voer voor elk regelitem in de volgorde een bedrag in dat van de bronhoeveelheid moet worden afgetrokken.

U wilt mogelijk gedeeltelijke verzendingen verzenden naar:

- Terugboekingen uitvoeren als inventarisatie wordt binnengekomen

- Aftrekposten van voorraden naar bron

Terwijl u verzendingen invoert, worden de ingevoerde hoeveelheden in de voorraad afgetrokken. In feite worden de punten van voorbehoud omgezet in de feitelijke aftrekposten voor de hoeveelheid.

## Een verzending maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde en open de weergavemodus.

1. Als de bestelling is betaald en gefactureerd en klaar is voor verzending, klikt u op **[!UICONTROL Ship]**.

1. Voltooi de Bronselectie voor het verzenden van producten per bron:

   - Klik op **[!UICONTROL Source Selection Algorithm]** en selecteer een algoritme.

     | Algorithm | Beschrijving |
     |--|--|
     | [Bronprioriteit](source-priority-algorithm.md) | beveelt aan om zendingen uit bronnen te verzenden volgens de orders van bronnen die aan het bestand zijn toegewezen. |
     | [Prioriteit afstand](distance-priority-algorithm.md) | Aanbevolen verzendingen van bronnen die zich het dichtst bij het verzendadres bevinden op basis van de fysieke afstand of de kortste levertijd. |

     >[!IMPORTANT]
     >
     >Wanneer het gebruiken van het Prioriteitsalgoritme van de Afstand voor het verschepen en de routes en de gegevens keert niet voor geselecteerde terug [Rekenmodus](distance-priority-algorithm.md) (het besturen, het fietsen, of het lopen) voor een lading, blijft SSA aan de Prioriteit Bron in gebreke. U kunt het beste ook de instelling [prioriteit voor bronnen per bestand](stocks-prioritize-sources.md).


   - Voor  **[!UICONTROL Select a Source to Ship from]**, selecteert u een bron om een verzending te verzenden.

   - Houd voor elk regelitem de aanbevolen hoeveelheid of voer een specifiek bedrag in in het gedeelte **[!UICONTROL Qty to Deduct]**. Deze waarde geeft het bedrag aan dat wordt afgetrokken van de inventaris van de geselecteerde bron.

   - Klik op **[!UICONTROL Proceed to Shipment]**.

     ![Selecteer een bron en voer een hoeveelheid in](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Controleer de _[!UICONTROL New Shipment]_en voert u zo nodig aanvullende wijzigingen in.

   De _[!UICONTROL Inventory]_in deze sectie worden de bron, de producten die worden verzonden, de totale geordende hoeveelheid en de hoeveelheid die wordt verzonden weergegeven.

   ![Voorraadgegevens voor de overbrenging, bijvoorbeeld gedeeltelijke overbrenging](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Klikken **[!UICONTROL Submit Shipment]** in.
