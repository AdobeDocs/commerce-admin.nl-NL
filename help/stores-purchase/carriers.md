---
title: Setup van transportbedrijf
description: Meer weten over de ondersteuning voor commerciële verzendaccounts die beschikbaar is voor je winkel?
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Setup van transportbedrijf

Als u een commerciële account hebt bij een ondersteunde provider, kunt u uw klanten het gemak bieden om die provider te kiezen tijdens het afrekenen. De tarieven worden automatisch gedownload, zodat te hoeven u niet omhoog de informatie te kijken.

>[!NOTE]
>
>Zie [ Commerce Marketplace ](../getting-started/commerce-marketplace.md) voor de extra verzendende diensten voor uw installatie van Commerce.

Voordat u uw klanten een selectie van verzendingsdragers kunt aanbieden, moet u de volgende stappen uitvoeren:

- Vorm de [ verschepende montages ](shipping-settings.md) om het punt van oorsprong voor uw opslag te vestigen.

- Vorm de montages voor elke dragerdienst die u wilt aanbieden.

   - [**UPS**](ups.md) - de Dienst van het Verenigde Pakket (UPS) biedt binnenlandse en internationale scheepvaartdiensten door land en lucht aan meer dan 220 landen aan.
   - [**USPS**](usps.md) - de Postdienst van de Verenigde Staten (USPS) is de onafhankelijke postdienst van de overheid van de Verenigde Staten. USPS biedt binnenlandse en internationale scheepvaartdiensten over land en door de lucht aan.
   - [**FedEx**](fedex.md) - FedEx biedt binnenlandse en internationale scheepvaartdiensten door land en lucht aan meer dan 220 landen aan.
   - [**DHL**](dhl.md) - DHL biedt de geïntegreerde internationale diensten en op maat gemaakte, klant-geconcentreerde oplossingen voor het beheren van en het vervoeren van brieven, goederen, en informatie aan.

## Afmetingen

Maatgewicht, soms ook wel volumetrisch gewicht genoemd, is een gangbare industriële praktijk die de vervoerprijs baseert op een combinatie van gewicht en verpakkingsvolume. Eenvoudig gezegd bepaalt het maatgewicht de verzendsnelheid op basis van de hoeveelheid ruimte die een pakket inneemt in het laadruimte van de vervoerder. Gewoonlijk wordt een maatgewicht gebruikt wanneer een verpakking relatief licht is in vergelijking met het volume.

Alle grote vervoerders passen maatgewicht toe op bepaalde ladingen. De manier waarop de dimensionale gewichtsprijsbepaling wordt toegepast, verschilt echter per vervoerder. Als uw bedrijf een groot aantal verzendingen heeft, kan zelfs een klein verschil in de verzendprijs in de loop van een jaar tot duizenden dollars leiden.

## Configuratie

De configuratieopties variëren voor elke drager. Voor alle onderdelen zijn echter de volgende stappen vereist:

1. Open een verzendaccount bij de vervoerder.

1. Voer uw accountnummer of gebruikersnaam en de gateway-URL naar het systeem in in de configuratie van uw winkel.

### Veroudering van USPS Web Tools API

Adobe Commerce-versies 2.4.6, 2.4.7 en 2.4.8 gebruiken de API&#39;s van de oude webgereedschappen voor out-of-the-box verzendintegratie met USPS. USPS heeft USPS API&#39;s geïntroduceerd, een op REST gebaseerd platform dat de verouderde API&#39;s voor webgereedschappen vervangt.

Op 25 januari 2026 worden de API&#39;s voor verouderde webgereedschappen door USPS ingetrokken. Na deze datum, zullen alle verzoeken aan de Hulpmiddelen APIs van het Web ontbreken.

Om verstoring van de verzendservices van USPS te voorkomen, voert u de volgende acties uit vóór 25 januari 2026:

- Pas het [ REST API van de Migratiekwaliteitspatch van de MACHT van USPS ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/usps-rest-api-migration-patch.html) (AC-1520) toe om steun voor het integreren met USPS REST APIs toe te voegen.

- Werk de Commerce USPS-configuratie bij om de REST API&#39;s te gebruiken:

   - [Configuratie van USPS Shipping Carrier](usps.md)

   - [Configuratie verzendlabel](shipping-label-create.md)

