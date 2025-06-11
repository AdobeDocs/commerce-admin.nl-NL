---
title: Widget lijst met nieuwe producten
description: Leer hoe u de widget lijst met nieuwe producten kunt gebruiken om een lijst weer te geven met de laatst toegevoegde producten.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Widget lijst met nieuwe producten

De lijst met nieuwe producten is een voorbeeld van dynamische inhoud en bestaat uit live-gegevens die uit uw productcatalogus zijn opgehaald. Door gebrek, omvat de _Nieuwe Lijst van Producten_ de eerste acht van de onlangs toegevoegde producten. Nochtans, kan het ook worden gevormd om slechts producten binnen een gespecificeerde datumwaaier te omvatten.

![ Nieuwe productlijst op de storefront homepage ](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Stap 1: elk product instellen als nieuw

![ Magento Open Source ](../assets/open-source.svg) Deze stap is slechts op Magento Open Source van toepassing.

![ Adobe Commerce ](../assets/adobe-logo.svg) voor de opslag van Adobe Commerce, zie [ plannend een Update ](content-staging-scheduled-update.md) en dan aan Stap 2 op deze pagina verdergaan.

_[!UICONTROL Set Product as New]_&#x200B;datumbereikinstelling kan alleen worden geconfigureerd in geplande updates.

Het plaatsen van een product als nieuw voegt het product aan de _Nieuwe producten_ lijst toe. U kunt de instelling op elk gewenst moment weer wijzigen wanneer u de instelling niet meer in de lijst wilt opnemen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek elk product dat u wilt gebruiken en open in bewerkingsmodus.

1. Schakel voor **[!UICONTROL Set Product as New]** de optie in om het product al dan niet als een nieuw product in te stellen.

   ![ plaatsend het product als nieuw ](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

1. Als u wordt gevraagd de paginacache opnieuw te indexeren en te vernieuwen, klikt u op de koppelingen boven aan de pagina en volgt u de instructies.

## Stap 2: De widget maken

De code die de inhoud van de lijst Nieuwe Producten en zijn plaatsing in uw opslag bepaalt wordt geproduceerd door het hulpmiddel Widget.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]** .

1. Ga als volgt te werk in de sectie _[!UICONTROL Settings]_:

   - Stel **[!UICONTROL Type]** in op `Catalog New Products List` .

   - Kies de **[!UICONTROL Design Theme]** die door de winkel wordt gebruikt.

1. Klik op **[!UICONTROL Continue]**.

   ![ De nieuwe montages van de productlijst widget ](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Ga als volgt te werk in de sectie _[!UICONTROL Storefront Properties]_:

   - Voer bij **[!UICONTROL Widget Title]** een beschrijvende titel in voor de widget. (Deze titel is zichtbaar slechts van _Admin_.)

   - Selecteer bij **[!UICONTROL Assign to Store Views]** de winkelweergaven waarin de widget zichtbaar is.

     U kunt een specifieke opslagweergave selecteren, of `All Store Views` . Als u meerdere weergaven wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   - (Optioneel) Voer bij **[!UICONTROL Sort Order]** een getal in om te bepalen in welke volgorde dit item bij anderen in hetzelfde gedeelte van de pagina wordt weergegeven. (`0` = first, `1` = second, `3` = third, enzovoort.)

   ![ de updates van de Lay-out ](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Stap 3: Kies de locatie

1. Klik in de sectie _[!UICONTROL Layout Updates]_&#x200B;op **[!UICONTROL Add Layout Update]**.

1. **[!UICONTROL Display On]** instellen op `Specified Page.`

1. Stel **[!UICONTROL Page]** in op `CMS Home Page` .

1. Stel **[!UICONTROL Block Reference]** in op `Main Content Area` .

1. Stel **[!UICONTROL Template]** in op een van de volgende opties:

   - `New Product List Template`
   - `New Products Grid Template`

     ![ de updates van de Lay-out ](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

   Momenteel kunt u het bericht negeren om de cache te vernieuwen.

## Stap 4: Vorm de Lijst

1. Kies **[!UICONTROL Widget Options]** in het linkerdeelvenster.

1. Stel **[!UICONTROL Display Products]** in op een van de volgende opties:

   - `All Products` - Hier worden de producten op volgorde weergegeven, te beginnen met de producten die het laatst zijn toegevoegd.
   - `New Products` - maakt een lijst van slechts de producten die als _nieuw_ worden geïdentificeerd. Een product wordt als nieuw beschouwd tijdens het datumbereik dat is opgegeven in _[!UICONTROL Set Product As New From/To]_. De lijst is leeg als het datumbereik vervalt zonder dat er nieuwe producten zijn gedefinieerd.

1. Stel **[!UICONTROL Display Page Control]** in op `Yes` als u navigatie wilt toepassen op lijsten met meerdere pagina&#39;s.

   Voer bij **[!UICONTROL Number of Products per Page]** het aantal producten in dat u op elke pagina wilt weergeven.

1. Stel de optie **[!UICONTROL Number of Products to Display]** in op het aantal nieuwe producten dat u in de lijst wilt opnemen.

   De standaardinstelling is `10` .

1. Kies bij **[!UICONTROL Cache Lifetime (Seconds)]** hoe vaak u de lijst met nieuwe producten wilt vernieuwen.

   De cache is standaard ingesteld op 86.400 seconden (24 uur).

   ![ Opties Widget ](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, klik de verbinding in het bericht bij de bovenkant van de pagina en volg de instructies.

## Stap 5: Een voorvertoning van uw werk bekijken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Vind de pagina in het net waar de _Nieuwe Producten_ lijst moet verschijnen en de **[!UICONTROL Preview]** verbinding in de _[!UICONTROL Action]_&#x200B;kolom klikken.
