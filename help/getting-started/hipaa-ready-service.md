---
title: HIPAA-gereedheid op Adobe Commerce
description: Leer hoe u de Adobe Commerce HIPAA-Klaar module kunt toevoegen en extra eigenschappen en functionaliteiten krijgt die u toestaan om aan uw verplichtingen van HIPAA te voldoen.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# HIPAA-gereedheid op Adobe Commerce

>[!IMPORTANT]
>
>**Rechtsvordering**<br/>
>Deze informatie is bedoeld om Adobe klanten te helpen hun vragen betreffende de HIPAA-Klaar Diensten van de Adobe beantwoorden. Het is geen juridisch advies. Handelaren moeten hun eigen juridische adviseur raadplegen om te begrijpen wat hun verplichtingen zijn in het kader van de HIPAA en wat het juiste gebruik en de juiste configuratie van de producten van de Adobe is.

>[!BEGINSHADEBOX]

**Health Insurance Portability and Accountability Act (HIPAA)**

De Health Insurance Portability and Accountability Act (HIPAA) is de belangrijkste federale privacywet voor gezondheidszorg in de Verenigde Staten en wordt gehandhaafd door het Amerikaanse ministerie van Gezondheid en Menselijke Diensten (HHS). HIPAA geldt voor _Gedekte entiteiten_ (zoals zorgaanbieders, verzekeraars en clearinghuizen) en _Zakelijke partners_ (zoals die entiteiten die diensten verlenen aan onder deze richtlijn vallende entiteiten). De vereisten van HIPAA worden geplaatst over drie afzonderlijke regels: de Regel van de Privacy, de Regel van de Veiligheid, en de Regel van het Bericht van het Schending. De Adobe treedt als BedrijfsVennoot voor bepaalde producten op, die de Adobe als &quot;HIPAA-Klaar Diensten&quot;classificeert. Gegevens die onder HIPAA vallen, worden aangeduid als _Beschermde gezondheidsinformatie_ of PHI. PHI is een subset van gezondheidsinformatie die (1) wordt gecreëerd of ontvangen door een zorgaanbieder, een gezondheidsplan of een clearinghouse voor de gezondheidszorg, (2) betrekking heeft op het verleden, het heden of de toekomstige lichamelijke of geestelijke gezondheid of toestand van een individu, de verstrekking van gezondheidszorg aan een individu, of de eerdere, huidige of toekomstige betaling voor de verstrekking van gezondheidszorg aan een individu, en (3) de persoon identificeert of ten aanzien waarvan er een redelijke basis voor bestaat informatie kan worden gebruikt om het individu te identificeren. De HIPAA-privacy- en beveiligingsregels vereisen dat een onder de overeenkomst vallende entiteit schriftelijke garanties krijgt van een Business Associate in de vorm van een Business Associate Agreement, of BAA, waarbij de Business Associate wordt verplicht de privacy en veiligheid van de PHI van de onder de overeenkomst vallende entiteit te waarborgen. Zie voor meer informatie [HIPAA en de Producten en de Diensten van de Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) in het Adobe Trust Center.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA gereed

Adobe Commerce HIPAA-Ready beschikt over extra functies en functies waarmee handelaren hun respectieve HIPAA-verplichtingen kunnen nakomen.

Adobe Commerce HIPAA-Ready wordt geleverd als een Adobe Commerce-extensie, `magento/hipaa-ee` die beschikbaar is voor Adobe Commerce op wolkeninfrastructuur of Adobe-Managed Services-projecten. Het Adobe Commerce HIPAA-Klaar installatieproces maakt sommige inheemse diensten en eigenschappen onbruikbaar om aan vereisten te voldoen HIPAA. Zie [Uitgeschakelde services en functies](#disabled-services-and-features).

*Deze materialen zijn uitsluitend bestemd voor informatieve doeleinden. Het verstrekken van deze informatie geeft de ontvanger geen recht op contractuele of andere rechten. Er zijn inspanningen geleverd om de juistheid van de informatie te waarborgen vanaf de datum waarop deze is verstrekt, maar er zijn geen aanwijzingen dat deze informatie juist en volledig is. Adobe verbindt zich ertoe deze informatie niet bij te werken wanneer de wet of de Adobe haar producten wijzigt. Dit document mag ook niet zonder schriftelijke toestemming van de Adobe worden verspreid onder een andere partij dan de beoogde ontvanger.*

## Systeemvereisten

Adobe Commerce moet worden geïmplementeerd op Adobe Commerce op cloudinfrastructuur of op Adobe Commerce Managed Services met versie 2.4.6-p3 of hoger (geen bètaversies).

## Installatie

Installeer de nieuwste versie van de HIPAA-Ready Services-extensie van de Adobe (`magento/hipaa-ee`) op een instantie die Adobe Commerce versie 2.4.6-p3 of hoger uitvoert. De extensie wordt geleverd als een componentmetapakket vanuit de [repo.magento.com](https://repo.magento.com) opslagplaats.

>[!BEGINSHADEBOX]

**Vereiste**

U moet toegang hebben tot [repo.magento.com](https://repo.magento.com) om de extensie te installeren. Voor sleutelgeneratie en het verkrijgen van de nodige rechten, zie [Uw verificatietoetsen ophalen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. Schakel op uw lokale werkstation de projectmap voor uw Adobe Commerce over het infrastructuurproject voor de cloud in.

   >[!NOTE]
   >
   >Voor informatie over het lokale beheer van Commerce-projectomgevingen raadpleegt u  [Het leiden van takken met CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) in de _Gebruikershandleiding Adobe Commerce on Cloud Infrastructure_.

1. Check de omgevingsvertakking uit om bij te werken met de Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. De metapakket toevoegen `magento/hipaa-ee` aan de componentenconfiguratie die composer CLI gebruikt.

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

   Als u op de updates drukt, wordt het dialoogvenster [Commerce-implementatieproces voor cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) om de wijzigingen toe te passen. Controleer de implementatiestatus via de [logboek implementeren](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Installatie controleren

Nadat de updates worden opgesteld, verifieer dat `Hipaa*` extensie is geïnstalleerd

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
   <truncated for brevity>
   ```

   Alle modules vooraf uitgerust met `Magento_Hipaa` moet in de toegelaten modulessectie zijn.

## Verbeterde functies voor HIPAA-gereedheid

De `magento/hipaa-ee` bevat enkele wijzigingen en verbeteringen voor het basis-Commerce-product. De volgende secties verstrekken details over deze veranderingen en hoe zij het basisproduct veranderen.

### Handelingenlogboeken

Controle het Registreren is een vereiste van HIPAA. In Adobe Commerce [Handelingenlogboeken](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) registreert elke wijziging die wordt aangebracht door een Admin-gebruiker die in uw winkel werkt. Om aan de vereisten van HIPAA voor het Logboek van de Controle te voldoen, is de eigenschap bijgewerkt om alle Admin gebruikers en klantenacties te registreren die door Admin UI en door API vraag worden uitgevoerd.

#### Rapport Action Logs

De _Handelingenlogboeken_ rapportraster (**[!UICONTROL System]** > Handelingenlogboeken > Rapport) wordt aangepast aan acties van klanten die via de interface van Admin en de API worden uitgevoerd.

1. Twee kolommen toegevoegd:
   - ***Bron***: Geeft weer waar de handeling is uitgevoerd.
Waarden: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Type client***: Geeft het clienttype weer.
Waarden: Klant | Beheerder | Integratie

2. De naam van de ***Gebruikersnaam*** kolonie naar ***Client-id***
   - ***Client-id***: Hiermee geeft u de aanmeldings-id weer voor de gebruiker die de handeling heeft uitgevoerd.
Waarden:
      - een e-mail als het Type van Cliënt Klant is
      - een gebruikersnaam als het type client beheerder is
      - een naam als het Type van Cliënt Integratie is

3. De naam van de ***Volledige naam van handeling*** kolom naar ***Doel***
   - ***Doel***: Geeft de naam van de handeling weer.
Waarden:
      - een eindpunt als Bron een REST API of SOAP API is
      - een naam voor query&#39;s of mutaties als een GraphQL API
      - een handelingnaam als een beheerdersinterface of gebruikersinterface van de klant.

#### Beheerdersacties configureren voor logbestanden

Deze functie is niet beschikbaar omdat alle handelingen standaard moeten worden opgenomen.

### Functies importeren en exporteren

Verbeteringen in de functies voor importeren en exporteren zijn gericht op het verbeteren van de beheerervaring en het bieden van een betere zichtbaarheid in gebruikersacties.

>[!NOTE]
>
>Deze ***de verbeteringen hebben geen invloed op de kernlogica voor importeren en exporteren*** De functionaliteit wordt eerder uitgebreid, zodat een uitgebreidere registratie en een betere gegevenstoewijzing mogelijk zijn. De fundamentele functionaliteit van importeren en exporteren blijft ongewijzigd. Gebruikers kunnen de bestaande functies en workflows blijven gebruiken zonder onderbreking.

#### Logboek van administratieve handelingen

Een van de belangrijkste verbeteringen in de import- en exportfuncties is de verbeterde registratie van administratieve handelingen. Deze verbetering introduceert de mogelijkheid om dieper in te gaan op activiteiten die verband houden met het importeren en exporteren van gegevens en zo bij te dragen tot een betere traceerbaarheid en controleerbaarheid. De volgende acties worden nu vastgelegd en weerspiegeld in het dialoogvenster **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**raster:

| Type | Handelingen |
| ---- | ------- |
| Importeren | <ul><li>Een Admin-gebruiker voert een importbewerking uit<li>Een Admin-gebruiker downloadt een geïmporteerd bestand<li>Een Admin-gebruiker downloadt een foutbestand<ul/> |
| Exporteren | <ul><li>Een Admin-gebruiker<li>Een Admin-gebruiker downloadt een geëxporteerd bestand<ul/> |
| Geplande invoer/uitvoer | <ul><li>Een Admin-gebruikersschema&#39;s exporteren<li>Een Admin-gebruiker bewerkt een geplande export<li>Een Admin-gebruiker voert een geplande export uit<li>Een Admin-gebruiker verwijdert een geplande export<li>Een Admin-gebruiker plant het importeren<li>Een Admin-gebruiker bewerkt een geplande import<li>Een Admin-gebruiker voert een geplande import uit<li>Een Admin-gebruiker verwijdert een geplande import<li>Een Admin-gebruiker voert een bulksgewijs verwijderen van import-/exportbewerkingen uit<ul/> |

### Verbeteringen weergeven en filteren en sorteren verbeteren

Om Admin gebruikers met meer informatieve netten te machtigen, verstrekt de HIPAA-Klaar dienst verscheidene verhogingen aan vertoning, filter, en soortgegevens.

#### Historie importeren ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Ingeschakeld filteren voor alle kolommen behalve voor **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, en **[!UICONTROL Summary]**.

#### Exporteren ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Toegevoegde **[!UICONTROL ID]** kolom.
- Toegevoegde **[!UICONTROL Requested At]** kolom (_datum en tijdstip waarop uitvoer is aangevraagd_).
- Toegevoegde **[!UICONTROL User]** kolom (_gebruikersnaam van een beheerder die het verzoek heeft gedaan_).
- Een **[!UICONTROL Action]** kolom.
- Verplaatst **[!UICONTROL Download]** koppeling naar een **[!UICONTROL File name]** kolom (_zoals het raster Historie importeren_).
- De handeling die verantwoordelijk is voor het verwijderen van een geëxporteerd bestand (_de tracering verbeteren_).
- sorteren ingeschakeld voor alle kolommen behalve **[!UICONTROL File name]**.
- Filteren ingeschakeld voor alle kolommen.

#### Geplande invoer en uitvoer ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Toegevoegde **[!UICONTROL ID]** kolom.
- Toegevoegde **[!UICONTROL Scheduled At]** kolom (de _datum en tijdstip waarop de import of export gepland was_).
- Toegevoegde **[!UICONTROL User]** kolom (de _gebruikersnaam van een Admin-gebruiker die het importeren of exporteren heeft gepland_).

## Uitgeschakelde services en functies

Om aan HIPAA-vereisten te voldoen, zijn sommige services en functies die door Adobe Commerce worden ondersteund, niet standaard beschikbaar of uitgeschakeld. Handelaren hebben de mogelijkheid deze diensten en kenmerken op eigen risico weer in te schakelen of te gebruiken.

### Services

- **Adobe Commerce-services**—Geen van de diensten van Adobe Commerce of rekbaarheidsdiensten zijn beschikbaar onder het HIPAA-bereidheid aanbieden. Deze diensten omvatten, maar zijn niet beperkt tot:

   - Live zoeken
   - API-net
   - App Builder
   - Catalogusservice

- **[SendGrid-service](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—Deze service is standaard uitgeschakeld omdat de toepassing niet HIPAA-compatibel is. De handelaren kunnen een steunverzoek indienen om Sendgrid toe te laten, maar zij moeten erkennen dat zij het risico om de dienst te gebruiken nemen.

### Functies die standaard zijn uitgeschakeld

De volgende functies zijn standaard uitgeschakeld in de HIPAA-gereedheidsmodule. Handelaren kunnen al deze functies op eigen risico inschakelen.

- **[Uitchecken door gast](../stores-purchase/checkout-guest.md)**—Deze functie brengt een potentieel risico met zich mee voor diverse aspecten van HIPAA, zoals houtkap, toegangscontrole, PHI-hygiëne en lineage, en mogelijk nog meer.

- **[Nieuwsbrief](../merchandising-promotions/newsletters.md)**—Deze functie is uitgeschakeld om te voorkomen dat PHI wordt gebruikt in een marketingcontext.

- **[Geavanceerde instelling voor rapportservice](../getting-started/business-intelligence.md)**— Deze configuratie-instelling is uitgeschakeld om te voorkomen dat PHI wordt gebruikt voor analyse en rapportage.
