---
title: Wish list storefront experience
description: Meer informatie over de tools voor het beheer van wensenlijsten die beschikbaar zijn voor uw klanten in de winkel.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Wish list storefront experience

Een verlanglijst is een handige manier voor klanten om producten terug te roepen die ze leuk vinden, maar die niet klaar zijn om te kopen. Items van een verlanglijst kunnen met anderen worden gedeeld of aan het winkelwagentje worden toegevoegd. Als de klant meerdere verlanglijsten heeft, wordt de naam van de huidige verlanglijst boven aan de pagina weergegeven. Klanten kunnen hun verlanglijstjes beheren via hun accountdashboard. Winkelbeheerders kunnen klanten ook helpen bij het beheren van hun verlanglijstjes via de beheerdersfunctie.

![Voorbeeld van een winkel - Mijn lijst met wensen](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce ondersteunt het gebruik van meerdere wenslijsten per klantenaccount.

![Magento Open Source](../assets/open-source.svg) De basis van de code van de Magento Open Source steunt het gebruik van één enkele verlanglijst per klantenrekening.

## Een verlanglijst maken

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

In de winkel kan een klant een verlanglijst maken van het dashboard van zijn account, een productpagina, een cataloguspagina en het winkelwagentje.

### Methode 1: Van een klantenaccount

1. In de zijbalk van het accountdashboard kiest de klant **[!UICONTROL My Wish List]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Create New Wish List]**.

1. Voer de naam van de wenslijst in.

1. Als u wilt toestaan dat anderen hun lijst met wensen kunnen zien, selecteert u de optie **[!UICONTROL Public Wish List]** selectievakje.

   >[!NOTE]
   >
   >Het belangrijkste verschil tussen `Public` en `Private` wenslijsten zijn geen persoonlijke verlanglijsten [doorzoekbaar](wishlist-configuration.md#add-wish-list-search) via verlanglijstjes.

1. Klik op **[!UICONTROL Save]**.

   ![Nieuwe verlanglijst maken](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Methode 2: Van de cataloguspagina

1. Vanuit de winkel gaat de klant naar de cataloguspagina die het product bevat dat zij aan een verlanglijst willen toevoegen.

1. Beweegt over het product.

1. De klant klikt op de pijl naast de _Toevoegen aan lijst met wensen_ en selecteert het **[!UICONTROL Create New Wish List]**.

1. Voer de naam van de wenslijst in.

1. Als u wilt toestaan dat anderen hun lijst met wensen kunnen zien, selecteert u de optie **[!UICONTROL Public Wish List]** selectievakje.

1. Na voltooiing klikt u op **[!UICONTROL Save]**.

### Methode 3: Van de pagina met productdetails

1. Vanuit de winkel gaat de klant naar de detailpagina van het product dat hij of zij aan een verlanglijst wil toevoegen.

1. Klik op de pijl naast **[!UICONTROL Add to Wish List]** en kiest **[!UICONTROL Create New Wish List]**.

1. Hiermee wordt het dialoogvenster **[!UICONTROL Wish List Name]**.

1. Als u wilt toestaan dat anderen hun lijst met wensen kunnen zien, selecteert u de optie **[!UICONTROL Public Wish List]** selectievakje.

1. Na voltooiing klikt u op **[!UICONTROL Save]**.

   ![Nieuwe verlanglijst maken op de pagina Productdetails](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Methode 4: Van het winkelwagentje

1. De klant opent de **[!UICONTROL Shopping Cart]** pagina.

1. Klik onder het item op de pijl naast **[!UICONTROL Move to Wishlist]** en kiest **[!UICONTROL Create New Wish List]**.

1. Hiermee wordt het dialoogvenster **[!UICONTROL Wish List Name]**.

1. Als u wilt toestaan dat anderen hun lijst met wensen kunnen zien, selecteert u de optie **[!UICONTROL Public Wish List]** selectievakje.

1. Na voltooiing klikt u op **[!UICONTROL Save]**.

![Nieuwe lijst met objecten maken op de pagina Winkelwagentje](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## De productaanbieding bijwerken

1. Van de verlanglijst, wijst de klant aan het product om de opties te tonen.

1. Als u een **[!UICONTROL Comment]** over het product, de tekst in het vak onder de prijs invullen.

   ![Bewerkingsopties](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Als u de selectie van productopties wilt wijzigen, klikt u op **[!UICONTROL Edit]** en doet het volgende:

   - Hiermee werkt u de opties op de pagina met productdetails bij.
   - Klikken **[!UICONTROL Update Wish List]**.

## Een product uit de verlanglijst toevoegen aan het winkelwagentje

1. In de verlanglijst, wijst de klant aan het product dat u wilt toevoegen.

1. Hiermee werkt u de **[!UICONTROL Qty]** en bewerk indien nodig de andere opties.

1. Klikken **[!UICONTROL Add to Cart]**.

## De verlanglijst delen

1. De klant klikt **[!UICONTROL Share Wishlist]**.

1. Voer het e-mailadres in van elke persoon die de verlanglijst moet ontvangen, gescheiden door een komma.

1. Hiermee voegt u een **[!UICONTROL Message]** in de e-mail op te nemen.

1. Klikken **[!UICONTROL Share Wish List]**.

   ![Uw verlanglijst delen](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   Het bericht wordt verzonden vanuit uw primaire [contactpersoon voor winkel](../getting-started/store-details.md#store-email-addresses) en bevat een miniatuurafbeelding van elk product met koppelingen naar uw winkel.

   ![E-mail met lijst met gedeelde wensen](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Wenslijsten bewerken

Klanten kunnen hun verlanglijst op meerdere manieren wijzigen via hun accountdashboard.

### Items naar een andere lijst verplaatsen

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

1. De klant selecteert het selectievakje van elk item dat moet worden verplaatst.

1. Klikken **[!UICONTROL Move Selected to Wish List]** en voert een van de volgende handelingen uit:

   - Kies een bestaande lijst met wensen.
   - Klikken **[!UICONTROL Create New Wish List]**.

### Items naar een andere lijst kopiëren

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

1. Selecteert het selectievakje van elk item dat moet worden verplaatst.

1. Klikken **[!UICONTROL Copy Selected to Wish List]** en voert een van de volgende handelingen uit:

   - Kies een bestaande lijst met wensen.
   - Klikken **[!UICONTROL Create New Wish List]**.

## Een wenslijst verwijderen

![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)

1. De klant opent de lijst met wensen die u wilt verwijderen.

1. Klikken **[!UICONTROL Delete Wish List]**.

1. Wanneer ertoe aangezet om te bevestigen, klikt **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Deze handeling kan niet ongedaan worden gemaakt.

## Lijstitems overbrengen naar winkelwagentje

Om alle wensen lijstpunten naar het karretje over te brengen, klikt de klant **[!UICONTROL Add All to Cart]**.

De klant doet het volgende om één item toe te voegen:

1. Hiermee plaatst u de muisaanwijzer boven het item en voert u de **[!UICONTROL Qty]** dat ze aan de wagen willen toevoegen.

1. Klikken **[!UICONTROL Add to Cart]**.

## Zoek een verlanglijst voor klanten

Als de [Widget Lijstzoekopdracht wensen](wishlist-configuration.md#add-wish-list-search) in uw winkelpagina&#39;s kunnen klanten zoeken op de naam of het e-mailadres van de eigenaar van de verlanglijst.

1. In de zoekwidget voor wensenlijst selecteert de klant een zoekoptie.

1. Voer de naam of het e-mailadres van de eigenaar van de wenslijst in en klik op **[!UICONTROL Search]**.

   De _Zoekopdracht in lijst_ wordt geopend en om het even welke passende vorstenlijsten worden getoond in de sectie van onderzoeksresultaten.

   >[!NOTE]
   >
   >Slechts worden de openbare wenslijsten getoond in onderzoeksresultaten-klanten&#39; privé wenslijsten niet openbaar viewable.

1. Als u de lijst met wenslijstonderdelen wilt weergeven, klikt u op **[!UICONTROL View]**.

   De naam van de eigenaar en de datum van de laatste update worden voor elke verlanglijst weergegeven.

1. Om een product aan hun kar toe te voegen, selecteert de klant checkbox onder het product en klikt **[!UICONTROL Add to Cart]**.

   Je kunt ook objecten toevoegen die je leuk vindt van de verlanglijst van een andere klant.
