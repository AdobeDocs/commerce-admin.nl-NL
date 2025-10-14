---
title: Inhoud toevoegen - Blokkeren
description: Leer over het inhoudstype van het Blok, dat wordt gebruikt om een herbruikbaar blok aan het  [!DNL Page Builder]  stadium toe te voegen.
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Inhoud toevoegen - Blokkeren

Gebruik het _inhoudstype van het Blok_ om een bestaand, actief [&#x200B; blok &#x200B;](../content-design/blocks.md) aan het [[!DNL Page Builder]  stadium &#x200B;](workspace.md#stage) toe te voegen. In het volgende voorbeeld bevat de eerste kolom het blok met een zijmenu voor de pagina. De tweede kolom bevat een afbeelding.

![&#x200B; Blok met een zijmenu &#x200B;](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Gereedschap Blok

| Gereedschap | Pictogram | Beschrijving |
| --------- | -------- | ------------- |
| Verplaatsen | ![&#x200B; pictogram van de Beweging &#x200B;](./assets/pb-icon-move.png) | Verplaatst de blokcontainer en de inhoud ervan naar een andere positie in het werkgebied. |
| Instellingen | ![&#x200B; pictogram van Montages &#x200B;](./assets/pb-icon-settings.png) | Hiermee opent u de pagina Blok bewerken, waarin u het blok kunt kiezen en de eigenschappen van de container kunt wijzigen. |
| Verbergen | ![&#x200B; het pictogram van de Huid &#x200B;](./assets/pb-icon-hide.png) | Hiermee verbergt u de huidige blokcontainer en de inhoud ervan. |
| Tonen | ![&#x200B; toon pictogram &#x200B;](./assets/pb-icon-show.png) | Toont de verborgen blokcontainer en de inhoud ervan. |
| Dupliceren | ![&#x200B; Dupliceer pictogram &#x200B;](./assets/pb-icon-duplicate.png) | Hiermee maakt u een kopie van de blokcontainer en de inhoud ervan. |
| Verwijderen | ![&#x200B; verwijder pictogram &#x200B;](./assets/pb-icon-remove.png) | Verwijdert de blokcontainer en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een bestaand blok toevoegen

1. Navigeer naar de werkruimte [!DNL Page Builder] op de doelpagina, het blok, het dynamische blok, het product of de categorie.

1. Vouw [!DNL Page Builder] uit in het deelvenster **[!UICONTROL Add Content]** en sleep een tijdelijke aanduiding **[!UICONTROL Block]** naar het werkgebied.

   ![&#x200B; slepend een blok op het stadium &#x200B;](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Beweeg over de lege blokcontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![&#x200B; pictogram van Montages &#x200B;](./assets/pb-icon-settings.png){width="25"}).

1. Klik op **[!UICONTROL Select Block]**.

   ![&#x200B; Selecterend een blok &#x200B;](./assets/pb-add-content-block-select.png){width="200"}

1. Klik in de rij van het blok dat u wilt toevoegen op **[!UICONTROL Select]** in de laatste kolom.

   ![&#x200B; Geselecteerd blok &#x200B;](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   De naam van het geselecteerde blok verschijnt op de pagina.

   ![&#x200B; de naam van het Blok &#x200B;](./assets/pb-add-content-block-name.png){width="200"}

1. Vul de overige instellingen naar wens in en gebruik de veldbeschrijvingen aan het einde van deze pagina ter referentie.

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

### Geavanceerde instellingen

1. Kies een **[!UICONTROL Alignment]** als u de plaatsing van het blok binnen de bovenliggende container wilt bepalen:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
   | `Left` | Hiermee lijnt u de lijst uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Center` | Hiermee lijnt u de lijst in het midden van de bovenliggende container uit, rekening houdend met de opgegeven opvulling. |
   | `Right` | Hiermee lijnt u het blok uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

   {style="table-layout:auto"}

1. Stel een **[!UICONTROL Border]** -stijl in die wordt toegepast op alle vier zijden van de blokcontainer:

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

1. (Optioneel) Geef de namen van **[!UICONTROL CSS classes]** op uit de huidige stijlpagina die u op de container wilt toepassen.

   Scheid meerdere klassennamen met een spatie.

1. Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de blokcontainer te bepalen.

   Voer de overeenkomende waarden in het diagram in.

   | Containergebied | Beschrijving |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Blokinstellingen bewerken

1. Beweeg over de blokcontainer en kies het _pictogram van Montages_ ( ![&#x200B; pictogram van Montages &#x200B;](./assets/pb-icon-settings.png){width="25"}) in toolbox.

   ![&#x200B; Toolbox van het Blok &#x200B;](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Select Block]** om een ander blok te kiezen.

   - Klik in de lijst met actieve blokken op **[!UICONTROL Select]** het blok dat u wilt toevoegen.
   - Klik op **[!UICONTROL Add Selected]**.

1. Werk de overige instellingen naar wens bij en gebruik de veldbeschrijvingen aan het einde van deze pagina ter referentie.

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

## Een blok dupliceren

1. Beweeg over de blokcontainer om toolbox te tonen en _te kiezen dupliceert_ (![&#x200B; Dupliceer pictogram &#x200B;](./assets/pb-icon-duplicate.png)) pictogram.

   Het duplicaat wordt net onder het origineel weergegeven.

1. Om het nieuwe blok aan een nieuwe positie te bewegen, beweegt over de container, en klikt dan _Beweging_ (![&#x200B; pictogram van de Beweging &#x200B;](./assets/pb-icon-move.png)) in toolbox.

1. Selecteer en sleep het blok totdat de rode hulplijn op de nieuwe positie wordt weergegeven.

   De boven- en onderrand van elke container worden weergegeven als onderbroken lijnen terwijl het blok wordt verplaatst.

## Een blok uit het werkgebied verwijderen

1. Beweeg over de blokcontainer om toolbox te tonen en _te kiezen verwijder_ (![&#x200B; verwijder pictogram &#x200B;](./assets/pb-icon-remove.png)).

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
