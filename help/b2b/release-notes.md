---
title: '[!DNL Adobe Commerce B2B] opmerkingen bij de release'
description: Herzie de versienota's voor informatie over veranderingen in  [!DNL Adobe Commerce B2B]  versies.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: b3892e2b34aae1579472f3562e479267cca2dce3
workflow-type: tm+mt
source-wordcount: '7776'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] releaseopmerkingen

In deze releaseopmerkingen voor de B2B-extensie worden aanvullingen en correcties vastgelegd die Adobe tijdens een releasecyclus heeft toegevoegd, waaronder:

![ Nieuwe ](../assets/new.svg) Nieuwe eigenschappen
![ Vaste kwestie ](../assets/fix.svg) Oplossingen en verbeteringen
![ Bekende kwestie ](../assets/bug.svg) Bekende kwesties

>[!NOTE]
>
>Zie [ de beschikbaarheid van het Product ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) voor informatie over versies van de B2B uitbreiding van Commerce die voor beschikbare versies van Adobe Commerce wordt gesteund.


## B2B 1.5.0

*30 oktober, 2024*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}
Compatibel met Adobe Commerce-versies 2.4.8-beta1, 2.4.7 tot 2.4.7-p2, 2.4.6 tot 2.4.6-p7

De B2B v1.5.0 versie omvat nieuwe eigenschappen, kwaliteitsverbeteringen, en insectenmoeilijke situaties.

### Bedrijfsbeheer

![ Nieuwe ](../assets/new.svg) **Beheer van het Bedrijf**<!--B2B-2901--> - de Handelaars kunnen de bedrijven van Adobe Commerce nu bekijken en beheren als hiërarchische organisaties door bedrijven aan aangewezen ouderbedrijven toe te wijzen. Nadat een bedrijf aan een ouder wordt toegewezen, kan de beheerder van het moederbedrijf de bedrijfrekening beheren. Alleen geautoriseerde beheergebruikers kunnen bedrijfstoewijzingen toevoegen en beheren. Voor details, zie [ bedrijfshiërarchie beheren ](manage-company-hierarchy.md).

- Voeg bedrijfstoewijzingen toe en beheer deze vanuit de nieuwe sectie *[!UICONTROL Company Hierarchy]* op de pagina *[!UICONTROL Company Account]* in Admin.

- U kunt bedrijven sorteren en filteren met de nieuwe instelling *[!UICONTROL Company Type]* . In het net van Bedrijven, wijst de *[!UICONTROL Company Type]* kolom erop of een bedrijf een individueel bedrijf of een deel van organisatorische hiërarchie (ouder of kind) is.

![ Nieuw ](../assets/new.svg) **beheert bedrijfconfiguratie bij schaal**<!--B2B-2849--> - verander snel de montages van de bedrijfconfiguratie voor geselecteerde bedrijven gebruikend de *[!UICONTROL Change company setting]* bulkactie nu beschikbaar wanneer het beheren van bedrijven van het *[!UICONTROL Companies]* of *[!UICONTROL Company Hierarchy]* net. Als u bijvoorbeeld een nieuwe gedeelde catalogus voor een groep bedrijven maakt, kunt u de configuratie van de gedeelde catalogus in één actie wijzigen in plaats van elk bedrijf afzonderlijk te bewerken.

![ de Nieuwe ](../assets/new.svg) API Ontwikkelaars kunnen het nieuwe eindpunt van de Relaties van het Bedrijf REST API `/V1/company/{parentId}/relations` gebruiken om, bedrijftaken tot stand te brengen te bekijken en te verwijderen. Zie [ bedrijfvoorwerpen beheren ](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) in de *Gids van de Ontwikkelaar van het Web API*.

### Bedrijfsrekeningen

![ Nieuw ](../assets/new.svg)<!--B2B-2828--> **multi-bedrijf taak** - vereenvoudig de toegang van de bedrijfrekening voor bedrijfgebruikers door een gebruiker aan veelvoudige bedrijven toe te wijzen. Als je bijvoorbeeld een koper hebt die bestelt van meerdere bedrijfssites, maak dan één account en ken alle bedrijven waar de koper mee werkt aan die account. Vervolgens kan de koper zich één keer aanmelden en schakelen tussen bedrijfsaccounts door het bedrijf in de winkel te kiezen.

>[!NOTE]
>
>Een bedrijfgebruiker kan aan veelvoudige bedrijven worden toegewezen, maar zij kunnen de bedrijfbeheerder voor slechts één bedrijf zijn.

![ Nieuw ](../assets/new.svg) <!--B2B-2747--> **het werkingsgebiedselecteur van het Bedrijf** - verstrekt capaciteit voor bedrijfgebruikers die aan veelvoudige bedrijven worden toegewezen om bedrijven op de storefront te veranderen. Wanneer het werkingsgebied wordt geschakeld, werken de gegevens bij om de informatie te tonen die op de nieuwe bedrijfcontext wordt gebaseerd. Als het nieuwe bedrijf bijvoorbeeld een andere gedeelde catalogus gebruikt, ziet de gebruiker van het bedrijf producten, prijzen en andere informatie op basis van de nieuwe gedeelde catalogus. Content related to orders, quotes, quote templates also updates based on the context of the selected company.

>[!NOTE]
>
>Als de gebruiker van het bedrijf van bedrijven met punten in het winkelwagentje overschakelt, werk het karretje bij om productassortiment, de tarifering en de promotionele kortingen op basis van de nieuwe bedrijfcontext te weerspiegelen.

![](../assets/fix.svg)<!--ACP2E-1933--> `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`

### Quotes and Quote Templates

Verbeteringen in de mogelijkheden om offertes te citeren helpen kopers en verkopers om offertes effectiever te beheren en om offertes te schrijven.

![ Nieuwe ](../assets/new.svg) **malplaatjes van het Citaat** -<!--B2B-3367--> de Kopers en de verkopers kunnen het citaatproces nu stroomlijnen door herbruikbare en klantgerichte citaatmalplaatjes te creëren. Met behulp van offertesjablonen kan het onderhandelingsproces voor offertes eenmaal worden voltooid en kunnen kopers vooraf goedgekeurde gekoppelde offertes genereren voor terugkerende bestellingen in plaats van voor elke bestelling het onderhandelingsproces voor offertes te doorlopen. Aanhalingssjablonen breiden de bestaande functionaliteit voor aanhalingstekens uit door de volgende geavanceerde functies toe te voegen:

- **de drempels van de Orde** staan verkopers toe om minimum en maximumorderverplichtingen te bepalen, die de koper verzekeren aan overeengekomen-op koopgevolume.
- **plaatsende minimum en maximumhoeveelheden van de puntorde** voorziet de koper van de flexibiliteit om ordehoeveelheden op het verbonden citaat aan te passen zonder een nieuw malplaatje of verdere onderhandeling te vereisen.
- **spoor het aantal verbonden citaten die en met succes voltooide orden** worden geproduceerd om inzichten in de naleving van onderhandelde overeenkomsten te bereiken.
- ****

![](../assets/new.svg)****

- **bijgewerkte de regels van de Lijst van het Toegangsbeheer van Commerce (ACL)** staan B2B managers en supervisors toe om citaten en citaatmalplaatjes van ondergeschikte gebruikers te beheren. De afzonderlijke regels steunen korrelige configuratie voor mening, geef, en schrap toegang uit.

- **sparen Citaat als Ontwerp**<!--B2B-2566--> - wanneer het creëren van a [ citaat verzoek ](quote-request.md) van het het winkelwagentje, kunnen de kopers het citaat nu opslaan als ontwerp zodat zij het kunnen herzien en bijwerken alvorens het proces van de citaatonderhandeling met de verkoper in werking te stellen. Het conceptaanhalingsteken heeft geen vervaldatum. Kopers kunnen conceptobjecten vanuit de sectie [!UICONTROL My Quotes] van hun accountdashboard bekijken en bijwerken.

- **noem Citaat**<!--B2B-2596--> anders - de Kopers kunnen een citaatnaam van de [ de detailpagina van het Citaat ](account-dashboard-my-quotes.md#quote-actions) nu veranderen door de **[!UICONTROL Rename]** optie te selecteren. Deze optie is beschikbaar voor geautoriseerde kopers wanneer ze de prijsopgave bewerken. Gebeurtenissen van de naamwijziging worden opgenomen in het logboek met offertegeschiedenis.

- **Dubbele Citaat**<!--B2B-2701--> - de Kopers en de verkopers kunnen een nieuw citaat nu tot stand brengen door een bestaand citaat te kopiëren. Een exemplaar wordt gecreeerd van de het detailmening van het Citaat door **[!UICONTROL Create Copy]** op de [ het detailmening van het Citaat ](quote-price-negotiation.md#button-bar) in Admin of [ Storefront ](account-dashboard-my-quotes.md#quote-actions) te selecteren.

- **het citaat van de beweging citeert punt aan aanvraaglijst**<!--B2B-2755--> - de Kopers hebben nu de flexibiliteit om producten uit een citaat te verwijderen en hen te bewaren aan een verzoeklijst als zij beslissen om hen niet in het proces van de citaatonderhandelingen te omvatten.

- **verwijder veelvoudige producten uit a citaat**<!--B2B-2881--> - op citaten met een groot aantal producten, kunnen de kopers veelvoudige producten uit het citaat nu verwijderen door hen te selecteren en de *[!UICONTROL Remove]* optie van de *[!UICONTROL Actions]* controle op de de detailpagina van het Citaat te gebruiken. In vorige releases moest een koper de producten één voor één verwijderen.

- **het punt van de Lijn disconteren**<!--B2B-2597--> - tijdens citaatonderhandeling, kunnen de verkopers sluiten van de puntkorting van de lijn voor meer flexibiliteit gebruiken wanneer het toepassen van kortingen tijdens het proces van de citaatonderhandeling. Een verkoper kan bijvoorbeeld een korting op een speciaal regelobject toepassen op een object en het object vergrendelen om verdere kortingen te voorkomen. Wanneer een item is vergrendeld, kan de objectprijs niet worden bijgewerkt wanneer een korting op prijsniveau wordt toegepast. Zie [ citaat van de Initiatie voor een koper ](sales-rep-initiates-quote.md).

![ Vaste kwestie ](../assets/fix.svg) **Vormen voor bestaande citaatmogelijkheden**

- Wanneer verkopers op de knop *[!UICONTROL Print]* klikken in de gedetailleerde weergave van het citaat in Admin, wordt nu gevraagd het citaat op te slaan als een PDF. Eerder werden handelaren omgeleid naar een pagina met aanhalingsgegevens. <!--ACP2E-1984-->

- Eerder bij het verzenden van een aanhalingsteken van de klant met `0` percentage en het wijzigen van het aantal, genereert de beheerder een uitzondering, maar wordt het aantal opgeslagen. Nadat deze correctie is toegepast, wordt de uitzondering `0 percentage` right met een bericht gegenereerd. <!--ACP2E-1742-->

- Tijdens prijsonderhandelingen kan een verkoper nu een `0%` korting opgeven in het veld Offerteprijskorting voor onderhandelde offerte en de prijsopgave terugsturen naar de koper. Als de verkoper eerder een korting van 0% heeft ingevoerd en het prijsopgave heeft teruggestuurd naar de koper, heeft de beheerder een foutbericht van `Exception occurred during quote sending` geretourneerd. <!--ACP2E-1742-->

- De validatie van ReCaptcha werkt nu correct tijdens het afrekenen voor een B2B citaat wanneer ReCaptcha V3 voor storefront afhandeling wordt gevormd. Eerder is de validatie mislukt met een `recaptcha validation failed, please try again` -foutbericht.  <!--ACP2E-2097-->

### Aankooporders

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1825--> de orden van de Aankoop kunnen niet meer door een gebruiker worden geplaatst verbonden aan het bedrijf nadat het bedrijf is geblokkeerd. Eerder had een gebruiker die banden had met het bedrijf kooporders kunnen plaatsen wanneer het bedrijf werd geblokkeerd.

## B2B v1.4.2-p3

*8 Oktober, 2024*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p3+ en 2.4.6-p8+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB24-73 ](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

>[!IMPORTANT]
>
>Adobe Commerce B2B versie 1.4.2+ is compatibel met PHP 8.2. Als u de Commerce-instantie upgradet naar versie 2.4.7+, moet u ervoor zorgen dat de instantie PHP versie 8.2 gebruikt om compatibiliteit met de Adobe Commerce B2B-release te behouden. Bovendien, steunt de B2B 1.4.2+ versie niet de [ Server van de Toepassing van GraphQL ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.2-p2

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p2+ en 2.4.6-p7+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de moeilijke situaties van de Veiligheid die in Bulletin xxxx van de Veiligheid worden gedocumenteerd.

>[!IMPORTANT]
>
>Adobe Commerce B2B versie 1.4.2+ is compatibel met PHP 8.2. Als u de Commerce-instantie upgradet naar versie 2.4.7+, moet u ervoor zorgen dat de instantie PHP versie 8.2 gebruikt om de compatibiliteit met Adobe Commerce B2B-versie te behouden. Bovendien, steunt de B2B 1.4.2+ versie niet de [ Server van de Toepassing van GraphQL ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.2-p1

*9 augustus, 2024*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p1+ en 2.4.6-p6+ de versies van het veiligheidspatch.

>[!IMPORTANT]
>
>Adobe Commerce B2B versie 1.4.2+ is compatibel met PHP 8.2. Als u de Commerce-instantie upgradet naar versie 2.4.7+, moet u ervoor zorgen dat de instantie PHP versie 8.2 gebruikt om de compatibiliteit met Adobe Commerce B2B-versie te behouden. Bovendien, steunt B2B 1.4.2+ momenteel niet de [ Server van de Toepassing van GraphQL ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.2

*10 oktober, 2023*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

De B2B versie 1.4.2 bevat kwaliteitsverbeteringen en gecorrigeerde softwarefouten.

![](../assets/fix.svg) <!--B2B-2897-->Probleem opgelost Als een verkoper een offerte van een koper maakt met een SKU van het product die niet beschikbaar is in de gedeelde catalogus die aan het koperbedrijf is gekoppeld, wordt de foutmelding `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`weergegeven in het systeem .  Verkoper kan de offerte pas opslaan als hij het product heeft verwijderd dat niet beschikbaar is. Voorheen werd de offerte opgeslagen met de niet-beschikbare SKU opgenomen en kon de offerte niet op de etalage worden geladen.

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ is compatible with PHP 8.2. If you upgrade the Commerce instance to version 2.4.7+, ensure that the instance uses PHP version 8.2 to maintain compatibility with Adobe Commerce B2B release. [](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)

## B2B v1.4.1

**

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}[ Adobe Commerce 2.4.6-p2 ](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1.

De versie B2B v1.4.1 bevat kwaliteitsverbeteringen en oplossingen voor problemen.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1825--> de orden van de Aankoop kunnen niet meer door een gebruiker worden geplaatst verbonden aan het bedrijf nadat het bedrijf is geblokkeerd. Previously, a user associated with the company could place purchase orders when the company was blocked.

![](../assets/fix.svg)<!--ACP2E-1943--> Previously, products that were available for shipment were incorrectly identified as backordered.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1862--> als de vorm van de bedrijfregistratie een attribuut van het type van klantendossier omvat, is het dossier dat tijdens het registratieproces wordt geupload nu inbegrepen in de rekeningsinformatie voor de Beheerder van het Bedrijf nadat het bedrijf wordt gecreeerd. Eerder ontbrak de bijlage.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1793--> De monsterselecteur voor een configureerbaar product wordt nu getoond zoals verwacht in de pagina van de het puntconfiguratie van de verzoeklijst. Eerder, werd de monsterselecteur getoond als dropdown gebied in de pagina van de de puntconfiguratie van de verzoeklijst.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1968--> wanneer het gebruiken van de [ vraag van GraphQL van het Bedrijf ](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) om bedrijfdetails terug te keren, zijn de resultaten nu met succes zonder fout teruggekeerd.

## B2B v1.4.0

*13 Juni, 2023*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}[ Adobe Commerce 2.4.6-p1 ](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1

Deze release bevat nieuwe mogelijkheden en verbeteringen voor B2B-onderhandelbare aanhalingstekens en meerdere opgeloste problemen.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-bèta1.

![ Nieuwe ](../assets/new.svg) **Verkoper stelde citaten** in werking - de verkopers kunnen een citaat voor een koper direct van het Citaat en de netten van de Klant in Admin nu in werking stellen. Dit vermogen stroomlijnt het prijsverhogingsproces en vermindert ingewikkeldheid voor klanten. Als een klant geen bestelling heeft geïnitieerd, kan een verkoper snel een prijsopgave namens de klant maken en het onderhandelingsproces starten. Eerder konden prijsopgaven alleen door de koper of door een verkoper die zich als klant heeft aangemeld, van de winkel worden gemaakt.

![ Nieuwe ](../assets/new.svg) **het puntkortingen van de Lijn en onderhandeling** - <!--B2B-2440--> Binnen een citaat, kunnen de B2B kopers en verkopers nu op het niveau van het lijnpunt onderhandelen, die kortingen toepassen en nota&#39;s ruilen tot een overeenkomst wordt bereikt. De verwezenlijking van de nota en de updates zijn inbegrepen in het lijnpunt en citaatgeschiedenis om mededeling te volgen. Eerder konden kopers en verkopers alleen opmerkingen uitwisselen en kortingen toepassen op het prijsniveau.

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu correcte details tijdens betaling wanneer de optie van de Orden van de Aankoop wordt toegelaten en een virtueel citaat dat met de PayPal betalingsoptie werd gecreeerd is geselecteerd. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1504--> de fouten van de Bevestiging komen niet meer voor wanneer u probeert om een bedrijf met een kredietgrens te bewaren die 999 overschrijdt. Eerder, voor bedrijfskredietgrenzen groter dan 999, nam de handel van de Adobe een komma separator op, die een bevestigingsfout veroorzaakte die updates verhinderde worden bewaard.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1474--> het geselecteerde verschepende adres blijft nu onveranderd wanneer u een orde met een onderhandelbaar citaat plaatst. Eerder, toen u een bestelling plaatste, werd het geselecteerde verzendadres veranderd in het standaardverzendadres.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1429--> in de montages van de Configuratie van de Opslag voor Eigenschappen B2B, wordt het **[!UICONTROL Enable Shared Catalog direct products price assigning]** gebied nu automatisch onbruikbaar gemaakt. In de winkel is deze verborgen wanneer de instelling **[!UICONTROL Enable Company]** of **[!UICONTROL Enable Shared Catalog]** is ingesteld op **[!UICONTROL No]** .

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1683--> wanneer het creëren van een bedrijfrekening van de storefront, bevestigt Commerce nu het e-mailadres alvorens de bedrijfregistratie te verwerken. Als het e-mailadres ongeldig is, mislukt de bewerking en worden geen accountupdates verwerkt. Eerder werd een klantenrekening gecreeerd zelfs als het verzoek om een bedrijfrekening tot stand te brengen wegens een ongeldig e-mailadres ontbrak.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1664--> Product SKUs die dubbele aanhalingstekens in de Gedeelde Catalogus en het tarief structuur omvatten veroorzaakt niet meer fouten in Admin.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1498--> Bijgewerkt de configuratie van de Varnish voor de toepassing van Commerce om de gebruikers van de Gast te verhinderen gegevens van andere klantengroepen te zien.

### Bekend probleem

Als u installeert of B2B 1.4.0 op [ versie 2.4.6-p1 van Adobe Commerce ](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) bevordert, komt de volgende fout voor:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

U kunt deze kwestie bevestigen door handgebiedsdelen voor het B2B veiligheidspakket toe te voegen door handgebiedsdelen voor het B2B veiligheidspakket met a [ stabiliteitsmarkering ](https://getcomposer.org/doc/04-schema.md#package-links) toe te voegen. Voor instructies, zie de [ Kennisbank van Adobe Commerce ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5-p8

*8 Oktober, 2024*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met de de veiligheidsflardversies van Adobe Commerce 2.4.6-p8.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB24-73 ](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

## B2B v1.3.5-p7

*9 augustus, 2024*

[!BADGE ]{type=Informative tooltip="Supported"}

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met de de veiligheidsflardversies van Adobe Commerce 2.4.6-p7.

## B2B v1.3.5

*Maart 14, 2023*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) vrijgekomen B2B versie 1.3.5-p2 om verenigbaarheid met Adobe Commerce 2.4.6-p2 te steunen.

![Nieuwe](../assets/new.svg) versie B2B 1.3.5-p1 ter ondersteuning van compatibiliteit met Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Nadat u Commerce hebt bijgewerkt van versie 2.4.6 naar de [nieuwste versie](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), moet u een update uitvoeren naar de ondersteunde patchversie voor B2B 1.3.5. Of u kunt de B2B-extensie bijwerken van versie 1.3.5 naar versie 1.4.0 of hoger voor de nieuwste functies.

![Nieuwe](../assets/new.svg) toegevoegde ondersteuning voor Adobe Commerce 2.4.6.

![](../assets/fix.svg) <!--- ACP2E-689--> Probleem opgelost Adobe Commerce geeft nu de juiste gegevens tijdens de betaling weer wanneer de optie Inkooporders is ingeschakeld en een virtuele offerte is gemaakt met de optie PayPal betaling is geselecteerd. Previously, totals were displayed as zero under these conditions.

![](../assets/fix.svg)<!--- ACP2E-609-->****

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1244--> Het de klantenattribuut van het Belasting/van het BTW Aantal werkt nu zoals verwacht met de rekeningen van het bedrijfbeheer op zowel Admin als storefront. Custom Tax/VAT attributes are no longer required to create a company account. Eerder, toen een handelaar een ondernemingsrekening met een douaneTarief/BTW attribuut creeerde, gaf Adobe Commerce een bevestigingsfout op zowel storefront als Admin.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1236--> het onbruikbaar maken van de gedeelde cataloguseigenschap op een specifiek werkingsgebied werkt nu correct. Voorheen stelde Adobe Commerce een ongeldig bereik in toen een handelaar de configuratie van een gedeelde catalogus opsloeg.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1203--> Admin gebruikers kunnen klanten de waarden van de douaneattributen voor bedrijfgebruikers nu bewaren. Eerder konden de douanekenmerken van de klant voor bedrijfgebruikers niet worden bewaard.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1221--> De kwesties van prestaties worden opgelost met de bevestiging van bedrijftoestemmingen die door GraphQL worden verstrekt wanneer vele bedrijftoestemmingen reeds worden toegewezen.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce werpt niet meer een fout op de wortelpagina wanneer de Snelle Orde wordt gebruikt om een product in een hoeveelheid toe te voegen die beschikbare voorraad overschrijdt.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1090--> De prestaties van `SELECT` verrichtingen van bedrijftoestemmingen zijn verbeterd.

![](../assets/fix.svg)<!--- ACP2E-2456-->

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-6829--> De **[!UICONTROL Place Order]** knoop werkt nu zoals verwacht wanneer het voltooien van een aankoop met een goedgekeurd citaatverzoek. Problemen met de plug-in voor verhandelbare aanhalingstekens `negotiableQuoteCheckoutSessionPlugin` zijn opgelost.

## B2B v1.3.4-p10

*9 Oktober, 2024*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5-p10.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB24-73 ](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

## B2B v1.3.4

*9 augustus, 2022*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-453--> Adobe Commerce verzendt niet meer e-mailberichten telkens als een bestaand Bedrijf door een API vraag wordt bijgewerkt. E-mails worden nu alleen verzonden wanneer een bedrijf wordt gemaakt.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-406--> Adobe Commerce berekent nu correct een groot totaal van een onderhandelbaar citaat wanneer het **[!UICONTROL Enable Cross Border Trade]** plaatsen van de belastingberekening wordt toegelaten.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-322--> De configureerbare producten worden nu verplaatst naar de laatste positie in de productlijst nadat de voorraad wordt bijgewerkt wanneer **[!UICONTROL Move out of stock to the bottom]** het plaatsen wordt toegelaten. Er wordt een nieuwe aangepaste databasequery geïmplementeerd om ervoor te zorgen dat de sorteervolgorde voor de index van de Elasticsearch nu overeenkomt met de sorteervolgorde voor beheerders. Eerder, werden de configureerbare producten en hun kindproducten niet verplaatst naar de bodem van de lijst toen dit het plaatsen werd toegelaten.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-308--> E-mail van de Orde van de Aankoop neemt nu het e-mailverzenden van het plaatsen van elke website in een multi-plaatsplaatsing. Een controle op de instelling **[!UICONTROL Disable Email Communications]** wordt toegevoegd aan de aangepaste logica voor e-mailwachtrijen. Eerder heeft Adobe Commerce de instelling voor het verzenden van e-mail voor de secundaire website niet gerespecteerd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-302--> De titel van het gebied van SKU van de Snelle pagina van de Orde wordt veranderd voor duidelijkheid.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-543--> Adobe Commerce toont nu een meer informatief foutenbericht wanneer een verkoopster een ongeldige SKU in het **ingaat SKU of gebied van de Naam van het Product** ingaat.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1753--> het **[!UICONTROL Account Created in]** gebied voor een bedrijfbeheerder blijft nu zijn waarde zoals verwacht nadat u sparen het bedrijf.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-722 --> de `customer` vraag keert niet meer lege resultaten terug wanneer het vorderingslijsten terugwint die door `uid` worden gefiltreerd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-210 --> voegde een stop vóór de `collectQuoteTotals` vraag toe om ervoor te zorgen dat de opslagkredieten slechts eenmaal worden toegepast.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-665 --> Klanten worden nu opnieuw gericht aan de login pagina wanneer hun rekening door een beheerder van Admin wordt geschrapt. Eerder gaf Adobe Commerce een fout. Het codeblok van de plug-in (`SessionPlugin` ) bevindt zich nu in het `try…catch` -blok. Eerder, werd deze code niet verpakt binnen het generische uitzondering-behandelende blok.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-661 --> op de Snelle pagina van de Orde op mobiele wijze, het drukken **gaat** na het ingaan van een geldige productnaam binnen of SKU neemt nu de verkoopster aan het volgende gebied zoals verwacht.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-607 --> De naam van het Bedrijf is nu zichtbaar zoals verwacht in het factureren en het verschepen adressecties van het controlewerkschema.

![](../assets/fix.svg)<!--- ACP2E-375 -->**[!UICONTROL Zero Subtotal Checkout]** Previously, the Store Credit checkbox was not functional during order placement from the Admin. `The requested Payment Method is not available`

## B2B v1.3.3

*9 augustus, 2022*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.4.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41985--> de tijd die wordt vereist om van Adobe Commerce 2.3.x aan Adobe Commerce 2.4.x in plaatsingen met meer dan 100.000 bedrijfrollen te bevorderen is wezenlijk verminderd.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42153--> Het verzoek van de POST `V1/order/:orderId/invoice` steunt nu de verwezenlijking van gedeeltelijke facturen wanneer de **[!UICONTROL Payment on Account]** betalingsmethode wordt toegelaten. `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity` [](https://github.com/magento/magento2/issues/32428)

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro werkt nu zoals verwacht met B2B verhandelbaar citaat wanneer de wagentje van de klant andere producten bevat. Adobe Commerce verwerkt de bestelling nu met succes en stuurt een e-mail naar de klant zoals u had verwacht. Eerder gaf Adobe Commerce een fatale fout en stuurde een bevestigingsbericht naar de klant met daarin de nulwaarden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41819--> Paginering wordt nu correct getoond op de pagina van het resultaat van het catalogusonderzoek na het uitsluiten van sommige producten in gedeelde catalogus.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42886--> de douaneattributen van de Klant worden nu bewaard zoals verwacht wanneer het creëren van of het opslaan van een bedrijfgebruiker in Admin.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42927--> De **[!UICONTROL Submit]** knoop op de Create Nieuwe vorm van het Bedrijf wordt nu onbruikbaar gemaakt na één klik om veelvoudige vormvoorlegging te verhinderen. Eerder kon u dit formulier meerdere keren verzenden door herhaaldelijk op deze knop te klikken. Er is een fout opgetreden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce toont niet meer de reorder verbinding op de opslagplaats wanneer een verkoopster zich in een opslag registreert waarvoor reorders zijn onbruikbaar gemaakt.

![](../assets/fix.svg) <!--- MC-43115--> Probleem opgelost Snel zoeken via SKU is nu onderscheid tussen hoofdletters en kleine letters wanneer gedeelde catalogus is ingeschakeld.

![Oplossing van een probleem](../assets/fix.svg) <!--- MC-42203--> U kunt nu een bestand bijwerken voor een klantkenmerk wanneer u een bedrijf maakt. Bij eerdere pogingen om een bedrijf met een typebijlage `File`te maken, heeft Adobe Commerce het bedrijf niet gemaakt en deze fout geregistreerd in het uitzonderingslogbestand: `Something went wrong while saving file`.

![Oplossing van een probleem](../assets/fix.svg) <!--- MC-42242--> U kunt nu een bedrijf maken met een klantaccount dat een aangepast kenmerk met een (`File`) of (`Image`) type heeft. Als in vorige versies een van deze aanpasbare opties voor het account beschikbaar was, kon de paginalader voor het bedrijf niet worden opgelost, waardoor de bedrijfsgegevens niet meer kunnen worden bewerkt.

![Opgelost probleem](../assets/fix.svg) <!--- MC-42268--> De `products` query retourneert nu een nauwkeurig `total_count` veld wanneer gedeelde catalogus is ingeschakeld.

![](../assets/fix.svg)<!--- MC-42203--> `File``Something went wrong while saving file`

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-43178--> de _Configuratie van het Bedrijf_ en _creëren bedrijf_ pagina&#39;s nu werken zoals verwacht nadat u online het verschepen methode onbruikbaar maakt. Verification has been added to prevent the attempted processing of disabled Shipping modules. Eerder gaf Adobe Commerce deze fout weer: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected` .

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42214--> de _pagina van de Categorie_ toont nu verenigbare productgegevens terwijl de toestemmingen tijdens het gedeeltelijke indexeren worden geproduceerd. Aan dit proces is een nieuwe partiële index voor directorymachtigingen toegevoegd. Eerder waren de gegevens die werden weergegeven terwijl de indexeerder werd uitgevoerd onjuist.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42567--> De `categoryList` vraag keert nu het correcte aantal producten terug wanneer de catalogustoestemmingen worden gebruikt en de producten aan een gedeelde catalogus worden toegewezen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42528--> de `categoryList` vraag respecteert nu categorietoestemmingen en keert slechts toegelaten categorieën terug. Eerder, keerde het alle toegewezen en niet toegewezen categorieën terug.

![](../assets/fix.svg)<!--- MC-42399-->`rest/V1/company/{id}``is_purchase_order_enabled`

![](../assets/fix.svg)<!--- ACP2E-128-->__

![](../assets/fix.svg)<!--- ACP2E-130-->

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-133--> de Snelle fouten van de Orde worden niet meer getoond in het het winkelwagentje. Eerder, toonde Adobe Commerce deze fout in het winkelwagentje toen SKU niet in de catalogus werd gevonden: `The SKU was not found in the catalog`.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-194--> Gedeelde catalogus sparen verrichtingen zijn geoptimaliseerd om sneller uit te voeren. Het opslaan van een gedeelde catalogus met veel klantengroepen kan eerder enkele minuten in beslag nemen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce schrapt nu alle subcategorierechten van de `sharedcatalog_category_permissions` lijst wanneer de oudercategorie wordt geschrapt. Eerder werden alleen de gegevens van de bovenliggende categorie verwijderd.

## B2B v1.3.2

*Augustus 29, 2022*

[!BADGE  Gesteund ]{type=Informative tooltip="Supported"}

![](../assets/new.svg)

![](../assets/fix.svg)<!--- MC-39862--> Eerder, toen een verhandelbaar prijsopgave verstreek, heeft Adobe Commerce geen e-mails verzonden voor updates.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce verzendt nu met succes updatemails over spoedig om te verlopen en verlopen onderhandelbare citaten wanneer een `cron` baan mist.

### Bedrijf

![](../assets/fix.svg)<!--- MC-41542--> `AN`

![](../assets/fix.svg)<!--- MC-41260-->**[!UICONTROL Return]** Previously, the administrator was redirected to the Order History page.

![](../assets/fix.svg)<!--- MC-40798-->`app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply``bin/magento setup:upgrade` Previously, Adobe Commerce did not use batch size for collection when initializing permissions, but instead loaded a collection of all company roles.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40551--> De gebruikers van het Bedrijf kunnen klanten de waarden van de douaneattributen nu uitgeven en bijwerken. Eerder waren deze kenmerken niet correct gekoppeld aan het formulier voor het maken en bewerken van een gebruikersformulier. Een bedrijfgebruiker kan verschillende kenmerkwaarden invoeren, maar Adobe Commerce heeft deze waarden niet correct opgeslagen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-32653--> De middelboom voor de toestemmingen van de bedrijfrol kan nu worden vertaald zoals verwacht. Eerder was de machtigingenstructuur niet vertaald, ook al waren er geldige vertaalbestanden aanwezig.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce bewaart nu de waarden van de douaneklantenattributen voor B2B gebruikers zoals verwacht. Eerder leidde het maken van een bedrijfsaccount met aangepaste klantkenmerken tot een sjabloonfout en het formulier werd niet geladen door Adobe Commerce. Door een argument toe te voegen aan de lay-out van `company_create_account` is dit probleem opgelost.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41721--> de gebruikersfilters van het Bedrijf zoals toon Alle Gebruikers, toon Actieve Gebruikers, en toon Inactieve Gebruikers nu werken zoals verwacht. Eerder, veroorzaakte het filtreren acties op de pagina van de bedrijfgebruiker een fout van JavaScript.

### Bedrijfskrediet

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41551--> Beheerders met beperkte rekeningen die slechts website-vlakke voorrechten omvatten kunnen nu een bedrijf tot stand brengen dat een verschillende munt dan de website gebruikt.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce verzendt nu bedrijfe-mails van het correcte `from` e-mailadres en werkingsgebied. Eerder heeft Adobe Commerce geen rekening gehouden met het bereik van de website bij het verzenden van een bedrijfskrediet of het bijwerken van een e-mail.

### Quick Order

![](../assets/fix.svg)<!--- MC-42104-->

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40268--> het gebruiken van Snelle Orde aan onderzoek op veelvoudige SKUs werkt nu zoals verwacht. Eerder waren er dubbele vermeldingen in de resultaten opgenomen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40261--> de Toegevoegde de lijstvertoning van het Product behandelt nu SKUs ingegaan in kleine letters en in hoofdletters het zelfde wanneer u SKUs gebruikt om veelvoudige producten tijdens Snelle Orde te selecteren.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40225--> Gebruikend Snelle Orde voegt nu producten in de hoeveelheid toe die door de verkoopster wordt gespecificeerd. Eerder heeft Adobe Commerce slechts één product toegevoegd, zelfs als de door de winkel opgegeven hoeveelheden groter zijn dan één product.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41283--> de Snelle autocomplete eigenschap van de Orde werkt nu met gedeeltelijke SKUs.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce toont nu producten die als **niet zichtbaar individueel** op de Snelle pagina van de Orde auto-stelt lijst en onderzoeksresultaten zijn gevormd voor.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42402--> de Kopers kunnen de Snelle vorm van de Orde nu gebruiken om veelvoudige producten door SKUs toe te voegen die karakters in hoofdletters omvatten. Previously, only the first product was added.

### Negotiable quote

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41232--> De Klanten worden nu opnieuw gericht aan de onderhandelbare citaatpagina na het kleven van de verbinding aan een onderhandelbaar citaat op het gebied URL en met succes het programma openen. Eerder werd de koper doorgestuurd naar de pagina Mijn account.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39317--> die nu opnieuw rangschikt werkt zoals verwacht voor orden die een product met een Aanpasbare Optie van de Datum voor een klantenrekening bevatten die tijdens controle werd gecreeerd. Eerder heeft Adobe Commerce de reorder niet verwerkt en deze fout weergegeven: `The product has required options. Enter the options and try again` .

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39063--> Het verschepende adres voor een verhandelbaar citaat is niet meer editable tijdens controle wanneer de module van de Orde van de Aankoop wordt onbruikbaar gemaakt. Dit gedrag is het gevolg van een vorige correctie waarbij `isQuoteAddressLocked` is verwijderd uit de verhandelbare renderer voor het uitchecken van aanhalingstekens.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-38967--> De handelaren kunnen producten aan een onderhandelbaar citaat van Admin nu toevoegen.

### Aankooporders

![Het probleem](../assets/fix.svg) <!--- MC-39983--> is opgelost in Adobe Commerce toont nu een informatief foutbericht zoals verwacht wanneer u een inkooporder plaatst met PayPal Express checkout wanneer het **[!UICONTROL Name Prefix]** kenmerk is ingesteld op `required`. Voorheen heeft Adobe Commerce de bestelling niet geplaatst en er wordt geen foutbericht weergegeven.

![](../assets/fix.svg) <!--- MC-39620--> Probleem opgelost De ui-component voor het factuuradres in de module Inkooporder gebruikt nu op de juiste wijze het offerteadres wanneer Google Tag Manager is ingeschakeld. Eerder deed zich een JavaScript-fout voor op de betalingspagina.

### Lijsten van opdracht

![](../assets/fix.svg)<!--- MC-40426-->`rest/all/V1/requisition_lists` `Could not save Requisition List`

![](../assets/fix.svg)<!--- MC-41123-->**[!UICONTROL Add to Requisition List]** Als een winkelwagentje twee producten bevatte waarvan één niet op voorraad was, werd de knop _[!UICONTROL Add to Requisition List]_niet weergegeven voor beide producten.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40877--> U kunt REST API nu gebruiken om een product aan een aanvraaglijst toe te voegen.

![ Opgeloste kwestie ](../assets/fix.svg) <!--- MC-40155--> de waarden van de lijst van de Vereiste **[!UICONTROL Latest Activity Date]** houden nu aan het formaat van de scène.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce werpt niet meer een fatale fout wanneer u een bundelproduct van een verzoeklijst uitgeeft.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce toont nu de correcte productprijs wanneer u een product met een klantgerichte optie `(File)` aan een verlanglijst van een verzoeklijst toevoegt. De koppeling naar het geüploade bestand is ook zichtbaar zoals u had verwacht. Eerder gaf Adobe Commerce onjuiste productprijzen weer en werd de koppeling naar het bestand niet weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-36383--> de Producten met een klantgerichte optie `(File)` kunnen nu aan een het winkelwagentje van een verzoeklijst worden toegevoegd.

### Gedeelde catalogus

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40497--> een beheerder met een rol die tot een specifieke website wordt beperkt kan een gedeelde catalogus nu creëren, bekijken en uitgeven. Previously, Adobe Commerce threw a fatal error when an administrator with a limited role tried to create a shared catalog.

![](../assets/fix.svg)<!--- MC-41337--> Previously, only one filter could be applied, and Adobe Commerce displayed an inaccurate product count in layered navigation.

![](../assets/fix.svg)<!--- MC-40779--> Eerder gebruikte een insteekmodule voor de pagina met zoekresultaten geen Elasticsearch, maar werd een nieuwe query naar de database verzonden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce schrapt niet meer laagprijzen wanneer een handelaar alle producten van een standaard gedeelde catalogus schrapt.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39802--> Filters worden nu gefiltreerd door de huidige categorie en correct getoond op alle pagina&#39;s wanneer de gedeelde catalogi worden toegelaten. Eerder werden filters alleen voor de huidige pagina verkeerd berekend en niet door de huidige categorie gefilterd.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39522--> de vraag van GraphQL `products` keert niet meer de prijswaaier en de categorie van een product voor producten terug die niet aan een gedeelde catalogus worden toegewezen wanneer de gedeelde catalogus wordt toegelaten. Eerder gaf de query de aggregaties van het product, ook al werd het product zelf niet geretourneerd in de `items` -array.

## B2B v1.3.1

**

[!BADGE ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.2.

![](../assets/new.svg)

![](../assets/fix.svg)

![](../assets/fix.svg)

![](../assets/fix.svg)

![](../assets/fix.svg)**[!UICONTROL Website Restriction]****[!UICONTROL Restriction Mode]**`Private Sales: Login Only` <!--- MC-38934-->

![ Vaste kwestie ](../assets/fix.svg) de geschiedenis van de Orde laadt nu zoals verwacht in de pagina van het de rekeningsdashboard van een bedrijfbeheerder in plaatsingen met een B2B bedrijfshiërarchie die vele klanten (groter dan 13000) bevat. Voorheen werd de bestelhistorie langzaam of helemaal niet geladen en gaf Adobe Commerce een 503-fout weer. <!--- MC-38830-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer veelvoudige identieke waarschuwingsberichten wanneer u een niet gevormd product met klantgerichte opties aan een Lijst van de Vereiste van een pagina van de Categorie toevoegt. <!--- MC-38342-->

![ de Vaste kwestie ](../assets/fix.svg) Nieuwe en gedupliceerde producten zijn nu zichtbaar zoals verwacht op de categoriepagina wanneer B2B gedeelde catalogi worden toegelaten. <!--- MC-38307-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce handhaaft nu het correcte `store_id` dat met een bedrijfbeheerder wordt geassocieerd wanneer de klantengroep voor een bedrijf wordt bijgewerkt. Eerder is `store_id` veranderd in de standaardopslag toen de groep werd bijgewerkt. <!--- MC-38196-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce bewaart nu een gegroepeerd product aan een verzoeklijst als lijst van eenvoudige producten op de zelfde manier als het een gegroepeerd product aan een winkelwagentje toevoegt. Eerder werd vanwege de manier waarop Adobe Commerce gegroepeerde producten heeft opgeslagen, de koppeling voor een gegroepeerd product uit de aanvraaglijst altijd omgeleid naar eenvoudige producten en niet naar het gegroepeerde product. <!--- MC-38049-->

![ Vaste kwestie ](../assets/fix.svg) u kunt orden door het **[!UICONTROL Company Name]** gebied nu filtreren wanneer het uitvoeren van ordeinformatie in formaat CSV. Eerder heeft Adobe Commerce een fout aangemeld in `var/export/{file-id}` . <!--- MC-37785-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu Create popup van de Lijst van de Vergunning zoals verwacht wanneer u creeert het Create Nieuwe lusje van de Lijst van de Vergunning op de storefront selecteert. <!--- MC-37915-->

![ de Vaste lijst van de kwestie ](../assets/fix.svg) Vereiste omvat nu alle gegroepeerde producten en hoeveelheden die aan de lijst zijn toegevoegd. `1 product(s) require your attention - Options were updated. Please review available configurations`<!--- MC-37621-->

![](../assets/fix.svg) `The store view is not in the associated website`<!--- MC-37488-->

![](../assets/fix.svg)<!--- MC-37427-->

![ Vaste kwestie ](../assets/fix.svg) de **[!UICONTROL Add to Cart]** knoop wordt niet meer geblokkeerd wanneer de _[!UICONTROL Enter Multiple SKUs]_sectie van de Snelle pagina van de Orde een lege waarde bevat. In plaats daarvan geeft Adobe Commerce nu een bericht weer waarin u wordt gevraagd geldige SKU&#39;s in te voeren. <!--- MC-37387-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu dit bericht op de productpagina wanneer u een productoverzicht van een verzoeklijst indient: `You submitted your review for moderation`. De revisie wordt ook weergegeven op de pagina Revisies in behandeling (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]** ). Hoewel Adobe Commerce de revisie eerder heeft toegevoegd aan de lijst van lopende recensies, heeft het een fout van 404 op de productpagina geplaatst. <!--- MC-37119-->

![ Vaste kwestie ](../assets/fix.svg) De prestaties van de `sharedCatalogUpdateCategoryPermissions` consument zijn verbeterd. Na het creëren van een gedeelde catalogus, gebruikt de indexator van de catalogustoestemming nu slechts identiteitskaart van de klantengroep van de gedeelde catalogus, niet alle klantengroepen. <!--- MC-36770-->

![](../assets/fix.svg)<!--- MC-36630-->

![](../assets/fix.svg)`rest/V1/carts/{<CART_ID>/items` `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave` `No such shared catalog entity`<!--- MC-36535-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce verzendt nu nieuwe e-mails van de bedrijfs gebruikersregistratie van het adres van de opslag van Adobe Commerce. Eerder werd deze e-mail verzonden van het adres van de bedrijfbeheerder. <!--- MC-36480-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce controleert nu douanekenmerken voor duplicatie van gereserveerde namen van bedrijfattributen alvorens een handelaar toe te laten om een nieuw attribuut te bewaren. <!--- MC-36282-->

![ Vaste kwestie ](../assets/fix.svg) de `credit_history` vraag keert nu de gespecificeerde kredietgeschiedenis van het bedrijf voor zowel het oorspronkelijk toegewezen bedrag als het gekochte bedrag terug. Eerder heeft deze query een fout geretourneerd.

![ Vaste kwestie ](../assets/fix.svg) de **[!UICONTROL Company]** en **[!UICONTROL Job Title]** gebieden op de Edit pagina van de Informatie van de Rekening zijn niet meer editable.

### Bekende problemen

- B2B-kopers kunnen online betalingsmethoden gebruiken om de gebruikelijke inkooporderstroom te omzeilen. Dit scenario kan optreden als de koper zijn volledige afrekentotaal kan verlagen tot 0 , bijvoorbeeld met een aanbiedingscode of cadeaubon, en vervolgens de code of cadeaubon kan verwijderen. Zelfs onder die omstandigheden plaatst Adobe Commerce nog steeds de order voor het juiste bedrag op basis van de prijzen van de artikelen in de toegewezen catalogus. **_Oplossing_**: Schakel cadeaubonnen en couponcodes uit wanneer online betaalmethoden zijn ingeschakeld voor goedkeuring van inkooporders. <!--- B2B-1603-->

- Kopers worden omgeleid naar het winkelwagentje wanneer ze een bestelling proberen te plaatsen via een inkooporder met PayPal Express Checkout wanneer **[!UICONTROL In-Context Mode]** is uitgeschakeld. <!--- B2B-1604-->

- Adobe Commerce geeft soms een fout van 404 weer wanneer een koper een inkooporder maakt en vervolgens naar de afhandelingspagina navigeert. Deze fout treedt op wanneer een koper eerder een andere inkooporder met een online betalingsmethode heeft gemaakt voordat hij naar de betalingspagina navigeert zonder de vorige aankoop te voltooien. De koper kan de kooporder nog steeds plaatsen. **_werk rond_**: niets. <!--- B2B-1605-->

- Kortingen voor een specifieke betalingsmethode blijven bestaan tijdens afhandeling voor een inkooporder, zelfs als de koper zijn betalingsmethode wijzigt tijdens de laatste afhandeling. Als gevolg hiervan kunnen klanten een korting ontvangen waarop ze geen recht hebben. Deze kwestie doet zich voor omdat ondanks de wijziging in de betalingsmethode nog steeds een kartregel voor de oorspronkelijke betalingsmethode wordt toegepast. **_werk rond_**: niets. Zie [ Adobe Commerce 2.4.2 B2B bekende kwestie: de korting blijft voor online Orden van de Aankoop nadat de betalingsmethode ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _artikel van de Kennisbank_ wordt veranderd. <!-- B2B-1012 -->

- De query `deleteRequisitionListOutput` retourneert details over de verwijderde aanvraaglijst in plaats van de resterende aanvraaglijsten. <!--- MC-39894-->

## B2B v1.3.0

*15 oktober 2020*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

Deze release bevat verbeteringen voor goedkeuringen voor bestellingen, verzendmethoden, winkelwagentje en registratie van beheeracties.

![](../assets/new.svg)

![](../assets/new.svg)

![](../assets/new.svg)<!--- BUNDLE-160 161 162 -->

![ Nieuwe ](../assets/new.svg) Merchants kunnen gebruikers nu toestaan om de inhoud van hun winkelwagentje in één enkele actie te ontruimen en kunnen deze capaciteit onafhankelijk op elke website vormen <!--- BUNDLE-108 -->

![ de Nieuwe ](../assets/new.svg) B2B kopers kunnen individuele punten of de volledige inhoud van hun winkelwagentje direct aan een verzoeklijst nu toevoegen. <!--- BUNDLE-145 144-->

![ Nieuwe ](../assets/new.svg) B2B handelaren kunnen orden van Admin namens klanten tot stand brengen gebruikend Betaling op Rekening als betalingsmethode. <!--- BUNDLE-166 178-->

![ Nieuwe ](../assets/new.svg) Merchants kunnen alle citaten direct bekijken verbonden aan een gebruiker van de de detailpagina van de klant. <!--- BUNDLE-139 -->

![ Nieuwe ](../assets/new.svg) Merchants kunnen de Klanten nu Online net door Bedrijf filtreren. <!--- BUNDLE-137 -->

![](../assets/new.svg)<!--- BUNDLE-110 -->

![](../assets/new.svg)<!--- BUNDLE-154 -->

![](../assets/new.svg) `Company``NegotiableQuote``CompanyCredit``SharedCatalog`<!--- BUNDLE-180 181 182 183 -->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer de **[!UICONTROL Delete customer]** knoop op de **Klanten** pagina wanneer de het programma geopende beheerder geen rechten heeft om klanten in plaatsingen te schrappen waar B2B geïnstalleerd is. <!--- MC-35655-->

![](../assets/fix.svg)<!--- MC-35254-->

![](../assets/fix.svg)`Allow`**[!UICONTROL Display Product Prices]****[!UICONTROL Add to Cart]** `Deny``Allow`<!--- MC-34792-->

![](../assets/fix.svg)<!--- MC-34777-->

![](../assets/fix.svg)**[!UICONTROL Allow To Exceed Credit Limit]** <!--- MC-34584-->

![ Vaste kwestie ](../assets/fix.svg) de container van de HTML die productprijs op verzoeklijsten omringt wordt nu correct teruggegeven voor de kinderen van gebundelde producten. <!--- MC-36331-->

![ de Vaste kwestie ](../assets/fix.svg) Merchants kunnen nu de taal aanwijzen waarin de bedrijfgebruiker e-mail wordt verzonden wanneer het creëren van een bedrijf in meertalige plaatsingen. Eerder werd het vervolgkeuzemenu waarin de winkeliers de juiste winkelweergave kunnen selecteren en werd de taal niet weergegeven.  <!--- MC-35777-->

![ de Vaste 1} gebieden van de de attributen van het klantenadres van de uitgave {worden nu getoond zoals verwacht in het storefront controlewerkschema. <!--- MC-35607-->](../assets/fix.svg)

![ Vaste kwestie ](../assets/fix.svg) het B2B de configuratielusje van Eigenschappen opent nu correct. <!--- MC-35458--> de gasten kunnen QuickOrder nu gebruiken om producten aan hun kar toe te voegen en dan met succes punten te verwijderen. Eerder, toen een verkoopster QuickOrder gebruikte om veelvoudige producten aan hun kar toe te voegen, en dan een product te verwijderen, werd het product niet verwijderd. <!--- MC-35327-->

![ Vaste kwestie ](../assets/fix.svg) een bedrijf kan nu worden bijgewerkt gebruikend het REST API PUT `/V1/company/:companyId` verzoek zonder `region_id` te specificeren wanneer de staat als **niet wordt gevormd vereist**. Eerder gaf Adobe Commerce een fout als deze niet was opgegeven, ook al was `region_id` niet vereist. <!--- MC-35304-->

![ Vaste kwestie ](../assets/fix.svg) wanneer u creeert of een B2B Bedrijf bijwerkt gebruikend REST API (`http://magento.local/rest/V1/company/2`, waar `2` bedrijfsidentiteitskaart) vertegenwoordigt, omvat de reactie nu de montages voor `applicable_payment_method` of `available_payment_methods` zoals verwacht. <!--- MC-35248-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer een 404 pagina wanneer een handelaar **gaat** knoop in plaats van het klikken van de **[!UICONTROL Save]** knoop wanneer het creëren van een verzoeklijst op de storefront.<!--- MC-35094-->

![ Vaste de toestemmingen van de 1} Categorie van de kwestie {veranderen niet meer wanneer een nieuw product aan een openbare gedeelde catalogus wordt toegewezen. ](../assets/fix.svg) Eerder werden categorietoestemmingen gedupliceerd. <!--- MC-34386-->

![](../assets/fix.svg)`rest/default/V1/company/{id}`<!--- MC-34308-->

![](../assets/fix.svg) <!--- MC-34191-->

![](../assets/fix.svg) Eerder, gebruikte Adobe Commerce de algemene naam van de contactafzender die in het standaardwerkingsgebied voor alle e-mails wordt bepaald. <!--- MC-33917-->

![ Vaste kwestie ](../assets/fix.svg) U kunt multiShipping voor orden nu met succes uitvoeren die zowel fysieke als virtuele producten bevatten. <!--- MC-33818-->

![ Vaste kwestie ](../assets/fix.svg) De handelaren kunnen bedrijfgebruikers van de _[!UICONTROL Company Users]_sectie in Mijn pagina&#39;s van de Structuur van de Rekening en van het Bedrijf nu tot stand brengen wanneer **[!UICONTROL Access Restriction]**wordt toegelaten en **[!UICONTROL Restriction Mode]**aan `Sales: Login Only` wordt geplaatst. Eerder heeft Adobe Commerce deze fout gegenereerd toen een handelaar een gebruiker probeerde te maken: `Can not register new customer due to restrictions are enabled` . <!--- MC-33608-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce stelt niet meer de klantengroep van een klant aan het gebrek terug wanneer een klant hun rekeningsinformatie bewaart. <!--- MC-33554-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce werpt niet meer een fatale fout wanneer een beheerder een klant toewijst die een actief het winkelwagentje aan een klantengroep heeft. <!--- MC-33313-->

![](../assets/fix.svg)`addToCart`<!--- MC-33295-->

![ Vaste de e-mails van de kwestie ](../assets/fix.svg) Bericht die naar verkoopvertegenwoordigers worden verzonden die aan een bedrijf worden toegewezen omvat nu het toegewezen collectieve embleem. Eerder bevatte het e-mailbericht het standaard LUMA-logo, niet het geüploade bedrijfslogo. <!--- MC-33232-->

![ Vaste kwestie ](../assets/fix.svg) A de verzoeklijst omvat nu alle gegroepeerde producten en hoeveelheden die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, gaf Adobe Commerce deze fout weer: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![ Vaste kwestie ](../assets/fix.svg) de `products` vraag keert nu een nauwkeurig `total_count` gebied terug wanneer de gedeelde catalogus wordt toegelaten. <!--- MC-42268-->

![ Vaste kwestie ](../assets/fix.svg) de Configuratie van het Bedrijf en creeer nu de pagina&#39;s van het Bedrijf zoals verwacht na u een online het verschepen methode onbruikbaar maakt. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected` . <!--- MC-43178-->

![ Vaste kwestie ](../assets/fix.svg) het de testgeheugenconsumptie van de Integratie is verminderd, die testprestaties verbetert en de tijd vermindert die voor testvoltooiing wordt vereist. <!--- AC-266-->

## B2B v1.2.0

*28 juli, 2020*

[!BADGE  Gesteund ]{type=Informative tooltip="Ondersteund"}

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.0.

![ Nieuw ](../assets/new.svg) Onderzoek van de Orde van de Storefront, met toegevoegde dank voor bijdrage door Marek Mularczyk van [ Divante ](https://www.divante.com/) en communautaire leden.

![ Nieuwe ](../assets/new.svg) Orders van de Aankoop worden verbeterd en herschreven. Ze zijn nu standaard opgenomen in Adobe Commerce.

![ Nieuwe ](../assets/new.svg) Regels van de Goedkeuring van de Inkooporder zijn uitgevoerd. Met deze regels kunnen gebruikers de workflow voor inkooporders beheren door aankoopregels voor bestellingen te maken.

![ Nieuwe ](../assets/new.svg) Login als Klant is nu inbegrepen door gebrek in Adobe Commerce. Deze eigenschap staat plaatswerknemers toe om klanten bij te staan door zich aan te melden als klant om te zien wat zij zien.

](../assets/fix.svg) de samenvoegingen van het Attribuut van 0} Vaste kwestie {werken nu correct voor Gelaagde Navigatie met Elasticsearch![

![ Vaste kwestie ](../assets/fix.svg) Het zoeken van orden door speciale karakters werkt nu behoorlijk.

![ Vaste kwestie ](../assets/fix.svg) het klikken van de **[!UICONTROL Clear All]** Knoop breidt nu alle filters uit, eerder dan het doen ineenstorten van hen.

![ Vaste kwestie ](../assets/fix.svg) Product SKU/Naam is nu inbegrepen in de het onderzoeksfiltersamenvatting van de Geschiedenis van de Orde.

![ Vaste kwestie ](../assets/fix.svg) Sorterende Indicator wordt nu getoond behoorlijk in het Mijn Net van de Orden van de Aankoop.

![ Vaste kwestie ](../assets/fix.svg) nu, kunt u klikken goedkeuren, annuleert, verwerpt, en de knopen van de Orde van de Aankoop slechts eenmaal. Previously, you could click the button multiple times.

![](../assets/fix.svg)

![ Vaste kwestie ](../assets/fix.svg) eerder, goedkeurend een Inkooporder met een korting die is verlopen plaatste de orde bij het volledige bedrag en werkte niet het totaal van de Inkooporder bij. Nu wordt het totaal van de inkooporder bijgewerkt om het juiste totaal weer te geven.

![ Vaste kwestie ](../assets/fix.svg) Een kwestie werd geïntroduceerd in 2.3.4 waar de attributen van de douaneverlenging niet van het Adres van de Klant aan het Adres van het Citaat zouden worden gekopieerd. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) met geïnstalleerd B2B, zou een SQL fout verschijnen wanneer het toewijzen van categorieën aan gedeelde catalogi. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) wegens een onjuiste veranderlijke typewaarde, konden beheerders geen configureerbare producten aan een orde toevoegen. The option dropdowns would not populate. This feature now works properly.

![](../assets/fix.svg) This issue has been fixed.

![](../assets/fix.svg) Previously, an error message would appear when adding an item not in the catalog.

![ Vaste kwestie ](../assets/fix.svg) eerder, na het in werking stellen van het bevel `php bin/magento indexer:set-dimensions-mode catalog_product_price website` en dan het proberen om een gedeelde catalogus tot stand te brengen, zou een fout voorkomen. This issue has been fixed.

![](../assets/fix.svg) This issue has been fixed.

![](../assets/fix.svg)__ This issue has been fixed.

![](../assets/fix.svg) This issue has been fixed.

![ Vaste kwestie ](../assets/fix.svg) eerder, wanneer het plaatsen van een bedrijf aan &quot;Actief&quot;via API, zou een fout voorkomen. Dit probleem is nu opgelost.

![ Opgeloste kwestie ](../assets/fix.svg) wegens een onnodige `form` markering, ververfrist de ordepagina automatisch wanneer u op Enter na het veranderen van een voorgestelde verschepende last duwde. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) eerder, toen het plaatsen van een grens van de productvertoning op een cataloguspagina en die grens was minder dan het aantal totale producten, kwam een fout voor. Die functie werkt nu zoals verwacht.

![ Vaste kwestie ](../assets/fix.svg) eerder, toen het veranderen van admin van een bedrijf, het originele adminadres aan nieuwe admin zou worden gekopieerd, die hen twee adressen geven. Nu wordt alleen het juiste adres toegevoegd.

![ Vaste kwestie ](../assets/fix.svg) eerder, gebruikend API om een citaatpunt op te slaan wanneer het git aan &quot;Toegestaan wordt geplaatst en Klant&quot;op de hoogte brengt zou ontbreken. Deze API-aanroep werkt nu zoals verwacht.

![ Vaste kwestie ](../assets/fix.svg) De Vaste Belasting van het Product wordt nu getoond op de de detailpagina van Citaten.

![ Vaste kwestie ](../assets/fix.svg) eerder, klikkend een gehechtheid op het lusje van Commentaren van de Mijn pagina van Citaten zou er niet in slagen om het dossier te downloaden. Dit gedrag werkt nu zoals verwacht.

### Bekende problemen

- Adobe Commerce genereert een uitzondering tijdens de upgrade naar B2B 1.2.0 in een implementatie voor meerdere websites. Wanneer `setup:upgrade` wordt uitgevoerd, treedt deze fout op in de module `PurchaseOrder` module: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder` . **Oplossing**: Installeer de `B2B-716 Add NonTransactionableInterface` interface aan `InitPurchaseOrderSalesSequence` hotfix van het gegevenspatroon, die nu van **Mijn Rekening** beschikbaar is > **downloadt** sectie van `magento.com`.
- Als een kortingscode vervalt voordat een inkooporder (PO) wordt goedgekeurd, blijft de inkooporder het gedisconteerde bedrag weergeven, maar als de inkooporder eenmaal is goedgekeurd, wordt de order geplaatst op het niet-gedisconteerde totaal. **Oplossing**: Installeer `B2B-709 Purchase Order Discount patch` hotfix voor deze kwestie, die nu van **Mijn Rekening** > **Downloads** sectie van `magento.com` beschikbaar is.
- Als de items in een inkooporder niet in voorraad zijn of niet voldoende in voorraad zijn wanneer de inkooporder wordt omgezet in een werkelijke bestelling, treedt er een fout op. Als backorders worden ingeschakeld, wordt de volgorde op de normale wijze verwerkt.
