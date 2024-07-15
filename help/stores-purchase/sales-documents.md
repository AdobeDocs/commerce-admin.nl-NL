---
title: Verkoopdocumenten
description: Leer hoe u verkoopdocumenten configureert ter ondersteuning van bestellingen van klanten en het uitvoeren van uw Commerce-winkel.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Verkoopdocumenten

Om de ordewerkstroom te steunen en uw klanten documentatie over de orden te verstrekken die zij indienen, vorm de verwante verkoopdocumenten om uw merk van de winkel te weerspiegelen en verwijzingsinformatie te omvatten.

## Facturen en verpakkingsslips configureren

In tegenstelling tot de afbeeldingen van het logo die worden gebruikt in winkelpagina&#39;s, kan het logo voor PDF-facturen en andere verkoopdocumenten een afbeelding van 300 dpi met hoge resolutie zijn. Zorg ervoor dat de hoogte-breedteverhouding behouden blijft wanneer u het formaat van het logo wijzigt. Pas het formaat van het logo aan zodat het in de hoogte past en maak u geen zorgen over ongebruikte ruimte aan de rechterkant.

![ embleem van de Steekproef ](./assets/logo-pdf.png){width="200"}

U kunt de grootte van het logo aanpassen aan de vereiste grootte door een nieuwe, lege afbeelding met de juiste afmetingen te maken. Vervolgens plakt u de logoafbeelding en past u de grootte ervan aan de hoogte aan. In de meeste beeldbewerkingsprogramma&#39;s kunt u de afbeelding met een percentage schalen om de hoogte-breedteverhouding te behouden of de Shift-toets ingedrukt houden en de afbeelding handmatig vergroten of verkleinen.

**_om het embleem bij te werken:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Invoice and Packing Slip Design]** sectie uit en doe het volgende:

   ![ de configuratie van de Verkoop - verkoopfactuur en verpakkingsslipontwerp ](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Als u de **[!UICONTROL Logo for PDF Print-outs]** wilt uploaden, klikt u op **[!UICONTROL Choose File]** , zoekt u het logo dat u hebt voorbereid en klikt u op **[!UICONTROL Open]** .

   - Als u de **[!UICONTROL Logo for HTML Print View]** wilt uploaden, klikt u op **[!UICONTROL Choose File]** , zoekt u het logo dat u hebt voorbereid en klikt u op **[!UICONTROL Open]** .

   - Voer uw adres in zoals u het wilt weergeven op facturen en pakslips.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

   Ter referentie wordt voor elk veld een miniatuur van de geüploade afbeelding weergegeven. Maak u geen zorgen als de miniatuur vervormd wordt weergegeven. Het aandeel van het logo is correct op de factuur.

### Een afbeelding vervangen

1. Klik op **[!UICONTROL Choose File]** en kies een ander logobestand.

1. Schakel het selectievakje **[!UICONTROL Delete Image]** in voor de afbeelding die u wilt vervangen.

1. Klik op **[!UICONTROL Save Config]**.

### Afbeeldingsindelingen

| Indeling | Vereisten |
|--- |------------------------------------------|
| **_PDF_** |  |
| Bestandsindeling | JPG (JPEG), PNG, TIF (TIFF) |
| Afbeeldingsgrootte | Tot 1080 pixels breed x 270 pixels hoog |
| Resolutie | 300 DPI aanbevolen |
| **_HTML_** |  |
| Bestandsindeling | JPG (JPEG), PNG, GIF |
| Afbeeldingsgrootte | Gedefinieerd op thema. |
| Resolutie | 72 of 96 DPI |

{style="table-layout:auto"}

## Referentie-id&#39;s toevoegen

De identiteitskaart van de Orde en klantIP adres kunnen in de kopbal van verkoopdocumenten worden omvat die een orde vergezellen. Standaard worden zowel de bestellings-id als het IP-adres van de klant weergegeven in de koptekst van facturen, pakslips voor verzending en creditnota&#39;s.

![ de configuratie van de Verkoop - PDF druk-outs ](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_om ordeidentiteitskaart het plaatsen te veranderen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL PDF Print-outs]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **Factuur** sectie uit.

1. Stel **[!UICONTROL Display Order ID in Header]** in op basis van uw voorkeur.

1. Herhaal dit voor de secties **[!UICONTROL Shipment]** en **[!UICONTROL Credit Memo]** .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

**_om het klantIP adres te veranderen dat:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL General]** sectie uit.

   ![ configuratie van de Verkoop - algemene verkoopmontages ](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Hide Customer IP]** in op uw voorkeur.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
