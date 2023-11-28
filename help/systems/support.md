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

De hulpmiddelen van de steun worden ontworpen om bekende kwesties in uw systeem te identificeren. Ze kunnen worden gebruikt als bron tijdens de ontwikkelings- en optimalisatieprocessen en als diagnostisch hulpmiddel om ons ondersteuningsteam te helpen problemen op te sporen en op te lossen.

## Gegevensverzamelaar

De gegevensverzamelaar verzamelt de informatie over uw systeem die nodig is voor ons ondersteuningsteam om problemen met uw Adobe Commerce-installatie op te lossen. De steun die wordt gecreeerd vergt verscheidene notulen om te voltooien, en omvat zowel een code als gegevensbestandstortplaats. De gegevens kunnen worden geëxporteerd naar een CSV- of Excel XML-bestand.

![Systeem - Gegevensverzameling](./assets/data-collector.png){width="600" zoomable="yes"}

### De gegevensverzamelaar uitvoeren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL New Backup]**.

   Het genereren van de back-up duurt enkele minuten. U kunt de resultaten van de verwerking controleren door op **[!UICONTROL Refresh Status]**. Als de reservekopie is voltooid, wordt de reservekopie weergegeven in de _[!UICONTROL Data Collector]_raster.

1. Ga als volgt te werk om een logboek met de back-upgegevens weer te geven:

   - In de _[!UICONTROL Action]_kolom, selecteren **[!UICONTROL Show Log]**.

   - Klikken **[!UICONTROL Back]** om terug te keren naar het raster.

   ![gegevensverzamelingslogboek](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Back-upgegevens exporteren

1. Selecteer in de eerste kolom het selectievakje van de back-up die u wilt exporteren.

1. Gebruik de **[!UICONTROL Export]** om de indeling van de exportgegevens te kiezen.

   ![Exportindeling](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Open het bestand via de downloadlocatie van de webbrowser en **[!UICONTROL Save]** het.

### Back-upgegevens downloaden

Nadat de back-up is gegenereerd, kunt u de kopie van de code- en DB-gegevens downloaden.

1. Zoek de benodigde back-upentiteit in het raster.

1. Zorg ervoor dat het een `Complete` status.

1. Klik op de naam van de entiteit in _[!UICONTROL Code Dump]_of_[!UICONTROL DB Dump]_ kolommen.

Het downloadproces moet automatisch worden gestart.

## Back-upgegevens verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Zoek en selecteer de back-upgegevens die u wilt verwijderen.

1. In de _[!UICONTROL Action]_kolom, klik **[!UICONTROL Delete]**.

1. Klik op **[!UICONTROL OK]**.

## Systeemrapporten

Het systeem rapporteringshulpmiddel geeft u de capaciteit periodieke volledige, of gedeeltelijke, momentopnamen van het systeem, en bewaart hen voor toekomstige verwijzing. U kunt prestatiesmontages vóór en na de cycli van de codeontwikkeling, of veranderingen in servermontages vergelijken. Met het systeem voor systeemrapportage kan de tijd die nodig is om de informatie voor te bereiden en in te dienen om een onderzoek te starten, aanzienlijk worden verkort.

Via het raster Systeemrapporten kunt u bestaande rapporten weergeven en downloaden, rapporten verwijderen en rapporten maken.

### Toegangssysteemrapporten

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Admin - systeemrapporten](./assets/reports.png){width="600" zoomable="yes"}

### Een rapport genereren

1. Klik op **[!UICONTROL New Report]**.

1. In de **[!UICONTROL Groups]** selecteert u elke set gegevens die u in het rapport wilt opnemen. Standaard zijn alle groepen geselecteerd.

   ![Systeemrapport - groepen selecteren](./assets/report-create.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]**.

   Het zou een paar notulen voor het te produceren rapport kunnen vergen, afhankelijk van het aantal geselecteerde rapporttypes. Wanneer het rapport klaar is, verschijnt het boven aan het raster met de gegenereerde datum en tijd.

### Modulegegevens weergeven

U kunt nuttige informatie over geïnstalleerde modules vinden.

**_Om rapportinfo voor elke geïnstalleerde module te bekijken:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klik op **[!UICONTROL New Report]**.
1. Selecteren `Modules` van de **[!UICONTROL Groups]** lijst.
1. Klik op **[!UICONTROL Create]**.
1. Nadat het rapport is gegenereerd, klikt u **[!UICONTROL Select]** en vervolgens **[!UICONTROL View]** om alle moduleversies te zien.
1. Klikken **[!UICONTROL Download]** het rapport downloaden.

### Systeemrapporten beheren

In de **[!UICONTROL Action]** Selecteer een van de volgende opties in de kolom van het raster:

- `View` - Gebruik deze functie om de details van het rapport te bekijken.
- `Delete` - Gebruik deze functie om het gegenereerde rapport uit de lijst te verwijderen.
- `Download` - Gebruik deze functie om het rapport op te slaan als een HTML-bestand.

### Gegevens van systeemrapporten weergeven

1. Voor het rapport dat u nodig hebt, selecteert u **[!UICONTROL View]** in de _[!UICONTROL Actions]_kolom.

1. Vouw in het linkerdeelvenster uit ![Expansiekiezer](../assets/icon-display-expand.png) in elk gedeelte van het rapport worden de details weergegeven.

   ![Algemene informatie over systeemrapporten](./assets/report-information.png){width="600" zoomable="yes"}

### Beschikbare systeemrapporten

| Rapportgroep | Informatie inbegrepen |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce-versie<br>Aantal gegevens<br>Cachestatus<br>Indexstatus |
| [!UICONTROL Environment] | Omgevingsinformatie<br>MySQL-status |
| [!UICONTROL Data] | Categorieën dupliceren op URL-sleutel<br>Producten dupliceren op URL-sleutel<br>Producten dupliceren op SKU<br>Dubbele bestellingen op verhoging-id<br>Gebruikers dupliceren per e-mail<br>Beschadigde categoriegegevens |
| [!UICONTROL Modules] | Lijst met aangepaste modules<br>Lijst met uitgeschakelde modules<br>Alle modules |
| [!UICONTROL Configuration] | Configuratie<br>Gegevens van `app/etc/env.php`<br>Verzendmethoden<br>Betalingsmethoden<br>Matrix betalingsfuncties |
| [!UICONTROL Logs] | Logbestanden<br>Bovenste systeemberichten<br>De beste Systeemberichten van vandaag<br>Foutopsporingsberichten bovenaan<br>De beste Debug Berichten van vandaag<br>Bovenste uitzonderingsberichten<br>De beste uitzonderingsberichten van vandaag |
| [!UICONTROL Attributes] | Door gebruiker gedefinieerde EAV-kenmerken<br>Nieuwe EAV-kenmerken<br>Typen entiteiten<br>Alle EAV-kenmerken<br>Categorie EAV-kenmerken<br>EAV-kenmerken van product<br>Klant EAV-kenmerken<br>Klantadres EAV-kenmerk<br>EAV-kenmerken RMA-item |
| [!UICONTROL Events] | Aangepaste algemene gebeurtenissen<br>Aangepaste beheergebeurtenissen<br>Aangepaste front-end gebeurtenissen<br>Aangepaste documentgebeurtenissen<br>Aangepaste Crontab-gebeurtenissen<br>Aangepaste REST-gebeurtenissen<br>Aangepaste SOAP-gebeurtenissen<br>Algemene gebeurtenissen<br>Gebeurtenissen kernbeheerder<br>Core Front Events<br>Core Doc Events<br>Core Crontab Events<br>Core REST Events<br>Core SOAP Events<br>Alle algemene gebeurtenissen<br>Alle beheergebeurtenissen<br>Alle voorste gebeurtenissen<br>Alle documentgebeurtenissen<br>Alle REST-gebeurtenissen<br>Alle SOAP-gebeurtenissen<br>Alle Crontab-gebeurtenissen |
| [!UICONTROL Cron] | Planningen bijsnijden op statuscode<br>Planningen bijsnijden op taakcode<br>Fouten in wachtrij voor Cron Planningen<br>Lijst met bijsnijdschema&#39;s<br>Aangepaste algemene snijtaken<br>Aangepaste configureerbare snijtaken<br>Core Global Cron Jobs<br>Core Configureerbare Cron Jobs<br>Alle algemene snijtaken<br>Alle configureerbare Cron-taken |
| [!UICONTROL Design] | Lijst met beheerthema&#39;s<br>Lijst met voorste thema&#39;s |
| [!UICONTROL Stores] | Websitestructuur<br>Lijst met websites<br>Winkellijst<br>Lijst met winkelweergaven |
| OMS Connector <br>_(zichtbaar met OMS-integratie)_ | Verbindingsversie<br>Connectorbewaking<br>Resultaten van berichtverwerking |

{style="table-layout:auto"}
