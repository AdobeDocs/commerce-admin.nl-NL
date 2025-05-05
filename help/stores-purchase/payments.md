---
title: Overzicht van betalingen
description: Meer informatie over de betalingsmethoden en -services die native worden ondersteund in Adobe Commerce en Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Overzicht van betalingen

Adobe Commerce en Magento Open Source bieden ondersteuning voor verschillende betalingsmethoden en -services die u kunt aanbieden voor een eenvoudigere afhandeling en gebruiksvriendelijkheid voor klanten. Deze lijst bevat verschillende methoden voor offlinebetalingen, waaronder betaling via cheque of postwissel, en onder rembours. Er zijn ook native integratie voor vele online betalingsoplossingen en gateways, waaronder Braintree als een gebundelde door leveranciers ontwikkelde uitbreiding.

>[!TIP]
>
>Betalingsservices voor Adobe Commerce en Magento Open Source bieden een kant-en-klare oplossing voor zelfbediening, inclusief het testen van sandboxen en een eenvoudige configuratie, voor een robuuste en veilige betalingsverwerking. Meer over deze krachtige hulpmiddelreeks leren en hoe het u het inzicht en de controle kan geven u de beste ervaring voor uw kopers moet creëren, zie de [ Gids van de Gebruiker van de Diensten van de Betaling ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=nl-NL).

>[!NOTE]
>
>Herzie de [ PCI nalevingsrichtlijnen ](../getting-started/compliance-pci.md) die de vereisten schetsen die door de Industrie van de Kaart van de Betaling (PCI) voor ondernemingen worden geplaatst die betaling door creditcard over Internet goedkeuren.

## Wijzigingen in 2.4

Sommige integratie van betalingen en gebundelde extensies zijn verwijderd uit 2.4.x-releases en verplaatst naar Commerce Marketplace. U kunt de recentste officiële uitbreidingen van de betaalintegratie in [ Commerce Marketplace ](https://marketplace.magento.com/extensions/payments-security.html) vinden {:target="_blank"}.

- **Amazon betaalt** en **Klarna**: Adobe Commerce en Magento Open Source geven 2.4.0 door 2.4.3 op omvat deze leverancier-ontwikkelde uitbreidingen. Vanaf de release 2.4.4 worden deze extensies niet meer gebundeld met de kernversie en moeten ze vanaf de Commerce Marketplace worden geïnstalleerd en bijgewerkt. De Marketplace biedt ook toegang tot de huidige documentatie die wordt geleverd door de ontwikkelaar van de extensie.

  Als u één van beiden van deze gebundelde toegelaten en gevormde uitbreiding hebt, moet u uw composer.json- dossier als deel van het 2.4.4 verbeteringsproces bijwerken en om extensie updates te beheren die door:gaan. Zie [ modules van de Verbetering ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=nl-NL) in de _Gids van de Verbetering_ voor meer informatie.

- **Worldpay**, **Eway**, **CyberSource**, en **Authorize.Net**: Voor details over het maken van een veilige overgang van deze betaalintegratie, zie [ DevBlog ](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445) {:target="_blank"}.

## Offline betalingsmethoden

Adobe Commerce en Magento Open Source beschikken over verschillende ingebouwde methoden voor offlinebetalingen, waarvoor geen diensten van een betalingsverwerkingsbedrijf van een derde vereist zijn:

- [Afhandeling nul subtotaal](zero-subtotal-checkout.md)
- [Onder rembours](cash-on-delivery.md)
- [Bankoverschrijving](bank-transfer.md)
- [Cheque/postwissel](check-money-order.md)
- [Inkooporder](purchase-order.md)
- [ Betaling op Rekening ](../b2b/enable-basic-features.md#configure-payment-on-account) ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B)

## Onlinebetalingsmethoden

Adobe Commerce en Magento Open Source ondersteunen een groot aantal betalingsoplossingen die handelsdiensten aanbieden in alle delen van de wereld. In tegenstelling tot betalingsoplossingen die controle overdragen naar een andere site om de transactie te voltooien, maakt een betaalgateway het voor u mogelijk om creditcardbetalingen rechtstreeks van uw winkel te accepteren zonder dat de klant uw site verlaat.

### Aanbevolen oplossingen

- [ de Diensten van de Betaling ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=nl-NL)
- [PayPal Express-afhandeling](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Andere PayPal-betalingsoplossingen

Zie [ PayPal betalingsoplossingen ](paypal.md) voor meer informatie over PayPal de opties van de betalingsmethode.

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

- [ Oplossingen van de Bescherming van fraude op Marketplace ][1]

>[!NOTE]
>
>Ter ondersteuning van updates voor de naleving van de beveiligingsvoorschriften wordt de Signifying Fraude Protection uit Commerce verwijderd vanaf de release 2.4.0. Als u de Ondertekende integratie in een 2.3.x of vorige versie hebt gebruikt, wordt het geadviseerd dat u overgang aan de [ Ondertekende uitbreiding van de Bescherming van Fraude &amp; van de Doorbelasting ](https://marketplace.magento.com/signifyd-module-connect.html) {:target="_blank"}. Zorg ervoor dat u updates voor de extensie bijhoudt volgens de richtlijnen van de leverancier.

## Bronnen voor probleemoplossing

Voor hulp bij het oplossen van problemen met betaling, zie de [ Kennisbank van de Steun ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=nl-NL).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
