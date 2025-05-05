---
title: Geplande import en export
description: Leer hoe u geplande bewerkingen voor het importeren en exporteren van gegevens beheert.
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '2429'
ht-degree: 0%

---

# Geplande import en export

{{ee-feature}}

De geplande invoer en de uitvoer kunnen op een dagelijkse, wekelijkse, of maandbasis worden lopen. De bestanden die geïmporteerd of geëxporteerd moeten worden, kunnen zich op lokale Adobe Commerce-servers of op externe FTP-servers bevinden. De geplande Invoer/de Uitvoer wordt uitgevoerd door gebrek, en vereist geen extra configuratie. Alle geplande import en export worden beheerd door de Cron job planner.

## Toegang tot geplande import/export

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![ Geplande gegevensinvoer/uitvoer ](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. Als u een nieuwe geplande import- of exporttaak wilt maken, klikt u op de betreffende knop en volgt u de instructies voor het type geplande taak.

   - [Geplande export toevoegen](#schedule-an-export)
   - [Geplande import toevoegen](#schedule-an-import)

1. Wanneer de record wordt opgeslagen, wordt de taak weergegeven in het raster van _[!UICONTROL Scheduled Import/Export]_.

   >[!NOTE]
   >
   >Wanneer u een geplande import/export maakt of bijwerkt, leidt dit tot een wijziging in de systeemconfiguratie. Nadat u het bestand hebt opgeslagen, controleert u of u de melding van de cachevalidatie die boven aan de beheerpagina wordt weergegeven, hebt opgelost en verwijdert u de cache om het nieuwe of bijgewerkte schema toe te passen.

1. [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} na elke geplande baan, wordt een exemplaar van het dossier geplaatst in de `var/log/import_export` folder op de lokale server van Adobe Commerce.

   De details van elke verrichting worden niet geschreven aan het logboek. Als een fout optreedt, wordt een melding verzonden van de mislukte import-/exporttaak, met een beschrijving van de fout.

## Importeren plannen

Voor de beschikbare bestandsindeling voor import en de typen importentiteiten is het geplande importproces vergelijkbaar met het handmatig importeren:

- Het importbestand moet de CSV-indeling hebben
- U kunt product- en klantgegevens importeren

Het voordeel van geplande importbewerkingen is dat u een gegevensbestand meerdere keren automatisch kunt importeren nadat u de importparameters en -planning hebt opgegeven.

De details van elke de invoerverrichting worden niet geschreven aan een logboek, maar wanneer er een mislukking is ontvangt u Ontbroken _Invoer_ e-mail met een beschrijving van de fout. Het resultaat van de laatste geplande importtaak wordt weergegeven in de kolom Laatste resultaat op de geplande pagina Importeren/exporteren.

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} na elke de invoerverrichting, wordt een exemplaar van het de invoerdossier geplaatst in de `var/log/import_export` folder op de server waar Adobe Commerce of Magento Open Source wordt opgesteld. De tijdstempel, de markering van de geïmporteerde entiteit (producten of klanten) en het type bewerking (in dit geval importeren) worden toegevoegd aan de naam van het importbestand.

Na elke geplande importtaak wordt automatisch een herindexeringsbewerking uitgevoerd. Op de voorgrond worden wijzigingen in de beschrijvingen en andere tekstinformatie weerspiegeld nadat de bijgewerkte gegevens naar de database gaan, en de prijswijzigingen worden pas na de herindexeringsoperatie doorgevoerd.

### Stap 1: De importinstellingen voltooien

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Scheduled Import]** .

1. Stel de opties voor plannen en importeren in:

   - **[!UICONTROL Name]** — Voer een naam in voor het geplande importeren.

   - **[!UICONTROL Description]** — Voer een korte beschrijving in met uitleg over het doel van de import en hoe deze moet worden gebruikt.

   - **[!UICONTROL Entity Type]** — Stel een van de volgende opties in:

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]** — Stel een van de volgende opties in:

      - `Add/Update Complex Data` — Hiermee voegt u nieuwe complexe gegevens toe aan of werkt u deze bij aan de bestaande complexe gegevens voor bestaande vermeldingen in de database. Dit is de standaardwaarde.
      - `Replace` — Schrijft over bestaand complex voor bestaande entiteiten in de database.
      - `Delete Entities` — Verwijdert bestaande vermeldingen in de database.
      - `Custom Action` - Hiermee past u bestaande entiteiten in de database aan.

     >[!NOTE]
     >
     >Voor de typen _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_ , _[!UICONTROL Customers and Addresses (single file)]_&#x200B;en&#x200B;_[!UICONTROL Stock Sources]_ entiteit worden de volgende importgedragingen weergegeven: `Add/Update` , `Replace` en `Delete` . Voor de _Financiën van de Klant_, _het Belangrijkste Dossier van Klanten_, en _Klanten en richt_ entiteittypes, worden dit de invoergedrag getoond: `Add/Update Complex Data`, `Delete Entities`, en `Custom Action`.

   - **[!UICONTROL Start Time]** — Stel dit in op het uur, de minuut en de seconde waarop het importeren moet beginnen.

   - **[!UICONTROL Frequency]** — Stel dit in op een van de volgende opties: `Daily` , `Weekly` of `Monthly`

   - **[!UICONTROL On Error]** - Stel het volgende in: `Stop Import` of `Continue Processing`

   - **[!UICONTROL Status]** — Als u de geplande importbewerking wilt activeren, stelt u deze in op `Enabled` .

   - **[!UICONTROL Field Separator]** — Voer het teken in dat wordt gebruikt om velden in het importbestand van elkaar te scheiden. Het standaardteken is een komma.

   - **[!UICONTROL Multiple Value Separator]** — Voer het teken in dat wordt gebruikt om meerdere waarden in een veld van elkaar te scheiden.

   ![ de invoer van Gegevens - geplande de invoermontages ](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### Stap 2: de gegevens van het importbestand invullen

1. Stel **[!UICONTROL Server Type]** in op een van de volgende opties:

   - `Local Server` - Hiermee importeert u de gegevens van dezelfde server als waarop Adobe Commerce is geïnstalleerd.
   - `Remote FTP` - Hiermee importeert u de gegevens van een externe server.

   ![ Invoer van Gegevens - de geplande informatie van het de invoerdossier ](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wanneer de externe opslagmodule is ingeschakeld, schakelt `Local Server` automatisch over naar `Remote Storage` .

1. Voer de **[!UICONTROL File Directory]** in waar het importbestand vandaan komt.

   - `Local Server` - Voer een relatief pad in de Commerce-installatie in. Bijvoorbeeld `var/import` . Als de externe opslagmodule is geconfigureerd, gebruikt u `import_export/import` .
   - `Remote FTP server` - Voer de volledige URL en het volledige pad naar de importmap op de externe server in.

1. Voer de **[!UICONTROL File Name]** in die u wilt importeren.

1. Voer bij **[!UICONTROL Images File Directory]** het pad in naar de map waarin de productafbeeldingen zijn opgeslagen.

   Voer op een lokale server een relatief pad in, bijvoorbeeld: `var/import` . Voer op een externe opslaglocatie een relatief pad in, zoals: `import_export/import` of `import_export/import/some/dir` .

### Stap 3: het importeren van mislukte e-mails configureren

![ de invoer van Gegevens - ontbroken invoer gefiëerde e-mails ](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Failed Email Receiver]** in op de contactpersoon van de winkel die een melding ontvangt als er een fout optreedt tijdens het importeren.

1. Stel **[!UICONTROL Failed Email Sender]** in op de opslagcontactpersoon die wordt weergegeven als de afzender van het bericht.

1. Stel **[!UICONTROL Failed Email Template]** in op de sjabloon die voor de melding wordt gebruikt.

1. Voer bij **[!UICONTROL Send Failed Email Copy To]** het e-mailadres in van iedereen die een kopie van de melding moet ontvangen.

   Scheid meerdere e-mailadressen met een komma.

1. Stel **[!UICONTROL Failed Email Copy Method]** in op een van de volgende opties:

   - `Bcc` - Hiermee wordt een blinde, hoffelijke kopie van de mislukte melding bij importeren verzonden. De naam en het adres van de ontvanger zijn opgenomen in de oorspronkelijke e-maildistributie, maar zijn niet zichtbaar.
   - `Separate Email` - Hiermee wordt een kopie van het mislukte importbericht als een aparte e-mail verzonden.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   De nieuwe geplande importtaak wordt toegevoegd aan de lijst op de pagina _[!UICONTROL Scheduled Import/Export]_. Vanaf deze pagina kan deze direct worden uitgevoerd voor testen en worden bewerkt. Het importbestand wordt gevalideerd voordat elke importtaak wordt uitgevoerd.

>[!NOTE]
>
>Wanneer u een geplande import/export maakt of bijwerkt, leidt dit tot een wijziging in de systeemconfiguratie. Nadat u het bestand hebt opgeslagen, controleert u of u de melding van de cachevalidatie die boven aan de beheerpagina wordt weergegeven, hebt opgelost en verwijdert u de cache om het nieuwe of bijgewerkte schema toe te passen.

### Veldomschrijvingen

#### [!UICONTROL Import Settings]

| Veld | Beschrijving |
| ----- | ----------- | 
| [!UICONTROL Name] | De naam van de importbewerking. Hiermee kunt u een onderscheid maken tussen vele verschillende geplande importbewerkingen. |
| [!UICONTROL Description] | (Optioneel) U kunt een beschrijving invoeren. |
| [!UICONTROL Entity Type] | Hiermee definieert u de gegevens die moeten worden geïmporteerd. |
| [!UICONTROL Import Behavior] | Hiermee definieert u hoe complexe gegevens worden verwerkt als de entiteiten die worden geïmporteerd in de database bestaan. Complexe gegevens voor producten omvatten categorieën, websites, aangepaste opties, laagprijzen, verwante producten, upsells, cross-sells en bijbehorende productgegevens. De complexe gegevens voor klanten omvatten adressen. Opties:<br>**[!UICONTROL Add/Update Complex Data]**- de nieuwe complexe gegevens worden toegevoegd of aan de bestaande complexe gegevens voor bestaande ingangen in het gegevensbestand bijgewerkt. Dit is de standaardwaarde.<br>**[!UICONTROL Add/Update]** - Nieuwe gegevens worden toegevoegd aan de bestaande vermeldingen in de database. Alle velden behalve `sku` kunnen worden bijgewerkt voor producten. Meerdere veldwaarden die niet in het CSV-bestand worden vermeld, zoals categorieën of websites, blijven na het importeren in de database staan.<br>**[!UICONTROL Replace]**- De bestaande complexe gegevens voor de bestaande entiteiten worden vervangen.<br>**[!UICONTROL Delete Entities]** - Als er geïmporteerde entiteiten in de database aanwezig zijn, worden deze uit de database verwijderd.<br>**[!UICONTROL Custom Action]**- De bestaande complexe entiteiten worden tijdens het importproces aangepast. |
| [!UICONTROL Start Time] | Stel het beginuur, minuten en seconden van het importeren in. |
| [!UICONTROL Frequency] | Bepaal hoe vaak het importeren wordt uitgevoerd. Opties: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | Definieer het systeemgedrag voor het geval er tijdens de bestandsvalidatie fouten worden gevonden. Opties:<br>**de Invoer van het Einde** - het dossier wordt niet ingevoerd als om het even welke fouten tijdens bevestiging worden gevonden. Dit is de standaardwaarde.<br>**zet Verwerking** voort - voor het geval de fouten tijdens bevestiging worden gevonden, maar het invoeren is mogelijk, wordt het dossier ingevoerd. |
| [!UICONTROL Status] | Importeren is standaard ingeschakeld. U kunt dit opschorten door de status in te stellen op `Disabled` . |
| [!UICONTROL Field Separator] | Bepaalt welk teken wordt gebruikt om velden te scheiden. Standaardwaarde: `,` (komma) |
| [!UICONTROL Multiple Value Separator] | Bepaalt het teken dat wordt gebruikt om meerdere waarden binnen een veld van elkaar te scheiden. Standaardwaarde: `,` (komma) |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| Veld | Beschrijving |
| ----- | ----------- | 
| [!UICONTROL Server Type] | U kunt importeren vanuit een bestand op dezelfde server waarop Commerce is geïmplementeerd (selecteer `Local Server` ) of vanaf de externe FTP-server (selecteer `Remote FTP` ). Als u _[!UICONTROL Remote FTP]_&#x200B;selecteert, worden aanvullende opties voor referenties en instellingen voor bestandsoverdracht weergegeven. Als de externe opslagmodule is ingeschakeld, wordt het type `Local Server` automatisch geschakeld naar `Remote Storage` . |
| [!UICONTROL File Directory] | Geef de map op waarin het importbestand zich bevindt. Als Servertype is ingesteld op _[!UICONTROL Local Server]_, geeft u het pad op ten opzichte van de installatiemap van Commerce. Bijvoorbeeld: `var/import` of `import_export/import` voor externe opslag. |
| [!UICONTROL File Name] | Geef de naam van het importbestand op. |
| [!UICONTROL Images File Directory] | Voer het pad in naar de map waarin de productafbeeldingen zijn opgeslagen. Voer voor een lokale server een relatief pad in. Bijvoorbeeld: `var/import` of `import_export/import` voor externe opslag. |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| Veld | Beschrijving |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Geef het e-mailadres op waarnaar een e-mailmelding (niet-geïmporteerde e-mail) wordt verzonden als het importeren is mislukt. |
| [!UICONTROL Failed Email Sender] | Geef het e-mailadres op dat wordt gebruikt als de afzender voor het niet-geïmporteerde e-mailbericht. |
| [!UICONTROL Failed Email Template] | Selecteer een sjabloon voor het e-mailbericht voor importeren. Standaard is alleen de optie Importeren mislukt (standaardsjabloon van landinstelling is beschikbaar). U kunt aangepaste sjablonen maken onder _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_ . |
| [!UICONTROL Send Failed Email Copy To] | Het e-mailadres waarnaar een kopie van het niet-geïmporteerde e-mailbericht is verzonden. |
| [!UICONTROL Send Failed Email Copy Method] | Selecteer de methode voor het verzenden van kopieën voor de niet-geïmporteerde e-mail. |

{style="table-layout:auto"}

## Een exportbewerking plannen

De geplande Uitvoer is gelijkaardig aan een handmatige [ Uitvoer ](data-export.md) in het beschikbare formaat van het de uitvoerdossier en types van entiteiten die kunnen worden uitgevoerd:

- U kunt exporteren naar de CSV-indeling
- U kunt product- en klantgegevens exporteren

Het voordeel van het gebruik van Geplande export is dat u gegevens meerdere keren automatisch kunt exporteren, nadat u de exportparameters hebt opgegeven, en slechts één keer kunt plannen.

De details van elke export worden niet naar een logboek geschreven, maar als er een fout optreedt, ontvangt u een e-mail met exportfout die de foutbeschrijving bevat. Het resultaat van de laatste exporttaak wordt weergegeven in de kolom Laatste resultaat op de pagina Geplande import/export.

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} na elke uitvoer, wordt het uitvoerdossier geplaatst in de user-defined plaats, en een exemplaar in de `var/log/import_export` folder op de server waar Adobe Commerce of Magento Open Source wordt opgesteld. Het tijdstempel en de markering van de geëxporteerde entiteit (producten of klanten) en het type bewerking (in dit geval exporteren) worden toegevoegd aan de naam van het exportbestand.

### Stap 1: de exportinstellingen voltooien

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Scheduled Export]** en voer de volgende handelingen uit:

   - Voer een **[!UICONTROL Name]** in voor de geplande export.

   - Voer een korte **[!UICONTROL Description]** in met uitleg over het doel van de export en hoe deze moet worden gebruikt.

   - Stel **[!UICONTROL Entity Type]** in op een van de volgende opties:

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     De sectie _[!UICONTROL Entity Attributes]_&#x200B;onder aan de pagina wordt bijgewerkt met het geselecteerde Type entiteit.

   - Stel **[!UICONTROL Start Time]** in op het uur, de minuut en de seconde waarop het exporteren moet beginnen.

   - Stel **[!UICONTROL Frequency]** in op een van de volgende opties:

      - `Daily`
      - `Weekly`
      - `Monthly`

1. Stel **[!UICONTROL Status]** in op `Enabled` om het geplande exporteren te activeren.

1. Accepteer `CSV` als de standaardwaarde **[!UICONTROL File Format]** .

   ![ Geplande de uitvoermontages ](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### Stap 2: de gegevens van het exportbestand invullen

1. Stel **[!UICONTROL Server Type]** in op een van de volgende opties:

   - `Local Server` - Het exportbestand opslaan op dezelfde server als Commerce.
   - `Remote FTP` — Het exportbestand opslaan op een externe server.

   ![ Geplande de informatie van het de uitvoerdossier ](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wanneer de externe opslagmodule is ingeschakeld, schakelt de `Local Server` automatisch over naar `Remote Storage` .

1. Voer bij **[!UICONTROL File Directory]** als volgt de map in waarin het exportbestand moet worden opgeslagen:

   - Voer bij **[!UICONTROL Local Server]** een relatief pad in in de Commerce-installatie, bijvoorbeeld `var/export` . Als de externe opslagmodule is geconfigureerd, gebruikt u `import_export/export` .
   - Voer bij **[!UICONTROL Remote FTP server]** de volledige URL en het pad naar de doelmap op de doelserver in.

1. Als de _[!UICONTROL Remote FTP]_-server is geselecteerd, voert u verbindingsgegevens naar de server in en selecteert u aanvullende instellingen:

   - Voer bij **[!UICONTROL FTP Host[:Port]]** het externe FTP-hostadres in.
   - Voer bij **[!UICONTROL User Name]** de gebruikersnaam in die wordt gebruikt voor toegang tot de externe server.
   - Voer bij **[!UICONTROL Password]** het wachtwoord van de opgegeven gebruikersaccount in.
   - Kies `Binary` of `ASCII` bij **[!UICONTROL File Mode]** .
   - Kies `No` of `Yes` bij **[!UICONTROL Passive Mode]** .

### Stap 3: de e-mails met exportfouten configureren

1. Stel **[!UICONTROL Failed Email Receiver]** in op de contactpersoon van de winkel die een melding ontvangt als er een fout optreedt tijdens het exporteren.

1. Stel **[!UICONTROL Failed Email Sender]** in op de opslagcontactpersoon die wordt weergegeven als de afzender van het bericht.

1. Stel **[!UICONTROL Failed Email Template]** in op de sjabloon die voor de melding wordt gebruikt.

1. Voer bij **[!UICONTROL Send Failed Email Copy To]** het e-mailadres in van iedereen die een kopie van de melding moet ontvangen.

   Voor meerdere e-mailadressen scheidt u deze met een komma.

1. Stel **[!UICONTROL Failed Email Copy Method]** in op een van de volgende opties:

   - `Bcc` - Verstuurt een blinde, hoffelijke kopie. De naam en het adres van de ontvanger zijn opgenomen in de oorspronkelijke e-maildistributie, maar zijn niet zichtbaar.
   - `Separate Email` — Verzendt de kopie als een aparte e-mail.

### Stap 4: kies de entiteitskenmerken

1. Kies in de sectie _[!UICONTROL Entity Attributes]_&#x200B;de kenmerken die u wilt opnemen in de exportgegevens.

   - Als u exportgegevens wilt filteren op kenmerkwaarde, voert u de kenmerkwaarde in de kolom _[!UICONTROL Filter]_&#x200B;in.
   - Als u producten of klanten met bepaalde kenmerkwaarden wilt uitsluiten, voert u de waarden in van de kenmerken die u wilt uitsluiten en schakelt u het selectievakje Overslaan in de kolom Overslaan in.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   De nieuwe geplande exporttaak wordt toegevoegd aan de lijst op de pagina _[!UICONTROL Scheduled Import/Export]_. Vanaf deze pagina kan het onmiddellijk worden uitgevoerd, getest en bewerkt.

>[!NOTE]
>
>Wanneer u een geplande import/export maakt of bijwerkt, leidt dit tot een wijziging in de systeemconfiguratie. Nadat u het bestand hebt opgeslagen, controleert u of u de melding van de cachevalidatie die boven aan de beheerpagina wordt weergegeven, hebt opgelost en verwijdert u de cache om het nieuwe of bijgewerkte schema toe te passen.

### Veldomschrijvingen

#### [!UICONTROL Export Settings]

| Veld | Beschrijving |
| ----- | ----------- | 
| [!UICONTROL Name] | De naam van de exportbewerking. Hiermee kunt u een onderscheid maken tussen vele verschillende geplande exportbewerkingen. |
| [!UICONTROL Description] | (Optioneel) Een beschrijving van de geplande export. |
| [!UICONTROL Entity Type] | Identificeert de gegevens die moeten worden geëxporteerd. Nadat u de selectie hebt gemaakt, worden de entiteitskenmerken hieronder weergegeven. Opties: `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | Stel het beginuur, de minuten en de seconden van het exporteren in. |
| [!UICONTROL Frequency] | Bepaal hoe vaak de exporttaak wordt uitgevoerd. Opties: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | Een nieuwe geplande export is standaard ingeschakeld. U kunt dit opschorten door Status in te stellen op Uitgeschakeld. Opties: `Enabled` / `Disabled` |
| [!UICONTROL File Format] | Selecteer de indeling van het exportbestand. Momenteel is alleen de optie `.CSV` beschikbaar. |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| Veld | Beschrijving |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Bepaalt de locatie van het exportbestand. Opties:<br>**Lokale Server** - Plaatst het de uitvoerdossier op de zelfde server waar Commerce wordt opgesteld. Als de externe opslagmodule is ingeschakeld, wordt `Local Server` geschakeld naar `Remote Storage` .<br>**Verre FTP** — Plaatst het de uitvoerdossier op een verre server. Er worden extra opties voor referenties en instellingen voor bestandsoverdracht weergegeven. |
| [!UICONTROL File Directory] | Geef de map op waarin het exportbestand wordt geplaatst. Als _[!UICONTROL Server Type]_&#x200B;is ingesteld op `Local Server` , geeft u het pad op ten opzichte van het Commerce-installatiepad. Bijvoorbeeld `var/export` of `import_export/export` voor externe opslag. |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| Veld | Beschrijving |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Geef het e-mailadres op waarnaar een e-mailmelding (niet-geëxporteerde e-mail) wordt verzonden als het exporteren is mislukt. |
| [!UICONTROL Failed Email Sender] | Geef het e-mailadres op dat wordt gebruikt als e-mailafzender met exportfout. |
| [!UICONTROL Failed Email Template] | Selecteer een sjabloon voor de mislukte e-mail voor exporteren. Standaard is alleen de optie `Export Failed (Default Template from Locale)` beschikbaar. |
| [!UICONTROL Send Failed Email Copy To] | Het e-mailadres waarnaar een kopie van de niet-geëxporteerde e-mail wordt verzonden. |
| [!UICONTROL Send Failed Email Copy Method] | Geef de methode op voor het verzenden van kopieën voor de niet-geëxporteerde e-mail. |

{style="table-layout:auto"}
