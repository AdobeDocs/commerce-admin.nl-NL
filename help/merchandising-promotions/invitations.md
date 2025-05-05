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

In de sectie _[!UICONTROL My Invitations]_&#x200B;van de klantenaccount worden alle uitnodigingen weergegeven die de klant heeft verzonden. Klanten kunnen uitnodigingen verzenden aan vrienden en familie voor winkelgebeurtenissen, cadeauregisters, verlanglijsten enzovoort.

![ Mijn Uitnodigingen ](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Uitnodigingsworkflow

1. **Klant bereidt uitnodigingen** voor: Van het rekeningsdashboard, bereidt de klant de lijst van ontvangers voor en voltooit de uitnodiging. Afhankelijk van de configuratie kan een aangepast bericht worden opgenomen.
1. **de Klant verzendt uitnodigingen**: Wanneer klaar, klikt de klant de _[!UICONTROL Send Invitations]_&#x200B;knoop.
1. **het Systeem beheert transmissie**: Het systeem verzendt uitnodigingen in partijen, volgens het aantal dat in de configuratie wordt geplaatst.
1. **controleert de Klant reactie**: De klant controleert het statuut van elke uitnodiging van het rekeningsdashboard, zoals `Sent`, `Accepted`, of `Canceled`.

### Een uitnodiging verzenden

1. In de zijbalk van hun account op de storefront kiest de klant **[!UICONTROL My Invitations]** .

1. Voor de _Mijn pagina van de Uitnodiging_, klikt **[!UICONTROL Send Invitation]**.

1. Hiermee definieert u het nieuwe uitnodigingsitem:

   - Voltooi de e-mailgegevens.

   - (Optioneel) Hiermee maakt u een uitnodiging voor meerdere adressen door op **+** te klikken en een ander e-mailadres toe te voegen.

     Voor één uitnodiging geldt een limiet van vijf e-mailadressen.

   - (Optioneel) Voer een begeleidend bericht in.

1. Klik op **[!UICONTROL Send Invitation]** wanneer dit is voltooid.

Er wordt een uitnodigingsbericht verzonden naar het e-mailadres van de uitgenodigde gebruiker met de koppeling Instructies om het account in te stellen.

>[!NOTE]
>
>Een gebruiker kan slechts één uitnodiging naar een specifiek e-mailadres verzenden. Als u een uitnodiging opnieuw naar hetzelfde e-mailadres probeert te verzenden, wordt een foutbericht weergegeven en wordt de uitnodiging niet verzonden.

## Uitnodigingen inschakelen voor uw winkel

De uitnodigingsconfiguratie laat uitnodigingen voor de opslag toe en bepaalt hoe zij worden verzonden.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Invitations]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL General]** sectie uit.

   ![ configuratie van Klanten - uitnodigingen algemene opties ](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable Invitations Functionality]** in op `Yes` .

1. Om klanten toe te staan om uitnodigingen van de storefront te beheren, plaats **laat Uitnodigingen op Storefront** aan `Yes` toe.

1. Stel **[!UICONTROL Referred Customer Group]** in op een van de volgende opties:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Stel **[!UICONTROL New Accounts Registration]** in op een van de volgende opties:

   - `By Invitation Only`
   - `Available to All`

1. Selecteer `Yes` als u **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]** wilt gebruiken.

1. Als u het aantal uitnodigingen dat tegelijkertijd kan worden verzonden wilt beperken, voert u het nummer in het veld **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** in.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Email]** sectie uit en doe het volgende:

   ![ configuratie van Klanten - uitnodigingen e-mailopties ](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Selecteer de opslagidentiteit die u als **[!UICONTROL Customer Invitation Email Sender]** wilt gebruiken.

   - Selecteer de **[!UICONTROL Customer Invitation Email Template]** die wordt gebruikt voor verzonden uitnodigingen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Uitnodigingen verzenden en beheren in Beheer

In de [ Privé sectie van de Rapporten van de Verkoop ](../getting-started/private-sales-reports.md), kunt u het aantal uitnodigingen zien die tijdens een gespecificeerde periode worden verzonden, of klanten aan wie u uitnodigingen hebt verzonden.

### Een uitnodiging maken in de beheerder

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Invitations]** .

1. Voer in het volgende scherm e-mailadressen in om nieuwe klanten uit te nodigen, voeg een aangepast bericht toe, kies een afzender en selecteer een groep genodigden.

   Als u meerdere winkelweergaven hebt, gebruikt u de optie **[!UICONTROL Send From]** om de winkelweergave op te geven van waaruit een uitnodiging wordt verzonden.

   ![ Informatie van Uitnodigingen ](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

### Uitnodigingen voor één entiteit negeren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Zoek de gewenste uitnodiging met behulp van filters en open deze in de bewerkingsmodus.

1. Klik in de rechterbovenhoek op **[!UICONTROL Discard Invitation]** .

1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

### Uitnodigingen voor meerdere entiteiten negeren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Zoek en selecteer de uitnodigingen die u wilt verwijderen.

1. Kies in de linkerbovenhoek het menu **[!UICONTROL Actions]** om **[!UICONTROL Discard Selected]** te kiezen en klik op **[!UICONTROL Submit]** .

1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

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
