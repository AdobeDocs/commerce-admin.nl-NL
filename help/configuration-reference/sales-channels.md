---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] van Commerce Admin.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Deze instellingen zijn beschikbaar wanneer [[!DNL Amazon Sales Channel] ](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) is geïnstalleerd.

![ de Montages van Sales Channel ](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Algemeen | Opties:<br/><br/>**`Once Daily`**: selecteer deze optie om de activiteitengeschiedenis van uw winkel eenmaal per dag te wissen.<br/><br/>**`Once Weekly`**: Schakel deze optie in om de historie van de activiteiten van uw winkel één keer per week te wissen.<br/><br/>**`Once Monthly`**: (Standaard) Schakel deze optie in om de historie van de activiteiten van uw winkel één keer per maand te wissen. |
| [!UICONTROL Background Tasks (CRON) Source] | Algemeen | Selecteer `Magento CRON` om op te geven dat in [!DNL Amazon Sales Channel] de Commerce-instellingen voor uitsnijden worden gebruikt om de communicatie- en gegevenssync-intervallen te bepalen met Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Algemeen | Selecteer `Enabled` om extra synchronisatiegegevens te verzamelen wanneer het oplossen van problemen wordt vereist.<br/><br/> deze optie wordt onbruikbaar gemaakt door gebrek en zou slechts moeten worden toegelaten wanneer nodig voor het oplossen van problemen, aangezien het voortgezette registreren negatieve prestaties beïnvloedt. Indien ingeschakeld voor probleemoplossing, moet dit na voltooiing worden uitgeschakeld. |
| [!UICONTROL Read-Only Mode] | Algemeen | Selecteer `Enabled` om alle uitgaande toestandsveranderende API-aanvragen te blokkeren. Mogelijke wijzigingen worden opgeslagen, maar niet verzonden, totdat de modus Alleen-lezen is uitgeschakeld. Selecteer `Disabled` om de gegevensoverdracht opnieuw te starten.<br/><br/> wanneer een gegevensbestand aan een nieuw exemplaar van de instantie wordt gemigreerd (ontdekt wanneer URL van een opslag in de configuratie) verandert, read-only wijze wordt automatisch toegelaten.<br/><br/> dit wordt ontworpen voor gebruik op exemplaren van de productieinstantie, als _het Opvoeren_ of _QA_, en zou niet op de productieinstantie moeten worden gebruikt.<br/><br/>**_Nota _**: Het configuratiecache moet voor [!UICONTROL Read-Only Mode] worden ontruimd om toe te laten. |

{style="table-layout:auto"}
