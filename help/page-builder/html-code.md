---
title: Elements - HTML-code
description: Leer over het inhoudstype van de Code van de HTML, dat wordt gebruikt om fragmenten van HTML, CSS, en code van JavaScript in het  [!DNL Page Builder]  stadium toe te voegen.
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 556394327a6eff9282acb09bdd16777dd3fee360
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Elements - HTML-code

Gebruik het _inhoudstype van de Code 0} HTML {om fragmenten van HTML, CSS, en code van JavaScript in het [[!DNL Page Builder]  stadium ](workspace.md#stage) toe te voegen._ U kunt bijvoorbeeld aangepaste HTML toevoegen, een CSS-klasse declareren die op een element op de pagina kan worden toegepast. Of u wilt een codefragment toevoegen voor een logo, knop of banner die u van een externe provider hebt ontvangen.

## Gereedschap HTML-code

![ toolbox van de Code van HTML ](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| Gereedschap | Pictogram | Beschrijving |
| --------- | ---------- | ----------------- |
| Verplaatsen | ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="25"} | Verplaatst de container van de Code van de HTML naar een andere geldige plaats op de pagina. |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de pagina HTML-code bewerken, waarin u de eigenschappen van de container kunt wijzigen. |
| Verbergen | ![ het pictogram van de Huid ](./assets/pb-icon-hide.png){width="25"} | Verbergt de container van de Code van de HTML. |
| Tonen | ![ toon pictogram ](./assets/pb-icon-show.png){width="25"} | Toont de verborgen container van de Code van HTML. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Hiermee maakt u een kopie van de container HTML Code. |
| Verwijderen | ![ verwijder pictogram ](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de container HTML Code en de inhoud ervan uit het werkgebied. |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## HTML-code toevoegen

Het volgende voorbeeld toont aan hoe te om ][1] code in te bedden van de Doopvont van Google [ en de klassen van de douanerubriek te verklaren die de huidige stylesheet met voeten treden.

### Stap 1: Kies een Google-lettertype

1. Bezoek de [ plaats van de Doopvonten van Google ][1] en kies de doopvontfamilie die u wilt gebruiken.

1. Kopieer de gegenereerde code die moet worden ingesloten in de sectie `<head>` van de pagina en plak deze tijdelijk in een teksteditor.

   - Fontcode insluiten
   - CSS-regel

1. Voeg de regel font-family toe aan elke kopklasse en sluit de kopklassen in een `<style>` -tag in.

   Deze code wordt geplakt in [!DNL Page Builder] .

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### Stap 2: Voeg de code toe aan de pagina

1. In _Admin_ sidebar van uw opslag, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Zoek de pagina waar het lettertype beschikbaar moet zijn en open het in de bewerkingsmodus.

1. Schuif omlaag en vouw de sectie **[!UICONTROL Content]** uit.

1. Vouw in het deelvenster [!DNL Page Builder] **[!UICONTROL Elements]** uit en sleep een tijdelijke aanduiding **[!UICONTROL HTML Code]** naar een rij, kolom of tabset in het werkgebied.

   Gebruik de rode hulplijn om de scheidingslijn voor of na een andere inhoudscontainer in de rij, kolom of tabset te plaatsen.

   ![ slepend een placeholder van de Code van de HTML aan het stadium ](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. Beweeg over de container van de HTML om toolbox te tonen en de _Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}), pictogram.

1. Plak in het tekstvak de code en stijldeclaraties voor Google-fonts insluiten die u hebt voorbereid.

   U kunt een paar spaties invoeren om de code te laten inspringen, zodat u deze eenvoudiger kunt lezen.

   ![ HTML code en stijlen ](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. Werk de resterende montages zoals nodig bij (zie {de codecontages van de HTML van 0} Verandering ](#html-settings) voor details).[

1. Klik in de rechterbovenhoek op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

   Het nieuwe lettertype wordt weergegeven wanneer de pagina via een browser wordt weergegeven.

### Stap 3: Voorvertoning van de pagina weergeven

1. Stel **[!UICONTROL Enable Page]** in op `Yes` in de sectie _[!UICONTROL Currently Active]_.

   ![ toelatend de pagina ](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op de pijl **[!UICONTROL Save]** en kies **[!UICONTROL Save & Close]** .

1. Zoek de pagina in het raster en selecteer **[!UICONTROL View]** in de kolom _[!UICONTROL Actions]_.

   ![ Voorproef de paginakoppen met de nieuwe doopvontfamilie ](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## Instellingen voor HTML-code wijzigen {#html-settings}

1. Beweeg over de container van de HTML om toolbox te tonen en de _Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

1. Bewerk in het tekstvak de code naar wens.

   HTML-, CSS- en JavaScript-code worden ondersteund. Codefragmenten die in de sectie `<head>` van de pagina horen, kunnen hier worden ingevoerd.

   De redacteur verstrekt ook knopen om speciale elementen in de code op te nemen:

   | Knop | Beschrijving |
   | ------ | ----------- |
   | Widget invoegen... | Klik om een widget in te voegen op de positie van de cursor in het tekstvak HTML. |
   | Afbeelding invoegen... | Klik om een geüploade afbeelding of een afbeelding uit de galerie in te voegen op de positie van de cursor in het tekstvak HTML. |
   | Variabele invoegen... | Klik om een variabele op de positie van de cursor in het tekstvak HTML in te voegen. |

1. Werk de instellingen van _[!UICONTROL Advanced]_naar wens bij.

   - Kies een **[!UICONTROL Alignment]** als u de positie van de code binnen de bovenliggende container wilt bepalen:

     | Optie | Beschrijving |
     | ------ | ----------- |
     | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
     | `Left` | Hiermee lijnt u de lijst uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
     | `Center` | Hiermee lijnt u de lijst in het midden van de bovenliggende container uit, rekening houdend met de opgegeven opvulling. |
     | `Right` | Hiermee lijnt u het blok uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

     In het volgende voorbeeld worden de opties zo ingesteld dat ze een uitlijning in het midden gebruiken voor het gerenderde codeblok.

     ![ Scheidingsverdeler met een centrumgroepering ](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Stel de **[!UICONTROL Border]** -stijl in die op alle vier zijden van de codecontainer wordt toegepast:

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

   - Als u een andere randstijl dan `None` instelt, voert u de weergaveopties voor de rand in:

     | Optie | Beschrijving |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
     | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
     | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

     {style="table-layout:auto"}

   - (Optioneel) Geef de namen van **[!UICONTROL CSS classes]** op uit de huidige stijlpagina die u op de container wilt toepassen.

     Scheid meerdere klassennamen met een spatie.

   - Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en binnenopvulling van de codecontainer te bepalen.

     Voer de overeenkomende waarden in het diagram in.

     | Containergebied | Beschrijving |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

[1]: https://fonts.google.com/
