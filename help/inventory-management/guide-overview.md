---
title: '''Inventory management Guide [!DNL Inventory Management] Hulplijn'
description: Uitgebreide informatie over [!DNL Inventory Management] voor Adobe Commerce en Magento Open Source beheerders, inclusief migratie en configuratie.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!DNL Inventory Management] Overzicht van hulplijnen

Deze handleiding is bedoeld voor beheerders van Adobe Commerce en Magento Open Source. Het verstrekt gedetailleerde informatie over het toelaten van deze module, met inbegrip van configuratie en beheer van zijn eigenschappen. Het veronderstelt een basisbegrip van de kern [!DNL Commerce] configuratie en functionaliteit.

[!DNL Inventory Management] heeft twee gebieden voor beheerders:

- Admin: Gebruik dit gebied om tot de configuratie UI en het melden toegang te hebben.
- De opdrachtregelinterface: gebruik dit gereedschap om installatie- en achtergrondconfiguratietaken uit te voeren.

Deze handleiding is van toepassing op:

| Onderwerp | Beschrijving |
| ------- | ----------- |
| [Inleiding](introduction.md) | Overzicht van de [!DNL Inventory Management] functies die u kunt gebruiken voor het beheer van voorraden op meerdere locaties, zodat de winkel van Koophandel de fysieke voorraad nauwkeurig weergeeft. |
| [Opmerkingen bij de release](release-notes.md) | Lees de opmerkingen bij de release voor meer informatie over alle [!DNL Inventory Management] lozingen. |
| Grondbeginselen van de inventarisatie | Leer de basisbeginselen van voorraadbeheer: [Voorraden en bronnen](sources-stocks.md), [bronselectie en voorbehouden](selection-reservations.md), [bestelling en reserveringsstatus](order-status.md), en [productsoorten](product-types.md) |
| Aan de slag | Meer informatie over de [!DNL Inventory Management] en hoe het in uw instantie van de Handel past en verrichtingen opslaat: [Verbeteringen in de handel](migrate.md), [module installeren en bijwerken](install-update.md), [soorten van commerciële aanschaf](merchant-sourcing.md), en [wijzigingen in bronstructuur](expand-restructure.md) |
| [Configuratie](configuration.md) | Meer informatie over de configuratie van [!DNL Inventory Management] opties die bronbeschikbaarheid, opslagproducten, en ordeverzending bepalen. |
| [Bronnen beheren](sources-manage.md) | Leer bronnen en hoe ze de fysieke locaties definiëren waar de productvoorraad wordt beheerd en verzonden voor bestelling, of waar services beschikbaar zijn. |
| [Bestanden beheren](stocks-manage.md) | Leer hoe voorraad wordt gebruikt om een virtuele, geaggregeerde inventaris van producten voor bronnen van uw verkoopkanalen te vertegenwoordigen. |
| [Hoeveelheden beheren](quantities-manage.md) | Leer hoe u bronnen en hoeveelheden kunt toewijzen voor nieuwe producten of bestaande producten kunt wijzigen. |
| [Bestellingen en verzendingen beheren](shipments.md) | Meer informatie over de extra [!DNL Inventory Management] kenmerken en opties voor het beheer van de inventarishoeveelheden via het verzendingsproces. |
| [CLI-verwijzing](cli.md) | Meer informatie over de opdrachten van de [!DNL Inventory Management] -module voor het beheren van inventarisgegevens en configuratie-instellingen. |

{style="table-layout:auto"}

## Informatie over ontwikkelaars

Zie [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in de ontwikkelaarsdocumentatie voor details over modulearchitectuur, APIs, en algoritmeaanpassing.

## Handelsdocumentatie

{{docs-links}}

## Problemen oplossen en ondersteuning

Gebruik de volgende bronnen als u informatie nodig hebt of vragen hebt die niet in deze handleiding worden behandeld:

- [Inconsistenties met betrekking tot grote nummerreserveringen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Inconsistenties in de inventaris](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Stalen zonder doorhalingsvoorraad bereiken &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Stock status onjuist na de inventarisinstallatie](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Ondersteuningstickets](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)—Verstuur een ticket om extra hulp te ontvangen.
