---
title: Winkellokalisatie
description: Leer hoe u een winkel- of winkelweergave lokaliseert.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# Winkellokalisatie

Het merendeel van de tekst die op pagina&#39;s in de winkel hard lijkt te zijn gecodeerd, kan direct worden gewijzigd in een andere taal door de landinstelling van de weergave te wijzigen. Als u de landinstelling wijzigt, wordt de tekst woord voor woord niet vertaald, maar wordt gewoon verwezen naar een andere vertaaltabel die de interfacetekst bevat die in de hele winkel wordt gebruikt. De tekst die kan worden veranderd omvat navigatietitels, etiketten, knopen, en verbindingen zoals _Mijn Kaart_ en _Mijn Rekening_. U kunt het [&#x200B; Inline Vertaling &#x200B;](../configuration-reference/advanced/developer.md) hulpmiddel ook gebruiken om tekst in de interface aan te raken.

De pakken van de taal kunnen onder [&#x200B; Vertalingen &amp; Localization &#x200B;](https://marketplace.magento.com/extensions/content-customizations/translations-localization.html){:target="_blank"} op Commerce Marketplace worden gevonden. Er worden voortdurend nieuwe extensies toegevoegd aan Marketplace. Ga daarom vaak terug.

## Stap 1: Een taalpakket installeren

Volg de standaardinstructies voor het installeren van de taalpakketextensie. Voor gedetailleerde informatie over het installeren van een uitbreiding, zie [&#x200B; Algemene installatie CLI &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) in de _Gids van Uitbreidingen_.

## Stap 2: Een winkelweergave voor de taal maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klik op **[!UICONTROL Create Store View]**.

1. Stel de opties voor de nieuwe winkelweergave in:

   - **[!UICONTROL Store]** — Kies de winkel die het bovenliggende item van de weergave is.

   - **[!UICONTROL Name]** — Voer een naam in voor de winkelweergave. Bijvoorbeeld: Portugees.

     In de kopbal van de opslag, verschijnt de naam in _taalkiezer_.

   - **[!UICONTROL Code]** — Voer een code in kleine letters in om de weergave te identificeren. Bijvoorbeeld: `portuguese` .

   - **[!UICONTROL Status]** — Als u de weergave wilt activeren, stelt u deze in op `Enabled` .

   - **[!UICONTROL Sort Order]** — (Optioneel) Voer een getal in om de volgorde te bepalen waarin deze weergave bij andere weergaven wordt weergegeven.

1. Klik op **[!UICONTROL Save Store View]** als de bewerking is voltooid.

## Stap 3: Wijzig de landinstelling van de winkelweergave

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Selecteer in het vervolgkeuzemenu **[!UICONTROL Scope]** de archiefweergave die u wilt configureren, en klik op **[!UICONTROL OK]** wanneer u daarom wordt gevraagd.

1. Voor de *[!UICONTROL General]* configuratiepagina, breid ![&#x200B; de selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Locale Options]** sectie.

1. Schakel het selectievakje **[!UICONTROL Use Website]** uit en stel **[!UICONTROL Locale]** in op de taal die u aan de weergave wilt toewijzen.

   Als er verschillende variaties van de beschikbare taal zijn, zorg ervoor om één voor het specifieke gebied of dialect te kiezen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

   Nadat u de taal van de scène verandert, moet de resterende inhoud die u hebt gecreeerd, met inbegrip van productnamen en beschrijvingen, categorieën, [&#x200B; CMS &#x200B;](../content-design/page-translate.md) pagina&#39;s, en blokken afzonderlijk voor elke archiefmening worden vertaald.

## Producten lokaliseren

Als uw winkel meerdere weergaven in verschillende talen heeft, zijn in elke winkelweergave dezelfde producten beschikbaar. U kunt dezelfde basisproductinformatie gebruiken, zoals SKU, prijs en inventarisniveau, ongeacht de taal. Vertaal vervolgens voor elke taal alleen de productnaam, beschrijvingsvelden en metagegevens.

### Stap 1: Productvelden vertalen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Zoek in het raster het product dat u wilt vertalen en open het in de bewerkingsmodus.

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op de weergave voor de vertaling en klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om de vertaling te bevestigen.

1. Ga als volgt te werk voor elk veld dat moet worden bewerkt:

   - Schakel het selectievakje **[!UICONTROL Use Default Value]** rechts van het veld uit.

   - Plak of typ de vertaalde tekst in het veld.

   Zorg ervoor om alle tekstgebieden, met inbegrip van [&#x200B; beeld &#x200B;](../catalog/catalog-images-video.md) etiketten en de tekst van Alt, [&#x200B; de gebieden van de Optimalisering van de Motor van het Onderzoek &#x200B;](../catalog/product-search-engine-optimization.md) en om het even welke [&#x200B; 5&rbrace; informatie van de Opties van de Douane te vertalen.](../catalog/settings-advanced-custom-options.md)

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

### Stap 2: Veldlabels vertalen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Zoek in de lijst naar het kenmerk dat moet worden vertaald en open in de bewerkingsmodus.

1. Kies **[!UICONTROL Manage Labels]** in het linkerdeelvenster.

1. Voer in de sectie _[!UICONTROL Manage Titles]_&#x200B;een vertaald label in voor elke winkelweergave.

   ![&#x200B; ga Vertaalde Etiketten &#x200B;](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"} in

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.

### Stap 3: Alle categorieën vertalen

1. Op _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **Categorieën**.

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op de weergave voor de vertaling en klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om de vertaling te bevestigen.

1. Zoek in de boomstructuur naar de categorie die u wilt vertalen en open deze in de bewerkingsmodus.

1. Voor _BasisInformatie_, vertaal **[!UICONTROL Category Name]**.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de _[!UICONTROL Content]_&#x200B;sectie uit en vertaalt **[!UICONTROL Description]**.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization Settings]** sectie uit en vertaal de volgende gebieden:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Voer onder de sectie _[!UICONTROL Search Engine Optimization Settings]_&#x200B;de volgende handelingen uit om de **[!UICONTROL URL Key]**&#x200B;te vertalen:

   - Schakel het selectievakje **[!UICONTROL Use Default Value]** rechts van het veld uit.

   - Voer de vertaalde tekst in.

   - Controleer of het selectievakje **[!UICONTROL Create Permanent Redirect for old URL]** is ingeschakeld.

   ![&#x200B; vertaal de sleutel URL &#x200B;](./assets/category-translate-url-key.png)

1. Klik op **[!UICONTROL Save Category]** als de bewerking is voltooid.

1. Herhaal dit proces voor alle categorieën die in de winkel worden gebruikt.

### Stap 4: Opties voor het vertalen van productkenmerken en -kenmerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Selecteer het kenmerk dat moet worden vertaald.

1. Kies **[!UICONTROL Manage Labels]** aan de linkerkant en stel de **[!UICONTROL Managed Titles]** -opties in om de vertalingen van de kenmerktitel te definiëren.

1. Kies **[!UICONTROL Properties]** aan de linkerkant en voer de vertaalde kenmerkopties in de sectie **[!UICONTROL Manage Options]** in.

   ![&#x200B; beheert Opties &#x200B;](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.
