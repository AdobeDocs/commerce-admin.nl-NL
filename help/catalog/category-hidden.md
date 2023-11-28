---
title: Verborgen categorieën
description: Leer hoe u verborgen categorieën gebruikt voor interne doeleinden of hoe u een koppeling tot stand brengt met een categorie die niet in het navigatiemenu staat.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Verborgen categorieën

Verborgen categorieën kunnen op verschillende manieren worden gebruikt. U zou extra categorieniveaus voor uw eigen interne doeleinden kunnen willen tot stand brengen, maar slechts de categorieën op hoger niveau aan uw klanten tonen. Of u wilt een koppeling maken naar een categorie die niet in het navigatiemenu is opgenomen.

## Verborgen categorieën maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Selecteer in de categoriestructuur de categorie die u wilt verbergen en ga als volgt te werk:

   - Set **[!UICONTROL Is Active]** tot `Yes`.
   - Set **[!UICONTROL Include in Menu]** tot `No`.

1. In de **[!UICONTROL Display Settings]** sectie, set **[!UICONTROL Anchor]** tot `No`.

   ![Verborgen categorie](./assets/hidden-categories.png){width="600" zoomable="yes"}

   De verborgen categorie is actief, maar wordt niet weergegeven in het bovenste menu of in gelaagde navigatie.

1. Voer de volgende instellingen voor elke verborgen subcategorie in om subcategorieën te maken:

   >[!NOTE]
   >
   >Hoewel de categorie verborgen is, kunt u onderliggende subcategorieën maken en deze activeren.

   - Set **[!UICONTROL Enable Category]** tot `Yes`.
   - In de **[!UICONTROL Display Settings]** sectie, set **[!UICONTROL Anchor]** tot `Yes`.

   Als actieve categorieën kunt u nu een koppeling maken naar deze categorieën vanuit andere locaties in uw winkel, maar deze worden niet weergegeven in het menu.

1. Klik op **[!UICONTROL Save]**.
