---
title: Bestelling door SKU
description: Leer hoe te om uw opslag te vormen om het opdracht geven door SKU als gemak voor uw klanten te steunen.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Bestelling door SKU

{{ee-feature}}

Een &#39;SKU&#39; is een &#39;Stock Keeping Unit&#39;. SKU&#39;s helpen online verkopers over het algemeen de belangrijkste productkenmerken zoals grootte, kleur, prijs, en materiaal te identificeren. Product-id&#39;s verschillen van SKU&#39;s:

- `Product ID` is opeenvolgende reeks aantallen die intern worden gebruikt om producten te identificeren en niet beschikbaar aan klanten zijn.
- De `SKU` wordt gegenereerd door de verkoper, meestal op basis van de productnaam en -kenmerken voor marketing of interne tracering. Bijvoorbeeld: een blauw, T-shirt voor de katoenproductie, formaatmedium: T-COT-MED-BL. Indien nodig kan de verkoper de SKU wijzigen.

Normaal gesproken bevat een SKU een reeks afkortingen die de onderscheidende kenmerken van het product aangeven. De maximale SKU-lengte is 64 tekens. SKUs is belangrijk om inventaris effectief te volgen en te beheren, zodat is het correct opzetten van hen voor e-handel kritiek.

_Orde door SKU_ is a [&#x200B; widget &#x200B;](../content-design/widgets.md) die in de opslag als gemak voor alle kopers kan worden getoond, of ter beschikking gesteld aan slechts de kopers in specifieke klantengroepen. Klanten kunnen de SKU- en kwantitatieve gegevens rechtstreeks in de Order invoeren per SKU-blok of een CSV-bestand uploaden vanaf hun klantenaccount. Ongeacht de configuratie, is de orde door SKU altijd beschikbaar om beheerders op te slaan.

![&#x200B; Orde door SKU in Storefront &#x200B;](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Volgorde door SKU configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de sectie **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Order by SKU Settings]** sectie uit.

1. Stel **[!UICONTROL Enable Order by SKU on my Account in Storefront]** in op een van de volgende opties:

   - `Yes, for Everyone` - Het blok van de Orde door SKU is beschikbaar in de opslag voor elke verkoopster.
   - `Yes, for Specified Customer Groups` - De orde door SKU is beschikbaar slechts aan leden van een specifieke klantengroep, zoals `Wholesale`.
   - `No` - Het blok van de Orde door SKU verschijnt niet in de winkel, en de Orde door de pagina van SKU is niet beschikbaar in de klantenrekening.

   ![&#x200B; Orde door de Montages van SKU &#x200B;](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

![&#x200B; Adobe Commerce B2B &#x200B;](../assets/b2b.svg) (Adobe Commerce B2B slechts) _&#x200B;**om de Orde door de functie van SKU toe te laten, maak de Snelle functie van de Orde onbruikbaar:**&#x200B;_

1. Ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_&#x200B;de optie **[!UICONTROL B2B Features]**

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL B2B Features]** sectie uit.

1. Stel **[!UICONTROL Enable Quick Order]** in op `No` .

   De [&#x200B; Snelle eigenschap van de Orde &#x200B;](../b2b/quick-order.md) staat klanten en gasten toe om orden snel te plaatsen die op SKU of productnaam worden gebaseerd.

## Storefront-ervaring

Wanneer de functionaliteit voor de opslag wordt gevormd, kunnen de klanten tot door SKU van om het even welke pagina opdracht geven die de _Orde door SKU_ widget of van hun rekeningsdashboard omvat.

### Volgorde door SKU van paginaslok

1. In de _Orde door het blok van SKU_, gaat de klant **[!UICONTROL SKU]** in en **[!UICONTROL Qty]** van het punt dat moet worden bevolen.

1. Als u nog een item wilt toevoegen, klikt u op **[!UICONTROL Add Row]** en herhaalt u het proces.

1. Klik op **[!UICONTROL Add to Cart]** .

### Bestellen door SKU van een klantenaccount

1. Vanaf de storefront meldt de klant zich aan bij zijn account.

1. Kies **[!UICONTROL Order by SKU]** in het linkerdeelvenster.

1. Hiermee voegt u afzonderlijke items toe op basis van voorkeur:

   _&#x200B;**voegt elk punt door SKU toe:**&#x200B;_

   - Voer de **[!UICONTROL SKU]** en **[!UICONTROL Qty]** in van het item dat moet worden geordend.

   - Om extra punten toe te voegen zoals nodig, klikt _Rij_ ![&#x200B; plus ondertekent knoop &#x200B;](../assets/button-add-item.png) en herhaalt voor zo vele punten zonodig.

   - Klik op **[!UICONTROL Add to Cart]** .

   _&#x200B;**uploadt een Csv- dossier van veelvoudige punten:**&#x200B;_

   - Bereidt een [&#x200B; dossier van de de invoergegevens CSV &#x200B;](../systems/data-csv.md) (komma-Gescheiden Waarde) voor dat kolommen voor `SKU` en `Qty` omvat.

   ![&#x200B; SKUs om &#x200B;](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"} in te voeren

   - Klik op **[!UICONTROL Choose File]** en selecteer het bestand dat u wilt uploaden om het CSV-bestand te uploaden.

   - Klik op **[!UICONTROL Add to Cart]** .

   Als een van de producten aanvullende opties heeft, wordt de klant vanuit het winkelwagentje gevraagd om aandacht voor het product.

   ![&#x200B; Product vereist Aandacht &#x200B;](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Als er dubbele SKU&#39;s zijn, worden de hoeveelheden gecombineerd in één artikel in het winkelwagentje. De klant kan het aantal van elk item wijzigen en op **[!UICONTROL Update Shopping Cart]** klikken om de totalen opnieuw te berekenen.

