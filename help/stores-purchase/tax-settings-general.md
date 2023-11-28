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

De volgende instructies nemen u door de basisbelastingconfiguratie voor uw instantie van de Handel. Voordat u belastingen instelt, moet u controleren of u bekend bent met de belastingvereisten van uw [landinstelling](store-localize.md#step-3-change-the-locale-of-the-store-view). Voltooi vervolgens de belastingconfiguratie volgens uw vereisten.

Beheerder [machtigingen](../systems/permissions.md) kan worden ingesteld op [toegang](../systems/permissions-user-roles.md) op basis van de bedrijfsactiviteit _moeten weten_. Als u een beheerdersrol wilt maken met toegang tot belastinginstellingen, kiest u zowel de BTW- als de systeembronnen. Als u een website instelt voor een gebied dat afwijkt van uw standaard verzendpunt van oorsprong, moet u ook toegang verlenen tot de bronnen voor Systeem/Verzending voor de rol. De verzendinstellingen bepalen het BTW-tarief voor de winkel dat wordt gebruikt voor catalogusprijzen.

## De algemene belastinginstellingen configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Voor een configuratie met meerdere sites stelt u **[!UICONTROL Store View]** naar de website en opslag die het doel van de configuratie is.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Tax]**.

1. Voer de volgende configuratie-instellingen uit.

   Indien nodig de **[!UICONTROL Use system value]** Schakel het selectievakje in van instellingen die grijs worden weergegeven.

### [!UICONTROL Tax Classes]

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Tax Classes]** sectie.

   ![Belastingklassen](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Belastingklasse voor verzending** — Instellen op de juiste klasse. De standaardklassen zijn: `None` en `Taxable Goods`
   - **Belastingsklasse voor Cadeauopties** — ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Stel dit in op de juiste klasse. De standaardklassen zijn: `None` en `Taxable Goods`
   - **Standaardbelastingklasse voor product** — Instellen op de juiste klasse. De standaardklassen zijn: `None` en `Taxable Goods`
   - **Standaardbelastingklasse voor klant** — Instellen op de juiste klasse. De standaardklasse is: `Retail Customer` en `Wholesale Customer`

1. Klik op **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Vouw de sectie **[!UICONTROL Calculation Settings]** uit.

   ![Instellingen voor berekening](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Tax Calculation Method Based On]** op een van de volgende wijzen:

   - `Unit Price` - De prijs van elk product
   - `Row Total` - Het totaal van het lijnitem in de volgorde, minus kortingen
   - `Total` - Het totaal van de bestelling

1. Set **[!UICONTROL Tax Calculation Based On]** op een van de volgende wijzen:

   - `Shipping Address` - Het adres waar de bestelling moet worden verzonden
   - `Billing Address` - Het factureringsadres van de klant of het bedrijf
   - `Shipping Origin` - Het adres dat als [punt van oorsprong](shipping-settings.md#point-of-origin) voor uw winkel

1. Set **[!UICONTROL Catalog Prices]** tot `Excluding Tax` of `Including Tax`.

1. Set **[!UICONTROL Shipping Prices]** tot `Excluding Tax` of `Including Tax`.

1. Set **[!UICONTROL Apply Customer Tax]** op een van de volgende wijzen om te bepalen of de belasting op de oorspronkelijke prijs of op de verlaagde prijs wordt toegepast: `After Discount` of `Before Discount`

1. Set **[!UICONTROL Apply Discount on Prices]** op een van de volgende manieren te bepalen of kortingen belastingen omvatten of uitsluiten: `Excluding Tax` of `Including Tax`

1. Set **[!UICONTROL Apply Tax On]** tot `Custom price if available` of `Original price only`.

1. Set **[!UICONTROL Enable Cross-Border Trade]** op een van de volgende wijzen:

   - `Yes` - Gebruik consistente prijzen voor verschillende belastingtarieven. Als de catalogusprijs ook belasting bevat, kiest u deze instelling om de prijs vast te stellen, ongeacht het belastingtarief van de klant.
   - `No` - Verander de prijs per belastingtarief.

   >[!IMPORTANT]
   >
   >Indien [grensoverschrijdende handel](#cross-border-price-consistency) wordt toegelaten, verandert de winstmarge door belastingtarief. De winst wordt bepaald door de formule (`Revenue - CustomerVAT - CostOfGoodsSold`). Om grensoverschrijdende handel mogelijk te maken, moeten de prijzen worden vastgesteld op basis van belastingen.

### [!UICONTROL Default Tax Destination Calculation]

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Default Tax Destination Calculation]** sectie.

   ![Berekening standaardbelastingbestemming](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Geef de **[!UICONTROL Default Country]** voor belastingberekeningen.

1. Geef, indien van toepassing, de **[!UICONTROL Default State]** voor belastingberekeningen.

1. Geef, indien van toepassing, de **[!UICONTROL Default Post Code]** voor belastingberekeningen.

1. Klik op **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Sommige combinaties van instellingen met betrekking tot een prijsweergave die zowel belasting bevatten als uitsluiten, kunnen verwarrend zijn voor de klant. Als u wilt voorkomen dat een waarschuwingsbericht wordt geactiveerd, raadpleegt u de [aanbevolen instellingen](taxes.md#warning-messages).

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Price Display Settings]** sectie.

   ![Weergave-instellingen prijs](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Display Product Prices in Catalog]** op een van de volgende wijzen:

   - `Excluding Tax` - Catalogusprijzen die in de winkelruimte worden weergegeven, omvatten geen belasting.
   - `Including Tax` - Catalogusprijzen in de winkel omvatten alleen belasting als een belastingregel overeenkomt met de fiscale oorsprong of als het adres van de klant overeenkomt met de belastingregel. Dit kan gebeuren als een klant een account maakt, zich aanmeldt of het gereedschap Belasting en verzending schatten in de winkelwagen gebruikt.
   - `Including and Excluding Tax` - Catalogusprijzen die in de winkel worden weergegeven, worden zowel met als zonder belasting weergegeven.

1. Set **[!UICONTROL Display Shipping Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

1. Klik op **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Shopping Cart Display Settings]** sectie.

   ![Weergave-instellingen winkelwagentje](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Kies voor elk van de volgende instellingen hoe u belastingen en prijzen in het winkelwagentje wilt weergeven, afhankelijk van de vereisten van uw winkel en landinstelling:

   - Set **[!UICONTROL Display Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - Set **[!UICONTROL Display Subtotal]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - Set **[!UICONTROL Display Shipping Amount]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Display Gift Wrapping Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Display Printed Card Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

1. Stel de volgende weergaveopties in op `Yes` of `No`, afhankelijk van uw behoeften:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klik op **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Uitbreiden ![Uitbreiding](../assets/icon-display-expand.png) de **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** sectie.

   ![Weergave-instellingen voor bestellingen, facturen, creditcards](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Geef op hoe prijzen en belastingen in bestellingen, facturen en creditnota&#39;s worden weergegeven:

   - Set **[!UICONTROL Display Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - Set **[!UICONTROL Display Subtotal]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - Set **[!UICONTROL Display Shipping Amount]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Display Gift Wrapping Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Display Printed Card Prices]** tot `Excluding Tax`, `Including Tax`, of `Including and Excluding Tax`.

1. Stel de volgende weergaveopties in op `Yes` of `No`, op basis van uw vereisten:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klik op **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Fixed Product Taxes]** sectie.

   ![Vaste productbelastingen](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable FPT]** aan of `Yes` of `No`, op basis van uw vereisten.

1. Als FPT is ingeschakeld, geeft u de weergaveopties voor FPT op:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Weergegeven prijzen omvatten vaste productbelastingen. De hoeveelheid FPT wordt niet afzonderlijk weergegeven.
   - `Including FPT and FPT description` - Weergegeven prijzen omvatten vaste productbelastingen. De hoeveelheid FPT wordt afzonderlijk weergegeven.
   - `Excluding FPT. Including FPT description and final price` - De weergegeven prijzen omvatten geen vaste productbelastingen. De hoeveelheid FPT wordt afzonderlijk weergegeven.
   - `Excluding FPT` - De weergegeven prijzen omvatten geen vaste productbelastingen. De hoeveelheid FPT wordt niet afzonderlijk weergegeven.

1. Set **[!UICONTROL Apply Discounts to FPT]** tot `Yes` of `No`, op basis van uw vereisten.

1. Set **[!UICONTROL FPT Tax Configuration]** bepalen hoe FPT wordt berekend.

   - `Not Taxed` - Selecteer deze optie als uw belastingjurisdictie FPT niet belast. (Bijvoorbeeld Californië.)
   - `Taxed` - Selecteer deze optie als de belastingjurisdictie FPT wel belast. (Bijvoorbeeld Canada.)
   - `Loaded and Displayed with Tax` - Klik op deze optie als FPT wordt toegevoegd aan het totaal van de bestelling voordat u belasting toepast. (Bijvoorbeeld EU-landen.)

1. Set **[!UICONTROL Include FPT in Subtotal]** tot `Yes` of `No`, op basis van uw vereisten.

1. Klik op **[!UICONTROL Save Config]**.

## Grensoverschrijdende prijsconsistentie

Grensoverschrijdende handel (ook wel prijsconsistentie genoemd) ondersteunt de Europese Unie (EU) en andere handelaren die consistente prijzen willen handhaven voor klanten wier belastingtarieven verschillen van het belastingtarief voor winkels.

Handelaren die in verschillende regio&#39;s en geografische gebieden actief zijn, kunnen één prijs weergeven door de belasting in de prijs van het product op te nemen. De prijzen zijn schoon en onoverzichtelijk, ongeacht de belastingstructuren en -tarieven die van land tot land verschillen. Voor deze instellingen moet een extensie voor belastingberekening zijn geïnstalleerd vanaf het tabblad [Marketplace](../getting-started/commerce-marketplace.md), zoals _Vertex Cloud_.

>[!NOTE]
>
>Wanneer grensoverschrijdende handel is ingeschakeld, wordt de winstmarge aangepast aan het belastingtarief. De winst wordt bepaald aan de hand van de formule:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Om de consistentie van de grensoverschrijdende prijzen mogelijk te maken:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Voor een configuratie met meerdere sites stelt u **[!UICONTROL Store View]** naar de website en opslag die het doel van de configuratie is.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Tax]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Calculation Settings]** sectie.

1. Set **[!UICONTROL Catalog Prices]** tot `Including Tax`.

1. Om grensoverschrijdende prijsconsistentie mogelijk te maken, stelt u **[!UICONTROL Enable Cross Border Trade]** tot `Yes`.

   ![Instellingen voor grensoverschrijdende handel inschakelen](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
