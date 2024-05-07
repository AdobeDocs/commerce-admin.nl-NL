---
title: HIPAA-gereedheid op Adobe Commerce
description: Leer hoe u de Adobe Commerce HIPAA-Klaar module kunt toevoegen en extra eigenschappen en functionaliteiten krijgt die u toestaan om aan uw verplichtingen van HIPAA te voldoen.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: c21c8b76e37e617885bae3492801b45093a6b5a5
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# HIPAA-gereedheid op Adobe Commerce

>[!IMPORTANT]
>
>**Rechtsvordering**<br/>
>Deze informatie is bedoeld om Adobe klanten te helpen hun vragen betreffende de HIPAA-Klaar Diensten van de Adobe beantwoorden. Het is geen juridisch advies. Handelaren moeten hun eigen juridische adviseur raadplegen om te begrijpen wat hun verplichtingen zijn in het kader van de HIPAA en wat het juiste gebruik en de juiste configuratie van de producten van de Adobe is.

## Health Insurance Portability and Accountability Act (HIPAA)

De Health Insurance Portability and Accountability Act (HIPAA) is de belangrijkste federale privacywet voor gezondheidszorg in de Verenigde Staten en wordt gehandhaafd door het Amerikaanse ministerie van Gezondheid en Menselijke Diensten (HHS). HIPAA geldt voor _Gedekte entiteiten_ (zoals zorgaanbieders, verzekeraars en clearinghuizen) en _Zakelijke partners_ (zoals die entiteiten die diensten verlenen aan onder deze richtlijn vallende entiteiten). De vereisten van HIPAA worden geplaatst over drie afzonderlijke regels: de Regel van de Privacy, de Regel van de Veiligheid, en de Regel van het Bericht van het Schending. De Adobe treedt als BedrijfsVennoot voor bepaalde producten op, die de Adobe als &quot;HIPAA-Klaar Diensten&quot;classificeert. Gegevens die onder HIPAA vallen, worden aangeduid als _Beschermde gezondheidsinformatie_ of PHI. PHI is een subset van gezondheidsinformatie die (1) wordt gecreëerd of ontvangen door een zorgaanbieder, een gezondheidsplan of een clearinghouse voor de gezondheidszorg, (2) betrekking heeft op het verleden, het heden of de toekomstige lichamelijke of geestelijke gezondheid of toestand van een individu, de verstrekking van gezondheidszorg aan een individu, of de eerdere, huidige of toekomstige betaling voor de verstrekking van gezondheidszorg aan een individu, en (3) de persoon identificeert of ten aanzien waarvan er een redelijke basis voor bestaat informatie kan worden gebruikt om het individu te identificeren. De HIPAA-privacy- en beveiligingsregels vereisen dat een onder de overeenkomst vallende entiteit schriftelijke garanties krijgt van een Business Associate in de vorm van een Business Associate Agreement, of BAA, waarbij de Business Associate wordt verplicht de privacy en veiligheid van de PHI van de onder de overeenkomst vallende entiteit te waarborgen.

## Adobe Commerce HIPAA gereed

Adobe Commerce HIPAA-Ready beschikt over extra functies en functies waarmee handelaren hun respectieve HIPAA-verplichtingen kunnen nakomen. U kunt de Adobe Commerce HIPAA-Ready installeren (`magento/hipaa-ee`) naar uw Adobe Commerce op cloudinfrastructuur. Er zijn ook enkele functies die moeten worden uitgeschakeld om compatibel te zijn met HIPAA.

*Deze materialen zijn uitsluitend bestemd voor informatieve doeleinden. Het verstrekken van deze informatie geeft de ontvanger geen recht op contractuele of andere rechten. Hoewel is getracht de juistheid van de informatie te waarborgen vanaf de datum waarop deze is verstrekt, wordt niet beweerd dat deze informatie juist en volledig is en verbindt de Adobe zich ertoe deze informatie niet bij te werken naarmate de wetgeving of de producten van de Adobe veranderen. Dit document mag ook niet zonder schriftelijke toestemming van de Adobe worden verspreid onder een andere partij dan de beoogde ontvanger.*

## Systeemvereisten

Voor HIPAA-gereedheid op Adobe Commerce gelden dezelfde systeemvereisten als voor Adobe Commerce met de aanvullende vereisten:

- Adobe Commerce versie 2.4.6-p3 of hoger (niet-bèta)
- Adobe Commerce op cloudinfrastructuur of Adobe Commerce op Managed Services
- Laatste versie van de `magento/hipaa-ee` extension

## Installatie

De HIPAA-Klaar Diensten van de Adobe is technisch een composer metapakket `magento/hipaa-ee` die verbindingen aan speciale modules bevat. Dit pakket van metapakketten bevindt zich in de opslagplaats [repo.magento.com](https://repo.magento.com).

1. Om te kunnen installeren `magento/hipaa-ee` metapakket, u moet toegang tot het hebben. Voor sleutelgeneratie en het verkrijgen van de noodzakelijke rechten, verwijs naar [Uw verificatietoetsen ophalen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Controleer de omgeving waarin u het pakket wilt installeren en zorg ervoor dat het voldoet aan de algemene [systeemvereisten](#system-requirements).

1. De metapakket toevoegen `magento/hipaa-ee` aan de componentenconfiguratie.

   De eenvoudigste manier is door composer CLI te gebruiken. Bijvoorbeeld:

   ```shell
   composer require magento/hipaa-ee
   ```

1. Als Adobe Commerce nog niet is geïnstalleerd, kunt u de installatie starten (volg de [Installatie-instructies](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Als Adobe Commerce al is geïnstalleerd, voert u deze na het downloaden van modules uit `bin/magento setup:upgrade` en volg de aanbevelingen.

   ```shell
   bin/magento setup:upgrade
   ```

   Wanneer deze opdracht wordt uitgevoerd, worden de nieuw gedownloade modules ingeschakeld en worden de scripts voor de installatie gestart. Meer over modulebeheer leren, zie [Modules in- of uitschakelen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. Nadat de installatie of het bijwerken proces is voltooid, moet u controleren of de `Hipaa*` er zijn relevante modules opgenomen .

   Voer de opdracht uit:

   ```shell
   bin/magento module:status
   ```

   Als het composer pakket HIPAA correct werd toegevoegd, ziet u de modules HIPAA in de output van het bevel. Bijvoorbeeld:

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

Controle het Registreren is een vereiste van HIPAA. In Adobe Commerce [Handelingenlogboeken](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) registreert elke wijziging die wordt aangebracht door een Admin-gebruiker die in uw winkel werkt. Om aan de vereisten van HIPAA over het Logboek van de Controle te voldoen, zijn er veranderingen in de eigenschap om alle Admin gebruikers en klantenacties te registreren die door Admin UI en door API vraag worden uitgevoerd.

#### Rapport Action Logs

De _Handelingenlogboeken_ rapportraster (**[!UICONTROL System]** > Handelingenlogboeken > Rapport) wordt aangepast aan acties van klanten die via de interface van Admin en de API worden uitgevoerd.

1. Twee extra kolommen:
   - ***Bron***: Geeft weer waar de handeling is uitgevoerd.\
     Waarden: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Type client***: Geeft het clienttype weer.\
     Waarden: Klant | Beheerder | Integratie


2. Naam wijzigen ***Gebruikersnaam*** tot ***Client-id***
   - ***Client-id***: Hiermee wordt de aanmeldings-id weergegeven voor de gebruiker die de handeling heeft uitgevoerd\
     Waarden:
      - een e-mail als het Type van Cliënt Klant is
      - een gebruikersnaam als het type client beheerder is
      - een naam als het Type van Cliënt Integratie is

3. Naam wijzigen ***Volledige naam van handeling*** tot ***Doel***
   - ***Doel***: Geeft de naam van de handeling weer\
     Waarden:
      - een eindpunt als Bron REST API of SOAP API is
      - een naam voor query/mutatie als GraphQL API
      - een naam voor een handeling als de interface van de beheerder of de gebruikersinterface van de klant.

#### Beheerdersacties configureren voor logbestanden

Deze functie is niet beschikbaar omdat alle handelingen standaard moeten worden opgenomen.

### Functies importeren/exporteren

Verbeteringen in de functies voor importeren/exporteren zijn gericht op het verbeteren van de beheerervaring en het bieden van een betere zichtbaarheid in gebruikersacties.

>[!NOTE]
>
>Deze ***Verbeteringen hebben geen invloed op de core-logica voor importeren/exporteren*** De functionaliteit wordt eerder uitgebreid, zodat een uitgebreidere registratie en een betere gegevenstoewijzing mogelijk zijn. De fundamentele functionaliteit van importeren/exporteren blijft ongewijzigd. Gebruikers kunnen de bestaande functies en workflows blijven gebruiken zonder onderbreking.

#### Logboek van administratieve handelingen

Een van de belangrijkste verbeteringen in de functie voor importeren/exporteren is de verbeterde registratie van administratieve handelingen. Hierdoor wordt de mogelijkheid geïntroduceerd om dieper in te gaan op activiteiten die verband houden met de invoer/uitvoer van gegevens en zo bij te dragen tot een betere traceerbaarheid en controleerbaarheid. De volgende acties worden nu vastgelegd en weerspiegeld in het dialoogvenster **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**raster:

| Type | Handelingen |
| ---- | ------- |
| Importeren | <ul><li>Een Admin-gebruiker voert een importbewerking uit<li>Een Admin-gebruiker downloadt een geïmporteerd bestand<li>Een Admin-gebruiker downloadt een foutbestand<ul/> |
| Exporteren | <ul><li>Een Admin-gebruiker<li>Een Admin-gebruiker downloadt een geëxporteerd bestand<ul/> |
| Geplande invoer/uitvoer | <ul><li>Een Admin-gebruikersschema&#39;s exporteren<li>Een Admin-gebruiker bewerkt een geplande export<li>Een Admin-gebruiker voert een geplande export uit<li>Een Admin-gebruiker verwijdert een geplande export<li>Een Admin-gebruiker plant het importeren<li>Een Admin-gebruiker bewerkt een geplande import<li>Een Admin-gebruiker voert een geplande import uit<li>Een Admin-gebruiker verwijdert een geplande import<li>Een Admin-gebruiker voert een bulksgewijs verwijderen van import-/exportbewerkingen uit<ul/> |

### Verbeteringen weergeven en filteren/sorteren verbeteren

Als u Admin-gebruikers meer informatieve rasters wilt geven, zijn er verschillende verbeteringen aangebracht in de weergave van gegevens en de mogelijkheden voor filteren en sorteren:

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

#### Geplande invoer/uitvoer ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Toegevoegde **[!UICONTROL ID]** kolom.
- Toegevoegde **[!UICONTROL Scheduled At]** kolom (_datum en tijdstip waarop de import of export gepland was_).
- Toegevoegde **[!UICONTROL User]** kolom (_gebruikersnaam van een Admin-gebruiker die de import/export heeft gepland_).

## Uitgeschakelde functies voor HIPAA-gereedheid

### SaaS-services

Geen van de SaaS-services die voor Adobe Commerce worden aangeboden, zijn beschikbaar in het kader van het HIPAA-readiness-aanbod. Dit omvat onder meer, maar is niet beperkt tot:

- Live zoeken
- API-net
- App Builder
- Catalogusservice

### Uitchecken door standaard uitgeschakelde gast

- Het uitchecken van gasten vormt een potentieel risico voor verschillende aspecten van HIPAA, zoals het kappen, toegangscontrole, PHI-hygiëne en lineage, en mogelijk nog meer.
- Afhandeling door gasten is standaard uitgeschakeld in de module HIPAA-gereedheid, maar dit kan door verkopers op eigen risico worden ingeschakeld.

### Standaard is de nieuwsbrief uitgeschakeld.

- De nieuwsbrief functie is standaard uitgeschakeld om te voorkomen dat PHI in een marketingcontext wordt gebruikt, maar kan door de handelaar op eigen risico worden ingeschakeld.

### Gehandicapte Geavanceerde dienst die van de Rapportering door gebrek plaatst

De Geavanceerde dienst die van de Rapportering wordt geplaatst is door gebrek gehandicapt om PHI te verhinderen voor analyse en rapportering worden gebruikt, maar kan door de handelaar op hun eigen risico worden toegelaten.

### Standaard uitgeschakelde Sendgrid-service

De service Sendgrid is standaard uitgeschakeld, omdat de toepassing niet compatibel is met HIPAA. De handelaren kunnen een steunverzoek indienen om Sendgrid toe te laten, maar zij moeten erkennen dat zij het risico zullen nemen om de dienst te gebruiken.
