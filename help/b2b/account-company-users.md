---
title: Gebruikersaccounts van bedrijven beheren
description: Meer informatie over bedrijfsgebruikersaccounts en hoe deze werken binnen het bijbehorende bedrijfsaccount.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Gebruikersaccounts van bedrijven beheren

De gebruikers van het bedrijf worden toegewezen door de bedrijfbeheerder, en zijn zichtbaar van Admin in Admin in _[!UICONTROL Customers]_raster naar type klant;_[!UICONTROL Company User]_. Deze personen zijn doorgaans kopers met verschillende machtigingsniveaus voor toegang tot services en bronnen in de winkel.

De bedrijfbeheerder plaatst eerst omhoog [bedrijfsstructuur](account-company-structure.md)en voltooit vervolgens de volgende taken, indien nodig:

- Bedrijfgebruikers maken en gebruikers toewijzen aan teams

- Rollen en machtigingen definiëren en gebruikers toewijzen aan rollen

>[!IMPORTANT]
>
>Gebruikers van het bedrijf kunnen alleen door de systeembeheerder worden toegevoegd, bewerkt of verwijderd. Verwijderen kan niet ongedaan worden gemaakt omdat de gebruiker uit de bedrijfsstructuur is verwijderd.

## Bedrijfsgebruikers toevoegen

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Company Users]**.

   ![Bedrijfsgebruikers](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Klikken **[!UICONTROL Add New User]** en doet het volgende:

   - Hiermee wordt het dialoogvenster **[!UICONTROL Job Title]** van de nieuwe gebruiker.

   - Kies de passende **[!UICONTROL User Role]** als de rollen en de toestemmingen worden bepaald. Anders kunnen ze later terugkeren om de rol toe te wijzen.

     ![Nieuwe gebruiker toevoegen](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Vul de overige velden naar wens in voor de gebruiker:

      - **[!UICONTROL First Name]** en **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   Standaard worden de **[!UICONTROL Status]** van de rekening `Active`.

1. Na voltooiing klikt u op **[!UICONTROL Save]**.

1. Herhaalt het proces om zo vele bedrijfgebruikers tot stand te brengen zoals nodig.

   De nieuwe gebruikers verschijnen in de lijst van de Gebruikers van het Bedrijf, samen met de Beheerder van het Bedrijf.

Om tijd tijdens hun eerste orde te besparen, kan de bedrijfbeheerder elke bedrijfgebruiker eraan herinneren om het standaardbedrijf het factureren en het verzendadres aan hun toe te voegen [adresboek](../customers/account-dashboard-address-book.md).

## Bedrijfsgebruikers bewerken

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Company Users]**.

1. Zoekt het gebruikersrecord dat moet worden bijgewerkt en klikt **[!UICONTROL Edit]**.

1. Hiermee brengt u de benodigde wijzigingen aan.

1. Na voltooiing klikt u op **[!UICONTROL Save]**.

## Een bedrijfsgebruiker verwijderen

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Company Structure]**.

1. Selecteert de bedrijfgebruiker in de bedrijfstructuur.

1. Klikken **[!UICONTROL Delete Selected]**.

   ![Gebruiker verwijderen](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Wanneer ertoe aangezet om te bevestigen, klikt **[!UICONTROL Delete]**.

In de Admin blijft de gebruiker van het bedrijf vermeld in [Klanten](../customers/customers-all.md) raster, maar met een `Inactive` status.

## Veldomschrijvingen

| Veld | Beschrijving |
|--------------|---------------|
| [!UICONTROL Job Title] | De functie van de bedrijfgebruiker. |
| [!UICONTROL User Role] | De [rol](account-company-roles-permissions.md) toegewezen aan de bedrijfgebruiker. Opties: `Default User` / (andere rollen) |
| [!UICONTROL First Name] | De voornaam van de bedrijfgebruiker. |
| [!UICONTROL Last Name] | De achternaam van de bedrijfgebruiker. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfgebruiker. |
| [!UICONTROL Phone Number] | Het telefoonnummer van de bedrijfgebruiker. |
| [!UICONTROL Status] | De status van de bedrijfsgebruikersaccount. Opties: `Active` / `Inactive` |

{style="table-layout:auto"}
