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

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Vouw de sectie **[!UICONTROL Password Options]** uit.

   ![Wachtwoordopties](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Stel de **[!UICONTROL Password Reset Protection Type]** aan de methode die u wilt gebruiken voor het controleren van verzoeken om opnieuw instellen van wachtwoorden:

   - `By IP and Email` - Controleren op vorige pogingen om het wachtwoord opnieuw in te stellen voor specifieke e-mail of van specifieke IP.
   - `By IP` - Controleren op vorige pogingen om het wachtwoord opnieuw in te stellen vanuit specifieke IP.
   - `By Email` - Controleren op vorige pogingen om het wachtwoord opnieuw in te stellen voor specifieke e-mail.
   - `None` - Beveiliging uitgeschakeld (geen beperkingen voor het opnieuw instellen van het wachtwoord).

   De **[!UICONTROL Max Number of Password Reset Requests]** en **[!UICONTROL Min Time Between Password Reset Requests]** worden berekend op basis van deze configuratie.

1. Ga als volgt te werk om het aantal aanvragen voor het opnieuw instellen van wachtwoorden dat per uur wordt verzonden te beperken:

   - Voor **[!UICONTROL Max Number of Password Reset Requests]** Voer het maximumaantal verzoeken om opnieuw in te stellen voor wachtwoorden dat per uur kan worden verzonden.

   - Voor **[!UICONTROL Min Time Between Password Reset Requests]** Voer het minimale aantal minuten in dat tussen de aanvragen moet verstrijken.

1. Ga als volgt te werk om het e-mailbericht voor het opnieuw instellen van wachtwoorden te configureren:

   - Set **[!UICONTROL Forgot Email Template]** naar de sjabloon die wordt gebruikt voor de e-mail die wordt verzonden naar klanten die hun wachtwoorden zijn vergeten.

   - Set **[!UICONTROL Remind Email Template]** naar de sjabloon die wordt gebruikt wanneer een klantwachtwoord door een Admin-gebruiker opnieuw wordt ingesteld.

   - Set **[!UICONTROL Reset Password Template]** aan het malplaatje dat wordt gebruikt wanneer de klanten hun wachtwoorden veranderen.

   - Set **[!UICONTROL Password Template Email Sender]** aan de [contactpersoon voor winkel](../getting-started/store-details.md) die wordt weergegeven als de verzender van wachtwoordgerelateerde meldingen.

1. Voer de volgende beveiligingsopties voor het opnieuw instellen van wachtwoorden in:

   - Voor **[!UICONTROL Recovery Link Expiration Period (hours)]**, ga het aantal uren in alvorens de verbinding van de wachtwoordterugwinning verloopt.

   - Als u wilt dat de velden in de aanmeldingsnaam van de klant automatisch worden ingevuld en dat wachtwoordformulieren niet meer worden ingevuld bij eerdere invoer, stelt u **[!UICONTROL Enable Autocomplete on login/forgot password forms]** tot `Yes`.

   - Voor **[!UICONTROL Number of Required Character Classes]** Voer het aantal verschillende tekentypen in dat in een wachtwoord moet worden opgenomen op basis van de volgende tekenklassen:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Voor **[!UICONTROL Maximum Login Failures to Lockout Account]**, voert u het aantal mislukte aanmeldingspogingen in totdat de klantenaccount is vergrendeld. Voer voor onbeperkte pogingen nul in (`0`).

   - Voor **[!UICONTROL Minimum Password Length]** Voer het minimale aantal tekens in dat in een wachtwoord kan worden gebruikt. Het getal moet groter zijn dan nul.

   - Voor **[!UICONTROL Lockout Time (minutes)]**, voert u het aantal minuten in dat een klantenaccount is vergrendeld nadat te veel mislukte aanmeldingspogingen zijn uitgevoerd.

1. Klik op **[!UICONTROL Save Config]**.
