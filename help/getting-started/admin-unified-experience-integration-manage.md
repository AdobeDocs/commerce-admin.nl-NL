---
title: De integratie van Experiencen Cloud beheren
description: Leer hoe u de integratie van Experiencen Cloud kunt beheren en problemen kunt oplossen
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# De integratie van Experiencen Cloud beheren

Na aanvankelijke enablement, beheer de status van de Experience Cloud integratie door de Handel toe te laten of onbruikbaar te maken Admin Verenigde uitbreiding van de Ervaring.

- Als Admin van de Handel verenigde de uitbreiding van de Ervaring wordt toegelaten en de beheerderrekeningen zijn [correct geleverd](#manage-admin-user-accounts), kunnen de beheerders van de Handel beschikbare projecten van de Handel van Adobe Experience Cloud bekijken en toegang hebben. De beheerders kunnen tot individuele projecten nog toegang hebben gebruikend Admin URL voor het het projectmilieu van de Handel.

- Als de Commerce Admin Verenigde Uitbreiding van de Ervaring wordt onbruikbaar gemaakt, is de toegang door Experience Cloud gehandicapt. De beheerders moeten login aan individuele projecten gebruikend Admin URL voor het het projectmilieu van de Handel.

>[!WARNING]
>
>Als de Adobe Identity Management Service (IMS)-integratie is uitgeschakeld, wordt het Experience Cloud automatisch geïntegreerd.

## De integratie beheren vanuit de beheerder

1. Open het menu Opslagconfiguratie in Beheer handel door **[!UICONTROL Stores]** in het navigatiemenu aan de linkerkant en selecteer **[!UICONTROL Configuration]**.

1. Selecteer in het menu Configuratie de optie **[!UICONTROL Advanced > Admin]** en breid vervolgens de **[!UICONTROL Unified Experience option]**.

   ![Admin Store Configuration for Experience Cloud integration](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Schakel de integratie in of uit door de **[!UICONTROL Enable]** waarde.

1. Wijzig de projectnaam die in de werkruimte van de Projecten van de Handel door wordt getoond of bij te werken **[!UICONTROL Project Name]** waarde.

1. Sla de configuratie op.

1. Wis de cache.

## Integratie beheren met de Adobe Commerce CLI

Systeembeheerders van de handel met Admin toegang tot het de wolkenproject van de Handel kan Adobe Commerce CLI bevelen gebruiken om de integratie van het Experience Cloud te beheren.

1. Meld u vanuit uw lokale ontwikkelomgeving aan bij het cloudproject.

   ```bash
   magento-cloud login
   ```

1. Van de wortelfolder van uw het projectmilieu van de Wolk, verbind met de de toepassingsserver van de Handel.

   ```bash
   ssh magento-cloud
   ```

1. Controleer de status van de Admin Unified Experience-extensie:

   ```bash
   bin/magento admin:uex:status
   ```

1. De status van de extensie wijzigen om de integratie uit te schakelen

   - **Inschakelen**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Uitschakelen**—`bin/magento config:set admin/unified_experience/enabled 0`

## Beheerdersaccounts beheren

Alle Admin van de Handel gebruikers moeten zowel een Admin rekening op de instantie van de Handel als een gebruikersrekening van de Adobe (Adobe ID) hebben om tot de producten en de diensten van de Adobe toegang te hebben. Beide accounts moeten aan hetzelfde e-mailadres zijn gekoppeld.

- **Commerce Admin-account**—[Admin-gebruikers voor handel beheren](../systems/permissions-users-all.md) van Admin voor de instantie van de Handel. De rekeningen van de gebruiker voor de beheerders van de Handel moeten de rol Admin worden toegewezen.

  De beheerders van het systeem op het project van de Handel kunnen gebruiken [SSH voor verbinding met de externe omgeving](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)en gebruik de Commerce CLI `admin:user:create` en `admin:user:unlock` opdrachten om Admin-gebruikersaccounts toe te voegen of te ontgrendelen.

- **Gebruikersaccount Adoben**—Een beheerder voor de organisatie van de Adobe verbonden aan de instantie van de Handel moet login aan Adobe Admin Console en Adobe ID voor elke beheerder van de Handel aan de organisatie toevoegen. Vervolgens moeten zij productrechten en machtigingen toewijzen om toegang te krijgen tot de toepassing Commerce. Zie [Adobe Commerce-gebruikers configureren in de Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Beheerders die de configuratie voor de integratie van Experiencen Cloud vanuit de Adobe Developer-console beheren, moeten een gebruikersaccount voor Adobe hebben bij System Administrator of Developer Access.

>[!NOTE]
>
>Een Adobe ID is een account die via Adobe is gemaakt en die vereist is voor toegang tot producten en services via Experience Cloud. Commerce-beheerders zonder Adobe ID kunnen [een gratis account maken](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) met hetzelfde e-mailadres dat ze gebruiken om zich aan te melden bij Commerce Admin.
