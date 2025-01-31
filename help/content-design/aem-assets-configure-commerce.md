---
title: De Experience Manager Assets-integratie installeren en configureren
description: Leer hoe te om  [!DNL AEM Assets Integration for Adobe Commerce]  op een instantie van Adobe Commerce te installeren en te vormen.
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: a2b9fc6584b9d8a57f24d87a9b5ebcdc2f29cbae
workflow-type: tm+mt
source-wordcount: '1387'
ht-degree: 0%

---

# De AEM Assets Integration voor Commerce installeren en configureren

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Bereid uw Commerce-omgeving voor om AEM Assets Integration voor Commerce te gebruiken door de `aem-assets-integration` PHP-extensie te installeren. Werk vervolgens de beheerconfiguratie bij om communicatie en workflows tussen Adobe Commerce en AEM Assets mogelijk te maken.

## Systeemvereisten

De AEM Assets Integration voor Commerce heeft de volgende systeem- en configuratievereisten.

**de vereisten van de Software**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Composer: 2.x

**de vereisten van de Configuratie**

- Account instellen en machtigingen:

   - [ de beheerder van het wolkenproject van Commerce ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) - installeer vereiste uitbreidingen en vorm de de toepassingsserver van Commerce van Admin of de bevellijn

   - [ Commerce Admin ](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview) - de opslagconfiguratie van de Update en beheert Commerce gebruikersrekeningen

>[!TIP]
>
> Adobe Commerce kan worden gevormd om [ authentificatie van Adobe te gebruiken IMS ](/help/getting-started/adobe-ims-config.md).

## Overzicht van configuratie

Schakel de integratie in door de volgende taken uit te voeren:

1. [ installeer de uitbreiding van de Integratie van AEM Assets (`aem-assets-integration`) ](#install-the-aem-assets-integration-extension).
1. [ vorm de Schakelaar van de Diensten van Commerce ](#configure-the-commerce-services-connector) om uw instantie van Adobe Commerce en met de diensten te verbinden die gegevens toelaten om tussen Adobe Commerce en AEM Assets worden overgebracht.
1. [Adobe I/O-gebeurtenissen configureren voor Commerce](#configure-adobe-io-events-for-commerce)
1. [Verificatiegegevens ophalen voor API-toegang](#get-authentication-credentials-for-api-access)

## De extensie AEM Assets Integration installeren

>[!BEGINSHADEBOX]

**Vereiste**

- Toegang [ repo.magento.com ](https://repo.magento.com/admin/dashboard) om de uitbreiding te installeren.

  Voor zeer belangrijke generatie en het verkrijgen van de noodzakelijke rechten, zie [ uw authentificatiesleutels ](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) krijgen. Voor wolkeninstallaties, zie [ Commerce op de Gids van de Infrastructuur van de Wolk ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Toegang tot de opdrachtregel van de Adobe Commerce-toepassingsserver.

>[!ENDSHADEBOX]

Installeer de nieuwste versie van de extensie AEM Assets Integration (`aem-assets-integration`) op een Adobe Commerce-instantie met versie Adobe Commerce 2.4.5+. De AEM Integratie van Activa wordt geleverd als composer metapakket van de {](https://repo.magento.com/admin/dashboard) bewaarplaats 0} repo.magento.com.[

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
>Wanneer het opstellen aan productie, overweeg geen gecompileerde code om tijd te besparen. Maak altijd een back-up van uw systeem voordat u wijzigingen aanbrengt.

>[!ENDTABS]

## De Commerce Services Connector configureren

De Commerce Services Connector maakt gegevenssynchronisatie en communicatie mogelijk tussen de Commerce-instantie, de Asset Rule Engine Service en andere ondersteunende services.

>[!NOTE]
>
>De opstelling van de Verbinding van de Diensten van Commerce is een eenmalig proces dat wordt vereist om [ de diensten van Adobe Commerce SaaS ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices) te gebruiken. Als u de connector voor een andere service al hebt geconfigureerd, kunt u de bestaande configuratie weergeven via Commerce Admin door **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]** te selecteren.

Om gegevens tussen uw instantie van Adobe Commerce en de diensten over te brengen die de Integratie van AEM Assets toelaten, vorm de Schakelaar van de Diensten van Commerce met het volgende:

- API-sleutels voor productie en sandbox voor verificatie.
- Stel een gegevensruimte (SaaS-id) in voor beveiligde cloudopslag.
- Geef de IMS-organisatie-id op waar uw Commerce- en AEM Assets-omgevingen zijn ingericht.

Voor gedetailleerde instructies, zie ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid) de Schakelaar van de Diensten van 0} Commerce.[

Nadat u de Verbinding van de Diensten van Commerce vormt, produceert het systeem het project SaaS en gegevensbestand IDs die het veilige milieu van de wolkenopslag voor uw Diensten van Commerce identificeren en identiteitskaarts in de configuratie Admin tonen. Deze waarden zijn vereist om het instapproces voor de synchronisatie van bedrijfsmiddelen te voltooien.

![ project SaaS en gegevensruimte ids voor de integratie van AEM Assets ](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Adobe I/O-gebeurtenissen configureren voor Commerce

De integratie van AEM Assets gebruikt de dienst van de Gebeurtenissen van Adobe I/O om de gegevens van de douanegebeurtenis tussen de instantie van Commerce en Experience Cloud te verzenden. De gebeurtenisgegevens worden gebruikt om workflows voor AEM Assets-integratie te coördineren.

>[!BEGINSHADEBOX]

**Vereiste**

- Zorg ervoor dat RabbitMQ is ingeschakeld en dat u luistert naar gebeurtenissen.
   - [ Opstelling van RabbitMQ voor Adobe Commerce op gebouw ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [ Opstelling van RabbitMQ voor Adobe Commerce op wolkeninfrastructuur ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - Verifieer dat [ gewassentaken ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) worden toegelaten. Cron-taken zijn vereist voor communicatie en workflows voor AEM Assets-integratie.

>[!NOTE]
>
> Voor projecten op versie 2.4.5 van Commerce, moet u [ de modules van Adobe I/O ](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce) installeren. In Commerce versie 2.4.6+, worden deze modules automatisch geladen. Voor de AEM Assets-integratie voor Commerce hoeft u alleen de modules te installeren. App Builder-instelling is niet vereist.

>[!ENDSHADEBOX]

### Commerce Event-framework inschakelen

Schakel het gebeurtenisframework in via Commerce Admin.

1. Van Admin, ga **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Gebeurtenissen van de Adobe I/O**.

1. Vouw **[!UICONTROL Commerce events]** uit.

1. Stel **[!UICONTROL Enabled]** in op `Yes` .

   ![ Adobe I/O Gebeurtenissen Commerce Admin configuratie - laat de gebeurtenissen van Commerce ](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"} toe

1. Voer de bedrijfsnaam van de handelaar in **[!UICONTROL Merchant ID]** en de omgevingsnaam in **[!UICONTROL Environment ID]** gebieden in. Gebruik bij het instellen van deze waarden alleen alfanumerieke tekens en onderstrepingstekens.

>[!BEGINSHADEBOX]

**vorm Douane VCL voor het blokkeren van verzoeken**

Als u een aangepast VCL-fragment gebruikt om onbekende binnenkomende aanvragen te blokkeren, moet u mogelijk de HTTP-header `X-Ims-Org-Idheader` opnemen om binnenkomende verbindingen van de AEM Assets Integration for Commerce-service toe te staan.

>[!TIP]
>
> U kunt de Fastly CDN module gebruiken om Edge ACL met een lijst van IP adressen tot stand te brengen die u wilt blokkeren.

De volgende aangepaste VCL-fragmentcode (JSON-indeling) toont een voorbeeld met een `X-Ims-Org-Id` aanvraagkoptekst.

```json
{
  "name": "blockbyuseragent",
  "dynamic": "0",
  "type": "recv",
  "priority": "5",
  "content": "if ( req.http.X-ims-org ~ \"<YOUR-IMS-ORG>\" ) {error 405 \"Not allowed\";}"
}
```

Voordat u een op dit voorbeeld gebaseerd fragment maakt, controleert u de waarden om te bepalen of u wijzigingen wilt aanbrengen:

- `name`: naam voor het VCL-fragment. In dit voorbeeld hebben we de naam `blockbyuseragent` gebruikt.

- `dynamic` : stelt de fragmentversie in. In dit voorbeeld hebben we `0` gebruikt. Zie de [ Snelle fragmenten VCL ](https://www.fastly.com/documentation/reference/api/vcl-services/snippet/) voor gedetailleerde informatie van het gegevensmodel.

- `type` - Geeft het type VCL-fragment op, dat de locatie van het fragment in de gegenereerde VCL-code bepaalt. In dit voorbeeld, gebruikten wij `recv`, zie de [ VCL fragmentverwijzing ](https://docs.fastly.com/api/config#api-section-snippet) voor de lijst van fragmenttypes.

- `priority`: hiermee wordt bepaald wanneer het VCL-fragment wordt uitgevoerd. In dit voorbeeld wordt prioriteit `5` gebruikt om direct te starten en te controleren of een beheerdersverzoek afkomstig is van een toegestaan IP-adres.

- `content`: Het fragment van VCL-code dat moet worden uitgevoerd, dat het client-IP-adres controleert. Als IP in ACL van Edge is, wordt het geblokkeerd van toegang met een `405 Not allowed` fout voor de volledige website. Alle andere client-IP-adressen hebben toegang.

Voor gedetailleerde informatie over het gebruiken van fragmenten VCL om inkomende verzoeken te blokkeren, zie [ Douane VCL voor het blokkeren van verzoeken ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-blocking) in _Commerce op de Gids van de Infrastructuur van de Wolk_.

>[!ENDSHADEBOX]

## Verificatiegegevens ophalen voor API-toegang

Voor AEM Assets Integration for Commerce zijn OAuth-verificatiereferenties vereist om API-toegang tot de Commerce-instantie te verlenen. Deze gegevens zijn vereist voor het verifiëren van API-aanvragen bij het beheer van middelen met de AEM Assets-integratie.

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

   1. Selecteer de externe mediabron **[!UICONTROL Catalog > Inventory > Products > External Media]** .

      ![ Configuratie van de Integratie Admin voor API middelen ](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

### Referenties genereren

Voor de pagina van Integraties, produceer de OAuth authentificatiegeloofsbrieven door **te klikken activeer** voor de integratie van Assets. U hebt deze gegevens nodig om het Commerce-project te registreren bij de Assets Rule Engine-service en om API-aanvragen in te dienen voor het beheer van middelen tussen Adobe Commerce en AEM Assets.

1. Genereer de referenties op de pagina Integraties door op **[!UICONTROL Activate]** te klikken.

   ![ activeer de configuratie van Commerce voor de integratie van Assets ](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Als u de API wilt gebruiken, slaat u de referenties voor de consumentensleutel en het toegangstoken op om verificatie in uw API-client te configureren.

   ![ OAuth geloofsbrieven om API verzoeken ](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"} voor authentiek te verklaren

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt ook verificatiegegevens genereren met de Adobe Commerce API&#39;s. Voor details over dit proces en meer informatie over op OAuth-Gebaseerde authentificatie voor Adobe Commerce, zie [ op OAuth-Gebaseerde authentificatie ](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in de documentatie van Adobe Developer.
