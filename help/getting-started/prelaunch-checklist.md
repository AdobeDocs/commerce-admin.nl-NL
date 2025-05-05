---
title: Controlelijst voor starten
description: Gebruik deze lijst om de vereiste configuratiemontages te controleren om ervoor te zorgen dat alles correct is alvorens uw opslag aan productie gaat.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Controlelijst voor starten

Nadat u het ontwerp, de ontwikkeling, en het testen van uw opslag voltooit, controleer de volgende configuratiemontages om ervoor te zorgen dat alles correct is alvorens de opslag _levend_ gaat. Voor een uitvoerige beschrijving van elke configuratie die plaatsen, zie de [_Verwijzing van de Configuratie_](../configuration-reference/guide-overview.md).

## Algemene instellingen

- [ opslag URLs ](../stores-purchase/store-urls.md) - verifieer dat opslag URLs voor de opslag en Admin voor een levende productiemilieu correct zijn.
- Beveiligingscertificaat - Installeer een 100% ondertekend en vertrouwd beveiligingscertificaat voor het domein dat is opgegeven in de basis-URL voordat u de winkel start.
- [ E-mailadressen van de Opslag ](../getting-started/store-details.md#store-email-addresses) - voltooi alle e-mailadressen die worden gebruikt om e-mailberichten, zoals nieuwe orden, facturen, verzendingen, creditnota&#39;s, productprijsalarm, en nieuwsbrieven te verzenden en te ontvangen. Zorg ervoor dat elk veld een geldig e-mailadres voor het bedrijf bevat.

## Marketinginstellingen

- [ E-mailMalplaatjes ](../systems/email-templates.md) - werk de standaard e-mailmalplaatjes bij om op uw merk te wijzen. Als u sjablonen maakt, moet u de configuratie bijwerken.
- [ Mededelingen van de Verkoop ](../stores-purchase/introduction.md#order-management-and-operations) - zorg ervoor dat uw facturen en verpakkingsslips de correcte bedrijfsinformatie omvatten en op uw merk wijzen.
- [ de Hulpmiddelen van Google ](../merchandising-promotions/google-tools.md) - [!DNL Commerce] verstrekt integratie met Google API om uw zaken toe te staan om Googles Analytics en Google AdWords te gebruiken.

## Verkoopinstellingen

- {de Opties van het Kart van 0} [&#128279;](../stores-purchase/cart-configuration.md) - bekijk de montages van de wortelconfiguratie, om te zien of is er om het even wat dat u, zoals het plaatsen van het minimumordebedrag en het leven van de prijzen in de kar wilt veranderen.
- [ Opties van de Controle ](../stores-purchase/checkout-process.md#checkout-options) - bekijk de controleopties, om te zien of is er om het even wat dat u, zoals opstellings termijnen en voorwaarden, en het vormen gastcontrole wilt veranderen.
- [ Belastingen ](../stores-purchase/taxes.md) - zorg ervoor dat de belastingen behoorlijk volgens uw regels van de bedrijfsbelasting en lokale vereisten worden gevormd.
- [ Methoden van de Levering ](../stores-purchase/delivery.md) - laat alle dragers en leveringsmethodes toe die door het bedrijf moeten worden gebruikt.
- [ PayPal ](../stores-purchase/paypal.md) - als u van plan bent om uw klanten het gemak aan te bieden om met PayPal te betalen, open een Merchant Rekening van PayPal, en opstelling een betalingsmethode. Voer een aantal testtransacties uit in de Sandbox-modus voordat de winkel actief wordt.
- [ de Methoden van de Betaling ](../stores-purchase/payments.md) - laat de betalingsmethodes toe die u van plan bent te gebruiken, en zorg ervoor dat zij behoorlijk worden gevormd. Controleer de instellingen voor de status van de bestelling, de geaccepteerde valuta, de landen die dit toestaan, enzovoort.

## Systeeminstellingen

[ Uitsnede (Geplande Taken) ](../systems/cron.md) - de banen van de Kroon worden gebruikt om e-mail, de regels van de catalogusprijs, bulletins, klantenalarm, Google sitemaps, updatematrijzen, etc. te verwerken. Zorg ervoor dat de banen van het Gewas aan looppas bij het aangewezen tijdinterval, in notulen worden geplaatst.
