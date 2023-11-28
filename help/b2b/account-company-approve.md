---
title: Een bedrijfsaccount goedkeuren
description: Leer hoe u aanvragen voor bedrijfsaccounts goedkeurt in Admin.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Een bedrijfsaccount goedkeuren

De status van de verzoeken die van de winkel worden ontvangen om een bedrijf op te richten is `Pending Approval` tot het verzoek door de opslagbeheerder wordt herzien, en of goedgekeurd of verworpen. De status van een bedrijfsaccount kan op een van de volgende manieren worden ingesteld:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

U kunt ook de opdracht [Handelingencontrole](account-company-manage.md) om veelvoudige bedrijfverzoeken goed te keuren.

![In behandeling](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Een bedrijfsaccount goedkeuren dat in behandeling is

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   U kunt de _[!UICONTROL Columns]_selector boven het raster om de **[!UICONTROL Status]**kolom.

1. In de _[!UICONTROL Action]_kolom, klik **[!UICONTROL Edit]**.

1. Set **[!UICONTROL Company Status]** tot `Active`.

   ![De bedrijfsstatus instellen](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL Change status]**.

   De bedrijfsbeheerder ontvangt een e-mailbericht dat het bedrijf nu actief is.

1. Indien van toepassing, instellen **[!UICONTROL Sales Representative]** naar een specifieke Admin-gebruikersaccount.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png)  de **[!UICONTROL Account Information]** en de **[!UICONTROL Comment]** veld voor het invoeren van notities over de account.

   De opmerkingen zijn niet zichtbaar vanuit de winkel.

1. Klik op **[!UICONTROL Save]**.

   Er wordt een bevestigingsbericht verzonden naar het bedrijf en de systeembeheerder van het bedrijf dat de bedrijfsaccount is goedgekeurd.

## Status van onderneming

| Status | Beschrijving |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | Het bedrijf wordt goedgekeurd en kan van de opslagplaats door de bedrijfbeheerder worden beheerd. |
| [!UICONTROL Pending Approval] | Een verzoek om een bedrijfsaccount te maken is ingediend door de winkel, maar wordt nog niet beoordeeld. |
| [!UICONTROL Rejected] | Het verzoek om een bedrijfsaccount te maken is afgewezen door de beheerder van de winkel. |
| [!UICONTROL Blocked] | De bedrijfsrekening verkeert niet meer in goede staat. De klant heeft toegang tot het account via de winkel, maar kan geen aankopen doen. |

{style="table-layout:auto"}
