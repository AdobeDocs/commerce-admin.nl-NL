---
title: Productwaarschuwingen
description: Meer informatie over productwaarschuwingen en hoe u deze kunt gebruiken om klanten op de hoogte te stellen van de voorraadstatus en prijswijzigingen voor producten.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Productwaarschuwingen

Klanten kunnen zich op twee soorten waarschuwingen abonneren via e-mail - berichten over prijswijziging en waarschuwingen in voorraad. Voor elk type alarm, kunt u bepalen als de klanten kunnen intekenen, het e-mailmalplaatje selecteren dat wordt gebruikt, en de afzender van e-mail identificeren.

![&#x200B; Teken omhoog voor een productalarm &#x200B;](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Waarschuwing prijswijziging

Wanneer het alarm van de prijsverandering wordt toegelaten, stelt a _me op de hoogte wanneer de prijsdalingen_ verbinding op elke productpagina verschijnt. Klanten kunnen op de koppeling klikken om zich te abonneren op waarschuwingen met betrekking tot het product. Gasten wordt gevraagd om een account bij uw winkel te openen. Telkens wanneer de prijs verandert of het product bijzonder wordt, ontvangt iedereen die zich op de waarschuwing heeft geabonneerd een e-mailbericht.

## Waarschuwingen in de voorraadboekhouding

Het alarm in voorraad leidt tot een verbinding genoemd _deelt me mee wanneer dit product in voorraad_ voor elk product is dat uit voorraad is. Klanten kunnen op de koppeling klikken om zich te abonneren op de waarschuwing. Wanneer het product weer in voorraad is, ontvangen klanten een e-mail bericht dat het product beschikbaar is. De producten met alarm hebben het 1&rbrace; lusje van de Alarm van het Product van a _&lbrace;in het paneel van de Informatie van het Product dat van de klanten een lijst maakt die aan een alarm hebben ingetekend._

![&#x200B; Lijst van product en prijsalarm abonnementen &#x200B;](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Productwaarschuwingen instellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Klik om de sectie _[!UICONTROL Product Alerts]_&#x200B;uit te vouwen en voer de volgende handelingen uit:

   ![&#x200B; de Alarm van het Product &#x200B;](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Allow Alert When Product Price Changes]** in op `Yes` om waarschuwingen over prijswijzigingen aan uw klanten aan te bieden.

   - Stel **[!UICONTROL Price Alert Email Template]** in op de sjabloon die u wilt gebruiken voor berichten over prijswaarschuwingen.

   - Stel **[!UICONTROL Allow Alert When Product Comes Back in Stock]** in op `Yes` als u waarschuwingen wilt ontvangen wanneer producten uit de voorraad weer beschikbaar komen.

     >[!NOTE]
     >
     >_deelt me mee wanneer dit product in voorraad_ bericht verschijnt slechts wanneer **[!UICONTROL Display Out of Stock Products]** aan `Yes` (in de Configuratie bij [!UICONTROL Catalog] > [!UICONTROL Inventory] wordt geplaatst).

   - Stel **[!UICONTROL Stock Alert Email Template]** in op de sjabloon die u wilt gebruiken voor waarschuwingen over productvoorraad.

   - Plaats **[!UICONTROL Alert Email Sender]** aan het [&#x200B; opslagcontact &#x200B;](../getting-started/store-details.md#store-email-addresses){target="_blank"} dat u als afzender van het e-mailalarm wilt verschijnen. Leer meer over [&#x200B; opslag e-mailadressen &#x200B;](../configuration-reference/general/store-email-addresses.md){target="_blank"} in de gids van de kerngebruiker.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## E-mailsjablonen voor productwaarschuwingen configureren

Vervolgens configureert, voegt u de e-mailsjabloon toe of wijzigt u de prijswaarschuwing. Mogelijk wilt u de configuraties voor prijswaarschuwingen bewerken nadat u aanvullende templates hebt gemaakt.

Voor meer gedetailleerde informatie over het gebruiken van e-mailoverseinen, zie [&#x200B; Malplaatjes van het Bericht &#x200B;](../systems/email-template-custom.md#message-templates) in de _Gids van Systemen Admin_.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klik op **[!UICONTROL Add New Template]**.

1. Onder _het standaardmalplaatje van de Lading_, kies **[!UICONTROL Template]** dat u wilt aanpassen.

   U kunt de waarschuwingssjabloon kiezen die bij uw thema is inbegrepen. U kunt ook de sjablonen `Price Alert` of `Stock Alert` onder _[!UICONTROL Magento_PriceAlert]_&#x200B;selecteren.

1. Klik op **[!UICONTROL Load Template]**.

1. Voer een **[!UICONTROL Template Name]** in.

   U kunt deze naam in de _Waarschuwingen van de Prijs_ configuratie selecteren.

1. Lees de bestaande inhoud door en breng indien nodig wijzigingen aan voor het volgende:

   | Veld | Beschrijving |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Deze tekst wordt weergegeven in de onderwerpregel van een e-mail. |
   | [!UICONTROL Template Content] | Deze tekst wordt weergegeven in de volledige inhoud van de verzonden e-mail. |

1. Als u gegenereerde informatie uit [!DNL Commerce] -gegevens wilt toevoegen, gebruikt u de optie **[!UICONTROL Insert Variable]** om een lijst met beschikbare variabelen te gebruiken.

1. Klik op **[!UICONTROL Save Template]**.

## Instellingen voor productwaarschuwingen

Met deze instellingen kunt u bepalen hoe vaak [!DNL Commerce] controleert op wijzigingen waarvoor waarschuwingen moeten worden verzonden. U kunt ook de ontvanger, afzender en sjabloon selecteren voor e-mailberichten die worden verzonden als het verzenden van waarschuwingen mislukt.

![&#x200B; de Waakzame Montages van de Looppas van het Product &#x200B;](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Product Alerts Run Settings]** sectie uit.

1. Stel **[!UICONTROL Frequency]** in op een van de volgende opties om te bepalen hoe vaak productwaarschuwingen worden verzonden:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Stel **[!UICONTROL Start Time]** in op het uur, de minuut en de seconde om te bepalen op welk tijdstip productwaarschuwingen worden verzonden.

   >[!NOTE]
   >
   >Productwaarschuwingen worden verzonden door de consument &quot;product_alert&quot;.

1. Voer bij **[!UICONTROL Error Email Recipient]** de e-mail in van de persoon met wie contact moet worden opgenomen als er een fout optreedt.

1. Selecteer voor de **[!UICONTROL Error Email Sender]** de opslagidentiteit die wordt weergegeven als de afzender van de foutmelding.

1. Stel **[!UICONTROL Error Email Template]** in op de transactionele e-mailsjabloon die moet worden gebruikt voor de foutmelding.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
