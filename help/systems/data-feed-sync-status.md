---
title: Statuscontrole gegevensinvoer
description: De synchronisatie van de gegevensuitvoer van de monitor en identificeert om het even welke kwesties of vertragingen met voederverwerking voor  [!DNL Catalog Service],  [!DNL Live Search], en  [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 4cc5f5842e772ead9785b8280557a7b5b8f26419
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 0%

---


# Statuscontrole gegevensinvoer

Adobe Commerce-beheerders kunnen de synchronisatiestatus controleren van gegevens die vanuit Adobe Commerce naar verbonden Commerce-services zijn geëxporteerd via de statuspagina voor gegevensinvoer in Commerce Admin.

![&#x200B; de detailpagina van de Status van de Synchronisatie van het Gegeven van Gegevens met de status van het voederpunt rapporterend &#x200B;](assets/data-feed-sync-status.png)

Deze pagina biedt realtime inzichten in de gezondheid en prestaties van gegevensexportfeeds die product- en categoriegegevens van Commerce overbrengen naar externe services zoals [!DNL Product Recommendations] , [!DNL Live Search] en [!DNL Catalog Service] .

Op de statuspagina voor synchroniseren wordt alleen de exportstatus weergegeven. Een successtatus geeft aan dat de gegevens zijn geëxporteerd en uiteindelijk beschikbaar zijn in verbonden Commerce-services. Gebruik het [&#x200B; dashboard van het gegevensbeheer &#x200B;](data-dashboard.md) om de daadwerkelijke staat van entiteitsynchronisatie te zien.

Door de status van de feed te controleren, bent u verzekerd van consistentie bij de gegevens en kunt u problemen die zich tijdens het exportproces voordoen, snel oplossen. Beheerders kunnen:

* **Mening de synchronisatiestatus** voor alle gegevensvoer
* **identificeer en los fouten** in voederverwerking problemen op
* **toegang gedetailleerde statusinformatie** voor individuele voederpunten

De status wordt bijgehouden voor de volgende feeds:

* Producten
* Productkenmerken Feed
* Diervoeders voor categorieën
* Feed met productoverschrijvingen
* Diervoeders productprijzen
* Diervoeders voor productvarianten

>[!TIP]
>
>Om meer over het proces van de gegevenssynchronisatie te leren, zie [&#x200B; gegevens met SaaS- gegevensuitvoer &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization) in de *Gids van de Uitvoer van Gegevens SaaS* synchroniseren.

## De extensie installeren

De pagina Status gegevensfeed is beschikbaar voor alle Commerce-handelaren met actieve licenties voor de volgende Commerce-services:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+] &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) met een actieve vergunning.

**Vereisten**

* PHP 8.1, 8.2, 8.3 of 8.4
* Adobe Commerce 2.4.4+
* [&#x200B; de Uitbreiding van de Uitvoer van Gegevens van Adobe Commerce &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension), versie 103.4.15 of later
* Toegang tot [&#x200B; repo.magento.com &#x200B;](https://repo.magento.com)

  Om sleutels te produceren en de noodzakelijke rechten te verkrijgen, zie [&#x200B; uw authentificatiesleutels &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) krijgen. Voor wolkeninstallaties, zie [&#x200B; Commerce op de Gids van de Infrastructuur van de Wolk &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Toegang tot de opdrachtregel van de Adobe Commerce-toepassingsserver.

### Installatiestappen

Voeg de module `magento/module-data-exporter-status` toe met behulp van Composer:

```shell
composer require magento/module-data-exporter-status
```

Raadpleeg de volgende handleidingen voor gedetailleerde installatiestappen:

* [&#x200B; installeer uitbreiding op Adobe Commerce op de Infrastructuur van de Wolk &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [&#x200B; installeer uitbreiding Adobe Commerce op-gebouw &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## De statuspagina van de gegevensfeed openen

Open vanuit Commerce Admin de statuspagina voor gegevensinvoer via Commerce Admin op **[!DNL System]** > Gegevensoverdracht > **[!DNL Data Feed Sync Status]** .

![&#x200B; de pagina van de Status van de Synchronisatie van het Gegevensvoer die gegevens samenvatten voer uitvoeractiviteit &#x200B;](assets/data-feed-sync-status.png)

De controle van de Status van de Diervoeders van gegevens verstrekt twee interfaces:

* De [&#x200B; overzichtspagina van de Status van de Synchronisatie van het Gegeven van Gegevens &#x200B;](#data-feed-sync-status-summary) die van de beschikbare voer en huidige staat een lijst maakt
* De [&#x200B; Status van de Synchronisatie van het Gegeven van Gegevens - de pagina van Details &#x200B;](#data-feed-sync-status-details) die gedetailleerde informatie over een geselecteerde voer toont.

## Overzicht van status bij synchronisatiestatus gegevensfeed

De overzichtspagina van de Status van de Synchronisatie van het voer verstrekt informatie over de de uitvoeractiviteit van de gegevenstoevoer met inbegrip van de volgende informatie:

| Veld | Beschrijving |
|-------|-------------|
| **Naam van het voer** | De naam van de voederindexeerder die verantwoordelijk is voor het synchroniseren van een specifieke entiteit of een onderdeel daarvan, bijvoorbeeld de product- of productprijs. |
| **de Verslagen van Source** | Aantal records dat beschikbaar is voor export uit de Commerce-database. Dit nummer kan groter zijn dan het aantal records dat in Commerce Admin wordt weergegeven, omdat elk feed-item tot een specifiek bereik behoort, zoals de code voor winkelweergave. |
| **met succes Verzonden Verslagen** | Aantal records dat naar Commerce SaaS is verzonden voor verdere verwerking. Als de fouten tijdens transmissie voorkwamen, het aantal verslagen met succes die aan de externe diensten worden overgebracht. |
| **Ontbroken Verslagen** | Aantal records dat niet is geëxporteerd en dat aandacht vereist. |
| **Actie** | Selecteer **[!UICONTROL Details]** om de synchronisatieactiviteit voor een feed weer te geven. |

## Gegevens over synchronisatiestatus gegevensfeed

Klik op de overzichtspagina Status gegevensfeed op een naam van een feed of gebruik de handeling [!DNL View Details] om toegang te krijgen tot gedetailleerde informatie over afzonderlijke records in een feed.

![[!UICONTROL Data Feed Sync Status - Details] pagina met statusrapportage van feed-item &#x200B;](assets/data-feed-sync-status-details.png)

De detailweergave bevat de volgende informatie voor elk feed-item:

| Veld | Beschrijving |
|-------|-------------|
| **identiteitskaart van het Punt van het voer** | Interne id voor de feed-record |
| **identiteitskaart van de Entiteit** | De id van de bronentiteit (product-id, categorie-id, enzovoort) |
| **de Status van de Uitvoer** | De [&#x200B; synchronisatiestatus &#x200B;](#export-status-types) van het voederpunt. Huidige status van de exportpoging met kleurgecodeerde indicatoren |
| **Laatste Datum van de Synchronisatie** | Tijdstempel wanneer de record voor het laatst naar Commerce Services is verzonden |
| **wordt entiteit geschrapt?** | Geeft aan of de entiteit of haar onderdeel (bijvoorbeeld product- of productprijs) in Adobe Commerce is verwijderd. Items worden alleen weergegeven als er een fout is opgetreden tijdens de synchronisatie. |
| **identiteitskaart van het Verzoek** | Een unieke id voor de synchronisatieaanvraag. Geef deze id door aan Support wanneer het oplossen van problemen met specifieke entiteiten wordt bijgewerkt. |
| **Fout** | Gedetailleerde foutinformatie als het feed-item niet kon worden gesynchroniseerd. |

U kunt de weergave beheren met de volgende besturingselementen:

* [!DNL Mass Action] voor het plannen van de resynchronisatie voor geselecteerde feed-items
* [!DNL Filters]
* [!DNL Default View] om een gefilterde weergave te maken en op te slaan, en te schakelen tussen weergaven
* [!DNL Columns] gebruiken om kolommen in de tabel weer te geven en te verbergen.

### Gezondheidsindicatoren voor diervoeders

Boven aan elke pagina met voederdetails geven kritieke gezondheidsindicatoren de systeemstatus voor elke feed aan:

#### Indexeerstatus

* **Geldig**: Het gegeven wordt gesynchroniseerd; geen vereiste herindex.
* **Ongeldig**: De originele gegevens werden veranderd; de index zou moeten worden bijgewerkt.
* **Verwerking**: Bezig indexerend.

>[!TIP]
>
>Meer over indexverwerking leren, zie het [&#x200B; onderwerp van het Beheer van de Index 0&rbrace;.](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management)

#### Changelog-achterstand

* **allen gesynchroniseerd**: Geen hangende veranderingen om te verwerken
* **Punten in achterstand**: Aantal hangende veranderingen die om wachten worden verwerkt

### Statustypen exporteren

Het systeem verstrekt statusindicatoren om u snel te helpen kwesties identificeren:

#### Statuscategorieën

| **Status** | **Beschrijving** | **Vereiste Actie** |
|--------|-----------|-------------|
| **Voorgelegd aan de dienst** | Voeding is geëxporteerd naar Commerce-service. | Geen |
| **Ontbroken, zal opnieuw proberen** | Tijdelijke fout. Het systeem zal automatisch opnieuw proberen. | Monitor voor resolutie |
| **ontbroken, vereist aandacht** | Mislukt door toepassing of gegevensfout. | Het probleem in de kolom [!DNL Error] onderzoeken en oplossen |
| **wachtend op voorlegging** | In de wachtrij voor uitvoer maar nog niet verwerkt. | Normale verwerkingsstatus |

## Status van gegevensfeed controleren

Wanneer u aan producten en categorieën gerelateerde entiteiten bijwerkt in de Commerce-database, worden de gegevens doorgestuurd naar Commerce-services volgens uw configuratie van de feed. U kunt dit proces in real time controleren van de overzichtspagina van de Status van de Synchronisatie van de Diervoeders van Gegevens.

>[!IMPORTANT]
>
>De tijd die nodig is om de gegevenssynchronisatie te voltooien, is afhankelijk van de grootte van de catalogus, het volume van de bijgewerkte gegevens en de prestaties van de externe service.

Wanneer het aantal met succes verzonden verslagen het aantal bronverslagen aanpast, wijst het erop dat de synchronisatie volledig is en alle gegevens met succes zijn overgebracht.

>[!NOTE]
>
>Adobe biedt ook opdrachtregelinterfacegereedschappen en systeemlogboeken die ontwikkelaars en systeemintegrators kunnen gebruiken om synchronisatiebewerkingen te beheren en bij te houden. Voor details, zie de [&#x200B; Gids van de Uitvoer van Gegevens SaaS &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Mislukte exportbewerkingen beheren

De details van mislukte exporten bekijken en corrigerende maatregelen nemen:

1. Zoek op de statuspagina van Feed Sync naar de feed met mislukte records.
1. Klik op **[!DNL Details]**.

1. Controleer foutberichten voor specifieke mislukkingen.

1. Gebruik massaacties om resync-bewerkingen voor mislukte items te plannen.

### Resync failed data

U kunt mislukte of problematische gegevensfeeds handmatig opnieuw synchroniseren met het menu [!DNL Actions] op de [!DNL Data Feed Sync Status - Details] -pagina.

Terwijl het systeem automatisch bepaalde soorten mislukkingen opnieuw probeert, kan handinterventie in de volgende scenario&#39;s noodzakelijk zijn:

* Er treden verificatie- of machtigingsfouten op (401, 403 statuscodes).
* Na het oplossen van gegevensformaatkwesties die payload fouten veroorzaakten.
* Na updates aan externe de dienstconfiguraties of eindpunten.
* U implementeert aanpassingen die van invloed zijn op het exporteren van gegevens.

Door de status van de feed proactief te controleren en fouten direct aan te pakken, kunt u de consistentie en betrouwbaarheid van gegevens in uw Commerce-ecosysteem behouden.

#### Voedingsitems handmatig opnieuw synchroniseren

Als u specifieke voedingsartikelen opnieuw moet synchroniseren:

1. **Uitgezochte Verslagen**: checkboxes van het gebruik om ontbroken verslagen te selecteren die aandacht vergen.
2. **kies Actie**: Selecteer **[!DNL Schedule Resync]** van de drop-down massageHandeling.
3. **bevestigt**: Klik **[!DNL Submit]** en bevestig de opnieuw synchronisatieverrichting.
4. **Resultaten van de Monitor**: Controleer het succesbericht en controleer statusveranderingen.

## Aanbevolen procedures

### Regelmatig toezicht

1. **Dagelijkse Controles**: Herzie de overzichtspagina dagelijks voor om het even welke voer die hoge mislukkingstarieven tonen
1. **Wekelijks diep Duik**: Onderzoek de gedetailleerde status voor kritieke voer (producten, prijzen)
1. **Maandelijkse Analyse**: De tendensen van het spoor in de uitvoersuccespercentages en prestaties

### Workflow voor probleemoplossing

1. **identificeer Kwesties**: Zoek fouten en hoge mislukkingen tellingen
1. **de Gezondheid van de Indexer van de Controle**: Zorg ervoor dat de indexeerders geldig zijn en de achterstand handelbaar is
1. **Details van de Fout van het Overzicht**: Klik op ontbroken verslagen om specifieke foutenmeldingen te zien
1. **opnieuw synchroniseren van het Programma**: De massa van het gebruik acties om ontbroken uitvoer opnieuw te proberen
1. **Resolutie van de Monitor**: Verifieer dat opnieuw gesynchroniseerde punten succesvolle status tonen

### Algemene problemen verhelpen

#### Hoge foutpercentages

**Symptomen**: Het grote aantal verslagen die &quot;Ontbroken tonen, vereisen aandacht&quot;status

**Potentiële oorzaken**:

* Wijzigingen in externe serviceconfiguratie
* Onverenigbaarheden gegevensformaat
* Verificatie- of machtigingsproblemen

**stappen van de Resolutie**:

1. De externe de dienststatus en configuratie controleren
1. Foutberichten voor patronen controleren
1. Verificatiegegevens verifiëren
1. Indien nodig contact opnemen met de externe service

#### Trage exportprestaties

**Symptomen**: Hoog veranderende achterstand, langzame statusupdates

**Potentiële Oorzaken**:

* Problemen met indexprestaties
* Hoog gegevensvolume
* Beperking van de externe servicetarieven

**Stappen van de Resolutie**:

1. Indexerstatus controleren en opnieuw uitvoeren indien ongeldig
2. De externe de dienstreactietijden van de monitor
3. Overweeg de export tijdens uren buiten de piekuren te plannen
4. Systeembronnen en prestaties controleren

#### Verificatie mislukt

**Symptomen**: 401 of 403 statuscodes

**Stappen van de Resolutie**:

1. API-referenties en tokens controleren
1. De machtigingen voor externe serviceaccounts controleren
1. Verlopen verificatietokens verlengen
1. Neem contact op met uw serviceprovider voor toegangsproblemen

>[!MORELIKETHIS]
>
>* [&#x200B; Dashboard van het Beheer van Gegevens &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [&#x200B; Gids van de Uitvoer van Gegevens SaaS &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
