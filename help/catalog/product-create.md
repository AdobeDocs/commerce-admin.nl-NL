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

Het kiezen van een producttype is een van de eerste dingen die u moet doen om een product te maken. Als u nog maar net uw productcatalogus gaat samenstellen, kunt u een aantal voorbeeldproducten maken om met elk producttype te experimenteren. Naast de basisproductsoorten wordt de term _complex product_ wordt soms gebruikt om naar producten met veelvoudige opties, zoals een configureerbaar product te verwijzen dat in diverse kleuren en grootten beschikbaar is.

>[!NOTE]
>
>Raadpleeg de catalogus voor meer informatie [navigatie](navigation.md), hoe te opstelling [categorieën](categories.md) en [attributes](product-attributes.md)en de catalogus [URL-opties](catalog-urls.md) die beschikbaar zijn. Nadat u deze concepten begrijpt, is de meest efficiënte manier om veel producten aan de catalogus toe te voegen: [import](../systems/data-import.md) uit een CSV-bestand.

![Productpagina op de winkel](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Productsoorten

**[Eenvoudig product](product-create-simple.md)** - Een eenvoudig product is een fysiek artikel met één SKU. Eenvoudige producten hebben verschillende prijzen en invoercontroles waardoor variaties van het product kunnen worden verkocht. De eenvoudige producten kunnen in combinatie met gegroepeerde, bundel, en configureerbare producten worden gebruikt.

**[Configureerbaar product](product-create-configurable.md)** - Een configureerbaar product lijkt één product met lijsten van opties voor elke variatie te zijn. Elke optie vertegenwoordigt echter een afzonderlijk, eenvoudig product met een afzonderlijke SKU, waardoor het mogelijk is de inventaris voor elke variatie te volgen.

**[Gegroepeerd product](product-create-grouped.md)** - Een gegroepeerd product presenteert meerdere zelfstandige producten als een groep. Je kunt variaties van één product aanbieden of ze groeperen voor een speciale actie. De producten kunnen afzonderlijk of als groep worden aangeschaft.

**[Virtuele producten](product-create-virtual.md)** - Een virtueel product is geen tastbaar product en wordt gewoonlijk gebruikt voor producten zoals services, lidmaatschap, garanties en abonnementen. Virtuele producten kunnen worden gebruikt in combinatie met gegroepeerde en gebundelde producten.

**[Bundel](product-create-bundle.md)**  - Met een bundelproduct kunnen klanten hun eigen product maken op basis van een assortiment opties. De bundel kan een cadeaumandje, computer of iets anders zijn dat u kunt aanpassen. Elk item in de bundel is een afzonderlijk product.

**[Downloadbaar product](product-create-downloadable.md)** - Een digitaal downloadbaar product bestaat uit een of meer bestanden die worden gedownload. De bestanden kunnen zich op uw server bevinden of als URL&#39;s naar een andere server worden verzonden.

**[Cadeaukaart](product-gift-card-create.md)** - ([Adobe Commerce](../landing/home.md#product-editions) Alleen) Er zijn drie soorten cadeaukaarten. _Virtueel_ cadeaukaarten worden per e-mail verzonden. _Fysiek_ cadeaukaarten worden naar de ontvanger verzonden . _Gecombineerd_ cadeaukaarten die een combinatie van virtueel en fysiek zijn. Elke code heeft een unieke code, die wordt afgelost tijdens het afrekenen. Cadeaukaarten kunnen ook in een gegroepeerd product worden opgenomen.

## Productinstellingen

De meest gebruikte productinstellingen en -kenmerken worden boven aan de pagina weergegeven, gevolgd door aangepaste kenmerken. Eventuele andere productinstellingen bevinden zich in uitbreidbare secties onder aan de pagina.

![Productinstellingen](./assets/product-settings.png){width="600" zoomable="yes"}

| Instelling | Beschrijving |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (Wanneer [[!DNL Inventory Management]](../inventory-management/introduction.md) (wordt toegelaten) maakt een lijst van de bronnen waarvan het product kan worden verdeeld. |
| [[!UICONTROL Content]](product-content.md) | Wordt gebruikt om de hoofdproductbeschrijving op de productpagina van de winkel in te voeren en te bewerken. |
| [[!UICONTROL Configurations]](product-configurations.md) | Maakt een lijst van om het even welke bestaande variaties van het product en kan worden gebruikt om variaties voor gebruik met het Configurable producttype te produceren. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Hier worden alle beoordelingen weergegeven die klanten voor het product hebben ingediend. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Hiermee geeft u de URL-sleutel en metagegevensvelden op die door zoekprogramma&#39;s worden gebruikt om het product te indexeren. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Gebruikt aan opstellings eenvoudige promotieblokken op de winkel die een selectie van extra producten voorstellen die van belang voor de klant zouden kunnen zijn. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Hiermee voegt u aanpasbare opties toe aan een product. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identificeert elke website waar het product beschikbaar is, volgens de opslaghiërarchie. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Wordt gebruikt om een ander thema op de productpagina toe te passen, de kolomlay-out te wijzigen, te bepalen waar de productopties verschijnen en aangepaste XML-code in te voeren. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Wordt gebruikt om een berichtoptie voor een cadeau tijdens het afrekenen op productniveau in of uit te schakelen. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (Beschikbaar met [Adobe Commerce B2B](../b2b/introduction.md) alleen) Hiermee kunt u gedeelde catalogi onderhouden met aangepaste prijzen voor verschillende bedrijven. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Hiermee definieert u de parameters voor het downloaden van producten. |

{style="table-layout:auto"}

## Geavanceerde prijzen en inventarisatie

Klik op de onderstaande koppeling voor toegang tot de geavanceerde prijs- en voorraadinstellingen **[!UICONTROL Price]** en **[!UICONTROL Quantity]**. Zie voor meer informatie [Prijsbeheer](pricing-advanced.md) en [Inventory management](../inventory-management/introduction.md).
