---
title: Overbrengingen
description: Leer hoe u verzendrecords voor facturen maakt en verzendingen annuleert.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Overbrengingen

Het _[!UICONTROL Shipments]_-raster bevat de verzendrecord van alle facturen die zijn voorbereid voor verzending. Een ladingsverslag kan worden geproduceerd wanneer een orde [&#128279;](invoices.md) of later wordt gefactureerd.

Adobe Commerce en de Magento Open Source steunen gedeeltelijke en volledige ordeverzending, met extra opties beschikbaar bij [&#x200B; Inventory management &#x200B;](../inventory-management/introduction.md) en derdeuitbreidingen.

![&#x200B; het net van Verzendingen &#x200B;](./assets/shipments.png){width="600" zoomable="yes"}

## Kolombeschrijvingen

| Kolom of besturingselement | Beschrijving |
|--- |--- |
| [!UICONTROL Select] | Schakel het selectievakje in voor elk aanhalingsteken dat aan een handeling moet worden onderworpen, of gebruik het selectiegereedschap in de kolomkop. Opties: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Een uniek, opeenvolgend aantal dat wordt toegewezen wanneer een nieuwe lading voor het eerst wordt bewaard |
| [!UICONTROL Ship Date] | Verzenddatum |
| [!UICONTROL Order] | Uniek nummer van de bestelling |
| [!UICONTROL Order Date] | De datum en het tijdstip waarop de order is geplaatst |
| [!UICONTROL Ship-to Name] | De naam van de persoon aan wie de order is verzonden |
| [!UICONTROL Total Quantity] | Totale hoeveelheid te verzenden objecten |
| [!UICONTROL Action] | Weergeven opent de verzending in de bewerkingsmodus |

{style="table-layout:auto"}

Aanvullende kolommen:

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Order Status] | Hiermee wordt de status van de volgorde aangegeven |
| [!UICONTROL Purchased From] | Geeft de website-, opslag- en opslagweergave aan waar de volgorde is geplaatst |
| [!UICONTROL Customer Name] | De naam van de klant of koper die de bestelling heeft geplaatst |
| [!UICONTROL Email] | Het e-mailadres van een geregistreerde klant |
| [!UICONTROL Customer Group] | De naam van de klantengroep of gedeelde catalogus waaraan de klant is toegewezen |
| [!UICONTROL Billing Address] | De naam van de klant of koper die de bestelling heeft geplaatst |
| [!UICONTROL Shipping Address] | De naam van de persoon aan wie de order is verzonden |
| [!UICONTROL Payment Method] | De wijze van betaling die voor de opdracht moet worden gebruikt |
| [!UICONTROL Shipping Information] | De methode die moet worden gebruikt om de bestelling te verzenden |

{style="table-layout:auto"}

## Een verzending maken

Met de volgende instructies doorloopt u het proces voor het maken van een verzending in Adobe Commerce of Magento Open Source. Als u Inventory management hebt toegelaten, kunt u [&#x200B; willen herzien creeer de Verzendingen van meerdere Source &#x200B;](../inventory-management/shipments-create.md) en selecteer een bron (of plaats) en een hoeveelheid per lijnpunt te verzenden.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde in het raster en open deze.

1. Als de bestelling is betaald, gefactureerd en klaar is om te worden verzonden, klikt u op **[!UICONTROL Ship]** .

   De secties boven aan de verzending bevatten naam, adres en betalingsgegevens uit de verkooporder.

1. Vul elke sectie van het verzendformulier in met de instructies in de volgende secties.

### [!UICONTROL Items to Ship]

Wijzig voor elk regelitem in de volgorde de **[!UICONTROL Qty to Ship]** naar wens.

### [!UICONTROL Shipping Information]

**Methode 1:** Gebruikend de orde pagina

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Klik in de kolom **[!UICONTROL Action]** voor de geselecteerde volgorde op **[!UICONTROL View]** .

1. Klik op **[!UICONTROL Ship]**.

1. Blader omlaag naar het _[!UICONTROL Payment & Shipping Method]_-blok en klik op **[!UICONTROL Add Tracking Number]**.

1. Instellen **[!UICONTROL Carrier]** :

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Voer **[!UICONTROL Title]** en **[!UICONTROL Number]** in om de verzending te volgen.

**Methode 2:** Gebruikend de verzendingspagina

Deze methode is alleen toegestaan als de verzending van de bestelling al vanaf de bestelpagina is gemaakt.
U kunt de verzendgegevens en trackinggegevens naar wens wijzigen met de pagina voor rechtstreekse verzending:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. De verzending zoeken en openen in de bewerkingsmodus.

1. Schuif omlaag naar het _[!UICONTROL Payment & Shipping Method]_-blok.

1. Selecteer de **[!UICONTROL Carrier]** .

1. Voer een **[!UICONTROL Title]** in voor het pakket.

1. Voer de tekstspatiëring in **[!UICONTROL Number]** .

1. Klik op **[!UICONTROL Add]**.

1. Als u een e-mail met trackinggegevens naar de klant wilt verzenden, klikt u op **[!UICONTROL Send Tracking Information]** en bevestigt u de handeling.

   Als u de locatie van een willekeurige verzending wilt bijhouden, opent u de gewenste verzending in de bewerkingsmodus en klikt u op **[!UICONTROL Track this shipment]** .

   ![&#x200B; het verschepen en het Volgen Informatie &#x200B;](./assets/tracking-information.png){width="600" zoomable="yes"}

### Knoppen

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Sluit het nieuwe verzendformulier en keert terug naar de bestelling |
| **[!UICONTROL Submit Shipment]** | Voegt de zending voor de orde toe. |
| **[!UICONTROL Reset]** | Hiermee herstelt u de oorspronkelijke waarden van alle velden. |

{style="table-layout:auto"}

### Opmerkingen verzenden

1. Ga **Commentaren** voor de verzending in, indien nodig.

1. Wanneer de verzending klaar is, klik **voorleggen Verzending**.

## Opmerkingen instellen voor verzendingen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Selecteer onder _[!UICONTROL Sales]_&#x200B;de optie **[!UICONTROL Sales Email]**.

1. Breid de **sectie van de Commentaren van de Verzending** uit en wijzig de montages zoals nodig:

   ![&#x200B; de commentaarconfiguratie van de Verzending &#x200B;](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - De optie **[!UICONTROL Enabled]** is standaard ingesteld op `Yes` . Dit houdt in dat de e-mail naar een klant wordt verzonden wanneer een verzendopmerking wordt ingevoerd.

   - Selecteer voor **[!UICONTROL Shipment Comment Email Sender]** de persoon van wie de opmerkingsmail voor verzending is verzonden. Standaard zijn er vijf e-mailadressen.

   - Selecteer voor **[!UICONTROL Shipment Comment Email Template]** de sjabloon op basis van uw vereiste of selecteer de standaardoptie.

   - Kies voor **[!UICONTROL Shipment Comment Email Template for Guests]** de sjabloon die wordt gebruikt voor klanten die geen account in uw winkel hebben.

   - Voer voor **[!UICONTROL Shipment Comment Email Copy To]** de e-mailadressen in om een e-mailexemplaar met opmerkingen over de verzending te verzenden. Scheid meerdere e-mailadressen met een komma.

   - Selecteer bij **[!UICONTROL Shipment Comment Email Copy Method]** de methode `bcc` (blinde koolstofkopie) of `separate email copy` op basis van uw voorkeur.

1. Klik op **[!UICONTROL Save Config]**.

## Een verzending annuleren

Voordat een zending naar een vervoerder wordt verzonden, kan deze worden geannuleerd door de bestelling te openen en naar de lading te navigeren, op voorwaarde dat de vervoerder annuleringen ondersteunt. Sommige dragers beperken of beperken annuleringen na het boeken. UPS staat bijvoorbeeld annuleringen toe, maar vereist dat u 24 uur wacht nadat de verzending is geboekt. Als een transport wordt geannuleerd, kan de annulering niet worden teruggedraaid. De enige mogelijkheid is om de bestelling opnieuw te maken.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde in het raster.

1. In de _kolom van de Actie_, kies **[!UICONTROL View]**.

1. Kies **[!UICONTROL Shipments]** in het linkerdeelvenster.

   Als de verzending kan worden geannuleerd, wordt _[!UICONTROL Cancel Shipment]_&#x200B;weergegeven als een optie in de bovenste knopbalk.

1. Klik op **[!UICONTROL Cancel Shipment]**.

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.

De status van de verzending verandert in `Canceled` . Als de vervoerder geen annuleringen ondersteunt, wordt een foutbericht weergegeven waarin wordt uitgelegd waarom de verzending niet kan worden geannuleerd.

## Beschrijvingen van verzendvelden

### [!UICONTROL Shipping Information]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Carrier] | De naam van de geselecteerde vervoerder |
| [!UICONTROL Title] | Een beschrijvende naam die door de vervoerder aan het pakket is toegewezen. |
| [!UICONTROL Number] | Het gekoppelde volgnummer dat aan het pakket is toegewezen. |
| [!UICONTROL Action] | ![&#x200B; Trashcan pictogram &#x200B;](../assets/icon-delete-trashcan-solid.png) - schrapt de pakketinformatie van het ladingsverslag. |
| [!UICONTROL Add] | Voeg nog een pakket toe aan de verzending. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Origin Location] | Geeft een lijst met beschikbare locaties weer. |
| [!UICONTROL International] | Indien gecontroleerd, identificeert de zending als een internationale zending. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Description] | De beschrijving van het item. |
| [!UICONTROL SKU] | De voorraadbewaareenheid van het artikel. |
| [!UICONTROL Weight] | Het gewicht van het object. |
| [!UICONTROL Qty Ordered] | De hoeveelheid van het item dat is besteld. |
| [!UICONTROL Qty Shipped] | De hoeveelheid objecten die is verzonden. |
| [!UICONTROL Qty Packed] | Het aantal items dat in dit pakket is opgenomen. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Comments] | Opmerkingen over de zending zijn bestemd voor intern gebruik. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Download het etiket van het vervoerspakket. Grootte: A6 (105 x 148 mm; 4,1 x 5,6 inch) |

{style="table-layout:auto"}
