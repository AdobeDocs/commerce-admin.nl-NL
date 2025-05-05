---
title: Manage the Company Hierarchy
description: Build and manage company hierarchies to support B2B organizations with complex operational models.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Company Hierarchy]

[!UICONTROL Company Hierarchy]

Creëer in Beheer een moederbedrijf door een afzonderlijk bedrijf (`[!UICONTROL Company Type] = Company`) te bewerken en verwante bedrijven toe te wijzen in de [!UICONTROL Company Hierarchy] -configuratie.

![](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>[!UICONTROL Company Hierarchy][&#128279;](account-company-create.md#company-hierarchy)

*[!UICONTROL Company Hierarchy]* *[!UICONTROL Actions]*[&#128279;](#change-company-settings)

## Assign companies to a parent company

1. __&#x200B;**[!UICONTROL Customers]**&#x200B;**[!UICONTROL Companies]**

   ![ het Net van Bedrijven ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Open vanuit het [!UICONTROL Companies] -raster de pagina met bedrijfsdetails om de toewijzingen te maken.

   - Als u extra bedrijven wilt toewijzen aan een bestaand moederbedrijf, selecteert u de handeling **[!UICONTROL Edit]** voor het moederbedrijf.
   - Als u een moedermaatschappij wilt maken, selecteert u de handeling **[!UICONTROL Edit]** voor het bedrijf dat als moedermaatschappij is aangewezen.

     U kunt geen nieuw moederbedrijf van een bestaand ouder of kindbedrijf tot stand brengen.

1. Vouw op de pagina Bedrijfsgegevens **[!UICONTROL Company Hierarchy]** uit en selecteer vervolgens **[!UICONTROL Assign Companies]** .

   ![ creeer ouderbedrijf ](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. Kies in de lijst met beschikbare bedrijven de bedrijven die u wilt toewijzen en selecteer vervolgens **[!UICONTROL Assign Selected Companies]** .

   ![ Uitgezochte bedrijven om toe te wijzen ](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Als hierom wordt gevraagd, voltooit u de bedrijfstoewijzing door **[!UICONTROL Assign]** te selecteren.

## Ondernemingen van een moedermaatschappij ontkoppelen

1. **[!UICONTROL Edit]**

   ![](./assets/company-update.png){width="700" zoomable="yes"}

1. **[!UICONTROL Company Hierarchy]**

1. Remove the company from the organization.

   - In de kolom [!UICONTROL Action] die het bedrijf moet verwijderen, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]** .

     ![](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - **[!UICONTROL Unassign]**

## Manage company settings for an organization

[&#128279;](account-company-create.md#advanced-settings)

During the update process the initial configuration values default to the the current values configured for the parent company. You must change at least one setting to update the configuration for selected companies.

**verander de Geavanceerde configuratie van Montages voor veelvoudige bedrijven**

1. Voor _Admin_ sidebar, navigeer aan **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Bewerk in het raster [!UICONTROL Companies] het bovenliggende bedrijf door **[!UICONTROL Edit]** in de kolom **[!UICONTROL Action]** te selecteren.

1. Vouw de sectie **[!UICONTROL Company Hierarchy]** op de detailpagina van het moederbedrijf uit om bedrijven in de organisatie weer te geven.

1. Selecteer de bedrijven die u wilt configureren.

   ![ Uitgezochte bedrijven van bedrijfshiërarchie ](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Selecteer **[!UICONTROL Change company settings]** bij het **[!UICONTROL Actions]** -besturingselement boven het raster.

   ![ bedrijfmontages van de Verandering voor bedrijfshiërarchie ](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Wijzig de configuratie van de instellingen.

   - Zoek op de pagina [!UICONTROL Change company settings] naar de configuratie-instelling die u wilt wijzigen.

   - Schakel het selectievakje **[!UICONTROL Change]** in om de instelling in te schakelen.

   - Update the value as needed.

     ![](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. **[!UICONTROL Apply Changes]**

1. **[!UICONTROL Change settings]**

>[!TIP]
>
>Manage the advanced settings configuration for a single company by editing the company line item.
