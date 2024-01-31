---
title: Optimalisatie van afbeeldingen in mediagalerie
description: Leer hoe u de optimalisatie van afbeeldingen kunt gebruiken voor uw [!DNL Commerce] media-elementen.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Optimalisatie van afbeeldingen in mediagalerie

De nieuwe [Medialerie](media-gallery.md) verstrekt een _optimalisering van afbeeldingen_ verbeteren, waardoor de prestaties worden verbeterd en de bestandsgrootte van mediabestanden in de winkel afneemt. Deze optimalisatie is standaard ingeschakeld en kan worden gewijzigd in de configuratie-instellingen van de winkel.

## Optimalisatie van afbeeldingen configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Enable Image Optimization]** tot `Yes`.
   - Voer de **[!UICONTROL Maximum Width]** en **[!UICONTROL Maximum Height]** -waarden (in pixels) naar wens.

## Gedrag

Als optimalisatiefunctionaliteit voor afbeeldingen in de medialerie is ingeschakeld, wordt automatisch een geoptimaliseerde kopie van een afbeelding ingevoegd in de inhoud van het dialoogvenster [Medialerie](media-gallery.md) in plaats van het oorspronkelijke bestand.

Wanneer de _Maximale breedte_ en _Maximumhoogte_ De waarden worden veranderd in de configuratie, werkt het alle bestaande geoptimaliseerde beelden bij die eerder werden opgenomen.

Voor het optimaliseren van afbeeldingen in de mediagalerie moet de optie `media.gallery.renditions.update` de rijconsumenten lopen voor het regenereren van geoptimaliseerde beelden wanneer de configuratie wordt veranderd. Zie [Berichtenrijen beheren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in de _Configuratiegids_ voor meer informatie .

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
