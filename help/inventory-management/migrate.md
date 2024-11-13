---
title: '[!DNL Commerce] upgrades'
description: Leer hoe de verbeteringen van Adobe Commerce en van de Magento Open Source catalogus en  [!DNL Inventory Management]  configuraties beïnvloeden.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 392d8550741fe6fca3ea1301575c9ebb5e2483bd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] upgrades

Als u in een vorige versie een inventarisatie van één bron hebt gebruikt, bevat deze informatie informatie over nieuwe functies en wijzigingen in uw bestaande catalogus en inventarisconfiguraties.

[!DNL Inventory Management] voor Adobe Commerce en Magento Open Source bevat functies, verbeteringen en ondersteuning voor ontwikkelaars die al het productvoorraadbeheer verbeteren en bijwerken en nieuwe functies toevoegen. Alle functies zijn offline beschikbaar, inclusief het Source-selectiegereedschap en de gelijktijdige afhandeling, zodat de orderhoeveelheden overeenkomen met de bronnen en de afhandeling van bestellingen. Afhankelijk van uw websites, winkels en winkeltype kunt u extra voorraad en bronnen maken, inventarisbedragen toewijzen en nog veel meer. Voor volledige informatie, zie [ Inventory management ](introduction.md).

Wanneer u Magento Open Source 2.4.x of Adobe Commerce 2.4.x installeert, komen de volgende aanvankelijke veranderingen voor:

- [ Inventory management ](enable.md) laat op het globale opslag of productniveau toe. Met de optie Stock beheren kunt u inventarishoeveelheden, berekeningen van de geaggregeerde verkoophoeveelheden en boekingsbeheer bijhouden of het bijhouden van aankopen tot aan de factuur en de verzending uitschakelen. U kunt deze optie uitschakelen om een ERP en andere services van derden te gebruiken voor het beheer van voorraden, orders en verzendingen. Zie [!DNL Inventory Management] Modules hieronder voor meer informatie.

- A [ StandaardSource ](sources-manage.md) en [ StandaardVoorraad ](stocks-manage.md) voegt aan het systeem toe. Schakel deze standaardinstellingen niet uit of verwijder deze niet. [!DNL Commerce] wijst bestaande en nieuw geïmporteerde producten toe aan deze standaardinstellingen.

  >[!IMPORTANT]
  >
  >Het gebruik van de standaardvoorraad en de standaard-Source wordt sterk afgeraden omdat deze deel uitmaken van de module `CatalogInventory` , die nu is vervangen. Het wordt aanbevolen aangepaste voorraden en bronnen te maken en te gebruiken.

   - De voorraden leveren een geaggregeerde, virtuele, verkoopbare hoeveelheid met reserveringen voor het volgen van winkelwagentjes en bestellingen, waardoor een gelijktijdige afhandeling wordt gegarandeerd.

   - Alle bestaande producten in uw catalogus worden toegewezen aan de standaard-Source. Totdat u nieuwe bronnen toevoegt, verandert de productinterface niet. Als u alleen producten verzendt van één locatie, zijn er geen andere verschillen voor bronnen. U kunt douane[ bronnen ](sources-add.md) tot stand brengen en [ hoeveelheden ](quantities-manage.md) per ladingsplaats toewijzen.

   - U kunt een bron vormen als Plaats van de Bestelwagen en [ toewijzen hoeveelheden ](quantities-manage.md) voor die bron.

   - Uw website wijst de standaardvoorraad toe. U kunt douane [ aandelen ](stocks-add.md) tot stand brengen om verkoopkanalen (websites) en bronnen (plaatsen) te verbinden.

- De extra [ configuratieopties ](configuration.md) voegen aan uw producten en globale opslag toe. Sommige bestaande configuratieopties ontvangen bijgewerkte opties en gedragingen:

   - Vermeld voor onderstaande hoeveelheid de meldingen en breng de bedragen in mindering op de verkoopbare hoeveelheid.

   - De Drempel van de bezetting steunt positieve bedragen, nul, en negatieve bedragen. Als Achterorden ingeschakeld, worden positieve bedragen genegeerd, als nul (of oneindig) beschouwd.

   - Achterorden steunen nul (oneindig) en negatieve bedragen. Als deze optie is ingeschakeld, wordt de onderstaande hoeveelheid aangeven en niet afgetrokken van de verkoopbare hoeveelheid.

- Met nieuwe reserveringen wordt de potentiële verkoop bijgehouden, waarbij wordt overgeschakeld op kwantitatieve aftrekposten wanneer de bestelling wordt verzonden. U hebt nooit rechtstreeks toegang tot reserveringen of maakt deze. [!DNL Commerce] maakt en beheert reserveringen achter de schermen via bestellingen, verzendingen en creditnota&#39;s.

- [ de orden en de verzendingen ](shipments.md) omvatten nieuwe eigenschappen om verzendingen aan te bevelen gebruikend het Algoritme van de Selectie van Source en gedeeltelijke overbrengingen van veelvoudige bronnen te steunen om een orde te vervullen.

- De nieuwe [ invoer/de uitvoereigenschappen ](inventory-import-export.md) staan u toe om bronnen toe te voegen, inventarishoeveelheden bij te werken, en voorraadstatus (in/uit voorraad) voor alle SKUs in uw catalogus te plaatsen. Met deze functies kunt u één, geselecteerde of alle bronnen wijzigen.

- De nieuwe bulkopties door de pagina van de het rooster van het Product steunen bulkgoederen [ toewijzend en ontkennend bronnen ](bulk-assignment.md), en [ overbrengend inventaris aan bron ](inventory-transfer.md).

- [!DNL Inventory Management] ondersteunt B2B-catalogi. Momenteel moeten alle B2B-producten worden toegewezen aan de standaard-Source en de standaardvoorraad.

## [!DNL Commerce Order Management] en [!DNL Inventory Management]

[ Commerce Order Management (MCOM) ][1] is niet compatibel met [!DNL Inventory Management]. Als MCOM-modules zijn geïnstalleerd, bieden ze alle functies voor voorraadbeheer aan [!DNL Commerce], waaronder beheer van één en meerdere bronnen, voorraden, reserveringen en nog veel meer. De modules [!DNL Inventory Management] zijn standaard uitgeschakeld.

MCOM biedt uitgebreide functies en services voor geavanceerd omnichannel-orderbeheer, wereldwijde inventarisatie en multisourcing, opslag naar opslagbestelling en gecentraliseerde klantenservice. Voor een volledige lijst van eigenschappen, zie de [ lijst van de Eigenschap MCOM ][2].

[!DNL Inventory Management] breidt bestaande [!DNL Commerce] -functies uit met extra opties voor het bijhouden van bestellingen tijdens het proces, on-hand inventarisatie, beschikbare voorraad en API&#39;s voor de ontwikkeling van extensies.

## [!DNL Inventory Management] modules

U kunt [!DNL Inventory Management] modules uitschakelen in:

- Versnellen van de upgrade van de huidige handelaars op Adobe Commerce of Magento Open Source 2.0/2.1/2.2/2.3 en migreren naar 2.4.x.

- Gebruik aangepaste inventarisatie- en bestelbeheermodules of modules van andere leveranciers.

- Gebruik [!DNL Order Management System] voor voorraadbeheer. De huidige connector biedt geen ondersteuning voor [!DNL Inventory Management] -interfaces. Voor OMS-handelaren die een upgrade uitvoeren naar Adobe Commerce 2.4.0, moeten ze deze modules uitschakelen.

Voor volledige details, zie [ installeren en bijwerken ](install-update.md).

[1]: https://commerce-docs.github.io/oms-documentation-archive/
[2]: https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/
