---
title: Bedrijfsbeheer
description: Stroomlijnd beheer en beheer van B2B-organisaties met complexe operationele modellen.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Bedrijfsbeheer

[!BADGE 1.5.0-bèta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"}

Bedrijfsbeheer stroomlijnt bedrijfsactiviteiten voor bedrijven met complexe organisatiestructuren. De gebruikers van Admin kunnen een bedrijfshiërarchie bouwen om een organisatie te weerspiegelen B2B door bedrijven aan het aangewezen ouderbedrijf toe te wijzen. Met deze toewijzing kan de beheerder van het moederbedrijf bedrijven binnen de organisatie weergeven en beheren.

Beheerstaken voor bedrijven initiëren vanuit de *[!UICONTROL Companies]* weergeven. Ga vanuit de beheerder naar  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B-raster Bedrijven beheren](./assets/companies-grid-view.png){width="700" zoomable="yes"}

In de *[!UICONTROL Companies grid]* de *[!UICONTROL Company Type]* de kolom wijst erop of een bedrijf als deel van een organisatie, of als afzonderlijk bedrijf wordt beheerd.

- `Parent` is een bedrijfsorganisatie met een of meer toegewezen ondernemingen. Een moedermaatschappij kan niet worden toegewezen als een onderliggend onderdeel van een ander bedrijf.

- `Child` is een bedrijf dat aan een organisatie is toegewezen. Een bedrijf kan slechts aan één moederbedrijf worden toegewezen.

- `Company` vertegenwoordigt één enkele onderneming. Eén bedrijf kan deel uitmaken van een organisatie door van het bedrijf een moedermaatschappij te maken of door het toe te wijzen aan een bestaand moederbedrijf.

Als u een bovenliggend of onderliggend bedrijf bewerkt, vouwt u *[!UICONTROL Company Hierarchy]* alle bedrijven in de organisatie te bekijken. A `Current` De markering geeft het bedrijf aan dat u bewerkt.

![B2B-raster bedrijfshiërarchie](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## De mening en vormt [!UICONTROL Company Hierarchy]

Bij de initiële oprichting van een bedrijf [!UICONTROL Company Hierarchy] raster is leeg. Het is ook leeg als de onderneming één enkele onderneming is.

![B2B-bedrijfshiërarchieraster](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Voor bovenliggende bedrijven kunnen Admin-gebruikers met de juiste machtigingen de volgende taken uitvoeren:

- Bouw de bedrijfshiërarchie door een nieuwe ouderorganisatie, of het bijwerken van bestaande te creëren.
- Beheer een bestaande organisatie om bedrijven toe te voegen of te verwijderen.

Zie voor meer informatie [De bedrijfshiërarchie beheren](assign-companies.md).
