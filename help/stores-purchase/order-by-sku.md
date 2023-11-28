---
title: Bestelling door SKU
description: Leer hoe te om uw opslag te vormen om het opdracht geven door SKU als gemak voor uw klanten te steunen.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Bestelling door SKU

{{ee-feature}}

Een &#39;SKU&#39; is een &#39;Stock Keeping Unit&#39;. SKU&#39;s helpen online verkopers over het algemeen de belangrijkste productkenmerken zoals grootte, kleur, prijs, en materiaal te identificeren. Product-id&#39;s verschillen van SKU&#39;s:

- De `Product ID` is opeenvolgende reeksen van aantallen die intern worden gebruikt om producten te identificeren en niet beschikbaar aan klanten zijn.
- De `SKU` wordt gegenereerd door de verkoper, gewoonlijk op basis van de productnaam en de kenmerken voor marketing of interne tracking. Bijvoorbeeld: een blauw, T-shirt voor de katoenproductie, formaatmedium: T-COT-MED-BL. Indien nodig kan de verkoper de SKU wijzigen.

Normaal gesproken bevat een SKU een reeks afkortingen die de onderscheidende kenmerken van het product aangeven. De maximale SKU-lengte is 64 tekens. SKUs is belangrijk om inventaris effectief te volgen en te beheren, zodat is het correct opzetten van hen voor e-handel kritiek.

_Bestelling door SKU_ is een [widget](../content-design/widgets.md) die in de winkel als gebruiksgemak voor alle kopers kunnen worden weergegeven, of die alleen aan de kopers in specifieke klantengroepen ter beschikking kunnen worden gesteld. Klanten kunnen de SKU- en kwantitatieve gegevens rechtstreeks in de Order invoeren per SKU-blok of een CSV-bestand uploaden vanaf hun klantenaccount. Ongeacht de configuratie, is de orde door SKU altijd beschikbaar om beheerders op te slaan.

![Bestel door SKU in de Storefront](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Volgorde door SKU configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster de **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Order by SKU Settings]** sectie.

1. Set **[!UICONTROL Enable Order by SKU on my Account in Storefront]** op een van de volgende wijzen:

   - `Yes, for Everyone` - De Orde door het blok van SKU is beschikbaar in de opslag voor elke verkoopster.
   - `Yes, for Specified Customer Groups` - De orde door SKU is beschikbaar slechts aan leden van een specifieke klantengroep, zoals `Wholesale`.
   - `No` - Het blok van de Orde door SKU verschijnt niet in de opslagruimte, en de Orde door de pagina van SKU is niet beschikbaar in de klantenrekening.

   ![Bestellen op SKU-instellingen](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

![B2B voor Adobe Commerce](../assets/b2b.svg) (Alleen B2B voor Adobe Commerce) _**Als u de functie Order by SKU wilt inschakelen, schakelt u de functie Snelle volgorde uit:**_

1. Ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL B2B Features]**

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL B2B Features]** sectie.

1. Set **[!UICONTROL Enable Quick Order]** tot `No`.

   De [Functie Snelle bestelling](../b2b/quick-order.md) kunnen klanten en gasten snel bestellingen plaatsen op basis van SKU of productnaam.

## Storefront-ervaring

Wanneer de functionaliteit voor de opslag wordt gevormd, kunnen de klanten tot door SKU van om het even welke pagina opdracht geven die omvat _Bestelling door SKU_ widget of hun accountdashboard.

### Volgorde door SKU van paginaslok

1. In de _Bestelling door SKU_ blok, gaat de klant binnen **[!UICONTROL SKU]** en **[!UICONTROL Qty]** van het te bestellen item.

1. Als u nog een item wilt toevoegen, klikt u op **[!UICONTROL Add Row]** en herhaal het proces.

1. Klikken **[!UICONTROL Add to Cart]**.

### Bestellen door SKU van een klantenaccount

1. Vanaf de storefront meldt de klant zich aan bij zijn account.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Order by SKU]**.

1. Hiermee voegt u afzonderlijke items toe op basis van voorkeur:

   _**Voegt elk punt door SKU toe:**_

   - Hiermee wordt het dialoogvenster **[!UICONTROL SKU]** en **[!UICONTROL Qty]** van het te bestellen item.

   - Klik op _Rij toevoegen_ ![Knop Plus](../assets/button-add-item.png) en herhaalt voor zoveel items als nodig is.

   - Klikken **[!UICONTROL Add to Cart]**.

   _**Uploadt een CSV-bestand met meerdere items:**_

   - Bereidt een [CSV-importgegevens](../systems/data-csv.md) (Door komma&#39;s gescheiden waarde) bestand met kolommen voor `SKU` en `Qty`.

   ![Te importeren SKU&#39;s](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Als u het CSV-bestand wilt uploaden, klikt u **[!UICONTROL Choose File]** en selecteer het bestand dat u wilt uploaden.

   - Klikken **[!UICONTROL Add to Cart]**.

   Als een van de producten aanvullende opties heeft, wordt de klant vanuit het winkelwagentje gevraagd om aandacht voor het product.

   ![Product vereist aandacht](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Als er dubbele SKU&#39;s zijn, worden de hoeveelheden gecombineerd in één artikel in het winkelwagentje. De klant kan het aantal van elk onderdeel wijzigen en op **[!UICONTROL Update Shopping Cart]** om de totalen opnieuw te berekenen.

