---
title: '[!DNL Inventory Management] releaseopmerkingen'
description: Herzie de versienota's voor informatie over alle  [!DNL Inventory Management]  versies.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] releaseopmerkingen

Deze releaseopmerkingen beschrijven de releases van [!DNL Inventory Management] en bevatten:

![ Nieuwe ](../assets/new.svg) Nieuwe eigenschappen
![ Vaste kwestie ](../assets/fix.svg) Oplossingen en verbeteringen
![ Bekende kwestie ](../assets/bug.svg) Bekende kwesties

[!DNL Inventory Management] is een speciaal project van de Techniek van de Gemeenschap van de Magento Open Source open aan contribuanten. Om deel te nemen en bij te dragen, zie het ](https://github.com/magento/inventory) bewaarplaats van het project GitHub en [ wiki ](https://github.com/magento/inventory/wiki) om begonnen te worden. [ Om het project te bespreken, sluit me aan bij het ](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) kanaal van de Slack [ ([ zelf-tekent ](https://opensource.magento.com/slack)).

[ programma van de Versie ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) {target="_blank"} voor gesteunde en compatibele versies.

## v1.2.7

[!DNL Inventory Management] 1.2.7 de versienota&#39;s zijn inbegrepen in de [ kern 2.4.7 versienota&#39;s ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (moduleversie: `magento/inventory-metapackage = 1.2.6` ) wordt ondersteund met versie 2.4.6 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) de opslag toont nu samengestelde producten (configureerbaar, bundel, en gegroepeerd) als in-voorraad wanneer de kindproducten die uit waren verkocht aan voorraad worden teruggekeerd. Voorheen gaf de winkel aan dat het samengestelde product onder deze omstandigheden uit voorraad was. <!-- ACP2E-1106-->

![ Vaste kwestie ](../assets/fix.svg) De configureerbare productopties worden nu getoond zoals verwacht zoals uit voorraad op de opslagplaats als de optie met hoeveelheid werd gecreeerd die aan 0 wordt geplaatst en **[!UICONTROL Display out-of-stock products]** wordt toegelaten. <!-- ACP2E-1148-->

![ Vaste de paginakaarten van de Uitgave ](../assets/fix.svg) Categorie niet meer ongeldig wanneer de voorraadhoeveelheid verandert en het product nog in voorraad is. Adobe Commerce laadt nu pagina&#39;s uit het cachegeheugen in plaats van deze opnieuw te genereren wanneer het aantal producten (en niets anders) op de pagina met winkelcategorieën verandert. <!-- ACP2E-118-->

![ Vaste kwestie ](../assets/fix.svg) het aantal van het categorielijstproduct is nu correct wanneer het gebruiken van Inventaris op enig-bronwijze met **[!UICONTROL Display Out-Of-Stock Products]** toegelaten plaatsen. Adobe Commerce controleert nu of een product bij het tellen verkoopbaar is. <!-- ACP2E-1033-->

![ Vaste kwestie ](../assets/fix.svg) de regels van de Prijs van de Kar voor In-Store Levering werken nu zoals verwacht wanneer de Inventaris wordt toegelaten. Voorheen werden onder deze voorwaarden geen door de regels bepaalde kortingen op de kartprijs toegepast. <!-- ACP2E-1015-->

![ Vaste kwestie ](../assets/fix.svg) Het bijwerken van productinventaris op geplande wijze ontruimt niet meer alle geheime voorgeheugens. Eerder, ontruimde de indexeerder van de Inventaris alle configuratiekaarten. <!-- ACP2E-1003-->

![ Vaste kwestie ](../assets/fix.svg) De waarde voor het **[!UICONTROL Allow Multiple Boxes for Shipping]** attribuut voor een product in Geavanceerde Inventaris wordt nu bewaard zoals verwacht. <!-- ACP2E-992-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce geeft nu de nauwkeurige reserveringscompensatie na een gedeeltelijke creditnota van de restitutie voor een orde uit die met in-store bestelwagen werd geplaatst. Eerder werd een onjuiste reservering opgeslagen in de tabel `inventory_reservation` wanneer een beheerder een creditmemo heeft gemaakt zonder het selectievakje **[!UICONTROL Return to Stock]** in te schakelen. <!-- ACP2E-979-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer configureerbare producten als uit voorraad op de opslagplaats wanneer één van zijn variaties manueel aan voorraad in plaatsingen is teruggekeerd die multi-bron inventaris uitvoeren. <!-- ACP2E-952-->

![ Vaste kwestie ](../assets/fix.svg) de positie van de kolom op het productnet (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) keert niet meer aan zijn vorige positie terug nadat de pagina in plaatsingen met veelvoudige gevormde inventarisbronnen opnieuw laadt. <!-- ACP2E-925-->

![ Vaste kwestie ](../assets/fix.svg) De hoeveelheid van de voorraad is nu correct nadat een creditnota voor een virtueel product wordt uitgegeven wanneer checkbox **[!UICONTROL Back to stock]** niet wordt geselecteerd. <!-- ACP2E-908-->

![ Vaste kwestie ](../assets/fix.svg) U kunt categorieën met automatisch product nu bewaren sorterend en werkingsgebied dat aan niet-gebrek voorraad wordt toegewezen. Eerder heeft Adobe Commerce de categorie niet opgeslagen en deze fout weergegeven: `Something went wrong while saving the category` . <!-- ACP2E-859-->

![ Vaste kwestie ](../assets/fix.svg) De configureerbare status van de productvoorraad wordt nu bijgewerkt zoals verwacht wanneer het product met alle uit-van-voorraad configureerbare variaties wordt gecreeerd. <!-- ACP2E-813-->

![ Vaste kwestie ](../assets/fix.svg) het hulpmiddel van de analyseer van de inconsistentie van de reserve werkt nu correct met gedeeltelijk verscheepte orden die configureerbare, bundel, en gegroepeerde producten bevatten. Samengestelde productsoorten worden nu geanalyseerd. Eerder werden annuleringen en terugbetalingen alleen opgeslagen voor bovenliggende producten, niet voor onderdelen van subproductorders van configureerbare en samengevoegde bundelproducten. <!-- ACP2E-924-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer een fout wanneer een admin gebruiker probeert om 200 of meer inventarisbronnen aan een voorraad of een product toe te wijzen. <!-- ACP2E-1180-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce steunt nu de verwezenlijking van een creditnota voor een orde waarvan een product is geschrapt. Eerder konden handelaren geen creditnota maken toen producten uit de bestelling waren geschrapt nadat een factuur was opgesteld. De toepassing heeft deze fout weergegeven: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![ Vaste kwestie ](../assets/fix.svg) De opslag wordt nu gefiltreerd gebaseerd op zowel enige als veelvoudige opslag IDs. De productkenmerkcode van `event` is toegevoegd aan de lijst met gereserveerde kenmerkcodes. In het rapport over de lage voorraad werd een uitzondering gemaakt toen de voorraadmodule werd geïnstalleerd. <!-- ACP2E-1017-->

![ Vaste kwestie ](../assets/fix.svg) Gelaagde navigatiefilters werken nu zoals verwacht, en de uit-van-voorraad producten worden nu toegevoegd aan de lijst van het de opslagcategorie product. Het nieuwe sorteerkenmerk `is_out_of_stock` gebruikt de Elasticsearch dynamic field mapper voor de collectie van het storefront-product. <!-- ACP2E-748-->

![ Vaste kwestie ](../assets/fix.svg) Samengesteld product (bundel, gegroepeerd, en configureerbaar) voorraadstatus wordt bijgewerkt zoals verwacht wanneer de status van de kindproductvoorraad door een vraag van het SPEL `POST /rest/V1/inventory/source-items` wordt veranderd. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (moduleversie: `magento/inventory-metapackage = 1.2.5` ) wordt ondersteund met versie 2.4.5 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) De standaardvoorraadstatus van bundel en gegroepeerde producten wordt nu bijgewerkt zoals verwacht wanneer een handelaar een zending van Admin leidt. Eerder bleef de status van deze producten ongewijzigd nadat een transport was gecreëerd. <!--- ACP2E-418-->

![ Vaste kwestie ](../assets/fix.svg) De configureerbare producten zijn nu teruggekeerd terug naar voorraad wanneer één van de volgende voorwaarden wordt voldaan: 1. Het bovenliggende product heeft ten minste één opgeslagen onderliggend item in voorraad. 2. Het configureerbare product zelf werd bijgewerkt en geplaatst als **in voorraad** en had minstens één kind in voorraad. <!--- ACP2E-443-->

![ de Vaste veranderingen van de Uitgave ](../assets/fix.svg) Voorraad die door REST API worden uitgevoerd worden nu weerspiegeld zoals verwacht op de pagina&#39;s van het productdetail. De cache voor catalogusproducten wordt nu schoongemaakt nadat de laatste en de huidige voorraadstatus zijn vergeleken. Eerder, resulteerde het weglaten van de callback functie in de onjuiste evaluatie van voorraadstatusveranderingen, die niet de noodzakelijke geheim voorgeheugenschoonmaakbeurt teweegbrachten. Dientengevolge weerspiegelde de opslagront de inventariswijzigingen niet. <!--- ACP2E-161-->

![ Vaste kwestie ](../assets/fix.svg) Producten die aan standaardvoorraad worden toegewezen en eerder uit voorraad waren zijn nu zichtbaar op de storefront nadat het bronpunt gebruikend `/V1/inventory/source-items` wordt bijgewerkt. Eerder stelde dit REST API-eindpunt het verkeerde `stock_status` in. <!--- ACP2E-562-->

![ Vaste kwestie ](../assets/fix.svg) het Onlanger toewijzen van inventarisbronnen door bulkactie (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) werkt nu zoals verwacht wanneer de bronnen SKUs omvatten die duplicaten behalve voorloopnul (bijvoorbeeld, `01234` en `1234`) zijn. Eerder werden door de toepassing geen inventarisbronnen verwijderd en werd een fout gegenereerd. <!--- ACP2E-2641-->

![ Vaste de voorraadstatus van het 1} Product van de kwestie {is nu altijd **in voorraad** op de opslagplaats wanneer de oneindige achterorden worden toegelaten en het product wordt toegewezen aan een douanevoorraad, ongeacht de hoeveelheid backordered. ](../assets/fix.svg) Eerder waren de producten uit voorraad, zelfs toen de back orders werden toegelaten. <!--- ACP2E-664-->

![ Vaste kwestie ](../assets/fix.svg) het Configureerbare product ouder en de voorraad van het kindproduct wordt nu correct bijgewerkt nadat het bronpunt met `POST /V1/inventory/source-items` wordt bijgewerkt. Nadat het onderliggende product via de API is bijgewerkt, wordt een nieuwe voorraadinsteekmodule beschikbaar gesteld voor standaardvoorraadcontroles en updates voor configureerbare producthoeveelheid en status. <!--- ACP2E-442-->

![ Vaste kwestie ](../assets/fix.svg) uit-van-voorraad gegroepeerde producten zijn niet meer vermeld op de pagina van de opslagmiddelencategorie. <!--- ACP2E-2082-->

![ Vaste kwestie ](../assets/fix.svg) Correcteerde de pakketnaam in `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![ Vaste kwestie ](../assets/fix.svg) de achterordestatus wordt nu correct vertegenwoordigd in Admin na het plaatsen van een orde met nul kwantitatief product in een multi bron/voorraadplaatsing. [ GitHub-33756 ](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![ Vaste kwestie ](../assets/fix.svg) de producten van de uit-van-voorraad bundel worden niet meer getoond op de pagina van de opslagcategorie wanneer het bundelproduct van de voorraadsectie wordt bijgewerkt. <!--- ACP2E-2012-->

![ Vaste kwestie ](../assets/fix.svg) De kwesties van de Verenigbaarheid met PHP 7.4 worden opgelost. <!--- AC-3192-->

![ Vaste kwestie ](../assets/fix.svg) De prestaties van sparen verrichtingen die bundelproducten omvatten die vele opties (verscheidene 100) bevatten wordt verbeterd. Eerder duurde het opslaan van deze grote bundelproducten enkele minuten en soms leidde het tot vertragingen in implementaties met ingeschakelde inventarisservices. [ GitHub-34732 ](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![ Vaste kwestie ](../assets/fix.svg) het product bulkactiegereedschap (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) werkt nu zoals verwacht wanneer het toewijzen van inventarisbron aan veelvoudige producten wanneer SKUs behalve een belangrijke `0` (bijvoorbeeld, `01234` en `1234`) wordt gedupliceerd. Eerder werd slechts één product een inventarisbron toegewezen. [ GitHub-35171 ](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![ Vaste kwestie ](../assets/fix.svg) het `ProductInterface.only_x_left_in_stock` gebied keert nu 0 terug als de inventaris 0 is. Eerder werd null geretourneerd. [ GitHub-29932 ](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![ Vaste kwestie ](../assets/fix.svg) U kunt standaardvoorraad van Admin **[!UICONTROL Stores]** nu uitgeven > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Eerder werd een JavaScript-fout weergegeven in de console toen u probeerde bronnen toe te voegen aan of te verwijderen uit de standaardvoorraad, maar u kon websites toewijzen aan de standaardvoorraad. <!--- ACP2E-545-->

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-274--> Het aantal van het categorielijstproduct is nu correct wanneer het gebruiken van inventaris enig-bronwijze met **[!UICONTROL Display Out-Of-Stock Products]** toegelaten plaatsen. Een nieuwe plug-in gebruikt nu `AreProductsSalableInterface` en `StockConfigurationInterface` om het totale aantal producten te bepalen. Eerder heeft de lijst met producten van de categorie de verkeerde hoeveelheid product geretourneerd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-322--> De configureerbare producten worden nu verplaatst naar de laatste positie in de productlijst nadat de voorraad wordt bijgewerkt wanneer **[!UICONTROL Move out of stock to the bottom]** het plaatsen wordt toegelaten. Er wordt een nieuwe aangepaste databasequery geïmplementeerd om de sorteervolgorde van de index van de Elasticsearch te negeren, waarbij de sorteervolgorde voor beheerders wordt genegeerd. Eerder, werden de configureerbare producten en hun kindproducten niet verplaatst naar de bodem van de lijst toen dit het plaatsen werd toegelaten.

## v1.2.4

Inventory management 1.2.4 (moduleversie: `magento/inventory-metapackage = 1.2.4`) wordt ondersteund met versie 2.4.4 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) Commerce toont nu een nauwkeurige verkoopbare kwantitatieve waarde voor alle producten in de Admin mening van de productlijst. Eerder werd een lege waarde weergegeven voor de verkoopbare hoeveelheid producten in voorraad met SKU&#39;s die speciale tekens bevatten. <!--- MC-41936-->

![ Vaste kwestie ](../assets/fix.svg) Prestaties zijn verbeterd voor kar-en-controlemaatregelen zoals het toevoegen van producten aan de kar in plaatsingen met vele (ongeveer 10.000) inventarisbronnen. <!--- MC-42570-->

![ Vaste kwestie ](../assets/fix.svg) het `bin/magento inventory:reservation:list-inconsistencies` bevel behandelt nu correct orden met gedeeltelijke verzendingen zelfs als de reserveringen van het gegevensbestand worden overgeslagen en het geheime voorgeheugen is ontruimd. Eerder, toen deze opdracht werd uitgevoerd met een vooraf gewist cachegeheugen, gaf Commerce de volgende fout weer: `Area code is not set` . <!--- MC-42142-->

![ Vaste kwestie ](../assets/fix.svg) Incrementele indexering van gegroepeerde producten van het productkind veroorzaakt niet meer andere gegroepeerde producten om verkeerd worden geïndexeerd wanneer de kinderen worden gedeeld. <!--- MC-41963-->

![ Vaste kwestie ](../assets/fix.svg) de pagina van de storefrontcategorie toont nu de correcte producttelling na het verwijderen van een product uit een categorie door API. Eerder was het aantal producten op de categoriepagina onjuist tot opnieuw indexeren plaatsvond. <!--- MC-42287-->

![ Vaste kwestie ](../assets/fix.svg) De configureerbare producten kunnen nu aan voorraad worden teruggekeerd wanneer het creëren van een creditnota wanneer de **[!UICONTROL Manage Stock]** optie gehandicapt is. Eerder, gaf Commerce niet de **Terugkeer aan voorraad** checkbox op de pagina van de creatie van het creditmemo weer toen deze optie werd onbruikbaar gemaakt. <!--- MC-42002-->

![ Vaste kwestie ](../assets/fix.svg) Het beheer van het Voorraad dat 10.000 punten overschrijdt is verbeterd. Eerder waren handelaars vanwege prestatieproblemen soms niet in staat om voorraden te bewerken in Admin voordat ze hun website lanceerden. <!--- MC-42643-->

![ Vaste kwestie ](../assets/fix.svg) De **[!UICONTROL User Roles]** pagina in Admin wordt bijgewerkt om beheerders van beperkte toestemmingentoegang tot de configuratie van de leveringsmethodes te voorzien. De _Verzendmethodes_ sectie is anders genoemd aan _[!UICONTROL Delivery methods]_, en_[!UICONTROL In-Store Pickup]_ wordt bewogen onder de _[!UICONTROL Delivery methods]_sectie. [ GitHub-30053 ](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce leidt niet meer tot een dubbele productreserve nadat een creditnota door API wordt bijgewerkt. <!--- MC-41757-->

![ Vaste kwestie ](../assets/fix.svg) Het schakelen van het _[!UICONTROL Pick up in Store]_lusje aan het_[!UICONTROL Shipping]_ lusje in het controlewerkschema leidt niet meer tot een fout van JavaScript wanneer slechts de Bestelling van de Bestelwagen In-Store beschikbaar is. <!--- MC-42808-->

![ Vaste kwestie ](../assets/fix.svg) Verkoopbare producthoeveelheid en in voorraad producthoeveelheid worden nu correct gesynchroniseerd. Eerder werd de compensatie voor de boeking van voorraden niet opnieuw gemaakt voor geannuleerde orders. <!--- MC-42485-->

![ Vaste kwestie ](../assets/fix.svg) De prestaties van validator worden geoptimaliseerd om te verhinderen toevoegend nieuwe bron aan het kindproduct van een gebundeld product met ladingstype `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (moduleversie: `magento/inventory-metapackage = 1.2.3` ) wordt ondersteund met versie 2.4.3 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) Vaste verscheidene kwesties met betrekking tot de samengestelde productzichtbaarheid op het front.

![ Vaste kwestie ](../assets/fix.svg) Verbeterde prestaties van het het paginanummerbeheer van de kar met de minimaal vereiste hoeveelheid.

![ Vaste kwestie ](../assets/fix.svg) Verscheidene moeilijke situaties die worden gericht om kwesties met bronverwezenlijking, uit voorraadpunten, voorraadbron het sorteren van toegewezen bronnen, in-opslaglevering, en inventarisbevelen op te lossen.

![ Vaste kwestie ](../assets/fix.svg) [!DNL Commerce] steunt nu driecijferige Canadese postcodes voor in-store levering. codes met zes cijfers worden niet ondersteund vanwege beperkingen die zijn ingesteld door `geonames.org` .

![ Vaste kwestie ](../assets/fix.svg) Admin toont nu de correcte hoeveelheid standaardvoorraad voor gehandicapte producten op het **Produkten** net en **uitgeeft de pagina van het Product** voor multi-store plaatsingen.

![ Vaste kwestie ](../assets/fix.svg) [!DNL Commerce] verfrist nu het geheime voorgeheugen van het categorieproduct wanneer een bundelproduct terug in voorraad terugkomt.

## 1.2.

[!DNL Inventory Management] 1.2.2 (moduleversie: `magento/inventory-metapackage = 1.2.2` ) wordt ondersteund met versie 2.4.2 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) Vaste verscheidene kwesties met betrekking tot de samengestelde productzichtbaarheid op het front.

![ Vaste kwestie ](../assets/fix.svg) Verbeterde prestaties van de wortelpagina tijdens kwantitatieve update op B2B.

![ Vaste kwestie ](../assets/fix.svg) Verscheidene moeilijke situaties die worden gericht om kwesties met in-store bestelwagen, massa updates, en inventarisdrempel op te lossen.

![ Nieuwe ](../assets/new.svg) **Functionele tests.** Introduceerde nieuwe functionele tests en verstrekte correcties voor bestaande tests om deze stabieler te maken.

## 1.

[!DNL Inventory Management] 1.2.1 (moduleversie: `magento/inventory-metapackage = 1.2.1` ) wordt ondersteund met versie 2.4.1 en compatibel met versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) bekende kwestie met betrekking tot de `inventory_cleanup_reservations` bouwbaan en behandelde een kwestie met betrekking tot de functionaliteit van de Bestelwagen van de Opslag in-Opslag voor bundelproducten. Deze update bevat ook algemene verbeteringen voor het berekenen van voorraden, ondersteuning voor gebundelde producten en backorder-functionaliteit.

![ Nieuwe ](../assets/new.svg) **Functionele tests.** Introduceerde nieuwe functionele tests om extra dekking te bieden voor de functie Ophalen in de winkel.

## 1.2.0.

[!DNL Inventory Management] 1.2.0 (moduleversie: `magento/inventory-metapackage = 1.2.0` ) wordt ondersteund door versie 2.4.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) talrijke moeilijke situaties om kwesties met brontaak, scalable de eigenschapsteun van het milieu, en verenigbaarheid met PHP 7.4, MySQL 8, en PHPUNIT 9 op te lossen.

![ Nieuwe ](../assets/new.svg) **In-store leveringsmethode.** Er is een optie toegevoegd waarmee gebruikers een bron kunnen selecteren die tijdens het uitchecken moet worden gebruikt als ophaallocatie. Zie [ In-store Levering ](../stores-purchase/shipping-in-store-delivery.md) in de _Gids van de Ervaring van de Verkoop en van de Aankoop_.

![ Nieuwe ](../assets/new.svg) **de productsteun van de Bundel voor multi-bronwijze.** Inventory ondersteunt alle producttypen met meerdere bronnen.

![ Nieuwe ](../assets/new.svg) **Asynchrone aandelen die opnieuw indexeren.** Hiermee hebt u de mogelijkheid toegevoegd om de voorraad asynchroon opnieuw te indexeren en de prestaties van verschillende kritieke scenario&#39;s te verbeteren.

![ Nieuwe ](../assets/new.svg) **Bulk interfaces.** Nieuwe bulkinterfaces voor controle op de verkoopbaarheid geïntroduceerd: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface` , `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface` .

![ Nieuwe ](../assets/new.svg) **Verhoogde testdekking.** Nieuwe functionaliteit wordt behandeld met geautomatiseerde tests, waaronder uitgebreide dekking voor ontdekte en opgeloste problemen.

![ Bekende kwestie ](../assets/bug.svg) **Bekende kwestie.** Door het ontbreken van het veld `object_id` in de metagegevens van reserveringen werkt de `inventory_cleanup_reservations` -snijtaak niet goed. Deze kwestie werd geïntroduceerd in [ magento/voorraad#3046 ](https://github.com/magento/inventory/pull/3046).

**Oplossing:** voer de volgende vragen MySQL uit om reserveringen manueel op te schonen:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6.

[!DNL Inventory Management] 1.1.6 (moduleversie: `inventory-composer-metapackage = 1.1.6` ) wordt ondersteund met versie 2.3.6 en is compatibel met versie 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) Bevestigingen om kwesties met betrekking tot backorders, creditmemo&#39;s, het lage net van het voorraadrapport op te lossen, moeilijke situaties verbonden aan &quot;los inconsistenties&quot;CLI hulpmiddel en algemene verbeteringen op.

![ Nieuwe ](../assets/new.svg) **Asynchrone aandelen die opnieuw indexeren.** Hiermee hebt u de mogelijkheid toegevoegd om de voorraad asynchroon opnieuw te indexeren en de prestaties van verschillende kritieke scenario&#39;s te verbeteren.

## 1.1.5.

[!DNL Inventory Management] 1.1.5 (moduleversie: `inventory-composer-metapackage = 1.1.5` ) wordt ondersteund met versie 2.3.5 en compatibel met versie 2.3.4, 2.3.3, 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Nieuwe ](../assets/new.svg) **inventaris van de Update zodra product SKU wordt veranderd.** Introduceerde een nieuwe configuratie die plaatst om op het nieuwe gedrag over te schakelen: &quot;synchroniseert met Catalogus&quot;.

![ Nieuwe ](../assets/new.svg) **Functionele tests.** Introduceerde nieuwe functionele tests om de leemte in de testdekking te elimineren. Verschillende problemen verholpen om tests stabieler en betrouwbaarder te maken).

![ Bekende kwestie ](../assets/bug.svg) Bevestigingen om productoververkoop, &quot;uit voorraad&quot;producten zicht op de winkel, talrijke moeilijke situaties voor scalable milieusteun en gebruikersinterfaceverbeteringen te verhinderen.

## 1.1.4.

[!DNL Inventory Management] 1.1.4 (moduleversie: `inventory-composer-metapackage = 1.1.4` ) wordt ondersteund met versie 2.3.4 en compatibel met versie 2.3.3, 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg)**Verhoogde prestaties.** Inleiding tot bunching logic voor Inventory Reservations CLI command om geheugengebruik te verminderen en gevallen te voorkomen wanneer het proces vastloopt zonder enige reactie.

![ Nieuwe ](../assets/new.svg)**Verhoogde testdekking.** Introduceerde veel nieuwe functionele tests. Bijna alle scenario&#39;s met handmatige inventarisatie worden behandeld met geautomatiseerde tests.

![ Bekende kwestie ](../assets/bug.svg) talrijke moeilijke situaties die worden gericht om kwesties met creditmemo&#39;s, gegroepeerde producten, en bron en voorraadmassaacties op te lossen.

## 1.1.3.

[!DNL Inventory Management] 1.1.3 (moduleversie: `inventory-composer-metapackage = 1.1.3` ) wordt ondersteund met versie 2.3.3 en compatibel met versie 2.3.2, 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg)**Betere integratie met Adobe Commerce en B2B eigenschappen.** [!DNL Inventory Management] werkt nu correct met de volgende functies voor websites die niet-standaard inventarisbronnen en -voorraden gebruiken:

- Bestelling door SKU (Adobe Commerce)
- Snelle volgorde (B2B)
- Aanvraaglijsten (B2B)

![ Nieuwe ](../assets/new.svg)**Verhoogde prestaties.** Browserprestaties van de Storefront-catalogus worden verbeterd voor websites waarop de standaardvoorraad en -bron worden uitgevoerd.

![ Nieuwe ](../assets/new.svg)**Verhoogde testdekking.** De testdekking voor geautomatiseerde functionaliteit en integratie is aanzienlijk toegenomen.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (moduleversie: `inventory-composer-metapackage = 1.1.2` ) wordt ondersteund met versie 2.3.2 en compatibel met versie 2.3.1 en 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) toegevoegd `source_code` aan de reactie voor het GET `/V1/shipments` eindpunt REST. <!-- https://github.com/magento/inventory/pull/2142 -->

![ Vaste kwestie ](../assets/fix.svg) loste kwestie op om reserveringen correct te ontruimen en producthoeveelheden bij te werken na het uitgeven van een creditnota voor een niet verscheepte orde. Wanneer u de optie selecteert die u wilt gebruiken <!-- https://github.com/magento/inventory/pull/2179 -->

![ Vaste kwestie ](../assets/fix.svg) Oplossing voor kwestie om hoeveelheid voor configureerbare productkinderen correct te bewaren wanneer het ingaan van hoeveelheden tijdens productverwezenlijking. <!-- https://github.com/magento/inventory/pull/2158 -->

Nieuwe modules voor [!DNL Inventory Management] 1.1.2 Beta zijn:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![ Nieuw ](../assets/new.svg) **voegde een Bulk Gedeeltelijke Eindpunt van de Overdracht van het Dossier** toe - De Huidige bulkoverdrachteindpunten bewegen al toegewezen hoeveelheid van een oorsprong aan een bestemmingsbron. Het nieuwe `/rest/V1/inventory/bulk-partial-source-transfer` eindpunt staat verkopers toe om gedeeltelijk materiaal van bron aan bron als bulkverrichting over te brengen. Als u een bepaalde hoeveelheid wilt overbrengen, voert u een aanvraag in bij het eindpunt met de waarden `sku`, `qty`, `origin_source_code` en `destination_source_code` . Bij overdrachten wordt gecontroleerd of de bron is toegewezen aan de `sku` , of er voldoende hoeveelheid is om over te dragen, enzovoort. Zie [ de massaacties van de Inventaris ](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/) {target="_blank"} in de REST API documentatie. <!-- https://github.com/magento/inventory/pull/2117 -->

![ Nieuwe ](../assets/new.svg) **Toegevoegde Reservation CLI** - de Nieuwe bevelen geven u opties om reserveringsinconsistenties te ontdekken en op te lossen. Terwijl bestellingen worden verzonden en de status wordt gewijzigd, genereert [!DNL Inventory Management] initiële reserveringen en updates via compensatiereserveringen. Deze bevelen keren een lijst van ontdekte inconsistenties door identiteitskaart van de Orde, SKU, en identiteitskaart van het Beeld terug en creeer reserveringen om op te lossen. Zie de [ CLI verwijzing ](cli.md) voor meer informatie. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![ Nieuwe ](../assets/new.svg) **de verbeteringen van Prestaties voor bronnen en opties SSA** - het sorteren en het selecteren van bronnen tijdens lading veroorzaakte prestatiesdegradatie voor voorraden met hoge aantallen bronnen. Deze release biedt aanzienlijke prestatieverbeteringen voor het weergeven en sorteren van beschikbare bronnen bij het controleren en selecteren van SSA-opties in verzendingen. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![ Nieuwe ](../assets/new.svg) **Toegevoegde steun van GraphQL voor Inventory management** - Deze versie installeert een nieuwe `magento/module-inventory-graph-ql` module. De attributen van GraphQL [ ProductInterface ](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/) {target="_blank"} omvatten nu de `only_x_left_in_stock` en `stock_status` attributen voor [!DNL Inventory Management] steun. <!-- https://github.com/magento/inventory/pull/2124 -->

![ Nieuwe ](../assets/new.svg) **Vereenvoudigde UI voor Toegewezen Bronnen** - de Toegewezen Bronlijst in productpagina&#39;s heeft inhoud voor gemakkelijkere updates en verhoogde prestaties wanneer het tonen van vele bronnen vereenvoudigd. Alle bronnen worden weergegeven op naam van bron (houd de muisaanwijzer boven `source_code`).

![ Nieuwe ](../assets/new.svg) **de Geaggregeerde Dienst van het Voorraad van de Uitvoer** - Deze versie verleent de nieuwe uitvoer-geaggregeerde voorraaddienst (het behouden van reserveringen in het systeem) om externe Sales Channel, zoals Amazon, eBay, en Google het Winkelen advertenties te steunen.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0.

[!DNL Inventory Management] 1.1.0 (moduleversie: `inventory-composer-metapackage = 1.1.0` ) wordt ondersteund en is compatibel met versie 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code. [!DNL Inventory Management] 1.1.1 wordt alleen vrijgegeven als een pakketnaamupdate, ondersteund voor versie 2.3.1 en compatibel met versie 2.3.0 van Adobe Commerce, Adobe Commerce op cloudinfrastructuur en de basis van de Magento Open Source code.

![ Vaste kwestie ](../assets/fix.svg) **Toegevoegde steun voor Elasticsearch voor enige en multi-bronwijzen** — U kunt Elasticsearch met douanevoorraden nu vormen en gebruiken. Zie {de dienst van de Elasticsearch van de opstelling ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html) {target="_blank"} voor installatieinformatie. <!-- PR https://github.com/magento/inventory/pull/1943 -->[

![ Vaste kwestie ](../assets/fix.svg) Opgeloste prestatieskwesties met StandaardVoorraad om prestaties met talrijke verrichtingen drastisch te verhogen. De verbeteringen verhogen prestaties voor single-source wijze, Overdracht Inventaris aan Source, de pagina&#39;s van de Categorie van de Storefront, en de berekeningen van de Hoeveelheid van de Verkoop.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![ Vaste kwestie ](../assets/fix.svg) Opgeloste kwesties met uit de status van de Voorraad en bulkoverdracht van de Inventaris aan Voorraad voor configureerbare en gegroepeerde producten. Het selecteren van de bovenliggende producten en het uitvoeren van acties in bulk heeft geen invloed op de productstatus. Als het moederproduct in voorraad was, blijft het in voorraad.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![ Nieuw ](../assets/new.svg) **Prioritair Algoritme van de Afstand** - het Prioriteitsalgoritme van de Afstand is een nieuw, uit-van-de-doos Algoritme van de Selectie van Source voor op afstand-gebaseerde verschepende aanbevelingen. Dit algoritme vergelijkt de plaats van het verzendende bestemmingsadres met bronplaatsen om de dichtstbijzijnde bron te bepalen om verzendingen te vervullen. De afstand kan worden bepaald door fysieke afstand of door de tijd die is besteed aan het reizen van de ene naar de andere locatie, met behulp van geïmporteerde geocode-locatiegegevens of Google-richtingen (rijden, lopen of fietsen).

![ Nieuwe ](../assets/new.svg) **Uitgebreide bronkwantitatieve lijst** — De handelaren met een hoog aantal bronnen kunnen gemakkelijk bewegen en alle bronnen per product door het Net van het Product bekijken. Elk product bevat minimaal vijf bronnen en overeenkomende hoeveelheden. Wanneer u de muis boven de bronnen houdt, kunt u door de volledige lijst met bronnen en huidige hoeveelheden bladeren.

![ Bekende kwestie ](../assets/bug.svg) Bekende kwestie met Magento Open Source en Adobe Commerce v2.3.1 - de Asynchrone migratie van gegevens tussen bronnen ontmoet kwesties toe te schrijven aan veranderingen in Asynchrone APIs met onderwerpnamen die PHP klasse en methodenamen weerspiegelen. U wordt aangeraden synchrone bewerkingen te gebruiken door **[!UICONTROL Run asynchronously]** in te stellen op `No` .
