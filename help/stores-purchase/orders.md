---
title: Orders
description: Leer meer over de werkruimte Bestellingen en de zoekmogelijkheden die worden gebruikt om bestellingen te zoeken in Admin.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 0%

---

# Orders

Het _bevel_ net maakt een lijst van alle huidige orden en volgt hun vooruitgang en [ ordestatus ](order-status.md) door het [ werkschema ](order-processing.md). Een gemakkelijke manier om het basisproces te begrijpen is dat een orde een [ factuur ](invoices.md) wordt, en een factuur wordt a [ lading ](shipments.md). Het net vertegenwoordigt het eerste stadium van het proces, en is waar u [ ](order-update.md) bestaande orden kunt bijwerken en orden creëren.

Gewoonlijk worden bestellingen gemaakt wanneer klanten het afrekenproces vanuit de winkel voltooien. Nochtans, als een klant hulp nodig heeft, kunt u tot hun [ winkelwagentje ](shopping-assisted-cart-manage.md) of [ tot een orde ](customer-account-create-order.md) of van het _Orders_ net of direct van hun klantenrekening toegang hebben.

## De werkruimte voor bestellingen

De werkruimte van Orden maakt een lijst van alle huidige orden, en geeft u de capaciteit om bestaande orden uit te geven en [ ](customer-account-create-order.md) orden tot stand te brengen. Elke rij in het raster staat voor de volgorde van de klant en elke kolom staat voor een kenmerk of gegevensveld. Gebruik de standaard [ controles ](../getting-started/admin-grid-controls.md) om de lijst te sorteren en te filtreren, orden te vinden, en [ acties ](../getting-started/admin-actions-control.md) op geselecteerde orden toe te passen. Met de tabbladen boven de pagineringsbesturingselementen kunt u de lijst filteren, de standaardweergave wijzigen, kolommen wijzigen en opnieuw rangschikken en gegevens exporteren.

![ het net van Orden ](./assets/orders-grid.png){width="700" zoomable="yes"}

### Rasterindeling

De selectie van kolommen en hun volgorde in het raster kunnen naar wens worden gewijzigd. De nieuwe lay-out kan als net _mening_ worden bewaard. Standaard worden slechts negen van de 20 beschikbare kolommen in het raster opgenomen.

![ de Kolommen van het Net van de Orde ](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### De kolomselectie wijzigen

In de hoger-juiste hoek, klik de _controle van de Kolommen_ ( ![ montages van de Kolom ](../assets/icon-columns.png)) en doe het volgende:

- Schakel het selectievakje in van de kolommen die u aan het raster wilt toevoegen.
- Schakel het selectievakje uit van elke kolom die u uit het raster wilt verwijderen.

#### De kolomselectie opnieuw instellen

1. Klik de _controle van Kolommen_ ( ![ montages van de Kolom ](../assets/icon-columns.png)).

1. Klik op **[!UICONTROL Reset]** om de rasterkolommen opnieuw in te stellen.

   De netlay-out verandert om slechts [ standaardkolommen ](#column-descriptions) te tonen.

#### Een kolom verplaatsen

1. Klik en houd de kopbal van de kolom.

1. Sleep de kolom naar de nieuwe positie en laat deze los.

#### Een rasterweergave opslaan

1. Klik de **[!UICONTROL View]** ( ![ pictogram van het Ogen ](../assets/icon-view-eye.png)) controle.

1. Klik op **[!UICONTROL Save Current View]**.

1. Voer een **[!UICONTROL name]** in voor de weergave.

1. Om alle veranderingen te bewaren, klik de pijl ( ![ pictogram van de Pijl ](../assets/icon-arrow-save.png)).

   De naam van de weergave wordt nu weergegeven als de huidige weergave.

#### De weergave wijzigen

Klik de **[!UICONTROL View]** ( ![ pictogram van het Ogen ](../assets/icon-view-eye.png)) controle. Voer vervolgens een van de volgende handelingen uit:

- Klik op de naam van de weergave als u een andere weergave wilt gebruiken.

- Om de naam van een mening te veranderen, klik _uitgeven_ ( ![ pictogram van het Potlood ](../assets/icon-edit-pencil.png)) pictogram en werk de naam bij.

### Workspace-besturingselementen

| Besturing | Beschrijving |
|--- |--- |
| [!UICONTROL Create New Order] | Hiermee maakt u een volgorde. Zie [ Creërend een Orde ](customer-account-create-order.md) voor meer informatie. |
| [!UICONTROL Go to Archive] | Hiermee geeft u de lijst met gearchiveerde bestellingen weer. |
| [!UICONTROL Search] | Hiermee wordt een zoekopdracht naar bestellingen gestart op basis van de huidige filters. |
| [!UICONTROL Filters] | Definieert een set zoekparameters die wordt gebruikt om de records te filteren die in het raster worden weergegeven. |
| [!UICONTROL Default View] | Bepaalt de standaardkolomlay-out van het raster. |
| [!UICONTROL Columns] | Bepaalt de selectie van kolommen en hun orde in het net. De kolomlay-out kan als a _mening_ worden veranderd en worden bewaard. Standaard worden slechts enkele kolommen in het raster opgenomen. |
| [!UICONTROL Export] | Hiermee exporteert u de geselecteerde records als een CSV- of Excel XML-bestand. |

{style="table-layout:auto"}

### Handelingen

Als u een actie wilt toepassen op specifieke orders, schakelt u het selectievakje in de eerste kolom van elke volgorde in. Als u alle bestellingen wilt selecteren of deselecteren, gebruikt u het besturingselement boven aan de kolom.

](./assets/orders-action.png){width="600" zoomable="yes"} de Acties van de orde 0}![

| Besturing | Beschrijving |
|--- |--- |
| [!UICONTROL Actions] | Hiermee geeft u alle handelingen weer die op geselecteerde bestellingen kunnen worden toegepast. Als u een handeling wilt toepassen op een bestelling of groep bestellingen, schakelt u het selectievakje in de eerste kolom van elke bestelling in. <br/> de acties van de Orde: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce) |
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
| [!UICONTROL Action] | _[!UICONTROL View]_opent de volgorde in de bewerkingsmodus. |
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
| [!UICONTROL Refunded to Store Credit] | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) om het even welk bedrag van de orde die aan het de opslagkrediet van de klant moet worden teruggegeven. |
| [!UICONTROL Company Name] | ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B) de naam van het [ bedrijf ](../b2b/account-companies.md) die de orde plaatste. |

{style="table-layout:auto"}

## Zoeken in bestellingen

Het vakje van het Onderzoek in het hogere linkerzijde van het net van Orden kan worden gebruikt om specifieke orden door sleutelwoord te vinden, of door de ordecords in het net te filtreren.

![ Resultaten van het Onderzoek ](./assets/order-search.png){width="600" zoomable="yes"}

### Zoeken naar een overeenkomst

1. Voer een zoekterm in het zoekvak van de pagina in.

1. Om de resultaten te tonen, klik _Onderzoek_ ( ![ Vergrootglaspictogram ](../assets/icon-magnify-search.png) ).

### De zoekopdracht filteren

1. Om de selectie van onderzoeksfilters te tonen, klik de _Filters_ ( ![ het pictogram van het Kanaal ](../assets/icon-filter-search.png)) tabel.

   ![ de Filters van de Orde ](./assets/order-search-filter.png){width="600" zoomable="yes"}

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

- [ de vertoningsfout van Orden ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html)
- [ PayPal dubbele orden 10415 fout ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-6/mdva-31006-magento-patch-paypal-duplicate-orders-10415-error.html)
- [ de Nieuwe orden worden verzonden naar archief ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/new-orders-are-sent-to-archive.html)
- [ de Orden worden niet getoond in het net van Orden in Admin ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
- [ status van de Orde - onjuiste die verzending via REST API wordt gecreeerd ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-7/mdva-30972-magento-patch-order-status-incorrect-shipment-created-via-rest-api.html)
