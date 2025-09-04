---
title: Dynamische media-URL's
description: Meer informatie over het gebruik van een dynamische media-URL als een relatieve verwijzing naar een afbeelding of ander media-element.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamische media-URL&#39;s

Een dynamische media-URL is een relatieve verwijzing naar een afbeelding of ander media-element. Wanneer toegelaten, kunnen de dynamische media URLs worden gebruikt om rechtstreeks met activa op uw server, of aan dossiers te verbinden die op het netwerk van de inhoudslevering van a [ worden opgeslagen ](media-storage-content-delivery-network.md). Het gebruik van dynamische media URLs kan catalogusprestaties beïnvloeden, en de [ redacteur ](editor.md#configure-the-editor) kan worden gevormd om of statische of dynamische media URLs te gebruiken.

Zoals met alle [ prijsverhogingsmarkeringen ](../systems/markup-tags.md), is de richtlijn ingesloten in dubbele krullende steunen. De indeling van een dynamische media-URL ziet er als volgt uit:

`\{\{media url="path/to/image.jpg"}}`

Dynamische URL-instructies worden verwerkt op basis van opgeslagen HTML-inhoud wanneer de pagina in de winkel wordt weergegeven. Elke keer dat de pagina wordt weergegeven, wordt de inhoud gescand voor `\{\{media url="..."}}` en wordt elke aanwijzing vervangen door de bijbehorende media-URL.

{{$include /help/_includes/directives-caution.md}}

## URL&#39;s van statische media configureren

Afbeeldingen die vanuit de WYSIWYG-editor in de catalogus worden ingevoegd, hebben standaard relatieve, dynamische URL&#39;s. Als u liever een statische URL gebruikt, kunt u de configuratie-instelling wijzigen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_de optie **[!UICONTROL Content Management]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL WYSIWYG Options]** sectie uit.

   ![ de Opties van WYSIWYG ](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** in op een van de volgende opties:

   - `Yes` - Gebruikt statische URL&#39;s voor media-inhoud die met de WYSIWYG-editor is ingevoegd. Statische URLs is absolute en onderbreking als [ basis URL ](../stores-purchase/store-urls.md) van de opslag verandert.

   - `No` - (Standaard) Gebruikt dynamische URL&#39;s voor media-inhoud die met de WYSIWYG-editor wordt ingevoegd, op basis van de instructie `\{\{media url="..."}}` . Dynamische URL&#39;s zijn relatief en worden niet afgebroken als de basis-URL van de winkel verandert.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
