---
title: Media-opslag
description: Leer hoe u met media-opslag mediabestanden die op de server zijn opgeslagen, kunt organiseren en gebruiken.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Media-opslag

Met Media-opslag kunt u mediabestanden die op de server zijn opgeslagen, ordenen en toegang krijgen. Het pad naar de locatie van de bestanden wordt bepaald door de [basis-URL](../stores-purchase/store-urls.md) configuratie. Bestanden in mediaopslag zijn toegankelijk vanuit de editor wanneer u werkt aan pagina&#39;s en statische blokken. Meestal bevindt de mediaopslag zich in het bestandssysteem op dezelfde server als de [!DNL Commerce] programmabestanden.

U kunt mediabestanden ook beheren in een [database](media-storage-database.md), of op een aparte server of [inhoudsleveringsnetwerk](media-storage-content-delivery-network.md). Het voordeel van het gebruik van alternatieve opslag is dat hierdoor de vereiste inspanningen voor het synchroniseren van media tot een minimum worden beperkt. De prestaties van de synchronisatie worden vooral beïnvloed wanneer de veelvoudige instanties van het systeem op verschillende servers worden opgesteld die toegang tot de zelfde beelden, CSS dossiers, en andere media dossiers vereisen.

De redacteur kan worden gevormd om of statisch te gebruiken of [dynamische media-URL&#39;s](../catalog/catalog-urls.md#configure-catalog-media-url-format) voor inhoud van catalogus in categorie- of productbeschrijvingen.

![[!DNL Commerce] Media-opslag](./assets/media-storage.png){width="650" zoomable="yes"}

## Bestanden toevoegen aan de mediaopslag

De eerste twee stappen zijn hetzelfde als wanneer u een afbeelding invoegt.

1. Op de [editor](editor.md) klikt u op de _Afbeelding invoegen_ pictogram.

   ![Pictogram Afbeelding invoegen](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Deze handeling opent de _[!UICONTROL Insert/edit image]_in.

1. Na _[!UICONTROL Source]_klikt u op de knop_ Zoeken _icon (![Zoekpictogram](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Voer een van de volgende handelingen uit in de mappenstructuur aan de linkerkant:

   - Navigeer naar de map waarin u de geüploade afbeelding wilt opslaan.

   - Navigeer naar de plaats waar u een map wilt maken en klik **Map maken**.

     Als u een map wilt toevoegen, voert u de mapnaam in en klikt u op **[!UICONTROL OK]**.

1. Als u een of meer bestanden wilt toevoegen aan Media Storage, kunt u de bestanden van uw systeem uploaden of de [Adobe Stock-integratie](adobe-stock.md):

   Als u bestanden vanaf uw systeem wilt uploaden, klikt u op **[!UICONTROL Choose Files]** en voer de volgende handelingen uit:

   - Navigeer in de map van uw lokale computer naar de locatie van de afbeeldingen.

   - Selecteer elke afbeelding die u wilt uploaden.

   - Klik op **[!UICONTROL Open]**.

   Als u middelen van Adobe Stock wilt gebruiken met de [integratie](adobe-stock.md):

   - Klik op **[!UICONTROL Search Adobe Stock]**.

   - Een voorvertoning of afbeelding met licentie toevoegen vanuit Adobe Stock (zie [Adobe Stock-afbeeldingen gebruiken](adobe-stock-manage.md)).

De afbeeldingen worden geüpload naar de huidige map Media Storage op de server.

![[!DNL Commerce] Media-opslag](./assets/media-storage.png){width="650" zoomable="yes"}

## Een afbeelding invoegen uit media-opslag

Open de pagina of het blok dat u wilt bewerken. Gebruik vervolgens een van de volgende methoden om een afbeelding van mediaopslag in te voegen:

### Methode 1: WYSIWYG-modus

1. Op de [editor](editor.md) klikt u op de _Afbeelding invoegen_ pictogram.

1. Na _[!UICONTROL Source]_klikt u op de knop_ Zoeken _icon (![Zoekpictogram](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Het zoekpictogram selecteren](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Navigeer in de mappenstructuur aan de linkerkant naar de map waarin de afbeelding is opgeslagen.

1. Selecteer de tegel van de afbeelding en klik op **[!UICONTROL Add Selected]**.

### Methode 2: modus HTML

1. Plaats de cursor in de code op de positie waar de `<img>` -tag wordt ingevoegd.

1. Klik op **[!UICONTROL Insert Image]**.

   ![Afbeelding invoegen (modus HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
