---
title: Pagina's
description: Leer details over de pagina's van de kerninhoud inbegrepen met de  [!DNL Commerce]  demoopslag, en het veranderen van de configuratie van de Pagina's Standaard.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# Pagina&#39;s

Inhoud kan worden bekeken in termen van de houdbaarheid, net als elk product in een winkel. Wist u dat de houdbaarheid van sociale media-inhoud minder dan 24 uur bedraagt? De potentiële houdbaarheid van de inhoud die u maakt, kan u helpen te bepalen waar u uw bronnen wilt investeren.

De inhoud met een lange houdbaarheid wordt soms bedoeld als _evergreen inhoud_. De voorbeelden van de algroene inhoud omvatten de verhalen van het klantensucces, _hoe te_ instructies, en Veelgestelde Vragen (FAQ). Inhoud die door de natuur aan bederf onderhevig is, omvat daarentegen gebeurtenissen, nieuws uit de industrie en persberichten.

![ De pagina Over ons die is opgenomen in het Luminagearchief van het voorbeeld ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Basisinhoudpagina&#39;s

In de demo-store van [!DNL Commerce] staan voorbeelden van de belangrijkste inhoudspagina&#39;s waarmee u aan de slag kunt. Al deze pagina&#39;s kunnen worden aangepast aan uw behoeften. Bekijk de volgende pagina&#39;s in uw opslag en zorg ervoor dat de inhoud uw bericht, stem, en merk overbrengt.

### Home

De demo [ 1} pagina van het Huis {omvat een banner, een beeldcarrousel, verscheidene statische blokken met verbindingen, en een lijst van nieuwe producten.](../getting-started/storefront.md#home-page)

### Privacybeleid

De opslag [ pagina van het Beleid van de Privacy ](../getting-started/privacy-policy.md) zou met uw eigen informatie moeten worden bijgewerkt. Als beste praktijken, zou uw privacybeleid aan uw klanten het type van informatie moeten verklaren dat uw bedrijf verzamelt en hoe het wordt gebruikt.

### 404 Niet gevonden

De pagina 404 Pagina niet gevonden wordt genoemd naar de antwoordcode die wordt geretourneerd wanneer een pagina niet kan worden gevonden. URL-omleidingen verminderen het aantal keren dat deze pagina wordt weergegeven. Nochtans, voor die tijden wanneer het noodzakelijk is, zou u uit de kans kunnen ook voordeel halen om sommige verbindingen aan te bieden aan producten die de klant interessant zou kunnen vinden.

### Toegang geweigerd

{{b2b-feature}}

De [ Ontkende Toegang ](../b2b/account-company-roles-permissions.md) pagina verschijnt wanneer de toestemmingen die aan een bedrijfgebruiker worden toegewezen toegang tot de pagina verhinderen.

### Cookies inschakelen

[ laat Cookies ](../getting-started/compliance-cookie-law.md) pagina toe verschijnt wanneer de bezoekers aan uw plaats geen koekjes hebben die in hun browsers worden toegelaten. De pagina bevat stapsgewijze, geïllustreerde instructies om cookies in te schakelen voor de populairste browsers.

### Service niet beschikbaar

De [ 503 niet beschikbare ](../configuration-reference/general/general.md) pagina van de Dienst wordt genoemd voor de antwoordcode die is teruggekeerd wanneer de server niet beschikbaar is.

### Over ons

De pagina Over ons is gekoppeld vanuit de voettekst van uw winkel. U kunt afbeeldingen, video, koppelingen naar persberichten en aankondigingen opnemen. De voorbeeldpagina heeft een afbeelding aan de rechterkant en een decoratieve pagina die het einde van de pagina aangeeft.

### Klantenservice

De pagina van de Dienst van de Klant is een ander knooppunt in de paginahiërarchie. De twee kopballen op de pagina hebben inhoud die slechts zichtbaar wordt wanneer de klant de kopbal klikt.

![ pagina van de Dienst van de Klant op de winkel ](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Standaardpagina&#39;s configureren

De _standaardconfiguratie van Pagina&#39;s_ bepaalt de het landen pagina die met [ basis URL ](../stores-purchase/store-urls.md) en de overeenkomstige homepage wordt geassocieerd. Het bepaalt ook welke pagina verschijnt wanneer de a _Gevonden niet Pagina_ fout voorkomt, en als het spoor van a [ breadcrumb ](../catalog/navigation-breadcrumb-trail.md) bij de bovenkant van elke pagina verschijnt.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_de optie **[!UICONTROL Web]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Default Pages]** sectie uit.

   ![ Standaardpagina&#39;s ](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Veld | [ Reikwijdte ](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Winkelweergave | Geeft de bestemmingspagina aan die aan de basis-URL is gekoppeld. Standaard is dit veld ingesteld op `cms` om een pagina aan te geven vanuit het inhoudsbeheersysteem van [!DNL Commerce] . U kunt ook een ander type bestemmingspagina gebruiken, zoals een blog. Als een blog bijvoorbeeld is geïnstalleerd op de server op `magento/blog` , kunt u de mapnaam `blog` invoeren als een relatief pad naar de selectie van pagina&#39;s. |
   | [!UICONTROL CMS Home Page] | Winkelweergave | Als u de homepage voor de winkel wilt kiezen, selecteert u gewoon de CMS-pagina in de lijst. Standaard wordt op de startpagina van CMS de volledige selectie van CMS-pagina&#39;s weergegeven die beschikbaar zijn voor je winkel. |
   | [!UICONTROL Default No-route URL] | Winkelweergave | Bevat de URL van de standaardpagina die u wilt weergeven wanneer een fout `404 Page not Found` optreedt. De standaardwaarde is `cms/noroute/index` . |
   | [!UICONTROL CMS No Route Page] | Winkelweergave | Hiermee wordt een specifieke CMS-pagina aangegeven die moet worden weergegeven wanneer een fout van 404 pagina niet gevonden optreedt. De standaardpagina is `404 Not Found` . |
   | [!UICONTROL CMS No Cookies Page] | Winkelweergave | Hiermee wordt een specifieke CMS-pagina aangegeven die wordt weergegeven wanneer cookies niet zijn ingeschakeld voor de browser. Op de pagina wordt uitgelegd waarom cookies worden gebruikt en hoe u deze voor elke browser inschakelt. De standaardpagina is `Enable Cookies` . |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Winkelweergave | Hiermee wordt bepaald of een broodkruimelspoor op alle CMS-pagina&#39;s in de catalogus wordt weergegeven. Opties: `Yes` / `No` |

   {style="table-layout:auto"}

1. Voer bij **[!UICONTROL Default Web URL]** het relatieve pad in naar de map in de [!DNL Commerce] -installatie die de bestemmingspagina bevat.

   De standaardinstelling `cms` geeft een pagina aan vanuit het inhoudsbeheersysteem van [!DNL Commerce] .

   >[!NOTE]
   >
   >Voor een specifieke opslagweergave schakelt u het selectievakje **[!UICONTROL Use Default]** naast _[!UICONTROL Default Web URL]_uit en eventuele andere standaardinstellingen die moeten worden gewijzigd.

1. Stel **[!UICONTROL CMS Home Page]** in op de CMS-pagina die u als startpagina wilt gebruiken. Andere gemaakte pagina&#39;s kunnen als de homepage worden gebruikt, zoals:

   - Welkom bij de exclusieve online winkel
   - Punten belonen
   - Over ons
   - Klantenservice
   - Cookies inschakelen
   - Privacybeleid
   - Bedrijf: Toegang geweigerd

1. Voor **[!UICONTROL Default No-route URL]**, ga de relatieve weg aan de omslag in de [!DNL Commerce] installatie in waar de pagina wordt opnieuw gericht wanneer de a _404 niet Gevonden Pagina_ fout voorkomt.

   De standaardwaarde is `cms/index/noRoute` .

1. Plaats **[!UICONTROL CMS No Route Page]** aan de pagina van CMS die verschijnt wanneer a _404 pagina niet gevonden_ fout voorkomt.

1. Stel **[!UICONTROL CMS No Cookies Page]** in op de CMS-pagina die wordt weergegeven wanneer cookies zijn uitgeschakeld in de browser. Op de pagina wordt uitgelegd waarom cookies worden gebruikt en hoe u deze voor elke browser inschakelt. De standaardpagina is `Enable Cookies` .

1. Stel **[!UICONTROL Show Breadcrumbs for CMS Pages]** in op `Yes` als u een breedbandtrail boven aan alle CMS-pagina&#39;s wilt weergeven.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
