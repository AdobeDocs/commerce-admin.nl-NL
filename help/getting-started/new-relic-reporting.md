---
title: '[!DNL New Relic] rapporten'
description: Leer over  [!DNL New Relic]  rapportering beschikbaar voor rekeningen voor Adobe Commerce op wolkeninfrastructuur, die de software voor de dienst van New Relic APM omvat.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] rapporten

[ New Relic ][1] is de dienst van de softwareanalyse die u helpt toepassingsinteractie analyseren en verbeteren. Voor Adobe Commerce-accounts in de cloud-infrastructuur is de software voor de [!DNL New Relic APM] -service inbegrepen. Voor meer informatie, zie {de diensten van 0} New Relic ][4] in _Commerce op de Gids van de Infrastructuur van de Wolk_.[

## Stap 1: Aanmelden voor een [!DNL New Relic] -account

1. Ga naar de [[!DNL New Relic]][1] -website en meld u aan voor een account.

   U kunt zich ook aanmelden voor een gratis proefaccount.

1. Volg de instructies op de site. Wanneer u hierom wordt gevraagd, kiest u het product dat u als eerste wilt installeren.

1. Zoek in uw account naar de volgende referenties die nodig zijn om de Commerce-configuratie te voltooien:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | Account-ID | Vanuit het [!DNL New Relic] -accountdashboard is de account-id het nummer in de URL na: `/accounts` |
   | Toepassings-id | Klik op het dashboard van uw [!DNL New Relic] -account op **[!UICONTROL New Relic APM]** . Kies **[!UICONTROL Applications]** in het menu. Kies vervolgens de toepassing. De toepassings-ID is het nummer in de URL na: `/applications/` |
   | Nieuwe Relic API-sleutel | Klik op het dashboard van uw [!DNL New Relic] -account op **[!UICONTROL Account Settings]** . Kies in het menu aan de linkerkant onder Integraties de optie **[!UICONTROL Data Sharing]** . U kunt de API-sleutel van deze pagina maken, opnieuw genereren of verwijderen. |
   | API-sleutel voor inzichten | Klik op het dashboard van uw [!DNL New Relic] -account op **[!UICONTROL Insights]** . Kies **[!UICONTROL API Keys]** in het menu links onder Beheer. Uw API-sleutels voor inzichten worden op deze pagina weergegeven. Indien nodig, klik het plusteken (**+**) naast de Sleutels van het Tussenvoegsel om een sleutel te produceren. |

   {style="table-layout:auto"}

## Stap 2: Installeer de [!DNL New Relic] -agent op de server

Als u [!DNL New Relic APM Pro] wilt gebruiken om gegevens te verzamelen en te verzenden, moet de PHP-agent op uw server zijn geïnstalleerd.

1. Wanneer ertoe aangezet om een Webagent te kiezen, klik **PHP**.

1. Volg de instructies om de PHP-agent op uw server in te stellen.

   Als u hulp nodig hebt, zie [ New Relic voor PHP ][3].

1. Controleer of de uitsnede op de server wordt uitgevoerd.

   Meer leren, zie [ uitsnede ][5] vormen en in werking stellen in de ontwikkelaardocumentatie.

## Stap 3: Configureer uw winkel

>[!NOTE]
>Deze configuratieopties zijn niet van toepassing op Adobe Commerce op Cloud Infrastructure.
>
>Als u op het Pro plan bent, is New Relic reeds [ preconfigured en toegelaten door gebrek ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Als u op het plan van de Aanzet bent, moet u de [ de configuratiestappen van New Relic ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) voltooien die deel van het opstellingsproces uitmaken.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies **[!UICONTROL New Relic Reporting]** in het navigatievenster aan de linkerkant waar **[!UICONTROL General]** wordt uitgevouwen en voer de volgende handelingen uit:

   ![ New Relic die configuratie ](./assets/new-relic-reporting-general.png){width="600"} meldt

   * Stel **[!UICONTROL Enable New Relic Integration]** in op `Yes` .

   * Vervang in **[!UICONTROL Insights API URL]** het percentagesymbool (`%` ) door uw New Relic-account-id.

   * Voer uw **[!UICONTROL New Relic Account ID]** in.

   * Voer uw **[!UICONTROL New Relic Application ID]** in.

   * Voer uw **[!UICONTROL New Relic API Key]** in.

   * Voer u in **[!UICONTROL Insights API Key]**.

1. Voer bij **[!UICONTROL New Relic Application Name]** een naam in om de configuratie voor interne verwijzing te identificeren.

1. (Optioneel) Selecteer `Yes` voor **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]** om verzamelde gegevens voor de storefront en Admin als aparte toepassingen naar New Relic te verzenden.

   Voor deze optie moet een naam worden ingevoerd voor de **[!UICONTROL New Relic Application Name]** .

   >[!NOTE]
   >
   >Als u deze functie inschakelt, vermindert u het aantal fout-positieve [!DNL New Relic] waarschuwingen en kunt u de geconfigureerde bewaking en waarschuwingen strikt toepassen op de prestaties vooraf. New Relic ontvangt afzonderlijke toepassingsgegevensbestanden met de namen Application Name toegevoegd aan `Adminhtml` en frontend. Bijvoorbeeld: `MyStore_Adminhtml`

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Stap 4: Uitsnijden inschakelen voor [!DNL New Relic] -rapportage

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Cron]** sectie uit.

   ![ de configuratie van het Gewas van New Relic ](./assets/new-relic-reporting-cron.png){width="600"}

1. Stel **[!UICONTROL Enable Cron]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## [!DNL New Relic] query&#39;s

[!DNL New Relic Insights] -gegevens zijn gebaseerd op instructies die zijn geschreven in [!DNL New Relic Query Language] (NRQL) en eventuele aangepaste parameters die u kunt opnemen. Gegevens kunnen worden geretourneerd van ad-hocquery&#39;s of door query&#39;s die zijn opgeslagen op het dashboard. Meer leren, zie de [ NRQL Verwijzing ][6] in de [!DNL New Relic] documentatie.

### Gebeurtenissen van Admin

#### Actieve Admin-gebruikers

Geeft het aantal actieve Admin-gebruikers.

     SELECT uniqueCount (AdminId) 
     VAN Transactie 
     WAAR appName=&#39;&lt;your_app_name>&#39; SINCE 15 minuten geleden 

#### Momenteel actieve beheergebruikers

Retourneert de namen van actieve Admin-gebruikers.

     SELECTEER uniques (AdminName) 
     VAN Transactie 
     WAAR appName=&#39;&lt;your_app_name>&#39; SINCE 15 minuten geleden 

#### Recente beheeractiviteiten

Retourneert het aantal recente Admin-handelingen.

     UITGEZOCHTE telling (AdminId) 
     VAN Transactie 
     WAAR appName =&#39;&lt;your_app_name>&#39; FACET AdminName SINCE 1 dag geleden 

#### Laatste beheeractiviteit

Retourneert gedetailleerde informatie over recente beheerdersacties, waaronder de gebruikersnaam, duur en toepassingsnaam van de beheerder.

    SELECTEER AdminName, duur, naam
    VAN Transactie
    WAAR appName=&#39;&lt;your_app_name>&#39; EN AdminName IS NIET NULL
    EN AdminName !&lt;/your_app_name>= &#39;N.V.T.&#39; LIMIET 50

### Cron evenementen

#### Aantal categorieën

Retourneert het aantal toepassingsgebeurtenissen per categorie gedurende de opgegeven periode.

     SELECTEER gemiddelde (CatalogCategoryCount) 
     VAN Kroon 
     WAAR CatalogCategoryCount NIET ONGELDIG 
     EN appName = &quot;&lt;your_app_name>&#39; TIMESERIES 2 minuten 
 is
#### Huidig aantal catalogi

Retourneert het gemiddelde aantal toepassingsgebeurtenissen in de catalogus per categorie gedurende de opgegeven tijdsperiode.

    SELECTEER gemiddelde(CatalogCategoryCount)
    VAN Cron
    WAAR CatalogCategoryCount NIET NULL
    IS EN CatalogCategoryCount > 0
    EN appName = &#39;&lt;your_app_name>&#39; SINDS 2 minuten geleden LIMIET 1
&lt;/your_app_name>
#### Actieve producten

Retourneert het aantal toepassingsgebeurtenissen per product gedurende de opgegeven periode.

     SELECTEER gemiddelde (CatalogProductActiveCount) 
     VAN Kroon 
     WAAR CatalogProductActiveCount NIET ONGELDIG 
     EN appName = &quot;&lt;your_app_name>&#39; TIMESERIES 2 minuten 
 IS
#### Aantal actieve producten

Geeft als resultaat het gemiddelde aantal actieve toepassingsgebeurtenissen per product gedurende de opgegeven periode.

     SELECT gemiddelde (CatalogProductActiveCount) 
     VAN Uitsnede 
     WAAR CatalogProductActiveCount NIET ONGELDIG 
     EN CatalogProductActiveCount > 0 
     EN appName = &quot;&lt;your_app_name>&quot;SINCE 2 minuten geleden LIMIT 1 
 is
#### Configureerbare producten

Retourneert het gemiddelde aantal toepassingsgebeurtenissen voor configureerbare producten tijdens de opgegeven tijdsperiode.

     SELECT gemiddelde (CatalogProductConfigurableCount) 
     VAN Kroon 
     WAAR CatalogProductConfigurableCount NIET ONGELDIG 
     EN appName = &quot;&lt;your_app_name>&#39; TIMESERIES 2 minuten 
 IS
#### Configureerbaar aantal producten

Retourneert het gemiddelde aantal toepassingsgebeurtenissen per configureerbaar product tijdens de opgegeven tijdsperiode.

     SELECT gemiddelde (CatalogProductConfigurableCount) 
     VAN Uitsnede 
     WAAR CatalogProductConfigurableCount NIET ONGELDIG 
     EN CatalogProductConfigurableCount > 0 
     EN appName = &quot;&lt;your_app_name>&quot;SINCE 2 minuten geleden LIMIT 1 
 is
#### Aantal producten (alle)

Retourneert het totale aantal toepassingsgebeurtenissen voor alle producten.

     SELECTEER gemiddelde (CatalogProductCount) 
     VAN Kroon 
     WAAR CatalogProductCount NIET ONGELDIG 
     EN appName = &quot;&lt;your_app_name>&#39; TIMESERIES 2 minuten 
 IS
#### Huidig aantal producten (alle)

Retourneert het gemiddelde aantal toepassingsgebeurtenissen voor alle producten gedurende de opgegeven tijdsperiode.

     SELECT gemiddelde (CatalogProductCount) 
     VAN Uitsnede 
     WAAR CatalogProductCount NIET ONGELDIG 
     EN CatalogProductCount > 0 
     EN appName = &quot;&lt;your_app_name>&quot;SINCE 2 minuten geleden LIMIT 1 
 IS
#### Aantal klanten

Retourneert het gemiddelde aantal toepassingsgebeurtenissen per klant.

     SELECTEER gemiddelde (CustomerCount) 
     VAN Kroon 
     WAAR CustomerCount NIET ONGELDIG 
     EN CustomerCount > 0 &lt;
     EN appName = &quot;&lt;your_app_name>&quot;TIMESERIES 2 minuten 
 IS
#### Huidig aantal klanten

Retourneert het gemiddelde aantal klanten gedurende de opgegeven tijdsperiode.

     SELECTEER gemiddelde (CustomerCount) 
     VAN Kroon 
     WAAR CustomerCount NIET ONGELDIG 
     EN CustomerCount > 0 
     EN appName = &quot;&lt;your_app_name>&quot;SINCE 2 minuten geleden LIMIT 1 
 IS
#### Modulestatus

Retourneert het gemiddelde aantal keren dat toepassingsmodules tijdens de opgegeven tijdsperiode zijn ingeschakeld, uitgeschakeld of geïnstalleerd.

     SELECT gemiddelde (ModulesDisabled), gemiddelde (ModulesEnabled), gemiddelde 
     (ModulesInstalled) 
     VAN Kroon &lt;
     WHERE appName = &quot;&lt;your_app_name>&#39; TIMESERIES 2 minuten 

#### Huidige status van module

Retourneert het gemiddelde aantal keren dat modules tijdens de opgegeven tijdsperiode zijn ingeschakeld, uitgeschakeld of geïnstalleerd.

     SELECT gemiddelde (ModulesDisabled), gemiddelde (ModulesEnabled), gemiddelde 
     (ModulesInstalled) 
     VAN Kroon 
     WAAR appName = &quot;&lt;your_app_name>&quot;SINCE 2 minuten geleden LIMIT 1 

#### Telling van website en winkel

Geeft het gemiddelde aantal toepassingsgebeurtenissen per website en store tijdens de opgegeven tijdsperiode.

     SELECT gemiddelde (StoreViewCount), gemiddelde (WebsiteCount) 
     VAN Kroon 
     WAAR appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 minuten 

#### Huidige website- en winkelaantallen

Retourneert het gemiddelde aantal huidige toepassingsgebeurtenissen gedurende de opgegeven tijdsperiode.

     UITGEZOCHTE gemiddelde (StoreViewCount), gemiddelde (WebsiteCount) 
     VAN Uitsnede 
     WAAR appName = &quot;&lt;your_app_name>&quot;SINCE 2 minuten geleden LIMIT 1 

#### Uitsnijden - alle gegevens van de gebeurtenis

Retourneert alle gebeurtenisgegevens van de toepassing.

     SELECTEER *
     VAN Uitsnede 
     WAAR appName = &quot;&lt;your_app_name>&quot;

### Klanten

#### Aantal actieve klanten

Retourneert het aantal actieve klanten tijdens de opgegeven tijdsperiode.

     SELECT uniqueCount (CustomerId) 
     VAN Transactie 
     WAAR appName = &quot;&lt;your_app_name>&quot;SINCE 15 minuten geleden 

#### Actieve klanten

Retourneert de namen van actieve klanten tijdens de opgegeven tijdsperiode.

     SELECTEER uniques (CustomerName) 
     VAN Transactie 
     WAAR appName=&#39;&lt;your_app_name>&#39; SINCE 15 minuten geleden 

#### Topklanten

Retourneert de bovenste klanten tijdens de opgegeven tijdsperiode.

     UITGEZOCHTE telling (CustomerId) 
     VAN Transactie 
     WAAR appName = &quot;&lt;your_app_name>&#39; FACET CustomerName SINCE 1 dag geleden 

#### Recente beheeractiviteiten

Retourneert een gedefinieerd aantal records met recente activiteit, die de naam van de klant en de duur van het bezoek bevatten.

    SELECTEER KlantNaam, duur, naam
    VAN Transactie
    WAAR appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;N.V.T.&#39; LIMIET 50

### Orders

#### Aantal geplaatste bestellingen

Retourneert het aantal bestellingen dat tijdens de opgegeven periode is geplaatst.

    SELECTEER count(Order)
    FROM Transactie SINDS 1 dag geleden

#### Totale orderwaarde

Retourneert het totale aantal regelitems dat is geordend tijdens de opgegeven tijdsperiode.

    SELECTEER sum(orderValue)
    FROM Transactie SINDS 1 dag geleden

#### Totaal aantal bestelde regelitems

Retourneert het totale aantal regelitems dat tijdens de opgegeven periode is besteld.

     SELECT som (lineItemCount) 
     VAN Transactie SINCE 1 dag geleden 


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
