---
title: Adobe Stock-integratie
description: Integreer Adobe Stock met uw  [!DNL Commerce]  instantie om tot talloze media activa voor gebruik in uw opslag toegang te hebben.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 0d072ecdba696383bd33b88b64d751736429f2f6
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Adobe Stock-integratie

Om toegang tot ontelbare media activa voor gebruik in uw opslag te krijgen, integreer [ Adobe Stock ][adobe-stock] met [!UICONTROL Commerce].

![ Resultaten van het Onderzoek van Adobe Stock ](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

De Adobe Stock-service biedt bedrijven toegang tot miljoenen hoogwaardige, gekrulde, royaltyvrije foto&#39;s, vectoren, illustraties, video&#39;s, sjablonen en 3D-middelen voor al hun creatieve projecten. [!DNL Commerce] -gebruikers kunnen snel Adobe Stock-elementen zoeken, voorvertonen en in licentie geven. De gebruikers kunnen hen aan de [ media opslag ](./media-storage.md) ook bewaren, allen zonder de werkruimte te verlaten Admin.

## Vereisten

Deze integratie vereist:

- Een [ Adobe Developer ][dev-console] rekening
- Adobe Commerce of Magento Open Source, 2.3.4 of hoger

Voor licenties voor Adobe Stock-afbeeldingen is het volgende vereist:

- Een [ rekening van de Adobe ][adobe-signin]
- Een betaald &rbrack;[adobe-stock] plan van Adobe Stock &lbrack; verbonden aan de rekening

## Integreer [!DNL Commerce] en Adobe Stock

Het configureren van de Adobe Stock-integratie voor Adobe Commerce bestaat uit twee stappen:

1. [ creeer een integratie adobe.developer ](#create-an-adobe-developer-integration) om een API Sleutel te produceren
1. [De Adobe Stock-integratie configureren in Commerce Admin](#configure-the-adobe-stock-integration)

### Een Adobe Developer-integratie maken

1. Navigeer aan [ Adobe Developer Console ][dev-console].

1. Klik onder _[!UICONTROL Quick Start]_&#x200B;op **[!UICONTROL Create new project]**.

1. Klik in het blok _[!UICONTROL Project overview]_&#x200B;op **[!UICONTROL Add API]**.

1. Selecteer **[!UICONTROL Adobe Stock]** in de lijst Integraties en klik op **[!UICONTROL Next]** .

1. Selecteer OAuth 2.0 **[!UICONTROL Web App]**.

1. Geef de waarde **[!UICONTROL redirect URI]** op.

   De standaard omleidings-URI heeft de vorm `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/` , bijvoorbeeld `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/` , waarin:

   - `${HOST}` is de [!DNL Commerce] volledig gekwalificeerde domeinnaam (bijvoorbeeld `https://store.myshop.com` ).
   - `${ADMIN_URI}` is de [!DNL Commerce] Admin URI (zoals `admin_hgkq1l` ), die kan worden opgehaald door `magento info:adminuri` uit te voeren.

1. Geef de waarde **[!UICONTROL Redirect URI pattern]** op. Deze waarde is gelijk aan de manier waarop u de URI omleidt met twee verschillen:

   - Om het even welke periodes (`.`) moeten met twee backslashes (`\\`) worden ontsnapt.
   - Voeg `.*` toe aan het einde van het patroon.

   Als u het voorbeeld van de vorige standaard omleidings-URI gebruikt, is dit `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*` .

1. Klik op **[!UICONTROL Next]**.

1. Controleer het beschikbare bereik en klik op **[!UICONTROL Save configured API]** .

1. Kopieer op de volgende pagina de **[!UICONTROL Client ID]** (API-sleutel) en **[!UICONTROL Client secret]** .

   Deze informatie wordt gebruikt in stappen van de volgende sectie.

### De Adobe Stock-integratie configureren

Om de systeemconfiguratie in uw [!DNL Commerce] Admin te plaatsen, gebruik _API Sleutel_ en _het geheim van de Cliënt_ in de [ vorige sectie ][create-integration] wordt geproduceerd.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** uit en doe het volgende:

   - Stel **[!UICONTROL Enabled Adobe Stock]** in op `Yes` .

   - Voer uw **[!UICONTROL API Key (Client ID)]** in.

   - Voer uw **[!UICONTROL Client Secret]** in.

   - Klik op **[!UICONTROL Test Connection]** om uw toetsen te valideren.

   ![ Geavanceerde configuratie - de integratie van Adobe Stock ](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Geef de validatie een paar seconden. Als uw geloofsbrieven geldig zijn, zou u een groene _Succesvolle Verbinding moeten zien!_ -bericht.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/nl/manage-account/using/access-adobe-id-account.html
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
