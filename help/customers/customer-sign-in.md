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

Klanten hebben gemakkelijk toegang tot hun accounts vanaf elke pagina in uw winkel. Afhankelijk van de [configuratie](../customers/account-options-new.md), kunnen klanten worden omgeleid naar hun accountdashboard, of blijven winkelen nadat ze zich bij hun accounts hebben aangemeld.

Indien [CAPTCHA](../systems/security-captcha.md) wordt toegelaten in de configuratie, moet de persoon een test correct voltooien die hen controleert om menselijk te zijn, alvorens tot hun rekeningen toegang te krijgen.

Wanneer klanten hun wachtwoorden vergeten, wordt een koppeling om de instellingen opnieuw in te stellen verzonden naar het e-mailadres dat aan het account is gekoppeld. De [Wachtwoordopties](../customers/password-options.md) de configuratie controleert de klantenervaring voor login pogingen:

- Het aantal keren dat een klant kan proberen een wachtwoord in te voeren
- Het aantal minuten tussen pogingen
- Het aantal pogingen voordat de account is vergrendeld
- De lengte van de vergrendeling

![Koppeling Aanmelden in de winkelkop](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Aanmelden bij een klantenaccount

1. In de kopbal van de opslag, klikt de klant **[!UICONTROL Sign in]**.

   ![Aanmelden bij klant](assets/login.png){width="700" zoomable="yes"}

1. Voer hun **[!UICONTROL Email]** adres en **[!UICONTROL Password]**.

1. Klikken **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Als ze hun wachtwoord niet kunnen onthouden, kan de klant op **[!UICONTROL Forgot Your Password?]** en volgt de [instructies](../customers/password-reset.md) om het wachtwoord opnieuw in te stellen.

## Omleiding naar het accountdashboard instellen na aanmelding bij de klant

U kunt de winkel zo configureren dat klanten na hun aanmelding worden omgeleid naar het dashboard van hun account of dat ze door kunnen gaan met winkelen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Vouw de sectie **[!UICONTROL Login Options]** uit.

1. Set **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** op een van de volgende wijzen:

   - `Yes` - Het accountdashboard wordt weergegeven wanneer klanten zich aanmelden bij hun accounts.
   - `No` - Klanten kunnen blijven winkelen nadat ze zich hebben aangemeld bij hun accounts.

1. Klik op **[!UICONTROL Save Config]**.

## Aanmelden met Amazon

Voor opslag met een configuratie [!DNL Amazon Pay] en [!DNL Login with Amazon] kunnen klanten zich aanmelden bij hun Amazon-kopersaccount.

1. In de kopbal van de opslag, klikt de klant **[!UICONTROL Sign in]**.

1. Klikken **[!UICONTROL Login with Amazon]**.

   ![Aanmelden bij Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Wanneer de klant wordt gevraagd zich aan te melden, gaat de klant het **[!UICONTROL email address]** en **[!UICONTROL password]** voor hun Amazon-kopersaccount.

   ![Amazon-gebruikersgegevens invoeren](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Als u Amazon toestemming wilt geven om de volgende gegevens van hun account te delen met de winkel bij het verwerken van aankopen, klikt u op **Oké**.

   - Naam
   - E-mailadres
   - Verzendadressen

   ![Toestemming verlenen voor het delen van gegevens](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Afmelden bij een klantenaccount

1. In de rechterbovenhoek naast  _[!UICONTROL Welcome, Customer Name!]_, klikt de klant op de knop **[!UICONTROL v]**menuselector.

1. Kies **[!UICONTROL Sign Out]**.

Na het afmelden wordt de klant omgeleid naar de startpagina.
