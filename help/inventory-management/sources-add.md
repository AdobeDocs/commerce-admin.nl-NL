---
title: Een inventarisbron toevoegen
description: Leer hoe u een bron voor een locatie maakt, zoals een pakhuis, een baksteen- en mortierwinkel, een distributiecentrum of een verlader.
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Een bron toevoegen

Beheer de inventarisatie en bestelling op meerdere locaties met aangepaste bronnen. Maak een bron voor elke locatie, zoals pakhuizen, baksteen- en mortierwinkels, distributiecentra en verlopende bevrachters. Bronnen toewijzen en hoeveelheden per product bijwerken

Als u de standaardbron bewerkt, kunt u alle configuraties bewerken, behalve de naam en code. Aanbevolen wordt dat single-source-handelaren informatie toevoegen die overeenkomt met hun locatie.

## Een inventarisbron toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Klik op **[!UICONTROL Add New Source]**.

   ![Bronnen beheren](assets/inventory-sources.png)

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL General]** en voer de volgende handelingen uit:

   - Voer een unieke inventarisbron in om de inventarisbron te identificeren **[!UICONTROL Name]**.

   - Voer een unieke waarde in **[!UICONTROL Code]**.

     De code ondersteunt hoofdletters en kleine letters, cijfers, streepjes en onderstrepingstekens. De code is een unieke id die wordt gebruikt bij het toewijzen van gegevens aan voorraad en exporteren.

   - Als deze inventarisbron gebruiksklaar is, stelt u **[!UICONTROL Is Enabled]** tot `Yes`.

   - Voer een korte beschrijving in **[!UICONTROL Description]** voor deze locatie voor snelle informatie of aanvullende informatie.

   - Voor **[!UICONTROL Latitude]** en **[!UICONTROL Longitude]** Voer de GPS-coördinaten (Global Positioning System) van de locatie van de faciliteit in.

     De GPS-coördinaten zoeken met [Google-kaarten][1], typt u het adres in het zoekvak. Klik met de rechtermuisknop op de markering op de kaart en kies **[!UICONTROL What's here?]**. De GPS-coördinaten worden weergegeven in het detailvak onder het adres van de straat.

     ![Algemene bronopties](assets/inventory-source-general.png)

   - Als deze inventarisbron een ophaallocatie is, stelt u **[!UICONTROL Use as Pickup Location]** tot `Yes`.

     De standaardbron kan niet worden gebruikt als ophaallocatie voor ophaalorders in de winkel.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Contact Info]** en voer de volgende handelingen uit:

   - Voor **[!UICONTROL Contact Name]**, voert u de volledige naam van de primaire contactpersoon op de locatie in.

   - Voer een **[!UICONTROL Email]** adres voor het contacteren van de plaats.

   - Voor **[!UICONTROL Phone]**, voert u de gebiedscode en het telefoonnummer in.

   - Voor **[!UICONTROL Fax]**, voert u de netnummer en het telefoonnummer van de fax in, indien beschikbaar.

     ![Contactinfo](assets/inventory-source-contact-info.png)

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Address Data]** en voer de volgende handelingen uit:

   - Kies de optie **[!UICONTROL Country]**.

   - Voor **[!UICONTROL State/Province]** Voer de standaardafkorting voor de provincie in.

   - Voer de **[!UICONTROL City]**.

   - Voer de fysieke waarde in **[!UICONTROL Street]** adres.

   - Voor **[!UICONTROL Postcode]** Voer de postcode in.

     ![Adresgegevens](assets/inventory-source-address.png)

1. Als u de bron instelt als een ophaallocatie in de eerdere stap, vouwt u ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Pickup Location]** en geef een beschrijving van de locatie:

   - Voer de **[!UICONTROL Frontend Name]** van de oppiklocatie.

   - Voer een **[!UICONTROL Frontend Description]** van de oppiklocatie. In dit tekstvak kunt u winkeluren, de locatie ten opzichte van andere markeringen of andere nuttige informatie weergeven waarmee de klant de juiste locatie voor het ophalen kan selecteren.

     ![Ophaallocatie](assets/inventory-pickup-location.png)

   Voor meer informatie over hoe te om e-mailberichten te vormen wanneer het gebruiken van een bron als bestelplaats, zie [Verkoop-e-mails](../configuration-reference/sales/sales-emails.md) in de _Referentiehandleiding voor configuratie_.

1. Voer een van de volgende handelingen uit om uw werk op te slaan:

   - Als u uw werk wilt opslaan en wilt doorgaan met bewerken, klikt u op **[!UICONTROL Save & Continue]**.

   - Als u uw werk wilt opslaan en wilt terugkeren naar de pagina Bronnen beheren, klikt u op de pijl omlaag (![Menupijl](../assets/icon-menu-down-arrow-red.png)) en kiest u **[!UICONTROL Save & Close]**.

   - Als u uw werk op de huidige bronrecord wilt opslaan en een nieuwe bron wilt invoeren, kiest u **[!UICONTROL Save & New]**.

## Knopbalk

| Knop | Beschrijving |
|--|--|
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Bronnen beheren. |
| [!UICONTROL Reset] | Hiermee herstelt u de waarden van alle velden in het formulier op het moment van de laatste keer opslaan. |
| [!UICONTROL Save & Continue] | Hiermee slaat u alle wijzigingen op en opent u het formulier voor verdere bewerking. Klik op de pijl-omlaag voor extra opties:<br/>**[!UICONTROL Save & Close]**- Hiermee slaat u wijzigingen op in de huidige record, sluit u het formulier en keert u terug naar de pagina Bronnen beheren.<br/>**[!UICONTROL Save & New]** - Hiermee slaat u wijzigingen op, sluit u de huidige record en opent u een nieuw, leeg formulier. |

## Veldomschrijvingen

| Veld | Beschrijving |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | (Vereist) Een unieke naam die de inventarisbron voor Admin-gebruikers identificeert. |
| [!UICONTROL Code] | (Vereist) Een unieke alfanumerieke code die door het systeem wordt gebruikt om de inventarisbron te identificeren. Voer de code in hoofdletters of kleine letters en/of cijfers in, zonder spaties. Indien nodig kunt u een afbreekstreepje of onderstrepingsteken gebruiken in plaats van een spatie. De code kan na het maken van de bron niet worden bewerkt. Dit is een unieke id die u gebruikt wanneer u bronnen toewijst aan voorraden en productgegevens exporteert en/of importeert. |
| [!UICONTROL Is Enabled] | Hiermee wordt bepaald of de inventarisbron beschikbaar is voor gebruik. Opties: Ja/Nee |
| [!UICONTROL Description] | Een korte beschrijving van de locatie van de inventarisbron. Neem details op die nuttig zijn voor uw Admin-gebruikers. |
| [!UICONTROL Latitude] | Hiermee geeft u de breedtecoördinaat van de inventarisbron voor GPS op. Voer de waarde in als een getal, voorafgegaan door een plusteken of minteken. Het gradensymbool en de letters zijn niet toegestaan. Bijvoorbeeld: Latitude 32.7555 |
| [!UICONTROL Longitude] | Hiermee geeft u de lengtecoördinaat van de inventarisbron voor GPS op. Voer de waarde in als een getal, voorafgegaan door een plusteken of minteken. Het gradensymbool en de letters zijn niet toegestaan. Bijvoorbeeld: `-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | De naam van de primaire contactpersoon op de locatie van de inventarisbron. |
| [!UICONTROL Email] | De e-mail van de primaire contactpersoon. |
| [!UICONTROL Phone] | De netnummer en het telefoonnummer van de primaire contactpersoon, in de gewenste indeling. Bijvoorbeeld: `(123) 456-7890` of `123-456-7890` |
| [!UICONTROL Fax] | De netnummer en het faxnummer van de primaire contactpersoon. |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | (Vereist) Het land waar de inventarisbron zich bevindt. |
| [!UICONTROL State/Province] | De staat of provincie waar de bron van de inventaris zich bevindt. |
| [!UICONTROL City] | De plaats waar de inventarisbron zich bevindt. |
| [!UICONTROL Street] | Het adres van de straat van de inventarisbron. |
| [!UICONTROL Postcode] | (Vereist) De postcode of postcode van de inventarisbron. |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | De naam van de oppiklocatie voor de bron die in de winkel wordt weergegeven. |
| [!UICONTROL Frontend Description] | De beschrijving van de oppiklocatie voor de bron die in de winkel wordt weergegeven. Het kan gekoppelde afbeeldingen bevatten. |

[1]: https://www.google.com/maps
