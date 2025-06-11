---
title: Inhoudsblokken toevoegen
description: Maak aangepaste blokken inhoud die u op elke pagina of in een ander blok kunt hergebruiken.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Inhoudsblokken toevoegen

U kunt aangepaste blokken inhoud maken en deze vervolgens toevoegen aan elke pagina, groep pagina&#39;s of zelfs aan een ander blok. U kunt bijvoorbeeld een afbeeldingsschuifregelaar in een blok plaatsen en het blok vervolgens op de startpagina plaatsen. De werkruimte van Blokken gebruikt de zelfde [ basiscontroles ](pages-workspace.md) zoals de _3} werkruimte van Pagina&#39;s {om u te helpen beschikbare blokken vinden en routineonderhoud uitvoeren._ Wanneer het blok volledig is, kunt u het [ gebruiken Widget ](widget-static-block.md) hulpmiddel om het op specifieke pagina&#39;s in uw opslag te plaatsen.

![ de pagina van Blokken toont een net van bestaande blokken ](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Een blok maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. In de hoger-juiste hoek, klik **voeg Nieuw Blok** toe.

   ![ de Nieuwe pagina van het Blok toont opties en een inhoudsruimte ](./assets/block-detail.png){width="500" zoomable="yes"}

1. Als u de gebrek-toegelaten status van het nieuwe blok wilt veranderen, plaats **laat Blok** `No` toe.

1. Wijs Titel van het a **Blok** voor interne verwijzing toe.

1. Wijs een uniek **Herkenningsteken** voor het blok toe.

   Gebruik alleen kleine letters met onderstrepingstekens in plaats van spaties.

1. Selecteer elke **[!UICONTROL Store View]** waar u het blok beschikbaar wilt maken.

1. Voeg de inhoud voor het blok toe met behulp van de gereedschapsset voor weergegeven inhoud:

   - Als [ de Bouwer van de Pagina ](../page-builder/introduction.md) wordt toegelaten, selecteer **[!UICONTROL Edit with Page Builder]** om de hulpmiddelen van de Bouwer van de Pagina in de inhoud [ werkruimte ](../page-builder/workspace.md) te gebruiken.

     ![ de werkruimte van de Bouwer van de Pagina ](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Voor informatie over het toevoegen van blokken met de Bouwer van de Pagina, zie [ Leerprogramma 2: Blokken ](../page-builder/2-blocks.md).

   - Gebruik de [ redacteur ](editor.md) om tekst te formatteren, verbindingen tot stand te brengen, en lijsten, beelden, video, en audio toe te voegen.

     Als u verkiest om met de code van HTML te werken, klik **tonen/de Redacteur van de Verbergen**.

     ![ de redacteur van het Blok (verborgen) ](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Klik op de pijl **[!UICONTROL Save]** als de bewerking is voltooid en kies **[!UICONTROL Save & Close]** .

   Het nieuwe blok verschijnt onder aan de lijst in het raster Blokken.

1. Gebruik het [ hulpmiddel van Widget ](widget-static-block.md) om het voltooide blok op een specifieke pagina in uw opslag te plaatsen.

## Een blok verwijderen

Er zijn twee manieren om een aangepast blok te verwijderen. U kunt het uit het _Raster van Blokken_ verwijderen, of uit uitgeven blokpagina.

### Methode 1: Een blok verwijderen uit het raster Blokken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Zoek de blokken met filters boven het raster en schakel het selectievakje in voor een of meer blokken die u wilt verwijderen.
1. Stel **[!UICONTROL Actions]** in op `Delete` in de linkerbovenhoek van de lijst.
1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

### Methode 2: Een blok verwijderen van de bewerkingspagina

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Zoek het blok dat moet worden verwijderd.
1. In de _kolom van Acties_ voor het blok, klik **[!UICONTROL Select]** en kies **[!UICONTROL Edit]**.
1. Klik in de menubalk op **[!UICONTROL Delete Block]** .
1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

## Menu Opslaan

| Opdracht | Beschrijving |
|----------|----------- |
| [!UICONTROL Save] | Sla het huidige blok op en ga verder met werken. |
| [!UICONTROL Save & Duplicate] | Sla het huidige blok op, sluit het en open een nieuwe kopie. |
| [!UICONTROL Save & Close] | Sla het huidige blok op, sluit het en ga terug naar het raster Blokken. |

{style="table-layout:auto"}

## Een lichtbak of regelaar toevoegen

- Het is gemakkelijk om a [ schuif ](../page-builder/slider.md) aan uw opslag met [[!DNL Page Builder]](../page-builder/introduction.md) toe te voegen. De schuifregelaar kan automatisch worden ingesteld om te worden afgespeeld of kan handmatig worden ingesteld met navigatieknoppen.

  ![ schuif van de Bouwer van de Pagina ](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  Er is ook een groot aantal op jQuery gebaseerde afbeeldingslichtvakken beschikbaar op [[!DNL Commerce Marketplace]][1] . Sommige zijn gratis.

- U kunt ook een extensie downloaden van [!DNL Commerce Marketplace] . Raadpleeg de documentatie die is verstrekt door de ontwikkelaar van de extensie voor meer informatie.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
