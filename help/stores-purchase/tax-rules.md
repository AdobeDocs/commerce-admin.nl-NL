---
title: Belastingregels
description: Leer hoe u de belastingregels definieert aan de hand van productklasse, klantenklasse en belastingtarief.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Belastingregels

De belastingregels omvatten een combinatie productklasse, klantenklasse, en belastingtarief. Elke klant wordt toegewezen aan een klantenklasse, en elk product wordt toegewezen een productklasse. Commerce analyseert het winkelwagentje van elke klant en berekent de toepasselijke belasting volgens de klant en de productklassen, en de regio. De regio is gebaseerd op het verzendadres, het factuuradres of de herkomst van de verzending van de klant.

>[!NOTE]
>
>Wanneer er veel belastingtarieven moeten worden gedefinieerd, kunt u het proces vereenvoudigen door deze in te voeren.

![&#x200B; de Regels van de Belasting &#x200B;](./assets/tax-rules.png){width="600" zoomable="yes"}

## Stap 1: De informatie over de belastingregel invullen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Tax Rule]** .

1. Onder _de Informatie van de Regel van de Belasting_, ga a **[!UICONTROL Name]** voor de nieuwe regel in.

   ![&#x200B; de Informatie van de Regel van de Belasting &#x200B;](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Kies de **[!UICONTROL Tax Rate]** die op de regel van toepassing is.

   Ga als volgt te werk om een bestaand belastingtarief te bewerken:

   - Beweeg over het belastingtarief en klik _uitgeven_ ![&#x200B; pictogram van het Potlood &#x200B;](../assets/icon-edit-pencil.png) pictogram.

   - Werk het formulier naar wens bij en klik op **[!UICONTROL Save]** .

1. Gebruik een van de volgende methoden om belastingtarieven in te voeren:

### Methode 1: BTW-tarieven handmatig invoeren

1. Klik op **[!UICONTROL Add New Tax Rate]**.

1. Voltooi de vorm zoals nodig (zie [&#x200B; de streken en de Tarieven van de Belasting &#x200B;](tax-zones-rates.md)).

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   ![&#x200B; Nieuw Tarief van de Belasting &#x200B;](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Methode 2: Belastingtarieven bij invoer

1. Schuif omlaag naar de sectie onder aan de pagina.

1. Ga als volgt te werk om belastingtarieven te importeren:

   - Klik op **[!UICONTROL Choose File]** en navigeer naar het CSV-bestand met de belastingtarieven die u wilt importeren.

   - Klik op **[!UICONTROL Import Tax Rates]**.

1. Om belastingtarieven uit te voeren, klik **[!UICONTROL Export Tax Rates]** (zie [&#x200B; de Tarieven van de Belasting van de Invoer/van de Uitvoer &#x200B;](../systems/data-transfer-tax-rates.md)).

![&#x200B; Invoer/de Tarieven van de Uitvoer &#x200B;](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Stap 2: Voltooi de extra instellingen

1. Klik op **[!UICONTROL Additional Settings]** om de sectie te openen.

   ![&#x200B; Extra Montages voor belastingregel &#x200B;](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Kies de **[!UICONTROL Customer Tax Class]** waarop de regel van toepassing is.

   - Om een klasse van de klantenbelasting uit te geven, klik __ ![&#x200B; pictogram van het Potlood &#x200B;](../assets/icon-edit-pencil.png), werk de vorm zoals nodig bij, en klik **[!UICONTROL Save]**.

   - Als u een belastingklasse wilt maken, klikt u op **[!UICONTROL Add New Tax Class]** , vult u het formulier naar wens in en klikt u op **[!UICONTROL Save]** .

1. Kies de **[!UICONTROL Product Tax Class]** waarop de regel van toepassing is.

   - Om een klasse van de productbelasting uit te geven, klik __ ![&#x200B; pictogram van het Potlood &#x200B;](../assets/icon-edit-pencil.png), werk de vorm zoals nodig bij, en klik **[!UICONTROL Save]**.

   - Als u een belastingklasse wilt maken, klikt u op **[!UICONTROL Add New Tax Class]** , vult u het formulier naar wens in en klikt u op **[!UICONTROL Save]** .

1. Wanneer meer dan één belasting van toepassing is, ga een aantal in om de prioriteit van deze belasting voor **[!UICONTROL Priority]** te wijzen.

   Als twee belastingregels met dezelfde prioriteit van toepassing zijn, worden de belastingen toegevoegd. Als twee belastingen met verschillende prioritaire montages van toepassing zijn, worden de belastingen samengevoegd.

1. Als u belastingen wilt baseren op het subtotaal van de bestelling, schakelt u het selectievakje **[!UICONTROL Calculate off Subtotal Only]** in.

1. Voer bij **[!UICONTROL Sort Order]** een getal in om de volgorde van deze belastingregel aan te geven wanneer deze bij anderen wordt aangeboden.

1. Klik op **[!UICONTROL Save Rule]** als de bewerking is voltooid.

## Demo voor valuta- en belastingregels

Bekijk deze video voor meer informatie over het beheren van valuta- en belastingregels:

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12&learn=on)
