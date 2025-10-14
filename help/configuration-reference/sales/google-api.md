---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Google API] van Commerce Admin.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 5ee52e8d4f2ebb8fc28f13cca53e87c3529f76d3
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![&#x200B; Google Analytics &#x200B;](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Winkelweergave | Schakelt [!DNL Google Analytics] in voor uw winkel. Opties: `Yes` / `No` |
| [!UICONTROL Account Type] | Winkelweergave | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt de configuratieopties volgens uw Google Analytics accounttype. Opties: Universal Analytics (standaard) / Google Tag Manager |
| [!UICONTROL Account Number] | Winkelweergave | Het accountnummer, of trackingcode, dat is toegewezen toen u uw [!DNL Google Analytics] -account maakte. |
| [!UICONTROL Anonymize IP] | Winkelweergave | Hiermee bepaalt u of identificatiegegevens worden verwijderd uit IP-adressen die worden weergegeven in [!DNL Google Analytics] -resultaten. |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![&#x200B; Google Analytics - het accounttype van de Manager van de Markering van Google &#x200B;](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Wanneer **[!UICONTROL Account Type]** is ingesteld op `Google Tag Manager` , worden er extra velden weergegeven.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Winkelweergave | De unieke id voor de container [!DNL Google Tag Manager] . Deze waarde begint doorgaans met `GTM-` . Deze id staat in uw [!DNL Google Tag Manager] -account. Als [!DNL Google Tag Manager] al is geïnstalleerd en geconfigureerd voor uw winkel, wordt de container-id automatisch weergegeven in dit veld. |
| [!UICONTROL List property for the catalog page] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die aan de cataloguspagina is gekoppeld. Standaardwaarde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan het blok voor cross-sell. Standaardwaarde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan het blok Up-sell. Standaardwaarde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan het verwante productblok. Standaardwaarde: `Related Products` |
| [!UICONTROL List property for the search results page] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan de pagina met zoekresultaten. Standaardwaarde: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan de labels voor interne promoties. Standaardwaarde: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![&#x200B; Google AdWords &#x200B;](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Winkelweergave | Hiermee schakelt u Google AdWords in voor de winkel. Opties: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Winkelweergave | De id van je Google AdWords-account. |
| [!UICONTROL Conversion Language] | Winkelweergave | De taal die voor omzettingen AdWords wordt gebruikt. Opties: `All available languages` |
| [!UICONTROL Conversion Format] | Winkelweergave | Bepaalt de indeling van het [!DNL Google Site Stats] -bericht dat op de conversiepagina wordt weergegeven. De melding is gekoppeld aan een pagina waarop bezoekers worden geïnformeerd over de cookies die worden gebruikt om hun bezoeken bij te houden. Deze numerieke waarde wordt toegewezen aan de variabele `google_conversion_format` in uw AdWords-script. Meer leren, zie [&#x200B; Ongeveer Omzetting het Volgen &#x200B;](https://support.google.com/google-ads/answer/1722022?hl=en) op de website van Google. Opties: <br/>**`1`**- geeft een melding van één regel weer.<br/>**`2`** - (Standaard) Hiermee wordt een melding van twee regels weergegeven. <br/>**`3`**- Geeft geen klantmelding weer. |
| [!UICONTROL Conversion Color] | Winkelweergave | Bepaalt de kleur van het conversielabel. Gebruik de plukker van de a [&#x200B; kleur &#x200B;](https://www.w3schools.com/colors/colors_picker.asp) om de hexadecimale waarde te kiezen. Deze hexadecimale waarde wordt toegewezen aan de variabele `google_conversion_color` in uw AdWords-script. Bijvoorbeeld: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Winkelweergave | Een tekstlabel dat wordt weergegeven bij de melding [!DNL Google Site Stats] . Deze tekstreeks wordt toegewezen aan de variabele `~` in het script AdWords. Bijvoorbeeld: &quot;Bedankt voor het winkelen!&quot; |
| [!UICONTROL Conversion Value Type] | Winkelweergave | Hiermee geeft u het type waarde op dat wordt gebruikt om te bepalen wanneer een conversie plaatsvindt. Opties: <br/>**`Dynamic`**- Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van het dynamische orderbedrag.<br/>**`Constant`** - Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van de ingevoerde waarde. |
| [!UICONTROL Conversion Value] | Winkelweergave | Hiermee wordt de waarde opgegeven die wordt gebruikt voor een _[!UICONTROL Constant]_&#x200B;omzetwaarde. |
| [!UICONTROL Send Order Currency] | Winkelweergave | Hiermee worden transactiespecifieke valutawisselwaarden ingeschakeld in AdWords (voor websites met verschillende basisvaluta&#39;s). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![&#x200B; Google Analytics4 &#x200B;](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Winkelweergave | Hiermee wordt Google Analytics 4 ingeschakeld voor je winkel. Opties: `Yes` / `No` |
| [!UICONTROL Account Type] | Winkelweergave | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt de configuratieopties volgens uw Google Analytics accounttype. Opties: `Google Analytics4` (standaardwaarde) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Winkelweergave | Het accountnummer, of trackingcode, dat is toegewezen bij het maken van uw Google Analytics-account. |
| [!UICONTROL Anonymize IP] | Winkelweergave | Hiermee bepaalt u of identificatiegegevens worden verwijderd uit IP-adressen die worden weergegeven in Google Analytics-resultaten. |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![&#x200B; Google Analytics4 - het accounttype van de Manager van de Markering van Google &#x200B;](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Wanneer **[!UICONTROL Account Type]** is ingesteld op `Google Tag Manager` , worden er extra velden weergegeven.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Winkelweergave | De unieke id voor de container [!DNL Google Tag Manager] . Deze waarde begint doorgaans met `GTM-` . Deze id staat in uw Google Tab Manager-account. Als [!DNL Google Tag Manager] al is geïnstalleerd en geconfigureerd voor uw winkel, wordt de container-id automatisch weergegeven in dit veld. |
| [!UICONTROL List property for the catalog page] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die aan de cataloguspagina is gekoppeld. Standaardwaarde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan het blok voor cross-sell. Standaardwaarde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan het blok Up-sell. Standaardwaarde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan het verwante productblok. Standaardwaarde: `Related Products` |
| [!UICONTROL List property for the search results page] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan de pagina met zoekresultaten. Standaardwaarde: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Winkelweergave | Hiermee wordt de eigenschap [!DNL Google Tag Manager] geïdentificeerd die is gekoppeld aan de labels voor interne promoties. Standaardwaarde: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![&#x200B; Google AdWords &#x200B;](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Winkelweergave | Hiermee schakelt u Google AdWords in voor de winkel. Opties: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Winkelweergave | De id van je Google AdWords-account. |
| [!UICONTROL Conversion Language] | Winkelweergave | De taal die voor omzettingen AdWords wordt gebruikt. Opties: alle beschikbare talen |
| [!UICONTROL Conversion Format] | Winkelweergave | Hiermee bepaalt u de indeling van het bericht voor Google-sitestatussen dat op de conversiepagina wordt weergegeven. De melding is gekoppeld aan een pagina waarop bezoekers worden geïnformeerd over de cookies die worden gebruikt om hun bezoeken bij te houden. Deze numerieke waarde wordt toegewezen aan de variabele `google_conversion_format` in uw AdWords-script. Meer leren, zie [&#x200B; Ongeveer Omzetting het Volgen &#x200B;](https://support.google.com/google-ads/answer/1722022?hl=en) op de website van Google. Opties: <br/>**`1`**- geeft een melding van één regel weer.<br/>**`2`** - (Standaard) Hiermee wordt een melding van twee regels weergegeven. <br/>**`3`**- Geeft geen klantmelding weer. |
| [!UICONTROL Conversion Color] | Winkelweergave | Bepaalt de kleur van het conversielabel. Gebruik de plukker van de a [&#x200B; kleur &#x200B;](https://www.w3schools.com/colors/colors_picker.asp) om de hexadecimale waarde te kiezen. Deze hexadecimale waarde wordt toegewezen aan de variabele `google_conversion_color` in uw AdWords-script. Bijvoorbeeld: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Winkelweergave | Een tekstlabel dat wordt weergegeven bij de melding Google Site Stats. Deze tekstreeks wordt toegewezen aan de variabele `~` in het script AdWords. Bijvoorbeeld: &quot;Bedankt voor het winkelen!&quot; |
| [!UICONTROL Conversion Value Type] | Winkelweergave | Hiermee geeft u het type waarde op dat wordt gebruikt om te bepalen wanneer een conversie plaatsvindt. Opties: <br/>**`Dynamic`**- Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van het dynamische orderbedrag.<br/>**`Constant`** - Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van de ingevoerde waarde. |
| [!UICONTROL Conversion Value] | Winkelweergave | Hiermee wordt de waarde opgegeven die wordt gebruikt voor een _[!UICONTROL Constant]_&#x200B;omzetwaarde. |
| [!UICONTROL Send Order Currency] | Winkelweergave | Hiermee worden transactiespecifieke valutawisselwaarden ingeschakeld in AdWords (voor websites met verschillende basisvaluta&#39;s). |

{style="table-layout:auto"}
