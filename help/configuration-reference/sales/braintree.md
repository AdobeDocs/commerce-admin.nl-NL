---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Controleer de configuratie-instellingen voor de [!UICONTROL Braintree] de [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] pagina van de Commerce Admin.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '2330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Handel 2.4 Migratie:**<br/>
>Voor eerdere versies van Adobe Commerce en Magento Open Source dan versie 2.4.0 werd aanbevolen dat verkopers de extensie voor de officiële integratie van Braintreeën installeren en configureren vanuit de [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) de kernintegratie te vervangen. Vanaf 2.4.0 is de extensie nu opgenomen in de kernrelease.
><br/><br/>
>Bij de migratie naar Handel 2.4 moeten handelaren de extensie verwijderen die op de Marketplace wordt gedistribueerd (`paypal/module-braintree` of `gene/module-braintree`) en eventuele codeaanpassingen bijwerken om de `PayPal_Braintree` naamruimte in plaats van `Magento_Braintree`. De montages van de configuratie van de gebundelde uitbreiding voor Handel en de uitbreiding die op de Commerce Marketplace wordt verdeeld worden voortgeduurd. Betalingen die met die versies van de extensie worden geplaatst, worden als normaal vastgelegd, geweigerd of terugbetaald.
><br/><br/>
>Als u aan Handel 2.4.0 bevordert en niet de geadviseerde uitbreiding van de Commerce Marketplace in uw vorige versie 2.3.x gebruikt, werkt de multi adreseigenschap niet met versie 2.4.0 van Braintree. Wanneer een winkelier selecteert _leveren aan veelvoudige adressen_ , wordt de betalingsmethode voor Braintree niet weergegeven. De eerder voor 2.3.x geadviseerde uitbreiding van de Commerce Marketplace heeft deze veelvoudige adreskwestie.

{{config}}

{{beta2-updates}}

## [!UICONTROL Basic Braintree Settings]

![Standaardinstellingen Braintree](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Title] | Winkelweergave | Standaardwaarde: `Credit Card` (Braintree) |
| [!UICONTROL Environment] | Winkelweergave | Opties: `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | Winkelweergave | Bepaalt de actie die door de Braintree wordt ondernomen wanneer een betaling wordt verwerkt. Opties: <br/>**`Authorize`**- Gelden op de creditcard van de klant worden toegestaan, maar niet van de rekening overgedragen. Er wordt een bestelling gemaakt in uw winkelbeheerder. U kunt de uitverkoop later vastleggen en een factuur maken.<br/>**`Intent Sale`** (eerder `Authorize and Capture` in eerdere versies) - Fondsen op de creditcard van de klant worden geautoriseerd en vastgelegd door Braintree, en een bestelling en factuur worden gemaakt in uw winkel Admin. |
| [!UICONTROL Sandbox Merchant ID] | Winkelweergave | Dit is de unieke id voor uw gehele sandboxgatewayaccount. Ook bekend als de _openbare id_ of _productie-id_, is uw bedrijfs-id anders voor uw productie- en sandboxgateways. Dit veld wordt weergegeven als het _[!UICONTROL Environment]_veld is ingesteld op `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | Winkelweergave | Dit is uw gebruiker-specifieke, openbare herkenningsteken dat toegang tot gecodeerde gegevens beperkt. Elke gebruiker die aan uw gateway van de Braintree Sandbox wordt geassocieerd heeft zijn eigen zandbak openbare sleutel. Dit veld wordt weergegeven als het _[!UICONTROL Environment]_veld is ingesteld op `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | Winkelweergave | Dit is uw gebruiker-specifieke, privé herkenningsteken dat toegang tot gecodeerde gegevens beperkt. Elke gebruiker die aan de gateway van de Braintree van Sandbox wordt gekoppeld heeft zijn eigen privé sleutel voor de zandbak. Dit veld wordt weergegeven als het _[!UICONTROL Environment]_veld is ingesteld op `Sandbox`. |
| [!UICONTROL Merchant ID] | Winkelweergave | Dit is het unieke herkenningsteken voor uw volledige gatewayrekening, met inbegrip van de veelvoudige handelaarrekeningen die in uw gateway kunnen zijn. Ook bekend als de _openbare id_ of _productie-id_, is uw bedrijfs-id anders voor uw productie- en sandboxgateways. Dit veld wordt weergegeven als het _[!UICONTROL Environment]_veld is ingesteld op `Production`. |
| [!UICONTROL Public Key] | Winkelweergave | Dit is uw gebruiker-specifieke, openbare herkenningsteken dat toegang tot gecodeerde gegevens beperkt. Elke gebruiker verbonden aan uw gateway van de Braintree heeft hun eigen openbare sleutel. Dit veld wordt weergegeven als het _[!UICONTROL Environment]_veld is ingesteld op `Production`. |
| [!UICONTROL Private Key] | Winkelweergave | Dit is uw gebruiker-specifieke, privé herkenningsteken dat toegang tot gecodeerde gegevens beperkt. Elke gebruiker verbonden aan uw gateway van de Braintree heeft zijn eigen privé sleutel. Dit veld wordt weergegeven als het _[!UICONTROL Environment]_veld is ingesteld op `Production`. |
| [!UICONTROL Enable Card Payments] | Website | Hiermee bepaalt u of de betalingsmethode voor creditcard van de Braintree beschikbaar is voor uw klanten als betalingsmethode. Opties: `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Website | Als deze optie is ingeschakeld, beschikt u over een veilige opslagruimte voor de betalingsgegevens van de klant, zodat klanten hun creditcardgegevens niet telkens opnieuw hoeven in te voeren. Opties: `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Website | Wanneer toegelaten, wordt de bevestiging gedaan voor de regels CVV opstelling in uw Rekening van de Braintree. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Geavanceerde instellingen Braintreeën](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Website | Een beschrijvende titel voor uw referentie die de vault identificeert waar uw klantenkaartinformatie wordt opgeslagen. |
| [!UICONTROL Merchant Account ID] | Website | De Merchant Account ID die aan Braintree transacties van deze website moet worden gekoppeld. Als deze optie niet wordt opgegeven, wordt de standaardzakelijke account van uw Braintree gebruikt. |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Website | Voorkomt dat de transactie ter evaluatie wordt verzonden als onderdeel van [!DNL Advanced Fraud Tools] controles, alleen op bestellingen die via de beheerder worden geplaatst wanneer deze is ingesteld op `Yes`.<br/>Opties: `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Website | `Advanced Fraud Protection` controles worden overgeslagen wanneer de drempelwaarde wordt bereikt of overschreden. Als u dit veld leeg laat, wordt deze optie uitgeschakeld. |
| [!UICONTROL Debug] | Website | Bepaalt als de mededelingen tussen het systeem van de Braintree en uw opslag in een logboekdossier worden geregistreerd. Opties: `Yes` / `No` |
| [!UICONTROL CVV Verification] | Website | Hiermee bepaalt u of klanten de driecijferige beveiligingscode moeten opgeven vanaf de achterzijde van een creditcard. Opties: `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Website | Verzend de winkelwagentjes voor alle betalingsmethoden. Opties: `Yes` / `No` |
| [!UICONTROL Credit Card Types] | Website | Hiermee geeft u elke creditcard op die u accepteert als betaling via Braintree. Pers en greep `Ctrl` (of `Command` op Mac) om een combinatie van kaarten te selecteren. Opties: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Website | Hiermee bepaalt u de volgorde waarin Braintree bij andere betalingsmethoden wordt weergegeven tijdens het afrekenen. |

## [!UICONTROL Braintree Webhooks Settings]

![Instellingen Braintree webhooks](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Website | De webhaakfunctionaliteit voor fraudebescherming, ACH-betalingen en lokale betalingsmethoden mogelijk maken. Opties: `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Website | Voeg deze URL toe aan uw account voor Braintreeën als de [!UICONTROL Webhook Destination URL]. **Deze URL moet veilig en openbaar toegankelijk zijn.** |
| [!UICONTROL Fraud Protection Approve Order Status] | Website | Wanneer de fraudebescherming door Braintree wordt goedgekeurd, wordt de geselecteerde ordestatus toegewezen aan de orde van de Handel. Deze status wordt gebruikt om de status bij te werken van de order waar de ACH - betalingsmethode wordt gebruikt en wanneer deze wordt `SETTLED` in Braintree. |
| [!UICONTROL Fraud Protection Reject Order Status] | Website | Wanneer de fraudebescherming door Braintree wordt verworpen, wordt de geselecteerde ordestatus toegewezen aan de orde van de Handel. Deze status wordt gebruikt om de status bij te werken van de order waar de ACH - betalingsmethode wordt gebruikt en wanneer `SETTLEMENT` is `DECLINED` in Braintree. |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![Landspecifieke instellingen](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Website | Hiermee bepaalt u of u betalingen accepteert die worden verwerkt door Braintree uit alle landen of alleen bepaalde landen. Opties: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Indien van toepassing, identificeert u de specifieke landen waaruit u door Braintree verwerkte betalingen accepteert. |
| [!UICONTROL Country Specific Credit Card Types] | Website | Identificeert de creditcards die per land worden geaccepteerd voor betalingen die door Braintree worden verwerkt. Voor elk land wordt een record opgeslagen. Opties: <br/>**`Country`**- Kies het land.<br/>**`Allowed Card Types`** - Selecteer elke creditcard die in het land wordt geaccepteerd als betaling via Braintree. <br/>**`Add`**- Voeg een regel toe voor creditcards voor een ander land.<br/>**`Action`** - Verwijdert de registratie van toegestane creditcards voor het land. |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH door Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Website | Hiermee wordt bepaald of [!DNL ACH Direct Debit] is opgenomen als betalingsmethode via Braintree. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Hiermee bepaalt u de volgorde [!DNL ACH Direct Debit] wordt bij het afrekenen met andere betalingsmethoden aangeboden. |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple betalen via Braintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Website | Hiermee wordt bepaald of Apple Pay is opgenomen als betalingsmethode via Braintree. Opties: `Yes` / `No` <br/><br/> Het domein moet [eerst geverifieerd in Braintree-account](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Payment Action] | Website | Bepaalt de actie die door de Braintree wordt ondernomen wanneer een betaling wordt verwerkt. Opties: <br/>**`Authorize`**- Gelden op de kaart van de klant zijn toegestaan, maar niet van de rekening van de klant overgedragen. Er wordt een bestelling gemaakt in uw winkelbeheerder. U kunt de uitverkoop later vastleggen en een factuur maken.<br/>**`Intent Sale`** - Middelen op de kaart van de klant worden geautoriseerd en vastgelegd door Braintree, en een bestelling en factuur worden gemaakt in uw winkel Admin. **_Opmerking:_** Dit was `Authorize and Capture` in 2.3.x en eerdere versies. |
| [!UICONTROL Merchant Name] | Winkelweergave | Label dat wordt weergegeven aan klanten in de pop-up van ApplePay. |
| [!UICONTROL Sort Order] | Website | Hiermee bepaalt u de bestelling dat Apple Pay bij andere betalingsmethoden wordt aangeboden tijdens het afrekenen. |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![Lokale betalingsmethoden](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Website | Hiermee wordt bepaald of Lokale betalingsmethode via Braintree wordt opgenomen als betalingsmethode. Opties: `Yes` / `No` |
| [!UICONTROL Title] | Website | Label dat wordt weergegeven in het gedeelte Betalingsmethode voor afrekenen. Standaardwaarde: `Local Payments` |
| [!UICONTROL Allowed Payment Method] | Website | Selecteer de lokale betalingsmethode die moet worden ingeschakeld. Opties: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (nog niet ondersteund) |
| [!UICONTROL Sort Order] | Website | Hiermee bepaalt u de volgorde waarin Lokale betalingsmethode bij andere betalingsmethoden wordt weergegeven tijdens het afrekenen. |

{style="table-layout:auto"}

>[!NOTE]
>
>De extensie van de gebundelde Braintree ondersteunt niet alle lokale betalingsmethoden die in de [Braintree ontwikkelaarsdocumentatie](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Andere lokale betalingsmethoden worden momenteel ontwikkeld en zullen in toekomstige versies worden ondersteund.

## [!UICONTROL GooglePay through Braintree]

![GooglePay via Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Website | Hiermee wordt bepaald of [!DNL Google Pay] Betaling wordt via Braintree als betalingsmethode opgenomen. Opties: `Yes` / `No` |
| [!UICONTROL Payment Action] | Website | Bepaalt de actie die door de Braintree wordt ondernomen wanneer een betaling wordt verwerkt. Opties: <br/>**`Authorize`**- Gelden op de kaart van de klant zijn toegestaan, maar niet van de rekening van de klant overgedragen. Er wordt een bestelling gemaakt in uw winkelbeheerder. U kunt de uitverkoop later vastleggen en een factuur maken.<br/>**`Intent Sale`** - Middelen op de kaart van de klant worden geautoriseerd en vastgelegd door Braintree, en een bestelling en factuur worden gemaakt in uw winkel Admin. **_Opmerking:_** Dit was `Authorize and Capture` in 2.3.x en eerdere versies. |
| [!UICONTROL Button Color] | Website | Bepaalt de kleur van [!DNL Google Pay] knop. Opties: `White` / `Black` |
| [!UICONTROL Merchant ID] | Winkelweergave | ID opgegeven door Google moet hier worden ingevoerd. |
| [!UICONTROL Accepted Cards] | Website | Selecteer het type kaarten dat een klant kan gebruiken om de bestelling te plaatsen met [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | Website | Hiermee bepaalt u de bestelling dat Google Pay bij andere betalingsmethoden wordt aangeboden tijdens het afrekenen. |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo door Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Website | Hiermee wordt bepaald of [!DNL Venmo] is opgenomen als betalingsmethode via Braintree. Opties: `Yes` / `No` |
| [!UICONTROL Payment Action] | Website | Bepaalt de actie die door de Braintree wordt ondernomen wanneer een betaling wordt verwerkt. Opties: <br/>**`Authorize`**- Gelden op de kaart van de klant zijn toegestaan, maar niet van de rekening van de klant overgedragen. Er wordt een bestelling gemaakt in uw winkelbeheerder. U kunt de uitverkoop later vastleggen en een factuur maken.<br/>**`Intent Sale`** - Middelen op de kaart van de klant worden geautoriseerd en vastgelegd door Braintree, en een bestelling en factuur worden gemaakt in uw winkel Admin. **_Opmerking:_** Dit was  _Autoriseren en vastleggen_ in 2.3.x en eerdere versies. |
| [!UICONTROL Sort Order] | Website | Bepaalt de bestelling dat Venmo bij andere betalingsmethoden wordt vermeld tijdens het afrekenen. |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal via Braintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Website | Hiermee wordt bepaald of PayPal via Braintree wordt opgenomen als betalingsmethode. Opties: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Website | Hiermee wordt bepaald of PayPal-creditering via Braintree als betalingsmethode wordt opgenomen. Opties: `Yes` / `No`. Dit veld wordt weergegeven wanneer `Enable PayPal through Braintree` is ingesteld op `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Website | Hiermee wordt bepaald of PayPal PayPal Later via Braintree als betalingsmethode wordt opgenomen. Opties: `Yes` / `No`. Dit veld wordt weergegeven wanneer `Enable PayPal through Braintree` is ingesteld op `Yes` |
| [!UICONTROL Title] | Winkelweergave | Het label dat PayPal identificeert via Braintree aan klanten tijdens het afrekenen. Standaardwaarde: `PayPal` |
| [!UICONTROL Vault Enabled] | Website | Als deze optie is ingeschakeld, beschikt u over een veilige opslagruimte voor de betalingsgegevens van de klant, zodat klanten hun PayPal-gegevens niet telkens opnieuw hoeven in te voeren. Opties: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Een getal dat de volgorde bepaalt waarin PayPal via Braintree bij andere betalingsmethoden wordt weergegeven tijdens het afrekenen. |
| [!UICONTROL Override Merchant Name] | Winkelweergave | Een alternatieve naam die kan worden gebruikt om de handelaar voor elke archiefmening te identificeren. |
| [!UICONTROL Payment Action] | Website | Hiermee bepaalt u de actie die door PayPal via Braintree wordt uitgevoerd wanneer een betaling wordt verwerkt. Opties: <br/>**`Authorize`**- Gelden op de kaart van de klant zijn toegestaan, maar niet van de rekening van de klant overgedragen. Er wordt een bestelling gemaakt in uw winkelbeheerder. U kunt de uitverkoop later vastleggen en een factuur maken.<br/>**`Authorize and Capture`** - Gelden op de kaart van de klant worden geautoriseerd en via Braintree vastgelegd door PayPal, en er wordt een bestelling en factuur gemaakt in uw winkel Admin. |
| [!UICONTROL Payment from Applicable Countries] | Website | Hiermee bepaalt u of je betalingen accepteert die door PayPal worden verwerkt via Braintree uit alle landen of alleen bepaalde landen. Opties: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Indien van toepassing, identificeert u de specifieke landen waaruit u door Braintree verwerkte betalingen accepteert. |
| [!UICONTROL Require Customer's Billing Address] | Website | Hiermee bepaalt u of het factuuradres van de klant vereist is om een bestelling te verzenden. Opties: `Yes` / `No` |
| [!UICONTROL Debug] | Website | Hiermee bepaalt u of de communicatie tussen PayPal via Braintree en uw winkel wordt opgenomen in een logbestand. Opties: `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Website | Hiermee wordt bepaald of de PayPal-knop wordt weergegeven in het dialoogvenster [minikaart](../../stores-purchase/cart-configuration.md#mini-cart) en op de [winkelwagentje](../../stores-purchase/cart.md) pagina. Opties: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Styling]

![PayPal-stijlen](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Location] | Website | Hiermee bepaalt u waar PayPal-knoppen en -berichten worden weergegeven op de winkelserver. Opties: `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

De opties en instellingen in deze sectie variëren afhankelijk van de instelling in het dialoogvenster _[!UICONTROL Location]_veld.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Website | Hiermee stelt u de knop in op een van de volgende drie typen: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

De opties en instellingen in deze sectie variëren afhankelijk van het knoptype dat u in het dialoogvenster _[!UICONTROL PayPal Button Type]_veld.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Website | Hiermee bepaalt u de locatie van de PayPal-knop op de geselecteerde locatie. Opties: `Yes` / `No` |
| [!UICONTROL Button Label] | Website | Bepaalt het label voor de PayPal-knop. Opties: `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | Website | Hiermee bepaalt u de kleur van de PayPal-knop. Opties: `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | Website | Hiermee bepaalt u de vorm van de PayPal-knop. Opties: `Pill` / `Rectangle` |
| [!UICONTROL Size] | Website | Hiermee bepaalt u de grootte van de PayPal-knop. Opties: `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

**[!UICONTROL PayLater Messaging]**

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Website | Hiermee wordt het PayLater-bericht ingeschakeld op de geselecteerde locatie. Opties: `Yes` / `No`. Als deze optie is ingeschakeld, wordt PayLater-berichten weergegeven voor beschikbare aanbiedingen ([beperkingen gelden](https://developer.paypal.com/docs/checkout/pay-later/us/)). |
| [!UICONTROL Message Layout] | Website | Bepaalt de lay-out van het PayLater-bericht. Opties: `Text` / `Flex` |
| [!UICONTROL Logo] | Website | Bepaalt het type logo dat wordt gebruikt voor de PayPal-knop. Opties: `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | Website | Hiermee bepaalt u de logopositie voor de PayPal-knop. Opties: `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | Website | Bepaalt de tekstkleur van de PayPal-knop. Opties: `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

Wanneer deze opties zijn ingesteld, kunt u een voorvertoning van de PayPal-knoppen en PayPal-berichten zien. U kunt de instellingen toepassen of de waarden opnieuw instellen met behulp van de volgende besturingselementen:

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Apply] | Website | Hiermee slaat u de geselecteerde opmaakinstellingen voor knoppen en PayLater-berichten op en past u deze toe op de huidige locatie en het huidige knoptype. |
| [!UICONTROL Apply to All Buttons] | Website | Hiermee slaat u de geselecteerde opmaakinstellingen voor knoppen en PayLater-berichtwaarden op en past u deze toe op alle knoptypen en -locaties. |
| [!UICONTROL Reset to Recommended Defaults] | Website | Retourneert de opmaakinstellingen naar de aanbevolen standaardwaarden voor knoppen en PayLater-berichten en past deze toe op alle knoptypen en -locaties. |

{style="table-layout:auto"}

## 3d Instellingen voor beveiligde verificatie

![Instellingen voor beveiligde 3D-verificatie](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Website | Hiermee wordt bepaald of een transactie een extra verificatieproces moet doorstaan wanneer de klant is ingeschreven voor een programma zoals _Gecontroleerd door VISA_. Opties: `Yes` / `No` |
| [!UICONTROL Always request 3DS] | Website | Uitdaging het 3D Veilige verzoek altijd voor alle transacties. Opties: `Yes` / `No` |
| [!UICONTROL Threshold Amount] | Website | Hiermee bepaalt u het maximale orderbedrag dat is toegestaan voor verwerking op één bestelling. Braintree weigert toestemming als het orderbedrag dit drempelbedrag overschrijdt. |
| [!UICONTROL Verify for Applicable Countries] | Website | Hiermee bepaalt u in welke landen de betaling moet worden geverifieerd. Opties: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Website | Vermeld, indien van toepassing, de specifieke landen waaruit de betaling via Braintree moet worden geverifieerd. |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![Dynamische beschrijvingen](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Name] | Winkelweergave | De naamdescriptor bestaat uit twee delen, die door een sterretje (*) worden gescheiden. Het eerste deel van de descriptor identificeert het bedrijf of de DBA en het tweede deel identificeert het product. Bijvoorbeeld: `company*myproduct`  <br/><br/>De lengte van het bedrijf en de delen van het Product van de beschrijver kunnen op de volgende manieren, voor een gecombineerde lengte van maximaal 22 karakters worden toegewezen: <br/>**`Option 1`**- Bedrijf moet uit drie tekens bestaan / Het product mag uit maximaal 18 tekens bestaan<br/>**`Option 2`** - Bedrijf moet uit zeven tekens bestaan / Het product mag uit maximaal 14 tekens bestaan <br/>**`Option 3`**- Bedrijf moet uit 12 tekens bestaan / Het product mag uit maximaal negen tekens bestaan |
| [!UICONTROL Phone] | Winkelweergave | De telefoonbeschrijving moet tien tot 14 tekens lang zijn en mag alleen cijfers, streepjes, ronde haakjes en punten bevatten. Bijvoorbeeld: `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | Winkelweergave | De URL-descriptor vertegenwoordigt uw domeinnaam en kan maximaal 13 tekens lang zijn. Bijvoorbeeld: `company.com` |

{style="table-layout:auto"}
