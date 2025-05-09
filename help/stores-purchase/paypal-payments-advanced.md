---
title: PayPal-betalingen geavanceerd
description: Leer hoe u PayPal Payments Advanced instelt als een online betalingsoplossing in uw winkel.
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2161'
ht-degree: 0%

---

# PayPal-betalingen geavanceerd

[ Geavanceerde Betalingen van PayPal ][4] is a [ PCI-Volgzame ](../getting-started/compliance-pci.md) oplossing die uw klanten door debet of creditcard laat betalen zonder uw plaats te verlaten. Deze pagina bevat een ingesloten afhandelingspagina die kan worden aangepast om een naadloze en veilige afhandeling te maken.

Zelfs klanten zonder PayPal-rekening kunnen aankopen doen via de beveiligde betaalgateway van PayPal. Geaccepteerde kaarten zijn Visa, MasterCard, Switch/Maestro en Solo creditcards in de Verenigde Staten en het Verenigd Koninkrijk. Voor extra gemak wordt PayPal Express Checkout meegeleverd bij Paypal Payments Advanced.

>[!IMPORTANT]
>
>**PSD2 Vereisten:** <br/>
>Vanaf 14 september 2019, zouden de Europese banken betalingen kunnen verminderen die niet [ PSD2 ](../getting-started/compliance-payment-services-directive.md) vereisten voldoen. Als je wilt voldoen aan PSD2, moet PayPal Payments Advanced zijn geïntegreerd met een externe insteekmodule. Meer leren, zie [ 3-D Veilig voor Payflow ](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>PayPal Payments Advanced kan niet worden gebruikt voor bestellingen die zijn gemaakt via de beheerder van uw winkel.

## Vereisten

- [ PayPal bedrijfsrekening ][1]
- Als u meerdere Adobe Commerce- en Magento Open Source-websites beheert, moet u voor elke website een aparte PayPal Merchant-account hebben.

## Workflow voor uitchecken

1. **de Klant kiest betalingsmethode** - tijdens controle, verkiest de klant om met Geavanceerde Betalingen te betalen PayPal. De knop Nu betalen wordt weergegeven in plaats van de knop Bestelling plaatsen.

1. **Pay nu** - de klant klikt/tikt _nu betalen_, en een op PayPal-Geghoste vorm verschijnt. De klant voert de kaartgegevens in en de kaart wordt geverifieerd. Als dit lukt, wordt de pagina voor bevestiging van de bestelling weergegeven.

   **Betalen met PayPal** - de vorm omvat ook het _Betalen met PayPal_ knoop, die de klant aan de plaats van PayPal opnieuw richt, waar de betaling met Uitdrukkelijke Betaling PayPal kan worden gedaan.

1. **het Oplossen van problemen** - als de transactie om het even welke reden ontbreekt, verschijnt een foutenmelding op de controlepagina en de klant wordt opgedragen om opnieuw te proberen. Alle problemen worden beheerd door PayPal.

## Workflow voor het verwerken van bestellingen

De verwerking van bestellingen met PayPal Payments Geavanceerd is hetzelfde als bij elke normale PayPal-bestelling. Bestellingen worden gefactureerd en verzonden, en creditnota&#39;s worden gegenereerd voor zowel online als offline terugbetalingen. Er zijn echter geen meerdere online terugbetalingen beschikbaar voor bestellingen die met PayPal Payments Advanced zijn betaald.

1. **Klant plaatst orde** - in het definitieve stadium van controle, tikt de klant op de knoop van de Orde van de Plaats.

1. **PayPal antwoordt** - PayPal evalueert het verzoek. Als deze geldig blijkt te zijn, verwerkt PayPal de transactie.

1. **Commerce plaatst ordestatus** - Commerce ontvangt reactie van PayPal, en plaatst de ordestatus aan één van het volgende:

   - **Verwerking** - de transactie was succesvol.
   - **In afwachting van Betaling** - het systeem ontving geen reactie van PayPal.
   - **Geannuleerd** - de transactie was niet succesvol om één of andere reden
   - **Vermoedelijke Fraude** - de transactie ging niet enkele [ Paypal fraudefilters ](paypal.md#paypal-fraud-management-filters) over. Het systeem ontvangt van PayPal de reactie dat de transactie wordt gecontroleerd door de Fraud Service.

1. **Merchant voldoet orde** - de handelaarfacturen en verschepen de orde.

## Uw PayPal-account configureren

Voordat u Paypal Payments Advanced instelt in Commerce, moet u uw account configureren op de Paypal-website.

1. Login aan uw [ PayPal bedrijfsrekening ][2].

1. Ga naar **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** en voer de volgende instellingen in:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** de instellingen.

   >[!NOTE]
   >
   >Als u meerdere Commerce-websites hebt, moet u voor elke website een aparte geavanceerde Paypal-rekening maken.

1. Ga als volgt te werk wanneer u wordt gevraagd een lay-out te maken:

   - Klik boven aan de pagina op **[!UICONTROL Customize]** .

   - Kies **[!UICONTROL Layout C]** .

   - Klik op **[!UICONTROL Save and Publish]**.

1. Een andere gebruiker instellen (aanbevolen door PayPal):

   - Login aan uw [ PayPal bedrijfsrekening ][2].

   - Volg de instructies om een andere gebruiker in te stellen.

   - **[!UICONTROL Save]** de wijzigingen.

## PayPal-betalingen geavanceerd instellen in Commerce

>[!NOTE]
>
>Er kunnen twee PayPal-oplossingen tegelijk actief zijn: Express Checkout en een All-In-One of Payment Gateway-oplossing. Als u betalingsoplossingen wijzigt, is degene die eerder is gebruikt, uitgeschakeld.

>[!TIP]
>
>Klik op **[!UICONTROL Save Config]** om de voortgang op te slaan.

### Stap 1: Begin met de configuratie

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Als uw Commerce-installatie meerdere websites, winkels of weergaven bevat, stelt u **[!UICONTROL Store View]** in op de winkelweergave waar u deze configuratie wilt toepassen.

1. Selecteer in de sectie _[!UICONTROL Merchant Location]_de **[!UICONTROL Merchant Country]**waar uw bedrijf zich bevindt.

   Deze instelling bepaalt de selectie van PayPal-oplossingen die in de configuratie worden weergegeven.

   ![ Merchant Land ](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Vouw **[!UICONTROL PayPal All-in-One Payment Solution]** uit en klik op **[!UICONTROL Configure]** for **[!UICONTROL Payments Advanced]** .

   ![ Geavanceerde Betalingen van PayPal ](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### Stap 2: Voer de vereiste instellingen in

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Required PayPal Settings]** sectie uit, indien nodig.

   ![ Geavanceerde Vereiste Montages - Geavanceerde Betalingen PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. (Optioneel) Voer de **[!UICONTROL Email Associated with your PayPal Merchant Account]** in.

   >[!IMPORTANT]
   >
   >E-mailadressen zijn hoofdlettergevoelig. Als je een betaling wilt ontvangen, moet het e-mailadres overeenkomen met het e-mailadres dat is opgegeven in je PayPal Merchant-account.

   Klik op **[!UICONTROL Start accepting payments via PayPal]** als u geen PayPal-rekening hebt.

1. Voer een van de volgende gegevens in waarmee u zich aanmeldt bij uw PayPal-zakelijke account:

   - **[!UICONTROL Partner]** - Uw PayPal-partner-id.
   - **[!UICONTROL Vendor]** - De gebruikersnaam van uw PayPal-gebruikersaanmelding.
   - **[!UICONTROL User]** - De id van een andere gebruiker die is ingesteld op uw Paypal-account.

1. Voer de **[!UICONTROL Password]** in die aan uw Paypal-account is gekoppeld.

1. Als u testtransacties wilt uitvoeren, stelt u **[!UICONTROL Test Mode]** in op `Yes` .

   Wanneer het testen van de configuratie in een zandbak, gebruik slechts [ creditcardaantallen ][3] die door PayPal worden geadviseerd. Als u gereed bent om naar de productie te gaan, gaat u terug naar de configuratie en stelt u Testmodus in op `No` .

1. Als uw systeem een proxyserver gebruikt om de verbinding met het PayPal-systeem tot stand te brengen, stelt u **[!UICONTROL Use Proxy]** in op `Yes` en voert u de volgende handelingen uit:

   - Voer het IP-adres van de **[!UICONTROL Proxy Host]** in.

   - Voer het poortnummer van de **[!UICONTROL Proxy Port]** in.

     Er wordt een proxy gebruikt wanneer de serverfirewall directe toegang tot de PayPal-server voorkomt. In dit geval, wordt een derdenserver gebruikt om verkeer af te lossen.

1. Stel **[!UICONTROL Enable this Solution]** in op `Yes` .

1. Als u [ Krediet van PayPal ](paypal.md#paypal-credit-and-pay-later) aan uw klanten wilt aanbieden, plaats **[!UICONTROL Enable PayPal Credit]** aan `Yes`.

### Stap 3: Adverteer PayPal-creditering / Adverteer PayPal Later (optioneel)

Vanaf de release 2.4.3 wordt PayPal PayLater ondersteund in implementaties die PayPal bevatten. Met deze functie kunnen kopers een bestelling in tweewekelijkse termijnen betalen in plaats van het volledige bedrag op het moment van aankoop te betalen. De PayPal-ervaring is afgekeurd.

Stel **[!UICONTROL Enable PayPal PayLater Experience]** in op een van de volgende opties:

- `Yes` - Meer informatie over PayPal PayPal instellen
- `No` - Adverteer PayPal-creditering instellen

#### PayPal-krediet adverteren

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advertise PayPal Credit]** sectie uit.

   ![ Adverteer PayPal Krediet ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Get Publisher ID from PayPal]** en volg de instructies op uw account om uw accountgegevens op te vragen.

1. Voer uw **[!UICONTROL Publisher ID]** in.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Home Page]** sectie uit.

1. Stel **[!UICONTROL Display]** in op `Yes` als u een banner op de pagina wilt plaatsen.

1. Stel **[!UICONTROL Position]** in op een van de volgende opties:

   - `Header (center)`
   - `Sidebar (right)`

1. Stel **[!UICONTROL Size]** in op een van de volgende opties:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![ Adverteer de Montages van de Homepage van het Krediet van PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de resterende secties uit en herhaal de vorige stappen:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Adverteer PayPal PayPal Later

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advertise PayPal PayLater]** sectie uit.

1. Stel **[!UICONTROL Enable PayPal PayLater]** in op `Yes` .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Home Page]** sectie uit.

1. Stel **[!UICONTROL Display]** in op `Yes` als u een banner op de pagina wilt plaatsen.

1. Stel **[!UICONTROL Position]** in op een van de volgende opties:

   - `Header (center)`
   - `Sidebar`

1. Stel **[!UICONTROL Style Layout]** in op een van de volgende opties:

   - `Text`
   - `Flex`

1. Stel [!UICONTROL Style Layout] alleen **[!UICONTROL Text]** in op een van de volgende opties: **[!UICONTROL Logo Type]**

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Stel [!UICONTROL Style Layout] alleen **[!UICONTROL Text]** in op een van de volgende opties: **[!UICONTROL Logo Position]**

   - `Left`
   - `Right`
   - `Top`

1. Stel [!UICONTROL Style Layout] alleen **[!UICONTROL Text]** in op een van de volgende opties: **[!UICONTROL Text Color]**

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Stel [!UICONTROL Style Layout] alleen **[!UICONTROL Text]** in op een van de volgende opties: **[!UICONTROL Text Size]**

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Stel [!UICONTROL Style Layout] alleen **[!UICONTROL Flex]** in op een van de volgende opties: **[!UICONTROL Ratio]**

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Stel [!UICONTROL Style Layout] alleen **[!UICONTROL Flex]** in op een van de volgende opties: **[!UICONTROL Color]**

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![ Adverteer de Montages van de Homepage van het Krediet van PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de resterende secties uit en herhaal de vorige stappen:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Stap 4: De basisinstellingen voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Basic Settings - PayPal Payments Advanced]** sectie uit, indien nodig.

   ![ PayPal Payments Geavanceerde Basismontages ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Title]** in om Paypal-betalingen geavanceerd tijdens het afrekenen te identificeren.

   Men adviseert dat u de titel _Debit of Kaart_ gebruikt.

1. Als u meerdere betalingsmethoden aanbiedt, voert u een getal voor **[!UICONTROL Sort Order]** in om te bepalen in welke volgorde Paypal Payments Advanced wordt weergegeven wanneer deze bij andere betalingsmethoden wordt aangeboden tijdens het afrekenen.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Stel **[!UICONTROL Payment Action]** in op een van de volgende opties:

   - `Authorization` - Hiermee gaat u akkoord met de aankoop, maar u houdt de middelen in de wacht. Het bedrag wordt niet teruggetrokken tot het __ door de koopman wordt gevangen.
   - `Sale` - Het bedrag van de aankoop wordt geautoriseerd en onmiddellijk van de rekening van de klant teruggetrokken.

### Stap 5: De geavanceerde instellingen voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advanced Settings]** sectie uit.

   ![ Geavanceerde Montages - Geavanceerde Betalingen PayPal ](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Payment Applicable From]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_weergegeven. Houd Ctrl (PC) of Command (Mac) ingedrukt en selecteer elk land in de lijst waar klanten aankopen kunnen doen in uw winkel.

1. Als u communicatie met het betalingssysteem naar het logbestand wilt schrijven, stelt u **[!UICONTROL Debug Mode]** in op `Yes` .

   Het logbestand voor Paypal Payments Advanced is `payments_payflow_advanced.log` .

   >[!NOTE]
   >
   >In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier.

1. Als u verificatie van de authenticiteit van de host wilt inschakelen, stelt u **[!UICONTROL Enable SSL Verification]** in op `Yes` .

1. Stel **[!UICONTROL CVV Entry is Editable]** in op `Yes` om de klant in staat te stellen de driecijferige CVV-beveiligingscode vanaf de achterkant van een creditcard te corrigeren.

1. Stel **[!UICONTROL Require CVV Entry]** in op `Yes` als u wilt dat klanten een CVV-code invoeren.

1. Als u een bevestiging van de betaling naar de klant wilt verzenden, stelt u **[!UICONTROL Send Email Confirmation]** in op `Yes` .

1. Als u wilt bepalen welke methode wordt gebruikt om informatie uit te wisselen met de PayPal-server tijdens een transactie, stelt u de **[!UICONTROL URL method for Cancel URL and Return URL]** in op een van de volgende opties:

   - `GET` - (Standaard) Hiermee wordt informatie opgehaald die het resultaat is van een proces.
   - `POST` - Hiermee wordt een gegevensverwerkingsproces gestart, zoals gegevens die in een formulier worden ingevoerd.

   _annuleert URL_ en _Terugkeer URL_ verwijzen naar de pagina waar de klant na het voltooien van of het annuleren van het betalingsgedeelte van het controleproces op de server PayPal terugkeert.

1. Vul de volgende secties in, indien nodig voor uw winkel:

   - [Instellingen voor afwikkelingsrapport](#settlement-report-settings)
   - [Instellingen voor voorvertoning](#frontend-experience-settings)

#### Instellingen voor afwikkelingsrapport

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Settlement Report Settings]** sectie uit.

   ![ de Montages van het Rapport van de Afwikkeling van PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Voer voor **[!UICONTROL SFTP Credentials]** de volgende handelingen uit:

   - Als u zich hebt aangemeld voor Secure FTP Server van PayPal, voert u de volgende SFTP-aanmeldgegevens in:

      - Aanmelden
      - Wachtwoord

   - Als u testrapporten wilt uitvoeren voordat u live gaat, stelt u **[!UICONTROL Sandbox Mode]** in op `Yes` .

   - Voer de **[!UICONTROL Custom Endpoint Hostname or IP Address]** in.

     De standaardwaarde is `reports.paypal.com` .

   - Voer de **[!UICONTROL Custom Path]** in waarin rapporten worden opgeslagen.

     De standaardwaarde is `/ppreports/outgoing` .

1. Als u rapporten wilt genereren volgens een schema, voert u de **[!UICONTROL Scheduled Fetching]** -instellingen in:

   - Stel **[!UICONTROL Enable Automatic Fetching]** in op `Yes` .

   - Stel **[!UICONTROL Schedule]** in op een van de volgende opties:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal bewaart elk rapport 45 dagen.

   - Stel **[!UICONTROL Time of Day]** in op het uur, de minuut en de seconde waarop u de rapporten wilt genereren.

#### Instellingen voor voorvertoning

Gebruik _[!UICONTROL Frontend Experience Settings]_om te kiezen welke PayPal-logo&#39;s op uw site worden weergegeven en om de weergave van uw PayPal-handelpagina&#39;s aan te passen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Frontend Experience Settings]** sectie uit.

   ![ PayPal de Montages van de Voorwaartse Ervaring ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

1. Selecteer de **[!UICONTROL PayPal Product Logo]** die u in het PayPal-blok in uw winkel wilt weergeven.

   De PayPal-logo&#39;s zijn beschikbaar in vier stijlen en twee formaten:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. De weergave van je PayPal-winkelpagina&#39;s aanpassen:

   - Voer de naam in van de **[!UICONTROL Page Style]** die u wilt toepassen op de handelspagina&#39;s van PayPal:

      - `paypal` - Gebruikt de paginastijl van PayPal.
      - `primary` - gebruikt de paginastijl die u als _primaire_ stijl in uw rekeningsprofiel identificeerde.
      - `your_custom_value` - Gebruikt een aangepaste paginastijl voor betalingen, die in uw accountprofiel is opgegeven.

   - Voer bij **[!UICONTROL Header Image URL]** de URL in van de afbeelding die u in de linkerbovenhoek van de betaalpagina wilt weergeven. De maximale bestandsgrootte is 750 pixels breed en 90 pixels hoog.

   >[!NOTE]
   >
   >PayPal raadt aan de afbeelding op een beveiligde server (https) te plaatsen. Anders, kan browser waarschuwen dat _de pagina zowel veilige als niet veilige punten_ bevat.

   - Als u de kleur voor uw pagina&#39;s wilt instellen, voert u voor elk van de volgende handelingen de zestekenige hexadecimale code in, zonder het symbool `#` :

      - **[!UICONTROL Header Background Color]** - Achtergrondkleur voor de koptekst van de uitcheckpagina.
      - **[!UICONTROL Header Border Color]** - Kleur voor rand van twee pixels rond de koptekst.
      - **[!UICONTROL Page Background Color]** - Achtergrondkleur voor de uitcheckpagina en rond de koptekst en het betalingsformulier.

### Stap 6: Volledige basisinstellingen voor PayPal Express Checkout

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Basic Settings - PayPal Express Checkout]** sectie uit.

   ![ Uitdrukkelijke de Uitdrukkelijke Montages van de Controle van PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Voer bij **[!UICONTROL Title]** een titel in die deze betalingsmethode identificeert tijdens het afrekenen.

   Het plaatsen van de titel aan _PayPal_ voor elke opslagmening wordt geadviseerd.

1. Als u meerdere betalingsmethoden aanbiedt, voert u een getal voor **[!UICONTROL Sort Order]** in om de volgorde te bepalen waarin PayPal Express Checkout wordt weergegeven wanneer deze bij de andere betalingsmethoden wordt aangeboden.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Stel **[!UICONTROL Payment Action]** in op een van de volgende opties:

   - `Authorization` - Hiermee gaat u akkoord met de aankoop en houdt u de middelen in de wacht. Het bedrag wordt niet teruggetrokken tot het __ door de koopman wordt gevangen.
   - `Sale` - Het bedrag van de aankoop wordt geautoriseerd en onmiddellijk van de rekening van de klant teruggetrokken.

1. Stel **[!UICONTROL Display on Product Details Page]** in op `Yes` om de knop _[!UICONTROL Check out with PayPal]_op de productpagina weer te geven.

### Stap 7: Volledige geavanceerde instellingen - PayPal Express Checkout

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advanced Settings]** sectie uit.

   ![ Uitdrukkelijke Uitdrukkelijke Controle van PayPal Geavanceerde Montages ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. Als u PayPal Express Checkout beschikbaar wilt maken via het winkelwagentje en de minikaart, stelt u **[!UICONTROL Display on Shopping Cart]** in op `Yes` .

1. Stel **[!UICONTROL Payment Applicable From]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` |Na het kiezen van deze optie, verschijnt de _Betaling van de Specifieke lijst van Landen_. Houd Ctrl (PC) of Command (Mac) ingedrukt en klik op elk land in de lijst waar klanten aankopen kunnen doen in uw winkel.

1. Als u communicatie met het betalingssysteem naar het logbestand wilt schrijven, stelt u **[!UICONTROL Debug Mode]** in op `Yes` .

   >[!NOTE]
   >
   >In overeenstemming met [ Normen van de Veiligheid van Gegevens PCI ](../getting-started/compliance-pci.md), wordt de informatie van de creditcard niet geregistreerd in het logboekdossier.

1. Als u verificatie van de authenticiteit van de host wilt inschakelen, stelt u **[!UICONTROL Enable SSL Verification]** in op `Yes` .

1. Stel **[!UICONTROL Transfer Cart Line Items]** in op `Yes` als u een volledig overzicht wilt weergeven van de bestelling van de klant per regel op de Paypal-site.

1. Stel **[!UICONTROL Skip Order Review Step]** in op `Yes` als u de klant wilt toestaan de transactie van de PayPal-site te voltooien zonder deze terug te sturen naar uw winkel voor het reviseren van bestellingen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
