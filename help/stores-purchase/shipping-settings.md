---
title: Verzendinstellingen
description: Leer hoe u de verzendinstellingen configureert die het oorsprongspunt en het verzendbeleid voor uw winkel definiëren.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Verzendinstellingen

De verzendconfiguratie bepaalt het uitgangspunt voor alle verzendingen, uw verzendbeleid en de verwerking van verzendingen naar meerdere adressen.

## Punt van oorsprong

Het punt van oorsprong wordt gebruikt voor de berekening van de kosten voor overbrengingen uit uw winkel of pakhuis, en bepaalt ook het belastingtarief voor verkochte producten. Wanneer het berekenen van [&#x200B; EU belastingen &#x200B;](international-tax-guidelines.md#eu-tax-configuration), zorg ervoor dat de [&#x200B; Berekening van de StandaardBelastingbestemming &#x200B;](../configuration-reference/sales/tax.md) voor elke opslagmening aan het Verschepende punt van Montages van oorsprong beantwoordt.

![&#x200B; Oorsprong &#x200B;](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Shipping Settings]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Origin]** sectie uit en voltooi het volgende:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (en regel 2, indien nodig)

1. Klik op **[!UICONTROL Save Config]**.

## Verzendbeleid

Een verzendbeleid moet uitleg geven over de bedrijfsregels en richtlijnen van uw bedrijf voor verzendingen. Als je bijvoorbeeld prijsregels hebt die gratis verzending activeren, kun je de voorwaarden in je verzendbeleid uitleggen.

![&#x200B; Verzendbeleid tijdens Afhandeling &#x200B;](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Als je je verzendbeleid tijdens het afrekenen wilt weergeven, voltooi je de parameters voor het verzendbeleid in de configuratie. De tekst verschijnt wanneer de klanten _klikken zie ons het verschepen beleid_ tijdens controle.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Shipping Settings]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Shipping Policy Parameters]** sectie uit.

1. Stel **[!UICONTROL Apply Custom Shipping Policy]** in op `Yes` .

1. Plak of typ de **[!UICONTROL Shipping Policy]** in het tekstvak.

   >[!NOTE]
   >
   >Als u een tekstverwerker gebruikt om de tekst samen te stellen, zorg ervoor om het document als .txt dossier te bewaren om het even welke controlekarakters uit de tekst te verwijderen. Vervolgens kopieert en plakt u de tekst in het tekstvak Verzendbeleid.

   ![&#x200B; Verzendbeleidsparameters &#x200B;](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Meerdere adressen

Met de verzendopties voor meerdere adressen kunnen klanten tijdens het afrekenen een bestelling naar meerdere adressen verzenden en het maximumaantal adressen bepalen waarnaar een bestelling kan worden verzonden.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Multishipping Settings]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Options]** sectie uit.

   ![&#x200B; Verzendopties voor meerdere adressen &#x200B;](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Allow Shipping to Multiple Addresses]** in op `Yes` .

1. Voer de **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]** in.

1. Klik op **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![&#x200B; Adobe Commerce B2B &#x200B;](../assets/b2b.svg) (Adobe Commerce B2B) voor orden met veelvoudige verschepende adressen, is de [&#x200B; Betaling op Rekening &#x200B;](../b2b/enable-basic-features.md#configure-payment-on-account) betalingsmethode, zelfs als toegelaten, niet beschikbaar tijdens de controle.

## URL voor het bijhouden van verzending via e-mail

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service-projecten (door Adobe beheerde SaaS-infrastructuur)."}

Standaard zijn volgnummers voor verzendingen die in e-mails van winkels worden verzonden, onbewerkte tekst. U kunt deze volgnummers omzetten in klikbare koppelingen door de functie URL voor aangepaste URL bijhouden in te schakelen. Met deze functie kunt u een sjabloon definiëren voor het bijhouden van URL&#39;s voor verschillende verzendende maatschappijen. Elke sjabloon bevat de volledige URL naar de volgende website en een tijdelijke aanduiding voor het trackingnummer. Commerce vervangt de tijdelijke aanduiding door het werkelijke trackingnummer in het e-mailbericht.

De volgende luchtvaartmaatschappijen worden ondersteund:

- United States Postal Service (USPS)
- United Parcel Service (UPS)
- Federal Express (FedEx)
- DHL Express (DHL)

Aangepaste URL&#39;s voor bijhouden inschakelen of bewerken:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Shipping Settings]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Shipment Tracking URLs]** sectie uit.

1. Stel **[!UICONTROL Enable Custom Tracking URLs]** in op `Yes` .

1. Voor elke ondersteunde provider worden standaard-URL-sjablonen opgegeven. Als u een van deze waarden moet wijzigen, voert u in het desbetreffende veld een nieuwe URL-sjabloon in. Gebruik `{{tracking_number}}` als plaatsaanduiding voor het werkelijke trackingnummer. Als UPS bijvoorbeeld de URL wijzigt in `https://www.ups.com/newtracker?tracknumber` , ziet de nieuwe URL-sjabloon voor bijhouden er als volgt uit:

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. Klik op **[!UICONTROL Save Config]**.
