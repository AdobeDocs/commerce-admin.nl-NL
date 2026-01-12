---
title: Producten in categorieën sorteren
description: Leer hoe u de positie van producten in een categorie handmatig kunt bepalen of een vooraf gedefinieerde sorteervolgorde kunt toepassen.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Producten in categorieën sorteren

{{ee-feature}}

De positie van producten in een categorie kan handmatig worden opgegeven door producten naar de juiste positie te slepen of door een vooraf gedefinieerde sorteervolgorde toe te passen. Standaard kunnen producten worden gesorteerd op voorraadniveau, leeftijd, kleur, naam, SKU en prijs. Met Automatisch sorteren wordt de huidige sorteervolgorde genegeerd en worden eventuele handmatig ingestelde posities voor slepen en neerzetten opnieuw ingesteld. De soortorde van kleuren en het minimumvoorraadniveau dat voor producten kan worden vereist om in de lijst worden omvat worden geplaatst in de [ Visuele Merchandiser ](../configuration-reference/catalog/visual-merchandiser.md) configuratie.

U kunt opstelling afzonderlijk de categorieopties voor elke [ opslagmening ](../stores-purchase/stores.md#add-stores) om de selectie van producten, hun relatieve positie in de lijst, en de attributen te bepalen die voor categorieregels beschikbaar zijn. Nochtans, zijn er één enkele, **_globale_** sorteervolgorde en productpositie in de catalogus en zij worden gedeeld over alle [ opslagmeningen ](../stores-purchase/store-views.md), opslag, en websites.

## Stap 1: Plaats het werkingsgebied van de configuratie

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Kies zo nodig de **[!UICONTROL Store View]** waar de instellingen van toepassing zijn.

   Voor een installatie in meerdere opslagruimten past de instelling _[!UICONTROL Store View]_de sorteervolgorde toe op alle beschikbare weergaven in de winkel.

1. Kies in de categoriestructuur aan de linkerkant de categorie die u wilt bewerken.

   ![ boom van de Categorie ](./assets/category-selected.png){width="700" zoomable="yes"}

## Stap 2: De producten sorteren

>[!NOTE]
>
>Wanneer u een categorie sorteert op een productkenmerk, worden producten met dezelfde kenmerkwaarden ook in oplopende volgorde gesorteerd op _[!UICONTROL Product ID]_.

In de _[!UICONTROL Products in Category]_sectie, klik de tegels ( ![ de tegels van de Mening ](../assets/icon-view-tiles.png)) pictogram om de producttegels in een net te tonen. Gebruik de handmatige of automatische methode om de producten te sorteren.

![ de tegels van het Product ](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Methode 1: Handmatig sorteren

1. Stel **[!UICONTROL Sort Order]** in op uw voorkeur.

   ![ de orde van de Sortering ](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Sort]** om de nieuwe sorteervolgorde toe te passen.

1. Klik op **[!UICONTROL Save Category]** om de sorteervolgorde op te slaan.

1. Wanneer daarom wordt gevraagd, werkt u eventuele ongeldige indexen bij.

### Methode 2: Automatisch sorteren

1. Plaats **[!UICONTROL Match products by rule]** (![ Wissel ja ](../assets/toggle-yes.png)) aan `Yes`.


1. Stel **[!UICONTROL Automatic Sorting]** in op uw voorkeur.

1. Volg de instructies in de volgende stap om een categorieregel te maken.

## Stap 3: Een categorieregel maken

1. Plaats **[!UICONTROL Match products by rule]** (![ Wissel ja ](../assets/toggle-yes.png)) aan `Yes`.

1. Klik op **[!UICONTROL Add Condition]**.

1. Kies de **[!UICONTROL Attribute]** die de basis van de voorwaarde is.

1. Stel **[!UICONTROL Operator]** in op een van de volgende opties:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Voer de juiste **[!UICONTROL Value]** in.

   ![ voorwaarde van de Categorie ](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Als u nog een voorwaarde wilt toevoegen, klikt u op **[!UICONTROL Add Condition]** en herhaalt u het proces.

## Stap 4: Opslaan, vernieuwen en verifiëren

1. Klik op **[!UICONTROL Save Category]** als de bewerking is voltooid.

1. Wanneer u wordt gevraagd de cache te vernieuwen, klikt u op **[!UICONTROL Cache Management]** en vernieuwt u elke ongeldige cache.

1. Controleer in de winkel of de regels voor productselectie, sorteren en categorie correct werken.

   Als u aanpassingen moet aanbrengen, wijzigt u de instellingen en probeert u het opnieuw.
