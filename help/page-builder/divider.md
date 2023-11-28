---
title: Elementen - Verdeler
description: Leer over het inhoudstype Scheider, dat wordt gebruikt om een regel als visuele onderbreking tussen secties in te voegen [!DNL Page Builder] in het werkgebied.
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Elementen - Verdeler

Gebruik de _Scheidingslijn_ inhoudstype om een regel toe te voegen als een visueel onderbreking tussen secties in de [[!DNL Page Builder] stadium](workspace.md#stage). U kunt de lijnkleur, dikte en breedte van de scheidingslijn opgeven. U kunt ook de uitlijning bepalen, de marges en opvulling instellen en de opmaak van de containerrand instellen. Standaard is de scheidingslijn een haarlijnregel die de volledige breedte van de container uitbreidt, met ruimte voor opvulling.

![Standaardscheidingslijn in een container zonder rand](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

Hoewel de meeste verdeler containers onzichtbaar zijn, toont het volgende voorbeeld de container met een rode gestippelde grens zodat kunt u het verband tussen de verdeler, de opvulling, en de container zien. U kunt de opvulling boven en onder aan de scheidingslijn aanpassen om de afstand tussen de elementen te bepalen.

![Scheidingslijn met opvulling in container met onderbroken rand](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Scheidingsgereedschapset

| Gereedschap | Pictogram | Beschrijving |
| ---- | --------------------| ------------|
| Verplaatsen | ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="25"} | Verplaatst de container van de verdeler naar een andere geldige plaats op de pagina. |
| (label) | SCHEIDINGSTEKEN | Identificeert de huidige container als een scheidingselement. |
| Instellingen | ![Instellingenpictogram](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de pagina Verdeler bewerken, waarin u de eigenschappen van de scheidingslijn en de bijbehorende container kunt wijzigen. |
| Verbergen | ![Pictogram verbergen](./assets/pb-icon-hide.png){width="25"} | Hiermee verbergt u de scheidingscontainer. |
| Tonen | ![Pictogram tonen](./assets/pb-icon-show.png){width="25"} | Hiermee wordt de verborgen scheidingscontainer weergegeven. |
| Dupliceren | ![Pictogram Dupliceren](./assets/pb-icon-duplicate.png){width="25"} | Hiermee maakt u een kopie van de container voor scheidingstekens. |
| Verwijderen | ![Pictogram verwijderen](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de container van de scheidingslijn en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een scheidingslijn toevoegen

1. In de [!DNL Page Builder] deelvenster, uitvouwen **[!UICONTROL Elements]** en sleep een **[!UICONTROL Divider]** plaatsaanduiding voor een rij, kolom of tabset in het werkgebied.

   Gebruik de rode hulplijn ter referentie wanneer u de scheidingslijn voor of na een andere inhoudscontainer in het werkgebied plaatst.

   ![Een scheidingslijn naar het werkgebied slepen](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   In het volgende voorbeeld markeert de scheidingslijn het begin van een nieuwe tekstsectie.

   ![Secties van tekst scheiden door scheidingstekens](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. Volg de volgende procedure om de instellingen van de nieuwe scheidingslijn op te geven.

## De instellingen voor de scheidingslijn wijzigen

1. Houd de aanwijzer boven de container om de gereedschapset weer te geven en kies de optie _Instellingen_ ( ![Instellingenpictogram](./assets/pb-icon-settings.png){width="20"} ).

   ![Scheidingsgereedschapset](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. De scheidingslijn wijzigen **[!UICONTROL Line Color]** met een van de volgende methoden:

   - Voer een geldige waarde in [Kleurnaam HTML][1]. Bijvoorbeeld, `Teal`.
   - Voer de hexadecimale kleurwaarde in. Bijvoorbeeld, `#008080`.

   Klik op **[!UICONTROL Apply]**.

   ![De lijnkleur instellen](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. Voer de **[!UICONTROL Line Thickness]** in pixels.

1. Voer de **[!UICONTROL Line Width]** gevolgd door: `px` of `%`.

   ![Lijnkleur, -dikte en -breedte instellen](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. Werk de _[!UICONTROL Advanced]_instellingen.

   - Als u de positie van de scheidingslijn in de bovenliggende container wilt bepalen, kiest u de optie **[!UICONTROL Alignment]**:

     | Optie | Beschrijving |
     | ------ | ----------- |
     | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
     | `Left` | Hiermee lijnt u de lijst uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
     | `Center` | Hiermee lijnt u de lijst in het midden van de bovenliggende container uit, rekening houdend met de opgegeven opvulling. |
     | `Right` | Hiermee lijnt u het blok uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

     {style="table-layout:auto"}

     In het volgende voorbeeld worden de opties zo ingesteld dat voor de scheidingslijn een uitlijning in het midden wordt gebruikt.

     ![Scheidingslijn met middelste uitlijning](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Stel de **[!UICONTROL Border]** stijl toegepast op alle vier zijden van de container van de verdeler:

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

   - Als u een andere randstijl dan `None`, vult u de weergaveopties voor de rand in:

     | Optie | Beschrijving |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
     | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
     | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

     {style="table-layout:auto"}

   - (Optioneel) Geef de namen op van **[!UICONTROL CSS classes]** in het huidige stijlblad toe te passen op de container.

     Scheid meerdere klassennamen met een spatie.

   - Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de container van de verdeler te bepalen.

     Voer de overeenkomende waarden in het diagram in.

     | Containergebied | Beschrijving |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Klik op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de [!DNL Page Builder] werkruimte.

   ![Scheidingslijn gecentreerd in een rij](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## Een scheidingslijn dupliceren

Voor een opgemaakte scheidingslijn met specifieke instellingen is het efficiënter om een duplicaat te maken in plaats van opnieuw te beginnen met een nieuwe plaatsaanduiding.

1. Houd de aanwijzer boven de container om de gereedschapset weer te geven en kies de optie _Dupliceren_ ( ![Pictogram Dupliceren](./assets/pb-icon-duplicate.png){width="20"} ).

   De gedupliceerde container wordt net onder het origineel weergegeven.

   ![Dubbele scheidingslijn](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. Houd de aanwijzer boven de nieuwe scheidingscontainer om de gereedschapset weer te geven en kies de optie _Verplaatsen_ ( ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="20"} ).

   ![Een scheidingslijn verplaatsen](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. Selecteer en sleep de scheidingslijn totdat de rode hulplijn de nieuwe positie markeert.

   De boven- en onderrand van elke container worden weergegeven als onderbroken lijnen terwijl de scheidingslijn wordt verplaatst.

   ![De gedupliceerde scheidingslijn verplaatsen naar de juiste positie](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}

[1]: https://en.wikipedia.org/wiki/Web_colors
