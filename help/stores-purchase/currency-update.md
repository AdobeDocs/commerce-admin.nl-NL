---
title: Valuta's bijwerken
description: Klik hier als je wilt weten hoe je de valutakoersen handmatig instelt of ze in je winkel importeert.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Valuta&#39;s bijwerken

De wisselkoersen kunnen handmatig worden ingesteld of in de winkel worden geïmporteerd. Om ervoor te zorgen dat je winkel de meest actuele tarieven heeft, kunt je de valutakoersen configureren om automatisch en volgens schema te worden bijgewerkt.

Voordat u valutakoersen importeert, moet u de [valutawissel instellen](currency-configuration.md) om de valuta&#39;s te specificeren die u accepteert, en om de verbinding en het schema voor het importeren te vestigen.

![Valuta](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Een valutakoers handmatig bijwerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Klik op de wisselkoers die u wilt wijzigen en voer de nieuwe waarde in voor elke valuta die wordt ondersteund.

1. Klik op **[!UICONTROL Save Currency Rates]**.

## Valuta-invoer

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Set **[!UICONTROL Import Service]** aan de valutaverstrekker.

   De standaardprovider is `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >Vanaf de release van 2.4.6 kunt u [[!DNL Fixer.io]](https://fixer.io/) service is vervangen door de [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) service. Het wordt ten zeerste aanbevolen om een APILayer-account te gebruiken in plaats van een vervangen account [!DNL Fixer.io] account.

1. Klik op **[!UICONTROL Import]**.

   De bijgewerkte tarieven verschijnen in _[!UICONTROL Currency Rates]_lijst. Als de tarieven sinds de laatste update zijn gewijzigd, wordt hieronder de oude koers ter referentie weergegeven.

1. Klik op **[!UICONTROL Save Currency Rates]**.

1. Klik op de knop **[!UICONTROL Cache Management]** de ongeldige cache koppelen en vernieuwen.

   ![Systeembericht - de ongeldige cache vernieuwen](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Valuta&#39;s volgens schema importeren

1. Controleer of [Cron](../systems/cron.md) is ingeschakeld voor uw winkel.

1. Als u de valuta&#39;s wilt opgeven die u accepteert en de importverbinding en het schema wilt instellen, voert u de opdracht [Instellen valutakoers](currency-configuration.md).

1. Als u wilt controleren of de tarieven volgens schema worden geïmporteerd, controleert u op de knop _[!UICONTROL Currency Rates]_lijst.

1. Wacht op de periode van de frequentie die voor het schema wordt bepaald en controleer opnieuw de tarieven.
