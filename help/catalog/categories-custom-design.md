---
title: Categorieën - ontwerpinstellingen
description: Leer hoe u de [!UICONTROL Design] -instellingen gebruikt om de vormgeving van een categorie, alle bijbehorende productpagina's en de pagina-indeling te definiëren.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Categorieën - ontwerpinstellingen

In de sectie _[!UICONTROL Design]_&#x200B;hebt u controle over de vormgeving van een categorie, alle bijbehorende productpagina&#39;s en de paginalay-out. Je kunt een rubriekpagina en de bijbehorende producten aanpassen voor een speciale actie of om een onderscheid te maken tussen de rubrieken. U kunt bijvoorbeeld een speciaal ontwerp voor een merk of een speciale lijn met producten ontwikkelen of een update voor een bepaalde periode toepassen.

![&#x200B; montages van het Ontwerp voor een categorie &#x200B;](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wanneer het zelfde product aan verscheidene categorieën met verschillende ontwerpmontages voor elke categorie wordt toegewezen, wordt het geadviseerd om **Weg van de Categorieën van het Gebruik voor Product URLs** = `Yes` in de [&#x200B; configuratieopties van de Optimalisering van de Motor van het Onderzoek &#x200B;](../configuration-reference/catalog/catalog.md#search-engine-optimization) te plaatsen. Om tot dit het plaatsen toegang te hebben, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, breid **[!UICONTROL Catalog]**&#x200B;uit en kies **Catalogus**&#x200B;onderaan in het linkerpaneel, en breid dan de **sectie van de Optimalisering van de Motor van het Onderzoek**&#x200B;op de pagina uit.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Hiermee kan de huidige categorie de ontwerpinstellingen overnemen van de bovenliggende categorie. Indien gebruikt, worden alle andere gebieden in de sectie van het Ontwerp niet beschikbaar. Opties: `Yes` / ` No` |
| [!UICONTROL Theme] | Hiermee past u een aangepast thema toe op de categorie. |
| [!UICONTROL Layout] | Hiermee past u een andere indeling toe op de categoriepagina. Opties: <br/>**[!UICONTROL No layout updates]**- layout-updates zijn standaard niet beschikbaar voor categoriepagina&#39;s.<br/>**[!UICONTROL Empty]** - Gebruik deze optie om uw eigen pagina-indeling te definiëren. (Hiervoor is inzicht in XML vereist.) <br/>**[!UICONTROL 1 column]**- Past een lay-out van één kolom op de categoriepagina toe.<br/>**[!UICONTROL 2 columns with left bar]** - Past een lay-out van twee kolommen met een linkerzijbalk op de categoriepagina toe. <br/>**[!UICONTROL 2 columns with right bar]**- Hiermee past u een lay-out met twee kolommen en een rechterzijbalk toe op de categoriepagina.<br/>**[!UICONTROL 3 columns]** - Hiermee past u een indeling met drie kolommen toe op de categoriepagina.<br/>**[!UICONTROL Page -- Full Width]**- (Vereist [&#x200B; Bouwer van de Pagina &#x200B;](../page-builder/introduction.md)) past de full-width lay-out voor CMS pagina&#39;s op de categoriepagina toe.<br/>**[!UICONTROL Category -- Full Width]** - (Vereist de Bouwer van de Pagina) past de lay-out van volledige breedte voor categoriepagina&#39;s op de categoriepagina toe. <br/>**[!UICONTROL Product -- Full Width]**- (Vereist de Bouwer van de Pagina) past de lay-out van volledige breedte voor productpagina&#39;s op de categoriepagina toe. |
| [!UICONTROL Custom Layout Update] | Hier worden de beschikbare updatebestanden voor de aangepaste indeling op de server weergegeven. Kies de aangepaste layout-update die u op de categorie wilt toepassen. |
| [!UICONTROL Apply Design to Products] | Als deze optie is geselecteerd, worden de aangepaste instellingen toegepast op alle producten in de categorie. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

De sectie _[!UICONTROL Scheduled Design Update]_&#x200B;bepaalt het datumbereik wanneer een aangepast ontwerp wordt toegepast op categoriepagina&#39;s.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Hiermee bepaalt u het datumbereik wanneer een aangepaste indeling wordt toegepast op de categorie. |

![&#x200B; Geplande Update van het Ontwerp &#x200B;](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
