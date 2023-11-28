---
title: Voorbeeld van de prijsregel voor winkelwagentjes - korting met eerste aankoop
description: Bekijk een voorbeeld van het gebruik van een winkelprijsegel om klanten die voor het eerst een korting willen aanbieden.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Voorbeeld van de prijsregel voor winkelwagentjes - korting met eerste aankoop

{{ee-feature}}

Met de prijsregels voor winkelwagentjes kan automatisch een korting worden aangeboden aan klanten bij hun eerste aankoop, zonder dat er een coupon nodig is.

Om een korting aan te bieden die aan eerste klanten wordt gericht, kunt u:

- Creeer een klantensegment dat zoals wordt bepaald _kopers zonder bestelling_ en vervolgens
- Creeer een de prijsregel van de winkelwagentje die het nieuwe klantensegment richt.

>[!NOTE]
>
>Zorg ervoor dat de functie voor klantsegmenten is ingeschakeld. Zie [Een klantsegment maken](../customers/customer-segment-create.md).

## Stap 1. Een klantsegment maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Segment]**.

1. Definieer de **[!UICONTROL General Properties]**.

   - Voer een **[!UICONTROL Segment Name]** om het klantensegment te identificeren (Voorbeeld: _Eerste klant_).

   - Voor **[!UICONTROL Assigned to Website]** selecteert u de website waarop het klantensegment kan worden gebruikt.

   - Voor **[!UICONTROL Status]**, selecteert u `Active`.

   - Voor **[!UICONTROL Apply to]**, selecteert u `Visitors and Registered Customers`.

   - Klik op **[!UICONTROL Save and Continue Edit]**.

     Extra opties zijn beschikbaar in het deelvenster aan de linkerkant.

   ![Eigenschappen van klantensegment](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Definieer de **[!UICONTROL Conditions]**.

   In dit voorbeeld richt de voorwaarde zich op klanten voor wie _Het totale aantal bestellingen is kleiner dan 1_ is Waar.

   - Kies in het deelvenster aan de linkerkant de optie **[!UICONTROL Conditions]**.

     De standaardvoorwaarde begint, &quot;als ALLE van deze voorwaarden WAAR zijn:&quot;

   - Klikken _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) en selecteert u `Number of Orders`.

   - Klik op **[!UICONTROL is]** en selecteer `less than`.

   - Klikken **...** en betreden `1` in het veld.

   - Klik op het groene vinkje ( ![Groen vinkje](../assets/icon-checkmark-green-circle.png) ) om de voorwaarde-instelling op te slaan.

   ![Klantsegmentvoorwaarde](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

Het klantensegment wordt gecreeerd en in _[!UICONTROL Customer Segments]_raster.

>[!TIP]
>
>Noteer de segment-id. Met dit ID-nummer kunt u de regel voor de winkelprijs maken.

## Stap 2. De regel voor de winkelprijs maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Rule]**.

   De **[!UICONTROL Rule Information]** sectie wordt standaard weergegeven, met uitbreidbare secties voor **[!UICONTROL Conditions]** en **[!UICONTROL Conditions]**.

1. Definieer de **[!UICONTROL Rule Information]**.

   - Voltooi de **[!UICONTROL Rule Name]** en **[!UICONTROL Description]** velden. Deze velden zijn alleen bedoeld voor uw interne referentie.

   - Voor **[!UICONTROL Websites]** selecteert u de website waarop de regel beschikbaar moet zijn.

   - Voor **[!UICONTROL Customer Groups]** selecteert u de klantengroep waarop deze regel van toepassing is.

     Als u meerdere groepen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

     >[!NOTE]
     >
     >De opties in deze lijst hangen van de klantengroepen af die binnen worden gecreeerd en worden geleid **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - Voor **[!UICONTROL Coupon]**, selecteert u `No Coupon`.

   - Voor **[!UICONTROL Uses per Customer]**, enter `1`.

   - Voor **[!UICONTROL Priority]** Voer een getal in om de prioriteit van deze regel ten opzichte van andere regels vast te stellen.

     >[!NOTE]
     >
     >De instelling Prioriteit is belangrijk wanneer hetzelfde catalogusproduct voldoet aan de voorwaarden die voor meer dan één prijsregel zijn ingesteld. De regel met de hoogste Prioriteit het plaatsen wordt actief voor de klant. De hoogste prioriteit is 1. In dit voorbeeld voert u `1` betekent dat deze regel wordt toegepast vóór enige andere prijsregel. Deze waarde wordt gebruikt door de **[!UICONTROL Discard Subsequent Rules]** in het dialoogvenster **[!UICONTROL Action]** sectie.

   - Klik op **[!UICONTROL Save and Continue Edit]**.

     Extra opties zijn beschikbaar in het deelvenster aan de linkerkant.

   ![Informatie over de prijsregel voor winkelwagentjes](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Definieer de **[!UICONTROL Conditions]**.

   - Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Conditions]** sectie.

     De standaardregel begint met &quot;Als ALLE van deze voorwaarden WAAR zijn:&quot;.

   - Klikken _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) en selecteert u `Customer Segment`.

     Het kwalificatieveld is standaard ingesteld op `matches`.

   - Klikken **...** en ga segmentidentiteitskaart van het klantensegment in u wilt richten.

     Voor dit voorbeeld, segmentidentiteitskaart voor het nieuwe segment dat in Stap 1 wordt gecreeerd is `2`.

     >[!NOTE]
     >
     >Als u segmentid niet kent, klikt u op het pictogram van de kiezer ( ![Lijstpictogram](../assets/icon-list-chooser.png) ) om de lijst met klantsegmenten weer te geven. U kunt de id handmatig invoeren in het veld of het selectievakje voor het gewenste segment inschakelen om het veld automatisch in te vullen.

   - Klik op het groene vinkje ( ![Groen vinkje](../assets/icon-checkmark-green-circle.png) ) om de voorwaarde-instelling op te slaan.

   - Klik op **[!UICONTROL Save and Continue Edit]**.

     Deze lijn van de regel is op alle klanten van toepassing die klant segmentidentiteitskaart 2 aanpassen.

   ![Klantsegmentvoorwaarde](./assets/customer-segment-matches.png){width="400"}

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png)de **[!UICONTROL Conditions]** en definieert u de handelingen voor de regel.

   In deze sectie definieert u het type korting en de waarde/het bedrag van de korting die u wilt toepassen op nieuwe klanten. In dit voorbeeld wordt een korting van 10% gedefinieerd voor alle klanten die aan de gedefinieerde voorwaarde voldoen. Zie voor informatie over andere beschikbare opties [Een regel voor een startprijs maken](price-rules-cart-create.md).

   - Voor **[!UICONTROL Apply]**, selecteer Percentage van de korting op de productprijs.

   - Voor **[!UICONTROL Discount Amount]**, enter `10`.

   - Als u deze prijsregel alleen op productbedragen wilt toepassen, stelt u **[!UICONTROL Apply to Shipping Amount]** tot `No`.

   - Om te voorkomen dat het systeem meerdere prijsregels toepast op hetzelfde product, stelt u **[!UICONTROL Discard Subsequent Rules]** tot `Yes`.

   - Klik op **[!UICONTROL Save]**.

   ![Handelingen met prijsregels voor winkelwagentjes](./assets/actions-first-time.png){width="600" zoomable="yes"}

De nieuwe regel is normaal beschikbaar binnen het uur. Test de regel om er zeker van te zijn dat deze werkt zoals u deze hebt gedefinieerd.

## Stap 3: Sla de regel op en test deze

{{new-price-rule}}

1. Wanneer uw regel volledig is, klik **[!UICONTROL Save Rule]**.

1. Test de regel om er zeker van te zijn dat deze correct werkt.
