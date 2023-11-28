---
title: Productstalen
description: Leer hoe u stalen definieert voor uw configureerbare productaanbiedingen.
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Productstalen

Klanten hebben hoge verwachtingen bij het kiezen van een kleur en het is van cruciaal belang dat productbeschrijvingen elke beschikbare kleur, patroon of structuur nauwkeurig weergeven. De broek in het volgende voorbeeld is bijvoorbeeld niet beschikbaar in rood, groen en blauw. Ze zijn alleen beschikbaar in bepaalde soorten rood, groen en blauw, die waarschijnlijk uniek zijn voor dit product.

![Stalen op een productpagina](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

Voor [configureerbare producten](product-create-configurable.md), kan de kleur worden aangegeven door een visuele staal, een tekststaal of een invoerbesturingselement. Stalen kunnen worden gebruikt op de productpagina, in productaanbiedingen en in [gelaagde navigatie](navigation-layered.md). Op de productpagina worden stalen gesynchroniseerd om de bijbehorende productafbeelding weer te geven wanneer het staal wordt geselecteerd. Wanneer de klant het staal selecteert, wordt de corresponderende waarde weergegeven in het invoerveld en wordt het staal omgeven door de huidige selectie.

>[!NOTE]
>
>Staalkenmerken kunnen worden geconfigureerd om geen overeenkomende eenvoudige productafbeeldingen weer te geven wanneer het staal wordt geselecteerd door het instellen van de optie _[!UICONTROL Update Product Preview Image]_optiewaarde voor `No` op de [!UICONTROL Attribute Edit] in Admin.

## Op tekst gebaseerde stalen

Als een afbeelding niet beschikbaar is voor een staal, wordt de kenmerkwaarde weergegeven als tekst. Een op tekst gebaseerd staal is vergelijkbaar met een knop met een tekstlabel en gedraagt zich op dezelfde manier als een staal met een afbeelding. Als op tekst gebaseerde stalen worden gebruikt om de beschikbare formaten weer te geven, wordt de grootte die niet beschikbaar is, doorgehaald.

![Tekstgebaseerde selectie van stalen geeft een groter formaat weer](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## Stalen in gelaagde navigatie

Stalen kunnen ook worden gebruikt in gelaagde navigatie, als de _[!UICONTROL Use in Layered Navigation]_eigenschap van het kenmerk color is ingesteld op `Yes`. In het volgende voorbeeld ziet u zowel tekststalen als kleurafbeeldingsstalen in gelaagde navigatie.

![Stalen in weergave bij gelaagde navigatie](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## Stalen maken voor producten

Stalen kunnen worden gedefinieerd als een onderdeel van het dialoogvenster `color` kenmerk of lokaal instellen voor een specifiek product en geüpload als [productafbeeldingen](product-image.md#upload-an-image).

In de eerdere voorbeelden zijn de &quot;Sylvia Capri&quot;-broek beschikbaar in specifieke waarden van `red`, `green`, en `blue`. Omdat de stalen uit de afbeelding van het product zijn genomen, is elk een werkelijke weergave van de kleur. De `color` wordt gebruikt om de informatie voor alle productkleuren en stalen te beheren.

### Stap 1: De stalen maken

Gebruik een van de volgende methoden om stalen voor uw producten te maken.

#### Methode 1: Een kleurstaal toevoegen

1. Als u de ware kleur van een product wilt vastleggen, opent u de afbeelding in een foto-editor en gebruikt u het pipet om de exacte kleur te bepalen en noteert u de equivalente hexadecimale waarde.

   ![Hexadecimale kleurwaarden](./assets/swatch-hex-values.png){width="400"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Open in het raster de _kleur_ kenmerk in bewerkingsmodus.

1. Controleren of **[!UICONTROL Catalog Input Type for Store Owner]** is ingesteld op `Visual Swatch`.

1. Als u liever geen overeenkomende eenvoudige productafbeeldingen weergeeft wanneer het staal op de productweergavepagina is geselecteerd, stelt u **[!UICONTROL Update Product Preview Image]** tot `No`.

1. Onder _[!UICONTROL Manage Swatch (Values of Your Attribute)]_, klikt u op **[!UICONTROL Add Swatch]**en voer de volgende handelingen uit:

   ![Staalwaarden beheren](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - In de _Staal_ , klikt u op het nieuwe staal en selecteert u **[!UICONTROL Choose a color]** in het menu.

     ![Een staalkleur kiezen](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - Plaats de cursor in de kleurkiezer **Aantal** , verwijdert u de huidige waarde en voert u de hexadecimale waarde in van zes tekens van de nieuwe kleur.

     ![Voer de hexadecimale waarde in](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - Als u het staal wilt opslaan, klikt u op de knop _Kleurenwiel_ ( ![Kleurpictogram](../assets/icon-color-wheel.png) ) in de rechterbenedenhoek van de kleurkiezer.

   - In de _Beheerder_ Voer een label in om de kleur aan de beheerder van de winkel te beschrijven.

     Indien van toepassing kunt u ook de vertaling van de kleur voor elke ondersteunde taal invoeren. In het volgende voorbeeld wordt de SKU ter referentie opgenomen in het dialoogvenster _Beheerder_ -label omdat de kleuren alleen voor een bepaald product worden gebruikt. U kunt wel een spatie of onderstrepingsteken in het label opnemen, maar geen afbreekstreepje.

   - In de _Is standaard_ selecteert u het staal dat de standaardoptie moet zijn.

   - Als u de volgorde van de kleurstalen wilt wijzigen, klikt u op de knop _[!UICONTROL Order]_![Pictogram Sorteervolgorde](../assets/icon-sort-order.png) en sleep het item naar een nieuwe positie in de lijst.

     ![Staallabels](./assets/attribute-swatch-labels.png){width="400"}

1. Klik op **[!UICONTROL Save Attribute]** en vernieuw de cache wanneer hierom wordt gevraagd.

1. Elk product openen in de bewerkingsmodus en de **Kleur** met het juiste staal.

   Volg onderstaande stappen om meerdere producten tegelijk bij te werken.

#### Methode 2: Een staalafbeelding uploaden

1. Als u een afbeelding voor een staal wilt vastleggen, opent u de productafbeelding in een fotoeditor en slaat u een vierkant gebied van de afbeelding op waarin de kleur, het patroon of de structuur worden weergegeven.

   Indien nodig, kunt u deze actie voor elke variatie van het product herhalen.

   De grootte en afmetingen van het staal worden bepaald door het thema. In het algemeen kunt u de hoogte-breedteverhouding van een patroon behouden door een afbeelding op te slaan als een vierkant.

   ![Staalafbeeldingen](./assets/swatch-samples.png){width="400"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Open in het raster de **[!UICONTROL color]** kenmerk in bewerkingsmodus.

1. Controleren of **[!UICONTROL Catalog Input Type for Store Owner]** is ingesteld op `Visual Swatch`.

1. Als u liever geen overeenkomende eenvoudige productafbeeldingen weergeeft wanneer het staal op de productweergavepagina is geselecteerd, stelt u **[!UICONTROL Update Product Preview Image]** tot `No`.

1. Onder _[!UICONTROL Manage Swatch]_(waarden van het kenmerk) klikt u op **[!UICONTROL Add Swatch]**en voer de volgende handelingen uit:

   - In de _[!UICONTROL Swatch]_Klik op het nieuwe staal om het menu weer te geven en kies **[!UICONTROL Upload a file]**.

   - Navigeer naar het staalbestand dat u hebt voorbereid en kies het bestand dat u wilt uploaden.

   - Herhaal deze stappen voor elke staalafbeelding.

   - Voer de labels in voor de Beheer en de winkel.

     In dit voorbeeld is de SKU ter referentie opgenomen in het label Admin, omdat deze kleuren alleen voor een specifiek product worden gebruikt. U kunt een spatie of onderstrepingsteken in het label opnemen, maar u kunt geen afbreekstreepje opnemen.

     ![Labels invoeren](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. Klik op **[!UICONTROL Save Attribute]** en vernieuw de cache wanneer hierom wordt gevraagd.

1. Elk product openen in de bewerkingsmodus en de **[!UICONTROL Color]** met het juiste staal.

   Volg onderstaande stappen om meerdere producten tegelijk bij te werken.

### Stap 2: De producten bijwerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Gebruik de **[!UICONTROL Filter]** om de lijst op naam of SKU weer te geven en alleen de toepasselijke producten op te nemen.

1. Schakel in het raster het selectievakje in van elk product waarop het staal van toepassing is.

1. Set **[!UICONTROL Actions]** tot `Update Attributes`.

   In dit voorbeeld worden alle blauwe configuraties van de broek geselecteerd.

   ![Productstaalkenmerken bijwerken](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. Omlaag schuiven naar de **[!UICONTROL Color]** en selecteer de **[!UICONTROL Change]** selectievakje.

   ![Selectievakje wijzigen](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. Kies het staal dat van toepassing is op de geselecteerde producten en klik op **[!UICONTROL Save]**.

1. Vernieuw de cache wanneer daarom wordt gevraagd.

   ![Staal in weergegeven in de winkel](./assets/swatch-blue-schmear.png){width="200"}

## Stalen toevoegen aan een eenvoudig product

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in bewerkingsmodus, controleer de productstatus (moet zijn ingeschakeld).

1. Klikken **[!UICONTROL Create Configurations]** knop (onder de `Configurations` ).

1. Kies in het pop-upvenster het kenmerk Kleur en **[!UICONTROL Next]**.

1. Selecteer kleurstalen in het kenmerk dat u in dit product wilt opnemen.

1. Klik op de voortgangsbalk op **[!UICONTROL Next]**.

1. [De afbeeldingen, prijs en hoeveelheid configureren](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   Voor deze stap, plaats de beelden, de tarifering, en de hoeveelheid van elke configuratie. De beschikbare opties zijn voor elke optie gelijk en u kunt slechts één optie kiezen. U kunt het zelfde plaatsen op alle SKUs toepassen, een uniek plaatsen op elke SKU toepassen, of de montages voor nu overslaan.

1. Wanneer de configuratie voor afbeeldingen, prijs en hoeveelheid is voltooid, klikt u op **[!UICONTROL Next]** in de rechterbovenhoek.

   De huidige productvariaties verschijnen bij de bodem van de sectie van de Configuratie. Als u tevreden bent met de configuraties, klikt u op **[!UICONTROL Generate Products]**.
