---
title: Voorraden en bronnen
description: Meer informatie over de relaties tussen producten, bronnen en bestanden.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---

# Voorraden en bronnen

Beheer uw voorraad ongeacht de opslaglocatie, het type product of service of het verkoopkanaal. Geef bestellingen en verzendproducten van meerdere pakhuizen, baksteen- en mortierwinkels, distributiecentra en verzendingen af om bestellingen te voltooien met de nadruk op evenwichtige inventarisatie, verzendkosten en nog veel meer.

Deze beschrijvingen omvatten producten, bronnen en voorraden voor een fietsbedrijf met meerdere verzendlocaties en websites in de Verenigde Staten en Europa.

## Bronnen

[Bronnen](sources-manage.md) zijn de fysieke locaties waar de productinventaris wordt beheerd en verzonden voor het uitvoeren van bestellingen of waar services beschikbaar zijn. Deze locaties kunnen opslagplaatsen, baksteen- en mortierwinkels, distributiecentra en slagschepen omvatten. [!DNL Commerce] de hoeveelheden en de verkoopbare hoeveelheden per voorraad gebruikt en de voorraadbedragen voor beheerde producten en orders automatisch beheert. Als u één bron hebt, wordt u overwogen in _uit één bron_ -modus. Als u meerdere bronnen hebt, wordt u overwogen in _meerbron_ -modus.

Een bron kan voorrang hebben in de omvang van de voorraad in één entrepot, maar niet noodzakelijkerwijs in alle entrepots, aangezien de bron in verschillende voorraden kan worden hergebruikt. Het aantal voorraden en bronnen vergroot de complexiteit om te bepalen wat het beste pakhuis of de beste opslagplaats is om een bestelling uit te voeren. U hebt bijvoorbeeld een beperkt aantal producten beschikbaar op uw baksteen- en mortierlocaties met een uitgebreide voorraad in uw pakhuizen en services op belangrijke locaties met beperkte beschikbaarheid.

In dit voorbeeld beschikt de handelaar over een bergfiets die kan worden verzonden vanuit winkels, opslagplaatsen en een verlopende scheepsbevrachter.

![Voorbeeld van brondiagram](assets/diagram-sources.png){width="600" zoomable="yes"}

## Voorraden

[Voorraden](stocks-manage.md) een virtuele, geaggregeerde inventaris weergeven van producten die beschikbaar zijn voor verkoop aan uw verkoopkanalen (websites). Elke voorraad wijst uw verkoopkanalen met bronnen voor beschikbare inventarissen en verkoopbare hoeveelheden in kaart. Afhankelijk van uw plaatsconfiguratie, kan de voorraad aan één of meerdere verkoopkanalen en bronnen worden toegewezen.

Sales Channel vertegenwoordigen entiteiten die uw voorraad verkopen, zoals websites, winkelweergaven, B2B-klantgroepen enzovoort. Verkoopkanalen kunnen slechts aan één voorraad worden gekoppeld. Aan elk verkoopkanaal kan slechts één voorraad worden toegewezen en aan meerdere websites kan één voorraad worden toegewezen. Via de voorraad kunt u de prioritering wijzigen van bronnen die worden gebruikt bij verzendopdrachten en door de [Algoritme voor bronselectie](selection-reservations.md).

U begint met een standaardvoorraad die is toegewezen aan de standaardbron en uw website. Deze worden het beste gebruikt door single-source-handelaren. Alleen de standaardbron kan aan dit bestand worden toegewezen. Multikobron-handelaren maken waar nodig aangepaste voorraden voor aangepaste bronnen en websites.

![Diagram van bijvoorbeeld voorraden voor een winkel](assets/diagram-stock.png){width="600" zoomable="yes"}

## Producthoeveelheden

De hoeveelheid is het aantal producten in uw actieve voorraad dat kan worden aangeschaft. De hoeveelheid producten neemt toe en af wanneer u de verzending voltooit of de voorraad aanpast. Het toevoegen van producten aan een winkelwagentje heeft geen invloed op deze hoeveelheid. In het vak Aankoopbare hoeveelheid wordt de beschikbaarheid van het product voor een verkoopkanaal bijgehouden en wordt deze waarde ook gebruikt om de beschikbare voorraad voor aankoop te bepalen. Afhankelijk van het aantal bronnen, ziet en beheert u de producthoeveelheid voor een van de volgende opties:

- **Aantal** - Voor eenbronhandelaren: _[!UICONTROL Quantity]_de kolom en de waarde volgen de hoeveelheid beschikbare voorraad van de hand.
- **Hoeveelheid per bron** - Voor multisourcinghandelaren: _[!UICONTROL Quantity per Source]_de kolom en de waarden volgen de voorraad aan de hand beschikbaar door plaats. Als u meerdere bronnen toevoegt, vervangt deze waarde de Hoeveelheid en wordt elke bron en toegewezen hoeveelheid weergegeven.

De reserves volgen voorraadverzoeken voor het volledige het winkelen proces-toevoegend producten aan karretje, het voltooien van controle, en het beheren van terugbetalingen. Voor de beschikbare voorraad en voorraad wordt de reservevoorraad per bestelling via het afrekeningsproces van de verkoopbare hoeveelheid afgetrokken. Voorbehouden worden omgezet in aftrekbare hoeveelheden bij facturering en verzending van producten.

Met Aankoopbare hoeveelheid wordt de virtuele inventaris van producten (of beschikbaarheid) berekend aan de hand van geconfigureerde drempelwaarden, gereserveerde of verkochte hoeveelheden en hoeveelheden per bron. Voor elk bestand: [!DNL Commerce] Hiermee krijgt u toegang tot alle toegewezen bronnen en bijbehorende producthoeveelheden als aggregaat. Met deze basiswaarde trekt het dan alle reserveringsbedragen en _[!UICONTROL Notify for Quantity Below]_drempelwaarde.

![Berekening van de verkoopbare hoeveelheid voor een voorraad](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Voorraadconfiguraties

Elk product, bron, en voorraad omvat verscheidene opties om voor uw opslag op het globale, bron, voorraad, en productniveau te vormen. Voor een volledige lijst van deze opties, verwijs naar [Inventory management configureren](configuration.md).

De volgende opties zijn belangrijk voor [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Hier geeft u een bedrag op dat u van het verkoopbare aantal wilt aftrekken. Als u Achterorden toelaat, wordt deze waarde niet afgetrokken van het Aankoopbare Aantal.
- **[!UICONTROL Backorders]** - Hiermee wordt bepaald of producten na een nulvoorraad kunnen worden verkocht, waardoor bestellingen worden bewaard totdat de voorraad wordt opgevuld. Wanneer de backorders worden toegelaten, vormend [!UICONTROL Out-of-Stock Threshold] wordt aanbevolen.

>[!NOTE]
>
>De waarde bij Drempel voor de out-of-stock ondersteunt negatieve en positieve bedragen. Als u Achterorden toelaat, plaats deze waarde aan een negatieve hoeveelheid voor het maximumaantal producten die kunnen worden achtergeordend alvorens het product werkelijk als buiten voorraad wordt beschouwd.

## Inventory management demo

Bekijk deze video voor meer informatie over Inventory management-bronnen en -voorraden:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12)
