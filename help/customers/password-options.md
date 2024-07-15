---
title: Opties voor wachtwoord van klant
description: De opties van het klantenwachtwoord bepalen het niveau van veiligheid voor diverse klant-onder ogen ziet functies van uw opslag.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Opties voor wachtwoord van klant

De opties van het klantenwachtwoord bepalen het niveau van veiligheid dat voor de verzoeken van het wachtwoordterugstellen, de e-mailmalplaatjes wordt gebruikt die voor klantenbericht, en het leven van de verbinding van de wachtwoordterugwinning worden gebruikt. U kunt klanten toestaan om hun eigen wachtwoorden te veranderen of vereisen dat slechts de opslagbeheerders dit kunnen doen.

## Opties voor klantwachtwoord configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Password Options]** uit.

   ![ Opties van het Wachtwoord ](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Stel de **[!UICONTROL Password Reset Protection Type]** in op de methode die u wilt gebruiken voor het controleren van aanvragen voor het opnieuw instellen van wachtwoorden:

   - `By IP and Email` - Controleren op vorige pogingen om het wachtwoord opnieuw in te stellen voor specifieke e-mail of van specifieke IP.
   - `By IP` - Controle voor vorige pogingen om wachtwoord van specifieke IP terug te stellen.
   - `By Email` - Controleren op vorige pogingen om het wachtwoord voor specifieke e-mail opnieuw in te stellen.
   - `None` - Beveiliging uitgeschakeld (geen beperkingen voor het opnieuw instellen van het wachtwoord).

   De waarden **[!UICONTROL Max Number of Password Reset Requests]** en **[!UICONTROL Min Time Between Password Reset Requests]** worden berekend op basis van deze configuratie.

1. Ga als volgt te werk om het aantal aanvragen voor het opnieuw instellen van wachtwoorden dat per uur wordt verzonden te beperken:

   - Voer bij **[!UICONTROL Max Number of Password Reset Requests]** het maximumaantal verzoeken om opnieuw in te stellen voor wachtwoorden in dat per uur kan worden verzonden.

   - Voer bij **[!UICONTROL Min Time Between Password Reset Requests]** het minimale aantal minuten in dat tussen de aanvragen moet verstrijken.

1. Ga als volgt te werk om het e-mailbericht voor het opnieuw instellen van wachtwoorden te configureren:

   - Stel **[!UICONTROL Forgot Email Template]** in op de sjabloon die wordt gebruikt voor het e-mailbericht dat wordt verzonden naar klanten die hun wachtwoorden vergeten zijn.

   - Stel **[!UICONTROL Remind Email Template]** in op de sjabloon die wordt gebruikt wanneer een klantwachtwoord door een Admin-gebruiker opnieuw wordt ingesteld.

   - Stel **[!UICONTROL Reset Password Template]** in op de sjabloon die wordt gebruikt wanneer klanten hun wachtwoorden wijzigen.

   - Plaats **[!UICONTROL Password Template Email Sender]** aan het [ opslagcontact ](../getting-started/store-details.md) dat als afzender van op wachtwoord betrekking hebbende berichten verschijnt.

1. Voer de volgende beveiligingsopties voor het opnieuw instellen van wachtwoorden in:

   - Voer bij **[!UICONTROL Recovery Link Expiration Period (hours)]** het aantal uren in voordat de koppeling voor wachtwoordherstel verloopt.

   - Als u wilt dat de velden in de aanmeldingsnaam van de klant automatisch worden ingevuld en wachtwoordformulieren worden vergeten van vorige vermeldingen, stelt u **[!UICONTROL Enable Autocomplete on login/forgot password forms]** in op `Yes` .

   - Voer bij **[!UICONTROL Number of Required Character Classes]** het aantal verschillende tekentypen in dat in een wachtwoord moet worden opgenomen op basis van de volgende tekenklassen:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Voer bij **[!UICONTROL Maximum Login Failures to Lockout Account]** het aantal mislukte aanmeldingspogingen in totdat de klantenaccount is vergrendeld. Voor onbeperkte pogingen, ga nul (`0`) in.

   - Voer bij **[!UICONTROL Minimum Password Length]** het minimale aantal tekens in dat in een wachtwoord kan worden gebruikt. Het getal moet groter zijn dan nul.

   - Voer voor **[!UICONTROL Lockout Time (minutes)]** het aantal minuten in dat een klantenaccount is vergrendeld nadat te veel mislukte aanmeldingspogingen zijn uitgevoerd.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
