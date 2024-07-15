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

Na aanvankelijke enablement, beheer de status van de Experience Cloud integratie door de Commerce Admin Verenigde uitbreiding van de Ervaring toe te laten of onbruikbaar te maken.

- Als de Commerce Admin Verenigde Uitbreiding van de Ervaring wordt toegelaten en de beheerderrekeningen [ correct provisioned ](#manage-admin-user-accounts) zijn, kunnen de beheerders van Commerce beschikbare projecten van Commerce van Adobe Experience Cloud bekijken en toegang hebben. Beheerders hebben nog steeds toegang tot afzonderlijke projecten met de beheerdersURL voor de Commerce-projectomgeving.

- Als de Commerce Admin Unified Experience-extensie is uitgeschakeld, is de toegang via het Experience Cloud uitgeschakeld. Beheerders moeten zich aanmelden bij afzonderlijke projecten met de beheerdersinterface voor de Commerce-projectomgeving.

>[!WARNING]
>
>Als de Adobe Identity Management Service (IMS)-integratie is uitgeschakeld, wordt het Experience Cloud automatisch geïntegreerd.

## De integratie beheren vanuit de beheerder

1. Open in Commerce Admin het menu Store Configuration door **[!UICONTROL Stores]** te selecteren in het navigatiemenu links en vervolgens **[!UICONTROL Configuration]** te selecteren.

1. Selecteer **[!UICONTROL Advanced > Admin]** in het menu Configuratie en vouw vervolgens de **[!UICONTROL Unified Experience option]** uit.

   ![ Configuratie van de Winkel Admin voor de integratie van het Experience Cloud ](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Schakel de integratie in of uit door de waarde **[!UICONTROL Enable]** te selecteren.

1. Wijzig de projectnaam die wordt weergegeven in de Commerce Projecten-werkruimte door de waarde **[!UICONTROL Project Name]** toe te voegen of bij te werken.

1. Sla de configuratie op.

1. Wis de cache.

## Integratie beheren met de Adobe Commerce CLI

Commerce-systeembeheerders met beheerdersrechten voor het Commerce-cloudproject kunnen Adobe Commerce CLI-opdrachten gebruiken om de integratie van het Experience Cloud te beheren.

1. Meld u vanuit uw lokale ontwikkelomgeving aan bij het cloudproject.

   ```bash
   magento-cloud login
   ```

1. Maak verbinding met de Commerce-toepassingsserver vanuit de hoofdmap van uw Cloud-projectomgeving.

   ```bash
   ssh magento-cloud
   ```

1. Controleer de status van de Admin Unified Experience-extensie:

   ```bash
   bin/magento admin:uex:status
   ```

1. De status van de extensie wijzigen om de integratie uit te schakelen

   - **laat** toe—`bin/magento config:set admin/unified_experience/enabled 1`

   - **maak** onbruikbaar `bin/magento config:set admin/unified_experience/enabled 0`

## Beheerdersaccounts beheren

Alle Commerce Admin-gebruikers moeten zowel een Admin-account op het Commerce-exemplaar als een Adobe-gebruikersaccount (Adobe ID) hebben om toegang te krijgen tot producten en services van de Adobe. Beide accounts moeten aan hetzelfde e-mailadres zijn gekoppeld.

- **Commerce Admin rekening** - [ beheert Commerce Admin gebruikers ](../systems/permissions-users-all.md) van Admin voor de instantie van Commerce. Aan gebruikersaccounts voor Commerce-beheerders moet de beheerdersrol worden toegewezen.

  De beheerders van het systeem op het project van Commerce kunnen [ SSH gebruiken om met het verre milieu ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment) te verbinden, en Commerce CLI `admin:user:create` en `admin:user:unlock` bevelen te gebruiken om Admin gebruikersrekeningen toe te voegen of te ontgrendelen.

- **gebruikersrekening van de Adobe** - een beheerder voor de organisatie van de Adobe verbonden aan de instantie van Commerce moet login aan Adobe Admin Console en Adobe ID voor elke beheerder van Commerce aan de organisatie toevoegen. Vervolgens moeten ze productrechten en machtigingen toewijzen om toegang te krijgen tot de Commerce-toepassing. Zie [ de gebruikers van Adobe Commerce in Adobe Admin Console ](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console) vormen.

De beheerders die de configuratie voor de Experience Cloud integratie van Adobe Developer Console beheren moeten een gebruikersrekening van de Adobe met de toegang van de Beheerder of van de Ontwikkelaar van het Systeem hebben.

>[!NOTE]
>
>Een Adobe ID is een account die via Adobe is gemaakt en die vereist is voor toegang tot producten en services via Experience Cloud. De beheerders van Commerce die geen Adobe ID hebben kunnen [ een vrije rekening ](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) tot stand brengen gebruikend het zelfde e-mailadres zij gebruiken om binnen aan Commerce Admin te ondertekenen.
