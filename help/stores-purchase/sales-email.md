---
title: E-mails over verkoop
description: Leer hoe te om verkoope-mails te vormen om mededelingen aan klanten over hun orden te steunen.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# E-mails over verkoop

Verschillende e-mailberichten worden geactiveerd door de gebeurtenissen met betrekking tot een bestelling en de configuratie is vergelijkbaar. Zorg ervoor dat u het opslagcontact identificeert dat als afzender van het bericht verschijnt, het te gebruiken e-mailmalplaatje, en iedereen anders die een exemplaar van het bericht moet ontvangen. Verkoop-e-mails kunnen worden verzonden wanneer ze worden geactiveerd door een gebeurtenis of door een vooraf bepaald interval.

![ de configuratie van de Verkoop - verkoop e-mails ](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Stap 1. E-mailsjablonen bijwerken

Zorg ervoor om het [ e-mailkopbal ](../systems/email-template-custom.md#header-template) malplaatje bij te werken zodat het uw merk, en de andere e-mailmalplaatjes zoals nodig weerspiegelt. Voor een volledige lijst van malplaatjes, zie [ E-mailmalplaatjes ](../systems/email-templates.md).

## Stap 2. Het type verzending kiezen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales Emails]** .

1. Indien noodzakelijk, breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL General Settings]** sectie uit.

   ![ configuratie van de Verkoop - verkoop e-mail algemene montages ](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Standaard is Asynchroon verzenden ingesteld op `Disable` . Als u de systeeminstelling wilt wijzigen, schakelt u het selectievakje **[!UICONTROL Use system value]** uit en stelt u **[!UICONTROL Asynchronous sending]** in op een van de volgende opties:

   - `Disable` - Verstuurt een e-mail over de verkoop wanneer deze door een gebeurtenis wordt geactiveerd.
   - `Enable` - Verzendt een e-mail met vooraf bepaalde, regelmatige intervallen.

   Adobe Commerce Support raadt u aan asynchrone verzending in te schakelen om de prestaties voor het plaatsen van bestellingen te verbeteren. Zie [ beste praktijken van de Configuratie voor ordeverwerking ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) in de Kennisbank van de Steun van Adobe Commerce.

## Stap 3. Voer de gegevens voor elk e-mailbericht in

1. Indien noodzakelijk, breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie uit.

   ![ configuratie van de Verkoop - verkoop e-mailorde ](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Controleer of **[!UICONTROL Enabled]** is ingesteld op `Yes` (standaardwaarde).

1. Stel **[!UICONTROL New Order Confirmation Email]** in op de opslagcontactpersoon die wordt weergegeven als de afzender van het bericht.

1. Stel **[!UICONTROL New Order Confirmation Template]** in op de sjabloon die wordt gebruikt voor het e-mailbericht dat naar geregistreerde klanten wordt verzonden.

1. Stel **[!UICONTROL New Order Confirmation Template for Guest]** in op de sjabloon die wordt gebruikt voor het e-mailbericht dat wordt verzonden naar gasten die geen account bij uw winkel hebben.

1. Voer bij **[!UICONTROL Send Order Email Copy To]** het e-mailadres in van iedereen die een kopie van de e-mail met de nieuwe bestelling moet ontvangen.

   Als u een kopie naar meerdere ontvangers verzendt, scheidt u elk adres met een komma.

1. Stel **[!UICONTROL Send Order Email Copy Method]** in op een van de volgende opties:

   - `Bcc` - verzendt a _blinde beleefdheidsexemplaar_ door de ontvanger in de kopbal van zelfde e-mail te omvatten die naar de klant wordt verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
   - `Separate Email` - Verzendt de kopie als een aparte e-mail.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Order Comments]** sectie uit en herhaal deze stappen.

   ![ de configuratie van de Verkoop - de opmerkingen van de de ordeorde van de Verkoop ](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Voltooi de configuratie voor de overige e-mailtypen voor de verkoop:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

   Wanneer ertoe aangezet, klik de [&#128279;](../systems/cache-management.md) verbinding van het Beheer van het Geheime voorgeheugen  in het bericht bij de bovenkant van de werkruimte en ontruim alle ongeldige geheime voorgeheugens.
