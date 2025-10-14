---
title: Winkel- en sitestructuur
description: Leer meer over de website, de opslag, en de hiërarchie van de opslagmening.
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Winkel- en sitestructuur

Wanneer Adobe Commerce of Magento Open Source is geïnstalleerd, wordt een hiërarchie gemaakt die een hoofdwebsite, winkel en winkelweergave bevat. Desgewenst kunt u aanvullende websites, winkels en winkelweergaven maken. Naast uw hoofdwebsite hebt u bijvoorbeeld mogelijk aanvullende websites met een ander domein. Binnen elke website kunt u meerdere winkels gebruiken en in elke winkel aparte weergaven voor de winkel. Veel installaties hebben één website en één winkel, maar met meerdere opslagweergaven om verschillende talen te ondersteunen.

Voordat u begint, plant u de catalogushiërarchie van uw winkel van tevoren, omdat in de hele configuratie naar deze hiërarchie wordt verwezen. Elke opslag kan een afzonderlijke [&#x200B; wortelcategorie &#x200B;](../catalog/category-root.md) hebben, die het mogelijk maakt om een volledig verschillende reeks belangrijkste menuopties voor elke opslag te hebben.

![&#x200B; diagram van het Reikwijdte &#x200B;](./assets/scope-multisite.svg){width="550"}

## Opslag toevoegen

Eén installatie van Adobe Commerce of Magento Open Source kan meerdere opslagruimten hebben die een beheerder delen. Winkels die zich onder dezelfde website bevinden, hebben hetzelfde IP-adres en hetzelfde domein, gebruiken hetzelfde beveiligingscertificaat en delen één afrekenproces.

Belangrijk is dat de winkels dezelfde code gebruiken en een beheerder delen. Elke winkel kan een aparte catalogus hebben of de opslagruimten kunnen een catalogus delen. Elke opslag kan een afzonderlijke [&#x200B; wortelcategorie &#x200B;](../catalog/category-root.md) hebben, die het mogelijk maakt om een verschillend hoofdmenu voor elke opslag te hebben. Winkels kunnen ook verschillende branding, presentatie en inhoud hebben. Neem wat tijd om uw opslaghiërarchie met toekomstige groei in mening te plannen alvorens u begint, omdat het door de configuratie wordt gebruikt.

![&#x200B; Reikwijdte - veelvoudige opslag &#x200B;](./assets/scope-multistore.svg){width="550"}

Hier zijn sommige voorbeelden van hoe URLs voor veelvoudige opslag kan worden gevormd:

| URL | Beschrijving |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | Elke winkel heeft een ander pad, maar deelt een domein. |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | Elke opslag heeft een verschillend subdomein van het primaire domein. |

Installaties voor meerdere opslagruimten van Adobe Commerce moeten worden geconfigureerd via de beheerfunctie en ook vanaf de opdrachtregel van de server. De Gids van de Configuratie van Adobe Commerce [&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=nl-NL) verstrekt gedetailleerde instructies voor het vormen van het servermilieu.

### Stap 1: kies het archiefdomein

De eerste stap bestaat uit het kiezen van de positie van de winkel. Moeten de opslag een domein delen, elk hebben subdomain, of duidelijk verschillende domeinen? Voer voor elke winkel een van de volgende handelingen uit:

- Als u de winkel één niveau onder het primaire domein wilt plaatsen, hoeft u niets te doen.
- Stel een subdomein van uw primaire domein in.
- Stel een ander primair domein in.

### Stap 2: De winkel maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klik op **[!UICONTROL Create Store]** en stel de opties voor de nieuwe winkel in:

   - **[!UICONTROL Web Site]** — Kies een website die de bovenliggende website van de nieuwe winkel moet zijn. Accepteer de standaardwaarde (`Main Website`) als de installatie slechts één website heeft.

   - **[!UICONTROL Name]** — Voer een naam in voor de nieuwe winkel. De naam is alleen bedoeld voor interne referentie.

   - **[!UICONTROL Code]** — Voer een code in kleine letters in om de winkel te identificeren. Bijvoorbeeld: `mainstore` .

   - **[!UICONTROL Root Category]** — Reeks aan de [&#x200B; wortelcategorie &#x200B;](../catalog/category-root.md) die de categoriestructuur voor het belangrijkste menu van de nieuwe opslag bepaalt. Als u al een specifieke hoofdcategorie voor de winkel hebt gemaakt, selecteert u deze. Anders selecteert u `Default Category` . U kunt later terugkomen en het plaatsen bijwerken.

   ![&#x200B; creeer Opslag - opslagopties &#x200B;](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Store]**.

### Stap 3: Een standaardwinkelweergave maken

1. Klik op **[!UICONTROL Create Store View]** en stel de weergaveopties voor de winkel in:

   - **[!UICONTROL Store]** — Instellen op de nieuwe winkel die u hebt gemaakt.

   - **[!UICONTROL Name]** — Voer een naam in voor de weergave. Bijvoorbeeld `English` .

   - **[!UICONTROL Code]** — Voer een code in voor de weergave in kleine letters.

   - **[!UICONTROL Status]** — Ingesteld op `Enabled` .

   - **[!UICONTROL Sort Order]** — Voer een getal in om de positie van de winkel te bepalen wanneer deze bij andere winkels wordt vermeld.

1. Klik op **[!UICONTROL Save Store View]**.

   Als u de winkel opent in de bewerkingsmodus, ziet u dat deze nu een standaardweergave heeft.

   ![&#x200B; Nieuwe opslag met standaardmening &#x200B;](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### Stap 4: De URL van de winkel configureren

1. Voor _Admin_ sidebar, klik **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies onder _[!UICONTROL General]_&#x200B;in het linkerdeelvenster aan de linkerkant de optie **[!UICONTROL Web]**.

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op de weergave die u voor de nieuwe winkel hebt gemaakt.

1. Wanneer ertoe aangezet om [&#x200B; werkingsgebied &#x200B;](../getting-started/websites-stores-views.md#scope-settings) omschakeling te bevestigen, klik **[!UICONTROL OK]**.

   ![&#x200B; kies de opslagmening &#x200B;](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Base URLs]** sectie uit en ga basis URL voor de opslag in.

   Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om de instelling te wijzigen.

   ![&#x200B; Algemene configuratie - Web basis URLs &#x200B;](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Secure Base URLs]** sectie uit en herhaal de vorige stap als u de opslag [&#x200B; veilige URL &#x200B;](store-urls.md) wilt vormen.

1. Klik op **[!UICONTROL Save Config]**.

### Stap 5: Configureer de server

Om uw server te vormen om veelvoudige websites te steunen, zie [&#x200B; Veelvoudige websites of opslag &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=nl-NL) in de _Gids van de Configuratie_.

Zie de volgende bronnen voor hulp bij het configureren van uw webserver:

- [&#x200B; Opstelling veelvoudige websites met NGNX &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html?lang=nl-NL)
- [&#x200B; Opstelling veelvoudige websites met Apache &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html?lang=nl-NL)

Voor Adobe Commerce op wolkeninfrastructuur, zie [&#x200B; Opstelling veelvoudige websites of opslag &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html?lang=nl-NL).

## Websites toevoegen

U kunt meerdere websites instellen vanuit één Adobe Commerce- of Magento Open Source-installatie met hetzelfde domein of verschillende domeinen. Standaard hebben opslagruimten die zich onder dezelfde website bevinden, hetzelfde IP-adres en hetzelfde domein, gebruiken ze hetzelfde beveiligingscertificaat en delen ze één afrekenproces. Als u elke opslag een specifiek controleproces onder zijn eigen domein wilt hebben, moet elke opslag een verschillend IP adres en een afzonderlijk veiligheidscertificaat hebben.

Installaties van Adobe Commerce of Magento Open Source op meerdere locaties moeten worden geconfigureerd via de beheerfunctie en ook via de opdrachtregel van de server. De Gids van de Configuratie van Commerce [&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=nl-NL) verstrekt gedetailleerde instructies voor het vormen van het servermilieu.

![&#x200B; Reikwijdte - websites &#x200B;](./assets/scope-multisite.svg){width="550"}

### Stap 1: Een website maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Create Website]** .

1. Stel de opties voor **[!UICONTROL Web Site Information]** in:

   ![&#x200B; creeer website - opties &#x200B;](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]** — Voer het domein van de nieuwe website in. Bijvoorbeeld `domain.com` .

   - **[!UICONTROL Code]** — Voer een code in die op de server wordt gebruikt om naar het domein te wijzen.

     De code moet beginnen met een kleine letter (a-z) en kan elke combinatie van letters (a-z), cijfers (0-9) en het onderstrepingsteken (_) bevatten.

   - **[!UICONTROL Sort Order]** — _(Facultatief)_ ga een aantal in om de opeenvolging te bepalen waarin deze plaats met andere plaatsen vermeld is. Om deze plaats bij de bovenkant van de lijst te maken verschijnen, ga nul (`0`) in.

1. Klik op **[!UICONTROL Save Web Site]**.

1. Opstelling elk [&#x200B; opslag &#x200B;](#add-stores) en [&#x200B; opslagmening &#x200B;](store-views.md) die voor de nieuwe website nodig is.

   Vervolgens kunt u de website openen in de bewerkingsmodus om de standaardopslag in te stellen.

### Stap 2: Vorm de opslag URL

Om de [&#x200B; opslag URLs &#x200B;](store-urls.md) te vormen, volg de instructies.

### Stap 3: Configureer de server

Om uw server te vormen om veelvoudige websites te steunen, zie [&#x200B; Veelvoudige websites of opslag &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=nl-NL) in de _Gids van de Configuratie_.

Raadpleeg de volgende zelfstudies voor hulp bij het configureren van uw webserver:

- [&#x200B; Opstelling veelvoudige websites met NGNX &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html?lang=nl-NL)
- [&#x200B; Opstelling veelvoudige websites met Apache &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html?lang=nl-NL)

Voor Adobe Commerce op wolkeninfrastructuur, zie [&#x200B; Opstelling veelvoudige websites of opslag &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html?lang=nl-NL).
