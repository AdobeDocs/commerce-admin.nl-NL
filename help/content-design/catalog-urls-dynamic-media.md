---
title: Dynamische media-URL's
description: Meer informatie over het gebruik van een dynamische media-URL als een relatieve verwijzing naar een afbeelding of ander media-element.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Dynamische media-URL&#39;s

Een dynamische media-URL is een relatieve verwijzing naar een afbeelding of ander media-element. Indien ingeschakeld, kunnen dynamische media-URL&#39;s worden gebruikt om rechtstreeks te koppelen aan elementen op uw server of aan bestanden die zijn opgeslagen op een [inhoudsleveringsnetwerk](media-storage-content-delivery-network.md). Het gebruik van dynamische media-URL&#39;s kan van invloed zijn op de prestaties van de catalogus en de [editor](editor.md#configure-the-editor) kan worden gevormd om of statische of dynamische media URLs te gebruiken.

Zoals bij alles [opmaaktags](../systems/markup-tags.md)De richtlijn staat tussen twee accolades. De indeling van een dynamische media-URL ziet er als volgt uit:

`\{\{media url="path/to/image.jpg"}}`

Dynamische URL-instructies worden verwerkt op basis van opgeslagen HTML-inhoud wanneer de pagina wordt weergegeven op de opslagruimte. Elke keer dat de pagina wordt gerenderd, wordt de inhoud gescand voor `\{\{media url="..."}}` en elke instructie wordt vervangen door de bijbehorende media-URL.

{{$include /help/_includes/directives-caution.md}}

## URL&#39;s van statische media configureren

Standaard hebben afbeeldingen die vanuit de WYSIWYG-editor in de catalogus worden ingevoegd, relatieve, dynamische URL&#39;s. Als u liever een statische URL gebruikt, kunt u de configuratie-instelling wijzigen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Content Management]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL WYSIWYG Options]** sectie.

   ![WYSIWYG-opties](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** op een van de volgende wijzen:

   - `Yes` - Gebruikt statische URLs voor media inhoud die met de redacteur WYSIWYG wordt opgenomen. Statische URL&#39;s zijn absoluut en onderbreken als de [basis-URL](../stores-purchase/store-urls.md) van de winkel wijzigen.

   - `No` - (Standaard) Gebruikt dynamische URL&#39;s voor media-inhoud die met de WYSIWYG-editor wordt ingevoegd, op basis van de `\{\{media url="..."}}` richtlijn. Dynamische URL&#39;s zijn relatief en worden niet afgebroken als de basis-URL van de winkel verandert.

1. Klik op **[!UICONTROL Save Config]**.
