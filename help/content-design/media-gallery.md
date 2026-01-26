---
title: The [!DNL Media Gallery]
description: Met de medialerie kunt u uw mediabestanden op de server ordenen en beheren.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# De [!DNL Media Gallery]

Met Adobe Commerce of Magento Open Source 2.4, kunnen de handelaren nieuwe _verbeterde_ gebruiken [!DNL Media Gallery] om hun media dossiers op de server te organiseren en te beheren. Dit nieuwe [!DNL Media Gallery] bevat de zelfde functionaliteit zoals de bestaande media opslag, maar omvat een beter gebruikersinterface en een nauwere integratie met [&#x200B; Adobe Stock &#x200B;](https://stock.adobe.com).

![&#x200B; Beelden die in het net van de Galerij van Media worden getoond &#x200B;](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Productafbeeldingen die worden toegevoegd aan de [_[!UICONTROL Images and Videos]_&#x200B;productsectie &#x200B;](../catalog/product-image.md#upload-an-image) , worden niet beheerd door de [!DNL Media Gallery] . Alleen afbeeldingen die worden gebruikt in de velden van de productsectie van&#x200B;_[!UICONTROL Content]_ , worden weergegeven en gefilterd in de nieuwe [!DNL Media Gallery] .

## De nieuwe functie inschakelen [!DNL Media Gallery]

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]** uit.

   ![&#x200B; Geavanceerde configuratie - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable Old Media Gallery]** in op `No` .

1. Klik op **[!UICONTROL Save Config]**.

1. Klik op de koppeling **[!UICONTROL Cache Management]** in het systeembericht als daarom wordt gevraagd en vernieuw de ongeldige cache.

   In het [[!UICONTROL Content] menu &#x200B;](/help/content-design/content-menu.md) wordt nu de nieuwe optie _[!UICONTROL Media Gallery]_&#x200B;weergegeven.

>[!NOTE]
>
>Volledige functionaliteit voor nieuwe [!DNL Media Gallery] vereist dat `media.gallery.synchronization` - en `media.content.synchronization` -gebruikers in de wachtrij worden gestart voor eerste synchronisatie. Zie [&#x200B; berichtrijen &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=nl-NL) beheren in de _Gids van de Configuratie_ voor meer details.

## Toegang krijgen tot de nieuwe [!DNL Media Gallery]

Nieuw [!DNL Media Gallery] is toegankelijk van het menu van de Inhoud of wanneer u [&#x200B; een pagina &#x200B;](/help/content-design/page-add.md) toevoegt of uitgeeft. U kunt tot het ook toegang hebben wanneer u [&#x200B; creeert of een categorie &#x200B;](/help/catalog/category-create.md) uitgeeft, of wanneer u [&#x200B; beelden opneemt gebruikend de Redacteur van de Inhoud &#x200B;](/help/content-design/editor-insert-image.md).

Toegang krijgen tot het nieuwe [!UICONTROL Media Gallery] via het menu [!UICONTROL Content] :

- Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

De nieuwe medialerie openen wanneer u een pagina toevoegt of bewerkt:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klik op **[!UICONTROL Add a New Page]**.

   Als u een bestaande pagina wilt bewerken, klikt u op de kolom _[!UICONTROL Action]_&#x200B;en kiest u **[!UICONTROL Select]**.**[!UICONTROL Edit]**

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie uit en doe het volgende:

   - Als u [&#x200B; toegelaten Bouwer van de Pagina &#x200B;](../page-builder/setup.md) hebt, breid het **[!UICONTROL Media]** paneel uit en sleep **[!UICONTROL Image]** placeholder aan de doelcontainer. Klik vervolgens op **[!UICONTROL Select from Gallery]** .

     ![&#x200B; beeld van de belemmering aan stadium &#x200B;](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Als u de [&#x200B; toegelaten redacteur van WYSIWYG &#x200B;](/help/content-design/editor.md) hebt, klik **[!UICONTROL Show/Hide Editor]** en klik dan **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

Bekijk deze video voor meer informatie over [!DNL Media Gallery] :

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)
