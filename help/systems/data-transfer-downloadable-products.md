---
title: downloadbare producten importeren
description: Bekijk een voorbeeld van het importeren van productgegevens voor een downloadbaar product.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# downloadbare producten importeren

De stroom voor het invoeren van downloadbare producten is het zelfde als voor [&#x200B; de Producten van de Bundel &#x200B;](data-transfer-bundle-products.md) of [&#x200B; Configurable Producten &#x200B;](data-transfer-configurable-products.md). Het verschil is dat een downloadbaar product [&#x200B; downloadbare verbindingen &#x200B;](../catalog/product-create-downloadable.md) en [&#x200B; downloadbare steekproeven &#x200B;](../catalog/product-create-downloadable.md) met zijn beelden heeft.

De standaardhoofdmap voor downloadbare koppelingen en voorbeelden is `<Magento-root-folder>/pub/media/import` . Als de externe opslagmodule is ingeschakeld, is de standaardhoofdmap voor downloadbare koppelingen en voorbeelden de map `<remote-storage-root-folder>/media/import` .

Het CSV-bestand heeft aparte kolommen voor `downloadable_links` en `downloadable_samples` .

- **Downloadbare verbindingsbeelden** — In het volgende voorbeeld, zijn de downloadbare verbindingsbeelden (`red.jpg` en `black.jpg`) in de `<Magento-root-folder>/pub/media/import/test` omslag. Als externe opslag is ingeschakeld, bevinden deze afbeeldingen zich in de map `<remote-storage-root-folder>/media/import/test` .

  ![&#x200B; gegevens van het Voorbeeld - downloadbaar product met downloadbare verbindingen &#x200B;](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Downloadbare steekproefbeelden** - in het volgende voorbeeld, is het downloadbare steekproefbeeld (`white.jpg`) in de `<Magento-root-folder>/pub/media/import/test` omslag. Als externe opslag is ingeschakeld, bevindt deze afbeelding zich in de map `<remote-storage-root-folder>/media/import/test` .

  ![&#x200B; gegevens van het Voorbeeld - downloadbaar product met downloadbare steekproeven &#x200B;](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Voor meer informatie over het toelaten van en het beheren van de verre opslagmodule, zie [&#x200B; verre opslag &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=nl-NL) in de _gids van de Configuratie_ vormen.
