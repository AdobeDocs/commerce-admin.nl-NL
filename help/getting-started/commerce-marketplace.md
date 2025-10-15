---
title: '[!DNL Adobe Commerce Marketplace]'
description: Leer over  [!DNL Commerce Marketplace], die verkopers een gekromde selectie van oplossingen aanbiedt, en gekwalificeerde ontwikkelaars de hulpmiddelen, het platform, en de eerste plaats verstrekt om een het bloeien zaken te bouwen.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 7b5c331625e4c4dab0e41156722c4a8deb4aa4c0
workflow-type: tm+mt
source-wordcount: '1293'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[ Adobe Commerce Marketplace ][1] is de toepassingsopslag die verkopers een gekromde selectie van oplossingen aanbiedt, en gekwalificeerde ontwikkelaars de hulpmiddelen, het platform, en de eerste plaats verstrekt om een het bloeien zaken te bouwen. [!DNL Commerce Marketplace] biedt een selectie van extensies die gratis beschikbaar zijn en andere extensies die te koop zijn. De aankopen kunnen door creditcard of [ PayPal ][2] worden betaald.

Alle extensies die beschikbaar zijn op [!DNL Commerce Marketplace] , hebben een uitgebreide revisie doorlopen. Het [ Programma van de Kwaliteit van de Uitbreiding ][3] (EQP) combineert [!DNL Commerce] deskundigheid, ontwikkelingsrichtlijnen, en controlehulpmiddelen om ervoor te zorgen dat alle uitbreidingen op Commerce Marketplace coderingsnormen en beste praktijken voldoen. Het revisieproces omvat zowel een automatische controle als een handmatige kwaliteitscontrole. Tijdens het proces worden de structuur en de code van elke extensie onderzocht en getest op tekenen van besmetting met virussen/malware, en op aanwijzingen voor plagiaat. De revisie omvat een diepgaande technische controle en controle van de hygiëne die door een [!DNL Commerce] ingenieur wordt uitgevoerd, met nadruk op documentatie, codeerstructuur, prestaties, scalability, veiligheid, en verenigbaarheid met de [!DNL Commerce] kern.

Hoewel u extensies kunt kopen van andere bronnen, worden alleen de extensies die beschikbaar zijn op [!DNL Commerce Marketplace] gecontroleerd aan de hand van uitgebreide technische en marketingrevisie in het Extension Quality Program.

## App-bronnen

Ontwikkelaars hebben van oudsher PHP gebruikt om &#39;in-process&#39; extensies te maken die functies, functionaliteit, services en integratie toevoegen aan Adobe Commerce. Door toepassingen te maken die niet langer procesextensies maar uitbreidbaar zijn, kunt u compatibiliteitsproblemen voorkomen.

De volgende bronnen bieden een beginpunt voor nieuwe gebruikers om vertrouwd te raken met apps:

### Commerce-bronnen

- [&#x200B; Vestigings I/O Gebeurtenissen voor Adobe Commerce &#x200B;](https://developer.adobe.com/commerce/extensibility/events/)
- [&#x200B; Vormende Gebeurtenissen voor Adobe Commerce &#x200B;](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [&#x200B; Plaatsende Admin UI SDK &#x200B;](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [&#x200B; Omzettend een uitbreiding in app &#x200B;](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-bronnen

- [&#x200B; Commerce App Builder Overzicht &#x200B;](https://developer.adobe.com/commerce/extensibility/app-development/)
- [&#x200B; Vestigings API Net voor Adobe Developer App Builder &#x200B;](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [&#x200B; het Opstellen van App Builder apps &#x200B;](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [&#x200B; CI/CD voor App Builder apps &#x200B;](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Aan de slag met App Builder/Developer Console
   - [&#x200B; Aan de slag met App Builder &#x200B;](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [&#x200B; Begrijpend Projecten en Werkruimten &#x200B;](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] referenties

Voordat u een extensie kunt installeren die u hebt aangeschaft van [!DNL Commerce Marketplace] , meldt u zich aan bij uw [!DNL Commerce] -account en controleert u of u een actieve toegangssleutel hebt. U kunt binnen aan uw [!DNL Commerce] rekening van de kopbal van [[!DNL Marketplace]][1] of [ Magento.com ][6] ondertekenen.

Uw toegangssleutel is een reeks openbare en persoonlijke sleutels die wordt gebruikt om uw [!DNL Commerce] installatie met uw [!DNL Commerce] rekening te synchroniseren en uw geloofsbrieven te verifiëren. Nadat uw account is gesynchroniseerd, moet u elke keer dat u een extensie of module installeert vanuit Commerce Marketplace, uw persoonlijke sleutel invoeren of de installatie van [!DNL Commerce] upgraden.

U kunt meerdere toegangstoetsen maken voor verschillende doeleinden en deze naar wens in- of uitschakelen. U moet echter dezelfde toegangstoets gebruiken als waarmee de software van [!DNL Commerce] is geïnstalleerd. U kunt bijvoorbeeld geen Magento Open Source-toegangstoets gebruiken om Adobe Commerce bij te werken of bij te werken, of omgekeerd. U kunt ook geen toegangstoets gebruiken die tot een andere gebruiker of één behoort die van a [&#x200B; gedeelde rekening &#x200B;](commerce-account-share.md) is.

### Een toegangstoets maken

1. Meld u aan bij uw [!DNL Commerce] -account.

1. Kies op de pagina _[!UICONTROL My Account]_&#x200B;de tab **[!UICONTROL Marketplace]**.

1. Klik in de rechterbovenhoek naast uw naam op de pijl omlaag en kies **[!UICONTROL My Profile]** .

   ![&#x200B; Uw [!DNL Marketplace] profiel &#x200B;](./assets/marketplace-profile.png){width="600"}

1. Klik op de tab _[!UICONTROL Marketplace]_&#x200B;onder&#x200B;_[!UICONTROL My Products]_ op **[!UICONTROL Access Keys]** en voer een van de volgende twee handelingen uit:

   - Controleer of je al een set toegangstoetsen hebt voor je aankopen op Marketplace. U kunt meerdere sets toegangstoetsen maken voor verschillende doeleinden.

   ![&#x200B; Sleutels van de Toegang &#x200B;](./assets/access-keys.png){width="600"}

   - Klik op **[!UICONTROL Create a New Access Key]**. Voer een naam in voor het nieuwe sleutelpaar en klik op **[!UICONTROL OK]** . Geldige tekens zijn hoofdletters en kleine letters en koppeltekens in plaats van spaties.

1. Klik op **[!UICONTROL OK]** als de bewerking is voltooid.

   De nieuwe toegangssleutel wordt toegelaten en verschijnt in de lijst.

   Merk op de _verbinding van het 0&rbrace; Exemplaar &lbrace;na elke openbare en privé sleutel._ In de volgende stap kopieert en plakt u deze waarden om uw winkel te synchroniseren met Commerce Marketplace.

## Installatieproces

>[!IMPORTANT]
>
>Beginnend met Adobe Commerce en Magento Open Source 2.4.0, wordt de Tovenaar van de Opstelling van het Web verwijderd, en u moet de bevellijn gebruiken om [&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=nl-NL) te installeren of [&#x200B; verbetering &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html?lang=nl-NL) uw instantie.  Dit vereiste omvat ook [&#x200B; modules &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=nl-NL) en [&#x200B; uitbreidingen &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=nl-NL).

Het installatieproces voor [!DNL Marketplace] aankopen is verschillend voor _op-gebouw_ installaties van Commerce dan voor installaties die op [ worden ontvangen de Architectuur van de Wolk van Adobe ][4].

![&#x200B; Commerce Marketplace &#x200B;](./assets/marketplace.png){width="600"}

## Ondersteuning

Als u hulp bij het installeren of met het gebruiken van een uitbreiding nodig hebt, kijk eerst in de documentatie die de uitbreiding vergezelt. Als u het antwoord op uw vraag niet kunt vinden, gebruikt u de contactgegevens in de lijst met extensies om rechtstreeks contact op te nemen met de ontwikkelaar. Als wat u op Marketplace koopt niet aan uw behoeften voldoet, kunt u [&#x200B; om een terugbetaling verzoeken &#x200B;](#refund-requests) binnen 25 dagen na de datum van aankoop. Adobe herziet alle verzoeken om terugbetaling en geeft (indien goedgekeurd) de juiste terugbetaling uit. Voor problemen met betrekking tot Commerce Marketplace:

Methode 1: Ga naar [&#x200B; de Marketplace van Adobe Commerce &#x200B;](https://commercemarketplace.adobe.com/), navigeer aan de bodem van de pagina en klik [!UICONTROL Contact Us] die een vorm zal openen om een kaartje voor te leggen.

Methode 2: [&#x200B; E-mailsteun &#x200B;](mailto:commercemarketplacesupport@adobe.com).

### Afhandelingsproblemen

De adresvelden in uw accountprofiel moeten worden ingevuld voor verificatiedoeleinden in het aankoopsysteem voor Markttoegang.

1. Voeg de adresvelden toe aan uw Marketplace-accountprofiel.
1. Sla het bijgewerkte profiel op.
1. Ga door met het afrekenen.

### Aanmeldingsproblemen

Aanmeldingsproblemen hebben doorgaans betrekking op een onjuiste combinatie van uw MAGEID en e-mailadres in de accountdatabase. Neem contact op met de ondersteuning van de marktplaats.

>[!INFO]
>
>De aankopen van de toepassing en van de uitbreiding kunnen niet [&#x200B; worden overgebracht &#x200B;](#purchase-transfers) naar een nieuwe rekening.

### Bronvragen openen

Het team van de Steun van de Marktplaats lost kwesties met betrekking tot [&#x200B; handelsemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) en [&#x200B; handelsontwikkelaar.adobe.com/](https://commercedeveloper.adobe.com/) slechts plaatsen op. Gelieve te richten vragen over Magento Open Source aan het [&#x200B; Communautaire Forum &#x200B;](https://community.magento.com/) of [&#x200B; contact een partner &#x200B;](https://business.adobe.com/nl/products/magento/partners.html) die met Magento Open Source kan helpen.

### Terugbetalingsaanvragen

Als u een terugbetaling wilt aanvragen voor een aankoop op een Marketplace, meldt u zich aan bij uw account en voert u de volgende stappen uit:

1. Klik [!UICONTROL **Mijn Profiel**] > [!UICONTROL **Geschiedenis van de Aankoop**].
1. Bepaal de plaats van de aankoop en klik [!UICONTROL **Verzoek om een Terugbetaling**].
1. Vul het formulier voor de terugbetalingsopdracht in.

Marketplace Support vraagt om informatie nadat het verzoek om terugbetaling is gegenereerd. De terugbetalingsoptie is 25 dagen na de aankoopdatum beschikbaar. Zie de [&#x200B; Overeenkomst van de Klant van de Marketplace &#x200B;](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Facturen bestellen

U kunt de facturen van de orde van de [!UICONTROL **Geschiedenis van de Aankoop**] in uw rekening van de Marketplace downloaden. De factuur levert de BTW of het adres van de verkoper niet, omdat dit momenteel geen marktverplichting is.

Als u een bestelfactuur wilt downloaden voor een aankoop in een handelsplaats, meldt u zich aan bij uw Marketplace-account en voert u de volgende stappen uit:

1. Klik [!UICONTROL **Mijn Profiel**] > [!UICONTROL **Geschiedenis van de Aankoop**].
1. Zoek de aankoop.
1. Klik op het printerpictogram in de rechterbovenhoek van de volgorde.

### Inkoopoverdrachten

Het marktondersteuningsteam heeft niet de mogelijkheid om aankopen naar een andere account over te dragen. U moet alle apps en extensies aanschaffen op de primaire Commerce-account om installatie- en implementatieproblemen te voorkomen. Adobe Commerce heeft recht op één unieke identificatiecode. Aangezien Composer voor installatie wordt gebruikt, slechts kan één reeks [&#x200B; toegangssleutels &#x200B;](#create-an-access-key) verbonden aan de primaire rekening worden gebruikt. De enige beschikbare oplossing is om [&#x200B; een terugbetaling &#x200B;](#refund-requests) van de de kooprekening van de Marktplaats te verzoeken (als toegestaan door het terugbetalingsbeleid van Adobe Commerce).

U kunt [&#128279;](commerce-account-share.md) een instantie van Commerce door de primaire rekening delen. Gedeelde toegang verleent speciale toestemmingen aan een ondergeschikte rekening van een primaire rekening. Het gedeelde toegangspunt wordt gegenereerd van de primaire account. De primaire account kan de Commerce-account, de hoofdzakelijke account of een account zijn die binnen een organisatie wordt gedeeld.

Deze speciale machtigingen verlenen Adobe Commerce hetzelfde toegangsniveau als de primaire rechten, maar ze worden niet overgedragen naar Adobe Commerce Marketplace of Developer Portal. Dit betekent dat het kopen van een extensie van een ondergeschikte rekening op de Marketplace niet kan worden gedeeld met de primaire account. Gedeelde toegang is een eenrichtingsweg (primair account dat ondergeschikt is). Het werkt niet wanneer een ondergeschikte account probeert terug te delen naar de primaire account.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/nl/products/magento/magento-commerce.html
