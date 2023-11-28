---
title: E-mailcommunicatie configureren
description: Leer hoe te om e-mailmededelingen, met inbegrip van het verpletteren van teruggekeerde e-mail of antwoorden aan een specifiek e-mailadres te vormen.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# E-mailcommunicatie configureren

De _Instellingen voor verzending per post_ geef u de capaciteit om teruggekeerde e-mail of antwoorden aan e-mail naar een specifiek adres te leiden. Als uw opslag op een server SMTP of van Vensters loopt, kunt u de gastheer en havenmontages verifiëren.

>[!IMPORTANT]
>
>**Beveiligingskennisgeving** Alle handelaren zouden hun post onmiddellijk plaatsen verzendende configuratie tegen onlangs geïdentificeerd potentiële verre codeuitvoering moeten beschermen uitbuiten. Tot dit probleem is opgelost, wordt u ten zeerste aangeraden het gebruik van [!DNL Sendmail] voor e-mailcommunicatie. In de _[!UICONTROL Mail Sending Settings]_ervoor zorgen dat_[!UICONTROL Set Return Path]_ is ingesteld op `No`.

Voor een gedetailleerde lijst van de configuratiemontages, zie [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) in de _Configuratieverwijzing_.

## E-mailcommunicatie configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Mail Sending Settings]** en voer de volgende handelingen uit:

   ![Geavanceerde configuratie - instellingen voor het verzenden van e-mail](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Indien nodig, instellen **[!UICONTROL Disable Email Communications]** tot `No`.

   - Voor **[!UICONTROL Transport]** kiest u het transporttype voor e-mailcommunicatie in de winkel: `Sendmail` of `SMTP`

   - Als het lopen op een server SMTP of van Vensters, verifieer de volgende montages:

      - **[!UICONTROL Host]** - `localhost` of andere

      - **[!UICONTROL Port (25)]** - `25` of andere

   - Voor **[!UICONTROL Set Return Path]** kiest u een van de volgende opties:

      - `No` - (Aanbevolen beveiligingsmaatregel) Routes hebben een e-mail naar het standaard e-mailadres van de winkel geretourneerd.
      - `Yes` - Routes hebben een e-mail naar het standaard e-mailadres van de winkel geretourneerd.
      - `Specified` - Routes hebben een e-mail teruggestuurd naar het opgegeven e-mailadres **[!UICONTROL Return Path Email]**.

   - Als het lopen op een server SMTP, vorm de verbinding:

      - **[!UICONTROL Username]** - Voer de gebruikersnaam voor de aanmelding voor de SMTP-server in.
      - **[!UICONTROL Password]** - Voer het wachtwoord voor de SMTP-serveraanmelding in.
      - **[!UICONTROL Auth]** - Kies het verificatietype voor de SMTP-serververbinding: `NONE` , `PLAIN`, of `LOGIN`
      - **[!UICONTROL SSL]** - Kies het verificatietype voor het serverbeveiligingscertificaat: `SSL` of `TLS`

     ![Geavanceerde configuratie - instellingen voor het verzenden van e-mail](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales Emails]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL General Settings]** sectie.

1. Set **[!UICONTROL Asynchronous sending]** tot `Enable`.

   ![Verkoopconfiguratie - algemene e-mailinstellingen](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van de configuratiemontages, zie [_Algemene instellingen_](../configuration-reference/sales/sales-emails.md) in de _Configuratieverwijzing_.

1. Klik op **[!UICONTROL Save Config]**.
