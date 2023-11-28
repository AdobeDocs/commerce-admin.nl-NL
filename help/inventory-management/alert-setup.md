---
title: Productwaarschuwingen
description: Meer informatie over productwaarschuwingen en hoe u deze kunt gebruiken om klanten op de hoogte te stellen van de voorraadstatus en prijswijzigingen voor producten.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Productwaarschuwingen

Klanten kunnen zich op twee soorten waarschuwingen abonneren via e-mail - berichten over prijswijziging en waarschuwingen in voorraad. Voor elk type alarm, kunt u bepalen als de klanten kunnen intekenen, het e-mailmalplaatje selecteren dat wordt gebruikt, en de afzender van e-mail identificeren.

![Aanmelden voor een productwaarschuwing](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Waarschuwing prijswijziging

Wanneer waarschuwingen over prijswijzigingen zijn ingeschakeld, wordt een _Stuur me een bericht wanneer de prijs daalt_ op elke productpagina wordt een koppeling weergegeven. Klanten kunnen op de koppeling klikken om zich te abonneren op waarschuwingen met betrekking tot het product. Gasten wordt gevraagd om een account bij uw winkel te openen. Telkens wanneer de prijs verandert of het product bijzonder wordt, ontvangt iedereen die zich op de waarschuwing heeft geabonneerd een e-mailbericht.

## Waarschuwingen in de voorraadboekhouding

Met de waarschuwing in voorraad maakt u een koppeling met de naam _Stuur mij een melding wanneer dit product in voorraad is_ voor elk product dat uit voorraad is. Klanten kunnen op de koppeling klikken om zich te abonneren op de waarschuwing. Wanneer het product weer in voorraad is, ontvangen klanten een e-mail bericht dat het product beschikbaar is. Producten met waarschuwingen hebben een _Productwaarschuwingen_ in het venster Productinformatie waarin de klanten worden vermeld die zich op een waarschuwing hebben geabonneerd.

![Lijst met product- en prijswaarschuwingen](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Productwaarschuwingen instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Klik om de _[!UICONTROL Product Alerts]_en voer de volgende handelingen uit:

   ![Productwaarschuwingen](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Om berichten over prijswijzigingen aan uw klanten aan te bieden, stelt u **[!UICONTROL Allow Alert When Product Price Changes]** tot `Yes`.

   - Set **[!UICONTROL Price Alert Email Template]** aan de template die u wilt gebruiken voor berichten over prijswaarschuwingen.

   - Als u waarschuwingen wilt aanbieden wanneer producten uit de voorraad weer beschikbaar komen, stelt u **[!UICONTROL Allow Alert When Product Comes Back in Stock]** tot `Yes`.

     >[!NOTE]
     >
     >De _Stuur mij een melding wanneer dit product in voorraad is_ bericht wordt alleen weergegeven als **[!UICONTROL Display Out of Stock Products]** is ingesteld op `Yes` (in de Configuratie bij [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Set **[!UICONTROL Stock Alert Email Template]** in de template die u wilt gebruiken voor berichten over productvoorraad.

   - Set **[!UICONTROL Alert Email Sender]** aan de [contactpersoon voor winkel](../getting-started/store-details.md#store-email-addresses){target="_blank"} that you want to appear as the sender of the email alert. Learn more about [store email addresses](../configuration-reference/general/store-email-addresses.md){target="_blank"} in de basisgebruikershandleiding.

1. Klik op **[!UICONTROL Save Config]**.

## E-mailsjablonen voor productwaarschuwingen configureren

Vervolgens configureert, voegt u de e-mailsjabloon toe of wijzigt u de prijswaarschuwing. Mogelijk wilt u de configuraties voor prijswaarschuwingen bewerken nadat u aanvullende templates hebt gemaakt.

Voor meer gedetailleerde informatie over het gebruiken van e-mailoverseinen, zie [Berichttemplates](../systems/email-template-custom.md#message-templates) in de _Admin Systems Guide_.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klik op **[!UICONTROL Add New Template]**.

1. Onder _Standaardsjabloon laden_, kiest u de **[!UICONTROL Template]** die u wilt aanpassen.

   U kunt de waarschuwingssjabloon kiezen die bij uw thema is inbegrepen. U kunt ook de optie `Price Alert` of `Stock Alert` sjablonen onder _[!UICONTROL Magento_PriceAlert]_.

1. Klik op **[!UICONTROL Load Template]**.

1. Voer een **[!UICONTROL Template Name]**.

   U kunt deze naam selecteren in het dialoogvenster _Prijswaarschuwingen_ configuratie.

1. Lees de bestaande inhoud door en breng indien nodig wijzigingen aan voor het volgende:

   | Veld | Beschrijving |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Deze tekst wordt weergegeven in de onderwerpregel van een e-mail. |
   | [!UICONTROL Template Content] | Deze tekst wordt weergegeven in de volledige inhoud van de verzonden e-mail. |

1. Gegenereerde informatie toevoegen van [!DNL Commerce] gegevens gebruiken **[!UICONTROL Insert Variable]** gebruiken om een lijst met beschikbare variabelen te gebruiken.

1. Klik op **[!UICONTROL Save Template]**.

## Instellingen voor productwaarschuwingen

Met deze instellingen kunt u bepalen hoe vaak [!DNL Commerce] controleert op wijzigingen waarvoor waarschuwingen moeten worden verzonden. U kunt ook de ontvanger, afzender en sjabloon selecteren voor e-mailberichten die worden verzonden als het verzenden van waarschuwingen mislukt.

![Instellingen voor productwaarschuwingen](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Product Alerts Run Settings]** sectie.

1. Om te bepalen hoe vaak productwaarschuwingen worden verzonden, stelt u **[!UICONTROL Frequency]** op een van de volgende wijzen:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Om de tijd te bepalen van de dag dat productwaarschuwingen worden verzonden, stelt u **[!UICONTROL Start Time]** naar het uur, de minuut en de seconde.

   >[!NOTE]
   >
   >Productwaarschuwingen worden verzonden door de consument &quot;product_alert&quot;.

1. Voor **[!UICONTROL Error Email Recipient]** Voer de e-mail in van de persoon met wie contact moet worden opgenomen als er een fout optreedt.

1. Voor de **[!UICONTROL Error Email Sender]** selecteert u de opslagidentiteit die wordt weergegeven als de afzender van de foutmelding.

1. Set **[!UICONTROL Error Email Template]** naar de transactionele e-mailsjabloon die moet worden gebruikt voor de foutmelding.

1. Klik op **[!UICONTROL Save Config]**.
