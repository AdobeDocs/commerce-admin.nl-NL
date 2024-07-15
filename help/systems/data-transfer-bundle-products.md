---
title: Bundelproducten importeren
description: Bekijk een voorbeeld van het importeren van productgegevens voor een bundelproduct.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Bundelproducten importeren

Een bundelproduct biedt een selectie van items en biedt klanten de mogelijkheid om de items te kiezen die ze willen kopen. Alle punten die omhoog een bundel maken bestaan in de catalogus als of [ Eenvoudige Producten ](../catalog/product-create-simple.md) of [ Virtuele Producten ](../catalog/product-create-virtual.md). Gewoonlijk worden bundelproducten gemaakt en bijgewerkt via de beheerder. U kunt echter ook gegevens importeren om een bundelproduct te maken of u kunt bestaande bundelproducten exporteren, de gegevens bewerken en weer importeren in de catalogus. De Sprite Yoga Companion Kit is een bundelproduct in de voorbeeldgegevens die in de volgende voorbeelden worden gebruikt.

![ Bundel Product ](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## De volgorde van bundelitems wijzigen

Er zijn twee manieren om de orde van punten in een bundelproduct te veranderen.

### Methode 1: Slepen en neerzetten

Wanneer het werken met a [ Bundel ](../catalog/product-create-bundle.md) product van Admin, kunt u punten en secties in positie slepen en laten vallen.

![ Bundel Punten ](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Methode 2: De productgegevens bewerken

De beste manier om de structuur van een bundelproduct te begrijpen is het product uit te voeren en de gegevens in een spreadsheet te onderzoeken. U kunt de volgorde van bundelitems wijzigen door het product te exporteren en een positieparameter toe te voegen aan de gegevens voor elk item. De itemgegevens staan in de kolom `bundle_values` van het geëxporteerde product. Wanneer de items in een spreadsheet worden geopend, bevinden alle items die aan het product zijn gekoppeld zich in één cel als een lange tekenreeks. De kolom `bundle_values` bevat de volgende elementen voor elk item:

- Naam van de itemsectie
- Invoerbesturingselement
- Vereiste itemindicator
- SKU
- Kleur
- Prijs
- Standaard, optie-indicator
- Standaardhoeveelheid
- Prijssoort
- Indicator voor bewerkbare hoeveelheid

#### Stap 1: Het bundelproduct exporteren

In deze stap, wordt SPRITE Yoga Companion Kit uitgevoerd als a ([ CSV ](data-csv.md) dossier. U kunt elk ander bundelproduct gebruiken dat u in uw catalogus hebt.

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Onder _de Montages van de Uitvoer_, plaats **[!UICONTROL Entity Type]** aan `Products`.

1. Blader in de lijst met productkenmerken omlaag naar **[!UICONTROL SKU]** en voer de SKU in van het bundelproduct dat u wilt exporteren.

   De SKU is `24-WG080` voor het product in dit voorbeeld.

1. Schuif omlaag naar de onderkant van de sectie en klik op **[!UICONTROL Continue]** .

1. Klik in de kolom _[!UICONTROL Action]_van het_[!UICONTROL File name]_ raster op **[!UICONTROL Select]** en kies `Download` .

   Het bestand wordt weergegeven op de downloadlocatie die door de browser wordt gebruikt.

#### Stap 2: De gegevens bewerken

1. Open het gedownloade CSV-bestand in een spreadsheet.

1. Schuif helemaal naar rechts, totdat u de kolom `bundle_values` ziet.

   In de `bundle_values` -gegevens wordt elk element gescheiden door komma&#39;s en wordt elk bundelitem gescheiden van het volgende element met een verticale balk. (Het laatste item eindigt niet met een verticale balk.) De geëxporteerde bundelgegevens moeten er ongeveer als volgt uitzien:

   ![ Bundel Waarden ](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Om het gemakkelijker te maken om uit te geven, kunt u de `bundle_values` gegevens kopiëren, en het kleven in een tekstredacteur, dan, voeg een lijnonderbreking na elk punt toe, zodat is elk punt op een afzonderlijke lijn.

1. Nadat u de gegevens hebt bewerkt, verwijdert u zorgvuldig de regeleinden en plakt u de bewerkte gegevens weer in de kolom `bundle_values` .

   In de volgende afbeelding wordt een parameter `position=[number]` toegevoegd aan elke yoga-riem om de volgorde van de items in de winkellijst te wijzigen.

   ![ Parameter van de Positie ](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. Nadat u de gegevens hebt bewerkt, **[!UICONTROL Save]** het CSV-bestand.

#### Stap 3: het bijgewerkte product importeren

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Stel onder _[!UICONTROL Import Settings]_de waarde **[!UICONTROL Entity Type]**in op `Products` .

1. Stel **[!UICONTROL Import Behavior]** in op `Replace` .

   Met deze optie overschrijft u de vorige gegevens voor het bundelproduct in plaats van uw wijzigingen toe te voegen als extra items.

1. De rol neer aan het _Dossier om_ sectie in te voeren en te klikken **[!UICONTROL Choose File]**.

1. Selecteer het CSV-bestand dat u hebt bewerkt.

1. Klik op **[!UICONTROL Check Data]** en wacht even tot de gegevens zijn gecontroleerd.

1. Klik op **[!UICONTROL Import]** als het bestand geldig is.

1. Wanneer het proces is voltooid, gaat u naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**en klikt u op **[!UICONTROL Flush Cache Storage]**.

   Dit zorgt ervoor dat het bijgewerkte product direct beschikbaar is in de winkel.
