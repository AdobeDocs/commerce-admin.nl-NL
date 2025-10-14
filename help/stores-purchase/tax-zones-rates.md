---
title: Belastingzones en -tarieven
description: Leer hoe u belastingtarieven definieert voor elk geografisch gebied waar u belastingen int en terugbetaalt.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Belastingzones en -tarieven

Over het algemeen gelden belastingtarieven voor transacties die binnen een bepaald geografisch gebied plaatsvinden. Gebruik het _hulpmiddel van de Zones en van Tarieven van de Belasting_ om het belastingtarief voor elk geografisch gebied te specificeren waarvan u belastingen int en verdeelt. Omdat elke belastingzone en elk tarief een uniek herkenningsteken hebben, kunt u veelvoudige belastingtarieven voor een bepaald geografisch gebied (zoals plaatsen die geen voedsel of geneeskunde, maar belasting andere voorwerpen belasten) hebben.

Winkelbelasting wordt berekend op basis van het adres van de winkel. De daadwerkelijke klantenbelasting voor een orde wordt berekend nadat de klant de ordeinformatie voltooit. Commerce berekent vervolgens de belasting op basis van de belastingconfiguratie van de winkel.

![&#x200B; Belastingzones en Tarieven &#x200B;](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Een nieuw belastingtarief definiëren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Tax Rate]** .

   ![&#x200B; Nieuw Tarief van de Belasting &#x200B;](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Tax Identifier]** in.

1. Voer de code voor **[!UICONTROL Zip/Post Code]** in als u het belastingtarief op één postcode of postcode wilt toepassen.

   Het asteriskvervanging (`*`) kan worden gebruikt om tot tien karakters in de code aan te passen. `90*` vertegenwoordigt bijvoorbeeld alle ZIP-codes tussen 90000 en 90999.

1. Ga als volgt te werk om het belastingtarief toe te passen op een reeks postcodes of postcodes:

   - Schakel het selectievakje **[!UICONTROL Zip/Post is Range]** in en definieer het bereik door de eerste en laatste postcode voor **[!UICONTROL Range From]** en **[!UICONTROL Range To]** in te voeren.

     ![&#x200B; ZIP/Post is Waaier &#x200B;](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Kies de **[!UICONTROL State]** waar het belastingtarief van toepassing is.

   - Kies de **[!UICONTROL Country]** waar het belastingtarief van toepassing is.

   - Voer de **[!UICONTROL Rate Percent]** in die voor de berekening van het belastingtarief wordt gebruikt.

1. Als u meerdere winkels hebt, kunt u **[!UICONTROL Tax Titles]** instellen voor elke winkelweergave.

   >[!NOTE]
   >
   >Laat dit veld leeg als u de BTW-ID wilt gebruiken.

1. Klik op **[!UICONTROL Save Rate]** als de bewerking is voltooid.

## Een bestaand belastingtarief bewerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Zoek het belastingtarief in het _[!UICONTROL Tax Zones and Rates]_&#x200B;net, en open het verslag in geef wijze uit.

   Als er vele tarieven in de lijst zijn, gebruik de [&#x200B; filtercontroles &#x200B;](../getting-started/admin-grid-controls.md) om het tarief te vinden u wenst.

1. Breng de gewenste wijzigingen aan in de **[!UICONTROL Tax Rate Information]** .

1. Werk de **[!UICONTROL Tax Titles]** zo nodig bij.

1. Klik op **[!UICONTROL Save Rate]** als de bewerking is voltooid.

## Belastingtarief verwijderen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Zoek het belastingtarief dat moet worden geschrapt en open het in uitgeven wijze.

1. Klik in de menubalk op **[!UICONTROL Delete Rate]** .

1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.
