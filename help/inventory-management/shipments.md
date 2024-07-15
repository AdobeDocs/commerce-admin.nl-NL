---
title: Bestellingen en verzendingen beheren vanuit voorraad
description: Leer over de extra  [!DNL Inventory Management]  eigenschappen en de opties om inventarishoeveelheden door het verzendingsproces te beheren.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Bestellingen en verzendingen beheren

[!DNL Inventory Management] bevat aanvullende functies en opties voor het beheer van inventarishoeveelheden tijdens het verzendproces. Terwijl u verzendingen controleert en uitvoert, bestellingen annuleert en creditnota&#39;s uitgeeft, worden de verkochte producten en hoeveelheden van het product automatisch bijgewerkt.

Deze informatie bevat specificaties voor [!DNL Inventory Management] . Voor extra informatie, zie het [ onderwerp van Orden ](../stores-purchase/orders.md){target="_blank"} in de _Gids van de Ervaring van de Verkoop en van de Aankoop_.

## Orders

[!DNL Commerce] ondersteunt losse bestellingen en bestellingen voor meerdere adressen buiten de box zonder extra configuraties. Terwijl klanten of personeel orders invoeren, houdt [!DNL Inventory Management] inventarisaties bij met behulp van reserveringen voor de verkoopbare hoeveelheid, in mindering gebracht op de voorraadhoeveelheid voor gefactureerde en verzonden producten.

### Volgorde van meerdere adressen

Voor multi-adresorden, wordt een reeks enige orden geproduceerd-voor elk ingegaan bestemmingsadres. Tijdens controle, selecteren de klanten elke reeks producten verbonden per adres tijdens controle produceert als enige orden volgens het bestemmingsadres. Elke orde omvat de producten verbonden per adres.

[!DNL Commerce] beheert een overzicht voor deze bestellingen met meerdere adressen, net als voor afzonderlijke bestellingen. Het staat voor de aanbevelingen of met voeten treedt van het Algoritme van de Selectie van Source tijdens verzending, gedeeltelijke overbrengingen, het annuleren van orden, en het terugvloeien met voorraadupdates toe.

![ Multi-address bij controle ](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Restituties

Wanneer het ingaan van a [ kredietmemo ](../stores-purchase/credit-memo-create.md){target="_blank"} om een restitutie uit te geven, kunt u de producthoeveelheid aan de afgetrokken bron terugkeren. De orderinformatie bevat de inventarisbron die het product heeft verzonden. Het wordt aanbevolen de geretourneerde producthoeveelheid toe te wijzen via een creditnota wanneer u het geretourneerde product ontvangt.

![ Punten aan Terugbetaling met Terugkeer aan Geselecteerde Voorraad ](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Niet-verzonden bestellingen annuleren

Als een bestelling niet is verzonden en wordt geannuleerd (geheel of gedeeltelijk), retourneert [!DNL Inventory Management] automatisch de productvoorraad naar de verkoopbare hoeveelheid. Tot de factuur en de verzending worden de aangekochte producten afgeboekt op de verkoopbare hoeveelheid en niet afgetrokken van de werkelijke hoeveelheid. Op het punt van facturering en verzending van de bestelling zet het systeem de boeking om in een voorraadaftrek.

Achter de schermen voert [!DNL Inventory Management] automatisch een compensatiereservering in waarbij de wachtstand op de producthoeveelheid wordt verwijderd. De hoeveelheid wordt teruggebracht naar de geaggregeerde virtuele verkoopbare hoeveelheid.

## Overbrengingen

Als [!DNL Inventory Management] is ingeschakeld, kunt u gehele of gedeeltelijke zendingen van een of meer bronnen verzenden om orders uit te voeren. U beheert de uitgaande voorraad voor elke bestelling, waarbij u de af te trekken bedragen instelt, een of meer verzendingen verzendt en de voorraad en de achterstand instelt terwijl de voorraad beschikbaar is. Voer voor elk regelitem in de volgorde een bedrag in dat van de bronhoeveelheid moet worden afgetrokken. Genereer een verzending per bron terwijl u voorraad voorraad hebt, totdat aan de volledige bestelling is voldaan.

### Gedeeltelijke overbrengingen

Voor leveranciers met meerdere bronnen genereert [!DNL Commerce] een verzending voor elke bron die u selecteert. Met de algemene workflow kunt u een bron selecteren, de hoeveelheid producten instellen die moet worden afgetrokken om aan de bestelling te voldoen en doorgaan met de verzending. Als u klaar bent, maakt u aanvullende verzendingen voor elke bron totdat u aan de bestelling hebt voldaan.

Single-source-handelaren kunnen ook gedeeltelijke verzendingen verzenden ter ondersteuning van backorders of balanstotaal wanneer bestellingen worden binnengebracht voor populaire items.

### Recommendations- en Source-selectiealgoritme

Het [ Algoritme van de Selectie van Source ](selection-reservations.md) (SSA) verstrekt aanbevelingen voor gedeeltelijke en volledige transporten. U hebt toegang tot Source-selectiealgoritmen wanneer u verzendfacturen voor een bestelling maakt. Voer op elk gewenst moment via de pagina Schip het algoritme Source Priority of Distance Priority uit om de beste opties voor het afstemmen van geordende hoeveelheden en beschikbare bronnen te bepalen. Het systeem ondersteunt het verzenden van een volledige bestelling van één bron en het verbreken van de bestelling in meerdere gedeeltelijke verzendingen van meerdere bronnen. U hebt toegang tot deze opties voor directe uitvoering en gespreide verzending om in de loop der tijd kleinere hoeveelheden te verzenden.

Om een bestelling te voltooien en te verzenden, moet deze zijn voldaan en gefactureerd. Momenteel, kunt u SSA voor aanbevelingen en schip van één of meerdere bronnen opnieuw uitvoeren, of de aanbevelingen SSA met manueel vastgestelde bronnen en hoeveelheden met voeten treden om verzending te vervullen.

- U wordt aangeraden de SSA opnieuw uit te voeren om de aanbevelingen voor elke verzending te beoordelen.

- Als u de selecties wilt wijzigen, kunt u deze overschrijven met handmatige bronaftrekkingen.

### Overbrengingen en reserveringen

Bij het genereren van de zendingen worden de voorbehouden voor de producten duidelijk en wordt de producthoeveelheid afgetrokken. De hoeveelheid per voorraad wordt bijgewerkt op basis van de verzendingsgegevens. Als u bijvoorbeeld zendingen verzendt voor tien producten uit twee bronnen, brengen de hoeveelheden voor die bronnen elk 10 in mindering. De verkoopbare hoeveelheid wordt automatisch vernieuwd voor de bijbehorende voorraden, zodat klanten en personeel de meest recente productbedragen krijgen. En de bedenkingen zijn volkomen duidelijk, en tellen niet langer mee voor de salarishoeveelheid.
