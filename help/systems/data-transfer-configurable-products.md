---
title: Configureerbare producten importeren
description: Bekijk een voorbeeld van het invoeren van productgegevens voor een configureerbaar product.
exl-id: bb8b2a6d-867e-4ab2-bdfd-98a01d79c457
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Configureerbare producten importeren

De beste manier om te begrijpen hoe configureerbare productgegevens gestructureerd zijn, is een configureerbaar product en zijn variaties uit te voeren, en de gegevens in een spreadsheet te onderzoeken.

In het volgende voorbeeld voegt u een set productvariaties toe voor een nieuwe grootte in elke kleur. Eerst, voert u het configureerbare product uit, en onderzoekt de gegevensstructuur. Vervolgens werkt u de gegevens bij en importeert u deze weer in de catalogus. Als u niet door de oefening van het uitvoeren van de gegevens wilt gaan, kunt u het Csv- dossier downloaden dat in het voorbeeld wordt gebruikt.

![ de storefront van het Voorbeeld - grootte en kleurenattributen ](./assets/storefront-hoodie-new-size.png){width="700" zoomable="yes"}

## Stap 1: Verifieer de montages en de waarden van attributen

1. Voordat u begint, moet u ervoor zorgen dat de kenmerken die worden gebruikt voor productvariaties, de vereiste eigenschapinstellingen hebben.

   - [**[!UICONTROL Scope]**](../getting-started/websites-stores-views.md#scope-settings) - `Global`
   - [**[!UICONTROL Catalog Input Type for Store Owner]**](data-attributes-product.md) - Het invoertype van om het even welk attribuut dat voor een productvariatie wordt gebruikt moet één van het volgende zijn:

      - `Dropdown`
      - `Visual Swatch`
      - `Text Swatch`
      - `Multi-Select`

   - **[!UICONTROL Values Required]** - `Yes`

1. Als u een grootte of kleur toevoegt of een andere wijziging aanbrengt in een bestaand kenmerk, moet u het kenmerk bijwerken met de nieuwe waarde.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Zoek het kenmerk in de lijst en open in de bewerkingsmodus.

1. Voeg de nieuwe waarde toe aan het kenmerk.

   In het volgende voorbeeld wordt een nieuwe grootte toegevoegd aan een tekststaal.

   ![ attribuut van het Product - voeg nieuwe waarde ](./assets/data-transfer-configurable-product-add-new-attribute-value.png){width="500" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.

1. Als u een attribuut toevoegt, volg de instructies aan [ creeer de attributen ](../catalog/attribute-product-create.md) alvorens u begint.

## Stap 2: Exporteer het configureerbare product

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek het configureerbare product dat u wilt exporteren:

   - Klik op **[!UICONTROL Filters]**.
   - Stel **[!UICONTROL Type]** in op `Configurable Product` en klik op **[!UICONTROL Apply Filters]** .
   - Kies het configureerbare product dat u voor uw testuitvoer wilt gebruiken en neem nota van **[!UICONTROL SKU]**.

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

   ![ de uitvoermontages van Gegevens ](./assets/data-transfer-export-settings.png){width="600" zoomable="yes"}

1. Onder _[!UICONTROL Export Setting]s_, doe het volgende:

   - Stel **[!UICONTROL Entity Type]** in op `Products` .

   - Stel **[!UICONTROL Export File Format]** in op `CSV` .

1. Blader onder _[!UICONTROL Entity Attributes]_omlaag of gebruik het kenmerklabelfilter om het kenmerk **[!UICONTROL SKU]**te zoeken en voer de volgende handelingen uit:

   - Voer de SKU in van het configureerbare product dat u wilt exporteren en klik op **[!UICONTROL Continue]** .

     ![ de uitvoer SKU van Gegevens ](./assets/data-transfer-export-sku.png){width="600" zoomable="yes"}

   - Zoek het bestand op de downloadlocatie voor uw webbrowser en open het als spreadsheet.

     Het CSV-bestand heeft een aparte rij voor elke eenvoudige productvariatie en één rij voor het configureerbare product. In `product_type column` worden meerdere eenvoudige productvariaties weergegeven die aan één configureerbaar product zijn gekoppeld.

     ![ gegevens van het Voorbeeld - configureerbaar product met variaties ](./assets/data-transfer-csv-configurable-product.png){width="600" zoomable="yes"}

   - Schuif helemaal rechts van het werkblad naar de volgende kolommen.

      - `configurable_variations` - Bepaalt het één-aan-vele verband tussen het configureerbare productverslag en elke variatie.
      - `configurable_variation_labels` - Definieert het label dat elke variatie identificeert.

     In dit voorbeeld zijn de gegevens te vinden in de kolommen CG en CH. Afhankelijk van het aantal variaties, kan de tekenreeks met gegevens in de kolom `configurable_variations` lang zijn. De gegevens worden gebruikt als index voor de bijbehorende productvariaties en hebben de volgende structuur:

     ```text
     sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}| sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}
     ```

     Elke SKU wordt gescheiden door een pijpsymbool (|), en de attributen worden gescheiden door een komma. De waarde van elk attribuut wordt vertegenwoordigd door de attributencode, eerder dan het attributenetiket. Zo worden de werkelijke gegevens weergegeven:

     ```text
     sku=MH01-XS-Black,size=XS,color=Black|sku=MH01-XS-Gray,size=XS,color=Gray|sku=MH01-XS-Orange,size=XS,color=Orange</pre>
     ```

1. Wanneer u de structuur van configureerbare productgegevens begrijpt, kunt u de gegevens bewerken of nieuwe variaties rechtstreeks aan het CSV-bestand toevoegen.

   Meer leren, zie [ Complexe Gegevens ](data-attributes-product.md#complex-product-data-attributes).

## Stap 3: De gegevens bewerken

In het volgende voorbeeld wordt de set XL-formaten gekopieerd en in het werkblad geplakt om een set productvariaties te maken voor een nieuwe grootte in elke kleur.

1. Kopieer de set productvariaties die u als sjabloon voor de nieuwe producten wilt gebruiken.

   ![ Geëxporteerde gegevens - kopieer productvariaties ](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. Voeg de gekopieerde rijrecords in het werkblad in.

   U hebt nu twee identieke sets van de eenvoudige productvariaties.

   ![ CSV gegevens - voeg productvariaties ](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"} toe

1. Werk indien nodig de gegevens in de volgende kolommen van de nieuwe variaties bij.

   - `sku`
   - `name`
   - `url_key`
   - `additional_attributes`

   In dit voorbeeld worden alle `XL` -verwijzingen gewijzigd in `XXL` .

1. Werk de informatie in de `product_variations` kolom van het configureerbare productverslag bij, zodat de nieuwe variaties als deel van het configureerbare product inbegrepen zijn.

   Klik in de rij met de configureerbare productrecord op de cel die de `product_variations` -gegevens bevat. Kopieer vervolgens in de formuleringsbalk de laatste set parameters, te beginnen met het pijlsymbool.

   ![ product_variation gegevens ](./assets/data-transfer-export-configurable-product-product-variations-data.png){width="600" zoomable="yes"}

1. Plak de parameters aan het einde van de gegevens en bewerk deze naar wens voor de nieuwe variaties.

   In dit voorbeeld worden de parameters `sku` en `size` bijgewerkt voor de nieuwe XXL-grootte.

1. Verwijder alle rijen die niet zijn gewijzigd voordat de gegevens weer in de catalogus worden geïmporteerd.

   In dit voorbeeld worden alleen de drie nieuwe variaties voor de nieuwe grootte en de rij met het bijgewerkte configureerbare product weer geïmporteerd naar de catalogus. De andere rijen kunnen uit het CSV-bestand worden verwijderd. Zorg er echter voor dat u de koptekstrij niet met kolomlabels verwijdert.

   ![ CSV gegevens om in te voeren ](./assets/data-transfer-csv-configurable-product-data-ready-to-import.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]** het CSV-bestand.

   De gegevens kunnen nu in de catalogus worden geïmporteerd.

   >[!NOTE]
   >
   >Een importbestand mag niet groter zijn dan 2 MB.

## Stap 4: de bijgewerkte gegevens importeren

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Stel onder _[!UICONTROL Import Settings]_de waarde **[!UICONTROL Entity Type]**in op `Products` .

1. Stel onder _[!UICONTROL Import Behavior]_de waarde **[!UICONTROL Import Behavior]**in op `Add/Update` .

   ![ het invoergedrag van Gegevens ](./assets/data-transfer-configurable-product-import-behavior.png){width="600" zoomable="yes"}

1. Klik onder _[!UICONTROL File to Import]_op **[!UICONTROL Choose File]**en navigeer naar het CSV-bestand dat u hebt voorbereid voor importeren en kies het bestand.

   ![ het invoerdossier van Gegevens ](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Check Data]** .

1. Klik op **[!UICONTROL Import]** als het bestand geldig is.

   Corrigeer anders eventuele problemen in de gegevens en probeer het opnieuw.

   ![ het bericht van het Systeem - het dossier is geldig ](./assets/data-transfer-configurable-product-import-validation-results.png){width="600" zoomable="yes"}

1. Wanneer het importeren is voltooid, klikt u op **[!UICONTROL Cache Management]** in het bericht boven aan de pagina en vernieuwt u alle ongeldige cache.

   De nieuwe productvariaties zijn nu beschikbaar in de catalogus van de beheerder en in de winkel. In dit voorbeeld is het deksel nu beschikbaar in grootte XXL voor alle kleuren.
