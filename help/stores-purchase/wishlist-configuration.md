---
title: Wenslijsten configureren
description: Leer hoe u functionaliteit voor wensenlijsten kunt configureren voor klanten in uw winkel.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Wenslijsten configureren

De configuratie van de wensenlijst laat wensen lijsten toe en bepaalt het e-mailmalplaatje en de afzender van e-mailberichten die worden gebruikt wanneer een verlanglijst wordt gedeeld.

## Functionaliteit voor wensenlijst inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Wish List]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL General Options]** en voer de volgende handelingen uit:

   ![Configuratie van klanten - algemene instellingen voor verlanglijstbeheer](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Schakelen **[!UICONTROL Enabled]** tot `Yes`, die de module van de verlanglijst voor de opslag activeert.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) In-/uitschakelen **[!UICONTROL Enable Multiple Wish Lists]** tot `Yes`, waardoor klanten meerdere verlanglijsten kunnen maken en onderhouden.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Als u het aantal wenslijsten wilt beperken dat klanten aan hun account kunnen koppelen, voert u een waarde in voor **[!UICONTROL Number of Multiple Wish Lists]**.

   - Schakelen **[!UICONTROL Show in Sidebar]** tot `Yes`, die de verlanglijsten in de zijbalk weergeeft.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Share Options]** en voer de volgende handelingen uit:

   ![Configuratie van klanten - opties voor het delen van wensenlijsten](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Stel de **[!UICONTROL Email Sender]** aan het opslagcontact dat als afzender van het bericht zou moeten verschijnen. Opties: Algemene contactpersoon, Verkoper, Klantenondersteuning, Aangepaste e-mail.

   - Stel de **[!UICONTROL Email Template]** te gebruiken wanneer een klant een verlanglijst deelt.

   - Als u het totale aantal e-mailberichten dat een klant kan verzenden wilt beperken, voert u een **[!UICONTROL Max Emails Allowed to be Sent]** waarde. De standaardwaarde is 10 en het toegestane maximum is 10.000.

   - Voer een waarde in voor **[!UICONTROL Email Text Length Limit]**. De standaardwaarde is 255.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL My Wish List Link]** sectie en set **[!UICONTROL Display Wish List Summary]** op een van de volgende wijzen:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configuratie van klanten - weergave van wensenlijsten](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Zoekopdracht voor wensenlijst toevoegen

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

Een openbare lijst met wensen kunt u vinden met de zoekopdracht in de lijst met wensen [widget](../content-design/widgets.md). Met de widget kan een klant zoeken op de naam of het e-mailadres van de eigenaar van de wenslijst. Winkelklanten kunnen wensenlijsten vinden die bij andere klanten horen, hen bekijken en producten van hen bestellen, of de producten toevoegen aan hun eigen wensen lijsten. Als een object door een andere klant van een openbare verlanglijst wordt gekocht, wordt het niet uit de oorspronkelijke verlanglijst verwijderd. De _Zoekopdracht in lijst_ widget kan aan elke pagina van uw winkel worden toegevoegd om het voor klanten gemakkelijk te maken om de verlanglijsten van vrienden en familieleden te vinden.

![Voorbeeld van winkel - zoeken in wensenlijst](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]**.

1. In de _[!UICONTROL Settings]_doet u het volgende:

   - Set **[!UICONTROL Type]** tot `Wish List Search`.

   - Set **[!UICONTROL Design Theme]** aan het thema van de winkel waar de verlanglijst wordt toegevoegd.

   - Klik op **[!UICONTROL Continue]**.

1. Voltooi de _[!UICONTROL Storefront Properties]_:

   - Voer de **[!UICONTROL Widget Title]**.

   - Set **[!UICONTROL Assign to Store Views]** naar de weergave of website waar de widget moet worden gebruikt.

   - Voor **[!UICONTROL Sort Order]** voert u een getal in om de plaatsing van de widget in de container te bepalen.

     `0` = eerste (standaardwaarde), `1` = seconde, `2` = derde, enzovoort.

1. In de _[!UICONTROL Layout Updates]_sectie, klikken **[!UICONTROL Add Layout Update]**en instellen **[!UICONTROL Display on]**op een van de volgende wijzen:

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. In de **[!UICONTROL Container]** kiest u het gebied van de paginalay-out waar u de pagina wilt plaatsen.

   ![Zoekwidget voor wenslijst - lay-out](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Widget Options]**.

1. Set **[!UICONTROL Quick Search Form Types]** op een van de volgende wijzen:

   - `All Forms` - Klanten kunnen zoeken op basis van alle beschikbare parameters.
   - `Owner Name` - Klanten kunnen op naam van eigenaar zoeken naar verlanglijsten.
   - `Owner Email` - Klanten kunnen op e-mailadres van eigenaar zoeken naar verlanglijsten.

   >[!NOTE]
   >
   >Verzendadressen worden niet opgenomen in verlanglijsten.

1. Stel de overige widgeigenschappen naar wens in volgens de standaard [instructies](../content-design/widget-create.md).

1. Klik op **[!UICONTROL Save]**.

1. Vernieuw bij de aanwijzing alle ongeldige caches.
