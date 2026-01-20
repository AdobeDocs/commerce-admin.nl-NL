---
title: Productinstellingen - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Voor een product definiëren de [!UICONTROL Related Products, Up-Sells, and Cross-Sells] -instellingen eenvoudige promotieblokken op de productpagina die een selectie extra producten markeren.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 36c91007d21834b49351c8b53c617e442deebaa0
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Productinstellingen - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Gebruik de sectie _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_&#x200B;om eenvoudige promotieblokken in te stellen die een selectie van extra producten voorstellen die van belang kunnen zijn voor de klant. Voor meer informatie, zie [&#x200B; Verhoudingen van het Product &#x200B;](../merchandising-promotions/product-relationships.md).

![&#x200B; Verwante Producten, omhoog-Verkopen, en dwars-Verkoop &#x200B;](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Elk blok bestaat uit een lijst van producten die tot een specifieke optie behoren.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke id die aan de productentiteit is toegewezen. |
| [!UICONTROL Thumbnail] | Afbeelding met productminiaturen. |
| [!UICONTROL Name] | De naam van het product. |
| [!UICONTROL Status] | Geeft de productstatus aan. Opties: `Enabled` / `Disabled` . Uitgeschakelde producten worden niet weergegeven in de blokken aan de voorzijde. |
| [!UICONTROL Attribute Set] | De naam van de kenmerkenreeks die als malplaatje voor het product wordt gebruikt. |
| [!UICONTROL SKU] | De unieke Stock Keeping Unit die aan het product wordt toegewezen. |
| [!UICONTROL Price] | De eenheidsprijs van het product. |
| [!UICONTROL Action] | Opties: `Remove`. Hiermee verwijdert u een product uit het blok. |

{style="table-layout:auto"}

>[!TIP]
>
>![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) **Aanbevelingen van het Product die door Adobe AI** worden aangedreven vereenvoudigt het proces om productverhoudingen te bepalen door kunstmatige intelligentie en machine-leert algoritmen te gebruiken om een diepe analyse van samengevoegde bezoekersgegevens uit te voeren. Deze gegevens, in combinatie met uw Adobe Commerce-catalogus, resulteren in zeer boeiende, relevante en persoonlijke ervaringen voor de klant.
><br/>
>Voor meer informatie over het gebruiken van deze Adobe-ontwikkelde uitbreiding als alternatief aan manueel gevormde productaanbevelingen en omhoog-verkoopt, zie de _[Gids van de Aanbevelingen van het Product &#x200B;](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html)_.

## Verwante producten

Verwante producten zijn bedoeld om te worden aangeschaft naast het object dat de klant bekijkt. De klant kan het item in het winkelwagentje plaatsen door gewoon op het selectievakje te klikken. De plaatsing van het _Verwante blok van Producten_ varieert volgens bepaald thema en paginalay-out. In het voorbeeld hieronder, verschijnt het _Verwante Producten_ blok bij de bodem van de _pagina van de Mening van het Product_. Met een twee-kolom lay-out, verschijnt het _Verwante Producten_ blok vaak in juiste sidebar.

![&#x200B; Verwante Producten &#x200B;](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Verwante producten instellen:

1. Open het product in de bewerkingsmodus.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sectie.

1. Klik op **[!UICONTROL Add Related Products]**.

1. Gebruik de [&#x200B; filtercontroles &#x200B;](../getting-started/admin-grid-controls.md) om de producten te vinden die u wilt.

1. Selecteer in de lijst het selectievakje van een product dat u als verwant product wilt gebruiken.

   ![&#x200B; Verwante Producten &#x200B;](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Add Selected Products]** als de bewerking is voltooid.

## Up-sells

Up-sell-producten zijn objecten die uw klant wellicht liever gebruikt dan het product dat momenteel wordt overwogen. Een object dat wordt aangeboden als een up-verkoop kan van hogere kwaliteit zijn, populairder zijn of een betere winstmarge hebben. Up-sell de producten verschijnen op de productpagina onder een rubriek zoals _u in de volgende producten_ ook kunt geinteresseerd zijn.

![&#x200B; omhoog-Verkoop &#x200B;](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Je kunt als volgt producten selecteren:

1. Open het product in de bewerkingsmodus.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sectie.

1. Klik op **[!UICONTROL Add Up-Sell Products]**.

1. Gebruik de [&#x200B; filtercontroles &#x200B;](../getting-started/admin-grid-controls.md) om de producten te vinden die u wilt.

1. Schakel in de lijst het selectievakje in van elk product dat u wilt gebruiken als een up-sell-product.

   ![&#x200B; omhoog-Verkoop Producten &#x200B;](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Add Selected Products]** als de bewerking is voltooid.

>[!NOTE]
>
>Het bovenliggende bundelproduct wordt altijd automatisch weergegeven als een up-sell-product voor alle onderliggende producten.

## Cross-sells

Cross-sell-items zijn vergelijkbaar met impulsaankopen die naast het kasregister op de afrekenlijn worden geplaatst. Producten die worden aangeboden als een cross-sell, worden weergegeven op de winkelwagentje, vlak voordat de klant het afrekenproces start.

>[!NOTE]
>
>Om dwars-verkoop punten per opslagmening te tonen of te verbergen, zie [&#x200B; Controle > het Schepen van Kar &#x200B;](../configuration-reference/sales/checkout.md) optie genoemd _[!UICONTROL Show Cross-sell Items]_&#x200B;in het Schepen Kar. U kunt cross-sells tijdens specifieke verkoop of voor het testen A/B in een archiefmening willen verbergen.

![&#x200B; dwars-verkoopt in het winkelwagentje &#x200B;](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Om producten voor meerdere verkooppunten te selecteren:_**

1. Open het product in de bewerkingsmodus.

1. De rol neer en breidt ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sectie.

1. Klik op **[!UICONTROL Add Cross-Sell Products]**.

1. Gebruik de [&#x200B; filtercontroles &#x200B;](../getting-started/admin-grid-controls.md) om de producten te vinden die u wilt.

1. Schakel in de lijst het selectievakje in van elk product dat u als een cross-selproduct wilt gebruiken.

   ![&#x200B; dwars-verkoopt Producten &#x200B;](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Add Selected Products]** als de bewerking is voltooid.
