---
title: Retourneert
description: Meer informatie over de geretourneerde workflow en het geven van een geretourneerde handelsvergunning.
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Retourneert

A _geretourneerde handelsvergunning_ (RMA) kan worden toegekend aan klanten die een product willen retourneren ter vervanging of terugbetaling. Doorgaans neemt de klant contact op met de handelaar om terugbetaling aan te vragen. Indien goedgekeurd, wordt een uniek aantal RMA toegewezen om het teruggekeerde product te identificeren. In de configuratie, kunt u of RMA voor alle producten toelaten of RMA voor slechts bepaalde producten toestaan. De _[!UICONTROL Returns]_Het net maakt een lijst van de huidige teruggekeerde handelsmiddelverzoeken (RMAs) en wordt gebruikt om nieuwe terugkeerverzoeken in te gaan.

![Retourneert raster](./assets/return.png){width="600" zoomable="yes"}

RMAs kan voor eenvoudige, gegroepeerde, configureerbare, en bundelproducttypes worden uitgegeven. RMA&#39;s zijn echter niet beschikbaar voor virtuele producten, downloadbare producten en cadeaukaarten.

## Kolombeschrijvingen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Selecteer de selectievakjes voor de geretourneerde waarden die aan een handeling moeten worden onderworpen of gebruik het selectiegereedschap in de kolomkop. Opties: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | Een unieke numerieke id die aan elke return is toegewezen |
| [!UICONTROL Requested] | Datum en tijd waarop de return is geplaatst |
| [!UICONTROL Order] | Een uniek nummer van de oorspronkelijke volgorde |
| [!UICONTROL Ordered] | De datum en het tijdstip waarop de order is geplaatst |
| [!UICONTROL Customer] | De naam van de klant of koper die de bestelling heeft geplaatst |
| [!UICONTROL Status] | Retourstatus. Opties: `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** Hiermee wordt de geretourneerde waarde geopend in de bewerkingsmodus. |

{style="table-layout:auto"}

## RMA en retourworkflow

1. **Aanvraag ontvangen** - Indien [enabled](rma-configure.md#enable-rmas-for-your-store) voor de winkel kunnen zowel geregistreerde klanten als gasten een RMA aanvragen. U kunt [een RMA-verzoek indienen in de beheerder](#create-a-return-request-in-the-admin).

2. **RMA uitgegeven** - Nadat u het verzoek hebt overwogen, kunt u het gedeeltelijk, volledig of geannuleerd. Als u de terugzending toestaat en ermee akkoord gaat de terugzending te betalen, kunt u een bestelling van Admin met een gesteunde drager tot stand brengen.

3. **Ontvangen goederen en verwerkte terugzending van producten** - Het volgende stroomdiagram beschrijft de operationele orde om het terugkeerproces te voltooien:

   ![Workflow voor teruggave van producten](./assets/workflow-customer-returns.png){width="500"}

## RMA-status

Tijdens zijn levenscyclus, kan een teruggekeerde handelsvergunning (RMA) vele toegewezen statussen (zoals In behandeling hebben of geautoriseerd) hebben. De status RMA wijst op de vooruitgang van een verzoek RMA dat door de gebruiker of de handelaar wordt opgeheven.

| Status | Beschrijving |
|--- |--- |
| [!UICONTROL Pending] | De aanvankelijke status die aan een RMA- verzoek wordt toegewezen wanneer het door een gebruiker op de storefront of door de handelaar in Admin wordt opgeheven. |
| [!UICONTROL Authorized] | Deze status wordt toegewezen aan RMA wanneer alle gevraagde punten door de handelaar in Admin voor de terugkeer worden toegelaten. |
| [!UICONTROL Partially Authorized] | Deze status wordt toegewezen aan RMA als om het even welke gevraagde punten zijn ontkend en andere producten worden toegelaten. |
| [!UICONTROL Denied] | Deze status wordt toegewezen aan RMA als alle gevraagde punten door de handelaar in Admin voor de winst worden verworpen. |
| [!UICONTROL Return Received] | Deze status wordt toegewezen door de handelaar aan RMA wanneer de gevraagde punten van de gebruiker worden ontvangen. |
| [!UICONTROL Return Partially Received] | Deze status wordt toegewezen door de handelaar aan RMA wanneer de gevraagde punten gedeeltelijk zijn teruggekeerd en sommige punten worden ontkend om te verwerken. |
| [!UICONTROL Approved] | Deze status wordt toegewezen door de handelaar aan RMA wanneer de gevraagde punten worden goedgekeurd om verder te verwerken. |
| [!UICONTROL Rejected] | Deze status wordt door de handelaar aan RMA toegewezen wanneer de gevraagde punten worden verworpen om verder te verwerken. |
| [!UICONTROL Processed and Closed] | Deze status wordt toegewezen door de handelaar aan RMA wanneer alle gevraagde punten worden goedgekeurd om verder te verwerken. |
| [!UICONTROL Closed] | Deze status wordt toegewezen door de handelaar aan RMA wanneer de gevraagde punten om voor terugkeer worden ontkend te verwerken. |

{style="table-layout:auto"}

## Een verzoek om terugkeer maken in de beheerder

Een handelaar kan een terugkeerverzoek namens de klant van Admin tot stand brengen. Klanten kunnen [een verzoek om terugkeer maken](rma-customer-experience.md) op de winkel van Adobe Commerce.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. Klik op **[!UICONTROL New Return Request]**.

1. Om een terugkeerverzoek tot stand te brengen, klik een orde met een `Complete` status.

1. Onder de _[!UICONTROL Return Information]_selecteert u de **[!UICONTROL Return Items]**tab.

1. Als u items wilt toevoegen die u wilt retourneren, klikt u op **[!UICONTROL Add Items]**.

1. Schakel het selectievakje voor het vereiste product in en klik op **[!UICONTROL Add Selected Product to returns]**.

1. Voor **[!UICONTROL Requested]**, voert u het aantal objecten in dat moet worden geretourneerd.

1. Set **[!UICONTROL Return Reason]** op een van de volgende wijzen:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   Als de reden voor het retourneren anders is dan de vermelde opties, kunt u uw eigen keuze invoeren als u de optie `Other` -optie.

1. Set **[!UICONTROL Item Condition]** op een van de volgende wijzen:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Set **[!UICONTROL Resolution]** op een van de volgende wijzen:

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. Als u een terugkeer wilt maken, klikt u op **[!UICONTROL Submit Returns]**.

   ![Aangevraagde RMA-items](./assets/return-item-request.png){width="600" zoomable="yes"}

   Het nieuwe RMA-verzoek wordt weergegeven op het tabblad **[!UICONTROL Returns]** pagina met een `Pending` status.
