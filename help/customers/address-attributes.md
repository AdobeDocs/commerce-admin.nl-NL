---
title: Adreskenmerken van klant
description: Leer over de attributen van het klantenadres en hoe te om deze attributeneigenschappen te vormen.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# Adreskenmerken van klant

{{ee-feature}}

De de kenmerkenreeks van het Adres van de Klant bepaalt de eigenschappen van straatadressen die in de [adresboek](account-dashboard-address-book.md) van de rekening van de klant of tijdens [uitchecken](../stores-purchase/checkout-process.md).

De het adresattributen van de douane kunnen opstelling zijn om extra informatie, zoals een facultatief e-mailadres, de rekening van Skype, afwisselend telefoonaantal, gebouw, of graafschap te verstrekken. Het aangepaste kenmerk kan vervolgens worden opgenomen in het [adressjabloon](address-templates.md) die wordt gebruikt voor het opstellen van verkoopdocumenten. Het proces om een attribuut van het douaneadres tot stand te brengen is bijna het zelfde als het creëren van [klantkenmerk](attribute-properties.md).

De adreskenmerken van de klant worden in de volgende formulieren gebruikt:

- [Klantadresregistratie](account-create.md)
- [Adres van klantenaccount](account-dashboard-address-book.md)

![Beheerder - Adreskenmerken van klant](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Stap 1: Voltooi de kenmerkeigenschappen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Attribute]**.

   ![Eigenschappen van klantkenmerken](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. In de **[!UICONTROL Attribute Properties]** Ga als volgt te werk:

   - Voer een **[!UICONTROL Default Label]** die het kenmerk tijdens de gegevensinvoer identificeert.

   - Voer een **[!UICONTROL Attribute Code]** die het kenmerk binnen het systeem identificeert.

     De kenmerkcode moet met een letter beginnen en kan elke combinatie van kleine letters (a-z) en cijfers (0-9) bevatten. De code moet uit minder dan 30 tekens bestaan en mag geen speciale tekens of spaties bevatten. Het onderstrepingsteken (_) kan worden gebruikt om een spatie aan te geven.

     >[!TIP]
     >
     >**_Sneltoets:_** Als u alleen de vereiste velden wilt voltooien, schuift u omlaag naar [!UICONTROL Storefront Properties], voert u de [!UICONTROL Sort Order]en opslaan.

1. Om het type van inputcontrole te bepalen dat voor gegevensingang wordt gebruikt, reeks **[!UICONTROL Input Type]** op een van de volgende wijzen:

   - `Text Field` - Een tekstveld met één regel.
   - `Text Area` - Een tekstgebied met meerdere regels.
   - `Multiple Line` - Hiermee maakt u meerdere tekstregels voor het kenmerk, vergelijkbaar met een adres voor meerdere regels. Het aantal afzonderlijke gegevensinvoerregels kan tussen 2 en 20 liggen. Gebruik de `Default Value` om de beginwaarde van het veld op te geven.
   - `Date` - Geeft een datumveld met een pop-upkalender weer. Aanvullende eigenschappen: gebruiken `Default Value` om de beginwaarde van het veld op te geven. <br/>Gebruiken `Minimal Value` om de vroegste datum te specificeren die kan worden ingegaan.  Gebruiken `Maximum Value` om de uiterste datum te specificeren die kan worden ingegaan.
   - `Dropdown` - Een vervolgkeuzelijst waarin slechts één waarde kan worden geselecteerd.
   - `Multiple Select` - Een vervolgkeuzelijst waarin meerdere waarden kunnen worden geselecteerd.
   - `Yes/No` - Een veld dat alleen een keuze biedt `Yes` of `No` waarden.
   - `File (attachment)` - Een veld waarin een bestand kan worden geüpload en dat als bijlage aan het kenmerk customer kan worden gekoppeld.
   - `Image File` - Een veld waarmee een afbeelding naar de galerie kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant.

1. Als de klant een waarde in het veld moet invoeren, stelt u **[!UICONTROL Values Required]** tot `Yes`.

1. Als u een initiële waarde aan het veld wilt toewijzen, voert u een **[!UICONTROL Default Value]**.

1. Als u wilt controleren of de gegevens die in het veld zijn ingevoerd correct zijn voordat de record wordt opgeslagen, stelt u **[!UICONTROL Input Validation]** op het type gegevens dat in het veld is toegestaan. De beschikbare waarden zijn afhankelijk van de _[!UICONTROL Input Type]_opgegeven.

   - `None` - Het veld heeft geen invoervalidatie tijdens het invoeren van gegevens.
   - `Alphanumeric` - Accepteert elke combinatie van getallen (0-9) en alfabetische tekens (a-z, A-Z) tijdens de gegevensinvoer. Als u speciale tekens wilt opnemen, raadpleegt u [!UICONTROL Escape HTML Entities] in de volgende stap.
   - `Alphanumeric with Space` - Accepteert elke combinatie van getallen (0-9), alfabetische tekens (a-z, A-Z) en spaties tijdens gegevensinvoer.
   - `Numeric Only` - Accepteert alleen getallen (0-9) tijdens gegevensinvoer.
   - `Alpha Only` - Accepteert alleen alfabetische tekens (a-z, A-Z) tijdens gegevensinvoer.
   - `URL` - Accepteert alleen een URL tijdens gegevensinvoer.
   - `Email` - Accepteert alleen een e-mailadres bij het invoeren van gegevens.
   - `Length Only` - Valideert de invoer op basis van de lengte van de gegevens die in het veld zijn ingevoerd.

1. Als u een voorbewerkingsfilter wilt toepassen op waarden die zijn ingevoerd in een tekstveld, tekstgebied of invoertype voor meerdere regels, stelt u **[!UICONTROL Input/Output Filter]** op een van de volgende wijzen:

   - `None` - Hiermee wordt geen filter toegepast op tekst die in het veld wordt ingevoerd.
   - `Strip HTML Tags` - Hiermee verwijdert u HTML-tags uit de tekst. Met dit filter kunt u gegevens opschonen die in een veld worden geplakt vanuit een andere bron die HTML-tags bevat.
   - `Escape  HTML Entities`  - Hiermee worden speciale tekens in de tekst omgezet in een geldige HTML-escapereeks, zoals `&;`. Escape-reeksen staan tussen een ampersand en een puntkomma en worden vaak gebruikt voor slimme aanhalingstekens, copyright en handelsmerken van typografische tekens. Escape-reeksen worden ook gebruikt om tekens zoals de tekst kleiner dan (`<`) en groter dan (`>`) en het ampersand-teken dat ook in de code wordt gebruikt. Met dit filter kunt u speciale tekens opschonen die soms door tekstverwerkers in databasevelden worden geplakt.

1. Voltooi het klantennet en segmenteigenschappen:

   - Als u de kolom wilt opnemen in het raster Klanten, stelt u **[!UICONTROL Add to Column Options]** tot `Yes`.

   - Als u het raster Klanten op dit kenmerk wilt filteren, stelt u **[!UICONTROL Use in Filter Options]** tot `Yes`.

   - Als u het raster Klanten op tekstkenmerk wilt filteren met verschillende filterovereenkomende voorwaarden, stelt u **[!UICONTROL Grid Filter Condition Type]** tot `Partial Match`, `Prefix Match`, of `Full Match`. Het heeft geen invloed op de _Zoeken op trefwoord_ veld voor het raster.

   - Als u het raster Klanten op dit kenmerk wilt doorzoeken, stelt u **[!UICONTROL Use in Search Options]** tot `Yes`.

   - Om dit kenmerk beschikbaar te maken voor [klantsegmenten](customer-segments.md), set **[!UICONTROL Use in Customer Segment]** tot `Yes`.

## Stap 2: Voltooi de storefront-eigenschappen

1. Omlaag schuiven naar de **[!UICONTROL Storefront Properties]** sectie.

   ![Adreskenmerken van klant - Eigenschappen van winkel](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Als u het kenmerk zichtbaar wilt maken voor klanten, stelt u **[!UICONTROL Show on Storefront]** tot `Yes`.

1. Voer een getal in het dialoogvenster **[!UICONTROL Sort Order]** veld, dat de weergavevolgorde bepaalt wanneer deze met andere kenmerken wordt weergegeven.

1. Set **[!UICONTROL Forms to Use]** op elk formulier dat het kenmerk moet bevatten.

   Als u beide opties wilt kiezen, houdt u Ctrl (PC) of Command (Mac) ingedrukt terwijl u op elk formulier klikt.

   - [Registratie van adres klant](account-create.md)
   - [Adres van klant](account-dashboard-address-book.md)

## Stap 3: Voltooi het label en sla het op

1. Kies in het deelvenster aan de linkerkant de optie **[!UICONTROL Manage Labels/Options]**.

1. Onder **[!UICONTROL Manage Titles]** Voer een label in om het kenmerk voor elke [winkelweergave](../getting-started/websites-stores-views.md).

1. Klik op **[!UICONTROL Save Attribute]**.

   ![Adreskenmerken van de klant - labels/opties](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Veldomschrijvingen

### [!UICONTROL Attribute Properties]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Default Label] | Het standaardlabel dat het kenmerk in Admin en storefront identificeert. |
| [!UICONTROL Attribute Code] | Een unieke code die het kenmerk binnen het systeem identificeert. De code kan maximaal 21 tekens lang zijn en mag geen spaties of speciale tekens bevatten. U kunt het onderstrepingsteken gebruiken in plaats van een spatie. |
| [!UICONTROL Input Type] | Hiermee bepaalt u de [invoerbesturingselement](../catalog/attributes-input-types.md) die wordt gebruikt voor gegevensinvoer. Opties: <br/>**`Text Field`**- Een tekstveld met één regel.<br/>**`Text Area`** - Een tekstgebied met meerdere regels. <br/>**`Multiple Line`**- Hiermee maakt u meerdere tekstregels voor het kenmerk, vergelijkbaar met een adres voor meerdere regels. Het aantal afzonderlijke gegevensinvoerregels kan tussen 2 en 20 liggen.<br/>**`Date`** - Geeft een datumveld met een pop-upkalender weer.<br/>**`Dropdown`**- Een vervolgkeuzelijst waarin slechts één waarde kan worden geselecteerd.<br/>**`Multiple Select`** - Een vervolgkeuzelijst waarin meerdere waarden kunnen worden geselecteerd. <br/>**`Yes/No`**- Een veld dat alleen een keuze biedt `Yes` of `No` waarden.<br/>**`File (attachment)`** - Een veld waarin een bestand kan worden geüpload en dat als bijlage aan het kenmerk customer kan worden gekoppeld. <br/>**`Image File`**- Een veld waarmee een afbeelding naar de galerie kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant. |
| [!UICONTROL Values Required] | Hiermee wordt bepaald of een waarde in het veld moet worden ingevoerd. Opties: `Yes` / `No` |
| [!UICONTROL Default Value] | Specifies the initial value of the attribute. |
| [!UICONTROL Input Validation] | De selectie van opties wordt bepaald door het invoertype. Opties: <br/>**`None`**- Het veld heeft geen invoervalidatie tijdens het invoeren van gegevens.<br/>**`Alphanumeric`** - Accepteert elke combinatie van getallen (0-9) en alfabetische tekens (a-z, A-Z) tijdens de gegevensinvoer. <br/>**`Alphanumeric with Space`**- Hiermee kunnen spaties op het adres van de straat voldoen aan de maximale lengtevereisten van de vervoerder. Tijdens het afrekenen, kan de klant om het even welke combinatie aantallen (0-9), alfabetische karakters (a-z, A-Z), en ruimten in het straatadres van de ontvanger en de afzender ingaan. Eventuele extra spaties worden bijgesneden wanneer het adres wordt opgeslagen.<br/>**`Numeric Only`** - Accepteert alleen getallen (0-9) tijdens gegevensinvoer. <br/>**`Alpha Only`**- Accepteert alleen alfabetische tekens (a-z, A-Z) tijdens gegevensinvoer.<br/>** URL **- Accepteert alleen een URL tijdens gegevensinvoer.<br/>**`Email`** - Accepteert alleen een e-mailadres bij het invoeren van gegevens. <br/>**`Length Only`**- Valideert de invoer op basis van de lengte van de gegevens die in het veld zijn ingevoerd. |
| [!UICONTROL Input/Output Filter] | Hiermee past u een voorbewerkingsfilter toe op waarden die zijn ingevoerd in een tekstveld, tekstgebied of invoertype voor meerdere regels voordat de record wordt opgeslagen. Opties: <br/>**`None`**- Hiermee wordt geen filter toegepast op tekst die in het veld wordt ingevoerd.<br/>**`Strip HTML Tags`** - Hiermee verwijdert u HTML-tags uit de tekst. Met dit filter kunt u gegevens opschonen die in een veld worden geplakt vanuit een andere bron die HTML-tags bevat. <br/>**`Escape HTML Entities`**- Hiermee worden speciale tekens in de tekst omgezet in een geldige HTML-escapereeks, zoals `amp;`. Escape-reeksen worden ingesloten tussen een ampersand en een puntkomma en worden vaak gebruikt voor slimme aanhalingstekens, copyrightsymbolen en handelsmerken van typografische tekens. Escape-reeksen worden ook gebruikt om tekens zoals de tekst kleiner dan (`<`) en groter dan (`>`) en het ampersand-teken dat ook in de code wordt gebruikt. Met dit filter kunt u speciale tekens opschonen die soms door tekstverwerkers in databasevelden worden geplakt. |
| [!UICONTROL Add to Column Options] | Hiermee wordt opgegeven of het kenmerk wordt opgenomen als een kolom in het dialoogvenster [Klanten](./customers-all.md) raster. Opties: `Yes` / `No` |
| Gebruiken in filteropties | Geeft aan of het kenmerk kan worden gebruikt als filter voor zoekbewerkingen vanuit het raster. Opties: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Geeft filterovereenkomende voorwaarden voor kenmerken in zoekbewerkingen op vanuit het raster. Het heeft geen invloed op de _[!UICONTROL Search by keyword]_veld voor het raster. Opties: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Geeft aan of de kenmerkwaarde kan worden gebruikt als een trefwoord in zoekbewerkingen. Opties: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Hiermee wordt bepaald of het kenmerk is opgenomen in [klantensegment](./customer-segments.md) voorwaarden. Opties: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Show on Storefront] | Hiermee bepaalt u of het kenmerk wordt weergegeven als een veld in de klantgegevens in de winkelbrowser. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Geeft de sorteervolgorde van dit kenmerk ten opzichte van andere klantkenmerken aan. De sorteervolgorde bepaalt de volgorde waarin velden focus krijgen tijdens het invoeren van gegevens wanneer toetsenbordnavigatie wordt gebruikt. |
| [!UICONTROL Forms to Use in] | Hiermee bepaalt u de pagina&#39;s met gegevensinvoerformulieren waarop het kenmerk wordt weergegeven. Opties: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
