---
title: Een vriend e-mailen
description: Leer hoe u een e-mailkoppeling kunt maken waarmee uw klanten eenvoudig koppelingen naar producten met hun vrienden kunnen delen.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Een vriend e-mailen

Met de koppeling E-mail kunnen uw klanten eenvoudig koppelingen naar producten delen met hun vrienden. In de demo Luma-store wordt de e-mailkoppeling weergegeven als een enveloppictogram. Het berichtmalplaatje kan voor uw stem en merk worden aangepast. Om spamming te verhinderen, kunt u het aantal ontvangers voor elke e-mail, en het aantal producten beperken die over een periode van één uur kunnen worden gedeeld.

![Voorbeeld van winkel - e-mail een vriend](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## E-mail-a-vriend configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Email to a Friend]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Email Templates]** en stel de opties in:

   ![Catalogusconfiguratie - e-mailsjablonen](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [E-mailsjablonen](../configuration-reference/catalog/email-to-a-friend.md) in de _Referentiehandleiding voor configuratie_.

   Als u de standaardinstelling van een veld wilt wijzigen, schakelt u de optie **[!UICONTROL Use system value]** Schakel het selectievakje in om het veld bewerkbaar te maken.

   - Set **[!UICONTROL Enabled]** tot `Yes`.

   - Set **[!UICONTROL Select Email Template]** aan het malplaatje dat u als basis van de berichten wilt gebruiken.

   - Als u wilt dat alleen geregistreerde klanten e-mail naar vrienden kunnen verzenden, stelt u **[!UICONTROL Allow for Guests]** tot `No`.

   - Voor **[!UICONTROL Max Recipients]** Voer het maximumaantal vrienden in dat op de distributielijst voor één bericht kan staan.

   - Voor **[!UICONTROL Max Products Sent in 1 Hour]**, voert u het maximumaantal producten in dat door één gebruiker met vrienden kan worden gedeeld over een periode van één uur.

   - Set **[!UICONTROL Limit Sending By]** naar een van de volgende methoden om de afzender van e-mails te identificeren:

     `IP Address`  - (Aanbevolen) Identificeert de afzender door het IP adres van de computer die wordt gebruikt om de e-mails te verzenden.

     `Cookie (unsafe)` - Identificeert de afzender door browser koekje. Deze methode is minder effectief omdat de afzender het cookie kan verwijderen om de limiet te overschrijden.

1. Klik op **[!UICONTROL Save Config]**.

## E-mail verzenden naar een vriend in de winkel

Wanneer deze functie is geconfigureerd, volgen klanten deze stappen om productinformatie met vrienden te delen.

1. Op een cataloguspagina klikt de klant op de knop **[!UICONTROL Email]** koppeling.

1. Als de eigenschap slechts voor geregistreerde gebruikers wordt gevormd, doe één van het volgende:

   - Meld u aan bij uw klantenaccount.
   - Aanmelden voor een nieuwe account.

1. Hiermee voltooit u het **[!UICONTROL Message]** en wordt de ontvanger **[!UICONTROL Name]** en **[!UICONTROL Email Address]**.

   Indien nodig kan de klant meer ontvangers toevoegen:

   - Klikken **[!UICONTROL Add Invitee]**.

   - Hiermee wordt het dialoogvenster **[!UICONTROL Name]** en **[!UICONTROL Email Address]** van de extra persoon.

     Zij kunnen het bericht naar zoveel extra mensen verzenden zoals de configuratie toestaat. Ze kunnen de toegevoegde genodigde verwijderen door op de knop **[!DNL Remove]** koppeling.

1. Wanneer klaar om het bericht te verzenden, klikt u **[!UICONTROL Send Email]**.

   ![Voorbeeld van winkel - e-mail naar een vriend](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
