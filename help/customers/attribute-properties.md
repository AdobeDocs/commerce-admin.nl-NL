---
title: Eigenschappen van klantkenmerken
description: Leer hoe te om de eigenschappen van klantenattributen te vormen.
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1774'
ht-degree: 0%

---

# Eigenschappen van klantkenmerken

{{ee-feature}}

De attributen van de klant verstrekken de informatie die wordt vereist om de orde, naleving, en de processen van het klantenbeheer te steunen. Omdat uw zaken uniek zijn, zou u gebieden naast de standaardpunten kunnen nodig hebben die door het systeem worden verstrekt. U kunt aangepaste kenmerken toevoegen aan de gedeelten Accountinformatie, Adresboek en Factureringsgegevens van de account van de klant. Klant [adreskenmerken](address-attributes.md) kan ook worden gebruikt in de _Factuurgegevens_ -gedeelte tijdens afrekenen of wanneer gasten zich registreren voor een account.

![Klantkenmerken](./assets/attributes-customer.png){width="700" zoomable="yes"}

## Stap 1: Voltooi de eigenschappen van het kenmerk

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Attribute]**.

   ![Eigenschappen van klantkenmerken](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. In de **[!UICONTROL Attribute Properties]** Ga als volgt te werk:

   - Voer een **[!UICONTROL Default Label]** die het kenmerk tijdens de gegevensinvoer identificeert.

   - Voer een **[!UICONTROL Attribute Code]** die het kenmerk binnen het systeem identificeert.

   De kenmerkcode moet met een letter beginnen en kan elke combinatie van kleine letters (a-z) en cijfers (0-9) bevatten. De code moet uit minder dan 30 tekens bestaan en mag geen speciale tekens of spaties bevatten. Het onderstrepingsteken (`_`) kan worden gebruikt om een spatie aan te geven.

   >[!TIP]
   >
   >**Sneltoets:** Als u alleen de vereiste velden wilt voltooien, schuift u omlaag naar _[!UICONTROL Storefront Properties]_, voert u de_[!UICONTROL Sort Order]_ en opslaan.

1. Vul de eigenschappen van gegevensinvoer in:

   - Om het type van inputcontrole te bepalen dat voor gegevensingang wordt gebruikt, reeks **[!UICONTROL Input Type]** op een van de volgende wijzen:

     | Type | Beschrijving |
     |----|-----------|
     | `Text Field` | Een tekstveld met één regel. |
     | `Text Area` | Een invoerveld met meerdere regels voor het invoeren van tekstalinea&#39;s, zoals een productbeschrijving. U kunt de redacteur WYSIWYG gebruiken om de tekst met markeringen van HTML te formatteren, of de markeringen direct in de tekst in te gaan. |
     | `Multiple Line` | Hiermee maakt u meerdere tekstregels voor het kenmerk, vergelijkbaar met een adres voor meerdere regels. Het aantal afzonderlijke gegevensinvoerregels kan tussen twee en twintig liggen. Gebruik de `Default Value` om de beginwaarde van het veld op te geven. |
     | `Date` | Hiermee geeft u een datumwaarde weer in de datumnotatie en tijdzone van de voorkeur. Datumwaarden kunnen worden geselecteerd in een lijst of kalender ( ![Kalenderpictogram](../assets/icon-calendar.png) ). <br/><br/>**_Opmerking:_**Afhankelijk van uw systeemconfiguratie,_Beheerder _gebruikers kunnen rechtstreeks datums in een veld invoeren of een datum in de kalender of lijst selecteren. Voor informatie over het specificeren van datum en tijdwaarden, zie [Datum- en tijdopties](../catalog/attributes-input-types.md#date-and-time-options). |
     | `Yes/No` | Hiermee geeft u een vervolgkeuzelijst weer met vooraf gedefinieerde opties voor `Yes` en `No`. |
     | `Dropdown` | Hiermee wordt een vervolgkeuzelijst met waarden weergegeven waarin slechts één selectie wordt geaccepteerd. Het invoertype Vervolgkeuzelijst is een sleutelcomponent van [configureerbare producten](../catalog/product-create-configurable.md). |
     | `Multiple Select` | Een vervolgkeuzelijst waarin meerdere waarden kunnen worden geselecteerd. |
     | `File (attachment)` | Een veld waarin een bestand kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant als bijlage. |
     | `Image File` | Een veld waarmee een afbeelding naar de galerie kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant. |

   - Als de klant een waarde in het veld moet invoeren, stelt u **[!UICONTROL Values Required]** tot `Yes`.

   - Als u een initiële waarde aan het veld wilt toewijzen, voert u een **[!UICONTROL Default Value]**.

   - Als u wilt controleren of de gegevens die in het veld zijn ingevoerd correct zijn voordat de record wordt opgeslagen, stelt u **[!UICONTROL Input Validation]** op het type gegevens dat in het veld is toegestaan. De beschikbare waarden zijn afhankelijk van de [!UICONTROL Input Type] opgegeven.

     | Waarde | Beschrijving |
     |-----|-----------|
     | `None` | Het veld heeft geen invoervalidatie tijdens het invoeren van gegevens. |
     | `Alphanumeric` | Accepteert elke combinatie van getallen (0-9) en alfabetische tekens (a-z, A-Z) tijdens de gegevensinvoer. Als u speciale tekens wilt opnemen, raadpleegt u _Escape HTML Entities_. |
     | `Alphanumeric with Space` | Accepteert elke combinatie van getallen (0-9), alfabetische tekens (a-z, A-Z) en spaties tijdens gegevensinvoer. |
     | `Numeric Only` | Accepteert alleen getallen (0-9) tijdens gegevensinvoer. |
     | `Alpha Only` | Accepteert alleen alfabetische tekens (a-z, A-Z) tijdens gegevensinvoer. |
     | `URL` | Accepteert alleen een URL tijdens gegevensinvoer. |
     | `Email` | Accepteert slechts een e-mailadres tijdens gegevensingang. |
     | `Length Only` | Valideert de invoer op basis van de lengte van de gegevens die in het veld zijn ingevoerd. |

   - Als u de grootte van de invoertypen voor tekstvelden en tekstgebieden wilt beperken, voert u de **[!UICONTROL Minimum Text Length]** en **[!UICONTROL Maximum Text Length]**.

   - Als u een voorbewerkingsfilter wilt toepassen op waarden die zijn ingevoerd in een tekstveld, tekstgebied of invoertype voor meerdere regels, stelt u **[!UICONTROL Input/Output Filter]** op een van de volgende wijzen:

     | Waarde | Beschrijving |
     |-----|-----------|
     | `None` | Hiermee wordt geen filter toegepast op tekst die in het veld wordt ingevoerd. |
     | `Strip HTML Tags` | Hiermee verwijdert u HTML-tags uit de tekst. Met dit filter kunt u gegevens opschonen die in een veld worden geplakt vanuit een andere bron die HTML-tags bevat. |
     | `Escape  HTML Entities` | Hiermee worden speciale tekens die in de tekst worden gevonden, omgezet in een geldige HTML escape-reeks, zoals `&;`. Escape-reeksen staan tussen een ampersand en een puntkomma en worden vaak gebruikt voor slimme aanhalingstekens, copyright en handelsmerken van typografische tekens. Escape-reeksen worden ook gebruikt om tekens zoals de tekst kleiner dan (`<`) en groter dan (`>`) en het ampersand-teken dat ook in de code wordt gebruikt. Met dit filter kunt u speciale tekens opschonen die soms door tekstverwerkers in databasevelden worden geplakt. |

1. Voltooi het klantennet en segmenteigenschappen:

   - Als u de kolom wilt opnemen in het raster Klanten, stelt u **[!UICONTROL Add to Column Options]** tot `Yes`.

   - Als u het raster Klanten op dit kenmerk wilt filteren, stelt u **[!UICONTROL Use in Filter Options]** tot `Yes`.

   - Als u het raster Klanten op tekstkenmerk wilt filteren met verschillende filterovereenkomende voorwaarden, stelt u **[!UICONTROL Grid Filter Condition Type]** tot `Partial Match`, `Prefix Match`, of `Full Match`. Het heeft geen invloed op de _Zoeken op trefwoord_  veld voor het raster.

   - Als u het raster Klanten op dit kenmerk wilt doorzoeken, stelt u **[!UICONTROL Use in Search Options]** tot `Yes`.

   - Om dit kenmerk beschikbaar te maken voor [klantsegmenten](customer-segments.md), set **[!UICONTROL Use in Customer Segment]** tot `Yes`.

## Stap 2: Voltooi de storefront-eigenschappen

1. Omlaag schuiven naar de **[!UICONTROL Storefront Properties]** sectie.

   ![Klantkenmerken - eigenschappen van winkel](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. Als u het kenmerk zichtbaar wilt maken voor klanten, stelt u **[!UICONTROL Show on Storefront]** tot `Yes`.

1. Voer een getal in het dialoogvenster **[!UICONTROL Sort Order]** veld, dat de weergavevolgorde bepaalt wanneer deze met andere kenmerken wordt weergegeven.

1. Set **[!UICONTROL Forms to Use]** op elk formulier dat het kenmerk moet bevatten. Houd Ctrl ingedrukt en klik op elk formulier om meerdere opties te kiezen.

   - [&quot;Klantenregistratie&quot;](customer-sign-in.md)
   - [Klantenaccount bewerken](account-create.md)
   - [` Admin Checkout`](../stores-purchase/checkout-process.md)

## Stap 3: Voltooi het label en sla het op

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Manage Labels/Options]**.

1. Onder **[!UICONTROL Manage Titles]** Voer een label in om het kenmerk voor elke [winkelweergave](../getting-started/websites-stores-views.md).

1. Klik op **[!UICONTROL Save Attribute]**.

   ![Kenmerken van de klant - labels/opties](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## Veldomschrijvingen

### [!UICONTROL Attribute Properties]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Default Label] | Het standaardlabel dat het kenmerk in Admin en storefront identificeert. |
| [!UICONTROL Attribute Code] | Een unieke code die het kenmerk binnen het systeem identificeert. De code kan maximaal 60 tekens lang zijn en mag geen spaties of speciale tekens bevatten. U kunt het onderstrepingsteken gebruiken in plaats van een spatie. |
| [!UICONTROL Input Type] | Bepaalt de invoercontrole die voor gegevensingang wordt gebruikt. Opties: <br/>**`Text Field`**- Een tekstveld met één regel.<br/>**`Text Area`** - Een tekstgebied met meerdere regels. <br/>**`Multiple Line`**- Hiermee maakt u meerdere tekstregels voor het kenmerk, vergelijkbaar met een adres voor meerdere regels. Het aantal afzonderlijke gegevensinvoerregels kan tussen 2 en 20 liggen.<br/>**`Date`** - Geeft een datumveld met een pop-upkalender weer.<br/>**`Dropdown`**- Een vervolgkeuzelijst waarin slechts één waarde kan worden geselecteerd.<br/>**`Multiple Select`** - Een vervolgkeuzelijst waarin meerdere waarden kunnen worden geselecteerd. <br/>**`Yes/No`**- Een veld dat alleen een keuze biedt `Yes` of `No` waarden.<br/>**`File (attachment)`** - Een veld waarin een bestand kan worden geüpload en dat als bijlage aan het kenmerk customer kan worden gekoppeld. <br/>**`Image File`**- Een veld waarmee een afbeelding naar de galerie kan worden geüpload en dat is gekoppeld aan het kenmerk van de klant. |
| [!UICONTROL Values Required] | Hiermee wordt bepaald of een waarde in het veld moet worden ingevoerd. Opties: `Yes` / `No` |
| [!UICONTROL Default Value] | Specifies the initial value of the attribute. |
| [!UICONTROL Input Validation] | De selectie van opties wordt bepaald door het invoertype. Opties: <br/>**`None`**- Het veld heeft geen invoervalidatie tijdens het invoeren van gegevens.<br/>**`Alphanumeric`** - Accepteert elke combinatie van getallen (0-9) en alfabetische tekens (a-z, A-Z) tijdens de gegevensinvoer. <br/>**`Alphanumeric with Space`**- Hiermee kunnen spaties op het adres van de straat voldoen aan de maximale lengtevereisten van de vervoerder. Tijdens het afrekenen, kan de klant om het even welke combinatie aantallen (0-9), alfabetische karakters (a-z, A-Z), en ruimten in het straatadres van de ontvanger en de afzender ingaan. Eventuele extra spaties worden bijgesneden wanneer het adres wordt opgeslagen.<br/>**`Numeric Only`** - Accepteert alleen getallen (0-9) tijdens gegevensinvoer. <br/>**`Alpha Only`**- Accepteert alleen alfabetische tekens (a-z, A-Z) tijdens gegevensinvoer.<br/>**`URL`** - Accepteert alleen een URL tijdens gegevensinvoer. <br/>**`Email`**- Accepteert alleen een e-mailadres bij het invoeren van gegevens.<br/>**`Length Only`** - Valideert de invoer op basis van de lengte van de gegevens die in het veld zijn ingevoerd. |
| [!UICONTROL Input/Output Filter] | Hiermee past u een voorbewerkingsfilter toe op waarden die zijn ingevoerd in een tekstveld, tekstgebied of invoertype voor meerdere regels voordat de record wordt opgeslagen. Opties: <br/>**`None`**- Hiermee wordt geen filter toegepast op tekst die in het veld wordt ingevoerd.<br/>**`Strip HTML Tags`** - Hiermee verwijdert u HTML-tags uit de tekst. Met dit filter kunt u gegevens opschonen die in een veld worden geplakt vanuit een andere bron die HTML-tags bevat. <br/>**`Escape HTML Entities`**- Hiermee worden speciale tekens in de tekst omgezet in een geldige HTML-escapereeks, zoals `amp;`. Escape-reeksen worden ingesloten tussen een ampersand en een puntkomma en worden vaak gebruikt voor slimme aanhalingstekens, copyrightsymbolen en handelsmerken van typografische tekens. Escape-reeksen worden ook gebruikt om tekens zoals de tekst kleiner dan (`<`) en groter dan (`>`) en het ampersand-teken dat ook in de code wordt gebruikt. Met dit filter kunt u speciale tekens opschonen die soms door tekstverwerkers in databasevelden worden geplakt. |
| [!UICONTROL Add to Column Options] | Hiermee wordt opgegeven of het kenmerk wordt opgenomen als een kolom in het dialoogvenster [Klanten](customers-all.md) raster. Opties: `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | Geeft aan of het kenmerk kan worden gebruikt als filter voor zoekbewerkingen vanuit het raster. Opties: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Geeft de filterovereenkomende voorwaarden voor kenmerken voor zoekbewerkingen uit het raster op. Het heeft geen invloed op de _Zoeken op trefwoord_ veld voor het raster. Opties: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Geeft aan of de kenmerkwaarde kan worden gebruikt als een trefwoord in zoekbewerkingen. Opties: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Hiermee wordt bepaald of het kenmerk is opgenomen in [klantensegment](customer-segments.md) voorwaarden. Opties: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Show on Storefront] | Hiermee bepaalt u of het kenmerk wordt weergegeven als een veld in de klantgegevens in de winkelbrowser. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Geeft de sorteervolgorde van dit kenmerk ten opzichte van andere klantkenmerken aan. De sorteervolgorde bepaalt de volgorde waarin velden focus krijgen tijdens het invoeren van gegevens wanneer toetsenbordnavigatie wordt gebruikt. |
| [!UICONTROL Forms to Use in] | Hiermee bepaalt u de pagina&#39;s met gegevensinvoerformulieren waarop het kenmerk wordt weergegeven. Opties: <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## Standaardklantkenmerken

| Kenmerkcode | Beschrijving |
| --------------- | ------------------ |
| `created_at` | De datum waarop de klantenaccount is gemaakt. |
| `updated_at` | De datum waarop de klantenaccount voor het laatst is bijgewerkt. |
| `website_id` | De website-id van de site waar de klantenaccount is gemaakt. |
| `store_id` | De winkel-id van de site waar de klantenaccount is gemaakt. |
| `created_in` | De winkelweergave waar het account is gemaakt. |
| `group_id` | De id van de klantengroep waaraan de klant is toegewezen. |
| `disable_auto_group_change` | Hiermee bepaalt u of klantgroepen dynamisch kunnen worden toegewezen tijdens [Validatie van BTW-id](../stores-purchase/vat.md#configure-vat-id-validation). |
| `prefix` | Elk voorvoegsel dat met de naam van de klant wordt gebruikt (zoals Mr., Mw. of Dr.). |
| `firstname` | De voornaam van de klant. |
| `middlename` | De middelste naam of middelste startnaam van de klant. |
| `lastname` | De achternaam van de klant. |
| `suffix` | Een achtervoegsel dat wordt gebruikt met de naam van de klant. (zoals Jr., Sr. of Esquire) |
| `email` | Het e-mailadres van de klant |
| `dob` | De geboortedatum van de klant.  <br><br>**_Belangrijk:_**In overeenstemming met de huidige beste praktijken op het gebied van beveiliging en privacy, dient u zich bewust te zijn van mogelijke juridische en veiligheidsrisico&#39;s die verbonden zijn aan de opslag van de volledige geboortedatum van de klant (maand, dag, jaar) met andere persoonlijke identificatoren. U wordt aangeraden de opslag van de volledige geboortedatum van de klant te beperken en u aan te raden het geboortejaar van de klant als alternatief te gebruiken. |
| `taxvat` | De BTW-identificatienummer dat aan de klant is toegewezen. Het standaardlabel van dit kenmerk is `VAT Number`. Het veld BTW-nummer is altijd aanwezig in alle adressen van de verzend- en factureringsklant wanneer deze wordt bekeken vanuit de beheerder, maar is geen verplicht veld. |
| `gender` | The customer gender. |

## Demo voor klantkenmerken

Bekijk deze video voor een demonstratie over het maken van klantkenmerken:

>[!VIDEO](https://video.tv.adobe.com/v/343661?quality=12)
