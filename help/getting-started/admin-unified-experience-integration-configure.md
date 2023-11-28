---
title: Vorm de Integratie van het Experience Cloud voor Admin van de Handel
description: Leer hoe te om een project van de Handel te vormen om beheerdertoegang door Experience Cloud toe te laten.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 0%

---

# Vorm de Integratie van het Experience Cloud met Commerce Admin

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Ga aan de slag met de integratie van het Experience Cloud met Commerce Admin door de toepassing van de Handel te vormen om de Commerce te gebruiken Admin verenigde de uitbreidingen van de Gebeurtenissen van de Ervaring en van de Handel.


## Vereisten

- Adobe Commerce moet zijn geconfigureerd voor gebruik [Adobe IMS-verificatie](../getting-started/adobe-ims-config.md)
- Accountprovisioning en -machtigingen—Beheerders moeten beschikken over een [Adobe bedrijfsprofiel](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) met toegang tot de volgende middelen om de integratie van het Experience Cloud te vormen:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Gebruikers- en ontwikkelaarsaccounts voor Adoben toevoegen en beheren voor de organisatie
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—De ontwikkelaar of de toegang van de systeembeheerder om de projecten van de Bouwer van de App tot stand te brengen en de verbindingsgeloofsbrieven en de projectconfiguratie te produceren om de dienst van de Gebeurtenissen van Adobe I/O te gebruiken
   - [Handel in infrastructuurprojecten in de cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—Vereiste modules installeren en de Commerce-toepassingsserver configureren met behulp van de Adobe Commerce CLI
   - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Update store configuration en beheer de gebruikersrekeningen van de Handel

## Overzicht van configuratie

Schakel de integratie in door de volgende taken uit te voeren:

1. [Controleer de omgeving en de toepassingsconfiguratie van de Handel](#check-the-commerce-environment-and-application-configuration).

1. [De extensie Commerce Admin Unified Experience inschakelen](#enable-the-commerce-admin-unified-experience-extension).

1. [Adobe I/O-gebeurtenissen instellen voor handel](#set-up-adobe-io-events).

1. [Integratie testen](#test-the-integration).

## Controleer de omgeving en de toepassingsconfiguratie van de Handel

Alvorens de integratie van het Experience Cloud te vormen, verifieer dat uw project en toepassing van de Handel aan de vereisten voldoen.

1. Voor uw lokale werkstation, verandering in de projectfolder voor uw project van de Handel.

1. Bekijk de omgevingsvertakking voor de instantie die u met het Experience Cloud wilt integreren.

1. Controleer of Adobe IMS is ingeschakeld.

   - Gebruik de [URL voor SSH-toegang](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) voor de omgeving verbinding maken met de Commerce-toepassingsserver.

   - Gebruik vanuit de opdrachtregel de Adobe Commerce CLI om de status van de IMS-module te controleren.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Als de module niet is ingeschakeld, [het gebruiken van de Organisatie en geloofsbrieven voor het IMS integratieproject toelaten](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module). Als u niet over de geloofsbrieven beschikt, [een ondersteuningsticket voor Adobe indienen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

1. Controleer of de Admin-gebruiker zich met de Adobe ID kan aanmelden bij de Commerce Admin.

   - Ga naar Admin URL van de Handel.

   - Als u bent aangemeld, meldt u zich af.

   - Zorg ervoor dat de Admin-gebruiker opnieuw wordt omgeleid om zich aan te melden met behulp van zijn Adobe ID.

     ![Adobe Commerce aanmelden met Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Van de folder van het wolkenproject op uw lokale werkstation, verifieer dat de Handel Admin Verenigde uitbreiding van de Ervaring geïnstalleerd is.

   ```bash
   composer show *unified-experience*
   ```

   Als de extensie is geïnstalleerd, retourneert Composer de naam en beschrijving van de extensie.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Als de extensie niet is geïnstalleerd, installeert u deze met Composer. Breng vervolgens de wijzigingen aan en implementeer de cloudomgeving opnieuw.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Gecombineerde ervaring voor Admin Commerce inschakelen

Laat Admin van de Handel toe verenigde de uitbreiding van de Ervaring, en login dan door Experience Cloud.

>[!NOTE]
>
>Deze instructies tonen hoe een Commerce Cloud projectbeheerder de uitbreiding kan toelaten gebruikend Adobe Commerce CLI. De Admin van de handel gebruikers kunnen de uitbreiding ook toelaten door het bijwerken van [Configuratieinstellingen van de Commerce Store](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Van de wortelfolder van uw het projectmilieu van de Wolk op uw lokale werkstation, gebruik [magento-cloud, CLI-gereedschap](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) aan login aan de de toepassingsserver van de Handel.

   ```bash
   magento-cloud ssh
   ```

1. De optie `magento/module-unified-experience` extensie met Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Wis de cache.

   ```bash
   bin/magento cache:clean
   ```

## Adobe I/O-gebeurtenissen instellen voor handel

Wanneer de integratie van het Experience Cloud wordt toegelaten, verzendt de dienst van de Gebeurtenissen van Adobe I/O de Handel gebeurtenisgegevens naar Experience Cloud om beheerdertoegang tot de projecten van de Handel te beheren. De dienst die opstelling vereist het toelaten van de Gebeurtenissen van de Adobe I/O voor de uitbreiding van de Handel (`magento/commerce-eventing`) en het configureren van de service Adobe I/O Events in Admin.

### Commerce-gebeurtenissen inschakelen

De extensie Commerce Events inschakelen (`magento/commerce-eventing`) om gegevens van de douanegebeurtenis van de toepassing van de Handel naar de dienst van de Gebeurtenissen van Adobe I/O te verzenden.

>[!NOTE]
>
>Voor Handel 2.4.6 en later, wordt de uitbreiding van de Gebeurtenissen van de Handel geïnstalleerd door gebrek. Voor handelsprojecten met Commerce 2.4.5: gebruik Composer eerst om [de extensie installeren](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)en schakel het vervolgens in.

1. Van uw lokale milieu van de het projectontwikkeling van de Handel, voeg de volgende configuratie aan toe `.magento.env.yaml` bestand.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. De bijgewerkte versie toevoegen, toewijzen en implementeren `.magento.env.yaml file` naar de cloud-omgeving.

>[!TIP]
>
>Voor meer informatie over het configureren en beheren van omgevingsvariabelen met de functie `.magento.env.yaml` bestand, zie [Omgevingsvariabelen voor implementatie configureren](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### De integratie van Commerce Events configureren

Vorm de integratie van de Gebeurtenissen van de Handel door de volgende taken te voltooien. Zie voor gedetailleerde instructies [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/) ontwikkelaarsdocumentatie.

1. [Een App Builder-project maken](https://developer.adobe.com/commerce/extensibility/events/project-setup/) om gebeurtenisgegevens van de instantie van de Handel te ontvangen.

   U hebt geloofsbrieven en configuratiegegevens van het project App Builder nodig om de integratie in Commerce Admin te vormen.

1. Configureer Adobe Commerce om Adobe I/O-gebeurtenissen te gebruiken.

   - [Werk de montages van de Configuratie van de Opslag voor de dienst van de Gebeurtenissen van Adobe I/O bij](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Een gebeurtenisprovider configureren om gebeurtenissen Commerce te verzenden](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Werk het project App Builder bij om gebeurtenisgegevens van de instantie van de Handel te ontvangen](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Registreer of onderteken niet aan gebeurtenissen van de instantie van de Handel. De gebeurtenisregistratie wordt geduwd aan het project App Builder wanneer u de gebeurtenisleverancier voor de toepassing van de Handel vormt.

   Na het verbinden van de gebeurtenisleverancier aan het project App Builder, onderteken aan `observer.uex_commerce_instance_update` en slaat de wijzigingen op.

1. Om de verbinding tot stand te brengen, verzend een gebeurtenis door de gebeurtenisleverancier aan de consument.

   - Van de bevellijn in de lokale folder van het wolkenproject, [gebruik SSH om met de de toepassingsserver van de Handel te verbinden](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Verzend gebeurtenisgegevens door de status van de Admin Verenigde uitbreiding van de Ervaring te controleren gebruikend Adobe Commerce CLI.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Integratie testen

Verifieer dat een Beheerder van de Handel login aan Experience Cloud kan om beschikbare projecten van de Handel te bekijken en tot Admin en Storefront voor elk project toegang te hebben.

1. [Aanmelden bij Experience Cloud](https://experiencecloud.adobe.com/library) het gebruik van de Adobe ID en de organisatie die bij de instantie Commerce horen.

   ![De projecten van de Handel van de toegang van de homepage van de Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Beschikbare Commerce-projecten weergeven door **[!UICONTROL Commerce]**.

   ![Werkruimte voor handelsprojecten voor Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Open de beheerder voor een instantie door **[!UICONTROL Open]**.

   ![De Admin van de handel mening met toegelaten Experience Cloud integratie](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Controleer of u de beheertaken naar behoren kunt uitvoeren.

   Workflows in de Commerce Admin moeten hetzelfde proces volgen. Als u werkstroomwijzigingen of fouten ervaart nadat u de integratie van het Experience Cloud hebt ingeschakeld, neemt u contact op met de systeembeheerder of [een ondersteuningsticket voor Adobe indienen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Nadat u de integratie van het Experience Cloud vormt, verifieer dat de beheerderrekeningen correct zijn provisioned om tot de projecten van de Handel door Experience Cloud toegang te hebben. Zie [Admin-gebruikers beheren](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
