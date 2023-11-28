---
title: CCPA-conformiteit
description: Leer over de Wet van de Privacy van de Consumentenprivacy van Californië (CCPA), die de rechten van consumenten in Californië uitbreidt om te bepalen hoe hun persoonlijke informatie wordt verzameld, opgeslagen, en gebruikt.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2260'
ht-degree: 0%

---

# CCPA-conformiteit

>[!NOTE]
>
>Deze informatie is in een reeks onderwerpen om verkopers en ontwikkelaars van Adobe Commerce te helpen de implicaties van de Wet van de Privacy van de Consumentenbescherming van Californië begrijpen. De informatie is gebaseerd op de tekst van het statuut. Om te bevestigen als CCPA op uw zaken van toepassing is, raadpleeg uw advocaat.

De [California Consumer Privacy Act][5] (CCPA) breidt de rechten van consumenten in Californië uit om te bepalen hoe hun persoonlijke informatie wordt verzameld, opgeslagen, en gebruikt. De nadruk ligt op de bescherming van de consument tegen de ongeoorloofde verkoop of uitwisseling van persoonlijke informatie. De CCPA is in 2018 vastgesteld en is op 1 januari 2020 in werking getreden.

De CCPA verleent de consument de volgende nieuwe rechten:

- **Recht op kennis** de categorieën van persoonlijke informatie over hen die in de afgelopen twaalf maanden worden verzameld, gebruikt, gedeeld of verkocht.
- **Recht om te verwijderen** bepaalde soorten persoonlijke informatie die in het bezit zijn van een bedrijf en/of hun dienstverleners.
- **Recht om te weigeren** van de verkoop van hun persoonlijke gegevens.
- **Recht op non-discriminatie** in termen van prijs of dienst voor het uitoefenen van een privacyrecht in het kader van de CCPA.

Voor CCPA-doeleinden wordt persoonlijke informatie in deze context gedefinieerd als:

>Informatie die identificeert, verband houdt met, beschrijft, kan worden geassocieerd met of redelijkerwijs direct of indirect kan worden gekoppeld aan een bepaalde consument of een bepaald huishouden. (Sectie 1798.140)

In dit verband omvat het bepaalde gegevenselementen die niet als persoonsgegevens in de context van andere wet- of regelgeving kunnen worden beschouwd. Handelaren moeten dit in gedachten houden wanneer zij bepalen of en hoe zij de wet moeten naleven.

CCPA vereist ook ondernemingen om te verstrekken _redelijke zekerheid_, en omvat uitgebreide bepalingen inzake gegevensbescherming voor consumenten, waaronder het recht om juridische stappen te ondernemen in geval van een inbreuk in verband met gegevens.

Raadpleeg uw juridische adviseur om te bepalen of en hoe u aan om het even welke vereisten zou moeten voldoen CCPA die op u en uw zaken van toepassing kunnen zijn. Dit omvat de nieuwe vereisten inzake kennisgeving, opt-out en registratie die bedrijven volgens de wet moeten uitvoeren.

## Zakelijke vereisten

CCPA is op ondernemingen met winstoogmerk van toepassing die zaken in Californië doen en om het even welke volgend ontmoeten:

- Een bruto jaaromzet van meer dan 25 miljoen dollar hebben
- Koop, ontvang of verkoop de persoonlijke informatie van 100.000 of meer inwoners van Californië, huishoudens of apparaten
- Afleiden 50% of meer van hun jaarlijkse opbrengst van het verkopen van de persoonlijke informatie van de inwoners van Californië.

## CCPA-compatibiliteitsgids

Deze sectie verstrekt een overzicht op hoog niveau van de stappen die voor verkopers worden vereist om privacyverordeningen zoals de Wet van de Privacy van de consument van Californië (CCPA) na te leven.

### GDPR en CCPA

Als uw bedrijf zowel aan [Algemene verordening inzake gegevensbescherming](compliance-gdpr.md) (GDPR) en de CCPA kunt u een deel van het werk uit uw GDPR nalevingsprogramma voor CCPA gebruiken. Hoewel de verordeningen enkele gelijkenissen vertonen, zijn er enkele verschillen:

- De definitie van persoonlijke informatie verschilt per verordening.
- De GDPR bepaalt dat consumenten zich moeten aanmelden voordat hun persoonsgegevens voor bepaalde doeleinden kunnen worden gebruikt; de CCPA geeft consumenten het recht om te weigeren.
- De CCPA heeft aanvullende vereisten inzake gegevensinventarisatie en -toewijzing.
- De regels hebben verschillende vereisten voor het privacybeleid.

Ondernemingen die aan de GDPR voldoen, kunnen aanvullende verplichtingen uit hoofde van de CCPA hebben. Zie voor meer informatie de [CCPA-werkblad][3]{:target=&quot;_blank&quot;}.

### Routekaart voor naleving

Er is een gecoördineerde inspanning nodig om een plan te ontwikkelen en uit te voeren om de naleving aan te pakken. Gebruik deze roadmap als gids om middelen te mobiliseren en aan taken voorrang te geven zodat u zich op veelvoudige fronten kunt bewegen. Het proces is in wezen hetzelfde voor iedereen [!DNL Commerce] installaties, met uitzondering van:

- **Adobe Commerce over cloudinfrastructuur**: Handelaars met winkels die op Adobe worden gehost [cloudinfrastructuur][4]{:target=&quot;_blank&quot;} kan de technische accountmanager van Adobe Commerce of de klantenondersteuning vragen om hulp bij het beantwoorden van consumentenverzoeken.

- **Op locatie**: Handelaren met installaties op locatie in Adobe Commerce of Magento Open Source moeten hun eigen processen en instrumenten ontwikkelen om te reageren op en om consumentenverzoeken in verband met privacyregels te beheren.

#### Stap 1: Samenstellen van een interfunctioneel team dat de naleving van de regelgeving moet aanpakken

Stel een team samen dat de volgende functionele rollen in uw zaken vertegenwoordigt, en plant een opleidingszitting om hen aan snelheid op de wetgeving te brengen. Vervolgens wijst u de vereiste taken toe aan de belanghebbenden op basis van hun rol.

- Bedrijfsstrategie en -activiteiten
- Juridisch
- Informatietechnologie
- Gebruikerservaring
- Klantenservice
- Administratieve ondersteuning

Vanuit zakelijk perspectief moet u bepalen of uw bedrijf deze privacybeschermingsmaatregelen alleen uitbreidt tot consumenten in Californië, of deze beschikbaar maakt voor alle consumenten, ongeacht hun locatie.

#### Stap 2: Maak een inventaris van uw digitale eigenschappen

**Belanghebbenden:** Informatietechnologie, juridische en administratieve ondersteuning

Maak een inventaris van uw digitale eigenschappen, inclusief alle integraties en wie toegang heeft tot uw consumentengegevens.

1. Bepaal welke persoonlijke openbare en persoonlijke gegevens worden verzameld via uw websites en mobiele toepassingen. Bijvoorbeeld, slaat een standaardgegevensbestand van de Handel de volgende soorten openbare en privé persoonlijke informatie op:

   - **Openbaar**: Gezichtslijsten, productoverzichten

   - **Persoonlijk**: Informatie van de klant, bestelgegevens, terugbetalingspunten, register van cadeau, adresboek, winkelkrediet, betalingsmethoden, factureringsovereenkomsten, abonnementen op nieuwsbrief, uitnodigingen.

     Als uw [!DNL Commerce] de installatie is aangepast, aanvullende persoonlijke informatie kan worden verzameld. Persoonlijke gegevens kunnen ook in [cookies](./compliance-cookie-law.md), tags en andere technologieën die informatie verzamelen.

1. Identificeer de partijen met wie u gegevens deelt. In de lijst moeten dienstverleners en derden worden opgenomen. Onder andere advertentienetwerken, internetserviceproviders, gegevensanalytische providers, overheidsentiteiten, besturingssystemen en platforms, sociale netwerken en wederverkopers van consumentengegevens die niet rechtstreeks persoonlijke informatie van uw consumenten verzamelen.

   - **Serviceproviders**: Entiteiten die voor zakelijke doeleinden toegang hebben tot uw consumentengegevens en die namens u services leveren. Adobe is bijvoorbeeld een serviceprovider, net als sommige ontwikkelaars van aanpassingen, extensies en services.

     Controleer de standaardinstellingen van Google Universal Analytics, Google Tag Manager (en alle andere gegevensservices die u gebruikt) en breng de wijzigingen aan die nodig zijn om aan de verordening te voldoen. Zie voor meer informatie [Google Privacy-instellingen](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Andere derde partijen**: Entiteiten met wie u consumentengegevens deelt of verkoopt. U kunt bijvoorbeeld consumentengegevens delen met een reclamenetwerk in ruil voor reclame.

#### Stap 3: Wijs de klantenreis en het proces van de gegevensinzameling in uw opslag toe

**Belanghebbenden:** Gebruikerservaring, informatietechnologie, administratieve ondersteuning

1. Elk punt in het dialoogvenster identificeren [reis van klant] wanneer persoonlijke informatie wordt verzameld, en het type informatie dat bij elke stap wordt verzameld.

   Bezoekers van uw site moeten hiervan vooraf op de hoogte worden gesteld of op het punt waar de gegevens worden verzameld. Een winkel zonder aangepaste integratie verzamelt bijvoorbeeld persoonlijke gegevens wanneer een klantenaccount wordt gemaakt en tijdens het afrekenen. Als uw winkel aangepaste integraties heeft, zijn er mogelijk aanvullende gegevensposten en kenmerken die moeten worden geïdentificeerd.

1. Zie de volgende onderwerpen voor toepasselijke gegevensstroomdiagrammen en de afbeeldingen van de gegevensbestandentiteit voor elke versie:

   - [Referentie van persoonlijke gegevens (2.x)][1]
   - [Referentie van persoonlijke gegevens (1.x)][2]

   ![diagram](./assets/privacy-frontend-diagram.svg)

#### Stap 4: Vestig procedures en mechanismen om op klantenverzoeken te antwoorden

**Belanghebbenden:** Klantenservice, informatietechnologie, gebruikerservaring, administratieve ondersteuning

Vanuit het oogpunt van gegevensbeheer zijn bij elk verzoek om persoonlijke informatie de volgende partijen betrokken:

- **Gegevensproefpersonen** (Consumenten): Onder CCPA kan elke persoon in Californië die persoonlijke informatie verstrekt om een aankoop te doen en/of een klantenrekening te handhaven een verzoek indienen om tot hun persoonlijke gegevens toegang te hebben of te schrappen.

- **Entiteiten die optreden als ondernemingen binnen het toepassingsgebied van de CCPA** (merken): [!DNL Commerce] handelaren verzamelen en bewaren persoonlijke gegevens van hun klanten en gasten die in hun winkels aankopen doen .

- **Gegevensprocessor** (Technologieleveranciers): Adobe Commerce en Magento Open Source werken als verwerkers van de persoonsgegevens die worden opgeslagen als onderdeel van de diensten die aan handelaren worden geleverd. Als verwerker verwerkt de Adobe persoonsgegevens overeenkomstig de toestemming en instructies van de handelaar, overeenkomstig de licentieovereenkomst.

Merchants zijn verantwoordelijk voor het volgende:

1. Identificeer de partijen betrokken bij het Verzoek van de Toegang van het Onderwerp van Gegevens (DSAR) en verifieer de identiteit van om het even welke persoon die verzoeken om te weten, te kiezen of te schrappen. Dit is van toepassing op een persoon met een wachtwoord of een persoon die in uw winkel winkelt als gast.

1. De consument binnen 45 dagen na ontvangst van een controleerbaar verzoek van de consument informatie verstrekken en aan hem verstrekken in antwoord op zijn verzoek om rechten, tenzij dit niet mogelijk is. (De wet bevat een aantal andere vereisten voor een bedrijf om naleving te handhaven bij vertragingen van maximaal 45 dagen).

   Handelaren moeten binnen 45 dagen op elke DSAR reageren, te beginnen op de dag waarop het verzoek is ontvangen. Indien nodig kunnen handelaren tot 45 dagen langer reageren, in totaal maximaal 90 dagen vanaf de dag van ontvangst van het verzoek. Dit vereist dat de handelaar de klant meedeelt om de reden voor de vertraging te verklaren.

1. Ontwikkel een mechanisme om de vereiste berichten in uw opslag te presenteren en de reactie van de consument te verzamelen.

1. Stel responsprocedures vast en documenteer elk van de volgende verzoeken:

   - **Verzoeken om kennis** - Bezoekers in uw winkel moeten op de hoogte worden gesteld van alle regelingen die u moet treffen om hun persoonlijke gegevens te verkopen of met derden te delen, en mogen zich afmelden. De details van uw gebruik van persoonlijke gegevens en de partijen met wie u gegevens deelt of verkoopt, kunnen in uw privacybeleid worden gehandhaafd.

   - **Verzoeken om te weigeren** - Indien persoonsgegevens worden verkocht of aan derden worden doorgegeven in ruil voor een waardevolle vergoeding, vereist de CCPA een _Mijn gegevens niet verkopen_ koppeling op elk punt waar deze wordt verzameld. Aanvullende door de gebruiker ingeschakelde invoerbesturingselementen, zoals selectievakjes en knoppen, kunnen worden gebruikt in e-mailcommunicatie, voorkeursinstellingen voor websites of in websiteformulieren op het punt van gegevensverzameling, zodat individuen een geldige &quot;opt-out&quot;-aanvraag kunnen indienen.

   - **Verzoeken om te verwijderen**

      - Handelaren wier winkels op Adobe Commerce Cloud worden gehost, dienen contact op te nemen met de Adobe Support voor hulp bij het verwijderen van persoonlijke gegevens. Neem voor meer informatie contact op met de technische accountmanager of de klantenondersteuning van de Adobe.
      - Handelaars die installaties van Adobe Commerce of Magento Open Source op gebouw in werking stellen moeten hun eigen proces en manuscript uitvoeren om persoonlijke informatie op verzoek te schrappen.

#### Stap 5: Schrijf de inhoud voor de vereiste klantenberichten

**Belanghebbenden:** Juridisch, Klantenservice, gebruikerservaring, informatietechnologie, administratieve ondersteuning

1. Bepaal in samenwerking met uw juridisch adviseur de soorten berichten die aan uw website moeten worden toegevoegd om aan verplichtingen CCPA te voldoen.

   - **Kennisgeving van verzameling**: Een kennisgeving die op of vóór het tijdstip waarop de persoonsgegevens bij de consument worden verzameld, wordt verstrekt. De kennisgeving moet in gewone taal worden geschreven en moet voor de gemiddelde persoon gemakkelijk te begrijpen zijn. De kennisgeving moet opvallend zijn en in een of meer dezelfde talen worden geleverd als de inhoud van uw website.

   - **Kennisgeving van het recht om te weigeren**: Een kennisgeving die consumenten informeert over hun recht om zich te onthouden van de verkoop van hun persoonlijke gegevens.

   - **Aankondiging van financiële stimulans**: Een kennisgeving waarin elke financiële prikkel, prijs of verschil in service wordt uitgelegd die uw bedrijf ontvangt in ruil voor persoonlijke informatie.

   - **Hoe te om een Verzoek om de Verzameling van Persoonlijke Informatie en Gebruik voor te leggen**: Instructies voor individuen om een verzoek in te dienen dat u de persoonlijke informatie openbaar maakt die u over het individu hebt verzameld, met inbegrip van:

      - Specifieke persoonlijke gegevens die u over de consument hebt verzameld
      - Categorieën persoonlijke gegevens die u over de consument hebt verzameld
      - Categorieën bronnen waaruit de persoonsgegevens worden verzameld
      - Categorieën persoonlijke informatie over de consument die u voor zakelijke doeleinden hebt verkocht of openbaar gemaakt
      - Categorieën derden aan wie de persoonsgegevens voor zakelijke doeleinden zijn verkocht of bekendgemaakt
      - De redenen waarom uw bedrijf persoonlijke gegevens verzamelt en/of verkoopt

1. Verzend de inhoud naar het team en, indien mogelijk, naar uw juridische adviseur voor controle.

1. Bepaal waar de berichten verschijnen, hoe zij (voor elk bezoek, bij authentificatie of bij klik-door) functioneren, en hun positie en formaat met betrekking tot andere inhoud.

1. Geef de goedgekeurde inhoud door aan uw ontwikkelingsteam.

#### Stap 6: Controleer uw overeenkomsten met serviceproviders

**Belanghebbenden:** Juridische en administratieve ondersteuning

Controleer en werk zo nodig alle dienstverleningscontracten bij om de CCPA-vereisten te weerspiegelen.

#### Stap 7: Je privacybeleid bijwerken

**Belanghebbenden:** Juridische en administratieve ondersteuning

Controleer uw huidige privacybeleid en overweeg wat, als om het even welk, extra informatie noodzakelijk is.

- **Gebruik van persoonlijke gegevens**: U moet openbaar maken welke persoonlijke gegevens worden verzameld en welke financiële prikkels u krijgt in ruil voor de verkoop van persoonlijke gegevens. U moet ook uitleggen hoe de prikkel in het kader van de CCPA is toegestaan en hoe de waarde van de persoonlijke gegevens wordt berekend.

- **Leeftijd van instemming**: Wanneer u persoonlijke gegevens over minderjarigen verzamelt of gebruikt, kan het zijn dat aan de volgende vereisten wordt voldaan:

   - **Mineruren &lt; 13**: Ouderlijke toelating is vereist voor minderjarigen jonger dan 13 jaar om zich aan te sluiten bij de verkoop van hun persoonlijke gegevens.

   - **Minder dan 13 tot &lt; 16**: Minderjarigen van ten minste 13 jaar en jonger dan 16 jaar kunnen zich aanmelden voor de verkoop van hun persoonlijke gegevens, mits het bedrijf een redelijke procedure instelt om de actie te documenteren. Het proces moet in het bedrijf worden beschreven [privacybeleid](privacy-policy.md). Wanneer een bedrijf verzoeken van minderjarigen in deze leeftijdsgroep ontvangt, moet het hen op de hoogte stellen van hun recht om later af te zien en uitleggen hoe ze dat moeten doen.

  >[!IMPORTANT]
  >
  >Handelaren mogen de persoonsgegevens van kinderen niet op [!DNL Commerce] platform of systemen. Als er redenen zijn om aan te nemen dat de verzamelde gegevens tot een minderjarige behoren, moet het uit een [!DNL Commerce] onmiddellijk platform om schending van de licentievoorwaarden van de Adobe te voorkomen.

#### Stap 8: alle gerelateerde procedures documenteren en registers bijhouden

**Belanghebbenden:** Klantenservice, administratieve ondersteuning

Gedurende 24 maanden nadat elk verzoek om individuele rechten is ontvangen, wordt een register bijgehouden van het verzoek en de antwoorden van uw bedrijf.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
