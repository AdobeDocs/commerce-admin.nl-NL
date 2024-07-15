---
title: Media - Video
description: Leer over het Video inhoudstype, dat wordt gebruikt om een video toe te voegen die op YouTube of Vimeo aan het  [!DNL Page Builder]  stadium wordt ontvangen.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 0%

---

# Media - Video

Gebruik het _Video_ inhoudstype om een video toe te voegen die op [ YouTube ][1] of [ Vimeo ][2] aan het [[!DNL Page Builder]  stadium ](workspace.md#stage) wordt ontvangen. U kunt video eenvoudig insluiten in een pagina of blok of in product- en categorieredetecties.

![ Video op de storefront homepage ](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Video, werkset

![ Video toolbox ](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Gereedschap | Pictogram | Beschrijving |
|--- |--- |--- |
| Verplaatsen | ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="25"} | Hiermee verplaatst u de video naar een andere positie in het werkgebied. |
| (label) | [!UICONTROL Video] | Identificeert de huidige inhoudscontainer als video. Houd de muisaanwijzer boven de container van de afbeelding om de gereedschapset weer te geven. |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de pagina _[!UICONTROL Edit Video]_, waar u de eigenschappen van de video en de container kunt wijzigen. |
| Verbergen | ![ het pictogram van de Huid ](./assets/pb-icon-hide.png){width="25"} | Hiermee verbergt u de huidige video. |
| Tonen | ![ toon pictogram ](./assets/pb-icon-show.png){width="25"} | De verborgen video wordt weergegeven. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Maakt een kopie van de video. |
| Verwijderen | ![ verwijder pictogram ](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de video uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een video toevoegen

1. Alvorens u begint, navigeer aan [ YouTube ][1] of [ video van de Vimeo ][2] die u, de verbinding wilt inbedden en kopiëren.

   U kunt ook een directe koppeling naar een geldig videobestand kopiëren. Zie [ Basis videomontages ](#basic-video-settings) voor geldige verbindingen.

1. Ga in [!DNL Commerce] Beheer terug naar de werkruimte van [!DNL Page Builder] waar u de video wilt toevoegen.

1. Vouw **[!UICONTROL Media]** uit in het deelvenster [!DNL Page Builder] en sleep een tijdelijke aanduiding **[!UICONTROL Video]** naar het werkgebied.

   ![ slepend een videoplaceholder aan het stadium ](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Beweeg over de videocontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

1. Plak bij **[!UICONTROL Video URL]** de URL van de video die u hebt gekopieerd.

   De URL van de video [!DNL Page Builder] die in dit voorbeeld wordt gebruikt, is: `https://www.youtube.com/watch?v=Y0KNS7C5dZA` .

1. Als u de **[!UICONTROL Maximum Width]** van de video wilt beperken, voert u de maximale breedte in pixels in.

   Als de video leeg is, is deze zo breed als is toegestaan door de container, wat marges en opvulling toestaat.

1. Klik in de rechterbovenhoek op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

## Video-instellingen wijzigen

1. Beweeg over de videocontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

1. Wijzig de instellingen volgens de volgende secties:

   - [Basis](#basic-video-settings)
   - [Geavanceerd](#advanced)

1. Klik in de rechterbovenhoek op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

### Standaardvideo-instellingen

1. Werk de **[!UICONTROL Video URL]** bij om de huidige video te wijzigen.

   Voer een geldige video-URL in. Geldige video-URL&#39;s kunnen koppelingen zijn naar:

   - YouTube-video&#39;s: `https://youtu.be/CoDhMRUUjeI`
   - Vimeo-video&#39;s: `https://vimeo.com/190156113`
   - Geldige videobestanden (`.mp4` wordt aanbevolen): `https://myvideos.com/spiral.mp4`

1. Als u de toegestane breedte voor de video in de winkelvoorgrond wilt wijzigen, voert u de nieuwe **[!UICONTROL Maximum Width]** in pixels in.

   Als de video leeg is, wordt de volledige breedte van de container uitgebreid, minus marges en opvulling.

1. Stel **[!UICONTROL Autoplay]** in op `Yes` als u de video automatisch wilt starten nadat de pagina is geladen.

   Als Automatisch afspelen is ingesteld op `Yes` , wordt de video gedempt bij het afspelen volgens het beleid. Zelfs met deze instelling kunnen mobiele apparaten uw video&#39;s echter niet automatisch afspelen. Raadpleeg de volgende bronnen voor ontwikkelaars voor meer informatie over dit beleid:

   - [ Autoplay beleid van Vimeo ](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [ Autoplay beleid van Google (Chrome/YouTube) ](https://developer.chrome.com/blog/autoplay/)
   - [ beleid Autoplay voor lokale video&#39;s ](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Als Automatisch afspelen is ingesteld op `No` , wordt de video alleen op verzoek van de gebruiker afgespeeld.

### [!UICONTROL Advanced]

1. Kies een **[!UICONTROL Alignment]** als u de horizontale plaatsing van de video binnen de container wilt bepalen:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
   | `Left` | Hiermee lijnt u de inhoud uit langs de linkerrand van de videocontainer, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Center` | Hiermee lijnt u de inhoud uit in het midden van de videopcontainer, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Right` | Hiermee lijnt u de inhoud uit langs de rechterrand van de videocontainer, waarbij rekening wordt gehouden met de opgegeven opvulling. |

   {style="table-layout:auto"}

- Stel de stijl **[!UICONTROL Border]** in die wordt toegepast op alle vier zijden van de videopcontainer:

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

- Als u een andere randstijl dan `None` instelt, voert u de weergaveopties voor de rand in:

  ![ Grenskleur ](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Optie | Beschrijving |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
  | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
  | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

  {style="table-layout:auto"}

- (Optioneel) Geef de namen van **[!UICONTROL CSS classes]** op uit het huidige stijlblad die u wilt toepassen op de videopcontainer.

  Scheid meerdere klassennamen met een spatie.

- Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de videopcontainer op te geven.

  Voer elke corresponderende waarde in het diagram van de videopcontainer in.

  | Containergebied | Beschrijving |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. |
  | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. |

  {style="table-layout:auto"}

## Een video verplaatsen

1. Beweeg over de videocontainer om toolbox te tonen en de _Beweging_ te kiezen ( ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="20"}) pictogram.

   ![ Bewegend een video ](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Selecteer en sleep de video naar de nieuwe positie, net onder de rode hulplijn.

   ![ Gebruikend de rode richtlijn om de video ](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"} te plaatsen

## Een video uit het werkgebied verwijderen

1. Beweeg over de videocontainer om toolbox te tonen en _te kiezen verwijder_ (![ verwijder pictogram ](./assets/pb-icon-remove.png)).

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
