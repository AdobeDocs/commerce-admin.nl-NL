---
title: Gegevensbeheerdashboard
description: Leer hoe te om tot inzichten over gegevensstromen voor  [!DNL Catalog Service],  [!DNL Live Search], en  [!DNL Product Recommendation] toegang te hebben.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 4495a27b57c04c6f9c37b2c5237b5f2233cc8532
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Gegevensbeheerdashboard

Het gegevensbeheerdashboard biedt een overzicht van de synchronisatiestatus voor productgegevens die van de Commerce-database naar Commerce SaaS-services worden overgedragen. Gebruikers kunnen de status van productsynchronisatie eenvoudig controleren en de synchronisatie van gegevens via een uniform dashboard starten. Deze functie biedt waardevolle inzichten in de beschikbaarheid van productgegevens voor uw winkel, zodat deze direct aan uw klanten kunnen worden weergegeven.

## Publiek

Het dashboard van het Beheer van Gegevens is beschikbaar aan alle verkopers van Commerce die [[!DNL Product Recommendations v6.0.0] gebruiken ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0] ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview), of [[!DNL Catalog Service v1.17] ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) met een actieve vergunning.

Het dashboard van het Beheer van Gegevens wordt gevestigd bij *Systeem* > Overdracht van Gegevens > *Dashboard van het Beheer van Gegevens*.

![ Dashboard van het Beheer van Gegevens ](assets/data-management-dashboard.png)

Het dashboard bevat de volgende velden:

| Veld | Beschrijving |
|--- |--- |
| Toepassingsgebied | Specifieke website voor de gesynchroniseerde gegevens. |
| [!DNL Product Recommendations] | De synchronisatiestatus van vertoningen, aantal gesynchroniseerde producten, en een lijst van [ toonbare ](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) producten voor [!DNL Product Recommendations]. |
| [!DNL Live Search] | De synchronisatiestatus van vertoningen, aantal gesynchroniseerde producten, en een lijst van [ toonbare ](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) producten voor [!DNL Live Search]. |
| [!DNL Catalog Service] | Geeft de synchronisatiestatus, het aantal gesynchroniseerde producten en een tabel met de gesynchroniseerde producten voor [!DNL Catalog Service] weer. |
| Instellingen | Opent een dialoog waar u [ kunt manueel de catalogusgegevens ](#resync-catalog-data) opnieuw synchroniseren. |
| Synchronisatiestatus | Toont het aantal producten die van het gegevensbestand van Commerce aan om het even welke diensten SaaS binnen de laatste drie uren zijn overgebracht. Als u uw catalogus niet vaak bijwerkt, is deze waarde vaak nul. Als een synchronisatie bezig is, klikt u op **[!UICONTROL Refresh]** om een bijgewerkt aantal op te halen. |
| Aantal producten | Geeft het totale aantal catalogusproducten weer dat beschikbaar is voor de service. De [!DNL Product Recommendations] en [!DNL Live Search] dashboards tonen het totale aantal _toonbare_ producten. [!DNL Catalog Service] filtert producten niet door deze weer te geven. Als u zowel [!DNL Catalog Service] als [!DNL Live Search] of [!DNL Product Recommendations] hebt geïnstalleerd, is het mogelijk dat de twee dashboards twee verschillende waarden voor het aantal producten tonen. |
| Gesynchroniseerde producten | Verstrekt details over de producten in de kernCommerce index. Deze tabel wordt standaard gesorteerd op Laatst bijgewerkt. Gebruik het veld **[!UICONTROL Search by SKU]** om een specifiek product te zoeken. Als u wilt bepalen welke kolommen worden weergegeven, klikt u op **[!UICONTROL Customize Table]** rechts van de tabel. |

## Het dashboard voor gegevensbeheer gebruiken

Wanneer u producten in de Commerce-database bijwerkt, worden de productgegevens naar SaaS-services overgebracht volgens uw systeemconfiguratie. Wanneer het synchronisatieproces in werking stelt, **Telling van het Product** wijst op het aantal producten die naar de diensten SaaS worden verzonden.

>[!IMPORTANT]
>
>De tijd die nodig is om de synchronisatie te voltooien, is afhankelijk van de grootte van de catalogus en het volume van de bijgewerkte gegevens.

Als het aantal verwerkte producten overeenkomt met het aantal bijgewerkte producten, geeft dit aan dat de synchronisatie is voltooid.

>[!NOTE]
>
>Adobe verstrekt ook een bevel-lijn interface en systeemlogboeken die de ontwikkelaars en systeemintegrators kunnen gebruiken om synchronisatieverrichtingen te beheren en te volgen en fouten voor de diensten van Commerce op te lossen SaaS. Voor details, zie de [ Gids van de Uitvoer van Gegevens SaaS ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Lijst van gesynchroniseerde producten

Als u de details van een gesynchroniseerd product wilt zien, klikt u op het product in de tabel.

![ Syncd de Details van het Product ](assets/sync-product-detail.png)

### Catalogusgegevens opnieuw synchroniseren

Om ervoor te zorgen dat uw diensten van Commerce SaaS altijd bijgewerkt met de recentste productinformatie zijn, zou u een programma ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) voor het synchroniseren van catalogusgegevens [ moeten uitvoeren.

Terwijl u [ ](#manually-resync-catalog) manueel kunt in werking stellen catalogusgegevens resync van het gegevensbestand van Commerce aan de diensten SaaS, wordt het niet geadviseerd aangezien het de lading op hardwaremiddelen kan verhogen. In de volgende gevallen kan het echter nodig zijn de catalogus handmatig opnieuw te synchroniseren:

- Telkens wanneer er belangrijke wijzigingen in uw productcatalogus worden aangebracht, zoals het toevoegen van nieuwe producten, het bijwerken van productdetails of het wijzigen van categorieën

- Als er discrepanties of prestatieproblemen optreden bij de weergave van productgegevens op uw winkels

- Na eventuele updates of wijzigingen in de integratie tussen de Commerce-database en SaaS-services

- Wanneer het opstellen van aanpassingen of configuraties die productgegevensbeheer of synchronisatieprocessen beïnvloeden

Door deze richtlijnen na te leven en zo nodig catalogusgegevens proactief te synchroniseren, kunt u de consistentie, nauwkeurigheid en betrouwbaarheid van gegevens in uw Adobe Commerce-ecosysteem behouden.

#### Catalogus handmatig opnieuw synchroniseren

Als u de catalogusgegevens opnieuw moet synchroniseren, klikt u op **[!UICONTROL Settings]** aan de rechterkant van de pagina om een dialoogvenster weer te geven waarin u een resync kunt starten. Door het opnieuw synchroniseren van catalogusgegevens wordt de service gedwongen gegevens van de Commerce-database te zoeken naar SaaS-services.

![ synchroniseer manueel Producten ](assets/resync-data.png)
