---
title: De bedrijfshiërarchie beheren
description: Bouw en beheer bedrijfshiërarchieën om B2B organisaties met complexe operationele modellen te steunen.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# De [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-bèta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"}

Beheerders kunnen een [!UICONTROL Company Hierarchy] door gelieerde ondernemingen toe te wijzen aan een aangewezen moedermaatschappij, die de onderneming bovenaan in de organisatiehiërarchie staat.

Een moederbedrijf maken door een bedrijf te bewerken dat niet is toegewezen aan een bestaand bedrijf [!UICONTROL Company Hierarchy], en het toewijzen van verbonden ondernemingen.

![Bedrijfshiërarchieraster](./assets/company-detail-view.png){width="700"}

Nadat een bedrijf aan een hiërarchie is toegewezen, [!UICONTROL Company type] in de **Bedrijven** het netwerk identificeert het bedrijf als `Parent` of  `Child` bedrijf.  Als de [!UICONTROL Company Type] is `Company`, maakt de onderneming geen deel uit van een hiërarchie van ondernemingen en komt in aanmerking om een moedermaatschappij te worden of om te worden toegewezen aan een bestaande moedermaatschappij.

>[!NOTE]
>
>Voor meer informatie over de [!UICONTROL Company Hierarchy] raster, zie [Bedrijfshiërarchie](account-company-create.md#company-hierarchy) veldbeschrijvingen.

In Admin, beheert u bedrijfstoewijzingen door een bedrijf uit te geven, en dan te gebruiken [!UICONTROL Company Hierarchy] van de [!UICONTROL Company] pagina om toe te wijzen aan of toe te wijzen aan bedrijven.

## Bedrijven toewijzen aan een moedermaatschappij

1. Op de _Beheerder_ zijbalk, navigeren naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Open in het raster Bedrijven de pagina met bedrijfsdetails om de toewijzingen te maken.

   - Als u aanvullende ondernemingen aan een bestaande moedermaatschappij wilt toewijzen, selecteert u de **[!UICONTROL Edit]** actie voor het moederbedrijf.
   - Als u een nieuw moederbedrijf wilt maken, selecteert u de optie **[!UICONTROL Edit]** actie voor het als moedermaatschappij aangewezen bedrijf.

     U kunt geen nieuw moederbedrijf van een bestaand ouder of kindbedrijf tot stand brengen.

   ![Nieuw bedrijf](./assets/company-update.png){width="700" zoomable="yes"}

1. Vouw op de pagina Bedrijfsgegevens de **[!UICONTROL Company Hierarchy]** vervolgkeuzelijst en selecteer **[!UICONTROL Assign Companies]**.

   ![Nieuw bedrijf](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   Wanneer u deze weergave uitvouwt, kunt u bestaande bedrijfstoewijzingen zien, als die er zijn. Het moederbedrijf verschijnt altijd boven aan het dialoogvenster _[!UICONTROL Company Hierarchy]_raster met een `current company indicator` weergegeven in de bedrijfsregel die wordt bewerkt.

1. Bedrijven die beschikbaar zijn voor toewijzing worden vermeld in het raster. Selecteer de bedrijven die u wilt toewijzen en selecteer vervolgens **[!UICONTROL Assign Selected Companies]**.

1. U kunt **Alles op deze pagina selecteren** of één specifiek onderdeel van de bedrijfsregel en klik op **[!UICONTROL Assign Selected Companies]**.

   ![Nieuw bedrijf](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. Als daarom wordt gevraagd, voltooit u de bedrijfstoewijzing door op **[!UICONTROL Assign]**.

## Ondernemingen van een moedermaatschappij ontkoppelen

1. Op de _Beheerder_ zijbalk, navigeren naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Open op de pagina Ondernemingen de pagina met bedrijfsgegevens voor de moedermaatschappij door de **[!UICONTROL Edit]** handeling.

   ![Nieuw bedrijf](./assets/company-update.png){width="700" zoomable="yes"}

1. Bekijk de lijst van toegewezen bedrijven door uit te breiden **[!UICONTROL Company Hierarchy]** vervolgkeuzelijst.

1. Maak in het hiërarchieraster van het bedrijf de toewijzing van een bedrijf ongedaan door het **[!UICONTROL Select]** actie voor het bedrijf en kies vervolgens **[!UICONTROL Unassign from parent]**.

   ![Nieuw bedrijf](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. Verwijder het toegewezen bedrijf uit de hiërarchie door **[!UICONTROL Unassign]**.
