---
title: Bestellingen en verzendingen beheren vanuit voorraad
description: Meer informatie over de extra [!DNL Inventory Management] kenmerken en opties voor het beheer van de inventarishoeveelheden via het verzendingsproces.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Bestellingen en verzendingen beheren

[!DNL Inventory Management] bevat aanvullende kenmerken en opties voor het beheer van inventarishoeveelheden tijdens het verzendproces. Terwijl u verzendingen controleert en uitvoert, bestellingen annuleert en creditnota&#39;s uitgeeft, worden de verkochte producten en hoeveelheden van het product automatisch bijgewerkt.

Deze informatie bevat specificaties voor [!DNL Inventory Management]. Zie voor meer informatie de [Orders](../stores-purchase/orders.md){target="_blank"} in het _Handleiding voor verkoop- en aankoopervaring_.

## Orders

[!DNL Commerce] steunt enige orden en multi-adresorden uit-van-de-doos zonder extra configuraties. Als klanten of personeel orders invoeren, [!DNL Inventory Management] inventarisatie bijhoudt met behulp van reserveringen ten opzichte van de verkoopbare hoeveelheid, in mindering gebracht op de voorraadhoeveelheid voor gefactureerde en verzonden producten.

### Volgorde van meerdere adressen

Voor multi-adresorden, wordt een reeks enige orden geproduceerd-voor elk ingegaan bestemmingsadres. Tijdens controle, selecteren de klanten elke reeks producten verbonden per adres tijdens controle produceert als enige orden volgens het bestemmingsadres. Elke orde omvat de producten verbonden per adres.

[!DNL Commerce] beheert voorraad voor deze multi-adresorden precies zoals enige orden. Het staat voor de aanbevelingen van het Algoritme van de Selectie Source of met voeten treedt tijdens verzending, gedeeltelijke overbrengingen, het annuleren van orden, en het terugvloeien met voorraadupdates toe.

![Meerdere adressen bij afrekenen](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Restituties

Wanneer u een [creditnota](../stores-purchase/credit-memo-create.md){target="_blank"} als u een restitutie wilt toekennen, kunt u de hoeveelheid van het product terugsturen naar de afgetrokken bron. De orderinformatie bevat de inventarisbron die het product heeft verzonden. Het wordt aanbevolen de geretourneerde producthoeveelheid toe te wijzen via een creditnota wanneer u het geretourneerde product ontvangt.

![Objecten die moeten worden terugbetaald met Terug naar voorraad geselecteerd](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Niet-verzonden bestellingen annuleren

Indien een order niet is verzonden en (geheel of gedeeltelijk) wordt geannuleerd, [!DNL Inventory Management] de voorraad van het product wordt automatisch teruggebracht naar de verkoopbare hoeveelheid. Tot de factuur en de verzending worden de aangekochte producten afgeboekt op de verkoopbare hoeveelheid en niet afgetrokken van de werkelijke hoeveelheid. Op het punt van facturering en verzending van de bestelling zet het systeem de boeking om in een voorraadaftrek.

achter de schermen, [!DNL Inventory Management] automatisch een compensatievoorbehoud maakt waardoor het houdbedrag van de producthoeveelheid wordt verwijderd. De hoeveelheid wordt teruggebracht naar de geaggregeerde virtuele verkoopbare hoeveelheid.

## Overbrengingen

Met [!DNL Inventory Management] Geactiveerd, kunt u gedeeltelijke of volledige zendingen van één of meerdere bronnen verzenden om orden te vervullen. U beheert de uitgaande voorraad voor elke bestelling, waarbij u de af te trekken bedragen instelt, een of meer verzendingen verzendt en de voorraad en de achterstand instelt terwijl de voorraad beschikbaar is. Voer voor elk regelitem in de volgorde een bedrag in dat van de bronhoeveelheid moet worden afgetrokken. Genereer een verzending per bron terwijl u voorraad voorraad hebt, totdat aan de volledige bestelling is voldaan.

### Gedeeltelijke overbrengingen

Voor multisource-handelaren: [!DNL Commerce] genereert een verzending voor elke bron die u selecteert. Met de algemene workflow kunt u een bron selecteren, de hoeveelheid producten instellen die moet worden afgetrokken om aan de bestelling te voldoen en doorgaan met de verzending. Als u klaar bent, maakt u aanvullende verzendingen voor elke bron totdat u aan de bestelling hebt voldaan.

Single-source-handelaren kunnen ook gedeeltelijke verzendingen verzenden ter ondersteuning van backorders of balanstotaal wanneer bestellingen worden binnengebracht voor populaire items.

### Algoritme voor Recommendations- en bronselectie

De [Algoritme voor bronselectie](selection-reservations.md) (SSA) bevat aanbevelingen voor gedeeltelijke en volledige overbrengingen. U hebt toegang tot algoritmen voor bronselectie wanneer u verzendfacturen voor een bestelling maakt. Voer via de pagina Schip op elk gewenst moment het algoritme Bronprioriteit of Afstand Prioriteit uit om de beste opties voor het afstemmen van geordende hoeveelheden en beschikbare bronnen te bepalen. Het systeem ondersteunt het verzenden van een volledige bestelling van één bron en het verbreken van de bestelling in meerdere gedeeltelijke verzendingen van meerdere bronnen. U hebt toegang tot deze opties voor directe uitvoering en gespreide verzending om in de loop der tijd kleinere hoeveelheden te verzenden.

Om een bestelling te voltooien en te verzenden, moet deze zijn voldaan en gefactureerd. Momenteel, kunt u SSA voor aanbevelingen en schip van één of meerdere bronnen opnieuw uitvoeren, of de aanbevelingen SSA met manueel vastgestelde bronnen en hoeveelheden met voeten treden om verzending te vervullen.

- U wordt aangeraden de SSA opnieuw uit te voeren om de aanbevelingen voor elke verzending te beoordelen.

- Als u de selecties wilt wijzigen, kunt u deze overschrijven met handmatige bronaftrekkingen.

### Overbrengingen en reserveringen

Bij het genereren van de zendingen worden de voorbehouden voor de producten duidelijk en wordt de producthoeveelheid afgetrokken. De hoeveelheid per voorraad wordt bijgewerkt op basis van de verzendingsgegevens. Als u bijvoorbeeld zendingen verzendt voor tien producten uit twee bronnen, brengen de hoeveelheden voor die bronnen elk 10 in mindering. De verkoopbare hoeveelheid wordt automatisch vernieuwd voor de bijbehorende voorraden, zodat klanten en personeel de meest recente productbedragen krijgen. En de bedenkingen zijn volkomen duidelijk, en tellen niet langer mee voor de salarishoeveelheid.
