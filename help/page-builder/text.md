---
title: Elementen - tekst
description: Leer over het inhoudstype van de Tekst, dat wordt gebruikt om een tekstcontainer in het  [!DNL Page Builder]  stadium toe te voegen.
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Elementen - tekst

Gebruik het _inhoudstype van de Tekst_ om een tekstcontainer met een WYSIWYG (&quot;wat u ziet is wat u&quot;krijgt) redacteur in het [[!DNL Page Builder]  stadium ](workspace.md#stage) toe te voegen. Bovendien kunt u verbindingen, beelden, [ variabelen ](../systems/variables-predefined.md), en widgets aan de tekst van de redacteurstoolbar toevoegen.

![ Opgemaakte tekst op een banner ](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Gereedschappen voor teksteditor

U kunt de teksteditor rechtstreeks vanuit het werkgebied of vanaf een instellingspagina openen. Wijzigingen die rechtstreeks in het werkgebied worden aangebracht, worden automatisch opgeslagen. Voor meer informatie, zie [ Gebruikend de Redacteur ](../content-design/editor.md).

![ het redacteurshulpmiddel van de Tekst - TinyMCE ](./assets/pb-elements-text-editor-tools.png){width="600"}

## Gereedschap Tekstcontainer

![ de containertoolbox van de Tekst ](./assets/pb-elements-text-toolbox.png){width="600"}

| Gereedschap | Pictogram | Beschrijving |
| --------- | --------------------- | -------------- |
| Verplaatsen | ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="25"} | Verplaatst de tekstcontainer naar een andere geldige plaats op de pagina. |
| (label) | TEXT | Identificeert de huidige container als een tekstelement. |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de eigenschappen van de tekstcontainer in de bewerkingsmodus. |
| Verbergen | ![ het pictogram van de Huid ](./assets/pb-icon-hide.png){width="25"} | Verbergt de tekstcontainer. |
| Tonen | ![ toon pictogram ](./assets/pb-icon-show.png){width="25"} | Hiermee wordt de verborgen tekstcontainer weergegeven. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Maakt een kopie van de tekstcontainer. |
| Verwijderen | ![ verwijder pictogram ](./assets/pb-icon-remove.png){width="25"} | Verwijdert de tekstcontainer en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Tekst toevoegen

1. Vouw in het deelvenster [!DNL Page Builder] **[!UICONTROL Elements]** uit en sleep een tijdelijke aanduiding **[!UICONTROL Text]** naar een rij, kolom of tabset in het werkgebied.

   ![ slepend een tekstplaceholder aan het stadium ](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. Gebruik de editor om zo nodig tekst in te voeren en op te maken.

   Voor meer informatie, zie [ Gebruikend de Redacteur ](../content-design/editor.md).

   ![ redacteur van de Tekst met inhoud ](./assets/pb-elements-text-editor.png){width="600"}

## Een koppeling maken

Met de knop Koppeling invoegen in de editor kunt u gemakkelijk een hyperlink naar een afbeelding in de galerie toevoegen. Het kan echter ook worden gebruikt om een inline-koppeling in tekst te maken, als u de URL vooraf hebt. In tegenstelling tot de knop Widget is de knop Koppeling invoegen/bewerken niet geïntegreerd met pagina&#39;s, producten of categorieën in de winkel.

Om een verbinding voor een telefoonnummer of e-mail tot stand te brengen, zie [ Toevoegend de Variabelen van de Douane ](../systems/variables-custom.md).

1. Navigeer in de storefront naar de pagina die de doelbestemming voor de koppeling moet zijn en kopieer de koppelingsinformatie.

   U kunt volledig - gekwalificeerde URL of een relatieve URL gebruiken die de verwijzing naar uw archiefdomein weglaat.

   Volledige URL - `https://mystore.com/women/tops-women/tees-women.html`

   Relatieve URL - `../women/tops-women/tees-women.html`

1. Selecteer de tekst in de redacteursruimte en klik _Tussenvoegsel/geef verbinding_ uit ( ![ Tussenvoegsel/geef verbindingsknoop ](./assets/pb-icon-add-link.png){width="20"}) op de redacteurstoolbar uit.

   ![ Toevoegend een verbinding aan geformatteerde teksten ](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. Voer bij **[!UICONTROL URL]** de relatieve koppeling in die u hebt voorbereid.

1. Stel **[!UICONTROL Target]** in op `None` .

   Met deze instelling wordt de pagina in hetzelfde browservenster geopend in plaats van een nieuw tabblad te openen.

1. Voer bij **[!UICONTROL Title]** `Shop Tees` in.

   Het koppelingskenmerk `Title` wordt door sommige browsers gebruikt als knopinfo.

1. Klik op **[!UICONTROL OK]** om de koppeling op te slaan en terug te keren naar de werkruimte van [!DNL Page Builder] .

   ![ het detail van de Verbinding ](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## Een afbeelding invoegen

1. Plaats de cursor in de tekst waar u de afbeelding wilt invoegen.

1. Klik _Tussenvoegsel/geef beeld_ uit ( ![ Tussenvoegsel/geef beeldknoop uit ](./assets/icon-pb-add-image.png){width="20"}) op de redacteurstoolbar.

1. Klik bij **[!UICONTROL Source]** op het zoekpictogram om de mediaopslag te gebruiken voor het zoeken naar en het selecteren van een afbeelding.

1. Voer bij **[!UICONTROL Image Description]** een beschrijvende tekst in voor de afbeelding.

   Deze tekst vult het kenmerk `alt` link voor de afbeelding en wordt door sommige browsers gebruikt voor toegankelijkheid.

1. Voer de breedte en hoogte in **[!UICONTROL Dimensions]** in pixels in voor het weergeven van de afbeelding op de pagina.

   Laat het selectievakje **[!UICONTROL Constrain proportions]** ingeschakeld om automatisch de hoogte-breedteverhouding voor de afbeelding te behouden.

1. Als u de afbeelding wilt invoegen en vervolgens wilt terugkeren naar de werkruimte van [!DNL Page Builder] , klikt u op **[!UICONTROL OK]** .

## Tekstinstellingen wijzigen

1. Beweeg over de tekstcontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

   >[!NOTE]
   >
   >Omdat de tekstcontainer stevig in een andere container wordt genest, zorg ervoor dat u correcte toolbox hebt.

1. Werk de inhoud naar wens bij.

1. Werk de instellingen van _[!UICONTROL Advanced]_&#x200B;naar wens bij.

   - Kies een **[!UICONTROL Alignment]** als u de positie van de tekst in de bovenliggende container wilt bepalen:

     | Optie | Beschrijving |
     | ------ |------------ |
     | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
     | `Left` | Hiermee lijnt u de lijst uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
     | `Center` | Hiermee lijnt u de lijst in het midden van de bovenliggende container uit, rekening houdend met de opgegeven opvulling. |
     | `Right` | Hiermee lijnt u het blok uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

     {style="table-layout:auto"}

   - Stel de stijl **[!UICONTROL Border]** in die wordt toegepast op alle vier zijden van de tekstcontainer:

     | Optie | Beschrijving |
     | ------ |------------ |
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

     | Optie | Beschrijving |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
     | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
     | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

     {style="table-layout:auto"}

   - (Optioneel) Geef de namen van **[!UICONTROL CSS classes]** op uit de huidige stijlpagina die u op de container wilt toepassen.

     Scheid meerdere klassennamen met een spatie.

   - Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en binnenopvulling van de tekstcontainer te bepalen.

     Voer de overeenkomende waarden in het diagram in.

     | Containergebied | Beschrijving |
     | -------------- |------------ |
     | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .
