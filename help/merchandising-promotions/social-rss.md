---
title: Sociale media en RSS-feeds
description: Leer hoe u sociale media en andere RSS-voederintegratie toevoegt om merk- en productbewustzijn te creëren.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Sociale media en RSS-feeds

Veel handelaren gebruiken sociale media en andere digitale hulpmiddelen om merk- en productbewustzijn te creëren. U kunt uw winkel integreren met uw sociale netwerken door een Marketplace-extensie te installeren of door een plug-in toe te voegen aan de pagina&#39;s met inhoud. Gebruik RSS-feeds om uw productinformatie te publiceren naar winkelverzamelingssites en deze zelfs op te nemen in uw nieuwsbrieven. Klanten kunnen zich abonneren op uw RSS-feeds om meer te leren over nieuwe producten en promoties.

## Sociale netwerken

Uw winkel kan verbinding maken met sociale netwerken door een [Marketplace-extensie](../getting-started/commerce-marketplace.md). Bovendien kunt u eenvoudig sociale plug-ins toevoegen, zoals de _leuk_ naar CMS-blokken die in de gehele winkel in pagina&#39;s kunnen worden opgenomen.

De sociale voorzien van een netwerkplaatsen hebben talrijke stop-ins die gemakkelijk aan uw opslag kunnen worden toegevoegd. Daarnaast bevat de Commerce Marketplace veel extensies die u kunt gebruiken om uw winkel te integreren met sociale media. In het volgende voorbeeld wordt getoond hoe u een Facebook kunt toevoegen _leuk_ aan uw winkel.

>[!NOTE]
>
>Adobe Commerce heeft de native _Magento sociaal_ Facebook-integratie en ondersteunt de extensie niet meer. Ga naar de [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} om alternatieve extensies te zoeken voor Facebook-integratie.

### Stap 1. De knopcode ophalen

1. Ga op de website van Meta-ontwikkelaars naar [knopinstelling](https://developers.facebook.com/docs/plugins/like-button) pagina.

1. Voor **[!UICONTROL URL to Like]**, voert u de URL in van de pagina in uw winkel die u wilt laten weergeven aan _leuk_.

   U kunt bijvoorbeeld de URL van de homepage van uw winkel invoeren.

1. Kies de optie **[!UICONTROL Layout]** voor de knop.

1. Voer de **[!UICONTROL Width]** in pixels die op uw site beschikbaar zijn voor de knop en eventuele bijbehorende tekstberichten.

1. Set **[!UICONTROL Action Type]** op een van de volgende wijzen:

   - `Like`
   - `Recommend`

1. Klikken **[!UICONTROL Get Code]** om de gegenereerde code naar het klembord te kopiëren.

### Stap 2. Een inhoudsblok maken

1. Ga terug naar de beheerder van uw winkel.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Block]**.

1. Voer een beschrijving in **[!UICONTROL Block Title]** voor interne referentie.

   Bijvoorbeeld: `Facebook Like Button`.

1. Een unieke waarde toewijzen **[!UICONTROL Identifier]** op het blok, met alle kleine letters en onderstrepingstekens in plaats van spaties.

   Bijvoorbeeld: `facebook_like_button`.

1. Als uw instantie van de Handel veelvoudige opslagmeningen heeft, kies elk **[!UICONTROL Store View]** wanneer het blok beschikbaar moet zijn.

1. Voeg het codefragment toe aan de blokinhoud, afhankelijk van het gereedschap Inhoud:

   - Wanneer u [!DNL Page Builder], voegt u een [HTML-code](../page-builder/html-code.md) naar het werkgebied en plak het codefragment dat u van de Facebook-site hebt gekopieerd. Anders plakt u het codefragment in de **[!UICONTROL Content]** doos.

   - Plak met de editor het codefragment dat u van de Facebook-site hebt gekopieerd naar de **[!UICONTROL Content]** doos.

1. Als het blok niet klaar is om live te gaan, stelt u **[!UICONTROL Enable Block]** tot `No`.

1. Klik op **[!UICONTROL Save Block]**.

### Stap 3. Plaats het blok

1. Voeg het blok toe, afhankelijk van het inhoudsgereedschap:

   - Wanneer u [!UICONTROL Page Builder]volgt u de instructies op [Voeg het blok toe](../page-builder/block.md) naar het werkgebied.

   - Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]** en voer de volgende handelingen uit:

   - ![B2B voor Adobe Commerce](../assets/b2b.svg) (Alleen beschikbaar bij B2B voor Adobe Commerce) In de _Instellingen_ sectie, set **[!UICONTROL Type]** tot `CMS Static Block` en klik op **[!UICONTROL Continue]**.

   - Controleren of **[!UICONTROL Design Theme]** wordt ingesteld op het huidige thema.

   - Klik op **[!UICONTROL Continue]**.

1. In de **[!UICONTROL Storefront Properties]** Ga als volgt te werk:

   - Voor **[!UICONTROL Widget Title]** voert u een titel in voor interne referentie.

   - Set **[!UICONTROL Assign to Store Views]** tot `All Store Views`of naar de weergave waar de app beschikbaar moet zijn. Als u meerdere weergaven wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   - Voer een getal in het dialoogvenster **[!UICONTROL Sort Order]** veld om de volgorde van het blok te bepalen als dit is toegewezen voor weergave op dezelfde locatie op de pagina als andere inhoudselementen. De bovenste positie is nul.

1. In de _[!UICONTROL Layout Updates]_sectie, klikken **[!UICONTROL Add Layout Update]**en instellen **[!UICONTROL Display On]**naar de categorie, het product of de pagina waarop u het blok wilt weergeven.

   Als u bijvoorbeeld `All Pages` en plaats het blok in of kopbal of footer, verschijnt het blok op de zelfde plaats op elke pagina van de opslag.

   Ga als volgt te werk om het blok op een specifieke pagina te plaatsen:

   - Set **[!UICONTROL Display On]** tot `Specified Page` en selecteert u de **[!UICONTROL Page]** waar u het blok wilt weergeven.

   - Kies de optie **[!UICONTROL Block Reference]** om de plaats op de pagina te identificeren waar het blok moet worden geplaatst.

   - Accepteer de standaardinstelling voor **[!UICONTROL Template]**, die is ingesteld op `CMS Static Block Default Template`.

   - Klik op **[!UICONTROL Save and Continue Edit]**.

1. Kies in het deelvenster aan de linkerkant de optie **[!UICONTROL Widget Options]**.

1. Klikken **[!UICONTROL Select Block…]** en kiest u het blok dat u wilt plaatsen.

1. Klik op **[!UICONTROL Save]**.

1. Volg desgevraagd de instructies boven aan de werkruimte om de index en de paginacache bij te werken.

   De widget wordt nu weergegeven in het deelvenster _[!UICONTROL Widgets]_lijst.

### Stap 4. De locatie in de winkel controleren

Ga terug naar de winkel om te controleren of het blok zich op de juiste locatie bevindt. Als u het blok wilt verplaatsen, kunt u de widget opnieuw openen en een andere pagina of blokverwijzing proberen.

## RSS-feeds

RSS (Echt Eenvoudige Syndicatie) is een op XML-Gebaseerd gegevensformaat dat wordt gebruikt om informatie online te verspreiden. Uw klanten kunnen op uw voer van RSS intekenen om over nieuwe producten en promoties te leren. RSS-feeds kunnen ook worden gebruikt om uw productinformatie te publiceren naar winkelverzamelplaatsen en kunnen worden opgenomen in nieuwsbrieven.

Wanneer RSS-feeds zijn ingeschakeld, worden eventuele toevoegingen aan producten, specials, categorieën en coupons automatisch naar de abonnees van elke feed verzonden. Een koppeling naar alle RSS-feeds die u publiceert, staat in de voettekst van uw winkel.

![RSS-feed, pictogram](./assets/icon-rss.png){width="100"}<br/>

De software die nodig is om een RSS-feed te lezen, wordt een feed-lezer genoemd en stelt mensen in staat zich te abonneren op koppen, blogs, podcasts en nog veel meer. Google Reader is een van de vele feed-lezers die gratis online beschikbaar zijn.

![Voorbeeld van storefront - RSS-feed](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Voordelen van het opzetten van een RSS-feed

- Download de nieuwste update van uw winkel of blog
- Lichtadvertenties
- Gewone aandelen
- SEO verhogen
- Verhoog de verkoop

### Typen RSS-feeds

| RSS Feed | Beschrijving |
|--- |--- |
| [!UICONTROL Wish List] | Als deze optie is ingeschakeld, wordt boven aan de pagina&#39;s met verlanglijsten voor klanten een koppeling naar de RSS-feed weergegeven. Bovendien bevat de pagina voor het delen van wensenlijsten een selectievakje waarmee u een koppeling naar de feed kunt opnemen vanuit lijsten met gedeelde wensen. |
| [!UICONTROL New Products] | Hiermee publiceert u een melding van nieuwe producten die aan de catalogus zijn toegevoegd. |
| [!UICONTROL Special Products] | Publiceert kennisgeving van producten met speciale prijzen. |
| [!UICONTROL Coupons / Discounts] | Hiermee wordt melding gepubliceerd van speciale coupons of kortingen die beschikbaar zijn in de winkel. |
| [!UICONTROL Top Level Category] | Hiermee publiceert u een melding van elke wijziging in de categoriestructuur op hoofdniveau van uw catalogus. Deze wijziging wordt weerspiegeld in het hoofdmenu. |
| [!UICONTROL Customer Order Status] | Biedt klanten de mogelijkheid hun orderstatus te volgen met RSS-feed. Als deze optie is ingeschakeld, wordt een koppeling naar de RSS-feed in de volgorde weergegeven. |

{style="table-layout:auto"}

### RSS-feeds instellen voor uw winkel

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In de rechterbovenhoek stelt u **[!UICONTROL Store View]** de weergaven waar de diervoeders beschikbaar moeten zijn.

   Als u wordt gevraagd te bevestigen, klikt u op **[!UICONTROL OK]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL RSS Feeds]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Rss Config]** sectie en set **[!UICONTROL Enable RSS]** tot `Enable`.

   ![Catalogusconfiguratie - RSS-feeds](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Indien nodig de **[!UICONTROL Use Default]** Schakel het selectievakje in om de standaardwaarde te wijzigen.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Wish List]** sectie en set **[!UICONTROL Enable RSS]** tot `Enable`.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Catalog]** sectie en andere feeds instellen op `Enable` indien nodig.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catalogus - instellingen voor RSS-feeds](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie en set **[!UICONTROL Customer Order Status Notification]** tot `Enable`.

1. Klik op **[!UICONTROL Save Config]**.

1. Zie het resultaat op de winkel met `/rss` aan het einde van de pagina-URL.

