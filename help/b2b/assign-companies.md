---
title: De bedrijfshiërarchie beheren
description: Leer hoe te om B2B organisaties met complexe operationele modellen te beheren door bedrijfhiërarchieën te bouwen
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# De [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-bèta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"}

Beheerders kunnen een [!UICONTROL Company Hierarchy] door gelieerde ondernemingen toe te wijzen aan een aangewezen moedermaatschappij, de onderneming die aan de top van de organisatie staat. Als de [!UICONTROL Company Type] is `Company`, maakt de onderneming geen deel uit van een organisatie en komt in aanmerking om een moedermaatschappij te worden of aan een bestaande moedermaatschappij te worden toegewezen.

In Admin, beheert u bedrijfstoewijzingen door een bedrijf uit te geven, en dan update [!UICONTROL Company Hierarchy] configuratie om bedrijven toe te wijzen of toe te wijzen.

![Bedrijfshiërarchieraster](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Voor meer informatie over de [!UICONTROL Company Hierarchy] raster, zie [Bedrijfshiërarchie](account-company-create.md#company-hierarchy) veldbeschrijvingen.

## Bedrijven toewijzen aan een organisatie

1. Van de _Beheerder_ zijbalk, navigeren naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. In de [!UICONTROL Companies] , opent u de pagina met bedrijfsdetails om de toewijzingen te maken.

   - Als u aanvullende ondernemingen aan een bestaande moedermaatschappij wilt toewijzen, selecteert u de **[!UICONTROL Edit]** actie voor het moederbedrijf.
   - Als u een moederbedrijf wilt maken, selecteert u de optie **[!UICONTROL Edit]** actie voor het bedrijf om als ouder aan te wijzen.

     U kunt geen moederbedrijf van een bestaand ouder of kindbedrijf tot stand brengen.

1. Vouw op de pagina met bedrijfsdetails uit **[!UICONTROL Company Hierarchy]**.

   ![Bedrijfshiërarchieraster](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   Het net toont bestaande bedrijfstoewijzingen, als om het even welk bestaan. Het moederbedrijf bevindt zich altijd boven aan de lijst [!UICONTROL Company Hierarchy] raster. De `[!UICONTROL Current]` de vlag wijst op het bedrijf dat wordt uitgegeven.

1. Bedrijven toevoegen aan de moederorganisatie.

   - Maak een keuze uit een lijst met beschikbare bedrijven door **[!UICONTROL Assign Companies]**.

   - **Alles op deze pagina selecteren** of selecteer een of meer specifieke onderdelen van de bedrijfslijn.

   - Selecteren **[!UICONTROL Assign Selected Companies]**.

   - Voltooi de bedrijfs taak door te selecteren **[!UICONTROL Assign]**.

     ![Bedrijven toewijzen aan organisatie](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Ondernemingen van een moedermaatschappij ontkoppelen

1. Op de _Beheerder_ zijbalk, navigeren naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. In de [!UICONTROL Companies] raster: open de pagina met bedrijfsgegevens voor het moederbedrijf door **[!UICONTROL Edit]**.

1. Bekijk de lijst van toegewezen bedrijven door uit te breiden **[!UICONTROL Company Hierarchy]**.

1. Van de [!UICONTROL Company Hierarchy] raster, toewijzen van bedrijf ongedaan maken met **[!UICONTROL Select]** actiecontrole om te kiezen **[!UICONTROL Unassign from parent]**.

   ![Ondernemingen van een moederorganisatie verwijderen](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Verwijder het toegewezen bedrijf uit de hiërarchie door **[!UICONTROL Unassign]**.
