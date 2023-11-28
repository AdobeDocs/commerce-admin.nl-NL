---
title: Klantsegmenten maken en verwijderen
description: Klanten kunnen de restitutiegegevens die aan de bestelling zijn gekoppeld, bekijken in het dashboard voor hun klantenaccount.
exl-id: 8a13271d-d0b5-4fc6-a701-3edfae04bfca
feature: Customers, Configuration
source-git-commit: 8d5cd6fa586feb5e44819755245814bff7678d34
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 0%

---

# Klantsegmenten maken en verwijderen

{{ee-feature}}

Het creëren van een klantensegment is gelijkaardig aan het bouwen van een [kartonnen prijsregel](../merchandising-promotions/price-rules-cart.md), behalve dat de opties onder andere [klantspecifieke segmentkenmerken](../customers/customer-segments.md).

![Lijst met klantsegmenten](assets/customer-segments.png){width="700" zoomable="yes"}

_**[!UICONTROL Customer Segments]raster **_

| Kolom | Beschrijving |
|--- |--- |
| **[!UICONTROL ID]** | De unieke id van het klantsegment. |
| **[!UICONTROL Segment]** | De naam van het klantensegment. |
| **[!UICONTROL Status]** | Geeft aan of het klantsegment _[!UICONTROL Active]_of_[!UICONTROL Inactive]_. |
| **[!UICONTROL Website]** | Geeft de website aan waartoe het klantensegment behoort. |

{style="table-layout:auto"}

## Vereiste: klantsegmenten inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Vouw de sectie **[!UICONTROL Customer Segments]** uit.

1. Controleren of **[!UICONTROL Enable Customer Segment Functionality]** is ingesteld op `Yes`.

   ![Configuratie van klanten - klantsegmenten](../configuration-reference/customers/assets/customer-configuration-customer-segments.png){width="600" zoomable="yes"}

1. (Optioneel) Als u realtime validatie voor klantsegmenten wilt uitschakelen, stelt u **[!UICONTROL Real-time Check if Customer is Matched by Segment]** tot `No`.

   Wanneer u bevestiging in real time onbruikbaar maakt, worden de klantensegmenten bevestigd door één enkele gecombineerde voorwaardeSQL vraag. Als u deze functie uitschakelt, verbetert u de prestaties van de segmentvalidatie als er veel klantensegmenten in het systeem zijn. De validatie werkt echter niet met een gesplitste database of wanneer er geen geregistreerde klanten zijn.

1. Klik op **[!UICONTROL Save Config]**.

## Een segment maken

De volgende stappen gebruiken een voorbeeld voor het creëren van een klantensegment dat vrouwelijke klanten in Los Angeles richt.

### Stap 1: Voeg een klantensegment toe

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Segment]**.

1. Voer een **[!UICONTROL Segment Name]** die het klantensegment identificeert wanneer het werken in Admin.

1. Voer een korte beschrijving in **[!UICONTROL Description]** dit verklaart het doel van het segment .

1. Set **[!UICONTROL Assigned to Website]** naar de website waar het klantensegment kan worden gebruikt.

1. Stel de **[!UICONTROL Status]** tot _Actief_ of _Inactief_.

1. Om de klantentypes te identificeren die u voor het toepassen van het segment wilt gebruiken, plaats **[!UICONTROL Apply to]** op een van de volgende wijzen:

   - `Visitors and Registered Customers` - Bevat alle kopers, ongeacht of ze zijn aangemeld bij een account.
   - `Registered Customers` - Omvat alleen kopers die zijn aangemeld bij een account.
   - `Visitors` - Omvat alleen kopers die niet zijn aangemeld bij een account.

   >[!TIP]
   >
   >Als u een segment creeert dat op klantenattributen wordt gebaseerd die in een klantenrekening worden opgeslagen, is het beste praktijken om het segment op geregistreerde klanten slechts toe te passen.

   >[!NOTE]
   >
   > Als een segment van toepassing is op `Visitors and Registered Customers`de [!UICONTROL Matched Customers] alleen weergeeft `Registered Customers`. Dit is zelfs het geval als bezoekers zich kunnen richten op basis van voorwaarden die op hen van toepassing zijn. Voor `Visitors` alleen segmenten, geen `Matched Customers` wordt weergegeven.


1. Klik op **[!UICONTROL Save and Continue Edit]**.

   Na het opslaan van het segment _[!UICONTROL General Properties]_extra opties beschikbaar in het linkerdeelvenster.

   ![Segmenteigenschappen](assets/customer-segment-saved.png){width="600" zoomable="yes"}

**_[!UICONTROL General Properties]_**

| Veld | Beschrijving |
|--- |---|
| **[!UICONTROL Segment Name]** | Een naam die het segment voor interne verwijzing identificeert. |
| **[!UICONTROL Description]** | Een korte beschrijving die het doel van het segment voor interne verwijzing verklaart. |
| **[!UICONTROL Assigned to Website]** | De enige website waarop het segment kan worden gebruikt. |
| **[!UICONTROL Status]** | Hiermee activeert en deactiveert u het segment. Eventuele prijsregels en -banners worden gedeactiveerd wanneer het segment wordt uitgeschakeld. Opties: `Active` / `Inactive` |
| **[!UICONTROL Apply to]** | Bepaalt de klantentypes waarop het segment wordt toegepast. De selectie beïnvloedt de set voorwaarden die beschikbaar zijn voor het maken van het segment. De instelling kan niet worden gewijzigd nadat het segment is opgeslagen. |

{style="table-layout:auto"}

### Stap 2: De voorwaarden definiëren

>[!NOTE]
>
> Voor bezoekers zijn alleen de volgende voorwaarden van toepassing: Winkelwagentvoorwaarden (aantal winkelwagentjes, aantal winkelwagentjes, aantal winkelwagentjes en aantal winkelwagentjes), productregels (producten in winkelwagentje en productgeschiedenis) en combinaties van deze artikelen. Als een segment zowel voor bezoekers als voor geregistreerde klanten geldt, worden de bezoekers alleen bijgehouden op basis van de vermelde voorwaarden.


1. Klik in het linkerdeelvenster op **[!UICONTROL Conditions]**.

   De standaardvoorwaarde begint met _[!UICONTROL If ALL of these conditions are TRUE:]_op de pagina.

   ![Voorwaarden](assets/customer-segment-conditions.png){width="600" zoomable="yes"}

1. Maak een voorwaarde die gericht is op vrouwelijke klanten:

   - Klik op de knop **[!UICONTROL Add]** pictogram om de lijst met voorwaarden weer te geven en `Gender`.

   - De standaardinstelling behouden **is** Voorwaardelijke beheeroptie.

   - Klikken **...** en selecteert u `female`.

   ![Voorwaardelijke regel 1](assets/customer-segment-condition-line1.png){width="600" zoomable="yes"}

1. Maak een andere voorwaarde die geldt voor inwoners van Los Angeles:

   - Klik op de volgende regel op de knop **[!UICONTROL Add]** pictogram en selecteer `Customer Address`.

     Met deze actie maakt u een bovenliggende voorwaarde waarin u een of meer adresvelden kunt definiëren die moeten overeenkomen.

   - Klik op de knop **[!UICONTROL Add]** pictogram om de lijst met adresvelden weer te geven en selecteer `City`.

   - Klikken **is** om de opties voor voorwaardenbeheer weer te geven en `contains`.

   - Klikken **...** en betreden `Los Angeles`.

   - Klik op de volgende regel op de knop **[!UICONTROL Add]** pictogram en selecteer `State/Province`.

   - De standaardinstelling behouden **is** Voorwaardelijke beheeroptie.

   - Klikken **...** en selecteert u `United States > California`.

   ![Voorwaarden voor vrouwen in Los Angeles, Californië](assets/customer-segment-conditions-la-ladies.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

### Stap 3: Herzie de lijst van aangepaste klanten

1. Klik in het linkerdeelvenster op **[!UICONTROL Matched Customers]** om alle klanten weer te geven die aan de voorwaarde voldoen.

   ![Overeenkomende klanten](assets/customer-segment-matched-customers.png){width="600" zoomable="yes"}

1. Als de lijst van klanten uw doel ontmoet, klik **[!UICONTROL Save]** om het klantensegment te voltooien.

1. Het klantensegment kan nu voor het richten van bevorderingen, inhoud, en postings worden gebruikt.

_**[!UICONTROL Matched Customers]raster **_

| Kolom | Beschrijving |
|--- |--- |
| **[!UICONTROL ID]** | De klant-id van een geregistreerde klant. |
| **[!UICONTROL Name]** | De naam van een geregistreerde klant. |
| **[!UICONTROL Email]** | Het e-mailadres van een geregistreerde klant. |
| **[!UICONTROL Group]** | De klantengroep waaraan de klant wordt toegewezen. |
| **[!UICONTROL Phone]** | Het telefoonnummer van de klant. |
| **[!UICONTROL ZIP]** | De postcode of postcode van de klant. |
| **[!UICONTROL Country]** | Het land waar de klant zich bevindt. |
| **[!UICONTROL State / Province]** | De staat of provincie waar de klant zich bevindt. |
| **[!UICONTROL Customer Since]** | De datum en tijd waarop de klantenaccount is gemaakt. |

{style="table-layout:auto"}

## Een klantsegment verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Zoek het segment dat u wilt verwijderen en selecteer het.

1. Klik in de menubalk op **[!UICONTROL Delete]** knop.

1. Klik op **[!UICONTROL OK]**.

## Knopbalk

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Hiermee wordt de _[!UICONTROL Customer Segments]_pagina zonder wijzigingen op te slaan. |
| **[!UICONTROL Delete]** | Verwijdert het huidige klantensegment. De klanten of voltooide orden verbonden aan de klant in het segment worden niet verwijderd. |
| **[!UICONTROL Reset]** | Herstelt om het even welke niet bewaarde veranderingen in het vorm van het klantensegment aan hun vorige waarden. |
| **[!UICONTROL Refresh Segment Data]** | Hiermee vernieuwt u de segmentgegevens naar de laatst opgeslagen waarden. Relevant als om het even welke segmentgegevens niet beschikbaar of verouderd zijn. |
| **[!UICONTROL Save and Continue Edit]** | Slaat veranderingen op en houdt het klantensegment open. |
| **[!UICONTROL Save]** | Slaat veranderingen op en sluit het klantensegment. |

{style="table-layout:auto"}

## Demo voor klantsegmenten

Bekijk deze video voor een demonstratie van het creëren van klantensegmenten:

>[!VIDEO](https://video.tv.adobe.com/v/343659/?quality=12)
