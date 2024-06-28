---
title: '''[!DNL Adobe Commerce B2B] opmerkingen vrijgeven'
description: Lees de release-notities voor meer informatie over wijzigingen in [!DNL Adobe Commerce B2B] lozingen.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 17eec4e7755ce4e83fb0533940bdce6c96ddc717
workflow-type: tm+mt
source-wordcount: '6867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] releaseopmerkingen

In deze releaseopmerkingen voor de B2B-extensie worden aanvullingen en correcties vastgelegd die Adobe tijdens een releasecyclus heeft toegevoegd, waaronder:

![Nieuw](../assets/new.svg) Nieuwe functies
![Probleem opgelost](../assets/fix.svg) Oplossingen en verbeteringen
![Bekend probleem](../assets/bug.svg) Bekende problemen

>[!NOTE]
>
>Zie [Productbeschikbaarheid](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) voor informatie over versies van de B2B Commerce-extensie die worden ondersteund voor beschikbare Adobe Commerce-releases.

## B2B 1.5.0-bèta

{{$include /help/_includes/b2b-beta-note.md}}

*13 november 2023*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

De B2B v1.5.0-bètaversie bevat nieuwe functies, kwaliteitsverbeteringen en oplossingen voor problemen.

![Nieuw](../assets/new.svg) De verbeteringen aan het citeren mogelijkheden helpen Kopers en Verkopers citaten beheren en citeren onderhandelingen effectiever.

- **Aanhalingsteken opslaan als concept**<!--B2B-2566-->—Bij het maken van een [prijsaanvraag](quote-request.md) in het winkelwagentje kunnen kopers het aanhalingsteken nu opslaan als een concept door **[!UICONTROL Save as Draft]** op de [!UICONTROL Request a Quote] formulier.

  Het conceptaanhalingsteken heeft geen vervaldatum. Kopers kunnen conceptaanhalingstekens van de [!UICONTROL My Quotes] van hun accountdashboard.

- **Naam prijsopgave wijzigen**<!--B2B-2596-->—Kopers kunnen nu een aanhalingstekennaam wijzigen in het menu [Offertegegevens](account-dashboard-my-quotes.md#quote-actions) pagina door de **[!UICONTROL Rename]** -optie. Deze optie is beschikbaar voor geautoriseerde kopers wanneer ze de prijsopgave bewerken. Gebeurtenissen van de naamwijziging worden opgenomen in het logboek met offertegeschiedenis.

- **Aanhalingsteken dupliceren**<!--B2B-2701-->—Kopers en verkopers kunnen nu een nieuw prijsopgave maken door een bestaand prijsopgave te kopiëren. Er wordt een kopie gemaakt van de gedetailleerde weergave van het citaat door  **[!UICONTROL Create Copy]** op de [Gedetailleerde weergave van offertes](quote-price-negotiation.md#button-bar) in de Admin of [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Vergrendeling van lijstitem**<!--B2B-2597-->—Tijdens prijsonderhandeling kunnen verkopers de sluiten van de lijnkorting van het puntobject voor meer flexibiliteit gebruiken wanneer het toepassen van kortingen. Een verkoper kan bijvoorbeeld een korting op een speciaal regelobject toepassen op een object en het object vergrendelen om verdere kortingen te voorkomen. Wanneer een item is vergrendeld, kan de objectprijs niet worden bijgewerkt wanneer een korting op prijsniveau wordt toegepast. Zie [Aanhalingstekens voor een koper starten](sales-rep-initiates-quote.md).

![Nieuw ](../assets/new.svg)**Bedrijfsbeheer**<!--B2B-2901-->—Merchants kunnen nu Adobe Commerce-bedrijven weergeven en beheren als hiërarchische organisaties door bedrijven toe te wijzen aan aangewezen moedermaatschappijen. Nadat een bedrijf aan een ouder wordt toegewezen, kan de beheerder van het moederbedrijf de bedrijfrekening beheren. Alleen geautoriseerde beheergebruikers kunnen bedrijfstoewijzingen toevoegen en beheren. Zie voor meer informatie [Bedrijfshiërarchie beheren](assign-companies.md).

- Op de pagina Companies wordt een nieuwe **[!UICONTROL Company Type]** in het veld worden de moederondernemingen en de onderliggende ondernemingen geïdentificeerd. De handelaren kunnen de bedrijfmening door bedrijfstype filtreren, en bedrijven beheren gebruikend lijnpunt of bulkacties.

- De handelaars kunnen bedrijfstaken van de nieuwe toevoegen en beheren **[!UICONTROL Company Hierarchy]** de [!UICONTROL Company Account] pagina.

- API-ontwikkelaars kunnen het nieuwe API-eindpunt voor bedrijfsrelaties REST gebruiken `/V1/company/{parentId}/relations` om bedrijfstoewijzingen te maken, weer te geven en te verwijderen. Zie [Bedrijfsobjecten beheren](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) in de *Web API Developer Guide*.

![Probleem opgelost](../assets/fix.svg)<!--ACP2E-1984-->Handelaren die op de knop **[!UICONTROL Print]** in de gedetailleerde mening van het Citaat in Admin wordt nu ertoe aangezet om het citaat als PDF te bewaren. Eerder werden handelaren omgeleid naar een pagina met aanhalingsgegevens.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1742-->Eerder bij het verzenden van een klantofferte met 0 procent en het wijzigen van het aantal, genereert de beheerder een uitzondering, maar wordt het aantal opgeslagen. Nadat deze correctie van toepassing is, geldt voor de `0 percentage` De juiste uitzondering met een bericht zal worden geworpen.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1742-->Tijdens prijsonderhandelingen kan een verkoper nu een `0%` korting in het veld korting van de korting op de prijsopgave van de onderhandelde offerte en verzend de prijsopgave terug naar de koper. Als de verkoper eerder een korting van 0% heeft opgegeven en het prijsopgave heeft teruggestuurd naar de koper, heeft de beheerder een `Exception occurred during quote sending` foutbericht.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-2097-->De validatie van ReCaptcha werkt nu correct tijdens het afrekenen voor een B2B citaat wanneer ReCaptcha V3 voor storefront afhandeling wordt gevormd. Eerder is de validatie mislukt met een `recaptcha validation failed, please try again` foutbericht.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1825-->Aankooporders kunnen niet meer worden geplaatst door een gebruiker die met het bedrijf is geassocieerd nadat het bedrijf is geblokkeerd. Eerder had een gebruiker die banden had met het bedrijf kooporders kunnen plaatsen wanneer het bedrijf werd geblokkeerd.

![Probleem opgelost](../assets/fix.svg)<!--ACP2E-1933-->De beheerders van het bedrijf kunnen bedrijfgebruikers van de storefront nu toevoegen. Eerder heeft Commerce een fout geregistreerd toen een Admin-gebruiker probeerde een nieuwe gebruiker toe te voegen: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2-p1

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Toegevoegde compatibiliteit met de patchreleases van Adobe Commerce 2.4.7-p1 en 2.4.6-p6.


## B2B v1.4.2

*10 oktober 2023*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

De B2B v1.4.2-release bevat kwaliteitsverbeteringen en foutoplossingen

![Probleem opgelost](../assets/fix.svg) <!--B2B-2897-->Als een verkoper een aanhalingsteken voor de koper maakt met een product-SKU die niet beschikbaar is in de gedeelde catalogus die bij de koper hoort, wordt het foutbericht weergegeven `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  De verkoper kan de prijsopgave pas opslaan als hij het product verwijdert dat niet beschikbaar is. Eerder, werd het citaat bewaard met niet beschikbare inbegrepen SKU, en het citaat kon niet op de storefront laden.

## B2B v1.4.1

*7 augustus 2023*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1.

De versie B2B v1.4.1 bevat kwaliteitsverbeteringen en oplossingen voor problemen.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1825-->Aankooporders kunnen niet meer worden geplaatst door een gebruiker die met het bedrijf is geassocieerd nadat het bedrijf is geblokkeerd. Eerder had een gebruiker die banden had met het bedrijf kooporders kunnen plaatsen wanneer het bedrijf werd geblokkeerd.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1943-->De status met terugwerkende kracht van het product wordt nu correct weergegeven in de winkel. Eerder werden producten die voor verzending beschikbaar waren, onjuist geïdentificeerd als achtergeordend.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1862-->Als het bedrijfsregistratieformulier een kenmerk van het type klantbestand bevat, wordt het bestand dat tijdens het registratieproces is geüpload, nu opgenomen in de accountgegevens voor de bedrijfsbeheerder nadat het bedrijf is gemaakt. Eerder ontbrak de bijlage.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1793-->De staalkiezer voor een configureerbaar product wordt nu weergegeven zoals u verwacht op de pagina met de configuratie van items in de lijst met aanvragen. Eerder, werd de monsterselecteur getoond als dropdown gebied in de pagina van de de puntconfiguratie van de verzoeklijst.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1968-->Wanneer u de opdracht [Onderneming GraphQL-query](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) om bedrijfsgegevens terug te sturen , worden de resultaten nu zonder fout geretourneerd .

## B2B v1.4.0

*13 juni 2023*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibel met Adobe Commerce 2.4.7-beta1

Deze release bevat nieuwe mogelijkheden en verbeteringen voor B2B-onderhandelbare aanhalingstekens en meerdere opgeloste problemen.

![Nieuw](../assets/new.svg) Toegevoegde compatibiliteit met Adobe Commerce 2.4.7-beta1.

![Nieuw](../assets/new.svg) **Aanhalingstekens door verkoper**—Verkopers kunnen nu rechtstreeks een prijsopgave voor een koper starten via het prijsopgave en de klantennetwerken in de beheerder. Dit vermogen stroomlijnt het prijsverhogingsproces en vermindert ingewikkeldheid voor klanten. Als een klant geen bestelling heeft geïnitieerd, kan een verkoper snel een prijsopgave namens de klant maken en het onderhandelingsproces starten. Eerder konden prijsopgaven alleen door de koper of door een verkoper die zich als klant heeft aangemeld, van de winkel worden gemaakt.

![Nieuw](../assets/new.svg) **Kortingen voor lijnitems en onderhandeling**—<!--B2B-2440--> Binnen een prijsopgave kunnen kopers en verkopers van B2B nu onderhandelen op het niveau van de lijnobjecten, door kortingen toe te passen en notities uit te wisselen totdat een overeenkomst is bereikt. De verwezenlijking van de nota en de updates zijn inbegrepen in het lijnpunt en citaatgeschiedenis om mededeling te volgen. Eerder konden kopers en verkopers alleen opmerkingen uitwisselen en kortingen toepassen op het prijsniveau.

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft nu de juiste gegevens weer tijdens de betaling wanneer de optie Aankooporders is ingeschakeld en er een virtueel prijsopgave is geselecteerd die met de PayPal-betalingsoptie is gemaakt. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1504--> Validatiefouten treden niet meer op wanneer u een bedrijf probeert op te slaan met een kredietlimiet die hoger is dan 999. Eerder, voor bedrijfskredietgrenzen groter dan 999, nam de handel van de Adobe een komma separator op, die een bevestigingsfout veroorzaakte die updates verhinderde worden bewaard.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1474-->  Het geselecteerde verzendadres blijft nu ongewijzigd wanneer u een bestelling plaatst met een verhandelbaar aanhalingsteken. Eerder, toen u een bestelling plaatste, werd het geselecteerde verzendadres veranderd in het standaardverzendadres.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1429--> In de montages van de Configuratie van de Opslag voor Functies B2B, **[!UICONTROL Enable Shared Catalog direct products price assigning]** veld wordt nu automatisch uitgeschakeld. In de winkel is deze verborgen wanneer de knop **[!UICONTROL Enable Company]** instellen of **[!UICONTROL Enable Shared Catalog]** instellen op **[!UICONTROL No]**.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1683--> Wanneer Commerce een bedrijfsaccount maakt vanuit de winkel, valideert het nu het e-mailadres voordat de bedrijfsregistratie wordt verwerkt. Als het e-mailadres ongeldig is, mislukt de bewerking en worden geen accountupdates verwerkt. Eerder werd een klantenrekening gecreeerd zelfs als het verzoek om een bedrijfrekening tot stand te brengen wegens een ongeldig e-mailadres ontbrak.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1664--> SKU&#39;s van producten die dubbele aanhalingstekens in de Gedeelde Catalogus en de prijsstructuur omvatten veroorzaken niet meer fouten in Admin.

![Probleem opgelost](../assets/fix.svg) <!--ACP2E-1498--> De Varnish-configuratie voor de Commerce-toepassing is bijgewerkt om te voorkomen dat gastgebruikers gegevens van andere klantgroepen kunnen zien.

### Bekend probleem

Als u B2B 1.4.0 installeert of verbetert op [Adobe Commerce versie 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), treedt de volgende fout op:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

U kunt dit probleem verhelpen door handmatige afhankelijkheden voor het B2B-beveiligingspakket toe te voegen door handmatige afhankelijkheden voor het B2B-beveiligingspakket toe te voegen met een [stabiliteitstag](https://getcomposer.org/doc/04-schema.md#package-links). Voor instructies raadpleegt u de [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14 maart 2023*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Release B2B versie 1.3.5-p2 ter ondersteuning van compatibiliteit met Adobe Commerce 2.4.6-p2.

![Nieuw](../assets/new.svg) Release B2B versie 1.3.5-p1 ter ondersteuning van compatibiliteit met Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Nadat u Commerce hebt geüpgraded van 2.4.6 naar [nieuwste release](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), zorg ervoor dat u een update uitvoert naar de ondersteunde B2B 1.3.5-patchrelease. Of upgrade de B2B-extensie van versie 1.3.5 naar versie 1.4.0 of hoger om de nieuwste functies te krijgen.

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.6.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce geeft nu de juiste gegevens weer tijdens de betaling wanneer de optie Aankooporders is ingeschakeld en er een virtueel prijsopgave is geselecteerd die met de PayPal-betalingsoptie is gemaakt. Eerder werden de totalen onder deze omstandigheden als nul weergegeven.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-609--> De lijst met klantgroepen voor de **Browsercategorie toestaan** het plaatsen bevat niet meer klantengroepen die met gedeelde catalogi verwant zijn.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1244--> Het kenmerk voor de klant van het BTW-nummer werkt nu zoals u had verwacht met de bedrijfsbeheeraccounts op zowel de Beheerder als de winkel. Aangepaste BTW-kenmerken zijn niet meer vereist om een bedrijfsaccount te maken. Eerder, toen een handelaar een ondernemingsrekening met een douaneBelastings/BTW attribuut creeerde, gaf Adobe Commerce een bevestigingsfout op zowel de opslagplaats als Admin.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1236--> Het uitschakelen van de functie voor gedeelde catalogus in een bepaald bereik werkt nu correct. Eerder stelde Adobe Commerce een ongeldig werkingsgebied in wanneer een handelaar gedeelde catalogusconfiguratie bewaarde.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1203--> Admin-gebruikers kunnen nu aangepaste kenmerkwaarden van klanten voor bedrijfsgebruikers opslaan. Eerder konden de douanekenmerken van de klant voor bedrijfgebruikers niet worden bewaard.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1221--> De problemen van prestaties worden opgelost met de bevestiging van bedrijftoestemmingen die door GraphQL worden verstrekt wanneer vele bedrijftoestemmingen reeds worden toegewezen.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce geeft niet langer een fout weer op de winkelwagentje wanneer met Snelle bestelling een product wordt toegevoegd in een hoeveelheid die groter is dan de voorraad.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1090--> De prestaties van `SELECT` de verrichtingen van de bedrijftoestemmingen zijn verbeterd.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-2456--> De vragen van de categorie keren nu productprijzen volgens de montages van de opslagconfiguratie terug wanneer er geen categorietoestemmingen uitdrukkelijk geplaatst op de categorie die worden gevraagd zijn.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-6829--> De **[!UICONTROL Place Order]** de knop werkt nu zoals u had verwacht wanneer u een aankoop met een goedgekeurd prijsverzoek voltooit. Problemen met de verhandelbare quote `negotiableQuoteCheckoutSessionPlugin` plug-in is opgelost.

## B2B v1.3.4

*9 augustus 2022*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.5.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce verzendt geen e-mailberichten meer telkens als een bestaand Bedrijf door een API vraag wordt bijgewerkt. E-mails worden nu alleen verzonden wanneer een bedrijf wordt gemaakt.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce berekent nu correct het totaal van een verhandelbaar prijsopgave wanneer de **[!UICONTROL Enable Cross Border Trade]** Instelling voor belastingberekening is ingeschakeld.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-322-->Configureerbare producten worden nu naar de laatste positie in de productlijst verplaatst nadat de voorraad is bijgewerkt wanneer de **[!UICONTROL Move out of stock to the bottom]** instelling is ingeschakeld. Er wordt een nieuwe aangepaste databasequery geïmplementeerd om ervoor te zorgen dat de sorteervolgorde voor de index van de Elasticsearch nu overeenkomt met de sorteervolgorde voor beheerders. Eerder, werden de configureerbare producten en hun kindproducten niet verplaatst naar de bodem van de lijst toen dit het plaatsen werd toegelaten.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-308-->E-mail met inkooporder respecteert nu de instelling voor het verzenden van e-mail van elke website in een implementatie met meerdere sites. Een controle voor de **[!UICONTROL Disable Email Communications]** deze instelling wordt toegevoegd aan de aangepaste logica voor e-mailwachtrijen. Eerder heeft Adobe Commerce de instelling voor het verzenden van e-mail voor de secundaire website niet gerespecteerd.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-302-->De titel van het SKU-veld van de pagina Snelle volgorde wordt voor de duidelijkheid gewijzigd.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce geeft nu een informatief foutbericht weer wanneer een winkel een ongeldige SKU invoert in het dialoogvenster **SKU of productnaam invoeren** veld.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-1753-->De **[!UICONTROL Account Created in]** het gebied voor een bedrijfbeheerder behoudt nu zijn waarde zoals verwacht nadat u het bedrijf opslaat.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-722 -->De `customer` de vraag keert geen lege resultaten meer terug wanneer het verzoeklijsten terugwint die door worden gefiltreerd `uid`.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-210 -->Een insteekmodule toegevoegd voor de `collectQuoteTotals` roep om ervoor te zorgen dat winkelkredieten slechts eenmaal worden toegepast.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-665 -->Klanten worden nu omgeleid naar de aanmeldingspagina wanneer hun account door een beheerder van de beheerder wordt verwijderd. Eerder gaf Adobe Commerce een fout. De insteekmodule (`SessionPlugin`) het codeblok bevindt zich nu in de `try…catch` blokkeren. Eerder, werd deze code niet verpakt binnen het generische uitzondering-behandelende blok.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-661 --> Druk op **Enter** nadat u een geldige productnaam of SKU hebt ingevoerd, gaat de verkoper nu naar het volgende veld zoals u had verwacht.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-607 -->De naam van het bedrijf is nu zichtbaar zoals u had verwacht in de gedeelten facturering en verzendadres van de afrekenworkflow.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-375 -->Winkelkrediet is nu niet beschikbaar als de **[!UICONTROL Zero Subtotal Checkout]** betalingsmethode is uitgeschakeld. Eerder was het selectievakje Winkelkrediet niet functioneel tijdens de plaatsing van de bestelling bij de beheerder. De toepassing heeft de order niet bij het winkelkrediet geplaatst en deze fout weergegeven: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 augustus 2022*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.4.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41985--> De tijd die nodig was om van Adobe Commerce 2.3.x aan Adobe Commerce 2.4.x in plaatsingen met meer dan 100.000 bedrijfrollen te bevorderen is aanzienlijk verminderd.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42153--> De POST `V1/order/:orderId/invoice` het verzoek steunt nu de opstelling van gedeeltelijke facturen wanneer de **[!UICONTROL Payment on Account]** betalingsmethode is ingeschakeld. Eerder heeft Adobe Commerce deze fout gegenereerd: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Probleem opgelost](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro werkt nu zoals u had verwacht met B2B verhandelbare aanhalingstekens wanneer het winkelwagentje van de klant andere producten bevat. Adobe Commerce verwerkt de bestelling nu met succes en stuurt een e-mail naar de klant zoals u had verwacht. Eerder gaf Adobe Commerce een fatale fout en stuurde een bevestigingsbericht naar de klant met daarin de nulwaarden.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41819--> Paginering wordt nu correct weergegeven op de pagina met zoekresultaten in een catalogus nadat sommige producten in een gedeelde catalogus zijn uitgesloten.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42886--> Aangepaste kenmerken van de klant worden nu op de verwachte manier opgeslagen wanneer u een bedrijfsgebruiker maakt of opslaat in de beheerdersbeheerder.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42927--> De **[!UICONTROL Submit]** op het formulier Nieuw bedrijf maken is nu uitgeschakeld nadat u met één klik hebt geklikt om te voorkomen dat meerdere formulieren worden verzonden. Eerder kon u dit formulier meerdere keren verzenden door herhaaldelijk op deze knop te klikken. Er is een fout opgetreden.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce geeft de koppeling voor opnieuw ordenen niet meer weer in de winkel wanneer een winkelier zich aanmeldt bij een winkel waarvoor opnieuw bestellingen zijn uitgeschakeld.

![Probleem opgelost](../assets/fix.svg) <!--- MC-43115--> Het zoeken in de snelle orde door SKU is nu case-insensitive wanneer de gedeelde catalogus wordt toegelaten.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42203--> U kunt een dossier voor een klantenattribuut nu bijwerken wanneer het creëren van een bedrijf. Eerder, toen u probeerde om een bedrijf met een gehechtheid van type tot stand te brengen `File`, Adobe Commerce heeft het bedrijf niet gemaakt en deze fout is in het uitzonderingenlogboek geregistreerd: `Something went wrong while saving file`.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42242--> U kunt nu een bedrijf met een klantenrekening tot stand brengen die een douaneattribuut met (`File`) of (`Image`) type. Eerder, als de rekening één van deze klantgerichte opties had, gaf het Bedrijf uit paginalader uitgeeft niet op, die het uitgeven van bedrijfdetails verhinderden.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42268--> De `products` query retourneert nu een nauwkeurige `total_count` veld wanneer gedeelde catalogus is ingeschakeld.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42203-->  U kunt een dossier voor een klantenattribuut nu bijwerken wanneer het creëren van een bedrijf. Eerder, toen u probeerde om een bedrijf met een gehechtheid van type tot stand te brengen `File`, Adobe Commerce heeft het bedrijf niet gemaakt en deze fout is in het uitzonderingenlogboek geregistreerd: `Something went wrong while saving file`.

![Probleem opgelost](../assets/fix.svg) <!--- MC-43178--> De _Bedrijfsconfiguratie_ en _Bedrijf maken_ De pagina&#39;s werken nu zoals u had verwacht nadat u een online verzendmethode onbruikbaar maakte. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42214--> De _Categorie_ De pagina toont nu verenigbare productgegevens terwijl de toestemmingen tijdens gedeeltelijke indexering worden geproduceerd. Er is een nieuwe gedeeltelijke indexator voor directorymachtigingen toegevoegd aan dit proces. Eerder waren de gegevens die werden weergegeven terwijl de indexeerfunctie werd uitgevoerd onjuist.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42567--> De `categoryList` de vraag keert nu het correcte aantal producten terug wanneer de catalogustoestemmingen worden gebruikt en de producten aan een gedeelde catalogus worden toegewezen.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42528--> De `categoryList` de vraag eerbiedigt nu categorietoestemmingen en keert slechts toegestane categorieën terug. Eerder, keerde het alle toegewezen en niet toegewezen categorieën terug.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42399--> De `rest/V1/company/{id}` request now returns `is_purchase_order_enabled` kenmerkwaarden zoals verwacht.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-128--> Aangepaste klantkenmerken worden nu op de verwachte manier weergegeven in het dialoogvenster _Bedrijfsbeheerder_ tab.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-130--> Het Mijn blok van de Lijst van de Wens op de Mijn pagina van de Rekening wordt nu getoond zoals verwacht voor de Admins van het Bedrijf en de Gebruikers van het Bedrijf.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-133--> Fouten in de Snelle volgorde worden niet meer weergegeven in het winkelwagentje. Eerder gaf Adobe Commerce deze fout weer in het winkelwagentje toen de SKU niet in de catalogus werd gevonden:  `The SKU was not found in the catalog`.

![Probleem opgelost](../assets/fix.svg) <!--- ACP2E-194--> Opslagbewerkingen voor gedeelde catalogus zijn geoptimaliseerd om sneller te kunnen worden uitgevoerd. Het opslaan van een gedeelde catalogus met veel klantengroepen kan eerder enkele minuten in beslag nemen.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce verwijdert nu alle machtigingen voor subcategorieën uit de `sharedcatalog_category_permissions` tabel wanneer de bovenliggende categorie wordt verwijderd. Eerder werden alleen de gegevens van de bovenliggende categorie verwijderd.

## B2B v1.3.2

*29 augustus 2022*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.3.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce verzendt nu bijgewerkte e-mailberichten over verlopen verhandelbare aanhalingstekens. Eerder, toen een verhandelbaar prijsopgave verstreek, heeft Adobe Commerce geen e-mails verzonden voor updates.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce verzendt nu met succes bijgewerkte e-mailberichten over binnenkort te verlopen en verlopen onderhandelbare prijsopgaven wanneer een `cron` taak ontbreekt.

### Bedrijf

![Probleem opgelost](../assets/fix.svg) <!--- MC-41542--> In het vervolgkeuzeveld voor het land van de pagina Nieuwe bedrijfsaccount maken worden geen lege optiewaarden meer weergegeven. Eerder waren de eerste twee optiewaarden en de landcode `AN` waren leeg.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41260--> Klik op de knop **[!UICONTROL Return]** voor een bestelling die door een bedrijfsgebruiker is gemaakt, wordt een beheergebruiker nu omgeleid naar de pagina Terugkeer maken zoals verwacht. Eerder werd de beheerder omgeleid naar de pagina Order History.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce mislukt niet meer door een fout als gevolg van onvoldoende geheugen bij het uitvoeren van de opdracht `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` methode tijdens `bin/magento setup:upgrade`. Eerder, gebruikte Adobe Commerce niet partijgrootte voor inzameling toen het initialiseren van toestemmingen, maar in plaats daarvan geladen een inzameling van alle bedrijfrollen.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40551--> De gebruikers van het bedrijf kunnen klanten de waarden van de douaneattributen nu uitgeven en bijwerken. Eerder waren deze kenmerken niet correct gekoppeld aan het formulier voor het maken en bewerken van gebruikers. Een bedrijfgebruiker kon verschillende kenmerkwaarden ingaan, maar Adobe Commerce heeft deze waarden niet correct bewaard.

![Probleem opgelost](../assets/fix.svg) <!--- MC-32653--> De middelboom voor de toestemmingen van de bedrijfrol kan nu worden vertaald zoals verwacht. Eerder was de machtigingenstructuur niet vertaald, ook al waren er geldige vertaalbestanden aanwezig.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce slaat nu de aangepaste kenmerkwaarden van de klant voor B2B-gebruikers op zoals verwacht. Eerder leidde het maken van een bedrijfsaccount dat aangepaste klantkenmerken bevatte tot een sjabloonfout en kon Adobe Commerce het formulier niet laden. Een argument toevoegen aan de layout van `company_create_account` dit probleem opgelost.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41721--> De gebruikersfilters van het bedrijf zoals tonen Alle Gebruikers, tonen Actieve Gebruikers, en tonen Inactieve Gebruikers werken nu zoals verwacht. Eerder veroorzaakte het filtreren van acties op de pagina van de bedrijfgebruiker een fout JavaScript.

### Bedrijfskrediet

![Probleem opgelost](../assets/fix.svg) <!--- MC-41551--> Beheerders met beperkte accounts die alleen bevoegdheden op websiteniveau bevatten, kunnen nu een bedrijf maken dat een andere valuta gebruikt dan de website.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce stuurt nu e-mailberichten van het bedrijf van de juiste `from` e-mailadres en bereik. Eerder heeft Adobe Commerce geen rekening gehouden met het bereik van de website bij het verzenden van een bedrijfskrediet of het bijwerken van een e-mail.

### Snelle bestelling

![Probleem opgelost](../assets/fix.svg) <!--- MC-42104--> Het maken van een volgorde met Snelle volgorde vanuit een CSV-bestand werkt nu zoals u verwacht met niet-bestaande SKU&#39;s.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40268--> Het gebruiken van Snelle Orde aan onderzoek op veelvoudige SKUs werkt nu zoals verwacht. Eerder waren er dubbele vermeldingen in de resultaten opgenomen.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40261--> In de weergave van de lijst Toegevoegde producten worden SKU&#39;s die in kleine letters en in hoofdletters zijn ingevoerd, nu op dezelfde manier behandeld als wanneer u SKU&#39;s gebruikt om meerdere producten te selecteren tijdens de Snelle volgorde.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40225--> Met Snelle volgorde voegt u nu producten toe in het aantal dat door de winkelier is opgegeven. Eerder heeft Adobe Commerce slechts één product toegevoegd, zelfs als de door de winkel opgegeven hoeveelheden groter zijn dan één product.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41283--> De functie Volgorde automatisch aanvullen werkt nu met gedeeltelijke SKU&#39;s.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce geeft nu producten weer die zijn geconfigureerd als **Niet afzonderlijk zichtbaar** op de lijst met automatisch suggesties en zoekresultaten van de pagina Snelle bestelling.

![Probleem opgelost](../assets/fix.svg) <!--- MC-42402--> Klanten kunnen nu het formulier Snelle volgorde gebruiken om meerdere producten toe te voegen door SKU&#39;s die hoofdletters bevatten. Eerder werd alleen het eerste product toegevoegd.

### Verhandelbaar aanhalingsteken

![Probleem opgelost](../assets/fix.svg) <!--- MC-41232--> De kopers worden nu omgeleid naar de onderhandelbare aanhalingspagina nadat ze de koppeling naar een onderhandelbaar aanhalingsteken in het URL-veld hebben geplakt en zich met succes hebben aangemeld. Eerder werd de koper doorgestuurd naar de pagina Mijn account.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39317--> Het opnieuw ordenen werkt nu zoals verwacht voor orders die een product met een Aanpasbare Optie Datum voor een klantenrekening bevatten die tijdens het afrekenen werd gecreeerd. Eerder heeft Adobe Commerce het opnieuw ordenen niet verwerkt en deze fout weergegeven: `The product has required options. Enter the options and try again`.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39063--> Het verzendadres voor een verhandelbaar aanhalingsteken kan niet meer worden bewerkt tijdens het afrekenen wanneer de module Inkooporder is uitgeschakeld. Dit gedrag is het resultaat van een vorige correctie waarbij `isQuoteAddressLocked` is verwijderd uit de onderhandelbare renderer voor uitchecken van aanhalingstekens.

![Probleem opgelost](../assets/fix.svg) <!--- MC-38967--> Handelaren kunnen nu producten toevoegen aan een verhandelbaar prijsopgave van de beheerder.

### Aankooporders

![Probleem opgelost](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce geeft nu een informatief foutbericht weer zoals u had verwacht wanneer u een inkooporder plaatst met PayPal Express Checkout wanneer de **[!UICONTROL Name Prefix]** kenmerk is ingesteld op `required`. Eerder heeft Adobe Commerce de bestelling niet geplaatst of een foutbericht weergegeven.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39620--> De UI-component voor het factuuradres in de module Inkooporder gebruikt nu het citaatadres correct wanneer Google Tag Manager is ingeschakeld. Er is eerder een JavaScript-fout opgetreden op de betaalpagina.

### Aanvraaglijsten

![Probleem opgelost](../assets/fix.svg) <!--- MC-40426--> Handelaren kunnen nu de POST gebruiken `rest/all/V1/requisition_lists` eindpunt om een verzoeklijst voor een klant tot stand te brengen. Eerder heeft Adobe Commerce deze fout van 400 gegenereerd toen u een aanvraag probeerde te maken: `Could not save Requisition List`.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41123--> De **[!UICONTROL Add to Requisition List]** wordt nu weergegeven voor in voorraad zijnde producten van een winkelwagentje wanneer het winkelwagentje ook producten uit de voorraad bevat. Als een winkelwagentje twee producten bevatte, waarvan er één uit voorraad was, dan was de _[!UICONTROL Add to Requisition List]_de knop is voor geen van beide producten weergegeven.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40877--> U kunt nu de REST API gebruiken om een product aan een aanvraaglijst toe te voegen.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40155--> Aanvraaglijst **[!UICONTROL Latest Activity Date]** waarden voldoen nu aan de landinstelling.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce genereert niet langer een fatale fout wanneer u een bundelproduct bewerkt vanuit een aanvraaglijst.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce geeft nu de juiste productprijs weer wanneer u een product met een aanpasbare optie toevoegt `(File)` aan een verlanglijst van een verzoeklijst. De koppeling naar het geüploade bestand is ook zichtbaar zoals u had verwacht. Eerder gaf Adobe Commerce onjuiste productprijzen weer en werd de koppeling naar het bestand niet weergegeven.

![Probleem opgelost](../assets/fix.svg) <!--- MC-36383--> Producten met een aanpasbare optie `(File)` kan nu vanuit een aanvraaglijst aan een winkelwagentje worden toegevoegd.

### Gedeelde catalogus

![Probleem opgelost](../assets/fix.svg) <!--- MC-40497--> Een beheerder met een rol die beperkt is tot een specifieke website, kan nu een gedeelde catalogus maken, weergeven en bewerken. Eerder gaf Adobe Commerce een fatale fout op toen een beheerder met een beperkte rol probeerde een gedeelde catalogus te creëren.

![Probleem opgelost](../assets/fix.svg) <!--- MC-41337--> Gelaagde navigatieresultaten bevatten nu een nauwkeurige telling van producten met gefilterde kenmerken en kopers kunnen nu meerdere filters toepassen. Eerder kon slechts één filter worden toegepast en gaf Adobe Commerce een onnauwkeurig aantal producten weer in gelaagde navigatie.

![Probleem opgelost](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce geeft nu correct het aantal producten weer in gelaagde navigatiefilters in zoekresultaten. Eerder gebruikte een insteekmodule voor de pagina met zoekresultaten geen Elasticsearch, maar werd een nieuwe query naar de database verzonden.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce verwijdert de prijzen niet meer uit de lijst wanneer een handelaar alle producten uit een standaard gedeelde catalogus verwijdert.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39802--> Filters worden nu gefilterd op de huidige categorie en correct weergegeven op alle pagina&#39;s wanneer gedeelde catalogi zijn ingeschakeld. Eerder werden filters alleen voor de huidige pagina verkeerd berekend en niet door de huidige categorie gefilterd.

![Probleem opgelost](../assets/fix.svg) <!--- MC-39522--> De GraphQL `products` de vraag keert niet meer de prijswaaier en de categorie van een product voor producten terug die niet aan een gedeelde catalogus worden toegewezen wanneer de gedeelde catalogus wordt toegelaten. Eerder gaf de query de aggregaties van het product, ook al werd het product zelf niet geretourneerd in de `items` array.

## B2B v1.3.1

*9 februari 2021*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.2.

![Nieuw](../assets/new.svg) Online betalingsmethoden worden nu ondersteund voor inkooporders.

![Probleem opgelost](../assets/fix.svg) Als u een configureerbaar product rechtstreeks vanuit een aanvraaglijst aan het winkelwagentje toevoegt terwijl dit product in een eerdere bestelling werd gebruikt, wordt niet langer een systeemfout geretourneerd.

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft nu het tabblad Vereist mijn goedkeuring correct weer voor inkooporders wanneer een gesplitste databaseconfiguratie wordt geïmplementeerd.

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft nu details weer over bundelproducten en cadeaukaart wanneer u inkooporders bekijkt.

![Probleem opgelost](../assets/fix.svg) Winkelen wordt nu omgeleid zoals u had verwacht nadat u zich hebt aangemeld bij hun account tijdens het bladeren in een winkel waar **[!UICONTROL Website Restriction]** is ingeschakeld en **[!UICONTROL Restriction Mode]** is ingesteld op `Private Sales: Login Only`. Eerder werden kopers omgeleid naar de homepage van de winkel. <!--- MC-38934-->

![Probleem opgelost](../assets/fix.svg) De geschiedenis van de orde laadt nu zoals verwacht in een de rekeningsdashboardpagina van een bedrijfbeheerder in plaatsingen met een B2B bedrijfshiërarchie die vele klanten (groter dan 13000) bevat. Eerder werd de volgorde van de historie traag of helemaal niet geladen en gaf Adobe Commerce een fout van 503 weer. <!--- MC-38830-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft niet langer meerdere identieke waarschuwingsberichten weer wanneer u een niet-geconfigureerd product met aanpasbare opties toevoegt aan een lijst met aanvragen van een categoriepagina. <!--- MC-38342-->

![Probleem opgelost](../assets/fix.svg) Nieuwe en gedupliceerde producten zijn nu zichtbaar zoals op de categoriepagina wordt verwacht wanneer gedeelde B2B-catalogi zijn ingeschakeld. <!--- MC-38307-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce handhaaft nu het juiste `store_id` dat met een bedrijfbeheerder wordt geassocieerd wanneer de klantengroep voor een bedrijf wordt bijgewerkt. Eerder `store_id` gewijzigd in de standaardwinkel toen de groep werd bijgewerkt. <!--- MC-38196-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce slaat nu een gegroepeerd product op een aanvraaglijst op als een lijst met eenvoudige producten, net zoals het een gegroepeerd product aan een winkelwagentje toevoegt. Als gevolg van de manier waarop Adobe Commerce gegroepeerde producten heeft opgeslagen, werd de koppeling voor een gegroepeerd product in de aanvraaglijst altijd doorgestuurd naar eenvoudige producten en niet naar het gegroepeerde product. <!--- MC-38049-->

![Probleem opgelost](../assets/fix.svg) U kunt nu orders filteren op **[!UICONTROL Company Name]** veld bij het exporteren van ordergegevens in CSV-indeling. Eerder heeft Adobe Commerce een fout aangemeld `var/export/{file-id}`. <!--- MC-37785-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft nu de pop-up Aanvraaglijst maken weer zoals u had verwacht wanneer u het tabblad Nieuwe lijst met aanvragen maken in de winkel selecteert. <!--- MC-37915-->

![Probleem opgelost](../assets/fix.svg) In de lijst met aanvragen worden nu alle gegroepeerde producten en hoeveelheden opgenomen die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, toonde Adobe Commerce deze fout: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Probleem opgelost](../assets/fix.svg) De juiste archiefweergave is nu gekoppeld aan de relevante website wanneer u een bedrijf maakt in een implementatie op meerdere sites. Eerder kon u geen bedrijf maken en Adobe Commerce gaf deze fout weer: `The store view is not in the associated website`. <!--- MC-37488-->

![Probleem opgelost](../assets/fix.svg) Het bestellen van producten door SKU met behulp van Snelle bestelling leidt niet langer tot dubbele producthoeveelheden in het CSV-bestand. <!--- MC-37427-->

![Probleem opgelost](../assets/fix.svg) De **[!UICONTROL Add to Cart]** de knop wordt niet meer geblokkeerd wanneer de _[!UICONTROL Enter Multiple SKUs]_bevat een lege waarde. In plaats daarvan geeft Adobe Commerce nu een bericht weer waarin u wordt gevraagd geldige SKU&#39;s in te voeren. <!--- MC-37387-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft dit bericht nu weer op de productpagina wanneer u een productoverzicht vanuit een aanvraaglijst verzendt: `You submitted your review for moderation`. De revisie wordt ook weergegeven op de pagina Revisies in behandeling (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Hoewel Adobe Commerce de revisie eerder heeft toegevoegd aan de lijst van lopende recensies, heeft het een fout van 404 op de productpagina geplaatst. <!--- MC-37119-->

![Probleem opgelost](../assets/fix.svg) De prestaties van de `sharedCatalogUpdateCategoryPermissions` de consument is verbeterd . Na het creëren van een gedeelde catalogus, gebruikt de indexator van de catalogustoestemming nu slechts identiteitskaart van de klantengroep van de gedeelde catalogus, niet alle klantengroepen. <!--- MC-36770-->

![Probleem opgelost](../assets/fix.svg) De gebieden van het de adresattribuut van de klant van de douane die met het niet-standaardadres van een verkoopster worden geassocieerd worden nu bewaard zoals verwacht in de storefront controlewerkschema. <!--- MC-36630-->

![Probleem opgelost](../assets/fix.svg) Bestellingen voor producten die behoren tot de standaard gedeelde catalogus van een winkel, kunnen nu voor kopers worden geplaatst via de API voor REST Admin (`rest/V1/carts/{<CART_ID>/items`) zoals verwacht. Adobe Commerce controleert nu of het product is toegewezen aan een openbare catalogus voordat de rechten voor gedeelde catalogi zijn gevalideerd in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Eerder heeft Adobe Commerce het product niet aan de winkelwagentje toegevoegd en deze fout veroorzaakt: `No such shared catalog entity`. <!--- MC-36535-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce stuurt nu e-mails met gebruikersregistratie voor nieuwe bedrijven via het adres van de Adobe Commerce-winkel. Eerder werd deze e-mail verzonden van het adres van de bedrijfbeheerder. <!--- MC-36480-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce controleert nu aangepaste kenmerken op duplicatie van gereserveerde namen van bedrijfskenmerken voordat een handelaar een nieuw kenmerk kan opslaan. <!--- MC-36282-->

![Probleem opgelost](../assets/fix.svg) De `credit_history` de vraag keert nu de gespecificeerde kredietgeschiedenis van het bedrijf voor zowel het oorspronkelijk toegewezen bedrag als het gekochte bedrag terug. Eerder heeft deze query een fout geretourneerd.

![Probleem opgelost](../assets/fix.svg) De **[!UICONTROL Company]** en  **[!UICONTROL Job Title]** velden op de pagina Accountgegevens bewerken kunnen niet meer worden bewerkt.

### Bekende problemen

- B2B-kopers kunnen online betalingsmethoden gebruiken om de gebruikelijke inkooporderstroom te omzeilen. Dit scenario kan zich voordoen als de koper zijn volledige afhandelingstotaal tot 0 kan terugbrengen — bijvoorbeeld door een promotiecode of een cadeaukaart — en vervolgens de code of geschenkkaart kan verwijderen. Zelfs onder deze omstandigheden plaatst Adobe Commerce nog steeds de order voor het juiste bedrag op basis van de prijzen van de items in de toegewezen catalogus. **_Workaround_**: Schakel cadeaukaarten en couponcodes uit als de online betalingsmethoden zijn ingeschakeld voor goedkeuring van inkooporders. <!--- B2B-1603-->

- Kopers worden omgeleid naar het winkelwagentje wanneer ze via PayPal Express Checkout een bestelling proberen te plaatsen bij een inkooporder wanneer **[!UICONTROL In-Context Mode]** is uitgeschakeld. <!--- B2B-1604-->

- Adobe Commerce geeft soms een fout van 404 weer wanneer een koper een inkooporder maakt en vervolgens naar de afhandelingspagina navigeert. Deze fout treedt op wanneer een koper eerder een andere inkooporder met een online betalingsmethode heeft gemaakt voordat hij naar de betalingspagina navigeert zonder de vorige aankoop te voltooien. De koper kan de kooporder nog steeds plaatsen. **_Omzetten_**: Geen. <!--- B2B-1605-->

- Kortingen voor een specifieke betalingsmethode blijven bestaan tijdens afhandeling voor een inkooporder, zelfs als de koper zijn betalingsmethode wijzigt tijdens de laatste afhandeling. Als gevolg hiervan kunnen klanten een korting ontvangen waarop ze geen recht hebben. Deze kwestie doet zich voor omdat ondanks de wijziging in de betalingsmethode nog steeds een kartregel voor de oorspronkelijke betalingsmethode wordt toegepast. **_Omzetten_**: Geen. Zie de [Bekende uitgave van Adobe Commerce 2.4.2 B2B: kortingen voor online inkooporders na wijziging van de betalingsmethode](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Kennisbank_ artikel. <!-- B2B-1012 -->

- De `deleteRequisitionListOutput` De vraag keert details over de geschrapte vraaglijst in plaats van de resterende vraaglijsten terug. <!--- MC-39894-->

## B2B v1.3.0

*15 oktober 2020*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

Deze release bevat verbeteringen voor goedkeuringen voor bestellingen, verzendmethoden, winkelwagentje en registratie van beheeracties.

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.1.

![Nieuw](../assets/new.svg) B2B-ordergoedkeuringen zijn verbeterd om de bruikbaarheid te verbeteren en om acties in bulk voor inkooporders mogelijk te maken.

![Nieuw](../assets/new.svg) B2B-handelaren kunnen nu de verzendmethoden controleren die aan elk bedrijf worden aangeboden.<!--- BUNDLE-160 161 162 -->

![Nieuw](../assets/new.svg) Handelaren kunnen gebruikers nu toestaan de inhoud van hun winkelwagentje in één handeling te wissen en kunnen deze mogelijkheid onafhankelijk op elke website configureren <!--- BUNDLE-108 -->

![Nieuw](../assets/new.svg) B2B-kopers kunnen nu afzonderlijke objecten of de volledige inhoud van hun winkelwagentje rechtstreeks aan een aanvraaglijst toevoegen. <!--- BUNDLE-145 144-->

![Nieuw](../assets/new.svg) B2B-handelaren kunnen namens klanten via Betaling op rekening als betalingsmethode orders van de beheerder maken. <!--- BUNDLE-166 178-->

![Nieuw](../assets/new.svg) Handelaars kunnen nu rechtstreeks alle aanhalingstekens die aan een gebruiker zijn gekoppeld, weergeven op de detailpagina van de klant. <!--- BUNDLE-139 -->

![Nieuw](../assets/new.svg) Merchants kunnen nu het Online net van Klanten nu door Bedrijf filtreren. <!--- BUNDLE-137 -->

![Nieuw](../assets/new.svg) Beheerders kunnen klanten in de Admin nu filteren op Verkoopvertegenwoordiger. <!--- BUNDLE-110 -->

![Nieuw](../assets/new.svg) Om het creëren van frauduleuze of spamrekeningen te verminderen, kunnen de handelaars nu Google reCAPTCHA op het Nieuwe formulier van het Verzoek van het Bedrijf op de winkel toelaten. <!--- BUNDLE-154 -->

![Nieuw](../assets/new.svg) De acties Admin die in de modules van het Bedrijf worden genomen worden nu het programma geopend het Logboek van Acties Admin. De acties worden geregistreerd van alle relevante bedrijfsmodules: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft de **[!UICONTROL Delete customer]** op de knop **Klanten** pagina wanneer de het programma geopende beheerder geen rechten heeft om klanten in plaatsingen te schrappen waar B2B geïnstalleerd is. <!--- MC-35655-->

![Probleem opgelost](../assets/fix.svg) De groep van de klant wordt niet meer automatisch veranderd voor een klant die aan een Bedrijf wordt toegewezen wanneer u de klant op het net van de Klant uitgeeft. <!--- MC-35254-->

![Probleem opgelost](../assets/fix.svg) Wanneer een handelaar een gedeelde catalogus maakt, worden de machtigingen nu automatisch ingesteld op `Allow` voor de **[!UICONTROL Display Product Prices]** en **[!UICONTROL Add to Cart]** functies in categorieën wanneer aan de klantengroep deze toegang wordt toegewezen in de instellingen voor catalogusmachtigingen. Eerder werden deze instellingen automatisch ingesteld op `Deny` zelfs wanneer catalogusmachtigingen zijn ingesteld op `Allow`.<!--- MC-34792-->

![Probleem opgelost](../assets/fix.svg) Machtigingen voor gedeelde cataloguscategorieën worden niet meer overschreven wanneer een product wordt bewerkt vanaf de pagina voor productbewerking.<!--- MC-34777-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce verzendt nu een e-mailbericht waarin wordt bevestigd dat een klant toestemming heeft om de aangewezen kredietlimiet te overschrijden wanneer een handelaar de **[!UICONTROL Allow To Exceed Credit Limit]** instellen. Eerder gaf het e-mailbericht van Adobe Commerce aan dat de klant geen toestemming had om de limiet te overschrijden. <!--- MC-34584-->

![Probleem opgelost](../assets/fix.svg) De container van de HTML die productprijs op verzoeklijsten omringt wordt nu correct teruggegeven voor de kinderen van gebundelde producten. <!--- MC-36331-->

![Probleem opgelost](../assets/fix.svg) Handelaars kunnen nu de taal aanwijzen waarin de e-mail van de bedrijfgebruiker wordt verzonden wanneer het creëren van een bedrijf in meertalige plaatsingen. Eerder, laat het drop-down menu verkopers toe om de aangewezen opslagmening te selecteren en de taal werd niet getoond.  <!--- MC-35777-->

![Probleem opgelost](../assets/fix.svg) De gebieden van de attributen van het klantenadres van de douane worden nu getoond zoals verwacht in de storefront controlewerkschema. <!--- MC-35607-->

![Probleem opgelost](../assets/fix.svg) Het tabblad Configuratie B2B-functies wordt nu correct geopend. <!--- MC-35458-->Gasten kunnen nu QuickOrder gebruiken om producten aan hun winkelwagentje toe te voegen en vervolgens items te verwijderen. Eerder, toen een verkoopster QuickOrder gebruikte om veelvoudige producten aan hun kar toe te voegen, en dan een product te verwijderen, werd het product niet verwijderd. <!--- MC-35327-->

![Probleem opgelost](../assets/fix.svg) Een bedrijf kan nu worden bijgewerkt met de REST API-PUT `/V1/company/:companyId` verzoek zonder het specificeren van `region_id` wanneer de staat wordt gevormd zoals **niet vereist**. Voorheen, hoewel `region_id` Adobe Commerce heeft een fout gegenereerd als deze niet is opgegeven. <!--- MC-35304-->

![Probleem opgelost](../assets/fix.svg) Wanneer u een B2B-bedrijf maakt of bijwerkt met de REST API (`http://magento.local/rest/V1/company/2`, waarbij `2` staat voor de bedrijfs-id), bevat het antwoord nu de instellingen voor `applicable_payment_method` of `available_payment_methods` zoals verwacht. <!--- MC-35248-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce geeft niet langer een pagina van 404 weer wanneer een handelaar de **Enter** in plaats van op de knop **[!UICONTROL Save]** wanneer u een aanvraaglijst in de winkel maakt.<!--- MC-35094-->

![Probleem opgelost](../assets/fix.svg) Categoriemachtigingen worden niet meer gewijzigd wanneer een nieuw product wordt toegewezen aan een openbare gedeelde catalogus. Eerder werden categorietoestemmingen gedupliceerd. <!--- MC-34386-->

![Probleem opgelost](../assets/fix.svg) De REST API-eindpuntPUT `rest/default/V1/company/{id}`, die wordt gebruikt om bedrijfs-e-mail bij te werken, is niet meer case-sensitive. <!--- MC-34308-->

![Probleem opgelost](../assets/fix.svg) Het onbruikbaar maken van beloningsmodules beïnvloedt niet meer B2B eigenschappen op klantenrekeningen. Eerder, toen de beloningsmodules onbruikbaar werden gemaakt, werden de volgende B2B-verwante lusjes niet getoond: Het Profiel van het Bedrijf, de Gebruikers van het Bedrijf, en de Rollen en Toestemmingen.<!--- MC-34191-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce gebruikt nu de juiste naam van de afzender in e-mailberichten wanneer er wijzigingen worden aangebracht in bedrijfsaccounts. Eerder, gebruikte Adobe Commerce de algemene naam van de contactafzender die in het standaardwerkingsgebied voor alle e-mails wordt bepaald. <!--- MC-33917-->

![Probleem opgelost](../assets/fix.svg) Het is nu mogelijk om multiShipping-taken uit te voeren voor bestellingen die zowel fysieke als virtuele producten bevatten. <!--- MC-33818-->

![Probleem opgelost](../assets/fix.svg) Handelaren kunnen nu bedrijfsgebruikers maken vanuit de _[!UICONTROL Company Users]_in Mijn Account en Bedrijfsstructuur **[!UICONTROL Access Restriction]**is ingeschakeld en **[!UICONTROL Restriction Mode]**is ingesteld op `Sales: Login Only`. Eerder heeft Adobe Commerce deze fout gegenereerd toen een handelaar een gebruiker probeerde te maken: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce herstelt de standaardklantengroep van een klant niet meer wanneer een klant zijn accountgegevens opslaat. <!--- MC-33554-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce genereert niet langer een fatale fout wanneer een beheerder een klant die een actief winkelwagentje heeft, toewijst aan een klantengroep. <!--- MC-33313-->

![Probleem opgelost](../assets/fix.svg) Adobe Commerce biedt nu een `addToCart` De gebeurtenis DataLayer voor Snelle Orde en de Vergunning maakt een lijst van pagina&#39;s.  <!--- MC-33295-->

![Probleem opgelost](../assets/fix.svg) E-mailberichten die worden verzonden naar verkoopvertegenwoordigers die aan een bedrijf zijn toegewezen, bevatten nu het toegewezen bedrijfslogo. Eerder bevatte het e-mailbericht het standaard LUMA-logo, niet het geüploade bedrijfslogo. <!--- MC-33232-->

![Probleem opgelost](../assets/fix.svg) Een aanvraaglijst bevat nu alle gegroepeerde producten en hoeveelheden die aan de lijst zijn toegevoegd. Eerder, toen een handelaar aan een verzoeklijst navigeerde nadat het toevoegen van producten aan het van een productdetailpagina, toonde Adobe Commerce deze fout: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Probleem opgelost](../assets/fix.svg) De `products` query retourneert nu een nauwkeurige `total_count` veld wanneer gedeelde catalogus is ingeschakeld. <!--- MC-42268-->

![Probleem opgelost](../assets/fix.svg) De Configuratie van het Bedrijf en creëren de pagina&#39;s van het Bedrijf werken nu zoals verwacht nadat u een online verschepende methode onbruikbaar maakt. Er is een verificatie toegevoegd om te voorkomen dat wordt geprobeerd uitgeschakelde Verzendmodules te verwerken. Eerder werd deze fout door Adobe Commerce weergegeven: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Probleem opgelost](../assets/fix.svg) Het geheugenverbruik van de integratietest is verminderd, wat de testprestaties verbetert en de tijd die nodig is voor het voltooien van de test verkort. <!--- AC-266-->

## B2B v1.2.0

*28 juli 2020*

[!BADGE Ondersteund]{type=Informative tooltip="Ondersteund"}

![Nieuw](../assets/new.svg) Extra ondersteuning voor Adobe Commerce 2.4.0.

![Nieuw](../assets/new.svg) Storefront Order Search, met dank voor de bijdrage van Marek Mularczyk van [Divante](https://www.divante.com/) en leden van de gemeenschap.

![Nieuw](../assets/new.svg) Inkooporders worden uitgebreid en herschreven. Ze zijn nu standaard opgenomen in Adobe Commerce.

![Nieuw](../assets/new.svg) Goedkeuringsregels voor inkooporders zijn geïmplementeerd. Met deze regels kunnen gebruikers de workflow voor inkooporders beheren door aankoopregels voor bestellingen te maken.

![Nieuw](../assets/new.svg) Aanmelden als klant is nu standaard opgenomen in Adobe Commerce. Deze eigenschap staat plaatswerknemers toe om klanten bij te staan door zich aan te melden als klant om te zien wat zij zien.

![Probleem opgelost](../assets/fix.svg) Kenmerkaggregaties werken nu correct voor gelaagde navigatie met Elasticsearch

![Probleem opgelost](../assets/fix.svg) Het zoeken naar bestellingen met speciale tekens werkt nu goed.

![Probleem opgelost](../assets/fix.svg) Klik op de knop **[!UICONTROL Clear All]** Met de knop worden nu alle filters uitgevouwen in plaats van samengevouwen.

![Probleem opgelost](../assets/fix.svg) Product-SKU/Naam is nu opgenomen in de samenvatting van het zoekfilter Volgorde.

![Probleem opgelost](../assets/fix.svg) De sorteerindicator wordt nu correct weergegeven in het raster Mijn inkooporders.

![Probleem opgelost](../assets/fix.svg) Nu kunt u slechts eenmaal op de knoppen Goedkeuren, Annuleren, Afwijzen en Inkooporder klikken. Eerder kon u meerdere keren op de knop klikken.

![Probleem opgelost](../assets/fix.svg) De knoppen Aankooporder goedkeuren, Afwijzen, Annuleren en Valideren worden nu correct weergegeven op mobiele apparaten.

![Probleem opgelost](../assets/fix.svg) Eerder werd bij het goedkeuren van een inkooporder met een korting die is verlopen, het volledige bedrag van de order geplaatst en het totaal van de inkooporder niet bijgewerkt. Nu wordt het totaal van de inkooporder bijgewerkt om het juiste totaal weer te geven.

![Probleem opgelost](../assets/fix.svg) Een kwestie werd geïntroduceerd in 2.3.4 waar de attributen van de douaneverlenging niet van het Adres van de Klant aan het Adres van het Citaat zouden worden gekopieerd. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Als B2B is geïnstalleerd, wordt een SQL-fout weergegeven bij het toewijzen van categorieën aan gedeelde catalogi. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Vanwege een onjuiste waarde voor het type variabele kunnen beheerders geen configureerbare producten aan een bestelling toevoegen. De keuzelijst met opties wordt niet gevuld. Deze functie werkt nu goed.

![Probleem opgelost](../assets/fix.svg) Eerder, wanneer het uitgeven van de Toestemmingen van de Categorie voor de niet Gelogde Groep, zou een fout voorkomen wanneer het bewaren van de veranderingen. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Er wordt een correctie toegevoegd waarmee opslagbeheerders producten kunnen toevoegen aan een volgorde die zich niet in de gedeelde catalogus bevindt. Er wordt eerder een foutbericht weergegeven wanneer u een item toevoegt dat zich niet in de catalogus bevindt.

![Probleem opgelost](../assets/fix.svg) Eerder, na het uitvoeren van de opdracht `php bin/magento indexer:set-dimensions-mode catalog_product_price website` en vervolgens probeert een gedeelde catalogus te maken, treedt er een fout op. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Bij het toevoegen van een bedrijf en het toewijzen van de bedrijfsbeheerder aan een niet-standaardwebsite, werd de verkeerde site-id verzonden, wat een fout veroorzaakte. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Eerder, nadat een klant naar een andere klantengroep werd bewogen, toevoegend een product aan een orde gebruikend _Snelle bestelling_ zou mislukken met een fout. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Eerder, toen het proberen om uit te checken gebruikend WebAPI met een citaat B2B, werd een onjuiste waarde verzonden naar API, veroorzakend een fout om voor te komen. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Als u een bedrijf via de API instelt op Actief, treedt er eerder een fout op. Dit probleem is nu opgelost.

![Probleem opgelost](../assets/fix.svg) Als gevolg van een onnodige `form` -tag, wordt de bestelpagina automatisch vernieuwd wanneer u op Enter drukt nadat u de voorgestelde verzendkosten hebt gewijzigd. Dit probleem is opgelost.

![Probleem opgelost](../assets/fix.svg) Er is eerder een fout opgetreden bij het instellen van een weergavelimiet voor een product op een cataloguspagina en die limiet was lager dan het totale aantal producten. Die functie werkt nu zoals u had verwacht.

![Probleem opgelost](../assets/fix.svg) Eerder, wanneer het veranderen van admin van een bedrijf, zou het originele admin adres aan nieuwe admin worden gekopieerd, die hen twee adressen geeft. Nu wordt alleen het juiste adres toegevoegd.

![Probleem opgelost](../assets/fix.svg) Eerder mislukte het gebruik van de API om een aanhalingsteken op te slaan wanneer deze is ingesteld op &quot;Allowed and Notify Customer&quot;. Deze API-aanroep werkt nu zoals u had verwacht.

![Probleem opgelost](../assets/fix.svg) De Vaste productbelasting wordt nu weergegeven op de detailpagina Aanhalingstekens.

![Probleem opgelost](../assets/fix.svg) Als u eerder op een bijlage op het tabblad Opmerkingen van de pagina Mijn aanhalingstekens klikt, kan het bestand niet worden gedownload. Dit gedrag werkt nu zoals verwacht.

### Bekende problemen

- Adobe Commerce genereert een uitzondering tijdens de upgrade naar B2B 1.2.0 in een implementatie voor meerdere websites. Wanneer `setup:upgrade` wordt uitgevoerd, treedt deze fout op in de `PurchaseOrder` module: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Workaround**: Installeer de `B2B-716 Add NonTransactionableInterface` interface aan `InitPurchaseOrderSalesSequence` hotfix voor gegevenspatches, die nu beschikbaar is via de **Mijn account** > **Downloads** deel van `magento.com`.
- Als een kortingscode vervalt voordat een inkooporder (PO) wordt goedgekeurd, blijft de inkooporder het gedisconteerde bedrag weergeven, maar als de inkooporder eenmaal is goedgekeurd, wordt de order geplaatst op het niet-gedisconteerde totaal. **Workaround**: Installeer de `B2B-709 Purchase Order Discount patch` hotfix voor dit probleem, dat nu beschikbaar is via de **Mijn account** > **Downloads** deel van `magento.com`.
- Als de items in een inkooporder niet in voorraad zijn of niet voldoende in voorraad zijn wanneer de inkooporder wordt omgezet in een werkelijke bestelling, treedt er een fout op. Als backorders worden ingeschakeld, wordt de volgorde op de normale wijze verwerkt.
