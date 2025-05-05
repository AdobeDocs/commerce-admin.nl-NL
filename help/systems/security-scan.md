---
title: Beveiligingsscan
description: Leer hoe u een uitgebreide beveiligingsscan uitvoert en elk van uw Adobe Commerce- en Magento Open Source-sites controleert.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Beveiligingsscan

Met de verbeterde beveiligingsscan kunt u elk van uw Adobe Commerce- en Magento Open Source-sites, inclusief PWA, controleren op bekende beveiligingsrisico&#39;s en malware, en patchupdates en beveiligingsmeldingen ontvangen.

- Verbeter inzicht in de veiligheidsstatus in real time van uw opslag.
- Ontvang suggesties die op beste praktijken worden gebaseerd helpen kwesties oplossen.
- De beveiligingsscan van het schema wordt wekelijks, dagelijks of op verzoek uitgevoerd.
- Voer meer dan 21.000 veiligheidstests uit om potentiële malware te helpen identificeren.
- Heb toegang tot historische veiligheidsrapporten die de vooruitgang van uw plaatsen volgen en controleren.
- Open het scanrapport met geslaagde en mislukte controles, met de aanbevolen acties.

Het aftasten van de Veiligheid hulpmiddel is beschikbaar voor vrij van het dashboard van uw [ Commerce/Magento rekening ](../getting-started/commerce-account-create.md). Voor technische informatie, zie [ Opstelling het Hulpmiddel van het Scannen van de Veiligheid ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html?lang=nl-NL#set-up-the-security-scan-tool) in _Commerce op de Gids van de Infrastructuur van de Wolk_.

![ het aftasten van de Veiligheid hulpmiddel ](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Een beveiligingsscan uitvoeren

1. Van de homepage van Commerce, teken binnen aan uw [ Commerce/rekening van het Magento ](../getting-started/commerce-account-create.md).

1. Controleer en accepteer de voorwaarden voor het gebruik van het hulpprogramma voor beveiligingsscan.

   - Kies **[!UICONTROL Security Scan]** in het linkerdeelvenster.
   - Klik op **[!UICONTROL Go to Security Scan]**.
   - Lees de **[!UICONTROL Terms and Conditions]** .
   - Klik op **[!UICONTROL Agree]** om door te gaan.

1. Klik op de pagina _[!UICONTROL Monitored Websites]_&#x200B;op **[!UICONTROL +Add Site]**.

   Als u meerdere sites met verschillende domeinen hebt, configureert u een aparte scan voor elk domein.

   ![ bewaakte Plaatsen ](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit om te controleren of u eigenaar bent van het sitedomein door een bevestigingscode toe te voegen:

   **Commerce storefront**:

   - Voer de **[!UICONTROL Site URL]** en **[!UICONTROL Site Name]** in.
   - Klik op **[!UICONTROL Generate Confirmation Code]**.
   - Klik **Exemplaar** om uw bevestigingscode aan het klembord te kopiëren.

     ![ produceer Bevestigingscode ](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Meld u aan bij de beheerder van uw winkel als een gebruiker met volledige beheerdersrechten en voer de volgende handelingen uit:

      - In _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Zoek uw site in de lijst en klik op **[!UICONTROL Edit]** .
      - Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL HTML Head]** sectie uit.
      - Blader omlaag naar **[!UICONTROL Scripts and Style Sheets]** en klik in het tekstvak aan het einde van een bestaande code en plak de bevestigingscode in het tekstvak.

        ![ Manuscripten en de Bladen van de Stijl ](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

   **PWA storefront**:

   - Voer de **[!UICONTROL Site URL]** en **[!UICONTROL Site Name]** in.

   - Kies bij **[!UICONTROL Confirmation Code]** de optie `META Tag` en klik op **[!UICONTROL Generate Code]** .

   - Klik op **[!UICONTROL Copy]** om de gegenereerde bevestigingscode van de META-tag naar het klembord te kopiëren.

     ![ produceer Bevestigingscode ](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Ga naar de PWA Studio storefront projectfolder en doe het volgende:

      - Ga onder de projectmap PWA Studio naar `packages > venia-concept > template.html` .
      - Voeg de gekopieerde bevestigingscode (de gegenereerde META-tag) toe aan de kop van de HTML en sla de wijzigingen op.

        ![ Code van de Bevestiging van het Exemplaar ](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Ga terug naar PWA Studio CLI, en gebruik garen om projectgebiedsdelen te installeren en het project in werking te stellen bouwt bevel.

        ```sh
        yarn install &&
        yarn build
        ```

      - *in uw project van de Wolk*, creeer a `pwa` omslag en kopieer de inhoud binnen de omslag van uw storefront project `dist`.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Met het gereedschap Git CLI kunt u deze wijzigingen in uw Cloud-project uitvoeren, uitvoeren en uitvoeren.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Nadat het bouwstijlproces voltooit, zullen de veranderingen aan uw PWA store front worden opgesteld.

1. Ga terug naar de pagina _[!UICONTROL Security Scan]_&#x200B;in uw Commerce-account en klik op **[!UICONTROL Verify Confirmation Code]**&#x200B;om de eigendom van het domein te bepalen.

1. Na een geslaagde bevestiging, vorm de **[!UICONTROL Set Automatic Security Scan]** opties voor één van de volgende types:

   **Scannen Wekelijks (geadviseerd)**:

   - Kies de **[!UICONTROL Week Day]** , **[!UICONTROL Time]** en **[!UICONTROL Time Zone]** waar de scan elke week moet plaatsvinden.
   - Standaard wordt de scan elke week om middernacht zaterdag, UTC en verder naar begin zondag gepland.

     ![ Wekelijks aftasten ](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Scannen Dagelijks**:

   - Kies de lus **[!UICONTROL Time]** en **[!UICONTROL Time Zone]** dat de scan elke dag moet worden uitgevoerd.
   - Standaard wordt de scan elke dag om middernacht (UTC) uitgevoerd.

     ![ Scan Dagelijks ](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Voer de **[!UICONTROL Email Address]** in waar u meldingen van voltooide scans en beveiligingsupdates wilt ontvangen.

   ![ E-mailadres ](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Klik op **[!UICONTROL Submit]** als de bewerking is voltooid.

   Nadat de eigendom van het domein is gecontroleerd, wordt de site weergegeven in de lijst Gecontroleerde websites van uw Commerce-account.

1. Als u meerdere websites met verschillende domeinen hebt, herhaalt u dit proces om voor elke website een beveiligingsscan in te stellen.
