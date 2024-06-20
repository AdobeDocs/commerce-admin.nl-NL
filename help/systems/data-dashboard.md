---
title: Gegevensbeheerdashboard
description: Leer hoe u toegang krijgt tot inzichten over gegevensstromen voor [!DNL Catalog Service], [!DNL Live Search], en [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: e883a678885aefaf832cece431e458c5d7741c40
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Gegevensbeheerdashboard

Het gegevensbeheerdashboard biedt een overzicht van de synchronisatiestatus voor productgegevens die van de Commerce-database naar Commerce SaaS-services worden overgedragen. Gebruikers kunnen de status van productsynchronisatie eenvoudig controleren en de synchronisatie van gegevens via een uniform dashboard starten. Deze functie biedt waardevolle inzichten in de beschikbaarheid van productgegevens voor uw winkel, zodat deze direct aan uw klanten kunnen worden weergegeven.

## Publiek

Het gegevensbeheerdashboard is zonder extra kosten beschikbaar voor alle Commerce-handelaren die [[!DNL Product Recommendations]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview), of [[!DNL Catalog Service]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) met een actieve licentie.

Het gegevensbeheerdashboard bevindt zich op *Systeem* > Gegevensoverdracht > *Gegevensbeheerdashboard*.

![Gegevensbeheerdashboard](assets/data-management-dashboard.png)

Het dashboard bevat de volgende velden:

| Veld | Beschrijving |
|--- |--- |
| Toepassingsgebied | Specifieke website voor de gesynchroniseerde gegevens. |
| [!DNL Product Recommendations] | Hiermee geeft u de synchronisatiestatus, het aantal gesynchroniseerde producten en een tabel van de [weergavebaar](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) gesynchroniseerde producten voor [!DNL Product Recommendations]. |
| [!DNL Live Search] | Hiermee geeft u de synchronisatiestatus, het aantal gesynchroniseerde producten en een tabel van de [weergavebaar](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) gesynchroniseerde producten voor [!DNL Live Search]. |
| [!DNL Catalog Service] | Hiermee geeft u de synchronisatiestatus, het aantal gesynchroniseerde producten en een tabel met de gesynchroniseerde producten weer voor [!DNL Catalog Service]. |
| Instellingen | Hiermee opent u een dialoogvenster waarin u [De catalogusgegevens handmatig opnieuw synchroniseren](#resync-catalog-data). |
| Synchronisatiestatus | Toont het aantal producten die van het gegevensbestand van Commerce aan om het even welke diensten SaaS binnen de laatste drie uren zijn overgebracht. Als u uw catalogus niet vaak bijwerkt, is deze waarde vaak nul. Als er een synchronisatie wordt uitgevoerd, klikt u op **[!UICONTROL Refresh]** om een bijgewerkt aantal te krijgen. |
| Aantal producten | Geeft het totale aantal catalogusproducten weer dat beschikbaar is voor de service. De [!DNL Product Recommendations] en [!DNL Live Search] het totale aantal dashboards wordt weergegeven _weergavebaar_ producten. [!DNL Catalog Service] filtert producten niet door weergave, dus als u beide [!DNL Catalog Service] en [!DNL Live Search] of [!DNL Product Recommendations] als deze optie is geïnstalleerd, kunnen op de twee dashboards twee verschillende waarden voor het aantal producten worden weergegeven. |
| Gesynchroniseerde producten | Verstrekt details over de producten in de kernCommerce index. Deze tabel wordt standaard gesorteerd op Laatst bijgewerkt. Als u een specifiek product wilt zoeken, gebruikt u de **[!UICONTROL Search by SKU]** veld. Klik op **[!UICONTROL Customize Table]** rechts van de tabel. |

## Het dashboard voor gegevensbeheer gebruiken

Wanneer u producten in de Commerce-database bijwerkt, worden de productgegevens naar SaaS-services overgebracht volgens uw systeemconfiguratie. Wanneer het synchronisatieproces wordt gestart, **Aantal producten** Hiermee wordt het aantal producten aangegeven dat naar SaaS-services wordt verzonden.

>[!IMPORTANT]
>
>De tijd die nodig is om de synchronisatie te voltooien, is afhankelijk van de grootte van de catalogus en het volume van de bijgewerkte gegevens.

Als het aantal verwerkte producten overeenkomt met het aantal bijgewerkte producten, geeft dit aan dat de synchronisatie is voltooid.

>[!NOTE]
>
>Adobe verstrekt ook een bevel-lijn interface en systeemlogboeken die de ontwikkelaars en systeemintegrators kunnen gebruiken om synchronisatieverrichtingen te beheren en te volgen en fouten voor de diensten van Commerce op te lossen SaaS. Zie voor meer informatie de [Handleiding voor het exporteren van SaaS-gegevens](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Lijst van gesynchroniseerde producten

Als u de details van een gesynchroniseerd product wilt zien, klikt u op het product in de tabel.

![Productgegevens synchroniseren](assets/sync-product-detail.png)

### Catalogusgegevens opnieuw synchroniseren

Om ervoor te zorgen dat uw Commerce SaaS-services altijd up-to-date zijn met de nieuwste productinformatie, moet u [een schema implementeren](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) voor het synchroniseren van catalogusgegevens.

Terwijl u [handmatig](#manually-resync-catalog) Als de gegevens uit de catalogus van de Commerce-database naar SaaS-services worden gesynchroniseerd, wordt dit niet aanbevolen, omdat hierdoor de belasting van hardwarebronnen kan toenemen. In de volgende gevallen kan het echter nodig zijn de catalogus handmatig opnieuw te synchroniseren:

- Telkens wanneer er belangrijke wijzigingen in uw productcatalogus worden aangebracht, zoals het toevoegen van nieuwe producten, het bijwerken van productdetails of het wijzigen van categorieën

- Als er discrepanties of prestatieproblemen optreden bij de weergave van productgegevens op uw winkels

- Na eventuele updates of wijzigingen in de integratie tussen de Commerce-database en SaaS-services

- Wanneer het opstellen van aanpassingen of configuraties die productgegevensbeheer of synchronisatieprocessen beïnvloeden

Door deze richtlijnen na te leven en zo nodig catalogusgegevens proactief te synchroniseren, kunt u de consistentie, nauwkeurigheid en betrouwbaarheid van gegevens in uw Adobe Commerce-ecosysteem behouden.

#### Catalogus handmatig opnieuw synchroniseren

Als u de catalogusgegevens opnieuw moet synchroniseren, klikt u op **[!UICONTROL Settings]** aan de rechterkant van de pagina om een dialoogvenster weer te geven waarin u een resync kunt starten. Door het opnieuw synchroniseren van catalogusgegevens wordt de service gedwongen gegevens van de Commerce-database te zoeken naar SaaS-services.

![Producten handmatig synchroniseren](assets/resync-data.png)
