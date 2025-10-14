---
title: Inleiding tot Inventory management
description: Leer hoe te om  [!DNL Inventory Management]  eigenschappen te gebruiken om voorraad in veelvoudige plaatsen te beheren zodat uw  [!DNL Commerce]  opslag nauwkeurig op de fysieke inventaris wijst.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Inleiding tot Inventory management

[!DNL Inventory Management] for [!DNL Commerce] biedt u de tools om uw productvoorraad te beheren. Handelaars met één winkel kunnen deze functies gebruiken om de verkoop en de verzending van goederen te voltooien. U kunt uw inventarishoeveelheden bijhouden, klanten nauwkeurige verkoopbare voorraadbedragen voor al uw websites verstrekken, en verschepen volgens aanbevelingen die op afstand of prioriteit worden gebaseerd. U kunt uw voorkeursproductconfiguraties ook globaal (voor alle winkels en producten), per bron en per product configureren. Deze eigenschappen groeien met uw zaken, toestaand u om van één enkel pakhuis of een complex verschepend netwerk met een paar extra montages te werken.

[!DNL Inventory Management] bevat de volgende functies:

- Verschillende configuraties voor handelaren waarvan de inventaris afkomstig is uit één bron en uit meerdere bronnen
- Voorraden voor het bijhouden van beschikbare geaggregeerde hoeveelheden via toegewezen bronnen
- Gelijktijdige afhandeling
- Verzendingsalgoritmen

>[!NOTE]
>
>Deze eigenschappen werden ontwikkeld als deel van [&#x200B; Inventory management &#x200B;](https://github.com/magento/inventory) (vroeger MSI) project door het Communautaire programma van de Techniek.<br/>
>
>De module [!DNL Inventory Management] wordt geïnstalleerd met Magento Open Source en Adobe Commerce, waarbij alle functies standaard zijn ingeschakeld. Voor informatie over veranderingen inbegrepen in moduleversies, zie de [&#x200B; Nota&#39;s van de Versie &#x200B;](release-notes.md).

## Basisterminologie

Het is belangrijk dat u de volgende termen begrijpt terwijl u met [!DNL Inventory Management] werkt:

[!UICONTROL **de Bronnen**] vertegenwoordigen fysieke plaatsen die opslaan en beschikbare producten verschepen. Deze locaties kunnen opslagplaatsen, baksteen- en mortierwinkels, distributiecentra en slagschepen omvatten. (Elke locatie kan worden aangewezen als bron voor virtuele producten.)

[!UICONTROL **Stocks**] kaart een verkoopkanaal (momenteel beperkt tot websites) aan bronplaatsen en inventaris. Een voorraad kan aan veelvoudige verkoopkanalen in kaart brengen, maar een verkoopkanaal kan aan slechts één voorraad worden toegewezen.

[!UICONTROL **Geaggregeerde Verkoop Aantal**] is de totale virtuele inventaris die door een verkoopkanaal kan worden verkocht. Het bedrag wordt berekend over alle bronnen die aan een voorraad zijn toegewezen.

[!UICONTROL **de spooraftrek van Reserveringen**] van de verkoopbare hoeveelheid aangezien de klanten producten aan karretjes en volledige controle toevoegen. Wanneer een bestelling wordt verzonden, worden de overgebrachte hoeveelheden door de boeking van de specifieke inventarishoeveelheden uit de bron verwijderd en afgetrokken.
