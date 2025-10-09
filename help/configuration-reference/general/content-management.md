---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL General] &gt; [!UICONTROL Content Management] van Commerce Admin.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![&#x200B; de Opties van WYSIWYG &#x200B;](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Winkelweergave | Bepaalt als de redacteur voor de opslag wordt toegelaten. Opties: Ingeschakeld door Standaard/Uitgeschakeld door Standaard/Volledig uitgeschakeld |
| [!UICONTROL WYSIWYG Editor] | Website | Bepaalt de versie van de redacteur TinyMCE die voor de redacteur van WYSIWYG wordt gebruikt. Opties: <br/>**`TinyMCE 5`**- (Standaard) gebruikt TinyMCE versie 5 als de standaard WYSIWYG-editor.<br><br>_ **&#x200B; Nota:**&#x200B;_Een update aan TinyMCE 5.10 bibliotheek in Adobe Commerce en Magento Open Source 2.4.5 verhelpt een kwetsbaarheid die willekeurige uitvoering van JavaScript wanneer het bijwerken van een beeld of verbinding gebruikend sommige types van URLs toeliet. TinyMCE 3 is afgekeurd in de release 2.4.0 en verwijderd uit de release 2.4.3. TinyMCE 4 is verwijderd uit de release 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Algemeen | Bepaalt als [&#x200B; statische URLs &#x200B;](../../content-design/catalog-urls-dynamic-media.md) voor media inhoud wordt gebruikt die van de redacteur van WYSIWYG van verwijzingen wordt voorzien. De instelling is van toepassing op alle plaatsen waar de WYSIWYG-editor beschikbaar is, inclusief producten, categorieën, pagina&#39;s en blokken. Opties: <br/>**`Yes`**- gebruikt statische URL&#39;s voor media-inhoud die wordt ingevoegd met de WYSIWYG-editor. Statische URLs is absolute en onderbreking als [&#x200B; basis URL &#x200B;](../../stores-purchase/store-urls.md) van de opslag verandert.<br/>**`No`** (Standaard) - Gebruikt dynamische URL&#39;s voor media-inhoud die wordt ingevoegd met de WYSIWYG-editor, op basis van de instructie `{{media url="..."}}` . Dynamische URL&#39;s zijn relatief en worden niet afgebroken als de basis-URL van de winkel verandert. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![&#x200B; de Hiërarchie van de Pagina van CMS &#x200B;](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Algemeen | Hiermee activeert u het gebruik van paginahiërarchie voor inhoudspagina&#39;s. Opties: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Algemeen | Hiermee kunt u metagegevens koppelen aan pagina&#39;s in de hiërarchie. Opties: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Algemeen | Bepaalt de standaardmenustijl. Opties: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![&#x200B; Geavanceerde Hulpmiddelen van de Inhoud &#x200B;](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/en/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Algemeen | Hiermee bepaalt u of de geavanceerde inhoudsgereedschappen van [!DNL Page Builder] beschikbaar zijn. Opties: <br/>**`Yes`**- De werkruimte [!DNL Page Builder] wordt weergegeven in de sectie Inhoud van pagina&#39;s, blokken, producten en categorieën.<br/>**`No`** - De standaard CMS-bewerkingsgereedschappen worden weergegeven in de _[!UICONTROL Content]_-sectie van pagina&#39;s, blokken, producten en categorieën. |
| [!UICONTROL Enable Page Builder Content Preview] | Algemeen | Hiermee wordt bepaald of de voorvertoningen van de [!DNL Page Builder] -inhoud zijn ingeschakeld voor producten en categorieën. Opties: `Yes` / `No` <br/>**_Note:_** Deze is standaard ingesteld op `Yes` , maar als u de voorvertoning uitschakelt, kunnen er prestatieproblemen optreden als gevolg van het laden van voorvertoningen in een product- of categorieformulier. |
| [!UICONTROL Google Maps API Key] | Algemeen | De [!DNL Google Maps] API-sleutel van uw Google-account. |
| [!UICONTROL Test Key] |  | Hiermee wordt de API-sleutel van [!DNL Google Maps] gevalideerd. |
| [!UICONTROL Google Maps Style] | Algemeen | Plak de JSON-code van de [!DNL Google Maps] -stijl hier om de vormgeving van het inhoudstype Kaart te wijzigen. |
| [!UICONTROL Default Column Grid Size] | Algemeen | Bepaalt het standaardaantal kolommen in het [!DNL Page Builder] -raster. |
| [!UICONTROL Maximum Column Grid Size] | Algemeen | Bepaalt het maximumaantal kolommen in het [!DNL Page Builder] raster. |

{style="table-layout:auto"}

>[!TIP]
>
>De Bouwer van de pagina maakt het gemakkelijk om inhoud-rijke pagina&#39;s met douanelay-outs tot stand te brengen die uw visueel verhaal verbeteren en klantenbetrokkenheid en loyaliteit te drijven. Deze functies zijn ontworpen om de kwaliteit te verbeteren en de tijd en kosten voor het maken van aangepaste pagina&#39;s te verminderen. Voor meer informatie over deze eigenschappen en hoe u hen kunt gebruiken om het in dienst nemen van inhoud voor uw opslag van Adobe Commerce of Magento Open Source tot stand te brengen, zie de [_Gids van de Gebruiker van de Bouwer van de Pagina_](../../page-builder/guide-overview.md).
