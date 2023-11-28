---
title: Beheerdersaccounts beheren
description: Leer hoe u Admin-gebruikersaccounts maakt en rollen toewijst om beheerdersfuncties machtigingen te verlenen.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Beheerdersaccounts beheren

Wanneer uw winkel voor het eerst wordt geïnstalleerd, wordt een standaard beheerdersaccount gemaakt met aanmeldingsgegevens die u volledige beheerrechten geven. Als beste praktijken, zou u een andere gebruikersrekening met volledige toegang van de Beheerder moeten tot stand brengen. Op die manier kunt u één account gebruiken voor uw dagelijkse beheeractiviteiten en de andere reserveren als een &quot;Super Admin&quot;-account. Dit kan nuttig zijn als u uw regelmatige geloofsbrieven vergeet, of zij op één of andere manier onbruikbaar worden.

Als er anderen op uw team of dienstverleners zijn die toegang nodig hebben, kunt u een afzonderlijke gebruikersrekening voor elk tot stand brengen en beperkte toegang toewijzen die op hun bedrijfsbehoefte wordt gebaseerd om te weten. Als u de websites of winkels waartoe gebruikers toegang hebben in Admin wilt beperken, moet u eerst [een rol maken](permissions-user-roles.md) met een beperkt toepassingsgebied en alleen de noodzakelijke middelen geselecteerd. Vervolgens kunt u de rol toewijzen aan een specifieke gebruikersaccount. Admin-gebruikers die zijn toegewezen aan een beperkte rol, kunnen alleen gegevens zien en wijzigen voor websites of winkels die zijn gekoppeld aan de rol, maar kunnen geen algemene instellingen of gegevens wijzigen.

>[!NOTE]
>
>Adobe Commerce-handelaren die een Adobe ID hebben en een gestroomlijnde aanmelding bij Adobe Commerce en Adobe Business-producten willen, kunnen handelsverificatie integreren met de Adobe IMS-verificatieworkflow. Nadat deze integratie voor uw opslag van de Handel wordt toegelaten, moet elke gebruiker Admin hun geloofsbrieven van de Adobe — niet hun geloofsbrieven van de Handel — gebruiken om zich aan te melden. Zie [Adobe Identity Management Service (IMS) - Overzicht van integratie](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Voor gebruikers of rollen die tijdelijk zijn, kunt u een vervaldatum voor de gebruikersrekening ook plaatsen.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Een gebruiker maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New User]**.

   Klik op een gebruikersnaam in het raster om een bestaande gebruiker te bewerken. U kunt de _[!UICONTROL User Info]_en_[!UICONTROL User Role]_ secties.

1. In de _[!UICONTROL Account Information]_Ga als volgt te werk:

   ![Gebruikersaccountgegevens](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Voer de **[!UICONTROL User Name]** voor rekening.

     De gebruikersnaam moet gemakkelijk te onthouden zijn. Het is niet hoofdlettergevoelig. Als de gebruikersnaam bijvoorbeeld `John`, kunnen zij zich ook aanmelden als `john`.

   - Voer de volgende gegevens in:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Elk gebruikersaccount moet een uniek e-mailadres hebben.

   - Voer een **[!UICONTROL Password]** voor de rekening.

     >[!NOTE]
     >
     >Een beheerderswachtwoord moet uit minimaal zeven tekens bestaan en zowel letters als cijfers bevatten. Zie voor meer wachtwoordopties [Beveiliging van beheerder configureren](security-admin.md).

   - Voor **[!UICONTROL Password Confirmation]**, voert u het wachtwoord opnieuw in om te controleren of het correct is ingevoerd.

   - Als uw winkel meerdere talen heeft, stelt u **[!UICONTROL Interface Locale]** aan de taal die voor de interface Admin moet worden gebruikt.

1. Set **[!UICONTROL This Account is]** tot `Active`.

1. Klik op het kalenderpictogram om het **[!UICONTROL Expiration Date]** voor de gebruikersaccount.

   Het definiëren van een vervaldatum is handig wanneer een gebruiker of rol tijdelijk is. Na de vervaldatum wordt de status van de gebruikersaccount gewijzigd in `Inactive` en kan zo nodig worden bijgewerkt.

1. Onder _[!UICONTROL Current User Identity Verification]_, voer het wachtwoord voor uw gebruikersaccount in.

>[!IMPORTANT]
>
>Met de _[!UICONTROL Account Information]_-sectie voltooid, kunt u de gebruiker opslaan. De nieuwe gebruiker wordt weergegeven in het dialoogvenster_[!UICONTROL Users]_ raster, maar de gebruikersnaam kan zich pas aanmelden wanneer een rol is toegewezen.

## Een gebruikersrol toewijzen

1. Klik in het linkerdeelvenster op **[!UICONTROL User Role]**.

   In het raster worden alle bestaande gebruikersrollen weergegeven. Voor een nieuwe winkel: _[!UICONTROL Administrators]_is de enige beschikbare rol.

   ![Admin - voeg nieuwe gebruikersrol toe](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. In de _[!UICONTROL Assigned]_een gebruikersrol selecteren.

   U kunt [bestaande of aanvullende gebruikersrollen weergeven](permissions-user-roles.md). Nadat een rol is gedefinieerd, moet u de gebruikersaccount bewerken om de nieuwe rol toe te wijzen.

## 2FA-providers controleren of opnieuw instellen

1. Open de Admin-gebruikersaccount.

1. Klik in het linkerdeelvenster op **[!UICONTROL 2FA]**.

   ![Admin - voeg nieuwe gebruikersrol toe](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Controleer de 2FA-oplossingen die beschikbaar zijn voor _Beheerder_ gebruikers en adviseren elke gebruiker om de oplossingen te installeren zij alvorens zij binnen willen gebruiken.

   Verificatie door slechts één 2FA-oplossing is vereist voor aanmelding bij de _Beheerder_.

1. Als de gebruiker de 2FA-oplossing opnieuw moet installeren, kunt u de huidige 2FA-configuratie opnieuw instellen.

   Hiervoor moet de gebruiker het installatieproces herhalen voordat hij of zij zich opnieuw kan aanmelden. De gebruiker kan bijvoorbeeld een nieuwe smartphone hebben en moet Google Authenticator opnieuw installeren. Als u de huidige 2FA-instelling van de gebruiker wilt wissen, klikt u op **[!UICONTROL Reset (Provider)]** voor elke oplossing die u wilt wissen. Klik op **[!UICONTROL OK]** ter bevestiging.

   De gebruiker ontvangt een e-mail met een koppeling naar [2FA configureren](security-two-factor-authentication.md). De koppeling kan slechts eenmaal worden gebruikt. Als de gebruiker meerdere keren inlogt, wordt na elke poging een nieuwe koppeling verzonden.

1. Klik op **[!UICONTROL Save User]**.

1. Voer desgevraagd uw wachtwoord in om uw identiteit te bevestigen en klik nogmaals **[!UICONTROL Save User]**.

   De _[!UICONTROL Users]_Het raster wordt geopend en bevat een lijst met alle gebruikers.

## Een Admin-gebruiker verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Zoek de gebruikersaccount met behulp van filters boven het raster en klik op de gebruikersnaam.

1. Voer desgevraagd uw wachtwoord in om uw identiteit te bevestigen.

1. Klik in de rechterbovenhoek op **[!UICONTROL Delete User]**.

1. Klik op **[!UICONTROL OK]**.

## Wachtwoord vergeten en e-mails opnieuw instellen

De sjabloonconfiguratie voor e-mailberichten van Admin bepaalt welke e-mailberichten worden verzonden wanneer gebruikers hun wachtwoorden vergeten en opnieuw instellen. Deze configuratie specificeert het opslagcontact dat als afzender van het bericht verschijnt en hoe lang de verbinding van de wachtwoordterugwinning geldig blijft.

**_De e-mailsjablonen voor beheerders configureren:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerpaneel de optie **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Admin]**.

1. Uitbreiden ![expansietakelaar](../assets/icon-display-expand.png) de **[!UICONTROL Admin User Emails]** sectie.

   ![Geavanceerde configuratie - Sjablooninstellingen voor e-mailbeheer](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Forgot Password Email Template]** naar de sjabloon die wordt verzonden wanneer een Admin-gebruiker zijn wachtwoorden vergeet.

1. Set **[!UICONTROL Forgot and Reset Email Sender]** aan het opslagcontact dat als afzender van het bericht verschijnt.

1. Set **[!UICONTROL User Notification Template]** naar de e-mailsjabloon die wordt gebruikt als de standaardsjabloon voor beheerberichten.

1. Klik op **[!UICONTROL Save Config]**.

## Vergrendelde gebruikers

Voor de beveiliging van uw bedrijf worden gebruikersaccounts standaard vergrendeld nadat zes mislukte pogingen zijn uitgevoerd om [aanmelden](../getting-started/admin-signin.md) aan de beheerder. Alle gebruikersaccounts die momenteel zijn vergrendeld, worden weergegeven in het raster Vergrendelde gebruikers. Een account kan worden ontgrendeld door elke andere gebruiker met volledige beheerdersrechten.

Aanvullende wachtwoordbeveiligingsmaatregelen kunnen worden geïmplementeerd in de [Geavanceerd beheer](../configuration-reference/advanced/admin.md#security) configuratie. Zie [Beveiliging beheerder](security-admin.md).

![Waarschuwingsvenster voor aanmeldingsscherm - account is tijdelijk uitgeschakeld](./assets/admin-login-locked-out-message.png){width="300"}

**_Een beheerdersaccount ontgrendelen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Schakel in het raster het selectievakje van het vergrendelde account in.

   ![Machtigingen - vergrendelde gebruikersaccounts](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. In de linkerbovenhoek, plaats **[!UICONTROL Actions]** tot `Unlock`.

1. Klikken **[!UICONTROL Submit]** om de account te ontgrendelen.
