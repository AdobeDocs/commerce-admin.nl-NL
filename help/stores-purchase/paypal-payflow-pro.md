---
title: PayPal Payflow Pro
description: Meer informatie over het instellen van PayPal Payflow Pro als een online betalingsoplossing in je winkel.
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '2194'
ht-degree: 0%

---

# PayPal Payflow Pro

De Pro gateway van de Payflow van PayPal, vroeger gekend als _Verisign_, is beschikbaar voor klanten van de Verenigde Staten, Canada, Australië, en Nieuw Zeeland. In tegenstelling tot andere PayPal-betalingsmethoden worden handelaren een vaste maandelijkse vergoeding aangerekend, plus een vaste vergoeding voor elke transactie, ongeacht het nummer.

![ Controle met PayPal ](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2 Vereisten:** <br/>
>Vanaf 14 september 2019, zouden de Europese banken betalingen kunnen verminderen die niet [ PSD2 ](../getting-started/compliance-payment-services-directive.md) vereisten voldoen. Om te voldoen aan PSD2, moet PayPal Payflow Pro zijn geïntegreerd met een externe insteekmodule. Meer leren, zie [ 3-D Veilig voor Payflow ](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## Vereisten

- [ PayPal BedrijfsRekening ][1] - de gateway van PayPal van de Payflow Pro van PayPal verbindt de handelaarrekening bij PayPal met de handelende website, handelend als zowel gateway als een handelaarrekening.

- Als u meerdere Adobe Commerce- en Magento Open Source-websites beheert, moet u voor elke website een aparte PayPal Merchant-account hebben.

## Workflow van de klant

1. **de Klant gaat naar de kassa** - tijdens kassa, verkiest de klant om met PayPal Payflow Pro te betalen, en gaat de creditcardinformatie in. Klanten hoeven geen persoonlijke PayPal-rekeningen te hebben. Afhankelijk van het handelende land kunnen klanten echter ook hun persoonlijke PayPal-rekening gebruiken om voor de bestelling te betalen.
1. **Klant legt orde** voor - de klant legt de orde voor, en de ordeinformatie wordt verzonden naar PayPal voor verwerking. De klant verlaat de afhandelingspagina van uw site niet.
1. **PayPal voltooit de transactie** - De betalingen worden goedgekeurd op het tijdstip dat de orde wordt geplaatst. Afhankelijk van de betalingsactie die in de configuratie is opgegeven, wordt een verkooporder of een verkooporder en een factuur gemaakt.

## Workflow voor online orderverwerking

1. **de Beheerder legt online factuur** voor - de opslagbeheerder legt een online factuur voor en, dientengevolge, wordt een overeenkomstige transactie en een factuur gecreeerd.
1. **PayPal ontvangt de transactie** - de ordeinformatie wordt verzonden naar PayPal. Er wordt een overzicht van de transactie en een factuur gegenereerd. U kunt alle transacties van de Gateway van de Payflow Pro in uw [ handelaarrekening van PayPal ][2] bekijken.

>[!NOTE]
>
>Gedeeltelijke facturen en gedeeltelijke terugbetalingen worden niet ondersteund door PayPal Payflow Pro.

## Uw PayPal-account configureren

1. Login aan uw [ PayPal bedrijfsrekening ][2].

1. Vorm de [ Ontvangen Pagina&#39;s van de Controle ][4] gebruikend Manager PayPal met de volgende montages:

   - Stel onder **[!UICONTROL Choose your settings]** de waarde **[!UICONTROL Transaction Process Mode]** in op `Live` .

   - Onder **[!UICONTROL Display options on payment page]**, de reeks **annuleert Methode URL** aan `POST`.

   - Selecteer onder **[!UICONTROL Billing Information]** de selectievakjes voor de beveiligingscode van de kaart **[!UICONTROL CSC]** voor vereiste en bewerkbare velden.

   - Stel onder **[!UICONTROL Payment Confirmation]** de waarde **[!UICONTROL Return URL Method]** in op `POST` .

   - Voer onder **[!UICONTROL Security Options]** de volgende instellingen in:

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - Kies **[!UICONTROL Customize]** en kies vervolgens **[!UICONTROL Layout C]** .

     Layout C geeft alleen velden voor creditcards en betaalkaarten weer en kan op uw site worden geframed of als een zelfstandig popup worden gebruikt. De grootte is vast op 490 x 565 pixels, met extra ruimte voor foutberichten. Op sommige systemen corrigeert deze instelling een probleem met transparante omleiding.

1. Klik op **[!UICONTROL Save and Publish]** wanneer de configuratie-instellingen zijn voltooid.

1. Kies **[!UICONTROL Account Administration]** in het menu PayPal Manager.

1. Klik onder **[!UICONTROL Manage Security]** op **[!UICONTROL Transaction Settings]** en voer de volgende handelingen uit:

   - Stel **[!UICONTROL Allow reference transactions]** in op `Yes` .

   - Klik op **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >Als u meerdere Commerce-websites hebt, moet u voor elke website een aparte geavanceerde Paypal-rekening maken.

1. Een andere gebruiker instellen (aanbevolen door PayPal):

   - Klik in de tweede rij van het hoofdmenu op **[!UICONTROL Manage Users]** .

   - Klik op **[!UICONTROL Add User]** als u nog een gebruiker aan de account wilt toevoegen. De koppeling bevindt zich net boven de titel Gebruikers beheren.

   - Vul de vereiste velden in de volgende secties van het _[!UICONTROL Add User]_-formulier in:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Klik op **[!UICONTROL Update]**.

1. Log uit van je PayPal-rekening.

## PayPal Payflow Pro instellen in Commerce

>[!TIP]
>
>Klik op **[!UICONTROL Save Config]** om de voortgang op te slaan.

### Stap 1: Begin met de configuratie

Bij deze instelmethode wordt ervan uitgegaan dat u een bestaand PayPal-account hebt.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Als uw Commerce-installatie meerdere websites, winkels of weergaven bevat, stelt u **[!UICONTROL Store View]** in op de winkelweergave waar u deze configuratie wilt toepassen.

1. Selecteer in de sectie _[!UICONTROL Merchant Location]_&#x200B;de **[!UICONTROL Merchant Country]**&#x200B;waar uw bedrijf zich bevindt.

   Deze instelling bepaalt de selectie van PayPal-oplossingen die in de configuratie worden weergegeven.

   ![ Merchant Land ](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Vouw **[!UICONTROL PayPal Payment Gateways]** (indien nodig) uit en klik op **[!UICONTROL Configure]** for **[!UICONTROL Payflow Pro]** .

   ![ vormen - de Pro van de Payflow ](./assets/payflow-pro.png){width="600" zoomable="yes"}

### Stap 2: Voltooi de vereiste PayPal-instellingen

![ Vereiste Montages - PayPal Payflow Pro ](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. (Optioneel) Voer de **[!UICONTROL Email Associated with your PayPal Merchant Account]** in.

   >[!IMPORTANT]
   >
   >E-mailadressen zijn hoofdlettergevoelig. Als je een betaling wilt ontvangen, moet het e-mailadres overeenkomen met het e-mailadres dat is opgegeven in je PayPal Merchant-account.

1. Voer een van de volgende gegevens in waarmee u zich aanmeldt bij uw PayPal-zakelijke account:

   - **[!UICONTROL Partner]** - Uw PayPal-partner-id.
   - **[!UICONTROL User]** - Als u een of meer extra gebruikers op de account instelt, is deze waarde de id van de gebruiker die gemachtigd is om transacties te verwerken. Als u echter geen extra gebruikers hebt ingesteld, heeft **[!UICONTROL USER]** dezelfde waarde als **[!UICONTROL Vendor]** .
   - **[!UICONTROL Vendor]** - Uw bedrijfs login identiteitskaart creeerde toen u voor de rekening registreerde.

1. Voer de **[!UICONTROL Password]** in die aan uw Paypal-account is gekoppeld.

1. Als u testtransacties wilt uitvoeren, stelt u **[!UICONTROL Test Mode]** in op `Yes` .

   Wanneer het testen van de configuratie in een zandbak, gebruik slechts [ creditcardaantallen ][3] die door PayPal worden geadviseerd. Als u gereed bent om naar de productie te gaan, gaat u terug naar de configuratie en stelt u Testmodus in op `No` .

1. Als uw systeem een proxyserver gebruikt om de verbinding met het PayPal-systeem tot stand te brengen, stelt u **[!UICONTROL Use Proxy]** in op `Yes` en voert u de volgende handelingen uit:

   - Voer het IP-adres van de **[!UICONTROL Proxy Host]** in.

   - Voer het poortnummer van de **[!UICONTROL Proxy Port]** in.

     Er wordt een proxy gebruikt wanneer de serverfirewall directe toegang tot de PayPal-server voorkomt. In een dergelijk geval, wordt een derdenserver gebruikt om verkeer af te lossen.

1. Stel **[!UICONTROL Enable this Solution]** in op `Yes` .

1. Als u [ Krediet van PayPal ](paypal.md#paypal-credit-and-pay-later) aan uw klanten wilt aanbieden, plaats **[!UICONTROL Enable PayPal Credit]** aan `Yes`.

1. Als u de betaling-/creditcardgegevens van de klant veilig wilt opslaan, zodat klanten niet telkens opnieuw betalingsgegevens hoeven in te voeren, stelt u **[!UICONTROL Vault Enabled]** in op `Yes` .

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

   ![ Adverteer de Montages van de Homepage van het Krediet van PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de resterende secties uit en herhaal de vorige stappen voor de montages van de homepage:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Adverteer PayPal PayPal Later

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advertise PayPal PayLater]** sectie uit.

1. Stel **[!UICONTROL Enable PayPal PayLater]** in op `Yes` .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Home Page]** sectie uit.

   ![ Adverteer de Montages van de Homepage van het Krediet van PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de resterende secties uit en herhaal de vorige stappen:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Stap 4: De basisinstellingen voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Basic Settings - PayPal Payflow Pro]** sectie uit.

   ![ Basismontages - PayPal Payflow Pro_ ](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. Voer voor **[!UICONTROL Title]** een titel in die aangeeft wat PayPal Payflow Pro is tijdens het afrekenen.

   Men adviseert dat u de titel _Debit of Kaart_ gebruikt.

1. Als u meerdere betalingsmethoden aanbiedt, voert u een getal in voor **[!UICONTROL Sort Order]** om te bepalen in welke volgorde Payflow Pro wordt weergegeven wanneer deze bij de andere betalingsmethoden wordt aangeboden.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Stel **[!UICONTROL Payment Action]** in op een van de volgende opties:

   - `Authorization` - Hiermee gaat u akkoord met de aankoop en houdt u de middelen in de wacht. De hoeveelheid wordt pas opgevangen nadat de handelaar deze heeft opgevangen.
   - `Sale` - Het bedrag van de aankoop wordt geautoriseerd en onmiddellijk van de rekening van de klant teruggetrokken.

1. Selecteer voor **[!UICONTROL Credit Card Settings]** de creditcards die je accepteert voor betaling in je winkel.

   Als u meerdere kaarten wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke kaart.

   >[!NOTE]
   >
   >American Express vereist een extra overeenkomst.

### Stap 5: De geavanceerde instellingen voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advanced Settings]** sectie uit.

   ![ Geavanceerde Montages - PayPal Payflow Pro ](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Payment Applicable From]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [ landen ](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_&#x200B;weergegeven. Houd Ctrl (PC) of Command (Mac) ingedrukt en selecteer elk land in de lijst waar klanten aankopen kunnen doen in uw winkel.

1. Als u communicatie met het betalingssysteem naar het logbestand wilt schrijven, stelt u **[!UICONTROL Debug Mode]** in op `Yes` .

   >[!NOTE]
   >
   >In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier.

1. Als u verificatie van de authenticiteit van de host wilt inschakelen, stelt u **[!UICONTROL Enable SSL Verification]** in op `Yes` .

1. Stel **[!UICONTROL Require CVV Entry]** in op `Yes` als u wilt dat klanten een CVV-code invoeren.

1. Vul de volgende secties in, indien nodig voor uw winkel:

   - [CVV- en AVS-instellingen](#cvv-and-avs-settings)
   - [Instellingen voor afwikkelingsrapport](#settlement-report-settings)
   - [Instellingen voor voorvertoning](#frontend-experience-settings)

#### CVV- en AVS-instellingen

Om te bepalen wanneer een transactie zou moeten worden verworpen wanneer het Systeem van de Verificatie van het Adres een mismatch identificeert, specificeer hoe te om diverse scenario&#39;s te behandelen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL CVV and AVS Settings]** sectie uit.

   ![ CVV en Montages AVS - PayPal Payflow Pro ](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. Als u een transactie wilt afwijzen die is gebaseerd op een niet-overeenkomende niet-overeenkomende straat, stelt u **[!UICONTROL AVS Street Does Not Match]** in op `Yes` .

1. Als u een transactie op basis van een niet-overeenkomende ZIP-code wilt afwijzen, stelt u **[!UICONTROL AVS Zip Does Not Match]** in op `Yes` .

1. Als u een transactie wilt afwijzen op basis van een niet-overeenkomende land-id, stelt u **[!UICONTROL International AVS Indicator Does Not Match]** in op `Yes` .

1. Als u een transactie op basis van een niet-overeenkomende CVV-code wilt afwijzen, stelt u **[!UICONTROL International Card Security Code Does Not Match]** in op `Yes` .

#### Instellingen voor afwikkelingsrapport

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Settlement Report Settings]** sectie uit.

   ![ de Montages van het Rapport van de Afrekening - PayPal Payflow Pro ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Voer voor **[!UICONTROL SFTP Credentials]** de volgende handelingen uit:

   - Als u zich hebt aangemeld bij de PayPal Secure FTP-server, voert u de volgende SFTP-aanmeldgegevens in:

      - Aanmelden
      - Wachtwoord

   - Stel **[!UICONTROL Sandbox Mode]** in op `Yes` als u testrapporten wilt uitvoeren voordat u live gaat met Express Checkout op uw site.

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

Met de instellingen voor de vooraf ingestelde ervaring kunt u kiezen welke PayPal-logo&#39;s op uw site worden weergegeven en kunt u de weergave van uw winkelpagina&#39;s van PayPal aanpassen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Frontend Experience Settings]** sectie uit.

   ![ De Montages van de Begeleving van de Voorzijde - PayPal Payflow Pro ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Stap 6: De basisinstellingen voor PayPal Express Checkout voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Basic Settings - PayPal Express Checkout]** sectie uit.

   ![ Uitdrukkelijke Basismontages van de Controle ](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Voer bij **[!UICONTROL Title]** een titel in die deze betalingsmethode identificeert tijdens het afrekenen.

   Het plaatsen van de titel aan _PayPal_ voor elke opslagmening wordt geadviseerd.

1. Als u meerdere betalingsmethoden aanbiedt, voert u een getal voor **[!UICONTROL Sort Order]** in om de volgorde te bepalen waarin PayPal Express Checkout wordt weergegeven wanneer deze bij de andere betalingsmethoden wordt aangeboden.

   Dit getal is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Stel **[!UICONTROL Payment Action]** in op een van de volgende opties:

   - `Authorization` - Hiermee gaat u akkoord met de aankoop en houdt u de middelen in de wacht. Het bedrag wordt niet teruggetrokken tot het __ door de koopman wordt gevangen.
   - `Sale` - Het bedrag van de aankoop wordt geautoriseerd en onmiddellijk van de rekening van de klant teruggetrokken.

1. Stel **[!UICONTROL Display on Product Details Page]** in op `Yes` om de knop _[!UICONTROL Check out with PayPal]_&#x200B;op de productpagina weer te geven.

### Stap 7: De geavanceerde instellingen voor PayPal Express-afhandeling voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Advanced Settings]** sectie uit.

   ![ Uitdrukkelijke Controle Geavanceerde Vestiging ](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Display on Shopping Cart]** in op `Yes` .

1. Stel **[!UICONTROL Payment Applicable From]** in op een van de volgende opties:

   - `All Allowed Countries` - Klanten uit alle landen die in uw winkelconfiguratie zijn opgegeven, kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_&#x200B;weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elk item.

1. Als u communicatie met het betalingssysteem naar het logbestand wilt schrijven, stelt u **[!UICONTROL Debug Mode]** in op `Yes` .

   >[!NOTE]
   >
   >In overeenstemming met de normen van de Veiligheid van Gegevens PCI, wordt de creditcardinformatie niet geregistreerd in het logboekdossier.

1. Als u verificatie van de authenticiteit van de host wilt inschakelen, stelt u **[!UICONTROL Enable SSL Verification]** in op `Yes` .

1. Stel **[!UICONTROL Transfer Cart Line Items]** in op `Yes` als u een volledig overzicht van de bestelling van de klant per lijstitem vanaf de PayPal-site wilt weergeven.

1. Stel **[!UICONTROL Skip Order Review Step]** in op `Yes` als u de klant wilt toestaan de transactie van de PayPal-site te voltooien zonder deze terug te sturen naar uw winkel voor het reviseren van bestellingen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Stap 8: Google reCAPTCHA toevoegen

Schakel Google reCAPTCHA in om PayPal Payflow Pro beter te beschermen. Het omvat opties om reCAPTCHA in werking te stellen gebruikend een klikbare interface of een onzichtbare controle om de klant te bevestigen. De onzichtbare optie wordt aanbevolen om de verkoopconversie te verhogen en uw winkel te beschermen. Voor details, zie [ Google reCAPTCHA ](../systems/security-google-recaptcha.md).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
