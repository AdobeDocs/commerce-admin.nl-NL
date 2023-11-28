---
title: Winkelkrediet toepassen
description: Winkelbeheerders kunnen winkelkrediet op een aankoop toepassen.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Winkelkrediet toepassen

{{ee-feature}}

Winkelbeheerders kunnen het creditsaldo en de geschiedenis van de rekening van de klant bekijken, en ook opslagkrediet op een aankoop toepassen.

![Kredietbalans en geschiedenis van klanten](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Het creditsaldo weergeven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klant in het raster.

1. In de _Handeling_ kolom, klik **[!UICONTROL Edit]**.

1. Schuiven _[!UICONTROL Customer View]_pagina en de **[!UICONTROL Store Credit Balance]**onderaan.

![Winkelcreditsaldo](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Kredietbalans van winkel bijwerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > _Bewerkingen_ > **[!UICONTROL All Customers]**.

1. Zoek de klant in het raster.

1. In de _Handeling_ kolom, klik **[!UICONTROL Edit]**.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Store Credit]**.

1. Kies de website (winkel) die u aan de balans wilt koppelen.

1. Voor **[!UICONTROL Update Balance]** Voer de nieuwe waarde in.

1. Als u de klant op de hoogte wilt stellen van de balansupdate, selecteert u de **[!UICONTROL Notify Customer by Email]** selectievakje en kies de winkelweergave vanuit **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Voer een **[!UICONTROL Comment]** over de wijziging.

1. Wanneer de updates zijn voltooid, klikt u op **[!UICONTROL Save and Continue Edit]** of **[!UICONTROL Save Customer]**.

De bijgewerkte balans wordt weergegeven in **[!UICONTROL Balance History]**.

## Pas een creditsaldo op een orde als opslagbeheerder toe

Als opslagbeheerder, kunt u diverse dingen namens een klant doen, met inbegrip van het voorleggen van orden. Wanneer u [een bestelling maken](../stores-purchase/customer-account-create-order.md), kun je een creditsaldo voor je winkel toepassen dat verschuldigd is aan de klant. De beschikbare balans wordt weergegeven in het dialoogvenster _Betalings- en verzendgegevens_ sectie. Selecteer de **[!UICONTROL Use Store Credit]** Schakel het selectievakje in om het saldo toe te passen of een deel van het saldo als het totaal van de volgorde lager is.

![Het creditsaldo van de winkel toepassen op de bestelling](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Winkelkrediet toepassen tijdens afhandeling

Als er een creditsaldo voor de plaats is, kan de klant opslagkrediet op het ordesaldo toepassen alvorens de orde op de storefront te plaatsen.

1. De klant bekijkt de hoeveelheid beschikbaar winkelkrediet.

   Tijdens de _Reviseren en betalen_ stap, het beschikbare bedrag wordt weergegeven onder _[!UICONTROL Store Credit]_.

1. Als u het bedrag op de volgorde wilt toepassen, klikt u op **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Het ordertotaal wordt opnieuw berekend en het bedrag van het winkelkrediet dat wordt toegepast, wordt weergegeven in de _[!UICONTROL Order Summary]_.

   ![Het creditsaldo van de winkel wordt toegepast op de bestelling](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Klik wanneer u klaar bent op **[!UICONTROL Place Order]**.
