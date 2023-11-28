---
title: De [!DNL Media Gallery]
description: Met de medialerie kunt u uw mediabestanden op de server ordenen en beheren.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# De [!DNL Media Gallery]

Met Adobe Commerce of Magento Open Source 2.4 kunnen handelaren de nieuwe _verbeterd_ [!DNL Media Gallery] om hun mediabestanden op de server te organiseren en te beheren. Deze nieuwe [!DNL Media Gallery] bevat dezelfde functies als de bestaande media-opslag, maar omvat een verbeterde gebruikersinterface en een nauwere integratie met [Adobe Stock][adobe-stock].

![Afbeeldingen die worden weergegeven in het raster Media Gallery](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Productafbeeldingen toegevoegd aan de [_[!UICONTROL Images and Videos]_productsectie](../catalog/product-image.md#upload-an-image) niet worden beheerd door de [!DNL Media Gallery]. Alleen afbeeldingen die worden gebruikt in het dialoogvenster_[!UICONTROL Content]_ de gebieden van de productsectie worden getoond en gefiltreerd in het nieuwe [!DNL Media Gallery].

## De nieuwe [!DNL Media Gallery]

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Geavanceerde configuratie - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable Old Media Gallery]** tot `No`.

1. Klik op **[!UICONTROL Save Config]**.

1. Klik op de knop **[!UICONTROL Cache Management]** koppeling in het systeembericht en vernieuw de ongeldige cache.

   De [[!UICONTROL Content] menu](/help/content-design/content-menu.md) geeft nu de nieuwe _[!UICONTROL Media Gallery]_-optie.

>[!NOTE]
>
>Volledige functionaliteit voor nieuwe [!DNL Media Gallery] vereist `media.gallery.synchronization` en `media.content.synchronization` gebruikers in de wachtrij voor eerste synchronisatie. Zie [Berichtenrijen beheren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in de _Configuratiegids_ voor meer informatie .

## Toegang krijgen tot de nieuwe [!DNL Media Gallery]

De nieuwe [!DNL Media Gallery] is toegankelijk via het menu Inhoud of wanneer u [Een pagina toevoegen of bewerken](/help/content-design/page-add.md). U kunt het ook openen wanneer u [een categorie maken of bewerken](/help/catalog/category-create.md)of wanneer u [afbeeldingen invoegen met de Content Editor](/help/content-design/editor-insert-image.md).

Toegang krijgen tot de nieuwe [!UICONTROL Media Gallery] via de [!UICONTROL Content] menu:

- Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

De nieuwe medialerie openen wanneer u een pagina toevoegt of bewerkt:

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klik op **[!UICONTROL Add a New Page]**.

   Als u een bestaande pagina wilt bewerken, kunt u de _[!UICONTROL Action]_te klikken kolom **[!UICONTROL Select]**en kiest u **[!UICONTROL Edit]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Content]** en voer de volgende handelingen uit:

   - Als u [Page Builder ingeschakeld](../page-builder/setup.md), breid de **[!UICONTROL Media]** en sleep een **[!UICONTROL Image]** plaatsaanduiding naar de doelcontainer. Klik vervolgens op **[!UICONTROL Select from Gallery]**.

     ![Afbeelding naar werkgebied slepen](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Als u de [WYSIWYG-editor ingeschakeld](/help/content-design/editor.md), klikt u op **[!UICONTROL Show/Hide Editor]** en klik vervolgens op **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

Meer informatie over de [!DNL Media Gallery]Bekijk deze video:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

