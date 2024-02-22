---
title: Gegevensbeheerdashboard
description: Leer hoe u inzichten kunt opvragen over gegevensstromen voor Catalog Service, Live Search en Product Recommendations.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Gegevensbeheerdashboard

Het gegevensbeheerdashboard biedt inzicht in gegevensstromen voor Adobe Commerce SaaS-producten. Gebruikers van [!DNL Live Search], [!DNL Product Recommendations], en [!DNL Catalog Service] U kunt de status van productsynchronisatie bekijken en gegevens vanaf één dashboard opnieuw synchroniseren.

Het gegevensbeheerdashboard bevindt zich op *Systeem* > Gegevensoverdracht > *Gegevensbeheerdashboard*.

![Gegevensbeheerdashboard](assets/data-management-dashboard.png)

## Instellingen

De **[!UICONTROL Settings]** aan de rechterkant van de pagina wordt het dialoogvenster geopend waarin u de catalogusgegevens opnieuw kunt synchroniseren.

Het opnieuw synchroniseren van catalogusgegevens dwingt de dienst om gegevens van het gegevensbestand van de Handel te herzoeken. Deze handeling wordt meestal tijdens de eerste instapprocedure gebruikt wanneer de catalogussynchronisatie een paar uur niet is gestart.

## Synchronisatiestatus

De _[!UICONTROL Sync]_het statuspaneel rapporteert het aantal producten dat in de laatste drie uur is gesynchroniseerd. Als u uw catalogus niet vaak bijwerkt, is deze waarde vaak nul. Klikken **[!UICONTROL Refresh]**om de telling te vernieuwen.

## Aantal producten

Het deelvenster Producentelling geeft het totale aantal catalogusproducten weer dat beschikbaar is voor de service.

De [!DNL Product Recommendations] en [!DNL Live Search] het totale aantal dashboards wordt weergegeven _weergavebaar_ producten. [!DNL Catalog Service] filtert producten niet door weergave, dus als u beide [!DNL Catalog Service] en [!DNL Live Search] of [!DNL Product Recommendations] als deze optie is geïnstalleerd, kunnen op de twee dashboards twee verschillende waarden voor het aantal producten worden weergegeven.

## Gesynchroniseerde producten

De tabel Gesynchroniseerde producten bevat gegevens over de producten in de index. Deze tabel wordt standaard gesorteerd op Laatst bijgewerkt.

Als u een specifiek product wilt zoeken, gebruikt u de **[!UICONTROL Search by SKU]** veld .
Klik op **[!UICONTROL Customize Table]** rechts van de tabel.
