---
title: Overzicht van gedeelde catalogus
description: Leer meer over de gedeelde catalogi die door B2B voor Adobe Commerce worden geleverd en hoe u deze kunt gebruiken om catalogi met aangepaste prijzen voor verschillende bedrijfsaccounts te onderhouden.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Overzicht van gedeelde catalogus

B2B voor Adobe Commerce biedt u de mogelijkheid om de classificatie te behouden _gedeeld_ catalogi met aangepaste prijzen voor verschillende bedrijven. Naast de norm _primair_, productcatalogus, biedt de klant toegang tot twee typen gedeelde catalogi met verschillende prijsstructuren.

Als de [Functie Gedeelde catalogus](enable-basic-features.md) is ingeschakeld in de configuratie, blijft de oorspronkelijke primaire catalogus zichtbaar in de beheerfunctie, maar is alleen de standaard (algemene) gedeelde catalogus die door de overheid wordt gebruikt zichtbaar in de winkel. Bovendien kunnen aangepaste catalogi worden gemaakt die alleen zichtbaar zijn voor leden van specifieke [bedrijf](account-companies.md) rekeningen.

Voor de `Default (General)` openbare gedeelde catalogus, moet u producten toewijzen om de catalogus in de winkel weer te geven. Standaard is deze leeg en bevat deze geen producten.

>[!NOTE]
>
>**[B2B-release 1.3.0](release-notes.md#b2b-v130) en hoger** — Wanneer u een gedeelde catalogus maakt, moet u elk [categorietoestemming](../catalog/category-permissions.md) voor de catalogus is ingesteld op _[!UICONTROL Allow for the Display Product Prices]_en_[!UICONTROL Add to Cart]_ voor klantengroepen die deze toegang in de montages van de catalogustoestemming worden toegewezen. Eerder werden deze instellingen automatisch ingesteld op `Deny` zelfs wanneer catalogusmachtigingen zijn ingesteld op `Allow`.

>[!IMPORTANT]
>
>Alle bestaande [machtigingen voor groep instellen](../configuration-reference/catalog/catalog.md#category-permissions) worden genegeerd door **_alles_** categorieën in de catalogus als de **_[!UICONTROL Shared Catalog]_** -functie is ingeschakeld. [!UICONTROL Shared Catalog] beheert volledig alle categorierechten in de catalogus wanneer deze is ingeschakeld.

De _[!UICONTROL Shared Catalogs]_biedt toegang tot de gereedschappen voor het beheer van uw gedeelde catalogi. De pagina is vergelijkbaar met de standaard [Werkruimte Beheer](../getting-started/admin-workspace.md)met filters en besturingselementen voor handelingen. In het raster worden alle gedeelde catalogi weergegeven, inclusief de standaard openbare gedeelde catalogus en alle aangepaste catalogi die u hebt ingesteld.

![Gedeelde catalogi](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Toegang krijgen tot de [!UICONTROL Shared Catalogs] page

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Besturingselementen voor handelingen

De [besturingselementen voor handelingen](../getting-started/admin-actions-control.md) in de linkerbovenhoek kunt u met het besturingselement voor massaacties geselecteerde gedeelde catalogi verwijderen die u niet meer nodig hebt. In het raster kunt u de _[!UICONTROL Actions]_de kolom bevat de volledige selectie van hulpmiddelen om uw gedeelde catalogi te beheren.

![Handelingen voor gedeelde catalogus](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

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
| [!UICONTROL Type] | Hiermee wordt het type gedeelde catalogus aangeduid als: <br/>**[!UICONTROL Public]**- De standaard openbare gedeelde catalogus wordt automatisch gemaakt wanneer B2B voor Adobe Commerce wordt geïnstalleerd. Deze wordt aanvankelijk toegewezen aan de `General` en `Not Logged In` de klantengroepen, en is zichtbaar aan gasten en individuele het programma geopende klanten die niet met een bedrijf worden geassocieerd. Het systeem ondersteunt slechts één openbare gedeelde catalogus tegelijk.<br/>**[!UICONTROL Custom]** - Een aangepaste gedeelde catalogus bevat prijzen die alleen zichtbaar zijn voor aangemelde medewerkers van de toegewezen bedrijfsaccounts. U kunt zoveel aangepaste gedeelde catalogi maken als u nodig hebt. |
| [!UICONTROL Customer Tax Class] | De belastingklasse die aan de overeenkomstige klantengroep wordt toegewezen. Deze kolom wordt niet weergegeven in het standaardraster, maar kan worden toegevoegd door de kolomlay-out te wijzigen. |
| [!UICONTROL Created At] | De datum en tijd waarop de gedeelde catalogus is gemaakt. |
| [!UICONTROL Created By] | De voornaam en achternaam van de opslagbeheerder die de gedeelde catalogus heeft gemaakt. |
| [!UICONTROL Action] | Hiermee geeft u acties weer die op geselecteerde catalogi moeten worden toegepast. Opties: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
