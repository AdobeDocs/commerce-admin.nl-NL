---
title: Orders
description: Leer meer over de werkruimte Bestellingen en de zoekmogelijkheden die worden gebruikt om bestellingen te zoeken in Admin.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Orders

Het _bevel_ net maakt een lijst van alle huidige orden en volgt hun vooruitgang en [&#x200B; ordestatus &#x200B;](order-status.md) door het [&#x200B; werkschema &#x200B;](order-processing.md). Een gemakkelijke manier om het basisproces te begrijpen is dat een orde een [&#x200B; factuur &#x200B;](invoices.md) wordt, en een factuur wordt a [&#x200B; lading &#x200B;](shipments.md). Het net vertegenwoordigt het eerste stadium van het proces, en is waar u [&#128279;](order-update.md) bestaande orden kunt bijwerken en orden creëren.

Gewoonlijk worden bestellingen gemaakt wanneer klanten het afrekenproces vanuit de winkel voltooien. Nochtans, als een klant hulp nodig heeft, kunt u tot hun [&#x200B; winkelwagentje &#x200B;](shopping-assisted-cart-manage.md) of [&#x200B; tot een orde &#x200B;](customer-account-create-order.md) of van het _Orders_ net of direct van hun klantenrekening toegang hebben.

## De werkruimte voor bestellingen

De werkruimte van Orden maakt een lijst van alle huidige orden, en geeft u de capaciteit om bestaande orden uit te geven en [&#128279;](customer-account-create-order.md) orden tot stand te brengen. Elke rij in het raster staat voor de volgorde van de klant en elke kolom staat voor een kenmerk of gegevensveld. Gebruik de standaard [&#x200B; controles &#x200B;](../getting-started/admin-grid-controls.md) om de lijst te sorteren en te filtreren, orden te vinden, en [&#x200B; acties &#x200B;](../getting-started/admin-actions-control.md) op geselecteerde orden toe te passen. Met de tabbladen boven de pagineringsbesturingselementen kunt u de lijst filteren, de standaardweergave wijzigen, kolommen wijzigen en opnieuw rangschikken en gegevens exporteren.

![&#x200B; het net van Orden &#x200B;](./assets/orders-grid.png){width="700" zoomable="yes"}

### Rasterindeling

De selectie van kolommen en hun volgorde in het raster kunnen naar wens worden gewijzigd. De nieuwe lay-out kan als net _mening_ worden bewaard. Standaard worden slechts negen van de 20 beschikbare kolommen in het raster opgenomen.

![&#x200B; de Kolommen van het Net van de Orde &#x200B;](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### De kolomselectie wijzigen

In de hoger-juiste hoek, klik de _controle van de Kolommen_ ( ![&#x200B; montages van de Kolom &#x200B;](../assets/icon-columns.png)) en doe het volgende:

- Schakel het selectievakje in van de kolommen die u aan het raster wilt toevoegen.
- Schakel het selectievakje uit van elke kolom die u uit het raster wilt verwijderen.

#### De kolomselectie opnieuw instellen

1. Klik de _controle van Kolommen_ ( ![&#x200B; montages van de Kolom &#x200B;](../assets/icon-columns.png)).

1. Klik op **[!UICONTROL Reset]** om de rasterkolommen opnieuw in te stellen.

   De netlay-out verandert om slechts [&#x200B; standaardkolommen &#x200B;](#column-descriptions) te tonen.

#### Een kolom verplaatsen

1. Klik en houd de kopbal van de kolom.

1. Sleep de kolom naar de nieuwe positie en laat deze los.

#### Een rasterweergave opslaan

1. Klik de **[!UICONTROL View]** ( ![&#x200B; pictogram van het Ogen &#x200B;](../assets/icon-view-eye.png)) controle.

1. Klik op **[!UICONTROL Save Current View]**.

1. Voer een **[!UICONTROL name]** in voor de weergave.

1. Om alle veranderingen te bewaren, klik de pijl ( ![&#x200B; pictogram van de Pijl &#x200B;](../assets/icon-arrow-save.png)).

   De naam van de weergave wordt nu weergegeven als de huidige weergave.

#### De weergave wijzigen

Klik de **[!UICONTROL View]** ( ![&#x200B; pictogram van het Ogen &#x200B;](../assets/icon-view-eye.png)) controle. Voer vervolgens een van de volgende handelingen uit:

- Klik op de naam van de weergave als u een andere weergave wilt gebruiken.

- Om de naam van een mening te veranderen, klik _uitgeven_ ( ![&#x200B; pictogram van het Potlood &#x200B;](../assets/icon-edit-pencil.png)) pictogram en werk de naam bij.

### Workspace-besturingselementen

| Besturing | Beschrijving |
|--- |--- |
| [!UICONTROL Create New Order] | Hiermee maakt u een volgorde. Zie [&#x200B; Creërend een Orde &#x200B;](customer-account-create-order.md) voor meer informatie. |
| [!UICONTROL Go to Archive] | Hiermee geeft u de lijst met gearchiveerde bestellingen weer. |
| [!UICONTROL Search] | Hiermee wordt een zoekopdracht naar bestellingen gestart op basis van de huidige filters. |
| [!UICONTROL Filters] | Definieert een set zoekparameters die wordt gebruikt om de records te filteren die in het raster worden weergegeven. |
| [!UICONTROL Default View] | Bepaalt de standaardkolomlay-out van het raster. |
| [!UICONTROL Columns] | Bepaalt de selectie van kolommen en hun orde in het net. De kolomlay-out kan als a _mening_ worden veranderd en worden bewaard. Standaard worden slechts enkele kolommen in het raster opgenomen. |
| [!UICONTROL Export] | Hiermee exporteert u de geselecteerde records als een CSV- of Excel XML-bestand. |

{style="table-layout:auto"}

### Handelingen

Als u een actie wilt toepassen op specifieke orders, schakelt u het selectievakje in de eerste kolom van elke volgorde in. Als u alle bestellingen wilt selecteren of deselecteren, gebruikt u het besturingselement boven aan de kolom.

![&#128279;](./assets/orders-action.png){width="600" zoomable="yes"} de Acties van de orde 0&rbrace;

| Besturing | Beschrijving |
|--- |--- |
| [!UICONTROL Actions] | Hiermee geeft u alle handelingen weer die op geselecteerde bestellingen kunnen worden toegepast. Als u een handeling wilt toepassen op een bestelling of groep bestellingen, schakelt u het selectievakje in de eerste kolom van elke bestelling in. <br/> de acties van de Orde: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (slechts Adobe Commerce) |
| [!UICONTROL Mass Actions] | Kan worden gebruikt om meerdere records te selecteren als het doel van de handeling. Schakel het selectievakje in de eerste kolom van elke record waarop de actie betrekking heeft. Opties: `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | Past de huidige actie op de geselecteerde ordecords toe. |
| [!UICONTROL Edit] | Hiermee opent u de volgorde in de bewerkingsmodus. |

{style="table-layout:auto"}

### Kolombeschrijvingen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Schakel de selectievakjes in voor de aanhalingstekens die aan een handeling moeten worden onderworpen of gebruik het selectiegereedschap in de kolomkop. Opties: Alles selecteren / Alles deselecteren |
| [!UICONTROL ID] | Een uniek, opeenvolgend aantal dat wordt toegewezen wanneer een nieuwe orde voor het eerst wordt bewaard. |
| [!UICONTROL Purchase Point] | Hiermee wordt de winkelweergave aangegeven waar de bestelling is geplaatst. |
| [!UICONTROL Purchase Date] | De datum en het tijdstip waarop de bestelling is geplaatst. Deze wordt altijd weergegeven op basis van de standaardtijdzone. |
| [!UICONTROL Bill-to Name] | De naam van de persoon die verantwoordelijk is voor de betaling van de beschikking. |
| [!UICONTROL Ship-to Name] | De naam van de persoon aan wie de order moet worden verzonden. |
| [!UICONTROL Grand Total (Base)] | Het totale bedrag van de bestelling. |
| [!UICONTROL Grand Total (Purchased)] | Het totaal-generaal aan producten die in de bestelling zijn aangeschaft. |
| [!UICONTROL Status] | De huidige orderstatus. |
| [!UICONTROL Action] | _[!UICONTROL View]_&#x200B;opent de volgorde in de bewerkingsmodus. |
| [!UICONTROL Allocated sources] | De bronnen die aan die specifieke orde worden toegewezen. |

{style="table-layout:auto"}

Extra beschikbare kolommen:

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Billing Address] | Het factureringsadres van de klant die de orde plaatste. |
| [!UICONTROL Shipping Address] | Het adres waar de bestelling moet worden verzonden. |
| [!UICONTROL Shipping Information] | De methode die moet worden gebruikt om de orde te verschepen. |
| [!UICONTROL Customer Email] | Het e-mailadres van de persoon die de bestelling heeft geplaatst. |
| [!UICONTROL Customer Group] | De klantengroep waaraan de persoon wordt toegewezen die de orde plaatste. |
| [!UICONTROL Subtotal] | Het subtotaal van de bestelling, zonder verzending en belasting. |
| [!UICONTROL Shipping and Handling] | Het bedrag dat in rekening wordt gebracht voor verzending. |
| [!UICONTROL Customer Name] | De voornaam en achternaam van de klant die de bestelling heeft geplaatst. |
| [!UICONTROL Payment Method] | De wijze van betaling die voor de bestelling moet worden gebruikt. |
| [!UICONTROL Total Refunded] | Elk bedrag van de bestelling dat aan de klant moet worden terugbetaald. |
| [!UICONTROL Refunded to Store Credit] | ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) om het even welk bedrag van de orde die aan het de opslagkrediet van de klant moet worden teruggegeven. |
| [!UICONTROL Company Name] | ![&#x200B; Adobe Commerce B2B &#x200B;](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) de naam van het [&#x200B; bedrijf &#x200B;](../b2b/account-companies.md) die de orde plaatste. |

{style="table-layout:auto"}

## Zoeken in bestellingen

Het vakje van het Onderzoek in het hogere linkerzijde van het net van Orden kan worden gebruikt om specifieke orden door sleutelwoord te vinden, of door de ordecords in het net te filtreren.

![&#x200B; Resultaten van het Onderzoek &#x200B;](./assets/order-search.png){width="600" zoomable="yes"}

### Zoeken naar een overeenkomst

1. Voer een zoekterm in het zoekvak van de pagina in.

1. Om de resultaten te tonen, klik _Onderzoek_ ( ![&#x200B; Vergrootglaspictogram &#x200B;](../assets/icon-magnify-search.png) ).

### De zoekopdracht filteren

1. Om de selectie van onderzoeksfilters te tonen, klik de _Filters_ ( ![&#x200B; het pictogram van het Kanaal &#x200B;](../assets/icon-filter-search.png)) tabel.

   ![&#x200B; de Filters van de Orde &#x200B;](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. Voer zoveel filters in als u wilt om de volgorde te beschrijven die u wilt zoeken.

1. Klik op **[!UICONTROL Apply Filters]** om de resultaten weer te geven.

### Zoekfilters

| Filter | Beschrijving |
|--- |--- |
| [!UICONTROL Purchase Date] | Hiermee filtert u de zoekopdracht op basis van de aangeschafte datum. Als u opdrachten wilt zoeken binnen een datumbereik, voert u zowel de datum **[!UICONTROL from]** als de datum **[!UICONTROL to]** in. |
| [!UICONTROL ID] | Hiermee filtert u de zoekopdracht op basis van bestellings-id. |
| [!UICONTROL Grand Total (Base)] | Hiermee filtert u de zoekopdracht op basis van het Eindtotaal van elke bestelling, inclusief eventuele credits die op de bestelling zijn toegepast. |
| [!UICONTROL Grand Total (Purchased)] | Hiermee filtert u de zoekopdracht op basis van het Eindtotaal van items die in elke bestelling zijn aangeschaft. |
| [!UICONTROL Bill-to Name] | Hiermee filtert u de zoekopdracht op basis van de naam van de persoon die voor de bestelling verantwoordelijk is. |
| [!UICONTROL Ship-to Name] | Hiermee filtert u de zoekopdracht op basis van de naam van de persoon aan wie de bestelling wordt verzonden. |
| [!UICONTROL Purchase Point] | Hiermee filtert u de zoekopdracht op website, in de winkel of in de opslagweergave waarin de bestelling is geplaatst. |
| [!UICONTROL Status] | Hiermee filtert u de zoekopdracht op basis van de orderstatus. Opties: `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | Hiermee wordt de zoekopdracht gefilterd op basis van de transactiebron. |

{style="table-layout:auto"}

### Zoeken in gereedschappen

| Gereedschap | Beschrijving |
|--- |--- |
| [!UICONTROL Apply Filters] | Hiermee past u alle filters toe op de zoekresultaten. |
| [!UICONTROL Cancel] | Annuleert de huidige zoekopdracht. |
| [!UICONTROL Clear All] | Wist alle zoekfilters. |

{style="table-layout:auto"}

## Bronnen voor probleemoplossing

Raadpleeg de volgende artikelen in de Commerce Support Knowledge Base voor hulp bij het oplossen van problemen met bestelproblemen:

- [&#x200B; de vertoningsfout van Orden &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html?lang=nl-NL)
- [&#x200B; de Orden worden niet getoond in het net van Orden in Admin &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
