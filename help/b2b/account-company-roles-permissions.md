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

De rollen voor bedrijfgebruikers worden opstelling met diverse niveaus van toestemming om tot verkoopinformatie en middelen toegang te hebben. Standaard is de bedrijfsbeheerder een _supergebruiker_ met volledige machtigingen. De [Toegang geweigerd](../content-design/pages.md#access-denied) wordt weergegeven als de gebruiker geen machtigingen heeft om de pagina te openen.

![Pagina Rollen en machtigingen met standaardrol](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Het systeem heeft een vooraf gedefinieerde standaardgebruikersrol, die u kunt gebruiken _ongewijzigd_ of worden aangepast aan uw behoeften. U kunt zo vele rollen tot stand brengen zonodig om uw bedrijfsstructuur en organisatorische verantwoordelijkheden, zoals het volgende aan te passen:

- **Standaardgebruiker** — De standaardgebruiker heeft volledige toegang tot activiteiten met betrekking tot verkoop en prijsopgaven, en bekijk-slechts toegang tot bedrijfsprofiel en kredietinformatie.

- **Senior koper** — Een senior koper heeft mogelijk toegang tot alle bronnen van Verkoop en Aanhalingstekens, en machtigingen voor alleen weergave voor het profiel van het bedrijf, gebruikers en teams, betalingsgegevens en bedrijfskrediet.

- **Assistent-koper** — Een assistent-koper kan toestemming hebben om een bestelling te plaatsen met _Afhandeling met offerte_ en om bestellingen, aanhalingstekens en informatie weer te geven in het bedrijfsprofiel.

## Rollen en machtigingen beheren

1. De bedrijfbeheerder ondertekent binnen aan hun opslagrekening.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Roles and Permissions]**.

1. Hiermee kunt u een van de volgende taken uitvoeren.

### Een rol maken

1. Klikken **[!UICONTROL Add New Role]**.

   ![Nieuwe rol toevoegen](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Hiermee wordt een beschrijvende waarde ingevoerd **[!UICONTROL Role Name]**.

1. Onder _[!UICONTROL Role Permissions]_, voert een van de volgende handelingen uit:

   - Selecteert checkbox van elk middel of activiteit dat de gebruikers de rol toewezen toestemming hebben om tot toegang te hebben.

   - Hiermee selecteert u de **[!UICONTROL All]** checkbox en ontruimt checkbox van elk middel of activiteit dat de gebruikers aan de rol toegewezen geen toestemming hebben om toegang te hebben.

1. Klikken **[!UICONTROL Save Role]**.

1. Hiermee maakt u zoveel rollen als nodig zijn door deze stappen te herhalen.

### Een rol wijzigen

1. Voor de te wijzigen rol, klikt de bedrijfbeheerder **[!UICONTROL Edit]** in de _[!UICONTROL Actions]_kolom.

1. Hiermee wijzigt u de benodigde naam- en machtigingsinstellingen.

1. Na voltooiing klikt u op **[!UICONTROL Save Role]**.

### Een rol dupliceren

1. Voor de te dupliceren rol klikt de bedrijfbeheerder **[!UICONTROL Duplicate]** in de _[!UICONTROL Actions]_kolom.

1. Hiermee wijzigt u de benodigde naam- en machtigingsinstellingen.

1. Na voltooiing klikt u op **[!UICONTROL Save Role]**.

### Een rol verwijderen

1. De bedrijfbeheerder vindt de rol die in de lijst van rollen moet worden geschrapt.

   Alleen rollen zonder toegewezen gebruikers kunnen worden verwijderd.

1. Klikken **[!UICONTROL Delete]** in de _[!UICONTROL Actions]_kolom.

1. Wanneer ertoe aangezet om te bevestigen, klikt **[!UICONTROL OK]**.

## Handelingen

| Handeling | Beschrijving |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Hiermee maakt u een kopie van de geselecteerde rol. De naam van de dubbele rol heeft `- Duplicated` toegevoegd aan het einde. |
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

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Company Users]**.

   ![Bedrijfsgebruikers](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Hiermee zoekt u de gebruiker in de lijst en klikt u **[!UICONTROL Edit]**.

1. Kies de passende **[!UICONTROL User Role]** voor de gebruiker.

   ![Gebruiker bewerken - kies een gebruikersrol](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Klikken **[!UICONTROL Save]**.
