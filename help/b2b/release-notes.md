---
title: '[!DNL Adobe Commerce B2B] releaseopmerkingen'
description: Herzie de versienota's voor informatie over veranderingen in  [!DNL Adobe Commerce B2B]  versies.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: b077b6a3efbfa9348ac7282d52a0b94d736ade4a
workflow-type: tm+mt
source-wordcount: '8867'
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

## B2B v1.5.2-p1

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8-p1 van Adobe Commerce, 2.4.7-p6, en 2.4.6-p11 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p5, 2.4.6 tot 2.4.6-p10

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-50 ](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

{{b2b-compatibility}}

## B2B 1.5.2

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8 van Adobe Commerce, 2.4.7-p5 en 2.4.6-p10 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p4, 2.4.6 tot 2.4.6-p9

De B2B v1.5.2 versie omvat kwaliteitsverbeteringen en insectenmoeilijke situaties.

### Bedrijfsbeheer

![ Nieuwe ](../assets/new.svg)<!-- B2B-4123 --> Beheerders kunnen veelvoudige bedrijven van één enkele rekening nu beheren gebruikend de schakelaar van het storefront bedrijf. Belangrijkste voordelen zijn:

- **Vereenvoudigd multi-bedrijf beheer** - de beheerders kunnen veelvoudige bedrijven van één gebruikersrekening nu controleren, die de behoefte elimineren om afzonderlijke logins voor elk bedrijf tot stand te brengen en te beheren.
- **Efficiënte bedrijfsomschakeling** - een intuïtieve interface staat beheerders toe om snel tussen bedrijven te schakelen en updates te maken, die productiviteit verbeteren wanneer het beheren van veelvoudige entiteiten.
- **Gestroomlijnde verrichtingen** - de regionale managers en bedrijfsleiders kunnen centraal al hun bedrijven beheren, toelatend snellere besluitvorming en vlottere bedrijfsverrichtingen.

Deze verbetering bouwt voort op het multi-company van B2B 1.5.0 vermogen van het lidmaatschap, dat gebruikers om tot veelvoudige bedrijven toeliet te behoren maar geen admin toegang over bedrijven steunde. De bedrijfschakelaar elimineert de behoefte aan afzonderlijke adminrekeningen terwijl het handhaven van juiste toegangscontroles en bedrijf-specifieke meningen.

### Bedrijf

![ Vaste kwestie ](../assets/fix.svg)<!-- B2B-4480 --> Vaste een kwestie waar de gastklanten een `No such entity with cartId = ?` foutenmelding zouden zien wanneer het aanmelden als bedrijfgebruiker met producten in hun het winkelwagentje.

### Verhandelbaar aanhalingsteken

![ Vaste kwestie ](../assets/fix.svg) B2B v1.5.2 versie omvat de volgende moeilijke situaties voor verhandelbare citaten:

- &#x200B;<!-- B2B-3252 -->In het veld [!UICONTROL Line Item Discount Amount] wordt invoer nu gevalideerd om te voorkomen dat negatieve kortingswaarden worden ingevoerd.
- &#x200B;<!-- B2B-3224 -->Probleem met gebruikerservaring verholpen waarbij lange-line itemopmerkingen werden afgebroken en moeilijk leesbaar waren voor B2B-klanten.
- &#x200B;<!-- B2B-2865 -->B2B-klanten kunnen nu producthoeveelheden opgeven met decimale waarden (zoals 1,5 of 2,75) bij het maken van noteringen.

### Offertesjabloon

![ Nieuwe ](../assets/new.svg)<!-- B2B-4104 --> Nieuwe capaciteit voor B2B kopers en verkopers om externe documentverbindingen aan citaatmalplaatjes vast te maken. Met deze functie kunt u rechtstreeks vanuit aanhalingstekens koppelingen maken naar documenten die worden gehost in services zoals DocuSign en Adobe Sign, als aanvulling op de bestaande mogelijkheden voor bestandsbijlagen. Belangrijkste voordelen zijn:

- Gestroomlijnde samenwerking via directe toegang tot kritieke overeenkomsten en contracten
- Verbeterde transparantie met onmiddellijke toegang tot de meest recente documentatie
- Snellere prijsonderhandelingen, omdat bestanden niet hoeven te worden gedownload en geüpload
- Flexibel documentbeheer met externe hostingservices voor documenten

## B2B 1.5.1

*11 Februari, 2025*

[!BADGE &#x200B; Gesteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.7-p4+ en 2.4.6-p9+ de versies van het veiligheidspatch van Adobe Commerce.
Compatibel met Adobe Commerce-versies 2.4.8-beta1 tot 2.4.8-beta2, 2.4.7 tot 2.4.7-p3, 2.4.6 tot 2.4.6-p8

De versie B2B v1.5.1 bevat kwaliteitsverbeteringen en oplossingen voor problemen.

### Bedrijf

![ Vaste kwestie ](../assets/fix.svg)<!-- B2B-4422 --> als een klant probeert om bedrijven op de pagina van de Details van het Citaat te schakelen, richt het systeem nu de klant aan een *Ontkende Toegang* pagina om ervoor te zorgen dat een citaat dat voor één bedrijf wordt gecreeerd niet kan worden gebruikt om een orde met de prijzen van een ander bedrijf te plaatsen. Voorheen kon een gebruiker een prijsopgave voor één bedrijf maken en vervolgens overschakelen op een ander bedrijf om een bestelling met verschillende prijzen te plaatsen.

### Korting op regelobjecten

![ Vaste kwestie ](../assets/fix.svg)<!-- B2B-2938 --> Verbeterde systeemefficiency door een prestatiesdegradatie te richten die in het scenario van de citaatherberekening wordt waargenomen. Eerder werden twee nieuwe entiteiten toegevoegd aan elk onderdeel van de winkelwagentje, wat een merkbare toename van de databaseaanvragen veroorzaakte, wat tot langzamere prestaties leidde.

### Verhandelbaar aanhalingsteken

![ Vaste kwestie ](../assets/fix.svg)<!-- B2B-3820 --> het systeem handhaaft nu de positie van elementen UI wanneer de bevestiging van JavaScript wordt toegepast op de *[!UICONTROL min/max qty]* gebieden op de pagina van het Malplaatje van het Citaat van de Opbrengst van de Luma. Als u eerder JavaScript-validatie toepaste op deze velden, werden andere UI-elementen op de pagina verschoven.

### Winkelwagentje

![ Vaste kwestie ](../assets/fix.svg)<!-- B2B-4222 --> introduceerde een nieuw het winkelwagentbeheerssysteem dat wordt ontworpen om de het winkelen ervaring voor gebruikers te stroomlijnen die veelvoudige bedrijfrekeningen beheren. Het nieuwe systeem associeert winkelwagentjes met individuele bedrijven eerder dan de klantenrekening om de het winkelen ervaring te stroomlijnen en het werkschema te verbeteren door de volgende mogelijkheden te steunen.

- **bedrijf-specifieke wortels:** - De winkelwagentjes zijn nu verbonden met individuele bedrijven om bedrijf-specifieke tarifering en productopties te steunen.
- **Naadloze omschakeling** - de gebruikers kunnen gemakkelijk tussen verschillende bedrijfrekeningen schakelen zonder de inhoud van de kar van elk bedrijf te beïnvloeden.
- **Contextuele Integriteit** - Alle worteldetails blijven binnen de context van het respectieve bedrijf, die een verenigbare en betrouwbare het winkelen ervaring verstrekken.

## B2B 1.5.0

*30 oktober, 2024*

[!BADGE &#x200B; Gesteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.7-p3+ en 2.4.6-p8+ de versies van het veiligheidspatch van Adobe Commerce.
Compatibel met Adobe Commerce-versies 2.4.8-beta1, 2.4.7 tot 2.4.7-p2, 2.4.6 tot 2.4.6-p7.

Adobe Commerce B2B versie 1.5.0 is ook compatibel met PHP 8.3 en steunt de [ Server van de Toepassing van GraphQL ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

De B2B v1.5.0 versie omvat nieuwe eigenschappen, kwaliteitsverbeteringen, en insectenmoeilijke situaties.

>[!NOTE]
>
> Leer over achteruit-onverenigbaar veranderingen (BICs) die in B2B 1.5.0 versie door de hoogtepunten en verwijzingsinformatie in het [ Achteruit Incompatibele onderwerp van Veranderingen ](backward-incompatible-changes.md) worden geïntroduceerd.

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

![ Nieuw ](../assets/new.svg) <!--B2B-2747--> **het werkingsgebiedselecteur van het Bedrijf** - verstrekt capaciteit voor bedrijfgebruikers die aan veelvoudige bedrijven worden toegewezen om bedrijven op de storefront te veranderen. Wanneer het werkingsgebied wordt geschakeld, werken de gegevens bij om de informatie te tonen die op de nieuwe bedrijfcontext wordt gebaseerd. Als het nieuwe bedrijf bijvoorbeeld een andere gedeelde catalogus gebruikt, ziet de gebruiker van het bedrijf producten, prijzen en andere informatie op basis van de nieuwe gedeelde catalogus. De inhoud met betrekking tot orden, citaten, citaatmalplaatjes werkt ook bij gebaseerd op de context van het geselecteerde bedrijf.

>[!NOTE]
>De inhoud van het winkelwagentje weerspiegelt de items die door de huidige klant zijn geselecteerd. Als de klant een actieve winkelwagentje heeft en een ander bedrijf selecteert, wordt hen ertoe aangezet om de wagentje bij te werken om de productassortiment, de tarifering, en promotionele kortingen te weerspiegelen die op de nieuwe bedrijfcontext worden gebaseerd. Producten die niet beschikbaar zijn in de catalogus van het nieuwe bedrijf, worden uit het winkelwagentje verwijderd. Als het product een verschillende prijs of een beschikbaarheid heeft, werkt het karretje bij om de gegevens te weerspiegelen beschikbaar in de context van het geselecteerde bedrijf.<!--B2B-4222-->

![ Vaste kwestie ](../assets/fix.svg)<!--ACP2E-1933--> de beheerders van het Bedrijf kunnen bedrijfgebruikers van de storefront nu toevoegen. Eerder heeft Commerce een fout geregistreerd toen een Admin-gebruiker probeerde een nieuwe gebruiker toe te voegen: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123` .

### Aanhalingstekens en Citaatsjablonen

De verbeteringen aan het citeren mogelijkheden helpen Kopers en Verkopers citaten beheren en citeren onderhandelingen effectiever.

![ Nieuwe ](../assets/new.svg) **malplaatjes van het Citaat** - <!--B2B-3367--> Kopers en verkopers kunnen het citaatproces nu stroomlijnen door herbruikbare en klantgerichte citaatmalplaatjes te creëren. Met behulp van aanhalingstekensjablonen kan het onderhandelingsproces voor aanhalingstekens eenmaal worden voltooid en kunnen kopers vooraf goedgekeurde gekoppelde aanhalingstekens genereren voor terugkerende orders in plaats van voor elke bestelling het onderhandelingsproces voor aanhalingstekens te doorlopen. Aanhalingssjablonen breiden de bestaande functionaliteit voor aanhalingstekens uit door de volgende geavanceerde functies toe te voegen:

- **de drempels van de Orde** staan verkopers toe om minimum en maximumorderverplichtingen te bepalen, die de koper verzekeren aan overeengekomen-op koopgevolume.
- **plaatsende minimum en maximumhoeveelheden van de puntorde** voorziet de koper van de flexibiliteit om ordehoeveelheden op het verbonden citaat aan te passen zonder een nieuw malplaatje of verdere onderhandeling te vereisen.
- **spoor het aantal verbonden citaten die en met succes voltooide orden** worden geproduceerd om inzichten in de naleving van onderhandelde overeenkomsten te bereiken.
- **Gekoppelde citaten** zijn vooraf goedgekeurde citaten die de koper van een actief citaatmalplaatje produceert om terugkomende die orden voor te leggen op de termijnen in het citaatmalplaatje worden besproken.

![ Nieuwe ](../assets/new.svg) **Verbeteringen aan bestaande citaatmogelijkheden**

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

## B2B v1.4.2-p6

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p6+ en 2.4.6-p11+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-50 ](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

{{b2b-compatibility}}

## B2B v1.4.2-p5

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p5+ en 2.4.6-p10+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p5+ en 2.4.6-p10+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-26 ](https://helpx.adobe.com/security/products/magento/apsb25-26.html) worden gedocumenteerd.

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11 Februari, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p4+ en 2.4.6-p9+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p4+ en 2.4.6-p9+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ Bulletin APSB25-08 van de Veiligheid ](https://helpx.adobe.com/security/products/magento/apsb25-08.html) worden gedocumenteerd.

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8 Oktober, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p3+ en 2.4.6-p8+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p3+ en 2.4.6-p8+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB24-73 ](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p2+ en 2.4.6-p7+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p2+ en 2.4.6-p7+ de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de moeilijke situaties van de Veiligheid die in Bulletin xxxx van de Veiligheid worden gedocumenteerd.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9 augustus, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p1+ en 2.4.6-p6+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-p1+ en 2.4.6-p6+ de versies van het veiligheidspatch.

{{b2b-compatibility}}

## B2B v1.4.2

*10 oktober, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versie 2.4.7 van Adobe Commerce en versie van 2.4.6 aan 2.4.6-p5.

De B2B v1.4.2 versie omvat kwaliteitsverbeteringen en insectenmoeilijke situaties.

![ Vaste kwestie ](../assets/fix.svg) <!--B2B-2897--> als een Verkoper een koperscitaat creeert dat een product SKU niet beschikbaar in de gedeelde catalogus verbonden aan het kopersbedrijf omvat, toont het systeem het foutenbericht `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  De verkoper kan de prijsopgave pas opslaan als hij het product verwijdert dat niet beschikbaar is. Eerder, werd het citaat bewaard met niet beschikbare inbegrepen SKU, en het citaat kon niet op de storefront laden.

>[!IMPORTANT]
>
>Adobe Commerce B2B versie 1.4.2+ is compatibel met PHP 8.2. Als u de Commerce-instantie upgradet naar versie 2.4.7+, moet u ervoor zorgen dat de instantie PHP versie 8.2 gebruikt om de compatibiliteit met Adobe Commerce B2B-versie te behouden. Bovendien, steunt B2B 1.4.2+ momenteel niet de [ Server van de Toepassing van GraphQL ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7 Augustus, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} [ Adobe Commerce 2.4.6-p2 ](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1.

De versie B2B v1.4.1 bevat kwaliteitsverbeteringen en oplossingen voor problemen.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1825--> de orden van de Aankoop kunnen niet meer door een gebruiker worden geplaatst verbonden aan het bedrijf nadat het bedrijf is geblokkeerd. Eerder had een gebruiker die banden had met het bedrijf kooporders kunnen plaatsen wanneer het bedrijf werd geblokkeerd.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1943--> product backordered status wordt nu correct getoond op de storefront. Eerder werden producten die voor verzending beschikbaar waren, onjuist geïdentificeerd als achtergeordend.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1862--> als de vorm van de bedrijfregistratie een attribuut van het type van klantendossier omvat, is het dossier dat tijdens het registratieproces wordt geupload nu inbegrepen in de rekeningsinformatie voor de Beheerder van het Bedrijf nadat het bedrijf wordt gecreeerd. Eerder ontbrak de bijlage.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1793--> De monsterselecteur voor een configureerbaar product wordt nu getoond zoals verwacht in de pagina van de het puntconfiguratie van de verzoeklijst. Eerder, werd de monsterselecteur getoond als dropdown gebied in de pagina van de de puntconfiguratie van de verzoeklijst.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1968--> wanneer het gebruiken van de [ vraag van GraphQL van het Bedrijf ](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) om bedrijfdetails terug te keren, zijn de resultaten nu met succes zonder fout teruggekeerd.

## B2B v1.4.0

*13 Juni, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} [ Adobe Commerce 2.4.6-p1 ](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1

Deze release bevat nieuwe mogelijkheden en verbeteringen voor B2B-onderhandelbare aanhalingstekens en meerdere opgeloste problemen.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.7-bèta1.

![ Nieuwe ](../assets/new.svg) **Verkoper stelde citaten** in werking - de verkopers kunnen een citaat voor een koper direct van het Citaat en de netten van de Klant in Admin nu in werking stellen. Dit vermogen stroomlijnt het prijsverhogingsproces en vermindert ingewikkeldheid voor klanten. Als een klant geen bestelling heeft geïnitieerd, kan een verkoper snel een prijsopgave namens de klant maken en het onderhandelingsproces starten. Eerder konden prijsopgaven alleen door de koper of door een verkoper die zich als klant heeft aangemeld, van de winkel worden gemaakt.

![ Nieuwe ](../assets/new.svg) **het puntkortingen van de Lijn en onderhandeling** - <!--B2B-2440--> Binnen een citaat, kunnen de B2B kopers en verkopers nu op het niveau van het lijnpunt onderhandelen, die kortingen toepassen en nota&#39;s ruilen tot een overeenkomst wordt bereikt. De verwezenlijking van de nota en de updates zijn inbegrepen in het lijnpunt en citaatgeschiedenis om mededeling te volgen. Eerder konden kopers en verkopers alleen opmerkingen uitwisselen en kortingen toepassen op het prijsniveau.

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu correcte details tijdens betaling wanneer de optie van de Orden van de Aankoop wordt toegelaten en een virtueel citaat dat met de PayPal betalingsoptie werd gecreeerd is geselecteerd. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--ACP2E-1504--> de fouten van de Bevestiging komen niet meer voor wanneer u probeert om een bedrijf met een kredietgrens te bewaren die 999 overschrijdt. Eerder, voor bedrijfskredietgrenzen groter dan 999, voegde de handel van Adobe een komma separator in, die een bevestigingsfout veroorzaakte die updates verhinderde worden bewaard.

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

## B2B v1.3.5-p10

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p10+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met Adobe Commerce 2.4.6-p10 de versies van het veiligheidspatch.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-26 ](https://helpx.adobe.com/security/products/magento/apsb25-26.html) worden gedocumenteerd.

## B2B v1.3.5-p9

*11 Februari, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p9+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met de de veiligheidsflardversies van Adobe Commerce 2.4.6-p9.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ Bulletin APSB25-08 van de Veiligheid ](https://helpx.adobe.com/security/products/magento/apsb25-08.html) worden gedocumenteerd.

## B2B v1.3.5-p8

*8 Oktober, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p8+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met de de veiligheidsflardversies van Adobe Commerce 2.4.6-p8.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB24-73 ](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

## B2B v1.3.5-p7

*9 augustus, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p7+ de versies van het veiligheidspatch.

![ Nieuwe ](../assets/new.svg) Toegevoegde verenigbaarheid met de de veiligheidsflardversies van Adobe Commerce 2.4.6-p7.

## B2B v1.3.5

*Maart 14, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 - 2.4.6 en nieuwere versies

![ Nieuwe ](../assets/new.svg) vrijgekomen B2B versie 1.3.5-p2 om verenigbaarheid met Adobe Commerce 2.4.6-p2 te steunen.

![ Nieuwe ](../assets/new.svg) vrijgekomen B2B versie 1.3.5-p1 om verenigbaarheid met Adobe Commerce 2.4.6-p1 te steunen.

>[!NOTE]
>
>Nadat u Commerce van 2.4.6 aan de [ recentste versie ](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6) bevordert, zorg ervoor om aan de gesteunde B2B 1.3.5 flardversie bij te werken. Of upgrade de B2B-extensie van versie 1.3.5 naar versie 1.4.0 of hoger om de nieuwste functies te krijgen.

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.6.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce toont nu correcte details tijdens betaling wanneer de optie van de Orden van de Aankoop wordt toegelaten en een virtueel citaat dat met de PayPal betalingsoptie werd gecreeerd is geselecteerd. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-609--> de lijst van klantengroepen voor **toestaat het doorbladeren Categorie** het plaatsen bevat niet meer klantengroepen die met gedeelde catalogi verwant zijn.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1244--> het de klantenattribuut van het BTW/Aantal werkt nu zoals verwacht met bedrijf admin rekeningen op zowel Admin als opslag. Aangepaste BTW-kenmerken zijn niet meer vereist om een bedrijfsaccount te maken. Eerder, toen een handelaar een ondernemingsrekening met een douaneBelastings/BTW attribuut creeerde, gaf Adobe Commerce een bevestigingsfout op zowel de opslagplaats als Admin.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1236--> Het onbruikbaar maken van de gedeelde cataloguseigenschap op een specifiek werkingsgebied werkt nu correct. Eerder stelde Adobe Commerce een ongeldig werkingsgebied in wanneer een handelaar gedeelde catalogusconfiguratie bewaarde.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1203--> Admin gebruikers kunnen klanten de waarden van de douaneattributen voor bedrijfgebruikers nu bewaren. Eerder konden de douanekenmerken van de klant voor bedrijfgebruikers niet worden bewaard.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1221--> De kwesties van prestaties worden opgelost met de bevestiging van bedrijftoestemmingen die door GraphQL worden verstrekt wanneer vele bedrijftoestemmingen reeds worden toegewezen.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce werpt niet meer een fout op de wortelpagina wanneer de Snelle Orde wordt gebruikt om een product in een hoeveelheid toe te voegen die beschikbare voorraad overschrijdt.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1090--> De prestaties van `SELECT` verrichtingen van bedrijftoestemmingen zijn verbeterd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-2456--> de vragen van de Categorie keren nu productprijzen volgens de montages van de opslagconfiguratie terug wanneer er geen categorietoestemmingen uitdrukkelijk geplaatst op de categorie zijn die wordt gevraagd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-6829--> De **[!UICONTROL Place Order]** knoop werkt nu zoals verwacht wanneer het voltooien van een aankoop met een goedgekeurd citaatverzoek. Problemen met de plug-in voor verhandelbare aanhalingstekens `negotiableQuoteCheckoutSessionPlugin` zijn opgelost.

## B2B v1.3.4-p13

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5-p12.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-50 ](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

## B2B v1.3.4-p12

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5-p12.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-26 ](https://helpx.adobe.com/security/products/magento/apsb25-26.html) worden gedocumenteerd.

## B2B v1.3.4-p11

*11 Februari, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5-p11.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ Bulletin APSB25-08 van de Veiligheid ](https://helpx.adobe.com/security/products/magento/apsb25-08.html) worden gedocumenteerd.

## B2B v1.3.4-p10

*9 Oktober, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5-p10.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB24-73 ](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

## B2B v1.3.4

*9 augustus, 2022*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-453--> Adobe Commerce verzendt niet meer e-mailberichten telkens als een bestaand Bedrijf door een API vraag wordt bijgewerkt. E-mails worden nu alleen verzonden wanneer een bedrijf wordt gemaakt.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-406--> Adobe Commerce berekent nu correct een groot totaal van een onderhandelbaar citaat wanneer het **[!UICONTROL Enable Cross Border Trade]** plaatsen van de belastingberekening wordt toegelaten.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-322--> De configureerbare producten worden nu verplaatst naar de laatste positie in de productlijst nadat de voorraad wordt bijgewerkt wanneer **[!UICONTROL Move out of stock to the bottom]** het plaatsen wordt toegelaten. Er wordt een nieuwe aangepaste databasequery geïmplementeerd om ervoor te zorgen dat de sorteervolgorde voor de Elasticsearch-index nu overeenkomt met de sorteervolgorde voor beheerders. Eerder, werden de configureerbare producten en hun kindproducten niet verplaatst naar de bodem van de lijst toen dit het plaatsen werd toegelaten.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-308--> E-mail van de Orde van de Aankoop neemt nu het e-mailverzenden van het plaatsen van elke website in een multi-plaatsplaatsing. Een controle op de instelling **[!UICONTROL Disable Email Communications]** wordt toegevoegd aan de aangepaste logica voor e-mailwachtrijen. Eerder heeft Adobe Commerce de instelling voor het verzenden van e-mail voor de secundaire website niet gerespecteerd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-302--> De titel van het gebied van SKU van de Snelle pagina van de Orde wordt veranderd voor duidelijkheid.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-543--> Adobe Commerce toont nu een informatievere foutenmelding wanneer een verkoopster een ongeldige SKU in het **gaat SKU of gebied van de Naam van het Product** in.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-1753--> het **[!UICONTROL Account Created in]** gebied voor een bedrijfbeheerder behoudt nu zijn waarde zoals verwacht na u sparen het bedrijf.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-722 --> de `customer` vraag keert niet meer lege resultaten terug wanneer het vraaglijsten terugwint die door `uid` worden gefiltreerd.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-210 --> voegde een stop vóór de `collectQuoteTotals` vraag toe om ervoor te zorgen dat de opslagkredieten slechts eenmaal worden toegepast.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-665 --> Klanten worden nu opnieuw gericht aan de login pagina wanneer hun rekening door een beheerder van Admin wordt geschrapt. Eerder gaf Adobe Commerce een fout. Het codeblok van de plug-in (`SessionPlugin` ) bevindt zich nu in het `try…catch` -blok. Eerder, werd deze code niet verpakt binnen het generische uitzondering-behandelende blok.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-661 --> op de Snelle pagina van de Orde op mobiele wijze, het drukken **gaat** na het ingaan van een geldige productnaam binnen of SKU neemt nu de verkoopster aan het volgende gebied zoals verwacht.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-607 --> De naam van het Bedrijf is nu zichtbaar zoals verwacht in het factureren en het verschepen adressecties van het controlewerkschema.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-375 --> het krediet van de opslag is nu niet beschikbaar wanneer de **[!UICONTROL Zero Subtotal Checkout]** betalingsmethode wordt onbruikbaar gemaakt. Eerder was het selectievakje Winkelkrediet niet functioneel tijdens de plaatsing van de bestelling bij de beheerder. De toepassing heeft de bestelling niet bij het winkelkrediet geplaatst en deze fout weergegeven: `The requested Payment Method is not available`.

## B2B v1.3.3-p14

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.5-p12.

![ Vaste kwestie ](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [ het Bulletin van de Veiligheid APSB25-50 ](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

## B2B v1.3.3

*9 augustus, 2022*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.4.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41985--> de tijd die wordt vereist om van Adobe Commerce 2.3.x aan Adobe Commerce 2.4.x in plaatsingen met meer dan 100.000 bedrijfrollen te bevorderen is wezenlijk verminderd.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42153--> Het POST `V1/order/:orderId/invoice` verzoek steunt nu de verwezenlijking van gedeeltelijke facturen wanneer de **[!UICONTROL Payment on Account]** betalingsmethode wordt toegelaten. Eerder heeft Adobe Commerce deze fout gegenereerd: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity` . [ GitHub-32428 ](https://github.com/magento/magento2/issues/32428)

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro werkt nu zoals verwacht met B2B verhandelbaar citaat wanneer de wagentje van de klant andere producten bevat. Adobe Commerce verwerkt de bestelling nu met succes en stuurt een e-mail naar de klant zoals u had verwacht. Eerder gaf Adobe Commerce een fatale fout en stuurde een bevestigingsbericht naar de klant met daarin de nulwaarden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41819--> Paginering wordt nu correct getoond op de pagina van het resultaat van het catalogusonderzoek na het uitsluiten van sommige producten in gedeelde catalogus.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42886--> de douaneattributen van de Klant worden nu bewaard zoals verwacht wanneer het creëren van of het opslaan van een bedrijfgebruiker in Admin.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42927--> De **[!UICONTROL Submit]** knoop op de Create Nieuwe vorm van het Bedrijf wordt nu onbruikbaar gemaakt na één klik om veelvoudige vormvoorlegging te verhinderen. Eerder kon u dit formulier meerdere keren verzenden door herhaaldelijk op deze knop te klikken. Er is een fout opgetreden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce toont niet meer de reorder verbinding op de opslagplaats wanneer een verkoopster zich in een opslag registreert waarvoor reorders zijn onbruikbaar gemaakt.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-43115--> Snelle het onderzoek van de Orde door SKU is nu case-insensitive wanneer de gedeelde catalogus wordt toegelaten.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42203--> U kunt een dossier voor een klantenattribuut nu bijwerken wanneer het creëren van een bedrijf. Eerder, toen u probeerde om een bedrijf met een gehechtheid van type `File` tot stand te brengen, creeerde Adobe Commerce niet het bedrijf en registreerde deze fout in het uitzonderingslogboek: `Something went wrong while saving file`.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42242--> U kunt een bedrijf met een klantenrekening nu tot stand brengen die een douanekenmerk met a (`File`) of (`Image`) type heeft. Eerder, als de rekening één van deze klantgerichte opties had, gaf het Bedrijf uit paginalader uitgeeft niet op, die het uitgeven van bedrijfdetails verhinderden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42268--> De `products` vraag keert nu een nauwkeurig `total_count` gebied terug wanneer de gedeelde catalogus wordt toegelaten.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42203--> U kunt een dossier voor een klantenattribuut nu bijwerken wanneer het creëren van een bedrijf. Eerder, toen u probeerde om een bedrijf met een gehechtheid van type `File` tot stand te brengen, creeerde Adobe Commerce niet het bedrijf en registreerde deze fout in het uitzonderingslogboek: `Something went wrong while saving file`.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-43178--> de _Configuratie van het Bedrijf_ en _creëren bedrijf_ pagina&#39;s nu werken zoals verwacht nadat u een online het verschepen methode onbruikbaar maakt. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected` .

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42214--> de _Categorie_ pagina toont nu verenigbare productgegevens terwijl de toestemmingen tijdens het gedeeltelijke indexeren worden geproduceerd. Er is een nieuwe gedeeltelijke indexator voor directorymachtigingen toegevoegd aan dit proces. Eerder waren de gegevens die werden weergegeven terwijl de indexeerfunctie werd uitgevoerd onjuist.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42567--> De `categoryList` vraag keert nu het correcte aantal producten terug wanneer de catalogustoestemmingen worden gebruikt en de producten aan een gedeelde catalogus worden toegewezen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42528--> de `categoryList` vraag respecteert nu categorietoestemmingen en keert slechts toegelaten categorieën terug. Eerder, keerde het alle toegewezen en niet toegewezen categorieën terug.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42399--> Het `rest/V1/company/{id}` verzoek keert nu `is_purchase_order_enabled` attributenwaarden terug zoals verwacht.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-128--> de klantenattributen van de Douane worden nu getoond zoals verwacht in _Admin van het Bedrijf_ tabel.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-130--> het Mijn blok van de Lijst van de Wonen op de Mijn pagina van de Rekening wordt nu getoond zoals verwacht voor de Beheerders van het Bedrijf en de Gebruikers van het Bedrijf.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-133--> de Snelle fouten van de Orde worden niet meer getoond in het het winkelwagentje. Eerder, toonde Adobe Commerce deze fout in het winkelwagentje toen SKU niet in de catalogus werd gevonden: `The SKU was not found in the catalog`.

![ Vaste kwestie ](../assets/fix.svg) <!--- ACP2E-194--> Gedeelde catalogus sparen verrichtingen zijn geoptimaliseerd om sneller uit te voeren. Het opslaan van een gedeelde catalogus met veel klantengroepen kan eerder enkele minuten in beslag nemen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce schrapt nu alle subcategorierechten van de `sharedcatalog_category_permissions` lijst wanneer de oudercategorie wordt geschrapt. Eerder werden alleen de gegevens van de bovenliggende categorie verwijderd.

## B2B v1.3.2

*Augustus 29, 2022*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.3.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce verzendt nu met succes updatemails over verlopen verhandelbare citaten. Eerder, toen een verhandelbaar prijsopgave verstreek, heeft Adobe Commerce geen e-mails verzonden voor updates.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce verzendt nu met succes updatemails over spoedig om te verlopen en verlopen onderhandelbare citaten wanneer een `cron` baan mist.

### Bedrijf

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41542--> het Create Nieuwe het dropdown gebied van het de paginaland van de Rekening van het Bedrijf maakt maakt niet meer van lege optiewaarden een lijst. Eerder waren de eerste twee opties en de landcode `AN` leeg.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41260--> het klikken van de **[!UICONTROL Return]** knoop voor een orde die door een bedrijfgebruiker werd gecreeerd richt nu een administratieve gebruiker aan de Create pagina van de Terugkeer opnieuw zoals verwacht. Eerder werd de beheerder omgeleid naar de pagina Order History.

![ Vaste kwestie ](../assets/fix.svg) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} <!--- MC-40798--> Adobe Commerce ontbreekt niet meer met een uit-van-geheugenfout wanneer het uitvoeren van de `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` methode tijdens `bin/magento setup:upgrade`. Eerder, gebruikte Adobe Commerce niet partijgrootte voor inzameling toen het initialiseren van toestemmingen, maar in plaats daarvan geladen een inzameling van alle bedrijfrollen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40551--> De gebruikers van het Bedrijf kunnen klanten de waarden van de douaneattributen nu uitgeven en bijwerken. Eerder waren deze kenmerken niet correct gekoppeld aan het formulier voor het maken en bewerken van gebruikers. Een bedrijfgebruiker kon verschillende kenmerkwaarden ingaan, maar Adobe Commerce heeft deze waarden niet correct bewaard.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-32653--> De middelboom voor de toestemmingen van de bedrijfrol kan nu worden vertaald zoals verwacht. Eerder was de machtigingenstructuur niet vertaald, ook al waren er geldige vertaalbestanden aanwezig.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce bewaart nu de waarden van de douaneklantenattributen voor B2B gebruikers zoals verwacht. Eerder leidde het maken van een bedrijfsaccount dat aangepaste klantkenmerken bevatte tot een sjabloonfout en kon Adobe Commerce het formulier niet laden. Door een argument toe te voegen aan de lay-out van `company_create_account` is dit probleem opgelost.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41721--> de gebruikersfilters van het Bedrijf zoals toon Alle Gebruikers, toon Actieve Gebruikers, en toon Inactieve Gebruikers nu werken zoals verwacht. Eerder, veroorzaakte het filtreren acties op de pagina van de bedrijfgebruiker een fout van JavaScript.

### Bedrijfskrediet

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41551--> Beheerders met beperkte rekeningen die slechts website-vlakke voorrechten omvatten kunnen nu een bedrijf tot stand brengen dat een verschillende munt dan de website gebruikt.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce verzendt nu bedrijfe-mails van het correcte `from` e-mailadres en werkingsgebied. Eerder heeft Adobe Commerce geen rekening gehouden met het bereik van de website bij het verzenden van een bedrijfskrediet of het bijwerken van een e-mail.

### Snelle bestelling

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42104--> Creërend een orde gebruikend Snelle Orde van een Csv- dossier nu werkt zoals verwacht met nonexistent SKUs.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40268--> het gebruiken van Snelle Orde aan onderzoek op veelvoudige SKUs werkt nu zoals verwacht. Eerder waren er dubbele vermeldingen in de resultaten opgenomen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40261--> de Toegevoegde de lijstvertoning van het Product behandelt nu SKUs ingegaan in kleine letters en in hoofdletters het zelfde wanneer u SKUs gebruikt om veelvoudige producten tijdens Snelle Orde te selecteren.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40225--> Gebruikend Snelle Orde voegt nu producten in de hoeveelheid toe die door de verkoopster wordt gespecificeerd. Eerder heeft Adobe Commerce slechts één product toegevoegd, zelfs als de door de winkel opgegeven hoeveelheden groter zijn dan één product.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41283--> de Snelle autocomplete eigenschap van de Orde werkt nu met gedeeltelijke SKUs.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce toont nu producten die als **niet zichtbaar individueel** op de Snelle pagina van de Orde auto-stelt lijst en onderzoeksresultaten zijn gevormd voor.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-42402--> de Kopers kunnen de Snelle vorm van de Orde nu gebruiken om veelvoudige producten door SKUs toe te voegen die karakters in hoofdletters omvatten. Eerder werd alleen het eerste product toegevoegd.

### Verhandelbaar aanhalingsteken

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41232--> De Klanten worden nu opnieuw gericht aan de onderhandelbare citaatpagina na het kleven van de verbinding aan een onderhandelbaar citaat op het gebied URL en met succes het programma openen. Eerder werd de koper doorgestuurd naar de pagina Mijn account.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39317--> die nu opnieuw rangschikt werkt zoals verwacht voor orden die een product met een Aanpasbare Optie van de Datum voor een klantenrekening bevatten die tijdens controle werd gecreeerd. Eerder heeft Adobe Commerce de reorder niet verwerkt en deze fout weergegeven: `The product has required options. Enter the options and try again` .

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39063--> Het verschepende adres voor een verhandelbaar citaat is niet meer editable tijdens controle wanneer de module van de Orde van de Aankoop wordt onbruikbaar gemaakt. Dit gedrag is het gevolg van een vorige correctie waarbij `isQuoteAddressLocked` is verwijderd uit de verhandelbare renderer voor het uitchecken van aanhalingstekens.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-38967--> De handelaren kunnen producten aan een onderhandelbaar citaat van Admin nu toevoegen.

### Aankooporders

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce toont nu een informatief foutenmelding zoals verwacht wanneer u een kooporder gebruikend Uitdrukkelijke Betaling PayPal plaatst wanneer het **[!UICONTROL Name Prefix]** attribuut aan `required` wordt geplaatst. Eerder heeft Adobe Commerce de bestelling niet geplaatst of een foutbericht weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39620--> De component UI voor het factureringsadres in de module van de Orde van de Aankoop gebruikt nu correct citaatadres wanneer de Manager van de Markering van Google wordt toegelaten. Er is eerder een JavaScript-fout opgetreden op de betalingspagina.

### Aanvraaglijsten

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40426--> De handelaren kunnen het POST `rest/all/V1/requisition_lists` eindpunt nu gebruiken om een vraaglijst voor een klant tot stand te brengen. Eerder heeft Adobe Commerce deze fout van 400 gegenereerd toen u een aanvraaglijst probeerde te maken: `Could not save Requisition List` .

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41123--> De **[!UICONTROL Add to Requisition List]** knoop verschijnt nu voor de producten van het winkelwagentje in voorraad wanneer het karretje ook uit-van-voorraad producten bevat. Als een winkelwagentje twee producten bevatte, waarvan er één uit voorraad was, werd de knop _[!UICONTROL Add to Requisition List]_&#x200B;eerder voor geen van beide producten weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40877--> U kunt REST API nu gebruiken om een product aan een verzoeklijst toe te voegen.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40155--> de lijstwaarden van de Vereiste **[!UICONTROL Latest Activity Date]** houden nu aan scèneformaat vast.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce werpt niet meer een fatale fout wanneer u een bundelproduct van een verzoeklijst uitgeeft.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce toont nu de correcte productprijs wanneer u een product met een klantgerichte optie `(File)` aan een verlanglijst van een verzoeklijst toevoegt. De koppeling naar het geüploade bestand is ook zichtbaar zoals u had verwacht. Eerder gaf Adobe Commerce onjuiste productprijzen weer en werd de koppeling naar het bestand niet weergegeven.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-36383--> de Producten met een klantgerichte optie `(File)` kunnen nu aan een het winkelwagentje van een verzoeklijst worden toegevoegd.

### Gedeelde catalogus

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40497--> een beheerder met een rol die tot een specifieke website wordt beperkt kan een gedeelde catalogus nu creëren, bekijken en uitgeven. Eerder gaf Adobe Commerce een fatale fout op toen een beheerder met een beperkte rol probeerde een gedeelde catalogus te creëren.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-41337--> Gelaagde navigatieresultaten omvatten nu een nauwkeurige telling van producten met gefilterde attributen, en de kopers kunnen veelvoudige filters nu toepassen. Eerder kon slechts één filter worden toegepast en gaf Adobe Commerce een onnauwkeurig aantal producten weer in gelaagde navigatie.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce toont nu correct productaantallen in gelaagde navigatiefilters in onderzoeksresultaten. Eerder gebruikte een insteekmodule voor de pagina met zoekresultaten geen Elasticsearch, maar werd een nieuwe query naar de database verzonden.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce schrapt niet meer laagprijzen wanneer een handelaar alle producten van een standaard gedeelde catalogus schrapt.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39802--> Filters worden nu gefiltreerd door de huidige categorie en correct getoond op alle pagina&#39;s wanneer de gedeelde catalogi worden toegelaten. Eerder werden filters alleen voor de huidige pagina verkeerd berekend en niet door de huidige categorie gefilterd.

![ Vaste kwestie ](../assets/fix.svg) <!--- MC-39522--> de vraag van GraphQL `products` keert niet meer de prijswaaier en de categorie van een product voor producten terug die niet aan een gedeelde catalogus worden toegewezen wanneer de gedeelde catalogus wordt toegelaten. Eerder gaf de query de aggregaties van het product, ook al werd het product zelf niet geretourneerd in de `items` -array.

## B2B v1.3.1

*9 Februari, 2021*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.2.

![ Nieuwe ](../assets/new.svg) Online betalingsmethodes worden nu gesteund voor kooporden.

![ Vaste kwestie ](../assets/fix.svg) Toevoegend een configureerbaar product aan het winkelwagentje direct van een verzoeklijst wanneer dit product in een vroegere orde werd gebruikt keert niet meer een systeemfout terug.

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu correct het Vereist Mijn lusje van de Goedkeuring voor kooporden wanneer een gespleten gegevensbestandconfiguratie wordt opgesteld.

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu details over bundelproducten en giftekaart wanneer u kooporden bekijkt.

![ Vaste kwestie ](../assets/fix.svg) De Klanten worden nu opnieuw gericht zoals verwacht na het registreren in hun rekening terwijl het doorbladeren in een opslag waar **[!UICONTROL Website Restriction]** wordt toegelaten en **[!UICONTROL Restriction Mode]** wordt geplaatst aan `Private Sales: Login Only`. Eerder werden kopers omgeleid naar de homepage van de winkel. <!--- MC-38934-->

![ Vaste kwestie ](../assets/fix.svg) de geschiedenis van de Orde laadt nu zoals verwacht in de pagina van het de rekeningsdashboard van een bedrijfbeheerder in plaatsingen met een B2B bedrijfshiërarchie die vele klanten (groter dan 13000) bevat. Eerder werd de volgorde van de historie traag of helemaal niet geladen en gaf Adobe Commerce een fout van 503 weer. <!--- MC-38830-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer veelvoudige identieke waarschuwingsberichten wanneer u een niet gevormd product met klantgerichte opties aan een Lijst van de Vereiste van een pagina van de Categorie toevoegt. <!--- MC-38342-->

![ Vaste kwestie ](../assets/fix.svg) Nieuwe en gedupliceerde producten zijn nu zichtbaar zoals verwacht op de categoriepagina wanneer B2B gedeelde catalogi worden toegelaten. <!--- MC-38307-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce handhaaft nu het correcte `store_id` dat met een bedrijfbeheerder wordt geassocieerd wanneer de klantengroep voor een bedrijf wordt bijgewerkt. Eerder is de waarde van `store_id` gewijzigd in de standaardwinkel toen de groep werd bijgewerkt. <!--- MC-38196-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce bewaart nu een gegroepeerd product aan een verzoeklijst als lijst van eenvoudige producten op de zelfde manier aangezien het een gegroepeerd product aan een winkelwagentje toevoegt. Als gevolg van de manier waarop Adobe Commerce gegroepeerde producten heeft opgeslagen, werd de koppeling voor een gegroepeerd product in de aanvraaglijst altijd doorgestuurd naar eenvoudige producten en niet naar het gegroepeerde product. <!--- MC-38049-->

![ Vaste kwestie ](../assets/fix.svg) u kunt orden door het **[!UICONTROL Company Name]** gebied nu filtreren wanneer het uitvoeren van ordeinformatie in formaat CSV. Eerder heeft Adobe Commerce een fout aangemeld in `var/export/{file-id}` . <!--- MC-37785-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu Create popup van de Lijst van de Vergunning zoals verwacht wanneer u creeert het Create Nieuwe lusje van de Lijst van de Vergunning op de storefront selecteert. <!--- MC-37915-->

![ de Vaste lijst van de kwestie ](../assets/fix.svg) Vereiste omvat nu alle gegroepeerde producten en hoeveelheden die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, gaf Adobe Commerce deze fout weer: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![ Vaste kwestie ](../assets/fix.svg) de correcte opslagmening wordt nu geassocieerd met de relevante website wanneer u een bedrijf in een plaatsing op meerdere plaatsen creeert. Eerder kon u geen bedrijf maken en Adobe Commerce gaf deze fout weer: `The store view is not in the associated website` . <!--- MC-37488-->

![ Vaste kwestie ](../assets/fix.svg) die tot producten door SKU opdracht geeft die Snelle Orde gebruikt niet meer in dubbele producthoeveelheden in het Csv- dossier resulteert. <!--- MC-37427-->

![ Vaste kwestie ](../assets/fix.svg) de **[!UICONTROL Add to Cart]** knoop wordt niet meer geblokkeerd wanneer de _[!UICONTROL Enter Multiple SKUs]_&#x200B;sectie van de Snelle pagina van de Orde een lege waarde bevat. In plaats daarvan geeft Adobe Commerce nu een bericht weer waarin u wordt gevraagd geldige SKU&#39;s in te voeren. <!--- MC-37387-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont nu dit bericht op de productpagina wanneer u een productoverzicht van een verzoeklijst indient: `You submitted your review for moderation`. De revisie wordt ook weergegeven op de pagina Revisies in behandeling (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]** ). Hoewel Adobe Commerce de revisie eerder heeft toegevoegd aan de lijst van lopende recensies, heeft het een fout van 404 op de productpagina geplaatst. <!--- MC-37119-->

![ Vaste kwestie ](../assets/fix.svg) De prestaties van de `sharedCatalogUpdateCategoryPermissions` consument zijn verbeterd. Na het creëren van een gedeelde catalogus, gebruikt de indexator van de catalogustoestemming nu slechts identiteitskaart van de klantengroep van de gedeelde catalogus, niet alle klantengroepen. <!--- MC-36770-->

&rbrack;(../assets/fix.svg) de gebieden van het de klantenadresattribuut van de klant van 0&rbrace; Vaste kwestie &lbrace;die met het niet-standaardadres van een verkoopster worden geassocieerd worden nu bewaard zoals verwacht in het storefront controlewerkschema. <!--- MC-36630-->!&lbrack;

![ Vaste kwestie ](../assets/fix.svg) Orders voor producten die tot het gebrek van een opslag gedeelde catalogus behoren kunnen nu voor kopers door Admin REST API (`rest/V1/carts/{<CART_ID>/items`) worden geplaatst zoals verwacht. Adobe Commerce controleert nu of het product aan een openbare catalogus is toegewezen voordat de validatie van gedeelde catalogusmachtigingen in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave` wordt uitgevoerd. Eerder heeft Adobe Commerce het product niet aan de winkelwagentje toegevoegd en deze fout gegenereerd: `No such shared catalog entity` . <!--- MC-36535-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce verzendt nu nieuwe e-mails van de bedrijfs gebruikersregistratie van het adres van de opslag van Adobe Commerce. Eerder werd deze e-mail verzonden van het adres van de bedrijfbeheerder. <!--- MC-36480-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce controleert nu douanekenmerken voor duplicatie van gereserveerde namen van bedrijfattributen alvorens een handelaar toe te laten om een nieuw attribuut te bewaren. <!--- MC-36282-->

![ Vaste kwestie ](../assets/fix.svg) de `credit_history` vraag keert nu de gespecificeerde kredietgeschiedenis van het bedrijf voor zowel het oorspronkelijk toegewezen bedrag als het gekochte bedrag terug. Eerder heeft deze query een fout geretourneerd.

![ Vaste kwestie ](../assets/fix.svg) de **[!UICONTROL Company]** en **[!UICONTROL Job Title]** gebieden op de Edit pagina van de Informatie van de Rekening zijn niet meer editable.

### Bekende problemen

- B2B-kopers kunnen online betalingsmethoden gebruiken om de gebruikelijke inkooporderstroom te omzeilen. Dit scenario kan zich voordoen als de koper zijn volledige afhandelingstotaal tot 0 kan terugbrengen — bijvoorbeeld door een promotiecode of een cadeaukaart — en vervolgens de code of geschenkkaart kan verwijderen. Zelfs onder deze omstandigheden plaatst Adobe Commerce nog steeds de order voor het juiste bedrag op basis van de prijzen van de items in de toegewezen catalogus. **_Oplossing_**: maak geschenkkaarten en couponcodes onbruikbaar wanneer de online betalingsmethodes voor de goedkeuring van de inkooporde worden toegelaten. <!--- B2B-1603-->

- Kopers worden omgeleid naar het winkelwagentje wanneer ze een bestelling proberen te plaatsen via een inkooporder met PayPal Express Checkout wanneer **[!UICONTROL In-Context Mode]** is uitgeschakeld. <!--- B2B-1604-->

- Adobe Commerce geeft soms een fout van 404 weer wanneer een koper een inkooporder maakt en vervolgens naar de afhandelingspagina navigeert. Deze fout treedt op wanneer een koper eerder een andere inkooporder met een online betalingsmethode heeft gemaakt voordat hij naar de betalingspagina navigeert zonder de vorige aankoop te voltooien. De koper kan de kooporder nog steeds plaatsen. **_werk rond_**: niets. <!--- B2B-1605-->

- Kortingen voor een specifieke betalingsmethode blijven bestaan tijdens afhandeling voor een inkooporder, zelfs als de koper zijn betalingsmethode wijzigt tijdens de laatste afhandeling. Als gevolg hiervan kunnen klanten een korting ontvangen waarop ze geen recht hebben. Deze kwestie doet zich voor omdat ondanks de wijziging in de betalingsmethode nog steeds een kartregel voor de oorspronkelijke betalingsmethode wordt toegepast. **_werk rond_**: niets. Zie [ Adobe Commerce 2.4.2 B2B bekende kwestie: de korting blijft voor online Orden van de Aankoop nadat de betalingsmethode ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _artikel van de Kennisbank_ wordt veranderd. <!-- B2B-1012 -->

- De query `deleteRequisitionListOutput` retourneert details over de verwijderde aanvraaglijst in plaats van de resterende aanvraaglijsten. <!--- MC-39894-->

## B2B v1.3.0

*15 oktober 2020*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

Deze release bevat verbeteringen voor goedkeuringen voor bestellingen, verzendmethoden, winkelwagentje en registratie van beheeracties.

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.1.

![ de Nieuwe ](../assets/new.svg) B2B ordesgoedkeuringen zijn verbeterd om bruikbaarheid te verbeteren en voor bulkacties op kooporden toe te staan.

![ Nieuwe ](../assets/new.svg) B2B de handelaren kunnen verzendingsmethodes nu controleren die aan elk Bedrijf worden aangeboden.<!--- BUNDLE-160 161 162 -->

![ Nieuwe ](../assets/new.svg) Merchants kunnen gebruikers nu toestaan om de inhoud van hun winkelwagentje in één enkele actie te ontruimen en kunnen deze capaciteit onafhankelijk op elke website vormen <!--- BUNDLE-108 -->

![ de Nieuwe ](../assets/new.svg) B2B kopers kunnen individuele punten of de volledige inhoud van hun winkelwagentje direct aan een verzoeklijst nu toevoegen. <!--- BUNDLE-145 144-->

![ Nieuwe ](../assets/new.svg) B2B handelaren kunnen orden van Admin namens klanten tot stand brengen gebruikend Betaling op Rekening als betalingsmethode. <!--- BUNDLE-166 178-->

![ Nieuwe ](../assets/new.svg) Merchants kunnen alle citaten direct bekijken verbonden aan een gebruiker van de de detailpagina van de klant. <!--- BUNDLE-139 -->

![ Nieuwe ](../assets/new.svg) Merchants kunnen de Klanten nu Online net door Bedrijf filtreren. <!--- BUNDLE-137 -->

![ Nieuwe ](../assets/new.svg) Admins kan klanten in Admin door Verkoper nu filtreren. <!--- BUNDLE-110 -->

![ Nieuw ](../assets/new.svg) om verwezenlijking van frauduleuze of spamrekeningen te verminderen, kunnen de handelaren Google reCAPTCHA op de Nieuwe vorm van het Verzoek van het Bedrijf op de winkel nu toelaten. <!--- BUNDLE-154 -->

![ Nieuwe ](../assets/new.svg) acties Admin die in de modules van het Bedrijf worden genomen worden nu het programma geopend het Logboek van Acties Admin. Handelingen worden vanuit alle relevante bedrijfsmodules geregistreerd: `Company` , `NegotiableQuote` , `CompanyCredit` , `SharedCatalog` . <!--- BUNDLE-180 181 182 183 -->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer de **[!UICONTROL Delete customer]** knoop op de **Klanten** pagina wanneer de het programma geopende beheerder geen rechten heeft om klanten in plaatsingen te schrappen waar B2B geïnstalleerd is. <!--- MC-35655-->

![ Vaste kwestie ](../assets/fix.svg) de groep van de Klant wordt niet meer automatisch veranderd voor een klant die aan een Bedrijf wordt toegewezen wanneer u de klant op het net van de Klant uitgeeft. <!--- MC-35254-->

![ Vaste kwestie ](../assets/fix.svg) wanneer een handelaar tot een gedeelde catalogus leidt, worden de toestemmingen nu automatisch geplaatst aan `Allow` voor de **[!UICONTROL Display Product Prices]** en **[!UICONTROL Add to Cart]** eigenschappen in categorieën wanneer de klantengroep deze toegang in de montages van de catalogustoestemming wordt toegewezen. Eerder, werden deze montages automatisch geplaatst aan `Deny` zelfs toen catalogustoestemmingen aan `Allow` werden geplaatst.<!--- MC-34792-->

&rbrack;(../assets/fix.svg) Gedeelde de categorietoestemmingen van de 0&rbrace; Vaste kwestie &lbrace;worden niet meer beschreven wanneer een product van de product uitgeeft pagina wordt uitgegeven.<!--- MC-34777-->!&lbrack;

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce verzendt nu een e-mailbericht bevestigend dat een klant toestemming heeft om de aangewezen kredietgrens te overschrijden wanneer een handelaar **[!UICONTROL Allow To Exceed Credit Limit]** het plaatsen toelaat. Eerder gaf het e-mailbericht van Adobe Commerce aan dat de klant geen toestemming had om de limiet te overschrijden. <!--- MC-34584-->

![ Vaste kwestie ](../assets/fix.svg) de container van HTML die productprijs op aanvraaglijsten omringt wordt nu correct teruggegeven voor de kinderen van gebundelde producten. <!--- MC-36331-->

![ Vaste kwestie ](../assets/fix.svg) de Merchants kunnen nu de taal aanwijzen waarin de bedrijfgebruiker e-mail wordt verzonden wanneer het creëren van een bedrijf in meertalige plaatsingen. Eerder, laat het drop-down menu verkopers toe om de aangewezen opslagmening te selecteren en de taal werd niet getoond.  <!--- MC-35777-->

&rbrack;(../assets/fix.svg) de gebieden van de de klantenadresattributen van 0&rbrace; Vaste kwestie &lbrace;worden de gebieden van het klantenadres van de douane nu getoond zoals verwacht in het storefront controlewerkschema. <!--- MC-35607-->!&lbrack;

![ Vaste kwestie ](../assets/fix.svg) het B2B lusje van de configuratie van Eigenschappen opent nu correct. <!--- MC-35458--> de Gasten kunnen QuickOrder nu gebruiken om producten aan hun kar toe te voegen en dan met succes punten te verwijderen. Eerder, toen een verkoopster QuickOrder gebruikte om veelvoudige producten aan hun kar toe te voegen, en dan een product te verwijderen, werd het product niet verwijderd. <!--- MC-35327-->

![ Vaste kwestie ](../assets/fix.svg) Een bedrijf kan nu worden bijgewerkt gebruikend het REST API PUT `/V1/company/:companyId` verzoek zonder `region_id` te specificeren wanneer de staat als **wordt gevormd niet vereist**. Hoewel `region_id` voorheen niet vereist was, gaf Adobe Commerce een fout als deze niet was opgegeven. <!--- MC-35304-->

![ Vaste kwestie ](../assets/fix.svg) wanneer u creeert of een B2B Bedrijf bijwerkt gebruikend REST API (`http://magento.local/rest/V1/company/2`, waar `2` bedrijfsidentiteitskaart) vertegenwoordigt, omvat de reactie nu de montages voor `applicable_payment_method` of `available_payment_methods` zoals verwacht. <!--- MC-35248-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce toont niet meer een 404 pagina wanneer een handelaar **gaat** knoop in plaats van het klikken van de **[!UICONTROL Save]** knoop wanneer het creëren van een verzoeklijst op de storefront.<!--- MC-35094-->

![ Vaste de toestemmingen van de 1&rbrace; Categorie van de kwestie &lbrace;veranderen niet meer wanneer een nieuw product aan een openbare gedeelde catalogus wordt toegewezen. ](../assets/fix.svg) Eerder werden categorietoestemmingen gedupliceerd. <!--- MC-34386-->

![ Vaste kwestie ](../assets/fix.svg) het REST API eindpunt PUT `rest/default/V1/company/{id}`, dat wordt gebruikt om bedrijfs-e-mail bij te werken, is niet meer case-sensitive. <!--- MC-34308-->

![ Vaste kwestie ](../assets/fix.svg) het onbruikbaar maken beloningsmodules beïnvloedt niet meer B2B eigenschappen op klantenrekeningen. Eerder, toen de beloningsmodules onbruikbaar werden gemaakt, werden de volgende B2B-Verwante lusjes niet getoond: Het Profiel van het Bedrijf, de Gebruikers van het Bedrijf, en Rollen en Toestemmingen.<!--- MC-34191-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce gebruikt nu de correcte afzendernaam op e-mailberichten wanneer de veranderingen in bedrijfrekeningen worden aangebracht. Eerder, gebruikte Adobe Commerce de algemene naam van de contactafzender die in het standaardwerkingsgebied voor alle e-mails wordt bepaald. <!--- MC-33917-->

![ Vaste kwestie ](../assets/fix.svg) U kunt multiShipping voor orden nu met succes uitvoeren die zowel fysieke als virtuele producten bevatten. <!--- MC-33818-->

![ Vaste kwestie ](../assets/fix.svg) De handelaren kunnen bedrijfgebruikers van de _[!UICONTROL Company Users]_&#x200B;sectie in Mijn pagina&#39;s van de Structuur van de Rekening en van het Bedrijf nu tot stand brengen wanneer **[!UICONTROL Access Restriction]**&#x200B;wordt toegelaten en **[!UICONTROL Restriction Mode]**&#x200B;aan `Sales: Login Only` wordt geplaatst. Eerder heeft Adobe Commerce deze fout gegenereerd toen een handelaar een gebruiker probeerde te maken: `Can not register new customer due to restrictions are enabled` . <!--- MC-33608-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce stelt niet meer de klantengroep van een klant aan het gebrek terug wanneer een klant hun rekeningsinformatie bewaart. <!--- MC-33554-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce werpt niet meer een fatale fout wanneer een beheerder een klant toewijst die een actief het winkelwagentje aan een klantengroep heeft. <!--- MC-33313-->

![ Vaste kwestie ](../assets/fix.svg) Adobe Commerce verstrekt nu een `addToCart` gebeurtenis DataLayer voor de Snelle lijsten van de Orde en van de Vereiste pagina&#39;s.  <!--- MC-33295-->

![ Vaste de e-mails van de kwestie ](../assets/fix.svg) Bericht die naar verkoopvertegenwoordigers worden verzonden die aan een bedrijf worden toegewezen omvat nu het toegewezen collectieve embleem. Eerder bevatte het e-mailbericht het standaard LUMA-logo, niet het geüploade bedrijfslogo. <!--- MC-33232-->

![ Vaste kwestie ](../assets/fix.svg) A de verzoeklijst omvat nu alle gegroepeerde producten en hoeveelheden die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, gaf Adobe Commerce deze fout weer: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![ Vaste kwestie ](../assets/fix.svg) de `products` vraag keert nu een nauwkeurig `total_count` gebied terug wanneer de gedeelde catalogus wordt toegelaten. <!--- MC-42268-->

![ Vaste kwestie ](../assets/fix.svg) de Configuratie van het Bedrijf en creeer nu de pagina&#39;s van het Bedrijf zoals verwacht na u een online het verschepen methode onbruikbaar maakt. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected` . <!--- MC-43178-->

![ Vaste kwestie ](../assets/fix.svg) het de testgeheugenconsumptie van de Integratie is verminderd, die testprestaties verbetert en de tijd vermindert die voor testvoltooiing wordt vereist. <!--- AC-266-->

## B2B v1.2.0

*28 juli, 2020*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

![ Nieuwe ](../assets/new.svg) Toegevoegde steun voor Adobe Commerce 2.4.0.

![ Nieuw ](../assets/new.svg) Onderzoek van de Orde van de Storefront, met toegevoegde dank voor bijdrage door Marek Mularczyk van [ Divante ](https://www.divante.com/) en communautaire leden.

![ Nieuwe ](../assets/new.svg) Orders van de Aankoop worden verbeterd en herschreven. Ze zijn nu standaard opgenomen in Adobe Commerce.

![ Nieuwe ](../assets/new.svg) Regels van de Goedkeuring van de Inkooporder zijn uitgevoerd. Met deze regels kunnen gebruikers de workflow voor inkooporders beheren door aankoopregels voor bestellingen te maken.

![ Nieuwe ](../assets/new.svg) Login als Klant is nu inbegrepen door gebrek in Adobe Commerce. Deze eigenschap staat plaatswerknemers toe om klanten bij te staan door zich aan te melden als klant om te zien wat zij zien.

![&#128279;](../assets/fix.svg) de samenvoegingen van het Attribuut van 0&rbrace; Vaste kwestie &lbrace;werken nu correct voor Gelaagde Navigatie met Elasticsearch

![ Vaste kwestie ](../assets/fix.svg) Het zoeken van orden door speciale karakters werkt nu behoorlijk.

![ Vaste kwestie ](../assets/fix.svg) het klikken van de **[!UICONTROL Clear All]** Knoop breidt nu alle filters uit, eerder dan het doen ineenstorten van hen.

![ Vaste kwestie ](../assets/fix.svg) Product SKU/Naam is nu inbegrepen in de het onderzoeksfiltersamenvatting van de Geschiedenis van de Orde.

![ Vaste kwestie ](../assets/fix.svg) Sorterende Indicator wordt nu getoond behoorlijk in het Mijn Net van de Orden van de Aankoop.

![ Vaste kwestie ](../assets/fix.svg) nu, kunt u klikken goedkeuren, annuleert, verwerpt, en de knopen van de Orde van de Aankoop slechts eenmaal. Eerder kon u meerdere keren op de knop klikken.

![ Vaste kwestie ](../assets/fix.svg) De Bevel van de Aankoop keurt, verwerpt, annuleert, en bevestigt knopen nu correct op mobiele apparaten terug.

![ Vaste kwestie ](../assets/fix.svg) eerder, goedkeurend een Inkooporder met een korting die is verlopen plaatste de orde bij het volledige bedrag en werkte niet het totaal van de Inkooporder bij. Nu wordt het totaal van de inkooporder bijgewerkt om het juiste totaal weer te geven.

![ Vaste kwestie ](../assets/fix.svg) Een kwestie werd geïntroduceerd in 2.3.4 waar de attributen van de douaneverlenging niet van het Adres van de Klant aan het Adres van het Citaat zouden worden gekopieerd. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) met geïnstalleerd B2B, zou een SQL fout verschijnen wanneer het toewijzen van categorieën aan gedeelde catalogi. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) wegens een onjuiste veranderlijke typewaarde, konden beheerders geen configureerbare producten aan een orde toevoegen. De keuzelijst met opties wordt niet gevuld. Deze functie werkt nu goed.

![ Vaste kwestie ](../assets/fix.svg) eerder, wanneer het uitgeven van de Toestemmingen van de Categorie voor niet Gelogde binnen groep, zou een fout voorkomen wanneer het bewaren van de veranderingen. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) een moeilijke situatie wordt toegevoegd om opslagbeheerders toe te staan om producten aan een orde toe te voegen die niet in de gedeelde catalogus zijn. Er wordt eerder een foutbericht weergegeven wanneer u een item toevoegt dat zich niet in de catalogus bevindt.

![ Vaste kwestie ](../assets/fix.svg) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} eerder, na het in werking stellen van het bevel `php bin/magento indexer:set-dimensions-mode catalog_product_price website` en dan het proberen om een gedeelde catalogus tot stand te brengen, zou een fout voorkomen. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) toen het toevoegen van een bedrijf en het toewijzen van de bedrijfbeheerder aan een niet-standaard website, werd verkeerde plaatsidentiteitskaart verzonden, veroorzakend een fout. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) eerder, nadat een klant aan een andere klantengroep werd bewogen, die een product aan een orde toevoegt gebruikend _Snelle Orde_ zou met een fout ontbreken. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) eerder, toen het proberen om uit te checken gebruikend WebAPI met een citaat B2B, werd een onjuiste waarde verzonden naar API, veroorzakend een fout om voor te komen. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) eerder, wanneer het plaatsen van een bedrijf aan &quot;Actief&quot;via API, zou een fout voorkomen. Dit probleem is nu opgelost.

![ Vaste kwestie ](../assets/fix.svg) wegens een onnodige `form` markering, verfrist de ordepagina automatisch wanneer u binnengaan na het veranderen van een voorgestelde het verschepen tarief duwde. Dit probleem is opgelost.

![ Vaste kwestie ](../assets/fix.svg) eerder, toen het plaatsen van een grens van de productvertoning op een cataloguspagina en die grens was minder dan het aantal totale producten, kwam een fout voor. Die functie werkt nu zoals u had verwacht.

![ Vaste kwestie ](../assets/fix.svg) eerder, toen het veranderen van admin van een bedrijf, het originele adminadres aan nieuwe admin zou worden gekopieerd, die hen twee adressen geven. Nu wordt alleen het juiste adres toegevoegd.

![ Vaste kwestie ](../assets/fix.svg) eerder, gebruikend API om een citaatpunt op te slaan wanneer het git aan &quot;Toegestaan wordt geplaatst en Klant&quot;op de hoogte brengt zou ontbreken. Deze API-aanroep werkt nu zoals u had verwacht.

![ Vaste kwestie ](../assets/fix.svg) De Vaste Belasting van het Product wordt nu getoond op de de detailpagina van Citaten.

![ Vaste kwestie ](../assets/fix.svg) eerder, klikkend een gehechtheid op het lusje van Commentaren van de Mijn pagina van Citaten zou er niet in slagen om het dossier te downloaden. Dit gedrag werkt nu zoals verwacht.

### Bekende problemen

- Adobe Commerce genereert een uitzondering tijdens de upgrade naar B2B 1.2.0 in een implementatie voor meerdere websites. Wanneer `setup:upgrade` wordt uitgevoerd, treedt deze fout op in de module `PurchaseOrder` module: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder` . **Oplossing**: Installeer de `B2B-716 Add NonTransactionableInterface` interface aan `InitPurchaseOrderSalesSequence` hotfix van het gegevenspatroon, die nu van **Mijn Rekening** beschikbaar is > **downloadt** sectie van `magento.com`.
- Als een kortingscode vervalt voordat een inkooporder (PO) wordt goedgekeurd, blijft de inkooporder het gedisconteerde bedrag weergeven, maar als de inkooporder eenmaal is goedgekeurd, wordt de order geplaatst op het niet-gedisconteerde totaal. **Oplossing**: Installeer `B2B-709 Purchase Order Discount patch` hotfix voor deze kwestie, die nu van **Mijn Rekening** > **Downloads** sectie van `magento.com` beschikbaar is.
- Als de items in een inkooporder niet in voorraad zijn of niet voldoende in voorraad zijn wanneer de inkooporder wordt omgezet in een werkelijke bestelling, treedt er een fout op. Als backorders worden ingeschakeld, wordt de volgorde op de normale wijze verwerkt.
