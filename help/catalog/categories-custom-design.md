---
title: Categorieën - ontwerpinstellingen
description: Meer informatie over het gebruik van de [!UICONTROL Design] instellingen om het uiterlijk van een categorie, alle bijbehorende productpagina's en de paginalay-out te definiëren.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Categorieën - ontwerpinstellingen

De _[!UICONTROL Design]_kunt u de vormgeving van een categorie, alle bijbehorende productpagina&#39;s en de pagina-indeling bepalen. Je kunt een rubriekpagina en de bijbehorende producten aanpassen voor een speciale actie of om een onderscheid te maken tussen de rubrieken. U kunt bijvoorbeeld een speciaal ontwerp voor een merk of een speciale lijn met producten ontwikkelen of een update voor een bepaalde periode toepassen.

![Ontwerpinstellingen voor een categorie](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Als hetzelfde product wordt toegewezen aan verschillende categorieën met verschillende ontwerpinstellingen voor elke categorie, wordt het aanbevolen **Categoriepad gebruiken voor product-URL&#39;s** = `Yes` in de [Configuratieopties voor optimalisatie zoekmachine](../configuration-reference/catalog/catalog.md#search-engine-optimization). Ga voor toegang tot deze instelling naar  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, uitbreiden **[!UICONTROL Catalog]**en kiest u **Catalogus**onder in het linkerdeelvenster en vouw vervolgens het **Optimalisatie zoekmachine**op de pagina.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Hiermee kan de huidige categorie de ontwerpinstellingen overnemen van de bovenliggende categorie. Indien gebruikt, worden alle andere gebieden in de sectie van het Ontwerp niet beschikbaar. Opties: `Yes` / ` No` |
| [!UICONTROL Theme] | Hiermee past u een aangepast thema toe op de categorie. |
| [!UICONTROL Layout] | Hiermee past u een andere indeling toe op de categoriepagina. Opties: <br/>**[!UICONTROL No layout updates]**- Standaard zijn indelingsupdates niet beschikbaar voor categoriepagina&#39;s.<br/>**[!UICONTROL Empty]** - Gebruik deze optie om uw eigen pagina-indeling te definiëren. (Hiervoor is inzicht in XML vereist.) <br/>**[!UICONTROL 1 column]**- Hiermee past u een indeling met één kolom toe op de categoriepagina.<br/>**[!UICONTROL 2 columns with left bar]** - Hiermee past u een lay-out met twee kolommen en een linkerzijbalk toe op de categoriepagina. <br/>**[!UICONTROL 2 columns with right bar]**- Hiermee past u een lay-out met twee kolommen en een rechterzijbalk toe op de categoriepagina.<br/>**[!UICONTROL 3 columns]** - Hiermee past u een indeling met drie kolommen toe op de categoriepagina.<br/>**[!UICONTROL Page -- Full Width]**- (Vereist [Page Builder](../page-builder/introduction.md)) Hiermee past u de volledige-breedtelay-out voor CMS-pagina&#39;s toe op de categoriepagina.<br/>**[!UICONTROL Category -- Full Width]** - (Vereist de Bouwer van de Pagina) past de volledige lay-out voor categoriepagina&#39;s op de categoriepagina toe. <br/>**[!UICONTROL Product -- Full Width]**- (Vereist de Bouwer van de Pagina) past de volledige lay-out voor productpagina&#39;s op de categoriepagina toe. |
| [!UICONTROL Custom Layout Update] | Hier worden de beschikbare updatebestanden voor de aangepaste indeling op de server weergegeven. Kies de aangepaste layout-update die u op de categorie wilt toepassen. |
| [!UICONTROL Apply Design to Products] | Als deze optie is geselecteerd, worden de aangepaste instellingen toegepast op alle producten in de categorie. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

De _[!UICONTROL Scheduled Design Update]_bepaalt het datumbereik wanneer een aangepast ontwerp wordt toegepast op categoriepagina&#39;s.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Hiermee bepaalt u het datumbereik wanneer een aangepaste indeling wordt toegepast op de categorie. |

![Geplande ontwerpupdate](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
