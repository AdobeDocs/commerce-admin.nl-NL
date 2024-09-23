---
title: Experience Manager Assets configureren
description: Voeg de metagegevens voor elementen toe die nodig zijn om de AEM Assets Integration voor Commerce in te schakelen voor het synchroniseren van elementen tussen Adobe Commerce- en Experience Manager Assets-projecten.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 8a150c79c2e15ce5bd2cb2037f94c94f90b7a1df
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Experience Manager Assets configureren

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Bereid de AEM as a Cloud Service-omgeving voor om Commerce-middelen te beheren door de omgevingsconfiguratie bij te werken en de Assets-metagegevens te configureren voor het identificeren en beheren van Commerce-elementen.

De integratie vereist het toevoegen van een douane `Commerce` namespace en extra [ profielmeta-gegevens ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles) en [ schemameta-gegevens ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas).

Adobe verstrekt een AEM projectmalplaatje om namespace en de middelen van het meta-gegevensschema aan de as a Cloud Service het omgevingsconfiguratie van AEM Assets toe te voegen. De sjabloon voegt toe:

- A [ douanenamespace ](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` om op Commerce betrekking hebbende eigenschappen te identificeren.

- Een aangepast metagegevenstype `commerce:isCommerce` met het label `Does it exist in Commerce?` om Commerce-elementen die aan een Adobe Commerce-project zijn gekoppeld, van tags te voorzien.

- Een aangepast metagegevenstype `commerce:productmetadata` en een overeenkomende UI-component om een eigenschap *[!UICONTROL Product Data]* toe te voegen. Productgegevens bevatten de eigenschappen van metagegevens om een Commerce-element te koppelen aan product-SKU&#39;s en om afbeeldings- `role` en `position` -kenmerken voor het element op te geven.

  ![ Controle UI van de Gegevens van het Product van de Douane ](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Een metagegevensschema met een Commerce-tabblad dat de velden `Does it exist in Adobe Commerce?` en `Product Data` bevat voor het labelen van Commerce-elementen. Het formulier bevat ook opties voor het weergeven of verbergen van de velden `roles` en `order` (positie) in de gebruikersinterface van AEM Assets.

  ![ Commerce lusje voor de vorm van het de meta-gegevensschema van AEM Assets ](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- A [ steekproef geëtiketteerde en goedgekeurde activa van Commerce ](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg` om aanvankelijke activasynchronisatie te steunen. Alleen goedgekeurde Commerce-middelen kunnen van AEM Assets naar Adobe Commerce worden gesynchroniseerd.

Voor extra informatie over het Commerce-Assets AEM project, zie [ Leesmij ](https://github.com/ankumalh/assets-commerce).

## De AEM Assets-omgevingsconfiguratie aanpassen

>[!BEGINSHADEBOX]

**Eerste vereisten**

- [ Toegang tot het Programma van AEM Assets Cloud Manager en milieu&#39;s ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) met de rollen van de Manager van het Programma en van de Plaatsing.

- A [ lokale AEM ontwikkelomgeving ](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) en vertrouwdheid met het AEM lokale ontwikkelingsproces.

- Begrijp [ AEM projectstructuur ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) en hoe te om de pakketten van de douaneinhoud op te stellen gebruikend Cloud Manager.

>[!ENDSHADEBOX]

### Implementeer het Commerce-Assets AEM-project in de AEM Assets-ontwerpomgeving

1. Creëer vanuit de Cloud Manager productie- en staging-omgevingen voor uw AEM Assets-project, indien nodig.

1. Vorm een plaatsingspijpleiding, indien nodig.

1. Van GitHub, download de boilerplate code van het [ Commerce-Assets AEM project ](https://github.com/ankumalh/assets-commerce).

1. Van uw [ lokale AEM ontwikkelomgeving ](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview), installeer de douanecode in uw het milieuconfiguratie van AEM Assets als Geweven pakket, of door de code in de bestaande projectconfiguratie manueel te kopiëren.

1. Leg de wijzigingen vast en duw uw lokale ontwikkelingsvertakking naar de Cloud Manager git-opslagplaats.

1. Van Cloud Manager, [ stelt uw code op om het AEM milieu ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager) bij te werken.

## Een metagegevensprofiel configureren

Stel standaardwaarden in voor metagegevens van Commerce-elementen door een metagegevensprofiel te maken. Nadat u dit profiel hebt ingesteld, past u dit profiel toe op AEM mappen Middelen om deze standaardinstellingen automatisch te gebruiken. Deze optionele installatie helpt de verwerking van bedrijfsmiddelen te stroomlijnen door handmatige stappen te verminderen.

1. Ga in de Adobe Experience Manager-werkruimte naar de werkruimte voor het beheer van inhoud voor auteurs voor AEM Assets door op het Adobe Experience Manager-pictogram te klikken.

   ![ AEM Assets authoring ](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Open de Hulpmiddelen van de Beheerder door het hamerpictogram te selecteren.

   ![ AEM Admin van de Auteur beheert meta-gegevensprofielen ](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Open de pagina voor profielconfiguratie door op **[!UICONTROL Metadata Profiles]** te klikken.

1. **[!UICONTROL Create]** een metagegevensprofiel voor de Commerce-integratie.

   ![AEM Auteur Admin voegt metagegevensprofielen toe ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Voeg een tabblad toe voor Commerce-metagegevens.

   1. Klik links op **[!UICONTROL Settings]** .

   1. Klik op **[!UICONTROL +]** in de tabsectie en geef vervolgens de **[!UICONTROL Tab Name]** , `Commerce` op.

1. Voeg het veld `Does it exist in Commerce?` toe aan het formulier en stel de standaardwaarde in op `yes` .

   ![ AEM Admin van de Auteur voegt meta-gegevensgebieden aan profiel toe ](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Sla de update op.

1. Pas het metagegevensprofiel `Commerce integration` toe op de map waarin Commerce-elementen zijn opgeslagen.

   1. Van de [!UICONTROL  Metadata Profiles] pagina, selecteer het de integratieprofiel van Commerce.

   1. Selecteer **[!UICONTROL Apply Metadata Profiles to Folder(s)]** in het menu Handeling.

   1. Selecteer de map met Commerce-elementen.

      Maak een Commerce-map als deze niet bestaat.

   1. Klik op **[!UICONTROL Apply]**.

>[!TIP]
>
>U kunt Commerce-elementen tijdens het uploaden naar de AEM Assets-omgeving automatisch synchroniseren door het metagegevensprofiel bij te werken en de standaardwaarde voor het veld _[!UICONTROL Review Status]_in te stellen op `Approved` . Het eigenschapstype voor het veld `Review Status` is `./jcr:content/metadata/dam:status` .


## Volgende stappen

Nadat u de AEM hebt bijgewerkt, stelt u Adobe Commerce in:

1. [De AEM Assets Integration voor Commerce installeren en configureren](aem-assets-configure-commerce.md)
2. [Middelensynchronisatie inschakelen om elementen over te brengen tussen uw Adobe Commerce-projectomgeving en de AEM Assets-projectomgeving](aem-assets-setup-synchronization.md)
