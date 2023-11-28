---
title: Een bestelling verzenden
description: Leer hoe u de verzendgegevens voor een verwerkingsbestelling invult en de verzendings- en trackinggegevens bekijkt.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Een bestelling verzenden

Een bestelling die is betaald maar nog niet is verzonden, heeft de `Processing` status. Het overladingsverslag bevat een gedetailleerde geschiedenis van het aan de bestelling gerelateerde afhandelingsproces. Gedeeltelijke overbrengingen kunnen plaatsvinden totdat aan de bestelling is voldaan.

1. Op de _Beheerder_ zijbalk, selecteren **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. In de _[!UICONTROL Orders]_, zoekt u de te verzenden order en klikt u om deze te openen.

1. Klik in de rechterbovenhoek op de knop **[!UICONTROL Ship]** knop.

1. Als u het facturerings- of verzendadres wilt bijwerken, klikt u op de knop **[!UICONTROL Edit]** in de rechterbovenhoek van de sectie.

   Breng de gewenste wijzigingen aan en klik op **[!UICONTROL Save Order Address]**.

1. Als u wilt dat de vervoerder een verzendlabel genereert, selecteert u de optie **[!UICONTROL Create Shipping Label]** Schakel het selectievakje in en stel de opties in:

   - Schuif omlaag naar de _[!UICONTROL Shipping Information]_en klik op **[!UICONTROL Add Tracking Number]**.

   - Voer een van de volgende handelingen uit:

      - Selecteer de **[!UICONTROL Carrier]** en voer de tekstspatiëring in **[!UICONTROL Number]**.

      - Set **[!UICONTROL Carrier]** tot `Custom Value`, voert u een **[!UICONTROL Title]** voor de aangepaste vervoerder en voer de volgende gegevens in **[!UICONTROL Number]**.

      - [Trackinggegevens weergeven](#track-the-shipment).

1. Als u een gedeeltelijke verzending wilt maken, schuift u omlaag naar de sectie Items naar verzending en voert u de optie **[!UICONTROL Qty to Ship]** voor elk item.

1. Ga als volgt te werk om klanten via e-mail op de hoogte te stellen van de verzending:

   - Voer de opmerkingen in die u in het dialoogvenster **[!UICONTROL Shipment Comments]** doos.

   - Als u de opmerkingen wilt opnemen in het e-mailbericht dat naar de klant is verzonden, selecteert u de optie **[!UICONTROL Append Comments]** selectievakje.

   - Als u een kopie van het e-mailbericht naar uzelf wilt verzenden, selecteert u de optie **[!UICONTROL Email Copy of Shipment]** selectievakje.

     De status van een e-mail op de factuur wordt weergegeven naast het factuurnummer van de voltooide factuur, al dan niet verzonden.

1. Klik op **[!UICONTROL Submit Shipment]**.

   De status van de bestelling verandert van `Processing` tot `Complete`.

>[!NOTE]
>
>Als een bestelling wordt geplaatst als &#39;levering in de winkel&#39;, zijn er geen verzendopties beschikbaar. Klikken **[!UICONTROL Notify Order is Ready for Pickup]** om een e-mail naar de klant te activeren. De status van de bestelling wordt vervolgens gewijzigd in `Complete`.

## De verzenddetails weergeven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Zoek de verzending in de lijst en klik om de record te openen.

1. Als u een opmerking aan de volgorde wilt toevoegen, schuift u omlaag naar de _[!UICONTROL Comments History]_en voer de opmerking in het vak in.

   - Als u de opmerking per e-mail naar de klant wilt verzenden, selecteert u de optie **[!UICONTROL Notify Customer by Email]** selectievakje.

   - Als u het commentaar in de account van de klant wilt plaatsen, selecteert u de optie **[!UICONTROL Visible on Frontend]** selectievakje.

1. Klik op **[!UICONTROL Submit Comment]**.

## De verzending volgen

**Methode 1:** Van het lusje van de Orderinformatie

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de verzendvolgorde op het raster en klik op **[!UICONTROL View]**.

1. Omlaag schuiven naar de _[!UICONTROL Shipping & Handling Information]_sectie en klik op **[!UICONTROL Track Order]**.

   Alle beschikbare trackinggegevens worden weergegeven in een pop-upvenster.

1. Klik op **[!UICONTROL Close Window]**.

**Methode 2:** Van het lusje van de verzending van de orde

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Zoek de verzending in de lijst en klik om de record te openen.

1. Klik op **[!UICONTROL Track this Shipment]**.

   Alle beschikbare trackinggegevens worden weergegeven in een pop-upvenster.

1. Klik op **[!UICONTROL Close Window]**.
