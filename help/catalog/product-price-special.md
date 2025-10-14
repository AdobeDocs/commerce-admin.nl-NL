---
title: Speciale prijzen
description: Leer hoe u speciale prijzen aanbiedt voor een bepaalde periode.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Speciale prijzen

Voor een bepaalde periode kan een speciale prijs worden aangeboden. Gedurende de opgegeven periode verschijnt de speciale prijs in plaats van de reguliere prijs, gevolgd door een notatie die de reguliere prijs weergeeft.

![&#x200B; Speciale prijs op een productpagina &#x200B;](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Speciale prijs toepassen op een afzonderlijk product

U kunt eenvoudig een speciale prijs instellen voor één product in de catalogus.

### Een geplande update gebruiken

{{ee-feature}}

Adobe Commerce omvat steun voor [&#x200B; geplande updates &#x200B;](../content-design/content-staging-scheduled-update.md). Gebruik deze promotietools om een speciale prijs toe te passen op een specifiek product gedurende een bepaalde periode.

1. Open het product in de bewerkingsmodus.

1. Klik op **[!UICONTROL Scheduled Update]**.

   ![&#x200B; voeg geplande update voor product &#x200B;](./assets/product-schedule-new-update.png){width="600" zoomable="yes"} toe

1. Voor **Naam van de Update**, ga een naam voor de speciale prijsbevordering in.

1. Voer een korte beschrijving in **[!UICONTROL Description]** .

1. Gebruik het _pictogram van de Kalender_ ( ![&#x200B; kalenderpictogram &#x200B;](../assets/icon-calendar.png)) om **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor de speciale prijsbevordering te kiezen.

   U kunt ook de schuifregelaars **[!UICONTROL Hour]** en **[!UICONTROL Minute]** gebruiken om de begin- en eindtijd te kiezen. Klik op **[!UICONTROL Close]** wanneer het begin en het einde zijn ingesteld.

   ![&#x200B; sparen als Nieuwe Update &#x200B;](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. De rol neer aan het _Prijs_ gebied, klikt **[!UICONTROL Advanced Pricing]**, en gaat de hoeveelheid **[!UICONTROL Special Price]** in die volgens de geplande update moet worden toegepast.

   ![&#x200B; Speciale het Tarief Montages &#x200B;](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Klik na voltooiing op **[!UICONTROL Done]** en vervolgens op **[!DNL Save]** .

   In de winkel moet de speciale prijs zowel in de cataloguslijst als op de productpagina worden vermeld.

   De _[!UICONTROL Scheduled Change]_&#x200B;wordt boven aan de pagina weergegeven.

   ![&#x200B; Geplande Verandering &#x200B;](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Een eenvoudige begin- en einddatum gebruiken

{{ce-feature}}

Magento Open Source bevat eenvoudige begin- en einddatumopties in de geavanceerde prijsopties.

1. Open het product in de bewerkingsmodus.

1. Schuif omlaag naar het veld _[!UICONTROL Price]_, klik op **[!UICONTROL Advanced Pricing]**&#x200B;en voer de hoeveelheid **[!UICONTROL Special Price]**&#x200B;in.

1. Gebruik het _pictogram van de Kalender_ ( ![&#x200B; pictogram van de Kalender &#x200B;](../assets/icon-calendar.png)) om **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor de speciale prijsbevordering te kiezen.

   De speciale prijs gaat in onmiddellijk na middernacht aan het begin van de begindatum (00:01) en loopt door tot net vóór middernacht (23:59) op de dag vóór de einddatum.

   ![&#x200B; Geplande Verandering &#x200B;](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Klik na voltooiing op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** .

   In de winkel moet de speciale prijs zowel in de cataloguslijst als op de productpagina worden vermeld.

## Een speciale prijs toepassen op meerdere producten

U kunt een speciale prijs aan veelvoudige producten, zoals veelvoudige variaties van a [&#x200B; ook toewijzen configureerbaar product &#x200B;](product-create-configurable.md).

### Een speciale prijs instellen voor geselecteerde producten

{{ee-feature}}

In het volgende voorbeeld ziet u hoe u dezelfde speciale prijs kunt toewijzen aan meerdere productvariaties van een configureerbaar product in Adobe Commerce.

1. Klik op de pagina _[!UICONTROL Products]_&#x200B;op **[!UICONTROL Filters]**&#x200B;en voer de **[!UICONTROL Name]**&#x200B;van het configureerbare product in.

1. Stel **[!UICONTROL Type]** in op `Configurable Product` en klik op **[!UICONTROL Apply Filters]** .

1. Als u dezelfde speciale prijs aan alle producten wilt toewijzen, stelt u het besturingselement in de koptekst van de eerste kolom in op `Select All` .

   U kunt ook het selectievakje inschakelen voor elk product dat u wilt opnemen.

1. Stel het besturingselement **[!UICONTROL Actions]** in op `Update attributes` .

1. Schuif omlaag naar het veld _[!UICONTROL Special Price]_&#x200B;en schakel het selectievakje **[!UICONTROL Change]**&#x200B;onder het veld&#x200B;_[!UICONTROL Special Price]_ in. Voer vervolgens de speciale prijs in die u wilt aanbieden.

   ![&#x200B; de Speciale gebieden van de Prijs &#x200B;](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

De speciale prijs die beschikbaar is in de winkel, wordt weergegeven in catalogusaanbiedingen en op de productpagina. Voor een configureerbaar product wordt de normale prijs ook op de productpagina weergegeven wanneer de opties worden gekozen.

### Een speciale prijs en een bepaald datumbereik instellen voor bepaalde producten

{{ce-feature}}

Het volgende voorbeeld toont hoe te om de zelfde speciale prijs aan veelvoudige productvariaties van een configureerbaar product in Magento Open Source toe te wijzen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Klik op **[!UICONTROL Filters]**.

1. Voer de **[!UICONTROL Name]** van het configureerbare product in.

1. Stel **[!UICONTROL Type]** in op `Simple Product` .

   ![&#x200B; Filters &#x200B;](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Apply Filters]**.

   Het net maakt een lijst van alle eenvoudige producten die als variaties van het configureerbare product worden geassocieerd.

1. Als u dezelfde speciale prijs aan alle producten wilt toewijzen, stelt u het besturingselement in de koptekst van de eerste kolom in op `Select All` .

   U kunt ook het selectievakje inschakelen voor elk product dat u wilt opnemen.

1. Stel het besturingselement **[!UICONTROL Actions]** in op `Update attributes` .

   ![&#x200B; de Attributen van de Update &#x200B;](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Schuif omlaag naar het veld _[!UICONTROL Special Price]** en voer de volgende handelingen uit:

   - Schakel het selectievakje **[!UICONTROL Change]** onder het veld _[!UICONTROL Special Price]** in en voer de speciale prijs in die u wilt aanbieden.

   - Selecteer **[!UICONTROL Change]** checkbox onder het _Speciale Prijs van Datum_ gebied, klik _Kalender_ ( ![&#x200B; pictogram van de Kalender &#x200B;](../assets/icon-calendar.png)), en kies de eerste datum van de speciale prijsbevordering.

     De speciale prijs gaat in onmiddellijk na middernacht aan het begin van de begindatum (00:01) en loopt door tot net vóór middernacht (23:59) op de dag vóór de einddatum.

   - Selecteer **[!UICONTROL Change]** checkbox onder het _Speciale Prijs aan Datum_ gebied, klik _Kalender_ ( ![&#x200B; pictogram van de Kalender &#x200B;](../assets/icon-calendar.png)), en kies de laatste datum van de speciale prijsbevordering.

   ![&#x200B; Speciale Prijsgebieden &#x200B;](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   Een bericht geeft aan hoeveel records met de speciale prijs zijn bijgewerkt.

   De speciale prijs wordt beschikbaar in de winkel op de opgegeven datum en wordt weergegeven in catalogusaanbiedingen en op de productpagina. Voor een configureerbaar product wordt de normale prijs ook op de productpagina weergegeven wanneer de opties worden gekozen.

   ![&#x200B; Speciale Prijs voor Configureerbaar Product &#x200B;](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Testen

Als de speciale prijs niet correct in de winkel op zowel de cataloguslijst als productpagina&#39;s verschijnt, ontruim uw browser geheim voorgeheugen:

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Klik op **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>De **_definitieve_** productprijs wordt berekend als **_minimum_** relevante prijs, gebruikend de volgende formule: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>_&#x200B;**product Aanpasbare Opties van de Prijs van de Vaste Prijs**&#x200B;_ &lbrace;worden _niet_ beïnvloed door de Prijs van de Groep, de Prijs van de Rij, de Speciale Prijs, of de regels van de Prijs van de Catalogus.
