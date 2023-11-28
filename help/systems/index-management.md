---
title: Indexbeheer
description: Leer over indexbeheer, met inbegrip van de acties die het opnieuw indexeren en beste praktijken teweegbrengen.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# Indexbeheer

Adobe Commerce en Magento Open Source worden automatisch opnieuw berekend telkens als een of meer items worden gewijzigd. Acties die opnieuw indexeren activeren, zijn onder andere prijswijzigingen, het maken van catalogi- of winkelregels voor winkelwagenprijzen, het toevoegen van nieuwe categorieën enzovoort. Om prestaties te optimaliseren, accumuleert de Handel gegevens in speciale lijsten gebruikend indexeerders. Als de gegevens veranderen, moeten de geïndexeerde tabellen worden bijgewerkt of opnieuw worden gedesdexeerd. De handel herstelt als achtergrondproces, en uw opslag blijft toegankelijk tijdens de processen.

Het opnieuw indexeren van gegevens versnelt de verwerking, en vermindert de tijd de klant moet wachten. Als je bijvoorbeeld de prijs van een object wijzigt van $4,99 in $3,99, worden de gegevens opnieuw ingedexeerd om de prijswijziging in de winkel aan te geven. Zonder indexering zou de Commerce de prijs van elk product tijdens de vlucht moeten berekenen; de regels van de winkelwagenprijs, de bundelprijs, kortingen, de laagprijs, enzovoort. Het laden van de prijs voor een product kan langer duren dan de klant bereid is te wachten.

De indexeerders kunnen worden ingesteld op bijwerken tijdens het opslaan of op schema. Alle indexen kunnen beide opties gebruiken, behalve Klantenraster dat alleen ondersteuning biedt voor opslaan. Wanneer de indexering bij sparen, de Uitwisseling begint een herindex op sparen acties. De pagina van het Beheer van de Index voltooit de update en spoelt het geheime voorgeheugen, met het herindexbericht verschijnen binnen een minuut of twee. Wanneer opnieuw indexeren op een programma, loopt een herindex volgens een programma als bijbaanbaan. Er verschijnt een systeembericht als een [snijtaak](cron.md) is niet beschikbaar voor het bijwerken van indexen die ongeldig worden. Uw winkel blijft toegankelijk tijdens herindexeringsprocessen.

>[!NOTE]
> Handelaren van Adobe Commerce die Live Search, Catalog Service of Product Recommendations gebruiken, kunnen een [Op SaaS gebaseerde prijsindexer](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

Als een nieuwe index nodig is, verschijnt een melding boven aan de pagina. De index en het bericht worden gewist op basis van de herindexmodus en de mogelijke acties die u uitvoert. Raadpleeg voor meer informatie over indexering de [Hoe de toepassing indexering implementeert](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) in de _PHP-ontwikkelaarsgids_.

![Indexbeheer - handelingen](./assets/index-management.png){width="700" zoomable="yes"}

- Index Management heeft een iets andere presentatie voor platte productcatalogi.
- Om problemen te voorkomen wanneer meerdere Admin-gebruikers objecten bijwerken die automatisch opnieuw indexeren activeren, wordt u aangeraden alle indexen volgens schema uit te voeren [kroonbanen](cron.md). Anders kunnen objecten met onderlinge afhankelijkheden, telkens wanneer een object wordt opgeslagen, een impasse veroorzaken. Symptomen van een impasse zijn onder andere een hoog CPU-gebruik en MySQL-fouten. Als beste praktijken, adviseert men dat u geplande indexering gebruikt.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Standaard worden beheeracties, zoals opnieuw indexeren, vastgelegd door het systeem en kunnen deze worden weergegeven in het dialoogvenster [Rapport met handelingslogboeken](action-log-report.md). Het registreren van de actie kan in worden gevormd [Logboekregistratie van beheerhandelingen](action-log.md) in de geavanceerde beheerinstellingen van uw winkel.

## Aanbevolen werkwijzen voor herindexering

Bij de Handel hebben opnieuw indexeren en in cache plaatsen verschillende doeleinden. De indexen volgen gegevensbestandinformatie voor verhoogde onderzoeksprestaties, snellere gegevensherwinning voor opslagmilieu&#39;s, en meer. [Cursussen](cache-management.md) Sla geladen gegevens, afbeeldingen, indelingen en dergelijke op voor betere prestaties bij het laden en openen van de winkel.

- Doorgaans wilt u opnieuw indexeren bij het bijwerken van gegevens in de handel.
- Als u een grote winkel of meerdere winkels hebt, kunt u indexeerders zoals categorie en producten instellen op geplande snijtaken vanwege de mogelijkheid van herindexering. U kunt de herdex instellen volgens een schema gedurende niet-piekuren.
- Wanneer u opnieuw indexeert, hoeft u niet ook een uitlijncache uit te voeren.
- Voor nieuwe installaties van de Handel, moet u het geheime voorgeheugen en de herdex leegmaken.
- Door het leegmaken van caches en het opnieuw indexeren wordt de webbrowsercache van uw computer niet leeggemaakt. Wis de browsercache nadat u de updates voor uw winkel hebt voltooid.

## De indexmodus wijzigen

>[!IMPORTANT]
>
>Voor winkels die [B2B voor Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) en hebben Elasticsearch ingesteld als de volledige tekst (`catalogsearch_fulltext`) indexer: De fulltext-index moet opnieuw worden uitgevoerd nadat de bulkmachtigingen zijn gewijzigd of wanneer de indexfunctie &#39;permissions&#39; in de modus &#39;Gepland&#39; staat.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Schakel het selectievakje in voor elke index die u wilt wijzigen.

1. Set **[!UICONTROL Actions]** op een van de volgende wijzen:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >Het Net van de Klant kan slechts opnieuw worden gedexeerd gebruikend `Update on Save`. Deze index doet dit **_niet_** ondersteuning `Update by Schedule`.

1. Klikken **[!UICONTROL Submit]** om de wijziging toe te passen op elke geselecteerde index.

   **Kolommen Indexbeheer**

   | Kolom | Beschrijving |
   | ------ | ----------- |
   | [!UICONTROL Indexer] | De naam van de index. |
   | [!UICONTROL Description] | Een beschrijving van de index. |
   | [!UICONTROL Mode] | Hiermee wordt de huidige updatemodus voor elke index aangegeven. Opties: <br/>**[!UICONTROL Update on Save]**- De index wordt ingesteld op bijwerken wanneer een entiteitswijziging wordt opgeslagen. Deze entiteiten omvatten producten, categorieën, en klanten. Wanneer de opslagactie is voltooid, wordt een reeks stappen uitgevoerd om de wijzigingen vast te leggen en de index bij te werken. De pagina van het Beheer van de Index werkt en spoelt het herindexbericht binnen een minuut of twee bij.<br/>**[!UICONTROL Update on Schedule]** - De index is ingesteld op een update volgens een schema [snijtaak](cron.md). De bouwbaan omvat het planningsinterval voor het opnieuw indexeren, schrijvend updates aan de index wanneer looppas. |
   | [!UICONTROL Schedule Status] | Geeft de statusupdates van het schema weer. |
   | [!UICONTROL Status] | Hiermee geeft u een van de volgende opties weer: <br/>**[!UICONTROL Ready]**— De index is bijgewerkt.<br/>**[!UICONTROL Scheduled]** - Herindexering is gepland. <br/>**[!UICONTROL Running]**- Er wordt opnieuw geïndexeerd.<br/>**[!UICONTROL Reindex Required]** - Er is een wijziging aangebracht die opnieuw indexeren vereist, maar de indexen kunnen niet automatisch worden bijgewerkt. Controleren of [kraan](cron.md) is beschikbaar en correct gevormd. |
   | [!UICONTROL Updated] | Geeft de datum en tijd aan waarop een index voor het laatst is bijgewerkt. |

   {style="table-layout:auto"}

## Opnieuw indexeren met de opdrachtregel

De handel verstrekt extra herindexopties gebruikend de bevellijn. Voor volledige details en bevelopties, zie [Opnieuw indexeren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} in het dialoogvenster _Configuratiegids_.

## Gebeurtenissen van indextrigger

## Triggers opnieuw indexeren

| Indextype | Gebeurtenis voor opnieuw indexeren |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Klantengroep toevoegen<br/>Configuratieinstellingen wijzigen |
| [!UICONTROL Flat catalog product data] | Winkel toevoegen<br/>Winkelgroep toevoegen<br/>Kenmerk toevoegen, bewerken of verwijderen (voor zoeken en filteren) |
| [!UICONTROL Flat catalog category data] | Winkel toevoegen<br/>Winkelgroep toevoegen<br/>Kenmerk toevoegen, bewerken of verwijderen (voor zoeken en filteren) |
| [!UICONTROL Catalog category/product index] | Producten toevoegen, bewerken of verwijderen (enkelvoudig, massa en importeren)<br/>Relaties tussen producten en categorieën wijzigen<br/>Categorieën toevoegen, bewerken of verwijderen<br/>Opslag toevoegen of verwijderen<br/>Winkelgroepen verwijderen<br/>Websites verwijderen |
| [!UICONTROL Catalog search index] | Producten toevoegen, bewerken of verwijderen (enkelvoudig, massa en importeren)<br/>Opslag toevoegen of verwijderen<br/>Winkelgroepen verwijderen<br/>Websites verwijderen |
| [!UICONTROL Stock status index] | Wijzig de configuratie-instellingen voor de voorraad. |
| [!UICONTROL Category permissions index] | Winkel toevoegen<br/>Winkelgroep toevoegen<br/>Kenmerk toevoegen, verwijderen of bijwerken (voor zoeken en filteren) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Het gebruik van een platte catalogus wordt niet langer aanbevolen als beste praktijk. Het is bekend dat voortdurend gebruik van deze functie prestatievermindering en andere indexeringsproblemen kan veroorzaken. Zie [Plat catalogusproduct gebruiken](../catalog/catalog-flat.md) voor meer informatie .

## Indexhandelingen en -besturingselementen

| Handeling | Resultaat | Besturingselementen |
| ------ | ------ | -------- |
| Een winkel, nieuwe klantengroep of een handeling maken die in `Actions that Cause a Full Reindex` | Volledige herclassificatie | De volledige herindexering wordt uitgevoerd volgens het schema dat door uw Adobe Commerce of Magento Open Source wordt bepaald bouwbaan. |
| Bulksgewijs laden van items (Commerce importeren/exporteren, Direct SQL-query en elke andere methode die gegevens direct toevoegt, wijzigt of verwijdert) | Gedeeltelijke herindex (alleen gewijzigde items worden opnieuw gedesdexeerd) | Met de frequentie die wordt bepaald door de kroon van de Handel baan. |
| Bereik wijzigen (bijvoorbeeld van algemeen naar website) | Gedeeltelijke herindex (alleen gewijzigde items worden opnieuw gedesdexeerd) | Met de frequentie die wordt bepaald door de kroon van de Handel baan. |

{style="table-layout:auto"}

## Gebeurtenissen die volledige redexering activeren

| Indexer | Gebeurtenis |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Een webwinkel maken<br/>Een webwinkelweergave maken<br/>Maak of verwijder een kenmerk dat een van de volgende kenmerken heeft:<br/>- Doorzoekbaar of zichtbaar in geavanceerd zoeken<br/>- Filterbaar<br/>- Filterbaar in zoekopdracht<br/>- Gebruikt voor sorteren<br/>Wijzig een bestaand kenmerk in een van de voorgaande kenmerken.<br/>Opties voor één winkelcentrum voor categorieën inschakelen |
| [!UICONTROL Catalog Product Flat Indexer] | Een webwinkel maken<br>Een webwinkelweergave maken<br/>Maak of verwijder een kenmerk dat een van de volgende kenmerken heeft:<br/>- Doorzoekbaar of zichtbaar in geavanceerd zoeken<br>- Filterbaar<br>- Filterbaar in zoekopdracht<br/>- Gebruikt voor sorteren <br/>Wijzig een bestaand kenmerk in een van de voorgaande kenmerken.<br/>Opties voor één winkelcentrum voor categorieën inschakelen |
| [!UICONTROL Stock status indexer] | Wanneer het volgende _Opties voor catalogusinventarisatie_ wijziging in de systeemconfiguratie:<br/>`Stock Options` - Weergave producten uit voorraad<br/>`Product Stock Options` - Voorraad beheren |
| [!UICONTROL Price Indexer] | Een klantengroep toevoegen.<br/>Wanneer een of meer van de volgende opties in de catalogusinventarisatie worden gewijzigd in de systeemconfiguratie:<br/>`Stock Options` - Weergave producten uit voorraad<br/>`Product Stock Options` - Voorraad beheren<br/>`Price` - Bereik catalogusprijs |
| [!UICONTROL Category or Product Indexer] | Een winkelweergave maken of verwijderen<br/>Een winkel verwijderen<br/>Een website verwijderen |

{style="table-layout:auto"}
