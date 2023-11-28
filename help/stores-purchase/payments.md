---
title: Overzicht van betalingen
description: Meer informatie over de betalingsmethoden en -services die native worden ondersteund in Adobe Commerce en Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# Overzicht van betalingen

Adobe Commerce en Magento Open Source bieden ondersteuning voor verschillende betalingsmethoden en -services die u kunt aanbieden voor een eenvoudigere afhandeling en gebruiksvriendelijkheid voor klanten. Deze lijst bevat verschillende methoden voor offlinebetalingen, waaronder betaling via cheque of postwissel, en onder rembours. Er zijn ook native integratie voor talrijke online betalingsoplossingen en gateways, met inbegrip van Braintree als gebundelde leverancier-ontwikkelde uitbreiding.

>[!TIP]
>
>Betalingsservices voor Adobe Commerce en Magento Open Source bieden een kant-en-klare oplossing voor zelfbediening, inclusief het testen van sandboxen en een eenvoudige configuratie, voor een robuuste en veilige betalingsverwerking. Als u meer wilt weten over deze krachtige gereedschapsset en over de manier waarop u het inzicht en de controle krijgt dat u nodig hebt om de beste ervaring voor kopers te creëren, raadpleegt u de [Gebruikershandleiding voor betalingsservices](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>Controleer de [Richtlijnen voor naleving van PCI](../getting-started/compliance-pci.md) die een overzicht geven van de vereisten die door de betaalkaartindustrie (PCI) zijn vastgesteld voor bedrijven die betalingen via een creditcard via internet accepteren.

## Wijzigingen in 2.4

Sommige integratie van betalingen en gebundelde extensies zijn verwijderd uit 2.4.x-releases en verplaatst naar de Commerce Marketplace. U kunt de nieuwste extensies voor officiële integratie voor betalingen vinden in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.

- **Amazon Pay** en **Klarna**: Adobe Commerce en Magento Open Source versie 2.4.0 tot en met 2.4.3 bevatten deze door leveranciers ontwikkelde extensies. Vanaf de release 2.4.4 worden deze extensies niet meer gebundeld met de kernrelease en moeten ze vanaf de Commerce Marketplace worden geïnstalleerd en bijgewerkt. De Marketplace biedt ook toegang tot de huidige documentatie die wordt geleverd door de ontwikkelaar van de extensie.

  Als u één van beiden van deze gebundelde toegelaten en gevormde uitbreiding hebt, moet u uw composer.json- dossier als deel van het 2.4.4 verbeteringsproces bijwerken en om extensie updates te beheren die door:gaan. Zie [Upgrademodules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) in de _Upgradehandleiding_ voor meer informatie .

- **Worldpay**, **Eway**, **CyberSource**, en **Authorize.Net**: Zie voor meer informatie over het maken van een veilige overgang van deze integratie van betalingen de [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## Offline betalingsmethoden

Adobe Commerce en Magento Open Source omvatten verschillende ingebouwde methoden voor offlinebetalingen, waarvoor geen diensten van een betalingsverwerkingsbedrijf van een derde vereist zijn:

- [Afhandeling nul subtotaal](zero-subtotal-checkout.md)
- [Onder rembours](cash-on-delivery.md)
- [Bankoverschrijving](bank-transfer.md)
- [Cheque/postwissel](check-money-order.md)
- [Inkooporder](purchase-order.md)
- [Betaling op rekening](../b2b/enable-basic-features.md#configure-payment-on-account) ![B2B voor Adobe Commerce](../assets/b2b.svg) (Beschikbaar bij B2B voor Adobe Commerce)

## Onlinebetalingsmethoden

Adobe Commerce en Magento Open Source ondersteunen tal van betalingsoplossingen die handelsdiensten aanbieden in alle delen van de wereld. In tegenstelling tot betalingsoplossingen die controle overdragen naar een andere site om de transactie te voltooien, maakt een betaalgateway het voor u mogelijk om creditcardbetalingen rechtstreeks van uw winkel te accepteren zonder dat de klant uw site verlaat.

### Aanbevolen oplossingen

- [Betalingsdiensten](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [PayPal Express-afhandeling](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Andere PayPal-betalingsoplossingen

Zie [PayPal-betalingsoplossingen](paypal.md) voor meer informatie over opties voor PayPal-betalingsmethoden.

#### Alles-in-één PayPal-oplossingen

- [PayPal-betalingen geavanceerd](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### PayPal-betalingsgateways

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow Link](paypal-payflow-link.md)

## Fraudebescherming

Met de services en filters voor fraudebescherming worden verzonden bestellingen gecontroleerd voordat de transactie wordt verwerkt om frauduleuze bestellingen op te sporen en u te beschermen tegen de kosten van terugbetalingen. Adobe Commerce en Magento Open Source ondersteunen de volgende oplossingen voor fraudebescherming:

- [Paypal-filter Fraudebeheer](paypal.md#paypal-fraud-management-filters)

- [Oplossingen voor fraudebescherming op de markt][1]

>[!NOTE]
>
>Ter ondersteuning van updates voor de naleving van de beveiligingsregels wordt de Signifyd-bescherming voor fraude verwijderd uit de handel vanaf de release 2.4.0. Als u de integratie Ondertekenen hebt gebruikt in een versie van 2.3.x of lager, is het raadzaam over te schakelen naar de [Bezig met ondertekenen van de extensie Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target=&quot;_blank&quot;}. Zorg ervoor dat u updates voor de extensie bijhoudt volgens de richtlijnen van de leverancier.

## Bronnen voor probleemoplossing

Voor hulp bij het oplossen van betalingsproblemen raadpleegt u de [knowledgebase ondersteuning](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
