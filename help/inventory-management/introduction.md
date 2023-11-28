---
title: Inleiding tot Inventory management
description: Leren gebruiken [!DNL Inventory Management] functies voor het beheer van aandelen op meerdere locaties, zodat uw [!DNL Commerce] de fysieke voorraad nauwkeurig wordt weergegeven.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Inleiding tot Inventory management

[!DNL Inventory Management] for [!DNL Commerce] biedt u de tools om uw productvoorraad te beheren. Handelaars met één winkel kunnen deze functies gebruiken om de verkoop en de verzending van goederen te voltooien. U kunt uw inventarishoeveelheden bijhouden, klanten nauwkeurige verkoopbare voorraadbedragen voor al uw websites verstrekken, en verschepen volgens aanbevelingen die op afstand of prioriteit worden gebaseerd. U kunt uw voorkeursproductconfiguraties ook globaal (voor alle winkels en producten), per bron en per product configureren. Deze eigenschappen groeien met uw zaken, toestaand u om van één enkel pakhuis of een complex verschepend netwerk met een paar extra montages te werken.

[!DNL Inventory Management] de volgende functies zijn beschikbaar:

- Verschillende configuraties voor handelaren waarvan de inventaris afkomstig is uit één bron en uit meerdere bronnen
- Voorraden voor het bijhouden van beschikbare geaggregeerde hoeveelheden via toegewezen bronnen
- Gelijktijdige afhandeling
- Verzendingsalgoritmen

>[!NOTE]
>
>Deze functies zijn ontwikkeld als onderdeel van het [Inventory management](https://github.com/magento/inventory) (vroeger MSI) project door het Communautaire Programma van de Techniek.<br/>
>
>De [!DNL Inventory Management] wordt geïnstalleerd met Magento Open Source en Adobe Commerce, waarbij alle functies standaard zijn ingeschakeld. Voor informatie over veranderingen inbegrepen in moduleversies, zie [Opmerkingen bij de release](release-notes.md).

## Basisterminologie

Het is belangrijk dat u de volgende termen begrijpt terwijl u werkt met [!DNL Inventory Management]:

[!UICONTROL **Bronnen**] vertegenwoordigen fysieke plaatsen die beschikbare producten opslaan en verschepen. Deze locaties kunnen opslagplaatsen, baksteen- en mortierwinkels, distributiecentra en slagschepen omvatten. (Elke locatie kan worden aangewezen als bron voor virtuele producten.)

[!UICONTROL **Voorraden**] een verkoopkanaal (momenteel beperkt tot websites) toewijzen aan bronlocaties en on-hand-inventaris. Een voorraad kan aan veelvoudige verkoopkanalen in kaart brengen, maar een verkoopkanaal kan aan slechts één voorraad worden toegewezen.

[!UICONTROL **Geaggregeerde aanpasbare hoeveelheid**] is de totale virtuele voorraad die via een verkoopkanaal kan worden verkocht. Het bedrag wordt berekend over alle bronnen die aan een voorraad zijn toegewezen.

[!UICONTROL **Voorbehouden**] traceer aftrekposten van de verkoopbare hoeveelheid wanneer klanten producten aan winkelwagentjes toevoegen en de afhandeling voltooien. Wanneer een bestelling wordt verzonden, worden de overgebrachte hoeveelheden door de boeking van de specifieke inventarishoeveelheden uit de bron verwijderd en afgetrokken.
