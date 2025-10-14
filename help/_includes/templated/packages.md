---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# Adobe Commerce met B2B-pakketten

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B gebruikt Composer om PHP-pakketten te beheren.

In het bestand `composer.json` wordt de lijst met pakketten gedeclareerd, terwijl in het bestand van `composer.lock` een volledige lijst met pakketten (een volledige versie van elk pakket en de bijbehorende afhankelijkheden) wordt opgeslagen die worden gebruikt om een installatie van Adobe Commerce B2B te maken.

De volgende referentiedocumentatie wordt gegenereerd uit het `composer.lock` -bestand en omvat de vereiste pakketten die zijn opgenomen in Adobe Commerce B2B 1.5.2.

## Afhankelijkheden

`magento/extension-b2b 1.5.2` heeft de volgende afhankelijkheden:

- magento/framework: >=103.0.6 &lt;103.0.9
- magento/magento2-b2b-base: 1.5.2
- [&#x200B; magento/module-b2b &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-b2b/): 100.5.2
- [&#x200B; magento/module-bundle-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/): 100.5.1
- [&#x200B; magento/module-bundel-vordering-lijst &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/): 100.5.1
- [&#x200B; magento/module-bundle-requisition-list-graph-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/): 1.5.1
- [&#x200B; magento/module-bundle-shared-catalog &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/): 100.5.1
- [&#x200B; magento/module-checkout-adres-onderzoek-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/): 100.5.1
- [&#x200B; magento/module-checkout-agreements-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/): 100.5.1
- [&#x200B; magento/module-checkout-agreements-aankoop-orde &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/): 1.5.1
- [&#x200B; magento/module-bedrijf &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company/): 102.0.2
- [&#x200B; magento/module-bedrijf-asynchrone-verrichtingen &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/): 1.5.1
- [&#x200B; magento/module-bedrijf-krediet &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/): 100.5.2
- [&#x200B; magento/module-bedrijf-krediet-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/): 1.5.1
- [&#x200B; magento/module-bedrijf-klant-invoer-uitvoer &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/): 1.5.0
- [&#x200B; magento/module-bedrijf-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/): 1.5.2
- [&#x200B; magento/module-bedrijf-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/): 1.5.1
- [&#x200B; magento/module-bedrijf-onderhandelbaar-citaat-malplaatje &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/): 1.5.1
- [&#x200B; magento/module-bedrijf-betaling &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/): 100.5.1
- [&#x200B; magento/module-bedrijf-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/): 1.5.2
- [&#x200B; magento/module-bedrijf-citaat-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/): 1.5.2
- [&#x200B; magento/module-bedrijf-verhouding &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/): 1.5.2
- [&#x200B; magento/module-bedrijf-verband-gedeelde-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/): 1.5.1
- [&#x200B; magento/module-bedrijf-verschepen &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/): 1.5.1
- [&#x200B; magento/module-configureerbaar-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/): 100.5.1
- [&#x200B; magento/module-configureerbaar-eis-lijst &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/): 100.5.1
- [&#x200B; magento/module-configureerbaar-aanvraag-lijst-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/): 1.5.1
- [&#x200B; magento/module-configureerbaar-gedeeld-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/): 100.5.1
- [&#x200B; magento/module-downloadbaar-bedrijf &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/): 1.5.1
- [&#x200B; magento/module-downloadbaar-aanvraag-lijst-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/): 1.5.1
- [&#x200B; magento/module-gift-kaart-verhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/): 100.5.1
- [&#x200B; magento/module-gift-kaart-aanvraag-lijst &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/): 100.5.1
- [&#x200B; magento/module-gift-kaart-vordering-lijst-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/): 1.5.1
- [&#x200B; magento/module-gift-kaart-gedeelde-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/): 100.5.1
- [&#x200B; magento/module-gegroepeerd-aanvraag-lijst &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/): 100.5.1
- [&#x200B; magento/module-gegroepeerde-gedeelde-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/): 100.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/): 101.0.2
- [&#x200B; magento/module-onderhandelbaar-citaat-async-orde &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/): 1.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-dubbel &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/): 1.5.2
- [&#x200B; magento/module-onderhandelbaar-citaat-dubbel-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/): 1.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/): 1.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-aanvraag-lijst &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/): 1.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-aanvraag-lijst-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/): 1.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-gedeelde-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/): 100.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-malplaatje &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/): 1.5.2
- [&#x200B; magento/module-onderhandelbaar-citaat-malplaatje-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/): 1.5.2
- [&#x200B; magento/module-onderhandelbaar-citaat-malplaatje-gedeeld-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/): 1.5.1
- [&#x200B; magento/module-onderhandelbaar-citaat-weee &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/): 100.5.1
- [&#x200B; magento/module-orde-geschiedenis-onderzoek &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/): 100.5.2
- [&#x200B; magento/module-paypal-onderhandelbaar-citaat &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/): 1.5.1
- [&#x200B; magento/module-paypal-aankoop-orde &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/): 1.5.1
- [&#x200B; magento/module-aankoop-orde &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/): 100.5.2
- [&#x200B; magento/module-aankoop-orde-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/): 1.5.1
- [&#x200B; magento/module-aankoop-orde-regel &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/): 100.5.2
- [&#x200B; magento/module-aankoop-orde-regel-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/): 1.5.1
- [&#x200B; magento/module-snel-orde &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/): 100.5.1
- [&#x200B; magento/module-snel-orde-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/): 1.5.1
- [&#x200B; magento/module-aanvraag-lijst &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/): 100.5.2
- [&#x200B; magento/module-aanvraag-lijst-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/): 1.5.1
- [&#x200B; magento/module-gedeeld-catalogus &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/): 100.5.2
- [&#x200B; magento/module-gedeelde-catalogus-grafiek-ql &#x200B;](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/): 1.5.1
- magento/security-package-b2b: 1.0.6

## Licenties van derden

### Apache-2.0, alleen LGPL-2.1

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php"> openssearch-project/openssearch-php </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP-client voor OpenSearch</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp"> astock/stock-api-libphp </a>
    </td>
    <td>Bibliotheek</td>
    <td>Adobe Stock API-bibliotheek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php"> aws/aws-crt-php </a>
    </td>
    <td>Bibliotheek</td>
    <td>AWS Common Runtime voor PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php"> aws/aws-sdk-php </a>
    </td>
    <td>Bibliotheek</td>
    <td>AWS SDK for PHP - Amazon Web Services gebruiken in je PHP project</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api"> open-telemetry/api </a>
    </td>
    <td>Bibliotheek</td>
    <td>API voor OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context"> open-telemetrie/context </a>
    </td>
    <td>Bibliotheek</td>
    <td>Context-implementatie voor OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      paypal/module-breintree
    </td>
    <td>Metapakket</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php"> wikimedia/less.php</a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP poort van de LESS processor</td>
  </tr>
  </tbody>
</table>

### BSD-2-Clause

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode"> bacon/bacon-qr-code </a>
    </td>
    <td>Bibliotheek</td>
    <td>BaconQrCode is een QR code generator voor PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum"> dasprid/enum </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP 7.1 enum implementatie</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer"> webimpress/safe-writer </a>
    </td>
    <td>Bibliotheek</td>
    <td>Gereedschap om bestanden veilig te schrijven om rasomstandigheden te voorkomen</td>
  </tr>
  </tbody>
</table>

### BSD-3-Clause

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File"> colinmelenhour/cache-back-end-file </a>
    </td>
    <td>Magento-module</td>
    <td>De stock Zend_Cache_Backend_File achtergrond heeft uiterst slechte prestaties voor schoonmaken door markeringen die het onbruikbaar maken maken aangezien het aantal caching punten stijgt. Deze backend brengt vele veranderingen met zich mee die in een enorme prestatiesverhoging, vooral voor markeringszuivering resulteren.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract"> colinmolenhour/php-redis-session-abstract </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een op Redis gebaseerde sessiehandler met optimistische vergrendeling</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php"> duosecurity/duo_Universal_php </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP-implementatie van de Duo Universal SDK.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt"> firebase/php-jwt </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een eenvoudige bibliotheek voor het coderen en decoderen van JSON Web Tokens (JWT) in PHP. Moet in overeenstemming zijn met de huidige specificatie.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha"> laminas/laminas-captcha </a>
    </td>
    <td>Bibliotheek</td>
    <td>CAPTCHA's genereren en valideren met behulp van figuren, afbeeldingen, ReCaptcha en meer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code"> laminas/laminas-code </a>
    </td>
    <td>Bibliotheek</td>
    <td>Extensies voor de PHP Reflectie-API, scannen van statische code en genereren van code</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config"> laminas/laminas-config </a>
    </td>
    <td>Bibliotheek</td>
    <td>biedt een geneste, op objecteigenschappen gebaseerde gebruikersinterface voor toegang tot deze configuratiegegevens binnen de toepassingscode</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di"> laminas/laminas-di </a>
    </td>
    <td>Bibliotheek</td>
    <td>Geautomatiseerde afhankelijkheidsinjectie voor PSR-11 containers</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper"> laminas/laminas-escaper </a>
    </td>
    <td>Bibliotheek</td>
    <td>Veilig en veilig ontsnappen aan HTML, HTML-kenmerken, JavaScript, CSS en URL's</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager"> laminas/laminas-eventmanager </a>
    </td>
    <td>Bibliotheek</td>
    <td>Trigger en luister naar gebeurtenissen in een PHP-toepassing</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed"> laminas/laminas-voer </a>
    </td>
    <td>Bibliotheek</td>
    <td>biedt functionaliteit voor het maken en gebruiken van RSS- en Atom-feeds</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter"> laminas/laminas-filter </a>
    </td>
    <td>Bibliotheek</td>
    <td>Gegevens en bestanden programmatisch filteren en normaliseren</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http"> laminas/laminas-http </a>
    </td>
    <td>Bibliotheek</td>
    <td>Biedt een eenvoudige interface voor het uitvoeren van HTTP-aanvragen (Hyper-Text Transfer Protocol)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n"> laminas/laminas-i18n </a>
    </td>
    <td>Bibliotheek</td>
    <td>Vertaal uw toepassing en filtert en valideert geïnternationaliseerde waarden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json"> laminas/laminas-json </a>
    </td>
    <td>Bibliotheek</td>
    <td>biedt gebruiksvriendelijke methoden voor het serialiseren van native PHP naar JSON en het decoderen van JSON naar native PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader"> laminas/laminas-loader </a>
    </td>
    <td>Bibliotheek</td>
    <td>Laden van autoloading en plug-in</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager"> laminas/laminas-modulemanager </a>
    </td>
    <td>Bibliotheek</td>
    <td>Modulair toepassingssysteem voor laminas-mvc-toepassingen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc"> laminas/laminas-mvc </a>
    </td>
    <td>Bibliotheek</td>
    <td>De gebeurtenis-gedreven laag MVC van Laminas, met inbegrip van Toepassingen MVC, Controllers, en Insteekmodules</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl"> laminas/laminas-permissions-acl </a>
    </td>
    <td>Bibliotheek</td>
    <td>Verstrekt een lichtgewichten flexibele implementatie van de toegangsbeheerlijst (ACL) voor toegangsbeheer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha"> laminas/laminas-recaptcha </a>
    </td>
    <td>Bibliotheek</td>
    <td>OOP-wrapper voor de ReCaptcha-webservice</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router"> laminas/laminas-router </a>
    </td>
    <td>Bibliotheek</td>
    <td>Flexibel verpletterend systeem voor HTTP en consoletoepassingen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server"> laminas/laminas-server </a>
    </td>
    <td>Bibliotheek</td>
    <td>Op reflectie gebaseerde RPC-servers maken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager"> laminas/laminas-servicemanager </a>
    </td>
    <td>Bibliotheek</td>
    <td>In de fabriek aangebrachte afhankelijkheidsinjectiecontainer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session"> laminas/laminas-zitting </a>
    </td>
    <td>Bibliotheek</td>
    <td>Object-oriented interface aan PHP zittingen en opslag</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap"> laminas/laminas-soap </a>
    </td>
    <td>Bibliotheek</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib"> laminas/laminas-stdlib </a>
    </td>
    <td>Bibliotheek</td>
    <td>SPL-extensies, arrayhulpprogramma's, fouthandlers en meer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text"> laminas/laminas-text </a>
    </td>
    <td>Bibliotheek</td>
    <td>FIGlets en op tekst gebaseerde tabellen maken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator"> laminas/laminas-vertaler </a>
    </td>
    <td>Bibliotheek</td>
    <td>Interfaces voor de component Translator van laminas-i18n</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri"> laminas/laminas-uri </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een component die helpt bij het manipuleren en valideren van URI's (Uniform Resource Identifiers)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator"> laminas/laminas-validator </a>
    </td>
    <td>Bibliotheek</td>
    <td>Validatieklassen voor een groot aantal domeinen en de mogelijkheid om validators te ketenen om complexe validatiecriteria te maken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view"> laminas/laminas-mening </a>
    </td>
    <td>Bibliotheek</td>
    <td>Flexibele weergavelaag die meerdere weergavelagen, hulplijnen en meer ondersteunt en biedt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum"> marc-mabe/php-enum </a>
    </td>
    <td>Bibliotheek</td>
    <td>Eenvoudige en snelle implementatie van opsommingen met native PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser"> nikic/php-parser </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP parser geschreven in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha"> phpfui/recaptcha </a>
    </td>
    <td>Bibliotheek</td>
    <td>Clientbibliotheek voor Google reCAPTCHA voor PHP 8.4 en hoger</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink"> tedivm/jshrink </a>
    </td>
    <td>Bibliotheek</td>
    <td>Javascript Minifier geïntegreerd in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port"> tubalmartin/cssmin </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP-poort van de YUI CSS-compressor</td>
  </tr>
  </tbody>
</table>

### BSD-3-Clause-Modification

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis"> colinmolenhour/cache-backend-redis </a>
    </td>
    <td>Magento-module</td>
    <td>Zend_Cache backend met Redis met volledige ondersteuning voor tags.</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat"> paragonie/natrium_compat </a>
    </td>
    <td>Bibliotheek</td>
    <td>Puur PHP implementatie van libnatrium; gebruikt de PHP extensie als deze bestaat</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1 of hoger

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier"> ezyang/htmlpurifier </a>
    </td>
    <td>Bibliotheek</td>
    <td>HTML-filter voldoet aan standaarden geschreven in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib"> php-amqplib/php-amqplib </a>
    </td>
    <td>Bibliotheek</td>
    <td>Vroeger videlalvaro/php-amqplib.  Deze bibliotheek is een pure PHP-implementatie van het AMQP-protocol. Het is getest op RabbitMQ.</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php"> breintree/braintree_php </a>
    </td>
    <td>Bibliotheek</td>
    <td>Braintree PHP Client Library</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math"> steen/math </a>
    </td>
    <td>Bibliotheek</td>
    <td>Rekenkundige bibliotheek met willekeurige precisie</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter"> baksteen/varexporter </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een krachtig alternatief voor var_export(), dat sluitingen en objecten zonder __set_state() kan exporteren</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32"> christian-riesen/base32 </a>
    </td>
    <td>Bibliotheek</td>
    <td>Base32 encoder/decoder volgens RFC 4648</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis"> colinmolenhour/credits </a>
    </td>
    <td>Bibliotheek</td>
    <td>Credis is een lichtgewicht interface naar de sleutelwaardewinkel van Redis, waar de phpredis-bibliotheek wordt geplaatst als deze beschikbaar is voor betere prestaties.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle"> composer/ca-bundle </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hier vindt u een pad naar de CA-bundel van het systeem en een fallback naar de Mozilla CA-bundel.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator"> composer/klasse-kaart-generator </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hulpprogramma's voor het scannen van PHP-code en het genereren van klassenkaarten.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer"> composer/composer </a>
    </td>
    <td>Bibliotheek</td>
    <td>Met Composer kunt u afhankelijkheden van PHP-projecten declareren, beheren en installeren. Zo weet u zeker dat u overal de juiste stapel hebt.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier"> composer/metadata-minifier </a>
    </td>
    <td>Bibliotheek</td>
    <td>Kleine nutsbibliotheek die meta-gegevensminificatie en uitbreiding behandelt.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre"> composer/pcre </a>
    </td>
    <td>Bibliotheek</td>
    <td>PCRE-wrapping-bibliotheek met type-veilige preg_* vervangingen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver"> composer/semver </a>
    </td>
    <td>Bibliotheek</td>
    <td>Semverbibliotheek met hulpprogramma's, parsering en validatie van versiebeperkingen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses"> composer/spdx-vergunningen </a>
    </td>
    <td>Bibliotheek</td>
    <td>Lijst met SPDX-licenties en validatiebibliotheek.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler"> composer/xdebug-manager </a>
    </td>
    <td>Bibliotheek</td>
    <td>Start een proces zonder Xdebug opnieuw.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer"> doctrine/lexer </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP Doctrine Lexer parser bibliotheek die gebruikt kan worden in top-down, Recursive Descent Parsers.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator"> egulias/e-mail-validator </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een bibliotheek voor het valideren van e-mailberichten op verschillende RFC's</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php"> elastic/vervoer </a>
    </td>
    <td>Bibliotheek</td>
    <td>HTTP transport PHP bibliotheek voor Elastic producten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php"> elasticsearch/elasticsearch </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP-client voor Elasticsearch</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code"> endroid/qr-code </a>
    </td>
    <td>Bibliotheek</td>
    <td>QR-code van Endroid</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams"> ezimuel/guzzlestreams </a>
    </td>
    <td>Bibliotheek</td>
    <td>Vork van guzzle/streams (verlaten) voor gebruik met elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp"> ezimuel/ringphp </a>
    </td>
    <td>Bibliotheek</td>
    <td>Vork van guzzle/RingPHP (verlaten) voor gebruik met elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle"> guzzlehttp/guzzle </a>
    </td>
    <td>Bibliotheek</td>
    <td>Guzzle is een PHP HTTP client library</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises"> guzzlehttp/promise </a>
    </td>
    <td>Bibliotheek</td>
    <td>Guzzle belooft library</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7"> guzzlehttp/psr7 </a>
    </td>
    <td>Bibliotheek</td>
    <td>PSR-7 berichtimplementatie die ook gemeenschappelijke nutsmethodes verstrekt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema"> justinrainbow/json-schema </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een bibliotheek om een jseschema te valideren.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem"> liga/vliegsysteem </a>
    </td>
    <td>Bibliotheek</td>
    <td>Abstractie van bestandsopslag voor PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3"> liga/flysystem-ws-s3-v3 </a>
    </td>
    <td>Bibliotheek</td>
    <td>AWS S3-bestandssysteemadapter voor Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local"> liga/flysystem-local </a>
    </td>
    <td>Bibliotheek</td>
    <td>Lokale bestandssysteemadapter voor Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection"> liga/mime-type-opsporing </a>
    </td>
    <td>Bibliotheek</td>
    <td>MIME-typedetectie voor Flysystem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog"> monolog/monolog </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee verzendt u uw logbestanden naar bestanden, sockets, inboxen, databases en verschillende webservices</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php"> mtdowling/jmespath.php</a>
    </td>
    <td>Bibliotheek</td>
    <td>Declaratief opgeven hoe elementen uit een JSON-document worden geëxtraheerd</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding"> paragonie/constant_time_encoding </a>
    </td>
    <td>Bibliotheek</td>
    <td>Constante-tijdImplementaties van Codering RFC 4648 (basis-64, basis-32, basis-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat"> paragonie/random_compat </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP 5.x polyfill for random_bytes() en random_int() van PHP 7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier"> pelago/emogrifier </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee zet u CSS-stijlen om in inline stijlkenmerken in uw HTML-code</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery"> php-http/discovery </a>
    </td>
    <td>Composer-plug-in</td>
    <td>Vindt en installeert PSR-7, PSR-17, PSR-18 en HTTPlug implementaties</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug"> php-http/httplug </a>
    </td>
    <td>Bibliotheek</td>
    <td>HTTPlug, de HTTP client abstractie voor PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise"> php-http/promise </a>
    </td>
    <td>Bibliotheek</td>
    <td>Promise die voor asynchrone HTTP- verzoeken wordt gebruikt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath"> phpgt/cssxpath </a>
    </td>
    <td>Bibliotheek</td>
    <td>CSS-kiezers converteren naar XPath-query's.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom"> phpgt/dom </a>
    </td>
    <td>Bibliotheek</td>
    <td>Moderne DOM API.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc"> phpgt/propfunc </a>
    </td>
    <td>Bibliotheek</td>
    <td>Functies van accessoreigenschap en mutator.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat"> phpseclib/mcrypt_compat </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP 5.x-8.x polyfill for mcrypt extension</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib"> phpseclib/phpseclib </a>
    </td>
    <td>Bibliotheek</td>
    <td>PHP Secure Communications Library - Pure-PHP implementaties van RSA, AES, SSH2, SFTP, X.509 enz.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache"> psr/cache </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene interface voor het in cache plaatsen van bibliotheken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock"> psr/klok </a>
    </td>
    <td>Bibliotheek</td>
    <td>Gemeenschappelijke interface voor het lezen van de klok.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container"> psr/container </a>
    </td>
    <td>Bibliotheek</td>
    <td>Common Container Interface (PHP FIG PSR-11)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher"> psr/event-dispatcher </a>
    </td>
    <td>Bibliotheek</td>
    <td>Standaardinterfaces voor gebeurtenisafhandeling.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client"> psr/http-client </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene interface voor HTTP-clients</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory"> psr/http-factory </a>
    </td>
    <td>Bibliotheek</td>
    <td>PSR-17: Gemeenschappelijke interfaces voor PSR-7 HTTP- berichtfabrieken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message"> psr/http-message </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene interface voor HTTP-berichten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log"> psr/log </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene interface voor logbibliotheken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders"> ralouphie/getallheaders </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een polyfill voor getallheaders.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection"> ramsey/inzameling </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP-bibliotheek voor het weergeven en manipuleren van verzamelingen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid"> ramsey/uuid </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP-bibliotheek voor het genereren en gebruiken van universeel unieke id's (UUID's).</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise"> reactie/belofte </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een lichte implementatie van CommonJS Promises/A voor PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser"> sabberworm/php-css-parser </a>
    </td>
    <td>Bibliotheek</td>
    <td>Parser voor CSS-bestanden geschreven in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint"> seld/jsonlint </a>
    </td>
    <td>Bibliotheek</td>
    <td>JSON Linter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils"> seld/phar-utils </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hulpprogramma's voor PHAR-bestandsindelingen, bijvoorbeeld wanneer PHP je opbelt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler"> geselecteerd/signaal-manager </a>
    </td>
    <td>Bibliotheek</td>
    <td>Eenvoudige unix signaalmanager die ongemerkt ontbreekt waar de signalen niet voor gemakkelijke dwars-platformontwikkeling worden gesteund</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap"> spomky-labs/aes-key-wrap </a>
    </td>
    <td>Bibliotheek</td>
    <td>AES Key Wrap voor PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp"> spomky-labs/otphp </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP bibliotheek voor het produceren van één tijdwachtwoorden volgens RFC 4226 (het Algoritme van HOTP) en RFC 6238 (TOTP Algorithm) en compatibel met de Authenticator van Google</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework"> spomky-labs/pki-kader </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP-framework voor het beheren van infrastructuur voor openbare sleutels. Het omvat X.509 openbare zeer belangrijke certificaten, attributencertificaten, certificatieverzoeken en certificatiewegbevestiging.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config"> symfony/config </a>
    </td>
    <td>Bibliotheek</td>
    <td>Helpt u configuratiewaarden van om het even welke aard te vinden, te laden, te combineren, automatisch te vullen en te bevestigen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console"> symfony/console </a>
    </td>
    <td>Bibliotheek</td>
    <td>Versnelt het creëren van mooie en testable bevellijninterfaces</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector"> symfony/css-selector </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee converteert u CSS-kiezers naar XPath-expressies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection"> symfony/afhankelijkheid-injectie </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee kunt u de manier waarop objecten in uw toepassing worden gemaakt standaardiseren en centraliseren</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts"> symfony/deprecation-Contracten </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een algemene functie en conventie voor het activeren van plaatsingsberichten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler"> symfony/fout-manager </a>
    </td>
    <td>Bibliotheek</td>
    <td>Biedt tools om fouten te beheren en foutopsporing in PHP-code te vereenvoudigen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher"> symfony/event-dispatcher </a>
    </td>
    <td>Bibliotheek</td>
    <td>Verstrekt hulpmiddelen die uw toepassingscomponenten toestaan om met elkaar te communiceren door gebeurtenissen te verzenden en aan hen te luisteren</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts"> symfony/event-dispatcher-Contracts </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene abstracties met betrekking tot verzendgebeurtenis</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem"> symfony/filesystem </a>
    </td>
    <td>Bibliotheek</td>
    <td>Biedt basisfuncties voor het bestandssysteem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder"> symfony/vinder </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee zoekt u bestanden en mappen via een intuïtieve fluent-interface</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client"> symfony/http-client </a>
    </td>
    <td>Bibliotheek</td>
    <td>Biedt krachtige methoden om HTTP-bronnen synchroon of asynchroon op te halen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts"> symfony/http-client-Contracts </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene abstracties met betrekking tot HTTP-clients</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation"> symfony/http-foundation </a>
    </td>
    <td>Bibliotheek</td>
    <td>Definieert een objectgeoriënteerde laag voor de HTTP-specificatie</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel"> symfony/http-kernel </a>
    </td>
    <td>Bibliotheek</td>
    <td>Verstrekt een gestructureerd proces om een Verzoek in een Reactie om te zetten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl"> symfony/intl </a>
    </td>
    <td>Bibliotheek</td>
    <td>Verleent toegang tot de localisatiegegevens van de bibliotheek ICU</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer"> symfony/mailer </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hulp bij het verzenden van e-mails</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime"> symfony/mime </a>
    </td>
    <td>Bibliotheek</td>
    <td>MIME-berichten kunnen worden bewerkt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype"> symfony/polyfill-type </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill voor tekstfuncties</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme"> symfony/polyfill-intl-grapheme </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill voor de functies grapheme_* van intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn"> symfony/polyfill-intl-idn </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill voor de functies idn_to_ascii en idn_to_utf8</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer"> symfony/polyfill-intl-normalizer </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill voor de klasse Normalizer van intl en verwante functies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring"> symfony/polyfill-mbstring </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill voor de extensie Mbstring</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73"> symfony/polyfill-php73 </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill geeft een aantal functies van PHP 7.3+ terug naar lagere PHP versies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80"> symfony/polyfill-php80 </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill geeft een aantal functies van PHP 8.0+ terug naar lagere PHP versies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81"> symfony/polyfill-php81 </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill geeft een aantal functies van PHP 8.1+ terug naar lagere PHP versies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82"> symfony/polyfill-php82 </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill geeft een aantal functies van PHP 8.2+ terug naar lagere PHP versies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83"> symfony/polyfill-php83 </a>
    </td>
    <td>Bibliotheek</td>
    <td>Symfony polyfill geeft een aantal functies van PHP 8.3+ terug naar lagere PHP versies</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process"> symfony/proces </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee voert u opdrachten uit in subprocessen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts"> symfony/dienst-contracten </a>
    </td>
    <td>Bibliotheek</td>
    <td>Algemene abstracties met betrekking tot schrijfdiensten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string"> symfony/koord </a>
    </td>
    <td>Bibliotheek</td>
    <td>Biedt een objectgeoriënteerde API voor tekenreeksen en behandelt bytes, UTF-8-codepunten en grafeemclusters op een uniforme manier</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper"> symfony/var-dumper </a>
    </td>
    <td>Bibliotheek</td>
    <td>Biedt mechanismen om willekeurige PHP variabelen te doorlopen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter"> symfony/var-exporter </a>
    </td>
    <td>Bibliotheek</td>
    <td>Hiermee wordt het exporteren van eventuele serialiseerbare PHP-gegevensstructuur naar normale PHP-code toegestaan</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml"> symfony/yaml </a>
    </td>
    <td>Bibliotheek</td>
    <td>YAML-bestanden laden en dumpen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework"> web-token/jwt-framework </a>
    </td>
    <td>Symfony-bundle</td>
    <td>JSON Object Signing and Encryption library for PHP and Symfony Bundle.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php"> webonyx/graphql-php </a>
    </td>
    <td>Bibliotheek</td>
    <td>Een PHP-poort van GraphQL referentie-implementatie</td>
  </tr>
  </tbody>
</table>

### OSL-3.0, AFL-3.0

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-breintree-customer-balance
    </td>
    <td>Magento2-module</td>
    <td>NVT</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card
    </td>
    <td>Magento2-module</td>
    <td>NVT</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card-account
    </td>
    <td>Magento2-module</td>
    <td>NVT</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-wrapping
    </td>
    <td>Magento2-module</td>
    <td>NVT</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Magento2-module</td>
    <td>NVT</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-promise
    </td>
    <td>Magento2-module</td>
    <td>NVT</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode"> 2tvenom/cancode </a>
    </td>
    <td>Bibliotheek</td>
    <td>CBOR encoder voor PHP</td>
  </tr>
  </tbody>
</table>

### Eigen

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### bedrijfseigen

<table>
  <thead>
    <tr>
      <th>Naam</th>
      <th>Type</th>
      <th>Beschrijving</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-breintree-core
    </td>
    <td>Magento2-module</td>
    <td>Vork uit de Magento Braintree 2.2.0 module door Gene Commerce for PayPal.</td>
  </tr>
  </tbody>
</table>
