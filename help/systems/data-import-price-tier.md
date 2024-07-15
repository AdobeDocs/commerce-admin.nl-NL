---
title: Invoerprijzen
description: Leer hoe u prijsgegevens voor lagen kunt exporteren en bijgewerkte gegevens kunt importeren.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Invoerprijzen

Eerder dan het ingaan van [ laagprijzen ](../catalog/product-price-tier.md) manueel voor elk product, kan het efficiënter zijn om [ in te voeren ](data-import.md) de het tarief gegevens. Maak voordat u begint een voorbeeldbestand met geëxporteerde prijsgegevens voor lagen die u als sjabloon kunt gebruiken.

![ Voorbeeld storefront - tiered tarifering ](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Stap 1: Gegevens over de laagprijs exporteren

In het volgende voorbeeld worden prijsgegevens voor lagen voor één product geëxporteerd. Vervolgens kunt u de geëxporteerde gegevens gebruiken als een sjabloon voor het bulkimporteren van gegevens over de laagprijs. Meer over het uitvoeren van geavanceerde het tarief gegevens leren, zie [ Geavanceerde het tarief gegevens ](data-attributes-product.md#advanced-pricing-attributes).

![ product tiered tarifering ](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Stel onder _[!UICONTROL Export Settings]_de waarde **[!UICONTROL Entity Type]**in op `Advanced Pricing` .

1. Blader in het **[!UICONTROL Entity Attributes]** -raster omlaag naar de SKU-kenmerken en voer de volgende handelingen uit:

   - Voor laagprijzen die op een disconteringspercentage zijn gebaseerd, de SKU van elk uit te voeren product, die door een komma wordt gescheiden.

     ![ de uitvoer van Gegevens - product SKUs ](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Voer voor de op een vast bedrag gebaseerde prijzen de SKU van elk product in.

   - Schuif omlaag en klik op **[!UICONTROL Continue]** .

1. Zoek het exportbestand op de downloadlocatie voor uw webbrowser en open het bestand.

   ![ Voorbeeld - de uitgevoerde gegevens van de de rijprijs van de klantengroep ](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Uitgevoerde gegevens van de laagprijs_**

De volgende kolommen worden opgenomen in de geëxporteerde gegevens:

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

U gebruikt de geëxporteerde gegevens als een sjabloon voor het importeren van gegevens over de laagprijs.

## Stap 2: De gegevens bijwerken

1. Werk indien nodig de gegevens over de laagprijs voor elk product bij.

   Producten zonder update van de laagprijs kunnen uit het CSV-bestand worden verwijderd. Producten die niet zijn gewijzigd, hoeven niet opnieuw te worden geïmporteerd.

1. **[!UICONTROL Save]** het bijgewerkte CSV-bestand.

>[!NOTE]
>
>Een importbestand mag niet groter zijn dan 2 MB.

## Stap 3: De bijgewerkte gegevens importeren

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Onder _de Montages van de Invoer_, plaats **[!UICONTROL Entity Type]** aan `Advanced Pricing`.

1. Stel **[!UICONTROL Import Behavior]** in op `Add/Update` .

1. Klik onder **[!UICONTROL File to Import]** op **[!UICONTROL Choose File]** en selecteer het bestand dat u uit de map wilt importeren.

1. Klik in de rechterbovenhoek op **[!UICONTROL Check Data]** .

1. Klik op **[!UICONTROL Import]** als het bestand geldig is.

   Als dat niet het geval is, verhelpt u elk probleem met de gegevens in het bericht en probeert u het bestand opnieuw te importeren.
