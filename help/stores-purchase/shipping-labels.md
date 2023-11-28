---
title: Verzendlabels
description: Meer informatie over de workflow voor verzendlabels voor normale verzendingen en producten met een retourvergunning voor producten.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Verzendlabels

De handel omvat een hoog niveau van integratie met belangrijke scheepvaartmaatschappijen, die u toegang tot dragerverzendsystemen verleent om orden te volgen, verschepende etiketten te creëren, en meer. Er kunnen verzendlabels worden gemaakt voor regelmatige zendingen en producten met een retourvergunning. Naast de door de scheepvaartmaatschappij verstrekte informatie bevat het etiket ook het ordernummer van de koophandel, het nummer van de verpakking en de totale hoeveelheid colli voor de zending.

![USPS Prioritair verzendlabel](./assets/shipping-usps-priority-label.png){width="300"}

- [Verzendlabels configureren](shipping-label-configure.md)
- [Verzendlabels en -pakketten maken](shipping-label-create.md)

## Workflow voor verzendlabel

Verzendlabels kunnen worden geproduceerd op het moment dat een verzending wordt gemaakt of later. Verzendlabels worden opgeslagen in de indeling PDF en gedownload naar de computer.

### Stap 1: Merchant verzendt aanvraag voor een verzendlabel

De verkoper/de opslagmanager voltooit de informatie noodzakelijk om etiketten te produceren, en legt het verzoek voor.

### Stap 2: Verzoek verzonden aan drager

De handel neemt contact op met de scheepvaartmaatschappij en leidt tot een bestelling in het systeem van de vervoerder. Voor elk verzonden pakket wordt een aparte volgorde gemaakt.

### Stap 3: De vervoerder verstuurt het label en trackingnummer

De vervoerder verstuurt het verzendlabel en trackingnummer voor de zending.

- Bij één verzending met meerdere pakketten worden meerdere verzendlabels ontvangen.

- Als u dezelfde verzendlabels meerdere keren genereert, blijven de oorspronkelijke volgnummers behouden.

- Voor geretourneerde producten met RMA-nummers worden de oude volgnummers vervangen door nieuwe.

### Stap 4: Merchant downloadt en drukt het label af

Nadat het verzendlabel is gegenereerd, wordt de nieuwe verzending opgeslagen en kan het label worden afgedrukt. Als het verzendlabel niet kan worden gemaakt vanwege verbindingsproblemen of om een andere reden, wordt de verzending niet gemaakt. Afhankelijk van de browserinstellingen kan het PDF-bestand worden geopend en afgedrukt. Elk label wordt op een aparte pagina in de PDF weergegeven.
