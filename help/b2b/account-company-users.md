---
title: Gebruikersaccounts van bedrijven beheren
description: Meer informatie over bedrijfsgebruikersaccounts en hoe deze werken binnen het bijbehorende bedrijfsaccount.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 9c16d7a3909598328cc42bbcbf39fc14ae6a9eb9
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Gebruikersaccounts van bedrijven beheren

Op de opslagruimte, worden de bedrijfgebruikers toegewezen door de bedrijfbeheerder, en zijn zichtbaar van de _[!UICONTROL Company Users]_pagina. Deze personen zijn doorgaans kopers met verschillende machtigingsniveaus voor toegang tot services en bronnen in de winkel.

De bedrijfbeheerder plaatst eerst omhoog de [ bedrijfstructuur ](account-company-structure.md), en voltooit dan de volgende taken, zoals nodig:

- Bedrijfgebruikers maken en gebruikers toewijzen aan teams

- Rollen en machtigingen definiëren en gebruikers toewijzen aan rollen

De gebruikers van het bedrijf kunnen slechts door de bedrijfbeheerder worden toegevoegd, worden uitgegeven, worden geïnactiveerd of worden geschrapt.

- Wanneer een gebruiker wordt verwijderd, verandert de rekeningsstatus in *inactief*, en de klant kan niet meer login aan het bedrijf. Beheerders hebben nog steeds toegang tot alle inhoud die aan de gebruiker is gekoppeld. De accountbeheerder kan de toegang herstellen door de accountstatus te wijzigen in *[!UICONTROL Active]* op de pagina [!UICONTROL Company Users] .

- Wanneer een gebruikersaccount wordt verwijderd, worden het account en de bijbehorende inhoud uit de winkel verwijderd. Deze handeling kan niet worden teruggedraaid.

## Bedrijfsgebruikers toevoegen

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies **[!UICONTROL Company Users]** in het linkerdeelvenster.

   ![ Gebruikers van het Bedrijf ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Add New User]** en voer de volgende handelingen uit:

   - Voer de **[!UICONTROL Job Title]** van de nieuwe gebruiker in.

   - Kies de juiste **[!UICONTROL User Role]** als de rollen en machtigingen zijn gedefinieerd. Anders kunnen ze later terugkeren om de rol toe te wijzen.

     ![ voeg nieuwe gebruiker ](./assets/company-structure-users-add.png){width="700" zoomable="yes"} toe

   - Voegt de gebruikersinformatie in de resterende gebieden toe:
      - **[!UICONTROL First Name]** en **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Work Phone Number]**

   De standaardwaarde voor **[!UICONTROL Status]** van de account is `Active` .

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

1. Herhaalt het proces om zo vele bedrijfgebruikers tot stand te brengen zoals nodig.

   De nieuwe gebruikers verschijnen in de lijst van de Gebruikers van het Bedrijf, samen met de Beheerder van het Bedrijf.

Om tijd tijdens hun eerste orde te besparen, kan de bedrijfbeheerder elke bedrijfgebruiker eraan herinneren om het standaardbedrijf het factureren en het verschepen adres aan hun [ adresboek ](../customers/account-dashboard-address-book.md) toe te voegen.

## Een gebruiker verwijderen uit de [!UICONTROL Company structure]

Bedrijfsbeheerders kunnen een gebruiker uit de [!UICONTROL Company Structure] verwijderen.

Nadat een rekening wordt verwijderd, verandert de status van de gebruikersrekening in *inactief*, en de gebruiker kan niet meer in de storefront registreren.
De beheerder kan een account opnieuw activeren door de gegevens van de gebruikersaccount op de pagina Bedrijfgebruikers te bewerken.

1. Vanuit de winkel ondertekent de beheerder van het bedrijf zich aan bij zijn account.

1. Kies **[!UICONTROL Company Structure]** in het linkerdeelvenster.

1. Selecteert de bedrijfgebruiker in de bedrijfstructuur.

1. Klik op **[!UICONTROL Remove from Structure]** .

   ![ Schrap Gebruiker ](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Remove]** wanneer u wordt gevraagd om te bevestigen.

   In Admin, blijft de bedrijfgebruiker vermeld in het [ netwerk van Klanten ](../customers/customers-all.md), maar met een `Inactive` status.

## Gebruikersaccounts van bedrijven weergeven en beheren

Bedrijfsbeheerders kunnen bedrijfsgebruikersaccounts weergeven en beheren met de weergavefilters op de pagina [!UICONTROL Company Users] .

![ Gebruikers van het Bedrijf ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- Selecteer **[!UICONTROL Show Inactive Users]** om alleen inactieve gebruikers weer te geven.
- Selecteer **[!UICONTROL Show Active Users]** om alleen actieve gebruikers weer te geven.
- Alle gebruikers weergeven door **[!UICONTROL Show All Users]** te selecteren.

De bedrijfsbeheerder kan een individuele account beheren met het regelitem *[!UICONTROL Actions]* om de accountgegevens te bewerken, de accountstatus te beheren of een account te verwijderen.

### Gebruikersaccountgegevens van een bedrijf bewerken

Bedrijfsbeheerders kunnen de profielgegevens van gebruikersaccounts bijwerken en de status van de account wijzigen.

1. Zoek op de pagina [!UICONTROL Company Users] naar de gebruikersaccount die u wilt bijwerken. Klik op **[!UICONTROL Edit]**.

1. Breng de vereiste wijzigingen aan in de gegevens van de gebruikersaccount, waaronder het wijzigen van de accountstatus.

1. Pas de wijzigingen toe door op **[!UICONTROL Save]** te klikken.

>[!NOTE]
>
>Als u een bedrijfsgebruikersaccount bewerkt en u ziet dat in het profiel vereiste accountgegevens ontbreken, zoals de functie en het telefoonnummer van het werk, geeft dit aan dat de account is toegevoegd door een Commerce-sitebeheerder. Deze accounts kunnen niet vanuit de opslagruimte worden bewerkt. Neem contact op met uw sitebeheerder om informatie bij te werken of de accountstatus te wijzigen.

### Een actief account deactiveren of verwijderen

1. Zoek op de pagina [!UICONTROL Company Users] naar de gebruikersaccount die u wilt bijwerken. Klik op **[!UICONTROL Manage]**.

   ![ beheert gebruiker van de pagina van de Gebruikers van het Bedrijf ](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. Schakel desgevraagd de gebruikersaccount in of verwijder deze.

>[!IMPORTANT]
>
>Als u een gebruikersaccount van een bedrijf verwijdert, worden de account en alle bijbehorende inhoud van het systeem verwijderd. Deze handeling kan niet worden teruggedraaid.

## Beschrijvingen in de velden Gebruikersaccountprofiel van het bedrijf

| Veld | Beschrijving |
|--------------------------------|---------------|
| [!UICONTROL Job Title] | De functie van de bedrijfgebruiker. |
| [!UICONTROL User Role] | De [ rol ](account-company-roles-permissions.md) die aan de bedrijfgebruiker wordt toegewezen. Opties: `Default User` / (andere rollen) |
| [!UICONTROL First Name] | De voornaam van de bedrijfgebruiker. |
| [!UICONTROL Last Name] | De achternaam van de bedrijfgebruiker. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfgebruiker. |
| [!UICONTROL Work Phone Number] | Het het werktelefoonaantal van de bedrijfgebruiker. |
| [!UICONTROL Status] | De status van de bedrijfsgebruikersaccount. Opties: `Active` / `Inactive` |

{style="table-layout:auto"}
