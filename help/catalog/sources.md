---
title: Productinstellingen - [!UICONTROL Sources]
description: Voor een product geldt het [!UICONTROL Sources] toegang tot de [!DNL Inventory Management] bronnen waaruit het product kan worden gedistribueerd.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Productinstellingen - [!UICONTROL Sources]

De _[!UICONTROL Sources]_in het gedeelte met productinstellingen worden de bronnen weergegeven waaruit het product kan worden gedistribueerd. Het wordt gebruikt om bronnen toe te wijzen en weg te wijzen en de hoeveelheid en de beschikbaarheid van het product te beheren. Deze sectie wordt alleen weergegeven als er meer dan één bron is gedefinieerd voor uw winkel. Zie voor meer informatie over bronnen [Bronnen beheren](../inventory-management/sources-manage.md).

## Een bron toewijzen voor een product

1. Klik op **[!UICONTROL Assign Source]**.

1. Schakel het selectievakje voor de vereiste bronnen in.

1. Klik op **[!UICONTROL Done]**.

1. Selecteren **[!UICONTROL Source Item Status]** en voert u de **[!UICONTROL Qty]** en **[!UICONTROL Notify Qty]** waarden.

1. Klikken **[!UICONTROL Save]** om de wijzigingen op te slaan

![Bronweergave](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Veldverwijzing

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Name] | De unieke naam voor een bron. |
| [!UICONTROL Source Status] | Hiermee wordt bepaald of het product in de catalogus is in- of uitgeschakeld. |
| [!UICONTROL Source Item Status] | Bepaalt de huidige beschikbaarheid van het product. Opties:<br />**[!UICONTROL In Stock]**- Maakt het product beschikbaar voor aankoop.<br />**[!UICONTROL Out of Stock]** - Als er geen backorders worden geactiveerd, kan het product niet worden aangeschaft en wordt de aanbieding uit de catalogus verwijderd. |
| [!UICONTROL Qty] | Aandelen voor elke bron. |
| [!UICONTROL Notify Qty] | Een bedrag voor de _Melden voor hoeveelheid_ voor deze specifieke bron als `Notify Quantity Use Default` is niet geselecteerd. |
| [!UICONTROL Notify Qty Use Default] | Geeft aan dat de standaardinstelling voor _Melden voor hoeveelheid_ in het product Geavanceerde Inventory of globale het plaatsen in de archiefconfiguratie. Voor meer informatie over geavanceerde voorraadinstellingen voor uw product raadpleegt u [Geavanceerde productopties configureren](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Voor een toegewezen bron klikt u op **[!UICONTROL Unassign]** om de bron niet beschikbaar te maken voor het product. Voor een niet toegewezen bron klikt u op **[!UICONTROL Assign Sources]** een bron voor het product beschikbaar te stellen. Voor meer informatie over [!UICONTROL Assign Sources] opties, zie [Bronnen toewijzen per product](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
