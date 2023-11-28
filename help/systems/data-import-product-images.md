---
title: Importeren van productafbeelding
description: Leer hoe u productafbeeldingen importeert met het pad en de bestandsnaam van elke afbeelding.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Importeren van productafbeelding

Meerdere productafbeeldingen van elk type kunnen worden geïmporteerd in Adobe Commerce en Magento Open Source en zijn gekoppeld aan een specifiek product. Het pad en de bestandsnaam van elke productafbeelding worden ingevoerd in het CSV-bestand en de afbeeldingsbestanden die moeten worden geïmporteerd, worden geüpload naar het overeenkomstige pad op de Commerce-server of externe server.

De handel leidt tot zijn eigen folderstructuur voor productbeelden die alfabetisch wordt georganiseerd. Wanneer u productgegevens met bestaande afbeeldingen exporteert naar een CSV-bestand, wordt het alfabetische pad weergegeven vóór de bestandsnaam van elke afbeelding. Wanneer u echter nieuwe afbeeldingen importeert, hoeft u geen pad op te geven, omdat de mapstructuur automatisch wordt beheerd met de optie Handel. Zorg er echter voor dat u het relatieve pad naar de importmap opgeeft vóór de bestandsnaam van elke afbeelding die u wilt importeren.

Als u afbeeldingen wilt uploaden, hebt u aanmeldingsgegevens en juiste machtigingen nodig voor toegang tot de map Commerce op de server. Met de juiste referenties kunt u elk SFTP-hulpprogramma gebruiken om de bestanden van uw desktopcomputer naar de server te uploaden.

Voordat u een groot aantal afbeeldingen gaat importeren, moet u eerst de stappen in de importmethode die u wilt gebruiken controleren en het proces met een paar producten doorlopen. Nadat u begrijpt hoe het werkt, zult u zeker voelen invoerend grote hoeveelheden beelden.

>[!IMPORTANT]
>
>Het wordt aanbevolen een programma te gebruiken dat UTF-8-codering ondersteunt voor het bewerken van CSV-bestanden, zoals Kladblok++. Microsoft® Excel voegt extra karakters in de kolomkopbal van het Csv- dossier in, dat kan verhinderen de gegevens terug in Handel worden ingevoerd.

## Methode 1: afbeeldingen importeren van de lokale server

1. Upload de afbeeldingsbestanden op de Commerce-server naar `var/import/images` map of een submap, zoals `var/import/images/product_images`. Dit is de standaardhoofdmap voor het importeren van productafbeeldingen.

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Vanaf de Adobe Commerce en de Magento Open Source `2.3.2` versie, het pad dat is opgegeven in het dialoogvenster **[!UICONTROL Images File Directory]** schakelt deze aaneen voor import naar de basismap images - `<Magento-root-folder>/var/import/images`. Voor eerdere Adobe Commerce- en Magento Open Source-releases kunt u een andere map op de Commerce-server gebruiken, mits het pad naar de map tijdens het importproces is opgegeven.

1. Voer in de CSV-gegevens de naam in van elk afbeeldingsbestand dat op de juiste rij moet worden geïmporteerd, door `sku`en in de juiste kolom op basis van het afbeeldingstype (`base_image`, `small_image`, `thumbnail_image`, of `additional_images`).

   >[!NOTE]
   >
   Voor afbeeldingen in de standaardimportmap (`var/import/images`), neemt u het pad vóór de bestandsnaam niet op in de CSV-gegevens.

   Het CSV-bestand mag alleen het `sku` en de bijbehorende afbeeldingskolommen.

   ![Voorbeeld: CSV-afbeeldingsgegevens importeren](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Volg de instructies op [import](data-import.md) de gegevens.

1. Nadat u het te importeren bestand hebt geselecteerd, voert u het volgende relatieve pad in **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![Map voor het importeren van afbeeldingen](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   Verlaten _[!UICONTROL Images File Directory]_leeg om de `<Magento-root-folder>/var/import/images` directory. Vanaf Adobe Commerce en Magento Open Source versie 2.3.2 is dit de standaardbasismap voor geïmporteerde afbeeldingen.

   Als u meerdere afbeeldingen voor één afbeelding importeert `sku`, voegt u de afbeeldingen in een kolom in met de naam `additional_images` (voeg de kolom toe als deze nog niet is toegevoegd), gescheiden door komma&#39;s. Voorbeeld: `image02.jpg,image03.jpg`

## Methode 2: Afbeeldingen importeren van externe server

1. Upload de afbeeldingen die u wilt importeren naar de toegewezen map op de externe server.

1. Voer in de CSV-gegevens de volledige URL voor elk afbeeldingsbestand in in de juiste kolom op afbeeldingstype (`base_image`, `small_image`, `thumbnail_image`, of `additional_images`).

   ```terminal
   https://example.com/images/image.jpg
   ```

1. Volg de instructies op [import](data-import.md) de gegevens.

## Methode 3: Afbeeldingen importeren met externe opslag

1. Upload de afbeeldingsbestanden in de module Externe opslag naar de `var/import/images` map of een submap, zoals `var/import/images/product_images`. Dit is de standaardhoofdmap voor het importeren van productafbeeldingen.

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Vanaf de Adobe Commerce en de Magento Open Source `2.3.2` versie, het pad dat is opgegeven in het dialoogvenster _[!UICONTROL Images File Directory]_schakelt voor het importeren naar de basismap van de afbeelding samengevoegd: `<remote-storage-root-folder>/var/import/images`. Voor eerdere Adobe Commerce- en Magento Open Source-releases kunt u een andere map op de Commerce-server gebruiken zolang het pad naar de map tijdens het importeren is opgegeven.

1. Voer in de CSV-gegevens de naam in van elk afbeeldingsbestand dat op de juiste rij moet worden geïmporteerd, door `sku`en in de juiste kolom op basis van het afbeeldingstype (`base_image`, `small_image`, `thumbnail_image`, of `additional_images`).

   >[!NOTE]
   >
   Voor afbeeldingen in de standaardimportmap (`var/import/images`), neemt u het pad vóór de bestandsnaam niet op in de CSV-gegevens.

   Het CSV-bestand mag alleen het `sku` en de bijbehorende afbeeldingskolommen.

   ![Voorbeeld: CSV-afbeeldingsgegevens importeren](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Volg de instructies op [import](data-import.md) de gegevens.

1. Nadat u het te importeren bestand hebt geselecteerd, voert u het volgende relatieve pad in **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   Laat de _[!UICONTROL Images File Directory]_leeg om de `<Magento-root-folder>/var/import/images` directory. Vanaf Adobe Commerce en Magento Open Source versie 2.3.2 is dit de standaardbasismap voor geïmporteerde afbeeldingen.

   Als u meerdere afbeeldingen voor één afbeelding importeert `sku`, voegt u de afbeeldingen in een kolom in met de naam `additional_images` (voeg de kolom toe als deze nog niet is toegevoegd), gescheiden door komma&#39;s: `image02.jpg,image03.jpg`

Voor meer informatie over het toelaten en het beheren van de Verre opslagmodule, zie [Externe opslag configureren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) in de _Configuratiegids_.

>[!NOTE]
>
Als u productafbeeldingen importeert, wordt het formaat van de afbeelding niet gewijzigd. Afbeeldingen van het product worden op de voorgrond vergroot of verkleind `pub/get.php`. Zorg ervoor dat uw `pub/get.php` werkt correct; anders, kunnen de beelden niet resized.
