---
title: Klantsegmenten maken en verwijderen
description: Klanten kunnen de restitutiegegevens die aan de bestelling zijn gekoppeld, bekijken in het dashboard voor hun klantenaccount.
exl-id: 8a13271d-d0b5-4fc6-a701-3edfae04bfca
feature: Customers, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Klantsegmenten maken en verwijderen

{{ee-feature}}

Creërend een klantensegment is gelijkaardig aan de bouw van de regel van de a [ kartprijs ](../merchandising-promotions/price-rules-cart.md), behalve dat omvatten de opties [ klant segment-specifieke attributen ](../customers/customer-segments.md).

![ de segmentlijst van de Klant ](assets/customer-segments.png){width="700" zoomable="yes"}

_&#x200B;**[!UICONTROL Customer Segments]grid &#x200B;** _

| Kolom | Beschrijving |
|--- |--- |
| **[!UICONTROL ID]** | De unieke id van het klantsegment. |
| **[!UICONTROL Segment]** | De naam van het klantensegment. |
| **[!UICONTROL Status]** | Geeft aan of het klantsegment _[!UICONTROL Active]_&#x200B;of&#x200B;_[!UICONTROL Inactive]_ is. |
| **[!UICONTROL Website]** | Geeft de website aan waartoe het klantensegment behoort. |

{style="table-layout:auto"}

## Vereiste: klantsegmenten inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Customer Segments]** uit.

1. Controleer of **[!UICONTROL Enable Customer Segment Functionality]** is ingesteld op `Yes` .

   ![ configuratie van Klanten - klantensegmenten ](../configuration-reference/customers/assets/customer-configuration-customer-segments.png){width="600" zoomable="yes"}

1. (Optioneel) Als u realtime validatie voor klantsegmenten wilt uitschakelen, stelt u **[!UICONTROL Real-time Check if Customer is Matched by Segment]** in op `No` .

   Wanneer u bevestiging in real time onbruikbaar maakt, worden de klantensegmenten bevestigd door één enkele gecombineerde voorwaardeSQL vraag. Als u deze functie uitschakelt, verbetert u de prestaties van de segmentvalidatie als er veel klantensegmenten in het systeem zijn. De validatie werkt echter niet met een gesplitste database of wanneer er geen geregistreerde klanten zijn.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Een segment maken

De volgende stappen gebruiken een voorbeeld voor het creëren van een klantensegment dat vrouwelijke klanten in Los Angeles richt.

### Stap 1: Voeg een klantensegment toe

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Segment]** .

1. Voer een **[!UICONTROL Segment Name]** in die het klantsegment identificeert wanneer u in Admin werkt.

1. Voer een korte **[!UICONTROL Description]** in die het doel van het segment aangeeft.

1. Stel **[!UICONTROL Assigned to Website]** in op de website waar het klantsegment kan worden gebruikt.

1. Plaats **[!UICONTROL Status]** aan _Actief_ of _Inactief_.

1. Stel **[!UICONTROL Apply to]** in op een van de volgende opties om de klanttypen te identificeren die u wilt gebruiken voor het toepassen van het segment:

   - `Visitors and Registered Customers` - Bevat alle kopers, ongeacht of ze zijn aangemeld bij een account.
   - `Registered Customers` - Omvat alleen kopers die zijn aangemeld bij een account.
   - `Visitors` - Omvat alleen kopers die niet zijn aangemeld bij een account.

   >[!TIP]
   >
   >Als u een segment creeert dat op klantenattributen wordt gebaseerd die in een klantenrekening worden opgeslagen, is het beste praktijken om het segment op geregistreerde klanten slechts toe te passen.

   >[!NOTE]
   >
   > Als een segment van toepassing is op `Visitors and Registered Customers` , geeft [!UICONTROL Matched Customers] alleen `Registered Customers` weer. Dit is zelfs het geval als bezoekers zich kunnen richten op basis van voorwaarden die op hen van toepassing zijn. Voor `Visitors` alleen segmenten wordt geen tab `Matched Customers` weergegeven.


1. Klik op **[!UICONTROL Save and Continue Edit]**.

   Nadat u het segment hebt opgeslagen _[!UICONTROL General Properties]_, worden aanvullende opties beschikbaar in het linkerdeelvenster.

   ![ eigenschappen van het Segment ](assets/customer-segment-saved.png){width="600" zoomable="yes"}

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


1. Klik in het linkerdeelvenster op **[!UICONTROL Conditions]** .

   De standaardvoorwaarde begint met _[!UICONTROL If ALL of these conditions are TRUE:]_&#x200B;op de pagina.

   ![ Voorwaarden ](assets/customer-segment-conditions.png){width="600" zoomable="yes"}

1. Maak een voorwaarde die gericht is op vrouwelijke klanten:

   - Klik op het pictogram **[!UICONTROL Add]** om de lijst met voorwaarden weer te geven en selecteer `Gender` .

   - Verlaat het gebrek **is** optie van de voorwaardencontrole.

   - Klik op **...** en selecteer `female` .

   ![ lijn 1 van de Voorwaarde 1 ](assets/customer-segment-condition-line1.png){width="600" zoomable="yes"}

1. Maak een andere voorwaarde die geldt voor inwoners van Los Angeles:

   - Klik op de volgende regel op het pictogram **[!UICONTROL Add]** en selecteer `Customer Address` .

     Met deze actie maakt u een bovenliggende voorwaarde waarin u een of meer adresvelden kunt definiëren die moeten overeenkomen.

   - Klik op het pictogram **[!UICONTROL Add]** om de lijst met adresvelden weer te geven en selecteer `City` .

   - Klik **is** om de opties van de voorwaardencontrole te tonen en te selecteren `contains`.

   - Klik op **...** en voer `Los Angeles` in.

   - Klik op de volgende regel op het pictogram **[!UICONTROL Add]** en selecteer `State/Province` .

   - Verlaat het gebrek **is** optie van de voorwaardencontrole.

   - Klik op **...** en selecteer `United States > California` .

   ![ Voorwaarden voor vrouwtjes in Los Angeles, Californië ](assets/customer-segment-conditions-la-ladies.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

### Stap 3: Herzie de lijst van aangepaste klanten

1. Klik in het linkerdeelvenster op **[!UICONTROL Matched Customers]** om alle klanten weer te geven die aan de voorwaarde voldoen.

   ![ Gelijke klanten ](assets/customer-segment-matched-customers.png){width="600" zoomable="yes"}

1. Als de lijst met klanten aan uw doel voldoet, klikt u op **[!UICONTROL Save]** om het klantsegment te voltooien.

1. Het klantensegment kan nu voor het richten van bevorderingen, inhoud, en postings worden gebruikt.

_&#x200B;**[!UICONTROL Matched Customers]grid &#x200B;** _

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

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Zoek het segment dat u wilt verwijderen en selecteer het.

1. Klik in de menubalk op de knop **[!UICONTROL Delete]** .

1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

## Knopbalk

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Hiermee gaat u terug naar de _[!UICONTROL Customer Segments]_-pagina zonder wijzigingen op te slaan. |
| **[!UICONTROL Delete]** | Verwijdert het huidige klantensegment. De klanten of voltooide orden verbonden aan de klant in het segment worden niet verwijderd. |
| **[!UICONTROL Reset]** | Herstelt om het even welke niet bewaarde veranderingen in het vorm van het klantensegment aan hun vorige waarden. |
| **[!UICONTROL Refresh Segment Data]** | Hiermee vernieuwt u de segmentgegevens naar de laatst opgeslagen waarden. Relevant als om het even welke segmentgegevens niet beschikbaar of verouderd zijn. |
| **[!UICONTROL Save and Continue Edit]** | Slaat veranderingen op en houdt het klantensegment open. |
| **[!UICONTROL Save]** | Slaat veranderingen op en sluit het klantensegment. |

{style="table-layout:auto"}

## Demo voor klantsegmenten

Bekijk deze video voor een demonstratie van het creëren van klantensegmenten:

>[!VIDEO](https://video.tv.adobe.com/v/343659/?quality=12&learn=on)
