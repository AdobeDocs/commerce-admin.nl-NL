---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] pagina van de Commerce Admin.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 80630957dbe25d21c45f64d8027a39b7b396619d
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] voor Adobe Commerce en Magento Open Source biedt u de tools om uw productvoorraad te beheren. Handelaars met één winkel kunnen deze functies gebruiken om de verkoop en de verzending van goederen te voltooien. Zie voor meer informatie over deze functies en hoe u deze kunt gebruiken om bestanden op meerdere locaties te beheren de [_[!DNL Inventory Management] Handboek _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Opties voor voorraad](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Algemeen | Indien ingesteld op `Yes`, de hoeveelheid in voorraad vermindert wanneer de bestelling wordt geplaatst. Met _Stock beheren_ eventueel worden voorbehouden voor de bestelde producten en hoeveelheden geboekt. Opties: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Winkelweergave | Indien ingesteld op `Yes`, retourneert item naar voorraad wanneer de bestelling wordt geannuleerd. Met _Stock beheren_ mogelijk wordt de boeking voor de geannuleerde producten en hoeveelheden goedgekeurd. Opties: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Algemeen | Indien ingesteld op `Yes`, geeft producten weer die uit voorraad zijn. Als productwaarschuwingen ook zijn ingeschakeld, kunnen klanten zich aanmelden om op de hoogte te worden gesteld wanneer het product beschikbaar komt. Opties: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Website | De drempel voor de `Only x left` bericht. Bijvoorbeeld, als reeks aan 3, verschijnt het bericht wanneer er drie of minder van een punt in voorraad zijn. Het bericht wordt niet weergegeven als de waarde is ingesteld op `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | Winkelweergave | Indien ingesteld op `Yes`, geeft een `In Stock` of `Out of Stock` bericht op de productpagina. Opties: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Algemeen | Hiermee wordt bepaald of een inventariscontrole wordt uitgevoerd bij het laden van een product in de winkelwagen. Als u deze voorraadcontrole uitschakelt, kunnen de prestaties voor de afhandelingsstappen verbeteren, met name wanneer er veel items in het winkelwagentje staan. Als u de prevalidatie echter overslaat, kunnen klanten deze zien _uit voorraad_ fouten in het uitcheckproces. Opties: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Algemeen | Wanneer ingesteld op `Yes`, worden de inventarisgegevens aangepast aan de wijzigingen in de catalogus (zoals de verwijdering van producten, wijzigingen in productSKU en wijzigingen in producttypen) en wordt de consistentie tussen de inventaris en de catalogus gehandhaafd. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Product Stock Options]

![Opties voor productvoorraad](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Algemeen | Hiermee bepaalt u of u de volledige voorraadcontrole gebruikt om de items in uw catalogus te beheren. Opties: <br/>**Ja** - Hiermee activeert u de volledige voorraadcontrole om het aantal objecten te volgen dat momenteel in voorraad is. <br/>**Nee** - traceert niet het aantal objecten dat momenteel in voorraad is. |
| [!UICONTROL Backorders] | Algemeen | Hiermee bepaalt u hoe de winkel de achtergronden beheert. Een backorder verandert de verwerkingsstatus van de order niet. Geldmiddelen worden nog steeds onmiddellijk toegestaan of vastgelegd wanneer de bestelling wordt geplaatst, ongeacht of het product in voorraad is. Zodra het product beschikbaar is, wordt het verzonden. Opties: <br/>**Geen achtergronden** - Accepteert geen backorders wanneer het product uit voorraad is. <br/>**Aantal onder 0 toestaan** - Accepteert backorders als de hoeveelheid onder nul daalt. <br/>**Aantal onder 0 toestaan en klant op de hoogte stellen** - Accepteert backorders wanneer het aantal onder nul daalt, maar waarschuwt klanten dat de orders nog kunnen worden geplaatst. |
| [!UICONTROL Use deferred Stock update] | Algemeen | ![Adobe Commerce](../../assets/adobe-logo.svg) (Alleen Adobe Commerce) Hiermee wordt bepaald of voorraadupdate moet worden uitgesteld als backorders zijn toegestaan (de _Achterste bestellingen_ is ingesteld op alles behalve `No backorders` standaardwaarde). Het werkt voor één product of voor een hele website en gebruikt de _Taakwachtrij_ mechanisme om de inventariskwantitatieve indicatoren na de plaatsing van de orders asynchroon te laten bijwerken. Deze optie werkt ook met [Asynchrone orderplaatsing](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) in combinatie met [Inventory management](../../inventory-management/introduction.md). |
| Maximale toegestane hoeveelheid in winkelwagentje | Algemeen | Hiermee bepaalt u het maximumaantal producten dat in één bestelling kan worden aangeschaft. Standaard is de maximale hoeveelheid ingesteld op 10.000. |
| [!UICONTROL Out-of-Stock Threshold] | Algemeen | Hiermee wordt bepaald op welk voorraadniveau een product als niet in voorraad wordt beschouwd. Opties: <br/>**Positief bedrag** - met _Achtergronden_ uitgeschakeld, geeft u een positieve waarde op. Als Achterorden ingeschakeld, wordt deze hoeveelheid genegeerd. <br/>**Nul** - met _Achtergronden_ ingeschakeld, invoeren `0` staat voor oneindige achterorden toe. <br/>**Negatief bedrag** - met _Achtergronden_ We raden u aan een negatief bedrag in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld -50 in om bestellingen tot dit bedrag toe te staan. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Algemeen | Bepaalt het minimumbedrag van een punt dat voor aankoop volgens klantengroep beschikbaar is. Standaard is de minimale hoeveelheid ingesteld op 1. Klikken **[!UICONTROL Add Minimum Qty]** om een verschillende waarde voor een specifieke klantengroep in te gaan. |
| [!UICONTROL Notify for Quantity Below] | Algemeen | Hiermee wordt bepaald op welk niveau de inventarisatie onder de drempelwaarde is gedaald. |
| [!UICONTROL Enable Qty Increments] | Algemeen | Hiermee bepaalt u of objecten in hoeveelheden kunnen worden verkocht. Opties: `Yes` / `No` |
| [!UICONTROL Qty Increments] | Algemeen | Hiermee wordt het aantal producten vastgesteld waaruit een verhoging van de hoeveelheid bestaat. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Algemeen | Hiermee wordt bepaald of objecten die in creditnota&#39;s zijn opgenomen automatisch worden geretourneerd naar de voorraad. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Admin Bulk Operations]

![Bulkbewerkingen voor beheerders](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>Configureren en ondersteunen **asynchrone rijmanagers** moet u de opdrachtregel gebruiken. Hiervoor kan hulp van ontwikkelaars nodig zijn. Zie [Gebruikers in de wachtrij met berichten starten](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) in de _Configuratiegids_.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Algemeen | Hiermee wordt bepaald of bulkbewerkingen asynchroon worden uitgevoerd voor acties voor grote producten, waaronder [bulkgoederen](../../inventory-management/bulk-assignment.md) bronnen toewijzen, bronnen ongedaan maken en [voorraad overbrengen naar bron](../../inventory-management/inventory-transfer.md). Het verzamelt bulkacties tot _[!UICONTROL Asynchronous batch size]_en voert die handelingen uit. Deze functie is standaard uitgeschakeld. We raden u aan de prestaties te evalueren met acties in bulk voordat u deze inschakelt. Opties:<br/>**`Yes`**- Alle bulkbewerkingen uitvoeren voor [!DNL Inventory Management] asynchroon. Om toe te laten, moet u een asynchrone rijmanager vormen.<br/>**`No`**- Standaard. Hiermee worden bulkbewerkingen niet asynchroon uitgevoerd. |
| [!UICONTROL Asynchronous batch size] | Algemeen | Set **[!UICONTROL Run asynchronously]** tot `Yes` om een waarde in te voeren voor _[!UICONTROL Asynchronous batch size]_veld. <br/>De standaardbatch-grootte is 100. Wanneer de bulkprocessen dit bedrag bereiken, worden zij uitgevoerd. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Inventory Indexer Settings]

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Algemeen | Hiermee bepaalt u de strategie die wordt gebruikt voor herindexering van voorraden/bronnen. Opties: `Synchronous` / `Asynchronous` (een asynchrone rijmanager moet voor asynchrone wijze worden gevormd) |

>[!NOTE]
>
> Vanwege de afhankelijkheden van voorraadupdates voor de aan bestellingen gerelateerde activiteiten, wordt de voorraadindexering ook geactiveerd bij het opslaan van het product, ongeacht de `Synchronous` of `Asynchronous` instellen.


{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Distance Provider for Distance Based SSA]

![Leveranciers van afstand voor Op afstand gebaseerde SSA](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Provider] | Algemeen | Bepaalt de leverancier om voor het Algoritme van de Selectie van de Bron van de Prioriteit van de Afstand te gebruiken. Deze functie is standaard ingeschakeld. Opties: <br/>**`Google MAP`**- Gebruikt Google-services om de afstand en tijd tussen het verzendadres en de bronlocatie (adres en GPS-coördinaten) te berekenen. Voor deze optie is een Google API-sleutel vereist en de kosten kunnen via Google worden berekend.<br/>**`Offline Calculation`** - Berekent de afstand gebruikend een ingebedde gegevensbestand om de dichtste bron aan het verzendende bestemmingsadres te bepalen. Als u deze optie wilt gebruiken, hebt u mogelijk hulp van ontwikkelaars nodig om eerst de inhoud van de databaselocatie te downloaden voor alle landen die u verzendt naar een opdrachtregel. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google Distance Provider]

![Google Distance Provider](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Google API key] | Algemeen | Voer de Google API-sleutel voor de Google MAP-provider in. De toets is afkomstig van de [!DNL Google Maps Platform] en moet [!DNL Geocoding API] en [!DNL Distance Matrix API] ingeschakeld. Zie voor meer informatie [Het algoritme voor prioriteitsafstand configureren](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) in de _Inventory management Guide_. |
| [!UICONTROL Computation mode] | Algemeen | Bepaalt de richtingen en de wegen om de afstand van het het verschepen adres en alle bronnen te berekenen die aan de voorraad worden toegewezen. Voor berekeningen wordt standaard de rijmodus gebruikt. Opties: <br/>**`Driving`**- Standaardinstelling, vraagt om standaardrijrichtingen met behulp van het wegennet.<br/>**`Walking`** - Verzoekt lopende richtingen met gebruik van voetgangerspaden en zijdealen (indien beschikbaar). <br/>**`Bicycling`**- Verzoekt fietsrichtingen met fietspaden en de voorkeurstraten (momenteel alleen beschikbaar in de VS en sommige Canadese steden). |
| [!UICONTROL Value] | Algemeen | Geeft aan wat er moet worden berekend en geretourneerd voor de afstand en tijd van de bronlocaties naar het verzendadres. Het algoritme van de Prioriteit van de Afstand adviseert de bron met de kortste afstand of de tijd aan het verzendende bestemmingsadres, dat sneller en misschien goedkoper levert om verzendingen te vervullen. Opties: <br/>**`Distance`**- Geeft als resultaat de afstand tussen punten in metriek (kilometers en meters) of imperial (mijlen en voeten).<br/>**`Time to Destination`** - Geeft de tijd die nodig is om van de bronlocaties naar het verzendadres te gaan in uren en minuten. |

{:style=&quot;table-layout:auto&quot;}
