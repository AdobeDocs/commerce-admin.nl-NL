---
title: Breadcrumb, sporen
description: Leer meer over de verschillende trailpatronen van de broodkruimelspoor en hoe te om hen te vormen om op inhoud en cataloguspagina's te verschijnen.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Breadcrumb, sporen

A _broodkruimelspoor_ is een reeks verbindingen die de klant toont waar zij met betrekking tot andere pagina&#39;s in de opslag zijn. Ze kunnen op een willekeurige koppeling in het broodkruimelspoor klikken om terug te keren naar de vorige pagina.

Het pad van de broodkruimel kan zo worden geconfigureerd dat het wordt weergegeven op inhoudspagina&#39;s en op cataloguspagina&#39;s. Het formaat en de positie van het broodkruimelspoor variëren door thema, maar het wordt typisch gevestigd enkel onder de kopbal. Standaard wordt het broodkruimelspoor weergegeven op CMS-pagina&#39;s.

![ Breadcrumb spoor dat in storefront ](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"} wordt getoond

## Algemene soorten broodkruimels

Broodkruimels kunnen in drie hoofdtypen worden verdeeld, die qua doel verschillen. De essentie en de belangrijkste beginselen van de uitvoering van elk type kruimel van brood worden hieronder beschreven.

### Hiërarchiegebaseerde broodkruimels

Dit type breadcrumb is gebaseerd op de categoriehiërarchie die op de site is ingesteld. De aangeboden ketens vertellen de gebruiker waar in de structuur ze zich bevinden. In dit geval is elke tekstkoppeling bedoeld voor een pagina die één niveau hoger is dan de vorige.

Voorbeeld: `Men > Tops > Hoodies & Sweatshirts`

Het voordeel van dit type is dat gebruikers gemakkelijk kunnen zien in welk categorieniveau ze zich bevinden en gemakkelijk toegang hebben tot navigatie tussen cataloguspagina&#39;s.

### Op geschiedenis gebaseerde broodkruimels

De op geschiedenis (of weg-gebaseerde navigatie is gelijkaardig aan de achterknoop in browser. Met dit type navigatie kunnen gebruikers snel terugkeren naar de vorige pagina&#39;s die ze hebben bezocht.

Het voordeel van dit type is dat het vooral handig is als klanten naar een vorige pagina willen terugkeren nadat ze meerdere filters op een categoriepagina hebben geselecteerd.

Voorbeeld: `Home > What's New > Gear > Bags`

### Breedkruimels op basis van kenmerken

Bij dit type broodkruimel worden de kenmerken weergegeven die op de categoriepagina zijn geselecteerd. Het belangrijkste verschil met de andere typen is dat de op kenmerken gebaseerde breadcrumbs de filters en opties vertegenwoordigen die de klant in de navigatielaag heeft geselecteerd voor bepaalde producten (zoals prijs, kwaliteit en kleur).

Voorbeeld: `Home > Suits > All Suits > Refined by > Slim Fit`

## Breedkruimels toevoegen/verwijderen uit CMS-pagina&#39;s

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_de optie **[!UICONTROL Web]**.

   ![ toon Broodkruimels voor Pagina&#39;s CMS ](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Vouw de sectie _[!UICONTROL Default Pages]_uit.

1. Schakel het selectievakje **[!UICONTROL Use system value]** uit.

1. Stel **[!UICONTROL Show Breadcrumbs for CMS Pages]** in op `No` of `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

>[!NOTE]
>
>De oudercategorie wordt niet getoond op het Trail van de Breadcrumb, op de pagina van de kindcategorie, wanneer het `Browsing Category`= `Deny` [ categorietoestemming ](category-permissions.md) montages heeft.
