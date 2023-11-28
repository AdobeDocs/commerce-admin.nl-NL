---
title: E-mails over verkoop
description: Leer hoe te om verkoope-mails te vormen om mededelingen aan klanten over hun orden te steunen.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# E-mails over verkoop

Verschillende e-mailberichten worden geactiveerd door de gebeurtenissen met betrekking tot een bestelling en de configuratie is vergelijkbaar. Zorg ervoor dat u het opslagcontact identificeert dat als afzender van het bericht verschijnt, het te gebruiken e-mailmalplaatje, en iedereen anders die een exemplaar van het bericht moet ontvangen. Verkoop-e-mails kunnen worden verzonden wanneer ze worden geactiveerd door een gebeurtenis of door een vooraf bepaald interval.

![Verkoopconfiguratie - e-mails over verkoop](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Stap 1. E-mailsjablonen bijwerken

Zorg ervoor dat u de [e-mailheader](../systems/email-template-custom.md#header-template) een sjabloon die uw merk weerspiegelt en zo nodig de andere e-mailsjablonen. Voor een volledige lijst met sjablonen raadpleegt u [E-mailsjablonen](../systems/email-templates.md).

## Stap 2. Het type verzending kiezen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales Emails]**.

1. Indien nodig uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de  **[!UICONTROL General Settings]** sectie.

   ![Verkoopconfiguratie - algemene instellingen voor e-mail voor verkoop](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Standaard is Asynchroon verzenden ingesteld op `Disable`. Als u de systeeminstelling wilt wijzigen, wist u de knop **[!UICONTROL Use system value]** selectievakje en set **[!UICONTROL Asynchronous sending]** op een van de volgende wijzen:

   - `Disable` - Verzendt een e-mail over de verkoop wanneer deze door een gebeurtenis wordt geactiveerd.
   - `Enable` - Verstuurt verkoopberichten op vooraf bepaalde, regelmatige intervallen.

   Adobe Commerce Support raadt u aan asynchrone verzending in te schakelen om de prestaties voor het plaatsen van bestellingen te verbeteren. Zie [Best practices voor configuratie voor verwerking van bestellingen](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) in Adobe Commerce Support Knowledge Base.

## Stap 3. Voer de gegevens voor elk e-mailbericht in

1. Indien nodig uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie.

   ![Verkoopconfiguratie - e-mailbestelling voor verkoop](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Controleren of **[!UICONTROL Enabled]** is ingesteld op `Yes` (standaard).

1. Set **[!UICONTROL New Order Confirmation Email]** aan het opslagcontact dat als afzender van het bericht verschijnt.

1. Set **[!UICONTROL New Order Confirmation Template]** naar de sjabloon die wordt gebruikt voor de e-mail die naar geregistreerde klanten wordt verzonden.

1. Set **[!UICONTROL New Order Confirmation Template for Guest]** naar de sjabloon die wordt gebruikt voor het e-mailbericht dat wordt verzonden naar gasten die geen account bij uw winkel hebben.

1. Voor **[!UICONTROL Send Order Email Copy To]**, voert u het e-mailadres in van iedereen die een kopie van de nieuwe bestelling per e-mail ontvangt.

   Als u een kopie naar meerdere ontvangers verzendt, scheidt u elk adres met een komma.

1. Set **[!UICONTROL Send Order Email Copy Method]** op een van de volgende wijzen:

   - `Bcc` - verzendt een _blinde, hoffelijke kopie_ door de ontvanger op te nemen in de koptekst van dezelfde e-mail die naar de klant is verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
   - `Separate Email` - Hiermee verzendt u de kopie als een aparte e-mail.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Order Comments]** en herhaalt u deze stappen.

   ![Verkoopconfiguratie - Opmerkingen bij verkooporders](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Voltooi de configuratie voor de overige e-mailtypen voor de verkoop:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Klik op **[!UICONTROL Save Config]**.

   Klik op de knop [Cachebeheer](../systems/cache-management.md) in het bericht boven aan de werkruimte en wis alle ongeldige caches.
