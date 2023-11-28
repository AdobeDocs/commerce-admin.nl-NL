---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL General] &gt; [!UICONTROL Content Management] pagina van de Commerce Admin.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG-opties](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Winkelweergave | Bepaalt als de redacteur voor de opslag wordt toegelaten. Opties: Ingeschakeld door Standaard/Uitgeschakeld door Standaard/Volledig uitgeschakeld |
| [!UICONTROL WYSIWYG Editor] | Website | Bepaalt de versie van de redacteur TinyMCE die voor de redacteur WYSIWYG wordt gebruikt. Opties: <br/>**`TinyMCE 5`**- (Gebrek) gebruikt TinyMCE versie 5 als standaardredacteur WYSIWYG.<br><br>_** Opmerking:**_Een update van de TinyMCE 5.10-bibliotheek in Adobe Commerce en Magento Open Source 2.4.5 verhelpt een kwetsbaarheid die willekeurige JavaScript-uitvoering toestaat bij het bijwerken van een afbeelding of koppeling met bepaalde typen URL&#39;s. TinyMCE 3 is afgekeurd in de release 2.4.0 en verwijderd uit de release 2.4.3. TinyMCE 4 is verwijderd uit de release 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Algemeen | Hiermee wordt bepaald of [statische URL&#39;s](../../content-design/catalog-urls-dynamic-media.md) worden gebruikt voor media inhoud die van de redacteur WYSIWYG van verwijzingen wordt voorzien. De instelling is van toepassing op alle plaatsen waar de WYSIWYG-editor beschikbaar is, inclusief producten, categorieën, pagina&#39;s en blokken. Opties: <br/>**`Yes`**- Gebruikt statische URLs voor media inhoud die met de redacteur WYSIWYG wordt opgenomen. Statische URL&#39;s zijn absoluut en onderbreken als de [basis-URL](../../stores-purchase/store-urls.md) van de winkel wijzigen.<br/>**`No`** (Standaard) - Gebruikt dynamische URL&#39;s voor media-inhoud die wordt ingevoegd met de WYSIWYG-editor, op basis van de  `{{media url="..."}}` richtlijn. Dynamische URL&#39;s zijn relatief en worden niet afgebroken als de basis-URL van de winkel verandert. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS-paginahiërarchie](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Algemeen | Hiermee activeert u het gebruik van paginahiërarchie voor inhoudspagina&#39;s. Opties: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Algemeen | Hiermee kunt u metagegevens koppelen aan pagina&#39;s in de hiërarchie. Opties: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Algemeen | Bepaalt de standaardmenustijl. Opties: `Content` / `Left Column` / `Right Column` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Content Tools]

![Geavanceerde gereedschappen voor inhoud](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Algemeen | Hiermee wordt bepaald of de [!DNL Page Builder] er zijn geavanceerde inhoudsgereedschappen beschikbaar . Opties: <br/>**`Yes`**- de [!DNL Page Builder] wordt weergegeven in de sectie Inhoud van pagina&#39;s, blokken, producten en categorieën.<br/>**`No`** - De standaard CMS-bewerkingsgereedschappen worden weergegeven in het dialoogvenster _[!UICONTROL Content]_sectie van pagina&#39;s, blokken, producten, en categorieën. |
| [!UICONTROL Enable Page Builder Content Preview] | Algemeen | Hiermee wordt bepaald of de [!DNL Page Builder] voorvertoningen van inhoud zijn ingeschakeld voor producten en categorieën. Opties: `Yes` / `No` <br/>**_Opmerking:_**Deze is ingesteld op `Yes` standaard, maar als u de voorvertoning uitschakelt, kunnen er prestatieproblemen optreden als gevolg van het laden van voorvertoningen in een product- of categorieformulier. |
| [!UICONTROL Google Maps API Key] | Algemeen | De [!DNL Google Maps] API-sleutel uit uw Google-account. |
| [!UICONTROL Test Key] |  | Hiermee valideert u de [!DNL Google Maps] API-sleutel. |
| [!UICONTROL Google Maps Style] | Algemeen | Plak de [!DNL Google Maps] stijl JSON-code hier om het uiterlijk van het inhoudstype Kaart te wijzigen. |
| [!UICONTROL Default Column Grid Size] | Algemeen | Bepaalt het standaardaantal kolommen in [!DNL Page Builder] raster. |
| [!UICONTROL Maximum Column Grid Size] | Algemeen | Hiermee bepaalt u het maximumaantal kolommen in het dialoogvenster [!DNL Page Builder] raster. |

{:style=&quot;table-layout:auto&quot;}

>[!TIP]
>
>De Bouwer van de pagina maakt het gemakkelijk om inhoud-rijke pagina&#39;s met douanelay-outs tot stand te brengen die uw visueel verhaal verbeteren en klantenbetrokkenheid en loyaliteit te drijven. Deze functies zijn ontworpen om de kwaliteit te verbeteren en de tijd en kosten voor het maken van aangepaste pagina&#39;s te verminderen. Raadpleeg voor meer informatie over deze functies en hoe u deze kunt gebruiken om aantrekkelijke inhoud voor uw Adobe Commerce- of Magento Open Source-winkel te maken de [_Gebruikershandleiding voor Page Builder_](../../page-builder/guide-overview.md).

{:style=&quot;table-layout:auto&quot;}
