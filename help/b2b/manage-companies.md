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

[!BADGE  1.5.0-bèta ]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor Beta-programmadeelnemers"}

Bedrijfsbeheer stroomlijnt bedrijfsactiviteiten voor bedrijven met complexe organisatiestructuren. De gebruikers van Admin kunnen een bedrijfshiërarchie bouwen om een organisatie te weerspiegelen B2B door bedrijven aan het aangewezen ouderbedrijf toe te wijzen. Met deze toewijzing kan de beheerder van het moederbedrijf bedrijven binnen de organisatie weergeven en beheren.

Start bedrijfsbeheertaken vanuit de *[!UICONTROL Companies]* -weergave. Ga vanuit Beheer naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]** .

![ B2B beheert het Net van Bedrijven ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

In de kolom *[!UICONTROL Companies grid]* geeft de kolom *[!UICONTROL Company Type]* aan of een bedrijf wordt beheerd als onderdeel van een organisatie of als een afzonderlijk bedrijf.

- `Parent` is een bedrijfsorganisatie met een of meer toegewezen bedrijven. Een moedermaatschappij kan niet worden toegewezen als een onderliggend onderdeel van een ander bedrijf.

- `Child` is een bedrijf dat is toegewezen aan een organisatie. Een bedrijf kan slechts aan één moederbedrijf worden toegewezen.

- `Company` staat voor één bedrijf. Eén bedrijf kan deel uitmaken van een organisatie door van het bedrijf een moedermaatschappij te maken of door het toe te wijzen aan een bestaand moederbedrijf.

Wanneer u een ouder of kindbedrijf uitgeeft, breid *[!UICONTROL Company Hierarchy]* uit om alle bedrijven in de organisatie te bekijken. Een markering `Current` geeft het bedrijf aan dat u bewerkt.

![ B2B het net van de Hiërarchie van het Bedrijf ](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## De [!UICONTROL Company Hierarchy] weergeven en configureren

Bij het maken van het eerste bedrijf is het [!UICONTROL Company Hierarchy] -raster leeg. Het is ook leeg als de onderneming één enkele onderneming is.

![ B2B het Net van de Hiërarchie van het Bedrijf ](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Voor bovenliggende bedrijven kunnen Admin-gebruikers met de juiste machtigingen de volgende taken uitvoeren:

- Bouw de bedrijfshiërarchie door een nieuwe ouderorganisatie, of het bijwerken van bestaande te creëren.
- Beheer een bestaande organisatie om bedrijven toe te voegen of te verwijderen.

Voor details, zie [ de bedrijfshiërarchie ](assign-companies.md) leiden.
