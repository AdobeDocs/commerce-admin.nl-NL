---
title: '[!DNL Commerce] upgrades'
description: Leer hoe upgrades van Adobe Commerce en Magento Open Source gevolgen hebben voor catalogus en [!DNL Inventory Management] configuraties.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] upgrades

Als u in een vorige versie een inventarisatie van één bron hebt gebruikt, bevat deze informatie informatie over nieuwe functies en wijzigingen in uw bestaande catalogus en inventarisconfiguraties.

[!DNL Inventory Management] voor Adobe Commerce en Magento Open Source bevat functies, verbeteringen en ondersteuning voor ontwikkelaars die al het productvoorraadbeheer verbeteren en bijwerken en nieuwe functies toevoegen. Alle functies zijn offline beschikbaar, inclusief het algoritme voor bronselectie en de gelijktijdige afhandeling om orderhoeveelheden af te stemmen op bronnen en bestellingen. Afhankelijk van uw websites, winkels en winkeltype kunt u extra voorraad en bronnen maken, inventarisbedragen toewijzen en nog veel meer. Voor volledige informatie, zie [Inventory management](introduction.md).

Wanneer u Magento Open Source 2.4.x of Adobe Commerce 2.4.x installeert, komen de volgende aanvankelijke veranderingen voor:

- [Inventory management](enable.md) wordt ingeschakeld op het wereldwijde winkel- of productniveau. Met de optie Stock beheren kunt u inventarishoeveelheden, berekeningen van de geaggregeerde verkoophoeveelheden en boekingsbeheer bijhouden of het bijhouden van aankopen tot aan de factuur en de verzending uitschakelen. U kunt deze optie uitschakelen om een ERP en andere services van derden te gebruiken voor het beheer van voorraden, orders en verzendingen. Zie voor meer informatie [!DNL Inventory Management] Modules hieronder.

- A [Standaardbron](sources-manage.md) en [Standaardvoorraad](stocks-manage.md) toevoegen aan het systeem. Schakel deze standaardinstellingen niet uit of verwijder deze niet. [!DNL Commerce] Wijst bestaande en onlangs ingevoerde producten aan deze gebreken toe.

  >[!IMPORTANT]
  >
  >Het gebruik van de standaardvoorraad en de standaardbron wordt sterk afgeraden, omdat deze deel uitmaken van de `CatalogInventory` , die nu afgekeurd is. Het wordt aanbevolen aangepaste voorraden en bronnen te maken en te gebruiken.

   - De voorraden leveren een geaggregeerde, virtuele, verkoopbare hoeveelheid met reserveringen voor het volgen van winkelwagentjes en bestellingen, waardoor een gelijktijdige afhandeling wordt gegarandeerd.

   - Alle bestaande producten in uw catalogus wijzen aan de Standaardbron toe. Totdat u nieuwe bronnen toevoegt, verandert de productinterface niet. Als u alleen producten verzendt van één locatie, zijn er geen andere verschillen voor bronnen. U kunt aangepaste [bronnen](sources-add.md) en [hoeveelheden toewijzen](quantities-manage.md) per verzendlocatie.

   - U kunt een bron vormen als Pickup Plaats en [hoeveelheden toewijzen](quantities-manage.md) voor die bron.

   - Uw website wijst de standaardvoorraad toe. U kunt aangepaste [voorraden](stocks-add.md) om verkoopkanalen (websites) en bronnen (plaatsen) aan te sluiten.

- Extra [configuratieopties](configuration.md) toevoegen aan uw producten en wereldwijde winkel. Sommige bestaande configuratieopties ontvangen bijgewerkte opties en gedragingen:

   - Vermeld voor onderstaande hoeveelheid de meldingen en breng de bedragen in mindering op de verkoopbare hoeveelheid.

   - De Drempel van de bezetting steunt positieve bedragen, nul, en negatieve bedragen. Als Achterorden ingeschakeld, worden positieve bedragen genegeerd, als nul (of oneindig) beschouwd.

   - Achterorden steunen nul (oneindig) en negatieve bedragen. Als deze optie is ingeschakeld, wordt de onderstaande hoeveelheid aangeven en niet afgetrokken van de verkoopbare hoeveelheid.

- Met nieuwe reserveringen wordt de potentiële verkoop bijgehouden, waarbij wordt overgeschakeld op kwantitatieve aftrekposten wanneer de bestelling wordt verzonden. U hebt nooit rechtstreeks toegang tot reserveringen of maakt deze. [!DNL Commerce] maakt en beheert reserveringen achter de schermen via bestellingen, verzendingen en creditnota&#39;s.

- [Orders en overbrengingen](shipments.md) omvat nieuwe eigenschappen om verzendingen aan te bevelen gebruikend het Algoritme van de Selectie Bron en gedeeltelijke verzendingen van veelvoudige bronnen te steunen om een orde te vervullen.

- Nieuw [functies importeren/exporteren](inventory-import-export.md) kunt u bronnen in massa toevoegen, inventarishoeveelheden bijwerken en de voorraadstatus (in/uit voorraad) voor alle SKU&#39;s in uw catalogus instellen. Met deze functies kunt u één, geselecteerde of alle bronnen wijzigen.

- Nieuwe bulkopties via de pagina Productraster ondersteunen bulksgewijs [Bronnen toewijzen en de toewijzing ervan opheffen](bulk-assignment.md), en [inventariseren naar bron](inventory-transfer.md).

- [!DNL Inventory Management] ondersteunt B2B-catalogi. Momenteel moeten alle B2B-producten worden toegewezen aan de standaardbron en de standaardvoorraad.

## [!DNL Commerce Order Management] en [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] is niet verenigbaar met de [!DNL Inventory Management]. Wanneer MCOM-modules zijn geïnstalleerd, bieden deze alle voorzieningen voor voorraadbeheer aan [!DNL Commerce], met inbegrip van beheer van één en meerdere bronnen, voorraden, reserveringen en meer. De [!DNL Inventory Management] modules worden standaard uitgeschakeld.

MCOM biedt uitgebreide functies en services voor geavanceerd omnichannel-orderbeheer, wereldwijde inventarisatie en multisourcing, opslag naar opslagbestelling en gecentraliseerde klantenservice. Voor een volledige lijst met functies raadpleegt u de [Lijst met MCOM-functies][2].

[!DNL Inventory Management] breidt bestaande [!DNL Commerce] functies met extra opties voor het bijhouden van bestellingen tijdens het proces, on-hand inventarisatie, beschikbare voorraad voor een bestand en API&#39;s voor de ontwikkeling van extensies.

## [!DNL Inventory Management] modules

U kunt desgewenst uitschakelen [!DNL Inventory Management] modules voor:

- Versnellen van de upgrade van de huidige handelaars op Adobe Commerce of Magento Open Source 2.0/2.1/2.2/2.3 en migreren naar 2.4.x.

- Gebruik aangepaste inventarisatie- en bestelbeheermodules of modules van andere leveranciers.

- Gebruiken [!DNL Order Management System] voor voorraadbeheer. De huidige schakelaar steunt niet [!DNL Inventory Management] interfaces. Voor OMS-handelaren die een upgrade uitvoeren naar Adobe Commerce 2.4.0, moeten ze deze modules uitschakelen.

Voor volledige details, zie [Installeren en bijwerken](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
