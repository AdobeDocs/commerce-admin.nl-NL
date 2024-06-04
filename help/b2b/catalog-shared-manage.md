---
title: Uw gedeelde catalogi beheren
description: Meer informatie en gereedschappen vindt u op de pagina Gedeelde catalogi.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Uw gedeelde catalogi beheren

De _[!UICONTROL Shared Catalogs]_biedt toegang tot de gereedschappen die nodig zijn voor het beheer van uw gedeelde catalogi. De pagina is vergelijkbaar met de standaardwerkruimte voor beheerders, met filters en besturingselementen voor handelingen. In het raster worden alle gedeelde catalogi weergegeven, inclusief de standaard openbare gedeelde catalogus en alle aangepaste catalogi die u hebt ingesteld.

## De productselectie bijwerken

De selectie van producten in een gedeelde catalogus kan eenvoudig worden bijgewerkt vanuit de _[!UICONTROL Action]_kolom van het gedeelde catalogusraster. De wijzigingen die u aanbrengt, zijn zichtbaar voor leden van gekoppelde bedrijfsaccounts. Het proces is in wezen hetzelfde als het kiezen van producten voor een nieuwe [catalogusstructuur](catalog-shared-pricing-structure.md), behalve dat het bereik van de configuratie niet kan worden gewijzigd.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus in het raster naar **[!UICONTROL Action]** kolom en selecteer **[!UICONTROL Set Pricing and Structure]**.

   ![Raster en actiemenu van gedeelde catalogus](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Volg de instructies in [Stap 2: Producten kiezen](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   U kunt het eerste item overslaan, omdat het bereik van een gedeelde catalogus niet kan worden gewijzigd nadat het voor de eerste keer is opgeslagen.

Als u met een bepaald product werkt, _[!UICONTROL Products In Shared Catalog]_een lijst van elke gedeelde catalogus waar het product beschikbaar is. Zie voor meer informatie [Producten toevoegen aan een gedeelde catalogus](catalog-shared-product-add.md).

![Product in gedeelde catalogi](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Aangepaste prijzen bijwerken

De aangepaste prijzen van producten in een gedeelde catalogus kunnen eenvoudig worden bijgewerkt in de kolom Actie van het raster Gedeelde catalogi. De veranderingen u aanbrengt zijn zichtbaar aan in de winkel aan leden van het bijbehorende bedrijf of de klantengroep. Het proces is in wezen hetzelfde als het instellen van aangepaste prijzen voor een nieuwe [gedeelde catalogus](catalog-shared-pricing-structure.md), behalve dat het bereik van de configuratie niet kan worden gewijzigd.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus in het raster die u wilt bijwerken naar de **[!UICONTROL Action]** kolom en selecteer **[!UICONTROL Set Pricing and Structure]**.

1. Op de _[!UICONTROL Catalog Structure]_pagina, klikt u **[!UICONTROL Configure]**en voer een van de volgende handelingen uit:

   - Klik in de voortgangsindicator boven aan de pagina op **[!UICONTROL Pricing]**.
   - Klik in de rechterbovenhoek op **[!UICONTROL Next]**.

1. Volg de instructies in [Stap 3: Aangepaste prijzen instellen](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Categoriemachtigingen bijwerken

[Categoriemachtigingen](../catalog/category-permissions.md) worden automatisch ingesteld op `Allow` voor producten die vanuit de categoriestructuur worden toegevoegd aan een gedeelde catalogus. U kunt de toestemmingen later aanpassen, of extra regels tot stand brengen, zoals nodig.

>[!NOTE]
>
>**[B2B-release 1.3.0](release-notes.md#b2b-v130) en hoger** — Wanneer u een gedeelde catalogus maakt, moet u elk [categorietoestemming](../catalog/category-permissions.md) voor de catalogus is ingesteld op `Allow` voor de _[!UICONTROL Display Product Prices]_en_[!UICONTROL Add to Cart]_ voor klantengroepen die deze toegang in de montages van de catalogustoestemming worden toegewezen. Eerder werden deze instellingen automatisch ingesteld op `Deny` zelfs wanneer catalogusmachtigingen zijn ingesteld op `Allow`.

>[!IMPORTANT]
>
>Alle bestaande [machtigingen voor groep instellen](../configuration-reference/catalog/catalog.md#category-permissions) worden genegeerd door **_alles_** categorieën in de catalogus als de **_[!UICONTROL Shared Catalog]_** -functie is ingeschakeld. [!UICONTROL Shared Catalog] beheert volledig alle categorierechten in de catalogus wanneer deze is ingeschakeld.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de categorie met producten die u wilt bijwerken.

   Als u alle producten wilt opnemen, selecteert u de bovenste categorie in de structuur.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Category Permissions]** sectie.

1. Klikken **[!UICONTROL New Permission]** en voer de volgende handelingen uit:

   ![Nieuwe machtiging](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Kies de optie **[!UICONTROL Customer Group]** die overeenkomt met de gedeelde catalogus en wijzigt u zo nodig de machtigingsinstellingen.

     ![Regel voor machtigingen voor categorieën](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Om een toestemmingsregel voor een andere klantengroep tot stand te brengen, klik **[!UICONTROL New Permissions]** en herhaal het proces.

   - Als u een machtigingsregel wilt verwijderen, klikt u op de knop _Verwijderen_ ![Prullenbak](../assets/icon-delete-trashcan-solid.png) pictogram.

1. Klik op **[!UICONTROL Save]**.

## De catalogusdetails bijwerken

De gedetailleerde informatie van om het even welke gedeelde catalogus kan gemakkelijk van de kolom van de Actie van het Gedeelde net van Catalogi worden bijgewerkt. De veranderingen u aanbrengt worden weerspiegeld in om het even welke bijbehorende bedrijfsrekeningen.

![Algemene instellingen](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus die u wilt bijwerken naar de **[!UICONTROL Action]** kolom en selecteer **[!UICONTROL General Settings]**.

   ![Catalogusdetails](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Werk indien nodig de gedetailleerde informatie over de catalogus bij.

   - Als u de naam van een gedeelde catalogus wijzigt, verandert ook de naam van de bijbehorende klantengroep.
   - Het catalogustype wijzigen vanuit `Custom` tot `Public` Zet de bestaande openbare catalogus in een douanecatalogus om. Alle bedrijven die banden hebben met de oorspronkelijke openbare catalogus, worden opnieuw toegewezen aan de vervangende catalogus. Een openbare catalogus kan niet worden omgezet in een aangepaste catalogus.

1. Klik op **[!UICONTROL Save]**.

## Verwijzing naar gedeelde cataloguspagina

### Knopbalk

| Knop | Beschrijving |
|--- |--- |
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Gedeelde catalogi zonder de nieuwe gedeelde catalogus op te slaan. |
| [!UICONTROL Delete] | Hiermee verwijdert u de catalogus en wijst u eventuele gekoppelde bedrijven en hun leden toe aan de gedeelde openbare catalogus. |
| [!UICONTROL Reset] | Hiermee wist u de vorm van niet-opgeslagen wijzigingen en herstelt u de oorspronkelijke details van de catalogus. |
| [!UICONTROL Duplicate] | Maakt een [kopie van catalogus](catalog-shared-create.md). Voor een aangepaste catalogus, het prijsmodel en de structuur van het origineel, maar zonder de ondernemersverenigingen. Als een openbare gedeelde catalogus wordt gedupliceerd, verandert het type van de gedupliceerde catalogus in `custom`. Er wordt ook een overeenkomende klantengroep gemaakt met dezelfde naam als de gedupliceerde catalogus. Standaard krijgt een gedupliceerde catalogus de naam _Dupliceren van_ de oorspronkelijke catalogus. |
| [!UICONTROL Save and Continue Edit] | Hiermee slaat u alle wijzigingen op en het formulier blijft geopend in de bewerkingsmodus. |
| [!UICONTROL Save] | Hiermee slaat u wijzigingen op, sluit u het formulier en keert u terug naar de pagina Gedeelde catalogi. |

{style="table-layout:auto"}

### Catalogusdetails

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Name] | Identificeert de gedeelde catalogus door Admin, en in de klantenrekeningen waar het beschikbaar is. De catalogusnaam moet beschrijvend zijn en mag niet langer zijn dan 32 tekens. U kunt geen twee gedeelde catalogi met dezelfde naam hebben. Maximum aantal tekens: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identificeert een catalogus met aangepaste prijzen die alleen beschikbaar is voor de specifieke ondernemingen waaraan deze is toegewezen.<br/>**[!UICONTROL Public]**- Identificeert de gedeelde catalogus die beschikbaar is voor alle gastbezoekers en voor aangemelde klanten die niet aan een bedrijf zijn gekoppeld. Een &quot;standaard&quot;openbare gedeelde catalogus wordt gecreeerd wanneer Adobe Commerce B2B wordt geïnstalleerd, maar moet door de beheerder worden gevormd. Er kan slechts één openbare gedeelde catalogus tegelijk bestaan. |
| [!UICONTROL Customer Tax Class] | Bepaalt de belastingklasse die wordt gebruikt voor aankopen uit de catalogus. De opties omvatten alle beschikbare belastingklassen. |
| [!UICONTROL Description] | Een korte uitleg van de manier waarop de catalogus moet worden gebruikt. |

{style="table-layout:auto"}
