---
title: Aankooporders voor bedrijven
description: Meer informatie over workflows voor inkooporders waarmee bedrijven hun uitgaven kunnen bijhouden en controleren.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: c1d8bdcd2d09567846ef6819660c57468062ab01
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Aankooporders voor bedrijven

Aankooporders (PO&#39;s) zijn een gemeenschappelijke manier voor bedrijven om hun uitgaven te volgen en te controleren. [ de orde van de Aankoop ](../stores-purchase/purchase-order.md) is één van de standaard off-line betalingsmethodes die in Adobe Commerce en Magento Open Source worden gesteund. Wanneer B2B van Adobe Commerce wordt geïnstalleerd en [_laat de Orden van de Aankoop toe_](account-company-manage.md#advanced-settings) voor een bedrijfrekening wordt geactiveerd, worden alle orden automatisch gecreeerd als Opdrachten van de Aankoop (PO). De gebruikers van het bedrijf met de vereiste [ toestemmingen ](account-company-roles-permissions.md) kunnen tot stand brengen, uitgeven en POs schrappen die zij en POs creëren door ondergeschikte gebruikers worden gecreeerd.

## Kooporderstroom

Afhankelijk van hun rol, en de orde, zouden de bedrijfgebruikers aan verscheidene goedkeuringsregels kunnen worden onderworpen. En afhankelijk van of het gebruiken van online of off-line betalingsmethodes, is de stroom lichtjes verschillend. Bedrijfsbeheerders kunnen automatisch orders maken, waarbij de goedkeuringsregels worden omzeild. Omdat het opslaan van online betalingsgegevens tijdens het goedkeuringsproces een veiligheidsrisico is, worden deze gegevens na goedkeuring toegevoegd en wordt de kooporder vervolgens omgezet in een echte order.

![ stroom van de Kooporde ](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Een bestelling kan niet worden geplaatst als een of meer producten in de kooporder momenteel uit voorraad zijn of zijn.

De workflow voor inkooporders voor een bedrijf kan op een aantal manieren variëren:

- Als er geen goedkeuringsregels zijn vastgesteld, kunnen kooporders worden geplaatst en kan de order rechtstreeks worden uitgevoerd.

  >[!NOTE]
  >
  >Standaard wordt een `Purchase order has been submitted for approval` -bericht altijd weergegeven voor bedrijfsgebruikers, zelfs als er geen goedkeuringsregels zijn ingesteld. Wanneer geen goedkeuringsproces wordt vereist, ontvangen de bedrijfgebruikers automatisch een e-mail die hen informeren dat de orde werd gecreeerd en goedgekeurd.

- Als de goedkeuringsregels door de bedrijfbeheerder worden bepaald, gaan de gebruikers door het goedkeuringsproces.
- Als er meerdere goedkeuringsregels gelden voor een inkooporder, moeten alle unieke vereiste fiatteurs het goedkeuren.
- Bij het aanmaken van de kooporder worden de details van de offlinebetaling ingevoerd.
- De online betalingsgegevens worden ingevoerd nadat de kooporder is goedgekeurd.

>[!NOTE]
>
>De Orden van de aankoop leiden a _momentopname_ van puntprijzen, kortingen, en verschepende prijzen op het tijdstip dat de orde werd gecreeerd. Als de prijs van een item verandert nadat de inkooporder is gemaakt, wordt de oorspronkelijke prijs gebruikt.

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

Als deze regels gelden voor een bedrijf, kan een bedrijfsgebruiker de bestelling direct voltooien wanneer de bestelling minder dan $100 is. Om de definitie van de goedkeuringsregel te leren, zie [ Regels van de Goedkeuring ](account-dashboard-approval-rules.md).

### Soorten winkelgebruikers

De workflow voor inkooporders kan ook verschillen, afhankelijk van wie de aankoop uitvoert.

- Een reguliere werknemer kan aan alle goedkeuringsregels worden onderworpen
- Een manager zou meer koopkracht kunnen hebben en zou verschillende goedkeuringsregels hebben
- Bedrijfsbeheerders kunnen alle goedkeuringsregels omzeilen en hun inkooporders automatisch laten uitvoeren.

Al deze factoren kunnen van invloed zijn op het exacte afrekeningsproces.

## [!UICONTROL My Purchase Orders]

Wanneer inkooporders zijn ingeschakeld voor een bedrijf, wordt het **[!UICONTROL My Purchase Orders]** -item in het linkerdeelvenster weergegeven voor klanten die zijn aangemeld bij een gebruikersaccount van het bedrijf. Er zijn drie tabbladen met verschillende lijsten en functies voor inkooporders:

- **[!UICONTROL My Purchase Orders]**: PO&#39;s die door de klant zijn gemaakt.
- **[!UICONTROL Company Purchase Orders]**: PO&#39;s die worden gemaakt door ondergeschikte gebruikers binnen het bedrijf (zijn afhankelijk van de bedrijfsstructuur en rollen).
- **[!UICONTROL Requires My Approval]**: (Zichtbaar voor aangewezen fiatteurs) PO&#39;s die op goedkeuring van de klant wachten. De teller toont hoeveel orden op goedkeuring wachten.

![ Mijn orden van de Aankoop ](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Voor meer informatie over de gesteunde functies van de inkooporder beschikbaar voor bedrijfgebruikers op de winkel, zie [ Mijn Orden van de Aankoop ](account-dashboard-my-purchase-orders.md).

## Offline versus online betalingsmethoden

Workflows kunnen variëren afhankelijk van de betalingsmethode. Meer over de betalingsmethodes van Adobe Commerce leren, zie [ Methoden van de Betaling ](../stores-purchase/payments.md) in de _Gids van de Ervaring van de Verkoop en van de Aankoop_.

>[!IMPORTANT]
>
>De orden van de aankoop zouden een _In-Context_ controleervaring moeten gebruiken. _uit-van-Context_ controles worden niet gesteund omdat zij de normale controlestroom omzeilen. Over het algemeen, _in-Context_ betekent de klantenverblijven op uw handelsplaats om het proces te voltooien. _uit-van-Context_ is wanneer de klant aan een andere plaats wordt genomen om de aankoop te voltooien.

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
