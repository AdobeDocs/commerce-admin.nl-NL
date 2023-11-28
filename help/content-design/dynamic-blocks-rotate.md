---
title: Een roterend dynamisch blok toevoegen
description: Presenteer een presentatie van interactieve inhoud in de winkel door meerdere dynamische blokken aan een rotator toe te voegen.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Een roterend dynamisch blok toevoegen

{{ee-feature}}

Als u een presentatie van interactieve inhoud wilt weergeven, kunt u meerdere [dynamische blokken](dynamic-blocks.md) naar een rotator. De [widget](widgets.md) wordt gebruikt om de rotator op een specifieke plaats op één enkele pagina of op veelvoudige pagina&#39;s door uw opslag te plaatsen.

![Dynamische blokrotator](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Stap 1: afzonderlijke dynamische blokken maken

Naar [de dynamische blokken maken](dynamic-blocks.md) die u in de rotator wilt plaatsen, volgt u deze instructies:

## Stap 2: Een dynamische blokrotator-widget toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]**.

1. Onder _Instellingen_, set **[!UICONTROL Type]** tot `Dynamic Blocks Rotator`.

1. Kies de huidige **[!UICONTROL Design Theme]** van de winkel.

   Deze instelling identificeert het huidige pakket of [thema](themes.md) dat de paginalay-out van de opslag bepaalt.

1. Klik op **[!UICONTROL Continue]**.

   ![Dynamische rotatie-instellingen blok](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Stap 3: De opties voltooien

1. Onder _Eigenschappen van Storefront_ stelt u de opties in:

   - Voer een **[!UICONTROL Title]** voor de rotator.

   - In de **[!UICONTROL Assign to Store Views]** Selecteer de [winkelweergaven](../getting-started/websites-stores-views.md) waar de rotator beschikbaar is.

   - (Optioneel) Voer een **[!UICONTROL Sort Order]** getal om de positie van de rotator in de doelcontainer te bepalen. Het is relatief ten opzichte van andere widgets die aan dezelfde container kunnen worden toegewezen.

   ![Eigenschappen van Rotator-storefront](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Onder _Lay-outopties_, klikt u op **[!UICONTROL Add Layout Update]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Display on]** op de pagina, of het type van pagina, waar de rotator moet verschijnen.

      - `Categories` - Geeft de rotator weer op een van de [anker](../catalog/navigation-layered.md) of niet-ankercategoriepagina&#39;s. Opties: Ankercategorieën / Niet-ankercategorieën
      - `Products` - Geeft de rotator weer op een specifiek type productpagina of op alle productpagina&#39;s. Opties: alle producttypen / [Eenvoudig product](../catalog/product-create-simple.md) /  [Virtueel product](../catalog/product-create-virtual.md) / [Bundel](../catalog/product-create-bundle.md) / [Downloadbaar product](../catalog/product-create-downloadable.md) / [Cadeaukaart](../catalog/product-gift-card-create.md) / [Configureerbaar product](../catalog/product-create-configurable.md) / [Gegroepeerd product](../catalog/product-create-grouped.md)
      - `Generic Pages` - Geeft de rotator weer op alle pagina&#39;s, op een specifieke pagina of alleen op pagina&#39;s met een bepaalde indeling. Opties: `All Pages` / `Specified Page` / `Page Layouts`

     In het voorbeeld moet de rotator op een `Specified Page`.

   - Selecteer de specifieke **[!UICONTROL Page]** waar de rotator moet worden weergegeven.

   - Set **[!UICONTROL Container]** op het deel van het [pagina-indeling](page-layout.md#standard-page-layouts) waar de rotator moet worden weergegeven.

     Als andere widgets aan dezelfde container worden toegewezen, worden ze op volgorde weergegeven volgens de sorteervolgorde.

   - Accepteren `Dynamic Block Template` als standaard **[!UICONTROL Template]**.

     Deze instelling bepaalt de sjabloon die wordt gebruikt om de rotator op te maken, op basis van het feit of de rotator zelfstandig moet staan of in bestaande tekst moet worden geplaatst.

     ![Updates van de lay-out Rotator](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Klik op **[!UICONTROL Save and Continue Edit]**.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Widget Options]**.

1. Voor de **[!UICONTROL Dynamic Blocks to Display]**, accepteren `Specified Dynamic Blocks`.

   Deze instelling bepaalt het type dynamische blokken dat in de rotator is opgenomen.

   - `Specified Dynamic Blocks` - Bevat alleen specifieke dynamische blokken.
   - `Cart Price Rule Related` - Omvat alleen dynamische blokken die zijn gekoppeld aan een kartprijsregel.
   - `Catalog Price Rule Related` - Bevat alleen dynamische blokken die zijn gekoppeld aan de regel voor catalogusprijzen.

1. Naar **[!UICONTROL Restrict the Dynamic Block Types]** die met de widget kunnen worden gebruikt, selecteert u `Content Area`.

   Met deze instelling beperkt u de banner tot een specifiek gedeelte van de pagina-indeling.

   - `Content Area` - Plaatst het dynamische blok in het belangrijkste inhoudsgebied van de pagina.
   - `Footer` - Hiermee plaatst u het dynamische blok in de voettekst van de pagina.
   - `Header` - Plaatst het dynamische blok in de paginakoptekst.
   - `Left Column` - Plaatst het dynamische blok in de linkerkolom van de paginalay-out, als beschikbaar.
   - `Right Column` - Plaatst het dynamische blok in de juiste kolom van de paginalay-out, als beschikbaar.

1. Set **[!UICONTROL Rotation Mode]** op een van de volgende wijzen:

   - `Display all instead of rotating` - Geeft een stapel dynamische blokken weer, waarin alle blokken zichtbaar zijn.
   - `One at a time, Random` - Geeft de opgegeven dynamische blokken in willekeurige volgorde weer. Wanneer de pagina wordt vernieuwd, wordt een ander (en willekeurig) dynamisch blok weergegeven.
   - `One at the time, Series` - Geeft de opgegeven dynamische blokken weer in de volgorde waarin ze zijn toegevoegd. Wanneer de pagina wordt vernieuwd, wordt het volgende dynamische blok in de reeks weergegeven.
   - `One at the time, Shuffle` - Geeft één dynamisch blok tegelijk weer in willekeurige volgorde. Deze optie lijkt op de optie `One at a time, Random` , behalve dat hetzelfde dynamische blok niet wordt herhaald.

     ![Opties voor de rotatiewidget](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. In de **[!UICONTROL Specify Dynamic Blocks]** , schakelt u het selectievakje in van elk dynamisch blok dat u in de rotator wilt opnemen.

1. Klik op **[!UICONTROL Save]**.
