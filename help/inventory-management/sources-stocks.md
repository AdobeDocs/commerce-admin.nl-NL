---
title: Voorraden en bronnen
description: Meer informatie over de relaties tussen producten, bronnen en bestanden.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Voorraden en bronnen

Beheer uw voorraad ongeacht de opslaglocatie, het type product of service of het verkoopkanaal. Geef bestellingen en verzendproducten van meerdere pakhuizen, baksteen- en mortierwinkels, distributiecentra en verzendingen af om bestellingen te voltooien met de nadruk op evenwichtige inventarisatie, verzendkosten en nog veel meer.

Deze beschrijvingen omvatten producten, bronnen en voorraden voor een fietsbedrijf met meerdere verzendlocaties en websites in de Verenigde Staten en Europa.

## Bronnen

[&#x200B; de Bronnen &#x200B;](sources-manage.md) zijn de fysieke plaatsen waar de productinventaris wordt beheerd en voor ordevervulling verscheept of waar de diensten beschikbaar zijn. Deze locaties kunnen opslagplaatsen, baksteen- en mortierwinkels, distributiecentra en slagschepen omvatten. [!DNL Commerce] gebruikt de hoeveelheden en de verkoopbare hoeveelheden per voorraad en beheert de inventarisbedragen automatisch voor beheerde producten en bestellingen. Als u één bron hebt, wordt u overwogen op _enig-bron_ wijze. Als u veelvoudige bronnen hebt, wordt u overwogen op _multi-source_ wijze.

Een bron kan voorrang hebben in de omvang van de voorraad in één entrepot, maar niet noodzakelijkerwijs in alle entrepots, aangezien de bron in verschillende voorraden kan worden hergebruikt. Het aantal voorraden en bronnen vergroot de complexiteit om te bepalen wat het beste pakhuis of de beste opslagplaats is om een bestelling uit te voeren. U hebt bijvoorbeeld een beperkt aantal producten beschikbaar op uw baksteen- en mortierlocaties met een uitgebreide voorraad in uw pakhuizen en services op belangrijke locaties met beperkte beschikbaarheid.

In dit voorbeeld beschikt de handelaar over een bergfiets die kan worden verzonden vanuit winkels, opslagplaatsen en een verlopende scheepsbevrachter.

![&#x200B; Bronsdiagram van het Voorbeeld &#x200B;](assets/diagram-sources.png){width="600" zoomable="yes"}

## Voorraden

[&#x200B; Voorraden &#x200B;](stocks-manage.md) vertegenwoordigen een virtuele, bijeengevoegde inventaris van producten beschikbaar voor verkoop aan uw verkoopkanalen (websites). Elke voorraad wijst uw verkoopkanalen met bronnen voor beschikbare inventarissen en verkoopbare hoeveelheden in kaart. Afhankelijk van uw plaatsconfiguratie, kan de voorraad aan één of meerdere verkoopkanalen en bronnen worden toegewezen.

Sales Channel vertegenwoordigen entiteiten die uw voorraad verkopen, zoals websites, winkelweergaven, B2B-klantgroepen enzovoort. Verkoopkanalen kunnen slechts aan één voorraad worden gekoppeld. Aan elk verkoopkanaal kan slechts één voorraad worden toegewezen en aan meerdere websites kan één voorraad worden toegewezen. Door de voorraad, kunt u de prioritering van gebruikte bronnen wijzigen wanneer het verschepen van orden en door het [&#x200B; Algoritme van de Selectie van Source &#x200B;](selection-reservations.md).

U begint met een standaardvoorraad die is toegewezen met de standaard-Source en uw website. Deze wordt het beste gebruikt door single-source-handelaren. Alleen de standaard Source kan aan deze voorraad worden toegewezen. Multikobron-handelaren maken waar nodig aangepaste voorraden voor aangepaste bronnen en websites.

![&#x200B; Diagram voor bijvoorbeeld voorraden voor een opslag &#x200B;](assets/diagram-stock.png){width="600" zoomable="yes"}

## Producthoeveelheden

De hoeveelheid is het aantal producten in uw actieve voorraad dat kan worden aangeschaft. De hoeveelheid producten neemt toe en af wanneer u de verzending voltooit of de voorraad aanpast. Het toevoegen van producten aan een winkelwagentje heeft geen invloed op deze hoeveelheid. In het vak Aankoopbare hoeveelheid wordt de beschikbaarheid van het product voor een verkoopkanaal bijgehouden en wordt deze waarde ook gebruikt om de beschikbare voorraad voor aankoop te bepalen. Afhankelijk van het aantal bronnen, ziet en beheert u de producthoeveelheid voor een van de volgende opties:

- **Hoeveelheid** - voor single-source handelaren, volgen de _[!UICONTROL Quantity]_&#x200B;kolom en de waarde de hoeveelheid beschikbare voorraad van de hand.
- **Hoeveelheid per Source** - voor multi-bronverkopers, volgen de _[!UICONTROL Quantity per Source]_&#x200B;kolom en de waarden de voorraad ter plaatse beschikbaar door plaats. Als u meerdere bronnen toevoegt, vervangt deze waarde de Hoeveelheid en wordt elke bron en toegewezen hoeveelheid weergegeven.

De reserves volgen voorraadverzoeken voor het volledige het winkelen proces-toevoegend producten aan karretje, het voltooien van controle, en het beheren van terugbetalingen. Voor de beschikbare voorraad en voorraad wordt de reservevoorraad per bestelling via het afrekeningsproces van de verkoopbare hoeveelheid afgetrokken. Voorbehouden worden omgezet in aftrekbare hoeveelheden bij facturering en verzending van producten.

Met Aankoopbare hoeveelheid wordt de virtuele inventaris van producten (of beschikbaarheid) berekend aan de hand van geconfigureerde drempelwaarden, gereserveerde of verkochte hoeveelheden en hoeveelheden per bron. Voor elke voorraad heeft [!DNL Commerce] toegang tot alle toegewezen bronnen en bijbehorende producthoeveelheden als aggregaat. Met deze basiswaarde worden vervolgens alle reserveringsbedragen en de drempelwaarde _[!UICONTROL Notify for Quantity Below]_&#x200B;afgetrokken.

![&#x200B; Berekend de verkoopbare hoeveelheid voor een voorraad &#x200B;](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Voorraadconfiguraties

Elk product, bron, en voorraad omvat verscheidene opties om voor uw opslag op het globale, bron, voorraad, en productniveau te vormen. Voor een volledige lijst van deze opties, verwijs naar [&#x200B; het Vormen Inventory management &#x200B;](configuration.md).

De volgende belangrijke opties zijn belangrijk voor [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Hiermee stelt u een bedrag in dat u van het verkoopbare aantal wilt aftrekken. Als u Achterorden toelaat, wordt deze waarde niet afgetrokken van het Aankoopbare Aantal.
- **[!UICONTROL Backorders]** - Hiermee bepaalt u of producten na een nulvoorraad kunnen worden verkocht, waardoor bestellingen worden opgeslagen totdat ze opnieuw worden opgeslagen. Wanneer de backorders worden toegelaten, wordt het vormen van [!UICONTROL Out-of-Stock Threshold] geadviseerd.

>[!NOTE]
>
>De waarde bij Drempel voor de out-of-stock ondersteunt negatieve en positieve bedragen. Als u Achterorden toelaat, plaats deze waarde aan een negatieve hoeveelheid voor het maximumaantal producten die kunnen worden achtergeordend alvorens het product werkelijk als buiten voorraad wordt beschouwd.

## Inventory management demo

Bekijk deze video voor meer informatie over Inventory management-bronnen en -voorraden:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12&learn=on)
