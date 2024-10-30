---
title: Bedrijfsbeheer
description: Stroomlijn het beheer van B2B-organisaties met complexe operationele modellen.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Bedrijfsbeheer

Bedrijfsbeheer stroomlijnt bedrijfsactiviteiten voor bedrijven met complexe organisatiestructuren. Beheerders kunnen een bedrijfshiërarchie bouwen om een B2B-organisatie te spiegelen door bedrijven toe te wijzen aan het aangewezen moederbedrijf. Met deze toewijzing kan de beheerder van het moederbedrijf bedrijven binnen de organisatie weergeven en beheren.

Start bedrijfsbeheertaken vanuit de *[!UICONTROL Companies]* -weergave. Ga vanuit de beheerder naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]** .

![ B2B leidt het Net van Bedrijven ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

De kolom *[!UICONTROL Company Type]* geeft aan of een bedrijf wordt beheerd als onderdeel van een organisatie of als afzonderlijk bedrijf.

- `Parent` is een bedrijfsorganisatie met een of meer toegewezen bedrijven. Een moederbedrijf kan niet worden toegewezen als een onderliggend bedrijf van een ander bedrijf.

- `Child` is een bedrijf dat is toegewezen aan een organisatie. Een bedrijf kan slechts aan één moederbedrijf worden toegewezen.

- `Company` staat voor één bedrijf. Een enkel bedrijf kan deel uitmaken van een organisatie door het een moederbedrijf te maken of door het toe te wijzen aan een bestaand moederbedrijf.

Als u een ouder- of onderliggend bedrijf bewerkt, vouwt u *[!UICONTROL Company Hierarchy]* uit om alle bedrijven in de organisatie weer te geven. Een markering `Current` geeft het bedrijf aan dat u bewerkt.

![ B2B het net van de Hiërarchie van het Bedrijf ](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## De [!UICONTROL Company Hierarchy] weergeven en configureren

Bij het maken van het eerste bedrijf is het raster *[!UICONTROL Company Hierarchy]* leeg. Het is ook leeg als het bedrijf één bedrijf is.

![ B2B het Net van de Hiërarchie van het Bedrijf ](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Als het bedrijf een moederbedrijf voor een organisatie is en de bedrijfsaccounts voor andere bedrijven in de organisatie al zijn geconfigureerd in Adobe Commerce, kunnen Admin-gebruikers met de juiste machtigingen bedrijven toewijzen en het *[!UICONTROL Company Hierarchy]* -raster gebruiken om andere bedrijfbeheertaken uit te voeren:

- Bekijk alle bedrijven die zijn gekoppeld aan het moederbedrijf.
- Wijs meer bedrijven toe aan de organisatie vanaf de detailpagina van het moederbedrijf.
- Verwijder een bedrijf uit een organisatie met de handeling *[!UICONTROL Unassign from parent]* .
- Werk de *[!UICONTROL Advanced Settings]* -configuratie bij om dezelfde instellingen op meerdere bedrijven toe te passen.

Voor gedetailleerde instructies, zie [ de bedrijfshiërarchie ](manage-company-hierarchy.md) leiden.

