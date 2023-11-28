---
title: Een mediadatabase gebruiken
description: Leer hoe u een mediadatabase gebruikt om uw [!DNL Commerce] mediabestanden.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Een mediadatabase gebruiken

>[!IMPORTANT]
>
>De opslagmethode voor databasemedia wordt vanaf Adobe Commerce en Magento Open Source 2.4.3 afgekeurd.

Standaard worden alle afbeeldingen, gecompileerde CSS-bestanden en gecompileerde JavaScript-bestanden van de [!DNL Commerce] -instantie worden opgeslagen in het bestandssysteem op de webserver. U kunt ervoor kiezen deze bestanden op te slaan in een database op een databaseserver. Een voordeel van deze aanpak is de optie voor automatische synchronisatie en omgekeerde synchronisatie tussen het bestandssysteem van de webserver en de database. U kunt de standaarddatabase gebruiken om media op te slaan of te maken. Als u een nieuw gemaakte database wilt kunnen gebruiken als mediaopslag, moet u informatie over de database en de toegangsgegevens ervan toevoegen aan de `env.php` bestand.

## Databaseworkflow

1. **Browser vraagt media aan** - Een pagina uit de winkel wordt geopend in de browser van de klant en de browser vraagt om de media die in de HTML zijn opgegeven.

1. **Systeem zoekt naar media in bestandssysteem** - Het systeem zoekt naar de media in het bestandssysteem en geeft deze door aan de browser, indien deze wordt gevonden.

1. **Systeem zoekt media in database** - Als de media niet in het bestandssysteem worden gevonden, wordt een verzoek voor de media verzonden naar de database die in de configuratie is opgegeven.

1. **Systeem zoekt media in database** - Met een PHP-script worden de bestanden van de database naar het bestandssysteem overgebracht en naar de browser van de klant verzonden. De browser request for media activeert het script als volgt:

   - Als webserver [herschrijven](../merchandising-promotions/url-rewrite.md) zijn ingeschakeld voor [!DNL Commerce] en wordt ondersteund door de server, wordt het PHP-script alleen uitgevoerd wanneer de aangevraagde media niet in het bestandssysteem zijn gevonden.
   - Als herschrijvingen van webservers zijn uitgeschakeld voor [!DNL Commerce]Het PHP-script wordt hoe dan ook uitgevoerd, of wordt niet ondersteund door de server, zelfs als de vereiste media beschikbaar is in het bestandssysteem.

## Een database gebruiken voor mediaopslag

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. In de linkerbovenhoek, plaats **[!UICONTROL Store View]** tot `Default Config` om de configuratie op mondiaal niveau toe te passen.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Storage Configuration for Media]** en voer de volgende handelingen uit:

   ![Geavanceerde configuratie - opslagconfiguratie voor media](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Media Storage]** tot `Database`.

   - Set **[!UICONTROL Select Media Database]** naar de database die u wilt gebruiken.

   - Als u de bestaande media wilt overbrengen naar de nieuw geselecteerde database, klikt u op **[!UICONTROL Synchronize]**.

   - Voer de **[!UICONTROL Environment Update Time]** in seconden.

1. Klik op **[!UICONTROL Save Config]**.
