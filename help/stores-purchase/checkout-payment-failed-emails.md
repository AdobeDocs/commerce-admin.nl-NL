---
title: Melding betalingsfout
description: Leer hoe u e-mailcommunicatie configureert voor een betalingsmethode die een transactie niet kan voltooien.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Melding betalingsfout

Er wordt een melding verzonden naar de contactpersoon van de winkel of naar een aangewezen Admin-gebruiker als de tijdens het afrekenen geselecteerde betalingsmethode de transactie niet voltooit.

## Stap 1: de e-mailsjabloon bijwerken

Zorg ervoor dat u de vereiste e-mailsjabloon hebt bijgewerkt met uw merk. Voor een volledige lijst van malplaatjes, zie [ Lijst van het Malplaatje E-mail ](../systems/email-templates.md#email-template-list).

## Stap 2: de betalings mislukte e-mails configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Payment Failed Emails]** sectie uit.

   ![ Betaling Ontbroken E-mail ](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Stel de opties voor mislukte e-mails voor betaling in:

   - Stel **[!UICONTROL Payment Failed Email Sender]** in op de opslagcontactpersoon die wordt weergegeven als de afzender van het bericht.
   - Stel **[!UICONTROL Payment Failed Email Receiver]** in op de contactpersoon van de winkel die meldingen van mislukte e-mailverzendingen ontvangt.
   - Stel **[!UICONTROL Payment Failed Template]** in op de sjabloon die wordt gebruikt voor de e-mail die wordt verzonden wanneer de betalingsmethode tijdens het uitchecken mislukt.

1. Voer voor **[!UICONTROL Send Payment Failed Email Copy To]** het e-mailadres in van iedereen die een kopie van de melding wegens betalingsfout moet ontvangen.

   Als u een kopie naar meerdere ontvangers verzendt, scheidt u elk adres met een komma.

1. Stel **[!UICONTROL Payment Failed Copy Method]** in op een van de volgende opties:

   - `Bcc` - verzendt a _blinde beleefdheidsexemplaar_ door de ontvanger in de kopbal van zelfde e-mail te omvatten die naar de klant wordt verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
   - `Separate Email` - Verzendt de kopie als een aparte e-mail.

1. Klik op **[!UICONTROL Save Config]**.
