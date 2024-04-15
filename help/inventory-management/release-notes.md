---
title: '''[!DNL Inventory Management] opmerkingen vrijgeven'
description: Lees de opmerkingen bij de release voor meer informatie over alle [!DNL Inventory Management] lozingen.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] releaseopmerkingen

In deze releaseopmerkingen worden de releases van [!DNL Inventory Management] en omvatten:

![Nieuw](../assets/new.svg) Nieuwe functies
![Probleem opgelost](../assets/fix.svg) Oplossingen en verbeteringen
![Bekend probleem](../assets/bug.svg) Bekende problemen

[!DNL Inventory Management] is een speciaal project van de Techniek van de Gemeenschap van de Magento Open Source dat aan contribuanten open staat. Als u wilt deelnemen en bijdragen, raadpleegt u de [GitHub-project](https://github.com/magento/inventory) opslagplaats en [wiki](https://github.com/magento/inventory/wiki) aan de slag. Als u het project wilt bespreken, sluit u zich aan bij de [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) kanaal ([zelfinschrijving](https://opensource.magento.com/slack)).

[Releaseplanning](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} voor ondersteunde en compatibele releases.

## v1.2.7

[!DNL Inventory Management] 1.2.7 Opmerkingen bij de release zijn opgenomen in de [Opmerkingen bij de release core 2.4.7](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (moduleversie: `magento/inventory-metapackage = 1.2.6`) wordt ondersteund door versie 2.4.6 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) In de winkel worden nu samengestelde producten (configureerbaar, gebundeld en gebundeld) weergegeven als in voorraad wanneer onderliggende producten die waren verkocht, naar voorraad worden geretourneerd. Voorheen gaf de winkel aan dat het samengestelde product onder deze omstandigheden uit voorraad was. <!-- ACP2E-1106-->

![Probleem opgelost](../assets/fix.svg) Configureerbare productopties worden nu naar verwachting weergegeven als in voorraad in de winkel als de optie is gemaakt met hoeveelheid ingesteld op 0 en **[!UICONTROL Display out-of-stock products]** is ingeschakeld. <!-- ACP2E-1148-->

![Probleem opgelost](../assets/fix.svg) caches van categoriepagina&#39;s worden niet meer ongeldig gemaakt wanneer de voorraadhoeveelheid verandert en het product nog in voorraad is. Adobe Commerce laadt nu pagina&#39;s uit het cachegeheugen in plaats van deze opnieuw te genereren wanneer het aantal producten (en niets anders) op de pagina met winkelcategorieën verandert. <!-- ACP2E-118-->

![Probleem opgelost](../assets/fix.svg) Het aantal producten in de categorielijst is nu correct wanneer u Inventory in de modus Eén bron gebruikt met de **[!UICONTROL Display Out-Of-Stock Products]** instelling ingeschakeld. Adobe Commerce controleert nu of een product bij het tellen verkoopbaar is. <!-- ACP2E-1033-->

![Probleem opgelost](../assets/fix.svg) De regels voor winkelprijzen werken nu zoals verwacht wanneer Winkelvoorraad is ingeschakeld. Voorheen werden onder deze voorwaarden geen door de regels bepaalde kortingen op de kartprijs toegepast. <!-- ACP2E-1015-->

![Probleem opgelost](../assets/fix.svg) Wanneer u de productvoorraad bijwerkt in de geplande modus, worden niet meer alle cache gewist. Eerder, ontruimde de indexeerder van de Inventaris alle configuratiekaarten. <!-- ACP2E-1003-->

![Probleem opgelost](../assets/fix.svg) De waarde voor de **[!UICONTROL Allow Multiple Boxes for Shipping]** wordt het kenmerk voor een product in Geavanceerde voorraad nu opgeslagen zoals u had verwacht. <!-- ACP2E-992-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft nu een correcte reserveringscompensatie na een gedeeltelijke terugbetalingscreditnota voor een bestelling die bij het ophalen in de winkel is geplaatst. Eerder is een onjuiste reservering opgeslagen naar de `inventory_reservation` tabel wanneer een beheerder een creditnota heeft gemaakt zonder de **[!UICONTROL Return to Stock]** selectievakje. <!-- ACP2E-979-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft niet langer configureerbare producten weer als onvoorraad in de winkel wanneer een van de variaties handmatig is teruggebracht naar voorraad in implementaties die voorraden met meerdere bronnen implementeren. <!-- ACP2E-952-->

![Probleem opgelost](../assets/fix.svg) Kolompositie op het productraster (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) wordt niet meer teruggezet naar de vorige positie nadat de pagina opnieuw is geladen in implementaties waarbij meerdere inventarisbronnen zijn geconfigureerd. <!-- ACP2E-925-->

![Probleem opgelost](../assets/fix.svg) De voorraadhoeveelheid is nu correct nadat een creditnota voor een virtueel product wordt uitgegeven wanneer de **[!UICONTROL Back to stock]** selectievakje is niet ingeschakeld. <!-- ACP2E-908-->

![Probleem opgelost](../assets/fix.svg) U kunt nu categorieën opslaan met automatische productsortering en bereik die zijn toegewezen aan niet-standaardvoorraad. Eerder heeft Adobe Commerce de categorie niet opgeslagen en deze fout weergegeven: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Probleem opgelost](../assets/fix.svg) De configureerbare status van de productvoorraad wordt nu bijgewerkt zoals verwacht wanneer het product wordt gemaakt met alle configureerbare variaties die buiten de voorraad liggen. <!-- ACP2E-813-->

![Probleem opgelost](../assets/fix.svg) Het hulpprogramma voor het analyseren van inconsistentie bij reserveringen werkt nu correct met gedeeltelijk verzonden bestellingen die configureerbare, gebundelde en gegroepeerde producten bevatten. Samengestelde productsoorten worden nu geanalyseerd. Eerder werden annuleringen en terugbetalingen alleen opgeslagen voor bovenliggende producten, niet voor onderdelen van subproductorders van configureerbare en samengevoegde bundelproducten. <!-- ACP2E-924-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft niet langer een fout weer wanneer een beheerder probeert 200 of meer inventarisbronnen toe te wijzen aan een voorraad of product. <!-- ACP2E-1180-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce ondersteunt nu het maken van een creditnota voor een bestelling waarvan een product is verwijderd. Eerder konden handelaren geen creditnota maken toen producten uit de bestelling waren geschrapt nadat een factuur was opgesteld. Deze fout is in de toepassing weergegeven: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Probleem opgelost](../assets/fix.svg) Winkels worden nu gefilterd op basis van zowel één als meerdere winkel-id&#39;s. De `event` productkenmerkcode is toegevoegd aan de lijst met gereserveerde kenmerkcodes. In het rapport over de lage voorraad werd een uitzondering gemaakt toen de voorraadmodule werd geïnstalleerd. <!-- ACP2E-1017-->

![Probleem opgelost](../assets/fix.svg) Gelaagde navigatiefilters werken nu zoals verwacht, en producten uit de voorraad worden nu toegevoegd aan de productlijst van de winkelcategorie. De nieuwe `is_out_of_stock` sorteerkenmerk gebruikt de Elasticsearch dynamic field mapper voor de collectie van het storefront-product. <!-- ACP2E-748-->

![Probleem opgelost](../assets/fix.svg) De voorraadstatus van het samengestelde product (bundel, gegroepeerd en configureerbaar) wordt naar verwachting bijgewerkt wanneer de status van de onderliggende productvoorraad wordt gewijzigd door een REST `POST /rest/V1/inventory/source-items` vraag. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (moduleversie: `magento/inventory-metapackage = 1.2.5`) wordt ondersteund door versie 2.4.5 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) De standaardvoorraadstatus van bundel en gegroepeerde producten wordt nu bijgewerkt zoals verwacht wanneer een handelaar een zending maakt van de beheerder. Eerder bleef de status van deze producten ongewijzigd nadat een transport was gecreëerd. <!--- ACP2E-418-->

![Probleem opgelost](../assets/fix.svg) Configureerbare producten worden nu teruggestuurd naar de voorraad wanneer aan een van de volgende voorwaarden wordt voldaan: 1. Het bovenliggende product heeft ten minste één opgeslagen onderliggend item in voorraad. 2. Het configureerbare product zelf werd bijgewerkt en ingesteld als **in voorraad** en ten minste één kind in voorraad had. <!--- ACP2E-443-->

![Probleem opgelost](../assets/fix.svg) Wijzigingen in de voorraad die via de REST API zijn geïmplementeerd, worden nu weerspiegeld zoals verwacht op de pagina&#39;s met productdetails. De cache voor catalogusproducten wordt nu schoongemaakt nadat de laatste en de huidige voorraadstatus zijn vergeleken. Eerder, resulteerde het weglaten van de callback functie in de onjuiste evaluatie van voorraadstatusveranderingen, die niet de noodzakelijke geheim voorgeheugenschoonmaakbeurt teweegbrachten. Dientengevolge weerspiegelde de opslagront de inventariswijzigingen niet. <!--- ACP2E-161-->

![Probleem opgelost](../assets/fix.svg) Producten die zijn toegewezen aan standaardvoorraad en die voorheen niet meer in voorraad waren, zijn nu zichtbaar op de winkel nadat het bronitem is bijgewerkt met `/V1/inventory/source-items`. Eerder stelde dit REST API eindpunt het verkeerde in `stock_status`. <!--- ACP2E-562-->

![Probleem opgelost](../assets/fix.svg) De toewijzing van voorraadbronnen ongedaan maken via bulkactie (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) werkt nu zoals verwacht wanneer bronnen SKU&#39;s bevatten die duplicaten zijn, behalve een voorloopnul (bijvoorbeeld `01234` en `1234`). Eerder werden door de toepassing geen inventarisbronnen verwijderd en werd een fout gegenereerd. <!--- ACP2E-2641-->

![Probleem opgelost](../assets/fix.svg) De status van de productvoorraad is nu altijd **in voorraad** op de opslagplaats wanneer oneindige achterorden worden toegelaten en het product aan een douanevoorraad wordt toegewezen, ongeacht de hoeveelheid backordered. Eerder waren de producten uit voorraad, zelfs toen de back orders werden toegelaten. <!--- ACP2E-664-->

![Probleem opgelost](../assets/fix.svg) Configureerbare bovenliggende producten en onderliggende productbestanden worden nu correct bijgewerkt nadat het bronitem is bijgewerkt met `POST /V1/inventory/source-items`. Nadat het onderliggende product via de API is bijgewerkt, wordt een nieuwe voorraadinsteekmodule beschikbaar gesteld voor standaardvoorraadcontroles en updates voor configureerbare producthoeveelheid en status. <!--- ACP2E-442-->

![Probleem opgelost](../assets/fix.svg) Producten met groepen die buiten de voorraad vallen, worden niet meer vermeld op de pagina met winkelrubrieken. <!--- ACP2E-2082-->

![Probleem opgelost](../assets/fix.svg) De pakketnaam is gecorrigeerd `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Probleem opgelost](../assets/fix.svg) De status van de backorder wordt nu correct weergegeven in de Admin nadat een bestelling met een product van 0 hoeveelheid in een implementatie van meerdere bronnen/bestanden is geplaatst. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Probleem opgelost](../assets/fix.svg) De producten van de bundel uit de voorraad worden niet meer getoond op de pagina van de opslagcategorie wanneer het bundelproduct van de voorraadsectie wordt bijgewerkt. <!--- ACP2E-2012-->

![Probleem opgelost](../assets/fix.svg) Compatibiliteitsproblemen met PHP 7.4 zijn opgelost. <!--- AC-3192-->

![Probleem opgelost](../assets/fix.svg) De prestaties van opslagbewerkingen met bundelproducten die veel opties bevatten (meerdere 100), zijn verbeterd. Eerder duurde het opslaan van deze grote bundelproducten enkele minuten en soms leidde het tot vertragingen in implementaties met ingeschakelde inventarisservices. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Probleem opgelost](../assets/fix.svg) Het gereedschap voor bulkacties van het product (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) werkt nu zoals verwacht wanneer u een inventarisbron toewijst aan meerdere producten wanneer SKU&#39;s worden gedupliceerd, behalve een regelafstand `0` (bijvoorbeeld `01234` en `1234`). Eerder werd slechts één product een inventarisbron toegewezen. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Probleem opgelost](../assets/fix.svg) De `ProductInterface.only_x_left_in_stock` wordt nu 0 geretourneerd als de voorraad 0 is. Eerder werd null geretourneerd. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Probleem opgelost](../assets/fix.svg) U kunt de standaardvoorraad nu bewerken via de beheerder **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Eerder werd een JavaScript-fout weergegeven in de console toen u probeerde bronnen toe te voegen aan of te verwijderen uit de standaardvoorraad, hoewel u websites kon toewijzen aan de standaardvoorraad. <!--- ACP2E-545-->

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-274--> Het aantal producten in de categorielijst is nu correct wanneer u de modus Eén bron inventariseren gebruikt met de **[!UICONTROL Display Out-Of-Stock Products]** instelling ingeschakeld. Een nieuwe insteekmodule gebruikt nu `AreProductsSalableInterface` en `StockConfigurationInterface` het totale aantal producten te bepalen. Eerder heeft de lijst met producten van de categorie de verkeerde hoeveelheid product geretourneerd.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-322--> Configureerbare producten worden nu naar de laatste positie in de productlijst verplaatst nadat de voorraad is bijgewerkt wanneer de **[!UICONTROL Move out of stock to the bottom]** instelling is ingeschakeld. Er wordt een nieuwe aangepaste databasequery geïmplementeerd om de sorteervolgorde van de index van de Elasticsearch te negeren, waarbij de sorteervolgorde voor beheerders wordt genegeerd. Eerder, werden de configureerbare producten en hun kindproducten niet verplaatst naar de bodem van de lijst toen dit het plaatsen werd toegelaten.

## v1.2.4

Inventory management 1.2.4 (moduleversie: `magento/inventory-metapackage = 1.2.4`) wordt ondersteund door versie 2.4.4 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Commerce geeft nu een nauwkeurige waarde voor de verkoopbare hoeveelheid voor alle producten weer in de overzichtsweergave van het Admin-product. Eerder werd een lege waarde weergegeven voor de verkoopbare hoeveelheid producten in voorraad met SKU&#39;s die speciale tekens bevatten. <!--- MC-41936-->

![Probleem opgelost](../assets/fix.svg) De prestaties zijn verbeterd voor kart-en-controlemaatregelen zoals het toevoegen van producten aan het karretje in plaatsingen met vele (ongeveer 10.000) inventarisbronnen. <!--- MC-42570-->

![Probleem opgelost](../assets/fix.svg) De `bin/magento inventory:reservation:list-inconsistencies` bevel behandelt nu correct orden met gedeeltelijke verzendingen zelfs als de reserveringen van het gegevensbestand worden overgeslagen en het geheime voorgeheugen is ontruimd. Eerder, toen dit bevel met een vooraf ontruimde geheime voorgeheugen werd uitgevoerd, toonde Commerce de volgende fout: `Area code is not set`. <!--- MC-42142-->

![Probleem opgelost](../assets/fix.svg) Het incrementele indexeren van gegroepeerde onderliggende producten leidt er niet langer toe dat andere gegroepeerde producten onjuist worden geïndexeerd wanneer onderliggende producten worden gedeeld. <!--- MC-41963-->

![Probleem opgelost](../assets/fix.svg) Op de pagina met winkelrubrieken wordt nu het juiste aantal producten weergegeven nadat een product uit een categorie is verwijderd door de API. Eerder was het aantal producten op de categoriepagina onjuist tot opnieuw indexeren plaatsvond. <!--- MC-42287-->

![Probleem opgelost](../assets/fix.svg) De configureerbare producten kunnen nu aan voorraad worden teruggegeven wanneer het creëren van een creditnota wanneer **[!UICONTROL Manage Stock]** is uitgeschakeld. Eerder gaf Commerce de **Terug naar voorraad** Schakel het selectievakje op de pagina voor het maken van creditnota&#39;s in toen deze optie was uitgeschakeld. <!--- MC-42002-->

![Probleem opgelost](../assets/fix.svg) Het beheer van voorraden van meer dan 10.000 artikelen is verbeterd. Eerder waren handelaars vanwege prestatieproblemen soms niet in staat om voorraden te bewerken in Admin voordat ze hun website lanceerden. <!--- MC-42643-->

![Probleem opgelost](../assets/fix.svg) De **[!UICONTROL User Roles]** De pagina in Admin wordt bijgewerkt om beheerders van beperkte toestemmingen toegang tot de configuratie van de leveringsmethodes te verlenen. De _Verzendmethoden_ de naam van de sectie is gewijzigd in _[!UICONTROL Delivery methods]_, en_[!UICONTROL In-Store Pickup]_ wordt verplaatst onder de _[!UICONTROL Delivery methods]_sectie. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce maakt niet langer een dubbele productreservering nadat een creditmemo door de API is bijgewerkt. <!--- MC-41757-->

![Probleem opgelost](../assets/fix.svg) Schakelen van de _[!UICONTROL Pick up in Store]_aan de_[!UICONTROL Shipping]_ in de workflow voor uitchecken wordt niet langer een JavaScript-fout geactiveerd wanneer alleen In-Store Ophalen beschikbaar is. <!--- MC-42808-->

![Probleem opgelost](../assets/fix.svg) De hoeveelheid van het verkoopbare product en de hoeveelheid van het in voorraad zijnde product worden nu correct gesynchroniseerd. Eerder werd de compensatie voor de boeking van voorraden niet opnieuw gemaakt voor geannuleerde orders. <!--- MC-42485-->

![Probleem opgelost](../assets/fix.svg) De prestaties van de validator zijn geoptimaliseerd om te voorkomen dat er een nieuwe bron wordt toegevoegd aan het onderliggende product van een gebundeld product met een verzendtype `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (moduleversie: `magento/inventory-metapackage = 1.2.3`) wordt ondersteund door versie 2.4.3 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Oplossing voor verschillende problemen met betrekking tot de zichtbaarheid van het samengestelde product aan de voorzijde.

![Probleem opgelost](../assets/fix.svg) Verbeterde prestaties voor cart page management met de minimaal vereiste hoeveelheid.

![Probleem opgelost](../assets/fix.svg) Verschillende oplossingen zijn bedoeld om problemen op te lossen met het maken van bronnen, items uit de voorraad, voorraadsourcing, het sorteren van toegewezen bronnen, levering in de winkel en inventarisopdrachten.

![Probleem opgelost](../assets/fix.svg) [!DNL Commerce] ondersteunt nu Canadese postcodes van drie cijfers voor levering in de winkel. codes met zes cijfers worden niet ondersteund vanwege beperkingen die zijn ingesteld door `geonames.org`.

![Probleem opgelost](../assets/fix.svg) De beheerder geeft nu de juiste hoeveelheid standaardvoorraad voor uitgeschakelde producten weer op de knop **Producten** raster en de **Product bewerken** pagina voor multi-store plaatsingen.

![Probleem opgelost](../assets/fix.svg) [!DNL Commerce] verfrist nu het geheime voorgeheugen van het categorieproduct wanneer een bundelproduct terug in voorraad is.

## 1.2.

[!DNL Inventory Management] 1.2.2 (moduleversie: `magento/inventory-metapackage = 1.2.2`) wordt ondersteund door versie 2.4.2 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Oplossing voor verschillende problemen met betrekking tot de zichtbaarheid van het samengestelde product aan de voorzijde.

![Probleem opgelost](../assets/fix.svg) Verbeterde prestaties van winkelwagenpagina&#39;s tijdens het bijwerken van de hoeveelheid op B2B.

![Probleem opgelost](../assets/fix.svg) Verschillende oplossingen zijn bedoeld om problemen op te lossen met het ophalen in de winkel, massaupdates en inventarisdrempel.

![Nieuw](../assets/new.svg) **Functionele tests.** Er zijn nieuwe functionele tests ingevoerd en er zijn correcties voor bestaande tests ingevoerd om deze stabieler te maken.

## 1.

[!DNL Inventory Management] 1.2.1 (moduleversie: `magento/inventory-metapackage = 1.2.1`) wordt ondersteund door versie 2.4.1 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Onbekende probleem met betrekking tot de `inventory_cleanup_reservations` uitsnijden en een probleem verhelpen dat te maken heeft met de functie Ophalen in winkel voor bundelproducten. Deze update bevat ook algemene verbeteringen voor het berekenen van voorraden, ondersteuning voor gebundelde producten en backorder-functionaliteit.

![Nieuw](../assets/new.svg) **Functionele tests.** Introduceerde nieuwe functionele tests om extra dekking te bieden voor de functie voor ophaalservice in de In-Store.

## 1.2.0.

[!DNL Inventory Management] 1.2.0 (moduleversie: `magento/inventory-metapackage = 1.2.0`) wordt ondersteund door versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Veel oplossingen bieden oplossingen voor problemen met brontoewijzing, ondersteuning voor schaalbare omgevingsfuncties en compatibiliteit met PHP 7.4, MySQL 8 en PHPUNIT 9.

![Nieuw](../assets/new.svg) **In-store leveringsmethode.** Gebruikers hebben een optie toegevoegd waarmee ze een bron kunnen selecteren die tijdens het uitchecken moet worden gebruikt als ophaallocatie. Zie [Levering in de winkel](../stores-purchase/shipping-in-store-delivery.md) in de _Handleiding voor verkoop- en aankoopervaring_.

![Nieuw](../assets/new.svg) **Bundel productondersteuning voor de multibronmodus.** De inventaris steunt alle producttypes met veelvoudige bronnen.

![Nieuw](../assets/new.svg) **Asynchrone herindexering van voorraden.** De mogelijkheid toegevoegd om de voorraad asynchroon opnieuw te indexeren en de prestaties van verschillende kritieke scenario&#39;s te verbeteren.

![Nieuw](../assets/new.svg) **Bulkinterfaces.** Introduceerde nieuwe bulkinterfaces voor salability controle: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nieuw](../assets/new.svg) **Verhoogde testdekking.** De nieuwe functionaliteit wordt behandeld met geautomatiseerde tests, met inbegrip van uitgebreide dekking voor ontdekte en vaste kwesties.

![Bekend probleem](../assets/bug.svg) **Bekend probleem.** Het ontbreken van `object_id` in de metagegevens van reserveringen voorkomt `inventory_cleanup_reservations` snijtaak werkt niet goed. Deze kwestie is geïntroduceerd in [magento/voorraad#3046](https://github.com/magento/inventory/pull/3046).

**Oplossing:** Voer de volgende vragen MySQL uit om reserveringen manueel schoon te maken:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6.

[!DNL Inventory Management] 1.1.6 (moduleversie: `inventory-composer-metapackage = 1.1.6`) wordt ondersteund door versie 2.3.6 en compatibel met versie 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Oplossingen voor problemen met betrekking tot achterordes, kredietmemo&#39;s, het lage raster voor aandelenrapporten, correcties in verband met het CLI-hulpmiddel &quot;inconsistenties oplossen&quot; en algemene verbeteringen.

![Nieuw](../assets/new.svg) **Asynchrone herindexering van voorraden.** De mogelijkheid toegevoegd om de voorraad asynchroon opnieuw te indexeren en de prestaties van verschillende kritieke scenario&#39;s te verbeteren.

## 1.1.5.

[!DNL Inventory Management] 1.1.5 (moduleversie: `inventory-composer-metapackage = 1.1.5`) wordt ondersteund door versie 2.3.5 en compatibel met versie 2.3.4, 2.3.3, 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Nieuw](../assets/new.svg) **De voorraad bijwerken zodra de SKU van het product is gewijzigd.** Introduceerde een nieuwe configuratie die plaatst om op het nieuwe gedrag over te schakelen: &quot;synchroniseren met Catalogus&quot;.

![Nieuw](../assets/new.svg) **Functionele tests.** Nieuwe functionele tests geïntroduceerd om de leemte in de testdekking te elimineren. Verschillende problemen verholpen om tests stabieler en betrouwbaarder te maken).

![Bekend probleem](../assets/bug.svg) Oplossingen om oververkoop van producten te voorkomen, zichtbaarheid van producten uit de &quot;out of stock&quot; op de winkel, talrijke oplossingen voor schaalbare milieubescherming en verbeteringen in de gebruikersinterface.

## 1.1.4.

[!DNL Inventory Management] 1.1.4 (moduleversie: `inventory-composer-metapackage = 1.1.4`) wordt ondersteund door versie 2.3.4 en compatibel met versie 2.3.3, 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost ](../assets/fix.svg)**Verbeterde prestaties.** Introduceerde bunching logica voor het bevel van de Reserve CLI van de Inventaris om geheugengebruik te verminderen en gevallen te vermijden wanneer het proces zonder enige reactie wordt geplakt.

![Nieuw ](../assets/new.svg)**Verhoogde testdekking.** Introduceerde veel nieuwe functionele tests. Bijna alle scenario&#39;s met handmatige inventarisatie worden behandeld met geautomatiseerde tests.

![Bekend probleem](../assets/bug.svg) Veel oplossingen zijn bedoeld om problemen op te lossen met kredietmemo&#39;s, gegroepeerde producten en massale acties voor bronnen en voorraden.

## 1.1.3.

[!DNL Inventory Management] 1.1.3 (moduleversie: `inventory-composer-metapackage = 1.1.3`) wordt ondersteund door versie 2.3.3 en compatibel met versie 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de codebasis van de Magento Open Source.

![Probleem opgelost ](../assets/fix.svg)**Betere integratie met Adobe Commerce- en B2B-functies.** [!DNL Inventory Management] werkt nu correct met de volgende functies voor websites die niet-standaard inventarisbronnen en -voorraden gebruiken:

- Bestelling door SKU (Adobe Commerce)
- Snelle volgorde (B2B)
- Aanvraaglijsten (B2B)

![Nieuw ](../assets/new.svg)**Verbeterde prestaties.** Browserprestaties van de Storefront-catalogus worden verbeterd voor websites waarop de standaardvoorraad en -bron worden uitgevoerd.

![Nieuw ](../assets/new.svg)**Verhoogde testdekking.** De geautomatiseerde testdekking voor functionaliteit en integratie is aanzienlijk toegenomen.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (moduleversie: `inventory-composer-metapackage = 1.1.2`) wordt ondersteund door versie 2.3.2 en compatibel met versie 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![Probleem opgelost](../assets/fix.svg) Toegevoegd `source_code` op het antwoord van de GET `/V1/shipments` REST-eindpunt. <!-- https://github.com/magento/inventory/pull/2142 -->

![Probleem opgelost](../assets/fix.svg) Correctie van het probleem met betrekking tot reserveringen en het bijwerken van de producthoeveelheden na de afgifte van een creditnota voor een niet-verscheepte order. Wanneer u de optie selecteert om <!-- https://github.com/magento/inventory/pull/2179 -->

![Probleem opgelost](../assets/fix.svg) Probleem opgelost waarbij de hoeveelheid voor configureerbare onderliggende producten correct wordt opgeslagen wanneer tijdens het maken van het product hoeveelheden worden ingevoerd. <!-- https://github.com/magento/inventory/pull/2158 -->

Nieuwe modules voor [!DNL Inventory Management] 1.1.2 Beta omvat:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nieuw](../assets/new.svg) **Een Bulk Partial Stock Transfer Endpoint toegevoegd** - Met de huidige eindpunten voor bulkoverdracht wordt alle toegewezen hoeveelheid van een oorsprong naar een doelbron verplaatst. De nieuwe `/rest/V1/inventory/bulk-partial-source-transfer` het eindpunt staat verkopers toe om gedeeltelijk materiaal van bron aan bron als bulkverrichting over te brengen. Als u een bepaalde hoeveelheid wilt overdragen, voert u een verzoek in bij het eindpunt met de optie `sku`, `qty`, `origin_source_code`, en `destination_source_code`. De overdrachten verifiëren dat de bron aan wordt toegewezen `sku`Er is voldoende hoeveelheid om over te dragen, enzovoort. Zie [Massa van de inventaris](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} in de REST API-documentatie. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nieuw](../assets/new.svg) **Toegevoegde reserve CLI** - Met nieuwe opdrachten kunt u inconsistenties in de reserveringen opsporen en oplossen. Als orders worden verzonden en de status worden gewijzigd, [!DNL Inventory Management] geeft aanleiding tot initiële voorbehouden en actualiseringen door middel van compensatievoorbehouden. Deze bevelen keren een lijst van ontdekte inconsistenties door identiteitskaart van de Orde, SKU, en identiteitskaart van het Beeld terug en creeer reserveringen om op te lossen. Zie de [CLI-verwijzing](cli.md) voor meer informatie . <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nieuw](../assets/new.svg) **Prestatieverbeteringen voor bronnen en SSA-opties** - Sorteren en selecteren van bronnen tijdens de verzending heeft geleid tot een verslechtering van de prestaties van voorraden met een groot aantal bronnen. Deze release biedt aanzienlijke prestatieverbeteringen voor het weergeven en sorteren van beschikbare bronnen bij het controleren en selecteren van SSA-opties in verzendingen. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nieuw](../assets/new.svg) **Extra GraphQL-ondersteuning voor Inventory management** - Deze release installeert een nieuwe `magento/module-inventory-graph-ql` -module. De GraphQL [ProductInterface-kenmerken](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} bevat nu de `only_x_left_in_stock` en `stock_status` kenmerken voor [!DNL Inventory Management] ondersteuning. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nieuw](../assets/new.svg) **Vereenvoudigde interface voor toegewezen bronnen** - De lijst Toegewezen Bronnen in productpagina&#39;s heeft vereenvoudigde inhoud voor gemakkelijkere updates en verhoogde prestaties wanneer het tonen van vele bronnen. Alle bronnen worden weergegeven op bronnaam (houd de muisaanwijzer boven de bronnaam `source_code`).

![Nieuw](../assets/new.svg) **Export Aggregated Stock Service** - Deze release biedt een nieuwe service voor geaggregeerde exportbestanden (met behoud van reserveringen in het systeem) ter ondersteuning van externe Sales Channel, zoals Amazon, eBay en Google-winkeladvertenties.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0.

[!DNL Inventory Management] 1.1.0 (moduleversie: `inventory-composer-metapackage = 1.1.0`) wordt ondersteund en is compatibel met versie 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code. [!DNL Inventory Management] 1.1.1 wordt alleen vrijgegeven als een pakketnaamupdate, ondersteund voor versie 2.3.1 en compatibel met versie 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source-code.

![Probleem opgelost](../assets/fix.svg) **Toegevoegde ondersteuning voor Elasticsearch voor modi met één en meerdere bronnen** — U kunt nu Elasticsearch configureren en gebruiken met aangepaste bestanden. Zie [Service Elasticsearch instellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} voor installatiegegevens. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Probleem opgelost](../assets/fix.svg) Oplossing voor prestatieproblemen met Default Stock om de prestaties met tal van bewerkingen drastisch te verbeteren. De verbeteringen verhogen prestaties voor single-source wijze, de Inventaris van de Overdracht aan Bron, de pagina&#39;s van de Categorie van de Storefront, en de berekeningen van de Hoeveelheid van de Verkoop.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Probleem opgelost](../assets/fix.svg) Opgeloste problemen met de status Out of Stock en bulkinventarisoverdracht naar Stock voor configureerbare en gegroepeerde producten. Het selecteren van de bovenliggende producten en het uitvoeren van acties in bulk heeft geen invloed op de productstatus. Als het moederproduct in voorraad was, blijft het in voorraad.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nieuw](../assets/new.svg) **Algoritme voor afstandprioriteit** — Het algoritme van de Prioriteit van de Afstand is een nieuw, uit-van-de-doos Algorithm Bron van de Selectie voor op afstand-gebaseerde het verschepen aanbevelingen. Dit algoritme vergelijkt de plaats van het verzendende bestemmingsadres met bronplaatsen om de dichtstbijzijnde bron te bepalen om verzendingen te vervullen. De afstand kan worden bepaald door fysieke afstand of door de tijd die is besteed aan het reizen van de ene naar de andere locatie, met behulp van geïmporteerde geocode-locatiegegevens of Google-richtingen (rijden, lopen of fietsen).

![Nieuw](../assets/new.svg) **Uitgebreide lijst met bronaantallen** — Handelaars met een groot aantal bronnen kunnen gemakkelijk alle bronnen per product via het productraster aanwijzen en bekijken. Elk product bevat minimaal vijf bronnen en overeenkomende hoeveelheden. Wanneer u de muis boven de bronnen houdt, kunt u door de volledige lijst met bronnen en huidige hoeveelheden bladeren.

![Bekend probleem](../assets/bug.svg) Bekende kwestie met Magento Open Source en Adobe Commerce v2.3.1 - Asynchrone migratie van gegevens tussen bronnen ontmoet kwesties toe te schrijven aan veranderingen in Asynchrone APIs met onderwerpnamen die PHP klasse en methodenamen weerspiegelen. Synchrone bewerkingen gebruiken, instellen **[!UICONTROL Run asynchronously]** tot `No`, wordt aanbevolen.
