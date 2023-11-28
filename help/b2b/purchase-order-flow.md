---
title: Aankooporders voor bedrijven
description: Meer informatie over workflows voor inkooporders waarmee bedrijven hun uitgaven kunnen bijhouden en controleren.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# Aankooporders voor bedrijven

Aankooporders (PO&#39;s) zijn een gemeenschappelijke manier voor bedrijven om hun uitgaven te volgen en te controleren. [Aankooporder](../stores-purchase/purchase-order.md) is een van de standaardmethoden voor offlinebetalingen die in Adobe Commerce en Magento Open Source worden ondersteund. Wanneer B2B van Adobe Commerce is geïnstalleerd en [_Aankooporders inschakelen_](account-company-manage.md#advanced-settings) wordt geactiveerd voor een bedrijfsaccount, worden alle bestellingen automatisch gemaakt als inkooporders (PO). Bedrijfgebruikers met de vereiste [machtigingen](account-company-roles-permissions.md) kan, POs tot stand brengen uitgeven en schrappen die zij en POs creëren die door ondergeschikte gebruikers worden gecreeerd.

## Kooporderstroom

Afhankelijk van hun rol, en de orde, zouden de bedrijfgebruikers aan verscheidene goedkeuringsregels kunnen worden onderworpen. En afhankelijk van of het gebruiken van online of off-line betalingsmethodes, is de stroom lichtjes verschillend. Bedrijfsbeheerders kunnen automatisch orders maken, waarbij de goedkeuringsregels worden omzeild. Omdat het opslaan van online betalingsgegevens tijdens het goedkeuringsproces een veiligheidsrisico is, worden deze gegevens na goedkeuring toegevoegd en wordt de kooporder vervolgens omgezet in een echte order.

![Kooporderstroom](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

De workflow voor inkooporders voor een bedrijf kan op een aantal manieren variëren:

- Als er geen goedkeuringsregels zijn vastgesteld, kunnen kooporders worden geplaatst en kan de order rechtstreeks worden uitgevoerd.

  >[!NOTE]
  >
  >Standaard wordt een `Purchase order has been submitted for approval` het bericht wordt altijd getoond aan bedrijfgebruikers, zelfs wanneer geen goedkeuringsregels worden geplaatst. Wanneer geen goedkeuringsproces wordt vereist, ontvangen de bedrijfgebruikers automatisch een e-mail die hen informeren dat de orde werd gecreeerd en goedgekeurd.

- Als de goedkeuringsregels door de bedrijfbeheerder worden bepaald, gaan de gebruikers door het goedkeuringsproces.
- Bij het aanmaken van de kooporder worden de details van de offlinebetaling ingevoerd.
- De online betalingsgegevens worden ingevoerd nadat de kooporder is goedgekeurd.

>[!NOTE]
>
>Inkooporders maken een _opname_ van objectprijzen, kortingen en verzendprijzen op het moment dat de bestelling werd gemaakt. Als de prijs van een item verandert nadat de inkooporder is gemaakt, wordt de oorspronkelijke prijs gebruikt.

### Voorbeeld van een standaardworkflow

Bedrijven gebruiken inkooporders om te controleren wat werknemers namens het bedrijf kunnen kopen en stellen vaak goedkeuringsregels op om de richtlijnen van het bedrijf af te dwingen. Afhankelijk van de goedkeuringsregels kunnen meerdere personen de volgorde moeten goedkeuren.

1. Gebruiker maakt een kooporder voor goederen van $25.000.
1. Hun manager moet goedkeuren.
1. Omdat de bestelling meer dan $10.000 is, moet V.P. ook goedkeuren.
1. Afhankelijk van de betalingsmethode wordt de kooporder na de goedkeuring automatisch omgezet in een bestelling of keert de gebruiker terug om de betalingsgegevens in te voeren.

### Goedkeuringsvoorschriften

De goedkeuringsregels worden gebruikt om uitgaven te controleren die op bedrijfsrichtlijnen worden gebaseerd. Voorbeelden van goedkeuringsregels zijn:

- Voor elke bestelling van meer dan $100 is de goedkeuring van uw manager vereist.
- Voor elke bestelling van meer dan $1000 is de goedkeuring van uw manager en de bedrijfsbeheerder vereist.
- Om het even welke orde met meer dan 30 unieke SKUs vereist de goedkeuring van de bedrijfbeheerder.

Als deze regels gelden voor een bedrijf, kan een bedrijfsgebruiker de bestelling direct voltooien wanneer de bestelling minder dan $100 is. Zie voor meer informatie over de definitie van goedkeuringsregels [Goedkeuringsregels](account-dashboard-approval-rules.md)

### Soorten winkelgebruikers

De workflow voor inkooporders kan ook verschillen, afhankelijk van wie de aankoop uitvoert.

- Een reguliere werknemer kan aan alle goedkeuringsregels worden onderworpen
- Een manager zou meer koopkracht kunnen hebben en zou verschillende goedkeuringsregels hebben
- Bedrijfsbeheerders kunnen alle goedkeuringsregels omzeilen en hun inkooporders automatisch laten uitvoeren.

Al deze factoren kunnen van invloed zijn op het exacte afrekeningsproces.

## [!UICONTROL My Purchase Orders]

Wanneer inkooporders voor een bedrijf zijn ingeschakeld, wordt **[!UICONTROL My Purchase Orders]** Het item wordt in het linkerdeelvenster weergegeven voor klanten die zijn aangemeld bij een gebruikersaccount van een bedrijf. Er zijn drie tabbladen met verschillende lijsten en functies voor inkooporders:

- **[!UICONTROL My Purchase Orders]**: POs die door de klant wordt gecreeerd.
- **[!UICONTROL Company Purchase Orders]**: POs die door ondergeschikte gebruikers binnen het bedrijf worden gemaakt (hangt van bedrijfsstructuur en rollen af).
- **[!UICONTROL Requires My Approval]**: (Zichtbaar voor aangewezen fiatteurs) POs die op de goedkeuring van de klant wachten. De teller toont hoeveel orden op goedkeuring wachten.

![Mijn inkooporders](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Voor meer informatie over de ondersteunde functies voor inkooporders die beschikbaar zijn voor gebruikers van bedrijven in de winkel, raadpleegt u [Mijn inkooporders](account-dashboard-my-purchase-orders.md).

## Offline versus online betalingsmethoden

Workflows kunnen variëren afhankelijk van de betalingsmethode. Ga voor meer informatie over betalingsmethoden van Adobe Commerce naar [Betalingsmethoden](../stores-purchase/payments.md) in de _Handleiding voor verkoop- en aankoopervaring_.

>[!IMPORTANT]
>
>Aankooporders moeten een _In context_ uitcheckervaring. _Buiten context_ kassa&#39;s worden niet ondersteund omdat deze de normale afrekenstroom omzeilen. In het algemeen _In context_ betekent de klant op uw handelsplaats blijft om het proces te voltooien. _Buiten context_ is wanneer de klant naar een andere site wordt gebracht om de aankoop te voltooien.

### Online betalingen

Om veiligheidsredenen willen online-winkels doorgaans geen creditcardgegevens van de winkel verzamelen in afwachting van de voltooiing van het goedkeuringsproces. Als een optie voor online betaling is geselecteerd, keert de maker van de inkooporder na goedkeuring terug naar de winkel, voert hij de betalingsgegevens in en voltooit hij de bestelling. Voorbeelden van online betalingen zijn:

- Creditcard/bankpas
- PayPal
- Braintree

>[!IMPORTANT]
>
>Het gebruik van cadeaukaarten, creditpunten of bonuspunten met online betalingsmethoden voor inkooporders wordt niet ondersteund. Als u deze functies inschakelt met onlinebetalingen, kan dit onverwachte gevolgen hebben. U wordt aangeraden cadeaukaarten uit te schakelen, crediteringen en bonuspunten op te slaan wanneer onlinebetalingen zijn ingeschakeld voor inkooporders.

### Offlinebetalingen

Aangezien offlinebetalingsmethoden, zoals een postwissel, buiten de website worden afgehandeld, zijn ze veiliger. Aankooporders met offline betalingen kunnen na elk goedkeuringsproces automatisch worden verwerkt.

Voorbeelden van offline betalingen zijn:

- Cheque/postwissel
- Betaling op rekening
- Onder rembours
- Bankoverschrijvingen
- Winkelkrediet
