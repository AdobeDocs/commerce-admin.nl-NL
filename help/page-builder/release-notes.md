---
title: Opmerkingen bij de release voor  [!DNL Page Builder]
description: Herzie de versienota's voor informatie over alle  [!DNL Page Builder]  versies.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Opmerkingen bij de release voor [!DNL Page Builder]

Deze releaseopmerkingen beschrijven de releases van [!DNL Page Builder] en bevatten:

![ Nieuwe ](../assets/new.svg) Nieuwe eigenschappen

![ Vaste kwestie ](../assets/fix.svg) Oplossingen en verbeteringen

![ Bekende kwestie ](../assets/bug.svg) Bekende kwesties

>[!IMPORTANT]
>
>Vanaf de release 2.4.3 is [!DNL Page Builder] nu beschikbaar als een gebundelde extensie in de Magento Open Source. Het is nu het standaardhulpmiddel voor het uitgeven van inhoud voor zowel Adobe Commerce als Magento Open Source, en kan de redacteur WYSIWG met om het even welke derde module vervangen.

## 1.7.2 voor Commerce 2.4.5

![ Nieuwe ](../assets/new.svg) **Nieuwe omslagentiteit - [!DNL Columns] container die voor kolomlay-outs** wordt geïntroduceerd - eerder, konden de gebruikers kolommen slechts binnen een andere container/omslag inhoudstype, zoals a [!DNL Tab] of [!DNL Row] toevoegen. De [!DNL Column] heeft nu een eigen wrapper en kan direct in het werkgebied worden toegevoegd. Bovendien heeft de container van [!DNL Columns] een montageselement waar de gebruikers configuratie voor deze omslagentiteit kunnen specificeren.<!--- PB-500-->

![ Nieuwe ](../assets/new.svg) **Nieuwe menuopties om, de groepen van Kolommen te dupliceren te verbergen en te schrappen** - met deze nieuwe opties, kunnen de gebruikers, [!DNL Columns] groepen dupliceren verbergen en schrappen - enkel als zij met inhoudstypes kunnen.<!--- PB-507-->

![ Nieuwe ](../assets/new.svg) <!-- Issue 594 -->**Nieuwe multiline kolomsteun die aan de groep van de Kolom** wordt toegevoegd - met deze toevoeging, kunnen de gebruikers veelvoudige lijnen van kolommen binnen één [!DNL Columns] groep manipuleren helpen kolomlay-outs veel flexibeler maken.<!--- PB-108-->

Zie [ Lay-out - Kolom ](./column.md) voor informatie over het gebruiken van de nieuwe [!DNL Columns] groep.

## 1.7.1 voor Commerce 2.4.4

![ Vaste kwestie ](../assets/fix.svg) de Bouwer van de Pagina is nu compatibel met PHP 8.1.<!--- AC-1300-->

![ Vaste kwestie ](../assets/fix.svg) De handelaren kunnen alternatieve tekst (`alt_text`) aan beelden (Beeld, Banner, Dia) nu toevoegen om inhoudstoegankelijkheid te verbeteren.<!--- PB-1193-->

![ Vaste kwestie ](../assets/fix.svg) Admin gebruikers met toestemmingen beperkt tot Inhoud uitgeven slechts ziet een fout niet meer wanneer het gebruiken van de Bouwer van de Pagina om een productwidget aan een CMS pagina toe te voegen. De Bouwer van de pagina toont ook een nauwkeurige producttelling op de widgetmontagespagina. Eerder, vereiste de Bouwer van de Pagina toestemmingen aan de module van de Catalogus wanneer het terugwinnen van het productaantal en toonde deze fout: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![ Vaste kwestie ](../assets/fix.svg) de kwesties van de Vertoning met het menu van het Formaat van de Bouwer van de Pagina worden nu opgelost met TinyMCE 5 bibliotheekverbetering. <!--- AC-446-->

![ Vaste kwestie ](../assets/fix.svg) U kunt de muis nu gebruiken om a **Tekst uit te geven** waarde in popup van de Verbinding van het Tussenvoegsel te tonen. <!--- AC-982-->

![ Vaste kwestie ](../assets/fix.svg) de Bouwer van de Pagina toont nu alle opties zoals verwacht op het de optiemenu van de Grootte van de Doopvont. Eerder werden niet alle opties weergegeven. <!--- AC-1056-->

![ Vaste kwestie ](../assets/fix.svg) werkte het `phpgt/dom` gebiedsdeel Composer voor de `magento/magento2-page-builder` uitbreiding aan de recentste versies bij. <!--- magento/magento2-page-builder/pull/779-->

![ Vaste kwestie ](../assets/fix.svg) de Bouwer van de Pagina resizes niet meer de de Verbinding van het Tussenvoegsel en dialoog van het Beeld van het Tussenvoegsel wanneer het tonen van de schuif in een kleine kolom. <!--- AC-973-->

![ Vaste kwestie ](../assets/fix.svg) Het menu van de Eigenschappen van de Lijst van de Bouwer van de Pagina wordt nu getoond zoals verwacht. <!--- AC-407-->

![ Vaste punten van de Uitgave ](../assets/fix.svg) van de Schuif worden niet meer getoond op de verbinding van het Tussenvoegsel of beeld modaal wanneer de muis niet over de schuif beweegt. <!--- AC-406-->

![ Vaste kwestie ](../assets/fix.svg) De doopvontgrootte die wordt gebruikt om de het menuopties van de Lijst te tonen is geoptimaliseerd. <!--- AC-396-->

![ Vaste kwestie ](../assets/fix.svg) Correcte anomalieën met het plaatsen van het Beeld van het Tussenvoegsel/geeft Beeld uit en Tussenvoegsel/geeft de dialoog van de Verbinding uit. <!--- AC-397-->

![ Vaste kwestie ](../assets/fix.svg) de Bouwer van de Pagina meldt niet meer een fout wanneer u op **Redacteur van de Tekst** voor een banner klikt. <!--- AC-398-->

![ Vaste kwestie ](../assets/fix.svg) de Bouwer van de Pagina zet niet meer alle dynamische blokken in één taal tijdens verbetering om. <!--- MC-42265-->

## 1.6.0 voor Adobe Commerce 2.4.2

![ Nieuwe ](../assets/new.svg) <!-- Issue 558 -->**Nieuwe [!DNL Page Builder] het stileren** - [!DNL Page Builder] maakte enorme verbeteringen aan hoe het inhoud stijgt. Door de wijzigingen kunt u nu eenvoudig eenvoudige CSS-kiezers maken die de bestaande stijlen voor inhoudstypen overschrijven. Met deze wijzigingen kunt u [!DNL Page Builder] -thema&#39;s maken die veel reageren op alle inhoudstypen.

![ Nieuwe ](../assets/new.svg) <!-- Issue 429 -->**container van de Rij nu facultatief** - u kunt inhoud in [!DNL Page Builder] nu tot stand brengen zonder een container van de Rij te vereisen. Naast de rij kunnen nu de volgende inhoudstypen rechtstreeks in het werkgebied worden gesleept en neergezet: HTML, Blok, Dynamisch blok, Kolommen en Tabs.

![ Nieuwe ](../assets/new.svg) <!-- Issue 636 -->**Nieuwe ontvankelijke viewport schakelaar** - u kunt uw [!DNL Page Builder] inhoud bij verschillende apparatenbreedten (breekpunten) nu voorproef gebruikend de nieuwe knopen van de viewport Admin boven het stadium. De viewport schakelaar simuleert hoe uw inhoud wanneer getoond op de storefront wanneer verschillende apparaten wordt gestileerd.

![ Nieuwe ](../assets/new.svg) <!-- Issue 637 -->**Nieuwe breekpunt-specifieke vormgebieden** - De waarden van het type van inhoud kunnen nu aan specifieke viewport breekpunten worden geplaatst. Pictogramindicatoren naast de velden geven de viewport weer waarop de veldwaarde van het inhoudstype wordt toegepast.

![ Nieuw ](../assets/new.svg) <!-- Issue 559 -->**Verwijderde vooraf bepaalde ingangen van het vormgebied** - Geavanceerde vormmontages voor marges, opvullingen, en op grens betrekking hebbende eigenschappen (grens, grensbreedte, en grensstraal) zijn nu geplaatst als `default`, zodat de waarden door CSS van een module kunnen worden bepaald.

![ Nieuw ](../assets/new.svg) <!-- Issue 635, 557,  -->**Toegevoegde stadium het uit elkaar plaatsen** - Rijen en Kolommen verstrekken nu extra het uit elkaar plaatsen emissierechten rond bevatte inhoudstypes op het stadium, maar niet op de opslag. Door de extra afstand in het werkgebied is het gemakkelijker om toegang te krijgen tot de menu&#39;s van de mouseover-optie voor zowel de container als de ingesloten inhoudstypen.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-37348 -->**Vaste auto-scrollen aan overzichten** - auto-scrolling aan productoverzichten op de storefront is nu bevestigd.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-36227 -->**Vaste bebouwde inhoud** - De categorie van de lengte en de productbeschrijvingen worden niet meer bebouwd.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-35402 -->**Vaste volledige breedte, volledig-afloopde inhoud van de Categorie** - de inhoud van de Categorie kan nu in een volledig-breedte of volledig-aflooplay-out worden getoond.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-37989 -->**de verhogingen van de Veiligheid**

## 1.5.1 voor Adobe Commerce 2.4.1-p1

![ Vaste kwestie ](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**de vertoning van de Fout** - Vaste een kwestie waarin [!DNL Page Builder] een fout toen het toevoegen van Subcategorieën van de Catalogus in Admin toonde.

## 1.5.0 voor Adobe Commerce 2.4.1

![ Nieuwe ](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Inmersive, volledig-scherm het uitgeven** - het uitgeven [!DNL Page Builder] inhoud is nu volledig-scherm slechts voor alle gebieden die door [!DNL Page Builder] worden gecontroleerd. Deze wijziging omvat CMS-pagina&#39;s, product- en categoriepagina&#39;s, blokken en dynamische blokken. Bij bewerking op volledig scherm krijgt de inhoud de focus en wordt een weergave geboden die beter aansluit bij de gebruikerservaring op de winkel.

![ Nieuwe ](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] inhoudsvoorproeven &#x200B;**- door gebrek, [!DNL Page Builder] verstrekt nu inhoudsvoorproeven niet alleen voor CMS pagina&#39;s, Blokken, en Dynamische Blokken, maar ook voor de pagina&#39;s van het Product en van de Categorie. U kunt deze functie zo configureren dat deze in- of uitgeschakeld is voor product- en categoriepagina&#39;s met de nieuwe instelling [!DNL Page Builder] Voorvertoning van inhoud, die u kunt openen in de winkelconfiguratie via Inhoudbeheer > Geavanceerde gereedschappen voor inhoud.

![ Nieuw ](../assets/new.svg) <!-- Issue 543 -->**Verbeterde toegang tot de korte beschrijvingen van het Product** - door gebrek, wordt een korte beschrijving van het Product nu getoond vóór de langere beschrijving. Deze wijziging komt overeen met de volgorde waarin ze in de winkel worden weergegeven. Hierdoor is het niet nodig door de langere beschrijvingsinhoud te bladeren om toegang te krijgen tot de korte beschrijving.

![ Nieuw ](../assets/new.svg) <!-- Issue 419 -->**verhinderde genestelde verbindingen in Banners en Dia&#39;s** - toevoegend verbindingen aan zowel de inhoud als de buitenelementen van Banners en Dia&#39;s creeerde genestelde verbindingen die niet correct op de storefront tonen of zich gedragen. Om de kwestie op te lossen, kunnen de verbindingen niet meer aan *zowel* het gebied van de Tekst van het Bericht als het attribuut van de Verbinding voor Banners en Dia&#39;s worden toegevoegd.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 421 --> Vaste kwestie waar het plaatsen van lege grensstraal op een Punt van het Lusje fouten veroorzaakte en de inhoud van het Punt van het Lusje brak.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 422 --> Vaste kwestie waar het toevoegen van bepaalde combinaties voorwaarden aan het filter van de Voorwaarde van Producten fouten veroorzaakte die het bewaren van de vorm van Producten verhinderden.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 425 --> Vaste kwestie waarin het de inhoudstype van de Schuif zich niet correct gedraagt toen het Oneindige plaatsen van de Lijn werd onbruikbaar gemaakt.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 426 --> Vaste de Minimum Geadverteerde Prijs zodat het nu in [!DNL Page Builder] werkt.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 436 --> Vaste de kwestie in Safari en IE 11 die het slepen van en het laten vallen van een Beeld aan het uploadgebied in Banners en Dia&#39;s verhinderde.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 525 --> Vaste de kwestie waarin het de inhoudstype van de Schuif niet in Firefox beantwoordde.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 567 --> Vaste de kwestie waar de widgetconfiguratie onjuiste selecteurs in DOM voor de verschillende verschijningen creeerde.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 609 --> Vaste de kwestie waarin de toolbar van de Kopbal het de optiemenu van het inhoudstype verborgen, dat toegang tot de vorm en andere opties verhinderde.

![ Vaste kwestie ](../assets/fix.svg) <!-- Issue 612, 613 --> Vaste kwesties waar de Schuifregelaars en de veelvoudige rijen die parallaxachtergronden gebruiken niet correct zouden teruggeven na het van een knevel voorzien van een knevel van de volledig-schermwijze verscheidene tijden.

![ Vaste kwestie ](../assets/fix.svg) <!--MC-35220--> Vaste de kwestie waar het proberen om de inhoud van een inhoudstype van de Rubriek aan een inhoudstype van de Tekst te kopiëren verhinderde [!DNL Page Builder] te bewaren.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-34620 --> Vaste het inhoudstype van de Tekst om niet-Latin-1 karakters correct te behandelen en te bewaren.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-34679 --> Vaste [!DNL Page Builder] CSS stijlen die Safari 13.1 om het de plaatsmenu van het thema van de Luma voor kleine meningshavens en mobiele schermen verkeerd terug te geven veroorzaakte.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-34848 --> Vaste het inhoudstype van HTML om ingebedde widgets als &quot;Orde door SKU&quot;op de Storefront correct te tonen.

## 1.4.1 voor Adobe Commerce 2.4.0-p1

![ Nieuw ](../assets/new.svg) <!-- PB-590 --> die aan TinyMCE 4 wordt bevorderd. TinyMCE 3 is verwijderd om de beveiliging te verbeteren.

## 1.4.0 voor Adobe Commerce 2.4.0

![ Nieuwe ](../assets/new.svg) <!-- PB-494 --> Toegevoegde steun voor PHP 7.4.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-31247 --> Vaste een kwestie waar het inhoudstype van Producten geen configureerbare producten toonde toen de voorwaarde aan prijs werd geplaatst.

![ Vaste kwestie ](../assets/fix.svg) <!-- PB-179 --> Vaste de groeperingsconfiguratie van Producten om slechts de productcontainer zelf, niet de inhoud van de productcontainer, zoals de productnaam, de prijs, knopen, beelden, en andere elementen te plaatsen.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-33556 --> de verbeteringen van Prestaties.

![ Vaste kwestie ](../assets/fix.svg) de verhogingen van de Veiligheid.

## 1.3.3-p1 voor Adobe Commerce 2.3.6-p1

![ Vaste kwestie ](../assets/fix.svg) de verhogingen van de Veiligheid.

## 1.3.3 voor Adobe Commerce 2.3.6

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-32766 --> Vaste het inhoudstype van de Tekst om de veranderlijke die richtlijnen correct te bewaren aan HTML attributen worden toegevoegd.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-34590 --> Vaste het inhoudstype van de Tekst om niet-Latin-1 karakters correct te behandelen en te bewaren.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-34677 --> Vaste [!DNL Page Builder] CSS stijlen die Safari 13.1 om het de plaatsmenu van het thema van de Luma voor kleine meningshavens en mobiele schermen verkeerd terug te geven veroorzaakte.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-34846 --> Vaste het inhoudstype van de HTML om ingebedde widgets als _Orde door SKU_ op de storefront correct te tonen.

![ Vaste kwestie ](../assets/fix.svg) een fout die gebruikers soms verhinderde inhoud-type vormen op te slaan. De fout (&quot;[!DNL Page Builder] gaf 5 seconden terug zonder sloten vrij te geven&quot;) veroorzaakte het ladingspictogram om eindeloos te draaien na het proberen om een vorm te bewaren.

## 1.3.2 voor Adobe Commerce 2.3.5-p2

![ Nieuwe ](../assets/new.svg) Verbeteringen van de Veiligheid.

## 1.3.1 voor Adobe Commerce 2.3.5-p1

Deze versie van [!DNL Page Builder] is slechts een versienummerupdate voor Adobe Commerce 2.3.5-p1. Alle functies die worden beschreven voor versie 1.3.0 zijn ook van toepassing op deze versie.

## 1.3.0 voor Adobe Commerce 2.3.5

![ Nieuwe ](../assets/new.svg) **Malplaatjes** - [!DNL Page Builder] heeft nu malplaatjes die van bestaande inhoud kunnen worden gecreeerd en op nieuwe inhoudsgebieden kunnen worden toegepast. In [!DNL Page Builder] -sjablonen worden zowel de inhoud als de lay-outs opgeslagen van bestaande pagina&#39;s, blokken, dynamische blokken, productkenmerken en categoriebeschrijvingen. U kunt bijvoorbeeld een bestaande [!DNL Page Builder] CMS-pagina opslaan als een sjabloon en die sjabloon vervolgens toepassen (met alle inhoud en lay-outs) om snel CMS-pagina&#39;s voor uw site te maken. Deze nieuwe eigenschap wordt hier gedocumenteerd: [ Malplaatjes ](templates.md).

![ Nieuwe ](../assets/new.svg) **Video Achtergronden voor Rijen, Banners, en Schuifregelaars** - [!DNL Page Builder] de Rijen, de Banners, en de Schuivers kunnen video&#39;s voor hun achtergronden nu gebruiken. Deze nieuwe eigenschappen worden hier gedocumenteerd: [ Rijen ](row.md), [ Banners ](banner.md), [ Schuifregelaars ](slider.md).

![ Nieuwe ](../assets/new.svg) **Video steuntoevoegingen en verhogingen** - [!DNL Page Builder] steunt nu een grotere verscheidenheid van videoformaten. Naast YouTube- en Vimeo-video&#39;s ondersteunen het inhoudstype Video en de videoachtergronden nu video-URL-koppelingen naar video-indelingen zoals `.mp4` en andere door de browser ondersteunde indelingen. Het inhoudstype Video voegt ook een automatisch afspeelbare functie toe. Deze nieuwe eigenschappen worden hier gedocumenteerd: [ Video inhoudstype ](video.md).

![ Nieuwe ](../assets/new.svg) **Volledige Rijen van de Hoogte, Banners, en Schuifregelaars** - [!DNL Page Builder] de Rijen, de Banners, en de Schuivers kunnen hun hoogten aan de volledige hoogte van de pagina nu plaatsen gebruikend een aantal met om het even welke CSS eenheid (px, %, vh, em) of een berekening tussen eenheden (100vh - 237px). Deze nieuwe eigenschappen worden hier gedocumenteerd: [ Rijen ](row.md), [ Banners ](banner.md), [ Schuifregelaars ](slider.md).

![ Nieuwe ](../assets/new.svg) **de bibliotheek van de typeverbetering van de Inhoud** - de Ontwikkelaars kunnen versies van [!DNL Page Builder] inhoudstypes nu tot stand brengen zonder achteruit-onverenigbaar kwesties met vorige versies te introduceren. Vóór deze release zouden belangrijke wijzigingen in configuraties van inhoudstypen leiden tot weergave- en gegevensverliesproblemen met eerder opgeslagen [!DNL Page Builder] -inhoudstypen. Deze problemen worden verwijderd door de nieuwe upgradebibliotheek. De bibliotheek wordt ontworpen om vorige versies van inhoudstypes te bevorderen die aan het gegevensbestand worden opgeslagen zodat zij de configuratieveranderingen in de nieuwe versies aanpassen. [!DNL Page Builder] voert de verbeteringsbibliotheek op inheemse inhoudstypes uit zoals nodig voor een nieuwe versie. Deze wijziging zorgt ervoor dat de ingebouwde [!DNL Page Builder] inhoudstypen altijd worden bijgewerkt zodat ze overeenkomen met eventuele wijzigingen die voor een nieuwere versie in de inhoudstypen zijn aangebracht.

>[!IMPORTANT]
>
>Als u extra gegevensbestandentiteiten voor het opslaan van [!DNL Page Builder] inhoud hebt gecreeerd, moet u __ die entiteiten aan uw `etc/di.xml` toevoegen. Als u dat niet doet, wordt de [!DNL Page Builder] -inhoud die in uw entiteit is opgeslagen, niet bijgewerkt, wat resulteert in mogelijk gegevensverlies en weergaveproblemen. Als u bijvoorbeeld een blogentiteit hebt gemaakt die [!DNL Page Builder] -inhoud opslaat, moet u uw blogentiteit aan uw `etc/di.xml` -bestand toevoegen als een `UpgradableEntitiesPool` -type, zodat de upgradebibliotheek de [!DNL Page Builder] -inhoudstypen die in uw blog worden gebruikt, kan bijwerken. Voor meer informatie en instructies bij het gebruiken van de verbeteringsbibliotheek, zie [ inhoudstypes van de Verbetering ](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) in de _Gids van de Ontwikkelaar van de Bouwer van de Pagina_.

![ Nieuwe ](../assets/new.svg) **Documentatie voor het toevoegen van nieuwe verschijningen** - de informatie van de Ontwikkelaar nu gepubliceerd over [ toevoegend verschijningen ](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) voor bestaande of types van douaneinhoud.

![ Vaste kwestie ](../assets/fix.svg) **Diverse moeilijke situaties**

- &#x200B;<!-- PB-50 -->Probleem verholpen waarbij het TinyMCE-menu voor dia-inhoud onder andere inhoudstypen werd weergegeven als de bovenliggende container van de dia is gedupliceerd.
- &#x200B;<!-- PB-166 -->Bijgewerkt [!DNL Page Builder] om een vernietigingsmethode te implementeren om geheugenlekken in sommige scenario&#39;s te voorkomen.
- &#x200B;<!-- PB-170 -->Verbeterde TinyMCE-prestaties wanneer meerdere instanties in het beheerwerkgebied worden gebruikt.
- &#x200B;<!-- PB-252 -->Probleem verholpen waarbij het inhoudstype Dynamisch blok niet wordt gerenderd in het beheerwerkgebied als de bovenste rij is gemarkeerd als verborgen.
- &#x200B;<!-- PB-273 -->Verfijnde muis-hover gebeurtenissen op het Admin stadium door een vertraging van 200 ms uit diverse controles UI te verwijderen. Door deze wijziging kunt u gemakkelijker werken met geneste inhoudsitems in het werkgebied.
- &#x200B;<!-- PB-294 -->Probleem verholpen waarbij het valutasymbool onjuist werd beschermd in de productlijstwidget in het blok/dynamisch blok in het beheerstadium.
- &#x200B;<!-- PB-296 -->Correctie van een probleem waarbij het producttotaal in het bewerkingspaneel [!DNL Page Builder] niet werkte voor aangepaste MSI-voorraadproducten.
- &#x200B;<!-- PB-317 -->Correctie van een probleem waarbij het opslaan van [!DNL Page Builder] -inhoud met achtergrondafbeeldingen op Microsoft Edge deze afbeeldingen niet op de winkelachtergrond weergeeft.
- &#x200B;<!-- PB-390 -->Correctie van een probleem waarbij geneste [!DNL Page Builder] -inhoud niet kon worden opgeslagen als gebruikers op de knop Opslaan klikken voordat de pagina volledig wordt weergegeven.
- &#x200B;<!-- PB-418 -->Correctie van uitzonderingsfout die in snijtaken is gegenereerd als gevolg van [!DNL Page Builder] analytics.

## 1.2.2 voor Adobe Commerce 2.3.4-p2

![ Nieuwe ](../assets/new.svg) Verbeteringen van de Veiligheid.

## 1.2.1 voor Adobe Commerce 2.3.4-p1

![ Nieuwe ](../assets/new.svg) Verbeteringen van de Veiligheid.

## 1.2.0 voor Adobe Commerce 2.3.4

![ Nieuwe ](../assets/new.svg) **[!DNL Page Builder]integratie met PWA Studio** - toegevoegde [!DNL Page Builder] inhoud die aan de app van Venia in PWA Studio teruggeeft. [!DNL Page Builder] -inhoud kan nu worden weergegeven in de app PWA Studio Venia. Zie de [!DNL Page Builder] documentatie binnen [ PWA Studio ] voor alle informatie over deze nieuwe eigenschap.

![ Nieuwe ](../assets/new.svg) **Toegevoegde carrousel van het Product** - <!-- PB-77, PB-173, PB-175 --> het inhoudstype van Producten verstrekt nu een optie om uw producten in een carrousel/schuifformaat, met inbegrip van verscheidene opties te tonen om de carrousel aan uw behoeften aan te passen.

![ Nieuw ](../assets/new.svg) **Toegevoegde het sorteren van SKU van het Product** - <!-- PB-69 --> het inhoudstype van Producten verstrekt nu een optie om uw producten door SKU in de orde te sorteren u hen aan een lijst binnen Admin toevoegt.

![ Nieuw ](../assets/new.svg) **Toegevoegde het sorteren van de Categorie van het Product** - <!-- PB-181 -->. Het inhoudstype van Producten verstrekt nu een optie om uw producten door categorie _positie_ te sorteren, tonend hen in de zelfde orde dat zij binnen uw Catalogus van Commerce verschijnen.

![ Nieuwe ](../assets/new.svg) **Toegevoegde de selectietotalen van het Product** - <!-- PB-107 -->. Het inhoudstype Admin van Producten uitgeeft nu het totale aantal producten die uw opties van de productselectie aanpassen.

![ Vaste kwestie ](../assets/fix.svg) **Diverse moeilijke situaties**

- &#x200B;<!-- PB-237 -->Verbeterde beveiliging.
- &#x200B;<!-- PB-41 -->Vaste zoekopdrachten binnen UI selecteren componenten om slechts één AJAX verzoek per zoekterm in te dienen.
- &#x200B;<!-- PB-76, PB-84-->Bijgewerkte productvoorvertoningen in de Admin die overeenkomen met de winkel, inclusief de sterrenwaardering, kleur en grootteopties van het product, indien van toepassing.
- &#x200B;<!-- PB-169 -->Correctie van een probleem waarbij [!DNL Page Builder] niet kon worden opgeslagen wanneer JavaScript minification en bundling zijn ingeschakeld in Commerce.
- &#x200B;<!-- PB-241 -->Oplossing voor een geschikte oplossing voor de voorvertoningen in Beheer van Producten, Blokken en Dynamische Blokken bij Commerce-installaties die verschillende URL&#39;s definiëren voor de Admin en de frontend.
- &#x200B;<!-- PB-238 -->Vaste Admin voorproeven van Producten, Blokken, en Dynamische Blokken om correct op de installaties van Commerce met B2B terug te geven die met _wordt geïnstalleerd Login slechts_ toegelaten optie. Voordat deze correctie wordt uitgevoerd, leidt de voorvertoning van [!DNL Page Builder] ertoe dat de pagina wordt omgeleid naar de aanmeldingsgegevens van de klantenaccount.
- &#x200B;<!-- PB-239 -->Oplossing voor een sessiefout die kan optreden wanneer een voorvertoning van een grote pagina in de [!DNL Page Builder] Admin wordt weergegeven.
- &#x200B;<!-- PB-248 -->[!DNL Page Builder] LESS-stijlen zijn bijgewerkt om overlapping in de storefront-stijl te voorkomen.

## 1.1.1 voor Adobe Commerce 2.3.3-p1

![ Nieuwe ](../assets/new.svg) Verbeteringen van de Veiligheid.

## 1.1.0 voor Adobe Commerce 2.3.3

![ Nieuw ](../assets/new.svg) <!-- MC-15250 --> Toegevoegde expliciete productsortering aan het inhoudstype van Producten.

![ Nieuwe ](../assets/new.svg) <!-- MC-17823 --> Toegevoegde knopen voor het opnemen van beelden, widgets, en variabelen in het inhoudstype van HTML.

![ Vaste kwestie ](../assets/fix.svg) Verbeterde [!DNL Page Builder] veiligheid.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-1805 --> Bijgewerkt [!DNL Page Builder] om PHP versie 7.3 te steunen.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-4137 --> bijgewerkte TinyMCE aan versie 4.9.5. Deze update verhelpt samen met de extra verbeteringen verschillende problemen met de inline TinyMCE-editor:

- De variabelen, de beelden, en de beeldverbindingen worden toegevoegd waar de curseur wordt geplaatst.
- Tabellen en tabelcellen kunnen worden gecentreerd.
- Met Kopiëren/plakken plakt u nu inhoud op de cursorpositie.
- Koppelingen kunnen worden toegepast op geselecteerde tekst.
- Opsommingstekens worden correct uitgelijnd.
- Wijzigingen in de inline editor kunnen worden opgeslagen zonder eerst buiten de editor te klikken.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-3880 --> Vaste een kwestie waarin de minimumhoogte en de verticale groepering tussen secties op uitgeeft paneel voor elk inhoudstype inconsistent waren.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-14994 --> Vaste een kwestie waarin de toolbar van het inhoudstype van de Kop verkeerd werd geplaatst toen eerst gelaten vallen op het stadium.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-15742 --> Vaste hard-gecodeerde marges in zowel de inhoudstypes van de Schuif als van de Video.

![ Vaste kwestie ](../assets/fix.svg) <!-- MC-16241 --> Vaste een kwestie waarin het vereiste asterisksymbool tweemaal op vormgebieden werd getoond.

## 1.0.3 voor Adobe Commerce 2.3.2-p2

![ Nieuwe ](../assets/new.svg) Verbeteringen van de Veiligheid.

## 1.0.2 voor Adobe Commerce 2.3.2-p1

![ Nieuwe ](../assets/new.svg) Verbeteringen van de Veiligheid.

## 1.0.1 voor Adobe Commerce 2.3.2

![ Nieuw ](../assets/new.svg) verzekert verenigbaarheid met Adobe Commerce 2.3.2.

## 1.0.0 voor Adobe Commerce 2.3.1

![ Nieuwe ](../assets/new.svg) Algemene beschikbaarheidsversie


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
