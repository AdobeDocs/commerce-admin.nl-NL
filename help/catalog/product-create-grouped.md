---
title: Gegroepeerd product
description: Leer hoe u een gegroepeerd product maakt dat bestaat uit eenvoudige zelfstandige producten die als groep worden aangeboden.
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---

# Gegroepeerd product

Een gegroepeerd product bestaat uit eenvoudige zelfstandige producten die als groep worden aangeboden. U kunt variaties van één enkel product aanbieden of hen groeperen door seizoen of thema. Het aanbieden van een gegroepeerd product kan klanten ertoe aanzetten extra items te kopen. Een gegroepeerd product biedt een eenvoudige manier om variaties van een product aan te bieden en ze allemaal op dezelfde pagina weer te geven.

Zo kunt u bijvoorbeeld open-stock-flatware verkopen en elk type gereedschap weergeven dat in een formele plaatsinstelling wordt gebruikt. Sommigen zouden meerdere salade-vorken, visvorken, diner-vorken, dinemessen, vismessen, botermessen, soep-lepels en dessert-lepels kunnen bestellen. Andere klanten zouden een eenvoudige vork, een mes, en een lepel kunnen opdracht geven. Klanten kunnen elk gewenst aantal items bestellen.

Hoewel ze als groep worden aangeboden, wordt elk product in de groep als afzonderlijk artikel aangekocht. In het winkelwagentje worden elk artikel en de aangeschafte hoeveelheid weergegeven als een afzonderlijk artikel.

De volgende instructies tonen het proces aan om een gegroepeerd product te creëren gebruikend a [ productmalplaatje ](attribute-sets.md), vereiste gebieden, en basismontages. Elk vereist gebied is duidelijk met een rode asterisk (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

![ Gegroepeerd Product ](./assets/product-grouped.png){width="700" zoomable="yes"}

## Stap 1: Kies het producttype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Voor _[!UICONTROL Add Product]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu bij de hoger-juiste hoek, kies **[!UICONTROL Grouped Product]**.

   ![ voeg Gegroepeerd Product ](./assets/product-add-grouped.png){width="700" zoomable="yes"} toe

## Stap 2: Kies de kenmerkset

Om de [ geplaatste attributen ](attribute-sets.md) te kiezen die als malplaatje voor het product wordt gebruikt, doe één van het volgende:

- Voer de naam van de **[!UICONTROL Attribute Set]** in om te zoeken.
- Kies in de lijst de kenmerkset die u wilt gebruiken.

Het formulier wordt bijgewerkt met de wijziging.

![ kies Malplaatje ](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

Als de vereiste kenmerken niet bestaan, kunt u nieuwe kenmerken toevoegen tijdens het maken van een product:

- Klik in de rechterbovenhoek op **[!UICONTROL Add Attribute]** .
- Bepaal een nieuw attribuut (zie [ Toevoegend een Attribuut aan een Product ](product-attributes-add.md)).

  ![ Nieuw Attribuut ](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

Om een bestaand attribuut aan het product toe te voegen, gebruik de [ filtercontroles ](../getting-started/admin-grid-controls.md) om de attributen in het net te vinden en het volgende te doen:

- Schakel het selectievakje in de eerste kolom van elk kenmerk dat u wilt toevoegen in.
- Klik op **[!UICONTROL Add Selected]**.

## Stap 3: Voer de vereiste instellingen in

1. Voer de **[!UICONTROL Product Name]** in.

1. Accepteer de standaardwaarde **[!UICONTROL SKU]** die is gebaseerd op de productnaam of voer een andere naam in.

   Het veld **[!UICONTROL Quantity]** is niet beschikbaar omdat de waarde wordt afgeleid van de afzonderlijke producten waaruit de groep bestaat.

   Een gegroepeerd product bevat geen eigen prijs in de catalogus. De prijs van het gegroepeerde product wordt afgeleid van de prijs van de afzonderlijke producten die in de groep zijn opgenomen.

1. Omdat het product nog niet klaar is om te publiceren, plaats **[!UICONTROL Enable Product]** aan `No` ( ![ knevel nr ](../assets/toggle-no.png)).

1. Klik op **[!UICONTROL Save]** en ga verder.

   Wanneer het product wordt bewaard, verschijnt de productnaam bij de bovenkant van de pagina, en [ verkiesster van de Mening van de Opslag ](introduction.md#product-scope) verschijnt in de upper-left hoek.

1. Kies de locatie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![ kies de Mening van de Opslag ](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Stap 4: De basisinstellingen voltooien

1. Accepteer de instelling **[!UICONTROL Stock Status]** van `In Stock` .

1. Als u **[!UICONTROL Categories]** aan het product wilt toewijzen, klikt u op het vak **[!UICONTROL Select…]** en voert u een van de volgende handelingen uit:

   **kies een bestaande categorie:**

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van de categorie die u wilt toewijzen.

   **creeer een categorie:**

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** in en kies de **[!UICONTROL Parent Category]** die de positie in de menustructuur bepaalt.

   - Klik op **[!UICONTROL Create Category]**.

1. Accepteer de **[!UICONTROL Visibility]** -instellingen van `Catalog, Search` .

1. Om het product in de [ lijst van nieuwe producten ](../content-design/widget-new-products-list.md) te voorzien, verkies **[!UICONTROL Set Product as New]** **[!UICONTROL from]** en **[!UICONTROL to]** data op de kalender.

1. Kies de **[!UICONTROL Country of Manufacture]** .

   Er kunnen aanvullende individuele kenmerken zijn die het product beschrijven. De selectie varieert kenmerkset en u kunt deze later voltooien.

## Stap 5: Producten toevoegen aan de groep

1. Blader omlaag naar de sectie **[!UICONTROL Grouped Products]** en klik op **[!UICONTROL Add Products to Group]** .

   ![ Gegroepeerde Producten ](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. Indien nodig, gebruik de [ filters ](../getting-started/admin-grid-controls.md) om de producten te vinden die u in de groep wilt omvatten.

1. Schakel in de lijst het selectievakje in van elk item dat u in de groep wilt opnemen.

   >[!NOTE]
   >
   >Alleen eenvoudige, downloadbare en virtuele producten zonder configureerbare opties kunnen worden gegroepeerd in onderliggende producten. Andere producttypen worden niet in de keuzelijst weergegeven.

   ![ voeg Geselecteerde Producten ](./assets/product-grouped-add-products.png){width="600" zoomable="yes"} toe

1. Klik op **[!UICONTROL Add Selected Products]** als u deze aan de productgroep wilt toevoegen.

   De geselecteerde producten worden weergegeven in de sectie _[!UICONTROL Grouped Products]_.

   Voor de Multicarehandel van Source met [ Inventory management ](../inventory-management/sources-stocks.md), omvat het net een **[!UICONTROL Quantity per Source]** kolom met elke toegewezen bron en voorraad.

   ![ Producten in Groep ](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Default Quantity]** in voor een van de items.

1. Om de orde van de producten te veranderen, greep het _pictogram van de Orde van de Verandering_ ( ![ het controlemechanisme van de Positie ](../assets/icon-sort-order.png)) in de eerste kolom en sleep het product aan de nieuwe positie in de lijst.

1. Als u een product uit de groep wilt verwijderen, klikt u op **[!UICONTROL Remove]** .

## Stap 5: De productinformatie invullen

Voer de benodigde gegevens in de volgende secties in:

- [Inhoud](product-content.md)
- [Afbeeldingen en video&#39;s](product-images-and-video.md)
- [Optimalisatie zoekmachine](product-search-engine-optimization.md)
- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)
- [Aanpasbare opties](settings-advanced-custom-options.md)
- [Producten op websites](settings-basic-websites.md)
- [Ontwerp](settings-advanced-design.md)
- [Cadeauopties](product-gift-options.md)

## Stap 6: Publish het product

1. Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** in op `Yes` .

1. Voer een van de volgende handelingen uit:

   **Methode 1:** sparen en Voorproef

   - Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

   - Om het product in uw opslag te bekijken, verkies **[!UICONTROL Customer View]** op _Admin_ ( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-black.png)) menu.

     De winkel wordt geopend in een nieuw browsertabblad.

     ![ Mening van de Klant ](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **Methode 2:** sparen en sluit

   - Voor _[!UICONTROL Save]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu, kies **[!UICONTROL Save & Close]**.

## Stap 7: De miniaturen van het winkelwagentje configureren (optioneel)

Als u voor elk product in de groep een andere afbeelding hebt, kunt u de configuratie zo instellen dat de juiste afbeelding wordt gebruikt voor de miniatuur van het winkelwagentje.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit **[!UICONTROL Shopping Cart]**.

   Voor een gedetailleerde lijst van deze configuratieopties, zie [ Shopping Kart ](../configuration-reference/sales/checkout.md#shopping-cart) in de _Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Grouped Product Image]** in op `Product Thumbnail Itself` .

   ![ Shopping Cart ](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om deze optie in te stellen.

1. Klik op **[!UICONTROL Save Config]**.

## Te onthouden zaken

- Een gegroepeerd product is in wezen een verzameling eenvoudige, verwante producten.

- Alle kindproducten worden toegewezen en unassigned van het gegroepeerde product **_globaal_** voor alle websites, opslag, en opslagmeningen tezelfdertijd.

- Gegroepeerde onderliggende producten kunnen eenvoudig, downloadbaar of virtueel zijn **[!UICONTROL without custom options]** .

- Elk aangeschaft artikel wordt afzonderlijk in het winkelwagentje weergegeven in plaats van als onderdeel van de groep.

- Een gegroepeerd product bevat geen eigen prijs in de catalogus. De prijs van het gegroepeerde product wordt afgeleid van de prijs van de afzonderlijke producten die in de groep zijn opgenomen.

- De miniatuurafbeelding in het winkelwagentje kan zo worden ingesteld dat de afbeelding van het gegroepeerde bovenliggende product of het bijbehorende product wordt weergegeven.
