---
title: 2-factor verificatie (2FA)
description: Meer informatie over ondersteuning voor verificatie met twee factoren voor de beveiliging van uw winkel en gegevens.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# 2-factor verificatie (2FA)

De handel _Beheerder_ voor uw Adobe Commerce- of Magento Open Source-installatie toegang biedt tot uw winkel, bestellingen en klantgegevens. Om ongeoorloofde toegang tot uw gegevens te voorkomen, proberen alle gebruikers zich aan te melden bij de _Beheerder_ moet een verificatieproces voltooien om hun identiteit te verifiëren.

>[!NOTE]
>
>Deze implementatie van tweefasenauthenticatie (2FA) geldt voor de _Beheerder_ alleen, en is niet beschikbaar voor klantenaccounts. De twee-factor authentificatie die uw rekening van de Handel beschermt heeft een afzonderlijke opstelling. Ga voor meer informatie naar [Je Commerce-account beveiligen](../getting-started/commerce-account-secure.md).

Verificatie met twee factoren wordt op grote schaal gebruikt en het is gebruikelijk om toegangscodes te genereren voor verschillende websites op dezelfde app. Dit zorgt ervoor dat alleen u zich kunt aanmelden bij uw gebruikersaccount. Als je je wachtwoord verliest of als een bot het vermoedt, voegt tweeledige verificatie een extra beveiligingslaag toe. U kunt bijvoorbeeld Google Authenticator gebruiken om codes te genereren voor de beheerder van uw winkel, uw Commerce-account en uw Google-account.

![Beveiligingsconfiguratie-iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce ondersteunt 2FA-methoden van meerdere providers. Sommige vereisen de installatie van een app die een eenmalig wachtwoord (OTP) produceert dat de gebruikers bij login ingaan om hun identiteit te verifiëren. De universele apparaten van de tweede Factor (U2F) lijken op een zeer belangrijk fob en produceren een unieke sleutel om identiteit te verifiëren. Andere apparaten verifiëren identiteit wanneer zij in een haven van USB worden opgenomen. Als opslagbeheerder, kunt u één of meerdere beschikbare methodes vereisen 2FA om gebruikersidentiteit te verifiëren. Uw 2FA-configuratie is van toepassing op alle websites en winkels die aan de Adobe Commerce-installatie zijn gekoppeld.

De eerste keer dat een gebruiker zich aanmeldt bij de _Beheerder_ moeten zij elk [2FA](../configuration-reference/security/2fa.md) methode die u nodig hebt, en hun identiteit verifiëren met de bijbehorende app of het bijbehorende apparaat. Na deze aanvankelijke opstelling, moet de gebruiker met één van de gevormde methodes voor authentiek verklaren telkens zij binnen ondertekenen. De 2FA-gegevens van elke gebruiker worden vastgelegd in hun _Beheerder_ en kan [reset](security-two-factor-authentication-manage.md) indien nodig. Ga voor meer informatie over het aanmeldingsproces naar [_Beheerder_ Aanmelden](../getting-started/admin-signin.md).

>[!NOTE]
>
>Voor opslagruimten die verificatie voor Adobe Identity Management Services (IMS) hebben ingeschakeld, zijn de native Adobe Commerce en Magento Open Source 2FA uitgeschakeld. De gebruikers Admin die in hun instantie van de Handel met hun geloofsbrieven van de Adobe worden geregistreerd hoeven niet voor vele Admin taken opnieuw voor authentiek te verklaren. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [Adobe Identity Management Service (IMS) - Overzicht van integratie](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

U kunt dit bekijken [videodemo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) voor een overzicht van tweeledige verificatie in de Admin.

## Uw vereiste 2FA-providers configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Security]** en kiest u **[!UICONTROL 2FA]**.

1. In de _[!UICONTROL General]_sectie, selecteert elk **[!UICONTROL Provider to use]**.

   | Provider | -functie |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Hiermee genereert u een eenmalig wachtwoord voor gebruikersverificatie in de toepassing. |
   | [!UICONTROL Duo Security] | Verstrekt SMS en dupbericht. |
   | [!UICONTROL Authy] | Genereert een tijd-afhankelijke zes-cijfercode en levert SMS of Vraag 2FA van de Stem bescherming of teken. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Gebruikt een fysiek apparaat voor verificatie, zoals [[!DNL YubiKey]](https://www.yubico.com/). |

   Houd Ctrl (PC) of Command (Mac) ingedrukt en klik op elk item om meerdere methoden te selecteren.

1. Vul de instellingen voor elke vereiste 2FA-methode in.

   ![Beveiligingsconfiguratie - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

   De eerste keer dat gebruikers zich aanmelden bij de _Beheerder_ moeten zij elke vereiste 2FA-methode instellen. Na deze aanvankelijke opstelling, moeten zij met één van de gevormde methodes voor authentiek verklaren telkens zij binnen ondertekenen.

## Instellingen 2FA-provider

Voer de instellingen in voor elke 2FA-methode die u nodig hebt.

### Google

Om te veranderen hoe lang het eenmalige wachtwoord (OTP) tijdens login beschikbaar is, ontruim **[!UICONTROL Use system value]** selectievakje. Voer vervolgens het aantal seconden in dat u de **[!UICONTROL OTP Window]** geldig zijn.

![Beveiligingsconfiguratie - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

### [!DNL Duo Security]

Voer de volgende gegevens in van uw Duo Security-account:

- Integratiesleutel
- Geheime sleutel
- API-hostnaam

![Beveiligingsconfiguratie - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Voer de API-sleutel in vanuit uw [!DNL Authy] account.

1. Als u het standaardbericht wilt wijzigen dat tijdens de verificatie wordt weergegeven, wist u het **[!UICONTROL Use system value]** selectievakje. Voer vervolgens de **[!UICONTROL OneTouch Message]** die u wilt weergeven.

   ![Beveiligingsconfiguratie - Authentieke](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F-apparaten ([!DNL Yubikey] en andere)

Het opslagdomein wordt standaard gebruikt tijdens het verificatieproces. Als u een aangepast domein wilt gebruiken voor verificatieproblemen, wist u het **[!UICONTROL Use system value]** selectievakje. Voer vervolgens de **[!UICONTROL WebAPi Challenge Domain]**.

![Beveiligingsconfiguratie - U2F-apparaten](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
