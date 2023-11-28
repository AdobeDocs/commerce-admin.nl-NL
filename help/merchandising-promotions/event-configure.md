---
title: Gebeurtenissen configureren
description: Leer hoe te om de basisconfiguratie te voltooien om gebeurtenissen toe te laten en opstelling het gebeurtenisblok in de storefront sidebar.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Gebeurtenissen configureren

{{ee-feature}}

Voordat u een gebeurtenis kunt maken, moet u de basisconfiguratie voltooien om gebeurtenissen in te schakelen en het gebeurtenisblok instellen in het zijpaneel.

## Gebeurtenissen inschakelen en configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Events]** en voer de volgende handelingen uit:

   ![Catalogusconfiguratie - catalogusgebeurtenissen](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Enable Catalog Events Functionality]** tot `Yes`.

   - Set **[!UICONTROL Enable Catalog Event Widget on Storefront]** tot `Yes`.

   - Voer de **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Deze waarde is standaard ingesteld op `5`. Als u slechts één gebeurtenis tegelijk in de schuifregelaar wilt weergeven, voert u `1`.

   - Voer het aantal van **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Deze waarde is standaard ingesteld op `2`. Als u wilt dat de schuifregelaar de volgende gebeurtenis in de juiste volgorde weergeeft wanneer op de knop wordt geklikt, voert u `1`.

1. Klik op **[!UICONTROL Save Config]**.

## Toegangsbeperkingen

De toegang tot een privé verkoop, gebeurtenis, of plaats kan tot geregistreerde klanten worden beperkt die login, of uitgebreid tot niet geregistreerde klanten die zich moeten registreren alvorens toegang te verkrijgen.

![Algemene configuratie - websitebeperkingen](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Toegang beperken

De toegang tot een privé verkoop, gebeurtenis, of plaats kan tot geregistreerde klanten worden beperkt die login, of uitgebreid tot niet geregistreerde klanten die zich moeten registreren alvorens toegang te verkrijgen.

![Algemene configuratie - websitebeperkingen](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL General]** en kiest u **[!UICONTROL General]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Website Restrictions]** sectie.

1. Set **[!UICONTROL Access Restriction]** tot `Yes`.

1. Set **[!UICONTROL Restriction Mode]** op een van de volgende wijzen:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Set **[!UICONTROL Startup Page]** op een van de volgende wijzen:

   - `To login form (302 Found)` - Gebruikers worden omgeleid naar het aanmeldingsformulier voordat ze toegang krijgen tot de site.

   - `To landing page (302 Found)` - Gebruikers worden omgeleid naar de opgegeven bestemmingspagina totdat zij zich aanmelden.

     >[!IMPORTANT]
     >
     >Zorg ervoor dat u een koppeling naar de aanmeldingspagina opneemt vanaf de bestemmingspagina, zodat klanten zich kunnen aanmelden om toegang te krijgen tot de site.

1. Kies de optie **[!UICONTROL Landing Page]** die wordt weergegeven voordat klanten zich aanmelden bij de particuliere verkoopsite.

1. Als u wilt weten dat de bestemmingspagina correct is en dat de site geen andere pagina&#39;s bevat die u wilt indexeren, stelt u **[!UICONTROL HTTP Response]** tot `200 OK`.

   In alle andere gevallen `503 Service Unavailable`.

   >[!NOTE]
   >
   >Alleen van toepassing als de beperkingsmodus is ingesteld op _Website gesloten_. De landingspagina wordt weergegeven als ruwe HTML.

1. Als u wilt dat de velden in de aanmeldingsnaam van de klant automatisch worden ingevuld en dat wachtwoordformulieren niet meer worden ingevuld bij eerdere invoer, stelt u **[!UICONTROL Enable Autocomplete on login/forgot password forms]** tot `Yes`.

1. Klik op **[!UICONTROL Save Config]**.

### Verkoop beperken

Standaard zijn producten die in volgende of gesloten gebeurtenissen worden weergegeven, niet beschikbaar voor algemene verkoop en de _[!UICONTROL Add to Cart]_niet op de productlijst of productpagina wordt weergegeven.

Als u de _[!UICONTROL Add to Cart]_knop voor een gesloten gebeurtenis, moet de gebeurtenis worden verwijderd (zie [Gebeurtenissen bijwerken](event-create.md#update-events)). Als een product echter is gekoppeld aan een andere categorie zonder verkoopbeperkingen, is de knop beschikbaar op de productpagina. Op dezelfde manier wordt het tickerblok niet op de productpagina weergegeven als het product is gekoppeld aan een andere categorie waarvoor geen verkoopbeperkingen gelden.
