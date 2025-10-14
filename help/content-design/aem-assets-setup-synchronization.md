---
title: De integratie configureren
description: Leer hoe u uw Adobe Commerce- en Experience Manager Assets-projecten kunt verbinden om de synchronisatie van bedrijfsmiddelen tussen deze twee systemen mogelijk te maken.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: f01ba239d885d96285186e35361a8d40f2f68e4e
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# De integratie configureren

Configureer de integratie door Commerce aan te sluiten op de AEM Assets-instantie en de bijbehorende strategie voor de synchronisatie van bedrijfsmiddelen te selecteren.

Nadat u het AEM Assets-project hebt geïdentificeerd, selecteert u de regel voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

- **[!UICONTROL Match by product SKU]** - Standaard regel die SKU in de activameta-gegevens met het [&#x200B; product SKU van Commerce &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce-operations/implementation-playbook/glossary#sku) aanpast om ervoor te zorgen dat de activa met de correcte producten worden geassocieerd.

- **[!UICONTROL Custom match]** - Het stemmen regel voor complexere scenario&#39;s of specifieke bedrijfsvereisten die aangepaste passende logica vereisen. Voor het implementeren van aangepaste overeenkomsten moet in Adobe Developer App Builder aangepaste code worden ontwikkeld om te bepalen hoe elementen op producten worden afgestemd. Binnenkort komen er meer details...

Voor de aanvankelijke opstelling, gebruik de standaard *Gelijke door productSKU* regel.

## Vereisten

- [AEM Assets-pakket installeren](aem-assets-configure-aem.md)

- [&#x200B; installeer de pakketten van Adobe Commerce &#x200B;](aem-assets-configure-commerce.md) om de uitbreiding toe te voegen en de vereiste geloofsbrieven en de verbindingen te produceren om de uitbreiding te gebruiken.

- Maak een ondersteuningsticket voor de AEM Assets for Commerce Integration. Neem in het ticket de **[!UICONTROL Program ID]** , **[!UICONTROL Environment ID]** en **[!UICONTROL IMS Org ID]** op voor de AEM Assets-ontwerpomgeving die u met Commerce wilt verbinden.

- Geef de **[!UICONTROL Asset Selector IMS Client ID]** op. Zie [&#x200B; ImsAuthProps &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) in de *3&rbrace; documentatie van de Selecteur van AEM Assets.*

## De verbinding configureren

1. Krijg [&#x200B; AEM Assets Authoring Environment &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) project en milieu identiteitskaart

   1. Open de AEM Sites-console en selecteer **[!UICONTROL Assets]** .

   1. Kopieer en bewaar project en milieu IDs van URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Open vanuit Commerce Admin de AEM Assets Integration-configuratie.

   1. Ga naar **[!UICONTROL Store]** > Configuratie > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]** .

      ![&#x200B; de Integratie van AEM Assets laat de integratie &#x200B;](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"} toe

1. Voer de AEM Assets-omgeving **[!UICONTROL Program ID]** en **[!UICONTROL Environment ID]** in.

   Bewerk de configuratiewaarden door de selectie uit *[!UICONTROL Use system value]* te verwijderen.

1. Voer de **[!UICONTROL Asset Selector IMS Client ID]** in.

   De [&#x200B; identiteitskaart van de Cliënt IMS van de Selecteur van Activa &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) wordt vereist door [!UICONTROL Assets Selector], een eigenschap van AEM Assets die gebruikers toestaat om visuele activa direct in de productpagina&#39;s van Commerce in te bedden.

1. Selecteer [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) voor het verifiëren van aanvragen tussen Commerce en de service voor het afstemmen van elementen.

1. Stel **[!UICONTROL Integration enabled]** in op `Yes` als u wilt dat Commerce binnenkomende updates van AEM Assets accepteert.

   Nadat u de integratie hebt ingeschakeld, zijn aanvullende configuratieopties beschikbaar om criteria voor het afstemmen van elementen op te geven.

1. Bepaal de passende regel voor activasynchronisatie.

   1. Selecteer **[!UICONTROL Match by product SKU]** of **[!UICONTROL Custom match (Requires App Builder)]** .

   1. Voeg de [&#x200B; het meta-gegevensgebiedsnaam van AEM Assets &#x200B;](aem-assets-configure-aem.md#configure-metadata) toe die voor het product SKUs van Commerce op het **[!UICONTROL Match by product SKU attribute name]** gebied, `commerce:skus` bijvoorbeeld wordt bepaald.

1. Selecteer **[!UICONTROL Save Config]** om updates toe te passen en de synchronisatie van elementen te starten.

   De configuratieupdate activeert het eerste synchronisatieproces, zodat Commerce binnenkomende updates van AEM Assets kan accepteren. De tijd die nodig is voor synchronisatie is afhankelijk van het volume van elementen en specifieke configuraties. De integratie gebruikt geautomatiseerde processen om de tijd die nodig is voor synchronisatie te minimaliseren.

### De URL van het aangepaste domein configureren

Als een handelaar a [&#x200B; Naam van het Domein van de Douane &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/custom-domain-names/add-custom-domain-name){target=_blank} in hun dashboard van AEM plaatst, is het noodzakelijk om dit **Domein URL van de Douane** in Commerce toe te voegen, zodat kan de integratie van AEM Assets het gebruiken.

1. Navigeer naar **[!UICONTROL Store]** > Configuratie > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]** .

   ![&#x200B; de Integratie van AEM Assets laat de integratie &#x200B;](assets/aem-assets-view.png){width="600" zoomable="yes"} toe

1. Voeg **URL van het Domein van de Douane** aan het **[!UICONTROL Asset Custom Domain]** gebied toe.

1. Klik op **[!UICONTROL Save Config]** om updates toe te passen en de synchronisatie van elementen te starten.

## Volgende stap

[AEM Assets gebruiken met Commerce](aem-assets-manage.md)
