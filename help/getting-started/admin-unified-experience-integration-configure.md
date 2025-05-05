---
title: De Experience Cloud-integratie voor Commerce Admin configureren
description: Leer hoe u een Commerce-project configureert om beheerderstoegang mogelijk te maken via Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# De Experience Cloud-integratie configureren met Commerce Admin

Ga aan de slag met de Experience Cloud-integratie met Commerce Admin door de Commerce-toepassing te configureren voor gebruik van de Commerce Admin Unified Experience- en Commerce Events-extensies.


## Vereisten

- Adobe Commerce moet worden gevormd om [ authentificatie van Adobe te gebruiken IMS ](../getting-started/adobe-ims-config.md)
- De provisioning van de rekening en toestemmings-beheerders moeten een [ bedrijfsprofiel van Adobe ](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) met toegang tot de volgende middelen hebben om de integratie van Experience Cloud te vormen:
   - [ Adobe Admin Console ](https://helpx.adobe.com/enterprise/admin-guide.html) - voeg toe en beheer Adobe gebruiker en ontwikkelaarsrekeningen voor de organisatie
   - [ Adobe Developer Console ](https://developer.adobe.com/developer-console/docs/guides/getting-started/) - ontwikkelaar of systeembeheerdertoegang om de projecten van App Builder tot stand te brengen en de verbindingsgeloofsbrieven en projectconfiguratie te produceren om de dienst van Adobe I/O Events te gebruiken
   - [ Commerce op het project van de wolkeninfrastructuur ](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface) - installeer vereiste modules en vorm de de toepassingsserver van Commerce gebruikend Adobe Commerce CLI
   - [ Commerce Admin ](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html) - de opslagconfiguratie van de Update en beheert Commerce gebruikersrekeningen

## Overzicht van configuratie

Schakel de integratie in door de volgende taken uit te voeren:

1. [ controleer het milieu en de toepassingsconfiguratie van Commerce ](#check-the-commerce-environment-and-application-configuration).

1. [ laat de Commerce Admin Verenigde uitbreiding van de Ervaring ](#enable-the-commerce-admin-unified-experience-extension) toe.

1. [ Opstelling Adobe I/O Events voor Commerce ](#set-up-adobe-io-events).

1. [ Test de integratie ](#test-the-integration).

## De Commerce-omgeving en toepassingsconfiguratie controleren

Voordat u de Experience Cloud-integratie configureert, controleert u of uw project en Commerce-toepassing aan de vereisten voldoen.

1. Wijzig op uw lokale werkstation de projectmap voor uw Commerce-project.

1. Bekijk de omgevingsvertakking voor de instantie die u met Experience Cloud wilt integreren.

1. Controleer of Adobe IMS is ingeschakeld.

   - Gebruik [ de Toegang URL van SSH ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) voor het milieu om met de de toepassingsserver van Commerce te verbinden.

   - Gebruik vanuit de opdrachtregel de Adobe Commerce CLI om de status van de IMS-module te controleren.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Als de module niet wordt toegelaten, [ laat het toe gebruikend de Organisatie en geloofsbrieven voor het IMS integratieproject ](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Controleer of de Admin-gebruiker zich met Adobe ID kan aanmelden bij de Commerce Admin.

   - Ga naar de Commerce Admin URL.

   - Als u bent aangemeld, meldt u zich af.

   - Zorg ervoor dat de Admin-gebruiker opnieuw wordt omgeleid om zich aan te melden met behulp van zijn Adobe ID.

     ![ het Teken van Adobe Commerce binnen gebruikend Adobe ID ](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Van de folder van het wolkenproject op uw lokale werkstation, verifieer dat de Commerce Admin Verenigde uitbreiding van de Ervaring geïnstalleerd is.

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

## Commerce Admin Unified Experience inschakelen

Schakel de Commerce Admin Unified Experience-extensie in en meld u vervolgens aan via Experience Cloud.

>[!NOTE]
>
>Deze instructies tonen hoe een het projectbeheerder van Commerce Cloud de uitbreiding kan toelaten gebruikend Adobe Commerce CLI. De gebruikers van Admin van Commerce kunnen de uitbreiding ook toelaten door de [ montages van de de opslagconfiguratie van Commerce ](admin-unified-experience-integration-manage.md#from-the-commerce-admin) bij te werken.

1. Van de wortelfolder van uw het projectmilieu van de Wolk op uw lokale werkstation, gebruik het [ magento-wolk CLI hulpmiddel ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) aan login aan de de toepassingsserver van Commerce.

   ```bash
   magento-cloud ssh
   ```

1. De extensie `magento/module-unified-experience` inschakelen met de Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Wis de cache.

   ```bash
   bin/magento cache:clean
   ```

## Adobe I/O Events instellen voor Commerce

Wanneer de integratie van Experience Cloud is ingeschakeld, stuurt de Adobe I/O Events-service Commerce-gebeurtenisgegevens naar Experience Cloud om de beheerderstoegang tot Commerce-projecten te beheren. Voor het instellen van de service is het inschakelen van de extensie Adobe I/O Events for Commerce (`magento/commerce-eventing`) en het configureren van de Adobe I/O Events-service in de beheerfunctie vereist.

### Commerce-gebeurtenissen inschakelen

Schakel de extensie Commerce Events (`magento/commerce-eventing`) in om aangepaste gebeurtenisgegevens van de Commerce-toepassing naar de Adobe I/O Events-service te verzenden.

>[!NOTE]
>
>Voor Commerce 2.4.6 en hoger wordt de extensie Commerce Events standaard geïnstalleerd. Voor de projecten van Commerce met Commerce 2.4.5, gebruik eerst Composer om [ de uitbreiding ](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce) te installeren, dan het toe te laten.

1. Voeg vanuit uw lokale Commerce-projectontwikkelomgeving de volgende configuratie toe aan het `.magento.env.yaml` -bestand.

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

1. Voeg de bijgewerkte `.magento.env.yaml file` toe aan de cloud-omgeving, wijs deze toe en implementeer deze.

>[!TIP]
>
>Voor details bij het vormen van en het beheren van omgevingsvariabelen die het `.magento.env.yaml` dossier gebruiken, zie [ milieu variabelen voor plaatsing ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html) vormen.

### De integratie met Commerce Events configureren

Configureer de integratie met Commerce Events door de volgende taken uit te voeren. Voor gedetailleerde instructies, zie [ Adobe I/O Events voor Commerce ](https://developer.adobe.com/commerce/extensibility/events/project-setup/) ontwikkelaarsdocumentatie.

1. [ creeer een project van App Builder ](https://developer.adobe.com/commerce/extensibility/events/project-setup/) om gebeurtenisgegevens van de instantie van Commerce te ontvangen.

   U hebt geloofsbrieven en configuratiegegevens van het project van App Builder nodig om de integratie in Commerce Admin te vormen.

1. Configureer Adobe Commerce voor het gebruik van Adobe I/O Events.

   - [ werk de montages van de Configuratie van de Opslag voor de dienst van Adobe I/O Events ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce) bij.

   - [ vorm een gebeurtenisleverancier om de gebeurtenissen van Commerce ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration) te verzenden.

1. [ werk het project van App Builder bij om gebeurtenisgegevens van de instantie van Commerce ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events) te ontvangen.

   Registreer of schrijf niet in voor gebeurtenissen van het Commerce-exemplaar. De gebeurtenisregistratie wordt naar het App Builder-project geduwd wanneer u de gebeurtenisprovider voor de Commerce-toepassing configureert.

   Nadat u de gebeurtenisprovider aan het App Builder-project hebt gekoppeld, meldt u zich aan de `observer.uex_commerce_instance_update` -gebeurtenis en slaat u de wijzigingen op.

1. Om de verbinding tot stand te brengen, verzend een gebeurtenis door de gebeurtenisleverancier aan de consument.

   - Van de bevellijn in de lokale folder van het wolkenproject, [ gebruik SSH om met de de toepassingsserver van Commerce ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment) te verbinden.

     ```bash
     magento-cloud ssh
     ```

   - Verzend gebeurtenisgegevens door de status van de Admin Verenigde uitbreiding van de Ervaring te controleren gebruikend Adobe Commerce CLI.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Integratie testen

Controleer of een Commerce-beheerder zich kan aanmelden bij Experience Cloud om de beschikbare Commerce-projecten weer te geven en toegang te krijgen tot de beheerfunctie en de winkelserver voor elk project.

1. [ Teken binnen aan Experience Cloud ](https://experiencecloud.adobe.com/library) gebruikend Adobe ID en de organisatie verbonden aan de instantie van Commerce.

   ![ de projecten van Commerce van de Toegang van de homepage van Experience Cloud ](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. U kunt beschikbare Commerce-projecten weergeven door **[!UICONTROL Commerce]** te selecteren.

   ![ de werkruimte van de Projecten van Commerce voor Experience Cloud ](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Open Admin voor een instantie door **[!UICONTROL Open]** te selecteren.

   ![ Commerce Admin mening met toegelaten integratie van Experience Cloud ](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Controleer of u de beheertaken naar behoren kunt uitvoeren.

   Workflows in de Commerce-beheerder moeten hetzelfde proces volgen. Als u werkschemaveranderingen of fouten na het toelaten van de integratie van Experience Cloud ervaart, contacteer uw het systeembeheerder van Commerce of [ voorlegt een kaartje van de Steun van Adobe ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Nadat u de integratie van Experience Cloud vormt, verifieer dat de beheerderrekeningen correct provisioned zijn om tot de projecten van Commerce door Experience Cloud toegang te hebben. Zie [ Admin gebruikers beheren ](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
