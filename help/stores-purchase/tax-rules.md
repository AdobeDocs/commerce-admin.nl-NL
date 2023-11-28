---
title: Belastingregels
description: Leer hoe u de belastingregels definieert aan de hand van productklasse, klantenklasse en belastingtarief.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Belastingregels

De belastingregels omvatten een combinatie productklasse, klantenklasse, en belastingtarief. Elke klant wordt toegewezen aan een klantenklasse, en elk product wordt toegewezen een productklasse. De handel analyseert het winkelwagentje van elke klant en berekent de aangewezen belasting volgens de klant en de productklassen, en de regio. De regio is gebaseerd op het verzendadres, het factuuradres of de herkomst van de verzending van de klant.

>[!NOTE]
>
>Wanneer er veel belastingtarieven moeten worden gedefinieerd, kunt u het proces vereenvoudigen door deze in te voeren.

![Belastingregels](./assets/tax-rules.png){width="600" zoomable="yes"}

## Stap 1: De informatie over de belastingregel invullen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Tax Rule]**.

1. Onder _Informatie over belastingregels_, voert u een **[!UICONTROL Name]** voor de nieuwe regel.

   ![Informatie over belastingregels](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Kies de optie **[!UICONTROL Tax Rate]** dat geldt voor de regel .

   Ga als volgt te werk om een bestaand belastingtarief te bewerken:

   - Houd de muis boven het belastingtarief en klik op de knop _Bewerken_ ![Pictogram Potlood](../assets/icon-edit-pencil.png) pictogram.

   - Werk het formulier naar wens bij en klik op **[!UICONTROL Save]**.

1. Gebruik een van de volgende methoden om belastingtarieven in te voeren:

### Methode 1: BTW-tarieven handmatig invoeren

1. Klik op **[!UICONTROL Add New Tax Rate]**.

1. Vul het formulier naar wens in (zie [Belastingzones en -tarieven](tax-zones-rates.md)).

1. Klik op **[!UICONTROL Save]**.

   ![Nieuw belastingtarief](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Methode 2: Belastingtarieven bij invoer

1. Schuif omlaag naar de sectie onder aan de pagina.

1. Ga als volgt te werk om belastingtarieven te importeren:

   - Klikken **[!UICONTROL Choose File]** en navigeer naar het CSV-bestand met de te importeren belastingtarieven.

   - Klik op **[!UICONTROL Import Tax Rates]**.

1. Als u belastingtarieven wilt exporteren, klikt u op **[!UICONTROL Export Tax Rates]** (zie [Belastingtarieven in-/uitvoer](../systems/data-transfer-tax-rates.md)).

![Belastingtarieven in-/uitvoer](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Stap 2: Voltooi de extra instellingen

1. Als u de sectie wilt openen, klikt u op **[!UICONTROL Additional Settings]**.

   ![Aanvullende instellingen voor de belastingregel](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Kies de optie **[!UICONTROL Customer Tax Class]** waarop de regel van toepassing is.

   - Als u een klasse met klantbelastingen wilt bewerken, klikt u op de knop _Bewerken_ ![Pictogram Potlood](../assets/icon-edit-pencil.png) pictogram, werk het formulier zo nodig bij en klik op **[!UICONTROL Save]**.

   - Als u een belastingklasse wilt maken, klikt u **[!UICONTROL Add New Tax Class]**, vult het formulier naar wens in en klikt u op **[!UICONTROL Save]**.

1. Kies de optie **[!UICONTROL Product Tax Class]** waarop de regel van toepassing is.

   - Als u een productbelastingklasse wilt bewerken, klikt u op de knop _Bewerken_ ![Pictogram Potlood](../assets/icon-edit-pencil.png) pictogram, werk het formulier zo nodig bij en klik op **[!UICONTROL Save]**.

   - Als u een belastingklasse wilt maken, klikt u **[!UICONTROL Add New Tax Class]**, vult het formulier naar wens in en klikt u op **[!UICONTROL Save]**.

1. Wanneer meer dan één belasting van toepassing is, ga een aantal in om de prioriteit van deze belasting voor te wijzen **[!UICONTROL Priority]**.

   Als twee belastingregels met dezelfde prioriteit van toepassing zijn, worden de belastingen toegevoegd. Als twee belastingen met verschillende prioritaire montages van toepassing zijn, worden de belastingen samengevoegd.

1. Als u belastingen op het orde subtotaal wilt baseren, selecteer **[!UICONTROL Calculate off Subtotal Only]** selectievakje.

1. Voor **[!UICONTROL Sort Order]** Voer een getal in om de volgorde van deze belastingregel aan te geven wanneer deze bij anderen wordt aangeboden.

1. Klik op **[!UICONTROL Save Rule]**.

## Demo voor valuta- en belastingregels

Bekijk deze video voor meer informatie over het beheren van valuta- en belastingregels:

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
