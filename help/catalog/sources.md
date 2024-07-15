---
title: Productinstellingen - [!UICONTROL Sources]
description: Voor een product, verleent de [!UICONTROL Sources] montages toegang tot  [!DNL Inventory Management]  bronnen waarvan het product kan worden verdeeld.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Productinstellingen - [!UICONTROL Sources]

In het gedeelte _[!UICONTROL Sources]_van de productinstellingen worden de bronnen weergegeven waaruit het product kan worden gedistribueerd. Het wordt gebruikt om bronnen toe te wijzen en weg te wijzen en de hoeveelheid en de beschikbaarheid van het product te beheren. Deze sectie wordt alleen weergegeven als er meer dan één bron is gedefinieerd voor uw winkel. Voor meer informatie over bronnen, zie [ bronnen ](../inventory-management/sources-manage.md) leiden.

## Een bron toewijzen voor een product

1. Klik op **[!UICONTROL Assign Source]**.

1. Schakel het selectievakje voor de vereiste bronnen in.

1. Klik op **[!UICONTROL Done]**.

1. Selecteer **[!UICONTROL Source Item Status]** en voer de waarden **[!UICONTROL Qty]** en **[!UICONTROL Notify Qty]** naar wens in.

1. Klik op **[!UICONTROL Save]** om de wijzigingen op te slaan.

![ Bronmening ](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Veldverwijzing

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Name] | De unieke naam voor een bron. |
| [!UICONTROL Source Status] | Hiermee wordt bepaald of het product in de catalogus is in- of uitgeschakeld. |
| [!UICONTROL Source Item Status] | Bepaalt de huidige beschikbaarheid van het product. Opties:<br />**[!UICONTROL In Stock]**- maakt het product beschikbaar voor aankoop.<br />**[!UICONTROL Out of Stock]** - Als er geen backorders zijn geactiveerd, kan het product niet worden aangeschaft en wordt de aanbieding uit de catalogus verwijderd. |
| [!UICONTROL Qty] | Aandelen voor elke bron. |
| [!UICONTROL Notify Qty] | Een bedrag voor _deelt voor Hoeveelheid_ voor deze specifieke bron mee als `Notify Quantity Use Default` niet wordt geselecteerd. |
| [!UICONTROL Notify Qty Use Default] | Wijst erop om het gebrek te gebruiken dat voor _plaatst op Melden voor Hoeveelheid_ in het product Geavanceerde Overzicht of het globale plaatsen in de opslagconfiguratie. Voor meer informatie over geavanceerde inventarismontages voor uw product, zie [ geavanceerde productopties ](../inventory-management/product-options.md) vormen. |
| [!UICONTROL Actions] | Voor een toegewezen bron klikt u op **[!UICONTROL Unassign]** om de bron niet beschikbaar te maken voor het product. Voor een niet-toegewezen bron klikt u op **[!UICONTROL Assign Sources]** om een bron beschikbaar te maken voor het product. Voor meer informatie over [!UICONTROL Assign Sources] opties, zie [ Toewijzende Bronnen per Product ](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
