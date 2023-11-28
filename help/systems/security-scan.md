---
title: Beveiligingsscan
description: Leer hoe u een uitgebreide beveiligingsscan uitvoert en elk van uw Adobe Commerce- en Magento Open Source-sites controleert.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '616'
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

Het gereedschap Beveiligingsscan is gratis beschikbaar vanaf het dashboard van uw [Handelsrekening](../getting-started/commerce-account-create.md). Voor technische informatie, zie [Het gereedschap Beveiligingsscan instellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) in de _Handleiding voor handel in Cloud-infrastructuur_.

![Beveiligingsscan](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Een beveiligingsscan uitvoeren

1. Ga naar de homepage van de Handel en meld u aan bij uw [Handelsrekening](../getting-started/commerce-account-create.md) en voer de volgende handelingen uit:

   - Kies in het linkerdeelvenster de optie **[!UICONTROL Security Scan]**.
   - Klik op **[!UICONTROL Go to Security Scan]**.
   - Lees de **[!UICONTROL Terms and Conditions]**.
   - Klikken **[!UICONTROL Agree]** om door te gaan.

1. Op de _[!UICONTROL Monitored Websites]_pagina, klikt u **[!UICONTROL +Add Site]**.

   Als u meerdere sites met verschillende domeinen hebt, moet u een aparte scan voor elk domein configureren.

   ![Gecontroleerde sites](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit om te controleren of u eigenaar bent van het sitedomein door een bevestigingscode toe te voegen:

   **Handelswinkel**:

   - Voer de **[!UICONTROL Site URL]** en **[!UICONTROL Site Name]**.
   - Klik op **[!UICONTROL Generate Confirmation Code]**.
   - Klikken **Kopiëren** om de bevestigingscode naar het klembord te kopiëren.

     ![Bevestigingscode genereren](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Meld u aan bij de beheerder van uw winkel als een gebruiker met volledige beheerdersrechten en voer de volgende handelingen uit:

      - In de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Zoek uw site in de lijst en klik op **[!UICONTROL Edit]**.
      - Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL HTML Head]** sectie.
      - Omlaag schuiven naar **[!UICONTROL Scripts and Style Sheets]** en klik in het tekstvak aan het einde van een bestaande code en plak de bevestigingscode in het tekstvak.

        ![Scripts en stijlbladen](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Klik op **[!UICONTROL Save Configuration]**.

   **PWA storefront**:

   - Voer de **[!UICONTROL Site URL]** en **[!UICONTROL Site Name]**.

   - Voor **[!UICONTROL Confirmation Code]**, kiest u de `META Tag` en klik vervolgens op **[!UICONTROL Generate Code]**.

   - Klikken **[!UICONTROL Copy]** om de gegenereerde bevestigingscode META-tag naar het klembord te kopiëren.

     ![Bevestigingscode genereren](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Ga naar de PWA Studio storefront projectfolder en doe het volgende:

      - Ga onder de projectfolder van de PWA Studio naar `packages > venia-concept > template.html`.
      - Voeg de gekopieerde bevestigingscode (de gegenereerde META-tag) toe aan de kop van de HTML en sla de wijzigingen op.

        ![Bevestigingscode kopiëren](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Ga terug naar PWA Studio CLI, en gebruik garen om projectgebiedsdelen te installeren en het project in werking te stellen bouwt bevel.

        ```sh
        yarn install &&
        yarn build
        ```

      - *In uw Cloud-project*, een `pwa` map en kopieer de inhoud binnen het project van uw winkel `dist` map.

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

1. Terugkeren naar de _[!UICONTROL Security Scan]_pagina in je Commerce-account en klik op **[!UICONTROL Verify Confirmation Code]**om vast te stellen wie het domein is.

1. Na een succesvolle bevestiging, vorm **[!UICONTROL Set Automatic Security Scan]** opties voor een van de volgende typen:

   **Wekelijks scannen (aanbevolen)**:

   - Kies de optie **[!UICONTROL Week Day]**, **[!UICONTROL Time]**, en **[!UICONTROL Time Zone]** de scan elke week moet plaatsvinden.
   - Standaard wordt de scan elke week om middernacht zaterdag, UTC en verder naar begin zondag gepland.

     ![Wekelijks scannen](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Dagelijks scannen**:

   - Kies de optie **[!UICONTROL Time]**, en **[!UICONTROL Time Zone]** dat de scan elke dag moet plaatsvinden.
   - Standaard wordt de scan elke dag om middernacht (UTC) uitgevoerd.

     ![Dagelijks scannen](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Voer de **[!UICONTROL Email Address]** waar u meldingen wilt ontvangen van voltooide scans en beveiligingsupdates.

   ![E-mailadres](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Klik op **[!UICONTROL Submit]**.

   Nadat de eigendom van het domein is geverifieerd, wordt de site weergegeven in de lijst Gecontroleerde websites van uw Commerce-account.

1. Als u meerdere websites met verschillende domeinen hebt, herhaalt u dit proces om voor elke website een beveiligingsscan in te stellen.
