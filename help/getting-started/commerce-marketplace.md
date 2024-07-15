---
title: '[!DNL Adobe Commerce Marketplace]'
description: Leer over  [!DNL Commerce Marketplace], die verkopers een gekromde selectie van oplossingen aanbiedt, en gekwalificeerde ontwikkelaars de hulpmiddelen, het platform, en de eerste plaats verstrekt om een het bloeien zaken te bouwen.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 20e1439810891b0d19cda62cc2646701ec5a778c
workflow-type: tm+mt
source-wordcount: '1264'
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

- [ Vestigings I/O Gebeurtenissen voor Adobe Commerce ](https://developer.adobe.com/commerce/extensibility/events/)
- [ Vormende Gebeurtenissen voor Adobe Commerce ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [ Vestiging Admin UI SDK ](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [ Omzettend een uitbreiding in app ](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-bronnen

- [ Commerce App Builder Overzicht ](https://developer.adobe.com/commerce/extensibility/app-development/)
- [ Vestigings API Net voor Adobe Developer App Builder ](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [ het Opstellen van App Builder apps ](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [ CI/CD voor App Builder apps ](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Aan de slag met App Builder/Developer Console
   - [ Aan de slag met App Builder ](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [ Begrijpend Projecten en Werkruimten ](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] referenties

Voordat u een extensie kunt installeren die u hebt aangeschaft van [!DNL Commerce Marketplace] , meldt u zich aan bij uw [!DNL Commerce] -account en controleert u of u een actieve toegangssleutel hebt. U kunt binnen aan uw [!DNL Commerce] rekening van de kopbal van [[!DNL Marketplace]][1] of [ Magento.com ][6] ondertekenen.

Uw toegangssleutel is een reeks openbare en persoonlijke sleutels die wordt gebruikt om uw [!DNL Commerce] installatie met uw [!DNL Commerce] rekening te synchroniseren en uw geloofsbrieven te verifiëren. Nadat uw account is gesynchroniseerd, moet u telkens uw persoonlijke sleutel invoeren wanneer u een extensie of module installeert vanuit de Commerce Marketplace of wanneer u de [!DNL Commerce] -installatie bijwerkt.

U kunt meerdere toegangstoetsen maken voor verschillende doeleinden en deze naar wens in- of uitschakelen. U moet echter dezelfde toegangstoets gebruiken als waarmee de software van [!DNL Commerce] is geïnstalleerd. U kunt bijvoorbeeld geen toegangssleutel voor Magento Open Sourcen gebruiken om Adobe Commerce bij te werken of bij te werken, of omgekeerd. U kunt ook geen toegangstoets gebruiken die tot een andere gebruiker of één behoort die van a [ gedeelde rekening ](commerce-account-share.md) is.

### Een toegangstoets maken

1. Meld u aan bij uw [!DNL Commerce] -account.

1. Kies op de pagina _[!UICONTROL My Account]_de tab **[!UICONTROL Marketplace]**.

1. Klik in de rechterbovenhoek naast uw naam op de pijl omlaag en kies **[!UICONTROL My Profile]** .

   ![ Uw [!DNL Marketplace] profiel ](./assets/marketplace-profile.png){width="600"}

1. Klik op de tab _[!UICONTROL Marketplace]_onder_[!UICONTROL My Products]_ op **[!UICONTROL Access Keys]** en voer een van de volgende twee handelingen uit:

   - Controleer of je al een set toegangstoetsen hebt voor je aankopen op Marketplace. U kunt meerdere sets toegangstoetsen maken voor verschillende doeleinden.

   ![ Sleutels van de Toegang ](./assets/access-keys.png){width="600"}

   - Klik op **[!UICONTROL Create a New Access Key]**. Voer een naam in voor het nieuwe sleutelpaar en klik op **[!UICONTROL OK]** . Geldige tekens zijn hoofdletters en kleine letters en koppeltekens in plaats van spaties.

1. Klik op **[!UICONTROL OK]** als de bewerking is voltooid.

   De nieuwe toegangssleutel wordt toegelaten en verschijnt in de lijst.

   Merk op de _verbinding van het 0} Exemplaar {na elke openbare en privé sleutel._ In de volgende stap kopieert en plakt u deze waarden om de winkel te synchroniseren met de Commerce Marketplace.

## Installatieproces

>[!IMPORTANT]
>
>Beginnend met Adobe Commerce en Magento Open Source 2.4.0, wordt de Tovenaar van de Opstelling van het Web verwijderd, en u moet de bevellijn gebruiken om ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) te installeren of [ verbetering ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) uw instantie. [ Dit vereiste omvat ook [ modules ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) en [ uitbreidingen ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Het installatieproces voor [!DNL Marketplace] aankopen is verschillend voor _op-gebouw_ installaties van Commerce dan voor installaties die op [ worden ontvangen de Architectuur van de Wolk van de Adobe ][4].

![ Commerce Marketplace ](./assets/marketplace.png){width="600"}

## Ondersteuning

Als u hulp bij het installeren of met het gebruiken van een uitbreiding nodig hebt, kijk eerst in de documentatie die de uitbreiding vergezelt. Als u het antwoord op uw vraag niet kunt vinden, gebruikt u de contactgegevens in de lijst met extensies om rechtstreeks contact op te nemen met de ontwikkelaar. Als wat u op Marketplace koopt niet aan uw behoeften voldoet, kunt u [ om een terugbetaling verzoeken ](#refund-requests) binnen 25 dagen na de datum van aankoop. De Adobe herziet alle terugbetalingsverzoeken en geeft (indien goedgekeurd) de juiste terugbetaling uit. Voor kwesties met betrekking tot Commerce Marketplace, contacteer [ Steun ](mailto:commercemarketplacesupport@adobe.com).

### Afhandelingsproblemen

De adresvelden in uw accountprofiel moeten worden ingevuld voor verificatiedoeleinden in het aankoopsysteem voor Markttoegang.

1. Voeg de adresvelden toe aan uw Marketplace-accountprofiel.
1. Sla het bijgewerkte profiel op.
1. Ga door met het afrekenen.

### Aanmeldingsproblemen

Aanmeldingsproblemen hebben doorgaans betrekking op een onjuiste combinatie van uw MAGEID en e-mailadres in de accountdatabase. Neem contact op met de ondersteuning van de marktplaats.

>[!INFO]
>
>De aankopen van de toepassing en van de uitbreiding kunnen niet [ worden overgebracht ](#purchase-transfers) naar een nieuwe rekening.

### Bronvragen openen

Het team van de Steun van de Marktplaats lost kwesties met betrekking tot [ handelsemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) en [ handelsontwikkelaar.adobe.com/](https://commercedeveloper.adobe.com/) slechts plaatsen op. Gelieve te richten vragen over Magento Open Source aan het [ Communautaire Forum ](https://community.magento.com/) of [ contact een partner ](https://business.adobe.com/products/magento/partners.html) die met Magento Open Source kan helpen.

### Terugbetalingsaanvragen

Als u een terugbetaling wilt aanvragen voor een aankoop op een Marketplace, meldt u zich aan bij uw account en voert u de volgende stappen uit:

1. Klik [!UICONTROL **Mijn Profiel**] > [!UICONTROL **Geschiedenis van de Aankoop**].
1. Bepaal de plaats van de aankoop en klik [!UICONTROL **Verzoek om een Terugbetaling**].
1. Vul het formulier voor de terugbetalingsopdracht in.

Marketplace Support vraagt om informatie nadat het verzoek om terugbetaling is gegenereerd. De terugbetalingsoptie is 25 dagen na de aankoopdatum beschikbaar. Zie de [ Overeenkomst van de Klant van de Marketplace ](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Facturen bestellen

U kunt de facturen van de orde van de [!UICONTROL **Geschiedenis van de Aankoop**] in uw rekening van de Marketplace downloaden. De factuur levert de BTW of het adres van de verkoper niet, omdat dit momenteel geen marktverplichting is.

Als u een bestelfactuur wilt downloaden voor een aankoop in een handelsplaats, meldt u zich aan bij uw Marketplace-account en voert u de volgende stappen uit:

1. Klik [!UICONTROL **Mijn Profiel**] > [!UICONTROL **Geschiedenis van de Aankoop**].
1. Zoek de aankoop.
1. Klik op het printerpictogram in de rechterbovenhoek van de volgorde.

### Inkoopoverdrachten

Het marktondersteuningsteam heeft niet de mogelijkheid om aankopen naar een andere account over te dragen. U moet alle apps en extensies aanschaffen op de primaire Commerce-account om installatie- en implementatieproblemen te voorkomen. Adobe Commerce heeft recht op één unieke identificatiecode. Aangezien Composer voor installatie wordt gebruikt, slechts kan één reeks [ toegangssleutels ](#create-an-access-key) verbonden aan de primaire rekening worden gebruikt. De enige beschikbare oplossing is om [ een terugbetaling ](#refund-requests) van de de kooprekening van de Marktplaats te verzoeken (als toegestaan door het terugbetalingsbeleid van Adobe Commerce).

U kunt [ ](commerce-account-share.md) een instantie van Commerce door de primaire rekening delen. Gedeelde toegang verleent speciale toestemmingen aan een ondergeschikte rekening van een primaire rekening. Het gedeelde toegangspunt wordt gegenereerd van de primaire account. De primaire account kan de Commerce-account, de hoofdzakelijke account of een account zijn die binnen een organisatie wordt gedeeld.

Deze speciale machtigingen verlenen Adobe Commerce hetzelfde toegangsniveau als de primaire rechten, maar ze worden niet overgedragen naar Adobe Commerce Marketplace of Developer Portal. Dit betekent dat het kopen van een extensie van een ondergeschikte rekening op de Marketplace niet kan worden gedeeld met de primaire account. Gedeelde toegang is een eenrichtingsweg (primair account dat ondergeschikt is). Het werkt niet wanneer een ondergeschikte account probeert terug te delen naar de primaire account.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/products/magento/magento-commerce.html
