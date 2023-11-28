---
title: Widget lijst met nieuwe producten
description: Leer hoe u de widget lijst met nieuwe producten kunt gebruiken om een lijst weer te geven met de laatst toegevoegde producten.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Widget lijst met nieuwe producten

De lijst met nieuwe producten is een voorbeeld van dynamische inhoud en bestaat uit live-gegevens die uit uw productcatalogus zijn opgehaald. Standaard worden de _Nieuwe producten_ de eerste acht van de onlangs toegevoegde produkten zijn opgenomen in de lijst . Nochtans, kan het ook worden gevormd om slechts producten binnen een gespecificeerde datumwaaier te omvatten.

![Lijst met nieuwe producten op de homepage van de winkel](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Stap 1: elk product instellen als nieuw

![Magento Open Source](../assets/open-source.svg) Deze stap is alleen van toepassing op Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Zie voor Adobe Commerce-winkels [Een update plannen](content-staging-scheduled-update.md) en ga vervolgens verder met Stap 2 op deze pagina.

_[!UICONTROL Set Product as New]_datumbereikinstelling kan alleen worden geconfigureerd in geplande updates.

Als u een product als nieuw instelt, wordt het product aan de _Nieuwe producten_ lijst. U kunt de instelling op elk gewenst moment weer wijzigen wanneer u de instelling niet meer in de lijst wilt opnemen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek elk product dat u wilt gebruiken en open in bewerkingsmodus.

1. Voor **[!UICONTROL Set Product as New]**, schakelt u de optie in om het product al dan niet als een nieuw product in te stellen.

   ![Het product instellen als nieuw](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

1. Als u wordt gevraagd de paginacache opnieuw te indexeren en te vernieuwen, klikt u op de koppelingen boven aan de pagina en volgt u de instructies.

## Stap 2: De widget maken

De code die de inhoud van de lijst Nieuwe Producten en zijn plaatsing in uw opslag bepaalt wordt geproduceerd door het hulpmiddel Widget.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]**.

1. In de _[!UICONTROL Settings]_Ga als volgt te werk:

   - Set **[!UICONTROL Type]** tot `Catalog New Products List`.

   - Kies de optie **[!UICONTROL Design Theme]** die door de winkel wordt gebruikt.

1. Klik op **[!UICONTROL Continue]**.

   ![Nieuwe widget-instellingen voor productlijsten](./assets/widget-settings.png){width="600" zoomable="yes"}

1. In de _[!UICONTROL Storefront Properties]_Ga als volgt te werk:

   - Voor **[!UICONTROL Widget Title]**, voert u een beschrijvende titel in voor de widget. (Deze titel is alleen zichtbaar vanaf het tabblad _Beheerder_.)

   - Voor **[!UICONTROL Assign to Store Views]** selecteert u de winkelweergaven waarin de widget zichtbaar is.

     U kunt een specifieke winkelweergave selecteren, of `All Store Views`. Als u meerdere weergaven wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   - (Optioneel) Voor **[!UICONTROL Sort Order]** Voer een getal in om de volgorde te bepalen waarin dit item wordt weergegeven met andere items op hetzelfde deel van de pagina. (`0` = eerst, `1` = seconde, `3` = derde, enzovoort.)

   ![Layout-updates](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Stap 3: Kies de locatie

1. In de _[!UICONTROL Layout Updates]_sectie, klikken **[!UICONTROL Add Layout Update]**.

1. Set **[!UICONTROL Display On]** tot `Specified Page.`

1. Set **[!UICONTROL Page]** tot `CMS Home Page`.

1. Set **[!UICONTROL Block Reference]** tot `Main Content Area`.

1. Set **[!UICONTROL Template]** op een van de volgende wijzen:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Layout-updates](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

   Momenteel kunt u het bericht negeren om de cache te vernieuwen.

## Stap 4: Vorm de Lijst

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Widget Options]**.

1. Set **[!UICONTROL Display Products]** op een van de volgende wijzen:

   - `All Products` - Hiermee geeft u een overzicht van de opeenvolgende producten, te beginnen met de producten die het laatst zijn toegevoegd.
   - `New Products` - Alleen de producten vermeld die als _new_. Een product wordt beschouwd als nieuw gedurende het datumbereik dat is opgegeven in _[!UICONTROL Set Product As New From/To]_. De lijst is leeg als het datumbereik vervalt zonder dat er nieuwe producten zijn gedefinieerd.

1. Als u navigatie wilt instellen voor lijsten met meerdere pagina&#39;s, stelt u **[!UICONTROL Display Page Control]** tot `Yes`.

   Voor **[!UICONTROL Number of Products per Page]**, voert u het aantal producten in dat u op elke pagina wilt weergeven.

1. Stel de **[!UICONTROL Number of Products to Display]** aan het aantal nieuwe producten dat u in de lijst wilt opnemen.

   De standaardinstelling is `10`.

1. Voor **[!UICONTROL Cache Lifetime (Seconds)]**, kiest u hoe vaak u de lijst met nieuwe producten wilt vernieuwen.

   De cache is standaard ingesteld op 86.400 seconden (24 uur).

   ![Widget-opties](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, klik de verbinding in het bericht bij de bovenkant van de pagina en volg de instructies.

## Stap 5: Een voorvertoning van uw werk bekijken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Zoek de pagina in het raster waar de _Nieuwe producten_ wordt weergegeven en klikt u op **[!UICONTROL Preview]** in de _[!UICONTROL Action]_kolom.
