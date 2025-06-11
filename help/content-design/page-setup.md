---
title: Pagina-instelling
description: Leer hoe u de standaardwaarden voor de hoofdonderdelen van een winkelpagina configureert.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Pagina-instelling

De hoofdsecties van de pagina worden gedeeltelijk bestuurd door een set standaard HTML-tags. Sommige van deze labels kunnen worden gebruikt om de lettertypen, kleur, grootte, achtergrondkleuren en afbeeldingen te selecteren die in elke sectie van de pagina worden gebruikt. Andere instellingen bepalen pagina-elementen, zoals het logo in de koptekst en de copyrightvermelding in de voettekst. Deze secties komen overeen met de onderliggende structuur van de HTML-pagina en veel van de basiseigenschappen kunnen worden ingesteld via Beheer.

- [HTML Head](#html-head)
- [Koptekst](#header)
- [Voettekst](#footer)

![ HTML paginagedeelten ](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTML Head

De instellingen in de sectie HTML Head komen overeen met de tag `<head>` van een HTML-pagina en kunnen voor elke winkelweergave worden geconfigureerd. Naast metagegevens voor de paginatitel, beschrijving en trefwoorden bevat de sectie een koppeling naar het favicon en diverse scripts. In deze sectie worden ook instructies voor robots van zoekprogramma&#39;s en de weergave van de mededeling van de opslagdemo geconfigureerd.

### De HTML Head configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _Andere Montages_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL HTML Head]** sectie uit.

   ![ de configuratiemontages van het Kop van HTML ](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Werk [ favicon ](../getting-started/storefront-branding.md#add-a-favicon) indien nodig bij.

1. Pas de instellingen voor de paginatitel aan uw wensen aan:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   U kunt een achtervoegsel en/of voorvoegsel met de standaardtitel gebruiken om een titel van twee of drie delen te maken. U kunt een verticale balk of dubbele punt toevoegen als scheidingsteken tussen het voor- of achtervoegsel en de standaardtitel.

1. Voeg of wijzig meta- gegevens toe die de Optimalisering van de Motor van het Onderzoek (SEO) steunen en helpt klanten aan uw opslag van onderzoeksresultaten sturen:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Voer zo nodig een **[!UICONTROL Scripts and Style Sheets]** in.

   >[!NOTE]
   >
   >Alle JavaScript die u in het veld [!UICONTROL Scripts and Style Sheets] invoert, moet worden vermeld in de CSP-instellingen (Content Security Policy), anders wordt de code niet uitgevoerd op de afhandelingspagina&#39;s. Voor meer informatie, zie [ Beleid van de Veiligheid van de Inhoud ](https://developer.adobe.com/commerce/php/development/security/content-security-policies).


1. Laat of maak de [ kennisgeving van de duoopslag ](../getting-started/storefront-branding.md#set-the-store-demo-notice) indien nodig toe onbruikbaar.

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

### HTML Head-veldbeschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Winkelweergave | Uploadt de kleine grafische afbeelding die wordt weergegeven in de adresbalk en het tabblad van de browser. Toegestane bestandstypen: ICO, PNG, APNG, GIF en JPG (JPEG). Niet alle browsers ondersteunen deze indelingen. |
| [!UICONTROL Default Page Title] | Winkelweergave | De titel die wordt weergegeven op de titelbalk van elke pagina wanneer deze wordt weergegeven in een browser. De standaardtitel wordt gebruikt voor alle pagina&#39;s, tenzij voor afzonderlijke pagina&#39;s een andere titel is opgegeven. |
| [!UICONTROL Page Title Prefix] | Winkelweergave | Een voorvoegsel kan vóór de titel worden toegevoegd om een titel met twee of drie delen te maken. Een verticale balk of dubbele punt kan als scheidingsteken aan het einde van het voorvoegsel worden gebruikt om het te onderscheiden van de tekst van de hoofdtitel. |
| [!UICONTROL Page Title Suffix] | Winkelweergave | U kunt na de titel een achtervoegsel toevoegen om een titel van twee of drie delen te maken. Een verticale balk of dubbele punt kan als scheidingsteken aan het einde van het voorvoegsel worden gebruikt om het te onderscheiden van de tekst van de hoofdtitel. |
| [!UICONTROL Default Meta Description] | Winkelweergave | De beschrijving bevat een overzicht van je site voor aanbiedingen met zoekprogramma&#39;s en mag niet langer zijn dan 160 tekens. |
| [!UICONTROL Default Meta Keywords] | Winkelweergave | Een reeks trefwoorden die uw winkel beschrijven, elk gescheiden door een komma. |
| [!UICONTROL Scripts and Style Sheets] | Winkelweergave | Bevat scripts die in de HTML moeten worden opgenomen vóór de afsluitende tag `<head>` . JavaScript van derden die vóór de tag `<body>` moet worden geplaatst, kan hier bijvoorbeeld worden ingevoerd. |
| [!UICONTROL Display Demo Store Notice] | Winkelweergave | Controls the display of the demo store notice at the top of the page. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## Koptekst

De configuratie van de Kopbal identificeert de weg aan uw archiefembleem en specificeert de lt tekst van het embleem en welkomstbericht.

![ de configuratiemontages van de Kopbal ](./assets/configuration-header.png){width="400" zoomable="yes"}

### De koptekst configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _Andere Montages_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Header]** sectie uit.

1. Breng de gewenste wijzigingen aan in de winkelweergave:

   - [&#128279;](../getting-started/storefront-branding.md#upload-your-logo) montages van 0&rbrace; Logo &lbrace;
   - [ Welkome bericht ](../getting-started/storefront-branding.md#change-the-welcome-message) montages

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

### Beschrijvingen van koptekstvelden

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Winkelweergave | Identificeert het pad naar het logo dat in de koptekst wordt weergegeven. Ondersteunde bestandstypen: PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Winkelweergave | De breedte van de logoafbeelding in pixels. |
| [!UICONTROL Logo Attribute Height] | Winkelweergave | De hoogte van de logoafbeelding in pixels. |
| [!UICONTROL Welcome Text] | Winkelweergave | Het welkomstbericht wordt weergegeven in de koptekst van de pagina en bevat de naam van de klanten die zijn aangemeld. |
| [!UICONTROL Logo Image Alt] | Winkelweergave | De Alt-tekst die aan het logo is gekoppeld. |
| [!UICONTROL Translate Title] | Winkelweergave | Hiermee bepaalt u of de instructie `Page Title` of `Meta Title` moet worden vertaald. |

{style="table-layout:auto"}

## Voettekst

De sectie van de de configuratieconfiguratie van de Voettekst is waar u de [ copyrightkennisgeving ](../getting-started/storefront-branding.md#change-the-copyright-notice) kunt bijwerken die bij de bodem van de pagina verschijnt, en diverse manuscripten ingaan die vóór de sluitende `<body>` markering moeten worden geplaatst.

![ de configuratiemontages van de Voettekst ](./assets/configuration-footer.png){width="400" zoomable="yes"}

### De voettekst configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _Andere Montages_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Footer]** sectie uit.

1. Breng de benodigde wijzigingen aan in de instellingen **[!UICONTROL Copyright]** en **[!UICONTROL Miscellaneous HTML]** .

   >[!NOTE]
   >
   >Alle JavaScript die u in het veld [!UICONTROL Miscellaneous HTML] invoert, moet worden vermeld in de CSP-instellingen (Content Security Policy), anders wordt de code niet uitgevoerd op de afhandelingspagina&#39;s. Voor meer informatie, zie [ Beleid van de Veiligheid van de Inhoud ](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

## Beschrijvingen van voettekstvelden

| Veld | Toepassingsgebied | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Winkelweergave | Een invoervak waarin u diverse scripts naar de server kunt uploaden die vlak voor de afsluitende tag `<body>` moeten worden geplaatst. |
| [!UICONTROL Copyright] | Winkelweergave | De copyrightinstructie die onder aan elke pagina wordt weergegeven. Als u het copyrightsymbool wilt opnemen, gebruikt u de HTML-tekeneenheid `\&copy;` als volgt: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` vervang de copyrightkennisgeving voor het voorbeeld door uw eigen tekeneenheid. |
| [!UICONTROL Display Report Bugs Link] | Winkelweergave | Hiermee wordt bepaald of de koppeling voor het foutopsporingsrapport (ondersteund voor bepaalde thema&#39;s) is in- of uitgeschakeld. |

{style="table-layout:auto"}
