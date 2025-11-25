---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] van Commerce Admin.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '4146'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![&#x200B; Vlak Tarief &#x200B;](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-flat-rate) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Wanneer toegelaten, verschijnt het Vaste Tarief als optie in de _Schatting Verzending en de sectie van de Belasting_ van het winkelwagentje, en in de _Verschepende_ sectie tijdens controle. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | De naam die tijdens het afrekenen voor deze verzendmethode wordt gebruikt. |
| [!UICONTROL Method Name] | Winkelweergave | Een naam die de berekeningsmethode beschrijft die wordt gebruikt om een schatting van de verzendkosten te maken. De naam van de methode staat naast de berekende geschatte snelheid in het winkelwagentje. De standaardwaarde is `Fixed` . |
| [!UICONTROL Type] | Website | Beschrijft het type berekening dat wordt gebruikt om het vaste tarief te bepalen. Opties: <br/>**`None`**- Er wordt geen berekening gebruikt. Hiermee stelt u de vaste snelheid in op nul. Dit is het equivalent van gratis verzending.<br/>**`Per Order`** - Hiermee wordt één vaste snelheid in rekening gebracht voor de volledige bestelling. <br/>**`Per Item`**- Hiermee wordt voor elk artikel in het winkelwagentje een afzonderlijke vaste prijs in rekening gebracht. Het tarief wordt vermenigvuldigd met het aantal punten in het karretje, zelfs als de totale hoeveelheid een combinatie van verschillende posten omvat. |
| [!UICONTROL Price] | Website | De prijs die je de klant in rekening brengt voor vaste verzendkosten. |
| [!UICONTROL Calculate Handling Fee] | Website | Bepaalt hoe de behandelingskosten worden berekend, indien inbegrepen. Opties: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Website | Voer het bedrag in dat moet worden aangerekend voor een verpakkingskosten op basis van de methode die u hebt gekozen voor de berekening van het bedrag. Als de vergoeding bijvoorbeeld op een vaste vergoeding is gebaseerd, voert u het bedrag in als een decimaal, bijvoorbeeld 4,90. Als de behandelingskosten echter zijn gebaseerd op een percentage van de bestelling, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de volgorde in rekening brengt, voert u de waarde in als `.06` . |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Een bericht dat verschijnt als een klant Plat Tarief kiest, maar om één of andere reden is de methode niet beschikbaar. |
| [!UICONTROL Ship to Applicable Countries] | Website | Identificeert de landen waar je vaste verzendkosten aanbiedt. Opties: <br/>**`All Allowed Countries`**- Klanten uit elk land dat in de winkelconfiguratie is opgegeven, kunnen gebruikmaken van vaste verzendkosten.<br/>**`Specific Countries`** - Klanten uit alleen bepaalde landen kunnen gebruikmaken van vaste verzendkosten. |
| [!UICONTROL Ship to Specific Countries] | Website | Identificeert elk land waar de klanten de Vaste Verzending van het Tarief kunnen gebruiken. |
| [!UICONTROL Show Method if Not Applicable] | Website | Hiermee wordt bepaald of Platte snelheid tijdens het uitchecken wordt weergegeven als de methode niet van toepassing is op de aankoop. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin Platte snelheid wordt weergegeven wanneer dit tijdens het uitchecken wordt vermeld met andere leveringsmethoden. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![&#x200B; Vrij die &#x200B;](./assets/delivery-methods-free-shipping.png)<!-- zoom --> verscheept

<!-- [Free Shipping](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-free) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Als deze optie is ingeschakeld, wordt Gratis verzending tijdens het afrekenen weergegeven als een optie in de sectie Verzending. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | De naam die tijdens het afrekenen voor deze verzendmethode wordt gebruikt. |
| Naam methode | Winkelweergave | Een naam die de berekeningsmethode beschrijft die wordt gebruikt om een schatting van de verzendkosten te maken. De naam van de methode staat naast de berekende geschatte snelheid in het winkelwagentje. De standaardwaarde is `Free` . |
| Minimumbedrag bestelling | Website | De minimale aanschaf die vereist is om Free Shipping toe te passen op een bestelling. |
| Inclusief BTW op bedrag | Website | Hiermee wordt bepaald of de belasting is opgenomen in de berekening van het minimumorderbedrag. Opties: <br/>**ja** - de Belasting is inbegrepen wanneer het berekenen van het Minimumbedrag van de Orde (Subtotaal + Belasting - Korting).<br/>**Nr** - de Belasting is niet inbegrepen belasting wanneer het berekenen van het Minimumbedrag van de Orde (Subtotaal - Korting). |
| Foutbericht weergeven | Winkelweergave | Een bericht dat wordt weergegeven als een klant Free Shipping kiest, maar om welke reden dan ook is de methode niet beschikbaar. |
| Schip naar landen van toepassing | Website | Identificeert de landen waar je Gratis verzending aanbiedt. Opties: <br/>**Alle Toegestane Landen** - de Klanten van om het even welk land dat in de opslagconfiguratie wordt gespecificeerd kunnen Vrije Verzending gebruiken. <br/>**Specifieke Landen** - de Klanten van slechts specifieke landen kunnen de Vrije Verzending gebruiken. |
| Schip naar specifieke landen | Website | Identificeert elk land waar klanten de Gratis Verzending kunnen gebruiken. |
| Methode tonen indien niet van toepassing | Website | Hiermee bepaalt u of Gratis verzending tijdens het afrekenen wordt weergegeven als de methode niet van toepassing is op de aankoop. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin Free Shipping wordt weergegeven wanneer deze bij andere leveringsmethoden wordt aangeboden tijdens het afrekenen. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![&#x200B; Tarieven van de Lijst &#x200B;](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-table-rate) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Als Tabeltarieven zijn ingeschakeld, wordt deze weergegeven als een optie in de sectie Schatting van verzending en belasting van het winkelwagentje en in de sectie Verzending tijdens het afrekenen. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | De naam die tijdens het afrekenen voor deze verzendmethode wordt gebruikt. |
| Naam methode | Winkelweergave | Een naam die de berekeningsmethode beschrijft die wordt gebruikt om een schatting van de verzendkosten te maken. De naam van de methode staat naast de berekende geschatte snelheid in het winkelwagentje. De standaardwaarde is `Table Rate` . |
| [!UICONTROL Condition] | Website | Hiermee bepaalt u de voorwaarde waarop de berekening wordt gebaseerd. De indeling van het CSV-bestand dat wordt geüpload, is specifiek voor elke voorwaarde. Opties: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Website | Hiermee wordt bepaald of virtuele producten, waarvoor geen verzending vereist is, worden opgenomen in de berekening van de tabeltarieven. |
| [!UICONTROL Calculate Handling Fee] | Website | Bepaalt hoe de behandelingskosten worden berekend, indien inbegrepen. Opties: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Website | Het bedrag aan kosten dat aan de verzendkosten wordt toegevoegd om de kosten van de afhandeling van de zending te dekken. Voer de waarde in als decimaal. Als de vergoeding bijvoorbeeld op een percentage is gebaseerd, voert u 0,06 in plaats van 6 % in. Voer `6.00` in voor een vast bedrag. |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Een bericht dat verschijnt als een klant de Tarieven van de Lijst kiest, maar om wat reden is de methode niet beschikbaar. |
| [!UICONTROL Ship to Applicable Countries] | Website | Hiermee geeft u aan in welke landen je verzendkosten voor tabeltarieven aanbiedt. Opties: <br/>**`All Allowed Countries`**- Klanten uit elk land dat in de winkelconfiguratie is opgegeven, kunnen gebruikmaken van de verzending van tabeltarieven.<br/>**`Specific Countries`** - Klanten uit alleen bepaalde landen kunnen gebruikmaken van de verzending van tabeltarieven. |
| [!UICONTROL Ship to Specific Countries] | Website | Identificeert elk land waar de klanten het verschepen van het Tarief van de Lijst kunnen gebruiken. |
| [!UICONTROL Show Method if Not Applicable] | Website | Hiermee wordt bepaald of Tabeltarieven tijdens het afrekenen als optie worden weergegeven als de methode niet van toepassing is op de aankoop. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin Tabeltarieven worden weergegeven wanneer deze bij andere leveringsmethoden worden vermeld tijdens het afrekenen. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![&#x200B; In-Store Levering &#x200B;](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-in-store-delivery) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Wanneer toegelaten, in-store kan de levering als optie in de _Schatting Verzending en de sectie van de Belasting_ van het winkelwagentje, en in de _Verschepende_ sectie tijdens controle verschijnen. Opties: `Yes` / `No` |
| [!UICONTROL Method Name] | Winkelweergave | Een naam die de ophaalfunctie in de winkel identificeert als een verzendmethode. Deze waarde wordt weergegeven als het label van een tab boven aan de pagina Verzendkosten en in de tabel met beschikbare verzendmethoden onder aan dezelfde pagina. De standaardwaarde is `In-store Delivery` . |
| [!UICONTROL Title] | Winkelweergave | De naam die tijdens het afrekenen voor deze verzendmethode wordt gebruikt. |
| [!UICONTROL Price] | Website | De prijs die u de klant aanrekent voor het ophalen in de winkel. |
| [!UICONTROL Search Radius] | Website | De straal in km die moet worden gebruikt bij het zoeken naar ophaallocaties. |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Een bericht dat wordt weergegeven wanneer een klant in-store oppikken selecteert, maar de leveringsmethode niet beschikbaar is. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![&#x200B; de Montages van de Rekening van UPS REST &#x200B;](./assets/delivery-methods-ups1.png)<!-- zoom -->

![&#x200B; de Montages van de Rekening van UPS XML &#x200B;](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings]https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Website | Hiermee bepaalt u of UPS tijdens het afrekenen beschikbaar is voor klanten als verzendmethode. Opties: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Website | Hiermee bepaalt u of UPS beschikbaar is voor klanten als verzendmethode voor een RMA. Opties: `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Winkelweergave | Geeft aan dat de account United Parcel Service live is. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | De naam die tijdens het afrekenen voor deze verzendmethode wordt gebruikt. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Website | Voor UPS REST-service worden de volgende URL&#39;s weergegeven die vereist zijn om JSON-gegevens te verzenden: Gateway URL, Tracking URL, Shipping URL. Gebruik ofwel de sandbox of de eindpunten van de productie volgens de instelling voor Live account. |
| [!UICONTROL Mode] | Website | Bepaalt de wijze van transmissie die voor gegevens wordt gebruikt die naar het systeem UPS worden verzonden. Opties: <br/>**`Development`**- UPS controleert niet of gegevens die van de Commerce-server zijn ontvangen, via SSL zijn verzonden.<br/>**`Live`** - UPS controleert of gegevens die van de Commerce-server zijn ontvangen, via een SSL (Secure Socket Layer) worden verzonden. |
| Gebruikersnaam | Website | Uw client-id voor UPS-verzendaccount. |
| [!UICONTROL Origin of the Shipment] | Website | (Alleen UPS REST) Het land of de regio waar de verzending van het product afkomstig is. |
| [!UICONTROL Password] | Winkelweergave | Uw UPS-verzendaccount clientgeheim. |

{style="table-layout:auto"}

![&#x200B; Informatie van het Pakket UPS &#x200B;](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information]https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Website | (Alleen UPS REST) Hiermee schakelt u speciale tarieven in of uit, afhankelijk van uw overeenkomst met UPS. Opties: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Website | Hiermee bepaalt u hoe gewicht wordt berekend voor overbrengingen met meerdere pakketten. Opties: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Website | (Alleen UPS-REST) Het uit zes tekens bestaande UPS-verzendnummer is vereist om te kunnen verwijzen naar overeengekomen tarieven. |
| [!UICONTROL Container] | Website | Hiermee stelt u het containertype in dat wordt gebruikt voor het verpakken van verzendingen. Opties: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Website | Hiermee stelt u de standaardmaateenheid voor productgewicht in uw winkel in. Zie [&#x200B; Afdrukgewicht &#x200B;](../../stores-purchase/carriers.md#dimensional-weight) voor extra informatie. |
| [!UICONTROL Tracking URL] | Website | (Alleen UPS REST) De URL van UPS die wordt gebruikt om pakketten bij te houden. Gebruik `https://onlinetools.ups.com/api/track` voor Productie OF `https://wwwcie.ups.com/api/track` voor Sandbox-instelling. |
| [!UICONTROL Destination Type] | Website | Hiermee stelt u het standaardtype van de verzendbestemming in. Opties: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Website | Hiermee stelt u het maximumgewicht in dat een pakket kan krijgen zoals opgegeven door UPS. Als de bestelde producten het maximale pakketgewicht overschrijden, is deze verzendoptie niet beschikbaar. Volgens [&#x200B; UPS.com &#x200B;](https://www.ups.com/us/en/global.page), kunnen de pakketten 150 lbs (70 kg) Controle met uw verzendende drager niet overschrijden om het maximumgewicht te verifiëren. |
| [!UICONTROL Pickup Method] | Website | Hiermee stelt u de ophaalmethode voor UPS in. Opties: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Website | Hiermee stelt u het minimumgewicht in dat een pakket kan hebben zoals opgegeven door UPS. Als de bestelde producten minder wegen dan het minimumpakketgewicht, is deze verzendoptie niet beschikbaar. Neem contact op met de vervoerder om het minimumgewicht te controleren. |
| [!UICONTROL Calculate Handling Fee] | Website | Hiermee stelt u de berekeningsmethode voor de behandelingskosten in voor het verzenden van tabeltarieven. Opties: <br>**`Fixed`**- De verwerkingskosten zijn een vast tarief.<br>**`Percent`** - De verwerkingskosten worden toegepast als een percentage van het orderbedrag. |
| [!UICONTROL Handling Applied] | Website | Geeft aan of behandelingskosten worden toegepast op elke bestelling of op elk pakket binnen een bestelling. |
| [!UICONTROL Handling Fee] | Website | Hiermee stelt u de afhandeling in die bij de verzendprijs wordt inbegrepen. De verwerkingskosten kunnen worden vastgesteld als een vast bedrag of als een percentage. <br/><br/>**_Note:_** Als het typen van een percentagehoeveelheid, gebruik het decimale formaat `0.25` voor 25%. |

{style="table-layout:auto"}

![&#x200B; UPS Toegestane Methoden &#x200B;](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods]https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Website | Geeft de toegestane verzendmethoden voor UPS aan die aan klanten worden aangeboden. De verzendkosten worden berekend op basis van de geselecteerde verzendmethode. |
| [!UICONTROL Free Method] | Website | Geeft aan welke methode wordt gebruikt voor de methode voor gratis verzending via UPS. Kies Geen als u de optie voor gratis verzending wilt uitschakelen. <br/><br/>**_Note:_** Deze methode is gelijkaardig aan basis [&#x200B; Vrij die &#x200B;](../../stores-purchase/shipping-free.md) verscheept, nochtans verschijnt het als UPS het verschepen optie tijdens controle. |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Hiermee bepaalt u of gratis verzending wordt toegepast wanneer het orderbedrag de drempel voor gratis verzending overschrijdt. Opties: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Hiermee stelt u het minimale totale bedrag in dat een bestelling moet bereiken om in aanmerking te komen voor gratis verzending. |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Het foutbericht dat wordt weergegeven wanneer deze verzendmethode om welke reden dan ook niet beschikbaar is. |

{style="table-layout:auto"}

![&#x200B; Toepasselijke Landen van UPS en Andere Montages &#x200B;](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings]https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Website | Geeft aan welk land klanten deze verzendmethode mogen gebruiken. Opties: <br/>**`All Allowed Countries`**- de Klanten van alle [&#x200B; landen &#x200B;](../../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze het verschepen methode gebruiken.<br/>**`Specific Countries`** - Nadat u deze optie hebt gekozen, wordt de lijst [!UICONTROL Ship to Specific Countries] weergegeven. Selecteer elk land in de lijst waar deze verzendmethode kan worden gebruikt. |
| [!UICONTROL Show Method if Not Applicable] | Website | Hiermee bepaalt u of UPS altijd wordt weergegeven als een verzendoptie tijdens het afrekenen. Opties: <br/>**`Yes`**- UPS wordt altijd weergegeven als een verzendoptie tijdens het uitchecken, zelfs als dit niet van toepassing is op de bestelling.<br/>**`No`** - UPS wordt alleen als een verzendoptie weergegeven tijdens het afrekenen als dit van toepassing is op de bestelling. (Bijvoorbeeld, als het ordegewicht de maximumgewichtshoeveelheid overschrijdt.) |
| [!UICONTROL Debug] | Website | Specificeert als de gegevenstransmissies tussen uw opslag en UPS het systeem voor het zuiveren worden geregistreerd. Tenzij er een probleem is dat moet worden bijgehouden en geregistreerd, moet deze optie worden ingesteld op `No` . |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin UPS wordt weergegeven wanneer UPS tijdens het uitchecken wordt vermeld met andere leveringsmethoden. Voer `0` in voor de bovenkant van de lijst. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| Ingeschakeld voor Afhandeling | Website | Hiermee bepaalt u of USPS tijdens het afrekenen beschikbaar is voor klanten als verzendmethode. Opties: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Website | De URL die wordt gebruikt om verbinding te maken met het USPS-systeem om de verzendkosten dynamisch op te halen. |
| [!UICONTROL Secure Gateway URL] | Website | De veilige URL die wordt gebruikt om via SSL (Secure Socket Layer) verbinding te maken met het USPS-systeem om de verzendsnelheden dynamisch op te halen. |
| [!UICONTROL Title] | Winkelweergave | De titel van deze verzendoptie zoals deze wordt weergegeven in het winkelwagentje. |
| [!UICONTROL User ID] | Website | Je gebruikersnaam van de Verzendaccount van USPS. |
| [!UICONTROL Password] | Website | Wachtwoord voor verzendaccount van USPS. |
| [!UICONTROL Mode] | Website | Bepaalt de wijze van transmissie die voor gegevens wordt gebruikt die naar het systeem USPS worden verzonden. Opties zijn: <br/>**`Development`**- USPS controleert niet of gegevens die van de Commerce-server zijn ontvangen, via SSL zijn verzonden.<br/>**`Live`** - USPS controleert of gegevens die van de Commerce-server zijn ontvangen, via een SSL (Secure Socket Layer) worden verzonden. |

{style="table-layout:auto"}

De volgende gebieden zijn beschikbaar slechts als u het [&#x200B; de kwaliteitsflard van de Migratie van de REST API van USPS &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) hebt toegepast. Deze patch maakt ondersteuning mogelijk voor de USPS API&#39;s, een REST-gebaseerd platform dat de webtools-API&#39;s vervangt. Voor details, zie [&#x200B; de veroudering van de Hulpmiddelen API van het Web van 0&rbrace; USPS.](../../stores-purchase/carriers.md)

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL USPS Type] | Website | Kies **USPS Rest APIs** of **de Hulpmiddelen API van het Web van USPS** wordt gebaseerd op welke zal u gebruiken. |
| [!UICONTROL Consumer Key] | Website | Uw client-id voor USPS-verzendaccount voor REST API. |
| [!UICONTROL Consumer Secret] | Website | Uw USPS Verzendaccount Client Secret Key for REST API. |
| [!UICONTROL Account Type] | Website | Type USPS-betaalrekening. Opties: `"EPS"` (Enterprise Payment System) of `"PERMIT"` (Permit Imprint) voor REST API. <br/><br/>**_Note:_** Dit gebied is facultatief; nochtans, wordt het vereist om de verwezenlijking van het verschepende etiket toe te laten. |
| [!UICONTROL Pricing Options] | Website | De Prijsopties van USPS: **Detailhandel** of **Commercieel**. Heeft invloed op de toegepaste verzendkosten. Het gebrek is **Commercieel** voor REST API. |
| [!UICONTROL Account Number] | Website | Uw USPS **rekeningsaantal**, dat voor betaling voor REST API wordt gebruikt.  <br/><br/>**_Note:_** Dit gebied is facultatief; nochtans, wordt het vereist om de verwezenlijking van het verschepende etiket toe te laten. |
| [!UICONTROL Customer Registration Identifier(CRID)] | Website | Een Klantenregistratie-identificatienummer (CRID) is een door USPS gegenereerde numerieke code die een bedrijf op een locatie voor de REST API uniek identificeert.  <br/><br/>**_Note:_** Dit gebied is facultatief; nochtans, wordt het vereist om de verwezenlijking van het verschepende etiket toe te laten. |
| [!UICONTROL Mailer Identifier(MID)] | Website | De server-id (MID) is een veld binnen de streepjescode voor intelligente e-mail dat wordt gebruikt om mailders te identificeren. MID&#39;s worden door de USPS toegewezen aan een Mail Owner, Mailing Agent of een andere serviceprovider die ze opvraagt voor REST API.  <br/><br/>**_Note:_** Dit gebied is facultatief; nochtans, wordt het vereist om de verwezenlijking van het verschepende etiket toe te laten. |
| [!UICONTROL Manifest MID] | Website | De unieke mailer-id die is toegewezen voor het manifest voor REST API.  <br/><br/>**_Note:_** Dit gebied is facultatief; nochtans, wordt het vereist om de verwezenlijking van het verschepende etiket toe te laten. |
| [!UICONTROL AES/ITN] | Website | USPS AES - Automated Export System / ITN - Internal Transaction Number for REST API. <br/><br/>**_Note:_** Dit gebied is over het algemeen facultatief, maar is vereist om het creëren van het verschepende etiket toe te laten als: <ul><li>Elk type van goederen in de zending (zoals die door Codes van de Uitvoer van het Programma B in <a href="https://www.census.gov/foreign-trade/schedules/b" target="_blank"> www.census.gov/foreign-trade/schedules/b </a> wordt bepaald) wordt gewaardeerd bij $2.500 of minder en vereist geen uitvoervergunning; of</li><li>De zending, ongeacht de waarde ervan, wordt naar Canada verzonden en heeft geen uitvoervergunning nodig.</li></ul> |

{style="table-layout:auto"}

![&#x200B; USPS het Verpakken Montages &#x200B;](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Website | Hiermee bepaalt u hoe gewicht wordt berekend voor overbrengingen met meerdere pakketten. Opties: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Website | Hiermee stelt u het containertype in dat wordt gebruikt voor het verpakken van verzendingen. Opties: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Niet-rechthoekig |
| [!UICONTROL Size] | Website | Hiermee stelt u de optie Grootte in op de standaardgrootte van het verzendpakket. Deze optie is van invloed op de berekening van de verzendkosten. Opties: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Website | Geeft aan of het pakket door de computer kan worden verwerkt. Deze optie is van invloed op de berekening van de verzendkosten. |
| [!UICONTROL Maximum Package Weight] | Website | Hiermee stelt u het maximumgewicht in dat een pakket kan krijgen, zoals opgegeven door USPS. Als de bestelde producten het maximale pakketgewicht overschrijden, is deze verzendoptie niet beschikbaar. |

{style="table-layout:auto"}

![&#x200B; USPS die de Montages van de Tarief behandelen &#x200B;](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Website | Hiermee stelt u de berekeningsmethode voor de behandelingskosten in voor het verzenden van tabeltarieven. Opties: <br/>**`Fixed`**- De verwerkingskosten zijn een vast tarief.<br/>**`Percent`** - De verwerkingskosten worden toegepast als een percentage van het orderbedrag. |
| [!UICONTROL Handling Applied] | Website | Geeft aan of behandelingskosten worden toegepast op elke bestelling of op elk pakket binnen een bestelling. |
| [!UICONTROL Handling Fee] | Website | Hiermee stelt u de afhandeling in die bij de verzendprijs wordt inbegrepen. De verwerkingskosten kunnen worden vastgesteld als een vast bedrag of als een percentage. <br/><br/>**_Note:_** Wanneer het typen van een percentagehoeveelheid, gebruik het decimale formaat `0.25` voor 25%. |

{style="table-layout:auto"}

![&#x200B; USPS Toegestane Methoden &#x200B;](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Website | Geeft de toegestane verzendmethoden van USPS aan die aan klanten worden aangeboden. De verzendkosten worden berekend op basis van de geselecteerde verzendmethode. |
| [!UICONTROL Free Method] | Website | Hiermee stelt u de methode voor gratis verzending in via USPS, of u kunt deze uitschakelen door `None` te selecteren. <br/><br/>**_Note:_** Deze verzendmethode is vergelijkbaar met de methode voor gratis verzending van je winkel, maar wordt aangeboden als een verzendoptie voor USPS en geïdentificeerd als verzending voor USPS. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Website | Hiermee stelt u het minimale orderbedrag in dat moet worden behaald om in aanmerking te komen voor gratis verzending. |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Het foutbericht dat wordt weergegeven wanneer USPS om welke reden dan ook niet beschikbaar is. |

{style="table-layout:auto"}

![&#x200B; USPS Toepasselijke Landen &#x200B;](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Website | Hiermee geeft u aan in welke landen bestellingen kunnen worden verzonden. Opties: <br/>**`All Allowed Countries`**- de Klanten van alle [&#x200B; landen &#x200B;](../../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze het verschepen methode gebruiken.<br/>**`Specific Countries`** - Nadat u deze optie hebt gekozen, wordt de lijst [!UICONTROL Ship to Specific Countries] weergegeven. Selecteer elk land in de lijst waar deze verzendmethode kan worden gebruikt. |
| [!UICONTROL Show Method if Not Applicable] | Website | Hiermee regelt u de weergave van verzendingen door USPS tijdens het afrekenen. Opties: <br/>**`Yes`**- USPS wordt altijd weergegeven als een verzendoptie tijdens het afrekenen, zelfs als dit niet van toepassing is op de bestelling.<br/>**`No`** - USPS wordt alleen weergegeven als een verzendoptie tijdens het afrekenen als dit van toepassing is op de bestelling (het gewicht van de bestelling is dus hoger dan het maximumgewicht). |
| [!UICONTROL Debug] | Website | Hiermee wordt bepaald of het systeem voor foutopsporing een logboek met gegevensverzendingen tussen uw opslag en USPS bijhoudt. Tenzij er een probleem is dat moet worden bijgehouden en geregistreerd, moet deze optie worden ingesteld op `No` . |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin USPS wordt weergegeven wanneer het tijdens het uitchecken wordt weergegeven bij andere leveringsmethoden. Voer `0` in voor de bovenkant van de lijst. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/fedex) -->

#### FedEx-accountinstellingen

![&#x200B; de Montages van de Rekening FedEx &#x200B;](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | Website | Hiermee wordt bepaald of FedEx beschikbaar is voor klanten als verzendmethode tijdens het afrekenen. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | De titel van deze verzendoptie zoals deze wordt weergegeven in het winkelwagentje. |
| [!UICONTROL Account ID] | Website | Je FedEx-account-id. |
| [!UICONTROL Api Key] | Website | De API-sleutel van uw FedEx-account. |
| [!UICONTROL Secret Key] | Website | De geheime sleutel voor uw FedEx-account-API. |
| [!UICONTROL Sandbox Mode] | Website | Als u FedEx-transacties wilt uitvoeren in een testomgeving, stelt u Sandbox-modus in op `Yes` . Opties: `Yes` / `No` . |
| [!UICONTROL Web-Services URL] | Website | De vereiste URL is afhankelijk van de instelling voor de sandboxmodus. Opties: <br/>**`Production`**- De URL voor toegang tot FedEx-webservices wanneer de winkel live is.<br/>**`Sandbox`** - De URL voor toegang tot de testomgeving voor FedEx-webservices. |

{style="table-layout:auto"}

#### FedEx-verpakkingsinstellingen

![&#x200B; Verpakken FedEx &#x200B;](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | Website | Selecteer in de lijst de ophaalmethode: <br/>**`DropOff at Fedex Location`**- (Standaard) Geeft aan dat u zendingen op uw lokale FedEx-station afsluit.<br/>**`Contact Fedex to Schedule`** - Geeft aan dat u contact opneemt met FedEx om een afhaalbewerking aan te vragen. <br/>**`Use Scheduled Pickup`**- Geeft aan dat de verzending wordt opgehaald als onderdeel van een normale geplande ophaling.<br/>**`On Call`** - Geeft aan dat het ophalen is gepland door FedEx aan te roepen. <br/>**`Package Return Program`**- Geeft aan dat de verzending is opgehaald door het FedEx Ground Package Returns Program.<br/>**`Regular Stop`** - Geeft aan dat de verzending wordt opgehaald volgens het normale ophaalschema. <br/>**`Tag`**- Geeft aan dat het ophalen van de verzending specifiek is voor een aanvraag voor het ophalen van de tag Express of grondaanroep. Dit is alleen van toepassing op verzendlabel voor retourzending. |
| [!UICONTROL Packages Request Type] | Website | Hiermee bepaalt u hoe gewicht wordt berekend voor overbrengingen met meerdere pakketten. Opties: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Website | Selecteer in de lijst het containertype dat u doorgaans gebruikt voor het verpakken van producten die in de winkel worden besteld. |
| [!UICONTROL Weight Unit] | Website | De eenheid die wordt gebruikt voor verpakkingsgewicht. Opties: `Pounds` (standaardwaarde) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | Website | De standaardwaarde voor FedEx is 150 pond. Raadpleeg uw verzendende provider voor maximaal ondersteund gewicht. Het gebruik van de standaardwaarde wordt aanbevolen, tenzij u speciale regelingen met FedEx hebt. |

{style="table-layout:auto"}

#### FedEx-instellingen voor verwerkingskosten

![&#x200B; FedEx die Tarief behandelt &#x200B;](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | Website | Bepaalt de methode die wordt gebruikt om de behandelingskosten te berekenen. Opties: `Fixed Fee` / `Percentage` <br/><br/>**_Note:_** De verpakkingskosten zijn optioneel en worden weergegeven als extra kosten die worden toegevoegd aan de verzendkosten van FedEx. |
| [!UICONTROL Handling Applied] | Website | Hiermee bepaalt u hoe behandelingskosten worden toegepast. Opties: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Website | Geeft het bedrag aan dat in rekening wordt gebracht als een behandelingsvergoeding, op basis van de methode die wordt gebruikt om het bedrag te berekenen. Als de kosten zijn gebaseerd op een vaste vergoeding, voert u het bedrag in als een decimaal, bijvoorbeeld `4.90` . Als de behandelingskosten gebaseerd zijn op een percentage van de bestelling, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de volgorde wilt opladen, voert u de waarde in als `.06` . |

{style="table-layout:auto"}

#### FedEx-leveringsmethoden

![&#x200B; Methoden van de Levering FedEx &#x200B;](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | Website | Stel dit in op een van de volgende opties, afhankelijk van het feit of u Business-to-Consumer (B2C) of Business-to-Business (B2B) verkoopt: <br/>**`Yes`**- voor B2C-leveringen<br/>**`No`** - voor B2B-leveringen |
| [!UICONTROL Allowed Methods] | Website | Selecteer in de lijst de verzendmethoden die u ondersteunt. De methoden zijn afhankelijk van uw FedEx-account, de frequentie en de grootte van uw verzendingen en of u internationale verzendingen toestaat. Als verkoper kun je besluiten alleen verzending op de grond aan te bieden. |
| [!UICONTROL Hub ID] | Website | Een id die wordt geleverd door FedEx en die wordt gebruikt met de methode [!DNL Smart Post] . |
| [!UICONTROL Free Method] | Website | Selecteer in de lijst de verzendmethode die je wilt gebruiken voor voorstellen voor gratis verzending. <br/><br/>**_Nota:_** Deze verschepende methode is gelijkaardig aan de regelmatige Vrije Verzending, nochtans is het vermeld binnen de FedEx het verschepen opties en geïdentificeerd als verschepen FedEx. |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Hiermee bepaalt u of een minimumbestelling vereist is voor gratis verzending. Opties: <br/>**`Enable`**- Maakt gratis verzending via FedEx mogelijk voor bestellingen die aan het minimumbedrag voldoen.<br/>**`Disable`** - Schakelt gratis verzending via FedEx met minimale bestelling uit. |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Hiermee geeft u het minimale orderbedrag op dat vereist is voor gratis verzending. |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Het bericht dat wordt weergegeven wanneer FedEx om welke reden dan ook niet beschikbaar is. U kunt het standaardbericht gebruiken of een ander ingaan. |

{style="table-layout:auto"}

#### FedEx, toepasbare landinstellingen

![&#x200B; FedEx Toepasselijke Landen &#x200B;](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | Website | Geeft de landen aan waar uw klanten kunnen verzenden via FedEx. Opties: <br/>**`All Allowed Countries`**- de Klanten van alle [&#x200B; landen &#x200B;](../../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze het verschepen methode gebruiken.<br/>**`Specific Countries`** - Nadat u deze optie hebt gekozen, wordt de lijst [!UICONTROL Ship to Specific Countries] weergegeven. Selecteer elk land in de lijst waar deze verzendmethode kan worden gebruikt. |
| [!UICONTROL Ship to Specific Countries] | Website | Geeft de specifieke landen aan waar uw klanten kunnen verzenden via FedEx. |
| [!UICONTROL Debug] | Website | Bepaalt als een logboek van gegevenstransmissies tussen uw opslag en FedEx door het systeem voor het zuiveren wordt gehandhaafd. Tenzij er een probleem is dat moet worden bijgehouden en geregistreerd, moet deze optie worden ingesteld op `No` . |
| [!UICONTROL Show Method if Not Applicable] | Website | Hiermee bepaalt u wanneer FedEx wordt weergegeven als een verzendmethode tijdens het afrekenen. Opties: <br/>**`Yes`**- De verzendoptie FedEx wordt weergegeven in de lijst met leveringsmethoden, ongeacht of de bestelling in aanmerking komt om deze te gebruiken.<br/>**`No`** - De verzendoptie FedEx wordt niet weergegeven in de lijst met leveringsmethoden als deze niet van toepassing is op de bestelling (bijvoorbeeld als het gewicht van de bestelling groter is dan het maximumgewicht). |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin FedEx wordt weergegeven bij andere leveringsmethoden tijdens het afrekenen. Voer `0` in voor de bovenkant van de lijst. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![&#x200B; De Montages van de Rekening van DHL &#x200B;](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Website | Hiermee wordt bepaald of DHL tijdens de afhandeling als verzendmethode voor klanten beschikbaar is. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Winkelweergave | De titel van deze verzendmethode zoals deze wordt weergegeven tijdens het afrekenen. |
| [!UICONTROL Gateway URL] | Website | Gewoonlijk, kunt u de standaardGateway URL goedkeuren. Als DHL u echter een alternatieve URL heeft gegeven, voert u de waarde in dit veld in. |
| [!UICONTROL Access ID] | Website | Toegang-id voor uw DHL-verzendaccount. |
| [!UICONTROL Password] | Website | Wachtwoord voor uw DHL-verzendaccount. |
| [!UICONTROL Account Number] | Website | Uw DHL-verzendrekeningnummer. |

{style="table-layout:auto"}

![&#x200B; De Montages van het Pakket DHL &#x200B;](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Website | De afhandelingskosten zijn optioneel en worden als extra kosten aan de DHL-verzendkosten toegevoegd. Selecteer in de lijst de methode die u wilt gebruiken voor het berekenen van afhandelingskosten. Opties: vaste kosten / percentage. |
| [!UICONTROL Handling Applied] | Website | Selecteer in de lijst hoe u de verwerkingskosten wilt toepassen. Opties: `Per Order` / `Per Package` |
| Verhandelingskosten | Website | Voer het bedrag in dat moet worden aangerekend voor een verpakkingskosten op basis van de methode die u hebt gekozen voor de berekening van het bedrag. Als de kosten bijvoorbeeld zijn gebaseerd op een vaste vergoeding, voert u het bedrag in als een decimaal, bijvoorbeeld `4.90` . Als de behandelingskosten echter zijn gebaseerd op een percentage van de bestelling, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de volgorde in rekening brengt, voert u de waarde in als `.06` . |
| [!UICONTROL Divide Order Weight] | Winkelweergave | Hiermee wordt bepaald of het gewicht van een bestelling van meer dan 70 kg in kleinere eenheden kan worden verdeeld om een nauwkeurige verzendkosten te garanderen. Opties: `Yes` / `No` |
| [!UICONTROL Weight Unit] | Winkelweergave | Bepaalt de maateenheid voor gewicht die wordt gebruikt bij verzendberekeningen. Opties: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Winkelweergave | Bepaalt de grootte van het pakket. Opties: <br/>**`Regular`**- Verzendpakketten voldoen aan de DHL-standaard verpakkingsmethoden. Selecteer in de lijst [!UICONTROL Allowed Methods] elke verpakkingsmethode die wordt gebruikt om producten uit uw winkel te verzenden.<br/>**`Specific`** - Als de verzonden pakketten aangepaste afmetingen hebben, voert u het volgende in: [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![&#x200B; DHL Toegestane Methoden &#x200B;](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Website | Selecteer in de lijst elke verzendmethode die u ondersteunt. |
| [!UICONTROL Ready Time] | Website | Hiermee geeft u aan wanneer het pakket gereed is voor ophalen (in uren) nadat een bestelling is verzonden. |
| [!UICONTROL Displayed Error Message] | Winkelweergave | Dit bericht wordt weergegeven wanneer DHL om welke reden dan ook niet beschikbaar is. U kunt het standaardbericht gebruiken of een eigen bericht ingaan. |
| [!UICONTROL Free Method] |  | Deze verzendmethode is vergelijkbaar met de gewone Vrij Verladen-methode, maar wordt vermeld in de DHL-scheepvaartopties en aangeduid als DHL-scheepvaart. Selecteer in de lijst de verzendmethode die je wilt gebruiken voor voorstellen voor gratis verzending. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Website | Stel dit op een van de volgende opties in: <br/>**`Enable`**- Om gratis DHL-verzending toe te staan voor bestellingen die aan het minimumbedrag voldoen.<br/>**`Disable`** - Geen gratis verzending van DHL met minimale bestelling. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Website | Als u [!UICONTROL Free Shipping with Minimum Order] inschakelt, voert u in het veld de minimale waarde voor de orderhoeveelheid in. |

{style="table-layout:auto"}

![&#x200B; DHL Toepasselijke Landen &#x200B;](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Website | Geeft aan welk land klanten deze verzendmethode mogen gebruiken. Opties: <br/>**Alle Toegestane Landen** - Alle toegestane landen zijn van toepassing om de vrije het verschepen methode te gebruiken. De landen met toestemming worden opgegeven op de configuratiepagina [!UICONTROL General] . <br/>**Specifieke Landen** - beperkt deze het verschepen optie tot de landen die in de Schip aan de Specifieke Lijst van Landen worden gespecificeerd. |
| [!UICONTROL Ship to Specific Countries] | Website | Geeft aan in welke landen DHL-verzendingen kunnen worden verzonden. Deze lijst met geselecteerde landen wordt gebruikt als `Specific Countries` is geselecteerd in de optie [!UICONTROL Ship to Applicable Countries] . |
| [!UICONTROL Show Method if Not Applicable] | Website | Hiermee bepaalt u wanneer DHL tijdens het afrekenen als een verzendmethode wordt weergegeven. Opties: <br/>**`Yes`**- DHL wordt altijd weergegeven als een verzendoptie tijdens het uitchecken, zelfs als dit niet van toepassing is op de bestelling.<br/>**`No`** - DHL wordt alleen bij de afhandeling weergegeven als een verzendoptie (dat wil zeggen dat het ordergewicht het maximale gewicht overschrijdt). |
| [!UICONTROL Debug] | Website | Hiermee maakt u een logbestand met foutgegevens. |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin DHL wordt weergegeven wanneer dit bij andere leveringsmethoden tijdens het afrekenen wordt vermeld. Voer `0` in als u deze boven aan de lijst wilt plaatsen. |

{style="table-layout:auto"}
