---
title: Inleiding tot catalogusbeheer
description: Leer hoe catalogus en productbereik werken in catalogusbeheer.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Inleiding tot catalogusbeheer

Adobe Commerce en Magento Open Source gebruiken de term _catalogus_ de productdatabank als geheel te raadplegen.

Een van de belangrijkste gebieden bij het maken en beheren van uw winkel is het maken van producten en categorieën. Admin verstrekt verscheidene hulpmiddelen die u voor de aanvankelijke opstelling van uw opslag, en voor het handhaven van uw opslag en het optimaliseren van uw zaken gebruikt.

>[!TIP]
>
>Inventory management for Adobe Commerce en Magento Open Source bieden u de tools om uw productvoorraad te beheren. Handelaars met één winkel kunnen deze functies gebruiken om de verkoop en de verzending van goederen te voltooien. Zie voor meer informatie over deze functies en hoe u deze kunt gebruiken om bestanden op meerdere locaties te beheren de [Inventory management-gebruikershandleiding](../inventory-management/introduction.md).

## Catalogusbereik

De toegang tot catalogusgegevens wordt bepaald door verschillende factoren, waaronder [bereik](../getting-started/websites-stores-views.md#scope-settings) instellen, de catalogusconfiguratie en de [hoofdcategorie](category-root.md) die aan de opslag wordt toegewezen. De catalogus bevat producten die zijn ingeschakeld en te koop zijn, en producten die momenteel niet te koop worden aangeboden.

Bij verkoop wordt de term _catalogus_ doorgaans wordt verwezen naar een gekromde selectie van te koop aangeboden producten. Een winkel kan bijvoorbeeld een &#39;Veringscatalogus&#39; en een &#39;Catalogus hervallen&#39; hebben.

Net als de inhoudsopgave van een afgedrukte catalogus, het hoofdmenu van de winkel — of _topnavigatie_ — organiseert producten per categorie, zodat klanten gemakkelijk kunnen vinden wat ze willen. Het hoofdmenu is gebaseerd op een _hoofdcategorie_, die een container is voor het menu dat aan de opslag wordt toegewezen. Omdat de specifieke menuopties op het niveau van de archiefmening worden bepaald, kan elke mening een verschillend hoofdmenu hebben dat op de zelfde wortelcategorie wordt gebaseerd. In elk menu kunt u een gekromde selectie van producten aanbieden die geschikt is voor de winkel.

![Hiërarchiediagram van catalogus](./assets/catalog-hierarchy-scope.svg){width="550"}

## Productbereik

Voor installaties met meerdere websites, winkels en weergaven wordt de [bereik](../getting-started/websites-stores-views.md#scope-settings) met deze instelling bepaalt u waar de producten te koop zijn en welke productinformatie voor elke winkelweergave beschikbaar is. In eerste instantie worden alle producten die u maakt, gepubliceerd naar de standaardwebsite, in de winkel en in de winkelweergave.

![winkeldiagram met meerdere locaties](./assets/scope-multisite.svg){width="550"}

Als u slechts één winkel hebt met de standaardweergave, kunt u uw winkel uitvoeren in [Single Store-modus](../getting-started/websites-stores-views.md#single-store-mode) om de bereikinstellingen te verbergen. Als uw winkel echter meerdere weergaven heeft, wordt onder de naam van elk veld een bereikindicator weergegeven.

- Als u de productinformatie voor een bepaalde weergave wilt bewerken, gebruikt u de _Winkelweergave_ in de linkerbovenhoek om de weergave te kiezen. Aanvullende besturingselementen zijn beschikbaar voor elk veld dat op het niveau van de winkelweergave kan worden bewerkt.

- Als u het bereik van een product in een installatie met meerdere sites wilt definiëren, raadpleegt u de [Product op websites](settings-basic-websites.md) deel van de productinformatie.

Het bewerken van een product voor een winkelweergave is vergelijkbaar met het toevoegen van een laag met productinformatie die specifiek is voor de weergave.

U kunt alleen producten bewerken of toewijzen voor de site waarvoor u machtigingen hebt, niet voor alle sites waarvoor het product is toegewezen.

Hoewel de _Spaans_ de opslagmening wordt geselecteerd in het volgende voorbeeld, verschijnt de productinformatie nog in de originele taal van de standaardarchiefmening. Als u de productinformatie wilt vertalen, moet u overschakelen op de _Spaans_ Sla de weergave op en vertaal de tekstvelden, zoals de producttitel, beschrijving en de metagegevens. Zie voor meer informatie [Producten lokaliseren](../stores-purchase/store-localize.md#localize-products).

## Een product bewerken voor een andere weergave

>[!NOTE]
>
>De _Alle winkelweergaven_ bereik is uitgeschakeld voor Admin-gebruikers die zijn beperkt tot een specifiek bereik wanneer het product ook buiten het toegestane bereik is gepubliceerd. Het eerste bereik dat beschikbaar is voor bewerken is standaard geselecteerd omdat gebruikers met een beperkt aantal functies niet kunnen uitvoeren _globaal_ acties of acties die van invloed zijn op het bereik wanneer zij geen toegang hebben.

1. In de linkerbovenhoek, plaats **[!UICONTROL Store View]** op de specifieke weergave die moet worden bewerkt.

1. Om de bereikwijziging te bevestigen klikt u op **[!UICONTROL OK]**.

1. Werk het veld bij met de nieuwe waarde voor de winkelweergave.

   Onder elk veld dat voor de winkelweergave kan worden bewerkt, wordt een selectievakje weergegeven. Als u de standaardwaarde wilt overschrijven, schakelt u de optie **Standaardwaarde gebruiken** selectievakje.

   ![Productnaam vertalen voor weergave in de Spaanse winkel](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

1. Stel in de linkerbovenhoek de **[!UICONTROL Store View]** terug naar de standaardwaarden.

1. Ga als volgt te werk om de wijziging in uw winkel te controleren:

   - Klik in de rechterbovenhoek op de knop _Beheerder_ menupijl en kies **[!UICONTROL Customer View]**.

     ![Klantenweergave](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - Stel in de rechterbovenhoek van de winkel de **[!UICONTROL Language Chooser]** in de winkelweergave van het product dat u hebt bewerkt en zoek naar het product dat u voor de weergave hebt bewerkt.

     ![Taalkeuze](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
