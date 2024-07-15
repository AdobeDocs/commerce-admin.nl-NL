---
title: Adreskenmerken van klant
description: Leer over de attributen van het klantenadres en hoe te om deze attributeneigenschappen te vormen.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Adreskenmerken van klant

{{ee-feature}}

De de kenmerkenreeks van het Adres van de Klant bepaalt de eigenschappen van straatadressen die in het [ adresboek ](account-dashboard-address-book.md) van de rekening van de klant of tijdens [ controle ](../stores-purchase/checkout-process.md) zijn ingegaan.

De het adresattributen van de douane kunnen opstelling zijn om extra informatie, zoals een facultatief e-mailadres, de rekening van Skype, afwisselend telefoonaantal, gebouw, of graafschap te verstrekken. Het douaneattribuut kan dan in het [ adresmalplaatje ](address-templates.md) worden opgenomen dat wordt gebruikt om verkoopdocumenten te produceren. Het proces om een attribuut van het douaneadres tot stand te brengen is bijna het zelfde als het creëren van a [ klantenattributen ](attribute-properties.md).

De adreskenmerken van de klant worden in de volgende formulieren gebruikt:

- [Klantadresregistratie](account-create.md)
- [Adres van klantenaccount](account-dashboard-address-book.md)

![ Admin - de adresattributen van de Klant ](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Stap 1: Voltooi de kenmerkeigenschappen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Attribute]** .

   ![ de attributeneigenschappen van de Klant ](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Ga als volgt te werk in de sectie **[!UICONTROL Attribute Properties]** :

   - Voer een **[!UICONTROL Default Label]** in die het kenmerk tijdens de gegevensinvoer identificeert.

   - Voer een **[!UICONTROL Attribute Code]** in die het kenmerk binnen het systeem identificeert.

     De kenmerkcode moet met een letter beginnen en kan elke combinatie van kleine letters (a-z) en cijfers (0-9) bevatten. De code moet uit minder dan 30 tekens bestaan en mag geen speciale tekens of spaties bevatten. Het onderstrepingsteken (_) kan worden gebruikt om een spatie aan te geven.

     >[!TIP]
     >
     >**_Kortere weg:_** om slechts de vereiste gebieden te voltooien, scrol neer aan [!UICONTROL Storefront Properties], ga [!UICONTROL Sort Order] in, en bewaar.

1. Stel **[!UICONTROL Input Type]** in op een van de volgende opties om het type invoerbesturingselement te bepalen dat wordt gebruikt voor gegevensinvoer:

   - `Text Field` - Een tekstveld met één regel.
   - `Text Area` - Een tekstgebied met meerdere regels.
   - `Multiple Line` - Maakt meerdere tekstregels voor het kenmerk, vergelijkbaar met een adres voor meerdere regels. Het aantal afzonderlijke gegevensinvoerregels kan tussen 2 en 20 liggen. Gebruik `Default Value` om de beginwaarde van het veld op te geven.
   - `Date` - Geeft een datumveld met een pop-upkalender weer. Aanvullende eigenschappen: gebruik `Default Value` om de beginwaarde van het veld op te geven. <br/> Gebruik `Minimal Value` om de vroegste datum te specificeren die kan worden ingegaan.  Gebruik `Maximum Value` om de laatste datum op te geven die kan worden ingevoerd.
   - `Dropdown` - Een vervolgkeuzelijst waarin slechts één waarde kan worden geselecteerd.
   - `Multiple Select` - Een vervolgkeuzelijst waarin meerdere waarden kunnen worden geselecteerd.
   - `Yes/No` - Een veld dat alleen een keuze uit `Yes` - of `No` -waarden biedt.
   - `File (attachment)` - Een veld waarmee een bestand kan worden geüpload en dat aan het kenmerk customer als bijlage kan worden gekoppeld.
   - `Image File` - Een veld waarmee een afbeelding naar de galerie kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant.

1. Als de klant een waarde in het veld moet invoeren, stelt u **[!UICONTROL Values Required]** in op `Yes` .

1. Voer een **[!UICONTROL Default Value]** in om een beginwaarde aan het veld toe te wijzen.

1. Als u wilt controleren of de gegevens die in het veld zijn ingevoerd correct zijn voordat de record wordt opgeslagen, stelt u **[!UICONTROL Input Validation]** in op het type gegevens dat in het veld is toegestaan. De beschikbare waarden zijn afhankelijk van de opgegeven _[!UICONTROL Input Type]_.

   - `None` - Het veld heeft geen invoervalidatie tijdens het invoeren van gegevens.
   - `Alphanumeric` - Accepteert elke combinatie van getallen (0-9) en alfabetische tekens (a-z, A-Z) tijdens de gegevensinvoer. Zie [!UICONTROL Escape HTML Entities] in de volgende stap als u speciale tekens wilt opnemen.
   - `Alphanumeric with Space` - Accepteert elke combinatie van getallen (0-9), alfabetische tekens (a-z, A-Z) en spaties tijdens de gegevensinvoer.
   - `Numeric Only` - Accepteert alleen getallen (0-9) tijdens gegevensinvoer.
   - `Alpha Only` - Accepteert alleen alfabetische tekens (a-z, A-Z) tijdens gegevensinvoer.
   - `URL` - Accepteert alleen een URL tijdens gegevensinvoer.
   - `Email` - Accepteert alleen een e-mailadres tijdens gegevensinvoer.
   - `Length Only` - Valideert de invoer op basis van de lengte van de gegevens die in het veld zijn ingevoerd.

1. Als u een voorbewerkingsfilter wilt toepassen op waarden die zijn ingevoerd in een tekstveld, tekstgebied of invoertype voor meerdere regels, stelt u **[!UICONTROL Input/Output Filter]** in op een van de volgende opties:

   - `None` - Hiermee wordt geen filter toegepast op tekst die in het veld wordt ingevoerd.
   - `Strip HTML Tags` - Hiermee verwijdert u HTML-tags uit de tekst. Met dit filter kunt u gegevens opschonen die in een veld worden geplakt vanuit een andere bron die HTML-tags bevat.
   - `Escape  HTML Entities` - Hiermee converteert u speciale tekens uit de tekst naar een geldige HTML-escapereeks, zoals `&;` . Escape-reeksen staan tussen een ampersand en een puntkomma en worden vaak gebruikt voor slimme aanhalingstekens, copyright en handelsmerken van typografische tekens. Escape-reeksen worden ook gebruikt om tekens zoals de symbolen kleiner dan (`<`) en groter dan (`>` ) te identificeren, en het ampersand-teken dat ook in de code wordt gebruikt. Met dit filter kunt u speciale tekens opschonen die soms door tekstverwerkers in databasevelden worden geplakt.

1. Voltooi het klantennet en segmenteigenschappen:

   - Stel **[!UICONTROL Add to Column Options]** in op `Yes` als u de kolom in het raster Klanten wilt opnemen.

   - Als u het raster Klanten met dit kenmerk wilt filteren, stelt u **[!UICONTROL Use in Filter Options]** in op `Yes` .

   - Als u het raster Klanten wilt filteren op tekstkenmerk met verschillende filterovereenkomende voorwaarden, stelt u **[!UICONTROL Grid Filter Condition Type]** in op `Partial Match` , `Prefix Match` of `Full Match` . Het beïnvloedt niet het _Onderzoek door sleutelwoord_ gebied voor het net.

   - Als u het raster Klanten op dit kenmerk wilt doorzoeken, stelt u **[!UICONTROL Use in Search Options]** in op `Yes` .

   - Om dit attribuut beschikbaar te maken aan [ klantensegmenten ](customer-segments.md), plaats **[!UICONTROL Use in Customer Segment]** aan `Yes`.

## Stap 2: Voltooi de storefront-eigenschappen

1. Schuif omlaag naar de sectie **[!UICONTROL Storefront Properties]** .

   ![ het adresattributen van de Klant - eigenschappen van de Storefront ](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Als u het kenmerk zichtbaar wilt maken voor klanten, stelt u **[!UICONTROL Show on Storefront]** in op `Yes` .

1. Voer in het veld **[!UICONTROL Sort Order]** een getal in dat de weergavevolgorde bepaalt wanneer andere kenmerken worden weergegeven.

1. Stel **[!UICONTROL Forms to Use]** in op elk formulier dat het kenmerk moet bevatten.

   Als u beide opties wilt kiezen, houdt u Ctrl (PC) of Command (Mac) ingedrukt terwijl u op elk formulier klikt.

   - [Registratie van adres klant](account-create.md)
   - [Adres van klant](account-dashboard-address-book.md)

## Stap 3: Voltooi het label en sla het op

1. Kies **[!UICONTROL Manage Labels/Options]** in het deelvenster aan de linkerkant.

1. Onder **[!UICONTROL Manage Titles]**, ga een etiket in om de attributen voor elke [ opslagmening ](../getting-started/websites-stores-views.md) te identificeren.

1. Klik op **[!UICONTROL Save Attribute]** als de bewerking is voltooid.

   ![ het adresattributen van de Klant - etiketten/opties ](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Veldomschrijvingen

### [!UICONTROL Attribute Properties]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Default Label] | Het standaardlabel dat het kenmerk in Admin en storefront identificeert. |
| [!UICONTROL Attribute Code] | Een unieke code die het kenmerk binnen het systeem identificeert. De code kan maximaal 21 tekens lang zijn en mag geen spaties of speciale tekens bevatten. U kunt het onderstrepingsteken gebruiken in plaats van een spatie. |
| [!UICONTROL Input Type] | Bepaalt de [ inputcontrole ](../catalog/attributes-input-types.md) die voor gegevensingang wordt gebruikt. Opties: <br/>**`Text Field`**- Een tekstveld met één regel.<br/>**`Text Area`** - Een tekstgebied met meerdere regels. <br/>**`Multiple Line`**- Maakt meerdere tekstregels voor het kenmerk, vergelijkbaar met een adres voor meerdere regels. Het aantal afzonderlijke gegevensinvoerregels kan tussen 2 en 20 liggen.<br/>**`Date`** - Geeft een datumveld met een pop-upkalender weer.<br/>**`Dropdown`**- Een vervolgkeuzelijst waarin slechts één waarde kan worden geselecteerd.<br/>**`Multiple Select`** - Een vervolgkeuzelijst waarin meerdere waarden kunnen worden geselecteerd. <br/>**`Yes/No`**- Een veld dat alleen een keuze uit `Yes` - of `No` -waarden biedt.<br/>**`File (attachment)`** - Een veld waarmee een bestand kan worden geüpload en dat aan het kenmerk customer als bijlage kan worden gekoppeld. <br/>**`Image File`**- Een veld waarmee een afbeelding naar de galerie kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant. |
| [!UICONTROL Values Required] | Hiermee wordt bepaald of een waarde in het veld moet worden ingevoerd. Opties: `Yes` / `No` |
| [!UICONTROL Default Value] | Specifies the initial value of the attribute. |
| [!UICONTROL Input Validation] | De selectie van opties wordt bepaald door het invoertype. Opties: <br/>**`None`**- Het veld heeft geen invoervalidatie tijdens het invoeren van gegevens.<br/>**`Alphanumeric`** - Accepteert elke combinatie van getallen (0-9) en alfabetische tekens (a-z, A-Z) tijdens de gegevensinvoer. <br/>**`Alphanumeric with Space`**- Hiermee kunnen spaties in het adres van de straat voldoen aan de maximale lengtevereisten van de vervoerder. Tijdens het afrekenen, kan de klant om het even welke combinatie aantallen (0-9), alfabetische karakters (a-z, A-Z), en ruimten in het straatadres van de ontvanger en de afzender ingaan. Eventuele extra spaties worden bijgesneden wanneer het adres wordt opgeslagen.<br/>**`Numeric Only`** - Accepteert alleen getallen (0-9) tijdens gegevensinvoer. <br/>**`Alpha Only`**- Accepteert alleen alfabetische tekens (a-z, A-Z) tijdens gegevensinvoer.<br/>** URL **- keurt slechts een URL tijdens gegevensingang goed.<br/>**`Email`** - Accepteert alleen een e-mailadres tijdens gegevensinvoer. <br/>**`Length Only`**- Valideert de invoer op basis van de lengte van de gegevens die in het veld zijn ingevoerd. |
| [!UICONTROL Input/Output Filter] | Hiermee past u een voorbewerkingsfilter toe op waarden die zijn ingevoerd in een tekstveld, tekstgebied of invoertype voor meerdere regels voordat de record wordt opgeslagen. Opties: <br/>**`None`**- past geen filter toe op tekst die in het veld wordt ingevoerd.<br/>**`Strip HTML Tags`** - Hiermee verwijdert u HTML-tags uit de tekst. Met dit filter kunt u gegevens opschonen die in een veld worden geplakt vanuit een andere bron die HTML-tags bevat. <br/>**`Escape HTML Entities`**- Hiermee converteert u speciale tekens uit de tekst naar een geldige HTML-escapereeks, zoals `amp;` . Escape-reeksen worden ingesloten tussen een ampersand en een puntkomma en worden vaak gebruikt voor slimme aanhalingstekens, copyrightsymbolen en handelsmerken van typografische tekens. Escape-reeksen worden ook gebruikt om tekens zoals de symbolen kleiner dan (`<`) en groter dan (`>` ) te identificeren, en het ampersand-teken dat ook in de code wordt gebruikt. Met dit filter kunt u speciale tekens opschonen die soms door tekstverwerkers in databasevelden worden geplakt. |
| [!UICONTROL Add to Column Options] | Specificeert als het attribuut als kolom in het [ net van Klanten ](./customers-all.md) inbegrepen is. Opties: `Yes` / `No` |
| Gebruiken in filteropties | Geeft aan of het kenmerk kan worden gebruikt als filter voor zoekbewerkingen vanuit het raster. Opties: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Geeft filterovereenkomende voorwaarden voor kenmerken in zoekbewerkingen op vanuit het raster. Het heeft geen invloed op het veld _[!UICONTROL Search by keyword]_voor het raster. Opties: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Geeft aan of de kenmerkwaarde kan worden gebruikt als een trefwoord in zoekbewerkingen. Opties: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Bepaalt als het attribuut in [ klantensegment ](./customer-segments.md) voorwaarden inbegrepen is. Opties: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Show on Storefront] | Hiermee bepaalt u of het kenmerk wordt weergegeven als een veld in de klantgegevens in de winkelbrowser. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Geeft de sorteervolgorde van dit kenmerk ten opzichte van andere klantkenmerken aan. De sorteervolgorde bepaalt de volgorde waarin velden focus krijgen tijdens het invoeren van gegevens wanneer toetsenbordnavigatie wordt gebruikt. |
| [!UICONTROL Forms to Use in] | Hiermee bepaalt u de pagina&#39;s met gegevensinvoerformulieren waarop het kenmerk wordt weergegeven. Opties: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
