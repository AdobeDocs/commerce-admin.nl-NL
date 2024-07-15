---
title: Wish list storefront experience
description: Meer informatie over de tools voor het beheer van wensenlijsten die beschikbaar zijn voor uw klanten in de winkel.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Wish list storefront experience

Een verlanglijst is een handige manier voor klanten om producten terug te roepen die ze leuk vinden, maar die niet klaar zijn om te kopen. Items van een verlanglijst kunnen met anderen worden gedeeld of aan het winkelwagentje worden toegevoegd. Als de klant meerdere verlanglijsten heeft, wordt de naam van de huidige verlanglijst boven aan de pagina weergegeven. Klanten kunnen hun verlanglijstjes beheren via hun accountdashboard. Winkelbeheerders kunnen klanten ook helpen bij het beheren van hun verlanglijstjes via de beheerdersfunctie.

![ de storefront van het Voorbeeld - Mijn Lijst van wensen ](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![ Adobe Commerce ](../assets/adobe-logo.svg) Adobe Commerce steunt het gebruik van veelvoudige wenslijsten per klantenrekening.

![ Magento Open Source ](../assets/open-source.svg) De basis van de code van de Magento Open Source steunt het gebruik van één enkele wensenlijst per klantenrekening.

## Een verlanglijst maken

![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce)

In de winkel kan een klant een verlanglijst maken van het dashboard van zijn account, een productpagina, een cataloguspagina en het winkelwagentje.

### Methode 1: Van een klantenaccount

1. In de zijbalk van het accountdashboard kiest de klant **[!UICONTROL My Wish List]** .

1. Klik in de rechterbovenhoek op **[!UICONTROL Create New Wish List]** .

1. Voer de naam van de wenslijst in.

1. Als u wilt dat anderen hun verlanglijst kunnen zien, schakelt u het selectievakje **[!UICONTROL Public Wish List]** in.

   >[!NOTE]
   >
   >Het belangrijkste verschil tussen `Public` en `Private` wenst lijsten is dat de privé wensen lijsten [ niet ](wishlist-configuration.md#add-wish-list-search) doorzoekbaar door wensen lijsten zijn.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   ![ creeer Nieuwe Gewenste Lijst ](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Methode 2: Van de cataloguspagina

1. Vanuit de winkel gaat de klant naar de cataloguspagina die het product bevat dat zij aan een verlanglijst willen toevoegen.

1. Beweegt over het product.

1. De klant klikt de pijl naast _toevoegt aan het pictogram van de Lijst van de Wissen_ en selecteert **[!UICONTROL Create New Wish List]**.

1. Voer de naam van de wenslijst in.

1. Als u wilt dat anderen hun verlanglijst kunnen zien, schakelt u het selectievakje **[!UICONTROL Public Wish List]** in.

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

### Methode 3: Van de pagina met productdetails

1. Vanuit de winkel gaat de klant naar de detailpagina van het product dat hij of zij aan een verlanglijst wil toevoegen.

1. Klik op de pijl naast **[!UICONTROL Add to Wish List]** en kies **[!UICONTROL Create New Wish List]** .

1. Voer de **[!UICONTROL Wish List Name]** in.

1. Als u wilt dat anderen hun verlanglijst kunnen zien, schakelt u het selectievakje **[!UICONTROL Public Wish List]** in.

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

   ![ creeer Nieuwe Wenslijst van de pagina van het Detail van het Product ](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Methode 4: Van het winkelwagentje

1. De klant opent de pagina **[!UICONTROL Shopping Cart]** .

1. Klik onder het item op de pijl naast **[!UICONTROL Move to Wishlist]** en kies **[!UICONTROL Create New Wish List]** .

1. Voer de **[!UICONTROL Wish List Name]** in.

1. Als u wilt dat anderen hun verlanglijst kunnen zien, schakelt u het selectievakje **[!UICONTROL Public Wish List]** in.

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

![ creeer Nieuwe Lijst van de Wens van de het Winkelen pagina van de Kar ](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## De productaanbieding bijwerken

1. Van de verlanglijst, wijst de klant aan het product om de opties te tonen.

1. Als u een **[!UICONTROL Comment]** over het product wilt toevoegen, voert u de tekst in het vak onder de prijs in.

   ![ geef Opties ](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"} uit

1. Als u de selectie van productopties wilt wijzigen, klikt u op **[!UICONTROL Edit]** en voert u de volgende handelingen uit:

   - Hiermee werkt u de opties op de pagina met productdetails bij.
   - Klik op **[!UICONTROL Update Wish List]** .

## Een product uit de verlanglijst toevoegen aan het winkelwagentje

1. In de verlanglijst, wijst de klant aan het product dat u wilt toevoegen.

1. Werkt **[!UICONTROL Qty]** bij en bewerk desgewenst de andere opties.

1. Klik op **[!UICONTROL Add to Cart]** .

## De verlanglijst delen

1. De klant klikt op **[!UICONTROL Share Wishlist]** .

1. Voer het e-mailadres in van elke persoon die de verlanglijst moet ontvangen, gescheiden door een komma.

1. Hiermee voegt u een **[!UICONTROL Message]** toe die in de e-mail moet worden opgenomen.

1. Klik op **[!UICONTROL Share Wish List]** .

   ![ deel Uw Lijst van de Wens ](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   Het bericht wordt verzonden van uw primaire [ opslagcontact ](../getting-started/store-details.md#store-email-addresses) en omvat een duimnagelbeeld van elk product, met verbindingen aan uw opslag.

   ![ Gedeelde E-mail van de Lijst van de Wens ](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Wenslijsten bewerken

Klanten kunnen hun verlanglijst op meerdere manieren wijzigen via hun accountdashboard.

### Items naar een andere lijst verplaatsen

![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce)

1. De klant selecteert het selectievakje van elk item dat moet worden verplaatst.

1. Klik op **[!UICONTROL Move Selected to Wish List]** en voer een van de volgende handelingen uit:

   - Kies een bestaande lijst met wensen.
   - Klik op **[!UICONTROL Create New Wish List]** .

### Items naar een andere lijst kopiëren

![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce)

1. Selecteert het selectievakje van elk item dat moet worden verplaatst.

1. Klik op **[!UICONTROL Copy Selected to Wish List]** en voer een van de volgende handelingen uit:

   - Kies een bestaande lijst met wensen.
   - Klik op **[!UICONTROL Create New Wish List]** .

## Een wenslijst verwijderen

![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce)

1. De klant opent de lijst met wensen die u wilt verwijderen.

1. Klik op **[!UICONTROL Delete Wish List]** .

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

>[!IMPORTANT]
>
>Deze handeling kan niet ongedaan worden gemaakt.

## Lijstitems overbrengen naar winkelwagentje

Als de klant alle gewenste lijstitems naar het winkelwagentje wilt overbrengen, klikt u op **[!UICONTROL Add All to Cart]** .

De klant doet het volgende om één item toe te voegen:

1. Hiermee plaatst u de cursor boven het item en voert u de **[!UICONTROL Qty]** in die ze aan het winkelwagentje willen toevoegen.

1. Klik op **[!UICONTROL Add to Cart]** .

## Zoek een verlanglijst voor klanten

Als de [ widget van het Onderzoek van de Lijst van de Wenslijst ](wishlist-configuration.md#add-wish-list-search) in inbegrepen in uw opslagpagina&#39;s, klanten door de naam of e-mailadres van de eigenaar van de verlanglijst kunnen zoeken.

1. In de zoekwidget voor wensenlijst selecteert de klant een zoekoptie.

1. Voer de naam of het e-mailadres van de eigenaar van de wenslijst in en klik op **[!UICONTROL Search]** .

   De _pagina van het Onderzoek van de Lijst van de Wenslijst_ opent en om het even welke passende vorstenlijsten worden getoond in de sectie van onderzoeksresultaten.

   >[!NOTE]
   >
   >Slechts worden de openbare wenslijsten getoond in onderzoeksresultaten-klanten&#39; privé wenslijsten niet openbaar viewable.

1. Klik op **[!UICONTROL View]** om de lijst met items in de wenslijst weer te geven.

   De naam van de eigenaar en de datum van de laatste update worden voor elke verlanglijst weergegeven.

1. Als u een product aan het winkelwagentje wilt toevoegen, selecteert de klant het selectievakje onder het product en klikt u op **[!UICONTROL Add to Cart]** .

   Je kunt ook objecten toevoegen die je leuk vindt van de verlanglijst van een andere klant.
