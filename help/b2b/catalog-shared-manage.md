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

De pagina _[!UICONTROL Shared Catalogs]_biedt toegang tot de gereedschappen die nodig zijn voor het beheer van uw gedeelde catalogi. De pagina is vergelijkbaar met de standaardwerkruimte voor beheerders, met filters en besturingselementen voor handelingen. In het raster worden alle gedeelde catalogi weergegeven, inclusief de standaard openbare gedeelde catalogus en alle aangepaste catalogi die u hebt ingesteld.

## De productselectie bijwerken

De selectie van producten in een gedeelde catalogus kan eenvoudig worden bijgewerkt vanuit de kolom _[!UICONTROL Action]_in het raster voor gedeelde catalogi. De wijzigingen die u aanbrengt, zijn zichtbaar voor leden van gekoppelde bedrijfsaccounts. Het proces is hoofdzakelijk het zelfde als het kiezen van producten voor een nieuwe [ catalogusstructuur ](catalog-shared-pricing-structure.md), behalve dat kan het werkingsgebied van de configuratie niet worden veranderd.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus in het raster naar de kolom **[!UICONTROL Action]** en selecteer **[!UICONTROL Set Pricing and Structure]** .

   ![ Gedeeld catalogusnet en actiemenu ](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Volg de instructies in [ Stap 2: Kies producten ](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   U kunt het eerste item overslaan, omdat het bereik van een gedeelde catalogus niet kan worden gewijzigd nadat het voor de eerste keer is opgeslagen.

Als u met een specifiek product werkt, wordt in de sectie _[!UICONTROL Products In Shared Catalog]_elke gedeelde catalogus weergegeven waarin het product beschikbaar is. Meer leren, zie [ producten aan een gedeelde catalogus ](catalog-shared-product-add.md) toevoegen.

![ Product in Gedeelde Catalogi ](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Aangepaste prijzen bijwerken

De aangepaste prijzen van producten in een gedeelde catalogus kunnen eenvoudig worden bijgewerkt in de kolom Actie van het raster Gedeelde catalogi. De veranderingen u aanbrengt zijn zichtbaar aan in de winkel aan leden van het bijbehorende bedrijf of de klantengroep. Het proces is hoofdzakelijk het zelfde als het plaatsen van douanetarifering voor een nieuwe [ gedeelde catalogus ](catalog-shared-pricing-structure.md), behalve dat kan het werkingsgebied van de configuratie niet worden veranderd.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus in het raster die u wilt bijwerken naar de kolom **[!UICONTROL Action]** en selecteer **[!UICONTROL Set Pricing and Structure]** .

1. Klik op de pagina _[!UICONTROL Catalog Structure]_op **[!UICONTROL Configure]**en voer een van de volgende handelingen uit:

   - Klik op **[!UICONTROL Pricing]** in de voortgangsindicator boven aan de pagina.
   - Klik in de rechterbovenhoek op **[!UICONTROL Next]** .

1. Volg de instructies in [ Stap 3: Plaats douaneprijzen ](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Categoriemachtigingen bijwerken

{de toestemmingen van de Categorie 0} ](../catalog/category-permissions.md) worden automatisch geplaatst aan `Allow` voor producten die van de categorieboom aan een gedeelde catalogus worden toegevoegd. [ U kunt de toestemmingen later aanpassen, of extra regels tot stand brengen, zoals nodig.

>[!NOTE]
>
>**[B2B versie 1.3.0 ](release-notes.md#b2b-v130) en later** - wanneer u een gedeelde catalogus creeert, wordt elk [ categorietoestemming ](../catalog/category-permissions.md) voor de catalogus geplaatst aan `Allow` voor _[!UICONTROL Display Product Prices]_en_[!UICONTROL Add to Cart]_ voor klantengroepen die deze toegang in de montages van de catalogustoestemming worden toegewezen. Eerder werden deze instellingen automatisch ingesteld op `Deny` , zelfs als catalogusmachtigingen waren ingesteld op `Allow` .

>[!IMPORTANT]
>
>Alle bestaande [ montages van de groepstoestemming ](../configuration-reference/catalog/catalog.md#category-permissions) worden genegeerd door **_alle_** categorieën in de catalogus wanneer de **_[!UICONTROL Shared Catalog]_** eigenschap wordt toegelaten. [!UICONTROL Shared Catalog] beheert alle categorierechten in de catalogus volledig wanneer deze is ingeschakeld.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de categorie met producten die u wilt bijwerken.

   Als u alle producten wilt opnemen, selecteert u de bovenste categorie in de structuur.

1. De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Category Permissions]** sectie.

1. Klik op **[!UICONTROL New Permission]** en voer de volgende handelingen uit:

   ![ Nieuwe Toestemming ](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Kies de **[!UICONTROL Customer Group]** die overeenkomt met de gedeelde catalogus en wijzig zo nodig de machtigingsinstellingen.

     ![ Regel van de Rechten van de Categorie ](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Als u een machtigingsregel voor een andere klantengroep wilt maken, klikt u op **[!UICONTROL New Permissions]** en herhaalt u het proces.

   - Om een toestemmingsregel te schrappen, klik _Schrapping_ ![ het prullenmand ](../assets/icon-delete-trashcan-solid.png) pictogram.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## De catalogusdetails bijwerken

De gedetailleerde informatie van om het even welke gedeelde catalogus kan gemakkelijk van de kolom van de Actie van het Gedeelde net van Catalogi worden bijgewerkt. De veranderingen u aanbrengt worden weerspiegeld in om het even welke bijbehorende bedrijfsrekeningen.

![ Algemene Montages ](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus die u wilt bijwerken naar de kolom **[!UICONTROL Action]** en selecteer **[!UICONTROL General Settings]** .

   ![ de Details van de Catalogus ](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Werk indien nodig de gedetailleerde informatie over de catalogus bij.

   - Als u de naam van een gedeelde catalogus wijzigt, verandert ook de naam van de bijbehorende klantengroep.
   - Als u het catalogustype wijzigt van `Custom` in `Public` , wordt de bestaande openbare catalogus omgezet in een aangepaste catalogus. Alle bedrijven die banden hebben met de oorspronkelijke openbare catalogus, worden opnieuw toegewezen aan de vervangende catalogus. Een openbare catalogus kan niet worden omgezet in een aangepaste catalogus.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Verwijzing naar gedeelde cataloguspagina

### Knopbalk

| Knop | Beschrijving |
|--- |--- |
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Gedeelde catalogi zonder de nieuwe gedeelde catalogus op te slaan. |
| [!UICONTROL Delete] | Hiermee verwijdert u de catalogus en wijst u eventuele gekoppelde bedrijven en hun leden toe aan de gedeelde openbare catalogus. |
| [!UICONTROL Reset] | Hiermee wist u de vorm van niet-opgeslagen wijzigingen en herstelt u de oorspronkelijke details van de catalogus. |
| [!UICONTROL Duplicate] | Creeert a [ dubbel exemplaar van de catalogus ](catalog-shared-create.md). Voor een aangepaste catalogus, het prijsmodel en de structuur van het origineel, maar zonder de ondernemersverenigingen. Als een openbare gedeelde catalogus wordt gedupliceerd, verandert het type van de gedupliceerde catalogus in `custom` . Er wordt ook een overeenkomende klantengroep gemaakt met dezelfde naam als de gedupliceerde catalogus. Door gebrek, wordt een dubbele catalogus genoemd _Duplicaat van_ de originele catalogus. |
| [!UICONTROL Save and Continue Edit] | Hiermee slaat u alle wijzigingen op en het formulier blijft geopend in de bewerkingsmodus. |
| [!UICONTROL Save] | Hiermee slaat u wijzigingen op, sluit u het formulier en keert u terug naar de pagina Gedeelde catalogi. |

{style="table-layout:auto"}

### Catalogusdetails

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Name] | Identificeert de gedeelde catalogus door Admin, en in de klantenrekeningen waar het beschikbaar is. De catalogusnaam moet beschrijvend zijn en mag niet langer zijn dan 32 tekens. U kunt geen twee gedeelde catalogi met dezelfde naam hebben. Maximum aantal tekens: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identificeert een catalogus met aangepaste prijzen die alleen beschikbaar is voor de specifieke bedrijven waaraan deze is toegewezen.<br/>**[!UICONTROL Public]**- Identificeert de gedeelde catalogus die beschikbaar is voor alle gastbezoekers en voor aangemelde klanten die niet aan een bedrijf zijn gekoppeld. Een &quot;standaard&quot;openbare gedeelde catalogus wordt gecreeerd wanneer Adobe Commerce B2B wordt geïnstalleerd, maar moet door de beheerder worden gevormd. Er kan slechts één openbare gedeelde catalogus tegelijk bestaan. |
| [!UICONTROL Customer Tax Class] | Bepaalt de belastingklasse die wordt gebruikt voor aankopen uit de catalogus. De opties omvatten alle beschikbare belastingklassen. |
| [!UICONTROL Description] | Een korte uitleg van de manier waarop de catalogus moet worden gebruikt. |

{style="table-layout:auto"}
