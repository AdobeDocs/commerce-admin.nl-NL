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

![ de storefront van het Voorbeeld - e-mail een vriend ](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## E-mail-a-vriend configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Email to a Friend]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Email Templates]** sectie uit en plaats de opties:

   ![ configuratie van de Catalogus - e-mailmalplaatjes ](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ E-mailMalplaatjes ](../configuration-reference/catalog/email-to-a-friend.md) in de _Gids van de Verwijzing van de Configuratie_.

   Als u de standaardinstelling van een veld wilt wijzigen, schakelt u het selectievakje **[!UICONTROL Use system value]** uit om het veld bewerkbaar te maken.

   - Stel **[!UICONTROL Enabled]** in op `Yes` .

   - Stel **[!UICONTROL Select Email Template]** in op de sjabloon die u als basis voor de berichten wilt gebruiken.

   - Stel **[!UICONTROL Allow for Guests]** in op `No` als u wilt dat alleen geregistreerde klanten e-mail naar vrienden kunnen verzenden.

   - Voer bij **[!UICONTROL Max Recipients]** het maximumaantal vrienden in dat zich in de distributielijst kan bevinden voor één bericht.

   - Voer bij **[!UICONTROL Max Products Sent in 1 Hour]** het maximumaantal producten in dat gedurende een periode van één uur door één gebruiker met vrienden kan worden gedeeld.

   - Stel **[!UICONTROL Limit Sending By]** in op een van de volgende methoden om de afzender van e-mailberichten te identificeren:

     `IP Address` - (Aanbevolen) Hiermee wordt de afzender aangeduid aan de hand van het IP-adres van de computer die wordt gebruikt om de e-mails te verzenden.

     `Cookie (unsafe)` - Identificeert de afzender door browser koekje. Deze methode is minder effectief omdat de afzender het cookie kan verwijderen om de limiet te overschrijden.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## E-mail verzenden naar een vriend in de winkel

Wanneer deze functie is geconfigureerd, volgen klanten deze stappen om productinformatie met vrienden te delen.

1. Op een cataloguspagina klikt de klant op de koppeling **[!UICONTROL Email]** .

1. Als de eigenschap slechts voor geregistreerde gebruikers wordt gevormd, doe één van het volgende:

   - Meld u aan bij uw klantenaccount.
   - Aanmelden voor een nieuwe account.

1. Voltooit **[!UICONTROL Message]** en voert de ontvanger **[!UICONTROL Name]** en **[!UICONTROL Email Address]** in.

   Indien nodig kan de klant meer ontvangers toevoegen:

   - Klik op **[!UICONTROL Add Invitee]** .

   - Voer de **[!UICONTROL Name]** en **[!UICONTROL Email Address]** van de extra persoon in.

     Zij kunnen het bericht naar zoveel extra mensen verzenden zoals de configuratie toestaat. Ze kunnen de toegevoegde genodigde verwijderen door op de koppeling **[!DNL Remove]** te klikken.

1. Wanneer u klaar bent om het bericht te verzenden, klikt u op **[!UICONTROL Send Email]** .

   ![ de storefront van het Voorbeeld - e-mail aan een vriend ](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
