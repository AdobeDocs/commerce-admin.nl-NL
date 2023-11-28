---
title: Belastingzones en -tarieven
description: Leer hoe u belastingtarieven definieert voor elk geografisch gebied waar u belastingen int en terugbetaalt.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Belastingzones en -tarieven

Over het algemeen gelden belastingtarieven voor transacties die binnen een bepaald geografisch gebied plaatsvinden. Gebruik de _Belastingzones en -tarieven_ een instrument om het belastingtarief te specificeren voor elk geografisch gebied waarvan u belastingen int en kwijtscheldt. Omdat elke belastingzone en elk tarief een uniek herkenningsteken hebben, kunt u veelvoudige belastingtarieven voor een bepaald geografisch gebied (zoals plaatsen die geen voedsel of geneeskunde, maar belasting andere voorwerpen belasten) hebben.

Winkelbelasting wordt berekend op basis van het adres van de winkel. De daadwerkelijke klantenbelasting voor een orde wordt berekend nadat de klant de ordeinformatie voltooit. De handel berekent dan de belasting volgens de belastingconfiguratie van de opslag.

![Belastingzones en -tarieven](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Een nieuw belastingtarief definiëren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Tax Rate]**.

   ![Nieuw belastingtarief](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Tax Identifier]**.

1. Als u het belastingtarief op één postcode of postcode wilt toepassen, voert u de code in voor **[!UICONTROL Zip/Post Code]**.

   Het sterretje (`*`) kan worden gebruikt om maximaal tien tekens in de code overeen te laten komen. Bijvoorbeeld: `90*` staat voor alle ZIP-codes tussen 90000 en 90999.

1. Ga als volgt te werk om het belastingtarief toe te passen op een reeks postcodes of postcodes:

   - Selecteer de **[!UICONTROL Zip/Post is Range]** selectievakje en geef het bereik op door de eerste en laatste postcode van **[!UICONTROL Range From]** en **[!UICONTROL Range To]**.

     ![ZIP/Post is bereik](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Kies de optie **[!UICONTROL State]** wanneer het belastingtarief van toepassing is.

   - Kies de optie **[!UICONTROL Country]** wanneer het belastingtarief van toepassing is.

   - Voer de **[!UICONTROL Rate Percent]** die wordt gebruikt voor de berekening van het belastingtarief.

1. Als u meerdere opslagruimten hebt, kunt u **[!UICONTROL Tax Titles]** voor elke winkelweergave.

   >[!NOTE]
   >
   >Laat dit veld leeg als u de BTW-ID wilt gebruiken.

1. Klik op **[!UICONTROL Save Rate]**.

## Een bestaand belastingtarief bewerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Zoek het belastingtarief in de _[!UICONTROL Tax Zones and Rates]_en opent u de record in de bewerkingsmodus.

   Als de lijst veel snelheden bevat, gebruikt u de opdracht [filterbesturingselementen](../getting-started/admin-grid-controls.md) om het tarief te vinden u nodig hebt.

1. Breng de noodzakelijke wijzigingen aan in de **[!UICONTROL Tax Rate Information]**.

1. Werk de **[!UICONTROL Tax Titles]** indien nodig.

1. Klik op **[!UICONTROL Save Rate]**.

## Belastingtarief verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Zoek het belastingtarief dat moet worden geschrapt en open het in uitgeven wijze.

1. Klik in de menubalk op **[!UICONTROL Delete Rate]**.

1. Klik op **[!UICONTROL OK]**.
