---
title: Belastingconfiguratie-instellingen
description: Leer hoe u elementaire belastinginstellingen configureert, waaronder belastingklassen, berekening en de standaardbelastingbestemming.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Belastingconfiguratie-instellingen

De volgende instructies nemen u door de basisbelastingconfiguratie voor uw Commerce-exemplaar. Alvorens vestiging uw belastingen, zorg ervoor dat u met de belastingvereisten van uw [&#x200B; scène &#x200B;](store-localize.md#step-3-change-the-locale-of-the-store-view) vertrouwd bent. Voltooi vervolgens de belastingconfiguratie volgens uw vereisten.

Admin [&#x200B; toestemmingen &#x200B;](../systems/permissions.md) kunnen worden geplaatst om [&#x200B; toegang &#x200B;](../systems/permissions-user-roles.md) aan belastingmiddelen te beperken, die op de zaken _worden gebaseerd moet_ kennen. Als u een beheerdersrol wilt maken met toegang tot belastinginstellingen, kiest u zowel de BTW- als de systeembronnen. Als u een website instelt voor een gebied dat afwijkt van uw standaard verzendpunt van oorsprong, moet u ook toegang verlenen tot de bronnen voor Systeem/Verzending voor de rol. De verzendinstellingen bepalen het BTW-tarief voor de winkel dat wordt gebruikt voor catalogusprijzen.

## De algemene belastinginstellingen configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Voor een configuratie met meerdere sites stelt u **[!UICONTROL Store View]** in op de website en slaat u die configuratie als doel heeft.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Tax]** .

1. Voer de volgende configuratie-instellingen uit.

   Wis indien nodig het selectievakje **[!UICONTROL Use system value]** van instellingen die grijs worden weergegeven.

### [!UICONTROL Tax Classes]

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Tax Classes]** sectie uit.

   ![&#x200B; Belastingklassen &#x200B;](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Klasse van de Belasting voor Verzending** — Reeks aan de aangewezen klasse. De standaardklassen zijn: `None` en `Taxable Goods`
   - **de Klasse van de Belasting voor de Opties van het Cadeautje** - ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) plaatste aan de aangewezen klasse. De standaardklassen zijn: `None` en `Taxable Goods`
   - **StandaardKlasse van de Belasting voor Product** — Reeks aan de aangewezen klasse. De standaardklassen zijn: `None` en `Taxable Goods`
   - **StandaardKlasse van de Belasting voor Klant** — Reeks aan de aangewezen klasse. De standaardklasse is: `Retail Customer` en `Wholesale Customer`

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### [!UICONTROL Calculation Settings]

1. Vouw de sectie **[!UICONTROL Calculation Settings]** uit.

   ![&#x200B; de Montages van de Berekening &#x200B;](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Tax Calculation Method Based On]** in op een van de volgende opties:

   - `Unit Price` - De prijs van elk product
   - `Row Total` - Het totaal van het lijstitem in de volgorde, minus kortingen
   - `Total` - Het totaal van de volgorde

1. Stel **[!UICONTROL Tax Calculation Based On]** in op een van de volgende opties:

   - `Shipping Address` - Het adres waar de bestelling moet worden verzonden
   - `Billing Address` - Het factureringsadres van de klant of het bedrijf
   - `Shipping Origin` - het adres dat als [&#x200B; uitgangspunt &#x200B;](shipping-settings.md#point-of-origin) voor uw opslag wordt gespecificeerd

1. Stel **[!UICONTROL Catalog Prices]** in op `Excluding Tax` of `Including Tax` .

1. Stel **[!UICONTROL Shipping Prices]** in op `Excluding Tax` of `Including Tax` .

1. Stel **[!UICONTROL Apply Customer Tax]** in op een van de volgende opties om te bepalen of belasting wordt toegepast op de oorspronkelijke prijs of op de gedisconteerde prijs: `After Discount` of `Before Discount`

1. Stel **[!UICONTROL Apply Discount on Prices]** in op een van de volgende opties om te bepalen of kortingen belasting bevatten of uitsluiten: `Excluding Tax` of `Including Tax`

1. Stel **[!UICONTROL Apply Tax On]** in op `Custom price if available` of `Original price only` .

1. Stel **[!UICONTROL Enable Cross-Border Trade]** in op een van de volgende opties:

   - `Yes` - Gebruik consistente prijzen voor verschillende belastingtarieven. Als de catalogusprijs ook belasting bevat, kiest u deze instelling om de prijs vast te stellen, ongeacht het belastingtarief van de klant.
   - `No` - Verander de prijs door belastingtarief.

   >[!IMPORTANT]
   >
   >Als [&#x200B; grensoverschrijdende handel &#x200B;](#cross-border-price-consistency) wordt toegelaten, verandert de winstmarge door belastingtarief. De winst wordt bepaald door de formule (`Revenue - CustomerVAT - CostOfGoodsSold`). Om grensoverschrijdende handel mogelijk te maken, moeten de prijzen worden vastgesteld op basis van belastingen.

### [!UICONTROL Default Tax Destination Calculation]

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Default Tax Destination Calculation]** sectie uit.

   ![&#x200B; Berekening van de StandaardBelastingbestemming &#x200B;](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Geef de **[!UICONTROL Default Country]** op voor belastingberekeningen.

1. Geef indien van toepassing de **[!UICONTROL Default State]** op voor belastingberekeningen.

1. Geef indien van toepassing de **[!UICONTROL Default Post Code]** op voor belastingberekeningen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Sommige combinaties van instellingen met betrekking tot een prijsweergave die zowel belasting bevatten als uitsluiten, kunnen verwarrend zijn voor de klant. Om het teweegbrengen van een waarschuwingsbericht te vermijden, zie [&#x200B; geadviseerde montages &#x200B;](taxes.md#warning-messages).

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Price Display Settings]** sectie uit.

   ![&#x200B; de Montages van de Vertoning van de Prijs &#x200B;](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Display Product Prices in Catalog]** in op een van de volgende opties:

   - `Excluding Tax` - Catalogusprijzen die in de winkel worden weergegeven, omvatten geen belasting.
   - `Including Tax` - Catalogusprijzen in de winkel omvatten alleen belasting als een belastingregel overeenkomt met de belastingoorsprong of als het adres van de klant overeenkomt met de belastingregel. Dit kan gebeuren als een klant een account maakt, zich aanmeldt of het gereedschap Belasting en verzending schatten in de winkelwagen gebruikt.
   - `Including and Excluding Tax` - Catalogusprijzen die in de winkel worden weergegeven, worden zowel met als zonder belasting weergegeven.

1. Stel **[!UICONTROL Display Shipping Prices]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### [!UICONTROL Shopping Cart Display Settings]

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Shopping Cart Display Settings]** sectie uit.

   ![&#x200B; het Shopping de Montages van de Vertoning van de Kar &#x200B;](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Kies voor elk van de volgende instellingen hoe u belastingen en prijzen in het winkelwagentje wilt weergeven, afhankelijk van de vereisten van uw winkel en landinstelling:

   - Stel **[!UICONTROL Display Prices]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

   - Stel **[!UICONTROL Display Subtotal]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

   - Stel **[!UICONTROL Display Shipping Amount]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

   - ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Display Gift Wrapping Prices]** aan `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Display Printed Card Prices]** aan `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

1. Stel de volgende weergaveopties naar wens in op `Yes` of `No` :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Breid ![&#x200B; Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** sectie.

   ![&#x200B; Orders, Facturen, de Montages van de Vertoning van de Memo&#39;s van Kredieten &#x200B;](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Geef op hoe prijzen en belastingen in bestellingen, facturen en creditnota&#39;s worden weergegeven:

   - Stel **[!UICONTROL Display Prices]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

   - Stel **[!UICONTROL Display Subtotal]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

   - Stel **[!UICONTROL Display Shipping Amount]** in op `Excluding Tax` , `Including Tax` of `Including and Excluding Tax` .

   - ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Display Gift Wrapping Prices]** aan `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Display Printed Card Prices]** aan `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

1. Stel de volgende weergaveopties naar wens in op `Yes` of `No` :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### [!UICONTROL Fixed Product Taxes]

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Fixed Product Taxes]** sectie uit.

   ![&#x200B; Vaste Belastingen van het Product &#x200B;](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable FPT]** naar wens in op `Yes` of `No` .

1. Als FPT is ingeschakeld, geeft u de weergaveopties voor FPT op:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Weergegeven prijzen omvatten vaste productbelastingen. De hoeveelheid FPT wordt niet afzonderlijk weergegeven.
   - `Including FPT and FPT description` - Weergegeven prijzen omvatten vaste productbelastingen. De hoeveelheid FPT wordt afzonderlijk weergegeven.
   - `Excluding FPT. Including FPT description and final price` - Weergegeven prijzen omvatten geen vaste productbelastingen. De hoeveelheid FPT wordt afzonderlijk weergegeven.
   - `Excluding FPT` - Weergegeven prijzen omvatten geen vaste productbelastingen. De hoeveelheid FPT wordt niet afzonderlijk weergegeven.

1. Stel **[!UICONTROL Apply Discounts to FPT]** in op `Yes` of `No` , afhankelijk van uw vereisten.

1. Stel **[!UICONTROL FPT Tax Configuration]** in om te bepalen hoe FPT wordt berekend.

   - `Not Taxed` - Selecteer deze optie als uw belastingjurisdictie geen FPT belast. (Bijvoorbeeld Californië.)
   - `Taxed` - Selecteer deze optie als uw belastingjurisdictie FPT wel belast. (Bijvoorbeeld Canada.)
   - `Loaded and Displayed with Tax` - Klik op deze optie als FPT wordt toegevoegd aan het totaal van de bestelling voordat u belasting toepast. (Bijvoorbeeld EU-landen.)

1. Stel **[!UICONTROL Include FPT in Subtotal]** in op `Yes` of `No` , afhankelijk van uw vereisten.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Grensoverschrijdende prijsconsistentie

Grensoverschrijdende handel (ook wel prijsconsistentie genoemd) ondersteunt de Europese Unie (EU) en andere handelaren die consistente prijzen willen handhaven voor klanten wier belastingtarieven verschillen van het belastingtarief voor winkels.

Handelaren die in verschillende regio&#39;s en geografische gebieden actief zijn, kunnen één prijs weergeven door de belasting in de prijs van het product op te nemen. De prijzen zijn schoon en onoverzichtelijk, ongeacht de belastingstructuren en -tarieven die van land tot land verschillen. Deze montages vereisen dat een uitbreiding van de belastingberekening van [&#x200B; Marketplace &#x200B;](../getting-started/commerce-marketplace.md), zoals _de Wolk van de Hoekpunt_ wordt geïnstalleerd.

>[!NOTE]
>
>Wanneer grensoverschrijdende handel is ingeschakeld, wordt de winstmarge aangepast aan het belastingtarief. De winst wordt bepaald door de formule:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_om grensoverschrijdende prijsconsistentie toe te laten:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Voor een configuratie met meerdere sites stelt u **[!UICONTROL Store View]** in op de website en slaat u die configuratie als doel heeft.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Tax]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Calculation Settings]** sectie uit.

1. Stel **[!UICONTROL Catalog Prices]** in op `Including Tax` .

1. Stel **[!UICONTROL Enable Cross Border Trade]** in op `Yes` om consistentie bij grensoverschrijdende prijzen mogelijk te maken.

   ![&#x200B; laat Grensoverschrijdende handelsinstellingen &#x200B;](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
