---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] van Commerce Admin.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 1aec5c618d1f3f7f083523956d2aee62b777faca
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Deze configuratieopties zijn niet van toepassing op Adobe Commerce op Cloud Infrastructure.
>
>Als u op het Pro plan bent, is New Relic reeds [ preconfigured en toegelaten door gebrek ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Als u op het plan van de Aanzet bent, moet u de [ de configuratiestappen van New Relic ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) voltooien die deel van het opstellingsproces uitmaken.

## [!UICONTROL General]

![ Algemeen ](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Winkelweergave | Hiermee bepaalt u of uw winkel kan worden gebruikt met [!DNL New Relic] Reporting. Opties: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Winkelweergave | De URL waar New Relic API&#39;s worden geïmplementeerd. Bijvoorbeeld: `https://api.newrelic.com/deployments.xml` |
| Insights API URL | Winkelweergave | De URL waar de API&#39;s voor inzichten worden geïmplementeerd. Gebruik het procentteken (%) om uw account-id weer te geven. Bijvoorbeeld: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Winkelweergave | De account-id die aan uw [!DNL New Relic] -account is toegewezen. |
| [!UICONTROL New Relic Application ID] | Winkelweergave | De toepassings-id die aan uw [!DNL New Relic] -account is toegewezen voor de Commerce-integratie. |
| [!UICONTROL New Relic API Key] | Winkelweergave | De sleutel die aan u wordt toegewezen voor het verkrijgen van toegang tot de [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Winkelweergave | De sleutel die aan u voor het verkrijgen van toegang tot Inzichten wordt toegewezen. |
| [!UICONTROL New Relic Application Name] | Winkelweergave | De naam die u aan uw [!DNL New Relic] integratie hebt toegewezen. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Winkelweergave | Een optie om rapportgegevens die voor de winkel en Admin zijn verzameld, als afzonderlijke apps naar New Relic te verzenden. Voor deze optie moet een naam worden ingevoerd voor de [!UICONTROL New Relic Application Name] . De functie voegt de toepassingsnaam met een onderstrepingsteken toe aan de verzamelde toepassingsgegevens. Bijvoorbeeld: `MyStore_Adminhtml` , `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![ Uitsnede ](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Winkelweergave | Bepaalt als [!DNL New Relic] de rapporten op programma met [ Gewas ](../../systems/cron.md) kunnen worden in werking gesteld. Opties: `Yes` / `No` |

{style="table-layout:auto"}
