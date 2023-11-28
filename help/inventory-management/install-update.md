---
title: "Installeren, bijwerken en verwijderen [!DNL Inventory Management]"
description: Leer hoe u de [!DNL Inventory Management] metapakket.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Installeren, bijwerken en verwijderen [!DNL Inventory Management]

[!DNL Inventory Management] modules bieden alle inventariskenmerken en opties voor single- en multi-source-handelaren om producthoeveelheden en voorraden voor verkoopkanalen te beheren. Deze functies zijn beschikbaar in 2.4.x-versies van Adobe Commerce en Magento Open Source.

Deze functies en extensies zijn ontwikkeld als onderdeel van de [Voorraadproject](https://github.com/magento/inventory) via het Magento Open Source Community Engineering-programma.

[!DNL Inventory Management] installeert in 2.3.x en 2.4.x versies van Adobe Commerce en Magento Open Source, met alle eigenschappen die door gebrek worden toegelaten. Er zijn geen aanvullende stappen vereist voor het inschakelen van deze voorraadfuncties. Voor upgrades vanaf v2.1.x of 2.2.x zijn mogelijk extra stappen vereist. Zie [Upgrade uitvoeren voor Inventory management](#upgrade-inventory-management).

Installatie volgens [Snelle start van de installatie op locatie](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} wordt aanbevolen. Installeren met een pakket voor alle [!DNL Inventory Management] modules.

De volgende regel in de `composer.json` metapackage-installaties [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Voor een lijst met [!DNL Inventory Management] metapakketversies, zie [releaseopmerkingen](release-notes.md).

De [!DNL Inventory Management] het installatieproces voegt alle modules aan `<Magento_installation_directory>/app/etc/config.php` bestand. A `1` de waarde wijst erop dat de overeenkomstige module wordt toegelaten. De volgende lijst van modules wordt toegevoegd:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Inschakelen [!DNL Inventory Management] functies

Wanneer geïnstalleerd, bevorderd, of bijgewerkt, _[!UICONTROL Manage Stock]_in Beheer is standaard ingeschakeld. Met deze optie kunt u inventarisgegevens bijhouden en beheren, maar dit heeft geen invloed op de status van de module. Zie de volgende sectie om modules uit te schakelen.

Voor meer informatie over configuraties, zie [Inventory management configureren](configuration.md).

## Inventory management uitschakelen

>[!IMPORTANT]
>
>De standaardwaarde gebruiken [!DNL Inventory Management] wordt sterk aanbevolen. Het alternatief [!DNL CatalogInventory] , die wordt gebruikt voor systemen met een handicap [!DNL Inventory Management] modules, is nu verouderd. Het onbruikbaar maken van [!DNL Inventory Management] modules kunnen een instabiel systeem veroorzaken en tot verschillende problemen leiden.

U kunt desgewenst uitschakelen [!DNL Inventory Management] modules voor:

* Het upgradeproces versnellen voor handelaren die van 2.0.x, 2.1.x, 2.2.x, of 2.3.x naar 2.4.x migreren.
* Gebruik aangepaste of externe inventarisatie- en orderbeheersysteemmodules.

Zie de [Modules in- of uitschakelen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) pagina in de _Installatiehandleiding_ voor informatie over hoe u de toepasselijke modules onbruikbaar maakt.

Na voltooiing verschaft het systeem een lijst met modules en waarden in `<Magento_installation_directory>/app/etc/config.php`, beginnend met:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Als u de OMS Connector modules hebt geïnstalleerd, zorg ervoor dat u niet onbruikbaar maakt `Magento_InventoryMessageBus` module, die een schakelaarmodule is. Het is vereist om de Schakelaar met OMS te gebruiken.

## Inventory management verwijderen

>[!IMPORTANT]
>
>De standaardwaarde gebruiken [!DNL Inventory Management] wordt sterk aanbevolen. Het alternatief [!DNL CatalogInventory] die wordt gebruikt voor systemen met verwijderde [!DNL Inventory Management] modules, is nu verouderd. De [!DNL Inventory Management] modules kunnen een instabiel systeem veroorzaken en tot verschillende problemen leiden.

Als u ervoor kiest om de [!DNL Inventory Management] kunt u deze modules verwijderen (verwijderen). Als u alle modules wilt verwijderen via het composerbestand, voegt u het volgende toe aan `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

Wanneer deze wijziging is voltooid, voert u de installatie van de composer uit en verwijdert u deze Inventory management-modules automatisch.

## Upgrade uitvoeren voor Inventory management

### Vorige [!DNL Commerce] versies

Bij het upgraden of bijwerken van een bestaande 2.1.x-, 2.2.x- of 2.3.x-installatie naar Adobe Commerce of Magento Open Source 2.4.x, [!DNL Inventory Management] modules worden standaard uitgeschakeld. Deze standaardinstelling is een voorzorg om achterwaarts incompatibele upgrades te voorkomen en om Order Management (OMS) beter te ondersteunen.

>[!NOTE]
>
>Order Management biedt geen ondersteuning voor [!DNL Inventory Management]. Bij upgrade: [!DNL Inventory Management] modules zijn uitgeschakeld om OMS en [!DNL Commerce] 2.3.x voor een naadloze werking.


Inschakelen [!DNL Inventory Management] modules:

1. Bewerk de `<Commerce_installation_directory>/app/etc/config.php` bestand.
1. Alle inventarismodules wijzigen vanuit `0` tot `1` om in te schakelen.
1. De database bijwerken:

   ```bash
   bin/magento setup:upgrade
   ```

1. De cache reinigen:

   ```bash
   bin/magento cache:clean
   ```

Het wordt aanbevolen om de [inconsistenties in reserveringen, opdrachten](cli.md) na de upgrade. Wanneer u een upgrade uitvoert, worden al uw producten toegevoegd aan de standaardvoorraad. Als u bestellingen in behandeling hebt, werken de opdrachten het verkoopbare aantal en de reserveringen voor verkoop en bestelling correct bij.

### Vorige [!DNL Inventory Management] versies

Bij een upgrade van eerdere versies van [!DNL Inventory Management] tot de recentste versie, volg normale stappen van de uitbreidingsverbetering.

Werk voor de meest recente versie van het pakket de volgende wijzigingen bij:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Raadpleeg de volgende handleidingen voor meer informatie over de opwaarderingen van Commerce:

* [Handleiding voor bijwerken van handel](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Modules in- of uitschakelen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
