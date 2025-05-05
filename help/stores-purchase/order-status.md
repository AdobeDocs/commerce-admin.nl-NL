---
title: Status van bestelling
description: Leer over de vooraf bepaalde ordestatus en hoe te om de statussen van de douaneorde te bepalen om zich aan uw operationele behoeften te richten.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Status van bestelling

Alle orden hebben een ordestatus die met een stadium in het orde verwerkt [ werkschema ](order-processing.md) wordt geassocieerd.\
Het verschil tussen orderstaten en orderstatussen is dat **[!UICONTROL order states]** programmatisch wordt gebruikt. Ze zijn niet
zichtbaar voor klanten of Admin-gebruikers. Zij bepalen de stroom van een orde, en welke verrichtingen mogelijk zijn voor een
orde in een bepaalde staat.\
**[!UICONTROL Order statuses]** worden gebruikt om de status van een bestelling door te geven aan klanten en beheerders.
U kunt extra ordestatussen tot stand brengen om zich aan uw operationele behoeften te richten. De status van bestellingen is handig om weer te geven
vooruitgang buiten Adobe Commerce, bijvoorbeeld het selecteren en leveren van bestellingen. Zij hebben geen invloed op de orde
verwerkingsworkflow.\
Elke orderstatus is gekoppeld aan een orderstatus. Uw winkel heeft een set vooraf gedefinieerde bestelstatus en
instellingen voor de ordestatus.

![ de staten en de statussen van de Orde ](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

De status van elke orde wordt getoond in de _kolom van de Status_ van het _3&rbrace; net van Orden &lbrace;._

![ Status van de Orde ](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>Een gedeeltelijk teruggegeven orde blijft in `Processing` status tot **_alle_** bevolen punten (met inbegrip van teruggegeven punten) worden verscheept. De status van de bestelling verandert niet in `Complete` totdat elk item in de bestelling is verzonden.

## Workflow voor de status Volgorde

![ de staatswerkschema van de Orde ](./assets/order-state-workflow.png)

## Vooraf gedefinieerde status

| Status van bestelling | Statuscode |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ontvangen | `received` | Deze status is de beginstatus voor bestellingen die worden geplaatst wanneer asynchrone orderplaatsing is ingeschakeld. |
| Vermoedelijke fraude | `fraud` | Soms worden de orden die via PayPal of een andere betaalgateway worden betaald duidelijk als _Vermoedelijke Fraude_. Deze status betekent dat er geen factuur is uitgereikt voor de bestelling en dat het bevestigingsbericht ook niet is verzonden. |
| Verwerking | `processing` | Wanneer het statuut van nieuwe orden aan &quot;Verwerking&quot;wordt geplaatst, wordt de _automatisch Alle Punten van de Factuur_ optie beschikbaar in de configuratie. Facturen worden niet automatisch gemaakt voor bestellingen die worden geplaatst met een creditcard, winkelcreditering, punten op beloning of andere methoden voor offlinebetaling. |
| In behandeling | `pending_payment` | Deze status wordt gebruikt als de bestelling wordt gemaakt en PayPal of een vergelijkbare betalingsmethode wordt gebruikt. Dit betekent dat de klant naar de website van de betaalgateway werd geleid, maar er zijn nog geen retourgegevens ontvangen. Deze status verandert wanneer de klant betaalt. |
| Betaalcontrole | `payment_review` | Deze status wordt weergegeven wanneer PayPal-betalingscontrole is ingeschakeld. |
| In behandeling | `pending` | Deze status geeft aan dat er geen factuur en verzendingen zijn ingediend. |
| In de wachtstand | `holded` | Deze status kan alleen handmatig worden toegewezen. U kunt om het even welke orde op greep zetten. |
| Voltooid | `complete` | Deze status houdt in dat de bestelling wordt gemaakt, betaald en naar de klant wordt verzonden. |
| Gesloten | `closed` | Deze status geeft aan dat aan een bestelling een creditnota is toegewezen en dat de klant een terugbetaling heeft ontvangen. |
| Geannuleerd | `canceled` | Deze status wordt handmatig toegewezen in de beheerder of, voor sommige betaalgateways, wanneer de klant niet binnen de opgegeven tijd betaalt. |
| Geweigerd | `rejected` | Deze status houdt in dat een bestelling is geweigerd tijdens asynchrone verwerking van bestellingen. Dit gebeurt wanneer een fout tijdens asynchrone ordetelling voorkomt. |
| PayPal geannuleerd terugdraaien | `paypay_canceled_reversal` | Deze status betekent dat PayPal de terugdraaiing heeft geannuleerd. |
| PayPal in behandeling | `pending_paypal` | Deze status betekent dat de bestelling is ontvangen door PayPal, maar dat de betaling nog niet is verwerkt. |
| PayPal omgedraaid | `paypal_reversed` | Deze status betekent dat PayPal de transactie heeft teruggedraaid. |

{style="table-layout:auto"}

## Status van aangepaste bestelling

Naast de vooraf ingestelde instellingen voor de status van de volgorde kunt u ook uw eigen aangepaste instellingen voor de status van de volgorde maken, deze instellingen toewijzen aan de status van de bestelling en de status van de standaardvolgorde instellen voor de status van de bestelling. De ordestatus geeft de positie van de order binnen de workflow voor orderverwerking aan en de status van de order wijst een duidelijk vertaalbaar label toe aan de positie van de order. U hebt bijvoorbeeld een aangepaste orderstatus nodig, zoals `packaging"` , `backordered` , of een status die specifiek is voor uw behoeften. U kunt een beschrijvende naam maken voor de aangepaste status en deze toewijzen aan de bijbehorende ordestatus in de workflow.

>[!NOTE]
>
>Alleen standaardwaarden voor de aangepaste orderstatus worden gebruikt in de workflow voor de volgorde. Aangepaste statuswaarden die niet als standaard zijn ingesteld, kunnen alleen worden gebruikt in de sectie Opmerkingen van de volgorde.

![ de montages van de Status van de Orde ](./assets/order-status.png){width="700" zoomable="yes"}

### Een aangepaste orderstatus maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Create New Status]** .

   ![ creeer de Nieuwe Status van de Orde ](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Werk de sectie _[!UICONTROL Order Status Information]_&#x200B;bij:

   - Voer een **[!UICONTROL Status Code]** in voor interne referentie. Het eerste teken moet een letter (a-z) zijn en de rest mag elke combinatie van letters en cijfers (0-9) zijn. Gebruik het onderstrepingsteken in plaats van een spatie.

   - Voer bij **[!UICONTROL Status Label]** een label in dat de status identificeert die zowel in Admin als in de winkel is ingesteld.

1. Voer in de sectie _[!UICONTROL Store View Specific Labels]_&#x200B;de labels in die nodig zijn voor verschillende winkelweergaven.

1. Klik op **[!UICONTROL Save Status]**.

### Een orderstatus aan een staat toewijzen

1. Voor de _pagina van de Status van de Orde_, klik **[!UICONTROL Assign Status to State]**.

   ![ wijs Status ](./assets/store-status-assign-status.png){width="600" zoomable="yes"} toe

1. Werk de sectie **[!UICONTROL Assignment Information]** als volgt bij:

   - Kies de **[!UICONTROL Order Status]** die u wilt toewijzen. Ze worden vermeld op statuslabel.

   - Stel **[!UICONTROL Order State]** in op de plaats in de workflow waar de orderstatus thuishoort.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** bevat de standaardstatus van de toegewezen volgorde. De status van de standaardvolgorde van `Pending` wordt bijvoorbeeld weergegeven in plaats van de statuswaarde van de `New` -volgorde.

   - Als u van deze status de standaardstatus voor de status van de volgorde wilt maken, schakelt u het selectievakje **[!UICONTROL Use Order Status as Default]** in.

     >[!NOTE]
     >
     >Alleen de standaardvolgordestatus wordt gebruikt in de workflow voor de volgorde. Niet-standaardstatussen kunnen alleen worden ingesteld in de sectie **[!UICONTROL Order Comments]** in Admin.

   - Schakel het selectievakje **[!UICONTROL Visible On Storefront]** in als u deze status vanuit de winkel zichtbaar wilt maken.

   ![ wijs Status aan Staat ](./assets/order-status-assign-state.png){width="600" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save Status Assignment]**.

### Een bestaande orderstatus bewerken

1. Open in het _[!UICONTROL Order Status]_-raster de statusrecord in de bewerkingsmodus.

1. Werk de statusinstellingen naar wens bij.

1. Klik op **[!UICONTROL Save Status]**.

### Een orderstatus uit een toegewezen status verwijderen

>[!NOTE]
>
>De toewijzing van een status kan niet ongedaan worden gemaakt als de status in gebruik is.

1. Zoek in het _[!UICONTROL Order Status]_-raster naar de orderstatusrecord die niet is toegewezen.

1. Klik in de kolom _[!UICONTROL Action]_&#x200B;helemaal rechts van de rij op de koppeling **[!UICONTROL Unassign]**.

   Boven aan de werkruimte verschijnt het bericht dat de status van de bestelling niet is toegewezen. Hoewel het statuslabel van de volgorde nog steeds in de lijst staat, wordt het niet meer toegewezen aan een status. De instellingen voor de orderstatus kunnen niet worden verwijderd.

>[!NOTE]
>
>Als de status van de standaardorde van de ordestatus unassigned is, _&#x200B;**wordt een andere**&#x200B;_ ordestatus _&#x200B;**automatisch geplaatst**&#x200B;_ als gebrek voor deze ordestatus.

## Melding

De klanten kunnen het statuut van hun orden door [ voer van RSS ](../merchandising-promotions/social-rss.md) volgen als het voer van RSS van de Orde in de configuratie wordt toegelaten. Als deze optie is ingeschakeld, wordt op elke bestelling een koppeling naar de RSS-feed weergegeven.

### Statusmelding van order inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL RSS Feeds]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie uit.

1. Stel **[!UICONTROL Customer Order Status Notification]** in op `Enable` .

   ![ Bericht van de Status van de Orde van de Klant ](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### E-mailberichten voor nieuwe bestellingen configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Sales Emails]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie uit.

   ![ Configuratie - de opties van de Orde ](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL New Order Confirmation Email Sender]** in op een van de volgende opties:

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Kies de sjablonen die u voor elk type klant wilt gebruiken:

   - **[!UICONTROL New Order Confirmation Template]** - Kies een sjabloon die u wilt gebruiken voor klanten met een geregistreerde winkelaccount.
   - **[!UICONTROL New Order Confirmation Template for Guest]** - Kies een sjabloon die u wilt gebruiken voor gastklanten zonder geregistreerde winkelaccount.

1. Als u een andere persoon (zoals een bedrijfsmanager) op de hoogte wilt stellen van de nieuwe bestelling, voert u het e-mailadres in naar **[!UICONTROL Send Order Email Copy To]** .

   U kunt meerdere e-mailadressen toevoegen als meerdere ontvangers vereist zijn.

1. Stel de **[!UICONTROL Send Order Email Copy Method]** in op een van de volgende opties:

   - `Bcc` - Er wordt slechts één e-mail over de nieuwe bestelling verzonden naar zowel de klant als de extra ontvanger, maar de klant ziet niet dat het e-mailbericht dat hij of zij heeft ontvangen ook naar de extra ontvanger is verzonden.
   - `Separate Email` - Er worden twee aparte e-mails verzonden: een naar de ontvanger en een naar de klant.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
