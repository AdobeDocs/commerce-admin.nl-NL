---
title: Experience Manager Assets-integratie installeren en configureren
description: "Leer hoe te om te installeren en te vormen  [!DNL AEM Assets Integration for Adobe Commerce]"
feature: CMS, Media
source-git-commit: 65a4339f0f6d4e9eb280ce90d6173caf671fde0f
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# De AEM Assets Integration voor Commerce installeren en configureren

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Installeer en configureer de AEM Assets-integratie voor Commerce door de extensie toe te voegen aan de Commerce-toepassing, verbinding te maken met de Commerce SaaS-services, e Adobe I/O Events-service en verbinding te maken met de Commerce SaaS.

## Systeemvereisten

**de vereisten van de Software**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Composer: 2.x

**de vereisten van de Configuratie**

- Adobe Commerce moet worden gevormd om [ authentificatie van Adobe te gebruiken IMS ](/help/getting-started/adobe-ims-config.md).
- Account instellen en machtigingen
   - [ de beheerder van het wolkenproject van Commerce ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) - installeer vereiste uitbreidingen en vorm de de toepassingsserver van Commerce van Admin of de bevellijn
   - [ Commerce Admin ](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview) - de opslagconfiguratie van de Update en beheert Commerce gebruikersrekeningen

## Overzicht van configuratie

Schakel de integratie in door de volgende taken uit te voeren:

1. [ installeer de de integratieuitbreiding van AEM Assets (`aem-assets-integration`) ](#install-the-aem-assets-integration-extension).
1. [ vorm de Schakelaar van de Dienst van Commerce ](#configure-the-commerce-services-connector) om uw instantie van Adobe Commerce en met de diensten aan te sluiten die gegevens toelaten om tussen Adobe Commerce en AEM Assets worden overgebracht.
1. [Adobe I/O-gebeurtenissen configureren voor Commerce](#configure-adobe-io-events-for-commerce)
1. [Verificatiegegevens ophalen voor API-toegang](#get-authentication-credentials-for-api-access)

## De extensie AEM Assets Integration installeren

>[!BEGINSHADEBOX]

**Vereiste**

- Toegang [ repo.magento.com ](https://repo.magento.com/admin/dashboard) om de uitbreiding te installeren. Voor zeer belangrijke generatie en het verkrijgen van de noodzakelijke rechten, zie [ uw authentificatiesleutels ](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) krijgen. Voor wolkeninstallaties, zie [ Commerce op de Gids van de Infrastructuur van de Wolk ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Toegang tot de opdrachtregel van de Adobe Commerce-toepassingsserver.

>[!ENDSHADEBOX]

Installeer de nieuwste versie van de extensie AEM Assets Integration ( `aem-assets-integration` ) op een Adobe Commerce waarop Adobe Commerce 2.4.4 of hoger wordt uitgevoerd. De AEM Integratie van Activa wordt geleverd als composer metapakket van de {](https://repo.magento.com/admin/dashboard) bewaarplaats 0} repo.magento.com.[

>[!BEGINTABS]

>[!TAB  de infrastructuur van de Wolk ]

Gebruik deze methode om de extensie [!DNL AEM Assets Integration] voor een Commerce Cloud-instantie te installeren.

1. Schakel op uw lokale werkstation de projectmap voor uw Adobe Commerce over het infrastructuurproject voor de cloud in.

   >[!NOTE]
   >
   >Voor informatie over het beheren van het projectmilieu&#39;s van Commerce plaatselijk, zie [ het Leiden takken met CLI ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) in _Adobe Commerce op de Gids van de Gebruiker van de Infrastructuur van de Wolk_.

1. Bekijk de omgevingsvertakking die u wilt bijwerken met de Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Voeg de extensie AEM Assets Integration voor Commerce toe.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Pakketafhankelijkheden bijwerken.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Wijzigingen in de code voor de bestanden `composer.json` en `composer.lock` doorvoeren en uitvoeren.

1. Voeg de codewijzigingen voor de `composer.json` - en `composer.lock` -bestanden toe, wijs deze toe en duw ze naar de cloudomgeving.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   Het duwen van de updates stelt het [ proces van de de wolkenplaatsing van Commerce ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) in werking om de veranderingen toe te passen. Controleer de plaatsingsstatus van [ opstellen logboek ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB  op-gebouw ]

Gebruik deze methode om de extensie [!DNL AEM Assets Integration] te installeren voor een instantie op locatie.

1. Gebruik Composer om de extensie AEM Assets Integration for Commerce toe te voegen aan uw project:

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Afhankelijkheden bijwerken en de extensie installeren:

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Upgrade Adobe Commerce:

   ```shell
   bin/magento setup:upgrade
   ```

1. Cache wissen:

   ```shell
   bin/magento cache:clean
   ```

   >[!TIP]
   >
   >In sommige gevallen, vooral wanneer het opstellen aan productie, zou u gecompileerde code kunnen willen vermijden omdat het wat tijd kan vergen. Zorg ervoor dat u een back-up van het systeem maakt voordat u wijzigingen aanbrengt.

>[!ENDTABS]

## De Commerce Services Connector configureren

De Commerce Services Connector maakt gegevenssynchronisatie en communicatie mogelijk tussen de Commerce-instantie, de Asset Rule Engine Service en andere ondersteunende services.

>[!NOTE]
>
>De opstelling van de Verbinding van de Diensten van Commerce is een eenmalig proces dat wordt vereist om [ de diensten van Adobe Commerce SaaS ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices) te gebruiken. Als u de connector voor een andere service al hebt geconfigureerd, kunt u de bestaande configuratie weergeven via Commerce Admin door **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]** te selecteren.

Om gegevens tussen uw instantie van Adobe Commerce en de diensten over te brengen die de Integratie van AEM Assets toelaten, vorm de Schakelaar van de Diensten van Commerce met het volgende:

- Configureer uw Commerce-instantie met de API-sleutels voor productie en sandbox voor verificatie.
- Geef een gegevensruimte (SaaS-id) op voor beveiligde cloudopslag.
- Meld u aan bij dezelfde IMS-organisatie die u gebruikt voor toegang tot AEM Assets om de verbinding tot stand te brengen tussen uw gegevensset en de Adobe Experience Platform.

Voor gedetailleerde instructies, zie ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid) de Schakelaar van de Diensten van 0} Commerce.[

Wanneer u de Schakelaar van de Diensten van Commerce vormt, produceert het systeem het project SaaS en gegevensbestandIds. U hebt deze id&#39;s nodig tijdens het instapproces voor huurders.

![ project SaaS en gegevensruimte ids voor de integratie van AEM Assets ](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Adobe I/O-gebeurtenissen configureren voor Commerce

De integratie van AEM Assets gebruikt de dienst van de Gebeurtenissen van Adobe I/O om de gegevens van de douanegebeurtenis tussen de instantie van Commerce en Experience Cloud te verzenden. De gebeurtenisgegevens worden gebruikt om workflows voor AEM Assets-integratie te coördineren.

>[!BEGINSHADEBOX]

**Vereiste**

- Zorg ervoor dat RabbitMQ is ingeschakeld en dat u luistert naar gebeurtenissen.
   - [ Opstelling van RabbitMQ voor Adobe Commerce op gebouw ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [ Opstelling van RabbitMQ voor Adobe Commerce op wolkeninfrastructuur ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Voor gedetailleerde informatie over de Gebeurtenissen van Adobe I/O voor Commerce, zie de [ Gebeurtenissen van de Adobe I/O voor Commerce ](https://developer.adobe.com/commerce/extensibility/events/) documentatie op de plaats van Adobe Developer.

Voor het instellen moeten de volgende stappen worden uitgevoerd.

1. Schakel het Commerce Event-framework in door Adobe I/O-gebeurtenissen te configureren op de toepassingsserver en in Admin.
1. Schakel gegevenssynchronisatie tussen Adobe Commerce en AEM Assets in met de Assets Rules Engine Service API om de verbinding te configureren.
1. Schakel de AEM Assets-integratie in de beheerfunctie in.

### Commerce Event-framework inschakelen

Schakel het Commerce-gebeurtenisframework in met de instructies voor de omgeving waarin uw Commerce-project wordt geïmplementeerd.

>[!BEGINTABS]

>[!TAB  de infrastructuur van de Wolk ]

1. Schakel de service Adobe I/O Events in via het menu [!DNL Store Settings Configuration] .

   1. Van Admin, ga **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Gebeurtenissen van de Adobe I/O**.

   1. Vouw **[!UICONTROL Commerce events]** uit.

   1. Stel **[!UICONTROL Enabled]** in op `Yes` .

      ![ Adobe I/O Gebeurtenissen Commerce Admin configuratie - laat de gebeurtenissen van Commerce ](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"} toe

      >[!NOTE]
      >
      >[ laat kruin ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) toe zodat Commerce gebeurtenissen naar API eindpunten kan verzenden om mededeling en werkschema&#39;s voor de integratie te beheren.

1. Werk de configuratie van het wolkenproject bij.

   1. Voeg het `app/etc/config.php` -bestand toe aan uw werkruimte:

   ```shell
   git add app/etc/config.php
   ```

   1. Voer de opdracht `composer info magento/ece-tools` uit om uw versie van de gereedschappen te bepalen. Als de versie minder dan `2002.1.13` is, [ update aan de meest recente versie ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package).

   1. Gebeurtenis inschakelen in het `.magento.env.yaml` -bestand:

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. Pas bijgewerkte bestanden toe op de cloud-omgeving en druk ze op deze bestanden.

>[!TAB  op-gebouw ]

1. Schakel de service Adobe I/O Events in via het menu [!DNL Store Settings Configuration] .

   1. Van Admin, ga **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Gebeurtenissen van de Adobe I/O**.

   1. Vouw **[!UICONTROL Commerce events]** uit.

   1. Stel **[!UICONTROL Enabled]** in op `Yes` .

      ![ Adobe I/O Gebeurtenissen Commerce Admin configuratie - laat de gebeurtenissen van Commerce ](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"} toe

      >[!NOTE]
      >
      >[ laat kanonnen banen ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) toe zodat Commerce gebeurtenissen kan verzenden om mededeling en werkschema&#39;s tussen AEM activa en Commerce te beheren.

>[!ENDTABS]

## Verificatiegegevens ophalen voor API-toegang

Voor AEM Assets Integration for Commerce zijn OAuth-verificatiereferenties vereist om API-toegang tot de Commerce-instantie te verlenen. U hebt deze gegevens nodig om het Commerce-project te registreren bij de Assets Rule Engine-service tijdens het aan boord nemen van pachters en om API-aanvragen in te dienen voor het beheer van middelen tussen Adobe Commerce en AEM Assets.

U genereert de referenties door de integratie aan de Commerce-instantie toe te voegen en deze te activeren.

### Integratie toevoegen aan de Commerce-omgeving

1. Van Admin, ga naar **Systeem** > Uitbreidingen > **Integraties**, dan klik **Nieuwe Integratie** toevoegen.

1. Voer informatie in over de integratie.

   In de **Algemene** sectie, specificeer slechts de integratie **Naam** en **E-mail**. Gebruik de e-mail voor een Adobe IMS-account met toegang tot de organisatie waar Commerce en Experience Manager Assets zijn geïmplementeerd.

   ![ Integratie van AEM Assets voor de configuratie van Admin van Commerce ](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Verifieer uw identiteit door **te klikken bevestigt Identiteit**.

   Het systeem verifieert uw identiteit door aan Experience Cloud met uw Adobe ID voor authentiek te verklaren.

1. API-bronnen configureren.

   1. Klik in het linkerdeelvenster op **[!UICONTROL API]** .
E
   1. Selecteer de externe mediabron **[!UICONTROL Catalog > Inventory > Products > External Media]** .

   ![ Configuratie van de Integratie Admin voor API middelen ](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

### Referenties genereren

Voor de pagina van Integraties, produceer de OAuth authentificatiegeloofsbrieven door **te klikken activeer** voor de integratie van Assets. U hebt deze gegevens nodig om het Commerce-project te registreren bij de Assets Rule Engine-service en om API-aanvragen in te dienen voor het beheer van middelen tussen Adobe Commerce en AEM Assets.

1. Genereer de referenties op de pagina Integraties door op **[!UICONTROL Activate]** te klikken.

   ![ activeer de configuratie van Commerce voor de integratie van Assets ](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Sla de referenties voor de consumentensleutel en toegangstoken op voor later gebruik.

![ OAuth geloofsbrieven om API verzoeken ](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"} voor authentiek te verklaren

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt ook verificatiegegevens genereren met de Adobe Commerce API&#39;s. Voor details over dit proces en meer informatie over op OAuth-Gebaseerde authentificatie voor Adobe Commerce, zie [ op OAuth-Gebaseerde authentificatie ](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in de documentatie van Adobe Developer.
