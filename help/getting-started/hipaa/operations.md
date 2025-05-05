---
title: Bewerkingen
description: Richtlijnen voor het migreren naar een HIPAA-klaar aanbieden en het gebruiken van de secundaire het opvoeren omgeving voor het oplossen van problemen.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Bewerkingen

Gebruik deze richtlijnen voor meer informatie over migreren naar het HIPAA-aanbod voor Adobe Commerce en het gebruik van de `staging_for_support` -omgeving voor probleemoplossing.

## Migratie

Klanten die migreren van een niet-HIPAA Commerce-aanbod naar een HIPAA-klaar aanbod, moeten zich aan de volgende richtlijnen houden:

1. **Schrap bestaande dataspaces**: Vóór migratie, moeten alle bestaande dataspaces worden geschrapt om het samenvoegen van gevoelige en niet-gevoelige gegevens in de laag van Adobe Commerce te verhinderen SaaS. Creeer een steunkaartje om uw gegevensgebieden te schrappen.
1. **vorm nieuw milieu**: De [ 3&rbrace; opstelling van de Schakelaar van de Diensten van Commerce &lbrace;in de nieuwe instantie van HIPAA Commerce zou moeten worden gevormd slechts nadat de dataspaces zijn geschrapt. ](https://experienceleague.adobe.com/nl/docs/commerce/user-guides/integration-services/saas) Het nieuwe milieu van HIPAA SaaS zou slechts moeten worden gebruikt nadat de oude dataspaces worden geschrapt. De opstelling van de Schakelaar van de Diensten van Commerce brengt automatisch de verwezenlijking van nieuwe dataspaces SaaS in werking.
1. **de strategie van de Migratie**: De schrapping van de dataspaces SaaS is een onomkeerbaar proces en schrapt elk van uw catalogusgegevens en verwante configuraties. Er moet een migratiestrategie zijn ingesteld als u uw oude gegevens of configuraties wilt doorsturen. Deze strategie valt onder de verantwoordelijkheid van de handelaar. Een steunkaartje voor het schrappen van de bestaande gegevensruimten zou slechts moeten worden gecreeerd nadat de steun van migratiegegevens (indien van toepassing) wordt gedaan.

>[!NOTE]
>Om bestaande dataspaces te schrappen, moeten de klanten een kaartje van de Steun van Adobe Commerce tot stand brengen getiteld &quot;Migratie HIPAA: Schrapping de Datasfrasen van SaaS&quot;, hun `MAGEID` verstrekken, en identiteitskaarts verstrekken van het Project SaaS die moet worden geschrapt.

## Problemen met Adobe Commerce-ondersteuning oplossen

De Adobe Commerce HIPAA-ready-aanbieding wordt geleverd met een extra `staging_for_support` -omgeving die door het Adobe Commerce Support-team moet worden gebruikt voor probleemoplossing.

Klanten moeten ervoor zorgen dat de `staging_for_support` -omgeving:

- Bevat geen gevoelige gegevens, zoals, maar niet beperkt tot, beschermde gezondheidsinformatie (PHI).
- Mag niet worden gebruikt voor productieactiviteiten.
- U mag geen andere naam opgeven dan `staging_for_support` om verwarring te voorkomen.
- Wordt bijgewerkt met zowel code als configuratie van het productiemilieu om ervoor te zorgen dat het oplossen van problemen in een milieu zo dicht mogelijk bij productie wordt uitgevoerd.

## Commerce-services

- **niet-HIPAA Klaar de diensten van Commerce** - de Klanten moeten de geen diensten van Adobe Commerce, zoals Levend Onderzoek, de Aanbevelingen van het Product, de Diensten van de Betaling, de Kanalen van de Verkoop, of Commerce Intelligence gebruiken omdat zij niet HIPAA klaar zijn. De klanten zouden de [ HIPAA-Klaar diensten ](overview.md) slechts moeten gebruiken.

- **Verbinding van Gegevens** - slechts de achter-Office Collector binnen de [ uitbreiding van de Verbinding van Gegevens ](https://experienceleague.adobe.com/nl/docs/commerce/data-connection/overview) is HIPAA klaar. Klanten dienen geen PHI naar gegevensverbindingsservices te verzenden die niet geschikt zijn voor HIPAA, zoals storefront-gebeurtenissen en Audience Activation. Klanten moeten ervoor zorgen dat gegevensverzameling voor de opslagomgeving is uitgeschakeld.

- **de Dienst van de Catalogus** - door ontwerp, [ de Dienst van de Catalogus ](https://experienceleague.adobe.com/nl/docs/commerce/catalog-service/overview) verwerkt geen PHI, zodat is het buiten werkingsgebied voor de controle en naleving van de HIPAA bereidheid. Klanten zijn verantwoordelijk voor het waarborgen dat zij deze service gebruiken op basis van hun eigen beoordeling van gebruiksgevallen en in overleg met juridische adviseurs. De klanten zouden de Dienst van de Catalogus door de gefedereerde dienst ook niet moeten gebruiken om het risico te vermijden om PHI tot de niet-HIPAA klaar diensten over te gaan.

- **Gegevens SaaS de Uitvoer** - de [ dienst van de Uitvoer van Gegevens SaaS ](https://experienceleague.adobe.com/nl/docs/commerce/saas-data-export/overview) zou moeten worden gevormd om gegevens slechts voor HIPAA klaar componenten in Adobe Commerce te verzenden.
