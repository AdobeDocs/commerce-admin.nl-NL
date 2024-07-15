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

Bedrijfgebruikers worden toegewezen door de systeembeheerder van het bedrijf en zijn zichtbaar van Admin in het _[!UICONTROL Customers]_-raster door het klanttype,_[!UICONTROL Company User]_ . Deze personen zijn doorgaans kopers met verschillende machtigingsniveaus voor toegang tot services en bronnen in de winkel.

De bedrijfbeheerder plaatst eerst omhoog de [ bedrijfstructuur ](account-company-structure.md), en voltooit dan de volgende taken, zoals nodig:

- Bedrijfgebruikers maken en gebruikers toewijzen aan teams

- Rollen en machtigingen definiëren en gebruikers toewijzen aan rollen

>[!IMPORTANT]
>
>Gebruikers van het bedrijf kunnen alleen door de systeembeheerder worden toegevoegd, bewerkt of verwijderd. Verwijderen kan niet ongedaan worden gemaakt omdat de gebruiker uit de bedrijfsstructuur is verwijderd.

## Bedrijfsgebruikers toevoegen

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies **[!UICONTROL Company Users]** in het linkerdeelvenster.

   ![ Gebruikers van het Bedrijf ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Add New User]** en voer de volgende handelingen uit:

   - Voer de **[!UICONTROL Job Title]** van de nieuwe gebruiker in.

   - Kies de juiste **[!UICONTROL User Role]** als de rollen en machtigingen zijn gedefinieerd. Anders kunnen ze later terugkeren om de rol toe te wijzen.

     ![ voeg nieuwe gebruiker ](./assets/company-structure-users-add.png){width="700" zoomable="yes"} toe

   - Vul de overige velden naar wens in voor de gebruiker:

      - **[!UICONTROL First Name]** en **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   De standaardwaarde voor **[!UICONTROL Status]** van de account is `Active` .

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

1. Herhaalt het proces om zo vele bedrijfgebruikers tot stand te brengen zoals nodig.

   De nieuwe gebruikers verschijnen in de lijst van de Gebruikers van het Bedrijf, samen met de Beheerder van het Bedrijf.

Om tijd tijdens hun eerste orde te besparen, kan de bedrijfbeheerder elke bedrijfgebruiker eraan herinneren om het standaardbedrijf het factureren en het verschepen adres aan hun [ adresboek ](../customers/account-dashboard-address-book.md) toe te voegen.

## Bedrijfsgebruikers bewerken

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies **[!UICONTROL Company Users]** in het linkerdeelvenster.

1. Hiermee zoekt u de gebruikersrecord die moet worden bijgewerkt en klikt u op **[!UICONTROL Edit]** .

1. Hiermee brengt u de benodigde wijzigingen aan.

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

## Een bedrijfsgebruiker verwijderen

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies **[!UICONTROL Company Structure]** in het linkerdeelvenster.

1. Selecteert de bedrijfgebruiker in de bedrijfstructuur.

1. Klik op **[!UICONTROL Delete Selected]** .

   ![ Schrap Gebruiker ](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Delete]** wanneer u wordt gevraagd om te bevestigen.

In Admin, blijft de bedrijfgebruiker vermeld in het [ netwerk van Klanten ](../customers/customers-all.md), maar met een `Inactive` status.

## Veldomschrijvingen

| Veld | Beschrijving |
|--------------|---------------|
| [!UICONTROL Job Title] | De functie van de bedrijfgebruiker. |
| [!UICONTROL User Role] | De [ rol ](account-company-roles-permissions.md) die aan de bedrijfgebruiker wordt toegewezen. Opties: `Default User` / (andere rollen) |
| [!UICONTROL First Name] | De voornaam van de bedrijfgebruiker. |
| [!UICONTROL Last Name] | De achternaam van de bedrijfgebruiker. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfgebruiker. |
| [!UICONTROL Phone Number] | Het telefoonnummer van de bedrijfgebruiker. |
| [!UICONTROL Status] | De status van de bedrijfsgebruikersaccount. Opties: `Active` / `Inactive` |

{style="table-layout:auto"}
