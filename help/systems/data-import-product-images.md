---
title: Importeren van productafbeelding
description: Leer hoe u productafbeeldingen importeert met het pad en de bestandsnaam van elke afbeelding.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Importeren van productafbeelding

Meerdere productafbeeldingen van elk type kunnen worden geïmporteerd in Adobe Commerce en Magento Open Source en zijn gekoppeld aan een specifiek product. Het pad en de bestandsnaam van elke productafbeelding worden in het CSV-bestand ingevoerd en de te importeren afbeeldingsbestanden worden geüpload naar het overeenkomstige pad op de Commerce-server of externe server.

Commerce maakt een eigen mappenstructuur voor productafbeeldingen die alfabetisch zijn geordend. Wanneer u productgegevens met bestaande afbeeldingen exporteert naar een CSV-bestand, wordt het alfabetische pad weergegeven vóór de bestandsnaam van elke afbeelding. Wanneer u echter nieuwe afbeeldingen importeert, hoeft u geen pad op te geven, omdat Commerce de mapstructuur automatisch beheert. Zorg er echter voor dat u het relatieve pad naar de importmap opgeeft vóór de bestandsnaam van elke afbeelding die u wilt importeren.

Als u afbeeldingen wilt uploaden, moet u over aanmeldingsgegevens en juiste machtigingen beschikken om toegang te krijgen tot de Commerce-map op de server. Met de juiste referenties kunt u elk SFTP-hulpprogramma gebruiken om de bestanden van uw desktopcomputer naar de server te uploaden.

Voordat u een groot aantal afbeeldingen gaat importeren, moet u eerst de stappen in de importmethode die u wilt gebruiken controleren en het proces met een paar producten doorlopen. Nadat u begrijpt hoe het werkt, zult u zeker voelen invoerend grote hoeveelheden beelden.

>[!IMPORTANT]
>
>Het wordt aanbevolen een programma te gebruiken dat UTF-8-codering ondersteunt voor het bewerken van CSV-bestanden, zoals Kladblok++. Microsoft® Excel voegt extra tekens in de kolomkop van het CSV-bestand in, waardoor de gegevens niet weer naar Commerce kunnen worden geïmporteerd.

## Methode 1: afbeeldingen importeren van de lokale server

1. Upload de afbeeldingsbestanden op de Commerce-server naar de map `var/import/images` of naar een submap, zoals `var/import/images/product_images` . Dit is de standaardhoofdmap voor het importeren van productafbeeldingen.

   ```
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Vanaf de release Adobe Commerce en Magento Open Source `2.3.2` wordt het pad dat in **[!UICONTROL Images File Directory]** is opgegeven, samengevoegd voor import naar de basismap images - `<Magento-root-folder>/var/import/images` . Voor eerdere Adobe Commerce- en Magento Open Source-releases kunt u een andere map op de Commerce-server gebruiken, mits het pad naar de map tijdens het importeren wordt opgegeven.

1. Voer in de CSV-gegevens de naam in van elk afbeeldingsbestand dat op de juiste rij, op `sku` en in de juiste kolom moet worden geïmporteerd op basis van het afbeeldingstype ( `base_image` , `small_image` , `thumbnail_image` of `additional_images`).

   >[!NOTE]
   >
   >Voor afbeeldingen in de standaard importmap (`var/import/images`) neemt u het pad vóór de bestandsnaam niet op in de CSV-gegevens.

   Het CSV-bestand mag alleen de kolom `sku` en de bijbehorende afbeeldingskolommen bevatten.

   ![ Voorbeeld - CSV de invoer van beeldgegevens ](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Volg de instructies aan [ invoer ](data-import.md) de gegevens.

1. Nadat u het te importeren bestand hebt geselecteerd, voert u het relatieve pad in na **[!UICONTROL Images File Directory]** .

   ```
   var/import/images
   ```

   ![ de invoer van gegevens beelddossier folder ](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Laat _[!UICONTROL Images File Directory]_&#x200B;leeg als u de map `<Magento-root-folder>/var/import/images` wilt gebruiken. Vanaf Adobe Commerce en Magento Open Source versie 2.3.2 is dit de standaardbasismap voor geïmporteerde afbeeldingen.

   Als u meerdere afbeeldingen voor één `sku` importeert, voegt u de afbeeldingen in in een kolom met de naam `additional_images` (voeg de kolom toe als deze nog niet is toegevoegd), gescheiden door komma&#39;s. Voorbeeld: `image02.jpg,image03.jpg`

## Methode 2: Afbeeldingen importeren van externe server

1. Upload de afbeeldingen die u wilt importeren naar de toegewezen map op de externe server.

1. Voer in de CSV-gegevens de volledige URL voor elk afbeeldingsbestand in in de juiste kolom op afbeeldingstype (`base_image`, `small_image`, `thumbnail_image` of `additional_images`).

   ```
   https://example.com/images/image.jpg
   ```

1. Volg de instructies aan [ invoer ](data-import.md) de gegevens.

## Methode 3: Afbeeldingen importeren met externe opslag

1. Upload de afbeeldingsbestanden in de module Extern opslaan naar de map `var/import/images` of een submap, zoals `var/import/images/product_images` . Dit is de standaardhoofdmap voor het importeren van productafbeeldingen.

   ```bash
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Vanaf de release Adobe Commerce en Magento Open Source `2.3.2` wordt het pad dat in _[!UICONTROL Images File Directory]_&#x200B;is opgegeven, samengevoegd voor import naar de basismap images: `<remote-storage-root-folder>/var/import/images` . Voor eerdere Adobe Commerce- en Magento Open Source-releases kunt u een andere map op de Commerce-server gebruiken zolang het pad naar de map tijdens het importeren is opgegeven.

1. Voer in de CSV-gegevens de naam in van elk afbeeldingsbestand dat op de juiste rij, op `sku` en in de juiste kolom moet worden geïmporteerd op basis van het afbeeldingstype ( `base_image` , `small_image` , `thumbnail_image` of `additional_images`).

   >[!NOTE]
   >
   >Voor afbeeldingen in de standaard importmap (`var/import/images`) neemt u het pad vóór de bestandsnaam niet op in de CSV-gegevens.

   Het CSV-bestand mag alleen de kolom `sku` en de bijbehorende afbeeldingskolommen bevatten.

   ![ Voorbeeld - CSV de invoer van beeldgegevens ](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Volg de instructies aan [ invoer ](data-import.md) de gegevens.

1. Nadat u het te importeren bestand hebt geselecteerd, voert u het relatieve pad in na **[!UICONTROL Images File Directory]** .

   ```
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >Laat _[!UICONTROL Images File Directory]_&#x200B;leeg om de map `<Magento-root-folder>/var/import/images` te gebruiken. Vanaf Adobe Commerce en Magento Open Source versie 2.3.2 is dit de standaardbasismap voor geïmporteerde afbeeldingen.

   Als u meerdere afbeeldingen voor één `sku` importeert, voegt u de afbeeldingen in in een kolom met de naam `additional_images` (voeg de kolom toe als deze nog niet is toegevoegd), gescheiden door komma&#39;s: `image02.jpg,image03.jpg`

Voor meer informatie over het toelaten van en het beheren van de Verre opslagmodule, zie [ verre opslag ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=nl-NL) in de _gids van de Configuratie_ vormen.

>[!NOTE]
>
>Als u productafbeeldingen importeert, wordt het formaat van de afbeelding niet gewijzigd. Afbeeldingen van producten worden op de voorgrond vergroot of verkleind met `pub/get.php` . Controleer of de `pub/get.php` goed werkt, anders wordt de grootte van de afbeeldingen mogelijk niet gewijzigd.
