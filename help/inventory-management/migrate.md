---
title: '[!DNL Commerce] upgrades'
description: Leer hoe de verbeteringen van Adobe Commerce en van Magento Open Source catalogus en  [!DNL Inventory Management]  configuraties beïnvloeden.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] upgrades

Als u in een vorige versie een inventarisatie van één bron hebt gebruikt, bevat deze informatie informatie over nieuwe functies en wijzigingen in uw bestaande catalogus en inventarisconfiguraties.

[!DNL Inventory Management] voor Adobe Commerce en Magento Open Source bevat functies, verbeteringen en ondersteuning voor ontwikkelaars die al het productvoorraadbeheer verbeteren en bijwerken en nieuwe functies toevoegen. Alle functies zijn offline beschikbaar, inclusief het Source-selectiegereedschap en de gelijktijdige afhandeling, zodat de orderhoeveelheden overeenkomen met de bronnen en de afhandeling van bestellingen. Afhankelijk van uw websites, winkels en winkeltype kunt u extra voorraad en bronnen maken, inventarisbedragen toewijzen en nog veel meer. Voor volledige informatie, zie [&#x200B; Inventory management &#x200B;](introduction.md).

Wanneer u Magento Open Source 2.4.x of Adobe Commerce 2.4.x installeert, vinden de volgende eerste wijzigingen plaats:

- [&#x200B; Inventory management &#x200B;](enable.md) laat op het globale opslag of productniveau toe. Met de optie Stock beheren kunt u inventarishoeveelheden, berekeningen van de geaggregeerde verkoophoeveelheden en boekingsbeheer bijhouden of het bijhouden van aankopen tot aan de factuur en de verzending uitschakelen. U kunt deze optie uitschakelen om een ERP en andere services van derden te gebruiken voor het beheer van voorraden, orders en verzendingen. Zie [!DNL Inventory Management] Modules hieronder voor meer informatie.

- A [&#x200B; StandaardSource &#x200B;](sources-manage.md) en [&#x200B; StandaardVoorraad &#x200B;](stocks-manage.md) voegt aan het systeem toe. Schakel deze standaardinstellingen niet uit of verwijder deze niet. [!DNL Commerce] wijst bestaande en nieuw geïmporteerde producten toe aan deze standaardinstellingen.

  >[!IMPORTANT]
  >
  >Het gebruik van de standaardvoorraad en de standaard-Source wordt sterk afgeraden omdat deze deel uitmaken van de module `CatalogInventory` , die nu is vervangen. Het wordt aanbevolen aangepaste voorraden en bronnen te maken en te gebruiken.

   - De voorraden leveren een geaggregeerde, virtuele, verkoopbare hoeveelheid met reserveringen voor het volgen van winkelwagentjes en bestellingen, waardoor een gelijktijdige afhandeling wordt gegarandeerd.

   - Alle bestaande producten in uw catalogus worden toegewezen aan de standaard-Source. Totdat u nieuwe bronnen toevoegt, verandert de productinterface niet. Als u alleen producten verzendt van één locatie, zijn er geen andere verschillen voor bronnen. U kunt douane[&#x200B; bronnen &#x200B;](sources-add.md) tot stand brengen en [&#x200B; hoeveelheden &#x200B;](quantities-manage.md) per ladingsplaats toewijzen.

   - U kunt een bron vormen als Plaats van de Bestelwagen en [&#x200B; toewijzen hoeveelheden &#x200B;](quantities-manage.md) voor die bron.

   - Uw website wijst de standaardvoorraad toe. U kunt douane [&#x200B; aandelen &#x200B;](stocks-add.md) tot stand brengen om verkoopkanalen (websites) en bronnen (plaatsen) te verbinden.

- De extra [&#x200B; configuratieopties &#x200B;](configuration.md) voegen aan uw producten en globale opslag toe. Sommige bestaande configuratieopties ontvangen bijgewerkte opties en gedragingen:

   - Vermeld voor onderstaande hoeveelheid de meldingen en breng de bedragen in mindering op de verkoopbare hoeveelheid.

   - De Drempel van de bezetting steunt positieve bedragen, nul, en negatieve bedragen. Als Achterorden ingeschakeld, worden positieve bedragen genegeerd, als nul (of oneindig) beschouwd.

   - Achterorden steunen nul (oneindig) en negatieve bedragen. Als deze optie is ingeschakeld, wordt de onderstaande hoeveelheid aangeven en niet afgetrokken van de verkoopbare hoeveelheid.

- Met nieuwe reserveringen wordt de potentiële verkoop bijgehouden, waarbij wordt overgeschakeld op kwantitatieve aftrekposten wanneer de bestelling wordt verzonden. U hebt nooit rechtstreeks toegang tot reserveringen of maakt deze. [!DNL Commerce] maakt en beheert reserveringen achter de schermen via bestellingen, verzendingen en creditnota&#39;s.

- [&#x200B; de orden en de verzendingen &#x200B;](shipments.md) omvatten nieuwe eigenschappen om verzendingen aan te bevelen gebruikend het Algoritme van de Selectie van Source en gedeeltelijke overbrengingen van veelvoudige bronnen te steunen om een orde te vervullen.

- De nieuwe [&#x200B; invoer/de uitvoereigenschappen &#x200B;](inventory-import-export.md) staan u toe om bronnen toe te voegen, inventarishoeveelheden bij te werken, en voorraadstatus (in/uit voorraad) voor alle SKUs in uw catalogus te plaatsen. Met deze functies kunt u één, geselecteerde of alle bronnen wijzigen.

- De nieuwe bulkopties door de pagina van de het rooster van het Product steunen bulkgoederen [&#x200B; toewijzend en ontkennend bronnen &#x200B;](bulk-assignment.md), en [&#x200B; overbrengend inventaris aan bron &#x200B;](inventory-transfer.md).

- [!DNL Inventory Management] ondersteunt B2B-catalogi. Momenteel moeten alle B2B-producten worden toegewezen aan de standaard-Source en de standaardvoorraad.

## [!DNL Commerce Order Management] en [!DNL Inventory Management]

[&#x200B; Commerce Order Management (MCOM) &#x200B;](https://commerce-docs.github.io/oms-documentation-archive/) is niet compatibel met [!DNL Inventory Management]. Als MCOM-modules zijn geïnstalleerd, bieden ze alle functies voor voorraadbeheer aan [!DNL Commerce], waaronder beheer van één en meerdere bronnen, voorraden, reserveringen en nog veel meer. De modules [!DNL Inventory Management] zijn standaard uitgeschakeld.

MCOM biedt uitgebreide functies en services voor geavanceerd omnichannel-orderbeheer, wereldwijde inventarisatie en multisourcing, opslag naar opslagbestelling en gecentraliseerde klantenservice. Voor een volledige lijst van eigenschappen, zie de [&#x200B; lijst van de Eigenschap MCOM &#x200B;](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/).

[!DNL Inventory Management] breidt bestaande [!DNL Commerce] -functies uit met extra opties voor het bijhouden van bestellingen tijdens het proces, on-hand inventarisatie, beschikbare voorraad en API&#39;s voor de ontwikkeling van extensies.

## [!DNL Inventory Management] modules

U kunt [!DNL Inventory Management] modules uitschakelen in:

- Versnellen van de upgrade van de huidige handelaars op Adobe Commerce of Magento Open Source 2.0/2.1/2.2/2.3 en migreren naar 2.4.x.

- Gebruik aangepaste inventarisatie- en bestelbeheermodules of modules van andere leveranciers.

- Gebruik [!DNL Order Management System] voor voorraadbeheer. De huidige connector biedt geen ondersteuning voor [!DNL Inventory Management] -interfaces. Voor OMS-handelaren die een upgrade uitvoeren naar Adobe Commerce 2.4.0, moeten ze deze modules uitschakelen.

Voor volledige details, zie [&#x200B; installeren en bijwerken &#x200B;](install-update.md).
