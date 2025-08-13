---
title: '[!DNL Google Tag Manager]'
description: Leer hoe te om  [!DNL Google Tag Manager]  te gebruiken om de vele markeringen (fragmenten van code) te beheren die met uw marketing campagnegebeurtenissen in uw plaatsen van Adobe Commerce verwant zijn.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] is een krachtig hulpmiddel dat u helpt diverse markeringen (codefragmenten) efficiënt beheren en op te stellen verbonden aan uw de campagnegebeurtenissen van de marketing. Met [!DNL Google Tag Manager] kunt u tags voor bijhouden toevoegen aan uw site om het publiek te meten of om marketinginitiatieven voor zoekprogramma&#39;s aan te passen, opnieuw te richten of uit te voeren.

[!DNL Google Tag Manager] brengt gegevens en gebeurtenissen rechtstreeks over naar [!DNL Google Analytics] , Enhanced Ecommerce en andere analyseoplossingen van derden om een duidelijk beeld te krijgen van hoe goed uw site, producten en promoties presteren.

U hebt een [!DNL Google Analytics] - en [!DNL Tag Manager] -account nodig om dit proces voort te zetten. Met de volgende instructies doorloopt u het proces voor het configureren van uw Google-accounts, het configureren van uw Commerce-winkel en het maken van een tag.

>[!NOTE]
>
>Als uw zaken aan privacyverordeningen zoals de [ Algemene Verordening van de Bescherming van Gegevens ](../getting-started/compliance-gdpr.md) en/of de [ Wet van de Privacy van de consument van Californië ](../getting-started/compliance-ccpa.md) onderworpen zijn, zie [ de Montages van de Privacy van Google ](google-tools.md#google-privacy-settings).

## Stap 1. Uw [!DNL Google Analytics] -account configureren

Zie [ het Onderzoek van de Plaats van de Opstelling ](https://support.google.com/analytics/answer/1012264) in de Hulp van Google voor de grondbeginselen u voor begonnen wordt nodig hebt. Zie ook de gidsen van Google voor [ Google Analytics ](https://support.google.com/analytics/answer/9304153) en [ de Manager van de Markering van Google ](https://support.google.com/tagmanager/answer/6102821).

1. Meld u aan bij uw [!DNL Google Analytics] -account.

1. Ga als volgt te werk om **[!UICONTROL Internal Site Search Tracking]** in te schakelen:

   - Ga naar **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Stel **[!UICONTROL Site Search Tracking]** in op `On` .

   - Stel de parameter **[!UICONTROL Query]** in op `q` .

   - Wanneer deze bewerking is voltooid, **[!UICONTROL Save]** de instellingen.

1. Ga als volgt te werk om weergavefuncties in te schakelen:

   - Kies **[!UICONTROL Property Settings]** .

   - Stel onder _[!UICONTROL Advertising Features]_&#x200B;de waarde **[!UICONTROL Enable Demographics and Interest Reports]**&#x200B;in op `On` .

   - **[!UICONTROL Save]** de instellingen.

1. Ga als volgt te werk om e-commerce Tracking in te schakelen:

   - Ga naar **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Stel **[!UICONTROL Enable Ecommerce]** in op `On` .

   - Stel **[!UICONTROL Enable Enhanced Ecommerce Reporting]** in op `On` .

   - **[!UICONTROL Save]** de instellingen.

1. Laad de pagina opnieuw en controleer of alle instellingen `On` blijven staan.

   >[!NOTE]
   >
   >Als niet alle instellingen `On` zijn, herhaalt u de vorige stappen, slaat u de pagina op en laadt u deze opnieuw. Herhaal dit proces totdat alle instellingen zijn ingesteld op `On` .

## Stap 2. Uw [!DNL Google Tag Manager] -account configureren

De volgende instructies tonen hoe te om een nieuwe container met de basismontages te vormen. Een steekproef {het 1} configuratiedossier van de Samensteller van de 1&rbrace; (.json) wordt gebruikt om het proces te vereenvoudigen, het invoeren om een markering in een nieuwe container te produceren. [&#128279;](https://developer.adobe.com/commerce/php/development/composer/) In dit voorbeeld wordt het aangeraden een container te maken in plaats van een bestaande container te wijzigen.

>[!NOTE]
>
>Voor extra informatie, zie de uitvoer en de invoer van de Container van Google [&#128279;](https://support.google.com/tagmanager/answer/6106997). Deze instructies bieden een doorloop voor het importeren van een voorbeeld-JSON in een nieuwe container.

1. Download het verbonden dossier [ GTM_M2_Config_json.txt ](./assets/GTM_M2_Config_json.txt), open het dossier in een redacteur, en bewaar het als `GTM_M2_Config.json`.

   Het JSON-bestand wordt rechtstreeks geüpload naar [!DNL Google Tag Manager] .

1. Navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]** .

1. Klik op **[!UICONTROL Choose container file]** en selecteer het JSON-bestand.

1. Klik onder **[!UICONTROL Choose workspace]** op **[!UICONTROL New]** .

1. Voer een titel en beschrijving in en klik op **[!UICONTROL Save]** .

1. Selecteer een van de volgende handelingen om het bestand te importeren:

   - De optie **[!UICONTROL Overwrite]** moet zijn geselecteerd voor een nieuwe container.

   - De optie **[!UICONTROL Merge]** moet zijn geselecteerd als u een bestaande container gebruikt.

1. Klik op **[!UICONTROL Preview]** om de tags, triggers en variabelen weer te geven.

1. Ga als volgt te werk om de **[!UICONTROL Google Analytics ID]** te bewerken waarnaar wordt verwezen in variabelen:

   - Navigeer naar **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]** .

   - Kies **[!UICONTROL Google Analytics]** en werk de tijdelijke aanduiding (`UA-xxxxxx-x` ) bij met uw eigen **[!UICONTROL GA ID]** .

1. Volg de instructies van Google voor het toevoegen van tags, triggers en variabelen aan de nieuwe container.

   Als u instellingen in een andere container hebt die u wilt gebruiken, kunt u deze naar de nieuwe container verplaatsen.

1. Klik op **[!UICONTROL Confirm]** wanneer u klaar bent.

1. Volg de instructies van Google voor het publiceren van de nieuwe container.

## Stap 3. Uw winkel configureren

{{gtag-api-note}}

1. Meld u aan bij de beheerder van uw Commerce-winkel.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Google API]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Google Analytics]** sectie uit en vorm het volgende:

   ![ configuratie van de Verkoop - Google Analytics ](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Enable]** in op `Yes` .

   - Stel **[!UICONTROL Account type]** in op `Google Tag Manager` .

   - Voer in het veld **[!UICONTROL Container ID]** uw GTM-id in (`GTM-xxxxxx` ).

   - Als u ook Google Analytics aan inhoudsexperimenten gebruikt, plaats **laat de Experimenten van de Inhoud** aan `Yes` toe.

   - Gebruik de standaardwaarden voor de overige velden.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Test de [!DNL Google Tag Manager] -instellingen en controleer of alles correct werkt.

>[!NOTE]
>
>Elke container is gekoppeld aan één website en u hebt slechts één container per account nodig. Als u een Commerce-instantie met meerdere sites hebt, hebt u aparte containers nodig.

## Veldomschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable] | Winkelweergave | Hiermee bepaalt u of Google Analytics Enhanced Ecommerce kan worden gebruikt om activiteiten in uw winkel te analyseren. Opties: `Yes` / `No` |
| [!UICONTROL Account type] | Winkelweergave | Bepaalt de het volgen code van Google die wordt gebruikt om opslagactiviteit en verkeer te controleren. Opties: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Winkelweergave | Hiermee bepaalt u of identificatiegegevens worden verwijderd uit IP-adressen die worden weergegeven in Google Analytics-resultaten. |
| [!UICONTROL Container Id] | Winkelweergave | Als [!DNL Google Tag Manager] al is geïnstalleerd en geconfigureerd voor uw winkel, wordt de container-id automatisch weergegeven in dit veld. |
| [!UICONTROL List property for the catalog page] | Winkelweergave | Hiermee wordt de eigenschap Tagbeheer geïdentificeerd die is gekoppeld aan de cataloguspagina. Standaardwaarde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan het dwars-verkoopblok. Standaardwaarde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan het up-sell blok. Standaardwaarde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan het verwante productblok. Standaardwaarde: `Related Products` |
| [!UICONTROL List property for the search results page] | Winkelweergave | Hiermee wordt de eigenschap Tagbeheer geïdentificeerd die is gekoppeld aan de pagina met zoekresultaten. Standaardwaarde: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Winkelweergave | Identificeert het bezit van de Manager van de Markering verbonden aan de etiketten voor interne bevorderingen. Standaardwaarde: `Label` |

{style="table-layout:auto"}

## Een tag maken voor het bijhouden van conversies

Als u een Google AdWords-account hebt, kunt u een tag maken die conversies bijhoudt. Het volgende voorbeeld toont hoe te om zowel [!DNL Google Tag Manager] als [!DNL Google Analytics] te gebruiken om een markering tot stand te brengen die op de 2&rbrace; Succespagina van de omzetting van uw opslag _in brand steekt._

### Stap 1. Een tag maken

1. Meld u aan bij uw [!DNL Google Tag Manager] -account en klik op de koppeling voor de container die u voor uw winkel hebt gemaakt.

1. Klik in het vak **[!UICONTROL New Tag]** op **[!UICONTROL Add a new tag]** .

1. Haal de volgende informatie op van je AdWords-account:

   - Conversie-id
   - Conversielabel

   Als u hulp nodig hebt, bezoek Google [ steunplaats ](https://support.google.com/tagmanager/answer/6105160).

1. Klik in het dashboard van [!DNL Google Tag Manager] op **[!UICONTROL Google AdWords]** en voer de volgende handelingen uit:

   - Klik op de tijdelijke aanduiding voor de titel en voer een naam voor de nieuwe tag in.

   - Selecteer onder **[!UICONTROL Choose Product]** de optie **[!UICONTROL Google AdWords]** .

   - Selecteer _[!UICONTROL Choose a Tag Type]_&#x200B;onder **[!UICONTROL AdWords Conversion Tracking]**&#x200B;en klik op **[!UICONTROL Continue]**.

1. Voer **[!UICONTROL Conversion ID]** en **[!UICONTROL Conversion Label]** in van uw AdWords-account en klik op **[!UICONTROL Continue]** .

### Stap 2. Een regel maken

Als u doorgaat vanaf het dashboard van [!DNL Google Tag Manager] , bestaat de volgende stap uit het maken van een regel waarmee de tag op de conversiepagina wordt geactiveerd.

1. Klik onder **[!UICONTROL Fire On]** op **[!UICONTROL Some Pages]** .

1. Voer in de sectie _[!UICONTROL Choose Pages]_&#x200B;de volgende instellingen in:

   - **[!UICONTROL Name]** - Voer een naam in voor de paginabeschrijving.

   - **[!UICONTROL Variable]** `url`

   - **Verrichting** - `matches RegEx`

     Meer leren, zie [ Regex en CSS selecteurs exploitanten ](https://support.google.com/tagmanager/answer/7679109) in de Hulp van de Manager van de Markering van Google.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Selecteer het groene selectievakje en klik op **[!UICONTROL Save]** .

   De trigger die u instelt, wordt weergegeven als een blauwe knop in het gedeelte Vuur op.

1. Klik op **[!UICONTROL Save Tag]** als de bewerking is voltooid.

### Stap 3. Voorvertonen en publiceren

De volgende stap in het proces is een voorvertoning van de tag. Elke keer dat een voorvertoning van de tag wordt weergegeven, wordt een momentopname van de versie opgeslagen. Als u tevreden bent met het resultaat, gaat u naar de gewenste versie en klikt u op **[!UICONTROL Publish]** .

## Aangepaste HTML-tag met JavaScript

In deze sectie wordt uitgelegd hoe u een CSP-abonnement één keer toevoegt aan de HTML-tag JavaScript Aangepast, zodat deze kan worden uitgevoerd op de afhandelingspagina, zodat wordt voldaan aan de CSP-vereisten (Content Security Policy). Deze toevoeging verbetert de sitebeveiliging door te voorkomen dat onbevoegde scripts worden uitgevoerd. Voor meer gedetailleerde informatie, zie de [ documentatie van het Beleid van de Veiligheid van de Inhoud 0&rbrace; &lbrace;.](https://developer.adobe.com/commerce/php/development/security/content-security-policies)

>[!NOTE]
>
>Het importeren van de globale variabele `cspNonce` naar Google Tag Manager wordt alleen ondersteund in Adobe Commerce versie 2.4.8 en hoger.

>[!WARNING]
>
>Het toevoegen van onbekende scripts aan uw winkel kan gegevensnadelig zijn. Scripts die zijn geautoriseerd op de afhandelingspagina kunnen vertrouwelijke klantgegevens, waaronder betalingsgegevens, stelen. Het is van essentieel belang dat u voorzorgsmaatregelen neemt om uw Google Tag Manager-account te beschermen. Voeg alleen vertrouwde scripts toe, controleer en controleer regelmatig uw tags en implementeer krachtige beveiligingsmaatregelen, zoals 2-factor verificatie (2FA) en toegangscontroles.

### Stap 1. Een CSP-variabele één keer maken

U kunt een CSP Nonce-variabele maken die binnen het Google-tagbeheer kan worden gebruikt door de variabeleconfiguratie te importeren of handmatig te configureren.

#### De variabele configuratie importeren

De NonceVariabele van CSP is inbegrepen in de voorbeeldcontainer [ GTM_M2_Config_json.txt ](./assets/GTM_M2_Config_json.txt). U kunt de variabele maken door deze code in uw werkruimte te importeren.

#### Handmatig de variabele maken

Als u niet de veranderlijke configuratie kunt invoeren, voltooi de volgende stappen hieronder om het tot stand te brengen.

1. In uw werkruimte, navigeer aan de **sectie van Variabelen** in sidebar.
1. Klik op de **Nieuwe** knoop bij de bodem van de pagina in de **user-defined sectie van Variabelen**.
1. Geef de variabele een naam `gtmNonce` .
1. Klik op het potloodpictogram om de variabele te bewerken.
1. Selecteer **Variabele van JavaScript** van de **Variabele van de Pagina** sectie.
1. Op het **gebied van de Naam van de Globale Variabele**, ga `window.cspNonce` in.
1. Sla de variabele op.

Meer over [ de Variabelen van de Manager van de Markering van Google ](https://support.google.com/tagmanager/answer/7683056?hl=en) leren, zie [ user-defined veranderlijke types voor Web ](https://support.google.com/tagmanager/answer/7683362?hl=en) in de documentatie van Google. In deze documentatie vindt u gedetailleerde instructies voor het maken en beheren van aangepaste variabelen die zijn afgestemd op het beheer van uw labels en die zijn afgestemd op specifieke marketing- en analytische behoeften.

### Stap 2. Een aangepaste HTML-tag maken

1. In uw werkruimte, navigeer aan de **sectie van Markeringen** in sidebar.
1. Klik de **Nieuwe** knoop.
1. In de **sectie van de Configuratie van de Markering**, de uitgezochte **Markering van HTML van de Douane**.
1. Voer de vereiste JavaScript in het tekstgebied in en voeg een eenmalig kenmerk toe aan de openingstag `<script>` die wijst naar de variabele die u in de vorige stap hebt gemaakt. Bijvoorbeeld:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Selecteer **Document.write van de Steun**.
1. In de **teweegbrengende** sectie, selecteer de gewenste trekker. Bijvoorbeeld, **toestemming Initialisatie - Alle Pagina&#39;s**.

Voor meer informatie over [ Markeringen ](https://support.google.com/tagmanager/answer/3281060) in de Manager van de Markering van Google, zie [ Eigen markeringen ](https://support.google.com/tagmanager/answer/6107167) in de documentatie van Google.
