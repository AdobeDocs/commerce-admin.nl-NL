---
title: Voorwaarden voor afhandeling
description: Leer over de voorwaarden en de functionaliteit die voor uw opslag kunnen worden gevormd.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Voorwaarden voor afhandeling

Wanneer de hand _functionaliteit van de Voorwaarden van 0} wordt toegelaten, worden de klanten vereist om met de voorwaarden van de verkoop in te stemmen alvorens de aankoop wordt gebeëindigd._ De verkoopvoorwaarden omvatten doorgaans informatie die wettelijk vereist is voor B2C- of B2B-sites, en schetst de rechten van de koper en de verkoper. Het bericht van de Voorwaarden verschijnt na de betalingsinformatie, enkel vóór de _knoop van de Orde van de Plaats_.

![ Termen en Voorwaarden bij controle ](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Stap 1: Bepalingen en voorwaarden voor afhandeling inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Options]** sectie uit.

   ![ de Opties van de Controle ](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Controleer of **[!UICONTROL Enable Onepage Checkout]** is ingesteld op `Yes` .

1. Stel **[!UICONTROL Enable Terms and Conditions]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]**.

## Stap 2: Voeg uw eigen voorwaarden en bepalingen informatie toe

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![ het net van Bepalingen en van Voorwaarden ](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Condition]** .

1. Voer de **[!UICONTROL Condition Name]** in voor interne referentie.

   ![ Nieuwe Voorwaarde ](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Status]** in op `Enabled` .

1. Stel **[!UICONTROL Applied]** in op een van de volgende opties:

   - `Automatically` - Voorwaarden worden automatisch geaccepteerd bij het afrekenen.
   - `Manually` - Klanten moeten de voorwaarden voor het plaatsen van een bestelling handmatig accepteren.

1. Stel **[!UICONTROL Show Content as]** in op een van de volgende opties:

   - `Text` - Geeft de voorwaarden en inhoud weer als niet-opgemaakte tekst.
   - `HTML` - Geeft de inhoud weer als HTML die kan worden opgemaakt.

1. Selecteer elke **[!UICONTROL Store View]** waar u deze Voorwaarden wilt gebruiken.

1. Schuif omlaag en voltooi de informatie die moet worden weergegeven:

   - Voer de **[!UICONTROL Checkbox Text]** in die u als tekst voor de koppeling Voorwaarden en Voorwaarden wilt gebruiken. Bijvoorbeeld `I understand and accept the terms and conditions of the sale` .

   - Voer in het vak **[!UICONTROL Content]** de volledige tekst in van de verkoopvoorwaarden.

1. (Optioneel) Voer de **[!UICONTROL Content Height (css)]** in pixels in om de hoogte van het tekstvak te bepalen waarin de instructie terms and conditions tijdens het uitchecken wordt weergegeven.

   Als u bijvoorbeeld het tekstvak 1 inch hoog wilt maken op een weergave van 96 dpi, voert u `96` in. Er wordt een schuifbalk weergegeven als de inhoud de hoogte van het vak overschrijdt.

1. Klik op **[!UICONTROL Save Condition]**.
