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

Het archief van de Acties Admin [ ](action-log.md) maakt een lijst van de CSV logboekdossiers die op de server worden opgeslagen. In de configuratie, kunt u specificeren hoe lang de logboekingangen worden opgeslagen, en hoe vaak zij worden gearchiveerd. Standaard bevat de bestandsnaam de huidige datum in de ISO-indeling:  `yyyyMMddHH`

>[!NOTE]
>
>Het archiveren van het logboek vereist a [ cron baan ](cron.md) om opstelling te zijn.

## Logarchief configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Admin Actions Log Archiving]** sectie uit en plaats deze opties:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Voer het aantal dagen in dat u de logbestandvermeldingen in de database wilt behouden voordat ze worden verwijderd.
   - **[!UICONTROL Log Archiving Frequency]** — Ingesteld op `Daily` , `Weekly` of `Monthly` .

   ![ Geavanceerde configuratie - het archiveren van het admin actielogboek ](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van de configuratiemontages, zie [ Logarchivering van Acties Admin ](../configuration-reference/advanced/system.md) in de _Verwijzing van de Configuratie_.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Het archief weergeven

Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![ archief van het Logboek van de Actie ](./assets/action-log-archive.png){width="600" zoomable="yes"}
