---
title: Kenmerken toevoegen aan een product
description: Leer hoe u kenmerken aan producten in uw catalogus kunt toevoegen.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 45d69ccc1a5a6a7b8d072465c19829a76dde826d
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Kenmerken toevoegen aan een product

Hoewel de attributen hoofdzakelijk van het [&#x200B; Opslag &#x200B;](../stores-purchase/stores-menu.md) menu worden beheerd, kunt u nieuwe attributen _op de vlucht_ ook toevoegen terwijl het werken aan een product. U kunt een keuze maken in de lijst met bestaande kenmerken of een kenmerk maken. Het nieuwe attribuut wordt toegevoegd aan de [&#x200B; geplaatste attributen &#x200B;](../catalog/attribute-sets.md) waarop het product gebaseerd is.

## Stap 1: Een kenmerk toevoegen

1. Open het product in de bewerkingsmodus.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Attribute]** .

   ![&#x200B; Nieuw product met standaard geplaatste attributen &#x200B;](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Om een bestaand attribuut aan het product toe te voegen, gebruik de [&#x200B; filtercontroles &#x200B;](../getting-started/admin-grid-controls.md) om de attributen in het net te vinden en het volgende te doen:

   - Schakel het selectievakje in de eerste kolom van elk kenmerk dat u wilt toevoegen in.

   - Klik op **[!UICONTROL Add Selected]**.

   ![&#x200B; Uitgezocht een attribuut &#x200B;](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Als u een nieuw kenmerk wilt definiëren, klikt u op **[!UICONTROL Create New Attribute]** en vult u de items in Stap 2 in.

## Stap 2: Beschrijf de eigenschappen van het basiskenmerk

![&#x200B; Eigenschappen van Attributen &#x200B;](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Voer onder _[!UICONTROL Attribute Properties]_&#x200B;een **[!UICONTROL Attribute Label]**&#x200B;in om het kenmerk te identificeren.

1. Plaats **[!UICONTROL Catalog Input Type for Store Owner]** aan het type van [&#x200B; inputcontrole &#x200B;](attributes-input-types.md) dat voor gegevensingang moet worden gebruikt.

   Als het attribuut voor a [&#x200B; configureerbaar product &#x200B;](product-create-configurable.md) wordt gebruikt, kies `Dropdown`. Stel vervolgens **[!UICONTROL Required]** in op `Yes` .

1. Ga als volgt te werk voor invoertypen `Dropdown` en `Multiple Select` :

   - Klik onder **[!UICONTROL Values]** op **[!UICONTROL Add Value]** .

   - Voer de eerste waarde in die u in de lijst wilt weergeven.

     U kunt één waarde voor Admin en een vertaling van de waarde voor elke archiefmening ingaan. Als u slechts één winkelweergave hebt, kunt u alleen de Admin-waarde invoeren en deze wordt ook voor de winkel gebruikt.

   - Klik op **[!UICONTROL Add Value]** en herhaal de vorige stap voor elke optie die u in de lijst wilt opnemen.

   - Selecteer **[!UICONTROL Is Default]** om de optie als standaardwaarde te gebruiken.

   ![&#x200B; Waarden &#x200B;](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Required]** in op `Yes` als u wilt dat de klant een optie kiest voordat het product kan worden aangeschaft.

## Stap 3: Beschrijf de geavanceerde eigenschappen (optioneel)

![&#x200B; Geavanceerde Eigenschappen van Attributen &#x200B;](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Voer een unieke **[!UICONTROL Attribute Code]** in in kleine letters en zonder spaties.

1. Stel **[!UICONTROL Scope]** in om aan te geven waar in de winkelhiërarchie het kenmerk kan worden gebruikt.

   Als het attribuut voor a [&#x200B; configureerbaar product &#x200B;](product-create-configurable.md) wordt gebruikt, kies `Global`.

1. Als dit kenmerk alleen op dit product van toepassing is, stelt u **[!UICONTROL Unique Value]** in op `Yes` .

1. Als u een geldigheidstest wilt uitvoeren voor gegevens die in een tekstveld worden ingevoerd, stelt u **[!UICONTROL Input Validation for Store Owner]** in op het type gegevens dat het veld moet bevatten.

   Dit veld is niet beschikbaar voor invoertypen met geselecteerde waarden. Invoervalidatie kan worden gebruikt voor:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![&#x200B; Bevestiging van de Input &#x200B;](./assets/product-attribute-input-validation.png){width="500"}

1. Als u het kenmerk wilt kunnen opnemen als een kolom in het raster Producten, stelt u **[!UICONTROL Add to Column Options]** in op `Yes` .

1. Als u het _[!UICONTROL Products]_&#x200B;raster door deze kolom wilt filteren, stelt u **[!UICONTROL Use in Filter Options]**&#x200B;in op `Yes` .

## Stap 4: Voer het veldlabel in

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Manage titles]** sectie uit.

1. Voer een **[!UICONTROL Title]** in die als label voor het veld moet worden gebruikt.

   Als uw winkel in verschillende talen beschikbaar is, kunt u voor elke weergave een vertaalde titel invoeren.

   ![&#x200B; beheert Titels &#x200B;](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > Als u dit kenmerk als facet wilt gebruiken in Live zoeken, moet u een archiefspecifiek label opgeven. Zonder dit, kan de attributennaam niet correct op de pagina van de facetconfiguratie tonen. Om de configuratie bij te werken, geef manueel het etiket uit gebruikend [&#x200B; uitgeeft optie in de Levende lijst van het Onderzoek facet &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) in de _Levende Gids van het Onderzoek_.

## Stap 5: Beschrijf de storefront-eigenschappen

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Storefront Properties]** sectie uit.

   ![&#x200B; Eigenschappen Storefront &#x200B;](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Use in Search]** in op `Yes` als u het kenmerk beschikbaar wilt maken voor zoeken.

1. Als u het kenmerk in Product vergelijken wilt opnemen, stelt u **[!UICONTROL Comparable on Storefront]** in op `Yes` .

1. Als u vervolgkeuzelijsten, meerdere selecties of prijskenmerken wilt opnemen in gelaagde navigatie, stelt u **[!UICONTROL Use in Search Results Layered Navigation]** in op een van de volgende opties:

   - `Filterable (with results)` - Gelaagde navigatie omvat slechts die filters waarvoor de passende producten kunnen worden gevonden. Kenmerkwaarde die al van toepassing is op alle producten in de lijst, wordt niet weergegeven als een beschikbaar filter. Kenmerkwaarden met een aantal van nul (0) overeenkomende producten worden ook weggelaten uit de lijst met beschikbare filters.<br/><br/> de gefiltreerde lijst van producten omvat slechts de producten die de filter aanpassen. De lijst met producten wordt alleen bijgewerkt als de geselecteerde filters wijzigen wat wordt weergegeven.

   - `Filterable (no results)` - Gelaagde navigatie omvat filters voor alle beschikbare attributenwaarden en hun productaantallen, met inbegrip van de producten met nul (0) productgelijken. Als de kenmerkwaarde een staal is, wordt de waarde weergegeven als een filter, maar uitgestreept.

   >[!NOTE]
   >
   >Wanneer de instelling _[!UICONTROL Use in Search]_&#x200B;is ingesteld op `No` , wordt de instelling&#x200B;_[!UICONTROL Use in Search Results Layered Navigation]_ niet weergegeven en wordt het kenmerk product niet gebruikt in de zoekopdracht met een instellingswaarde van [!UICONTROL Use in Layered Navigation] .

1. Als u het kenmerk in gelaagde navigatie wilt gebruiken op pagina&#39;s met zoekresultaten, stelt u **[!UICONTROL Use in Search Results Layered Navigation]** in op `Yes` en voert u een getal in het veld **[!UICONTROL Position]** in.

   Het positienummer geeft de relatieve positie van het kenmerk binnen het gelaagde navigatieblok aan.

   >[!NOTE]
   >
   >Het veld _[!UICONTROL Position]_&#x200B;wordt standaard grijs weergegeven en u moet het kenmerk opslaan voordat u deze instelling kunt wijzigen.

1. Stel **[!UICONTROL Use for Promo Rule Conditions]** in op `Yes` als u het kenmerk in prijsregels wilt gebruiken.

1. Als u wilt dat de tekst kan worden opgemaakt met HTML, stelt u **[!UICONTROL Allow HTML Tags on Storefront]** in op `Yes` .

   Met deze instelling wordt de WYSIWYG-editor beschikbaar gesteld wanneer u het veld bewerkt.

1. Stel **[!UICONTROL Visible on Catalog Pages on Storefront]** in op `Yes` om het kenmerk op de productpagina op te nemen.

1. Vul de volgende instellingen in zoals deze worden ondersteund door uw thema:

   - Als u het kenmerk wilt opnemen in productlijsten, stelt u **[!UICONTROL Used in Product Listing]** in op `Yes` .

   - Als u kenmerk wilt gebruiken als een sorteerparameter voor productlijsten, stelt u **[!UICONTROL Used for Sorting in Product Listing]** in op `Yes` .

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.
