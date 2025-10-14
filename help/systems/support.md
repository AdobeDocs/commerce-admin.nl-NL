---
title: Ondersteuningsgereedschappen
description: Leer over de verstrekte steunhulpmiddelen die u kunt gebruiken om kwesties in uw systeem te identificeren.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: addde8c3e41b641712f5b08107c1d68b40cd4159
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Ondersteuningsgereedschappen

{{ee-feature}}

De hulpmiddelen van de steun worden ontworpen om bekende kwesties in uw systeem te identificeren. Ze kunnen worden gebruikt als bron tijdens de ontwikkelings- en optimalisatieprocessen en als diagnostisch hulpmiddel om ons ondersteuningsteam te helpen problemen op te sporen en op te lossen.

## Systeemrapporten

Het systeem rapporteringshulpmiddel geeft u de capaciteit periodieke volledige, of gedeeltelijke, momentopnamen van het systeem, en bewaart hen voor toekomstige verwijzing. U kunt prestatiesmontages vóór en na de cycli van de codeontwikkeling, of veranderingen in servermontages vergelijken. Met het systeem voor systeemrapportage kan de tijd die nodig is om de informatie voor te bereiden en in te dienen om een onderzoek te starten, aanzienlijk worden verkort.

Via het raster Systeemrapporten kunt u bestaande rapporten weergeven en downloaden, rapporten verwijderen en rapporten maken.

### Toegangssysteemrapporten

Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![&#x200B; Admin - systeemrapporten &#x200B;](./assets/reports.png){width="600" zoomable="yes"}

### Een rapport genereren

1. Klik op **[!UICONTROL New Report]**.

1. Selecteer in de lijst **[!UICONTROL Groups]** elke set gegevens die u in het rapport wilt opnemen. Standaard zijn alle groepen geselecteerd.

   ![&#x200B; het rapport van het Systeem - uitgezochte groepen &#x200B;](./assets/report-create.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]** .

   Het zou een paar notulen voor het te produceren rapport kunnen vergen, afhankelijk van het aantal geselecteerde rapporttypes. Wanneer het rapport klaar is, verschijnt het boven aan het raster met de gegenereerde datum en tijd.

### Modulegegevens weergeven

U kunt nuttige informatie over geïnstalleerde modules vinden.

**_om rapportinfo voor elke geïnstalleerde module te bekijken:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klik op **[!UICONTROL New Report]**.
1. Selecteer `Modules` in de lijst **[!UICONTROL Groups]** .
1. Klik op **[!UICONTROL Create]**.
1. Nadat het rapport is gegenereerd, klikt u op **[!UICONTROL Select]** en vervolgens op **[!UICONTROL View]** om alle moduleversies weer te geven.
1. Klik op **[!UICONTROL Download]** om het rapport te downloaden.

### Systeemrapporten beheren

Selecteer in de kolom **[!UICONTROL Action]** van het raster een van de volgende opties:

- `View` - Gebruik deze functie om de details van het rapport te bekijken.
- `Delete` - Gebruik deze functie om het gegenereerde rapport uit de lijst te verwijderen.
- `Download` - Gebruik deze functie om het rapport op te slaan als een HTML-bestand.

### Gegevens van systeemrapporten weergeven

1. Selecteer **[!UICONTROL View]** in de kolom _[!UICONTROL Actions]_&#x200B;voor het rapport dat u nodig hebt.

1. In het linkerpaneel, breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) elke sectie van het rapport uit om het detail te bekijken.

   ![&#x200B; Algemene informatie van het systeemrapport &#x200B;](./assets/report-information.png){width="600" zoomable="yes"}

### Beschikbare systeemrapporten

| Rapportgroep | Informatie inbegrepen |
| ------------ | -------------------- |
| [!UICONTROL General] | De Status van het Geheime voorgeheugen van de Telling van de Versie van Adobe Commerce <br> <br> Index<br> |
| [!UICONTROL Environment] | De Informatie van het milieu <br> Status MySQL |
| [!UICONTROL Data] | De dubbele Categorieën door sleutel URL <br> dupliceren Producten door sleutel URL <br> dupliceert Producten door SKU <br> dubbele Orden door identiteitskaart van de Toename <br> dubbele Gebruikers door E-mail <br> beschadigde CategorieënGegevens |
| [!UICONTROL Modules] | De Lijst van de Modules van de Douane <br> Gehandicapte Lijst van Modules <br> Alle Lijst van Modules |
| [!UICONTROL Configuration] | De Gegevens van de configuratie <br> van `app/etc/env.php`<br> Verschepende Methoden <br> de Methoden van de Betaling <br> Matrijs van de Functionaliteit van Betalingen |
| [!UICONTROL Logs] | De Dossiers van het Logboek <br> Hoogste Berichten van het Systeem <br> Van vandaag de hoogste Berichten van het Systeem <br> Debug Berichten <br> Van vandaag de hoogste Berichten van de Uitzondering <br> <br> Van de de hoogste Uitzondering van vandaag Berichten |
| [!UICONTROL Attributes] | Gebruiker bepaalde EAV Attributen <br> Nieuwe Attributen EAV <br> Typen van de Entiteit <br> Alle Attributen EAV <br> attributen van de Categorie EAV <br> Attributen van het Product EAV <br> Attributen van de Klant EAV <br> Attributen van het Adres van de Klant &lbrace;<br> Attributen van het Punt RMA EAV |
| [!UICONTROL Events] | De Eigen Globale Gebeurtenissen van Gebeurtenissen van Admin van de Gebeurtenissen van Admin van de Douane {<br> Gebeurtenissen van de Gebeurtenissen van de Gebeurtenissen van de Gebeurtenissen van de Aangepaste Crontab van de Gebeurtenissen van de Eigen {<br> Eigen Gebeurtenissen van SOAP van de Kern van de Gebeurtenissen van Admin van 7} van de Kern van Admin {<br> Gebeurtenissen van de Gebeurtenissen van de Kern van de Voorzie {<br> 11} 111} 11} Core van de Gebeurtenissen van de Gebeurtenissen van de Gebeurtenissen van 1111110&rbrace; van de ECN van de Gebeurtenissen van de Gebeurtenissen van de ECN van de ECN van de ECN van de ECN { De Gebeurtenissen van de Kern van de Gebeurtenissen van SOAP 12} <br> Alle Globale Gebeurtenissen <br> Alle Gebeurtenissen Admin <br> Alle Gebeurtenissen van het Front <br> Alle Gebeurtenissen van Doc <br> Alle gebeurtenissen van het Terugsturen <br> Alle Gebeurtenissen van SOAP <br> Alle Gebeurtenissen Crontab<br><br><br><br><br><br><br><br><br> |
| [!UICONTROL Cron] | De programma&#39;s van het gewricht door statuscode <br> Gewas Programma&#39;s door baancode <br> Fouten in de 2&rbrace; Gewas Lijst van Programma&#39;s van de Rij <br> Eigen Globale Banen van het Gewas <br> Aangepaste Aanpasbare Banen van het Gewas <br> de Mondiale Banen van de Kern van de Banen van de Bouw van de Kern {<br> Zulden Alle Globale Gelijkaardige Gelijke Graadwerk van 7} Globale Graadwerk van de Globale Graad <br> Globale 3&rbrace; Globale Banen van de Globale Wegen <br> Globale Wegen <br> |
| [!UICONTROL Design] | Adminhtml Lijst van Thema&#39;s <br> de Lijst van Thema&#39;s van het Front |
| [!UICONTROL Stores] | De Boom van de website <br> Lijst van Websites <br> de Lijst van de Lijsten van de Opslag <br> Lijst van de Bekijken van de Opslag |
| OMS Connector <br>_(zichtbaar met integratie OMS)_ | De Versie van de schakelaar <br> Schakelaar controleerde <br> Resultaten van de Verwerking van het Bericht |

{style="table-layout:auto"}
