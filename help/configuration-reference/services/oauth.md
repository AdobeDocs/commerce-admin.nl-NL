---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Services] &gt; [!UICONTROL OAuth] van Commerce Admin.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![&#x200B; Symbolische Vervalsing van de Toegang &#x200B;](./assets/oauth-token-expire.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Algemeen | Bepaalt de tijdsduur in uren alvorens een klant API teken verloopt. De klanttoken verloopt nooit wanneer het veld leeg is. Standaardwaarde: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Algemeen | Hiermee bepaalt u de tijdsduur in uren voordat een API-beheertoken verloopt. De beheerderstoken verloopt nooit wanneer het veld leeg is. Standaardwaarde: `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>De dragerklant en admin API symbolische Lifetime en de encryptiealgoritmen worden gecontroleerd door de [&#x200B; JWT de configuratiemontages van de Authentificatie &#x200B;](magento-web-api.md#jwt-authentication).

## [!UICONTROL Cleanup Settings]

![&#x200B; Montages van de Schoonmaakbeurt &#x200B;](./assets/oauth-cleanup.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Algemeen | Hiermee geeft u het aantal OAuth-verzoeken op voordat opschoning wordt gestart. Voer `0` niet in om het opruimen uit te schakelen. |
| [!UICONTROL Enable WSDL Cache] | Algemeen | Hiermee bepaalt u de leeftijd van de items in minuten voordat ze worden schoongemaakt. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![&#x200B; Consumentenmontages &#x200B;](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Algemeen | Geeft het aantal seconden aan dat het systeem nodig heeft om de time-out op te geven wanneer klanten hun gegevens posten. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Algemeen | Hiermee wordt het maximale aantal omleidingen aangegeven dat betrekking heeft op het posten van de geloofsbrieven van de consument. |
| [!UICONTROL Expiration Period] | Algemeen | Bepaalt het aantal seconden alvorens een ongebruikte sleutel/een geheim verloopt nadat de symbolische uitwisseling OAuth begint. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![&#x200B; Vergrendelingen van de Authentificatie &#x200B;](./assets/oauth-locks.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Algemeen | Hiermee geeft u het maximum aantal verificatiefouten op waarmee account kan worden afgesloten. |
| [!UICONTROL Lockout Time (seconds)] | Algemeen | Hiermee geeft u de periode op in seconden waarna het account wordt ontgrendeld. |

{style="table-layout:auto"}
