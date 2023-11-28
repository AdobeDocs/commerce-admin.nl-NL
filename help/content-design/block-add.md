---
title: Inhoudsblokken toevoegen
description: Maak aangepaste blokken inhoud die u op elke pagina of in een ander blok kunt hergebruiken.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Inhoudsblokken toevoegen

U kunt aangepaste blokken inhoud maken en deze vervolgens toevoegen aan elke pagina, groep pagina&#39;s of zelfs aan een ander blok. U kunt bijvoorbeeld een afbeeldingsschuifregelaar in een blok plaatsen en het blok vervolgens op de startpagina plaatsen. De werkruimte Blokken gebruikt hetzelfde [basiscontroles](pages-workspace.md) als de _Pagina&#39;s_ werkruimte om u te helpen beschikbare blokken te vinden en routineonderhoud uit te voeren. Wanneer het blok volledig is, kunt u [Widget](widget-static-block.md) gebruiken om het bestand op specifieke pagina&#39;s in uw winkel te plaatsen.

![Op de pagina Blokken wordt een raster van bestaande blokken weergegeven](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Een blok maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klik in de rechterbovenhoek op **Nieuw blok toevoegen**.

   ![De pagina Nieuw blok bevat opties en een inhoudsruimte](./assets/block-detail.png){width="500" zoomable="yes"}

1. Als u de status van het nieuwe blok waarvoor de standaardwaarde is ingeschakeld, wilt wijzigen, stelt u **Blok inschakelen** tot `No`.

1. Een **Bloktitel** voor interne referentie.

1. Een unieke waarde toewijzen **Id** voor het blok.

   Gebruik alleen kleine letters met onderstrepingstekens in plaats van spaties.

1. Selecteer elk **[!UICONTROL Store View]** waar u het blok wilt beschikbaar zijn.

1. Voeg de inhoud voor het blok toe met behulp van de gereedschapsset voor weergegeven inhoud:

   - Indien [Page Builder](../page-builder/introduction.md) is ingeschakeld, selecteert u **[!UICONTROL Edit with Page Builder]** om de gereedschappen van Page Builder in de inhoud te gebruiken [werkruimte](../page-builder/workspace.md).

     ![De werkruimte van Page Builder](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Voor informatie over het toevoegen van blokken met de Bouwer van de Pagina, zie [Lesbestand 2: Blokken](../page-builder/2-blocks.md).

   - Gebruik de [editor](editor.md) om tekst op te maken, koppelingen te maken en tabellen, afbeeldingen, video en audio toe te voegen.

     Als u liever met HTML code werkt, klikt u op **Editor tonen/verbergen**.

     ![Blokeditor (verborgen)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Klik op de knop **[!UICONTROL Save]** en kiest u **[!UICONTROL Save & Close]**.

   Het nieuwe blok verschijnt onder aan de lijst in het raster Blokken.

1. Gebruik de [Widget](widget-static-block.md) gebruiken om het ingevulde blok op een specifieke pagina in uw winkel te plaatsen.

## Een blok verwijderen

Er zijn twee manieren om een aangepast blok te verwijderen. U kunt het verwijderen uit de _Blokken_ , of vanaf de pagina voor het bewerkingsblok.

### Methode 1: Een blok verwijderen uit het raster Blokken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Zoek de blokken met filters boven het raster en schakel het selectievakje in voor een of meer blokken die u wilt verwijderen.
1. In de linkerbovenhoek van de lijst stelt u **[!UICONTROL Actions]** tot `Delete`.
1. Klik op **[!UICONTROL OK]**.

### Methode 2: Een blok verwijderen van de bewerkingspagina

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Zoek het blok dat moet worden verwijderd.
1. In de _Handelingen_ kolom voor het blok, klik **[!UICONTROL Select]** en kiest u **[!UICONTROL Edit]**.
1. Klik in de menubalk op **[!UICONTROL Delete Block]**.
1. Klik op **[!UICONTROL OK]**.

## Menu Opslaan

| Opdracht | Beschrijving |
|----------|----------- |
| [!UICONTROL Save] | Sla het huidige blok op en ga verder met werken. |
| [!UICONTROL Save & Duplicate] | Sla het huidige blok op, sluit het en open een nieuwe kopie. |
| [!UICONTROL Save & Close] | Sla het huidige blok op, sluit het en ga terug naar het raster Blokken. |

{style="table-layout:auto"}

## Een lichtbak of regelaar toevoegen

- Het is gemakkelijk om een [schuifregelaar](../page-builder/slider.md) in uw winkel met [[!DNL Page Builder]](../page-builder/introduction.md). De schuifregelaar kan automatisch worden ingesteld om te worden afgespeeld of kan handmatig worden ingesteld met navigatieknoppen.

  ![Schuifregelaar voor Page Builder](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  Er is ook een groot aantal op jQuery gebaseerde afbeeldingslichtvakken beschikbaar op [[!DNL Commerce Marketplace]][1]en sommige zijn gratis.

- U kunt ook een extensie downloaden van [!DNL Commerce Marketplace]. Raadpleeg de documentatie die is verstrekt door de ontwikkelaar van de extensie voor meer informatie.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
