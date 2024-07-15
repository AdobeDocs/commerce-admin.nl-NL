---
title: Ondersteuningsgereedschappen
description: Leer over de verstrekte steunhulpmiddelen die u kunt gebruiken om kwesties in uw systeem te identificeren.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Ondersteuningsgereedschappen

{{ee-feature}}

De hulpmiddelen van de steun worden ontworpen om bekende kwesties in uw systeem te identificeren. Ze kunnen worden gebruikt als een resource tijdens de ontwikkelings- en optimalisatieprocessen en als een diagnostische tool om ons ondersteuningsteam te helpen problemen te identificeren en op te lossen.

## Dataverzamelaar

De gegevensverzamelaar verzamelt de informatie over uw systeem die ons ondersteuningsteam nodig heeft om problemen met uw Adobe Commerce-installatie op te lossen. De gemaakte back-up duurt enkele minuten en bevat zowel een code- als een databasedump. De gegevens kunnen worden geëxporteerd naar een CSV- of Excel-XML-bestand.

![systeem - dataverzamelaar](./assets/data-collector.png){width="600" zoomable="yes"}

### De dataverzamelaar uitvoeren

1. Ga in de zijbalk _Admin_ naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL New Backup]**.

   Het genereren van de back-up duurt enkele minuten. U kunt de resultaten van de verwerking controleren door op **[!UICONTROL Refresh Status]** te klikken. Als de back-up is voltooid, wordt deze weergegeven in het raster _[!UICONTROL Data Collector]_.

1. Ga als volgt te werk om een logboek met de back-updetails weer te geven:

   - Selecteer in de kolom _[!UICONTROL Action]_de optie **[!UICONTROL Show Log]**.

   - Klik op **[!UICONTROL Back]** om terug te keren naar het raster.

   ![logboek gegevensverzamelaar](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Back-upgegevens exporteren

1. Schakel in de eerste kolom het selectievakje in van de back-up die u wilt exporteren.

1. Gebruik het menu **[!UICONTROL Export]** om de indeling van de exportdata te kiezen.

   ![exportindeling](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Open het bestand vanaf de downloadlocatie van de webbrowser en **[!UICONTROL Save]**.

### Back-upgegevens downloaden

Nadat de back-up is gegenereerd, kunt u de kopie van code- en databasegegevens downloaden.

1. Zoek de benodigde back-upeenheid in het raster.

1. Zorg ervoor dat de status `Complete` is.

1. Klik op de entiteitsnaam in de kolommen _[!UICONTROL Code Dump]_of_[!UICONTROL DB Dump]_.

Het downloadproces moet automatisch starten.

## Back-upgegevens verwijderen

1. Ga in de zijbalk _Beheerder_ naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Zoek en selecteer de back-upgegevens die u wilt verwijderen.

1. Klik in de kolom _[!UICONTROL Action]_op **[!UICONTROL Delete]**.

1. Klik op **[!UICONTROL OK]** om de actie te bevestigen.

## Systeemrapporten

Met de tool voor systeemrapportage kunt u periodieke volledige of gedeeltelijke momentopnamen van het systeem maken en opslaan voor toekomstig gebruik. U kunt prestatie-instellingen vergelijken voor en na cycli voor codeontwikkeling of wijzigingen in serverinstellingen. Met de systeemrapportagetool kunt u de tijd die nodig is voor het voorbereiden en indienen van de informatie die ondersteuning nodig heeft om een onderzoek te starten, aanzienlijk verkorten.

Vanuit het raster Systeemrapporten kunt u bestaande rapporten bekijken en downloaden, rapporten verwijderen en rapporten maken.

### Systeemrapporten openen

Ga op de zijbalk _Admin_ naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Beheerder - systeemrapporten](./assets/reports.png){width="600" zoomable="yes"}

### Een rapport genereren

1. Klik op **[!UICONTROL New Report]**.

1. Selecteer in de lijst **[!UICONTROL Groups]** elke set informatie die u in het rapport wilt opnemen. Standaard zijn alle groepen geselecteerd.

   ![Systeemrapport - groepen selecteren](./assets/report-create.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]**.

   Het kan een paar minuten duren voordat het rapport wordt gegenereerd, afhankelijk van het aantal geselecteerde rapporttypen. Wanneer het rapport klaar is, wordt het boven aan het raster weergegeven met de gegenereerde datum en tijd.

### Informatie over module weergeven

U vindt nuttige informatie over geïnstalleerde modules.

**_Rapportinformatie weergeven voor elke geïnstalleerde module:_**

1. Ga in de zijbalk _Beheerder_ naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klik op **[!UICONTROL New Report]**.
1. Selecteer `Modules` in de lijst **[!UICONTROL Groups]**.
1. Klik op **[!UICONTROL Create]**.
1. Nadat het rapport is gegenereerd, klikt u op **[!UICONTROL Select]** en vervolgens op **[!UICONTROL View]** om alle moduleversies te bekijken.
1. Klik op **[!UICONTROL Download]** om het rapport te downloaden.

### Systeemrapporten beheren

Selecteer in de kolom **[!UICONTROL Action]** van het raster een van de volgende opties:

- `View` - Gebruik deze functie om de details van het rapport te bekijken.
- `Delete` - Gebruik deze functie om het gegenereerde rapport uit de lijst te verwijderen.
- `Download` - Gebruik deze functie om het rapport op te slaan als een HTML-bestand.

### Systeemrapportdetails weergeven

1. Selecteer voor het benodigde rapport **[!UICONTROL View]** in de kolom _[!UICONTROL Actions]_.

1. Vouw in het linkerdeelvenster ![Uitbreidingskiezer](../assets/icon-display-expand.png) elke sectie van het rapport uit om de details weer te geven.

   ![Algemene systeemrapportinformatie](./assets/report-information.png){width="600" zoomable="yes"}

### Beschikbare systeemrapporten

| Rapportgroep | Inbegrepen informatie |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce-versie <br>Aantal gegevens<br>cachestatus<br>indexstatus |
| [!UICONTROL Environment] | Omgevingsinformatie<br>MySQL-status |
| [!UICONTROL Data] | Categorieën dupliceren op URL-sleutel<br>Producten dupliceren op URL-sleutel<br>Producten dupliceren op SKU<br>Bestellingen dupliceren op increment-id<br>Gebruikers dupliceren op e-mail<br>Beschadigde categoriedata |
| [!UICONTROL Modules] | Aangepaste modules lijst<br>Uitgeschakelde modules lijst<br>Alle modules lijst |
| [!UICONTROL Configuration] | Configuratie<br>data van `app/etc/env.php`<br>verzendmethoden<br>betalingsmethoden<br>functionaliteitsmatrix voor betalingen |
| [!UICONTROL Logs] | Logbestanden<br>Top systeemberichten<br>De beste systeemberichten van vandaag<br>Top foutopsporingsberichten<br>De beste foutopsporingsberichten van vandaag<br>Top uitzonderingsberichten<br>De beste uitzonderingsberichten van vandaag |
| [!UICONTROL Attributes] | Door gebruiker gedefinieerde EAV-kenmerken<br>Nieuwe EAV-kenmerken<br>entiteitstypen<br>Alle EAV-kenmerken<br>Categorie EAV-kenmerken<br>Product EAV-kenmerken<br>Klant EAV-kenmerken<br>Klantadres EAV-kenmerk<br>RMA-item EAV-kenmerken |
| [!UICONTROL Events] | Aangepaste wereldwijde gebeurtenissen<br>Aangepaste beheergebeurtenissen<br>Aangepaste front-end gebeurtenissen<br>Aangepaste doc gebeurtenissen<br>Aangepaste CronTab gebeurtenissen<br>Aangepaste REST gebeurtenissen<br>Aangepaste SOAP SOAP gebeurtenissen<br>Algemene gebeurtenissen<br>Kernbeheerders gebeurtenissen<br>Kernfront-end gebeurtenissen<br>Kerndocgebeurtenissen<br>Kernconcrontabgebeurtenissen<br>Kerngebeurtenissen<br>Alle wereldwijde gebeurtenissen<br>Alle Beheergebeurtenissen<br>Alle front-end gebeurtenissen<br>Alle Doc gebeurtenissen<br><br>Alle REST gebeurtenissen<br>Alle SOAP gebeurtenissen<br>Alle CronTab gebeurtenissen |
| [!UICONTROL Cron] | Cron Schedules per statuscode<br>Cron Schedules per taakcode<br>Fouten in Cron Schedules Queue<br>Cron Schedules Lijst<br>Aangepaste globale Cron Taken<br>Aangepaste configureerbare Cron Taken<br>Kernglobale Cron Taken<br>Kernconfigureerbare Cron Taken<br>Alle wereldwijde Cron Taken<br>Alle configureerbare Cron Taken |
| [!UICONTROL Design] | AdminHTML Thema&#39;s Lijst<br>Frontend Thema&#39;s Lijst |
| [!UICONTROL Stores] | Website Boom<br>Websites Lijst<br>Winkellijst<br>Winkelweergaven Lijst |
| OMS-connector <br>_(zichtbaar met OMS-integratie)_ | Connectorversie<br>Connector controleren<br>Resultaten van berichtverwerking |

{style="table-layout:auto"}
