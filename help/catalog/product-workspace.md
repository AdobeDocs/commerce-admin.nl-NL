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

De werkruimte van het product is in principe hetzelfde voor alle producttypen, hoewel de selectie van velden afhankelijk van de gebruikte kenmerkenset verandert. De productkenmerken staan boven aan het formulier, gevolgd door uitbreidbare gedeelten van de productinformatie. Wanneer een nieuw product voor de eerste keer wordt opgeslagen, wordt de _[!UICONTROL Store View]_-kiezer linksboven in het formulier weergegeven.

![ de werkruimte van het Product ](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] instellen

De onlinestatus van het product wordt aangegeven door de switch boven aan het formulier. Als u de onlinestatus wilt wijzigen, stelt u de **[!UICONTROL Enable Product]** switch in op `Yes` of `No` .

| Besturing | Beschrijving |
|-------- | ----------- |
| ![ Wissel ja ](../assets/toggle-yes.png) | Geeft aan dat het product online is. |
| ![ knevel nr. ](../assets/toggle-no.png) | Geeft aan dat het product offline is. |

{style="table-layout:auto"}

## Kenmerkset

De naam van de [ geplaatste attributen ](attribute-sets.md) verschijnt in de upper-left hoek en bepaalt de gebieden die in het productverslag verschijnen. Als u een andere kenmerkset wilt kiezen, klikt u op de pijl omlaag naast de naam van de standaardkenmerkset.

![ Reeks van Attributen ](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Uitvouwen/samenvouwen

Om een sectie uit te breiden of te doen ineenstorten, klik of ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uitbreiden of ![ invouwen selecteur ](../assets/icon-display-collapse.png) pictogram.

## [!UICONTROL Save] menu

Het menu _[!UICONTROL Save]_&#x200B;bevat verschillende opties waarmee u een product kunt opslaan en vervolgen, opslaan en maken, het product kunt opslaan en dupliceren of het kunt opslaan en sluiten.

![ sparen menu ](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Opdracht | Beschrijving |
|--- |--- |
| [!UICONTROL Save] | Sla het huidige product op en ga verder met werken. |
| [!UICONTROL Save & New] | Sla het huidige product op, sluit het en start een nieuw product op basis van hetzelfde producttype en dezelfde sjabloon. |
| [!UICONTROL Save & Duplicate] | Sla het huidige product op, sluit het en open een nieuwe kopie. |
| [!UICONTROL Save & Close] | Sla het huidige product op en ga terug naar de werkruimte van _[!UICONTROL Products]_. |

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

De plaatsaanduidingen die de waarde van een ander veld vertegenwoordigen, worden tussen dubbele accolades geplaatst. Om het even welke kenmerkcode die in de product [ geplaatste attributen ](attribute-sets.md) inbegrepen is kan als placeholder worden gebruikt.

![ de Gebieden van het Product auto-Generatie ](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Voor een gedetailleerde lijst van deze montages, zie [ de Gebieden van het Product auto-Generatie ](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) in de _Verwijzing van de Configuratie_.

### De plaatsaanduidingswaarde bewerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Product Fields Auto-Generation]** sectie uit en breng om het even welke noodzakelijke veranderingen in de placeholder waarden aan.

   Als er bijvoorbeeld een specifiek trefwoord is dat u voor elk product wilt opnemen of een woordgroep die u in elke metabeschrijving wilt opnemen, voert u de waarde rechtstreeks in het desbetreffende veld in.

   >[!NOTE]
   >
   >Als u de bestaande plaatsaanduidingswaarden wilt behouden, behoudt u de dubbele accolades rondom elke opmaakcode.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

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
