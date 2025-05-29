---
title: Systeemback-ups
description: Leer hoe u systeemback-ups maakt en plant, inclusief het bestandssysteem, de database en mediabestanden.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Systeemback-ups

Met Adobe Commerce en Magento Open Source kunt u back-ups maken van verschillende onderdelen van het systeem, zoals het bestandssysteem, de database en de mediabestanden, en automatisch terugdraaien. Een verslag voor elke steun verschijnt in het net op de _pagina van Steunen_. Als u een record uit de lijst verwijdert, wordt ook het gearchiveerde bestand verwijderd. Back-upbestanden van databases worden gecomprimeerd in de GZ-indeling. Voor de systeemsteunen en de gegevensbestand en media steunen, wordt het formaat TGZ gebruikt. U kunt het beste de toegang tot back-uptools beperken en back-ups maken voordat u extensies en updates installeert.

- **Beperk toegang tot reservehulpmiddelen.** De toegang tot de steunen en het hulpmiddel van het het rolbackbeheer kan worden beperkt door [ gebruikersrollen ](permissions-user-roles.md) voor steun en rolbackmiddelen te vormen. Als u de toegang wilt beperken, schakelt u het desbetreffende selectievakje niet in. Om toegang tot terugschroeven van prijzen te verlenen, moet u toegang tot reservemiddelen ook verlenen.

- **file alvorens uitbreidingen en updates te installeren.** Maak altijd een back-up voordat u een extensie installeert of bijwerkt.

{{$include /help/_includes/backups-note.md}}

## Back-ups inschakelen en plannen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit **[!UICONTROL Backup Settings]**.

1. Stel **[!UICONTROL Enabled Schedule Backup]** in op `Yes` .

1. Stel de planningsopties in om automatische back-ups te plannen:

   - Stel **[!UICONTROL Enabled Schedule Backup]** in op `Yes` .
   - Stel **[!UICONTROL Scheduled Backup Type]** in op het type back-up dat met het geplande interval moet worden uitgevoerd.
   - Stel **[!UICONTROL Start Time]** in op het tijdstip van de dag waarop de back-upbewerking moet worden uitgevoerd.
   - Stel **[!UICONTROL Frequency]** in op `Daily` , `Weekly` of `Monthly` .
   - Stel **[!UICONTROL Maintenance Mode]** in op `Yes` .

   ![ Geavanceerde configuratie - steunen ](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Een back-up maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Klik in de rechterbovenhoek op het type back-up dat u wilt maken:

   - **[!UICONTROL System Backup]** - Maakt een volledige back-up van de database en het bestandssysteem. Tijdens het proces kunt u ervoor kiezen om de mediamap op te nemen in de back-up.

   - **[!UICONTROL Database and Media Backup]** - Maakt een back-up van de database en de mediamap.

   - **[!UICONTROL Database Backup]** - Maakt een back-up van de database.

   ![ hulpmiddelen van het Systeem - steunen ](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Schakel het selectievakje in om de opslagruimte tijdens de back-up in de onderhoudsmodus te zetten.

   Wanneer de back-up is voltooid, wordt de onderhoudsmodus automatisch uitgeschakeld.

1. Voor een systeemback-up schakelt u het selectievakje **[!UICONTROL Include Media folder to System Backup]** in om de mediamap op te nemen.

1. Bevestig de actie wanneer daarom wordt gevraagd.


