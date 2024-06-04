---
title: Verzendinstellingen
description: Leer hoe u de verzendinstellingen configureert die het oorsprongspunt en het verzendbeleid voor uw winkel definiëren.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Verzendinstellingen

De verzendconfiguratie bepaalt het uitgangspunt voor alle verzendingen, uw verzendbeleid en de verwerking van verzendingen naar meerdere adressen.

## Punt van oorsprong

Het punt van oorsprong wordt gebruikt voor de berekening van de kosten voor overbrengingen uit uw winkel of pakhuis, en bepaalt ook het belastingtarief voor verkochte producten. Bij het berekenen [EU-belastingen](international-tax-guidelines.md#eu-tax-configuration), zorgt u ervoor dat de [Berekening standaardbelastingbestemming](../configuration-reference/sales/tax.md) voor elke winkelweergave komt overeen met het beginpunt van de verzendinstellingen.

![Oorsprong](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Shipping Settings]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Origin]** en vult het volgende in:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (en regel 2, indien nodig)

1. Klik op **[!UICONTROL Save Config]**.

## Verzendbeleid

Een verzendbeleid moet uitleg geven over de bedrijfsregels en richtlijnen van uw bedrijf voor verzendingen. Als je bijvoorbeeld prijsregels hebt die gratis verzending activeren, kun je de voorwaarden in je verzendbeleid uitleggen.

![Verzendbeleid tijdens afhandeling](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Als je je verzendbeleid tijdens het afrekenen wilt weergeven, voltooi je de parameters voor het verzendbeleid in de configuratie. De tekst wordt weergegeven wanneer klanten op _Zie ons verzendbeleid_ tijdens het afrekenen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Shipping Settings]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Shipping Policy Parameters]** sectie.

1. Set **[!UICONTROL Apply Custom Shipping Policy]** tot `Yes`.

1. Plakken of voer uw **[!UICONTROL Shipping Policy]** in het tekstvak.

   >[!NOTE]
   >
   >Als u een tekstverwerker gebruikt om de tekst samen te stellen, zorg ervoor om het document als .txt dossier te bewaren om het even welke controlekarakters uit de tekst te verwijderen. Vervolgens kopieert en plakt u de tekst in het tekstvak Verzendbeleid.

   ![Parameters voor verzendbeleid](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Meerdere adressen

Met de verzendopties voor meerdere adressen kunnen klanten tijdens het afrekenen een bestelling naar meerdere adressen verzenden en het maximumaantal adressen bepalen waarnaar een bestelling kan worden verzonden.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Multishipping Settings]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Options]** sectie.

   ![Verzendopties voor meerdere adressen](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Allow Shipping to Multiple Addresses]** tot `Yes`.

1. Voer de **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Klik op **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Voor bestellingen met meerdere verzendadressen worden de [Betaling op rekening](../b2b/enable-basic-features.md#configure-payment-on-account) De betalingsmethode, zelfs als deze ingeschakeld is, is niet beschikbaar tijdens het afrekenen.
