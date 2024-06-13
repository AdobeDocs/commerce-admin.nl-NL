---
title: Installeer de [!DNL Adobe Commerce B2B] extension
description: Leer hoe u de [!DNL Adobe Commerce B2B] metapakket.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installeer de [!DNL Adobe Commerce B2B] extension

de Adobe Commerce B2B-extensie, `magento/extension-b2b` is beschikbaar voor alle ondersteunde versies van Adobe Commerce. Het wordt geïnstalleerd na de installatie van Adobe Commerce.


## Vereisten

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), alle ondersteunde versies
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## Ondersteunde platforms

- Adobe Commerce over wolkeninfrastructuur (ECE)
- Adobe Commerce (EE)

## Installatiestappen

>[!BEGINSHADEBOX]

**Vereisten**

- Toegang tot [repo.magento.com](https://repo.magento.com/) de extensie downloaden. Voor sleutelgeneratie en het verkrijgen van de nodige rechten, zie [Uw verificatietoetsen ophalen](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Sla verificatietoetsen voor de installatie op door deze globaal in uw [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Of sla ze op in een [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) in de hoofdmap van de Adobe Commerce-toepassing.

- [Ondersteunde versie van de B2B-extensie](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)- Bepaal de meest recente versie van de B2B uitbreiding die op de opgestelde versie van Adobe Commerce wordt gesteund.

- Raadpleeg de opmerkingen bij de release voor de meest recente informatie over versiecompatibiliteit, updates of wijzigingen die van invloed kunnen zijn op de installatie- of upgradevereisten.

   - [Opmerkingen bij de release B2B](release-notes.md)
   - [Opmerkingen bij de release van Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

De B2B-extensie installeren (`magento/b2b-extension`) met Composer. De extensie is een componentmetapakket dat de verzameling modules bevat die de B2B-mogelijkheden voor een Adobe Commerce-instantie inschakelen. Voor een lijst van inbegrepen modules, zie [B2B-pakketten](packages.md).

>[!BEGINTABS]

>[!TAB Cloud-infrastructuur]

>[!TIP]
>
>Wanneer u Adobe Commerce B2B installeert op cloudinfrastructuur, wordt u aangeraden uw Adobe Commerce-toepassing vóór het begin te implementeren in een integratie- of staging-omgeving.

De Adobe adviseert werkend in een ontwikkelingstak wanneer het toevoegen van de B2B uitbreiding aan uw project. Als u geen vertakking hebt, zie [Een vertakking maken voor ontwikkeling](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Bij de installatie van de B2B-extensie `Magento_B2b` de extensienaam wordt automatisch ingevoegd in het dialoogvenster `app/etc/config.php` bestand. U hoeft het bestand niet rechtstreeks te bewerken.

**De B2B-extensie installeren**:

1. Wijzig op uw lokale werkstation de projectmap.

1. Maak of check een ontwikkelingsvertakking uit.

1. Voeg de B2B-extensie toe aan de `require` van de `composer.json` bestand.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Werk de projectgebiedsdelen bij.

   ```bash
   composer update
   ```

1. Wijzigingen in code toevoegen, vastleggen en doorvoeren.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >Door updates naar de cloudomgeving te verscherpen, wordt het Commerce-implementatieproces voor de cloud gestart om de wijzigingen toe te passen. Controleer de implementatiestatus via de [logboek implementeren](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Als u plaatsingsfouten ontmoet, zie [Herstellen van componentfout](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Nadat de build en implementatie is voltooid, gebruikt u SSH om u aan te melden bij de externe omgeving en controleert u of de B2B-extensie is geïnstalleerd en ingeschakeld.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   De extensienaam gebruikt de indeling: `<VendorName>_<ComponentName>`.

   Monsterrespons:

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB In de bedrijfsruimten]

1. Werk vanuit de hoofdmap van de Adobe Commerce-toepassing de `composer.json` om de gebiedsdelen voor de B2B uitbreiding toe te voegen:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Als er bijvoorbeeld een fout optreedt:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Controleer de spelling van het pakket, de versiebeperking en of het pakket beschikbaar is en voldoet aan de minimale (stabiele) stabiliteitseis.

1. Voer desgevraagd uw [verificatietoetsen](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

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

>[!ENDTABS]

Nadat u de installatie hebt voltooid, configureert u de berichten en start u deze.

## Berichtconsumenten

De Adobe Commerce B2B-extensie gebruikt MySQL voor het beheer van de wachtrij met berichten. De volgende lijst maakt een lijst van de berichtconsumenten die B2B mogelijkheden steunen. Nadat u de extensie hebt geïnstalleerd, start u het bericht dat consumenten krijgen voor de B2B-mogelijkheden die vereist zijn voor uw Commerce-winkel.

| Consumenten | Beschrijving |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Hiermee werkt u de prijs voor elk product in een gedeelde catalogus bij. Vereist wanneer de [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `sharedCatalogUpdateCategoryPermissions` | Hiermee werkt u categorieën bij die zijn toegewezen aan een gedeelde cataloguscategorie. Vereist wanneer de [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `negotiableQuotePriceUpdate` | Prijzen voor verhandelbare koersen worden bijgewerkt. Vereist wanneer de [**[!UICONTROL Quotes]**](quotes.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `purchaseorder.toorder` | Hiermee converteert u een inkooporder naar bestelling. Vereist wanneer de [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `purchaseorder.transactional.email` | E-mails met inkoopordergegevens verzenden. Vereist wanneer de [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `purchaseorder.validation` | Valideert kooporder op basis van relevante [goedkeuringsregels](account-dashboard-approval-rules.md). Vereist wanneer de [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `quoteItemCleaner` | Hiermee verwijdert u ongeldige of inactieve prijsaanhalingstekens wanneer een product uit de catalogus wordt verwijderd of uit het winkelwagentje wordt verwijderd. Vereist wanneer de [**[!UICONTROL Quotes]**](quotes.md) Deze optie is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `inventoryQtyCounter` | Corrigeert asynchroon de aandelenindex nadat een bestelling is geplaatst of een product is verwijderd. Vereist wanneer de [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) is ingeschakeld voor Inventory management in de configuratie-instellingen voor Admin. Zie [Aanbevolen werkwijzen voor prestaties](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Hiermee maakt u berichten voor elke afzonderlijke taak van een [bulkbewerking](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) zoals het importeren of exporteren van producten, het massaal wijzigen van de prijzen en het toewijzen van producten aan een pakhuis. Vereist wanneer de [**Bulkbewerkingen voor beheerders**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) optie voor [!DNL Inventory Management] is ingesteld op **asynchroon uitvoeren** in de configuratie-instellingen voor het beheersysteem. |

{style="table-layout:auto"}

>[!NOTE]
>
>Voor een lijst van alle Adobe Commerce-berichtgebruikers raadpleegt u [Gebruikers in de wachtrij met berichten](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) in de _Configuratiegids_.

### Berichtconsumenten configureren

Voorkom mogelijke verwerkingsproblemen of vertragingen door de volgende parameters toe te voegen wanneer u [de boodschap van de consument beginnen](#start-message-consumers) voor B2B-mogelijkheden.

- `--max-messages <value>`— Geeft het maximum aantal berichten aan dat elke consument moet verwerken voordat deze wordt beëindigd (standaard = 10000). Hoewel de Adobe het niet adviseert, kunt u 0 gebruiken om de consument te verhinderen te eindigen. De beste manier voor een PHP-toepassing is om langlopende processen opnieuw te starten om mogelijke geheugenlekken te voorkomen.

- `--batch-size <value>`— Hiermee kunt u de systeembronnen beperken die door de consument worden verbruikt (CPU, geheugen). Het gebruik van kleinere batches verlaagt het gebruik van bronnen en leidt dus tot een langzamere verwerking.  Indien opgegeven, worden berichten in een wachtrij in batches geconsumeerd `<value>` elk. Deze optie is alleen van toepassing op de batchconsument. Indien `--batch-size` niet wordt bepaald, ontvangt de partijconsument alle beschikbare berichten in een rij.

Voor informatie over extra configuratieopties, zie [Specifieke configuratie](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

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

Zie voor meer informatie [Berichtenrijen beheren](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) in de _Configuratiegids_.

### Berichtconsumenten toevoegen aan uitsnijden

U kunt het runtime-programma voor de `SharedCatalogUpdateCategoryPermissions` en `SharedCatalogUpdatePrice` berichtconsumenten door de planning aan het dossier van de cron- configuratie toe te voegen [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

U kunt programma&#39;s voor berichtconsumenten van ook vormen [Configuratie-instellingen opslaan](../systems/cron.md) in de Admin.

## B2B-functies inschakelen in Admin

Na het installeren van de Adobe Commerce B2B-extensie en het starten van berichtgebruikers moet u ook [B2B-functies inschakelen in de beheerder](enable-basic-features.md).

