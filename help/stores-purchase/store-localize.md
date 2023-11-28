---
title: Winkellokalisatie
description: Leer hoe u een winkel- of winkelweergave lokaliseert.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Winkellokalisatie

Het merendeel van de tekst die op pagina&#39;s in de winkel hard lijkt te zijn gecodeerd, kan direct worden gewijzigd in een andere taal door de landinstelling van de weergave te wijzigen. Als u de landinstelling wijzigt, wordt de tekst woord voor woord niet vertaald, maar wordt gewoon verwezen naar een andere vertaaltabel die de interfacetekst bevat die in de hele winkel wordt gebruikt. De tekst die kan worden gewijzigd, bevat navigatitels, labels, knoppen en koppelingen, zoals _Mijn hart_ en _Mijn account_. U kunt ook de opdracht [Inline-omzetting](../configuration-reference/advanced/developer.md) gebruiken om tekst in de interface aan te raken.

Taalpakketten vindt u onder [Vertaling en lokalisatie][1]{:target=&quot;_blank&quot;} bij Commerce Marketplace. Er worden voortdurend nieuwe extensies toegevoegd aan Marketplace. Ga daarom vaak terug.

## Stap 1: Een taalpakket installeren

Volg de standaardinstructies voor het installeren van de taalpakketextensie. Voor gedetailleerde informatie over het installeren van een extensie raadpleegt u [Algemene CLI-installatie][2] in de _Handleiding voor extensies_.

## Stap 2: Een winkelweergave voor de taal maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klik op **[!UICONTROL Create Store View]**.

1. Stel de opties voor de nieuwe winkelweergave in:

   - **[!UICONTROL Store]** — Kies de winkel die het bovenliggende item van de weergave is.

   - **[!UICONTROL Name]** — Voer een naam in voor de winkelweergave. Bijvoorbeeld: Portugees.

     In de koptekst van de winkel wordt de naam weergegeven in het dialoogvenster _taalkiezer_.

   - **[!UICONTROL Code]** — Voer een code in kleine letters in om de weergave te identificeren. Bijvoorbeeld: `portuguese`.

   - **[!UICONTROL Status]** — Als u de weergave wilt activeren, stelt u in op `Enabled`.

   - **[!UICONTROL Sort Order]** — (Optioneel) Voer een getal in om de volgorde te bepalen waarin deze weergave bij andere weergaven wordt weergegeven.

1. Klik op **[!UICONTROL Save Store View]**.

## Stap 3: Wijzig de landinstelling van de winkelweergave

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In de linkerbovenhoek, plaats **[!UICONTROL Store View]** op de specifieke weergave waarop de configuratie van toepassing is.

1. Wanneer ertoe aangezet om werkingsgebiedomschakeling te bevestigen, klik **[!UICONTROL OK]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Locale Options]** sectie.

1. Wis de **[!UICONTROL Use Website]** selectievakje en set **[!UICONTROL Locale]** aan de taal die u aan de mening wilt toewijzen.

   Als er verschillende variaties van de beschikbare taal zijn, zorg ervoor om één voor het specifieke gebied of dialect te kiezen.

1. Klik op **[!UICONTROL Save Config]**.

   Nadat u de taal van de landinstelling hebt gewijzigd, blijft de resterende inhoud die u hebt gemaakt behouden, inclusief productnamen en beschrijvingen, categorieën, [CMS](../content-design/page-translate.md) pagina&#39;s en blokken moeten voor elke winkelweergave afzonderlijk worden vertaald.

## Producten lokaliseren

Als uw winkel meerdere weergaven in verschillende talen heeft, zijn in elke winkelweergave dezelfde producten beschikbaar. U kunt dezelfde basisproductinformatie gebruiken, zoals SKU, prijs en inventarisniveau, ongeacht de taal. Vertaal vervolgens voor elke taal alleen de productnaam, beschrijvingsvelden en metagegevens.

### Stap 1: Productvelden vertalen

1. Op de _Beheerder_ zijbalk, ga naar  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek in het raster het product dat u wilt vertalen en open het in de bewerkingsmodus.

1. In de linkerbovenhoek, plaats **[!UICONTROL Store View]** naar de weergave voor de vertaling en klik op **[!UICONTROL OK]** wanneer wordt gevraagd om te bevestigen.

1. Ga als volgt te werk voor elk veld dat moet worden bewerkt:

   - Hef de selectie van **[!UICONTROL Use Default Value]** Schakel het selectievakje rechts van het veld in.

   - Plak of typ de vertaalde tekst in het veld.

   Zorg ervoor dat u alle tekstvelden vertaalt, inclusief [image](../catalog/catalog-images-video.md) labels en Alt-tekst, [Optimalisatie zoekmachine](../catalog/product-search-engine-optimization.md) velden en alle [Aangepaste opties](../catalog/settings-advanced-custom-options.md) informatie.

1. Klik op **[!UICONTROL Save]**.

### Stap 2: Veldlabels vertalen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Zoek in de lijst naar het kenmerk dat moet worden vertaald en open in de bewerkingsmodus.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Manage Labels]**.

1. In de _[!UICONTROL Manage Titles]_een vertaald label voor elke winkelweergave invoeren.

   ![Vertaalde labels invoeren](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Attribute]**.

### Stap 3: Alle categorieën vertalen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **Categorieën**.

1. In de linkerbovenhoek, plaats **[!UICONTROL Store View]** naar de weergave voor de vertaling en klik op **[!UICONTROL OK]** wanneer wordt gevraagd om te bevestigen.

1. Zoek in de boomstructuur naar de categorie die u wilt vertalen en open deze in de bewerkingsmodus.

1. Voor _Basisinformatie_, vertalen **[!UICONTROL Category Name]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Content]_sectie en transleren **[!UICONTROL Description]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization Settings]** en vertaal de volgende velden:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Onder de _[!UICONTROL Search Engine Optimization Settings]_, voert u de volgende handelingen uit om de **[!UICONTROL URL Key]**:

   - Wis de **[!UICONTROL Use Default Value]** Schakel het selectievakje rechts van het veld in.

   - Voer de vertaalde tekst in.

   - Zorg ervoor dat de **[!UICONTROL Create Permanent Redirect for old URL]** selectievakje is ingeschakeld.

   ![De URL-sleutel vertalen](./assets/category-translate-url-key.png)

1. Klik op **[!UICONTROL Save Category]**.

1. Herhaal dit proces voor alle categorieën die in de winkel worden gebruikt.

### Stap 4: Opties voor het vertalen van productkenmerken en -kenmerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Selecteer het kenmerk dat moet worden vertaald.

1. Kies **[!UICONTROL Manage Labels]** aan de linkerkant en stel de **[!UICONTROL Managed Titles]** opties voor het definiëren van de vertalingen van de kenmerktitel.

1. Kies **[!UICONTROL Properties]** aan de linkerkant en voer de vertaalde kenmerkopties in het dialoogvenster **[!UICONTROL Manage Options]** sectie.

   ![Opties beheren](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
