---
title: Elements - Knoppen
description: Leer over het inhoudstype van Knopen, dat wordt gebruikt om een individuele knoop of een reeks knopen in het  [!DNL Page Builder]  stadium toe te voegen.
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 0%

---

# Elements - Knoppen

Gebruik het _inhoudstype van Knopen_ om of een individuele knoop of een reeks knopen in het [[!DNL Page Builder]  stadium ](workspace.md#stage) toe te voegen. U kunt knoppen horizontaal of verticaal rangschikken en rechtstreeks toevoegen aan rijen, kolommen, tabbladen en banners in het werkgebied.

![ Banner met een knoop op de storefront ](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Werkbalken

Wanneer u met het inhoudstype Knoppen werkt, voegt u afzonderlijke knoppen en de knoppencontainer die een of meer knoppen bevat toe en bewerkt u deze. Elk gereedschap heeft een eigen gereedschapset die u kunt gebruiken om knoppen te ontwerpen in het [!DNL Page Builder] -werkgebied.

### Afzonderlijke knopgereedschapset

![ toolbox van de Knoop ](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| Gereedschap | Pictogram | Beschrijving |
| --------- | -------- | -------------- |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de pagina Knop Bewerken, waar u de eigenschappen van de knop kunt wijzigen. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Hiermee maakt u een kopie van de knop. |
| Verwijderen | ![ verwijder pictogram ](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de knop uit het werkgebied. |

{style="table-layout:auto"}

### Knoppencontainer, gereedschapset

![ de containertoolbox van Knopen ](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| Gereedschap | Pictogram | Beschrijving |
| --------- | ----------------- | ----------- |
| Verplaatsen | ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="25"} | Verplaatst de knopcontainer naar een andere geldige plaats op de pagina. |
| Toevoegen | ![ voeg pictogram ](./assets/pb-icon-add-button.png){width="25"} toe | Hiermee voegt u een knop aan de container toe. |
| (label) | Knop | Identificeert de huidige container als een knopelement. |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de pagina Knoppen bewerken, waarin u de eigenschappen van de container kunt wijzigen. |
| Verbergen | ![ het pictogram van de Huid ](./assets/pb-icon-hide.png){width="25"} | Verbergt de knopcontainer. |
| Tonen | ![ toon pictogram ](./assets/pb-icon-show.png){width="25"} | Hiermee wordt de verborgen knopcontainer weergegeven. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Maakt een kopie van de knopcontainer. |
| Verwijderen | ![ verwijder pictogram ](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de knopcontainer en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een afzonderlijke knop toevoegen

1. Vouw in het deelvenster [!DNL Page Builder] **[!UICONTROL Elements]** uit en sleep een tijdelijke aanduiding **[!UICONTROL Buttons]** naar een rij, kolom of tabset in het werkgebied.

   ![ slepend een knoop aan het stadium ](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. Beweeg over de knoop om toolbox te tonen en het _pictogram van Montages_ te kiezen (![ pictogram van Montages ](./assets/pb-icon-settings.png)).

1. Voer de **[!UICONTROL Button Text]** in die op de knop moet worden weergegeven.

   ![ Basisknoopmontages ](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Button Type]** in op een van de volgende opties:

   | Type | Beschrijving |
   | ------ | ----------- |
   | `Primary` | Past de primaire knoopstijl van het huidige stijlblad toe. |
   | `Secondary` | Past de secundaire knoopstijl van het huidige stijlblad toe als toepasselijk. |
   | `Link` | Maakt een hyperlink in plaats van een knop. |

   {style="table-layout:auto"}

   ![ Primair en secundair knoopvoorbeeld ](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. Stel de **[!UICONTROL Button Link]** in met een van de volgende typen:

   - **[!UICONTROL URL]** - Voer de doel-URL voor de koppeling in.

     De URL kan een relatieve koppeling zijn naar een product of pagina in uw winkel of een volledig gekwalificeerde URL.

     Relatief URL-voorbeeld - `../luma-analog-watch.html`

     Volledig gekwalificeerd URL-voorbeeld - `http://mystore.com/luma-analog-watch.html`

     Als de koppeling naar een andere website gaat, kunt u de huidige pagina open houden voor uw winkel door de koppeling op een nieuw browsertabblad te openen.

     Schakel het selectievakje **[!UICONTROL Open in new tab]** in om te voorkomen dat de bezoeker uit uw winkel navigeert.

   - **[!UICONTROL Product]** - Voer een productnaam (gedeeltelijk of volledig) of SKU in en kies vervolgens de productnaam in de lijst.

     >[!NOTE]
     >
     >De producten worden getoond in de lijst volgens _toon uit voorraadproducten_ montages. Voor de Multicamakers van Source die [ Inventory management ](../inventory-management/introduction.md) gebruiken, wordt de productlijst beperkt door de bron die aan de standaardwebsite slechts wordt toegewezen.

     ![ Kiekend een product voor de knoopverbinding ](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Voer een categorienaam in (gedeeltelijk of volledig) of klik in het lege veld om de categoriestructuur weer te geven. Kies vervolgens de categorienaam in de structuur.

     ![ Kiekend een categorie voor de knoopverbinding ](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Voer de naam van een CMS-pagina in (gedeeltelijk of volledig) of klik in het lege veld om de volledige lijst weer te geven. Kies vervolgens de naam van de pagina in de lijst met zoekresultaten.

     ![ kies CMS pagina voor knoopverbinding ](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. Voltooi de [ geavanceerde montages ][advanced-settings] zoals nodig.

1. Klik na afloop op **[!UICONTROL Save]** in de rechterbovenhoek om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

## Een set knoppen toevoegen

In de volgende secties wordt een reeks stappen beschreven die met een afzonderlijke knop moeten beginnen en wordt een set van drie knoppen in een knopcontainer gemaakt. Als u nog geen afzonderlijke knop hebt, volgt u de vorige instructies om een afzonderlijke knop aan het werkgebied toe te voegen.

### Stap 1: De tweede knop maken

1. Beweeg over de knoopcontainer om toolbox te tonen en _te kiezen voeg_ toe ( ![ voeg pictogram ](./assets/pb-icon-add-button.png){width="20"} toe) pictogram.

   ![ Toevoegend een andere knoop ](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. Voer de tekst in die u op de tweede knop wilt weergeven.

1. Klik de nieuwe knoop om zijn toolbox te tonen en het _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

   ![ Uitgevend de knoop ](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. Stel **[!UICONTROL Button Type]** in op `Secondary` .

1. Stel de **[!UICONTROL Button Link]** naar wens in.

   In het volgende voorbeeld, is de verbinding een relatieve URL die naar de [ pagina van het Contact van ons ](../getting-started/store-details.md#contact-us-form) gaat.

   ![ de knoopmontages van het Contact van ons ](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. Voltooi de [ geavanceerde montages ][advanced-settings] zoals nodig.

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

### Stap 2: De derde knop maken

1. Klik opnieuw de tweede knoop op het stadium en kies _Dupliceer_ ( ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="20"}) pictogram.

   ![ Duplicerend een knoop ](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. Voer de tekst in die u op de derde knop wilt weergeven.

1. Klik de derde knoop om toolbox te tonen en het _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

   ![ Toolbox voor de derde knoop ](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. Werk de **[!UICONTROL Button Link]** zo nodig bij.

1. Klik in de rechterbovenhoek op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

### Stap 3: De knopcontainer bijwerken

1. Beweeg over de knoopcontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

   ![ de containertoolbox van Knopen ](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. Kies onder _[!UICONTROL Appearance]_&#x200B;de optie **[!UICONTROL Stacked]**.

1. Stel **[!UICONTROL All Buttons are same size]** in op `Yes` .

   ![ Gestapelde knopen van de zelfde grootte ](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. Werk de resterende montages zoals nodig bij, gebruikend de beschrijvingen van [ montages van de Verandering voor een knoopcontainer ][button-container].

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

   De volledige gestapelde knopset wordt in het werkgebied weergegeven met één primaire knop en twee secundaire knoppen.

   ![ Gestapelde knopen op het stadium ](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## Een knop verplaatsen

1. Klik op de knop die u wilt verplaatsen.

1. Selecteer en sleep het pictogram van de Beweging ( ![ het pictogram van de Beweging ](./assets/pb-icon-move.png){width="20"}), dat net vóór de knooptekst verschijnt, aan een nieuwe positie voor de knoop binnen de knoopcontainer.

   ![ Bewegend een knoop ](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## Instellingen voor een knop wijzigen

1. Klik de knoop op het stadium om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

   ![ toolboxes van de Knoop ](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. Werk de standaardinstellingen naar wens bij.

   - **[!UICONTROL Button Text]** - Voer de tekst in die op de knop moet worden weergegeven (kan ook rechtstreeks vanuit het werkgebied worden bijgewerkt).

   - **[!UICONTROL Button Type]** - Hiermee bepaalt u de knopindeling.

     | Type | Beschrijving |
     | ------ | ----------- |
     | `Primary` | Past de primaire knoopstijl van het huidige stijlblad toe. |
     | `Secondary` | Past de secundaire knoopstijl van het huidige stijlblad toe, indien van toepassing. |
     | `Link` | Maakt een hyperlink in plaats van een knop. |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]** - Bepaalt de bestemmingspagina die wordt gediend wanneer de knoop wordt geklikt.

     | Optie | Beschrijving |
     | ------ | ----------- |
     | `URL` | Gebruikt of een relatieve of volledig - gekwalificeerde URL om de bestemmingspagina te identificeren. |
     | `Product` | Identificeert de bestemmingspagina die op de productnaam of SKU wordt gebaseerd. U kunt zoeken naar de productnaam op basis van een gedeeltelijke of volledige naam. Het product wordt vervolgens gekozen uit de lijst met zoekresultaten. |
     | `Category` | Hiermee wordt de doelpagina geïdentificeerd als een specifieke categorie of subcategorie in de categoriestructuur. |
     | `Page` | Hiermee wordt de doelpagina geïdentificeerd als een specifieke CMS-pagina. |

     {style="table-layout:auto"}

1. Voltooi de [ geavanceerde montages ][advanced-settings] zoals nodig.

1. Als u de instellingen wilt opslaan en wilt terugkeren naar de werkruimte van [!DNL Page Builder] , klikt u op **[!UICONTROL Save]** in de rechterbovenhoek.

## Instellingen wijzigen voor een knopcontainer

1. Beweeg over de knoopcontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

1. Werk de instellingen van **[!UICONTROL Appearance]** naar wens bij.

   - Gebruik de opties voor rangschikking om de knoppen horizontaal of verticaal in de container weer te geven:

     | Optie | Beschrijving |
     | ------ | ----------- |
     | `Inline` | Hiermee rangschikt u de knoppen horizontaal. |
     | `Stacked` | Hiermee rangschikt u de knoppen verticaal. |

     {style="table-layout:auto"}

   - Stel de optie **[!UICONTROL All buttons are same size]** in op basis van uw voorkeur.

     Wanneer ingesteld op `Yes` , hebben alle knoppen in de container een consistente grootte, gebaseerd op de lengte van de langste knoptekst.

1. Voltooi de [ Geavanceerde montages ][advanced-settings] zoals nodig.

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

## Geavanceerde instellingen wijzigen

U kunt de _[!UICONTROL Advanced]_-instellingen voor afzonderlijke knoppen en voor de knopcontainer wijzigen.

1. Kies de optie **[!UICONTROL Alignment]** als u de positionering in de bovenliggende container wilt bepalen:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
   | `Left` | Hiermee lijnt u de inhoud uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Center` | Hiermee lijnt u de inhoud uit in het midden van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Right` | Hiermee lijnt u de inhoud uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

   {style="table-layout:auto"}

1. Stel de stijl **[!UICONTROL Border]** in die op alle vier zijden van de knop of knoppencontainer wordt toegepast:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Past de standaardrandstijl toe die door het bijbehorende stijlblad wordt gespecificeerd. |
   | `None` | Geeft geen zichtbare indicatie van de containerranden. |
   | `Dotted` | De containerrand wordt weergegeven als een stippellijn. |
   | `Dashed` | De containerrand wordt weergegeven als een onderbroken lijn. |
   | `Solid` | De containerrand wordt weergegeven als een effen lijn. |
   | `Double` | De containerrand wordt weergegeven als een dubbele lijn. |
   | `Groove` | De containerrand wordt weergegeven als een gegroefde lijn. |
   | `Ridge` | De containerrand wordt weergegeven als een afgeronde lijn. |
   | `Inset` | De containerrand wordt weergegeven als een inzetlijn. |
   | `Outset` | De containerrand wordt weergegeven als een omtreklijn. |

   {style="table-layout:auto"}

1. Als u een andere randstijl dan `None` instelt, voert u de weergaveopties voor de rand in:

   | Optie | Beschrijving |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
   | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
   | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

   {style="table-layout:auto"}

1. (Optioneel) Geef de namen van **[!UICONTROL CSS classes]** op uit het huidige stijlblad die u wilt toepassen op de knop of knoppencontainer.

   Scheid meerdere klassennamen met een spatie.

1. Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de knop of knoppencontainer te bepalen.

   Voer de overeenkomende waarden in het diagram in.

   | Containergebied | Beschrijving |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

[advanced-settings]: #change-advanced-settings
[button-container]: #change-settings-for-a-button-container

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
