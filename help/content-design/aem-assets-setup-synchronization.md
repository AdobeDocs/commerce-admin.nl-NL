---
title: De synchronisatieservice instellen
description: "Leer hoe u uw Adobe Commerce- en Experience Manager Assets-projecten kunt verbinden met de Assets Rule Engine Service om de synchronisatie van bedrijfsmiddelen tussen deze twee systemen mogelijk te maken."
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# De synchronisatieservice instellen

De Asset Rules Engine Service (ARES) is een service voor meerdere huurders die AEM Assets met Adobe Commerce integreert. Deze service synchroniseert elementen tussen Adobe Commerce en Experience Manager. De ARES-service stemt automatisch elementen in AEM overeen met producten in Adobe Commerce op basis van SKU of andere sleutelkenmerken. Het zorgt ook dat de recentste productactiva en de variaties altijd beschikbaar op de plaats van de Handel zijn.

Als u de service wilt instellen, moet u uw gebruikers-id registreren met de API van ARES GraphQL en de overeenkomende regel voor het synchroniseren van elementen selecteren.

## Een overeenkomende strategie kiezen

De integratie van AEM Assets voor Commerce ondersteunt twee overeenkomsten voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

- **MatchBySku** - dit is de standaard passende regel die activa aanpast die op de Houdende Eenheid van de Voorraad (SKU) van het product worden gebaseerd. De SKU is een uniek herkenningsteken voor elk product. Deze regel past SKU in de elementenmeta-gegevens met het product SKU van Commerce aan om ervoor te zorgen dat de activa met de correcte producten worden geassocieerd.

- **ExternalMatcher** - Deze passende regel is voor complexere scenario&#39;s of specifieke bedrijfsvereisten die douane passende logica vereisen. Als u deze regel wilt gebruiken, moet in Adobe Developer App Builder aangepaste code zijn geïmplementeerd die definieert hoe elementen overeenkomen met producten.

Gebruik de `MatchBySku` -strategie voor het eerst aan boord gaan. Indien nodig, kunt u de passende strategie later veranderen.

## Een huurder registreren

>[!BEGINSHADEBOX]

**Vereiste**

- [ het project van AEM Assets is gevormd met de meta-gegevens van Commerce die voor toewijzingsactiva ](aem-assets-configure-aem.md) worden vereist.

- [ installeer en vorm de Integratie van Experience Manager Assets in Adobe Commerce ](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Referenties verzamelen

U hebt de volgende geloofsbrieven nodig om uw het projectmilieu van Commerce en het projectmilieu van AEM Assets met de diensten van Commerce SaaS voor authentiek te verklaren en te verbinden.

| Vereiste gegevens | Source | Waar vindt u het? |
| ---------- | ------ | ------------- |
| API-sleutel van Magento-account | Commerce | Geef de openbare API-sleutel op voor de Commerce-omgeving die u gebruikt, Staging of Production. U kunt de API sleutels voor de milieu&#39;s van de Productie en van het Staging op de ](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) pagina van de Opstelling van de Schakelaar van de Dienst van 0} Commerce in Admin, of op de [!UICONTROL My Account] pagina in de [!UICONTROL API Portal] sectie vinden.[ |
| Commerce SaaS Project Identifier <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce Admin | Deze waarden identificeren de Commerce-omgeving en SaaS-gegevensruimte en -project waarmee verbinding moet worden gemaakt. De waarden komen uit de [ Configuratie van het Herkenningsteken van SaaS van de Schakelaar van Commerce Services ].(aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| AEM `programId`<br>`environmentId` | [ AEM Assets Authoring Environment ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Open de AEM Sites-pagina en selecteer **[!UICONTROL Assets]** .  Kopieer de project- en omgeving-id&#39;s van de URL: `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | Commerce storefront | De [ basis URL ](../stores-purchase/store-urls.md) voor uw Commerce storefront. |
| OAuth-referenties voor API-toegang | Commerce Admin | U kunt deze geloofsbrieven in de de configuratiemontages van Commerce [ voor de integratie van Assets ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release) vinden. |

## Registerhuurder

Volledige huurdersregistratie door een verzoek aan de Dienst van de Motor van de Regel van Assets te voorleggen om authentificatiegeloofsbrieven en huurder IDs toe te voegen. Het verzoek omvat geloofsbrieven en projectherkenningstekens die worden vereist om de verbindingen tussen de dienst, het project van Commerce, en het project van Experience Manager Assets te vestigen.

Verzend de aanvraag met een GraphQL-client of cURL.

>[!BEGINTABS]

>[!TAB  GraphQL Verzoek ]

Een GraphQL-client gebruiken om een aanvraag voor een POST naar het API-eindpunt te verzenden `https://commerce.adobe.io/assets-integration/graphql`

**Vereiste kopballen**

Geef de volgende HTTP-headers voor de aanvraag op:

- `x-api-key`: API-sleutel van uw Magento-account
- `magento-environment-Id`: SaaS-id
- `x-gw-signature`: JWT Token gekoppeld aan de MAGEID

**Verzoek:**

**Syntaxis**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**gebruik van het Voorbeeld**

Registreer een huurder en selecteer de `matchBySku` regel om activa tussen Adobe Commerce en het project van AEM Assets in kaart te brengen.

**Verzoek:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**Reactie**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB  cURL verzoek ]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### Invoervelden

#### AemInput

Identificeert de AEM Assets-instantie voor het opslaan van Commerce-elementen. U kunt deze informatie ophalen vanuit de weergave Mijn programma&#39;s van Cloud Manager of via de URL voor het schrijven van inhoud.

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| `programId` | Tekenreeks! | Unieke id voor uw project in AEM Cloud Service |
| `environmentId` | Tekenreeks! | Id voor het projectmilieu u gebruikt, zoals Productie, het Opvoeren, of Ontwikkeling |

#### CommerceInput

Dit invoerveld bevat de OAuth-verificatiegegevens voor API-toegang tot de Commerce-catalogus. U kunt deze geloofsbrieven in de de configuratiemontages van Commerce [ voor de integratie van Assets ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release) vinden.

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| `baseUrl` | String | De [ basis URL ](../stores-purchase/store-urls.md) voor uw Commerce storefront. |
| `credentials` | [ CommerceCredentialsInput ](#commercecredentialsinput)! | Geeft de referenties op voor toegang tot de instantie Commerce. |
| `extensionVersion` | String | Optioneel. De versie van de AEM Assets Integration voor de Commerce-extensie die is geïnstalleerd op de Commerce-instantie. |
| `version` | String | Optioneel. De versie van de Commerce-toepassing die op de Commerce-instantie is geïnstalleerd. |

#### CommerceCredentialsInput

Dit invoerveld bevat de OAuth-referenties voor API-toegang tot de Commerce-catalogus. U kunt deze geloofsbrieven in de de configuratiemontages van Commerce [ voor de integratie van Assets ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release) vinden.

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| `accessToken` | Tekenreeks! | Het toegangstoken dat voor de integratie van Assets wordt geproduceerd. |
| `accessTokenSecret` | Tekenreeks! | Het geheim van het toegangstoken dat voor de integratie van Assets wordt geproduceerd. |
| `consumerKey` | Tekenreeks! | De consumentensleutel die voor de Assets-integratie is gegenereerd. |
| `consumerSecret` | Tekenreeks! | Het consumentengeheim dat voor de Assets-integratie werd gegenereerd. |

#### ExternalMatcherInput

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| assetToProductUrl | Tekenreeks! | <!--Add field description--> |
| productToAssetUrl | Tekenreeks! | <!--Add field description--> |
| geloofsbrieven | [ ExternalMatcherCredentialsInput ](#externalmatchercredentials)! | Credentials for access the App Builder project for the AEM Assets integration for Commerce. |

#### ExternalMatcherCredentials

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| `oauthServerUrl` | Tekenreeks! |    |
| `clientId` | Tekenreeks! |      |
| `clientSecret` | Tekenreeks! |    |
| `imsOrgId` | Tekenreeks! | De IMS-organisatie waar AEM Assets en Adobe Commerce zijn ingericht. |

#### MatchBySkuRuleInput

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| metadataField | Tekenreeks! | Geef het metagegevensveld voor de elementen op dat moet worden gebruikt voor overeenkomsten. `commerce:skus` gebruiken |

#### RuleInput

Geeft de regel aan die moet worden gebruikt voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| externalMatcher | [ ExternalMatcherInput ](#externalmatcherinput) | Selecteert de externalMatcher regel voor activa aanpassing en specificeert de gegevens die worden vereist om het te gebruiken. |
| MatchBySkuRule | [ MatchBySkuRuleInput ](#matchbyskuruleinput) | Selecteert MatchBySkuRule voor activa aanpassing en specificeert de gegevens die worden vereist om het te gebruiken. |

#### RuleTypeInput

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| RuleType | enum | Hier geeft u een lijst op met regels voor assetovereenkomsten die beschikbaar zijn voor AEM Assets Integration voor Commerce. Beschikbare waarden zijn `matchBySKU` of `externalMatcher` . |

#### TenantInput

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| `aem` | [ AemInput!](#aeminput) | Hiermee wordt de AEM Assets-instantie in de AEM Cloud Service aangegeven waar u de Commerce-elementen opslaat. |
| `commerce` | [ CommerceInput!](#commerceinput) | Biedt Commerce-projectinformatie en -referenties voor API-toegang |
| `enabled` | Booleaans! | Schakel de elementensynchronisatie tussen Adobe Commerce en AEM Assets in of uit. |
| `projectId` | Tekenreeks! | Identiteitskaart van het Project SaaS van de [ Configuratie van het Herkenningsteken van SaaS van de Verbinding van de Diensten van Commerce ](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| `rule` | [ RuleInput!](#ruleinput) | Geeft de regel aan die moet worden gebruikt voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets. Geef `[matchBySkuRule](#matchbyskuruleinput)` of `[externalMatcher](#externalmatcherinput)` op. |

### Uitvoervelden

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| data | [ registerTenant ] | Retourneert de gegevens van de huurdersregistratie en eventuele foutberichten van de server. |

#### RegisterTenantResponse

| Veld | Gegevenstype | Beschrijving |
| ----- | --------- | ----------- |
| huurderId | Tekenreeks! | Retourneert de huurder-id die is geregistreerd. Deze Id zorgt ervoor dat gegevens voor de AEM Assets Integration voor Commerce worden opgeslagen en opgehaald uit de SaaS-gegevensruimte die is gekoppeld aan de Commerce-omgeving. |
| userErrors | [[userError!]!](#usererror) | Retourneert eventuele foutberichten die door de aanvraag worden gegenereerd. |

#### UserError

| Fout | Beschrijving |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | Deze fout treedt op als de milieu-id die in de header `Magento-Environment-Id` is opgegeven, niet is toegewezen aan de IMS-account. Deze fout kan voorkomen omdat de rekening IMS niet werd verbonden toen de [ Schakelaar van de Diensten van Commerce ](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) voor de instantie van Commerce werd gevormd. |
| `Client ID is invalid` | De header `x-api-key` is onjuist. |
| `Client ID is missing` | De header `x-api-key` is niet opgegeven. |
| `JWT is required` | De header `x-gw-signature` is niet opgegeven. |
| `JWT is invalid` | De header `x-gw-signature` is niet opgegeven. |
| `Tenant already exists` | Een huurder met de gegeven `mageID` (die uit het teken van JWT wordt genomen) en `saasId` (die door de `Magento-Environment-Id` kopbal wordt verstrekt) werd reeds geregistreerd. |
| `Unexpected error when connecting with AEM Assets` | Deze fout treedt op als gevolg van ongeldige of niet-bestaande `programId` - of `environmentId` -waarden. |
| `Unable to connect with AEM Assets` | Er zijn twee mogelijke redenen voor deze fout:<br> 1. De AEM-middelenrekening is gekoppeld aan een andere IMS-organisatie-id dan die voor Adobe Commerce.<br> 2. De metagegevens van `commerce:isCommerce` bestaan niet in AEM Assets en geven aan dat er geen goedgekeurde elementen zijn om van AEM Assets naar de instantie van Commerce te verzenden. |
| `Unexpected error when connecting with Commerce` | Deze fout treedt op wanneer een ongeldige handelsinkoop `baseURL` wordt opgegeven. |
| `Unable to connect with Commerce, unauthorized` | Er zijn ongeldige handelsgegevens opgegeven, wat leidt tot onbevoegde toegang. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | Het veld `Rule` bevat een onjuiste waarde. Voor het verzoek RegisterTenant, worden de beschikbare regeltypes bepaald door [ RuleTypeInput ](#ruletypeinput) enum. |

## Integratie met Experience Manager Assets inschakelen

Nadat u de huurder registreert, is de laatste stap van het onboarding proces het toelaten van de Integratie van Experience Manager Assets voor de uitbreiding van Commerce in Admin.

1. De extensie inschakelen.

   1. Ga naar **Slaat** > Montages > **Configuratie** > **Catalogus** op.

   1. Open de catalogusconfiguratie door **[!UICONTROL Catalog]** te selecteren.

   1. Vouw **[!UICONTROL AEM Assets integration]** uit.

   1. Stel **[!UICONTROL Integration enabled]** in op `yes` .

      ![ Integratie van AEM Assets voor de configuratie van Admin van Commerce ](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
