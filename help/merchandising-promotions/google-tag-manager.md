---
title: '[!DNL Google Tag Manager]'
description: Leren gebruiken [!DNL Google Tag Manager] om de vele tags (codefragmenten) te beheren die gerelateerd zijn aan uw marketingcampagnegebeurtenissen op uw Adobe Commerce-sites.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] helpt u de vele tags (codefragmenten) te beheren die betrekking hebben op uw marketingcampagnegebeurtenissen. [!DNL Google Tag Manager] biedt u de mogelijkheid om traceringstags aan uw site toe te voegen om het publiek te meten of om marketinginitiatieven voor zoekprogramma&#39;s aan te passen, opnieuw te richten of uit te voeren.

[!DNL Google Tag Manager] Hiermee worden gegevens en gebeurtenissen rechtstreeks overgedragen aan [!DNL Google Analytics], Enhanced Ecommerce en andere analysemogelijkheden van derden om een duidelijk beeld te krijgen van de prestaties van uw site, producten en promoties.

U moet een [!DNL Google Analytics] en [!DNL Tag Manager] om dit proces voort te zetten. De volgende instructies leiden u door het proces om uw Google rekeningen te vormen, uw opslag van de Handel te vormen, en een markering te creëren.

>[!NOTE]
>
>Als uw bedrijf onderworpen is aan privacyregels zoals [Algemene verordening inzake gegevensbescherming](../getting-started/compliance-gdpr.md) en/of de [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), zie [Google Privacy-instellingen](google-tools.md#google-privacy-settings).

## Stap 1. Configureer uw [!DNL Google Analytics] account

Zie [Zoeken naar sites instellen](https://support.google.com/analytics/answer/1012264) in Google Help voor de basisbeginselen die u nodig hebt om aan de slag te gaan. Zie ook de Google-hulplijnen voor [Googles Analytics](https://support.google.com/analytics/answer/9304153) en [Google-tagbeheer](https://support.google.com/tagmanager/answer/6102821).

1. Aanmelden bij uw [!DNL Google Analytics] account.

1. Inschakelen **[!UICONTROL Internal Site Search Tracking]** Ga als volgt te werk:

   - Ga naar **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Set **[!UICONTROL Site Search Tracking]** tot `On`.

   - Set **[!UICONTROL Query]** parameter to `q`.

   - Wanneer voltooid, **[!UICONTROL Save]** de instellingen.

1. Ga als volgt te werk om weergavefuncties in te schakelen:

   - Kies **[!UICONTROL Property Settings]**.

   - Onder _[!UICONTROL Advertising Features]_, set **[!UICONTROL Enable Demographics and Interest Reports]**tot `On`.

   - **[!UICONTROL Save]** de instellingen.

1. Ga als volgt te werk om e-commerce Tracking in te schakelen:

   - Ga naar **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Set **[!UICONTROL Enable Ecommerce]** tot `On`.

   - Set **[!UICONTROL Enable Enhanced Ecommerce Reporting]** tot `On`.

   - **[!UICONTROL Save]** de instellingen.

1. Laad de pagina opnieuw en controleer of alle instellingen behouden blijven `On`.

   >[!NOTE]
   >
   >Als niet alle instellingen `On`, herhaalt u de vorige stappen, slaat u de pagina op en laadt u deze opnieuw. Herhaal dit proces totdat alle instellingen zijn ingesteld op `On`.

## Stap 2. Configureer uw [!DNL Google Tag Manager] account

De volgende instructies tonen hoe te om een nieuwe container met de basismontages te vormen. Een monster [Composer](https://developer.adobe.com/commerce/php/development/composer/) .json-bestand (configuration) wordt gebruikt om het proces te vereenvoudigen en importeren om een tag in een nieuwe container te genereren. In dit voorbeeld wordt het aangeraden een container te maken in plaats van een bestaande container te wijzigen.

>[!NOTE]
>
>Zie Google voor meer informatie [Exporteren en importeren van containers](https://support.google.com/tagmanager/answer/6106997). Deze instructies bieden een doorloop voor het importeren van een voorbeeld-JSON in een nieuwe container.

1. Het gekoppelde bestand downloaden [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), opent u het bestand in een editor en slaat u het op als `GTM_M2_Config.json`.

   Het JSON-bestand wordt rechtstreeks geüpload naar [!DNL Google Tag Manager].

1. Ga naar **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Klikken **[!UICONTROL Choose container file]** en selecteert u het json-bestand.

1. Onder **[!UICONTROL Choose workspace]**, klikt u op **[!UICONTROL New]**.

1. Voer een titel en beschrijving in en klik vervolgens op **[!UICONTROL Save]**.

1. Selecteer een van de volgende handelingen om het bestand te importeren:

   - De **[!UICONTROL Overwrite]** Deze optie moet worden geselecteerd voor een nieuwe container.

   - De **[!UICONTROL Merge]** Deze optie moet zijn ingeschakeld als u een bestaande container gebruikt.

1. Klikken **[!UICONTROL Preview]** om de tags, triggers en variabelen te bekijken.

1. Als u de opdracht **[!UICONTROL Google Analytics ID]** waarnaar wordt verwezen in variabelen, gaat u als volgt te werk:

   - Ga naar **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Kies **[!UICONTROL Google Analytics]** en werk de tijdelijke aanduiding (`UA-xxxxxx-x`) met uw eigen **[!UICONTROL GA ID]**.

1. Volg de instructies van Google voor het toevoegen van tags, triggers en variabelen aan de nieuwe container.

   Als u instellingen in een andere container hebt die u wilt gebruiken, kunt u deze naar de nieuwe container verplaatsen.

1. Klikken **[!UICONTROL Confirm]** wanneer voltooid.

1. Volg de instructies van Google voor het publiceren van de nieuwe container.

## Stap 3. Uw winkel configureren

{{gtag-api-note}}

1. Meld u aan bij de beheerder van de winkel Commerce.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Google API]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Google Analytics]** en configureert u het volgende:

   ![Verkoopconfiguratie - Googles Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Enable]** tot `Yes`.

   - Set **[!UICONTROL Account type]** tot `Google Tag Manager`.

   - In de **[!UICONTROL Container ID]** veld, voer uw GTM-id in (`GTM-xxxxxx`).

   - Als u ook Googles Analytics gebruikt om inhoud te experimenteren, stelt u **Inhoud-experimenten inschakelen** tot `Yes`.

   - Gebruik de standaardwaarden voor de overige velden.

1. Klik op **[!UICONTROL Save Config]**.

1. Test uw [!DNL Google Tag Manager] en controleert u of alles correct werkt.

>[!NOTE]
>
>Elke container is gekoppeld aan één website en u hebt slechts één container per account nodig. Als u een instantie van de Handel van meerdere plaatsen hebt, hebt u afzonderlijke containers nodig.

## Stap 4. Voeg de GTM-code toe aan uw Adobe Commerce-winkel

1. Ga naar **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   Er zijn twee GTM-codefragmenten die moeten worden toegevoegd aan uw site voor handel: het eerste codefragment voor de `<head>` en de tweede voor de `<body>` -tag.

1. Ga in Commerce Admin naar **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**en opent u de winkelweergave in de bewerkingsmodus.

1. Onder _[!UICONTROL Other Settings]_, uitbreiden **[!UICONTROL HTML Head]**en plak de code die u van GTM voor `<head>` in de **[!UICONTROL Scripts and Style Sheets]**veld.

   ![Code invoegen in de HTML Head](./assets/head-tag.png){width="600" zoomable="yes"}

1. Uitbreiden **[!UICONTROL Footer]** en plak de GTM-code voor `<body>` in de **[!UICONTROL Miscellaneous HTML]** veld.

   ![Code in de voettekst invoegen](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Configuration]**.

## Veldomschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable] | Winkelweergave | Bepaalt als de Googles Analytics Verbeterde Handel kunnen worden gebruikt om activiteit in uw opslag te analyseren. Opties: `Yes` / `No` |
| [!UICONTROL Account type] | Winkelweergave | Bepaalt de het volgen code van Google die wordt gebruikt om opslagactiviteit en verkeer te controleren. Opties: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Winkelweergave | Bepaalt als het identificeren van informatie uit IP adressen wordt verwijderd die in Googles Analytics resultaten verschijnen. |
| [!UICONTROL Enable Content Experiments] | Winkelweergave | Activeert Google Content Experiments, waarmee u maximaal tien verschillende versies van dezelfde pagina kunt testen. Opties: `Yes` / `No` |
| [!UICONTROL Container Id] | Winkelweergave | Indien [!DNL Google Tag Manager] is al geïnstalleerd en geconfigureerd voor uw winkel, wordt de container-id automatisch in dit veld weergegeven. |
| [!UICONTROL List property for the catalog page] | Winkelweergave | Hiermee wordt de eigenschap Tagbeheer geïdentificeerd die is gekoppeld aan de cataloguspagina. Standaardwaarde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan het dwars-verkoopblok. Standaardwaarde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan het up-sell blok. Standaardwaarde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan het verwante productblok. Standaardwaarde: `Related Products` |
| [!UICONTROL List property for the search results page] | Winkelweergave | Hiermee wordt de eigenschap Tagbeheer geïdentificeerd die is gekoppeld aan de pagina met zoekresultaten. Standaardwaarde: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan de etiketten voor interne bevorderingen. Standaardwaarde: `Label` |

{style="table-layout:auto"}

## Een tag maken voor het bijhouden van conversies

Als u een Google AdWords-account hebt, kunt u een tag maken die conversies bijhoudt. In het volgende voorbeeld wordt getoond hoe u beide kunt gebruiken [!DNL Google Tag Manager] en [!DNL Google Analytics] om een tag te maken die wordt geactiveerd tijdens de conversie van uw winkel _Succes_ pagina.

### Stap 1. Een tag maken

1. Aanmelden bij uw [!DNL Google Tag Manager] en klik op de koppeling voor de container die u voor uw winkel hebt gemaakt.

1. In de **[!UICONTROL New Tag]** vak, klikt u op **[!UICONTROL Add a new tag]**.

1. Haal de volgende informatie op van je AdWords-account:

   - Conversie-id
   - Conversielabel

   Ga voor hulp naar Google [ondersteuningssite](https://support.google.com/tagmanager/answer/6105160).

1. Van de [!DNL Google Tag Manager] dashboard, klik **[!UICONTROL Google AdWords]** en voer de volgende handelingen uit:

   - Klik op de tijdelijke aanduiding voor de titel en voer een naam voor de nieuwe tag in.

   - Selecteer onder **[!UICONTROL Choose Product]** de optie **[!UICONTROL Google AdWords]**.

   - Onder _[!UICONTROL Choose a Tag Type]_, selecteert u **[!UICONTROL AdWords Conversion Tracking]**en klik op **[!UICONTROL Continue]**.

1. Voer de **[!UICONTROL Conversion ID]** en **[!UICONTROL Conversion Label]** van uw Advertentieaccount en klik op **[!UICONTROL Continue]**.

### Stap 2. Een regel maken

Doorgaan vanuit de [!DNL Google Tag Manager] Het dashboard, de volgende stap is een regel tot stand te brengen die de markering op de omzettingspagina in brand steken.

1. Onder **[!UICONTROL Fire On]**, klikt u op **[!UICONTROL Some Pages]**.

1. In de _[!UICONTROL Choose Pages]_in, voert u de volgende instellingen in:

   - **[!UICONTROL Name]** - Voer een naam in voor de paginabeschrijving.

   - **[!UICONTROL Variable]** `url`

   - **Bewerking** - `matches RegEx`

     Zie voor meer informatie [Operatoren Regex en CSS-kiezer](https://support.google.com/tagmanager/answer/7679109) in de Help van Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Selecteer het groene selectievakje en klik op **[!UICONTROL Save]**.

   De trigger die u instelt, wordt weergegeven als een blauwe knop in het gedeelte Vuur op.

1. Klik op **[!UICONTROL Save Tag]**.

### Stap 3. Voorvertonen en publiceren

De volgende stap in het proces is een voorvertoning van de tag. Elke keer dat een voorvertoning van de tag wordt weergegeven, wordt een momentopname van de versie opgeslagen. Als u tevreden bent met het resultaat, gaat u naar de gewenste versie en klikt u op **[!UICONTROL Publish]**.
