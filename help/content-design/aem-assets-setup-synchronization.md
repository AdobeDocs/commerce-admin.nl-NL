---
title: Elementsynchronisatie inschakelen
description: Leer hoe u uw Adobe Commerce- en Experience Manager Assets-projecten kunt verbinden om de synchronisatie van bedrijfsmiddelen tussen deze twee systemen mogelijk te maken.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Elementsynchronisatie inschakelen

Tijdens het enablement proces, registreert u huurdersidentiteitskaart voor het project gebruikend programma en milieu identiteitskaart voor uw AEM auteursmilieu. Deze id&#39;s identificeren het AEM Assets-project waarmee u verbinding maakt en bieden de referenties om communicatie tussen de Commerce- en AEM Assets-omgeving mogelijk te maken.

Nadat u het project met AEM elementen hebt geïdentificeerd, selecteert u de regel voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

- **[!UICONTROL Match by product SKU]** - Standaard regel die SKU in de activameta-gegevens met het [ product SKU van Commerce ](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) aanpast om ervoor te zorgen dat de activa met de correcte producten worden geassocieerd.

- **[!UICONTROL Custom match]** - Het stemmen regel voor complexere scenario&#39;s of specifieke bedrijfsvereisten die aangepaste passende logica vereisen. Voor het implementeren van aangepaste overeenkomsten moet in Adobe Developer App Builder aangepaste code worden ontwikkeld om te bepalen hoe elementen op producten worden afgestemd. Binnenkort komen er meer details...

Voor aanvankelijke onboarding, gebruik het gebrek *Gelijke door product sku* regel.

## Vereisten

- [Experience Manager Assets configureren AEM Commerce-middelen beheren](#aem-assets-configure-aem)
- [ installeer en vorm de Integratie van AEM Assets voor Commerce ](#aem-assets-configure-commerce.md) om de uitbreiding toe te voegen en de vereiste geloofsbrieven en de verbindingen te produceren om de uitbreiding te gebruiken.

## De verbinding configureren

1. Krijg [ AEM Assets Authoring Environment ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) project en milieu identiteitskaart

   1. Open de AEM Sites-console en selecteer **[!UICONTROL Assets]** .

   1. Kopieer en bewaar project en milieu IDs van URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Open vanuit Commerce Admin de AEM Assets Integration-configuratie.

   1. Ga naar **[!UICONTROL Store]** > Configuratie > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]** .

      ![ de Integratie van AEM Assets laat de integratie ](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"} toe

1. Voer de AEM Assets-omgeving **[!UICONTROL Program ID]** en **[!UICONTROL Environment ID]** in.

1. Ga ** [!UICONTROL Asset Selector IMS Client ID] in.

   [ identiteitskaart IMS ](../getting-started/adobe-ims-config.md) staat u toe om AEM Assets met de Bouwer van de Pagina te integreren.

1. Selecteer [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** voor het verifiëren van aanvragen tussen Commerce en de service voor het afstemmen van elementen.

1. Commerce toestaan binnenkomende updates van AEM Assets te accepteren door **[!UICONTROL Integration enabled]** in te stellen op `Yes` .

   Na het toelaten van de integratie, vorm de activa passende regel.

   ![ de uitgezochte regel van de de activagelijke van AEM Assets integratie ](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Bepaal de passende regel voor activasynchronisatie.

   1. Selecteer **[!UICONTROL Match by product SKU]** .

   1. Voeg de [ het meta-gegevensgebiedsnaam van AEM Assets ](aem-assets-configure-aem.md#configure-metadata) toe die voor het product SKUs van Commerce op het **[!UICONTROL Match by product SKU attribute name]** gebied, `commerce:skus` bijvoorbeeld wordt bepaald.

   ![ de uitgezochte regel van de de activagelijke van AEM Assets integratie ](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Selecteer **[!UICONTROL Save Config]** om updates toe te passen en de synchronisatie van middelen te starten
