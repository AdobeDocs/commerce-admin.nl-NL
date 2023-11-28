---
title: '[!DNL Page Builder] Werkruimte'
description: Meer informatie over de gereedschappen in het dialoogvenster [!DNL Page Builder] werkruimte maken wanneer u basispagina's, product- en cataloguspagina's, blokken en dynamische blokken maakt.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# [!DNL Page Builder] Werkruimte

Wanneer [[!DNL Page Builder] is ingeschakeld](setup.md)de _[!UICONTROL Content]_sectie en het proces voor het maken van inhoud worden gewijzigd om te profiteren van de geavanceerde [!DNL Page Builder] tools voor CMS [pagina&#39;s](../content-design/page-add.md), [product](../catalog/product-content.md) en [categorie](../catalog/categories-content-settings.md) pagina&#39;s, [blokken](../content-design/block-add.md), en [dynamische blokken](../content-design/dynamic-blocks.md). Deze sectie bevat een_ Inhoudskop _, een voorvertoning van de inhoud en eenvoudige toegang tot het volledige scherm [!DNL Page Builder] werkruimte.

![Sectie Inhoud met [!DNL Page Builder] voorvertoning](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Inhoudskop

Omdat zoekprogramma&#39;s op niveau 1 (H1) koppen zoeken, is het toevoegen van een kop op niveau 1 een eenvoudige manier om ervoor te zorgen dat de pagina correct wordt geïndexeerd.

>[!NOTE]
>
>De _[!UICONTROL Content Heading]_veld dat boven aan de pagina wordt weergegeven, is een verouderd veld dat inhoud ondersteunt die met eerdere [!DNL Commerce] lozingen. Het maakt echter geen deel uit van [!DNL Page Builder]. De [!UICONTROL Content Heading] wordt opgemaakt als een H1-kop op basis van het stijlblad dat aan het huidige thema is gekoppeld. Deze bevindt zich vlak boven het actieve inhoudsgebied dat wordt gedefinieerd door het tabblad [!DNL Page Builder] in het werkgebied.

Voor de beste controle over de plaatsing en het formaat van rubrieken van alle niveaus, adviseert men dat u het verlaten van _[!UICONTROL Content Heading]_veld leeg is en de [!DNL Page Builder] [Kop](heading.md) inhoudstype.

![Inhoudskop en andere koppen](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Voorvertoning

Wanneer u de _[!UICONTROL Content]_en er is bestaande inhoud gemaakt met [!DNL Page Builder]wordt een voorvertoning van de inhoud weergegeven zoals deze op een pagina wordt weergegeven. Klikken **[!UICONTROL Edit with Page Builder]**of in het voorvertoningsgebied van de inhoud om het dialoogvenster [!DNL Page Builder] waar u de benodigde updates kunt uitvoeren.

![Voorvertoning van productbeschrijving](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Voor de product- en categorieformulieren is deze voorbeeldweergave van de inhoud standaard ingeschakeld, maar kan deze worden uitgeschakeld. Als de prestaties achterblijven bij het laden van de voorvertoning, kunt u de voorvertoning uitschakelen in het dialoogvenster [Configuratie van inhoudsbeheer](../configuration-reference/general/content-management.md#advanced-content-tools) instellingen.

## Werkgebied

Wanneer u het dialoogvenster [!DNL Page Builder] vanuit de voorvertoning is het werkgebied het belangrijkste werkgebied waarin u inhoud kunt maken en opmaken en zelfs snel inhoud kunt bewerken. Het werkgebied is aanvankelijk leeg, zodat u het ontwerpoppervlak hebt waarin u rijen, kolommen en tabbladen vanuit het linkerdeelvenster kunt slepen.

>[!NOTE]
>
>Vanaf de release 2.4.1 is het bewerken van inhoud nu alleen op volledig scherm beschikbaar voor alle gebieden die worden beheerd door [!DNL Page Builder]—CMS-pagina&#39;s, product- en categoriepagina&#39;s, blokken en dynamische blokken. Bij bewerking op volledig scherm krijgt de inhoud de focus en wordt een weergave geboden die beter aansluit bij de gebruikerservaring op de winkel.

![Werkgebied met pagina-inhoud](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Viewports

A _viewport_ Dit is het zichtbare gebied van een webpagina dat een gebruiker ziet. In de ontwerpmodus Volledig scherm worden de viewportknoppen weergegeven boven de knop [!DNL Page Builder] om de inhoud weer te geven zoals de gebruiker die op de site ziet.

![Viewportknoppen](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] definieert ook onderbrekingspunten voor viewports. Met onderbrekingspunten worden de minimale en maximale breedte gedefinieerd waarbinnen bepaalde stijlen worden toegepast. De [!DNL Page Builder] viewports verstrekt de volgende inhoudsuitbreekpunten:

- **Onderbrekingspunt van bureaublad**—`min-width: 1024px`. Dit onderbrekingspunt past stijlen toe die voor viewport breedten worden bepaald die 1024 pixel en breder meten.
- **Mobiele onderbrekingspunten**—`max-width: 768px, min-width: 640px`. Deze onderbrekingspunten passen stijlen toe die zijn gedefinieerd voor viewport-breedten tussen 768 pixels en 640 pixels.

[!DNL Page Builder] viewports verstrekt twee eigenschappen: **_voorvertoningen van inhoud_** en **_onderbrekingspuntinstellingen_**.

### Voorvertoningen van inhoud

Standaard, [!DNL Page Builder] bevat twee voorvertoningen van viewport:

- **Desktop** — Geeft de voorvertoning van de inhoud weer zonder een vooraf gedefinieerde breedte. Door het bureaublad gedefinieerde stijlen (met een minimale breedte van 1024 pixels voor het onderbrekingspunt) worden nog steeds toegepast op de pagina. Maar de viewport van de Desktop breedte wordt bepaald door montages voor containerinhoudstypes, zoals Rijen. Als u de Desktop-viewport selecteert, ziet u hoe uw inhoud op de winkel is opgemaakt als de paginabreedte van de browser 1024 pixels en breder is.

  ![Bureaubladvoorvertoning met minimale breedte van 1024 pixels](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Mobiel** — Geeft de voorvertoning van de inhoud weer met een vooraf gedefinieerde breedte van 768 pixels. In tegenstelling tot de Desktop viewport, toont Mobile viewport uw paginainhoud bij een breedte van 768 pixel, samen met de stijlen die voor de breekpuntbreedten van 768 pixel (maximum) en 640 pixel (minimum) worden bepaald.

  ![Voorvertoning van mobiele viewport met minimale breedte van 768 pixels](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Instellingen voor onderbrekingspunten

Met de viewport-knoppen kunt u ook verschillende onderbrekingspuntstijlen toepassen op inhoudstypen op basis van de geselecteerde viewport. Standaard, [!DNL Page Builder] biedt onderbrekingspuntinstellingen voor de _[!UICONTROL Minimum Height]_velden Rijen, Kolommen, Tabs, Tabitems, Banners, Sliders en Dia&#39;s. Wanneer u de Mobiele viewport selecteert, dan open de redacteur voor één van die inhoudstypes, kunt u gebiedswaarden ingaan specifiek voor de Mobiele viewport breekpunten. In velden met inhoudstypen die specifieke instellingen voor onderbrekingspunten toestaan, wordt rechts van het veld een pictogram weergegeven, vergelijkbaar met het volgende voorbeeld voor een rij:

![Pictogramindicator voor instelling onderbrekingspunt](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Deelvenster

De [!DNL Page Builder] wordt links van het werkgebied weergegeven en bevat inhoudstypen die naar het werkgebied kunnen worden gesleept. Een container die specifiek is voor het inhoudstype wordt dan weergegeven met een gereedschapset met opties. De inhoudstypen worden als volgt geordend in het deelvenster:

### Layout

De _[!UICONTROL Layout]_van de [!DNL Page Builder] wordt gebruikt om rijen, kolommen of tabs toe te voegen aan het werkgebied. Wanneer u een inhoudstype van het paneel aan het stadium sleept, verschijnt een container met toolbox van opties die voor het inhoudstype specifiek zijn.

Standaard worden de [!DNL Page Builder] werkgebied is leeg. Terwijl u de inhoudstypen van de lay-out van het deelvenster naar het werkgebied sleept, kunt u ze boven, onder of in andere lay-outcontainers op de pagina plaatsen. Rijen kunnen alleen rechtstreeks aan het werkgebied worden toegevoegd.

![[!DNL Page Builder] deelvenster met inhoudstypen voor layout en werkgebied](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Inhoudstype Layout | Beschrijving |
| ------------------- |------------ |
| [Rij](row.md) | U kunt een nieuwe rij alleen slepen vanuit het deelvenster naar het werkgebied en boven of onder een andere rij, tab of kolomgroep plaatsen. Met de optie Dupliceren kunt u ook een kopie van een bestaande rij maken. |
| [Kolom](column.md) | U kunt een kolom van het deelvenster naar het werkgebied of naar rijen en tabs slepen. Het maximumaantal kolommen dat kan worden toegevoegd, wordt bepaald door het aantal rasterdivisies dat is opgegeven in het dialoogvenster [configuratie](setup.md). |
| [Tabs](tabs.md) | U kunt één tabblad van het deelvenster naar het werkgebied of naar rijen en kolommen slepen. U kunt extra tabbladen toevoegen vanuit de gereedschapset. |

{style="table-layout:auto"}

### Elementen

Gebruik de _[!UICONTROL Elements]_van de [!DNL Page Builder] om tekst, koppen, knoppen, scheidingslijnen en HTML-code toe te voegen aan een lay-outcontainer in het deelvenster [[!DNL Page Builder] stadium](workspace.md#stage). Wanneer u een inhoudstype van het paneel aan of een rij of een kolom, of aan een lusjereeks op het stadium sleept, verschijnt een container. Gebruik de gereedschapset voor inhoudstypen voor toegang tot de instellingen die specifiek zijn voor de tekst.

![[!DNL Page Builder] deelvenster met inhoudstypen voor elementen](./assets/pb-elements.png){width="600" zoomable="yes"}

| Type inhoud element | Beschrijving |
| -------------------- | ----------- |
| [Tekst](text.md) | Hiermee voegt u een tekstcontainer en -editor toe aan het werkgebied. |
| [Kop](heading.md) | Voegt een kopcontainer toe aan het werkgebied. |
| [Knoppen](buttons.md) | Hiermee voegt u een container voor een afzonderlijke knop of een set knoppen toe aan het werkgebied. |
| [Scheidingslijn](divider.md) | Voegt een container voor een scheidingslijn toe aan het werkgebied. |
| [HTML-code](html-code.md) | Voegt een container voor HTML-code toe aan het werkgebied. |

{style="table-layout:auto"}

### Media

Gebruik de _[!UICONTROL Media]_van de [!DNL Page Builder] om afbeeldingen, video, banners, schuifregelaars en [!DNL Google Maps] naar elke lay-outcontainer op de [[!DNL Page Builder] stadium](workspace.md#stage). Wanneer een type media-inhoud van het deelvenster naar het werkgebied wordt gesleept, wordt een container weergegeven met een gereedschapset met opties die specifiek zijn voor het inhoudstype.

![[!DNL Page Builder] deelvenster met media-inhoudstypen](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Het inhoudstype Media | Beschrijving |
| ------------------- | ------------------------------------------ |
| [Afbeelding](image.md) | Voegt een afbeeldingscontainer toe aan het werkgebied. |
| [Video](video.md) | Voegt een videopcontainer toe aan het werkgebied. |
| [Banner](banner.md) | Voegt een bannercontainer toe aan het werkgebied. |
| [Slider](slider.md) | Voegt een schuifregelaarcontainer toe aan het werkgebied. |
| [Kaart](map.md) | Hiermee voegt u een [!DNL Google Maps] naar het werkgebied. |

{style="table-layout:auto"}

### Inhoud toevoegen

Gebruik de _[!UICONTROL Add Content]_van de [!DNL Page Builder] om bestaande inhoud aan het [[!DNL Page Builder] stadium](workspace.md#stage). Wanneer u een inhoudstype voor media van het deelvenster naar het werkgebied sleept, wordt een container weergegeven. Gebruik de gereedschapset voor inhoudstypen voor toegang tot de_ Instellingen _die specifiek zijn voor het type.

![[!DNL Page Builder] deelvenster met typen inhoud toevoegen](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Inhoudstype | Beschrijving |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Blok](block.md) | Voegt een bestaand blok aan het stadium toe. |
| [Dynamisch blok](dynamic-block.md) | Voegt een bestaand dynamisch blok toe aan het werkgebied. |
| [Producten](products.md) | Hiermee voegt u een lijst met producten toe aan het werkgebied. |
| ![Alleen Adobe Commerce](../assets/adobe-logo.svg) [Product Recommendations](recommendations.md) | Voegt een aanbevolen eenheid aan het stadium toe. |

{style="table-layout:auto"}

## Gereedschapset

Elke inhoudscontainer in het werkgebied heeft een gereedschapset met opties. De opties variëren per inhoudstype, maar omvatten typisch Beweging, Montages, Verbergen/tonen, Dupliceren, en Verwijderen.

### De gereedschapset weergeven

Houd de muisaanwijzer boven de container om de gereedschapset weer te geven en kies een optie.

![Opties voor de gereedschapset Rij](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Opties voor gereedschapsset

| Optie | Pictogram | Beschrijving |
| --------- | ---------------------------------------- | ------------ |
| Verplaatsen | ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="25"} | Verplaatst de huidige inhoudscontainer naar een andere positie in het werkgebied. |
| Toevoegen | ![Pictogram toevoegen](./assets/pb-icon-add.png){width="25"} | Hiermee voegt u onderliggende elementen toe, zoals een knop, dia of tab. |
| (label) |           | Identificeert het containerinhoudstype. |
| Instellingen | ![Instellingenpictogram](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de eigenschappen van de inhoudscontainer in de bewerkingsmodus. |
| Verbergen | ![Pictogram verbergen](./assets/pb-icon-hide.png){width="25"} | Verbergt de huidige inhoudscontainer. |
| Tonen | ![Pictogram tonen](./assets/pb-icon-show.png){width="25"} | Hiermee wordt de huidige inhoudscontainer weergegeven. |
| Dupliceren | ![Pictogram Dupliceren](./assets/pb-icon-duplicate.png){width="25"} | Maakt een kopie van de huidige inhoudscontainer. |
| Verwijderen | ![Verwijderen](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de huidige inhoudscontainer uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}
