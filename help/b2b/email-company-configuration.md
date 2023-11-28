---
title: Bedrijfs-e-mail configureren
description: Leer over de e-mailopties en de malplaatjes die worden gebruikt om mededelingen voor bedrijfrekeningen te verzenden.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# E-mailopties voor bedrijven configureren

De [verkoopvertegenwoordiger](account-company-manage.md) dat als primair contact voor een bedrijf wordt toegewezen wordt gevormd door gebrek als afzender van vele geautomatiseerde e-mailberichten die naar het bedrijf worden verzonden.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Company Configuration]**.

1. Indien nodig, instellen **[!UICONTROL Store View]** in de winkelweergave om de [bereik](../getting-started/websites-stores-views.md#scope-settings) van de configuratie.

1. Voltooi de **[!UICONTROL Company Registration]** sectie:

   >[!NOTE]
   >
   >Wis de **[!UICONTROL Use system value]** Schakel het selectievakje in om het veld bewerkbaar te maken.

   - Set **[!UICONTROL Company Registration Email Recipient]** aan de [contactpersoon voor winkel](../getting-started/store-details.md#store-email-addresses) wie op de hoogte moet worden gesteld wanneer een nieuw registratieverzoek van een vennootschap wordt ontvangen.

   - In de **[!UICONTROL Send Company Registration Email Copy To]** Voer in het veld het e-mailadres in van elke persoon die een kopie van de registratiekennisgeving moet ontvangen. Scheid meerdere e-mailadressen met een komma.

   - Als u wilt bepalen hoe de kopie van het bericht wordt verzonden, stelt u **[!UICONTROL Send Email Copy Method]** op een van de volgende wijzen:

      - `Bcc` - verzendt een _blinde, hoffelijke kopie_ door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
      - `Separate Email` - Hiermee verzendt u de kopie als een aparte e-mail.

   - Als u een e-mailsjabloon hebt voorbereid voor gebruik in plaats van de standaardsjabloon, stelt u **[!UICONTROL Default Company Registration Email]** op de naam van de sjabloon. Standaard worden de `Company Registration Request` sjabloon wordt gebruikt.

     ![Configuratie van klanten - bedrijfsregistratie](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Voltooi de **[!UICONTROL Customer-Related Emails]** sectie:

   Als u alternatieve e-mailsjablonen hebt voorbereid voor gebruik in plaats van de standaardinstellingen, kiest u de sjabloon die u wilt gebruiken voor elk van de volgende opties:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuratie van klanten - aan klanten gerelateerde e-mails](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Voltooi de **[!UICONTROL Company Status Change]** sectie:

   - Set **[!UICONTROL Company Status Change for Email Recipient]** aan de [contactpersoon voor winkel](../getting-started/store-details.md#store-email-addresses) wie in kennis moet worden gesteld wanneer de status van een onderneming verandert.

   - In de **[!UICONTROL Send Company Status Change Email Copy To]** Voer in het veld het e-mailadres in van elke persoon die een kopie van het bericht voor statuswijziging moet ontvangen. Scheid meerdere e-mailadressen met een komma.

   - Als u wilt bepalen hoe de kopie van het bericht wordt verzonden, stelt u **[!UICONTROL Send Email Copy Method]** op een van de volgende wijzen:

      - `Bcc` - verzendt een _blinde, hoffelijke kopie_ door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
      - `Separate Email` - Hiermee verzendt u de kopie als een aparte e-mail.

   - Als u een voorbereid e-mailmalplaatje hebt dat in plaats van het gebrek moet worden gebruikt wanneer de bedrijfstatus van verandert `Pending Approval` tot `Active`, set **[!UICONTROL Default 'Company Status Change to Active 1' Email]** naar die template. Standaard worden de `Company Status Active 1` sjabloon wordt gebruikt.

   - Als u een voorbereid e-mailmalplaatje hebt dat in plaats van het gebrek moet worden gebruikt wanneer de bedrijfstatus van verandert `Rejected` of `Blocked` tot `Active`, set **[!UICONTROL Default 'Company Status Change to Active 2' Email]** naar die template. Standaard worden de `Company Status Active 2` sjabloon wordt gebruikt.

   - Als u een voorbereid e-mailmalplaatje hebt dat in plaats van het gebrek moet worden gebruikt wanneer de bedrijfstatus verandert in `Rejected`, set **[!UICONTROL Default 'Company Status Change to Rejected' Email]** naar die template. Standaard worden de `Company Status Rejected` sjabloon wordt gebruikt.

   - Als u een voorbereid e-mailmalplaatje hebt dat in plaats van het gebrek moet worden gebruikt wanneer de bedrijfstatus verandert in `Blocked`, set **[!UICONTROL Default 'Company Status Change to Blocked' Email]** naar die template. Standaard worden de `Company Status Blocked` sjabloon wordt gebruikt.

   - Als u een voorbereid e-mailmalplaatje hebt dat in plaats van het gebrek moet worden gebruikt wanneer de bedrijfstatus verandert in `Pending Approval`, set **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** naar die template. Standaard worden de `Company Status Pending Approval` sjabloon wordt gebruikt.

     ![Configuratie van klanten - wijziging van bedrijfsstatus](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Voltooi de **[!UICONTROL Company Credit Emails]** sectie:

   - Set **[!UICONTROL Company Credit Change Email Sender]** aan de [contactpersoon voor winkel](../getting-started/store-details.md#store-email-addresses) wie op de hoogte moet worden gebracht wanneer de kredietlimiet die aan een onderneming is toegekend, wordt gewijzigd. Standaard wordt het bericht verzonden naar _Verkoopvertegenwoordiger_.

   - In de **[!UICONTROL Send Company Credit Change Email Copy To]** Voer in het veld het e-mailadres in van elke persoon die een kopie van de kennisgeving van wijziging van creditcard moet ontvangen. Scheid meerdere e-mailadressen met een komma.

   - Als u wilt bepalen hoe de kopie van het bericht wordt verzonden, stelt u **[!UICONTROL Send Email Copy Method]** op een van de volgende wijzen:

      - `Bcc` - verzendt een _blinde, hoffelijke kopie_ door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
      - `Separate Email` - Hiermee verzendt u de kopie als een aparte e-mail.

   - Als u e-mailsjablonen hebt voorbereid voor gebruik in plaats van de standaardwaarden, kiest u de sjabloon voor elk van de volgende meldingen die naar de bedrijfsbeheerder worden verzonden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuratie van klanten - bedrijfskrediet-e-mails](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
