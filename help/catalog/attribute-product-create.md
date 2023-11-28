---
title: Productkenmerken maken en verwijderen
description: Leer over het creëren van en het verwijderen van productattributen, die worden gebruikt om specifieke kenmerken van de producten in uw catalogus te beschrijven.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Productkenmerken maken en verwijderen

U kunt kenmerken maken terwijl u aan een product werkt of via het menu _[!UICONTROL Product Attributes]_pagina. In de volgende stappen wordt getoond hoe u kenmerken kunt maken op basis van de_[!UICONTROL Stores]_ -menu.

## Stap 1: Beschrijf de eigenschappen van de basiskenmerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Klik op **[!UICONTROL Add New Attribute]**.

   ![Nieuwe kenmerkeigenschappen](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Voor **[!UICONTROL Default Label]**, voert u een label in dat het kenmerk identificeert.

1. Om het type van inputcontrole te bepalen dat voor gegevensingang wordt gebruikt, reeks **[!UICONTROL Catalog Input Type for Store Owner]** op een van de volgende wijzen:

   | Eigenschap | Beschrijving |
   |--- |--- |
   | `Text Field` | Een invoerveld bestaande uit één regel voor tekst. |
   | `Text Area` | Een invoerveld met meerdere regels voor het invoeren van tekstalinea&#39;s, zoals een productbeschrijving. Met de WYSIWYG Editor kunt u de tekst opmaken met HTML-tags of de tags rechtstreeks in de tekst invoeren. |
   | `Text Editor` | Een volledig werkende tekstredacteur bij de attributenplaats. |
   | Datum | Hiermee wordt een datumwaarde weergegeven in het dialoogvenster [voorkeursindeling](attributes-input-types.md#date-and-time-options) en [tijdzone](../getting-started/store-details.md#locale-options). Datumwaarden kunnen worden geselecteerd in een lijst of kalender ( ![Kalenderpictogram](../assets/icon-calendar.png) ). <br/><br/>**_Opmerking:_**Afhankelijk van uw systeemconfiguratie,_Beheerder _gebruikers kunnen rechtstreeks datums in een veld invoeren of een datum in de kalender of lijst selecteren. Voor informatie over het specificeren van datum en tijdwaarden, zie [Datum- en tijdopties](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Hiermee geeft u een vervolgkeuzelijst weer met vooraf gedefinieerde opties voor `Yes` en `No`. |
   | `Dropdown` | Hiermee wordt een vervolgkeuzelijst met waarden weergegeven waarin slechts één selectie wordt geaccepteerd. Het invoertype Vervolgkeuzelijst is een sleutelcomponent van [configureerbare producten](product-create-configurable.md). |
   | `Multiple Select` | Hiermee geeft u een vervolgkeuzelijst weer met waarden die meerdere selecties accepteren. |
   | `Price` | Dit inputtype wordt gebruikt om prijsgebieden tot stand te brengen die naast de vooraf bepaalde attributen zijn: Prijs, Speciale Prijs, de Prijs van de Rij, en Kosten. De gebruikte valuta wordt bepaald door uw systeemconfiguratie. |
   | `Media Image` | Hiermee wordt een extra afbeelding aan een product gekoppeld, zoals een productlogo, zorginstructies of ingrediënten uit een voedseletiket. Wanneer u een kenmerk van een mediaafbeelding toevoegt aan de kenmerkset van een product, wordt dit een extra afbeeldingstype, samen met Basis, Klein en Miniatuur. Het kenmerk Media image kan worden uitgesloten van het dialoogvenster [storefront media browser](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Hiermee kunt u definiëren [FPT-snelheden](../stores-purchase/fixed-product-tax.md) op basis van de vereisten van uw landinstelling. |
   | `Visual Swatch` | Hiermee geeft u een staal weer met de kleur, structuur of patroon van een configureerbaar product. A [visueel staal](swatches.md) kan worden gevuld met een hexadecimale kleurwaarde of een geüploade afbeelding weergeven die de kleur, het materiaal, de structuur of het patroon van de optie vertegenwoordigt. |
   | `Text Swatch` | Een op tekst gebaseerde representatie van een configureerbare productoptie die vaak voor de grootte wordt gebruikt. [Tekststalen](swatches.md#text-based-swatches) kan ook hexadecimale kleurwaarden bevatten. |
   | `Page Builder` | Een volledig functionerende [Page Builder](../page-builder/introduction.md) werkruimte op de kenmerklocatie, zodat u gemakkelijk aansprekende inhoud aan de productpagina kunt toevoegen. |

   {style="table-layout:auto"}

1. Als u een optie wilt selecteren voordat de klant het product kan kopen, stelt u **[!UICONTROL Values Required]** tot `Yes`.

1. Voor [!UICONTROL Dropdown] en [!UICONTROL Multiple Select] Voer de volgende handelingen uit voor invoertypen:

   - Onder _[!UICONTROL Manage Options]_, klikt u op **[!UICONTROL Add Option]**.

   - Voer de eerste waarde in die u in de lijst wilt weergeven.

     U kunt één waarde voor Admin, en een vertaling van de waarde voor elke archiefmening ingaan. Als u slechts één winkelweergave hebt, kunt u alleen de Admin-waarde invoeren en deze wordt ook voor de winkel gebruikt.

   - Klikken **[!UICONTROL Add Option]** en herhaal de vorige stap voor elke optie die u in de lijst wilt opnemen.

   - Selecteren **[!UICONTROL Is Default]** om de optie als standaardwaarde te gebruiken.

   ![Productkenmerk - opties beheren](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Stap 2: Beschrijf de geavanceerde eigenschappen (indien nodig)

1. Voer een unieke waarde in **[!UICONTROL Attribute Code]** in kleine letters en zonder spaties.

   ![Productkenmerk - geavanceerde eigenschappen](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Welke opties beschikbaar zijn, is afhankelijk van de _[!UICONTROL Catalog Input Type for Store Owner]_instellen.

1. Set **[!UICONTROL Scope]** om aan te geven waar in uw [opslaghiërarchie](../getting-started/websites-stores-views.md) dat het kenmerk kan worden gebruikt.

1. Als u dubbele waarden wilt voorkomen, stelt u **[!UICONTROL Unique Value]** tot `Yes`.

1. Voer voor invoertypen die waarden invoeren een geldigheidstest uit voor alle gegevens die in een tekstveld worden ingevoerd door **[!UICONTROL Input Validation for Store Owner]** op het type gegevens dat het veld moet bevatten.

   Dit veld is niet beschikbaar voor invoertypen met geselecteerde waarden. De test kan elk van de volgende valideringen uitvoeren:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Invoervalidatie](./assets/product-attribute-input-validation.png){width="400"}

1. Deze eigenschap toevoegen aan de [Lijst met producten](products-list.md)stelt u de volgende opties in op `Yes`.

   - **Opties voor Toevoegen aan kolom** - Hiermee neemt u het kenmerk op als een kolom in het dialoogvenster _[!UICONTROL Products]_lijst.
   - **Gebruiken in filteropties** - Voegt een filtercontrole aan de kolomkopbal in toe _[!UICONTROL Products]_lijst.

## Stap 3: Voer het veldlabel in

1. Kies in de navigatie aan de linkerkant de optie **[!UICONTROL Manage Labels]**.

1. Voer een **[!UICONTROL Title]** te gebruiken als label voor het veld.

   Als uw winkel in verschillende talen beschikbaar is, kunt u voor elke weergave een vertaalde titel invoeren.

   ![Productkenmerk - titels beheren](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Stap 4: Beschrijf de storefront-eigenschappen

1. Kies in de navigatie aan de linkerkant de optie **[!UICONTROL Storefront Properties]**.

   ![Productkenmerken - eigenschappen van winkel](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Welke opties beschikbaar zijn, is afhankelijk van de _[!UICONTROL Catalog Input Type for Store Owner]_instellen.

1. Als het kenmerk beschikbaar moet zijn voor zoeken, stelt u **[!UICONTROL Use in Search]** tot `Yes`.

   - Stel de **[!UICONTROL Search Weight]** Waarde die bepaalt waar het item wordt weergegeven in de zoekresultaten: 1 (laagste gewicht) tot 10 (hoogste gewicht).

   - Stel de **[!UICONTROL Visible in Advanced Search]** indien nodig. Meer informatie in [Geavanceerd zoeken](search.md#advanced-search).

1. Als u het kenmerk in Product vergelijken wilt opnemen, stelt u **[!UICONTROL Comparable on Storefront]** tot `Yes`.

1. Ga als volgt te werk voor vervolgkeuzelijsten, meerdere velden voor selecteren en prijzen:

   - Als u het kenmerk als een filter in gelaagde navigatie wilt gebruiken, stelt u **[!UICONTROL Use in Layered Navigation]** tot `Yes`.

   - Als u het kenmerk in gelaagde navigatie wilt gebruiken op pagina&#39;s met zoekresultaten, stelt u **[!UICONTROL Use in Search Results Layered Navigation]** tot `Yes`.

   - Voor **[!UICONTROL Position]** voert u een getal in om de relatieve positie van het kenmerk in het gelaagde navigatieblok aan te geven.

1. Als u het kenmerk wilt gebruiken in prijsregels, stelt u **[!UICONTROL Use for Promo Rule Conditions]** tot `Yes`.

1. Als u wilt toestaan dat de tekst wordt opgemaakt met HTML, stelt u **[!UICONTROL Allow HTML Tags on Frontend]** tot `Yes`.

   Deze instelling stelt de WYSIWYG-editor beschikbaar voor het veld.

1. Als u het kenmerk op de productpagina wilt opnemen, stelt u **[!UICONTROL Visible on Catalog Pages on Storefront]** tot `Yes`.

1. Vul de volgende instellingen in als dit door uw thema wordt ondersteund:

   - Als u het kenmerk wilt opnemen in productaanbiedingen, stelt u **[!UICONTROL Used in Product Listing]** tot `Yes`.

   - Als u kenmerk wilt gebruiken als een sorteerparameter voor productaanbiedingen, stelt u **[!UICONTROL Used for Sorting in Product Listing]** tot `Yes`.

1. Klik op **[!UICONTROL Save Attribute]**.

## Stap 5: Wijs het gemaakte kenmerk toe aan de kenmerkset

Als u wilt dat een kenmerk zichtbaar is op de pagina voor het maken van het product, voegt u het toe aan een specifieke kenmerkset.

1. Ga na het voltooien van de vorige stappen naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Selecteer de kenmerkset die u nodig hebt in de lijst en open deze in de bewerkingsmodus.

1. Sleep het gemaakte kenmerk van het dialoogvenster **[!UICONTROL Unassigned Attributes]** aan de aangewezen omslag in **Groepen** kolom.

1. Klik op **[!UICONTROL Save]**.

## Attributen voor configureerbare producten

Elk kenmerk dat wordt gebruikt als een vervolgkeuzelijst met opties voor een [configureerbaar product](product-create-configurable.md) moeten de volgende eigenschappen hebben:

| Eigenschap | Waarde |
|----------|------ |
| Invoertype catalogus voor winkeleigenaar | Vervolgkeuzelijst |
| Toepassingsgebied | Algemeen |

{style="table-layout:auto"}

## Een kenmerk verwijderen

Wanneer een attribuut wordt geschrapt, wordt het verwijderd uit om het even welke verwante producten en attributenreeksen. Systeemkenmerken maken deel uit van de kernfunctionaliteit van uw winkel en kunnen niet worden verwijderd.

Voordat u een kenmerk verwijdert, moet u ervoor zorgen dat dit momenteel niet wordt gebruikt door een product in de catalogus. Een gemakkelijke manier om te bepalen als een attribuut in gebruik is is het gebruiken van [Exporteren](../systems/data-export.md) om de lijst met kenmerken van productentiteiten te controleren. Als het kenmerk niet in de lijst staat, wordt het niet gebruikt door producten in de catalogus.

**_Een kenmerk verwijderen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Zoek het kenmerk in de lijst en open de bewerkingsmodus.

1. Klik op **[!UICONTROL Delete Attribute]**.

   ![Kenmerk verwijderen](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.
