---
title: HIPAA-gereedheid op Adobe Commerce
description: Ontdek hoe u de Adobe Commerce HIPAA-Ready-extensie kunt toevoegen en extra functies en functionaliteiten kunt krijgen waarmee u aan uw HIPAA-verplichtingen kunt voldoen.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: bce0e581e89139875e09b671038a21976eccebca
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 1%

---

# HIPAA-gereedheid op Adobe Commerce

>[!IMPORTANT]
>
>**Juridische Disclaimer**<br/>
>Deze informatie is bedoeld om Adobe klanten te helpen hun vragen betreffende de HIPAA-Klaar Diensten van de Adobe beantwoorden. Het is geen juridisch advies. Handelaren moeten hun eigen juridische adviseur raadplegen om te begrijpen wat hun verplichtingen zijn in het kader van de HIPAA en wat het juiste gebruik en de juiste configuratie van de producten van de Adobe is.

>[!BEGINSHADEBOX]

**de Portabiliteit en de Verantwoording van de Verzekering van de Gezondheid (HIPAA)**

De Health Insurance Portability and Accountability Act (HIPAA) is de belangrijkste federale privacywet voor gezondheidszorg in de Verenigde Staten en wordt gehandhaafd door het Amerikaanse ministerie van Gezondheid en Menselijke Diensten (HHS). HIPAA is op _Bedekte Entiteiten_ (zoals gezondheidszorgleveranciers, verzekeraars, en clearinghuizen) en _BedrijfsVennoten_ (zoals die entiteiten van toepassing die de diensten aan overdekte entiteiten verlenen) van toepassing. De vereisten van HIPAA worden geplaatst over drie afzonderlijke regels: de Regel van de Privacy, de Regel van de Veiligheid, en de Regel van het Bericht van het Schending. De Adobe treedt als BedrijfsVennoot voor bepaalde producten op, die de Adobe als &quot;HIPAA-Klaar Diensten&quot;classificeert. Gegevens die onder HIPAA worden gereguleerd worden bedoeld als _Beschermde Informatie van de Gezondheid_ of PHI. PHI is een subset van gezondheidsinformatie die (1) wordt gecreëerd of ontvangen door een zorgaanbieder, een gezondheidsplan of een clearinghouse voor de gezondheidszorg, (2) betrekking heeft op het verleden, het heden of de toekomstige lichamelijke of geestelijke gezondheid of toestand van een individu, de verstrekking van gezondheidszorg aan een individu, of de eerdere, huidige of toekomstige betaling voor de verstrekking van gezondheidszorg aan een individu, en (3) de persoon identificeert of ten aanzien waarvan er een redelijke basis voor bestaat informatie kan worden gebruikt om het individu te identificeren. De HIPAA-privacy- en beveiligingsregels vereisen dat een onder de overeenkomst vallende entiteit schriftelijke garanties krijgt van een Business Associate in de vorm van een Business Associate Agreement, of BAA, waarbij de Business Associate wordt verplicht de privacy en veiligheid van de PHI van de onder de overeenkomst vallende entiteit te waarborgen. Voor meer informatie, zie [ HIPAA en de Producten en de Diensten van de Adobe ](https://www.adobe.com/trust/compliance/hipaa-ready.html) in het Centrum van het Vertrouwen van de Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA gereed

De Adobe Commerce HIPAA-Ready-uitbreiding voegt extra functies en functies toe aan Adobe Commerce-installaties die handelaren in staat stellen te voldoen aan hun respectieve HIPAA-verplichtingen.

De Adobe Commerce HIPAA-Ready-extensie `magento/hipaa-ee` is beschikbaar voor Adobe Commerce op cloudinfrastructuur of Managed Services-projecten voor Adobe. Het Adobe Commerce HIPAA-Klaar installatieproces maakt sommige inheemse diensten en eigenschappen onbruikbaar om aan vereisten te voldoen HIPAA. Zie [ Gehandicapte diensten en eigenschappen ](#disabled-services-and-features).

>[!NOTE]
>
>Toegang tot functies en functionaliteit die klaar zijn voor HIPAA is alleen beschikbaar voor handelaren die de invoegtoepassing voor gezondheidszorg voor Adobe Commerce hebben aangeschaft.

*Deze materialen zijn voorgenomen voor informatieve slechts doeleinden. Het verstrekken van deze informatie geeft de ontvanger geen recht op contractuele of andere rechten. Er zijn inspanningen geleverd om de juistheid van de informatie te waarborgen vanaf de datum waarop deze is verstrekt, maar er zijn geen aanwijzingen dat deze informatie juist en volledig is. Adobe verbindt zich ertoe deze informatie niet bij te werken wanneer de wet of de Adobe haar producten wijzigt. Dit document mag ook niet zonder schriftelijke toestemming van de Adobe worden verspreid naar een andere partij dan de beoogde ontvanger.*

## Systeemvereisten

Adobe Commerce moet worden geïmplementeerd op Adobe Commerce op cloudinfrastructuur of op Adobe Commerce Managed Services met versie 2.4.6-p3 of hoger (geen bètaversies).

## Installatie

**Vereiste**

>[!BEGINSHADEBOX]

- Adobe heeft uw Adobe Commerce-account ingericht voor toegang tot de HIPAA Ready-extensie.
- Toegang tot [ repo.magento.com ](https://repo.magento.com) om de uitbreiding te installeren. Voor zeer belangrijke generatie en het verkrijgen van de noodzakelijke rechten, zie [ uw authentificatiesleutels ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) krijgen.

>[!ENDSHADEBOX]

Installeer de recentste versie van de uitbreiding van de Diensten van HIPAA-Klaar van de Adobe (`magento/hipaa-ee`) op een instantie die versie 2.4.6-p3 of later van Adobe Commerce in werking stelt. De uitbreiding wordt geleverd als composer metapack van de {](https://repo.magento.com) bewaarplaats 0} repo.magento.com. [ Het metapakket omvat de inzameling van modules die de mogelijkheden HIPAA voor een instantie van Adobe Commerce toelaten.

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
   <truncated for brevity>
   ```

   Alle modules die met `Magento_Hipaa` worden voorgefixeerd moeten in de toegelaten modulessectie zijn.

## Verbeterde functies voor HIPAA-gereedheid

De extensie `magento/hipaa-ee` bevat enkele wijzigingen en verbeteringen voor het basis-Commerce-product. De volgende secties verstrekken details over deze veranderingen en hoe zij het basisproduct veranderen.

### Handelingenlogboeken

Controle het Registreren is een vereiste van HIPAA. In Adobe Commerce, registreert de ](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) eigenschap van de Actie 0} {elke verandering die door een gebruiker wordt aangebracht Admin die in uw opslag werkt. [ Om aan de vereisten van HIPAA voor het Logboek van de Controle te voldoen, is de eigenschap bijgewerkt om alle Admin gebruikers en klantenacties te registreren die door Admin UI en door API vraag worden uitgevoerd.

#### Rapport Action Logs

Het _Logs van de Actie_ rapportnet (**[!UICONTROL System]** > Logboeken van de Actie > Rapport) wordt gewijzigd om klantenacties aan te passen die door Admin UI en API worden uitgevoerd.

1. Twee kolommen toegevoegd:
   - ***Source***: Toont waar de actie werd uitgevoerd.
Waarden: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Type van Cliënt***: Toont het cliënttype.
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

### Functies importeren en exporteren

Verbeteringen in de functies voor importeren en exporteren zijn gericht op het verbeteren van de beheerervaring en het bieden van een betere zichtbaarheid in gebruikersacties.

>[!NOTE]
>
>Deze ***verhogingen veranderen niet de de kernlogica van de Invoer en van de Uitvoer***; eerder, breiden zij de functionaliteit uit om uitvoeriger registreren en betere gegevensattributie aan te bieden. De fundamentele functionaliteit van importeren en exporteren blijft ongewijzigd. Gebruikers kunnen de bestaande functies en workflows blijven gebruiken zonder onderbreking.

#### Logboek van administratieve handelingen

Een van de belangrijkste verbeteringen in de import- en exportfuncties is de verbeterde registratie van administratieve handelingen. Deze verbetering introduceert de mogelijkheid om dieper in te gaan op activiteiten die verband houden met het importeren en exporteren van gegevens en zo bij te dragen tot een betere traceerbaarheid en controleerbaarheid. De volgende acties worden nu vastgelegd en weerspiegeld in het raster **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Type | Handelingen |
| ---- | ------- |
| Importeren | <ul><li>Een Admin-gebruiker voert een importbewerking uit<li>Een Admin-gebruiker downloadt een geïmporteerd bestand<li>Een Admin-gebruiker downloadt een foutbestand<ul/> |
| Exporteren | <ul><li>Een Admin-gebruiker<li>Een Admin-gebruiker downloadt een geëxporteerd bestand<ul/> |
| Geplande invoer/uitvoer | <ul><li>Een Admin-gebruikersschema&#39;s exporteren<li>Een Admin-gebruiker bewerkt een geplande export<li>Een Admin-gebruiker voert een geplande export uit<li>Een Admin-gebruiker verwijdert een geplande export<li>Een Admin-gebruiker plant het importeren<li>Een Admin-gebruiker bewerkt een geplande import<li>Een Admin-gebruiker voert een geplande import uit<li>Een Admin-gebruiker verwijdert een geplande import<li>Een Admin-gebruiker voert een bulksgewijs verwijderen van import-/exportbewerkingen uit<ul/> |

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

## Uitgeschakelde services en functies

Om aan HIPAA-vereisten te voldoen, zijn sommige services en functies die door Adobe Commerce worden ondersteund, niet standaard beschikbaar of uitgeschakeld. Handelaren hebben de mogelijkheid deze diensten en kenmerken op eigen risico weer in te schakelen of te gebruiken.

### Services

- **de diensten van Adobe Commerce** - niets van de diensten of de rekbaarheidsdiensten van Adobe Commerce zijn beschikbaar onder het HIPAA-bereidheid aanbieden. Deze diensten omvatten, maar zijn niet beperkt tot:

   - Live zoeken
   - API-net
   - App Builder

- **[dienst SendGrid ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** - Deze dienst wordt onbruikbaar gemaakt door gebrek omdat de toepassing niet-HIPAA-volgzaam is.

### Functies die standaard zijn uitgeschakeld

De volgende functies zijn standaard uitgeschakeld in de HIPAA-gereedheidsmodule. Handelaren kunnen al deze functies op eigen risico inschakelen.

- **[controle van de Gast](../stores-purchase/checkout-guest.md)** - Deze eigenschap stelt een potentieel risico voor diverse aspecten van HIPAA met inbegrip van registreren, toegangsbeheer, hygiëne PHI en lijn, en potentieel meer voor.

- **[eigenschap van het Nieuwsbrief](../merchandising-promotions/newsletters.md)** - Deze eigenschap wordt onbruikbaar gemaakt om PHI te verhinderen die in een marketing context wordt gebruikt.

- **[Geavanceerde het Melden van de dienst die](../getting-started/business-intelligence.md)** plaatst - Deze configuratie die wordt onbruikbaar gemaakt om PHI te verhinderen voor analyse en rapportering worden gebruikt.
