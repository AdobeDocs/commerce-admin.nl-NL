---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL General] &gt; [!UICONTROL Currency Setup] van Commerce Admin.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Zie [&#x200B; configuratie van de Valuta &#x200B;](../../stores-purchase/currency-configuration.md) voor meer details over deze configuraties.

## [!UICONTROL Currency Options]

![&#x200B; de Opstelling van de Valuta > Opties van de Valuta &#x200B;](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Website | De primaire valuta die wordt gebruikt voor alle online betalingstransacties. Voor veelvoudige opslagmeningen, moet het werkingsgebied van de prijs in de [&#x200B; configuratie van de Catalogus &#x200B;](../catalog/catalog.md) worden geplaatst. |
| [!UICONTROL Default Display Currency] | Winkelweergave | De primaire valuta die wordt gebruikt om prijzen weer te geven. |
| [!UICONTROL Allowed Currencies] | Winkelweergave | De valuta&#39;s die je winkel accepteert voor betaling. |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>Beginnend met versie 2.4.6, wordt de [[!DNL Fixer.io] &#x200B;](https://fixer.io/) dienst afgekeurd en met de [[!DNL Fixer API]  vervangen (APILayer) &#x200B;](https://apilayer.com/marketplace/fixer-api) dienst. Het wordt ten zeerste aanbevolen een APILayer-account te gebruiken in plaats van een afgekeurd [!DNL Fixer.io] -account.

![&#x200B; Opstelling van de Valuta > Fixer.io &#x200B;](./assets/currency-setup-fixer.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL API key] | Algemeen | De sleutel die wordt gebruikt om via uw [!DNL fixer.io] -account toegang te krijgen tot de conversieservice. Zie [[!DNL fixer.io] &#x200B;](https://fixer.io/) voor meer informatie. |
| [!UICONTROL Connection Timeout in Seconds] | Algemeen | Hiermee bepaalt u het aantal seconden dat inactiviteit optreedt voordat een Fixer.io-sessietime-out optreedt. Standaardwaarde: `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![&#x200B; de Opstelling van de Valuta > Fixer API (APILayer) &#x200B;](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL API key] | Algemeen | De sleutel die wordt gebruikt om via uw [!DNL APILayer] -account toegang te krijgen tot de conversieservice. Zie [[!DNL APILayer] &#x200B;](https://apilayer.com/) voor meer informatie. |
| [!UICONTROL Connection Timeout in Seconds] | Algemeen | Bepaalt het aantal seconden van inactiviteit vóór een [!DNL APILayer] sessietijden uit. De standaardwaarde is `100` . |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![&#x200B; Opstelling van de Valuta > API van de Convertor van de Valuta &#x200B;](./assets/currency-setup-converter.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL API key] | Algemeen | De sleutel die wordt gebruikt om tot de omzettingsdienst toegang te hebben. Voor meer informatie, zie [[!DNL Currency Convertor]  API &#x200B;](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Algemeen | Bepaalt het aantal seconden van inactiviteit vóór een [!DNL Currency Converter] sessietijden uit. Standaardwaarde: `100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![&#x200B; Opstelling van de Valuta > Geplande de Montages van de Invoer &#x200B;](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Winkelweergave | Hiermee wordt bepaald of geplande import is ingeschakeld voor valutakoersen. Opties: `Yes` / `No` |
| [!UICONTROL Service] | Winkelweergave | Specificeert de dienst die de gegevens voor de geplande invoer verstrekt. Standaardwaarde is `fixer.io` |
| [!UICONTROL Start Time] | Winkelweergave | Wijst op de begintijd door uur, minuut, en seconde, die op een klok van 24 uur wordt gebaseerd. |
| [!UICONTROL Frequency] | Winkelweergave | Hiermee bepaalt u hoe vaak de geplande import plaatsvindt. Opties: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Winkelweergave | Identificeert het e-mailadres van elke persoon die per e-mail op de hoogte wordt gesteld van geplande importfouten. Voor meerdere ontvangers scheidt u elke vermelding met een komma. |
| [!UICONTROL Error Email Sender] | Website | Hiermee wordt de contactpersoon van de winkel geïdentificeerd die wordt weergegeven als de afzender van het foutbericht in de e-mail. Standaardafzender: `General Contact` |
| [!UICONTROL Error Email Template] | Website | Hier geeft u de sjabloon op die wordt gebruikt als basis voor de e-mailfoutmelding. Standaardsjabloon: `Currency Update Warnings` |

{style="table-layout:auto"}
