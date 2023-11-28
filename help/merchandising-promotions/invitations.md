---
title: Uitnodigingen voor gebeurtenissen
description: Leer hoe klanten uitnodigingen voor gebeurtenissen en privé-verkoop kunnen verzenden en bekijken vanaf het dashboard van hun klantenaccounts.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Uitnodigingen voor gebeurtenissen

{{ee-feature}}

Wanneer uitnodigingen zijn ingeschakeld, kunnen klanten uitnodigingen verzenden en weergeven via het dashboard van hun klantenaccounts. De uitnodigings-e-mail bevat een koppeling naar de aanmeldingspagina van uw winkel voor klanten.

## Mijn uitnodigingen

De _[!UICONTROL My Invitations]_in het gedeelte van de klantenaccount worden alle uitnodigingen weergegeven die de klant heeft verzonden. Klanten kunnen uitnodigingen verzenden aan vrienden en familie voor winkelgebeurtenissen, cadeauregisters, verlanglijsten enzovoort.

![Mijn uitnodigingen](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Uitnodigingsworkflow

1. **De klant bereidt uitnodigingen voor**: Vanaf het accountdashboard bereidt de klant de lijst met ontvangers voor en voltooit de uitnodiging. Afhankelijk van de configuratie kan een aangepast bericht worden opgenomen.
1. **De klant verzendt uitnodigingen**: Wanneer gereed, klikt de klant op _[!UICONTROL Send Invitations]_knop.
1. **Systeem beheert transmissie**: Het systeem verzendt uitnodigingen in partijen, volgens het aantal dat in de configuratie wordt geplaatst.
1. **Antwoord van de klant**: De klant controleert de status van elke uitnodiging vanaf het accountdashboard, zoals `Sent`, `Accepted`, of `Canceled`.

### Een uitnodiging verzenden

1. In de zijbalk van hun account op de winkel kiest de klant **[!UICONTROL My Invitations]**.

1. Op de _Mijn uitnodiging_ pagina, klikken **[!UICONTROL Send Invitation]**.

1. Hiermee definieert u het nieuwe uitnodigingsitem:

   - Voltooi de e-mailgegevens.

   - (Optioneel) Hiermee maakt u een uitnodiging voor meerdere adressen door op **+** en nog een e-mailadres toevoegen.

     Voor één uitnodiging geldt een limiet van vijf e-mailadressen.

   - (Optioneel) Voer een begeleidend bericht in.

1. Na voltooiing klikt u op **[!UICONTROL Send Invitation]**.

Er wordt een uitnodigingsbericht verzonden naar het e-mailadres van de uitgenodigde gebruiker met de koppeling Instructies om het account in te stellen.

>[!NOTE]
>
>Een gebruiker kan slechts één uitnodiging naar een specifiek e-mailadres verzenden. Als u een uitnodiging opnieuw naar hetzelfde e-mailadres probeert te verzenden, wordt een foutbericht weergegeven en wordt de uitnodiging niet verzonden.

## Uitnodigingen inschakelen voor uw winkel

De uitnodigingsconfiguratie laat uitnodigingen voor de opslag toe en bepaalt hoe zij worden verzonden.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Invitations]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL General]** sectie.

   ![Configuratie van klanten - uitnodigingen, algemene opties](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable Invitations Functionality]** tot `Yes`.

1. Als u klanten wilt toestaan uitnodigingen te beheren vanuit de winkel, stelt u **Uitnodigingen inschakelen op Storefront** tot `Yes`.

1. Set **[!UICONTROL Referred Customer Group]** op een van de volgende wijzen:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Set **[!UICONTROL New Accounts Registration]** op een van de volgende wijzen:

   - `By Invitation Only`
   - `Available to All`

1. Naar **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, selecteert u `Yes`.

1. Als u het aantal uitnodigingen dat tegelijk kan worden verzonden wilt beperken, voert u het aantal in het dialoogvenster **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** veld.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Email]** en voer de volgende handelingen uit:

   ![Configuratie van klanten - e-mailopties voor uitnodigingen](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Selecteer de opslagidentiteit die u wilt gebruiken als de **[!UICONTROL Customer Invitation Email Sender]**.

   - Selecteer de **[!UICONTROL Customer Invitation Email Template]** gebruikt voor verzonden uitnodigingen.

1. Klik op **[!UICONTROL Save Config]**.

## Uitnodigingen verzenden en beheren in Beheer

In de [Privéverkooprapporten](../getting-started/private-sales-reports.md) kunt u het aantal uitnodigingen zien dat tijdens een bepaalde periode is verzonden, of klanten aan wie u uitnodigingen hebt verzonden.

### Een uitnodiging maken in de beheerder

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Invitations]**.

1. Voer in het volgende scherm e-mailadressen in om nieuwe klanten uit te nodigen, voeg een aangepast bericht toe, kies een afzender en selecteer een groep genodigden.

   Als u meerdere winkelweergaven hebt, gebruikt u de **[!UICONTROL Send From]** om de winkelweergave op te geven van waaruit een uitnodiging wordt verzonden.

   ![Uitnodigingen](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

### Uitnodigingen voor één entiteit negeren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Zoek de gewenste uitnodiging met behulp van filters en open deze in de bewerkingsmodus.

1. Klik in de rechterbovenhoek op **[!UICONTROL Discard Invitation]**.

1. Klik op **[!UICONTROL OK]**.

### Uitnodigingen voor meerdere entiteiten negeren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Zoek en selecteer de uitnodigingen die u wilt verwijderen.

1. Gebruik in de linkerbovenhoek de **[!UICONTROL Actions]** te kiezen menu **[!UICONTROL Discard Selected]** en klik op **[!UICONTROL Submit]**.

1. Klik op **[!UICONTROL OK]**.

### Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Schakel het selectievakje in om de uitnodigingen voor een handeling te selecteren of gebruik het selectiegereedschap in de kolomkop. Opties: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | Het interne id-nummer van een uitnodiging |
| [!UICONTROL Email] | Een overeenkomstig e-mailadres van de klant |
| [!UICONTROL Invitee] | E-mail voor uitgenodigde gebruikers |
| [!UICONTROL Sent] | Tijd en datum waarop een uitnodiging is verzonden |
| [!UICONTROL Registered] | Tijd en gegevens waarop een klant is geregistreerd |
| [!UICONTROL Status] | Status uitnodiging. Opties: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | De bijbehorende website |
| [!UICONTROL Invitee Group] | Een klantengroep van een genodigde |

{style="table-layout:auto"}
