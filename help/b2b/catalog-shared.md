---
title: Overzicht van gedeelde catalogus
description: Leer meer over de gedeelde catalogi die door Adobe Commerce B2B worden geleverd en hoe u deze kunt gebruiken om catalogi met aangepaste prijzen voor verschillende bedrijfsaccounts te onderhouden.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Overzicht van gedeelde catalogus

Adobe Commerce B2B geeft u de capaciteit om gegoten _gedeelde_ catalogi met douaneprijzen voor verschillende bedrijven te handhaven. Naast de norm, _primaire_, productcatalogus, verleent het klantentoegang tot twee types van gedeelde catalogi met verschillende het tarief structuren.

Als de [ Gedeelde eigenschap van de Catalogus ](enable-basic-features.md) in de configuratie wordt toegelaten, blijft de originele primaire catalogus zichtbaar van Admin, maar slechts het Standaard (Algemene) openbare gedeelde catalogus is zichtbaar van de storefront. Bovendien kunnen de douanecatalogi worden gecreeerd die slechts aan leden van specifieke [ bedrijf ](account-companies.md) rekeningen zichtbaar zijn.

Voor de openbare gedeelde catalogus van `Default (General)` moet u producten toewijzen om de catalogus in de winkel weer te geven. Standaard is deze leeg en bevat deze geen producten.

>[!NOTE]
>
>**[B2B versie 1.3.0 ](release-notes.md#b2b-v130) en later** - wanneer u een gedeelde catalogus creeert, wordt elk [ categorietoestemming ](../catalog/category-permissions.md) voor de catalogus geplaatst aan _[!UICONTROL Allow for the Display Product Prices]_&#x200B;en&#x200B;_[!UICONTROL Add to Cart]_ voor klantengroepen die deze toegang in de montages van de catalogustoestemming worden toegewezen. Eerder werden deze instellingen automatisch ingesteld op `Deny` , zelfs als catalogusmachtigingen waren ingesteld op `Allow` .

>[!IMPORTANT]
>
>Alle bestaande [ montages van de groepstoestemming ](../configuration-reference/catalog/catalog.md#category-permissions) worden genegeerd door **_alle_** categorieën in de catalogus wanneer de **_[!UICONTROL Shared Catalog]_** eigenschap wordt toegelaten. [!UICONTROL Shared Catalog] beheert alle categorierechten in de catalogus volledig wanneer deze is ingeschakeld.

De pagina _[!UICONTROL Shared Catalogs]_&#x200B;biedt toegang tot de gereedschappen voor het beheer van uw gedeelde catalogi. De pagina is gelijkaardig aan de standaard [ werkruimte Admin ](../getting-started/admin-workspace.md), met filters en actiecontroles. In het raster worden alle gedeelde catalogi weergegeven, inclusief de standaard openbare gedeelde catalogus en alle aangepaste catalogi die u hebt ingesteld.

![ Gedeelde Catalogi ](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## De pagina [!UICONTROL Shared Catalogs] openen

Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Besturingselementen voor handelingen

De [ actiecontroles ](../getting-started/admin-actions-control.md) in de upper-left hoek kunnen met de controle van massaacties worden gebruikt om geselecteerde gedeelde catalogi te schrappen die niet meer nodig zijn. In het raster bevat de kolom _[!UICONTROL Actions]_&#x200B;alle gereedschappen voor het beheer van uw gedeelde catalogi.

![ Gedeelde Acties van de Catalogus ](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Besturing | Beschrijving |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Bepaalt de productselectie en de aangepaste prijs die beschikbaar zijn in de gedeelde catalogus. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Hiermee bepaalt u welke bedrijven toegang hebben tot een gedeelde catalogus. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Hiermee bepaalt u de gedetailleerde informatie over de catalogus, zoals de naam, het type catalogus, de belastingklasse van de klant en de beschrijving. |
| [!UICONTROL Delete] | Hiermee verwijdert u de geselecteerde gedeelde catalogi. |

{style="table-layout:auto"}

## Kolombeschrijvingen

| Kop | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Hiermee selecteert u gedeelde catalogusrecords voor het toepassen van een handeling. U kunt het besturingselement in de koptekst gebruiken om alle gedeelde catalogusrecords in het raster te selecteren of de selectie ervan op te heffen. Schakel het selectievakje in als u een afzonderlijke gedeelde catalogus wilt selecteren. |
| [!UICONTROL ID] | Een unieke numerieke id die op volgorde wordt toegewezen wanneer de catalogus wordt gemaakt. |
| [!UICONTROL Name] | De naam van de gedeelde catalogus. Standaard is de standaard (algemene) gedeelde catalogus beschikbaar. |
| [!UICONTROL Type] | Identificeert het type gedeelde catalogus als: <br/>**[!UICONTROL Public]**- De standaard openbare gedeelde catalogus wordt automatisch gemaakt wanneer Adobe Commerce B2B wordt geïnstalleerd. Deze wordt in eerste instantie toegewezen aan de klantengroepen `General` en `Not Logged In` en is zichtbaar voor gasten en individuele aangemelde klanten die niet aan een bedrijf zijn gekoppeld. Het systeem ondersteunt slechts één openbare gedeelde catalogus tegelijk.<br/>**[!UICONTROL Custom]** - Een aangepaste gedeelde catalogus bevat prijzen die alleen zichtbaar zijn voor aangemelde medewerkers van de toegewezen bedrijfsaccounts. U kunt zoveel aangepaste gedeelde catalogi maken als u nodig hebt. |
| [!UICONTROL Customer Tax Class] | De belastingklasse die aan de overeenkomstige klantengroep wordt toegewezen. Deze kolom wordt niet weergegeven in het standaardraster, maar kan worden toegevoegd door de kolomlay-out te wijzigen. |
| [!UICONTROL Created At] | De datum en tijd waarop de gedeelde catalogus is gemaakt. |
| [!UICONTROL Created By] | De voornaam en achternaam van de opslagbeheerder die de gedeelde catalogus heeft gemaakt. |
| [!UICONTROL Action] | Hiermee geeft u acties weer die op geselecteerde catalogi moeten worden toegepast. Opties: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
