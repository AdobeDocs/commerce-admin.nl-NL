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

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Events]** sectie uit en doe het volgende:

   ![ configuratie van de Catalogus - catalogusgebeurtenissen ](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Enable Catalog Events Functionality]** in op `Yes` .

   - Stel **[!UICONTROL Enable Catalog Event Widget on Storefront]** in op `Yes` .

   - Voer de **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]** in. Deze waarde wordt standaard ingesteld op `5` . Voer `1` in als u slechts één gebeurtenis tegelijk in de schuifregelaar wilt weergeven.

   - Voer het getal **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]** in. Deze waarde wordt standaard ingesteld op `2` . Voer `1` in als u wilt dat de volgende gebeurtenis achtereenvolgens wordt weergegeven wanneer op de schuifregelaar wordt geklikt.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Toegangsbeperkingen

De toegang tot een privé verkoop, gebeurtenis, of plaats kan tot geregistreerde klanten worden beperkt die login, of uitgebreid tot niet geregistreerde klanten die zich moeten registreren alvorens toegang te verkrijgen.

![ Algemene configuratie - websitebeperkingen ](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Toegang beperken

De toegang tot een privé verkoop, gebeurtenis, of plaats kan tot geregistreerde klanten worden beperkt die login, of uitgebreid tot niet geregistreerde klanten die zich moeten registreren alvorens toegang te verkrijgen.

![ Algemene configuratie - websitebeperkingen ](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL General]** uit en kies **[!UICONTROL General]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Website Restrictions]** sectie uit.

1. Stel **[!UICONTROL Access Restriction]** in op `Yes` .

1. Stel **[!UICONTROL Restriction Mode]** in op een van de volgende opties:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Stel **[!UICONTROL Startup Page]** in op een van de volgende opties:

   - `To login form (302 Found)` - Gebruikers worden omgeleid naar het aanmeldingsformulier voordat ze toegang krijgen tot de site.

   - `To landing page (302 Found)` - Gebruikers worden omgeleid naar de opgegeven bestemmingspagina totdat zij zich aanmelden.

     >[!IMPORTANT]
     >
     >Zorg ervoor dat u een koppeling naar de aanmeldingspagina opneemt vanaf de bestemmingspagina, zodat klanten zich kunnen aanmelden om toegang te krijgen tot de site.

1. Kies de **[!UICONTROL Landing Page]** die wordt weergegeven voordat klanten zich aanmelden bij de persoonlijke verkoopsite.

1. Stel **[!UICONTROL HTTP Response]** in op `200 OK` als u wilt dat de zoekmachine bots en spinnen weet dat de bestemmingspagina correct is en er geen andere pagina&#39;s op de site staan die u wilt indexeren.

   In alle andere gevallen ingesteld op `503 Service Unavailable` .

   >[!NOTE]
   >
   >Van toepassing slechts als de beperkingswijze aan _Gesloten Website_ wordt geplaatst. De landingspagina wordt weergegeven als ruwe HTML.

1. Als u wilt dat de velden in de aanmeldingsnaam van de klant automatisch worden ingevuld en wachtwoordformulieren worden vergeten van vorige vermeldingen, stelt u **[!UICONTROL Enable Autocomplete on login/forgot password forms]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Verkoop beperken

Standaard zijn producten die in volgende of gesloten gebeurtenissen worden weergegeven, niet beschikbaar voor de algemene verkoop en staat de knop _[!UICONTROL Add to Cart]_&#x200B;niet op de productlijst of productpagina.

Om de _[!UICONTROL Add to Cart]_&#x200B;knoop voor een gesloten gebeurtenis te herstellen, moet de gebeurtenis worden geschrapt (zie [ gebeurtenissen van de Update ](event-create.md#update-events)). Als een product echter is gekoppeld aan een andere categorie zonder verkoopbeperkingen, is de knop beschikbaar op de productpagina. Op dezelfde manier wordt het tickerblok niet op de productpagina weergegeven als het product is gekoppeld aan een andere categorie waarvoor geen verkoopbeperkingen gelden.
