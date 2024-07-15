---
title: Bedrijfsrollen en -machtigingen
description: Leer over rollen en toestemmingen die een bedrijfbeheerder op bedrijfgebruikers kan toepassen, die voor diverse niveaus toegang tot ordeinformatie en middelen toestaan.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Bedrijfrollen en -machtigingen

De rollen voor bedrijfgebruikers worden opstelling met diverse niveaus van toestemming om tot verkoopinformatie en middelen toegang te hebben. Door gebrek, is de bedrijfbeheerder a _super gebruiker_ met volledige toestemmingen. De [ Ontkende Toegang ](../content-design/pages.md#access-denied) pagina verschijnt als de gebruiker geen toestemming heeft om tot de pagina toegang te hebben.

![ Rollen en de pagina van Toestemmingen met standaardrol ](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Het systeem heeft één vooraf bepaalde rol van de Gebruiker Standaard, die u _kunt gebruiken zoals_ is of zich wijzigt om uw behoeften aan te passen. U kunt zo vele rollen tot stand brengen zonodig om uw bedrijfsstructuur en organisatorische verantwoordelijkheden, zoals het volgende aan te passen:

- **StandaardGebruiker** - de standaardgebruiker heeft volledige toegang tot activiteiten met betrekking tot verkoop en citaten, en mening-slechts toegang tot bedrijfsprofiel en kredietinformatie.

- **Hogere Koper** — Een hogere koper zou toegang tot alle Verkoop en Citaten middelen, en mening-slechts toestemmingen aan het Profiel van het Bedrijf, Gebruiker en Teams, de Informatie van de Betaling, en het Krediet van het Bedrijf kunnen hebben.

- **HulpKoper** - een hulpkoper zou toestemming kunnen hebben om een orde te plaatsen gebruikend _Afhandeling met Citaat_, en om orden, citaten, en informatie in het bedrijfsprofiel te bekijken.

## Rollen en machtigingen beheren

1. De bedrijfbeheerder ondertekent binnen aan hun opslagrekening.

1. Kies **[!UICONTROL Roles and Permissions]** in het linkerdeelvenster.

1. Hiermee kunt u een van de volgende taken uitvoeren.

### Een rol maken

1. Klik op **[!UICONTROL Add New Role]** .

   ![ voeg Nieuwe Rol ](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"} toe

1. Hiermee wordt een beschrijvende waarde **[!UICONTROL Role Name]** ingevoerd.

1. Voer onder _[!UICONTROL Role Permissions]_een van de volgende handelingen uit:

   - Selecteert checkbox van elk middel of activiteit dat de gebruikers de rol toewezen toestemming hebben om tot toegang te hebben.

   - Selecteert checkbox **[!UICONTROL All]** en ontruimt checkbox van elke middel of activiteit dat de gebruikers aan de rol toegewezen geen toestemming hebben om toegang te hebben.

1. Klik op **[!UICONTROL Save Role]** .

1. Hiermee maakt u zoveel rollen als nodig zijn door deze stappen te herhalen.

### Een rol wijzigen

1. De bedrijfsbeheerder klikt op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Actions]_om de rol te wijzigen.

1. Hiermee wijzigt u de benodigde naam- en machtigingsinstellingen.

1. Klik op **[!UICONTROL Save Role]** wanneer dit is voltooid.

### Een rol dupliceren

1. De bedrijfsbeheerder klikt op **[!UICONTROL Duplicate]** in de kolom _[!UICONTROL Actions]_om de rol te dupliceren.

1. Hiermee wijzigt u de benodigde naam- en machtigingsinstellingen.

1. Klik op **[!UICONTROL Save Role]** wanneer dit is voltooid.

### Een rol verwijderen

1. De bedrijfbeheerder vindt de rol die in de lijst van rollen moet worden geschrapt.

   Alleen rollen zonder toegewezen gebruikers kunnen worden verwijderd.

1. Klik op **[!UICONTROL Delete]** in de kolom _[!UICONTROL Actions]_.

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

## Handelingen

| Handeling | Beschrijving |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Hiermee maakt u een kopie van de geselecteerde rol. De naam van de gedupliceerde rol is `- Duplicated` aan het einde toegevoegd. |
| [!UICONTROL Edit] | Wijzig de naam en/of set machtigingen. |
| [!UICONTROL Delete] | Verwijder de rol. Alleen rollen zonder toegewezen gebruikers kunnen worden verwijderd. |

{style="table-layout:auto"}

## Rolmachtigingen

- Alles
   - Verkoop
      - Afhandeling toestaan (volgorde plaatsen)
         - De methode Betalen op account gebruiken
      - Bestellingen weergeven
         - Bestellingen van ondergeschikte gebruikers weergeven
- Aanhalingen
   - Weergave
      - Aanvragen, bewerken, verwijderen
      - Afhandeling met aanhalingsteken
      - Aanhalingstekens van onderliggende gebruikers weergeven
- Goedkeuringen bestellen
   - Mijn inkooporders bekijken
      - Weergeven voor onderliggende waarden
      - Weergeven voor alle bedrijven
   - Automatisch PO&#39;s goedkeuren die binnen deze rol zijn gemaakt
   - Aankooporders goedkeuren zonder andere goedkeuring
   - Goedkeuringsregels weergeven
      - Maken, bewerken en verwijderen
- Bedrijfsprofiel
   - Accountinformatie (Weergave)
      - Bewerken
   - Juridisch adres
      - Bewerken
   - Contacten (weergave)
   - Betalingsgegevens (Weergave)
   - Verzendgegevens (Weergave)
- Gebruikersbeheer van bedrijven
   - Rollen en machtigingen weergeven
      - Rollen en machtigingen beheren
   - Gebruikers en teams weergeven
      - Gebruikers en teams beheren
- Bedrijfskrediet
   - Weergave

## Een rol toewijzen aan een bedrijfsgebruiker

Na het bepalen van de rollen die nodig zijn, wijst de bedrijfbeheerder een rol aan elke bedrijfgebruiker toe.

1. Meld u aan bij hun bedrijfsaccount als de beheerder van het bedrijf.

1. Kies **[!UICONTROL Company Users]** in het linkerdeelvenster.

   ![ Gebruikers van het Bedrijf ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Hiermee zoekt u de gebruiker in de lijst en klikt u op **[!UICONTROL Edit]** .

1. Kies de juiste **[!UICONTROL User Role]** voor de gebruiker.

   ![ geef Gebruiker uit - kies een gebruikersrol ](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** .
