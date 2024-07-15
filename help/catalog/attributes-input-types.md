---
title: Kenmerkinvoertypen
description: Leer over de inputtypes beschikbaar voor productattributen, die het type van gegevens bepalen die kunnen worden ingegaan en het formaat van het gebied of de inputcontrole.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Kenmerkinvoertypen

Wanneer u kenmerken weergeeft vanuit de beheerfunctie, zijn deze de velden die u invult wanneer u een product maakt. Het invoertype dat aan een attribuut wordt toegewezen bepaalt het type van gegevens dat kan worden ingegaan en het formaat van het gebied of de inputcontrole. Vanuit het standpunt van de klant, verstrekken de attributen informatie over het product, en zijn de opties en de gebieden van de gegevensingang die moeten worden voltooid om een product te kopen.

## Invoertypen

| Eigenschap | Beschrijving |
|--- |--- |
| [!UICONTROL Text Field] | Een invoerveld bestaande uit één regel voor tekst. |
| [!UICONTROL Text Area] | Een invoerveld met meerdere regels voor het invoeren van tekstalinea&#39;s, zoals een productbeschrijving. Met de WYSIWYG Editor kunt u de tekst opmaken met HTML-tags of de tags rechtstreeks in de tekst invoeren. |
| [!UICONTROL Text Editor] | Een volledig werkende tekstredacteur bij de attributenplaats. |
| [!UICONTROL Date] | Toont een datumwaarde in het [ aangewezen formaat ](#date-and-time-options) en [ tijdzone ](../getting-started/store-details.md#locale-options). De waarden van de datum kunnen van een lijst of een kalender ( ![ pictogram van de Kalender ](../assets/icon-calendar.png) worden geselecteerd). <br/><br/>**_Nota:_**afhankelijk van uw systeemconfiguratie,_ Admin _de gebruikers kunnen data in een gebied direct ingaan of een datum van de kalender of de lijst selecteren. Voor informatie over het specificeren van datum en tijdwaarden, zie [ Datum en tijdopties ](#date-and-time-options). |
| [!UICONTROL Date and Time] | Toont een datum en tijdwaarde in het [ aangewezen formaat ](#date-and-time-options) en [ tijdzone ](../getting-started/store-details.md#locale-options). De datum en tijd kunnen handmatig worden ingevoerd of vanuit een kalender worden geselecteerd. Voorbeeld: MM/DD/YYYY HH:MM |
| [!UICONTROL Yes/No] | Hiermee geeft u een vervolgkeuzelijst weer met vooraf gedefinieerde opties `Yes` en `No` . |
| Vervolgkeuzelijst | Hiermee wordt een vervolgkeuzelijst met waarden weergegeven waarin slechts één selectie wordt geaccepteerd. Het Dropdown inputtype is een zeer belangrijke component van [ configureerbare producten ](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Hiermee geeft u een vervolgkeuzelijst weer met waarden die meerdere selecties accepteren. |
| [!UICONTROL Price] | Dit invoertype wordt gebruikt om prijsvelden te maken die naast de vooraf gedefinieerde kenmerken staan: `Price`, `Special Price`, `Tier Price` en `Cost` . De gebruikte valuta wordt bepaald door uw systeemconfiguratie. |
| [!UICONTROL Media Image] | Hiermee wordt een extra afbeelding aan een product gekoppeld, zoals een productlogo, zorginstructies of ingrediënten uit een voedseletiket. Wanneer u een kenmerk van een mediaafbeelding toevoegt aan de kenmerkset van een product, wordt dit een extra afbeeldingstype, samen met Basis, Klein en Miniatuur. Het media beeldattribuut kan van [ storefront media browser ](catalog-images-video.md#storefront-media-browser) worden uitgesloten. |
| [!UICONTROL Fixed Product Tax] | Laat u [ tarieven van FPT ](../stores-purchase/fixed-product-tax.md) bepalen die op de vereisten van uw scène worden gebaseerd. |
| [!UICONTROL Visual Swatch] | Hiermee geeft u een staal weer met de kleur, structuur of patroon van een configureerbaar product. A [ het visuele monster ](swatches.md) kan met een hexadecimale kleurenwaarde worden gevuld, of een geupload beeld tonen dat de kleur, het materiaal, de textuur, of het patroon van de optie vertegenwoordigt. |
| [!UICONTROL Text Swatch] | Een op tekst gebaseerde representatie van een configureerbare productoptie die vaak voor de grootte wordt gebruikt. [ de stalen van de Tekst ](swatches.md) kunnen hexadecimale kleurenwaarden ook omvatten. |
| [!UICONTROL Page Builder] | Een [[!DNL Page Builder]](../page-builder/workspace.md) -werkruimte op de kenmerklocatie waarmee u eenvoudig aansprekende inhoud aan de productpagina kunt toevoegen. |

{style="table-layout:auto"}

## Datum- en tijdopties

U kunt de opmaak van datum- en tijdvelden aanpassen en het invoerbesturingselement selecteren dat wordt gebruikt voor gegevensinvoer. Datumwaarden kunnen worden geselecteerd in een vervolgkeuzelijst of in een pop-upkalender.

![ Voorbeeld - storefront popup kalender ](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_aan formaatdatum/tijdgebieden:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw **[!UICONTROL Catalog]** uit in het linkerdeelvenster en klik op het subitem **[!UICONTROL Catalog]** .

1. Vouw de sectie **[!UICONTROL Date & Time Custom Options]** uit.

   ![ configuratie van de Catalogus - datum en tijdopties ](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze opties, zie [_Opties van de Douane van de Datum &amp; van de Tijd_](../configuration-reference/catalog/catalog.md) in de _Verwijzing van de Configuratie_.

1. Als u een pop-upkalender wilt gebruiken als invoerbesturingselement voor datumvelden, stelt u **[!UICONTROL Use JavaScript Calendar]** in op `Yes` .

1. Stel de volgorde van elk deel van het datumveld zo nodig in om de **[!UICONTROL Date Fields Order]** in te stellen:

   - Maand
   - Dag
   - Jaar

1. Om uw aangewezen tijdformaat te plaatsen, plaats **Formaat van de Tijd** aan één van het volgende:

   - `12h AM/PM`
   - `24h`

1. Als u de waarde **[!UICONTROL Year Range]** voor de vervolgkeuzelijst wilt instellen, voert u het jaar (JJJJ) in waarin u de datums **[!UICONTROL from]** en **[!UICONTROL to]** wilt instellen.

   Indien leeg, wordt het veld standaard ingesteld op het huidige jaar.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
