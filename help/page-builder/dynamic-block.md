---
title: Inhoud toevoegen - Dynamisch blok
description: Meer informatie over het inhoudstype Dynamisch blok dat wordt gebruikt om een herbruikbaar dynamisch blok toe te voegen aan het dialoogvenster [!DNL Page Builder] in het werkgebied.
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Inhoud toevoegen - Dynamisch blok

Het inhoudstype Dynamisch blok gebruiken om een bestaand blok toe te voegen [dynamisch blok](../content-design/dynamic-blocks.md) aan de [[!DNL Page Builder] stadium](workspace.md#stage).

![Dynamisch blok op de opslagvoorgrond](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Werkset Dynamisch blok

| Gereedschap | Pictogram | Beschrijving |
| --------- | ------------- | ----------------- |
| Verplaatsen | ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="25"} | Verplaatst de blokcontainer en de inhoud ervan naar een andere positie in het werkgebied. |
| Instellingen | ![Instellingenpictogram](./assets/pb-icon-settings.png){width="25"} | Hiermee opent u de _Blok bewerken_ pagina, waar u het blok kunt kiezen en de eigenschappen van de container kunt wijzigen. |
| Verbergen | ![Pictogram verbergen](./assets/pb-icon-hide.png){width="25"} | Hiermee verbergt u de huidige blokcontainer en de inhoud ervan. |
| Tonen | ![Pictogram tonen](./assets/pb-icon-show.png){width="25"} | Toont de verborgen blokcontainer en de inhoud ervan. |
| Dupliceren | ![Pictogram Dupliceren](./assets/pb-icon-duplicate.png){width="25"} | Hiermee maakt u een kopie van de blokcontainer en de inhoud ervan. |
| Verwijderen | ![Pictogram verwijderen](./assets/pb-icon-remove.png){width="25"} | Verwijdert de blokcontainer en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een bestaand dynamisch blok toevoegen aan het werkgebied

1. Ga naar de [!DNL Page Builder] werkruimte op de doelpagina, het doelblok, het product of de doelcategorie.

1. In de [!DNL Page Builder] deelvenster, uitvouwen **[!UICONTROL Add Content]** en sleep een **[!UICONTROL Dynamic Block]** tijdelijke aanduiding naar het werkgebied.

   ![Een tijdelijke aanduiding voor een dynamisch blok naar het werkgebied slepen](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Houd de muisaanwijzer boven de lege dynamische blokcontainer om de gereedschapset weer te geven en kies de optie _Instellingen_ ( ![Instellingenpictogram](./assets/pb-icon-settings.png){width="20"} ).

   ![Werkset Dynamisch blok](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Op de _Dynamisch blok bewerken_ pagina, klikt u **[!UICONTROL Select Dynamic Block]** en gebruikt u de lijst om het blok te selecteren.

   ![Een dynamisch blok selecteren](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   Zoek in de lijst het dynamische blok dat u wilt invoegen en klik op **[!UICONTROL Select]**. Klik vervolgens op **[!UICONTROL Add Selected]**.

   ![Een dynamisch blok in de lijst selecteren](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   Hieronder wordt een samenvatting van de dynamische blokinformatie weergegeven.

   ![Samenvatting van dynamisch blok](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Template]** op een van de volgende wijzen:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | Voegt een standalone blok toe. |
   | `Dynamic Block Inline Template` | Voegt de blokinhoud in tekst in. |

   {style="table-layout:auto"}

   ![Dynamische bloksjabloon](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. Vul de gewenste geavanceerde instellingen in.

1. Klik op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de [!DNL Page Builder] werkruimte.

### Geavanceerde instellingen

1. Als u de plaatsing van het dynamische blok in de bovenliggende container wilt bepalen, kiest u een **[!UICONTROL Alignment]**:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
   | `Left` | Hiermee lijnt u de lijst uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Center` | Hiermee lijnt u de lijst in het midden van de bovenliggende container uit, rekening houdend met de opgegeven opvulling. |
   | `Right` | Hiermee lijnt u het blok uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

   {style="table-layout:auto"}

1. Stel de **[!UICONTROL Border]** stijl die wordt toegepast op alle vier zijden van de dynamische blokcontainer:

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

1. Als u een andere randstijl dan `None`, vult u de weergaveopties voor de rand in:

   | Optie | Beschrijving |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
   | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
   | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

   {style="table-layout:auto"}

1. (Optioneel) Geef de namen op van **[!UICONTROL CSS classes]** in het huidige stijlblad toe te passen op de container.

   Scheid meerdere klassennamen met een spatie.

1. Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de dynamische blokcontainer te bepalen.

   Voer de overeenkomende waarden in het diagram in.

   | Containergebied | Beschrijving |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de container. Opties: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Dynamische blokcontainerinstellingen bewerken

1. Houd de muisaanwijzer boven de dynamische blokcontainer om de gereedschapset weer te geven en kies de optie _Instellingen_ ( ![Instellingenpictogram](./assets/pb-icon-settings.png){width="20"} ).

   ![Werkset Dynamisch blok](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. Wijzig zo nodig het dynamische blok:

   - Klik op **[!UICONTROL Select Dynamic Block]**.

     ![Een ander dynamisch blok selecteren](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - Klik in de lijst met actieve dynamische blokken op **[!UICONTROL Select]** voor het blok dat u wilt toevoegen.

1. Werk de overige instellingen naar wens bij.

1. Klik op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de [!DNL Page Builder] werkruimte.

## Een dynamisch blok dupliceren

1. Houd de muisaanwijzer boven de dynamische blokcontainer om de gereedschapset weer te geven en kies de optie _Dupliceren_ ( ![Pictogram Dupliceren](./assets/pb-icon-duplicate.png){width="20"} ).

   Het duplicaat wordt net onder het origineel weergegeven.

   ![Een dynamisch blok dupliceren](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. Als u het nieuwe dynamische blok naar een andere positie wilt verplaatsen, houdt u de muisaanwijzer boven de container en kiest u _Verplaatsen_ ( ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="20"} ) in de gereedschapset.

1. Selecteer en sleep het dynamische blok totdat de rode hulplijn op de nieuwe positie wordt weergegeven.

   De boven- en onderrand van elke container worden weergegeven als onderbroken lijnen terwijl het dynamische blok wordt verplaatst.

## Een dynamisch blok uit het werkgebied verwijderen

1. Houd de muisaanwijzer boven de dynamische blokcontainer om de gereedschapset weer te geven en kies de optie _Verwijderen_ ( ![Pictogram verwijderen](./assets/pb-icon-remove.png){width="20"} ).

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.
