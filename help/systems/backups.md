---
title: Systeemback-ups
description: Leer hoe u systeemback-ups maakt en plant, inclusief het bestandssysteem, de database en mediabestanden.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Systeemback-ups

Met Adobe Commerce en Magento Open Source kunt u back-ups maken van verschillende onderdelen van het systeem, zoals het bestandssysteem, de database en de mediabestanden, en deze automatisch terugdraaien. Er wordt een record voor elke back-up weergegeven in het raster van het dialoogvenster _Back-ups_ pagina. Als u een record uit de lijst verwijdert, wordt ook het gearchiveerde bestand verwijderd. Back-upbestanden van databases worden gecomprimeerd in de GZ-indeling. Voor de systeemsteunen en de gegevensbestand en media steunen, wordt het formaat TGZ gebruikt. U kunt het beste de toegang tot back-uptools beperken en back-ups maken voordat u extensies en updates installeert.

- **Toegang tot back-uptools beperken.** De toegang tot de steunen en het hulpmiddel van het rolbackbeheer kan worden beperkt door te vormen [gebruikersrollen](permissions-user-roles.md) voor back-up- en terugdraaibronnen. Als u de toegang wilt beperken, schakelt u het desbetreffende selectievakje niet in. Om toegang tot terugschroeven van prijzen te verlenen, moet u toegang tot reservemiddelen ook verlenen.

- **Maak een back-up voordat u extensies en updates installeert.** Maak altijd een back-up voordat u een extensie of update installeert.

{{$include /help/_includes/backups-note.md}}

## Back-ups inschakelen en plannen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Backup Settings]**.

1. Set **[!UICONTROL Enabled Schedule Backup]** tot `Yes`.

1. Stel de planningsopties in om automatische back-ups te plannen:

   - Set **[!UICONTROL Enabled Schedule Backup]** tot `Yes`.
   - Set **[!UICONTROL Scheduled Backup Type]** naar het type back-up dat met het geplande interval moet worden uitgevoerd.
   - Set **[!UICONTROL Start Time]** tot het tijdstip waarop de back-upbewerking wordt uitgevoerd.
   - Set **[!UICONTROL Frequency]** tot `Daily`, `Weekly`, of `Monthly`.
   - Set **[!UICONTROL Maintenance Mode]** tot `Yes`.

   ![Geavanceerde configuratie - back-ups](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Een back-up maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Klik in de rechterbovenhoek op het type back-up dat u wilt maken:

   - **[!UICONTROL System Backup]** - Maakt een volledige back-up van de database en het bestandssysteem. Tijdens het proces kunt u ervoor kiezen om de mediamap op te nemen in de back-up.

   - **[!UICONTROL Database and Media Backup]** - Maakt een back-up van de database en de mediamap.

   - **[!UICONTROL Database Backup]** - Maakt een back-up van de database.

   ![Systeemgereedschappen - back-ups](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Schakel het selectievakje in om de opslagruimte tijdens de back-up in de onderhoudsmodus te zetten.

   Wanneer de back-up is voltooid, wordt de onderhoudsmodus automatisch uitgeschakeld.

1. Selecteer voor een systeemback-up de optie **[!UICONTROL Include Media folder to System Backup]** Schakel het selectievakje in om de mediamap op te nemen.

1. Bevestig de actie wanneer daarom wordt gevraagd.


