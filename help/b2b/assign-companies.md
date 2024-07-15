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

# De [!UICONTROL Company Hierarchy] beheren

[!BADGE  1.5.0-bèta ]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor Beta-programmadeelnemers"}

Beheerders kunnen een [!UICONTROL Company Hierarchy] maken door aan een aangewezen moedermaatschappij, het bedrijf boven aan de organisatie, verwante bedrijven toe te wijzen. Als [!UICONTROL Company Type] `Company` is, maakt het bedrijf geen deel uit van een organisatie en komt het in aanmerking om een moedermaatschappij te worden of om aan een bestaand moederbedrijf te worden toegewezen.

In Admin, beheert u bedrijfstoewijzingen door een bedrijf uit te geven, en dan de [!UICONTROL Company Hierarchy] configuratie bij te werken om bedrijven toe te wijzen of unassign.

![ Raster van de Hiërarchie van het Bedrijf ](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Voor details over het [!UICONTROL Company Hierarchy] net, zie [ de 2} gebiedsbeschrijvingen van de Hiërarchie van het Bedrijf {.](account-company-create.md#company-hierarchy)

## Bedrijven toewijzen aan een organisatie

1. Van _Admin_ sidebar, navigeer aan **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![ het Net van Bedrijven ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Open in het raster [!UICONTROL Companies] de pagina met bedrijfsdetails om de toewijzingen te maken.

   - Als u extra bedrijven wilt toewijzen aan een bestaand moederbedrijf, selecteert u de handeling **[!UICONTROL Edit]** voor het moederbedrijf.
   - Als u een bovenliggend bedrijf wilt maken, selecteert u de handeling **[!UICONTROL Edit]** die het bedrijf als bovenliggend bedrijf moet aanwijzen.

     U kunt geen moederbedrijf van een bestaand ouder of kindbedrijf tot stand brengen.

1. Vouw op de pagina met bedrijfsdetails **[!UICONTROL Company Hierarchy]** uit.

   ![ Raster van de Hiërarchie van het Bedrijf ](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   Het net toont bestaande bedrijfstoewijzingen, als om het even welk bestaan. Het bovenliggende bedrijf wordt altijd boven aan het [!UICONTROL Company Hierarchy] -raster geplaatst. De markering `[!UICONTROL Current]` geeft het bedrijf aan dat wordt bewerkt.

1. Bedrijven toevoegen aan de moederorganisatie.

   - Selecteer **[!UICONTROL Assign Companies]** als u een keuze wilt maken in een lijst met beschikbare bedrijven.

   - **selecteer allen op Deze Pagina**, of selecteer één of meerdere specifieke punten van de bedrijflijn.

   - Selecteer **[!UICONTROL Assign Selected Companies]** .

   - Voltooi de bedrijfstoewijzing door **[!UICONTROL Assign]** te selecteren.

     ![ wijs bedrijven aan organisatie ](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"} toe

## Ondernemingen van een moedermaatschappij ontkoppelen

1. Voor _Admin_ sidebar, navigeer aan **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![ het Net van Bedrijven ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Open in het [!UICONTROL Companies] -raster de pagina met bedrijfsdetails voor het bovenliggende bedrijf door **[!UICONTROL Edit]** te selecteren.

1. U kunt de lijst met toegewezen bedrijven weergeven door **[!UICONTROL Company Hierarchy]** uit te breiden.

1. Maak in het [!UICONTROL Company Hierarchy] -raster de toewijzing van een bedrijf ongedaan met behulp van het **[!UICONTROL Select]** actiecontrole om te kiezen **[!UICONTROL Unassign from parent]** .

   ![ wijst Bedrijven van een ouderorganisatie ](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"} unassign

1. Als daarom wordt gevraagd, verwijdert u het toegewezen bedrijf uit de hiërarchie door **[!UICONTROL Unassign]** te selecteren.
