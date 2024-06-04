---
title: Lijst met producten
description: Meer informatie over de _[!UICONTROL Products]_ pagina in Admin, waar u producten kunt tot stand brengen en bestaande degenen uitgeven.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Lijst met producten

Alle producten in de catalogus zijn toegankelijk via de _[!UICONTROL Products]_in Admin, waar u producten kunt tot stand brengen en bestaande degenen uitgeven. Voor een installatie op meerdere sites kan elke website een andere selectie producten aanbieden die in dezelfde catalogus te koop zijn.

De _[!UICONTROL Products]_de lijst bevat alle producten in de catalogus, geeft de websites aan waar deze beschikbaar zijn en of deze momenteel zijn ingeschakeld voor verkoop. In Adobe Commerce B2B-installaties met [gedeelde catalogi](../b2b/catalog-shared.md) Toegelaten, omvat het net een kolom die erop wijst welke producten afwisselende disconteringstarifering in een gedeelde catalogus hebben.

U kunt door de lijstpagina door pagina, of onderzoek naar specifieke producten doorbladeren. De standaard gebruiken [besturingselementen](../getting-started/admin-grid-controls.md) de lijst sorteren en filteren en toepassen [handelingen](../getting-started/admin-actions-control.md) op geselecteerde producten.

![Productraster](./assets/products-grid.png){width="700" zoomable="yes"}

## Weergave van product beperken

Als u de prestaties van grote catalogi wilt verbeteren, kunt u het beste het aantal producten beperken dat in het raster wordt weergegeven. U kunt weergegeven productrasters beperken tot:

- Productpagina
- Verwante/up-verkoop/producten van andere leveranciers toevoegen
- Producten toevoegen aan bundelproduct
- Producten toevoegen aan productgroep
- Volgorde maken (beheerder)

Deze configuratie-instelling voor de weergavebeperking van het product is standaard uitgeschakeld. Door het toe te laten, kunt u het aantal producten in het net tot een specifieke waarde beperken. Als deze functie is ingeschakeld en het aantal overeenkomende producten voor de rasterweergave groter is dan de recordlimiet, wordt een beperkte verzameling records geretourneerd. Wanneer de limiet is bereikt, worden de totale gevonden records, het aantal geselecteerde records en de pagineringselementen niet weergegeven in de rasterkop.

>[!NOTE]
>
>Als u niet wilt dat het productraster wordt beperkt, gebruikt u filters nauwkeuriger om een verzameling te maken die minder items bevat dan het aantal dat is opgegeven in het dialoogvenster _[!UICONTROL Records Limit]_veld.

**_De weergavebeperking van het product configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Uitbreiden **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Admin]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Admin Grids]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Limit Number of Products in Grid]** tot `Yes`.

   - (Optioneel) Voer een waarde in het dialoogvenster **[!UICONTROL Records Limit]** om het aantal producten in het raster tot een bepaalde waarde te beperken. De standaard minimumwaarde is `20000`.

   ![Configuratie-instellingen voor beheerrasters](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Paginabesturingselementen

| Besturing | Beschrijving |
|--- |--- |
| [!UICONTROL Add Product] | Hiermee wordt het proces gestart voor het maken van een nieuw eenvoudig product. Klik op de pijl omlaag om een specifiek producttype te kiezen. Opties: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Hiermee geeft u alle handelingen weer die op geselecteerde producten in de lijst kunnen worden toegepast. Als u een actie wilt toepassen op een product of groep producten, schakelt u het selectievakje in de eerste kolom van elk product in. Opties: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Hiermee wordt een cataloguszoekopdracht gestart op basis van de huidige filters. |
| [!UICONTROL Default View] | Geeft de huidige kolomlay-out van het raster aan. Als er opgeslagen rasterkolomweergaven zijn, kunt u een andere kolomweergave kiezen. |
| [!UICONTROL Columns] | Hiermee geeft u alle handelingen weer die op geselecteerde producten in de lijst kunnen worden toegepast. Als u een actie wilt toepassen op een product of groep producten, schakelt u het selectievakje in de eerste kolom van elk product in. |
| [!UICONTROL Search by keyword] | Het zoekvak in de linkerbovenhoek wordt gebruikt om producten op trefwoord te zoeken. |
| [!UICONTROL Edit] | Opent het product in Edit wijze. U kunt hetzelfde doen door ergens op de rij te klikken. |

{style="table-layout:auto"}

## Standaardkolommen

| Kolom | Beschrijving |
|--- |--- |
| (Selectievakje) | Hiermee selecteert u meerdere records die aan een handeling moeten worden onderworpen. Het selectievakje in de eerste kolom van elke geselecteerde record is gemarkeerd. Opties: <br/>**[!UICONTROL Select All]**- Hiermee selecteert u alle gevonden records die overeenkomen met de huidige filterinstellingen.<br/>**[!UICONTROL Select All on This Page]** - Hiermee selecteert u alleen de records op de huidige pagina die overeenkomen met de filterinstellingen. |
| [!UICONTROL ID] | Een uniek, opeenvolgend aantal dat wordt toegewezen wanneer een nieuw product voor het eerst wordt bewaard. |
| [!UICONTROL Thumbnail] | Geeft een miniatuur weer van de hoofdafbeelding van het product. |
| [!UICONTROL Name] | De productnaam. |
| [!UICONTROL Type] | Het producttype. |
| [!UICONTROL Attribute Set] | De naam van de kenmerkenreeks die als malplaatje voor het product wordt gebruikt. |
| [!UICONTROL SKU] | De unieke Stock Keeping Unit die aan het product wordt toegewezen. |
| [!UICONTROL Price] | De eenheidsprijs van het product. |
| [!UICONTROL Quantity] | De hoeveelheid in voorraad. |
| [!UICONTROL Salable Quantity] | De som van alle beschikbare eenheden van dit product. |
| [!UICONTROL Visibility] | Geeft aan waar het product zichtbaar is in de catalogus. Opties: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Geeft de status van het product aan. Opties: `Enabled` en `Disabled` |
| [!UICONTROL Websites] | Geeft de websites aan waar het product beschikbaar is. |
| [!UICONTROL Action] | Opent het product in Edit wijze. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar met [Adobe Commerce B2B](./b2b/../introduction.md) (alleen) Geeft de gedeelde catalogi aan die aangepaste prijzen voor het product bevatten. |

{style="table-layout:auto"}

## Andere kolommen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Short Description] | Korte beschrijving van het product. |
| [!UICONTROL Special Price From Date] | De eerste datum van de speciale prijsbevordering. |
| [!UICONTROL Special Price To Date] | De laatste datum van de speciale prijsbevordering. |
| [!UICONTROL Cost] | De werkelijke kosten van het object. |
| [!UICONTROL Manufacturer] | De fabrikant van het product. |
| [!UICONTROL Meta Keywords] | Meta-trefwoorden voor het product. |
| [!UICONTROL Color] | De productkleur. |
| [!UICONTROL Set Product as New from Date] | De eerste datum van het vastgestelde product als nieuwe bevordering. |
| [!UICONTROL Set Product as New to Date] | De laatste datum van het vastgestelde product als nieuwe bevordering. |
| [!UICONTROL Active From / To] | De begin- en einddatum van het product. |
| [!UICONTROL Layout] | De productindeling. |
| [!UICONTROL Minimum Advertised Price] | De minimale geadverteerde prijs van het product. |
| [!UICONTROL Allow Gift Message] | Het cadeaubericht aan klanten die een cadeaukaart kopen. |
| [!UICONTROL Special Price] | Speciale prijs voor het product. |
| [!UICONTROL Weight] | Het productgewicht. |
| [!UICONTROL Meta Title] | Meta-titel voor het product. |
| [!UICONTROL Meta Description] | Beschrijving van de metagegevens van het product. |
| [!UICONTROL Country of Manufacture] | Het land van vervaardiging. |
| [!UICONTROL New Theme] | Aangepast thema toegepast op het product. |
| [!UICONTROL URL Key] | De URL-sleutel van het product. |
| [!UICONTROL Tax Class] | The product tax class. |
| [!UICONTROL Allow Gift Message] | Geeft de beschikbaarheid van de berichtoptie voor het product weer. |

{style="table-layout:auto"}
