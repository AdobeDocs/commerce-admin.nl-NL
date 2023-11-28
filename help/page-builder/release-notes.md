---
title: Opmerkingen bij de release [!DNL Page Builder]
description: Lees de opmerkingen bij de release voor meer informatie over alle [!DNL Page Builder] lozingen.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Opmerkingen bij de release voor [!DNL Page Builder]

In deze releaseopmerkingen worden de releases van [!DNL Page Builder] en omvatten:

![Nieuw](../assets/new.svg) Nieuwe functies

![Probleem opgelost](../assets/fix.svg) Oplossingen en verbeteringen

![Bekend probleem](../assets/bug.svg) Bekende problemen

>[!IMPORTANT]
>
>Vanaf de release van 2.4.3, [!DNL Page Builder] is nu beschikbaar als gebundelde uitbreiding in Magento Open Source. Het is nu het standaardhulpmiddel voor het uitgeven van inhoud voor zowel Adobe Commerce als Magento Open Source, en kan de redacteur WYSIWG met om het even welke derde module vervangen.

## 1.7.2. Handel 2.4.5

![Nieuw](../assets/new.svg) **Nieuwe omvattende entiteit - [!DNL Columns] container geïntroduceerd voor kolomlay-outs** - Eerder konden gebruikers alleen kolommen toevoegen binnen een ander container/verpakkingstype, zoals een [!DNL Tab] of [!DNL Row]. Nu, [!DNL Column] heeft een eigen omhulsel en kan rechtstreeks in het werkgebied worden toegevoegd. Ook de [!DNL Columns] container heeft een instellingselement waarin gebruikers configuratie voor deze omsluitende entiteit kunnen opgeven.<!--- PB-500-->

![Nieuw](../assets/new.svg) **Nieuwe menuopties voor het dupliceren, verbergen en verwijderen van kolomgroepen** - Met deze nieuwe opties kunnen gebruikers dupliceren, verbergen en verwijderen [!DNL Columns] groepen — net als bij inhoudstypen.<!--- PB-507-->

![Nieuw](../assets/new.svg) <!-- Issue 594 -->**Nieuwe multiline kolomondersteuning toegevoegd aan kolomgroep** - Met deze toevoeging kunnen gebruikers meerdere regels kolommen binnen één regel manipuleren [!DNL Columns] groeperen om de lay-out van kolommen veel flexibeler te maken.<!--- PB-108-->

Zie [Layout - kolom](./column.md) voor informatie over het gebruik van de nieuwe [!DNL Columns] groep.

## 1.7.1. Handel 2.4.4.

![Probleem opgelost](../assets/fix.svg) Page Builder is nu compatibel met PHP 8.1.<!--- AC-1300-->

![Probleem opgelost](../assets/fix.svg) Handelaren kunnen nu alternatieve tekst toevoegen (`alt_text`) naar afbeeldingen (Afbeelding, Banner, Dia) om de toegankelijkheid van de inhoud te verbeteren.<!--- PB-1193-->

![Probleem opgelost](../assets/fix.svg) Admin-gebruikers met alleen beperkte machtigingen voor Inhoudsbewerking zien niet langer een fout wanneer ze Page Builder gebruiken om een productwidget aan een CMS-pagina toe te voegen. De Bouwer van de pagina toont ook een nauwkeurige producttelling op de widgetmontagespagina. Eerder, vereiste de Bouwer van de Pagina toestemmingen aan de module van de Catalogus wanneer het terugwinnen van het productaantal en toonde deze fout: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Probleem opgelost](../assets/fix.svg) De kwesties van de vertoning met het menu van het Formaat van de Bouwer van de Pagina worden nu opgelost met TinyMCE 5 bibliotheekverbetering. <!--- AC-446-->

![Probleem opgelost](../assets/fix.svg) U kunt nu de muis gebruiken om een **Weer te geven tekst** in het pop-upvenster Koppeling invoegen. <!--- AC-982-->

![Probleem opgelost](../assets/fix.svg) In het optiemenu voor de tekengrootte van de pagina Builder worden nu alle verwachte opties weergegeven. Eerder werden niet alle opties weergegeven. <!--- AC-1056-->

![Probleem opgelost](../assets/fix.svg) De `phpgt/dom` Composerafhankelijkheid voor de `magento/magento2-page-builder` uitbreiding tot de meest recente versies. <!--- magento/magento2-page-builder/pull/779-->

![Probleem opgelost](../assets/fix.svg) De Bouwer van de pagina resizes niet meer de Verbinding van het Tussenvoegsel en de dialoog van het Beeld van het Tussenvoegsel wanneer het tonen van de schuif in een kleine kolom. <!--- AC-973-->

![Probleem opgelost](../assets/fix.svg) Het menu Tabeleigenschappen van Page Builder wordt nu naar behoren weergegeven. <!--- AC-407-->

![Probleem opgelost](../assets/fix.svg) De punten van de schuif worden niet meer getoond op de verbinding van het Tussenvoegsel of beeld modaal wanneer de muis niet over de schuif beweegt. <!--- AC-406-->

![Probleem opgelost](../assets/fix.svg) De tekengrootte die wordt gebruikt om de opties in het menu Tabel weer te geven, is geoptimaliseerd. <!--- AC-396-->

![Probleem opgelost](../assets/fix.svg) Correctie van anomalieën bij de plaatsing van de dialoogvensters Afbeelding invoegen/bewerken en Koppeling invoegen/bewerken. <!--- AC-397-->

![Probleem opgelost](../assets/fix.svg) Page Builder genereert niet langer een fout wanneer u op **Teksteditor** voor een banner. <!--- AC-398-->

![Probleem opgelost](../assets/fix.svg) De Bouwer van de pagina zet niet meer alle dynamische blokken in één taal tijdens verbetering om. <!--- MC-42265-->

## 1.6.0 voor Adobe Commerce 2.4.2

![Nieuw](../assets/new.svg) <!-- Issue 558 -->**Nieuw [!DNL Page Builder] stijl** - [!DNL Page Builder] er zijn enorme verbeteringen aangebracht in de manier waarop inhoud wordt opgemaakt. Door de wijzigingen kunt u nu eenvoudig eenvoudige CSS-kiezers maken die de bestaande stijlen voor inhoudstypen overschrijven. Deze wijzigingen maken het mogelijk om [!DNL Page Builder] thema&#39;s met een rijke reactiesnelheid voor alle inhoudstypen.

![Nieuw](../assets/new.svg) <!-- Issue 429 -->**Rijcontainer is nu optioneel** - U kunt nu inhoud maken in [!DNL Page Builder] zonder dat een rijcontainer nodig is. Naast de rij kunnen nu de volgende inhoudstypen rechtstreeks in het werkgebied worden gesleept en neergezet: HTML, Blok, Dynamisch blok, Kolommen en Tabs.

![Nieuw](../assets/new.svg) <!-- Issue 636 -->**Nieuwe responsieve viewport-switch** - U kunt nu een voorvertoning van uw [!DNL Page Builder] inhoud op verschillende apparaatbreedten (onderbrekingspunten) met de nieuwe knoppen voor viewport van Admin boven het werkgebied. De viewport schakelaar simuleert hoe uw inhoud wanneer getoond op de storefront wanneer verschillende apparaten wordt gestileerd.

![Nieuw](../assets/new.svg) <!-- Issue 637 -->**Nieuwe brainstormspecifieke formuliervelden** - U kunt nu waarden voor inhoudsveldtypen instellen op specifieke viewport-onderbrekingspunten. Pictogramindicatoren naast de velden geven de viewport weer waarop de veldwaarde van het inhoudstype wordt toegepast.

![Nieuw](../assets/new.svg) <!-- Issue 559 -->**Vooraf gedefinieerde formuliervelditems zijn verwijderd** - Geavanceerde formulierinstellingen voor marges, opvullingen en eigenschappen die betrekking hebben op randen (rand, randbreedte en randstraal) zijn nu ingesteld als `default`, zodat waarden kunnen worden gedefinieerd door de CSS van een module.

![Nieuw](../assets/new.svg) <!-- Issue 635, 557,  -->**Tussenruimte werkgebied toegevoegd** - Rijen en kolommen beschikken nu over extra ruimte rond inhoudssoorten in het werkgebied, maar niet in de winkel. Door de extra afstand in het werkgebied is het gemakkelijker om toegang te krijgen tot de menu&#39;s van de mouseover-optie voor zowel de container als de ingesloten inhoudstypen.

![Probleem opgelost](../assets/fix.svg) <!-- MC-37348 -->**Automatisch schuiven naar revisies is nu opgelost** - Automatisch schuiven naar productreeksen op de winkel is nu opgelost.

![Probleem opgelost](../assets/fix.svg) <!-- MC-36227 -->**Vaste bijgesneden inhoud** - De categorie Lengte en de productomschrijvingen worden niet meer bijgesneden.

![Probleem opgelost](../assets/fix.svg) <!-- MC-35402 -->**Vaste inhoud van volledige afloopcategorie met volledige breedte** - Rubriekinhoud kan nu worden weergegeven in een lay-out met volledige breedte of volledige afloopbreedte.

![Probleem opgelost](../assets/fix.svg) <!-- MC-37989 -->**Verbeterde beveiliging**

## 1.5.1 voor Adobe Commerce 2.4.1-p1

![Probleem opgelost](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Foutweergave** - Oplossing voor een probleem waarbij [!DNL Page Builder] er is een fout weergegeven bij het toevoegen van subcategorieën van Catalog in Admin.

## 1.5.0 voor Adobe Commerce 2.4.1

![Nieuw](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Overweldigende, volledige schermbewerking** - Bewerken [!DNL Page Builder] de inhoud is nu alleen op volledig scherm beschikbaar voor alle gebieden die worden beheerd door [!DNL Page Builder]. Deze wijziging omvat CMS-pagina&#39;s, product- en categoriepagina&#39;s, blokken en dynamische blokken. Bij bewerking op volledig scherm krijgt de inhoud de focus en wordt een weergave geboden die beter aansluit bij de gebruikerservaring op de winkel.

![Nieuw](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] voorvertoningen van inhoud **- Standaard, [!DNL Page Builder] biedt nu voorvertoningen van inhoud, niet alleen voor CMS-pagina&#39;s, Blokkeringen en dynamische blokken, maar ook voor product- en categoriepagina&#39;s. U kunt deze functie zo configureren dat deze in- of uitgeschakeld is voor product- en categoriepagina&#39;s met de nieuwe [!DNL Page Builder] Instelling Voorvertoning van inhoud, toegankelijk in de winkelconfiguratie via Inhoudbeheer > Geavanceerde gereedschappen voor inhoud.

![Nieuw](../assets/new.svg) <!-- Issue 543 -->**Verbeterde toegang tot korte productbeschrijvingen** - Standaard wordt nu een korte beschrijving van het product weergegeven vóór de langere beschrijving. Deze wijziging komt overeen met de volgorde waarin ze in de winkel worden weergegeven. Hierdoor is het niet nodig door de langere beschrijvingsinhoud te bladeren om toegang te krijgen tot de korte beschrijving.

![Nieuw](../assets/new.svg) <!-- Issue 419 -->**Geneste koppelingen in banners en dia&#39;s voorkomen** - Door koppelingen toe te voegen naar zowel de inhoud als de buitenste elementen van Banners en dia&#39;s, zijn geneste koppelingen gemaakt die niet correct werden weergegeven of weergegeven op de winkel. Om het probleem op te lossen, kunnen koppelingen niet meer worden toegevoegd aan *beide* het gebied van de Tekst van het Bericht en het attribuut van de Verbinding voor Banners en Dia&#39;s.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 421 --> Het instellen van de lege randstraal op een tabitem leidde tot fouten en brak de inhoud van het tabitem. Dit probleem is nu opgelost.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 422 --> Het toevoegen van bepaalde combinaties van voorwaarden aan het filter Productvoorwaarde leidde tot fouten die het opslaan van het formulier Producten beletten. Dit probleem is nu opgelost.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 425 -->Het inhoudssoort Slider functioneerde niet correct toen de instelling Oneindige lus was uitgeschakeld. Dit probleem is nu opgelost.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 426 -->De minimale geadverteerde prijs is zo vastgesteld dat deze nu werkt in [!DNL Page Builder].

![Probleem opgelost](../assets/fix.svg) <!-- Issue 436 -->Probleem verholpen in Safari en IE 11 waarbij het slepen en neerzetten van een afbeelding naar het uploadgebied in Banners en dia&#39;s werd voorkomen.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 525 -->Correctie van het probleem waarbij niet kon worden gereageerd op het inhoudstype Slider in Firefox.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 567 -->Probleem verholpen waarbij in de widgetconfiguratie onjuiste kiezers werden gemaakt in het DOM voor de verschillende weergaven.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 609 -->Oplossing voor een probleem waarbij de koptekstwerkbalk het optiemenu van het inhoudstype bevatte, waardoor toegang tot het formulier en andere opties niet mogelijk was.

![Probleem opgelost](../assets/fix.svg) <!-- Issue 612, 613 -->Correctie van problemen waarbij Sliders en meerdere rijen die parallax-achtergronden gebruiken, niet correct werden gerenderd nadat de modus Volledig scherm verschillende keren was geschakeld.

![Probleem opgelost](../assets/fix.svg) <!--MC-35220-->Probleem verholpen waarbij het kopiëren van de inhoud van een inhoudssoort Kop naar een inhoudssoort Tekst werd voorkomen [!DNL Page Builder] van opslaan.

![Probleem opgelost](../assets/fix.svg) <!-- MC-34620 -->Probleem verholpen met het inhoudstype Tekst om niet-Latin-1-tekens correct af te handelen en op te slaan.

![Probleem opgelost](../assets/fix.svg) <!-- MC-34679 -->Vast [!DNL Page Builder] CSS-stijlen die ervoor zorgden dat Safari 13.1 het sitemenu van het Luma-thema voor kleine weergavepoorten en mobiele schermen onjuist rendert.

![Probleem opgelost](../assets/fix.svg) <!-- MC-34848 -->Probleem verholpen met het inhoudstype HTML om ingesloten widgets, zoals &quot;Order by SKU&quot;, correct weer te geven op de Storefront.

## 1.4.1 voor Adobe Commerce 2.4.0-p1

![Nieuw](../assets/new.svg) <!-- PB-590 --> Bijgewerkt naar TinyMCE 4. TinyMCE 3 is verwijderd om de beveiliging te verbeteren.

## 1.4.0 voor Adobe Commerce 2.4.0

![Nieuw](../assets/new.svg) <!-- PB-494 -->Toegevoegde ondersteuning voor PHP 7.4.

![Probleem opgelost](../assets/fix.svg) <!-- MC-31247 -->Probleem verholpen waarbij het inhoudstype Producten configureerbare producten niet weergaf toen de voorwaarde op prijs werd ingesteld.

![Probleem opgelost](../assets/fix.svg) <!-- PB-179 -->Probleem verholpen met de configuratie voor productuitlijning zodat alleen de productcontainer zelf wordt geplaatst, niet de inhoud van de productcontainer, zoals de productnaam, prijs, knoppen, afbeeldingen en andere elementen.

![Probleem opgelost](../assets/fix.svg) <!-- MC-33556 -->Prestatieverbeteringen.

![Probleem opgelost](../assets/fix.svg) Verbeterde beveiliging.

## 1.3.3-p1 voor Adobe Commerce 2.3.6-p1

![Probleem opgelost](../assets/fix.svg) Verbeterde beveiliging.

## 1.3.3 voor Adobe Commerce 2.3.6

![Probleem opgelost](../assets/fix.svg) <!-- MC-32766 -->Probleem verholpen met het inhoudstype Tekst om de aan HTML-kenmerken toegevoegde variabelerichtlijnen correct op te slaan.

![Probleem opgelost](../assets/fix.svg) <!-- MC-34590 -->Probleem verholpen met het inhoudstype Tekst om niet-Latin-1-tekens correct af te handelen en op te slaan.

![Probleem opgelost](../assets/fix.svg) <!-- MC-34677 -->Vast [!DNL Page Builder] CSS-stijlen die ervoor zorgden dat Safari 13.1 het sitemenu van het Luma-thema voor kleine weergavepoorten en mobiele schermen onjuist rendert.

![Probleem opgelost](../assets/fix.svg) <!-- MC-34846 -->Het inhoudssoort HTML is gecorrigeerd voor het correct weergeven van ingesloten widgets, zoals _Bestelling door SKU_ op de opslagplaats.

![Probleem opgelost](../assets/fix.svg) Probleem verholpen waardoor gebruikers soms geen inhoudsformulieren konden opslaan. De fout (&quot;[!DNL Page Builder] rendeert 5 seconden zonder vergrendelingen vrij te geven&quot;), werd het loader-pictogram oneindig weergegeven nadat werd geprobeerd een formulier op te slaan.

## 1.3.2 voor Adobe Commerce 2.3.5-p2

![Nieuw](../assets/new.svg) Verbeterde beveiliging.

## 1.3.1 voor Adobe Commerce 2.3.5-p1

Deze versie van [!DNL Page Builder] is slechts een versie-nummer update voor Adobe Commerce 2.3.5-p1. Alle functies die worden beschreven voor versie 1.3.0 zijn ook van toepassing op deze versie.

## 1.3.0 voor Adobe Commerce 2.3.5

![Nieuw](../assets/new.svg) **Sjablonen** - [!DNL Page Builder] heeft nu sjablonen die kunnen worden gemaakt op basis van bestaande inhoud en die kunnen worden toegepast op nieuwe inhoudsgebieden. [!DNL Page Builder] in sjablonen worden zowel de inhoud als de lay-outs van bestaande pagina&#39;s, blokken, dynamische blokken, productkenmerken en categorierendingen opgeslagen. U kunt bijvoorbeeld een bestaande [!DNL Page Builder] CMS-pagina als een sjabloon en pas die sjabloon vervolgens toe (met alle inhoud en lay-outs) om snel CMS-pagina&#39;s voor uw site te maken. Deze nieuwe functie wordt hier beschreven: [Sjablonen](templates.md).

![Nieuw](../assets/new.svg) **Videoachtergronden voor rijen, banners en schuifregelaars** - [!DNL Page Builder] Rijen, banners en schuifregelaars kunnen nu video&#39;s gebruiken voor hun achtergronden. Deze nieuwe functies worden hier beschreven: [Rijen](row.md), [Banners](banner.md), [Schuifregelaars](slider.md).

![Nieuw](../assets/new.svg) **Verbeteringen en toevoegingen voor videoondersteuning** - [!DNL Page Builder] ondersteunt nu een groter aantal verschillende video-indelingen. Naast YouTube- en Vimeo-video&#39;s ondersteunen het inhoudstype Video en de videoachtergronden nu video-URL-koppelingen naar video-indelingen, zoals `.mp4` en andere browserondersteunde indelingen. Het inhoudstype Video voegt ook een automatisch afspeelbare functie toe. Deze nieuwe functies worden hier beschreven: [Type video-inhoud](video.md).

![Nieuw](../assets/new.svg) **Rijen, banners en schuifregelaars op volledige hoogte** - [!DNL Page Builder] Rijen, banners en schuifregelaars kunnen hun hoogten nu instellen op de volledige hoogte van de pagina met een getal met een CSS-eenheid (px, %, vh, em) of een berekening tussen eenheden (100vh - 237px). Deze nieuwe functies worden hier beschreven: [Rijen](row.md), [Banners](banner.md), [Schuifregelaars](slider.md).

![Nieuw](../assets/new.svg) **Bijwaardebibliotheek voor inhoudstype** - Ontwikkelaars kunnen nu versies maken van [!DNL Page Builder] inhoudstypen zonder dat dit leidt tot incompatibele problemen met eerdere versies. Vóór deze release zouden belangrijke wijzigingen in configuraties van inhoudstypen problemen met weergave en gegevensverlies veroorzaken bij eerder opgeslagen [!DNL Page Builder] inhoudstypen. Deze problemen worden verwijderd door de nieuwe upgradebibliotheek. De bibliotheek wordt ontworpen om vorige versies van inhoudstypes te bevorderen die aan het gegevensbestand worden opgeslagen zodat zij de configuratieveranderingen in de nieuwe versies aanpassen. [!DNL Page Builder] voert de verbeteringsbibliotheek op inheemse inhoudstypes uit zoals nodig voor een nieuwe versie. Deze wijziging zorgt ervoor dat de ingebouwde [!DNL Page Builder] inhoudstypen worden altijd bijgewerkt zodat ze overeenkomen met eventuele wijzigingen die worden aangebracht in inhoudssoorten voor een nieuwere versie.

>[!IMPORTANT]
>
>Als u extra database-entiteiten hebt gemaakt voor opslag [!DNL Page Builder] inhoud, u _moet_ Voeg die entiteiten toe aan uw `etc/di.xml`. Als u dat niet doet, [!DNL Page Builder] inhoud die in uw entiteit is opgeslagen, wordt niet bijgewerkt, waardoor er mogelijk gegevens verloren gaan en weergaveproblemen optreden. Als u bijvoorbeeld een blogentiteit hebt gemaakt die [!DNL Page Builder] inhoud, moet u uw blogentiteit aan uw `etc/di.xml` bestand als een `UpgradableEntitiesPool` type zodat de upgradebibliotheek het dialoogvenster [!DNL Page Builder] inhoudstypen die in uw blog worden gebruikt. Zie voor meer informatie en instructies over het gebruik van de upgradebibliotheek [Typen inhoud upgraden](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) in de _Page Builder Developer Guide_.

![Nieuw](../assets/new.svg) **Documentatie voor het toevoegen van nieuwe weergaven** - Informatie over ontwikkelaars is nu gepubliceerd over [weergave toevoegen](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) voor bestaande of aangepaste inhoudstypen.

![Probleem opgelost](../assets/fix.svg) **Verschillende correcties**

- <!-- PB-50 -->Probleem verholpen waarbij het TinyMCE-menu voor dia-inhoud onder andere inhoudstypen werd weergegeven als de bovenliggende container van de dia is gedupliceerd.
- <!-- PB-166 -->Bijgewerkt [!DNL Page Builder] om een vernietigingsmethode uit te voeren om geheugenlekken in sommige scenario&#39;s te verhinderen.
- <!-- PB-170 -->Verbeterde TinyMCE-prestaties wanneer meerdere instanties in het beheerwerkgebied worden gebruikt.
- <!-- PB-252 -->Probleem verholpen waarbij het inhoudstype Dynamisch blok niet wordt gerenderd in het beheerwerkgebied als de bovenste rij is gemarkeerd als verborgen.
- <!-- PB-273 -->Verfijnde muis-hover gebeurtenissen op het Admin stadium door een vertraging van 200 ms uit diverse controles UI te verwijderen. Door deze wijziging kunt u gemakkelijker werken met geneste inhoudsitems in het werkgebied.
- <!-- PB-294 -->Probleem verholpen waarbij het valutasymbool onjuist werd beschermd in de productlijstwidget in het blok/dynamisch blok in het beheerstadium.
- <!-- PB-296 -->Probleem verholpen waarbij het product totaal was voor de [!DNL Page Builder] Het bewerkingspaneel werkt niet voor aangepaste MSI-voorraadproducten.
- <!-- PB-317 -->Oplossing voor een probleem waarbij opslaan [!DNL Page Builder] inhoud met achtergrondafbeeldingen op Microsoft Edge geeft deze afbeeldingen niet weer op de winkelvoorgrond.
- <!-- PB-390 -->Correctie van een probleem waarbij geneste [!DNL Page Builder] inhoud kan niet worden opgeslagen als gebruikers op de knop Opslaan klikken voordat de pagina volledig wordt weergegeven.
- <!-- PB-418 -->Fout met betrekking tot vaste uitzondering die wordt gegenereerd in snijtaken vanwege [!DNL Page Builder] analytische gegevens.

## 1.2.2 voor Adobe Commerce 2.3.4-p2

![Nieuw](../assets/new.svg) Verbeterde beveiliging.

## 1.2.1 voor Adobe Commerce 2.3.4-p1

![Nieuw](../assets/new.svg) Verbeterde beveiliging.

## 1.2.0 voor Adobe Commerce 2.3.4

![Nieuw](../assets/new.svg)  **[!DNL Page Builder]integratie met PWA Studio** - Toegevoegd [!DNL Page Builder] inhoud renderen naar de Venia-app in PWA Studio. [!DNL Page Builder] inhoud kan nu worden weergegeven in de app PWA Studio Venia. Zie de [!DNL Page Builder] documentatie binnen [PWA Studio] voor alle informatie over deze nieuwe functie.

![Nieuw](../assets/new.svg) **Toegevoegde productcarrousel** - <!-- PB-77, PB-173, PB-175 -->Het inhoudstype Producten biedt nu een optie om uw producten weer te geven in carrousel-/schuifvorm, inclusief verschillende opties om de carrousel aan uw wensen aan te passen.

![Nieuw](../assets/new.svg) **Toegevoegde product-SKU-sortering** - <!-- PB-69 -->Het inhoudstype van Producten verstrekt nu een optie om uw producten door SKU in de orde te sorteren u hen aan een lijst binnen Admin toevoegt.

![Nieuw](../assets/new.svg) **Sorteren in toegevoegde productcategorie** - <!-- PB-181 -->. Het inhoudstype Producten biedt nu een optie om uw producten op categorie te sorteren _positie_, waarbij ze in dezelfde volgorde worden weergegeven als in de handelscatalogus.

![Nieuw](../assets/new.svg) **Totaal toegevoegde productselectie** - <!-- PB-107 -->. Het inhoudstype Admin van Producten uitgeeft nu het totale aantal producten die uw opties van de productselectie aanpassen.

![Probleem opgelost](../assets/fix.svg) **Verschillende correcties**

- <!-- PB-237 -->Verbeterde beveiliging.
- <!-- PB-41 -->Vaste zoekopdrachten binnen UI selecteren componenten om slechts één AJAX verzoek per zoekterm in te dienen.
- <!-- PB-76, PB-84-->Bijgewerkte productvoorvertoningen in de Admin die overeenkomen met de winkel, inclusief de sterrenwaardering, kleur en grootteopties van het product, indien van toepassing.
- <!-- PB-169 -->Probleem verholpen waarbij [!DNL Page Builder] kan niet worden opgeslagen als JavaScript-miniatuur en -bundeling zijn ingeschakeld in de handelfunctie.
- <!-- PB-241 -->Oplossing voor de voorvertoningen Admin van Producten, Blokken, en Dynamische Blokken om correct op de installaties van de Handel terug te geven die verschillende URLs voor Admin en frontend bepalen.
- <!-- PB-238 -->Oplossing voor de voorvertoningen van Admin van Producten, Blokken, en Dynamische Blokken om correct op de installaties van de Handel met B2B terug te geven die met B2B worden geïnstalleerd met _Alleen aanmelden_ optie ingeschakeld. Voordat deze correctie wordt uitgevoerd, wordt [!DNL Page Builder] Als u deze voorvertoning bekijkt, wordt de pagina omgeleid naar de aanmeldingsnaam van de klantenaccount.
- <!-- PB-239 -->Oplossing voor een sessiefout die kan optreden wanneer een voorvertoning van een grote pagina wordt weergegeven in het dialoogvenster [!DNL Page Builder] Admin.
- <!-- PB-248 -->Bijgewerkt [!DNL Page Builder] Minder stijlen om overlapping met storefront-stijlen te voorkomen.

## 1.1.1 voor Adobe Commerce 2.3.3-p1

![Nieuw](../assets/new.svg) Verbeterde beveiliging.

## 1.1.0 voor Adobe Commerce 2.3.3

![Nieuw](../assets/new.svg) <!-- MC-15250 -->Expliciet sorteren van producten toegevoegd aan het inhoudstype Producten.

![Nieuw](../assets/new.svg) <!-- MC-17823 -->Knoppen toegevoegd voor het invoegen van afbeeldingen, widgets en variabelen in het inhoudstype HTML.

![Probleem opgelost](../assets/fix.svg) Verbeterd [!DNL Page Builder] beveiliging.

![Probleem opgelost](../assets/fix.svg) <!-- MC-1805 -->Bijgewerkt [!DNL Page Builder] om PHP versie 7.3 te ondersteunen.

![Probleem opgelost](../assets/fix.svg) <!-- MC-4137 -->Bijgewerkt TinyMCE naar versie 4.9.5. Deze update verhelpt samen met de extra verbeteringen verschillende problemen met de inline TinyMCE-editor:

- De variabelen, de beelden, en de beeldverbindingen worden toegevoegd waar de curseur wordt geplaatst.
- Tabellen en tabelcellen kunnen worden gecentreerd.
- Met Kopiëren/plakken plakt u nu inhoud op de cursorpositie.
- Koppelingen kunnen worden toegepast op geselecteerde tekst.
- Opsommingstekens worden correct uitgelijnd.
- Wijzigingen in de inline editor kunnen worden opgeslagen zonder eerst buiten de editor te klikken.

![Probleem opgelost](../assets/fix.svg) <!-- MC-3880 -->Probleem verholpen waarbij de minimale hoogte en de verticale uitlijning niet consistent waren tussen de secties in het bewerkingspaneel voor elk inhoudstype.

![Probleem opgelost](../assets/fix.svg) <!-- MC-14994 -->Probleem verholpen waarbij de werkbalk van het inhoudstype Kop verkeerd werd geplaatst toen deze voor het eerst in het werkgebied werd neergezet.

![Probleem opgelost](../assets/fix.svg) <!-- MC-15742 -->Correctie van marges met harde codes in zowel de inhoudstypen Slider als Video.

![Probleem opgelost](../assets/fix.svg) <!-- MC-16241 -->Probleem verholpen waarbij het vereiste sterretje tweemaal werd weergegeven op formuliervelden.

## 1.0.3 voor Adobe Commerce 2.3.2-p2

![Nieuw](../assets/new.svg) Verbeterde beveiliging.

## 1.0.2 voor Adobe Commerce 2.3.2-p1

![Nieuw](../assets/new.svg) Verbeterde beveiliging.

## 1.0.1 voor Adobe Commerce 2.3.2

![Nieuw](../assets/new.svg) Zorgt voor compatibiliteit met Adobe Commerce 2.3.2.

## 1.0.0 voor Adobe Commerce 2.3.1

![Nieuw](../assets/new.svg) Algemene beschikbaarheidsrelease


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
