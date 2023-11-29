---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Security] &gt; [!UICONTROL 2FA] pagina van de Commerce Admin.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Opslagruimten die verificatie voor Adobe Identity Management Services (IMS) hebben ingeschakeld, hebben native Adobe Commerce en Magento Open Source tweefelige verificatie (2FA) uitgeschakeld. Admin-gebruikers die zich bij hun Adobe Commerce-instantie hebben aangemeld met hun aanmeldingsgegevens voor de Adobe, hoeven niet opnieuw te worden geverifieerd voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [Overzicht van Adobe Commerce integreren met Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Zie voor meer informatie over het wijzigen van deze instellingen [2-factor verificatie (2FA)](../../systems/security-two-factor-authentication.md) in de _Admin Systems Guide_.

## [!UICONTROL General]

![Algemeen](./assets/2fa-general.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Algemeen | Wijst op de twee-factor authentificatiemethodes die u vereist. Als u meer dan één leverancier selecteert, wordt elke gebruiker vereist om elke methode te vormen 2FA de volgende tijd zij login. |
| [!UICONTROL Configuration Email URL for Web API] | Algemeen | Voor aangepaste implementaties, de URL voor een alternatieve e-mailconfiguratiekoppeling waarnaar wordt verzonden _Beheerder_ gebruikers bij eerste aanmelding. Gebruik de tijdelijke aanduiding in de e-mailsjabloon `:tfat` om aan te geven waar het token wordt geïnjecteerd. |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Algemeen | Het leven in seconden van elk eenmalig wachtwoord (OTP) dat door de Authenticator van Google wordt geproduceerd. Standaard: `30` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Security](./assets/2fa-duo-security.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Algemeen | De integratiesleutel van uw [!DNL Duo Security] account. |
| [!UICONTROL Secret Key] | Algemeen | De geheime sleutel van uw [!DNL Duo Security] account. |
| [!UICONTROL API Hostname] | Algemeen | De API-hostnaam van uw [!DNL Duo Security] account. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Auteur](./assets/2fa-authy.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL API Key] | Algemeen | De API-sleutel van uw [!DNL Authy] account. |
| [!UICONTROL OneTouch Message] | Algemeen | Het bericht dat wordt weergegeven in het dialoogvenster [!DNL Authy] authenticator bij aanmelden. Standaard: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F-sleutel](./assets/2fa-u2f-key.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Algemeen | Het domein dat wordt gebruikt aan kwestie en proces [!DNL WebAuthn] uitdagingen voor douaneimplementaties WebAPI. |

{style="table-layout:auto"}
