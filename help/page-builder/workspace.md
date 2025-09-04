---
title: '[!DNL Page Builder] Workspace'
description: Leer over de hulpmiddelen beschikbaar in de  [!DNL Page Builder]  werkruimte wanneer u basispagina's, product en cataloguspagina's, blokken, en dynamische blokken creeert.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

Wanneer [[!DNL Page Builder]  ](setup.md) wordt toegelaten, worden de _[!UICONTROL Content]_sectie en het proces van de inhoudsverwezenlijking gewijzigd om uit de geavanceerde [!DNL Page Builder] hulpmiddelen voor CMS [ pagina&#39;s ](../content-design/page-add.md), [ product ](../catalog/product-content.md) en [ categorie ](../catalog/categories-content-settings.md) pagina&#39;s, [ blokken ](../content-design/block-add.md), en [ dynamische blokken ](../content-design/dynamic-blocks.md) voordeel te halen. Deze sectie omvat het gebied van de Kop van de a_ Inhoud _, een voorproef van de inhoud, en gemakkelijke toegang tot het volledig-schermwerkruimte [!DNL Page Builder].

![ sectie van de Inhoud met [!DNL Page Builder] voorproef ](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Inhoudskop

Omdat zoekprogramma&#39;s op niveau 1 (H1) koppen zoeken, is het toevoegen van een kop op niveau 1 een eenvoudige manier om ervoor te zorgen dat de pagina correct wordt geïndexeerd.

>[!NOTE]
>
>Het veld _[!UICONTROL Content Heading]_dat boven aan de pagina wordt weergegeven, is een verouderd veld dat inhoud ondersteunt die is gemaakt met eerdere [!DNL Commerce] -releases. Het maakt echter geen deel uit van [!DNL Page Builder] . De [!UICONTROL Content Heading] wordt opgemaakt als een H1-kop op basis van het stijlblad dat aan het huidige thema is gekoppeld. Deze bevindt zich vlak boven het actieve inhoudsgebied dat wordt gedefinieerd door het [!DNL Page Builder] -werkgebied.

Voor de beste controle over het plaatsen en het formaat van rubrieken van alle niveaus, adviseert men dat u het _[!UICONTROL Content Heading]_gebied leeg verlaat, en het [!DNL Page Builder] [ ](heading.md) inhoudstype van de Rubriek gebruikt.

![ Kop van de Inhoud en andere rubrieken ](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Voorvertoning

Wanneer u de sectie _[!UICONTROL Content]_uitbreidt en er bestaande inhoud met [!DNL Page Builder] is gemaakt, wordt een voorvertoning van de inhoud weergegeven zoals deze op een pagina wordt weergegeven. Klik op **[!UICONTROL Edit with Page Builder]**of in het voorvertoningsgebied voor inhoud om de [!DNL Page Builder] -werkruimte te openen, waar u de benodigde updates kunt uitvoeren.

![ de beschrijvingsvoorproef van het Product ](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Voor de product- en categorieformulieren is deze voorbeeldweergave van de inhoud standaard ingeschakeld, maar kan deze worden uitgeschakeld. Als de prestaties te lijden hebben aan het laden van de voorproef, kunt u de voorproef in de [ configuratie van het Beheer van de Inhoud ](../configuration-reference/general/content-management.md#advanced-content-tools) montages onbruikbaar maken.

## Werkgebied

Wanneer u de [!DNL Page Builder] -werkruimte opent vanuit de voorvertoning, is het werkgebied het belangrijkste werkgebied waarin u inhoud kunt maken en opmaken en zelfs snel inhoud kunt bewerken. Het werkgebied is aanvankelijk leeg, zodat u het ontwerpoppervlak hebt waarin u rijen, kolommen en tabbladen vanuit het linkerdeelvenster kunt slepen.

>[!NOTE]
>
>Vanaf de release 2.4.1 is het bewerken van inhoud nu alleen op volledig scherm beschikbaar voor alle gebieden die door [!DNL Page Builder] worden beheerd: CMS-pagina&#39;s, product- en categoriepagina&#39;s, blokken en dynamische blokken. Bij bewerking op volledig scherm krijgt de inhoud de focus en wordt een weergave geboden die beter aansluit bij de gebruikerservaring op de winkel.

![ Stadium met paginacontent ](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Viewports

A _viewport_ is het zichtbare gebied van een Web-pagina die een gebruiker ziet. In de ontwerpmodus Volledig scherm worden de viewportknoppen boven het werkgebied van [!DNL Page Builder] weergegeven om u de inhoud te laten zien zoals de gebruiker die op de site ziet.

![ Viewport knopen ](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] definieert ook onderbrekingspunten voor viewports. Met onderbrekingspunten worden de minimale en maximale breedte gedefinieerd waarbinnen bepaalde stijlen worden toegepast. De viewports van [!DNL Page Builder] verstrekken de volgende inhoudsuitbreekpunten:

- **breekpunt van de Desktop** - `min-width: 1024px`. Dit onderbrekingspunt past stijlen toe die voor viewport breedten worden bepaald die 1024 pixel en breder meten.
- **Mobiele breekpunten** - `max-width: 768px, min-width: 640px`. Deze onderbrekingspunten passen stijlen toe die zijn gedefinieerd voor viewport-breedten tussen 768 pixels en 640 pixels.

[!DNL Page Builder] viewports verstrekt twee eigenschappen: **_inhoudvoorproeven_** en **_breekpuntmontages_**.

### Voorvertoningen van inhoud

Standaard biedt [!DNL Page Builder] twee voorvertoningen van viewport:

- **Desktop** — Toont de inhoudsvoorproef zonder een vooraf bepaalde breedte. Door het bureaublad gedefinieerde stijlen (met een minimale breedte van 1024 pixels voor het onderbrekingspunt) worden nog steeds toegepast op de pagina. Maar de viewport van de Desktop breedte wordt bepaald door montages voor containerinhoudstypes, zoals Rijen. Als u de Desktop-viewport selecteert, ziet u hoe uw inhoud op de winkel is opgemaakt als de paginabreedte van de browser 1024 pixels en breder is.

  ![ viewport voorproef van de Desktop met 1024 pixel minimumbreedte ](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Mobiel** — Toont de inhoudsvoorproef bij een vooraf bepaalde breedte van 768 pixel. In tegenstelling tot de Desktop viewport, toont Mobile viewport uw paginainhoud bij een breedte van 768 pixel, samen met de stijlen die voor de breekpuntbreedten van 768 pixel (maximum) en 640 pixel (minimum) worden bepaald.

  ![ Mobiele viewport voorproef met 768 pixel minimumbreedte ](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Instellingen voor onderbrekingspunten

Met de viewport-knoppen kunt u ook verschillende onderbrekingspuntstijlen toepassen op inhoudstypen op basis van de geselecteerde viewport. Standaard biedt [!DNL Page Builder] onderbrekingspuntinstellingen voor de velden _[!UICONTROL Minimum Height]_Rijen, Kolommen, Tabs, Tabitems, Banners, Sliders en Dia&#39;s. Wanneer u de Mobiele viewport selecteert, dan open de redacteur voor één van die inhoudstypes, kunt u gebiedswaarden ingaan specifiek voor de Mobiele viewport breekpunten. In velden met inhoudstypen die specifieke instellingen voor onderbrekingspunten toestaan, wordt rechts van het veld een pictogram weergegeven, vergelijkbaar met het volgende voorbeeld voor een rij:

![ de indicator van het Pictogram voor breekpunt die ](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"} plaatst

## Deelvenster

Het deelvenster [!DNL Page Builder] bevindt zich links van het werkgebied en bevat inhoudstypen die naar het werkgebied kunnen worden gesleept. Een container die specifiek is voor het inhoudstype wordt dan weergegeven met een gereedschapset met opties. De inhoudstypen worden als volgt geordend in het deelvenster:

### Layout

De sectie _[!UICONTROL Layout]_van het deelvenster [!DNL Page Builder] wordt gebruikt om rijen, kolommen of tabs toe te voegen aan het werkgebied. Wanneer u een inhoudstype van het paneel aan het stadium sleept, verschijnt een container met toolbox van opties die voor het inhoudstype specifiek zijn.

Standaard is het werkgebied van [!DNL Page Builder] leeg. Terwijl u de inhoudstypen van de lay-out van het deelvenster naar het werkgebied sleept, kunt u ze boven, onder of in andere lay-outcontainers op de pagina plaatsen. Rijen kunnen alleen rechtstreeks aan het werkgebied worden toegevoegd.

![[!DNL Page Builder] met inhoudstypen voor de layout en het werkgebied ](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Inhoudstype Layout | Beschrijving |
| ------------------- |------------ |
| [ Rij ](row.md) | U kunt een nieuwe rij alleen slepen vanuit het deelvenster naar het werkgebied en boven of onder een andere rij, tab of kolomgroep plaatsen. Met de optie Dupliceren kunt u ook een kopie van een bestaande rij maken. |
| [ Kolom ](column.md) | U kunt een kolom van het deelvenster naar het werkgebied of naar rijen en tabs slepen. Het maximumaantal kolommen dat kan worden toegevoegd wordt bepaald door het aantal netstreken die in de [ configuratie ](setup.md) worden gespecificeerd. |
| [ Lusjes ](tabs.md) | U kunt één tabblad van het deelvenster naar het werkgebied of naar rijen en kolommen slepen. U kunt extra tabbladen toevoegen vanuit de gereedschapset. |

{style="table-layout:auto"}

### Elementen

Gebruik de _[!UICONTROL Elements]_sectie van het [!DNL Page Builder] paneel om tekst, rubrieken, knopen, verdelers, en code van HTML aan om het even welke lay-outcontainer op het [[!DNL Page Builder]  stadium ](workspace.md#stage) toe te voegen. Wanneer u een inhoudstype van het paneel aan of een rij of een kolom, of aan een lusjereeks op het stadium sleept, verschijnt een container. Gebruik de gereedschapset voor inhoudstypen voor toegang tot de instellingen die specifiek zijn voor de tekst.

![[!DNL Page Builder] met inhoudstypen voor Element ](./assets/pb-elements.png){width="600" zoomable="yes"}

| Type inhoud element | Beschrijving |
| -------------------- | ----------- |
| [ Tekst ](text.md) | Hiermee voegt u een tekstcontainer en -editor toe aan het werkgebied. |
| [ Kop ](heading.md) | Voegt een kopcontainer toe aan het werkgebied. |
| [ Knopen ](buttons.md) | Hiermee voegt u een container voor een afzonderlijke knop of een set knoppen toe aan het werkgebied. |
| [ Scheidingsreiziger ](divider.md) | Voegt een container voor een scheidingslijn toe aan het werkgebied. |
| [ de Code van HTML ](html-code.md) | Voegt een container voor HTML-code toe aan het werkgebied. |

{style="table-layout:auto"}

### Media

Gebruik de _[!UICONTROL Media]_sectie van het [!DNL Page Builder] paneel om beelden, video, banners, schuiven, en [!DNL Google Maps] aan om het even welke lay-outcontainer op het [[!DNL Page Builder]  stadium ](workspace.md#stage) toe te voegen. Wanneer een type media-inhoud van het deelvenster naar het werkgebied wordt gesleept, wordt een container weergegeven met een gereedschapset met opties die specifiek zijn voor het inhoudstype.

![[!DNL Page Builder] met media-inhoudstypen ](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Het inhoudstype Media | Beschrijving |
| ------------------- | ------------------------------------------ |
| [ Beeld ](image.md) | Voegt een afbeeldingscontainer toe aan het werkgebied. |
| [ Video ](video.md) | Voegt een videopcontainer toe aan het werkgebied. |
| [ Banner ](banner.md) | Voegt een bannercontainer toe aan het werkgebied. |
| [ Schuifregelaar ](slider.md) | Voegt een schuifregelaarcontainer toe aan het werkgebied. |
| [ Kaart ](map.md) | Voegt een [!DNL Google Maps] -container toe aan het werkgebied. |

{style="table-layout:auto"}

### Inhoud toevoegen

Gebruik de _[!UICONTROL Add Content]_sectie van het [!DNL Page Builder] paneel om bestaande inhoud aan het [[!DNL Page Builder]  stadium ](workspace.md#stage) toe te voegen. Wanneer u een inhoudstype voor media van het deelvenster naar het werkgebied sleept, wordt een container weergegeven. Gebruik inhoudstype toolbox om tot de_ Montages _toegang te hebben die voor het type specifiek zijn.

![[!DNL Page Builder] met Typen inhoud toevoegen ](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Inhoudstype | Beschrijving |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [ Blok ](block.md) | Voegt een bestaand blok aan het stadium toe. |
| [ Dynamisch Blok ](dynamic-block.md) | Voegt een bestaand dynamisch blok toe aan het werkgebied. |
| [ Producten ](products.md) | Hiermee voegt u een lijst met producten toe aan het werkgebied. |
| ![ Adobe Commerce slechts ](../assets/adobe-logo.svg) [ Aanbevelingen van het Product ](recommendations.md) | Voegt een aanbevolen eenheid aan het stadium toe. |

{style="table-layout:auto"}

## Gereedschapset

Elke inhoudscontainer in het werkgebied heeft een gereedschapset met opties. De opties variëren per inhoudstype, maar omvatten typisch Beweging, Montages, Verbergen/tonen, Dupliceren, en Verwijderen.

### De gereedschapset weergeven

Houd de muisaanwijzer boven de container om de gereedschapset weer te geven en kies een optie.

![ de toolbox van de Rij opties ](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Opties voor gereedschapsset

| Optie | Pictogram | Beschrijving |
| --------- | ---------------------------------------- | ------------ |
| Verplaatsen | ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="25"} | Verplaatst de huidige inhoudscontainer naar een andere positie in het werkgebied. |
| Toevoegen | ![ voeg pictogram ](./assets/pb-icon-add.png){width="25"} toe | Hiermee voegt u onderliggende elementen toe, zoals een knop, dia of tab. |
| (label) |           | Identificeert het containerinhoudstype. |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de eigenschappen van de inhoudscontainer in de bewerkingsmodus. |
| Verbergen | ![ het pictogram van de Huid ](./assets/pb-icon-hide.png){width="25"} | Verbergt de huidige inhoudscontainer. |
| Tonen | ![ toon pictogram ](./assets/pb-icon-show.png){width="25"} | Hiermee wordt de huidige inhoudscontainer weergegeven. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Maakt een kopie van de huidige inhoudscontainer. |
| Verwijderen | ![ verwijder ](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de huidige inhoudscontainer uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
