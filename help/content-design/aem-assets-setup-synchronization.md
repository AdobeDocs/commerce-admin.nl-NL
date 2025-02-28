---
title: Elementsynchronisatie inschakelen
description: Leer hoe u uw Adobe Commerce- en Experience Manager Assets-projecten kunt verbinden om de synchronisatie van bedrijfsmiddelen tussen deze twee systemen mogelijk te maken.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: d8e255259e4a8b87c63a4d1c013b4c1feb2b29cb
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Elementsynchronisatie inschakelen

Schakel de synchronisatie van elementen in door de Commerce-omgevingsconfiguratie bij te werken en Commerce te verbinden met de AEM Assets-instantie. Dankzij deze integratie kunnen de elementen tussen Commerce en AEM Assets worden gesynchroniseerd, zodat productafbeeldingen en andere elementen altijd up-to-date zijn.

Nadat u het AEM-middelenproject hebt geïdentificeerd, selecteert u de regel voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

- **[!UICONTROL Match by product SKU]** - Standaard regel die SKU in de activameta-gegevens met het [ product SKU van Commerce ](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku) aanpast om ervoor te zorgen dat de activa met de correcte producten worden geassocieerd.

- **[!UICONTROL Custom match]** - Het stemmen regel voor complexere scenario&#39;s of specifieke bedrijfsvereisten die aangepaste passende logica vereisen. Voor het implementeren van aangepaste overeenkomsten moet in Adobe Developer App Builder aangepaste code worden ontwikkeld om te bepalen hoe elementen op producten worden afgestemd. Binnenkort komen er meer details...

Voor aanvankelijke onboarding, gebruik het gebrek *Gelijke door product sku* regel.

## Vereisten

- [AEM Assets configureren voor het beheer van Commerce-middelen](aem-assets-configure-aem.md)

- [ installeer en vorm de Integratie van AEM Assets voor Commerce ](aem-assets-configure-commerce.md) om de uitbreiding toe te voegen en de vereiste geloofsbrieven en de verbindingen te produceren om de uitbreiding te gebruiken.

- Creeer een steunkaartje aan verzoekenablement voor de Integratie van AEM Assets. U moet de eigenschappen **[!UICONTROL Program ID]** , **[!UICONTROL Environment ID]** en **[!UICONTROL IMS Org ID]** opgeven voor de AEM Assets-ontwerpomgeving die u wilt verbinden met Commerce.

  >[!TIP]
  >
  > (Optioneel) Geef de **[!UICONTROL Asset Selector IMS Client ID]** op, indien beschikbaar. Zie [ ImsAuthProps ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) in de *3} documentatie van de Selecteur van AEM Assets.*

## De verbinding configureren

1. Krijg [ AEM Assets Authoring Environment ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) project en milieu identiteitskaart

   1. Open de AEM Sites-console en selecteer **[!UICONTROL Assets]** .

   1. Kopieer en bewaar project en milieu IDs van URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Open vanuit Commerce Admin de AEM Assets Integration-configuratie.

   1. Ga naar **[!UICONTROL Store]** > Configuratie > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]** .

      ![ de Integratie van AEM Assets laat de integratie ](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"} toe

1. Voer de AEM Assets-omgeving **[!UICONTROL Program ID]** en **[!UICONTROL Environment ID]** in.

   Bewerk de configuratiewaarden door de selectie uit *[!UICONTROL Use system value]* te verwijderen.

1. Voer de **[!UICONTROL Asset Selector IMS Client ID]** in, indien beschikbaar.

   De [ identiteitskaart van de Cliënt IMS van de Selecteur van Activa ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) wordt vereist door [!UICONTROL Assets Selector], een eigenschap van AEM Assets die gebruikers toestaat om visuele activa direct in de productpagina&#39;s van Commerce in te bedden.

1. Selecteer [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) voor het verifiëren van aanvragen tussen Commerce en de service voor het afstemmen van elementen.

1. Stel **[!UICONTROL Integration enabled]** in op `Yes` als u wilt dat Commerce binnenkomende updates van AEM Assets accepteert.

   Nadat u de integratie hebt ingeschakeld, zijn aanvullende configuratieopties beschikbaar om criteria voor het afstemmen van elementen op te geven.

1. Bepaal de passende regel voor activasynchronisatie.

   1. Selecteer **[!UICONTROL Match by product SKU]** of **[!UICONTROL Custom match (Requires App Builder)]** .

   1. Voeg de [ het meta-gegevensgebiedsnaam van AEM Assets ](aem-assets-configure-aem.md#configure-metadata) toe die voor het product SKUs van Commerce op het **[!UICONTROL Match by product SKU attribute name]** gebied, `commerce:skus` bijvoorbeeld wordt bepaald.

1. Selecteer **[!UICONTROL Save Config]** om updates toe te passen en de synchronisatie van elementen te starten.

   De configuratieupdate activeert het initiële synchronisatieproces, waardoor Commerce binnenkomende updates van AEM Assets kan accepteren. De tijd die nodig is voor synchronisatie is afhankelijk van het volume van de middelen en specifieke configuraties. De integratie gebruikt geautomatiseerde processen om de tijd die nodig is voor synchronisatie te minimaliseren.

## Volgende stap

[AEM Assets gebruiken met Commerce](aem-assets-manage.md)
