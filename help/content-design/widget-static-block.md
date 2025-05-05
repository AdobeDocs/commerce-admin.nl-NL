---
title: Een widget gebruiken om een blok te plaatsen
description: Leer hoe u een statische blokwidget kunt gebruiken om een bestaande inhoud vrijwel overal in uw winkel te plaatsen.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Een widget gebruiken om een blok te plaatsen

Het _Statische Blok CMS_ [ widget ](widgets.md) geeft u de capaciteit om een bestaand [ inhoudsblok ](blocks.md) bijna overal in uw opslag te plaatsen.

![ Widgets ](./assets/widgets.png){width="700" zoomable="yes"}

## Stap 1: Kies het widgettype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]** .

1. In de _sectie van Montages_, plaats **[!UICONTROL Type]** aan `CMS Static Block` en klik **[!UICONTROL Continue]**.

1. Controleer of **[!UICONTROL Design Theme]** is ingesteld op het huidige thema en klik op **[!UICONTROL Continue]** .

   ![ montages van Widget ](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Ga als volgt te werk in de sectie _[!UICONTROL Storefront Properties]_:

   - Voer bij **[!UICONTROL Widget Title]** een beschrijvende titel in voor de widget.

     Deze titel is zichtbaar slechts van _Admin_.

   - Selecteer bij **[!UICONTROL Assign to Store Views]** de winkelweergaven waarin de widget zichtbaar is.

     U kunt een specifieke opslagweergave selecteren, of `All Store Views` . Als u meerdere weergaven wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   - (Optioneel) Voer bij **[!UICONTROL Sort Order]** een getal in om te bepalen in welke volgorde dit item bij anderen in hetzelfde gedeelte van de pagina wordt weergegeven. (`0` = first, `1` = second, `3` = third, enzovoort.)

     ![ eigenschappen Storefront ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Stap 2: De updates van de widgetlay-out voltooien

1. Klik in de sectie _[!UICONTROL Layout Updates]_&#x200B;op **[!UICONTROL Add Layout Update]**.

1. Stel **[!UICONTROL Display On]** in op de categorie, het product of de pagina waar u het blok wilt weergeven.

1. Ga als volgt te werk om het blok op een specifieke pagina te plaatsen:

   - Kies de locatie **[!UICONTROL Page]** waar u het blok wilt weergeven.

   - Kies de **[!UICONTROL Block Reference]** die de plaats identificeert waar het blok op de pagina wordt getoond.

   - Accepteer de standaardinstelling voor **[!UICONTROL Template]** , die is ingesteld op `CMS Static Block Default Template` .

     ![ de updates van de Lay-out ](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Update-opties voor lay-out

| Veld | Beschrijving |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Hiermee geeft u de widget weer op de pagina met ankercategorieën.<br/>**[!UICONTROL Categories]**- Categorieën waarin het anker wordt weergegeven. Opties: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Stel de container in op het deel van de paginalay-out waar u de widget wilt weergeven.<br/>**[!UICONTROL Template]**- Bepaalt het thema van de lay-out. |
| [!UICONTROL Non-Anchor Categories] | Hiermee geeft u de widget weer op de categoriepagina die niet als anker fungeert.<br/>**[!UICONTROL Categories]**- Categorieën waarin het anker wordt weergegeven. Opties: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Stel de container in op het deel van de paginalay-out waar u de widget wilt weergeven.<br/>**[!UICONTROL Template]**- Bepaalt het thema van de lay-out. |
| **_[!UICONTROL Products]_** |  |
| Alle producttypen | Hiermee geeft u de widget weer op een specifiek type productpagina of op alle productpagina&#39;s. <br/>**[!UICONTROL Products]**- Producten waarvoor de widget wordt weergegeven. Opties: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Stel de container in op het deel van de paginalay-out waar u de widget wilt weergeven.<br/>**[!UICONTROL Template]**- Bepaalt het thema van de lay-out. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Hiermee wordt de widget op alle pagina&#39;s weergegeven. <br/>**[!UICONTROL Container]**- Stel de container in op het deel van de paginalay-out waar u de widget wilt weergeven.<br/>**[!UICONTROL Template]** - Bepaalt het thema van de lay-out. |
| [!UICONTROL Specified Page] | Hiermee geeft u de widget op een specifieke pagina weer. Opties:<br/>**[!UICONTROL Page]**- Pagina&#39;s waarvoor widget wordt getoond.<br/>**[!UICONTROL Container]** - Stel de container in op het deel van de paginalay-out waar u de widget wilt weergeven.<br/>**Malplaatje** - bepaalt het thema van de lay-out. |
| [!UICONTROL Page Layouts] | Hiermee wordt de widget weergegeven op pagina&#39;s met een bepaalde indeling. <br/>**[!UICONTROL Page]**- Pagina&#39;s waarvoor de widget wordt weergegeven.<br/>**[!UICONTROL Container]** - Stel de container in op het deel van de paginalay-out waar u de widget wilt weergeven.<br/>**[!UICONTROL Template]**- Bepaalt het thema van de lay-out. |

{style="table-layout:auto"}

## Stap 3: Plaats het blok

1. Selecteer **[!UICONTROL Widget Options]** in het linkerdeelvenster.

1. Klik op **[!UICONTROL Select Block…]** en kies het blok dat u wilt plaatsen in de lijst.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   De app wordt nu in de lijst weergegeven.

1. Volg desgevraagd de instructies boven aan de pagina om de index en de paginacache bij te werken.

1. Ga terug naar de winkel om te controleren of het blok op de juiste locatie wordt weergegeven.

   Als u het blok wilt verplaatsen, kunt u de widget opnieuw openen of een andere pagina of blokverwijzing proberen.
