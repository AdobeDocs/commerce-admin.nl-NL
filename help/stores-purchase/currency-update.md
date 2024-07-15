---
title: Valuta's bijwerken
description: Klik hier als je wilt weten hoe je de valutakoersen handmatig instelt of ze in je winkel importeert.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Valuta&#39;s bijwerken

De wisselkoersen kunnen handmatig worden ingesteld of in de winkel worden geïmporteerd. Om ervoor te zorgen dat je winkel de meest actuele tarieven heeft, kunt je de valutakoersen configureren om automatisch en volgens schema te worden bijgewerkt.

Alvorens deviezentarieven in te voeren, voltooi de [ opstelling van het munttarief ](currency-configuration.md) om de valuta te specificeren die u goedkeurt, en de de invoerverbinding en planning te vestigen.

![ Wisselkoersen ](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Een valutakoers handmatig bijwerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Klik op de wisselkoers die u wilt wijzigen en voer de nieuwe waarde in voor elke valuta die wordt ondersteund.

1. Klik op **[!UICONTROL Save Currency Rates]** als de bewerking is voltooid.

## Valuta-invoer

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Stel **[!UICONTROL Import Service]** in op de valutaprovider.

   De standaardprovider is `fixer.io (legacy)` .

   >[!IMPORTANT]
   >
   >Beginnend met versie 2.4.6, wordt de [[!DNL Fixer.io] ](https://fixer.io/) dienst afgekeurd en met de [[!DNL Fixer API]  vervangen (APILayer) ](https://apilayer.com/marketplace/fixer-api) dienst. Het wordt ten zeerste aanbevolen een APILayer-account te gebruiken in plaats van een afgekeurd [!DNL Fixer.io] -account.

1. Klik op **[!UICONTROL Import]**.

   De bijgewerkte snelheden worden weergegeven in de lijst van _[!UICONTROL Currency Rates]_. Als de tarieven sinds de laatste update zijn gewijzigd, wordt hieronder de oude koers ter referentie weergegeven.

1. Klik op **[!UICONTROL Save Currency Rates]** als de bewerking is voltooid.

1. Wanneer u wordt gevraagd de cache bij te werken, klikt u op de koppeling **[!UICONTROL Cache Management]** en vernieuwt u de ongeldige cache.

   ![ bericht van het Systeem - vernieuw het ongeldige geheime voorgeheugen ](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Valuta&#39;s volgens schema importeren

1. Zorg ervoor dat [ het Gewas ](../systems/cron.md) voor uw opslag wordt toegelaten.

1. Om de valuta te specificeren die u goedkeurt en de de invoerverbinding en programma vestigt, voltooi de [ Opstelling van het Tarief van de Valuta ](currency-configuration.md).

1. Controleer de lijst met _[!UICONTROL Currency Rates]_om te controleren of de tarieven volgens schema worden geïmporteerd.

1. Wacht op de periode van de frequentie die voor het schema wordt bepaald en controleer opnieuw de tarieven.
