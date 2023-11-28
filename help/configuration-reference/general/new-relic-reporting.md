---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] pagina van de Commerce Admin.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 3%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![Algemeen](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Winkelweergave | Hiermee wordt bepaald of je winkel kan worden gebruikt [!DNL New Relic] Rapportage. Opties: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Winkelweergave | De URL waar New Relic API&#39;s worden geïmplementeerd. Bijvoorbeeld: `https://api.newrelic.com/deployments.xml` |
| Insights API URL | Winkelweergave | De URL waar de API&#39;s voor inzichten worden geïmplementeerd. Gebruik het procentteken (%) om uw account-id weer te geven. Bijvoorbeeld: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Winkelweergave | De account-id die aan uw [!DNL New Relic] account. |
| [!UICONTROL New Relic Application ID] | Winkelweergave | De toepassings-id die aan uw [!DNL New Relic] rekening houden met de integratie van de handel. |
| [!UICONTROL New Relic API Key] | Winkelweergave | De sleutel die aan u voor het verkrijgen van toegang tot wordt toegewezen [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Winkelweergave | De sleutel die aan u voor het verkrijgen van toegang tot Inzichten wordt toegewezen. |
| [!UICONTROL New Relic Application Name] | Winkelweergave | De naam die u aan uw [!DNL New Relic] integratie. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Winkelweergave | Een optie om rapportgegevens die voor de winkel en Admin zijn verzameld, als afzonderlijke apps naar New Relic te verzenden. Voor deze optie moet een naam worden ingevoerd voor het [!UICONTROL New Relic Application Name]. De functie voegt de toepassingsnaam met een onderstrepingsteken toe aan de verzamelde toepassingsgegevens. Bijvoorbeeld: `MyStore_Adminhtml`, `MyStore_frontend` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Winkelweergave | Hiermee wordt bepaald of [!DNL New Relic] rapporten kunnen volgens schema worden uitgevoerd met [Cron](../../systems/cron.md). Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
