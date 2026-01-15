---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Sales] van Commerce Admin.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![&#x200B; Algemeen &#x200B;](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | Winkelweergave | Hiermee bepaalt u of het IP-adres van de klant wordt weergegeven op bestellingen, facturen, verzendingen en creditnota&#39;s. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![&#x200B; Afhandelingstotalen de Orde van de Sortering &#x200B;](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-totals-sort-order) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Website | Een getal dat bepaalt wanneer het subtotaal wordt berekend ten opzichte van andere uitchecktotalen. Standaardwaarde: `10` |
| [!UICONTROL Discount] | Website | Een getal dat bepaalt wanneer de korting wordt berekend ten opzichte van andere uitchecktotalen. Standaardwaarde: `20` |
| [!UICONTROL Shipping] | Website | Een getal dat bepaalt wanneer de verzendkosten worden berekend ten opzichte van andere uitchecktotalen. Standaardwaarde: `30` |
| [!UICONTROL Tax] | Website | Een getal dat bepaalt wanneer belasting wordt berekend ten opzichte van andere uitchecktotalen. Standaardwaarde: `40` |
| [!UICONTROL Fixed Product Tax] | Website | Een getal dat bepaalt wanneer de Vaste productbelasting wordt berekend ten opzichte van andere uitchecktotalen. Standaardwaarde: `50` |
| [!UICONTROL Grand Total] | Website | Een getal dat bepaalt wanneer het Eindtotaal wordt berekend ten opzichte van andere uitchecktotalen. Standaardwaarde: `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![&#x200B; herschikt &#x200B;](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/shopper-tools/reorders-allow) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | Winkelweergave | Hiermee bepaalt u of de klanten de volgorde van hun accounts kunnen wijzigen. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | Winkelweergave | Bepaalt de mogelijkheid om een creditmemo met een totaal nul te creëren. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![&#x200B; Factuur en het Pakken Ontwerp van de Scheiding &#x200B;](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | Winkelweergave | Identificeert het logobestand dat wordt weergegeven in de koptekst van PDF-facturen en verpakkingsslips. Toegestane dossiertypes: <br/> JPG/JPEG <br/> TIF/TIFF <br/> PNG |
| [!UICONTROL Logo for HTML Print View] | Winkelweergave | Hiermee wordt het logobestand aangegeven dat wordt weergegeven in de koptekst van de afdrukweergave van HTML van facturen en verpakkingsschuifregelaars. Toegestane dossiertypes: <br/> JPG /JPEG <br/> GIF <br/> PNG |
| [!UICONTROL Address] | Winkelweergave | Het adres van de winkel waar u het wilt weergeven op facturen en pakslips. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![&#x200B; Minimale Hoeveelheid van de Orde &#x200B;](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#minimum-order-amount) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable] | Website | Hiermee wordt bepaald of een minimale orderhoeveelheid is ingesteld voor de site. Opties: `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Website | Hiermee wordt het minimale subtotaal opgegeven. De volgorde na kortingen wordt toegepast. |
| [!UICONTROL Include Discount Amount] | Website | Hiermee wordt bepaald of het minimumorderbedrag toegepaste kortingen omvat. Opties: `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Website | Hiermee wordt bepaald of het minimumbedrag van de bestelling inclusief belasting is. Opties: `Yes` / `No` |
| [!UICONTROL Description Message] | Winkelweergave | Hiermee bepaalt u het bericht dat boven aan het winkelwagentje wordt weergegeven wanneer het aantal winkelwagentjes lager is dan het minimale aantal bestellingen. Indien leeg gelaten, verschijnt het volgende standaardbericht: `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | Winkelweergave | Hiermee bepaalt u het bericht dat wordt weergegeven van de mini-winkelwagen of de uitcheckkoppeling wanneer het orderbedrag lager is dan het vereiste minimale orderbedrag. Als deze optie leeg blijft, wordt een standaardbericht weergegeven. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Website | Voor multi-item orden, bepaalt als de orde punten die aan afzonderlijke adressen gaan veel aan het minimumordebedrag voldoen. Opties: `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | Winkelweergave | Voor multi-adresorden, bepaalt het bericht dat in het het winkelwagentje verschijnt als de punten die naar een adres worden verzonden minder dan het minimumordebedrag zijn. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | Winkelweergave | Voor multi-adresorden, bepaalt het bericht dat van de mini kart of controleverbinding verschijnt wanneer het ordebedrag minder dan het vereiste minimumordebedrag is. Als deze optie leeg blijft, wordt een standaardbericht weergegeven. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![&#x200B; Dashboard &#x200B;](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://experienceleague.adobe.com/nl/docs/commerce-admin/start/admin/tools/admin-dashboard) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | Algemeen | Hiermee bepaalt u of real-time, samengevoegde verkoopgegevens worden gebruikt om momentopnamerapporten van het dashboard te maken. Als u een grote hoeveelheid gegevens hebt te verwerken, kunnen de prestaties worden verbeterd door de weergave van realtime gegevens uit te schakelen. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![&#x200B; orden de Montages van het Gewas &#x200B;](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://experienceleague.adobe.com/nl/docs/commerce-admin/systems/tools/cron) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Website | Bepaalt de levensduur van lopende orders in minuten. Standaardinstelling: `480` minuten (8 uur) |

{style="table-layout:auto"}

## [!UICONTROL Promotions]

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service-projecten (door Adobe beheerde SaaS-infrastructuur)."}

[!BADGE &#x200B; Sandbox &#x200B;]{type=Caution tooltip="De vermelde items zijn momenteel alleen beschikbaar in Sandbox-omgevingen. Adobe stelt nieuwe releases eerst beschikbaar in Sandbox-omgevingen, zodat u tijd hebt om toekomstige wijzigingen te testen voordat de release beschikbaar is in Productomgevingen."}

![&#x200B; de Montages van Bevorderingen &#x200B;](./assets/sales-promotions-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Apply Catalog Price Rule on Grouped Price] | Algemeen | Laat [&#x200B; rijtarifering voor catalogusprijsregels &#x200B;](../../catalog/product-price-tier.md) toe wanneer de hoeveelheid van een rijprijs aan `1` wordt geplaatst.  Opties: `Yes` / `No` |

## [!UICONTROL Gift Options]

![&#x200B; Cadeauopties &#x200B;](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#gift-options) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Website | Geef op of u een geschenk voor de gehele bestelling wilt toevoegen. |
| [!UICONTROL Allow Gift Messages on Order Items] | Website | Geef op of een cadeaubericht kan worden toegevoegd voor een afzonderlijk orderitem. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Website | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) specificeer of de gift het verpakken voor de volledige orde kan worden toegevoegd. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Website | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) specificeer of de gift het verpakken voor het individuele orde punt kan worden toegevoegd. |
| [!UICONTROL Allow Gift Receipt] | Website | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) specificeer of een geschenkontvangstbewijs voor de orde kan worden toegevoegd. |
| [!UICONTROL Allow Printed Card] | Website | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) specificeert of een gedrukte kaart voor de orde kan worden toegevoegd. |
| [!UICONTROL Default Price for Printed Card] | Website | ![&#x200B; Adobe Commerce &#x200B;](../../assets/adobe-logo.svg) (Adobe Commerce slechts) specificeer de standaardprijs voor de gedrukte kaart. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![&#x200B; Minimale Geadverteerde Prijs &#x200B;](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://experienceleague.adobe.com/nl/docs/commerce-admin/catalog/products/pricing/product-price-minimum-advertised) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Website | Hiermee activeert u de minimale geadverteerde prijs voor je winkel. Opties: `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Website | Hiermee bepaalt u waar de werkelijke prijs van een product zichtbaar is voor de klant. Opties: <br/>**`In Cart`**- Geeft de werkelijke productprijs weer in het winkelwagentje.<br/>**`Before Order Confirmation`** - Geeft de werkelijke productprijs weer aan het einde van het afrekenproces, vlak voordat de bestelling wordt bevestigd. <br/>**`On Gesture`**- Geeft de werkelijke productprijs weer in een pop-up wanneer de klant klikt op de optie &quot;Klik voor prijs&quot; of &quot;Wat is dit?&quot; koppeling. |
| [!UICONTROL Default Popup Text Message] | Winkelweergave | Het tekstbericht dat wordt weergegeven wanneer de klant de koppeling &quot;Klik voor prijs&quot; selecteert in een categorielijst of productweergavepagina. |
| [!UICONTROL Default "What's This" Text Message] | Winkelweergave | Het tekstbericht dat verschijnt wanneer de klant &quot;wat is dit?&quot;klikt koppeling op de pagina met productweergave. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | Algemeen | De door de fabrikant voorgestelde eindgebruikersprijs (MSRP). |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![&#x200B; Multicoupon Montages &#x200B;](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Website | Hiermee bepaalt u het maximum aantal toegestane coupons per bestelling. Deze functie is alleen beschikbaar in Admin, GraphQL en REST API. En het is **_niet beschikbaar_** in Storefront. |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![&#x200B; Orde door de Montages van SKU &#x200B;](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/point-of-purchase/cart/order-by-sku) -->

![&#x200B; Orde door de Montages van SKU voor de Groep van de Klant &#x200B;](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Website | Bepaalt als de Orde door SKU in het dashboard van de klantenrekening beschikbaar is. Opties: <br/>**`Yes, for Everyone`**- het tabblad Order by SKU wordt weergegeven in het accountdashboard van alle klanten.<br/>**`Yes, for Specified Customer Groups`** - Het tabblad Volgorde op SKU wordt weergegeven in het accountdashboard voor leden van opgegeven groepen of een gedeelde catalogus. <br/>**`No`**- Het tabblad Order by SKU is niet beschikbaar in de klantenaccount. |
| [!UICONTROL Customer Groups] | Website | Bepaalt de Klantengroepen. Opties: `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![&#x200B; Onmiddellijke Aankoop &#x200B;](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://experienceleague.adobe.com/nl/docs/commerce-admin/stores-sales/point-of-purchase/checkout-instant-purchase) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Winkelweergave | Hiermee schakelt u Onmiddellijke aanschaf in voor de winkelweergave, als de betalingsmethode, zoals Braintree, vault heeft ingeschakeld. Opties: `Yes` / `No` |
| [!UICONTROL Button Text] | Winkelweergave | Hiermee geeft u de tekst op die op de knop Onmiddellijk aanschaffen wordt weergegeven. De standaardtekst is `Instant Purchase` . |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![&#x200B; Tarief die &#x200B;](assets/sales-rate-limiting.png)<!-- zoom --> begrenzen

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | Winkelweergave | Hiermee bepaalt u of snelheidsbeperking wordt gebruikt voor het plaatsen van orders in de winkelweergave (de standaardwaarde is `No` ). Opties: `Yes` / `No` . |
| [!UICONTROL Requests limit per authenticated customer] | Winkelweergave | Het aantal koopverzoeken dat een voor authentiek verklaarde klant tijdens de periode kan maken. De standaardlimiet is `10` . |
| [!UICONTROL Requests limit per guest] | Winkelweergave | Het aantal koopverzoeken dat een niet-geverifieerde klant tijdens de opgegeven periode kan indienen. De standaardwaarde is `50` . |
| [!UICONTROL Counter resets in a ...] | Winkelweergave | De periode waarin een geverifieerde/niet-geverifieerde klant een bepaald aantal aankoopaanvragen kan indienen (de standaardwaarde is `Minute` ). Opties: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![&#x200B; orden, Facturen, Verzendingen, het Archiveren van de Memo&#39;s van de Krediet &#x200B;](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [&#x200B; het ordearchief &#x200B;](../../stores-purchase/order-archive.md#configure-the-order-archive) in de _Gids van de Opslag en van de Ervaring van de Aankoop_ vormen.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | Algemeen | Hiermee wordt bepaald of archiveren is ingeschakeld. Opties: `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | Algemeen | Hiermee bepaalt u het aantal dagen dat doorgaat voordat een voltooide bestelling wordt gearchiveerd. Standaardwaarde: `30` |
| [!UICONTROL Order  Statuses to be Archived] | Algemeen | Bepaalt de [&#x200B; status &#x200B;](../../stores-purchase/order-status.md) van te archiveren orden. Standaard worden bestellingen met de status Voltooid of Gesloten gearchiveerd. Opties: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![&#x200B; Montages RMA &#x200B;](./assets/sales-rma-settings.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [&#x200B; terugkeren &#x200B;](../../stores-purchase/rma-configure.md) in de _Gids van de Opslag en van de Ervaring van de Aankoop_ vormen.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Website | Bepaalt als de klanten RMA- verzoeken van de storefront kunnen tot stand brengen en bekijken. RMA kan op zowel nieuwe als bestaande orden worden toegepast. Standaard is RMA niet ingeschakeld voor de storefront. Opties: `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Website | Bepaalt de standaardwaarde voor het Enable gebied RMA in productinformatie. |
| [!UICONTROL Use Store Address] | Website | Hiermee bepaalt u de naam en het adres van de contactpersoon die wordt gebruikt voor zendingen geretourneerde goederen. Opties: <br/>**`Yes`**- gebruikt het [&#x200B; Punt van Oorsprong &#x200B;](../../stores-purchase/shipping-settings.md#point-of-origin) adres van het Verschepen Montages.<br/>**`No`** - Hiermee opent u het adresformulier, zodat u een alternatief adres kunt invoeren. |

{style="table-layout:auto"}
