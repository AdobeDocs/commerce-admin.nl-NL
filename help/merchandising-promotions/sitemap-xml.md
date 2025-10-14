---
title: Site-maps
description: Leer hoe u een site-overzicht configureert om alle pagina's en afbeeldingen van uw Commerce-sites te indexeren.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Site-maps

>[!TIP]
>
>Voor Adobe Commerce as a Cloud Service, zie de [&#x200B; richtlijnen van SEO &#x200B;](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=nl-NL) in de documentatie van de Storefront van Commerce

Een site-overzicht verbetert de manier waarop uw winkel wordt geïndexeerd door zoekprogramma&#39;s en is ontworpen om pagina&#39;s te zoeken die mogelijk door webcrawlers worden genegeerd. U kunt een site-overzicht configureren om alle pagina&#39;s en afbeeldingen te indexeren.

Als deze optie is ingeschakeld, maakt Commerce een bestand met de naam `sitemap.xml` dat in de door u opgegeven locatie wordt opgeslagen in uw installatie. De configuratie geeft u de capaciteit om de frequentie van de updates, en de prioriteit voor elk type van inhoud te plaatsen. Uw site-overzicht moet zo vaak worden bijgewerkt als de inhoud op uw site verandert, mogelijk dagelijks, wekelijks of maandelijks.

Terwijl uw site in ontwikkeling is, kunt u instructies in het `robots.txt` -bestand opnemen om te voorkomen dat webcrawlers de site indexeren. Vervolgens kunt u de instructies wijzigen zodat de site kan worden geïndexeerd.

Voor technische informatie, zie [ sitemap en robots.txt ][1] in _Commerce op de Gids van de Infrastructuur van de Wolk_ toevoegen.

![&#x200B; Net van de Sitemap &#x200B;](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Stap 1. Het site-overzicht configureren

Voltooi de [&#x200B; configuratie van de Sitemap van XML &#x200B;](#site-map-configuration) om te bepalen wat inbegrepen is, en hoe vaak wordt de plaatstoewijzing bijgewerkt.

## Stap 2. Site-overzicht genereren

1. Voor het _Admin_ menu, ga **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Klik op **[!UICONTROL Add Site Map]**.

   ![&#x200B; Net van het het kaartschema van de Plaats &#x200B;](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Voer het site-overzicht **[!UICONTROL Filename]** in. Bijvoorbeeld: `sitemap.xml`

1. Voer de **[!UICONTROL Path]** in om te bepalen waar het site-toewijzingsbestand zich op de server moet bevinden. Zorg ervoor dat het pad schrijfbaar is.

   - `/sitemap/` - Plaatst het dossier van de plaatsafbeelding in een folder genoemd _sitemap_.

   - `/` - Plaatst het bestand met het site-overzicht op het basispad of de hoofdmap van de Commerce-installatie.

   ![&#x200B; Nieuwe plaatskaart &#x200B;](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save & Generate]** als de bewerking is voltooid.

   Het kan enkele minuten duren voordat het site-overzicht in het raster wordt weergegeven.

## Stap 3. Robots.txt configureren en inschakelen (optioneel)

Voltooi de [&#x200B; robots van de onderzoeksmotor &#x200B;](seo-overview.md#search-engine-robots) configuratie met instructies die de directe onderzoeksmotoren om de delen van uw plaats kruipen die u wilt worden geïndexeerd.

## Stap 4. Uw site-overzicht verzenden naar zoekprogramma&#39;s

U kunt uw site-overzicht naar verschillende zoekprogramma&#39;s verzenden door deze de koppeling te geven naar het `sitemap.xml` -bestand in uw Commerce-installatie. Ga als volgt te werk om de koppeling te kopiëren:

1. In de _lijst van de Kaart van de Plaats_, klik URL in de **[!UICONTROL Link for Google]** kolom met de rechtermuisknop aan.

1. Kies **[!UICONTROL Copy Link Address]** in het menu.

Zie de instructies voor de specifieke zoekfunctie voor meer informatie. Hier volgt een koppeling naar de instructies voor twee zoekprogramma&#39;s bovenaan:

- [ Google ][2]
- [ Microsoft® Bing ][3]

## Stap 5: vorige instructies voor robot herstellen (optioneel)

U kunt nu de oorspronkelijke (standaard)beperkingen herstellen.

## Sitemaps en robots.txt beheren voor meerdere websites

Als u meerdere websites hebt, kunt u het maken en verzenden van sitemaps vereenvoudigen. Eenvoudig [&#x200B; creeer &#x200B;](#site-map-configuration) één of meerdere zetemaps die URLs voor al uw geverifieerde opslag omvatten en sparen de sitemaps aan één enkele plaats. Alle plaatsen moeten in [&#x200B; de Console van het Onderzoek van Google &#x200B;](https://support.google.com/webmasters/answer/7451001) worden geverifieerd.

Ga als volgt te werk om sitemaps voor een instantie van meerdere winkels te maken:

1. Maak een map met de naam `sitemaps` in de hoofdmap van uw website en maak vervolgens submappen voor elk domein:

        /sitemaps/domain_1/
        /sitemaps/domain_2/
   
1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Maak of bewerk de sitemapaanbiedingen voor elke winkel en stel de **[!UICONTROL Path]** in op de sitemapaanbiedingen die u voor de winkel hebt gemaakt:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Werk indien nodig het bestand robots.txt bij.

   Als u er zeker van wilt zijn dat de spinnen van de zoekmachine correct naar de nieuwe sitemaps worden geleid, kunt u het bestand robots.txt bijwerken of maken. Voeg de volgende regels bovenaan toe.

        Sitemap van de Website 
        Sitemap: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
        Sitemap: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Als uw plaats de [&#x200B; Apache &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html?lang=nl-NL) motor van de Webserver gebruikt, zou u het [`.htaccess` &#x200B;](https://httpd.apache.org/docs/current/howto/htaccess.html) dossier in de wortel van uw website moeten bijwerken om het even welke andere verzoeken sitemap aan de juiste plaats te leiden.

## Kolombeschrijvingen

| Kolom | Beschrijving |
|------|-----------|
| [!UICONTROL ID] | Het opeenvolgende recordnummer van het huidige site-overzicht. |
| [!UICONTROL Filename] | De bestandsnaam van het site-overzicht. |
| [!UICONTROL Path] | De locatie waar het site-overzicht zich op de server bevindt. Bijvoorbeeld: <br/>`/sitemap/` - Plaatst het dossier van het plaatskaart in een folder genoemd _sitemap_, één niveau onder de wortel van de installatie van Commerce. <br/>`/` - Plaatst het bestand met het site-overzicht op het basispad of de hoofdmap van de Commerce-installatie. |
| [!UICONTROL Link for Google] | De URL van het site-overzicht dat moet worden verzonden naar Google en andere zoekprogramma&#39;s. |
| [!UICONTROL Last Generated] | Geeft de datum en tijd aan waarop het site-overzicht voor het laatst is gegenereerd. |
| [!UICONTROL Store View] | De archiefweergave waarop het site-overzicht van toepassing is. |
| [!UICONTROL Generate] | Hiermee herstelt u het site-overzicht. |

{style="table-layout:auto"}

## Configuratie van site-overzicht

Uw site-overzicht moet zo vaak worden bijgewerkt als de inhoud op uw site verandert, mogelijk dagelijks, wekelijks of maandelijks. Met de configuratie kunt u de frequentie en de prioriteit voor elk type inhoud instellen.

### Stap 1. De frequentie en prioriteit van inhoudsupdates instellen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL XML Sitemap]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Categories Options]** sectie uit en doe het volgende:

   >[!NOTE]
   >
   >Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

   - Stel **[!UICONTROL Frequency]** in op een van de volgende opties:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Voer bij **[!UICONTROL Priority]** een waarde in tussen `0.0` en `1.0` . Nul heeft de laagste prioriteit.

   ![&#x200B; sitemap van XML - de opties van Categorieën &#x200B;](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [&#x200B; Opties van Categorieën &#x200B;](../configuration-reference/catalog/xml-sitemap.md#categories-options) in de _Verwijzing van de Configuratie_.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Products Options]** sectie uit en voltooi **[!UICONTROL Frequency]** en **[!UICONTROL Priority]** montages zoals nodig.

   Voor een gedetailleerde lijst van deze opties, zie [&#x200B; Opties van Producten &#x200B;](../configuration-reference/catalog/xml-sitemap.md#products-options) in de _Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Add Images into Sitemap]** in op een van de volgende opties om te bepalen in hoeverre afbeeldingen worden opgenomen in de sitemap:

   - `None`
   - `Base Only`
   - `All`

   ![&#x200B; configuratie van de Catalogus - de producten van XML sitemap &#x200B;](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL CMS Pages Options]** sectie uit en voltooi **[!UICONTROL Frequency]** en **[!UICONTROL Priority]** montages zoals nodig.

   ![&#x200B; configuratie van de Catalogus - de pagina&#39;s van CMS van XML sitemap &#x200B;](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie {de Opties van de Pagina&#39;s van 0} CMS [&#128279;](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) in de _Verwijzing van de Configuratie_.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Store Url Options]** sectie uit en voltooi **[!UICONTROL Frequency]** en **[!UICONTROL Priority]** montages zoals nodig.

   ![&#x200B; configuratie van de Catalogus - de opslag URL van XML sitemap &#x200B;](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [&#x200B; Opties van de Opslag Url &#x200B;](../configuration-reference/catalog/xml-sitemap.md#store-url-options) in de _Verwijzing van de Configuratie_.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Stap 2. De instellingen voor genereren voltooien

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Generation Settings]** sectie uit.

   Indien nodig, ontruim het **checkbox van de systeemwaarde van het 0&rbrace; Gebruik om deze montages te veranderen.**

   ![&#x200B; configuratie van de Catalogus - de montages van de de sitemapgeneratie van XML &#x200B;](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [&#x200B; Montages van de Generatie &#x200B;](../configuration-reference/catalog/xml-sitemap.md#generation-settings) in de _Verwijzing van de Configuratie_.

1. Als u een sitemap wilt genereren, stelt u **[!UICONTROL Enabled]** in op `Yes` en voert u de volgende handelingen uit:

   - Stel **[!UICONTROL Start Time]** in op het uur, de minuut en de seconde waarop u de sitemap wilt bijwerken.

   - Stel **[!UICONTROL Frequency]** in op een van de volgende opties:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - Voer voor **[!UICONTROL Error Email Recipient]** het e-mailadres in van de persoon die de melding moet ontvangen als er een fout optreedt tijdens een sitemap-update.

   - Stel **[!UICONTROL Error Email Sender]** in op de contactpersoon van de winkel die wordt weergegeven als de afzender van de foutmelding.

   - Stel **[!UICONTROL Error Email Template]** in op de sjabloon die wordt gebruikt voor de foutmelding.

### Stap 3. Limieten instellen voor bestanden in het site-overzicht

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Sitemap File Limits]** sectie uit.

   ![&#x200B; configuratie van de Catalogus - de beperkingen van het de sitemapdossier van XML &#x200B;](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie {de Limieten van het Dossier van 0} Sitemap [&#128279;](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) in de _Verwijzing van de Configuratie_.

1. Voer bij **[!UICONTROL Maximum No of URLs per File]** het maximumaantal URL&#39;s in dat in de sitemap kan worden opgenomen.

   De standaardwaarde is 50.000.

1. Voer bij **[!UICONTROL Maximum File Size]** de grootste grootte in bytes in die voor de sitemap is toegewezen.

   De standaardgrootte is 10.485.760 bytes.

### Stap 4. De verzendinstellingen voor de zoekmachine instellen

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Submission Settings]** sectie uit.

   ![&#x200B; configuratie van de Catalogus - de voorleggingsmontages van de de sitemaponderzoek van XML &#x200B;](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable Submission to Robots.txt]** in op `Yes` als u instructies gebruikt aan zoekprogramma&#39;s die door uw site kruipen.`robots.txt`

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html?lang=nl-NL
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
