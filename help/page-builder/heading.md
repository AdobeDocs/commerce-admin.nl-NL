---
title: Elementen - kop
description: Leer over het inhoudstype van de Kop, dat wordt gebruikt om een tekstcontainer met een kopniveau van H1 aan H6 aan het  [!DNL Page Builder]  stadium toe te voegen.
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Elementen - kop

Met kopniveaus wordt een hiërarchie ingesteld die inhoud ordent en zoekprogramma&#39;s helpt elke pagina te indexeren. Gebruik het _inhoudstype van de Kop_ in het [[!DNL Page Builder]  stadium ](workspace.md#stage) om een tekstcontainer met een kopniveau van H1 aan H6 aan het stadium toe te voegen. Koppen worden opgemaakt op basis van het stijlblad dat is gekoppeld aan het huidige thema.

Het [ gebied van de Kop van de Inhoud ](workspace.md) in de _[!UICONTROL Content]_sectie kan worden gebruikt om een H1 rubriek aan de bovenkant van de pagina toe te voegen. Het veld is echter een verouderde versie van [!DNL Commerce] en wordt geleverd ter ondersteuning van oudere inhoud. In dit veld worden de geavanceerde functies van [!DNL Page Builder] niet benut. Het wordt aanbevolen het veld Inhoudskop leeg te laten en het inhoudstype [!DNL Page Builder] Koptekst te gebruiken om koppen van een willekeurig niveau aan de pagina toe te voegen.

In het volgende voorbeeld ziet u hoe de inhoudsopgave Kop inhoud en Kop worden weergegeven wanneer deze worden opgemaakt door het thema Luma.

![ Kop van de Inhoud en de kopniveaus op de storefront ](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

U kunt een rubriek van de _sectie van Elementen_ van het [!DNL Page Builder] paneel aan een rij, een kolom, of een lusjereeks op het stadium slepen. Het kopniveau en de groepering kunnen van de redacteurstoolbar op het stadium worden gecontroleerd, of door de _controle van Montages_ te gebruiken ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Kop-editor

![ Redacteur van de Kop met toolbar ](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Gereedschap Keuzerondje

Net als bij alle inhoudscontainers wordt de gereedschapset weergegeven wanneer u de muisaanwijzer op de container plaatst.

![ de containertoolbox van de Rubriek ](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Gereedschap | Pictogram | Beschrijving |
| --------- | ----------------- | ---------------------- |
| Verplaatsen | ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="25"} | Hiermee verplaatst u de kopcontainer naar een andere geldige plaats op de pagina. |
| (label) | Kop | Identificeert de huidige container als een kop. |
| Instellingen | ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de pagina Koptekst bewerken, waarin u de eigenschappen van de container kunt wijzigen. |
| Verbergen | ![ het pictogram van de Huid ](./assets/pb-icon-hide.png){width="25"} | Hiermee verbergt u de container van de kop. |
| Tonen | ![ toon pictogram ](./assets/pb-icon-show.png){width="25"} | Hiermee wordt de verborgen kopcontainer weergegeven. |
| Dupliceren | ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="25"} | Hiermee maakt u een kopie van de kopcontainer. |
| Verwijderen | ![ verwijder pictogram ](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de kopcontainer en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een kop toevoegen

1. Vouw in het deelvenster [!DNL Page Builder] **[!UICONTROL Elements]** uit en sleep een tijdelijke aanduiding **[!UICONTROL Heading]** naar een rij, kolom of tabset in het werkgebied.

   ![ slepend een rubriek aan het stadium ](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. Voer in de editor de koptekst in boven de tijdelijke aanduiding voor `Edit Heading Text` .

   Standaard wordt aan de koptekst een koptekst van niveau twee (H2) toegewezen.

   ![ Placeholder in de koptekstredacteur ](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Kies in de werkbalk het juiste koptype tussen H1 en H6.

1. Wijzig indien nodig de uitlijning.

## Koptekstinstellingen bewerken

1. Beweeg over de koptekstcontainer om toolbox te tonen en de _pictogram van Montages_ te kiezen ( ![ pictogram van Montages ](./assets/pb-icon-settings.png){width="20"}).

   ![ Toolbox van de Rubriek ](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Werk indien nodig de kopinhoud bij (**[!UICONTROL Heading Type]** en **[!UICONTROL Heading Text]**).

   U kunt deze inhoud ook bijwerken in de kopteksteditor.

1. Werk de instellingen van _[!UICONTROL Advanced]_naar wens bij.

   - Kies een **[!UICONTROL Alignment]** als u de positie van de kop in de bovenliggende container wilt bepalen:

     | Optie | Beschrijving |
     | ------ | ----------- |
     | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
     | `Left` | Hiermee lijnt u de lijst uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
     | `Center` | Hiermee lijnt u de lijst in het midden van de bovenliggende container uit, rekening houdend met de opgegeven opvulling. |
     | `Right` | Hiermee lijnt u het blok uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

     {style="table-layout:auto"}

   - Stel de stijl **[!UICONTROL Border]** in die op alle vier zijden van de kopcontainer wordt toegepast:

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

     | Optie | Beschrijving |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
     | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
     | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

     {style="table-layout:auto"}

   - (Optioneel) Geef de namen van **[!UICONTROL CSS classes]** op uit de huidige stijlpagina die u op de container wilt toepassen.

     Scheid meerdere klassennamen met een spatie.

   - Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de kopcontainer te bepalen.

     Voer de overeenkomende waarden in het diagram in.

     | Containergebied | Beschrijving |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Klik na afloop op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de werkruimte van [!DNL Page Builder] .

## Een kop dupliceren

Voor een opgemaakte kop met specifieke instellingen is het efficiënter om de kop te dupliceren in plaats van opnieuw te beginnen met een nieuwe plaatsaanduiding.

1. Beweeg over de koptekstcontainer om toolbox te tonen en _te kiezen dupliceert_ ( ![ Dupliceer pictogram ](./assets/pb-icon-duplicate.png){width="20"}) pictogram.

   Het duplicaat wordt net onder het origineel weergegeven.

   ![ Duplicerend een koptekstcontainer ](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Beweeg over de nieuwe koptekstcontainer om toolbox te tonen en de _Beweging_ te kiezen ( ![ pictogram van de Beweging ](./assets/pb-icon-move.png){width="20"}) pictogram.

   ![ Bewegend een rubriek ](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Selecteer en sleep de kop totdat de rode hulplijn de nieuwe positie markeert.

   De boven- en onderrand van elke container worden weergegeven als onderbroken lijnen terwijl de kop wordt verplaatst.

   ![ Bewegend de gedupliceerde rubriek in positie ](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Als u het kopniveau wilt wijzigen, klikt u op de koptekst en kiest u het nieuwe niveau in de editor-werkbalk.

   ![ Kiekend een nieuw kopniveau ](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
