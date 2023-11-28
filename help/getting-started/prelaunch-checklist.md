---
title: Controlelijst voor starten
description: Gebruik deze lijst om de vereiste configuratiemontages te controleren om ervoor te zorgen dat alles correct is alvorens uw opslag aan productie gaat.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Controlelijst voor starten

Nadat u het ontwerp, de ontwikkeling, en het testen van uw opslag voltooit, controleer de volgende configuratiemontages om ervoor te zorgen dat alles correct vóór de opslag is _gaat live_. Voor een uitvoerige beschrijving van elke configuratie die plaatst, zie [_Configuratieverwijzing_](../configuration-reference/guide-overview.md).

## Algemene instellingen

- [URL&#39;s opslaan](../stores-purchase/store-urls.md) - Controleer of de URL&#39;s van de winkel voor de winkel en de beheerder correct zijn voor een live productieomgeving.
- Beveiligingscertificaat - Installeer een 100% ondertekend en vertrouwd beveiligingscertificaat voor het domein dat is opgegeven in de basis-URL voordat u de winkel start.
- [E-mailadressen van winkel](../getting-started/store-details.md#store-email-addresses) - Vul alle e-mailadressen in die worden gebruikt voor het verzenden en ontvangen van e-mailberichten, zoals nieuwe bestellingen, facturen, verzendingen, creditnota&#39;s, waarschuwingen over de productprijs en nieuwsbrieven. Zorg ervoor dat elk veld een geldig e-mailadres voor het bedrijf bevat.

## Marketinginstellingen

- [E-mailsjablonen](../systems/email-templates.md) - Werk de standaard e-mailsjablonen bij met uw merk. Als u sjablonen maakt, moet u de configuratie bijwerken.
- [Verkoopmededelingen](../stores-purchase/introduction.md#order-management-and-operations) - Zorg ervoor dat uw facturen en verpakkingsslips de juiste bedrijfsgegevens bevatten en uw merk weerspiegelen.
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] biedt integratie met Google API zodat uw bedrijf Googles Analytics en Google AdWords kan gebruiken.

## Verkoopinstellingen

- [Opties voor winkelwagentje](../stores-purchase/cart-configuration.md) - Bekijk de instellingen voor de configuratie van de winkelwagentje om te zien of er iets is dat u wilt wijzigen, zoals het bepalen van het minimale orderbedrag en de levensduur van de prijzen in de winkelwagentje.
- [Afhandelingsopties](../stores-purchase/checkout-process.md#checkout-options) - Bekijk de afrekenopties om te zien of er iets is dat u wilt wijzigen, zoals het instellen van voorwaarden en voorwaarden, en het configureren van uitchecken door gasten.
- [Belastingen](../stores-purchase/taxes.md) - Zorg ervoor dat belastingen correct zijn geconfigureerd volgens de belastingregels van uw bedrijf en de lokale vereisten.
- [Leveringsmethoden](../stores-purchase/delivery.md) - Alle vervoerders en leveringsmethoden door de onderneming laten gebruiken.
- [PayPal](../stores-purchase/paypal.md) - Als u uw klanten het gemak wilt bieden om met PayPal te betalen, opent u een PayPal Merchant-account en stelt u een betalingsmethode in. Voer een aantal testtransacties uit in de Sandbox-modus voordat de winkel actief wordt.
- [Betalingsmethoden](../stores-purchase/payments.md) - Schakel de betaalmethoden die u wilt gebruiken in en zorg ervoor dat deze correct zijn geconfigureerd. Controleer de instellingen voor de status van de bestelling, de geaccepteerde valuta, de landen die dit toestaan, enzovoort.

## Systeeminstellingen

[Uitsnijden (geplande taken)](../systems/cron.md) - Cron-taken worden gebruikt voor het verwerken van e-mail, catalogusprijsregels, nieuwsbrieven, klantenwaarschuwingen, Google-sitemaps, het bijwerken van valutakoersen, enzovoort. Zorg ervoor dat de banen van het Gewas aan looppas bij het aangewezen tijdinterval, in notulen worden geplaatst.
