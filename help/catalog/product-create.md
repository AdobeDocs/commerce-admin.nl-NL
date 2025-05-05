---
title: Een product maken
description: Meer informatie over de typen producten die u voor uw catalogus kunt maken.
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Een product maken

Het kiezen van een producttype is een van de eerste dingen die u moet doen om een product te maken. Als u nog maar net uw productcatalogus gaat samenstellen, kunt u een aantal voorbeeldproducten maken om met elk producttype te experimenteren. Naast de basistypes van het product, wordt het term _complexe product_ soms gebruikt om naar producten met veelvoudige opties, zoals een configureerbaar product te verwijzen dat in diverse kleuren en grootten beschikbaar is.

>[!NOTE]
>
>Voor een dieper begrip, verwijs naar catalogus [ navigatie ](navigation.md), hoe te opstelling [ categorieën ](categories.md) en [ attributen ](product-attributes.md), en de opties van catalogus [ URL ](catalog-urls.md) die beschikbaar zijn. Nadat u deze concepten begrijpt, moet de meest efficiënte manier om vele producten aan de catalogus toe te voegen [&#128279;](../systems/data-import.md) hen van een Csv- dossier invoeren.

![ pagina van het Product op de storefront ](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Productsoorten

**[Eenvoudig product](product-create-simple.md)** - een eenvoudig product is een fysiek punt met één enkele SKU. Eenvoudige producten hebben verschillende prijzen en invoercontroles waardoor variaties van het product kunnen worden verkocht. De eenvoudige producten kunnen in combinatie met gegroepeerde, bundel, en configureerbare producten worden gebruikt.

**[Configureerbaar product](product-create-configurable.md)** - een configureerbaar product lijkt één enkel product met lijsten van opties voor elke variatie te zijn. Elke optie vertegenwoordigt echter een afzonderlijk, eenvoudig product met een afzonderlijke SKU, waardoor het mogelijk is de inventaris voor elke variatie te volgen.

**[Gegroepeerd product](product-create-grouped.md)** - een gegroepeerd product stelt veelvoudige, standalone producten als groep voor. Je kunt variaties van één product aanbieden of ze groeperen voor een speciale actie. De producten kunnen afzonderlijk of als groep worden aangeschaft.

**[Virtuele producten](product-create-virtual.md)** - een virtueel product is geen tastbaar product, en wordt typisch gebruikt voor producten zoals de diensten, het lidmaatschap, de garanties, en de abonnementen. Virtuele producten kunnen worden gebruikt in combinatie met gegroepeerde en gebundelde producten.

**[product van de Bundel](product-create-bundle.md)** - een bundelproduct laat klanten &quot;hun&quot;van een assortiment opties bouwen. De bundel kan een cadeaumandje, computer of iets anders zijn dat u kunt aanpassen. Elk item in de bundel is een afzonderlijk product.

**[Downloadbaar product](product-create-downloadable.md)** - een digitaal downloadbaar product bestaat uit één of meerdere dossiers die worden gedownload. De bestanden kunnen zich op uw server bevinden of als URL&#39;s naar een andere server worden verzonden.

**[Cadeaukaart](product-gift-card-create.md)** - ([ Adobe Commerce ](../landing/home.md#product-editions) slechts) Er zijn drie soorten geschenkkaarten. _Virtuele_ geschenkkaarten worden verzonden door e-mail. _Fysieke_ geschenkkaarten worden verscheept aan de ontvanger. _Gecombineerde_ giftekaarten die een combinatie virtueel en fysiek zijn. Elke code heeft een unieke code, die wordt afgelost tijdens het afrekenen. Cadeaukaarten kunnen ook in een gegroepeerd product worden opgenomen.

## Productinstellingen

De meest gebruikte productinstellingen en -kenmerken worden boven aan de pagina weergegeven, gevolgd door aangepaste kenmerken. Eventuele andere productinstellingen bevinden zich in uitbreidbare secties onder aan de pagina.

![ Montages van het Product ](./assets/product-settings.png){width="600" zoomable="yes"}

| Instelling | Beschrijving |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (Wanneer [[!DNL Inventory Management]](../inventory-management/introduction.md) is ingeschakeld) Hier worden de bronnen weergegeven waaruit het product kan worden gedistribueerd. |
| [[!UICONTROL Content]](product-content.md) | Wordt gebruikt om de hoofdproductbeschrijving op de productpagina van de winkel in te voeren en te bewerken. |
| [[!UICONTROL Configurations]](product-configurations.md) | Maakt een lijst van om het even welke bestaande variaties van het product en kan worden gebruikt om variaties voor gebruik met het Configurable producttype te produceren. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Hier worden alle beoordelingen weergegeven die klanten voor het product hebben ingediend. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Hiermee geeft u de URL-sleutel en metagegevensvelden op die door zoekprogramma&#39;s worden gebruikt om het product te indexeren. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Gebruikt aan opstellings eenvoudige promotieblokken op de winkel die een selectie van extra producten voorstellen die van belang voor de klant zouden kunnen zijn. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Hiermee voegt u aanpasbare opties toe aan een product. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identificeert elke website waar het product beschikbaar is, volgens de opslaghiërarchie. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Wordt gebruikt om een ander thema op de productpagina toe te passen, de kolomlay-out te wijzigen, te bepalen waar de productopties verschijnen en aangepaste XML-code in te voeren. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Wordt gebruikt om een berichtoptie voor een cadeau tijdens het afrekenen op productniveau in of uit te schakelen. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met [ Adobe Commerce B2B ](../b2b/introduction.md) slechts) laat de capaciteit toe om gedeelde catalogi met douaneprijs voor verschillende bedrijven te handhaven. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Hiermee definieert u de parameters voor het downloaden van producten. |

{style="table-layout:auto"}

## Geavanceerde prijzen en inventarisatie

Klik op de onderstaande koppeling **[!UICONTROL Price]** en **[!UICONTROL Quantity]** om toegang te krijgen tot de geavanceerde prijs- en voorraadinstellingen. Voor meer informatie, zie [ het Leiden het Prijsen ](pricing-advanced.md) en [ Inventory management ](../inventory-management/introduction.md).
