---
title: Configuratie van productafbeelding
description: Leer hoe u een maximale pixelgrootte (breedte en hoogte) instelt en de grootte van de afbeeldingsbestanden van het product automatisch wijzigt tijdens het uploaden.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Configuratie van productafbeelding

Als u grote afbeeldingen wilt uploaden om deze op de _[!UICONTROL Product Details]_-pagina weer te geven, kunt u overwegen een maximale pixelgrootte (breedte en hoogte) in te stellen en de bestanden tijdens het uploaden automatisch te vergroten of te verkleinen. Voor ondersteuning van dit type uploaden van productafbeeldingen is er een optie waarmee u het automatisch wijzigen van het formaat van grotere afbeeldingsbestanden tijdens het uploaden kunt inschakelen. Voor het product dat u aan de catalogus wilt toevoegen maar dat u nog geen afbeeldingselement hebt om weer te geven, kunt u een voorlopige afbeelding configureren.

## Afbeeldingen van product vergroten/verkleinen

Wanneer u productafbeeldingen uploadt, kunt u grotere afbeeldingen met verschillende formaten toevoegen om gedetailleerde zoomen van hoge kwaliteit op de _[!UICONTROL Product Details]_-pagina te bieden. Om ervoor te zorgen dat alle afbeeldingen een vergelijkbare grootte en hetzelfde uiterlijk hebben, is er een optie voor het wijzigen van de grootte van de afbeelding om ervoor te zorgen dat alle afbeeldingen overeenkomen met een specifieke pixelgrootte. Met deze optie worden alle productafbeeldingen automatisch aangepast aan de hand van de configuratie-instellingen. Dit kan helpen bij het werken met zoomen, het sneller laden van afbeeldingen en een uniform uiterlijk van de productafbeeldingen behouden.

>[!NOTE]
>
>Voor de beste compatibiliteit wordt aangeraden alle productafbeeldingen te uploaden met het kleurprofiel `sRGB` . Alle andere kleurprofielen worden automatisch omgezet in het `sRGB` -kleurprofiel tijdens het uploaden van de productafbeelding, wat kleurinconsistentie in de geüploade afbeelding kan veroorzaken.

Als u een maximale pixelbreedte en -hoogte instelt, wordt de afbeelding aangepast aan de fysieke afmetingen per pixel. Commerce past de grootte van de afbeelding aan de hogere mate van breedte of hoogte aan, terwijl de verhoudingen behouden blijven. Als u de hoeveelheid kwaliteit voor JPG afbeeldingen verlaagt, wordt het bestand kleiner.

Een afbeeldingsbestand van 3000 x 2100 pixels JPG 100% kan bijvoorbeeld een afbeeldingsbestand van 5 MB of groter zijn. Als u deze afbeelding vergroot of verkleint, neemt de breedte af tot 1920 pixels, blijven de verhoudingen en de kwaliteit tot 80%, zodat het bestand veel kleiner wordt en een hoge kwaliteit heeft.

### Afbeeldingsgrootte inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de _Beelden uploaden de sectie van de Configuratie_.

   Als u de standaardinstellingen wilt wijzigen, schakelt u indien nodig het selectievakje **[!UICONTROL Use system value]** uit.

   ![ Beeld uploadt Configuratie ](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze configuratiemontages, zie [_Beeld uploadt Configuratie_](../configuration-reference/advanced/system.md#image-upload-configuration) in de _Verwijzing van de Configuratie_.

1. Zorg ervoor dat **[!UICONTROL Enable Frontend Resize]** is ingesteld op `Yes` om in te schakelen.

1. Voer een **[!UICONTROL Quality]** -instelling in tussen `1` en `100`%.

   Een instelling tussen 80 en 90% wordt aanbevolen voor bestanden met een lagere bestandsgrootte en een hogere kwaliteit.

1. Stel de **[!UICONTROL Maximum Width]** in pixels in voor de afbeelding.

   Wanneer de grootte van de afbeelding wordt gewijzigd, wordt de breedte niet overschreden en blijven de verhoudingen behouden.

1. Stel de **[!UICONTROL Maximum Height]** in pixels in voor de afbeelding.

   Wanneer de grootte van de afbeelding wordt gewijzigd, wordt deze hoogte niet overschreden en worden de verhoudingen behouden.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Veldomschrijvingen

| Veld | [ Reikwijdte ](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Quality] | Algemeen | Hiermee bepaalt u de JPG-kwaliteit voor de vergrote of verkleinde afbeelding. Bij een lagere kwaliteit wordt het bestand kleiner. 80-90% wordt aanbevolen om bestanden van hoge kwaliteit te verkleinen. Standaard: 80 |
| [!UICONTROL Enable Frontend Resize] | Algemeen | Hiermee kan Commerce de grootte wijzigen van grote, te grote afbeeldingen die u voor de _[!UICONTROL Product Details]_-pagina kunt uploaden. Commerce wijzigt de grootte van de afbeeldingsbestanden met JavaScript wanneer het bestand wordt geüpload. Als de grootte van de afbeelding wordt gewijzigd, blijft de afbeelding exact even groot om aan de maximale breedte of maximale hoogte te voldoen en wordt deze niet groter dan de grootste breedte. Standaard: `Yes` |
| [!UICONTROL Maximum Width] | Algemeen | Hiermee bepaalt u de maximale pixelbreedte voor de afbeelding. Wanneer het formaat van de afbeelding wordt gewijzigd, wordt deze breedte niet overschreden. Standaard: `1920` |
| [!UICONTROL Maximum Height] | Algemeen | Hiermee bepaalt u de maximale pixelhoogte voor de afbeelding. Wanneer het formaat van de afbeelding wordt gewijzigd, wordt deze hoogte niet overschreden. Standaard: `1200` |

{style="table-layout:auto"}

## Plaatsaanduidingen voor afbeeldingen

Adobe Commerce en Magento Open Source gebruiken tijdelijke afbeeldingen als plaatsaanduidingen totdat de permanente productafbeeldingen beschikbaar zijn. Voor elke rol kunt u een andere plaatsaanduiding uploaden. De eerste plaatsaanduidingsafbeelding is een voorbeeldlogo dat u kunt vervangen door de afbeelding van uw keuze.

![ Plaatsaanduiding van het Beeld ](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_om placeholder beelden te uploaden:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ pictogram van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Product Image Placeholders]** sectie.

   ![ Plaatsaanduidingen van het Beeld van het Product ](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze configuratiemontages, zie {Plaatsaanduidingen van het Beeld van 0} Product _[&#128279;](../configuration-reference/catalog/catalog.md#product-image-placeholders)in de_ Verwijzing van de Configuratie _._

1. Klik voor elke afbeeldingsrol op **[!UICONTROL Choose File]** , zoek de afbeelding op uw computer en upload het bestand.

   U kunt dezelfde afbeelding voor alle drie de rollen gebruiken of u kunt een andere plaatsaanduidingsafbeelding voor elke rol uploaden.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

Voor informatie over beeldrollen en geadviseerde grootte, zie [ een beeld ](product-image.md#upload-an-image) uploaden.
