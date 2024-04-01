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

Alle orders hebben een orderstatus die is gekoppeld aan een werkgebied in de orderverwerking [werkstroom](order-processing.md).\
Het verschil tussen orderstaten en orderstatussen is dat **[!UICONTROL order states]** worden via programmacode gebruikt. Ze zijn niet zichtbaar voor klanten of Admin-gebruikers. Zij bepalen de stroom van een orde, en welke verrichtingen voor een orde in een bepaalde staat mogelijk zijn.\
**[!UICONTROL Order statuses]** worden gebruikt om de status van een bestelling aan klanten en admingebruikers mee te delen.
U kunt extra ordestatussen tot stand brengen om zich aan uw operationele behoeften te richten. De status van bestellingen is handig om de voortgang buiten Adobe Commerce weer te geven, bijvoorbeeld het selecteren van bestellingen en de voortgang van de levering. Ze hebben geen invloed op de workflow voor het verwerken van bestellingen.\
Elke orderstatus is gekoppeld aan een orderstatus. Uw winkel heeft een reeks vooraf gedefinieerde instellingen voor de status van de bestelling en de status van de bestelling.

![Frames en statussen ordenen](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

Het statuut van elke orde wordt getoond in _Status_ kolom van de _Orders_ raster.

![Status van bestelling](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>Een gedeeltelijk terugbetaalde volgorde blijft in `Processing` status tot **_alles_** bestelde objecten (inclusief terugbetaalde objecten) worden verzonden. De orderstatus verandert niet in `Complete` totdat elk item in de bestelling is verzonden.

## Workflow voor de status Volgorde

![Workflow voor de status Volgorde](./assets/order-state-workflow.png)

## Vooraf gedefinieerde status

| Status van bestelling | Statuscode |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ontvangen | `received` | Deze status is de beginstatus voor bestellingen die worden geplaatst wanneer asynchrone orderplaatsing is ingeschakeld. |
| Vermoedelijke fraude | `fraud` | Soms worden via PayPal of een andere betaalgateway betaalde opdrachten gemarkeerd als _Vermoedelijke fraude_. Deze status betekent dat er geen factuur is uitgereikt voor de bestelling en dat het bevestigingsbericht ook niet is verzonden. |
| Verwerking | `processing` | Wanneer de status van nieuwe bestellingen is ingesteld op &#39;Verwerking&#39;, wordt _Alle items automatisch factureren_ deze optie is beschikbaar in de configuratie. Facturen worden niet automatisch gemaakt voor bestellingen die worden geplaatst met een creditcard, winkelcreditering, punten op beloning of andere methoden voor offlinebetaling. |
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

Naast de vooraf ingestelde instellingen voor de status van de volgorde kunt u ook uw eigen aangepaste instellingen voor de status van de volgorde maken, deze instellingen toewijzen aan de status van de bestelling en de status van de standaardvolgorde instellen voor de status van de bestelling. De ordestatus geeft de positie van de order binnen de workflow voor orderverwerking aan en de status van de order wijst een duidelijk vertaalbaar label toe aan de positie van de order. U hebt bijvoorbeeld een aangepaste orderstatus nodig, zoals `packaging"`, `backordered`of een status die specifiek is voor uw behoeften. U kunt een beschrijvende naam maken voor de aangepaste status en deze toewijzen aan de bijbehorende ordestatus in de workflow.

>[!NOTE]
>
>Alleen standaardwaarden voor de aangepaste orderstatus worden gebruikt in de workflow voor de volgorde. Aangepaste statuswaarden die niet als standaard zijn ingesteld, kunnen alleen worden gebruikt in de sectie Opmerkingen van de volgorde.

![Status van bestelling](./assets/order-status.png){width="700" zoomable="yes"}

### Een aangepaste orderstatus maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Create New Status]**.

   ![Nieuwe orderstatus maken](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Werk de _[!UICONTROL Order Status Information]_sectie:

   - Voer een **[!UICONTROL Status Code]** voor interne referentie. Het eerste teken moet een letter (a-z) zijn en de rest mag elke combinatie van letters en cijfers (0-9) zijn. Gebruik het onderstrepingsteken in plaats van een spatie.

   - Voor **[!UICONTROL Status Label]**, voert u een label in dat de statusinstelling in zowel Beheer als Store aangeeft.

1. In de _[!UICONTROL Store View Specific Labels]_in, voert u de benodigde labels in voor verschillende winkelweergaven.

1. Klik op **[!UICONTROL Save Status]**.

### Een orderstatus aan een staat toewijzen

1. Op de _Status van bestelling_ pagina, klikt u **[!UICONTROL Assign Status to State]**.

   ![Status toewijzen](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. Werk de **[!UICONTROL Assignment Information]** Ga als volgt te werk:

   - Kies de optie **[!UICONTROL Order Status]** die u wilt toewijzen. Ze worden vermeld op statuslabel.

   - Set **[!UICONTROL Order State]** op de plaats in de werkstroom waar de orderstatus thuishoort.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** lijst bevat de standaard toegewezen orderstatussen. Bijvoorbeeld de `Pending` de standaardorderstatus wordt weergegeven in plaats van de `New` statuswaarde van bestelling.

   - Als u van deze status de standaardstatus voor de status van de volgorde wilt maken, selecteert u de optie **[!UICONTROL Use Order Status as Default]** selectievakje.

     >[!NOTE]
     >
     >Alleen de standaardvolgordestatus wordt gebruikt in de workflow voor de volgorde. Niet-standaardstatussen kunnen alleen worden ingesteld in het dialoogvenster **[!UICONTROL Order Comments]** in de Admin.

   - Als u deze status zichtbaar wilt maken vanuit de winkel, selecteert u de optie **[!UICONTROL Visible On Storefront]** selectievakje.

   ![Status toewijzen aan status](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Status Assignment]**.

### Een bestaande orderstatus bewerken

1. In de _[!UICONTROL Order Status]_, opent u de statusrecord in de bewerkingsmodus.

1. Werk de statusinstellingen naar wens bij.

1. Klik op **[!UICONTROL Save Status]**.

### Een orderstatus uit een toegewezen status verwijderen

>[!NOTE]
>
>De toewijzing van een status kan niet ongedaan worden gemaakt als de status in gebruik is.

1. In de _[!UICONTROL Order Status]_niet-toegewezen raster.

1. In de _[!UICONTROL Action]_Klik in de rechterkolom van de rij op de knop **[!UICONTROL Unassign]**koppeling.

   Boven aan de werkruimte verschijnt het bericht dat de status van de bestelling niet is toegewezen. Hoewel het statuslabel van de volgorde nog steeds in de lijst staat, wordt het niet meer toegewezen aan een status. De instellingen voor de orderstatus kunnen niet worden verwijderd.

>[!NOTE]
>
>Als de status van de standaardvolgorde niet is toegewezen aan de status van de volgorde, _**een**_ orderstatus is _**automatisch instellen**_ als een standaardinstelling voor deze ordestatus.

## Melding

Klanten kunnen de status van hun bestellingen volgen op [RSS-feed](../merchandising-promotions/social-rss.md) als het voer van RSS van de Orde in de configuratie wordt toegelaten. Als deze optie is ingeschakeld, wordt op elke bestelling een koppeling naar de RSS-feed weergegeven.

### Statusmelding van order inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL RSS Feeds]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie.

1. Set **[!UICONTROL Customer Order Status Notification]** tot `Enable`.

   ![Kennisgeving van status van klant](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

### E-mailberichten voor nieuwe bestellingen configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales Emails]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Order]** sectie.

   ![Configuratie - Volgopties](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL New Order Confirmation Email Sender]** op een van de volgende wijzen:

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Kies de sjablonen die u voor elk type klant wilt gebruiken:

   - **[!UICONTROL New Order Confirmation Template]** - Kies een sjabloon die u wilt gebruiken voor klanten met een geregistreerde winkelaccount.
   - **[!UICONTROL New Order Confirmation Template for Guest]** - Kies een sjabloon die u wilt gebruiken voor gastklanten zonder geregistreerde winkelaccount.

1. Als u een andere persoon (bijvoorbeeld een bedrijfsmanager) op de hoogte wilt stellen van de nieuwe bestelling, voert u het e-mailadres in naar **[!UICONTROL Send Order Email Copy To]**.

   U kunt meerdere e-mailadressen toevoegen als meerdere ontvangers vereist zijn.

1. Stel de **[!UICONTROL Send Order Email Copy Method]** op een van de volgende wijzen:

   - `Bcc` - Er wordt slechts één e-mail over de nieuwe bestelling verzonden naar zowel de klant als de extra ontvanger, maar de klant ziet niet dat de e-mail die hij of zij heeft ontvangen ook naar de extra ontvanger is verzonden.
   - `Separate Email` - Er worden twee aparte e-mails verzonden: een naar de ontvanger en een naar de klant.

1. Klik op **[!UICONTROL Save Config]**.
