---
title: Categorieën maken
description: U kunt zo veel extra subcategorieën tot stand brengen zoals nodig, volgens de maximummenudiepte die in de configuratie wordt geplaatst.
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%

---

# Categorieën maken

De categoriestructuur van de catalogus is vergelijkbaar met een ondersteboven liggende structuur, met bovenaan het basiselement. Elke sectie van de boomstructuur kan worden uitgevouwen en samengevouwen. Alle uitgeschakelde of verborgen categorieën worden grijs weergegeven. De categorieën op het eerste niveau (onder de [basis](category-root.md)) worden doorgaans weergegeven als opties in het dialoogvenster [hoofdmenu](navigation-top.md). U kunt zo veel extra subcategorieën tot stand brengen zoals nodig, volgens de maximummenudiepte die in de configuratie wordt geplaatst. Categorieën kunnen naar andere locaties in de boomstructuur worden gesleept en neergezet. Het categorie-id-nummer staat tussen haakjes achter de categorienaam boven aan de pagina.

Voor een website met meerdere [winkelen](../stores-purchase/stores.md#add-stores), kunt u voor elke winkel een andere hoofdcategorie maken die de set categorieën definieert die voor de [topnavigatie](navigation-top.md).

![Categoriestructuur](./assets/category-selected.png){width="700" zoomable="yes"}

## Aanbevolen procedures

Gebruik deze beste werkwijzen wanneer u categorieën plant en creeert.

### Categoriestructuur

De structuur van de categorieën in het hoofdmenu kan van invloed zijn op de gebruikerservaring en -prestaties. Als beste praktijken, zou u één over-arching top-level categorie moeten identificeren, en vermijden hebbend andere categorieën met de zelfde naam. In plaats van meerdere categorieën voor &quot;Kinderen&quot; te hebben, bijvoorbeeld georganiseerd onder verschillende afdelingen, zoals `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. Het kan efficiënter zijn om van de oudercategorie op hoofdniveau te maken `Kids`en maak vervolgens subcategorieën naar wens hieronder. Zorg voor consistentie met de categoriestructuur en gebruik dezelfde aanpak voor alle producttypen in uw catalogus.

### Bedrijfsregels en automatisering

Houd rekening met de categoriestructuur en beschikbare kenmerkwaarden wanneer u bedrijfslogica gebruikt om vergelijkbare items op een cataloguspagina weer te geven of om een gepersonaliseerde promotie, geautomatiseerd proces of zoekcriteria in te stellen. Als u bijvoorbeeld &quot;polo&quot; opgeeft als een bovenliggende categorie, kunnen de resultaten betrekking hebben op producten die niet geschikt zijn voor mannen en vrouwen en die niet ouder zijn. Als u echter een specifieke subcategorie van polo-overhemden aanpast, zijn de resultaten beperkter en kunnen ze waarschijnlijk een beroep doen op een bepaalde klant. De resultaten kunnen zelfs specifieker zijn wanneer gecombineerd met andere attributenwaarden die een specifieke klant richten. Houd rekening met het aantal producten dat moet worden doorgefilterd en opgehaald wanneer u naar een bepaald categoriepad verwijst. Het verschil in resultaten kan dramatisch zijn. Bekijk de verschillende resultaten die door de volgende categoriepaden worden geretourneerd:

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

Het is van belang om categoriale relaties duidelijk te definiëren, zoals:

- bovenliggende categorie
- subcategorie
- categoriepad

Definieer ook de bijbehorende trefwoorden en kenmerken, zoals:

- beschikbaarheid
- verkoopprijs
- merk
- size
- kleur

## Stap 1: Een categorie maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Set **[!UICONTROL Store View]** om te bepalen waar de nieuwe categorie beschikbaar moet zijn.

1. Selecteer in de categoriestructuur de bovenliggende categorie van de nieuwe categorie.

   Het bovenliggende element bevindt zich op één niveau boven de nieuwe categorie.

   Als u zonder gegevens vanaf het begin begint, zijn er mogelijk slechts twee categorieën in de lijst: _Standaardcategorie_, dat de basis vormt, en _Voorbeeldcategorie_

1. Klik op **[!UICONTROL Add Subcategory]**.

## Stap 2: De basisgegevens invullen

1. Als je wilt dat de rubriek direct beschikbaar is in de winkel, stel je **[!UICONTROL Enable Category]** tot `Yes`.

1. De categorie opnemen in het dialoogvenster [topnavigatie](navigation-top.md), set **[!UICONTROL Include in Menu]** tot `Yes`.

1. Voer de **[!UICONTROL Category Name]**.

   ![Basisinformatie over rubrieken](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. klikken **[!UICONTROL Save]** en doorgaan.

## Stap 3: De inhoud van de categorie voltooien

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie.

   ![Categorie-inhoud](./assets/category-content.png){width="600" zoomable="yes"}

1. Als u een **[!UICONTROL Category Image]** boven aan de pagina kunt u uw eigen afbeelding uploaden of een afbeelding gebruiken die in het dialoogvenster [Media-opslag](../content-design/media-storage.md).

   - Als u uw eigen afbeelding wilt uploaden, klikt u op **[!UICONTROL Upload]** en kiest u de afbeelding die u wilt weergeven in de categorie.

   - Als u afbeeldingen van Media Storage wilt gebruiken, klikt u op **[!UICONTROL Select from Gallery]** en selecteer de afbeelding die u wilt weergeven in de categorie.

   >[!NOTE]
   >
   >In de Medialerie kunt u ook de opdracht [Adobe Stock-integratie](../content-design/adobe-stock.md) om een geschikte afbeelding te zoeken door op **[!UICONTROL Search Adobe Stock]**.

1. Voor **[!UICONTROL Description]** voert u de tekst of andere inhoud in die u op de bestemmingspagina van de categorie wilt weergeven.

   Zie voor meer informatie [Categorie-inhoud](categories-content-settings.md).

1. Als u een inhoudsblok wilt opnemen op de bestemmingspagina van de categorie, kiest u de optie **[!UICONTROL CMS Block]** die u wilt weergeven.

1. klikken **[!UICONTROL Save]** en doorgaan.

## Stap 4: De weergave-instellingen voltooien

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Display Setting]** sectie.

   ![Weergave-instellingen](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Zie voor meer informatie over deze opties voor meer informatie over deze opties  [Weergave-instellingen](categories-display-settings.md).

1. Set **[!UICONTROL Display Mode]** op een van de volgende wijzen:

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Als u wilt dat de categoriepagina de _`Filter by Attribute`_sectie met gelaagde navigatie, set **[!UICONTROL Anchor]**tot `Yes`.

1. Voor de **[!UICONTROL Available Product Listing Sort By]** selecteert u een of meer van de beschikbare waarden die beschikbaar zijn voor klanten om de lijst te sorteren. Deze instelling is niet van toepassing op [!DNL Live Search] [Widget pagina met productaanbiedingen](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   Standaard worden alle beschikbare waarden opgenomen. Hef de selectie van **[!UICONTROL Use All]** Schakel het selectievakje in om de selecties te wijzigen. De waarden kunnen bijvoorbeeld het volgende zijn:

   - `Position`
   - `Product Name`
   - `Price`

1. Als u de standaardsorteervolgorde voor de categorie wilt instellen, kiest u **[!UICONTROL Default Product Listing Sort By]** waarde. Deze instelling is niet van toepassing op [!DNL Live Search] [Widget pagina met productaanbiedingen](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. De standaardnavigatie in lagen wijzigen [prijsstap](navigation-layered.md#configure-price-navigation) Ga als volgt te werk om deze instelling in te stellen:

   - Hef de selectie van **[!UICONTROL Use Config Settings]** selectievakje.

   - Voer de waarde in die u als een incrementele prijsstap voor gelaagde navigatie wilt gebruiken.

1. Klikken **[!UICONTROL Save]** en doorgaan.

## Stap 5: De optimalisatie-instellingen voor zoekprogramma&#39;s voltooien

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization Settings]** sectie.

   ![Zoekmachine optimaliseren](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Zie voor meer informatie over deze opties [Zoekmachine optimaliseren](categories-search-engine-optimization.md).

1. Voer de volgende handelingen uit [metagegevens](../merchandising-promotions/meta-data.md) voor de categorie:

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Klikken **[!UICONTROL Save]** en doorgaan.

## Stap 6: kies de producten in categorie

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Products in Category]** sectie.

   ![Producten in categorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Zie voor meer informatie over deze opties [Producten in categorie](categories-product-assignments.md).

1. Gebruik indien nodig de [filters](../getting-started/admin-grid-controls.md) om de producten te vinden.

   Als u alle records wilt weergeven die nog niet in de categorie zijn opgenomen, stelt u de recordkiezer in de eerste kolom in op `No` en klik op **[!UICONTROL Search]**.

1. Selecteer in de eerste kolom het selectievakje voor elk product dat u in de categorie wilt opnemen.

1. Klikken **[!UICONTROL Save]** en doorgaan.

## Stap 7: De categorierechten instellen

{{ee-feature}}

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Category Permissions]** sectie.

1. Kies voor een installatie op meerdere locaties de optie **[!UICONTROL Website]** waar de categorierechten van toepassing zijn.

1. Kies de optie **[!UICONTROL Customer Group]** waar de categorierechten van toepassing zijn.

   ![Adobe Commerce B2B](../assets/b2b.svg) ([Adobe Commerce B2B](../b2b/introduction.md) (Alleen) Kies een **[!UICONTROL Shared Catalog]** in plaats daarvan.

1. Stel de volgende machtigingen naar wens in:

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Als u nog een machtigingsregel wilt toevoegen, klikt u op **[!UICONTROL New Permission]** en herhaal het proces.

   ![Categoriemachtigingen](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Stap 8: Voltooi de ontwerpinstellingen

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Design]** sectie.

1. Stel de ontwerpinstellingen naar wens in:

   - ([Adobe Commerce B2B](../b2b/introduction.md) alleen) Als u de ontwerpinstellingen van de bovenliggende categorie wilt toepassen op deze categorie, stelt u **[!UICONTROL Use Parent Category Settings]** tot `Yes`.

   - Als u het ontwerp van de categoriepagina&#39;s wilt wijzigen, kiest u de optie **[!UICONTROL Theme]** die u wilt toepassen.

   - Als u de kolomindeling van de categoriepagina&#39;s wilt wijzigen, kiest u de optie **[!UICONTROL Layout]** die u wilt toepassen.

   - Als u aangepaste code wilt invoeren, voert u in het dialoogvenster **[!UICONTROL Layout Update XML]** doos.

   - Als u hetzelfde ontwerp wilt gebruiken voor productpagina&#39;s, stelt u **[!UICONTROL Apply Design to Products]** tot `Yes`.

   ![Ontwerpinstellingen](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Ga als volgt te werk om de ontwerpupdate voor een bepaalde periode te plannen:

   - Vouw de sectie _[!UICONTROL Schedule Design Update]_uit.

   - De kalender gebruiken (![Kalenderpictogram](../assets/icon-calendar.png)) om de Update van het Programma te kiezen **[!UICONTROL from]** en **[!UICONTROL to]** datums.

   ![Geplande ontwerpupdate](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.
