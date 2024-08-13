---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Security] &gt; [!UICONTROL 2FA] van Commerce Admin.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Opslagruimten die verificatie voor Adobe Identity Management Services (IMS) hebben ingeschakeld, hebben native Adobe Commerce en Magento Open Source tweefelige verificatie (2FA) uitgeschakeld. Admin-gebruikers die zich bij hun Adobe Commerce-instantie hebben aangemeld met hun aanmeldingsgegevens voor de Adobe, hoeven niet opnieuw te worden geverifieerd voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [ Integrating Adobe Commerce met het overzicht van Adobe IMS ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Voor meer informatie over het veranderen van deze montages, zie [ dubbel-factor authentificatie (2FA) ](../../systems/security-two-factor-authentication.md) in de _Gids van Systemen Admin_.

## [!UICONTROL General]

![ Algemeen ](./assets/2fa-general.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Algemeen | Wijst op de twee-factor authentificatiemethodes die u vereist. Als u meer dan één leverancier selecteert, wordt elke gebruiker vereist om elke methode te vormen 2FA de volgende tijd zij login. |
| [!UICONTROL Configuration Email URL for Web API] | Algemeen | Voor douaneimplementaties, URL voor een afwisselende verbinding van de e-mailconfiguratie die naar _Admin_ gebruikers bij eerste login wordt verzonden. In het e-mailmalplaatje, gebruik placeholder `:tfat` om erop te wijzen waar het teken wordt ingespoten. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Algemeen | Hiermee bepaalt u hoe vaak een beheerder een [!DNL one-time password (OTP)] kan invoeren voordat zijn of haar account tijdelijk is uitgeschakeld. Standaard: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Algemeen | Hiermee bepaalt u hoe lang (in seconden) een beheerder kan wachten om een [!DNL one-time password (OTP)] in te voeren voordat zijn account tijdelijk is uitgeschakeld. Standaard: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![ Google ](./assets/2fa-google.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Algemeen | Hiermee bepaalt u hoe lang (in seconden) het systeem de beheerder [!DNL one-time-password (OTP)] accepteert nadat deze is verlopen. Kan niet hoger zijn dan het leven van één enkele OTP (gewoonlijk 30 seconden). Standaard: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![ Duo Veiligheid ](./assets/2fa-duo-security.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Algemeen | De integratietoets van uw [!DNL Duo Security] -account. |
| [!UICONTROL Secret Key] | Algemeen | De geheime sleutel van uw [!DNL Duo Security] account. |
| [!UICONTROL API Hostname] | Algemeen | De API-hostnaam van uw [!DNL Duo Security] -account. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![ Authy ](./assets/2fa-authy.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL API Key] | Algemeen | De API-sleutel van uw [!DNL Authy] -account. |
| [!UICONTROL OneTouch Message] | Algemeen | Het bericht dat bij het aanmelden in de [!DNL Authy] -verificator wordt weergegeven. Standaard: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![ Sleutel U2F ](./assets/2fa-u2f-key.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Algemeen | Het domein dat wordt gebruikt om [!DNL WebAuthn] uitdagingen voor douaneimplementaties uit te geven en te verwerken WebAPI. |

{style="table-layout:auto"}
