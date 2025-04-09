---
title: HIPAA-gereedheid op Adobe Commerce
description: Ontdek hoe u de Adobe Commerce HIPAA-Ready-extensie kunt toevoegen en extra functies en functionaliteiten kunt krijgen waarmee u aan uw HIPAA-verplichtingen kunt voldoen.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 2807c36fdb4ca169c31a5e92b4dab278a45c474c
workflow-type: tm+mt
source-wordcount: '2375'
ht-degree: 1%

---

# HIPAA-gereedheid op Adobe Commerce

>[!IMPORTANT]
>
>**Juridische disclaimer**<br/>
>Deze informatie is bedoeld om klanten van Adobe te helpen hun vragen betreffende de HIPAA-Klaar Diensten van Adobe beantwoorden. Het is geen juridisch advies. Handelaren moeten hun eigen juridische adviseur raadplegen om te begrijpen wat hun verplichtingen in het kader van de HIPAA zijn en wat het juiste gebruik en de juiste configuratie van Adobe-producten is.

>[!BEGINSHADEBOX]

**Wet op de overdraagbaarheid en verantwoordingsplicht van ziektekostenverzekeringen (HIPAA)**

De Health Insurance Portability and Accountability Act (HIPAA) is de belangrijkste federale privacywet voor de gezondheidszorg in de Verenigde Staten en wordt gehandhaafd door het Amerikaanse ministerie van Volksgezondheid en Human Services (HHS). HIPAA is van toepassing op _gedekte entiteiten_ (zoals zorgaanbieders, verzekeraars en clearinghouses) en _zakenpartners_ (zoals de entiteiten die diensten verlenen aan gedekte entiteiten). HIPAA-vereisten zijn verdeeld over drie afzonderlijke regels: privacyregel, beveiligingsregel en meldingsregel voor inbreuken. Adobe treedt op als zakenpartner voor bepaalde producten, die Adobe classificeert als &#39;HIPAA-Ready Services&#39;. Gegevens die onder HIPAA vallen, worden beschermde gezondheidsinformatie _of PHI genoemd_. PHI is een subset van gezondheidsinformatie die (1) wordt gecreëerd of ontvangen door een zorgverlener, gezondheidsplan of uitwisselingscentrum voor gezondheidszorg, (2) betrekking heeft op de vroegere, huidige of toekomstige fysieke of mentale gezondheid of toestand van een persoon, het verlenen van gezondheidszorg aan een persoon, of de vroegere, huidige of toekomstige betaling voor het verlenen van gezondheidszorg aan een persoon,  en (3) de persoon identificeert of ten aanzien waarvan er een redelijke basis is om aan te nemen dat de informatie kan worden gebruikt om de persoon te identificeren. De HIPAA-privacy- en beveiligingsregels vereisen dat een Gedekte entiteit schriftelijke garanties verkrijgt van een zakenpartner in de vorm van een Business Associate Agreement, of BAA, waarbij de zakenpartner de privacy en veiligheid van de PHI van de Gedekte entiteit moet beschermen. Zie [HIPAA- en Adobe-producten en -services](https://www.adobe.com/trust/compliance/hipaa-ready.html) in het Adobe Vertrouwenscentrum voor meer informatie.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA gereed

De Adobe Commerce HIPAA-Ready-uitbreiding voegt extra functies en functies toe aan Adobe Commerce-installaties die handelaren in staat stellen te voldoen aan hun respectieve HIPAA-verplichtingen.

De Adobe Commerce HIPAA-Ready-extensie `magento/hipaa-ee` is beschikbaar voor Adobe Commerce op cloudinfrastructuur of Adobe Managed Services-projecten. Het Adobe Commerce HIPAA-Klaar installatieproces maakt sommige inheemse diensten en eigenschappen onbruikbaar om aan vereisten te voldoen HIPAA. Zie [ Gehandicapte diensten en eigenschappen ](#disabled-services-and-features).

>[!NOTE]
>
>Toegang tot functies en functionaliteit die klaar zijn voor HIPAA is alleen beschikbaar voor handelaren die de invoegtoepassing voor gezondheidszorg voor Adobe Commerce hebben aangeschaft.

*Deze materialen zijn voorgenomen voor informatieve slechts doeleinden. Het verstrekken van deze informatie geeft de ontvanger geen recht op contractuele of andere rechten. Er zijn inspanningen geleverd om de juistheid van de informatie te waarborgen vanaf de datum waarop deze is verstrekt, maar er zijn geen aanwijzingen dat deze informatie juist en volledig is. Adobe verbindt zich er niet toe deze informatie bij te werken wanneer de wet of de Adobe-producten veranderen. Dit document mag ook niet zonder schriftelijke toestemming van Adobe worden verspreid naar een andere partij dan de beoogde ontvanger.*

## Systeemvereisten

In de volgende tabel wordt de compatibiliteit tussen versies van Adobe Commerce en de extensie HIPAA getoond:

| Adobe Commerce | Ondersteund | Notities |
|----------------|-----------|-------|
| 2.4.7-p4 - 2.4.7-p5 | 1.2.0. | 2.4.7-p4 de steun vereist a [ hotfix ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/hotfix-for-hipaa-package-1-2-0-compatibility-with-adobe-commerce-2-4-7-p4) |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0. | |
| 2.4.6-p8 | 1.1.0. | De steun voor [ datadiensten ](#adobe-commerce-services) werd geïntroduceerd in 1.1.0 |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0. | |

>[!IMPORTANT]
>
>- De extensie die klaar is voor HIPAA is alleen beschikbaar voor Adobe Commerce op Cloud- of Adobe Commerce Managed Services-projecten.
>- De extensie is beschikbaar als een Composer-metapakket van `repo.magento.com` .
>- Voor toegang tot functies en functionaliteit die klaar zijn voor HIPAA is de invoegtoepassing voor gezondheidszorg voor Adobe Commerce vereist.
>- Adobe Commerce bètaversies worden niet ondersteund.

## Installatie

**Vereiste**

>[!BEGINSHADEBOX]

- Adobe heeft uw Adobe Commerce-account ingericht voor toegang tot de HIPAA Ready-extensie.
- Toegang tot [ repo.magento.com ](https://repo.magento.com) om de uitbreiding te installeren. Voor zeer belangrijke generatie en het verkrijgen van de noodzakelijke rechten, zie [ uw authentificatiesleutels ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) krijgen.

>[!ENDSHADEBOX]

Installeer de nieuwste versie van de Adobe-extensie HIPAA-Ready Services (`magento/hipaa-ee`) voor een instantie die Adobe Commerce versie 2.4.7-p5 of 2.4.6-p3 tot en met 2.4.6-p8 uitvoert. De uitbreiding wordt geleverd als composer metapack van de {](https://repo.magento.com) bewaarplaats 0} repo.magento.com. [ Het metapakket omvat de inzameling van modules die de mogelijkheden HIPAA voor een instantie van Adobe Commerce toelaten.

>[!NOTE]
>
>Om achterbureaugebeurtenisgegevens te verzekeren die naar Experience Platform worden verzonden is HIPAA-klaar, zie de [ de uitbreidingsgids van de Verbinding van Gegevens ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. Schakel op uw lokale werkstation de projectmap voor uw Adobe Commerce over het infrastructuurproject voor de cloud in.

   >[!NOTE]
   >
   >Voor informatie over het beheren van het projectmilieu&#39;s van Commerce plaatselijk, zie [ het Leiden takken met CLI ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) in _Adobe Commerce op de Gids van de Gebruiker van de Infrastructuur van de Wolk_.

1. Check de omgevingsvertakking uit om bij te werken met de Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Voeg het metapakket `magento/hipaa-ee` toe aan de componentenconfiguratie gebruikend composer CLI.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Pakketafhankelijkheden bijwerken.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Voeg de bijgewerkte code toe aan de cloud-omgeving, wijs deze toe en duw er vervolgens op.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Het duwen van de updates stelt het [ proces van de de wolkenplaatsing van Commerce ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) in werking om de veranderingen toe te passen. Controleer de plaatsingsstatus van [ opstellen logboek ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Installatie controleren

Nadat de updates zijn geïmplementeerd, controleert u of de extensie `Hipaa*` is geïnstalleerd

1. Gebruik SSH om u aan te melden bij de externe cloud-omgeving.

   ```shell
   magento-cloud ssh
   ```

1. Van de bevellijn, gebruik CLI van Adobe Commerce om de modulestatus te controleren.

   ```shell
   bin/magento module:status
   ```

1. Verifieer dat de modules HIPAA in de lijst van toegelaten modules inbegrepen zijn:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   Alle modules die met `Magento_Hipaa` worden voorgefixeerd moeten in de toegelaten modulessectie zijn.

## Verbeterde functies voor HIPAA-gereedheid

De `magento/hipaa-ee` extensie introduceert enkele wijzigingen en verbeteringen in het basisproduct Commerce. In de volgende paragrafen vindt u meer informatie over deze wijzigingen en hoe deze het basisproduct wijzigen.

### Actie logboeken

Controle het Registreren is een vereiste van HIPAA. In Adobe Commerce, registreert de ](../../systems/action-log.md) eigenschap van de Actie 0} {elke verandering die door een gebruiker wordt aangebracht Admin die in uw opslag werkt. [ Om aan de vereisten van HIPAA voor het Logboek van de Controle te voldoen, is de eigenschap bijgewerkt om alle Admin gebruikers en klantenacties te registreren die door Admin UI en door API vraag worden uitgevoerd.

Met Action Logs worden ook gebeurtenissen vastgelegd wanneer Adobe-services toegang krijgen tot uw opslaggegevens. U kunt deze gebeurtenissen identificeren door te filteren op de actie &quot;Gegevens verzonden buiten&quot;in het rapport van de Logs van de Actie.

#### Rapport Actielogboeken

Het _rapportraster voor actielogboeken_ (**[!UICONTROL System]** > actielogboeken > rapport) is gewijzigd om tegemoet te komen aan acties van klanten die worden uitgevoerd via de gebruikersinterface en API van de beheerder.

1. Twee kolommen toegevoegd:
   - ***Bron***: Geeft aan waar de actie is uitgevoerd.
Waarden: `Admin UI` / `Customer UI` / `REST API` / / `SOAP API``GraphQL API`
   - ***Clienttype***: Geeft het clienttype weer.
Waarden: Klant | Beheerder | Integratie

2. Hernoemd ***Gebruikersnaam*** kolom aan ***Herkenningsteken van de Cliënt***
   - ***Identiteitskaart van de Cliënt***: Toont login identiteitskaart voor de gebruiker die de actie uitvoerde.
Waarden:
      - een e-mail als het Type van Cliënt Klant is
      - een gebruikersnaam als het type client beheerder is
      - een naam als het Type van Cliënt Integratie is

3. De anders genoemde ***Volledige kolom van de Naam van de Actie*** aan ***Doel***
   - ***Doel***: Toont de actienaam.
Waarden:
      - een eindpunt als Source een REST API of SOAP API is
      - een naam voor query&#39;s of mutaties als een GraphQL API
      - een handelingnaam als een beheerdersinterface of gebruikersinterface van de klant.

#### Beheerdersacties configureren voor logbestanden

Deze functie is niet beschikbaar omdat alle handelingen standaard moeten worden opgenomen.

### Beperking van zoekresultaten voor HIPAA-klanten

De HIPAA-functionaliteit voor het beperken van zoekresultaten bij klanten in Adobe Commerce zorgt voor naleving van HIPAA-regels door de toegang tot Protected Health Information (PHI) en Persoonlijk Identified Information (PII) te beperken. Deze eigenschap beperkt de capaciteit om klantenverslagen te zoeken en te bekijken die op gebruikersrollen worden gebaseerd, die ervoor zorgen dat slechts de erkende gebruikers tot deze informatie kunnen toegang hebben.

#### Belangrijkste kenmerken

- **de Beperkingen van het Onderzoek**: De gebruikers zonder de noodzakelijke rollen kunnen niet naar klantenverslagen zoeken of bekijken.
- **Verplicht Onderzoek naar Toegang**: In tegenstelling tot het standaardgedrag van Adobe Commerce, is het niet mogelijk om klanteninformatie te zien zonder een onderzoek uit te voeren. Dit zorgt ervoor dat de gebruikers specifieke details over een klant moeten kennen om van hun informatie de plaats te bepalen.
- **Beperkte Resultaten van het Onderzoek**: De resultaten van het onderzoek die de criteria aanpassen zijn beperkt tot 10 verslagen, die ervoor zorgen dat slechts een handelbaar aantal verslagen tegelijkertijd worden getoond.
- **Minimum Aantal Filters**: De gebruikers moeten een minimum van drie filters (b.v., e-mail, lastname, en staat) toepassen om een onderzoek uit te voeren, ervoor zorgend dat de onderzoeken specifiek en gericht zijn.
- **de Berichten van de Filter**: Wanneer de onderzoeksbeperkingen worden toegelaten, worden de gebruikers meegedeeld om filters toe te passen om hun onderzoeksresultaten te verfijnen.

#### Configuratie

De configuratie voor het beperken van het aantal klanten in de zoekresultaten vindt u in het deelvenster Beheer onder **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]** . Deze configuratie is standaard ingeschakeld wanneer de extensie `hipaa-ee` wordt geïnstalleerd.

- **Aantal Klanten van de Grens in Net**: Dit het plaatsen staat u toe om de beperking op het aantal klanten toe te laten of onbruikbaar te maken die in de resultaten van het netonderzoek worden getoond.
- **Limiet van het Resultaat van het Net van de Klant**: Dit het plaatsen specificeert het maximumaantal klantenverslagen die in de resultaten van het netonderzoek kunnen worden getoond.

#### Betrokken functionele gebieden

De beperkingsfunctionaliteit van de zoekresultaten is van invloed op de rasters van de klant op de pagina Bestelling maken (**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]** ) en de pagina Klanten ( **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** ).

- Filters worden standaard geopend.
- Gebruikers moeten minimaal drie filters toepassen om een zoekopdracht uit te voeren.
- De zoekresultaten zijn standaard beperkt tot 10 records.
- Als er meer records zijn die aan de zoekcriteria voldoen, worden gebruikers op de hoogte gebracht van de resultaatlimiet en van de noodzaak hun zoekopdracht te verfijnen.
- Rasterpaginering is niet beschikbaar.
- Eerdere zoekresultaten en toegepaste filters worden niet opgeslagen wanneer u van de pagina af navigeert.

De de beperkingsfunctionaliteit van onderzoeksresultaten is ook van toepassing op REST API voor klantenonderzoek (`/V1/customers/search`).

- Zonder toegepaste filters of met onvoldoende filters retourneert de API een foutbericht dat het vereiste aantal filters nodig is om een zoekopdracht uit te voeren.
- Wanneer voldoende filters worden toegepast door geautoriseerde gebruikers, retourneert de API de resultaten binnen de opgegeven limiet.
- Wanneer de resultaten beperkt zijn, wordt een bericht toegevoegd aan de reactie die op het totale aantal gevonden verslagen en de huidige toegepaste grens wijst.

### Functies importeren en exporteren

Verbeteringen in de functies voor importeren en exporteren zijn gericht op het verbeteren van de beheerervaring en het bieden van een betere zichtbaarheid in gebruikersacties.

>[!NOTE]
>
>Deze ***verhogingen veranderen niet de de kernlogica van de Invoer en van de Uitvoer***; eerder, breiden zij de functionaliteit uit om uitvoeriger registreren en betere gegevensattributie aan te bieden. De fundamentele functionaliteit van importeren en exporteren blijft ongewijzigd. Gebruikers kunnen de bestaande functies en workflows blijven gebruiken zonder onderbreking.

#### Logboek van administratieve handelingen

Een van de belangrijkste verbeteringen in de import- en exportfuncties is de verbeterde registratie van administratieve handelingen. Deze verbetering introduceert de mogelijkheid om dieper in te gaan op activiteiten die verband houden met het importeren en exporteren van gegevens en zo bij te dragen tot een betere traceerbaarheid en controleerbaarheid. De volgende acties worden nu vastgelegd en weerspiegeld in het raster **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Type | Handelingen |
| ---- | ------- |
| Importeren | <ul><li>Een Admin-gebruiker voert een import uit<li>Een Admin-gebruiker downloadt een geïmporteerd bestand<li>Een beheerder downloadt een foutbestand<ul/> |
| Exporteren | <ul><li>Een Admin-gebruiker<li>Een Admin-gebruiker downloadt een geëxporteerd bestand<ul/> |
| Geplande import/export | <ul><li>Een Admin-gebruikersschema&#39;s exporteren<li>Een Admin-gebruiker bewerkt een geplande export<li>Een Admin-gebruiker voert een geplande export uit<li>Een Admin-gebruiker verwijdert een geplande export<li>Een Admin-gebruiker plant het importeren<li>Een Admin-gebruiker bewerkt een geplande import<li>Een Admin-gebruiker voert een geplande import uit<li>Een Admin-gebruiker verwijdert een geplande import<li>Een Admin-gebruiker voert een bulksgewijs verwijderen van import-/exportbewerkingen uit<ul/> |

### Verbeteringen weergeven en filteren en sorteren verbeteren

Om Admin gebruikers met meer informatieve netten te machtigen, verstrekt de HIPAA-Klaar dienst verscheidene verhogingen aan vertoning, filter, en soortgegevens.

#### Historie importeren ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filteren ingeschakeld voor alle kolommen behalve **[!UICONTROL Imported File]** , **[!UICONTROL Error File]** , **[!UICONTROL Execution Time]** en **[!UICONTROL Summary]** .

#### Exporteren ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Er is een kolom **[!UICONTROL ID]** toegevoegd.
- Toegevoegd a **[!UICONTROL Requested At]** kolom (_datum en tijd toen de uitvoer werd gevraagd_).
- Toegevoegd a **[!UICONTROL User]** kolom (_gebruikersbenaming van admin die het verzoek_) deed.
- Een kolom **[!UICONTROL Action]** is verwijderd.
- Verplaatst de **[!UICONTROL Download]** verbinding naar a **[!UICONTROL File name]** kolom (_als het net van de Geschiedenis van de Invoer_).
- Uitgeschakeld de actie verantwoordelijk voor schrapping van een uitgevoerd dossier (_om het volgen_ te verbeteren).
- sorteren ingeschakeld voor alle kolommen behalve **[!UICONTROL File name]** .
- Filteren ingeschakeld voor alle kolommen.

#### Geplande import en export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Er is een kolom **[!UICONTROL ID]** toegevoegd.
- Toegevoegd a **[!UICONTROL Scheduled At]** kolom (de _datum en de tijd toen de invoer of de uitvoer_ gepland waren).
- Toegevoegd a **[!UICONTROL User]** kolom (de _gebruikersbenaming van een gebruiker Admin die de invoer of de uitvoer_ plaatste).

## HIPAA-services en -tools

In deze sectie worden de Adobe-services beschreven die klaar zijn voor HIPAA en die kunnen worden gebruikt met de HIPAA-aanbieding voor Adobe Commerce. Het beschrijft ook hulpmiddelen die u kunt gebruiken helpen zeer belangrijke veiligheid en nalevingscontroles voor uw opslag controleren.

| Service | Productie | Staging | staging_for_support | Ontwikkeling |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce met invoegtoepassing voor gezondheidszorg | Ja | Ja | Ja | Nee |
| SendGrid | Nee | Nee | Nee | Nee |
| AWS Simple Email Service | Ja | Ja | Ja | Nee |

### Adobe Commerce Services

De volgende lijst identificeert de diensten van Adobe Commerce die voor het HIPAA-bereidheid aanbieden beschikbaar zijn. Deze diensten omvatten, maar zijn niet beperkt tot:

| Service | Niet-productie | Productie |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [ Adobe Developer App Builder ](https://developer.adobe.com/app-builder/docs/overview/) | Ja | Ja |
| [ API Net voor Adobe Developer App Builder ](https://developer.adobe.com/graphql-mesh-gateway/) | Ja | Ja |
| [ de Uitvoer van Gegevens SaaS ](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) | Ja | Ja |
| [ Levend Onderzoek ](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) | Nee | Nee |
| [ Aanbevelingen van het Product ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | Nee | Nee |
| [ de Diensten van de Betaling ](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview) | Nee | Nee |
| [ De Gebeurtenissen van het Bureau van de Verbinding van Gegevens achteraan ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | Ja | Ja |
| [ de Gebeurtenissen van de Opslag van de Verbinding van Gegevens ](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#storefront-events) | Nee | Nee |
| [ Audience Activation ](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | Nee | Nee |

### Gereedschappen

Het [ Hulpmiddel van het Scannen van de Veiligheid ](../../systems/security-scan.md) voor Adobe Commerce helpt u uw opslag controleren om ervoor te zorgen dat alle vereiste veiligheidscontroles worden toegelaten en operationeel. Naast de standaard veiligheidscontroles, heeft Adobe het hulpmiddel verbeterd om HIPAA-specifieke controles voor klanten te tonen die het aanbieden van HIPAA voor Adobe Commerce gebruiken. De controles HIPAA in het Hulpmiddel van het Scannen van de Veiligheid worden ontworpen om ervoor te zorgen dat:

- De controlemodules zijn niet uitgeschakeld
- Tweevoudige verificatie (2FA) is niet uitgeschakeld
- Marketingfuncties zijn uitgeschakeld
- Alle geïnstalleerde extensies komen overeen met een vooraf gedefinieerde lijst van gewenste personen
- Geen niet-ondersteunde Adobe-services geïnstalleerd

U kunt [ het hulpmiddel ](../../systems/security-scan.md#run-a-security-scan) vormen om u e-mailberichten met details van geplande scans of [ manueel meningsrapporten ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report) te verzenden.

## Uitgeschakelde functies

Om aan HIPAA-vereisten te voldoen, zijn sommige functies die door Adobe Commerce worden ondersteund, niet standaard beschikbaar of uitgeschakeld. Handelaren hebben de mogelijkheid om deze functies op eigen risico weer in te schakelen of te gebruiken.

De volgende functies zijn standaard uitgeschakeld in de HIPAA-gereedheidsmodule. Handelaren kunnen al deze functies op eigen risico inschakelen.

- **[Transactionele e-mail ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** - SendGrid wordt onbruikbaar gemaakt door gebrek omdat de dienst niet-HIPAA-klaar is. Adobe Commerce verstrekt een integratieoptie die u met uw eigen [ Eenvoudige van AWS E-mailDienst ](https://docs.aws.amazon.com/ses/) rekening kunt gebruiken. Neem contact op met de technische accountmanager van de klant of de Adobe Commerce-ondersteuning voor configuratiegegevens.

- **[controle van de Gast](../../stores-purchase/checkout-guest.md)** - Deze eigenschap stelt een potentieel risico voor diverse aspecten van HIPAA met inbegrip van registreren, toegangsbeheer, hygiëne PHI en lijn, en potentieel meer voor.

- **[eigenschap van het Nieuwsbrief](../../merchandising-promotions/newsletters.md)** - Deze eigenschap wordt onbruikbaar gemaakt om PHI te verhinderen die in een marketing context wordt gebruikt.

- **[Geavanceerde het Melden van dienst die](../../getting-started/business-intelligence.md)** plaatsen-Deze configuratie wordt geplaatst onbruikbaar gemaakt om PHI te verhinderen voor analyse en rapportering worden gebruikt.
