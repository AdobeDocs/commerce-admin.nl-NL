---
title: Melding betalingsfout
description: Leer hoe u e-mailcommunicatie configureert voor een betalingsmethode die een transactie niet kan voltooien.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Melding betalingsfout

Er wordt een melding verzonden naar de contactpersoon van de winkel of naar een aangewezen Admin-gebruiker als de tijdens het afrekenen geselecteerde betalingsmethode de transactie niet voltooit.

## Stap 1: de e-mailsjabloon bijwerken

Zorg ervoor dat u de vereiste e-mailsjabloon hebt bijgewerkt met uw merk. Voor een volledige lijst met sjablonen raadpleegt u [E-mailsjabloonlijst](../systems/email-templates.md#email-template-list).

## Stap 2: de betalings mislukte e-mails configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Checkout]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Payment Failed Emails]** sectie.

   ![Betaling is mislukt](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Stel de opties voor mislukte e-mails voor betaling in:

   - Set **[!UICONTROL Payment Failed Email Sender]** aan het opslagcontact dat als afzender van het bericht verschijnt.
   - Set **[!UICONTROL Payment Failed Email Receiver]** naar de contactpersoon van de winkel die meldingen ontvangt over mislukte e-mailverzendingen.
   - Set **[!UICONTROL Payment Failed Template]** naar de sjabloon die wordt gebruikt voor de e-mail die wordt verzonden wanneer de betalingsmethode tijdens het uitchecken mislukt.

1. Voor **[!UICONTROL Send Payment Failed Email Copy To]**, voert u het e-mailadres in van iedereen die een kopie van de melding van een betalingsfout moet ontvangen.

   Als u een kopie naar meerdere ontvangers verzendt, scheidt u elk adres met een komma.

1. Set **[!UICONTROL Payment Failed Copy Method]** op een van de volgende wijzen:

   - `Bcc` - verzendt een _blinde, hoffelijke kopie_ door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
   - `Separate Email` - Hiermee verzendt u de kopie als een aparte e-mail.

1. Klik op **[!UICONTROL Save Config]**.
