---
title: Retourneert, kenmerk
description: Leer meer over de geretourneerde kenmerken en hoe u de kenmerken maakt die nodig zijn voor het verwerken van geretourneerde bedragen in uw winkel.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Retourneert, kenmerk

{{ee-feature}}

De terugkeerattributen worden gebruikt om informatie op te slaan die tijdens het proces van de productterugkeer nodig is. De standaardattributen omvatten de voorwaarde van het teruggekeerde product, de reden voor de terugkeer, en een gebied dat erop wijst hoe de terugkeer werd opgelost. Het proces voor het maken van een kenmerk returns is vergelijkbaar met het maken van een [klantkenmerk](../customers/attribute-properties.md).

![Admin - Retourneert kenmerken](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Een kenmerk voor geretourneerde waarden maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Attribute]**.

   ![Nieuwe return - eigenschappen van kenmerken](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Eigenschappen definiëren

1. Als u het kenmerk wilt identificeren tijdens het invoeren van gegevens, stelt u de optie **[!UICONTROL Default Label]**.

1. Voor **[!UICONTROL Attribute Code]**, voert u een code in die het kenmerk binnen het systeem identificeert.

1. Om het type van inputcontrole te bepalen dat voor gegevensingang wordt gebruikt, reeks **[!UICONTROL Input Type]** op een van de volgende wijzen:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Als u van het veld een vereist item wilt maken, stelt u **[!UICONTROL Values Required]** tot `Yes`.

1. Als u een initiële waarde aan het veld wilt toewijzen, voert u een **[!UICONTROL Default Value]**.

1. Als u de juistheid van de ingevoerde gegevens in het veld wilt controleren voordat de record wordt opgeslagen, stelt u **[!UICONTROL Input Validation]** op een van de volgende wijzen:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Voor de `Text Field` en `Text Area` invoertypen, voert u de **[!UICONTROL Minimum Text Length]** en **[!UICONTROL Maximum Text Length]**.

1. Als u een voorverwerkingsfilter wilt toepassen, stelt u **[!UICONTROL Input/Output Filter]** op een van de volgende wijzen:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Als u het kenmerk zichtbaar wilt maken voor klanten, stelt u **[!UICONTROL Show on Storefront]** tot `Yes` in de _[!UICONTROL Storefront Properties]_sectie.

1. (Optioneel) Voor **[!UICONTROL Sort Order]** Voer een getal in om te bepalen waar dit kenmerk wordt weergegeven ten opzichte van de andere kenmerken in hetzelfde gedeelte van de pagina. (`0` = eerst, `1` = seconde, `2` = derde, enzovoort.)

### De labels/opties beheren

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Manage Labels/Options]**.

1. In de **[!UICONTROL Manage Titles (Size, Color, etc.)]** , voert u het label in voor elke winkelweergave.

   ![Labels beheren](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Als de **[!UICONTROL Input Type]** for the attribute is `Dropdown`beheert u de opties in het dialoogvenster **[!UICONTROL Manage Options (Values of Your Attribute)]** sectie.

   - Als u een optie wilt toevoegen, klikt u **[!UICONTROL Add Option]** en voer het label voor Admin en elke winkelweergave in.
   - Als u van een optie de geselecteerde standaard wilt maken, kiest u **[!UICONTROL Is Default]**.
   - Klik op **[!UICONTROL Delete]**.

1. Als u wijzigingen wilt opslaan, klikt u op **[!UICONTROL Save Attribute]**.
