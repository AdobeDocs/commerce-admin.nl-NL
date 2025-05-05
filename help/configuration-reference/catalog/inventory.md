---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] van Commerce Admin.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] voor Adobe Commerce en Magento Open Source biedt u de tools om uw productvoorraad te beheren. Handelaars met één winkel kunnen deze functies gebruiken om de verkoop en de verzending van goederen te voltooien. Voor meer informatie over deze eigenschappen en hoe u hen kunt gebruiken om voorraad in veelvoudige plaatsen te beheren, zie de [_[!DNL Inventory Management] Gids van de Gebruiker _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![ Opties van de Voorraad ](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Algemeen | Indien ingesteld op `Yes` , wordt de hoeveelheid in voorraad verminderd wanneer de volgorde wordt geplaatst. Met _beheer toegelaten Voorraad_, zijn de reserveringen ingegaan voor de bevolen producten en de hoeveelheden. Opties: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Winkelweergave | Indien ingesteld op `Yes` , wordt het item geretourneerd naar de voorraad wanneer de volgorde wordt geannuleerd. Met _beheer toegelaten Voorraad_, wordt de reserve ontruimd voor de geannuleerde producten en de hoeveelheden. Opties: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Algemeen | Indien ingesteld op `Yes` , worden producten weergegeven die niet langer in voorraad zijn. Als productwaarschuwingen ook zijn ingeschakeld, kunnen klanten zich aanmelden om op de hoogte te worden gesteld wanneer het product beschikbaar komt. Opties: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Website | Hiermee stelt u de drempel voor het `Only x left` -bericht in. Bijvoorbeeld, als reeks aan 3, verschijnt het bericht wanneer er drie of minder van een punt in voorraad zijn. Het bericht wordt niet weergegeven als de waarde is ingesteld op `0` . |
| [!UICONTROL Display products availability in Stock on Storefront] | Winkelweergave | Indien ingesteld op `Yes` , wordt een `In Stock` - of `Out of Stock` -bericht weergegeven op de productpagina. Opties: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Algemeen | Hiermee wordt bepaald of een inventariscontrole wordt uitgevoerd bij het laden van een product in de winkelwagen. Als u deze voorraadcontrole uitschakelt, kunnen de prestaties voor de afhandelingsstappen verbeteren, met name wanneer er veel items in het winkelwagentje staan. Nochtans, als u pre-bevestiging overslaat, konden de klanten _uit voorraad_ fouten later in het controleproces zien. Opties: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Algemeen | Als u deze optie instelt op `Yes` , worden de inventarisgegevens aangepast aan de wijzigingen in de catalogus (zoals de verwijdering van het product, wijzigingen in de SKU-indeling van het product en wijzigingen in het producttype) en blijft de consistentie tussen inventaris en catalogus behouden. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![ Opties van de Voorraad van het Product ](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Algemeen | Hiermee bepaalt u of u de volledige voorraadcontrole gebruikt om de items in uw catalogus te beheren. Opties: <br/>**ja** - activeert volledige inventariscontrole om het aantal punten momenteel in voorraad te volgen. <br/>**Nr** - volgt niet het aantal punten momenteel in voorraad. |
| [!UICONTROL Backorders] | Algemeen | Hiermee bepaalt u hoe de winkel de achtergronden beheert. Een backorder verandert de verwerkingsstatus van de order niet. Geldmiddelen worden nog steeds onmiddellijk toegestaan of vastgelegd wanneer de bestelling wordt geplaatst, ongeacht of het product in voorraad is. Zodra het product beschikbaar is, wordt het verzonden. Opties: <br/>**Geen Achterorden** - keurt geen achterorden goed wanneer het product uit voorraad is. <br/>**staat Aantal onder 0** toe - keurt achterorden goed wanneer de hoeveelheid onder nul daalt. <br/>**staat Aantal onder 0 toe en deelt Klant** mee - keurt backorders goed wanneer het aantal onder nul daalt, maar deelt klanten mee dat de orden nog kunnen worden geplaatst. |
| [!UICONTROL Use deferred Stock update] | Algemeen | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt of om voorraadupdate uit te stellen als de achterorden worden toegestaan (de _Achterorden_ optie wordt geplaatst aan om het even wat naast de `No backorders` standaardwaarde). Het werkt voor één enkel product of een volledige website, en gebruikt het _mechanisme van de Rij van de 0&rbrace; Baan &lbrace;om de indicatoren van de inventarishoeveelheid toe te staan om asynchroon bij te werken nadat de orden worden geplaatst._ Deze optie werkt ook met [ Asynchrone ordeplaatsing ](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) in combinatie met [ Inventory management ](../../inventory-management/introduction.md). |
| Maximale toegestane hoeveelheid in winkelwagentje | Algemeen | Hiermee bepaalt u het maximumaantal producten dat in één bestelling kan worden aangeschaft. Standaard is de maximale hoeveelheid ingesteld op 10.000. |
| [!UICONTROL Out-of-Stock Threshold] | Algemeen | Hiermee wordt bepaald op welk voorraadniveau een product als niet in voorraad wordt beschouwd. Opties: <br/>**Positieve hoeveelheid** - met _Gehandicapte Achterorden_, ga een positieve hoeveelheid in. Als Achterorden ingeschakeld, wordt deze hoeveelheid genegeerd. <br/>**Nul** - met _toegelaten Achterorden_, die `0` ingaan staat voor oneindige achterorden toe. <br/>**Negatieve hoeveelheid** - met _Toegelaten Achterorden_, adviseren wij het ingaan van een negatief bedrag. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld -50 in om bestellingen tot dit bedrag toe te staan. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Algemeen | Bepaalt het minimumbedrag van een punt dat voor aankoop volgens klantengroep beschikbaar is. Standaard is de minimale hoeveelheid ingesteld op 1. Klik op **[!UICONTROL Add Minimum Qty]** om een andere waarde voor een specifieke klantengroep in te voeren. |
| [!UICONTROL Notify for Quantity Below] | Algemeen | Hiermee wordt bepaald op welk niveau de inventarisatie onder de drempelwaarde is gedaald. |
| [!UICONTROL Enable Qty Increments] | Algemeen | Hiermee bepaalt u of objecten in hoeveelheden kunnen worden verkocht. Opties: `Yes` / `No` |
| [!UICONTROL Qty Increments] | Algemeen | Hiermee wordt het aantal producten vastgesteld waaruit een verhoging van de hoeveelheid bestaat. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Algemeen | Hiermee wordt bepaald of objecten die in creditnota&#39;s zijn opgenomen automatisch worden geretourneerd naar de voorraad. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![ BevestigingVerrichtingen van Admin ](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>Om **asynchrone rijmanagers** te vormen en te steunen, moet u de bevellijn gebruiken. Hiervoor kan hulp van ontwikkelaars nodig zijn. Zie [ de gebruikers van de het berichtrij van het Begin ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) in de _Gids van de Configuratie_.

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Algemeen | Bepaalt als u bulkverrichtingen asynchroon voor de acties van het massaproduct met inbegrip van [ bulkgoederen ](../../inventory-management/bulk-assignment.md) toewijst, bronnen unassign, en [ overdrachtinventaris aan bron ](../../inventory-management/inventory-transfer.md) in werking stelt. De bulkacties worden verzameld tot aan _[!UICONTROL Asynchronous batch size]_, dan stelt die acties in werking. Deze functie is standaard uitgeschakeld. We raden u aan de prestaties te evalueren met acties in bulk voordat u deze inschakelt. Opties:<br/>**`Yes`**- hiermee worden alle bulkbewerkingen voor [!DNL Inventory Management] asynchroon uitgevoerd. Om toe te laten, moet u een asynchrone rijmanager vormen.<br/>**`No`**- Standaard. Hiermee worden bulkbewerkingen niet asynchroon uitgevoerd. |
| [!UICONTROL Asynchronous batch size] | Algemeen | Stel **[!UICONTROL Run asynchronously]** in op `Yes` om een waarde voor het veld _[!UICONTROL Asynchronous batch size]_&#x200B;in te voeren. <br/> de standaardpartijgrootte is 100. Wanneer de bulkprocessen dit bedrag bereiken, worden zij uitgevoerd. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Algemeen | Hiermee bepaalt u de strategie die wordt gebruikt voor herindexering van voorraden/bronnen. Opties: `Synchronous` / `Asynchronous` (voor de asynchrone modus moet een asynchrone rijmanager zijn geconfigureerd) |

{style="table-layout:auto"}

>[!NOTE]
>
> Wegens de afhankelijkheden van voorraadupdates voor de aan orde gerelateerde activiteiten, wordt de voorraadindexer ook teweeggebracht op product sparen, ongeacht `Synchronous` of `Asynchronous` het plaatsen.


## [!UICONTROL Distance Provider for Distance Based SSA]

![ Leveranciers van de Afstand voor Afstand Gebaseerde SSA ](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Provider] | Algemeen | Determines the provider to use for the Distance Priority Source Selection Algorithm. Deze functie is standaard ingeschakeld. Opties: <br/>**`Google MAP`**- gebruikt Google-services om de afstand en tijd te berekenen tussen het verzendadres en de bronlocatie (adres en GPS-coördinaten). Voor deze optie is een Google API-sleutel vereist en de kosten kunnen via Google worden berekend.<br/>**`Offline Calculation`** - Berekent de afstand gebruikend een ingebedde gegevensbestand om de dichtste bron aan het verzendende bestemmingsadres te bepalen. Als u deze optie wilt gebruiken, hebt u mogelijk hulp van ontwikkelaars nodig om eerst de inhoud van de databaselocatie te downloaden voor alle landen die u verzendt naar een opdrachtregel. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![ Leverancier van de Afstand van Google ](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Google API key] | Algemeen | Voer de Google API-sleutel voor de Google MAP-provider in. De toets is afkomstig uit [!DNL Google Maps Platform] en moet [!DNL Geocoding API] en [!DNL Distance Matrix API] hebben ingeschakeld. Voor details, zie [ het Prioritaire Algoritme van de Afstand ](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) in de _Gids van Inventory management_ vormen. |
| [!UICONTROL Computation mode] | Algemeen | Bepaalt de richtingen en de wegen om de afstand van het het verschepen adres en alle bronnen te berekenen die aan de voorraad worden toegewezen. Voor berekeningen wordt standaard de rijmodus gebruikt. Opties: <br/>**`Driving`**- standaardinstelling, vraagt standaard rijrichtingen aan via het wegennetwerk.<br/>**`Walking`** - Verzoekt lopende richtingen met gebruik van voetgangerspaden en zijkanten (indien beschikbaar). <br/>**`Bicycling`**- Verzoekt fietsrichtingen met fietspaden en de voorkeurstraten (momenteel alleen beschikbaar in de VS en sommige Canadese steden). |
| [!UICONTROL Value] | Algemeen | Geeft aan wat er moet worden berekend en geretourneerd voor de afstand en tijd van de bronlocaties naar het verzendadres. Het algoritme van de Prioriteit van de Afstand adviseert de bron met de kortste afstand of de tijd aan het verzendende bestemmingsadres, dat sneller en misschien goedkoper levert om verzendingen te vervullen. Opties: <br/>**`Distance`**- Geeft de afstand tussen punten in metriek (kilometers en meters) of imperial (mijlen en voeten).<br/>**`Time to Destination`** - Geeft de tijd die nodig is om van de bronlocaties naar het verzendadres te gaan in uren en minuten. |

{style="table-layout:auto"}
