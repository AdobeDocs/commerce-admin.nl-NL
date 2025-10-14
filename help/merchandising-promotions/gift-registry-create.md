---
title: Registratie van cadeautjes instellen
description: Leer hoe u registertypen voor cadeautjes kunt instellen voor klanten in uw winkel.
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Registratie van cadeautjes instellen

{{ee-feature}}

Een cadeauregister kan worden gemaakt voor elk type gebeurtenis, zoals een bruiloft, verjaardag, verjaardag, nieuwe baby of een andere speciale gelegenheid. Adobe Commerce bevat standaard de volgende speciale gebeurtenissen:

- Baby
- Geboortedatum
- Bruiloft

Wanneer u een register creeert, wordt het een optie in de lijst van cadeauregistertypes in de rekening van de klant.

U kunt een van de drie voorbereide cadeauregisters gebruiken of uw eigen aangepaste register maken. Elk type cadeauregister bevat verschillende kenmerken. Dit zijn de gegevensinvoervelden die een klant invult om een cadeauregister te maken. De attributen verstrekken extra informatie over de gebeurtenis, de tijd en de plaats, of om het even welke andere informatie die nodig is. Afhankelijk van het invoertype hebben sommige kenmerken meerdere opties. Het registertype `Wedding` gift heeft bijvoorbeeld het kenmerk `Role` , met de opties `Bride` , `Groom` en `Partner` . Meer over attributen en inputtypes leren, zie [&#x200B; Attributen &#x200B;](../customers/attribute-properties.md).

![&#x200B; Cadeauregistertypes &#x200B;](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## Een voorbereid cadeauregister gebruiken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   De verjaardagsregistraties, trouwboeken en babyregisters kunnen door klanten worden gebruikt via hun accounts.

1. Zorg ervoor om de [&#x200B; configuratie van het e-mailmalplaatje &#x200B;](../systems/email-templates.md#configure-email-templates) te voltooien, zodat wijzen zij op uw merk.

## Een aangepast cadeauregister maken

1. Ga op de zijbalk Beheerder naar **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Gift Registry Type]** .

1. Voer onder **[!UICONTROL General Information]** het volgende in:

   - Voer een uniek **[!UICONTROL Code]** in om het cadeauregister intern te identificeren.

     De code moet beginnen met een kleine letter. De rest van de code kan om het even welke combinatie kleine letters (a-z), aantallen (0-9), en onderstrepingsteken (`_`) zijn.

   - Voer bij **[!UICONTROL Label]** een naam voor het cadeauregister in, zoals u deze wilt weergeven in de winkel.

     Dit label is een optie in de lijst met registertypen voor cadeaus die beschikbaar zijn voor de klant.

   - Voer bij **[!UICONTROL Sort Order]** een getal in om de volgorde te bepalen waarin dit cadeauregister wordt weergegeven wanneer het met andere typen wordt weergegeven.

   - Stel **[!UICONTROL Is Listed]** in op `Yes` om het cadeauregister te activeren.

     ![&#x200B; de registratie van het Cadeautje - algemene informatie &#x200B;](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. Onderzoek elke sectie van de Registratie van het Cadeautje om het type van informatie te bepalen u wilt omvatten.

1. Kies **[!UICONTROL Attributes]** in het linkerdeelvenster en klik op **[!UICONTROL Add Attribute]** .

   ![&#x200B; de registratie van het Cadeautje - nieuwe attributen &#x200B;](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. Voer voor elk kenmerk de volgende handelingen uit:

   - Wijs een uniek **[!UICONTROL Code]** toe om het kenmerk intern te identificeren. De code kan maximaal 15 tekens lang zijn en moet beginnen met een kleine letter. De rest van de code kan kleine letters (`a` - `z`), aantallen (`0` - `9`), en het onderstrepingsteken (`_`) karakter omvatten om woorden te scheiden.

   - Kies de **[!UICONTROL Input Type]** die voor gegevensinvoer moet worden gebruikt. U kunt een van de aangepaste of statische typen gebruiken.

   - Als het invoertype meerdere opties heeft, klikt u op **[!UICONTROL Add New Option]** en vult u de gegevens voor elke optie in.

     Sommige invoertypen hebben aanvullende eigenschappen. De locatie van de gebeurtenis heeft bijvoorbeeld aanvullende eigenschappen om de gebeurtenis doorzoekbaar te maken en opgenomen in de openbare lijst met cadeauregisters van uw winkel.

      - Stel **[!UICONTROL Attribute Group]** in op de sectie in het cadeauregister waar u het kenmerk wilt weergeven.

      - Voer bij **[!UICONTROL Label]** een naam in om het gegevensinvoerveld in het register te identificeren.

      - Als de klant een selectie moet maken of een waarde in het veld moet invoeren, stelt u **[!UICONTROL Is Required]** in op `Yes` .

      - Voer bij **[!UICONTROL Sort Order]** een getal in om de volgorde te bepalen waarin dit cadeauregister wordt weergegeven wanneer het wordt weergegeven bij andere cadeauregisters die mogelijk beschikbaar zijn in de winkel.

1. Om een andere optie toe te voegen, klik **Nieuwe Optie** toevoegen.

   Elke nieuwe toegevoegde optie wordt in een nieuwe sectie bovenaan weergegeven. Herhaal dit proces voor het nieuwe kenmerk.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Veldomschrijvingen

### [!UICONTROL General Information]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Code] | A unique name to identify the gift register type internal. Het eerste teken van de code moet een kleine letter zijn. De rest van de code kan elke combinatie zijn van kleine letters (a-z), getallen (0-9) en het onderstrepingsteken (`_`). |
| [!UICONTROL Label] | De naam van het registertype van het cadeau dat in de winkel wordt weergegeven. |
| [!UICONTROL Sort Order] | Bepaalt de opeenvolging waarin dit type van cadeauregistratie verschijnt wanneer vermeld met andere types. |
| [!UICONTROL Is Listed] | Bepaalt als het type van het cadeauregister aan klanten in de opslag beschikbaar is. Opties: `Yes` / `No` . |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Code] | Een unieke naam om het kenmerk intern te identificeren. De code kan elke combinatie van kleine letters (a-z), getallen (0-9) en het onderstrepingsteken (`_`) bevatten. |
| [!UICONTROL Input Type] | Bepaalt het type van gegevens en inputcontrole dat met de attributen, volgens type wordt geassocieerd. |
| [!UICONTROL Attribute Group] | Selecteer de groep waar het kenmerk wordt weergegeven in het cadeauregister. |
| [!UICONTROL Label] | De naam die het kenmerk in het accountdashboard van de klant identificeert. |
| [!UICONTROL Is Required] | Geeft aan of het kenmerk een verplicht item is. Het cadeauregister kan pas worden opgeslagen als alle vereiste kenmerken zijn voltooid. Opties: `Yes` / `No` . |
| [!UICONTROL Sort Order] | Bepaalt de opeenvolging waarin het attribuut verschijnt wanneer vermeld met andere attributen. |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

Selecteer het type gegevens en invoerbesturingselement dat aan het kenmerk is gekoppeld.

**_[!UICONTROL Custom Types]_**

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Text] | Geeft het kenmerk weer als een tekstveld. |
| [!UICONTROL Select] | Geeft het kenmerk weer als een vervolgkeuzelijst. Klik **[!UICONTROL Add New Option]** om meer voorwaarden aan de drop-down lijst toe te voegen:<br/>**[!UICONTROL Code]**- een unieke naam om het attribuut intern te identificeren.<br/>**[!UICONTROL Label]** - De naam die het kenmerk in het accountdashboard van de klant identificeert.<br/>**[!UICONTROL Is Default]**- Plaats deze schakelaar om de standaardvoorwaarde te selecteren.<br/>**[!UICONTROL Delete Option]** - Klik om de optie te verwijderen. |
| [!UICONTROL Date] | Geeft het kenmerk weer als een datumveld. Opties: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | Hiermee geeft u het kenmerk weer als een vervolgkeuzelijst met landen. Stel **[!UICONTROL Show Region]** in op: `Yes` / `No` . |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Event Date] | Bepaalt hoe het datumkenmerk wordt gebruikt in de winkel. Opties: <br/>**[!UICONTROL Searchable]**- Hiermee bepaalt u of het kenmerk beschikbaar is voor Geavanceerd zoeken. Opties: `Yes` / `No` .<br/>**[!UICONTROL Is Listed]** - Hiermee wordt bepaald of de gebeurtenis is opgenomen in de lijst met gebeurtenissen die beschikbaar is in de winkel. Opties: `Yes` / `No` . <br/>**[!UICONTROL Date Format]**- Hiermee bepaalt u de indeling van de gebeurtenisdatum. Opties: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | Hiermee geeft u het kenmerk weer als een lijst met landen. Opties: <br/>**[!UICONTROL Searchable]**- Hiermee bepaalt u of het kenmerk beschikbaar is voor Geavanceerd zoeken. Opties: `Yes` / `No` .<br/>**[!UICONTROL Is Listed]** - Hiermee wordt bepaald of de gebeurtenis is opgenomen in de lijst met gebeurtenissen die beschikbaar is in de winkel. Opties: `Yes` / `No` . <br/>**[!UICONTROL Show Region]**- Hiermee bepaalt u het gebied van de gebeurtenis. |
| [!UICONTROL Event Location] | De locatie van de gebeurtenis die betrekking heeft op het register van cadeaus. <br/> Reeks **[!UICONTROL Is Searcheable]** aan: `Yes` / `No` <br/> Reeks **[!UICONTROL Is Listed]** aan: `Yes` / `No` |
| [!UICONTROL Role] | De rol die de ontvanger van de gift identificeert. Bijvoorbeeld `Bride` , `Groom` of `Partner` .<br/>**[!UICONTROL Is Searcheable]**- Reeks aan `Yes`/ `No`<br/>**&#x200B; wordt vermeld &#x200B;**- Reeks aan `Yes` / `No`<br/>**[!UICONTROL Add New Option]** - klik om meer voorwaarden aan het drop-down menu toe te voegen:<br/>**Code** - een unieke naam om de attributen intern te identificeren.<br/>**[!UICONTROL Label]**- De naam die het kenmerk in het accountdashboard van de klant identificeert.<br/>**[!UICONTROL Is Default]** - Plaats deze schakelaar om de standaardvoorwaarde te selecteren.<br/>**[!UICONTROL Delete Option]**- Klik om de optie te verwijderen. |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

Selecteer de groep waar het kenmerk wordt weergegeven in het cadeauregister.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Event Information] | Groepeert alle attributen van de cadeauregistratie die de informatie over de gebeurtenis van de cadeauregistratie, zijn tijd, plaats, etc. toevoegen. |
| [!UICONTROL Gift Registry Properties] | Combineert alle attributen die direct informatie over het giftenregister toevoegen. |
| [!UICONTROL Privacy Settings] | Hier worden de kenmerken weergegeven die informatie over de privacy van de cadeauregistergebeurtenis toevoegen. |
| [!UICONTROL Recipients Information] | Groepeert de attributen die informatie over de persoon verstrekken die tot een geschenkregister leidt. |
| [!UICONTROL Shipping Address] | Combineert de kenmerken die informatie over het verzendadres van de cadeauregistergebeurtenis toevoegen. |

{style="table-layout:auto"}
