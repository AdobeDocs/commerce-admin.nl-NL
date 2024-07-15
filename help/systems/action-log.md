---
title: Handelingenlogboeken
description: Leer over actielogboeken en hoe te om geregistreerde acties te vormen om u te helpen alle veranderingen volgen die aan uw opslag worden aangebracht.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Handelingenlogboeken

{{ee-feature}}

De functie Logs van de Actie registreert (registreert) elke verandering die door een gebruiker wordt aangebracht Admin die in uw opslag werkt. Zo kunt u alle wijzigingen bijhouden die in uw winkel zijn aangebracht. Het volgen van deze veranderingen, samen met het plaatsen van [ toestemmingen Admin ](permissions.md) voor een gebruiker, kan helpen om uw opslag tegen ongewenste veranderingen te beveiligen.

Voor de meeste Admin-acties bevat de geregistreerde informatie de actie, de naam van de gebruiker, het al dan niet slagen van de actie en de id van het object dat door de actie wordt beïnvloed. Het IP adres en de datum worden ook geregistreerd.

Standaard worden alle beheeracties ingeschakeld en geregistreerd. Als u Logboekregistratie voor beheeracties wilt configureren, controleert u de opties en schakelt u het selectievakje voor elk actietype in of uit. Adobe Commerce logt alleen geselecteerde typen in.

Bekijk het [ Logs Rapport van de Actie ](action-log-report.md) aan overzicht geregistreerde admin acties en details.

![ Geavanceerde configuratie - admin acties registreren ](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Voor een gedetailleerde lijst van de configuratiemontages, zie [ Logarchivering van Acties Admin ](../configuration-reference/advanced/system.md) in de _Verwijzing van de Configuratie_.

## Beheerdersacties configureren voor logbestanden

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Admin]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Admin Actions Logging]** sectie uit en doe het volgende voor elke actie:

   - Schakel het selectievakje in om het aanmelden bij Admin voor de handeling in te schakelen.
   - Schakel het selectievakje uit om het aanmelden bij Admin voor de handeling uit te schakelen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Logbestand met archiefbeheeracties

Logbestanden voor beheeracties kunnen gedurende een willekeurig aantal dagen worden gearchiveerd. Archiefbestanden kunnen ook na een opgegeven duur worden verwijderd.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Vouw **[!UICONTROL Admin Action Log Archiving]** uit en stel de opties in:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Stel het aantal dagen in waarop het gearchiveerde logbestand moet worden behouden.
   - **[!UICONTROL Log Archiving Frequency]** - Stel de frequentie in voor het maken van archieven.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
