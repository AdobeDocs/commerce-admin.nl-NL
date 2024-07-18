---
title: Installeer de  [!DNL Adobe Commerce B2B]  uitbreiding
description: Leer hoe te om het  [!DNL Adobe Commerce B2B]  metapakket te installeren.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# De extensie [!DNL Adobe Commerce B2B] installeren

De Adobe Commerce B2B-extensie `magento/extension-b2b` is beschikbaar voor alle ondersteunde versies van Adobe Commerce. Het wordt geïnstalleerd na de installatie van Adobe Commerce.


## Vereisten

- [ Adobe Commerce ](https://business.adobe.com/products/magento/magento-commerce.html), alle gesteunde versies
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## Ondersteunde platforms

- Adobe Commerce over wolkeninfrastructuur (ECE)
- Adobe Commerce (EE)

## Installatiestappen

>[!BEGINSHADEBOX]

**Eerste vereisten**

- Toegang tot [ repo.magento.com ](https://repo.magento.com/) om de uitbreiding te downloaden. Voor zeer belangrijke generatie en het verkrijgen van de noodzakelijke rechten, zie [ uw authentificatiesleutels ](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) krijgen.

  Sparen authentificatiesleutels voor installatie door hen globaal in uw [ COMPOSER_HOME ](https://getcomposer.org/doc/03-cli.md#composer-home) folder te bepalen. Of, bewaar hen aan een {](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) dossier 0} auth.json in de folder van de de toepassingswortel van Adobe Commerce.[

- [ Gesteunde versie van de B2B uitbreiding ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) - bepaal de meest recente versie van de B2B uitbreiding die op de opgestelde versie van Adobe Commerce wordt gesteund.

- Raadpleeg de opmerkingen bij de release voor de meest recente informatie over versiecompatibiliteit, updates of wijzigingen die van invloed kunnen zijn op de installatie- of upgradevereisten.

   - [Opmerkingen bij de release B2B](release-notes.md)
   - [ de Nota&#39;s van de Versie van Adobe Commerce ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installeer de B2B-extensie (`magento/b2b-extension`) met behulp van Composer. De extensie is een componentmetapakket dat de verzameling modules bevat die de B2B-mogelijkheden voor een Adobe Commerce-instantie inschakelen. Voor een lijst van inbegrepen modules, zie [ B2B Pakketten ](packages.md).

>[!BEGINTABS]

>[!TAB  de infrastructuur van de Wolk ]

>[!TIP]
>
>Wanneer u Adobe Commerce B2B installeert op cloudinfrastructuur, wordt u aangeraden uw Adobe Commerce-toepassing vóór het begin te implementeren in een integratie- of staging-omgeving.

De Adobe adviseert werkend in een ontwikkelingstak wanneer het toevoegen van de B2B uitbreiding aan uw project. Als u geen tak hebt, zie [ een tak voor ontwikkeling ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) creëren. Wanneer u de B2B-extensie installeert, wordt de extensienaam `Magento_B2b` automatisch ingevoegd in het `app/etc/config.php` -bestand. U hoeft het bestand niet rechtstreeks te bewerken.

**om de B2B uitbreiding** te installeren:

1. Wijzig op uw lokale werkstation de projectmap.

1. Maak of check een ontwikkelingsvertakking uit.

1. Voeg de B2B-extensie toe aan de sectie `require` van het `composer.json` -bestand.

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
   >Door updates naar de cloudomgeving te verscherpen, wordt het Commerce-implementatieproces voor de cloud gestart om de wijzigingen toe te passen. Controleer de plaatsingsstatus van [ opstellen logboek ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Als u plaatsingsfouten ontmoet, zie [ Herstel van componentenmislukking ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Nadat de build en implementatie is voltooid, gebruikt u SSH om u aan te melden bij de externe omgeving en controleert u of de B2B-extensie is geïnstalleerd en ingeschakeld.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Een extensienaam gebruikt de indeling: `<VendorName>_<ComponentName>` .

   Monsterrespons:

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB  op-gebouw ]

1. Werk vanuit de hoofdmap van de Adobe Commerce-toepassing de `composer.json` bij om de afhankelijkheden voor de B2B-extensie toe te voegen:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Als er bijvoorbeeld een fout optreedt:

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Controleer de spelling van het pakket, de versiebeperking en of het pakket beschikbaar is en voldoet aan de minimale (stabiele) stabiliteitseis.

1. Indien ertoe aangezet, ga uw [ authentificatietoetsen ](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) in.

   Uw _openbare sleutel_ is uw gebruikersbenaming; uw _privé sleutel_ is uw wachtwoord. Als u de openbare en persoonlijke sleutels in `auth.json` hebt opgeslagen, wordt u niet gevraagd om u te verifiëren.

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
   >In de productiemodus ontvangt u mogelijk een bericht aan `Please rerun Magento compile command` . Voer de opdrachten in om de installatie te voltooien. Adobe Commerce vraagt u niet om de opdracht -compile uit te voeren in de modus Developer.

>[!ENDTABS]

Nadat u de installatie hebt voltooid, configureert u de berichten en start u deze.

## Berichtconsumenten

De Adobe Commerce B2B-extensie gebruikt MySQL voor het beheer van de wachtrij met berichten. De volgende lijst maakt een lijst van de berichtconsumenten die B2B mogelijkheden steunen. Nadat u de extensie hebt geïnstalleerd, start u het bericht dat consumenten krijgen voor de B2B-mogelijkheden die vereist zijn voor uw Commerce-winkel.

| Consumenten | Beschrijving |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Hiermee werkt u de prijs voor elk product in een gedeelde catalogus bij. Vereist wanneer de optie [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `sharedCatalogUpdateCategoryPermissions` | Hiermee werkt u categorieën bij die zijn toegewezen aan een gedeelde cataloguscategorie. Vereist wanneer de optie [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `negotiableQuotePriceUpdate` | Prijzen voor verhandelbare koersen worden bijgewerkt. Vereist wanneer de optie [**[!UICONTROL Quotes]**](quotes.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `purchaseorder.toorder` | Hiermee converteert u een inkooporder naar bestelling. Vereist wanneer de optie [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `purchaseorder.transactional.email` | E-mails met inkoopordergegevens verzenden. Vereist wanneer de optie [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `purchaseorder.validation` | Valideert kooporder tegen relevante [ goedkeuringsregels ](account-dashboard-approval-rules.md). Vereist wanneer de optie [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `quoteItemCleaner` | Hiermee verwijdert u ongeldige of inactieve prijsaanhalingstekens wanneer een product uit de catalogus wordt verwijderd of uit het winkelwagentje wordt verwijderd. Vereist wanneer de optie [**[!UICONTROL Quotes]**](quotes.md) is ingeschakeld in de configuratie-instellingen voor het beheersysteem. |
| `inventoryQtyCounter` | Corrigeert asynchroon de aandelenindex nadat een bestelling is geplaatst of een product is verwijderd. Vereist wanneer de optie [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) voor Inventory management is ingeschakeld in de configuratie-instellingen voor Admin. Zie [ Beste praktijken van Prestaties ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Creeert berichten voor elke individuele taak van a [ bulkverrichting ](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) zoals het invoeren van of het uitvoeren van punten, het veranderen van prijzen op een massaschaal, en het toewijzen van producten aan een pakhuis. Vereist wanneer de [**bulkverrichtingen Admin**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) optie voor [!DNL Inventory Management] aan **Looppas asynchroon** in de de configuratiemontages van het Systeem Admin wordt geplaatst. |

{style="table-layout:auto"}

>[!NOTE]
>
>Voor een lijst van alle het berichtconsumenten van Adobe Commerce, zie [ de rijconsumenten van het Bericht ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) in de _Gids van de Configuratie_.

### Berichtconsumenten configureren

Verhinder mogelijke verwerkingskwesties of vertragingen door de volgende parameters toe te voegen wanneer u [ de berichtconsumenten ](#start-message-consumers) voor B2B mogelijkheden begint.

- `--max-messages <value>`— Geeft het maximumaantal berichten op dat elke consument moet verwerken voordat deze wordt beëindigd (standaard = 10000). Hoewel de Adobe het niet adviseert, kunt u 0 gebruiken om de consument te verhinderen te eindigen. De beste manier voor een PHP-toepassing is om langlopende processen opnieuw te starten om mogelijke geheugenlekken te voorkomen.

- `--batch-size <value>`— Hiermee kunt u de systeembronnen beperken die door de consument worden verbruikt (CPU, geheugen). Het gebruik van kleinere batches verlaagt het gebruik van bronnen en leidt dus tot een langzamere verwerking.  Indien opgegeven, worden berichten in een wachtrij in batches van `<value>` elk gebruikt. Deze optie is alleen van toepassing op de batchconsument. Als `--batch-size` niet wordt bepaald, ontvangt de partijconsument alle beschikbare berichten in een rij.

Voor informatie over extra configuratieopties, zie [ specifiek-configuratie ](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Beginnen met bericht aan consumenten

Om asynchrone verrichtingen voor B2B mogelijkheden toe te laten, moet u veelvoudige berichtconsumenten beginnen.

1. Maak een lijst van de beschikbare berichtconsumenten:

   ```bash
   bin/magento queue:consumers:list
   ```

   Het bevel keert beschikbare berichtconsumenten met inbegrip van alle [ B2B berichtconsumenten ](#message-consumers) terug.

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
>Als u het bestand op de achtergrond wilt uitvoeren, voegt u `&` toe aan de opdracht, keert u terug naar een vraag en gaat u verder met het uitvoeren van opdrachten. Bijvoorbeeld: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &` .

Voor meer informatie, zie [ berichtrijen ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) in de _Gids van de Configuratie_ beheren.

### Berichtconsumenten toevoegen aan uitsnijden

U kunt het runtime programma voor `SharedCatalogUpdateCategoryPermissions` en `SharedCatalogUpdatePrice` berichtconsumenten automatiseren door het programma aan het dossier van de cron- configuratie [ toe te voegen /app/code/Magento/MessageQueue/etc/crontab.xml ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

U kunt programma&#39;s voor berichtconsumenten van de [ montages van de Configuratie van de Opslag ](../systems/cron.md) in Admin ook vormen.

## B2B-functies inschakelen in Admin

Na het installeren van de uitbreiding van Adobe Commerce B2B en het beginnen berichtconsumenten, moet u ook [ eigenschappen B2B in Admin ](enable-basic-features.md) toelaten.

