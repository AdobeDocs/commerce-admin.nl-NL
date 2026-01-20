---
title: Extensies van Adobe
description: Bekijk de informatie over extensies voor Adobe Commerce en Magento Open Source die door Adobe zijn uitgebracht.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 36c91007d21834b49351c8b53c617e442deebaa0
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Extensies van Adobe

Dit onderwerp bevat informatie over PHP-extensies voor Adobe Commerce en Magento Open Source die door Adobe worden uitgegeven.

Met extensies voegt u functies, functionaliteit, services en integratie toe aan Admin en Store. Sommige van deze verlengingen worden ontwikkeld met behulp van de bijdragen van de Gemeenschap van Magento Open Source. Sommige extensies worden standaard geïnstalleerd en andere moeten apart worden geïnstalleerd.

+++Meer informatie over Adobe Commerce uitbreiden

Adobe biedt twee hoofdmanieren om uw Adobe Commerce-projecten uit te breiden of aan te passen:

- Procesuitbreidbaarheid: gebruikt aangepaste code en extensies die in het Adobe Commerce-toepassingsproces worden uitgevoerd, zoals PHP-extensies. Deze traditionele benadering staat diepe integratie toe maar vereist zorgvuldig beheer tijdens verbeteringen.

- Buiten-de-procesrekbaarheid: Gebruikt douanecode en toepassingen die onafhankelijk van de kernsoftware werken. Deze moderne aanpak helpt de totale eigendomskosten te verlagen door:

   - Verbeteringen vereenvoudigen omdat extensies worden losgekoppeld van de kern
   - Ontwikkelaars meer controle geven over de timing en methoden van de implementatie
   - Onafhankelijk schalen en onderhoud van extensiecomponenten inschakelen

Adobe Commerce biedt strategieën en instrumenten om beide soorten uitbreidbaarheid te ondersteunen. Meer leren, zie [&#x200B; uitbreidbaarheid van Adobe Commerce &#x200B;](https://developer.adobe.com/commerce/extensibility/).

+++

## Adobe-extensies die standaard zijn geïnstalleerd

De volgende Adobe-extensies worden meegeleverd bij Adobe Commerce en worden automatisch geïnstalleerd bij de Adobe Commerce-toepassing. Sommige extensies moeten verder worden geconfigureerd of ingeschakeld in de beheerfunctie, zoals vermeld in de extensiebeschrijving.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) biedt verbeterd beheer van voorraden en verzendingen op één of meerdere locaties en verkoopkanalen met gelijktijdige algoritmen voor afhandelingsbeveiliging en -matching. Houd uw voorraad bij, geef klanten nauwkeurige verkoopcijfers en verzend objecten volgens de aanbevelingen of handmatige selecties om uw hele voorraad te beheren. Configureer de beheerinstellingen globaal, per bron en per product.

>[!NOTE]
>
>Deze uitbreiding werd ontwikkeld als deel van het [[!DNL Inventory Management] &#x200B;](https://github.com/magento/inventory) (vroeger MSI) project door het Communautaire Programma van de Techniek.

[!DNL Inventory Management] wordt geïnstalleerd met alle functies die standaard zijn ingeschakeld. Er zijn geen extra stappen nodig om deze voorraadfuncties in te schakelen. Voor details over de [!DNL Inventory Management] mogelijkheden, zie de [[!DNL Inventory Management]  Gids van de Gebruiker &#x200B;](../inventory-management/guide-overview.md).

### Braintree

PayPal en Gene Commerce hebben samen de officiële Braintree-extensie voor Commerce 2.4.x-winkels ontwikkeld. De updates zijn uitgerust met een verbeterde afrekenervaring die is ontworpen om de conversie te stimuleren en bevatten PayLater-opties die automatisch relevante PayLater-berichten en -knoppen weergeven aan consumenten tijdens het winkelen en tijdens het afrekenen.

Deze uitbreiding wordt geïnstalleerd door gebrek, maar vereist de a [&#x200B; rekening van Braintree &#x200B;](https://www.braintreepayments.com/) en configuratie in Admin om voor uw opslag worden toegelaten. Om de kosten te bepalen die van toepassing zijn wanneer het gebruiken van Braintree om uw transacties te verwerken, controleer de [&#x200B; prijs van Braintree &#x200B;](https://www.braintreepayments.com/braintree-pricing).

Voor informatie over de configuratie van Braintree in Admin, zie het [&#x200B; Braintree &#x200B;](../stores-purchase/braintree.md) onderwerp in de _Gids van de Ervaring van de Verkoop en van de Aankoop_.

### Google reCAPTCHA

Google reCAPTCHA biedt een hoger beveiligingsniveau voor zowel de storefront als de Admin-gebruikersinterface dan beschikbaar is met de standaard CAPTCHA en biedt u de mogelijkheid om:

- Verifieer wanneer de klanten rekeningen creëren, wachtwoorden terugwinnen, login aan hun rekeningen, of uw bedrijf contacteren.
- Verbeter de beveiliging wanneer Admin-gebruikers zich aanmelden.

Het vermindert potentiële gebruikersfout wanneer het ingaan van een code Captcha en moedigt wortelomzetting aan zonder hindernissen tijdens het afrekenen toe te voegen. [&#x200B; laat en vormt reCAPTCHA &#x200B;](../systems/security-google-recaptcha.md) toe gebruikend onzichtbare of interactieve controles om veilige toegang tot [!DNL Commerce] Admin en storefront te verbeteren.

### Twee-factor authentificatie

De [!DNL Commerce] Admin verleent al toegang tot uw opslag, orden, en klantengegevens. [&#x200B; two-factor authentificatie &#x200B;](../systems/security-two-factor-authentication.md) (2FA of TFA) verbetert veiligheid door extra authentificatie, voorbij de standaard login naam en het wachtwoord te vereisen, om tot [!DNL Commerce] Admin van alle apparaten toegang te hebben. De extensie ondersteunt meerdere authenticators, waaronder Google Authenticator, Authy, [!DNL Duo] en U2F. Deze verificatie is alleen van toepassing op Admin-gebruikers. Het is niet beschikbaar voor klantenaccounts van winkels.

Deze functies zijn standaard ingeschakeld. Elke Admin-gebruiker moet een van de ondersteunde verificateurs installeren en configureren.

>[!NOTE]
>
>Adobe Commerce-winkels die Adobe Identity Management Services (IMS)-verificatie voor de Admin hebben ingeschakeld, hebben native Commerce 2FA uitgeschakeld. Gebruikers die zich bij de beheerder hebben aangemeld met hun Adobe-gebruikersgegevens hoeven niet opnieuw te verifiëren voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [&#x200B; het Overzicht van de Integratie van Adobe Identity Management van de Dienst (IMS) &#x200B;](./adobe-ims-integration-overview.md).

## Adobe-extensies die moeten worden geïnstalleerd

Adobe biedt extra extensies die afzonderlijk met Composer moeten worden geïnstalleerd. Deze extensies zijn via verschillende kanalen beschikbaar:

- Toegang tot opslagplaats (repo.magento.com)

  Voor de volgende extensies zijn provisioning en aanmeldingsgegevens van account vereist. Neem contact op met uw Adobe-accountvertegenwoordiger voor hulp.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [AEM Assets-integratie voor Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  De volgende uitbreidingen van Adobe zijn openbaar toegankelijk bij [&#x200B; marketplace.magento.com &#x200B;](https://marketplace.magento.com). Deze extensies zijn zonder extra kosten beschikbaar.

   - [Live zoeken](#live-search)
   - [Aanbevelingen voor producten](#product-recommendations)
   - [Catalogusservice](#catalog-service)
   - [Betalingsdiensten](#payment-services)

### [!DNL Adobe Commerce B2B]

![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) slechts Adobe Commerce, vereist een afzonderlijke vergunning.

[!DNL Adobe Commerce B2B] is een geïntegreerde extensie die standaard Commerce-winkels omzet in uitgebreide business-to-business platforms. Het laat bedrijven toe om complexe organisatorische structuren met veelvoudige kopers, douanerollen, en kooptoestemmingen onder verenigde bedrijfrekeningen te beheren. Tot de belangrijkste functies behoren bedrijfsspecifieke catalogi en prijzen, verhandelbare prijzen, beheer van inkooporders, aanvraaglijsten en mogelijkheden voor snel bestellen. De oplossing steunt zowel modellen B2B als B2C op één enkele instantie, die het voor diverse bedrijfsbehoeften flexibel maakt. De extensie vereist een aparte licentie en kan naadloos worden geïntegreerd met de kernfuncties van Adobe Commerce om een volledige E-commerceoplossing voor B2B te bieden.

Neem voor provisioning contact op met uw Adobe-accountvertegenwoordiger. Voor implementatiedetails en configuratiestappen, zie de [[!DNL B2B for Adobe Commerce]  Gids van de Gebruiker &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=nl-NL).

### [!DNL AEM Assets Integration for Commerce]

![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) slechts Adobe Commerce, vereist ook vergunningen voor Adobe Experience Manager (AEM) Assets en AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] maakt een verbinding tussen Adobe Commerce en het Adobe Experience Manager Digital Asset Management (DAM)-systeem om gecentraliseerde controle over alle digitale middelen mogelijk te maken. Deze integratie maakt automatische synchronisatie van bedrijfsmiddelen, real-time updates en efficiënt hergebruik van inhoud in verschillende winkelwinkelwinkelcentra mogelijk. Door de robuuste mogelijkheden voor middelenbeheer van AEM te combineren met Commerce, kunnen bedrijven profiteren van gestroomlijnde workflows, consistente merkervaringen en geoptimaliseerde media-levering via cloudgebaseerde infrastructuren.

Neem voor provisioning contact op met uw Adobe-accountvertegenwoordiger. Voor implementatiedetails en configuratiestappen, zie de [[!DNL Assets Integration]  Gids van de Gebruiker &#x200B;](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) slechts Adobe Commerce

Live zoeken is een exclusieve Adobe Commerce-functie die een door AI aangedreven zoekoplossing biedt met real-time functionaliteit voor &#39;zoeken als u-typen&#39;. Het levert snelle, relevante resultaten met productduimnagels terwijl de kopers typen, samen met intelligente facetten die filters automatisch aanpassen gebaseerd op winkelgedrag. De oplossing omvat verkoopbevorderende mogelijkheden voor product en het begraven, synoniem beheer, en onderzoek analyseert. [!DNL Live Search] wordt zonder extra kosten bij Adobe Commerce geleverd en vervangt de standaardzoekfunctionaliteit door een meer geavanceerde zoekervaring op basis van SaaS. Het vereist minimale configuratie om te beginnen.

Voor implementatiedetails en technische vereisten, zie de [&#x200B; Levende Gids van de Gebruiker van het Onderzoek &#x200B;](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=nl-NL).

### [!DNL Product Recommendations]

![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) slechts Adobe Commerce

[!DNL Product Recommendations] is een exclusieve Adobe Commerce-functie met Adobe AI-technologie die gepersonaliseerde productsuggesties levert gedurende de hele reis van de klant. De oplossing analyseert verkoopgedrag en productrelaties in real-time om automatisch relevante aanbevelingen te genereren, waarvoor geen handmatige handelsregels vereist zijn. Deze op AI gebaseerde aanpak helpt de conversiekoersen en het inkomstenpotentieel te verhogen en zorgt voor meer aantrekkelijke ervaringen met productdetectie voor kopers.

Voor implementatiedetails en beste praktijken, zie de [[!DNL Product Recommendations]  Gids van de Gebruiker &#x200B;](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=nl-NL).

### [!DNL Catalog Service]

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} installaties van Adobe Commerce en van Magento Open Source

[!DNL Catalog Service] is een krachtige oplossing voor Adobe Commerce en Magento Open Source die geoptimaliseerde toegang tot catalogusgegevens biedt via GraphQL-eindpunten. Er wordt een aparte gesynchroniseerde database bijgehouden voor productdetails en gerelateerde informatie, waarbij directe communicatie tussen toepassingen wordt overgeslagen om sneller pagina&#39;s te laden. De service is bijzonder waardevol voor pagina&#39;s met productdetails, categorielijsten en pagina&#39;s met zoekresultaten, waardoor deze ideaal is voor zowel traditionele als koploze handelsimplementaties.

Voor opstellingsinstructies en technische details, zie de [[!DNL Catalog Service]  Gids van de Gebruiker &#x200B;](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=nl-NL).

>[!NOTE]
>
>Catalogusservices worden automatisch geïnstalleerd wanneer Live zoeken of productaanbevelingen zijn ingeschakeld. Handmatige installatie is niet vereist.

### [!DNL Payment Services]

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} installaties van Adobe Commerce en van Magento Open Source

[!DNL Payment Services] is een kant-en-klare betalingsoplossing voor Adobe Commerce- en Magento Open Source-winkels die uitgebreide mogelijkheden voor betalingsverwerking biedt. De service integreert beveiligde betaalgatewayfunctionaliteit met ingebouwde fraudebescherming, terwijl er meerdere betalingsopties worden aangeboden, zoals krediet-/debetkaarten, PayPal, Venmo (VS) en PayLater plannen. Het biedt uniforme transactierapportering en orderbeheer via de Commerce Admin-interface, waardoor handelaren eenvoudig betalingen kunnen bijhouden, de kasstroom kunnen beheren en alle financiële gegevens op één locatie met elkaar in overeenstemming kunnen brengen.

Voor gedetailleerde configuratiestappen en betalingsopties, zie de [[!DNL Payment Services]  Gids van de Gebruiker &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce/payment-services/overview).
