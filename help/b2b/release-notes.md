---
title: '[!DNL Adobe Commerce B2B] releaseopmerkingen'
description: Herzie de versienota's voor informatie over veranderingen in  [!DNL Adobe Commerce B2B]  versies.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 976b91c6b205160b1f12cd9bad35ac0c5cf23e68
workflow-type: tm+mt
source-wordcount: '9502'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] releaseopmerkingen

In deze releaseopmerkingen voor de B2B-extensie worden aanvullingen en correcties vastgelegd die Adobe tijdens een releasecyclus heeft toegevoegd, waaronder:

![&#x200B; Nieuwe &#x200B;](../assets/new.svg) Nieuwe eigenschappen
![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg) Oplossingen en verbeteringen
![&#x200B; Bekende kwestie &#x200B;](../assets/bug.svg) Bekende kwesties

>[!NOTE]
>
>Zie [&#x200B; de beschikbaarheid van het Product &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) voor informatie over versies van de B2B uitbreiding van Commerce die voor beschikbare versies van Adobe Commerce wordt gesteund.

## B2B v1.5.3-bèta1

*Maart 10, 2026*

Compatibel met Adobe Commerce versie 2.4.9-bèta1.

De B2B v1.5.3-bèta1-versie omvat kwaliteitsverbeteringen en oplossingen voor problemen. De versie omvat ook de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB26-05 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb26-05.html) worden gedocumenteerd.

### Verhandelbaar aanhalingsteken

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-11973 --> **Negotiable citaatafrekening met Payflow Pro** - Adobe Commerce plaatst nu met succes orden wanneer het uitchecken van een verhandelbaar citaat gebruikend de de creditcardbetalingsmethode van de Payflow Pro. Als B2B-functies waren ingeschakeld en een koper via een verhandelbaar aanhalingsteken afhandelde, zorgde het selecteren van Payflow Pro en het klikken op Place Order ervoor dat de pagina oneindig bleef laden, zonder foutbericht, en dat de bestelling nooit werd gemaakt.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-13447 --> **het bericht van het Succes nadat het behandelbare citaat anders noemt** - Adobe Commerce toont nu constant een succesbericht nadat een bespreekbaar citaat of citaatmalplaatje op de storefront anders wordt genoemd. Eerder, wanneer een koper een onderhandelbaar citaat anders noemde, zou het succesbericht periodiek niet verschijnen (vaak die bijna onmiddellijk ontruimen), die ook geautomatiseerde tests veroorzaakte die op dit bericht wachten om te ontbreken alhoewel het anders noemen verrichting zelf slaagde.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-15280 --> **Verzendkosten in PayPal Uitdrukkelijke verhandelbare prijscontrole** - Adobe Commerce past nu de correcte verzendkosten toe wanneer het voltooien van een Uitdrukkelijke Controle van PayPal voor een goedgekeurd verhandelbaar citaat. Eerder werden de verzendkosten onjuist verdubbeld, wat leidde tot opgeblazen totalen.

### Aankooporders

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- ACP2E-3727 --> **totalen van de Inkooporder met Grensoverschrijdende handel** - een orde bevat nu correcte totalen wanneer geplaatst van een bestaande Inkooporder met toegelaten Grensoverschrijdende Handel.

### Aanvraaglijst

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-15862 --> **Gegroepeerde producten in aanvraaglijsten met categorie toestemmingen** - Vaste een TypeError die optrad wanneer het toevoegen van gegroepeerde producten aan een gevraagde lijst met toegelaten categorietoestemmingen. Na de correctie worden productopties veilig als arrays verwerkt, zodat alle producttypen zonder fouten kunnen worden toegevoegd.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-8575 --> **voeg aan de knoop van de Lijst van de Vereiste op categoriepagina toe** - de [!UICONTROL Add to Requisition List] knoop is nu zichtbaar op de categoriepagina. Eerder verdween de knop wanneer gebruikers probeerden een product toe te voegen van de categoriepagina.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-14711 --> **de paginadrukoptie van de Lijst van de Aanvraag** - de optie van de Druk op de pagina van de Lijst van de Aanvraag werkt nu correct. Eerder leidde het klikken op [!UICONTROL Print] tot de fout: `An error has happened during application run. See exception log for details.`

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-16226 --> **de lijstverwezenlijking van de Verzoek met Add Code van de Opslag aan URLs** - Vaste een kwestie waar de verzoeklijsten niet voor producten konden worden gecreeerd die aan een nieuwe website en een bron worden toegewezen wanneer [!UICONTROL Add Store Code to URLs] wordt toegelaten. Het probleem is opgetreden omdat de opslagcode is verwijderd uit de API-aanvraag, waardoor een onbevoegde fout is opgetreden. Na de correctie blijft de juiste archiefcontext behouden en worden aanvraaglijsten gemaakt.

### Gedeelde catalogus

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- ACP2E-3796 --> **Gedeelde cataloguscategorie untask prestaties** - De prestaties zijn beduidend verbeterd wanneer het ontkennen van categorieën in een B2B gedeelde catalogus. Eerder duurde het lang voordat de toewijzing van categorieën via de REST API ongedaan werd gemaakt.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- ACP2E-4097 --> **product unassign van Gedeelde Catalogus** - Admin kan producten van de Gedeelde Catalogus nu met succes ontkoppelen. Eerder, resulteerde het ontkoppelen van producten met een groot aantal lange product SKUs van Gedeelde Catalogus in een fout.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-15662 --> **de Gedeelde taak van het catalogusbedrijf voor beperkte beheerders** - Vaste een kwestie waar de beperkte gebruikers Admin een uitzondering ontmoetten toen het toewijzen van een bedrijf aan een gedeelde catalogus.

### Winkelwagentje en uitchecken

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-15962 --> **Afhandeling opnieuw na zittingsafloop** - Vaste een kwestie waar de gebruikers aan de Mijn Login van de Rekening pagina in plaats van checkout login na zittingsafloop werden opnieuw gericht, die ervoor zorgen zij correct aan controle met de login vorm worden genomen.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- ACP2E-4223 --> **het adresbevestiging van de Controle voor REST en GraphQL** - de bevestiging van de het adresgegevens van de Klant is verbeterd om tussen REST en GraphQL voor controle consistenter te zijn.

### Kader

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- ACP2E-4040 --> **Frontend 500 fout van caching lay-outstructuur** - Vaste een kwestie waar een pagina een 500 fout wegens een onjuiste lay-outstructuur zou terugkeren die in de lay-out in het voorgeheugen onder wordt gebracht.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- AC-15347 --> **Commerce stilende middelen in Communautaire thema&#39;s** - Verwijderde Commerce-Enige het stileren middelen uit Communautaire thema&#39;s door hen aan hun respectieve modulefolders te verplaatsen. Hierdoor wordt voorkomen dat ongebruikte CSS in de Community Edition wordt gebundeld, waardoor overbodige lading wordt voorkomen en regels met dode stijl worden verwijderd terwijl de juiste opmaak wordt gegarandeerd wanneer Commerce-modules worden ingeschakeld.

### GraphQL

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- ACP2E-3399 --> **de fout van GraphQL formaat van de foutenreactie** - verwierp een vorige verandering die fouten in een verschillend formaat teruggaf. Mogelijke fouten worden nu op een consistente manier geretourneerd, zodat het GraphQL-schema niet wordt verbroken.

## B2B v1.5.2-p4

*Maart 10, 2026*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8-p4 van Adobe Commerce, 2.4.7-p9, en 2.4.6-p14 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p9, 2.4.6 tot 2.4.6-p14.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [&#x200B; het Bulletin van de Veiligheid APSB26-05 &#x200B;](https://helpx.adobe.com/security/products/magento/apsb26-05.html) worden gedocumenteerd.

## B2B v1.5.2-p3

*14 oktober 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8-p3 van Adobe Commerce, 2.4.7-p8, en 2.4.6-p13 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p7, 2.4.6 tot 2.4.6-p12.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [&#x200B; het Bulletin van de Veiligheid APSB25-94 &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-94.html) worden gedocumenteerd.

## B2B v1.5.2-p2

*Augustus 12, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8-p2 van Adobe Commerce, 2.4.7-p7, en 2.4.6-p12 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p6, 2.4.6 tot 2.4.6-p11.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [&#x200B; het Bulletin van de Veiligheid APSB25-71 &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-71.html) worden gedocumenteerd.

## B2B v1.5.2-p1

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8-p1 van Adobe Commerce, 2.4.7-p6, en 2.4.6-p11 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p5, 2.4.6 tot 2.4.6-p10.

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg) omvat de veiligheidsmoeilijke situaties die in [&#x200B; het Bulletin van de Veiligheid APSB25-50 &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

## B2B 1.5.2

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.8 van Adobe Commerce, 2.4.7-p5 en 2.4.6-p10 de versies van het veiligheidspatch.
Compatibel met Adobe Commerce-versies 2.4.7 tot 2.4.7-p4, 2.4.6 tot 2.4.6-p9.

De B2B v1.5.2 versie omvat kwaliteitsverbeteringen en insectenmoeilijke situaties.

### Bedrijfsbeheer

![&#x200B; Nieuwe &#x200B;](../assets/new.svg)<!-- B2B-4123 --> Beheerders kunnen veelvoudige bedrijven van één enkele rekening nu beheren gebruikend de schakelaar van het storefront bedrijf. Belangrijkste voordelen zijn:

- **Vereenvoudigd multi-bedrijf beheer** - de beheerders kunnen veelvoudige bedrijven van één gebruikersrekening nu controleren, die de behoefte elimineren om afzonderlijke logins voor elk bedrijf tot stand te brengen en te beheren.
- **Efficiënte bedrijfsomschakeling** - een intuïtieve interface staat beheerders toe om snel tussen bedrijven te schakelen en updates te maken, die productiviteit verbeteren wanneer het beheren van veelvoudige entiteiten.
- **Gestroomlijnde verrichtingen** - de regionale managers en bedrijfsleiders kunnen centraal al hun bedrijven beheren, toelatend snellere besluitvorming en vlottere bedrijfsverrichtingen.

Deze verbetering bouwt voort op het multi-company van B2B 1.5.0 vermogen van het lidmaatschap, dat gebruikers om tot veelvoudige bedrijven toeliet te behoren maar geen admin toegang over bedrijven steunde. De bedrijfschakelaar elimineert de behoefte aan afzonderlijke adminrekeningen terwijl het handhaven van juiste toegangscontroles en bedrijf-specifieke meningen.

### Bedrijf

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- B2B-4480 --> Vaste een kwestie waar de gastklanten een `No such entity with cartId = ?` foutenmelding zouden zien wanneer het aanmelden als bedrijfgebruiker met producten in hun het winkelwagentje.

### Verhandelbaar aanhalingsteken

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg) B2B v1.5.2 versie omvat de volgende moeilijke situaties voor verhandelbare citaten:

- &#x200B;<!-- B2B-3252 -->In het veld [!UICONTROL Line Item Discount Amount] wordt invoer nu gevalideerd om te voorkomen dat negatieve kortingswaarden worden ingevoerd.
- &#x200B;<!-- B2B-3224 -->Probleem met gebruikerservaring verholpen waarbij lange-line itemopmerkingen werden afgebroken en moeilijk leesbaar waren voor B2B-klanten.
- &#x200B;<!-- B2B-2865 -->B2B-klanten kunnen nu producthoeveelheden opgeven met decimale waarden (zoals 1,5 of 2,75) bij het maken van noteringen.

### Offertesjabloon

![&#x200B; Nieuwe &#x200B;](../assets/new.svg)<!-- B2B-4104 --> Nieuwe capaciteit voor B2B kopers en verkopers om externe documentverbindingen aan citaatmalplaatjes vast te maken. Met deze functie kunt u rechtstreeks vanuit aanhalingstekens koppelingen maken naar documenten die worden gehost in services zoals DocuSign en Adobe Sign, als aanvulling op de bestaande mogelijkheden voor bestandsbijlagen. Belangrijkste voordelen zijn:

- Gestroomlijnde samenwerking via directe toegang tot kritieke overeenkomsten en contracten
- Verbeterde transparantie met onmiddellijke toegang tot de meest recente documentatie
- Snellere prijsonderhandelingen, omdat bestanden niet hoeven te worden gedownload en geüpload
- Flexibel documentbeheer met externe hostingservices voor documenten

## B2B 1.5.1

*11 Februari, 2025*

[!BADGE &#x200B; Gesteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.7-p4+ en 2.4.6-p9+ de versies van het veiligheidspatch van Adobe Commerce.
Compatibel met Adobe Commerce-versies 2.4.8-beta1 tot 2.4.8-beta2, 2.4.7 tot 2.4.7-p3, 2.4.6 tot 2.4.6-p8.

De versie B2B v1.5.1 bevat kwaliteitsverbeteringen en oplossingen voor problemen.

### Bedrijf

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- B2B-4422 --> als een klant probeert om bedrijven op de pagina van de Details van het Citaat te schakelen, richt het systeem nu de klant aan een *Ontkende Toegang* pagina om ervoor te zorgen dat een citaat dat voor één bedrijf wordt gecreeerd niet kan worden gebruikt om een orde met de prijzen van een ander bedrijf te plaatsen. Voorheen kon een gebruiker een prijsopgave voor één bedrijf maken en vervolgens overschakelen op een ander bedrijf om een bestelling met verschillende prijzen te plaatsen.

### Korting op regelobjecten

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- B2B-2938 --> Verbeterde systeemefficiency door een prestatiesdegradatie te richten die in het scenario van de citaatherberekening wordt waargenomen. Eerder werden twee nieuwe entiteiten toegevoegd aan elk onderdeel van de winkelwagentje, wat een merkbare toename van de databaseaanvragen veroorzaakte, wat tot langzamere prestaties leidde.

### Verhandelbaar aanhalingsteken

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- B2B-3820 --> het systeem handhaaft nu de positie van elementen UI wanneer de bevestiging van JavaScript wordt toegepast op de *[!UICONTROL min/max qty]* gebieden op de pagina van het Malplaatje van het Citaat van de Opbrengst van de Luma. Als u eerder JavaScript-validatie toepaste op deze velden, werden andere UI-elementen op de pagina verschoven.

### Winkelwagentje

![&#x200B; Vaste kwestie &#x200B;](../assets/fix.svg)<!-- B2B-4222 --> introduceerde een nieuw het winkelwagentbeheerssysteem dat wordt ontworpen om de het winkelen ervaring voor gebruikers te stroomlijnen die veelvoudige bedrijfrekeningen beheren. Het nieuwe systeem associeert winkelwagentjes met individuele bedrijven eerder dan de klantenrekening om de het winkelen ervaring te stroomlijnen en het werkschema te verbeteren door de volgende mogelijkheden te steunen.

- **bedrijf-specifieke wortels** - De het kopen kaarten zijn nu verbonden met individuele bedrijven om bedrijf-specifieke tarifering en productopties te steunen.
- **Naadloze omschakeling** - de gebruikers kunnen gemakkelijk tussen verschillende bedrijfrekeningen schakelen zonder de inhoud van de kar van elk bedrijf te beïnvloeden.
- **Contextuele Integriteit** - Alle worteldetails blijven binnen de context van het respectieve bedrijf, die een verenigbare en betrouwbare het winkelen ervaring verstrekken.

## Eerdere versies

### B2B 1.5.0

*30 oktober, 2024*

[!BADGE &#x200B; Gesteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versies 2.4.7-p3+ en 2.4.6-p8+ de versies van het veiligheidspatch van Adobe Commerce.
Compatibel met Adobe Commerce-versies 2.4.8-beta1, 2.4.7 tot 2.4.7-p2, 2.4.6 tot 2.4.6-p7.

Adobe Commerce B2B versie 1.5.0 is ook compatibel met PHP 8.3 en steunt de [&#x200B; Server van de Toepassing van GraphQL &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

De B2B v1.5.0 versie omvat nieuwe eigenschappen, kwaliteitsverbeteringen, en insectenmoeilijke situaties.

>[!NOTE]
>
> Leer over achteruit-onverenigbaar veranderingen (BICs) die in B2B 1.5.0 versie door de hoogtepunten en verwijzingsinformatie in het [&#x200B; Achteruit Incompatibele onderwerp van Veranderingen &#x200B;](backward-incompatible-changes.md) worden geïntroduceerd.

#### Bedrijfsbeheer

- **Beheer van het Bedrijf**<!--B2B-2901--> - de Merchants kunnen de bedrijven van Adobe Commerce nu bekijken en beheren als hiërarchische organisaties door bedrijven aan aangewezen ouderbedrijven toe te wijzen. Nadat een bedrijf aan een ouder wordt toegewezen, kan de beheerder van het moederbedrijf de bedrijfrekening beheren. Alleen geautoriseerde beheergebruikers kunnen bedrijfstoewijzingen toevoegen en beheren. Voor details, zie [&#x200B; bedrijfshiërarchie beheren &#x200B;](manage-company-hierarchy.md).

- Voeg bedrijfstoewijzingen toe en beheer deze vanuit de nieuwe sectie *[!UICONTROL Company Hierarchy]* op de pagina *[!UICONTROL Company Account]* in Admin.

- U kunt bedrijven sorteren en filteren met de nieuwe instelling *[!UICONTROL Company Type]* . In het net van Bedrijven, wijst de *[!UICONTROL Company Type]* kolom erop of een bedrijf een individueel bedrijf of een deel van een organisatorische hiërarchie (ouder of kind) is.

- **beheert bedrijfconfiguratie bij schaal**<!--B2B-2849--> - verander snel bedrijfconfiguratie montages voor geselecteerde bedrijven gebruikend de *[!UICONTROL Change company setting]* bulkactie nu beschikbaar wanneer het beheren van bedrijven van het *[!UICONTROL Companies]* of *[!UICONTROL Company Hierarchy]* net. Als u bijvoorbeeld een nieuwe gedeelde catalogus voor een groep bedrijven maakt, kunt u de configuratie van de gedeelde catalogus in één actie wijzigen in plaats van elk bedrijf afzonderlijk te bewerken.

- API-ontwikkelaars kunnen het nieuwe eindpunt van de REST API voor bedrijfsrelaties `/V1/company/{parentId}/relations` gebruiken om bedrijfstoewijzingen te maken, weer te geven en te verwijderen. Zie [&#x200B; bedrijfvoorwerpen beheren &#x200B;](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) in de *Gids van de Ontwikkelaar van het Web API*.

#### Bedrijfsrekeningen

- &#x200B;<!--B2B-2828--> **multi-bedrijf taak** - vereenvoudig de toegang van de bedrijfrekening voor bedrijfgebruikers door een gebruiker aan veelvoudige bedrijven toe te wijzen. Als je bijvoorbeeld een koper hebt die bestelt van meerdere bedrijfssites, maak dan één account en ken alle bedrijven waar de koper mee werkt aan die account. Vervolgens kan de koper zich één keer aanmelden en schakelen tussen bedrijfsaccounts door het bedrijf in de winkel te kiezen.

>[!NOTE]
>
>Een bedrijfgebruiker kan aan veelvoudige bedrijven worden toegewezen, maar zij kunnen de bedrijfbeheerder voor slechts één bedrijf zijn.

- &#x200B;<!--B2B-2747--> **het werkingsgebiedselecteur van het Bedrijf** - verstrekt de capaciteit voor bedrijfgebruikers die aan veelvoudige bedrijven worden toegewezen om bedrijven op de storefront te veranderen. Wanneer het werkingsgebied wordt geschakeld, werken de gegevens bij om de informatie te tonen die op de nieuwe bedrijfcontext wordt gebaseerd. Als het nieuwe bedrijf bijvoorbeeld een andere gedeelde catalogus gebruikt, ziet de gebruiker van het bedrijf producten, prijzen en andere informatie op basis van de nieuwe gedeelde catalogus. De inhoud met betrekking tot orden, citaten, citaatmalplaatjes werkt ook bij gebaseerd op de context van het geselecteerde bedrijf.

>[!NOTE]
>
>De inhoud van het winkelwagentje weerspiegelt de items die door de huidige klant zijn geselecteerd. Als de klant een actieve winkelwagentje heeft en een ander bedrijf selecteert, wordt hen ertoe aangezet om de wagentje bij te werken om de productassortiment, de tarifering, en promotionele kortingen te weerspiegelen die op de nieuwe bedrijfcontext worden gebaseerd. Producten die niet beschikbaar zijn in de catalogus van het nieuwe bedrijf, worden uit het winkelwagentje verwijderd. Als het product een verschillende prijs of een beschikbaarheid heeft, werkt het karretje bij om de gegevens te weerspiegelen beschikbaar in de context van het geselecteerde bedrijf.<!--B2B-4222-->

- &#x200B;<!--ACP2E-1933--> De beheerders van het bedrijf kunnen bedrijfgebruikers van de storefront nu toevoegen. Eerder heeft Commerce een fout geregistreerd toen een Admin-gebruiker probeerde een nieuwe gebruiker toe te voegen: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123` .

#### Aanhalingstekens en aanhalingstekensjablonen

Verbeteringen in de mogelijkheden om offertes op te halen helpen kopers en verkopers om offertes beter te beheren en om te onderhandelen met prijsopgaven.

- **de malplaatjes van het Citaat** - <!--B2B-3367--> Kopers en verkopers kunnen het citaatproces nu stroomlijnen door herbruikbare en klantgerichte citaatmalplaatjes te creëren. Met behulp van aanhalingstekensjablonen kan het onderhandelingsproces voor aanhalingstekens eenmaal worden voltooid en kunnen kopers vooraf goedgekeurde gekoppelde aanhalingstekens genereren voor terugkerende orders in plaats van voor elke bestelling het onderhandelingsproces voor aanhalingstekens te doorlopen. Aanhalingssjablonen breiden de bestaande functionaliteit voor aanhalingstekens uit door de volgende geavanceerde functies toe te voegen:

- **de drempels van de Orde** staan verkopers toe om minimum en maximumorderverplichtingen te plaatsen, ervoor zorgend de koper aan overeengekomen-op koopgevolume volgt.
- **plaatsende minimum en maximumhoeveelheden van de puntorde** voorziet de koper van de flexibiliteit om ordehoeveelheden op het verbonden citaat aan te passen zonder een nieuw malplaatje of verdere onderhandeling te vereisen.
- **spoor het aantal verbonden citaten die en met succes voltooide orden** worden geproduceerd om inzichten in de naleving van onderhandelde overeenkomsten te bereiken.
- **Gekoppelde citaten** zijn vooraf goedgekeurde citaten die de koper van een actief citaatmalplaatje produceert om terugkomende die orden voor te leggen op de termijnen in het citaatmalplaatje worden besproken.

- **Verbeteringen aan bestaande citaatmogelijkheden**

- **bijgewerkte de regels van de Lijst van het Toegangsbeheer van Commerce (ACL)** staan B2B managers en supervisors toe om citaten en citaatmalplaatjes van ondergeschikte gebruikers te beheren. De afzonderlijke regels steunen korrelige configuratie voor mening, geef, en schrap toegang uit.

- **sparen Citaat als Ontwerp**<!--B2B-2566--> - wanneer het creëren van a [&#x200B; citaat verzoek &#x200B;](quote-request.md) van het het winkelwagentje, kunnen de kopers het citaat nu opslaan als ontwerp zodat zij het kunnen herzien en bijwerken alvorens het proces van de citaatonderhandeling met de verkoper in werking te stellen. Het conceptaanhalingsteken heeft geen vervaldatum. Kopers kunnen conceptobjecten vanuit de sectie [!UICONTROL My Quotes] van hun accountdashboard bekijken en bijwerken.

- **noem Citaat**<!--B2B-2596--> anders - de Kopers kunnen een citaatnaam van de [&#x200B; de detailpagina van het Citaat &#x200B;](account-dashboard-my-quotes.md#quote-actions) nu veranderen door de **[!UICONTROL Rename]** optie te selecteren. Deze optie is beschikbaar voor geautoriseerde kopers wanneer ze de prijsopgave bewerken. Gebeurtenissen van de naamwijziging worden opgenomen in het logboek met offertegeschiedenis.

- **Dubbele Citaat**<!--B2B-2701--> - de Kopers en de verkopers kunnen een nieuw citaat nu tot stand brengen door een bestaand citaat te kopiëren. Een exemplaar wordt gecreeerd van de het detailmening van het Citaat door **[!UICONTROL Create Copy]** op de [&#x200B; het detailmening van het Citaat &#x200B;](quote-price-negotiation.md#button-bar) in Admin of [&#x200B; Storefront &#x200B;](account-dashboard-my-quotes.md#quote-actions) te selecteren.

- **het citaat van de beweging citeert punt aan aanvraaglijst**<!--B2B-2755--> - de Kopers hebben nu de flexibiliteit om producten uit een citaat te verwijderen en hen te bewaren aan een verzoeklijst als zij beslissen om hen niet in het proces van de citaatonderhandelingen te omvatten.

- **verwijder veelvoudige producten uit a citaat**<!--B2B-2881--> - op citaten met een groot aantal producten, kunnen de kopers veelvoudige producten uit het citaat nu verwijderen door hen te selecteren tegelijkertijd en de *[!UICONTROL Remove]* optie van de *[!UICONTROL Actions]* controle op de de detailpagina van het Citaat te gebruiken. In vorige releases moest een koper de producten een voor een verwijderen.

- **het punt van de Lijn disconteren**<!--B2B-2597--> - tijdens citaatonderhandeling, kunnen de verkopers sluiten van de puntkorting van de lijn voor meer flexibiliteit gebruiken wanneer het toepassen van kortingen tijdens het proces van de citaatonderhandeling. Een verkoper kan bijvoorbeeld een korting op een speciaal regelobject toepassen op een object en het object vergrendelen om verdere kortingen te voorkomen. Wanneer een item is vergrendeld, kan de objectprijs niet worden bijgewerkt wanneer een korting op prijsniveau wordt toegepast. Zie [&#x200B; citaat van de Initiatie voor een koper &#x200B;](sales-rep-initiates-quote.md).

- **Bevestigingen voor bestaande citaatmogelijkheden**

- Wanneer verkopers op de knop *[!UICONTROL Print]* klikken in de gedetailleerde weergave van het citaat in Admin, wordt nu gevraagd het citaat op te slaan als een PDF. Eerder werden handelaren omgeleid naar een pagina met aanhalingsgegevens. <!--ACP2E-1984-->

- Eerder, toen het verzenden van een klantencitaat met `0` percentage en veranderend aantal, wierp Admin een uitzondering maar bewaarde de hoeveelheid. Na deze correctie wordt een juiste uitzondering met een bericht gegenereerd voor het geval 0%. <!--ACP2E-1742-->

- Tijdens prijsonderhandelingen kan een verkoper nu een `0%` korting opgeven in het veld Offerteprijskorting voor onderhandelde offerte en de prijsopgave terugsturen naar de koper. Als de verkoper eerder een korting van 0% heeft ingevoerd en het prijsopgave heeft teruggestuurd naar de koper, heeft de beheerder een foutbericht van `Exception occurred during quote sending` geretourneerd. <!--ACP2E-1742-->

- De validatie van ReCaptcha werkt nu correct tijdens het afrekenen voor een B2B citaat wanneer ReCaptcha V3 voor storefront afhandeling wordt gevormd. Eerder is de validatie mislukt met een `recaptcha validation failed, please try again` -foutbericht.  <!--ACP2E-2097-->

#### Aankooporders

- &#x200B;<!--ACP2E-1825-->Aankooporders kunnen niet meer worden geplaatst door een gebruiker die met het bedrijf is geassocieerd nadat het bedrijf is geblokkeerd. Eerder had een gebruiker die banden had met het bedrijf kooporders kunnen plaatsen wanneer het bedrijf werd geblokkeerd.

### B2B v1.4.2-p8

*14 oktober 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p8+ en 2.4.6-p13+ de versies van het veiligheidspatch.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-94 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-94.html) worden gedocumenteerd.

{{b2b-compatibility}}

### B2B v1.4.2-p7

*Augustus 12, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p7+ en 2.4.6-p12+ de versies van het veiligheidspatch.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-71 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-71.html) worden gedocumenteerd.

{{b2b-compatibility}}

### B2B v1.4.2-p6

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p6+ en 2.4.6-p11+ de versies van het veiligheidspatch.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-50 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

{{b2b-compatibility}}

### B2B v1.4.2-p5

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p5+ en 2.4.6-p10+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de patchreleases van Adobe Commerce 2.4.7-p5+ en 2.4.6-p10+.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-26 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-26.html) worden gedocumenteerd.

{{b2b-compatibility}}

### B2B v1.4.2-p4

*11 Februari, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p4+ en 2.4.6-p9+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de patchreleases van Adobe Commerce 2.4.7-p4+ en 2.4.6-p9+.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-08 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-08.html) worden gedocumenteerd.

{{b2b-compatibility}}

### B2B v1.4.2-p3

*8 Oktober, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p3+ en 2.4.6-p8+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de patchreleases van Adobe Commerce 2.4.7-p3+ en 2.4.6-p8+.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB24-73 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

{{b2b-compatibility}}

### B2B v1.4.2-p2

*6 Augustus, 2024*

*6 Augustus, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p2+ en 2.4.6-p7+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de patchreleases van Adobe Commerce 2.4.7-p2+ en 2.4.6-p7+.

- Omvat de veiligheidsmoeilijke situaties die in het Bulletin van de Veiligheid [&#x200B; worden gedocumenteerd APSB24-73 &#x200B;](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

{{b2b-compatibility}}

### B2B v1.4.2-p1

*9 augustus, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.7-p1+ en 2.4.6-p6+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de patchreleases van Adobe Commerce 2.4.7-p1+ en 2.4.6-p6+.

{{b2b-compatibility}}

### B2B v1.4.2

*10 oktober, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} versie 2.4.7 van Adobe Commerce en versie van 2.4.6 aan 2.4.6-p5.

De B2B v1.4.2 versie omvat kwaliteitsverbeteringen en insectenmoeilijke situaties.

- &#x200B;<!--B2B-2897-->Als een verkoper een aanhalingsteken voor de koper maakt met een product-SKU die niet beschikbaar is in de gedeelde catalogus die bij de koper hoort, wordt het foutbericht weergegeven `The SKU you entered is not available in the shared catalog. Please check the SKU and try again` .  De verkoper kan de prijsopgave pas opslaan als hij het product verwijdert dat niet beschikbaar is. Eerder, werd het citaat bewaard met niet beschikbare inbegrepen SKU, en het citaat kon niet op de storefront laden.

>[!IMPORTANT]
>
>Adobe Commerce B2B versie 1.4.2+ is compatibel met PHP 8.2. Als u de Commerce-instantie upgradet naar versie 2.4.7+, moet u ervoor zorgen dat de instantie PHP versie 8.2 gebruikt om de compatibiliteit met Adobe Commerce B2B-versie te behouden. Bovendien, steunt B2B 1.4.2+ momenteel niet de [&#x200B; Server van de Toepassing van GraphQL &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

### B2B v1.4.1

*7 Augustus, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} [&#x200B; Adobe Commerce 2.4.6-p2 &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1.

De versie B2B v1.4.1 bevat kwaliteitsverbeteringen en oplossingen voor problemen.

- &#x200B;<!--ACP2E-1825-->Aankooporders kunnen niet meer worden geplaatst door een gebruiker die met het bedrijf is geassocieerd nadat het bedrijf is geblokkeerd. Eerder had een gebruiker die banden had met het bedrijf kooporders kunnen plaatsen wanneer het bedrijf werd geblokkeerd.

- &#x200B;<!--ACP2E-1943-->De status met terugwerkende kracht van het product wordt nu correct weergegeven in de winkel. Eerder werden producten die voor verzending beschikbaar waren, onjuist geïdentificeerd als achtergeordend.

- &#x200B;<!--ACP2E-1862-->Als het bedrijfsregistratieformulier een kenmerk van het type klantbestand bevat, wordt het bestand dat tijdens het registratieproces is geüpload, nu opgenomen in de accountgegevens voor de bedrijfsbeheerder nadat het bedrijf is gemaakt. Eerder ontbrak de bijlage.

- &#x200B;<!--ACP2E-1793-->De staalkiezer voor een configureerbaar product wordt nu weergegeven zoals u verwacht op de pagina met de configuratie van items in de lijst met aanvragen. Eerder, werd de monsterselecteur getoond als dropdown gebied in de pagina van de de puntconfiguratie van de verzoeklijst.

- &#x200B;<!--ACP2E-1968-->Wanneer het gebruiken van de [&#x200B; vraag van GraphQL van het Bedrijf &#x200B;](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) om bedrijfdetails terug te keren, zijn de resultaten nu met succes zonder fout teruggekeerd.

### B2B v1.4.0

*13 Juni, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} [&#x200B; Adobe Commerce 2.4.6-p1 &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1.

Deze release bevat nieuwe mogelijkheden en verbeteringen voor B2B-onderhandelbare aanhalingstekens en meerdere opgeloste problemen.

- Toegevoegde compatibiliteit met Adobe Commerce 2.4.7-beta1.

- **Verkoper stelde citaten in werking** - Verkopers kunnen nu een citaat voor een koper direct van het Citaat en de netten van de Klant in Admin in werking stellen. Dit vermogen stroomlijnt het prijsverhogingsproces en vermindert ingewikkeldheid voor klanten. Als een klant geen bestelling heeft geïnitieerd, kan een verkoper snel een prijsopgave namens de klant maken en het onderhandelingsproces starten. Eerder konden prijsopgaven alleen door de koper of door een verkoper die zich als klant heeft aangemeld, van de winkel worden gemaakt.

- **het puntkortingen van de Lijn en onderhandeling** - <!--B2B-2440--> binnen een citaat, kunnen de kopers B2B en de verkopers nu op het niveau van het lijnpunt onderhandelen, die kortingen toepassen en nota&#39;s ruilen tot een overeenkomst wordt bereikt. De verwezenlijking van de nota en de updates zijn inbegrepen in het lijnpunt en citaatgeschiedenis om mededeling te volgen. Eerder konden kopers en verkopers alleen opmerkingen uitwisselen en kortingen toepassen op het prijsniveau.

- Adobe Commerce geeft nu de juiste gegevens weer tijdens de betaling wanneer de optie Aankooporders is ingeschakeld en er een virtueel prijsopgave is geselecteerd die met de PayPal-betalingsoptie is gemaakt. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

- &#x200B;<!--ACP2E-1504--> Validatiefouten treden niet meer op wanneer u een bedrijf probeert op te slaan met een kredietlimiet die hoger is dan 999. Eerder, voor bedrijfskredietgrenzen groter dan 999, nam Adobe Commerce een kommascheidingsteken op, dat een bevestigingsfout veroorzaakte die updates verhinderde worden bewaard.

- &#x200B;<!--ACP2E-1474--> Het geselecteerde verzendadres blijft nu ongewijzigd wanneer u een bestelling plaatst met een verhandelbaar aanhalingsteken. Eerder, toen u een bestelling plaatste, werd het geselecteerde verzendadres veranderd in het standaardverzendadres.

- &#x200B;<!--ACP2E-1429--> In de montages van de Configuratie van de Opslag voor Functies B2B, wordt het **[!UICONTROL Enable Shared Catalog direct products price assigning]** gebied nu automatisch onbruikbaar gemaakt. In de winkel is deze verborgen wanneer de instelling **[!UICONTROL Enable Company]** of **[!UICONTROL Enable Shared Catalog]** is ingesteld op **[!UICONTROL No]** .

- &#x200B;<!--ACP2E-1683--> Wanneer Commerce een bedrijfsaccount maakt vanuit de winkel, valideert het nu het e-mailadres voordat de bedrijfsregistratie wordt verwerkt. Als het e-mailadres ongeldig is, mislukt de bewerking en worden geen accountupdates verwerkt. Eerder werd een klantenrekening gecreeerd zelfs als het verzoek om een bedrijfrekening tot stand te brengen wegens een ongeldig e-mailadres ontbrak.

- &#x200B;<!--ACP2E-1664--> SKU&#39;s van producten die dubbele aanhalingstekens in de Gedeelde Catalogus en de prijsstructuur omvatten veroorzaken niet meer fouten in Admin.

- &#x200B;<!--ACP2E-1498--> De Varnish-configuratie voor de Commerce-toepassing is bijgewerkt om te voorkomen dat gastgebruikers gegevens van andere klantgroepen kunnen zien.

#### Bekend probleem

Als u installeert of B2B 1.4.0 op [&#x200B; versie 2.4.6-p1 van Adobe Commerce &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) bevordert, komt de volgende fout voor:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

U kunt deze kwestie bevestigen door handgebiedsdelen voor het B2B veiligheidspakket met a [&#x200B; stabiliteitsmarkering &#x200B;](https://getcomposer.org/doc/04-schema.md#package-links) toe te voegen. Voor instructies, zie de [&#x200B; Kennisbank van Adobe Commerce &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

### B2B v1.3.5-p13

*14 oktober 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p13+ de versies van het veiligheidspatch.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-94 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-94.html) worden gedocumenteerd.

### B2B v1.3.5-p12

*Augustus 12, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p12+ de versies van het veiligheidspatch.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-71 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-71.html) worden gedocumenteerd.

### B2B v1.3.5-p10

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p10+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de Adobe Commerce 2.4.6-p10-beveiligingspatchreleases.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-26 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-26.html) worden gedocumenteerd.

### B2B v1.3.5-p9

*11 Februari, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p9+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de beveiligingspatchreleases van Adobe Commerce 2.4.6-p9.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-08 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-08.html) worden gedocumenteerd.

### B2B v1.3.5-p8

*8 Oktober, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p8+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de beveiligingspatchreleases van Adobe Commerce 2.4.6-p8.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB24-73 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

### B2B v1.3.5-p7

*9 augustus, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.6-p7+ de versies van het veiligheidspatch.

- Toegevoegde compatibiliteit met de beveiligingspatchreleases van Adobe Commerce 2.4.6-p7.

### B2B v1.3.5

*Maart 14, 2023*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 - 2.4.6 en nieuwere versies

- Release B2B versie 1.3.5-p2 ter ondersteuning van compatibiliteit met Adobe Commerce 2.4.6-p2.

- Release B2B versie 1.3.5-p1 ter ondersteuning van compatibiliteit met Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Nadat u Commerce van 2.4.6 aan de [&#x200B; recentste versie &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6) bevordert, zorg ervoor om aan de gesteunde B2B 1.3.5 flardversie bij te werken. Of upgrade de B2B-extensie van versie 1.3.5 naar versie 1.4.0 of hoger om de nieuwste functies te krijgen.

- Extra ondersteuning voor Adobe Commerce 2.4.6.

- &#x200B;<!--- ACP2E-689--> Adobe Commerce geeft nu de juiste gegevens weer tijdens de betaling wanneer de optie Aankooporders is ingeschakeld en er een virtueel prijsopgave is geselecteerd die met de PayPal-betalingsoptie is gemaakt. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

- &#x200B;<!--- ACP2E-609--> De lijst van klantengroepen voor **staat het doorbladeren Categorie** het plaatsen niet meer klantengroepen die met gedeelde catalogi verwant zijn.

- &#x200B;<!--- ACP2E-1244--> Het kenmerk voor de klant van het BTW-nummer werkt nu zoals u had verwacht met de bedrijfsbeheeraccounts op zowel de Beheerder als de winkel. Aangepaste BTW-kenmerken zijn niet meer vereist om een bedrijfsaccount te maken. Eerder, toen een handelaar een ondernemingsrekening met een douaneBelastings/BTW attribuut creeerde, gaf Adobe Commerce een bevestigingsfout op zowel de opslagplaats als Admin.

- &#x200B;<!--- ACP2E-1236--> Het uitschakelen van de functie voor gedeelde catalogus in een bepaald bereik werkt nu correct. Eerder stelde Adobe Commerce een ongeldig werkingsgebied in wanneer een handelaar gedeelde catalogusconfiguratie bewaarde.

- &#x200B;<!--- ACP2E-1203--> Admin-gebruikers kunnen nu aangepaste kenmerkwaarden van klanten voor bedrijfsgebruikers opslaan. Eerder konden de douanekenmerken van de klant voor bedrijfgebruikers niet worden bewaard.

- &#x200B;<!--- ACP2E-1221--> De problemen van prestaties worden opgelost met de bevestiging van bedrijftoestemmingen die door GraphQL worden verstrekt wanneer vele bedrijftoestemmingen reeds worden toegewezen.

- &#x200B;<!--- ACP2E-1242--> Adobe Commerce geeft niet langer een fout weer op de winkelwagentje wanneer met Snelle bestelling een product wordt toegevoegd in een hoeveelheid die groter is dan de voorraad.

- &#x200B;<!--- ACP2E-1090--> De prestaties van `SELECT` bedrijfstoestemmingsverrichtingen zijn verbeterd.

- &#x200B;<!--- ACP2E-2456--> De vragen van de categorie keren nu productprijzen volgens de montages van de opslagconfiguratie terug wanneer er geen categorietoestemmingen uitdrukkelijk geplaatst op de categorie die worden gevraagd zijn.

- &#x200B;<!--- ACP2E-6829--> De knop **[!UICONTROL Place Order]** werkt nu zoals u had verwacht bij het voltooien van een aankoop met een goedgekeurd aanhalingsverzoek. Problemen met de plug-in voor verhandelbare aanhalingstekens `negotiableQuoteCheckoutSessionPlugin` zijn opgelost.

### B2B v1.3.4-p16

*Maart 10, 2026*

[!BADGE &#x200B; Gesteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.5-p16 (uitgebreide steun)

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB26-05 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb26-05.html) worden gedocumenteerd.

### B2B v1.3.4-p15

*14 oktober 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-94 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-94.html) worden gedocumenteerd.

### B2B v1.3.4-p14

*Augustus 12, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-71 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-71.html) worden gedocumenteerd.

### B2B v1.3.4-p13

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.5-p12.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-50 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

### B2B v1.3.4-p12

*8 April, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.5-p12.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-26 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-26.html) worden gedocumenteerd.

### B2B v1.3.4-p11

*11 Februari, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.5-p11.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-08 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-08.html) worden gedocumenteerd.

### B2B v1.3.4-p10

*9 Oktober, 2024*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.5-p10.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB24-73 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb24-73.html) worden gedocumenteerd.

### B2B v1.3.4

*9 augustus, 2022*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.5.

- &#x200B;<!--- ACP2E-453-->Adobe Commerce verzendt geen e-mailberichten meer telkens als een bestaand Bedrijf door een API vraag wordt bijgewerkt. E-mails worden nu alleen verzonden wanneer een bedrijf wordt gemaakt.

- &#x200B;<!--- ACP2E-406-->Adobe Commerce berekent nu correct het totaal van een verhandelbaar aanhalingsteken wanneer de instelling voor **[!UICONTROL Enable Cross Border Trade]** belastingberekening is ingeschakeld.

- &#x200B;<!--- ACP2E-322-->Configureerbare producten worden nu naar de laatste positie in de productlijst verplaatst nadat de voorraad is bijgewerkt wanneer de instelling **[!UICONTROL Move out of stock to the bottom]** is ingeschakeld. Er wordt een nieuwe aangepaste databasequery geïmplementeerd om ervoor te zorgen dat de sorteervolgorde voor de Elasticsearch-index nu overeenkomt met de sorteervolgorde voor beheerders. Eerder, werden de configureerbare producten en hun kindproducten niet verplaatst naar de bodem van de lijst toen dit het plaatsen werd toegelaten.

- &#x200B;<!--- ACP2E-308-->E-mail met inkooporder respecteert nu de instelling voor het verzenden van e-mail van elke website in een implementatie met meerdere sites. Een controle op de instelling **[!UICONTROL Disable Email Communications]** wordt toegevoegd aan de aangepaste logica voor e-mailwachtrijen. Eerder heeft Adobe Commerce de instelling voor het verzenden van e-mail voor de secundaire website niet gerespecteerd.

- &#x200B;<!--- ACP2E-302-->De titel van het SKU-veld van de pagina Snelle volgorde wordt voor de duidelijkheid gewijzigd.

- &#x200B;<!--- ACP2E-543-->Adobe Commerce toont nu een informatievere foutenmelding wanneer een verkoopster een ongeldige SKU op het **ingaat SKU of gebied van de Naam van het Product**.

- &#x200B;<!--- ACP2E-1753-->Het veld **[!UICONTROL Account Created in]** voor een bedrijfsbeheerder behoudt nu zijn waarde zoals u had verwacht nadat u het bedrijf hebt opgeslagen.

- &#x200B;<!--- ACP2E-722 -->De query `customer` retourneert niet langer lege resultaten wanneer deze de aanvraaglijsten ophaalt die door `uid` zijn gefilterd.

- &#x200B;<!--- ACP2E-210 -->Er is een insteekmodule toegevoegd vóór de aanroep van `collectQuoteTotals` om ervoor te zorgen dat de opslagcredits slechts eenmaal worden toegepast.

- &#x200B;<!--- ACP2E-665 -->Klanten worden nu omgeleid naar de aanmeldingspagina wanneer hun account door een beheerder van de beheerder wordt verwijderd. Eerder gaf Adobe Commerce een fout. Het codeblok van de plug-in (`SessionPlugin` ) bevindt zich nu in het `try…catch` -blok. Eerder, werd deze code niet verpakt binnen het generische uitzondering-behandelende blok.

- &#x200B;<!--- ACP2E-661 --> Op de Snelle pagina van de Orde op mobiele wijze, die **drukken gaat** binnen na het ingaan van een geldige productnaam of SKU neemt nu de verkoopster aan het volgende gebied zoals verwacht.

- &#x200B;<!--- ACP2E-607 -->De naam van het bedrijf is nu zichtbaar zoals u had verwacht in de gedeelten facturering en verzendadres van de afrekenworkflow.

- &#x200B;<!--- ACP2E-375 -->Winkelkrediet is nu niet beschikbaar wanneer de betalingsmethode **[!UICONTROL Zero Subtotal Checkout]** is uitgeschakeld. Eerder was het selectievakje Winkelkrediet niet functioneel tijdens de plaatsing van de bestelling bij de beheerder. De toepassing heeft de bestelling niet bij het winkelkrediet geplaatst en deze fout weergegeven: `The requested Payment Method is not available`.

### B2B v1.3.3-p17

*Maart 10, 2026*

[!BADGE &#x200B; Gesteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.4-p17 (uitgebreide steun)

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB26-05 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb26-05.html) worden gedocumenteerd.

### B2B v1.3.3-p16

*14 oktober 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-94 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-94.html) worden gedocumenteerd.

### B2B v1.3.3-p15

*Augustus 12, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-71 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-71.html) worden gedocumenteerd.

### B2B v1.3.3-p14

*10 Juni, 2025*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.5-p12.

- Omvat de veiligheidsmoeilijke situaties die in [&#x200B; Bulletin APSB25-50 van de Veiligheid &#x200B;](https://helpx.adobe.com/security/products/magento/apsb25-50.html) worden gedocumenteerd.

### B2B v1.3.3

*9 augustus, 2022*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.4.

- &#x200B;<!--- MC-41985--> De tijd die nodig was om van Adobe Commerce 2.3.x aan Adobe Commerce 2.4.x in plaatsingen met meer dan 100.000 bedrijfrollen te bevorderen is aanzienlijk verminderd.

- &#x200B;<!--- MC-42153--> De POST `V1/order/:orderId/invoice` -aanvraag ondersteunt nu het maken van gedeeltelijke facturen wanneer de **[!UICONTROL Payment on Account]** -betalingsmethode is ingeschakeld. Eerder heeft Adobe Commerce deze fout gegenereerd: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity` . [&#x200B; GitHub-32428 &#x200B;](https://github.com/magento/magento2/issues/32428)

- &#x200B;<!--- MC-41975--> PayPal Payflow Pro werkt nu zoals u had verwacht met B2B verhandelbare aanhalingstekens wanneer het winkelwagentje van de klant andere producten bevat. Adobe Commerce verwerkt de bestelling nu met succes en stuurt een e-mail naar de klant zoals u had verwacht. Eerder gaf Adobe Commerce een fatale fout en stuurde een bevestigingsbericht naar de klant met daarin de nulwaarden.

- &#x200B;<!--- MC-41819--> Paginering wordt nu correct weergegeven op de pagina met zoekresultaten in een catalogus nadat sommige producten in een gedeelde catalogus zijn uitgesloten.

- &#x200B;<!--- MC-42886--> Aangepaste kenmerken van de klant worden nu op de verwachte manier opgeslagen wanneer u een bedrijfsgebruiker maakt of opslaat in de beheerdersbeheerder.

- &#x200B;<!--- MC-42927--> De knop **[!UICONTROL Submit]** in het formulier Nieuw bedrijf maken is nu uitgeschakeld nadat u met één muisklik hebt geklikt om te voorkomen dat meerdere formulieren worden verzonden. Eerder kon u dit formulier meerdere keren verzenden door herhaaldelijk op deze knop te klikken. Er is een fout opgetreden.

- &#x200B;<!--- MC-42787--> Adobe Commerce geeft de koppeling voor opnieuw ordenen niet meer weer in de winkel wanneer een winkelier zich aanmeldt bij een winkel waarvoor opnieuw bestellingen zijn uitgeschakeld.

- &#x200B;<!--- MC-43115--> Het zoeken in de snelle orde door SKU is nu case-insensitive wanneer de gedeelde catalogus wordt toegelaten.

- &#x200B;<!--- MC-42203--> U kunt een dossier voor een klantenattribuut nu bijwerken wanneer het creëren van een bedrijf. Eerder, toen u probeerde om een bedrijf met een gehechtheid van type `File` tot stand te brengen, creeerde Adobe Commerce niet het bedrijf en registreerde deze fout in het uitzonderingslogboek: `Something went wrong while saving file`.

- &#x200B;<!--- MC-42242--> U kunt een bedrijf met een klantenrekening nu tot stand brengen die een douanekenmerk met a (`File`) of (`Image`) type heeft. Eerder, als de rekening één van deze klantgerichte opties had, gaf het Bedrijf uit paginalader uitgeeft niet op, die het uitgeven van bedrijfdetails verhinderden.

- &#x200B;<!--- MC-42268--> De query `products` retourneert nu een accuraat `total_count` -veld wanneer de gedeelde catalogus is ingeschakeld.

- &#x200B;<!--- MC-42203-->  U kunt een dossier voor een klantenattribuut nu bijwerken wanneer het creëren van een bedrijf. Eerder, toen u probeerde om een bedrijf met een gehechtheid van type `File` tot stand te brengen, creeerde Adobe Commerce niet het bedrijf en registreerde deze fout in het uitzonderingslogboek: `Something went wrong while saving file`.

- &#x200B;<!--- MC-43178--> De _Configuratie van het Bedrijf_ en _creëren de pagina&#39;s van het Bedrijf_ nu werken zoals verwacht nadat u online het verschepen methode onbruikbaar maakt. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected` .

- &#x200B;<!--- MC-42214--> De _pagina van de Categorie_ toont nu verenigbare productgegevens terwijl de toestemmingen tijdens het gedeeltelijke indexeren worden geproduceerd. Er is een nieuwe gedeeltelijke indexator voor directorymachtigingen toegevoegd aan dit proces. Eerder waren de gegevens die werden weergegeven terwijl de indexeerfunctie werd uitgevoerd onjuist.

- &#x200B;<!--- MC-42567--> De query `categoryList` retourneert nu het juiste aantal producten wanneer catalogusmachtigingen worden gebruikt en producten worden toegewezen aan een gedeelde catalogus.

- &#x200B;<!--- MC-42528--> De query van `categoryList` respecteert nu categorierechten en retourneert alleen toegestane categorieën. Eerder, keerde het alle toegewezen en niet toegewezen categorieën terug.

- &#x200B;<!--- MC-42399--> De aanvraag `rest/V1/company/{id}` retourneert nu de `is_purchase_order_enabled` -kenmerkwaarden zoals verwacht.

- &#x200B;<!--- ACP2E-128--> De klantenattributen van de douane worden nu getoond zoals verwacht in _Admin van het Bedrijf_ tabel.

- &#x200B;<!--- ACP2E-130--> Het Mijn blok van de Lijst van de Wens op de Mijn pagina van de Rekening wordt nu getoond zoals verwacht voor de Admins van het Bedrijf en de Gebruikers van het Bedrijf.

- &#x200B;<!--- ACP2E-133--> Fouten in de Snelle volgorde worden niet meer weergegeven in het winkelwagentje. Eerder, toonde Adobe Commerce deze fout in het winkelwagentje toen SKU niet in de catalogus werd gevonden: `The SKU was not found in the catalog`.

- &#x200B;<!--- ACP2E-194--> Opslagbewerkingen voor gedeelde catalogus zijn geoptimaliseerd om sneller te kunnen worden uitgevoerd. Het opslaan van een gedeelde catalogus met veel klantengroepen kan eerder enkele minuten in beslag nemen.

- &#x200B;<!--- MC-42240--> Adobe Commerce verwijdert nu alle machtigingen voor subcategorieën uit de tabel `sharedcatalog_category_permissions` wanneer de bovenliggende categorie wordt verwijderd. Eerder werden alleen de gegevens van de bovenliggende categorie verwijderd.

### B2B v1.3.2

*Augustus 29, 2022*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.3.

- &#x200B;<!--- MC-39862--> Adobe Commerce verzendt nu bijgewerkte e-mailberichten over verlopen verhandelbare aanhalingstekens. Eerder, toen een verhandelbaar prijsopgave verstreek, heeft Adobe Commerce geen e-mails verzonden voor updates.

- &#x200B;<!--- MC-40682--> Adobe Commerce verzendt nu bijgewerkte e-mailberichten over binnenkort te verlopen en verlopen onderhandelbare aanhalingstekens wanneer een `cron` -taak ontbreekt.

#### Bedrijf

- &#x200B;<!--- MC-41542--> In het vervolgkeuzeveld voor het land van de pagina Nieuwe bedrijfsaccount maken worden geen lege optiewaarden meer weergegeven. Eerder waren de eerste twee opties en de landcode `AN` leeg.

- &#x200B;<!--- MC-41260--> Als u op de knop **[!UICONTROL Return]** klikt voor een order die door een bedrijfsgebruiker is gemaakt, wordt een gebruiker met beheerdersrechten nu omgeleid naar de pagina Teruggave maken, zoals verwacht. Eerder werd de beheerder omgeleid naar de pagina Order History.

- [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} <!--- MC-40798--> Adobe Commerce ontbreekt niet meer met een uit-van-geheugenfout wanneer het uitvoeren van de `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` methode tijdens `bin/magento setup:upgrade`. Eerder, gebruikte Adobe Commerce niet partijgrootte voor inzameling toen het initialiseren van toestemmingen, maar in plaats daarvan geladen een inzameling van alle bedrijfrollen.

- &#x200B;<!--- MC-40551--> De gebruikers van het bedrijf kunnen klanten de waarden van de douaneattributen nu uitgeven en bijwerken. Eerder waren deze kenmerken niet correct gekoppeld aan het formulier voor het maken en bewerken van gebruikers. Een bedrijfgebruiker kon verschillende kenmerkwaarden ingaan, maar Adobe Commerce heeft deze waarden niet correct bewaard.

- &#x200B;<!--- MC-32653--> De middelboom voor de toestemmingen van de bedrijfrol kan nu worden vertaald zoals verwacht. Eerder was de machtigingenstructuur niet vertaald, ook al waren er geldige vertaalbestanden aanwezig.

- &#x200B;<!--- MC-40358--> Adobe Commerce slaat nu de aangepaste kenmerkwaarden van de klant voor B2B-gebruikers op zoals verwacht. Eerder leidde het maken van een bedrijfsaccount dat aangepaste klantkenmerken bevatte tot een sjabloonfout en kon Adobe Commerce het formulier niet laden. Door een argument toe te voegen aan de lay-out van `company_create_account` is dit probleem opgelost.

- &#x200B;<!--- MC-41721--> De gebruikersfilters van het bedrijf zoals tonen Alle Gebruikers, tonen Actieve Gebruikers, en tonen Inactieve Gebruikers werken nu zoals verwacht. Eerder, veroorzaakte het filtreren acties op de pagina van de bedrijfgebruiker een fout van JavaScript.

#### Bedrijfskrediet

- &#x200B;<!--- MC-41551--> Beheerders met beperkte accounts die alleen bevoegdheden op websiteniveau bevatten, kunnen nu een bedrijf maken dat een andere valuta gebruikt dan de website.

- &#x200B;<!--- MC-41523--> Adobe Commerce stuurt nu e-mailberichten van het juiste e-mailadres en bereik van `from` . Eerder heeft Adobe Commerce geen rekening gehouden met het bereik van de website bij het verzenden van een bedrijfskrediet of het bijwerken van een e-mail.


#### Snelle bestelling

- &#x200B;<!--- MC-42104--> Het maken van een volgorde met Snelle volgorde vanuit een CSV-bestand werkt nu zoals u verwacht met niet-bestaande SKU&#39;s.

- &#x200B;<!--- MC-40268--> Het gebruiken van Snelle Orde aan onderzoek op veelvoudige SKUs werkt nu zoals verwacht. Eerder waren er dubbele vermeldingen in de resultaten opgenomen.

- &#x200B;<!--- MC-40261--> In de weergave van de lijst Toegevoegde producten worden SKU&#39;s die in kleine letters en in hoofdletters zijn ingevoerd, nu op dezelfde manier behandeld als wanneer u SKU&#39;s gebruikt om meerdere producten te selecteren tijdens de Snelle volgorde.

- &#x200B;<!--- MC-40225--> Met Snelle volgorde voegt u nu producten toe in het aantal dat door de winkelier is opgegeven. Eerder heeft Adobe Commerce slechts één product toegevoegd, zelfs als de door de winkel opgegeven hoeveelheden groter zijn dan één product.

- &#x200B;<!--- MC-41283--> De functie Volgorde automatisch aanvullen werkt nu met gedeeltelijke SKU&#39;s.

- &#x200B;<!--- MC-41299--> Adobe Commerce toont nu producten die als **niet zichtbaar individueel** op de Snelle pagina van de Orde auto-stelt lijst en onderzoeksresultaten zijn gevormd voor.

- &#x200B;<!--- MC-42402--> Klanten kunnen nu het formulier Snelle volgorde gebruiken om meerdere producten toe te voegen door SKU&#39;s die hoofdletters bevatten. Eerder werd alleen het eerste product toegevoegd.

#### Verhandelbaar aanhalingsteken

- &#x200B;<!--- MC-41232--> De kopers worden nu omgeleid naar de onderhandelbare aanhalingspagina nadat ze de koppeling naar een onderhandelbaar aanhalingsteken in het URL-veld hebben geplakt en zich met succes hebben aangemeld. Eerder werd de koper doorgestuurd naar de pagina Mijn account.

- &#x200B;<!--- MC-39317--> Het opnieuw ordenen werkt nu zoals verwacht voor orders die een product met een Aanpasbare Optie Datum voor een klantenrekening bevatten die tijdens het afrekenen werd gecreeerd. Eerder heeft Adobe Commerce de reorder niet verwerkt en deze fout weergegeven: `The product has required options. Enter the options and try again` .

- &#x200B;<!--- MC-39063--> Het verzendadres voor een verhandelbaar aanhalingsteken kan niet meer worden bewerkt tijdens het afrekenen wanneer de module Inkooporder is uitgeschakeld. Dit gedrag is het gevolg van een vorige correctie waarbij `isQuoteAddressLocked` is verwijderd uit de verhandelbare renderer voor het uitchecken van aanhalingstekens.

- &#x200B;<!--- MC-38967--> Handelaren kunnen nu producten toevoegen aan een verhandelbaar prijsopgave van de beheerder.

#### Aankooporders

- &#x200B;<!--- MC-39983--> Adobe Commerce geeft nu een informatief foutbericht weer zoals u had verwacht wanneer u een inkooporder plaatst met PayPal Express Checkout wanneer het kenmerk **[!UICONTROL Name Prefix]** is ingesteld op `required` . Eerder heeft Adobe Commerce de bestelling niet geplaatst of een foutbericht weergegeven.

- &#x200B;<!--- MC-39620--> De UI-component voor het factuuradres in de module Inkooporder gebruikt nu het citaatadres correct wanneer Google Tag Manager is ingeschakeld. Er is eerder een JavaScript-fout opgetreden op de betalingspagina.

#### Aanvraaglijsten

- &#x200B;<!--- MC-40426--> Merchants kunnen nu het POST `rest/all/V1/requisition_lists` -eindpunt gebruiken om een aanvraaglijst voor een klant te maken. Eerder heeft Adobe Commerce deze fout van 400 gegenereerd toen u een aanvraaglijst probeerde te maken: `Could not save Requisition List` .

- &#x200B;<!--- MC-41123--> De knop **[!UICONTROL Add to Requisition List]** wordt nu weergegeven voor producten in voorraad van een winkelwagentje wanneer het winkelwagentje ook producten uit de voorraad bevat. Als een winkelwagentje twee producten bevatte, waarvan er één uit voorraad was, werd de knop _[!UICONTROL Add to Requisition List]_&#x200B;eerder voor geen van beide producten weergegeven.

- &#x200B;<!--- MC-40877--> U kunt nu de REST API gebruiken om een product aan een aanvraaglijst toe te voegen.

- &#x200B;<!--- MC-40155--> De waarden in de aanvraaglijst **[!UICONTROL Latest Activity Date]** hebben nu de notatie voor de landinstelling.

- &#x200B;<!--- MC-39580--> Adobe Commerce genereert niet langer een fatale fout wanneer u een bundelproduct bewerkt vanuit een aanvraaglijst.

- &#x200B;<!--- MC-40454--> Adobe Commerce geeft nu de juiste productprijs weer wanneer u een product met een aanpasbare optie `(File)` toevoegt aan een verlanglijst in een aanvraaglijst. De koppeling naar het geüploade bestand is ook zichtbaar zoals u had verwacht. Eerder gaf Adobe Commerce onjuiste productprijzen weer en werd de koppeling naar het bestand niet weergegeven.

- &#x200B;<!--- MC-36383--> Producten met een aanpasbare optie `(File)` kunnen nu vanuit een aanvraaglijst aan een winkelwagentje worden toegevoegd.


#### Gedeelde catalogus

- &#x200B;<!--- MC-40497--> Een beheerder met een rol die beperkt is tot een specifieke website, kan nu een gedeelde catalogus maken, weergeven en bewerken. Eerder gaf Adobe Commerce een fatale fout op toen een beheerder met een beperkte rol probeerde een gedeelde catalogus te creëren.

- &#x200B;<!--- MC-41337--> Gelaagde navigatieresultaten bevatten nu een nauwkeurige telling van producten met gefilterde kenmerken en kopers kunnen nu meerdere filters toepassen. Eerder kon slechts één filter worden toegepast en gaf Adobe Commerce een onnauwkeurig aantal producten weer in gelaagde navigatie.

- &#x200B;<!--- MC-40779--> Adobe Commerce geeft nu correct het aantal producten weer in gelaagde navigatiefilters in zoekresultaten. Eerder gebruikte een insteekmodule voor de pagina met zoekresultaten geen Elasticsearch, maar werd een nieuwe query naar de database verzonden.

- &#x200B;<!--- MC-39978--> Adobe Commerce verwijdert de prijzen niet meer uit de lijst wanneer een handelaar alle producten uit een standaard gedeelde catalogus verwijdert.

- &#x200B;<!--- MC-39802--> Filters worden nu gefilterd op de huidige categorie en correct weergegeven op alle pagina&#39;s wanneer gedeelde catalogi zijn ingeschakeld. Eerder werden filters alleen voor de huidige pagina verkeerd berekend en niet door de huidige categorie gefilterd.

- &#x200B;<!--- MC-39522--> De GraphQL `products` -query retourneert niet langer het prijsbereik en de categorie van een product voor producten die niet aan een gedeelde catalogus zijn toegewezen wanneer de gedeelde catalogus is ingeschakeld. Eerder gaf de query de aggregaties van het product, ook al werd het product zelf niet geretourneerd in de `items` -array.

### B2B v1.3.1

*9 Februari, 2021*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.2.

- Online betalingsmethoden worden nu ondersteund voor inkooporders.

- Als u een configureerbaar product rechtstreeks vanuit een aanvraaglijst aan het winkelwagentje toevoegt terwijl dit product in een eerdere bestelling werd gebruikt, wordt niet langer een systeemfout geretourneerd.

- Adobe Commerce geeft nu het tabblad Vereist mijn goedkeuring correct weer voor inkooporders wanneer een gesplitste databaseconfiguratie wordt geïmplementeerd.

- Adobe Commerce geeft nu details weer over bundelproducten en cadeaukaart wanneer u inkooporders bekijkt.

- Winkels waarin **[!UICONTROL Website Restriction]** is ingeschakeld en **[!UICONTROL Restriction Mode]** is ingesteld op `Private Sales: Login Only` , worden nu omgeleid naar de verwachte status na het aanmelden bij hun account. Eerder werden kopers omgeleid naar de homepage van de winkel. <!--- MC-38934-->

- De geschiedenis van de orde laadt nu zoals verwacht in een de rekeningsdashboardpagina van een bedrijfbeheerder in plaatsingen met een B2B bedrijfshiërarchie die vele klanten (groter dan 13000) bevat. Eerder werd de volgorde van de historie traag of helemaal niet geladen en gaf Adobe Commerce een fout van 503 weer. <!--- MC-38830-->

- Adobe Commerce geeft niet langer meerdere identieke waarschuwingsberichten weer wanneer u een niet-geconfigureerd product met aanpasbare opties toevoegt aan een lijst met aanvragen van een categoriepagina. <!--- MC-38342-->

- Nieuwe en gedupliceerde producten zijn nu zichtbaar zoals op de categoriepagina wordt verwacht wanneer gedeelde B2B-catalogi zijn ingeschakeld. <!--- MC-38307-->

- Adobe Commerce handhaaft nu correct `store_id` dat met een bedrijfbeheerder wordt geassocieerd wanneer de klantengroep voor een bedrijf wordt bijgewerkt. Eerder is de waarde van `store_id` gewijzigd in de standaardwinkel toen de groep werd bijgewerkt. <!--- MC-38196-->

- Adobe Commerce slaat nu een gegroepeerd product op een aanvraaglijst op als een lijst met eenvoudige producten, net zoals het een gegroepeerd product aan een winkelwagentje toevoegt. Als gevolg van de manier waarop Adobe Commerce gegroepeerde producten heeft opgeslagen, werd de koppeling voor een gegroepeerd product in de aanvraaglijst altijd doorgestuurd naar eenvoudige producten en niet naar het gegroepeerde product. <!--- MC-38049-->

- U kunt nu orders filteren op het veld **[!UICONTROL Company Name]** wanneer u ordergegevens exporteert in de CSV-indeling. Eerder heeft Adobe Commerce een fout aangemeld in `var/export/{file-id}` . <!--- MC-37785-->

- Adobe Commerce geeft nu de pop-up Aanvraaglijst maken weer zoals u had verwacht wanneer u het tabblad Nieuwe lijst met aanvragen maken in de winkel selecteert. <!--- MC-37915-->

- In de lijst met aanvragen worden nu alle gegroepeerde producten en hoeveelheden opgenomen die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, gaf Adobe Commerce deze fout weer: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

- De juiste archiefweergave is nu gekoppeld aan de relevante website wanneer u een bedrijf maakt in een implementatie op meerdere sites. Eerder kon u geen bedrijf maken en Adobe Commerce gaf deze fout weer: `The store view is not in the associated website` . <!--- MC-37488-->

- Het bestellen van producten door SKU met behulp van Snelle bestelling leidt niet langer tot dubbele producthoeveelheden in het CSV-bestand. <!--- MC-37427-->

- De knop **[!UICONTROL Add to Cart]** wordt niet meer geblokkeerd wanneer de sectie _[!UICONTROL Enter Multiple SKUs]_&#x200B;van de pagina Snelle volgorde een lege waarde bevat. In plaats daarvan geeft Adobe Commerce nu een bericht weer waarin u wordt gevraagd geldige SKU&#39;s in te voeren. <!--- MC-37387-->

- Adobe Commerce geeft dit bericht nu weer op de productpagina wanneer u een productoverzicht vanuit een aanvraaglijst verzendt: `You submitted your review for moderation` . De revisie wordt ook weergegeven op de pagina Revisies in behandeling (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]** ). Hoewel Adobe Commerce de revisie eerder heeft toegevoegd aan de lijst van lopende recensies, heeft het een fout van 404 op de productpagina geplaatst. <!--- MC-37119-->

- De prestaties van de `sharedCatalogUpdateCategoryPermissions` -consument zijn verbeterd. Na het creëren van een gedeelde catalogus, gebruikt de indexator van de catalogustoestemming nu slechts identiteitskaart van de klantengroep van de gedeelde catalogus, niet alle klantengroepen. <!--- MC-36770-->

- De gebieden van het de adresattribuut van de klant van de douane die met het niet-standaardadres van een verkoopster worden geassocieerd worden nu bewaard zoals verwacht in de storefront controlewerkschema. <!--- MC-36630-->

- De orden voor producten die tot de standaard gedeelde catalogus van een opslag behoren kunnen nu voor kopers door Admin REST API (`rest/V1/carts/{<CART_ID>/items`) worden geplaatst zoals verwacht. Adobe Commerce controleert nu of het product aan een openbare catalogus is toegewezen voordat de validatie van gedeelde catalogusmachtigingen in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave` wordt uitgevoerd. Eerder heeft Adobe Commerce het product niet aan de winkelwagentje toegevoegd en deze fout gegenereerd: `No such shared catalog entity` . <!--- MC-36535-->

- Adobe Commerce stuurt nu e-mails met gebruikersregistratie voor nieuwe bedrijven via het adres van de Adobe Commerce-winkel. Eerder werd deze e-mail verzonden van het adres van de bedrijfbeheerder. <!--- MC-36480-->

- Adobe Commerce controleert nu aangepaste kenmerken op duplicatie van gereserveerde namen van bedrijfskenmerken voordat een handelaar een nieuw kenmerk kan opslaan. <!--- MC-36282-->

- De query `credit_history` retourneert nu de creditgeschiedenis van het opgegeven bedrijf voor zowel het oorspronkelijk toegewezen bedrag als het gekochte bedrag. Eerder heeft deze query een fout geretourneerd.

- De velden **[!UICONTROL Company]** en **[!UICONTROL Job Title]** op de pagina Accountinformatie bewerken kunnen niet meer worden bewerkt.

#### Bekende problemen

- B2B-kopers kunnen online betalingsmethoden gebruiken om de gebruikelijke inkooporderstroom te omzeilen. Dit scenario kan zich voordoen als de koper zijn volledige afhandelingstotaal tot 0 kan terugbrengen — bijvoorbeeld door een promotiecode of een cadeaukaart — en vervolgens de code of geschenkkaart kan verwijderen. Zelfs onder deze omstandigheden plaatst Adobe Commerce nog steeds de order voor het juiste bedrag op basis van de prijzen van de items in de toegewezen catalogus. **_Oplossing_**: maak geschenkkaarten en couponcodes onbruikbaar wanneer de online betalingsmethodes voor de goedkeuring van de inkooporde worden toegelaten. <!--- B2B-1603-->

- Kopers worden omgeleid naar het winkelwagentje wanneer ze een bestelling proberen te plaatsen via een inkooporder met PayPal Express Checkout wanneer **[!UICONTROL In-Context Mode]** is uitgeschakeld. <!--- B2B-1604-->

- Adobe Commerce geeft soms een fout van 404 weer wanneer een koper een inkooporder maakt en vervolgens naar de afhandelingspagina navigeert. Deze fout treedt op wanneer een koper eerder een andere inkooporder met een online betalingsmethode heeft gemaakt voordat hij naar de betalingspagina navigeert zonder de vorige aankoop te voltooien. De koper kan de kooporder nog steeds plaatsen. **_Oplossing_**: niets. <!--- B2B-1605-->

- Kortingen voor een specifieke betalingsmethode blijven bestaan tijdens afhandeling voor een inkooporder, zelfs als de koper zijn betalingsmethode wijzigt tijdens de laatste afhandeling. Als gevolg hiervan kunnen klanten een korting ontvangen waarop ze geen recht hebben. Deze kwestie doet zich voor omdat ondanks de wijziging in de betalingsmethode nog steeds een kartregel voor de oorspronkelijke betalingsmethode wordt toegepast. **_Oplossing_**: niets. Zie [&#x200B; Adobe Commerce 2.4.2 B2B bekende kwestie: de korting blijft voor online Orden van de Aankoop nadat de betalingsmethode &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _artikel van de Kennisbank_ wordt veranderd. <!-- B2B-1012 -->

- De query `deleteRequisitionListOutput` retourneert details over de verwijderde aanvraaglijst in plaats van de resterende aanvraaglijsten. <!--- MC-39894-->

### B2B v1.3.0

*15 oktober 2020*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

Deze release bevat verbeteringen voor goedkeuringen voor bestellingen, verzendmethoden, winkelwagentje en registratie van beheeracties.

- Extra ondersteuning voor Adobe Commerce 2.4.1.

- B2B-ordergoedkeuringen zijn verbeterd om de bruikbaarheid te verbeteren en om acties in bulk voor inkooporders mogelijk te maken.

- B2B de handelaren kunnen verzendmethodes nu controleren die aan elk Bedrijf worden aangeboden.<!--- BUNDLE-160 161 162 -->

- Handelaars kunnen gebruikers nu toestaan de inhoud van hun winkelwagentje in één handeling te wissen en kunnen deze mogelijkheid onafhankelijk van elkaar configureren op elke website. <!--- BUNDLE-108 -->

- B2B-kopers kunnen nu afzonderlijke objecten of de volledige inhoud van hun winkelwagentje rechtstreeks aan een aanvraaglijst toevoegen. <!--- BUNDLE-145 144-->

- B2B-handelaren kunnen namens klanten via Betaling op rekening als betalingsmethode orders van de beheerder maken. <!--- BUNDLE-166 178-->

- Handelaars kunnen nu rechtstreeks alle aanhalingstekens die aan een gebruiker zijn gekoppeld, weergeven op de detailpagina van de klant. <!--- BUNDLE-139 -->

- Merchants kunnen nu het Online net van Klanten nu door Bedrijf filtreren. <!--- BUNDLE-137 -->

- Beheerders kunnen klanten in Admin nu filteren op Verkoopvertegenwoordiger. <!--- BUNDLE-110 -->

- Om het creëren van frauduleuze of spamrekeningen te verminderen, kunnen de handelaars nu Google reCAPTCHA op het Nieuwe formulier van het Verzoek van het Bedrijf op de winkel toelaten. <!--- BUNDLE-154 -->

- De acties Admin die in de modules van het Bedrijf worden genomen worden nu het programma geopend het Logboek van Acties Admin. Handelingen worden vanuit alle relevante bedrijfsmodules geregistreerd: `Company` , `NegotiableQuote` , `CompanyCredit` , `SharedCatalog` . <!--- BUNDLE-180 181 182 183 -->

- Adobe Commerce toont niet meer de **[!UICONTROL Delete customer]** knoop op de **Klanten** pagina wanneer de het programma geopende beheerder geen rechten heeft om klanten in plaatsingen te schrappen waar B2B geïnstalleerd is. <!--- MC-35655-->

- De groep van de klant wordt niet meer automatisch veranderd voor een klant die aan een Bedrijf wordt toegewezen wanneer u de klant op het net van de Klant uitgeeft. <!--- MC-35254-->

- Wanneer een handelaar een gedeelde catalogus maakt, worden nu automatisch machtigingen ingesteld op `Allow` voor de functies **[!UICONTROL Display Product Prices]** en **[!UICONTROL Add to Cart]** in categorieën wanneer aan de klantengroep deze toegang wordt toegewezen in de machtigingsinstellingen voor de catalogus. Eerder, werden deze montages automatisch geplaatst aan `Deny` zelfs toen catalogustoestemmingen aan `Allow` werden geplaatst.<!--- MC-34792-->

- De gedeelde cataloguscategorietoestemmingen worden niet meer beschreven wanneer een product van de product uitgeeft pagina wordt uitgegeven.<!--- MC-34777-->

- Adobe Commerce verzendt nu een e-mailbericht waarin wordt bevestigd dat een klant toestemming heeft om de toegewezen kredietlimiet te overschrijden wanneer een handelaar de instelling **[!UICONTROL Allow To Exceed Credit Limit]** inschakelt. Eerder gaf het e-mailbericht van Adobe Commerce aan dat de klant geen toestemming had om de limiet te overschrijden. <!--- MC-34584-->

- De HTML-container die de productprijs op aanvraaglijsten omsluit, wordt nu correct weergegeven voor de kinderen van gebundelde producten. <!--- MC-36331-->

- Handelaars kunnen nu de taal aanwijzen waarin de e-mail van de bedrijfgebruiker wordt verzonden wanneer het creëren van een bedrijf in meertalige plaatsingen. Eerder werd het vervolgkeuzemenu waarin handelaren de juiste winkelweergave en taal kunnen selecteren, niet weergegeven.  <!--- MC-35777-->

- De gebieden van de attributen van het klantenadres van de douane worden nu getoond zoals verwacht in de storefront controlewerkschema. <!--- MC-35607-->

- Het tabblad Configuratie B2B-functies wordt nu correct geopend. <!--- MC-35458-->

- Gasten kunnen nu QuickOrder gebruiken om producten aan hun winkelwagentje toe te voegen en vervolgens items te verwijderen. Eerder, toen een verkoopster QuickOrder gebruikte om veelvoudige producten aan hun kar toe te voegen, en dan een product te verwijderen, werd het product niet verwijderd. <!--- MC-35327-->

- Een bedrijf kan nu worden bijgewerkt gebruikend het REST API PUT `/V1/company/:companyId` verzoek zonder `region_id` te specificeren wanneer de staat als **wordt gevormd niet vereist**. Hoewel `region_id` voorheen niet vereist was, gaf Adobe Commerce een fout als deze niet was opgegeven. <!--- MC-35304-->

- Wanneer u een B2B-bedrijf maakt of bijwerkt met de REST API (`http://magento.local/rest/V1/company/2` , waarbij `2` de bedrijfs-id vertegenwoordigt), bevat de reactie nu de instellingen voor `applicable_payment_method` of `available_payment_methods` zoals verwacht. <!--- MC-35248-->

- Adobe Commerce toont niet meer een 404 pagina wanneer een handelaar **binnengaan** knoop in plaats van het klikken van de **[!UICONTROL Save]** knoop wanneer het creëren van een verzoeklijst op de storefront.<!--- MC-35094-->

- Categoriemachtigingen worden niet meer gewijzigd wanneer een nieuw product wordt toegewezen aan een openbare gedeelde catalogus. Eerder werden categorietoestemmingen gedupliceerd. <!--- MC-34386-->

- Het eindpunt van REST API PUT `rest/default/V1/company/{id}`, dat wordt gebruikt om bedrijfs-e-mail bij te werken, is niet meer hoofdlettergevoelig. <!--- MC-34308-->

- Het onbruikbaar maken van beloningsmodules beïnvloedt niet meer B2B eigenschappen op klantenrekeningen. Eerder, toen de beloningsmodules onbruikbaar werden gemaakt, werden de volgende B2B-Verwante lusjes niet getoond: Het Profiel van het Bedrijf, de Gebruikers van het Bedrijf, en Rollen en Toestemmingen.<!--- MC-34191-->

- Adobe Commerce gebruikt nu de juiste naam van de afzender in e-mailberichten wanneer er wijzigingen worden aangebracht in bedrijfsaccounts. Eerder, gebruikte Adobe Commerce de algemene naam van de contactafzender die in het standaardwerkingsgebied voor alle e-mails wordt bepaald. <!--- MC-33917-->

- Het is nu mogelijk om multiShipping-taken uit te voeren voor bestellingen die zowel fysieke als virtuele producten bevatten. <!--- MC-33818-->

- Handelaars kunnen nu bedrijfsgebruikers maken vanuit de sectie _[!UICONTROL Company Users]_&#x200B;in Mijn account- en bedrijfsstructuur wanneer **[!UICONTROL Access Restriction]**&#x200B;is ingeschakeld en **[!UICONTROL Restriction Mode]**&#x200B;is ingesteld op `Sales: Login Only` . Eerder heeft Adobe Commerce deze fout gegenereerd toen een handelaar een gebruiker probeerde te maken: `Can not register new customer due to restrictions are enabled` . <!--- MC-33608-->

- Adobe Commerce herstelt de standaardklantengroep van een klant niet meer wanneer een klant zijn accountgegevens opslaat. <!--- MC-33554-->

- Adobe Commerce genereert niet langer een fatale fout wanneer een beheerder een klant die een actief winkelwagentje heeft, toewijst aan een klantengroep. <!--- MC-33313-->

- Adobe Commerce biedt nu een `addToCart` DataLayer-gebeurtenis voor snelle volgorde en aanvraaglijsten met pagina&#39;s.  <!--- MC-33295-->

- E-mailberichten die worden verzonden naar verkoopvertegenwoordigers die aan een bedrijf zijn toegewezen, bevatten nu het toegewezen bedrijfslogo. Eerder bevatte het e-mailbericht het standaard LUMA-logo, niet het geüploade bedrijfslogo. <!--- MC-33232-->

- Een aanvraaglijst bevat nu alle gegroepeerde producten en hoeveelheden die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, gaf Adobe Commerce deze fout weer: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

- De query `products` retourneert nu een accuraat `total_count` -veld wanneer de gedeelde catalogus is ingeschakeld. <!--- MC-42268-->

- De Configuratie van het Bedrijf en creëren de pagina&#39;s van het Bedrijf werken nu zoals verwacht nadat u een online verschepende methode onbruikbaar maakt. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected` . <!--- MC-43178-->

- Het geheugenverbruik van de integratietest is verminderd, wat de testprestaties verbetert en de tijd die nodig is voor het voltooien van de test verkort. <!--- AC-266-->

### B2B v1.2.0

*28 juli, 2020*

[!BADGE &#x200B; Ondersteunde &#x200B;]{type=Informative tooltip="Ondersteund"} Adobe Commerce 2.4.0 en nieuwere versies

- Extra ondersteuning voor Adobe Commerce 2.4.0.

- Het Onderzoek van de Orde van de Storefront, met dank voor de bijdrage van Marek Mularczyk van [&#x200B; Divante &#x200B;](https://www.divante.com/) en communautaire leden.

- Inkooporders worden uitgebreid en herschreven. Ze zijn nu standaard opgenomen in Adobe Commerce.

- Goedkeuringsregels voor inkooporders zijn geïmplementeerd. Met deze regels kunnen gebruikers de workflow voor inkooporders beheren door aankoopregels voor bestellingen te maken.

- Aanmelden als klant is nu standaard opgenomen in Adobe Commerce. Deze eigenschap staat plaatswerknemers toe om klanten bij te staan door zich aan te melden als klant om te zien wat zij zien.

- Kenmerkaggregaties werken nu correct voor gelaagde navigatie met Elasticsearch

- Het zoeken naar bestellingen met speciale tekens werkt nu goed.

- Wanneer u op de knop **[!UICONTROL Clear All]** klikt, worden alle filters uitgevouwen in plaats van samengevouwen.

- Product-SKU/Naam is nu opgenomen in de samenvatting van het zoekfilter Volgorde.

- De sorteerindicator wordt nu correct weergegeven in het raster Mijn inkooporders.

- Nu kunt u slechts eenmaal op de knoppen Goedkeuren, Annuleren, Afwijzen en Inkooporder klikken. Eerder kon u meerdere keren op de knop klikken.

- De knoppen Aankooporder goedkeuren, Afwijzen, Annuleren en Valideren worden nu correct weergegeven op mobiele apparaten.

- Eerder werd bij het goedkeuren van een inkooporder met een korting die is verlopen, het volledige bedrag van de order geplaatst en het totaal van de inkooporder niet bijgewerkt. Nu wordt het totaal van de inkooporder bijgewerkt om het juiste totaal weer te geven.

- Een kwestie werd geïntroduceerd in 2.3.4 waar de attributen van de douaneverlenging niet van het Adres van de Klant aan het Adres van het Citaat zouden worden gekopieerd. Dit probleem is opgelost.

- Als B2B is geïnstalleerd, wordt een SQL-fout weergegeven bij het toewijzen van categorieën aan gedeelde catalogi. Dit probleem is opgelost.

- Vanwege een onjuiste waarde voor het type variabele kunnen beheerders geen configureerbare producten aan een bestelling toevoegen. De keuzelijst met opties wordt niet gevuld. Deze functie werkt nu goed.

- Eerder, wanneer het uitgeven van de Toestemmingen van de Categorie voor de niet Gelogde Groep, zou een fout voorkomen wanneer het bewaren van de veranderingen. Dit probleem is opgelost.

- Er wordt een correctie toegevoegd waarmee opslagbeheerders producten kunnen toevoegen aan een volgorde die zich niet in de gedeelde catalogus bevindt. Er wordt eerder een foutbericht weergegeven wanneer u een item toevoegt dat zich niet in de catalogus bevindt.

- [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} vroeger, na het in werking stellen van het bevel `php bin/magento indexer:set-dimensions-mode catalog_product_price website` en dan het proberen om een gedeelde catalogus tot stand te brengen, zou een fout voorkomen. Dit probleem is opgelost.

- Bij het toevoegen van een bedrijf en het toewijzen van de bedrijfsbeheerder aan een niet-standaardwebsite, werd de verkeerde site-id verzonden, wat een fout veroorzaakte. Dit probleem is opgelost.

- Eerder, nadat een klant aan een andere klantengroep werd bewogen, zou het toevoegen van een product aan een orde gebruikend _Snelle Orde_ met een fout ontbreken. Dit probleem is opgelost.

- Eerder, toen het proberen om uit te checken gebruikend WebAPI met een citaat B2B, werd een onjuiste waarde verzonden naar API, veroorzakend een fout om voor te komen. Dit probleem is opgelost.

- Als u een bedrijf via de API instelt op Actief, treedt er eerder een fout op. Dit probleem is nu opgelost.

- Vanwege een overbodige `form` -tag is de bestelpagina automatisch vernieuwd wanneer u op Enter drukt nadat u de voorgestelde verzendkosten hebt gewijzigd. Dit probleem is opgelost.

- Er is eerder een fout opgetreden bij het instellen van een weergavelimiet voor een product op een cataloguspagina en die limiet was lager dan het totale aantal producten. Die functie werkt nu zoals u had verwacht.

- Eerder, wanneer het veranderen van admin van een bedrijf, zou het originele admin adres aan nieuwe admin worden gekopieerd, die hen twee adressen geeft. Nu wordt alleen het juiste adres toegevoegd.

- Eerder mislukte het gebruik van de API om een aanhalingsteken op te slaan wanneer de backorder is ingesteld op &quot;Allowed and Notify Customer&quot;.  &quot;Toegestaan en Klant op de hoogte stellen&quot; mislukt. Deze API-aanroep werkt nu zoals u had verwacht.

- De Vaste productbelasting wordt nu weergegeven op de detailpagina Aanhalingstekens.

- Als u eerder op een bijlage op het tabblad Opmerkingen van de pagina Mijn aanhalingstekens klikt, kan het bestand niet worden gedownload. Dit gedrag werkt nu zoals verwacht.

#### Bekende problemen

- Adobe Commerce genereert een uitzondering tijdens de upgrade naar B2B 1.2.0 in een implementatie voor meerdere websites. Wanneer `setup:upgrade` wordt uitgevoerd, treedt deze fout op in de module `PurchaseOrder` module: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder` . **Oplossing**: Installeer de `B2B-716 Add NonTransactionableInterface` interface aan `InitPurchaseOrderSalesSequence` hotfix van het gegevenspatroon, die nu van **Mijn Rekening** beschikbaar is > **downloadt** sectie van `magento.com`.
- Als een kortingscode vervalt voordat een inkooporder (PO) wordt goedgekeurd, blijft de inkooporder het gedisconteerde bedrag weergeven, maar als de inkooporder eenmaal is goedgekeurd, wordt de order geplaatst op het niet-gedisconteerde totaal. **Oplossing**: Installeer `B2B-709 Purchase Order Discount patch` hotfix voor deze kwestie, die nu van **Mijn Rekening** > **Downloads** sectie van `magento.com` beschikbaar is.
- Als de items in een inkooporder niet in voorraad zijn of niet voldoende in voorraad zijn wanneer de inkooporder wordt omgezet in een werkelijke bestelling, treedt er een fout op. Als backorders worden ingeschakeld, wordt de volgorde op de normale wijze verwerkt.
