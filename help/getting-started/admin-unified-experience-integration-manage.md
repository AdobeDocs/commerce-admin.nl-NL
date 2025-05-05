---
title: De Experience Cloud-integratie beheren
description: Leer hoe u de Experience Cloud-integratie kunt beheren en problemen kunt oplossen
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# De Experience Cloud-integratie beheren

Na eerste activering beheert u de status van de Experience Cloud-integratie door de Commerce Admin Unified Experience-extensie in of uit te schakelen.

- Als de Commerce Admin Verenigde Uitbreiding van de Ervaring wordt toegelaten en de beheerderrekeningen [ correct provisioned ](#manage-admin-user-accounts) zijn, kunnen de beheerders van Commerce beschikbare projecten van Commerce van Adobe Experience Cloud bekijken en toegang hebben. Beheerders hebben nog steeds toegang tot afzonderlijke projecten met de beheerdersURL voor de Commerce-projectomgeving.

- Als de Commerce Admin Unified Experience-extensie is uitgeschakeld, is de toegang via Experience Cloud uitgeschakeld. Beheerders moeten zich aanmelden bij afzonderlijke projecten met de beheerdersinterface voor de Commerce-projectomgeving.

>[!WARNING]
>
>Als de integratie met Adobe Identity Management Service (IMS) is uitgeschakeld, wordt de integratie met Experience Cloud automatisch uitgeschakeld.

## De integratie beheren vanuit de beheerder

1. Open in Commerce Admin het menu Store Configuration door **[!UICONTROL Stores]** te selecteren in het navigatiemenu links en vervolgens **[!UICONTROL Configuration]** te selecteren.

1. Selecteer **[!UICONTROL Advanced > Admin]** in het menu Configuratie en vouw vervolgens de **[!UICONTROL Unified Experience option]** uit.

   ![ Configuratie van de Winkel Admin voor de integratie van Experience Cloud ](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Schakel de integratie in of uit door de waarde **[!UICONTROL Enable]** te selecteren.

1. Wijzig de projectnaam die wordt weergegeven in de Commerce Projecten-werkruimte door de waarde **[!UICONTROL Project Name]** toe te voegen of bij te werken.

1. Sla de configuratie op.

1. Wis de cache.

## Integratie beheren met de Adobe Commerce CLI

Commerce-systeembeheerders met beheerdersrechten voor het Commerce-cloudproject kunnen Adobe Commerce CLI-opdrachten gebruiken om de Experience Cloud-integratie te beheren.

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

Alle Commerce Admin-gebruikers moeten zowel een Admin-account op het Commerce-exemplaar als een Adobe-gebruikersaccount (Adobe ID) hebben om toegang te krijgen tot Adobe-producten en -services. Beide accounts moeten aan hetzelfde e-mailadres zijn gekoppeld.

- **Commerce Admin rekening** - [ beheert Commerce Admin gebruikers ](../systems/permissions-users-all.md) van Admin voor de instantie van Commerce. Aan gebruikersaccounts voor Commerce-beheerders moet de beheerdersrol worden toegewezen.

  De beheerders van het systeem op het project van Commerce kunnen [ SSH gebruiken om met het verre milieu ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment) te verbinden, en Commerce CLI `admin:user:create` en `admin:user:unlock` bevelen te gebruiken om Admin gebruikersrekeningen toe te voegen of te ontgrendelen.

- **Adobe gebruikersrekening** - een beheerder voor de organisatie van Adobe verbonden aan de instantie van Commerce moet login aan Adobe Admin Console en Adobe ID voor elke beheerder van Commerce aan de organisatie toevoegen. Vervolgens moeten ze productrechten en machtigingen toewijzen om toegang te krijgen tot de Commerce-toepassing. Zie [ de gebruikers van Adobe Commerce in Adobe Admin Console ](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console) vormen.

Beheerders die de configuratie voor de Experience Cloud-integratie vanuit de Adobe Developer Console beheren, moeten over een Adobe-gebruikersaccount met System Administrator of Developer-toegang beschikken.

>[!NOTE]
>
>Een Adobe ID is een account die via Adobe is gemaakt en die vereist is voor toegang tot producten en services via Experience Cloud. De beheerders van Commerce die geen Adobe ID hebben kunnen [ een vrije rekening ](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) tot stand brengen gebruikend het zelfde e-mailadres zij gebruiken om binnen aan Commerce Admin te ondertekenen.
