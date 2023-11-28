---
title: Pagina's
description: Meer informatie over de basisinhoudspagina's die bij de [!DNL Commerce] opslaan van gegevens en het wijzigen van de configuratie Standaardpagina's.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# Pagina&#39;s

Inhoud kan worden bekeken in termen van de houdbaarheid, net als elk product in een winkel. Wist u dat de houdbaarheid van sociale media-inhoud minder dan 24 uur bedraagt? De potentiële houdbaarheid van de inhoud die u maakt, kan u helpen te bepalen waar u uw bronnen wilt investeren.

Inhoud met een lange houdbaarheid wordt soms ook wel _groengehalte_. Voorbeelden van groene inhoud zijn succesverhalen van klanten. _hoe te_ instructies en veelgestelde vragen (FAQ). Inhoud die door de natuur aan bederf onderhevig is, omvat daarentegen gebeurtenissen, nieuws uit de industrie en persberichten.

![De pagina About Us die is opgenomen in het voorbeeld van het Luma-archief ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Basisinhoudpagina&#39;s

De [!DNL Commerce] demo store bevat voorbeelden van basisinhoudspagina&#39;s die u helpen aan de slag te gaan. Al deze pagina&#39;s kunnen worden aangepast aan uw behoeften. Bekijk de volgende pagina&#39;s in uw opslag en zorg ervoor dat de inhoud uw bericht, stem, en merk overbrengt.

### Home

De demo [Home](../getting-started/storefront.md#home-page) Deze pagina bevat een banner, een carrousel voor afbeeldingen, verschillende statische blokken met koppelingen en een lijst met nieuwe producten.

### Privacybeleid

De winkel [Privacybeleid](../getting-started/privacy-policy.md) wordt bijgewerkt met uw eigen gegevens. Als beste praktijken, zou uw privacybeleid aan uw klanten het type van informatie moeten verklaren dat uw bedrijf verzamelt en hoe het wordt gebruikt.

### 404 Niet gevonden

De pagina 404 Pagina niet gevonden wordt genoemd naar de antwoordcode die wordt geretourneerd wanneer een pagina niet kan worden gevonden. URL-omleidingen verminderen het aantal keren dat deze pagina wordt weergegeven. Nochtans, voor die tijden wanneer het noodzakelijk is, zou u uit de kans kunnen ook voordeel halen om sommige verbindingen aan te bieden aan producten die de klant interessant zou kunnen vinden.

### Toegang geweigerd

{{b2b-feature}}

De [Toegang geweigerd](../b2b/account-company-roles-permissions.md) wordt weergegeven wanneer de machtigingen die aan een bedrijfsgebruiker zijn toegewezen, toegang tot de pagina voorkomen.

### Cookies inschakelen

De [Cookies inschakelen](../getting-started/compliance-cookie-law.md) wordt weergegeven wanneer bezoekers van uw site cookies niet hebben ingeschakeld in hun browsers. De pagina bevat stapsgewijze, geïllustreerde instructies om cookies in te schakelen voor de populairste browsers.

### Service niet beschikbaar

De [503 Service niet beschikbaar](../configuration-reference/general/general.md) Deze pagina krijgt de naam van de antwoordcode die wordt geretourneerd wanneer de server niet beschikbaar is.

### Over ons

De pagina Over ons is gekoppeld vanuit de voettekst van uw winkel. U kunt afbeeldingen, video, koppelingen naar persberichten en aankondigingen opnemen. De voorbeeldpagina heeft een afbeelding aan de rechterkant en een decoratieve pagina die het einde van de pagina aangeeft.

### Klantenservice

De pagina van de Dienst van de Klant is een ander knooppunt in de paginahiërarchie. De twee kopballen op de pagina hebben inhoud die slechts zichtbaar wordt wanneer de klant de kopbal klikt.

![De pagina van de Dienst van de klant op de winkel](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Standaardpagina&#39;s configureren

De _Standaardpagina&#39;s_ de configuratie bepaalt de landingspagina die met wordt geassocieerd [basis-URL](../stores-purchase/store-urls.md) en de bijbehorende homepage. Hiermee bepaalt u ook welke pagina wordt weergegeven als een _Pagina niet gevonden_ fout treedt op en als een [broodkruimelspoor](../catalog/navigation-breadcrumb-trail.md) boven aan elke pagina.

1. Op de _Beheerder_ zijbalk, ga naar  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Web]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Default Pages]** sectie.

   ![Standaardpagina&#39;s](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Veld | [Toepassingsgebied](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Winkelweergave | Geeft de bestemmingspagina aan die aan de basis-URL is gekoppeld. Dit veld is standaard ingesteld op `cms` om een pagina aan te geven van de [!DNL Commerce] contentbeheersysteem. U kunt ook een ander type bestemmingspagina gebruiken, zoals een blog. Als bijvoorbeeld een blog op de server is geïnstalleerd op `magento/blog`, kunt u de mapnaam invoeren `blog` als een relatief pad naar de selectie van pagina&#39;s. |
   | [!UICONTROL CMS Home Page] | Winkelweergave | Als u de homepage voor de winkel wilt kiezen, selecteert u gewoon de CMS-pagina in de lijst. Standaard wordt op de CMS-startpagina de volledige selectie van CMS-pagina&#39;s weergegeven die beschikbaar zijn voor uw winkel. |
   | [!UICONTROL Default No-route URL] | Winkelweergave | Bevat de URL van de standaardpagina die u wilt weergeven als een `404 Page not Found` fout treedt op. De standaardwaarde is `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Winkelweergave | Hiermee wordt een specifieke CMS-pagina aangegeven die moet worden weergegeven wanneer een fout van 404 pagina niet gevonden optreedt. De standaardpagina is `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Winkelweergave | Hiermee wordt een specifieke CMS-pagina aangegeven die wordt weergegeven wanneer cookies niet zijn ingeschakeld voor de browser. Op de pagina wordt uitgelegd waarom cookies worden gebruikt en hoe u deze voor elke browser inschakelt. De standaardpagina is `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Winkelweergave | Hiermee wordt bepaald of een breedbandtrail op alle CMS-pagina&#39;s in de catalogus wordt weergegeven. Opties: `Yes` / `No` |

   {style="table-layout:auto"}

1. Voor **[!UICONTROL Default Web URL]**, voert u het relatieve pad naar de map in het dialoogvenster [!DNL Commerce] een installatie die de openingspagina bevat.

   De standaardinstelling, `cms`, geeft een pagina aan vanuit de [!DNL Commerce] contentbeheersysteem.

   >[!NOTE]
   >
   >Wis voor een specifieke winkelweergave de optie **[!UICONTROL Use Default]** selectievakje naast _[!UICONTROL Default Web URL]_en andere standaardinstellingen die moeten worden gewijzigd.

1. Set **[!UICONTROL CMS Home Page]** op de CMS-pagina die als startpagina moet worden gebruikt. Andere gemaakte pagina&#39;s kunnen als de homepage worden gebruikt, zoals:

   - Welkom bij de exclusieve online winkel
   - Punten belonen
   - Over ons
   - Klantenservice
   - Cookies inschakelen
   - Privacybeleid
   - Bedrijf: Toegang geweigerd

1. Voor **[!UICONTROL Default No-route URL]**, voert u het relatieve pad naar de map in het dialoogvenster [!DNL Commerce] installatie waar de pagina wordt omgeleid wanneer een _404 pagina niet gevonden_ fout treedt op.

   De standaardwaarde is `cms/index/noRoute`.

1. Set **[!UICONTROL CMS No Route Page]** naar de CMS-pagina die wordt weergegeven wanneer een _404 pagina niet gevonden_ fout treedt op.

1. Set **[!UICONTROL CMS No Cookies Page]** op de CMS-pagina die wordt weergegeven wanneer cookies zijn uitgeschakeld in de browser. Op de pagina wordt uitgelegd waarom cookies worden gebruikt en hoe u deze voor elke browser inschakelt. De standaardpagina is `Enable Cookies`.

1. Als u een broodkruimelspoor bij de bovenkant van alle CMS pagina&#39;s wilt verschijnen, plaats **[!UICONTROL Show Breadcrumbs for CMS Pages]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.
