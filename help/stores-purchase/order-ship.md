---
title: Een bestelling verzenden
description: Leer hoe u de verzendgegevens voor een verwerkingsbestelling invult en de verzendings- en trackinggegevens bekijkt.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Een bestelling verzenden

Een bestelling die is betaald maar nog niet is verzonden, heeft de `Processing` -status. Het overladingsverslag bevat een gedetailleerde geschiedenis van het aan de bestelling gerelateerde afhandelingsproces. Gedeeltelijke overbrengingen kunnen plaatsvinden totdat aan de bestelling is voldaan.

1. Voor _Admin_ sidebar, uitgezochte **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek in de lijst _[!UICONTROL Orders]_&#x200B;de volgorde die u wilt verzenden en klik om deze te openen.

1. Klik in de rechterbovenhoek op de knop **[!UICONTROL Ship]** .

1. Als u het facturerings- of verzendadres wilt bijwerken, klikt u op de koppeling **[!UICONTROL Edit]** in de rechterbovenhoek van de sectie.

   Breng de gewenste wijzigingen aan en klik op **[!UICONTROL Save Order Address]** .

1. Als u wilt dat de vervoerder een verzendlabel genereert, schakelt u het selectievakje **[!UICONTROL Create Shipping Label]** in en stelt u de opties in:

   - Als u een trackingnummer wilt toevoegen, schuift u omlaag naar de sectie _[!UICONTROL Shipping Information]_&#x200B;en klikt u op **[!UICONTROL Add Tracking Number]**.

   - Voer een van de volgende handelingen uit:

      - Selecteer **[!UICONTROL Carrier]** en voer de tekstspatiëring in **[!UICONTROL Number]** .

      - Stel **[!UICONTROL Carrier]** in op `Custom Value` , voer een **[!UICONTROL Title]** voor de aangepaste drager in en voer de tekstspatiëring in **[!UICONTROL Number]** .

      - [&#x200B; het volgen van de Mening informatie &#x200B;](#track-the-shipment).

1. Als u een gedeeltelijke verzending wilt maken, schuift u omlaag naar de sectie Items naar verzending en voert u de **[!UICONTROL Qty to Ship]** voor elk item in.

1. Ga als volgt te werk om klanten via e-mail op de hoogte te stellen van de verzending:

   - Voer de opmerkingen in die u in het vak **[!UICONTROL Shipment Comments]** wilt opnemen.

   - Schakel het selectievakje **[!UICONTROL Append Comments]** in om de opmerkingen op te nemen in het e-mailbericht dat naar de klant wordt verzonden.

   - Schakel het selectievakje **[!UICONTROL Email Copy of Shipment]** in als u een kopie van de verzending-e-mail naar uzelf wilt verzenden.

     De status van een e-mail op de factuur wordt weergegeven naast het factuurnummer van de voltooide factuur, al dan niet verzonden.

1. Klik op **[!UICONTROL Submit Shipment]** als de bewerking is voltooid.

   De status van de volgorde verandert van `Processing` in `Complete` .

>[!NOTE]
>
>Als een bestelling wordt geplaatst als &#39;levering in de winkel&#39;, zijn er geen verzendopties beschikbaar. Klik op **[!UICONTROL Notify Order is Ready for Pickup]** om een e-mailbericht naar de klant te activeren. De status van de volgorde wordt vervolgens gewijzigd in `Complete` .

## De verzenddetails weergeven

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Zoek de verzending in de lijst en klik om de record te openen.

1. Als u een opmerking aan de volgorde wilt toevoegen, schuift u omlaag naar de sectie _[!UICONTROL Comments History]_&#x200B;en voert u de opmerking in het vak in.

   - Als u de opmerking per e-mail naar de klant wilt verzenden, schakelt u het selectievakje **[!UICONTROL Notify Customer by Email]** in.

   - Schakel het selectievakje **[!UICONTROL Visible on Frontend]** in om de opmerking op het account van de klant te plaatsen.

1. Klik op **[!UICONTROL Update]**.

## De verzending volgen

**Methode 1:** Van het lusje van de ordeinformatie

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de verzendvolgorde in het raster en klik op **[!UICONTROL View]** .

1. Blader omlaag naar de sectie _[!UICONTROL Shipping & Handling Information]_&#x200B;en klik op **[!UICONTROL Track Order]**.

   Alle beschikbare trackinggegevens worden weergegeven in een pop-upvenster.

1. Klik op **[!UICONTROL Close Window]** als u klaar bent.

**Methode 2:** Van de ladinglusje van de orde

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Zoek de verzending in de lijst en klik om de record te openen.

1. Klik op **[!UICONTROL Track this Shipment]**.

   Alle beschikbare trackinggegevens worden weergegeven in een pop-upvenster.

1. Klik op **[!UICONTROL Close Window]** als u klaar bent.
