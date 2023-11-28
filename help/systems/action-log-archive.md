---
title: Archief van handelingenlogboek
description: Leer hoe u het archief van het handelingenlogboek voor Admin configureert en bekijkt.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Archief van handelingenlogboek

{{ee-feature}}

De beheerder [handelingen](action-log.md) In archief worden de CSV-logbestanden weergegeven die op de server zijn opgeslagen. In de configuratie, kunt u specificeren hoe lang de logboekingangen worden opgeslagen, en hoe vaak zij worden gearchiveerd. Standaard bevat de bestandsnaam de huidige datum in de ISO-indeling:  `yyyyMMddHH`

>[!NOTE]
>
>Voor archivering van logbestanden is een [snijtaak](cron.md) op te zetten.

## Logarchief configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Admin Actions Log Archiving]** en stel de volgende opties in:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Voer het aantal dagen in dat u de logbestandvermeldingen in de database wilt bewaren voordat ze worden verwijderd.
   - **[!UICONTROL Log Archiving Frequency]** — Instellen op `Daily`, `Weekly`, of `Monthly`.

   ![Geavanceerde configuratie - archivering van logbestanden met beheeracties](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van de configuratiemontages, zie [Logbestand voor beheeracties archiveren](../configuration-reference/advanced/system.md) in de _Configuratieverwijzing_.

1. Klik op **[!UICONTROL Save Config]**.

## Het archief weergeven

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archief van handelingenlogboek](./assets/action-log-archive.png){width="600" zoomable="yes"}
