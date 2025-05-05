---
title: Storefront-branding
description: Meer informatie over het wijzigen van de elementen die de merkidentiteit van uw winkel definiëren.
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---

# Storefront-branding

Één van de eerste dingen u wilt doen is het embleem [&#128279;](#upload-your-logo) in de kopbal te veranderen en [ een favicon ](#add-a-favicon) voor browser te uploaden. [ Daarna, zou u uw welkome bericht ](#change-the-welcome-message) moeten toevoegen en [ de copyrightkennisgeving ](#change-the-copyright-notice) in footer bijwerken.  Deze taken zijn een paar eenvoudige ontwerpelementen die u meteen kunt uitvoeren. Terwijl uw opslag in ontwikkeling is, kunt u [ de kennisgeving van de opslagdemo ](#set-the-store-demo-notice) aanzetten, en dan het verwijderen wanneer u klaar bent om te lanceren.

![ Storefront brandende elementen ](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## Uw logo uploaden

De grootte en locatie van het logo in de koptekst wordt bepaald door het winkelthema. Uw logo kan worden opgeslagen als een GIF-, PNG- of JPG-bestandstype (JPEG) en worden geüpload vanuit de beheerder van uw winkel.

![ Logo in Kopbal ](./assets/storefront-header-logo.png){width="600"}

De afbeelding van het logo bevindt zich op de volgende locatie op de server. Elk afbeeldingsbestand met de naam `logo.svg` wordt gebruikt als het standaardthemalogo.

Volledig pad - `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

Relatief pad - `images/logo.svg`

Als u de grootte van het logo of andere afbeeldingen die in het thema worden gebruikt niet weet, opent u de pagina in een browser, klikt u met de rechtermuisknop op de afbeelding en inspecteert u het element.

>[!NOTE]
>
>Naast het embleem in de kopbal, verschijnt uw embleem ook op [ e-mailmalplaatjes ](../systems/email-templates.md#prepare-your-email-logo) en op [ PDF facturen ](../stores-purchase/sales-documents.md) en andere verkoopdocumenten. De logo&#39;s die voor e-mailsjablonen en facturen worden gebruikt, hebben verschillende groottevereisten en moeten afzonderlijk worden geüpload.

Ondersteunde bestandsindelingen voor logo&#39;s:

| Bestandsindeling | Beschrijving |
|--- |--- |
| PNG | (Portable Network Graphics) Dit nieuwere alternatief voor de indeling GIF ondersteunt maximaal 16 miljoen kleuren (24 bits). De compressie-indeling zonder verlies produceert een bitmapafbeelding van hoge kwaliteit met heldere tekst, maar een groter bestand dan sommige indelingen. De PNG-indeling ondersteunt transparante lagen en is ontworpen voor onlineweergave en -streaming. |
| GIF | (Graphics Interchange Format) Een breed ondersteunde en oudere bitmapindeling die is beperkt tot 256 kleuren (8 bits). De indeling GIF ondersteunt eenvoudige animatie en transparante lagen. |
| JPG (JPEG) | (Joint Photographic Expert Group) Een gecomprimeerde bitmapindeling die door de meeste digitale camera&#39;s wordt gebruikt. De compressie met verlies veroorzaakt gegevensverlies, wat soms opvalt als vage vlekken in tekst. |

{style="table-layout:auto"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![ pagina van de Configuratie van het Ontwerp ](./assets/design-configuration.png){width="700"}

1. Zoek de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Header]** sectie uit.

   ![ montages van de Kopbal ](./assets/configuration-header.png){width="600"}

1. Als u een nieuw logo wilt uploaden, klikt u op **[!UICONTROL Upload]** en kiest u het bestand in uw systeem.

1. Voer de **[!UICONTROL Logo Image Width]** en **[!UICONTROL Logo Image Height]** in pixels in.

1. Voer bij **[!UICONTROL Logo Image Alt]** de tekst in die u wilt weergeven wanneer iemand de cursor boven de afbeelding houdt.

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

## Een favicon toevoegen

_Favicon_ is kort voor _favoriet pictogram_ en verwijst naar het kleine pictogram op het lusje van elke browser pagina. Afhankelijk van de browser wordt het favicon ook weergegeven in de adresbalk, vlak voor de URL.

Een favicon heeft doorgaans een grootte van 16 x 16 pixels of 32 x 32 pixels. [!DNL Commerce] accepteert bestandstypen ICO, PNG, APNG, GIF en JPG (JPEG), hoewel niet alle browsers deze indelingen ondersteunen. De meest ondersteunde bestandsindeling voor een favicon is ICO. U kunt andere typen afbeeldingsbestanden gebruiken, maar de indeling wordt mogelijk niet door alle browsers ondersteund. Er zijn veel gratis gereedschappen online beschikbaar waarmee u een ICO-afbeelding kunt genereren of een afbeelding kunt omzetten in die indeling.

![ Favicon in browser tabel ](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] ondersteunt de volgende bestandsindelingen als favicon:

| Bestandsindeling | Beschrijving |
|--- |--- |
| ICO | Deze indeling voor afbeeldingsbestanden is ontworpen voor pictogramafbeeldingen op kleine grootte. De ICO-indeling wordt vooral gebruikt in Microsoft® Windows OS en kan afbeeldingen tot 256 x 256 pixels en 16 miljoen kleuren (24 bits) met 8 bits transparantie bevatten. |
| PNG | (Portable Network Graphics) Dit nieuwere alternatief voor de indeling GIF ondersteunt maximaal 16 miljoen kleuren (24 bits). De compressie-indeling zonder verlies produceert een bitmapafbeelding van hoge kwaliteit met heldere tekst, maar een groter bestand dan sommige indelingen. De PNG-indeling ondersteunt transparante lagen en is ontworpen voor onlineweergave en -streaming. |
| APNG | (Geanimeerde Portable Network Graphics) Een bestandsindeling die vergelijkbaar is met PNG en eenvoudige animatie ondersteunt. |
| GIF | (Graphics Interchange Format) Een breed ondersteunde en oudere bitmapindeling die is beperkt tot 256 kleuren (8 bits). De indeling GIF ondersteunt eenvoudige animatie en transparante lagen. |
| JPG (JPEG) | (Joint Photographic Expert Group) Een gecomprimeerde bitmapindeling die door de meeste digitale camera&#39;s wordt gebruikt. De compressie met verlies veroorzaakt gegevensverlies, wat soms opvalt als vage vlekken in tekst. |

{style="table-layout:auto"}

### Stap 1: Een favicon maken

1. Maak met de afbeeldingseditor van uw keuze een afbeelding van 16 x 16 of 32 x 32 pixels van het logo.

1. (Optioneel) Gebruik een van de beschikbare online gereedschappen om het bestand om te zetten in de indeling .ico en het bestand op te slaan op uw computer.

### Stap 2: Upload het favicon naar uw winkel

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek in het raster de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _[!UICONTROL Other Settings]_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL HTML Head]**&#x200B;sectie.

   ![ HTML Hoofd montages ](./assets/configuration-html-head.png){width="600"}

1. Als u huidig favicon wilt verwijderen, klik _Schrapping_ (![ het vuilnisbakpictogram ](../assets/icon-delete-trashcan.png)) pictogram in de laag-linkerhoek van het beeld.

1. Klik op **[!UICONTROL Upload]** en open het favicon-bestand dat u hebt voorbereid.

   ![ Geüpload favicon ](./assets/favicon-upload.png){width="400"}

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

### Stap 3: De cache vernieuwen

1. Als u wordt gevraagd de cache te vernieuwen, klikt u op de koppeling **[!UICONTROL Cache Management]** in het bericht boven aan de werkruimte.

1. Selecteer in de lijst het selectievakje **[!UICONTROL Page Cache]** dat is gemarkeerd als `Invalidated` .

1. Stel **[!UICONTROL Actions]** in op `Refresh` en klik op **[!UICONTROL Submit]** .

1. Als u het nieuwe favicon wilt weergeven, gaat u terug naar uw winkel en vernieuwt u de browser.

## Het welkomstbericht wijzigen

Het welkomstbericht in de koptekst wordt uitgebreid om de naam van de klant op te nemen die is aangemeld. Alvorens u uw opslag lanceert, ben zeker om het gebrek _Onthaal_ tekst voor elke archiefmening te veranderen.

![ Welkome bericht ](./assets/storefront-welcome-message.png){width="600"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek in het raster de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _[!UICONTROL Other Settings]_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Header]**&#x200B;sectie.

1. Voer bij **[!UICONTROL Welcome Text]** de welkomstberichttekst in die u wilt weergeven in de koptekst van uw winkel.

   ![ montages van de Kopbal ](./assets/configuration-header.png){width="600"}

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

1. Als u wordt gevraagd om de paginacache bij te werken, klikt u op de koppeling **[!UICONTROL Cache Management]** boven aan de werkruimte en volgt u de instructies om de cache te vernieuwen.

## De copyrightmelding wijzigen

In de winkel wordt op elke pagina een copyrightvermelding weergegeven. Als beste praktijken, zou de auteursrechtkennisgeving het huidige jaar moeten omvatten, en uw bedrijf identificeren als wettige eigenaar van de inhoud op de plaats.

![ de berichtvoorbeeld van Copyright ](./assets/storefront-footer-copyright.png){width="600"}

De tekencode `&copy;` wordt gebruikt om het copyrightsymbool in te voegen, zoals in de volgende voorbeelden wordt getoond:

- Voorbeeld van lange notatie

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- Voorbeeld van korte indeling

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_om de copyrightkennisgeving bij te werken:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek in het raster de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _Andere Montages_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Footer]** sectie uit.

   ![ het ontwerpmontages van de Voettekst ](./assets/configuration-footer.png){width="600"}

1. Voer bij **[!UICONTROL Copyright]** de copyrightvermelding in die u in de voettekst van elke pagina wilt weergeven.

   Gebruik de tekencode `&copy;` om een copyrightsymbool in te voegen.

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

## Melding van opslagdemo instellen

Als uw winkel online is, maar nog steeds in aanbouw is, kunt u boven aan de pagina een demo van de winkel weergeven om mensen te laten weten dat de winkel nog niet geopend is voor zakelijk gebruik. Wanneer u bereid bent om _levend_ te gaan, verwijder eenvoudig het bericht. Het is gelijkaardig aan het omdraaien van het teken dat in het venster van _gesloten_ aan _Open_ hangt. De indeling van de demo-kennisgeving wordt bepaald door het thema van uw winkel.

![ bericht van de de manifestatie van de Storefront ](./assets/storefront-demo-notice.png){width="600"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek in het raster de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _[!UICONTROL Other Settings]_, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL HTML Head]**&#x200B;sectie.

   ![ HTML Head ](./assets/configuration-html-head.png){width="600"}

1. Schuif omlaag naar de onderkant en stel de **[!UICONTROL Display Demo Store Notice]** in op uw voorkeur.

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

1. Als u wordt gevraagd om de cache bij te werken, klikt u op **[!UICONTROL Cache Management]** in het systeembericht en volgt u de instructies om de cache te vernieuwen.
