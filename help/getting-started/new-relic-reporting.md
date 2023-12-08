---
title: '''[!DNL New Relic] rapporteren'
description: Meer informatie over de [!DNL New Relic] rapportage beschikbaar voor accounts voor Adobe Commerce op cloudinfrastructuur, inclusief de software voor de New Relic APM-service.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] rapportage

[New Relic][1] is een service voor softwareanalyse waarmee u de interactie tussen toepassingen kunt analyseren en verbeteren. De accounts van Adobe Commerce op de cloud-infrastructuur bevatten de software voor de [!DNL New Relic APM] service. Zie voor meer informatie [New Relic-services][4] in de _Handleiding voor handel in Cloud-infrastructuur_.

## Stap 1: Meld u aan voor een [!DNL New Relic] account

1. Ga naar de [[!DNL New Relic]][1] website en aanmelden voor een account.

   U kunt zich ook aanmelden voor een gratis proefaccount.

1. Volg de instructies op de site. Kies desgevraagd het product dat u als eerste wilt installeren.

1. Zoek in uw account naar de volgende referenties die nodig zijn om de configuratie voor Commerce te voltooien:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | Account-id | Van uw [!DNL New Relic] account-dashboard, de account-id is het nummer in de URL na: `/accounts` |
   | Toepassings-id | Van uw [!DNL New Relic] accountdashboard, klik op **[!UICONTROL New Relic APM]**. Kies in het menu **[!UICONTROL Applications]**. Kies vervolgens de toepassing. De toepassings-id is het nummer in de URL na: `/applications/` |
   | Nieuwe Relic-API-sleutel | Van uw [!DNL New Relic] accountdashboard, klik op **[!UICONTROL Account Settings]**. Kies in het menu aan de linkerkant onder Integratie de optie **[!UICONTROL Data Sharing]**. U kunt de API-sleutel van deze pagina maken, opnieuw genereren of verwijderen. |
   | API-sleutel voor inzichten | Van uw [!DNL New Relic] accountdashboard, klik op **[!UICONTROL Insights]**. Kies in het menu links onder Beheer de optie **[!UICONTROL API Keys]**. Uw API-sleutels voor inzichten worden op deze pagina weergegeven. Klik indien nodig op het plusteken (**+**) naast Toetsen invoegen om een toets te genereren. |

   {style="table-layout:auto"}

## Stap 2: Installeer de [!DNL New Relic] agent op de server

Te gebruiken [!DNL New Relic APM Pro] om gegevens te verzamelen en te verzenden, moet de PHP agent op uw server geïnstalleerd zijn.

1. Als u wordt gevraagd een webagent te kiezen, klikt u op **PHP**.

1. Volg de instructies om de PHP-agent op uw server in te stellen.

   Voor hulp zie [New Relic voor PHP][3].

1. Controleer of de uitsnede op de server wordt uitgevoerd.

   Zie voor meer informatie [Uitsnede configureren en uitvoeren][5] in de ontwikkelaarsdocumentatie.

## Stap 3: Configureer uw winkel

>[!NOTE]
>Deze configuratieopties zijn niet van toepassing op Adobe Commerce op Cloud Infrastructure.
>
>Als je op het Pro-abonnement bent, is New Relic al [vooraf geconfigureerd en standaard ingeschakeld](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Als u op het plan van de Aanzet staat, moet u voltooien [New Relic-configuratiestappen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) die deel uitmaken van het installatieproces.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkernavigatievenster waar **[!UICONTROL General]** wordt uitgebreid, kiest u **[!UICONTROL New Relic Reporting]** en voer de volgende handelingen uit:

   ![New Relic Reporting Configuration](./assets/new-relic-reporting-general.png){width="600"}

   * Set **[!UICONTROL Enable New Relic Integration]** tot `Yes`.

   * In de **[!UICONTROL Insights API URL]**, vervang het percentage (`%`) met je New Relic-account-id.

   * Voer uw **[!UICONTROL New Relic Account ID]**.

   * Voer uw **[!UICONTROL New Relic Application ID]**.

   * Voer uw **[!UICONTROL New Relic API Key]**.

   * Voer u in **[!UICONTROL Insights API Key]**.

1. Voor **[!UICONTROL New Relic Application Name]**, voert u een naam in om de configuratie voor interne verwijzing te identificeren.

1. (Optioneel) Voor **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, selecteert u `Yes` om verzamelde gegevens voor de storefront en Admin als afzonderlijke toepassingen naar New Relic te verzenden.

   Voor deze optie moet een naam worden ingevoerd voor het **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Als u deze functie inschakelt, wordt het aantal fout-positieve waarden verminderd [!DNL New Relic] signaleert en staat voor gevormd toezicht en alarm strikt voor frontend prestaties toe. New Relic ontvangt afzonderlijke toepassingsgegevensbestanden met namen van toepassingsnamen die aan `Adminhtml` en naar voren. Bijvoorbeeld: `MyStore_Adminhtml`

1. Klik op **[!UICONTROL Save Config]**.

## Stap 4: Uitsnijden inschakelen voor [!DNL New Relic] rapportage

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Cron]** sectie.

   ![New Relic Cron-configuratie](./assets/new-relic-reporting-cron.png){width="600"}

1. Set **[!UICONTROL Enable Cron]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.

## [!DNL New Relic] query

[!DNL New Relic Insights] gegevens zijn gebaseerd op instructies die zijn geschreven in [!DNL New Relic Query Language] (NRQL) en eventuele aangepaste parameters die u kunt opnemen. Gegevens kunnen worden geretourneerd van ad-hocquery&#39;s of door query&#39;s die zijn opgeslagen op het dashboard. Zie voor meer informatie de [NRQL-verwijzing][6] in de [!DNL New Relic] documentatie.

### Gebeurtenissen van Admin

#### Actieve Admin-gebruikers

Geeft het aantal actieve Admin-gebruikers.

    SELECT uniqueCount(AdminId)
    VAN Transactie
    WHERE appName=&#39;&lt;your_app_name>&quot; SINCE 15 minuten geleden

#### Momenteel actieve beheergebruikers

Retourneert de namen van actieve Admin-gebruikers.

    Uniques SELECT (AdminName)
    VAN Transactie
    WHERE appName=&#39;&lt;your_app_name>&quot; SINCE 15 minuten geleden

#### Recente beheeractiviteiten

Retourneert het aantal recente Admin-handelingen.

    SELECT count(AdminId)
    VAN Transactie
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName SINCE 1 dag geleden

#### Laatste beheeractiviteit

Retourneert gedetailleerde informatie over recente beheerhandelingen, zoals de gebruikersnaam, duur en toepassingsnaam van de beheerder.

    SELECTEER AdminName, duration, name
    FROM Transaction
    WHERE appName=&lt;your_app_name>&#39;&#39; AND AdminName IS NOT NULL
    AND AdminName!&lt;/your_app_name>= &#39;N/A&#39;-LIMIET 50

### Cron-gebeurtenissen

#### Aantal categorieën

Retourneert het aantal toepassingsevenementen per categorie gedurende de opgegeven periode.

    SELECT average(CatalogCategoryCount)
    Van uitsnede
    WAAR CatalogCategoryCount NIET NULL IS
    AND appName = &#39;&lt;your_app_name>TIJDSTEMMEN 2 minuten

#### Huidig aantal catalogi

Retourneert het gemiddelde aantal toepassingsgebeurtenissen in de catalogus per categorie gedurende de opgegeven tijdsperiode.

    SELECT average (CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINDS 2 minuten ago LIMIT 1
&lt;/your_app_name>
#### Actieve producten

Retourneert het aantal toepassingsgebeurtenissen per product gedurende de opgegeven periode.

    SELECT average(CatalogProductActiveCount)
    Van uitsnede
    WAAR CatalogProductActiveCount NIET NULL IS
    AND appName = &#39;&lt;your_app_name>TIJDSTEMMEN 2 minuten

#### Aantal actieve producten

Geeft als resultaat het gemiddelde aantal actieve toepassingsgebeurtenissen per product gedurende de opgegeven periode.

    SELECT average(CatalogProductActiveCount)
    Van uitsnede
    WAAR CatalogProductActiveCount NIET NULL IS
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SINCE 2 minuten geleden LIMIT 1

#### Configureerbare producten

Retourneert het gemiddelde aantal toepassingsgebeurtenissen voor configureerbare producten tijdens de opgegeven tijdsperiode.

    SELECT average(CatalogProductConfigurableCount)
    Van uitsnede
    WAAR CatalogProductConfigurableCount NIET ONGELDIG IS
    AND appName = &#39;&lt;your_app_name>TIJDSTEMMEN 2 minuten

#### Configureerbaar aantal producten

Retourneert het gemiddelde aantal toepassingsgebeurtenissen per configureerbaar product tijdens de opgegeven tijdsperiode.

    SELECT average(CatalogProductConfigurableCount)
    Van uitsnede
    WAAR CatalogProductConfigurableCount NIET ONGELDIG IS
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SINCE 2 minuten geleden LIMIT 1

#### Aantal producten (alle)

Retourneert het totale aantal toepassingsgebeurtenissen voor alle producten.

    SELECT average(CatalogProductCount)
    Van uitsnede
    WAAR CatalogProductCount NIET NULL IS
    AND appName = &#39;&lt;your_app_name>TIJDSTEMMEN 2 minuten

#### Huidig aantal producten (alle)

Retourneert het gemiddelde aantal toepassingsgebeurtenissen voor alle producten gedurende de opgegeven tijdsperiode.

    SELECT average(CatalogProductCount)
    Van uitsnede
    WAAR CatalogProductCount NIET NULL IS
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SINCE 2 minuten geleden LIMIT 1

#### Aantal klanten

Retourneert het gemiddelde aantal toepassingsgebeurtenissen per klant.

    SELECT average (CustomerCount)
    Van uitsnede
    WAAR CustomerCount NIET NULL IS
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>TIJDSTEMMEN 2 minuten

#### Huidig aantal klanten

Retourneert het gemiddelde aantal klanten gedurende de opgegeven tijdsperiode.

    SELECT average (CustomerCount)
    Van uitsnede
    WAAR CustomerCount NIET NULL IS
    AND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SINCE 2 minuten geleden LIMIT 1

#### Modulestatus

Retourneert het gemiddelde aantal keren dat toepassingsmodules tijdens de opgegeven tijdsperiode zijn ingeschakeld, uitgeschakeld of geïnstalleerd.

    SELECT average (ModulesDisabled), average (ModulesEnabled), average
    (ModulesGeïnstalleerd)
    Uit uitsnede&lt;
    WHERE appName = &#39;&lt;your_app_name>TIJDSTEMMEN 2 minuten

#### Huidige status van module

Retourneert het gemiddelde aantal keren dat modules tijdens de opgegeven tijdsperiode zijn ingeschakeld, uitgeschakeld of geïnstalleerd.

    SELECT average (ModulesDisabled), average (ModulesEnabled), average
    (ModulesGeïnstalleerd)
    Van uitsnede
    WHERE appName = &#39;&lt;your_app_name>&quot; SINCE 2 minuten geleden LIMIT 1

#### Telling van website en winkel

Geeft het gemiddelde aantal toepassingsgebeurtenissen per website en store tijdens de opgegeven tijdsperiode.

    SELECT average(StoreViewCount), average(WebsiteCount)
    Van uitsnede
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 minuten

#### Huidige website- en winkelaantallen

Retourneert het gemiddelde aantal huidige toepassingsgebeurtenissen gedurende de opgegeven tijdsperiode.

    SELECT average(StoreViewCount), average(WebsiteCount)
    Van uitsnede
    WHERE appName = &#39;&lt;your_app_name>&quot; SINCE 2 minuten geleden LIMIT 1

#### Uitsnijden - alle gegevens van de gebeurtenis

Retourneert alle gebeurtenisgegevens van de toepassing.

    SELECTEREN *
    Van uitsnede
    WHERE appName = &#39;&lt;your_app_name>&#39;

### Klanten

#### Aantal actieve klanten

Retourneert het aantal actieve klanten tijdens de opgegeven tijdsperiode.

    SELECT uniqueCount(CustomerId)
    VAN Transactie
    WHERE appName = &#39;&lt;your_app_name>&quot; SINCE 15 minuten geleden

#### Actieve klanten

Retourneert de namen van actieve klanten tijdens de opgegeven tijdsperiode.

    EENDEN SELECTEREN (CustomerName)
    VAN Transactie
    WHERE appName=&#39;&lt;your_app_name>&quot; SINCE 15 minuten geleden

#### Topklanten

Retourneert de bovenste klanten tijdens de opgegeven tijdsperiode.

    SELECT count(CustomerId)
    VAN Transactie
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET Customer Name SINCE 1 dag geleden

#### Recente beheeractiviteiten

Retourneert een gedefinieerd aantal records met recente activiteit, die de naam van de klant en de duur van het bezoek bevatten.

    SELECTEER CustomerName, duration, name
    FROM Transaction
    WHERE appName=&lt;your_app_name>&#39;&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName!&lt;/your_app_name>= &#39;N/A&#39;-LIMIET 50

### Orders

#### Aantal geplaatste orders

Retourneert het aantal orders dat tijdens de opgegeven periode is geplaatst.

    SELECT count(Order)
    FROM Transactie SINCE 1 day ago

#### Totale orderwaarde

Retourneert het totale aantal regelitems dat is geordend tijdens de opgegeven tijdsperiode.

    SELECT sum(orderValue)
    FROM Transaction SINCE 1 day ago

#### Totaal aantal bestelde regelitems

Hiermee wordt het totale aantal tijdens de opgegeven periode bestelde regelitems geretourneerd.

    SELECT sum(lineItemCount)
    VANAF Transactie SINDS 1 dag geleden


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
