---
title: Installeer de [!DNL Adobe Commerce B2B] extension
description: Leer hoe u de [!DNL Adobe Commerce B2B] metapakket.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Installeer de [!DNL Adobe Commerce B2B] extension

De Adobe Commerce B2B-extensie is alleen beschikbaar voor Adobe Commerce v2.2.0 of hoger. Het wordt geïnstalleerd na de installatie van Adobe Commerce.

Installeer de meest recente versie van de B2B-extensie die wordt ondersteund door de geïmplementeerde Adobe Commerce-versie.

>[!NOTE]
>
>Deze installatie-instructies zijn van toepassing op Adobe Commerce dat op locaties wordt geïmplementeerd. Als u de B2B-extensie wilt installeren voor Commerce-projecten die worden geïmplementeerd op een cloudinfrastructuur, raadpleegt u de [Commerce Cloud-infrastructuurgids](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Vereisten

- Adobe Commerce versie 2.3.x of hoger
- [Ondersteunde versie van de B2B-extensie](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Geldig [verificatietoetsen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) om Adobe Commerce-extensies te downloaden.

  Sla verificatietoetsen voor de installatie op door deze globaal in uw [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Of sla ze op in een [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) in de hoofdmap van de Adobe Commerce-toepassing.

Voordat u de B2B-extensie installeert of bijwerkt, raadpleegt u de opmerkingen bij de release voor de meest recente informatie over versiecompatibiliteit, updates of wijzigingen die van invloed kunnen zijn op de installatie- of upgradevereisten.

- [Opmerkingen bij de release B2B](release-notes.md)
- [Opmerkingen bij de release van Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Installatiestappen

1. Werk vanuit de hoofdmap van de Adobe Commerce-toepassing de `composer.json` om de gebiedsdelen voor de B2B uitbreiding toe te voegen:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Als er bijvoorbeeld een fout optreedt:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Controleer de spelling van het pakket, de versiebeperking en of het pakket beschikbaar is en voldoet aan de minimale (stabiele) stabiliteitseis.

1. Voer desgevraagd uw [verificatietoetsen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   Uw _openbare sleutel_ is uw gebruikersnaam; uw _persoonlijke sleutel_ is uw wachtwoord. Als u openbare en persoonlijke sleutels hebt opgeslagen in `auth.json`, wordt u niet gevraagd om te verifiëren.

1. Voer de volgende opdrachten uit nadat Composer de modules heeft bijgewerkt:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >In de productiemodus ontvangt u mogelijk een bericht aan `Please rerun Magento compile command`. Voer de opdrachten in om de installatie te voltooien. Adobe Commerce vraagt u niet om de opdracht -compile uit te voeren in de modus Developer.

Nadat de installatie is voltooid, configureert en start u de berichtgebruikers, waaronder [parameters specificeren voor berichtconsumenten](#configure-message-consumers).

## Berichtconsumenten

De Adobe Commerce B2B-extensie gebruikt MySQL voor het beheer van de wachtrij met berichten. De volgende lijst maakt een lijst van de berichtconsumenten die B2B mogelijkheden steunen. Nadat u de extensie hebt geïnstalleerd, start u het bericht dat consumenten krijgen voor de B2B-mogelijkheden die vereist zijn voor uw Commerce-winkel.

| Consumenten | Beschrijving |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Hiermee werkt u de prijs bij voor elk product in een gedeelde catalogus. Vereist wanneer de [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `sharedCatalogUpdateCategoryPermissions` | Hiermee werkt u categorieën bij die zijn toegewezen aan een gedeelde cataloguscategorie. Vereist wanneer de [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `negotiableQuotePriceUpdate` | Prijzen voor verhandelbare koersen worden bijgewerkt. Vereist wanneer de [**[!UICONTROL Quotes]**](quotes.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `purchaseorder.toorder` | Hiermee converteert u een inkooporder naar bestelling. Vereist wanneer de [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `purchaseorder.transactional.email` | E-mails met inkoopordergegevens verzenden. Vereist wanneer de [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `purchaseorder.validation` | Valideert kooporder op basis van relevante [goedkeuringsregels](account-dashboard-approval-rules.md). Vereist wanneer de [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `quoteItemCleaner` | Hiermee verwijdert u ongeldige of inactieve prijsaanhalingstekens wanneer een product uit de catalogus wordt verwijderd of uit het winkelwagentje wordt verwijderd. Vereist wanneer de [**[!UICONTROL Quotes]**](quotes.md) Deze optie is ingeschakeld in de configuratie-instellingen van het beheersysteem. |
| `inventoryQtyCounter` | Corrigeert asynchroon de aandelenindex nadat een bestelling is geplaatst of een product is verwijderd. Vereist wanneer de [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) is ingeschakeld voor Inventory management in de configuratie-instellingen voor Admin. Zie [Aanbevolen werkwijzen voor prestaties](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Hiermee maakt u berichten voor elke afzonderlijke taak van een [bulkbewerking](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), zoals het importeren of exporteren van producten, het massaal wijzigen van de prijzen en het toewijzen van producten aan een pakhuis. Vereist wanneer de [**Bulkbewerkingen voor beheerders**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) optie voor [!DNL Inventory Management] is ingesteld op **asynchroon uitvoeren** in de configuratie-instellingen van het beheersysteem. |

{style="table-layout:auto"}

>[!NOTE]
>
>Voor een lijst van alle Adobe Commerce-berichtgebruikers raadpleegt u [Gebruikers in de wachtrij met berichten](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) in de _Configuratiegids_.

### Berichtconsumenten configureren

Voorkom mogelijke verwerkingsproblemen of vertragingen door de volgende parameters toe te voegen wanneer u [de boodschap van de consument beginnen](#start-message-consumers) voor B2B-mogelijkheden.

- `--max-messages <value>`— Geeft het maximum aantal berichten aan dat elke consument moet verwerken voordat deze wordt beëindigd (standaard = 10000). Hoewel wij het niet adviseren, kunt u 0 gebruiken om de consument te verhinderen te eindigen. De beste manier voor een PHP-toepassing is om langlopende processen opnieuw te starten om mogelijke geheugenlekken te voorkomen.

- `--batch-size <value>`— Hiermee kunt u de systeembronnen beperken die door de consument worden verbruikt (CPU, geheugen). Het gebruik van kleinere batches verlaagt het gebruik van bronnen en leidt dus tot een langzamere verwerking.  Indien opgegeven, worden berichten in een wachtrij in batches geconsumeerd `<value>` elk. Deze optie is alleen van toepassing op de batchconsument. Indien `--batch-size` niet wordt bepaald, ontvangt de partijconsument alle beschikbare berichten in een rij.

Voor informatie over extra configuratieopties, zie [Specifieke configuratie](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### Beginnen met bericht aan consumenten

Om asynchrone verrichtingen voor B2B mogelijkheden toe te laten, moet u veelvoudige berichtconsumenten beginnen.

1. Maak een lijst van de beschikbare berichtconsumenten:

   ```bash
   bin/magento queue:consumers:list
   ```

   De opdracht retourneert de beschikbare berichtconsumenten, inclusief alle [B2B-berichtconsumenten](#message-consumers).

1. Begin elke consument afzonderlijk:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Bijvoorbeeld:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Als u het bestand op de achtergrond wilt uitvoeren, voegt u `&` aan het bevel, terugkeer aan een herinnering, en verdere lopende bevelen. Bijvoorbeeld: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Zie voor meer informatie [Berichtenrijen beheren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in de _Configuratiegids_.

### Berichtconsumenten toevoegen aan uitsnijden

U hebt de optie om het runtimeprogramma voor de `SharedCatalogUpdateCategoryPermissions` en `SharedCatalogUpdatePrice` berichtconsumenten door de planning aan het dossier van de cron- configuratie toe te voegen [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

U kunt programma&#39;s voor berichtconsumenten van ook vormen [Configuratie-instellingen opslaan](../systems/cron.md) in de Admin.

## B2B-functies inschakelen in Admin

Na het installeren van de Adobe Commerce B2B-extensie en het starten van berichtgebruikers moet u ook [B2B-functies inschakelen in de beheerder](enable-basic-features.md).
