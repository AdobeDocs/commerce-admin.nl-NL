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

A _teruggekeerde handelsvergunning_ (RMA) kan aan klanten worden verleend die verzoeken om een punt voor vervanging of terugbetaling terug te keren. Doorgaans neemt de klant contact op met de handelaar om terugbetaling aan te vragen. Indien goedgekeurd, wordt een uniek aantal RMA toegewezen om het teruggekeerde product te identificeren. In de configuratie, kunt u of RMA voor alle producten toelaten of RMA voor slechts bepaalde producten toestaan. Het raster _[!UICONTROL Returns]_bevat een lijst met de huidige geretourneerde handelswijzigingsverzoeken (RMA&#39;s) en wordt gebruikt om nieuwe retourverzoeken in te voeren.

![ keert net ](./assets/return.png){width="600" zoomable="yes"} terug

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
| [!UICONTROL Action] | **[!UICONTROL View]** opent de terugkeer in uitgeeft wijze. |

{style="table-layout:auto"}

## RMA en retourworkflow

1. **ontvangt verzoek** - als [ ](rma-configure.md#enable-rmas-for-your-store) voor de storefront wordt toegelaten, zowel kunnen de geregistreerde klanten als de gasten om een RMA verzoeken. U kunt ook [ een verzoek RMA in Admin ](#create-a-return-request-in-the-admin) voorleggen.

2. **uitgegeven RMA** - na het overwegen van het verzoek, kunt u het gedeeltelijk, volledig machtigen, of het verzoek annuleren. Als u de terugzending toestaat en ermee akkoord gaat de terugzending te betalen, kunt u een bestelling van Admin met een gesteunde drager tot stand brengen.

3. **ontvangen Merchandies en verwerkte productterugkeer** - het volgende stroomdiagram beschrijft de operationele orde om het terugkeerproces te voltooien:

   ![ Werkschema van de Terugkeer van het Product ](./assets/workflow-customer-returns.png){width="500"}

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

Een handelaar kan een terugkeerverzoek namens de klant van Admin tot stand brengen. De klanten kunnen [ een terugkeerverzoek ](rma-customer-experience.md) op de storefront voor een opslag van Adobe Commerce tot stand brengen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. Klik op **[!UICONTROL New Return Request]**.

1. Als u een retouraanvraag wilt maken, klikt u op een bestelling met de status `Complete` .

1. Selecteer onder de sectie _[!UICONTROL Return Information]_de tab **[!UICONTROL Return Items]**.

1. Klik op **[!UICONTROL Add Items]** om items toe te voegen die u wilt retourneren.

1. Schakel het selectievakje voor het vereiste product in en klik op **[!UICONTROL Add Selected Product to returns]** .

1. Voer bij **[!UICONTROL Requested]** het aantal items in dat moet worden geretourneerd.

1. Stel **[!UICONTROL Return Reason]** in op een van de volgende opties:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   Als de reden voor de return anders is dan de vermelde keuzes, kunt u uw eigen keuzes invoeren als u de optie `Other` selecteert.

1. Stel **[!UICONTROL Item Condition]** in op een van de volgende opties:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Stel **[!UICONTROL Resolution]** in op een van de volgende opties:

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. Klik op **[!UICONTROL Submit Returns]** om een return te maken.

   ![ Gevraagde Punten RMA ](./assets/return-item-request.png){width="600" zoomable="yes"}

   Het nieuwe RMA-verzoek wordt weergegeven op de **[!UICONTROL Returns]** -pagina met de status `Pending` .
