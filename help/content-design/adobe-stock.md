---
title: Adobe Stock-integratie
description: Adobe Stock integreren met uw [!DNL Commerce] toegang tot talloze media-elementen voor gebruik in uw winkel.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock-integratie

Als u toegang wilt krijgen tot talloze media-elementen die u in uw winkel kunt gebruiken, kunt u [Adobe Stock][adobe-stock] with [!UICONTROL Commerce].

![Adobe Stock-zoekresultaten](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

De Adobe Stock-service biedt bedrijven toegang tot miljoenen hoogwaardige, gekrulde, royaltyvrije foto&#39;s, vectoren, illustraties, video&#39;s, sjablonen en 3D-middelen voor al hun creatieve projecten. [!DNL Commerce] gebruikers kunnen Adobe Stock-middelen snel zoeken, voorvertonen en licentiëren. Gebruikers kunnen deze ook opslaan in de [media-opslag][media-storage], allemaal zonder de beheerwerkruimte te verlaten.

## Vereisten

Deze integratie vereist:

- An [Adobe Developer][dev-console] account
- Adobe Commerce of Magento Open Source, 2.3.4 of hoger

Voor licenties voor Adobe Stock-afbeeldingen is het volgende vereist:

- An [Adobe][adobe-signin]
- Betaald [Adobe Stock][adobe-stock] aan de account gekoppeld plan

## Integreren [!DNL Commerce] en Adobe Stock

Het configureren van de Adobe Stock-integratie voor Adobe Commerce bestaat uit twee stappen:

1. [Een integratie met adobe.developer maken](#create-an-adobe-developer-integration) om een API-sleutel te genereren
1. [De Adobe Stock-integratie configureren in Commerce Admin](#configure-the-adobe-stock-integration)

### Een Adobe Developer-integratie maken

1. Ga naar de [Adobe Developer Console][dev-console].

1. Onder _[!UICONTROL Quick Start]_, klikt u op **[!UICONTROL Create new project]**.

1. In de _[!UICONTROL Project overview]_blok, klik **[!UICONTROL Add API]**.

1. Selecteren **[!UICONTROL Adobe Stock]** van de integratielijst en klik op **[!UICONTROL Next]**.

1. OAuth 2.0 selecteren **[!UICONTROL Web App]**.

1. Geef de **[!UICONTROL redirect URI]**.

   De standaard omleidings-URI bevindt zich in de vorm `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, zoals `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, waarbij:

   - `${HOST}` is uw [!DNL Commerce] volledig gekwalificeerde domeinnaam (bijvoorbeeld `https://store.myshop.com`).
   - `${ADMIN_URI}` is uw [!DNL Commerce] Admin URI (zoals `admin_hgkq1l`), die kan worden opgehaald door te lopen `magento info:adminuri`.

1. Geef de **[!UICONTROL Redirect URI pattern]**, die hetzelfde is als de omleiding van URI met twee verschillen:

   - Alle perioden (`.`) moet met twee backslashes worden beschermd (`\\`).
   - Toevoegen `.*` tot het einde van het patroon.

   Als u het voorbeeld van de vorige standaard omleidings-URI gebruikt, wordt deze `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Klik op **[!UICONTROL Next]**.

1. Bekijk het beschikbare bereik en klik op **[!UICONTROL Save configured API]**.

1. Kopieer op de volgende pagina uw **[!UICONTROL Client ID]** (API-sleutel) en **[!UICONTROL Client secret]**.

   Deze informatie wordt gebruikt in stappen van de volgende sectie.

### De Adobe Stock-integratie configureren

Om de systeemconfiguratie in uw te plaatsen [!DNL Commerce] Admin, gebruik _API-sleutel_ en _Clientgeheim_ in het [vorige sectie][create-integration].

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Enabled Adobe Stock]** tot `Yes`.

   - Voer uw **[!UICONTROL API Key (Client ID)]**.

   - Voer uw **[!UICONTROL Client Secret]**.

   - Klikken **[!UICONTROL Test Connection]** om uw toetsen te valideren.

   ![Geavanceerde configuratie - Adobe Stock-integratie](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Geef de validatie een paar seconden. Als uw referenties geldig zijn, wordt een groene _Verbinding gelukt!_ bericht.

1. Klik op **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
