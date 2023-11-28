---
title: Productwerkruimte
description: Leer meer over de instellingen en besturingselementen in de productwerkruimte.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Productwerkruimte

De werkruimte van het product is in principe hetzelfde voor alle producttypen, hoewel de selectie van velden afhankelijk van de gebruikte kenmerkenset verandert. De productkenmerken staan boven aan het formulier, gevolgd door uitbreidbare gedeelten van de productinformatie. Wanneer een nieuw product voor de eerste keer wordt opgeslagen, _[!UICONTROL Store View]_wordt linksboven in het formulier weergegeven.

![Productwerkruimte](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] instellen

De onlinestatus van het product wordt aangegeven door de switch boven aan het formulier. Als u de onlinestatus wilt wijzigen, stelt u de **[!UICONTROL Enable Product]** schakelen naar `Yes` of `No`.

| Besturing | Beschrijving |
|-------- | ----------- |
| ![Ja in-/uitschakelen](../assets/toggle-yes.png) | Geeft aan dat het product online is. |
| ![Niet in-/uitschakelen](../assets/toggle-no.png) | Geeft aan dat het product offline is. |

{style="table-layout:auto"}

## Kenmerkset

De naam van [kenmerkset](attribute-sets.md) wordt in de linkerbovenhoek weergegeven en bepaalt de velden die in de productrecord worden weergegeven. Als u een andere kenmerkset wilt kiezen, klikt u op de pijl omlaag naast de naam van de standaardkenmerkset.

![Kenmerkset](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Uitvouwen/samenvouwen

Als u een sectie wilt uitvouwen of samenvouwen, klikt u op de knop ![Expansiekiezer](../assets/icon-display-expand.png) of samenvouwen ![Selectie samenvouwen](../assets/icon-display-collapse.png) pictogram.

## [!UICONTROL Save] menu

De _[!UICONTROL Save]_bevat verschillende opties waarmee u een product kunt opslaan en vervolgen, opslaan en maken, het product kunt opslaan en dupliceren of het kunt opslaan en sluiten.

![Menu Opslaan](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Opdracht | Beschrijving |
|--- |--- |
| [!UICONTROL Save] | Sla het huidige product op en ga verder met werken. |
| [!UICONTROL Save & New] | Sla het huidige product op, sluit het en start een nieuw product op basis van hetzelfde producttype en dezelfde sjabloon. |
| [!UICONTROL Save & Duplicate] | Sla het huidige product op, sluit het en open een nieuwe kopie. |
| [!UICONTROL Save & Close] | Het huidige product opslaan en terugkeren naar de _[!UICONTROL Products]_werkruimte. |

{style="table-layout:auto"}

## Standaardveldwaarden

Als u tijd wilt besparen tijdens het maken van producten, verwijst de standaardwaarde van verschillende productvelden naar waarden van een ander veld. U kunt de standaardwaarde accepteren of een andere waarde invoeren. De volgende velden hebben automatisch standaardwaarden gegenereerd:

| Veld | Standaard |
|----- |------- |
| [!UICONTROL SKU] | Gebaseerd op productnaam. |
| [!UICONTROL Meta Title] | Gebaseerd op productnaam. |
| [!UICONTROL Meta Keywords] | Gebaseerd op productnaam. |
| [!UICONTROL Meta Description] | Gebaseerd op productnaam en beschrijving. |

{style="table-layout:auto"}

De plaatsaanduidingen die de waarde van een ander veld vertegenwoordigen, worden tussen dubbele accolades geplaatst. Elke kenmerkcode die in het product is opgenomen [kenmerkset](attribute-sets.md) kan als plaatsaanduiding worden gebruikt.

![Productvelden automatisch genereren](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Voor een gedetailleerde lijst van deze montages, zie [Productvelden automatisch genereren](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) in de _Configuratieverwijzing_.

### De plaatsaanduidingswaarde bewerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Product Fields Auto-Generation]** en brengt de gewenste wijzigingen aan in de waarden van de plaatsaanduiding.

   Als er bijvoorbeeld een specifiek trefwoord is dat u voor elk product wilt opnemen of een woordgroep die u in elke metabeschrijving wilt opnemen, voert u de waarde rechtstreeks in het desbetreffende veld in.

   >[!NOTE]
   >
   >Als u de bestaande plaatsaanduidingswaarden wilt behouden, behoudt u de dubbele accolades rondom elke opmaakcode.

1. Klik op **[!UICONTROL Save Config]**.

### Algemene plaatsaanduidingen

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
