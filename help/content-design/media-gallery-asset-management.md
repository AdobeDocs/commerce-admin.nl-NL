---
title: Middelen in galerie beheren
description: Leer hoe u geüploade mediabestanden en elementen die u via Adobe Stock-integratie aanschaft, beheert.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Middelen in galerie beheren

De nieuwe [&#x200B; Galerie van Media &#x200B;](media-gallery.md) verstrekt hulpmiddelen om geuploade media dossiers, en activa te beheren die u door de integratie van Adobe Stock [&#128279;](adobe-stock.md) verwerft. Als u een Adobe Stock [&#x200B; beeldvoorproef &#x200B;](adobe-stock-save-preview.md) hebt bewaard, kunt u [&#x200B; vergunning &#x200B;](adobe-stock-license-image.md) het beeld in de nieuwe Galerij van Media ook verlenen.

## Middelen uploaden

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klik op **[!UICONTROL Upload Image]**.

1. Selecteer het bestand dat u wilt uploaden.

   Het geselecteerde element wordt automatisch geüpload naar de geselecteerde map (of naar de opslagmap als er geen map is geselecteerd).

## Elementdetails weergeven

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klik de drie punten onder de activa (![&#x200B; pictogram van Details &#x200B;](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), dan klik **[!UICONTROL View Details]**.

   ![&#x200B; Acties van Activa &#x200B;](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   De elementdetails worden weergegeven in een deelvenster. Zij omvatten de informatie waar het actief wordt gebruikt:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![&#x200B; Details van Activa &#x200B;](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Klik op de koppelingen **[!UICONTROL Used In]** om de details weer te geven. In het raster in het volgende voorbeeld worden alle categorieën weergegeven waarin een specifiek element wordt gebruikt.

   ![&#x200B; Net van de Categorie &#x200B;](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   Het is ook mogelijk om de activa van de _sectie van de Details van de Mening_ te schrappen.

## Een element bewerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klik de drie punten onder de activa (![&#x200B; het menupictogram van Activa &#x200B;](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), dan klik **[!UICONTROL Edit]**.

   ![&#x200B; geef Activa &#x200B;](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"} uit

1. Wijzig zo nodig een van de volgende waarden voor metagegevens:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Deze gegevens worden opgeslagen in de database en in de metagegevens van het bestand zelf. XMP- en IPTC-indelingen worden momenteel ondersteund.

   U kunt de afbeelding downloaden met de bijgewerkte metagegevens.

## Een element gebruiken

Assets kan uitgebreid door Admin worden gebruikt, zoals [&#x200B; een pagina &#x200B;](page-add.md) toevoegen of uitgeven, [&#x200B; creeer of geef een categorie &#x200B;](../catalog/category-create.md) uit, of [&#x200B; neem beelden van de Redacteur van de Inhoud &#x200B;](editor-insert-image.md) op.

1. Open de nieuwe medialerie vanuit een gebied waarin u media-elementen kunt gebruiken.

1. Selecteer het element en klik op **[!UICONTROL Add Selected]** .

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Elementen verwijderen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klik op **[!UICONTROL Delete Images...]** en schakel het selectievakje in voor elk element dat u wilt verwijderen.

1. Klik op **[!UICONTROL Delete Image]** in het bevestigingsdialoogvenster.

   ![&#x200B; Bevestiging van de Schrapping &#x200B;](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Middelen zoeken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Gebruik de invoer **[!UICONTROL Search by keywords]** om het beeldonderzoek door sleutelwoorden/markeringen uit te voeren.

   Het onderzoek in het volgende voorbeeld vindt activa die een specifieke markering (`mountain`) bevatten.

   ![&#x200B; Onderzoek van Activa &#x200B;](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Leren hoe u beeldmarkeringen kunt bijwerken, zie _[activa](#edit-an-asset)_ sectie uitgeven.

## Elementen filteren

>[!NOTE]
>
>_Gebruikt in_ functionaliteit vereist dat [!UICONTROL Media Gallery Image Optimization] in de [&#x200B; configuratiemontages &#x200B;](media-gallery-image-optimization.md) wordt toegelaten.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klik op de tab **[!UICONTROL Filters]** .

   ![&#x200B; Filters &#x200B;](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Stel de filteropties in.

   U kunt de elementen filteren op basis van het gebruik door de entiteiten:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   U kunt de elementen ook filteren op **[!UICONTROL Store View]** , **[!UICONTROL License Status]** en **[!UICONTROL Content Status]** . Stel een datumbereik in voor **[!UICONTROL Uploaded Date]** en/of **[!UICONTROL Modification Date]** om elementen te filteren op basis van bestandsdatums.

1. Klik op **[!UICONTROL Apply Filters]** om de resultaten weer te geven.

   Het filtreren in het volgende voorbeeld vindt activa die in een specifieke categorie (`cars`) worden gebruikt en toegelaten.

   ![&#x200B; Filter voor Toegelaten Assets door Categorie &#x200B;](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Afbeeldingsduplicaten zoeken

1. Klik op de tab **[!UICONTROL Filters]** en selecteer het selectievakje **[!UICONTROL Show duplicates]** .

1. Klik op **[!UICONTROL Apply Filters]** om de resultaten weer te geven.

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
