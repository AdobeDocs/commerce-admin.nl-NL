---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] pagina van de Commerce Admin.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Deze instellingen zijn beschikbaar wanneer [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) is geïnstalleerd.

![Sales Channel-instellingen](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Algemeen | Opties:<br/><br/>**`Once Daily`**: Schakel deze optie in om de historie van je winkelactiviteiten eenmaal per dag te wissen.<br/><br/>**`Once Weekly`**: Schakel deze optie in om de historie van je winkelactiviteiten één keer per week te wissen.<br/><br/>**`Once Monthly`**: (Standaard) Schakel deze optie in om de historie van je winkelactiviteiten één keer per maand te wissen. |
| [!UICONTROL Background Tasks (CRON) Source] | Algemeen | Selecteren `Magento CRON` om te bepalen dat de [!DNL Amazon Sales Channel] gebruikt de Cron-instellingen van de Handel om de communicatie- en gegevenssync-intervallen te bepalen met Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Algemeen | Selecteren `Enabled` om extra synchronisatiegegevens te verzamelen wanneer het oplossen van problemen nodig is.<br/><br/>Deze optie is standaard uitgeschakeld en moet alleen worden ingeschakeld wanneer dat nodig is voor het oplossen van problemen, omdat continue registratie negatieve gevolgen heeft voor de prestaties. Indien ingeschakeld voor probleemoplossing, moet dit na voltooiing worden uitgeschakeld.<br/><br/>**_Opmerking _**: Amazon Sales Channel log wordt geschreven naar de `/var/log/channel_amazon.log` en kan worden weergegeven in [ontwikkelmodus](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Algemeen | Selecteren `Enabled` om alle uitgaande status-veranderende API verzoeken te blokkeren. Mogelijke wijzigingen worden opgeslagen, maar niet verzonden, totdat de modus Alleen-lezen is uitgeschakeld. Selecteer `Disabled`.<br/><br/>Wanneer een database wordt gemigreerd naar een nieuwe kopie van de instantie (gedetecteerd wanneer de URL van een winkel in de configuratie verandert), wordt de modus Alleen-lezen automatisch ingeschakeld.<br/><br/>Dit is ontworpen voor gebruik op kopieën van het productieexemplaar, zoals _Staging_ of _QA_, en mag niet worden gebruikt op de productie-instantie.<br/><br/>**_Opmerking _**: De configuratiecache moet worden gewist voor [!UICONTROL Read-Only Mode] om in te schakelen. |

{:style=&quot;table-layout:auto&quot;}
