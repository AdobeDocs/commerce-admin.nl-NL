---
title: Aanmelden bij klant
description: De klant ondertekent in functie op de storefront staat voor gemakkelijke toegang tot de rekeningen van de klanten toe.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Aanmelden bij klant

Klanten hebben gemakkelijk toegang tot hun accounts vanaf elke pagina in uw winkel. Afhankelijk van de [ configuratie ](../customers/account-options-new.md), kunnen de klanten aan hun rekeningsdashboard worden opnieuw gericht, of blijven het winkelen nadat zij login aan hun rekeningen.

Als [ CAPTCHA ](../systems/security-captcha.md) in de configuratie wordt toegelaten, moet de persoon een test correct voltooien die hen verifieert om menselijk te zijn, alvorens toegang tot hun rekeningen te verkrijgen.

Wanneer klanten hun wachtwoorden vergeten, wordt een koppeling om de instellingen opnieuw in te stellen verzonden naar het e-mailadres dat aan het account is gekoppeld. De [ Opties van het Wachtwoord ](../customers/password-options.md) configuratie controleert de klantenervaring voor login pogingen:

- Het aantal keren dat een klant kan proberen een wachtwoord in te voeren
- Het aantal minuten tussen pogingen
- Het aantal pogingen voordat de account is vergrendeld
- De lengte van de vergrendeling

![ Teken in verbinding op de storefront kopbal ](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Aanmelden bij een klantenaccount

1. In de koptekst van de winkel klikt de klant op **[!UICONTROL Sign in]** .

   ![ Login van de Klant ](assets/login.png){width="700" zoomable="yes"}

1. Voer hun **[!UICONTROL Email]** adres en **[!UICONTROL Password]** in.

1. Klik op **[!UICONTROL Sign in]** .

   >[!IMPORTANT]
   >
   >Als zij hun wachtwoord niet kunnen herinneren, kan de klant **[!UICONTROL Forgot Your Password?]** klikken en de [ instructies ](../customers/password-reset.md) volgen om het wachtwoord terug te stellen.

## Omleiding naar het accountdashboard instellen na aanmelding bij de klant

U kunt de winkel zo configureren dat klanten na hun aanmelding worden omgeleid naar het dashboard van hun account of dat ze door kunnen gaan met winkelen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Login Options]** uit.

1. Stel **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** in op een van de volgende opties:

   - `Yes` - Het accountdashboard wordt weergegeven wanneer klanten zich aanmelden bij hun accounts.
   - `No` - Klanten kunnen blijven winkelen nadat ze zich hebben aangemeld bij hun accounts.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Aanmelden met Amazon

Voor winkels met een geconfigureerde [!DNL Amazon Pay] en [!DNL Login with Amazon] integratie kunnen klanten zich aanmelden bij hun Amazon-kopersaccount.

1. In de koptekst van de winkel klikt de klant op **[!UICONTROL Sign in]** .

1. Klik op **[!UICONTROL Login with Amazon]** .

   ![ Login met Amazon ](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Wanneer de klant wordt gevraagd zich aan te melden, voert hij de **[!UICONTROL email address]** en **[!UICONTROL password]** in voor zijn Amazon-kopersaccount.

   ![ het ingaan van de geloofsbrieven van Amazon ](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Om de toestemming van Amazon te verlenen om de volgende informatie van hun rekening met de opslag te delen wanneer het verwerken van aankopen, klikt **Oke**.

   - Naam
   - E-mailadres
   - Verzendadressen

   ![ Toestemming van de Verlening om Gegevens ](assets/amazon-popup2.png){width="700" zoomable="yes"} te delen

## Afmelden bij een klantenaccount

1. In de rechterbovenhoek naast _[!UICONTROL Welcome, Customer Name!]_&#x200B;klikt de klant op de menukiezer **[!UICONTROL v]**.

1. Kies **[!UICONTROL Sign Out]** .

Na het afmelden wordt de klant omgeleid naar de startpagina.
