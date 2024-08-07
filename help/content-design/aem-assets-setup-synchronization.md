---
title: Elementsynchronisatie inschakelen
description: Leer hoe u uw Adobe Commerce- en Experience Manager Assets-projecten kunt verbinden om de synchronisatie van bedrijfsmiddelen tussen deze twee systemen mogelijk te maken.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Elementsynchronisatie inschakelen

>[!BEGINSHADEBOX]

**Eerste vereisten**

- [Experience Manager Assets configureren AEM Commerce-middelen beheren](#aem-assets-configure-aem)
- [ installeer en vorm de Integratie van AEM Assets voor Commerce ](#aem-assets-configure-commerce.md) om de uitbreiding toe te voegen en de vereiste geloofsbrieven en de verbindingen te produceren om de uitbreiding te gebruiken.

>[!ENDSHADEBOX]

Tijdens dit enablement proces, registreert u uw huurdersidentiteitskaart door programma en milieu identiteitskaart voor uw AEM auteursmilieu te verstrekken. Deze id&#39;s identificeren het AEM Assets-project waarmee u verbinding maakt en bieden de referenties om communicatie en workflows tussen Commerce en AEM Assets mogelijk te maken.

Nadat u het project met AEM elementen hebt geïdentificeerd, selecteert u de regel die u wilt gebruiken voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

De integratie van AEM Assets voor Commerce ondersteunt twee regels voor het synchroniseren van elementen tussen Adobe Commerce en AEM Assets.

- **Gelijke door product SKU** - dit is de standaard passende regel die activa aanpast die op de Bewaren het Houden Eenheid (SKU) van het product worden gebaseerd. De SKU is een uniek herkenningsteken voor elk product. Deze regel past SKU in de elementenmeta-gegevens met het product SKU van Commerce aan om ervoor te zorgen dat de activa met de correcte producten worden geassocieerd.

- **de gelijke van de Douane** - Deze passende regel is voor complexere scenario&#39;s of specifieke bedrijfsvereisten die douane passende logica vereisen. Als u deze regel wilt gebruiken, moet in Adobe Developer App Builder aangepaste code zijn geïmplementeerd die definieert hoe elementen overeenkomen met producten. Binnenkort komen er meer details...

Gebruik de standaard `Match by product sku` -regel voor de eerste keer dat de computer wordt opgenomen. Indien nodig, kunt u de passende regel later veranderen.

## Integratie inschakelen

1. Krijg project en milieu identiteitskaart voor uw [ het Authoring Milieu van AEM Assets ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Open de AEM Sites-console en selecteer **[!UICONTROL Assets]** .

   1. Kopieer en bewaar project en milieu IDs van URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Open vanuit Commerce Admin de AEM Assets Integration-configuratie.

   1. Selecteer **[!UICONTROL Store]** > Configuratie > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]** .

   1. Vouw **[!UICONTROL Experience Manager Assets integration]** uit.

      ![ de Integratie van AEM Assets laat de integratie ](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"} toe

1. Identificeer het Experience Manager Assets-project waarmee u verbinding wilt maken door de waarden **[!UICONTROL Program ID]** en **[!UICONTROL Environment ID]** in te voeren.

1. U kunt de OAUTH-referenties toevoegen om API-aanvragen tussen Adobe Commerce en de ARES-service te verifiëren door de **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** te selecteren, bijvoorbeeld `Assets integration` .

1. Commerce toestaan binnenkomende updates van AEM Assets te accepteren door **[!UICONTROL Enable integration]** in te stellen op `Yes` .

   Na het toelaten van de integratie, kunt u de activa passende regel vormen.

   ![ de uitgezochte regel van de de activagelijke van AEM Assets integratie ](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Bepaal de passende regel voor activasynchronisatie.

   1. Selecteer **[!UICONTROL Match by product SKU]** .

   1. Voeg de [ het meta-gegevensgebiedsnaam van AEM Assets ](aem-assets-configure-aem.md#configure-metadata) toe die voor het product SKUs van Commerce op het **[!UICONTROL Match by product SKU attribute name]** gebied, `commerce:skus` bijvoorbeeld wordt bepaald.

1. Pas de configuratie toe en start het synchronisatieproces door **[!UICONTROL Save Config]** te selecteren.
