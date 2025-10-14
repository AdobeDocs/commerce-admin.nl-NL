---
title: Overzicht van productkenmerken
description: Meer informatie over productkenmerken en hoe deze worden gebruikt om specifieke kenmerken van een product te beschrijven.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: e0468763b2314e69e8ee4922da9bb9cf65578904
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Overzicht van productkenmerken

Kenmerken zijn de bouwstenen van uw productcatalogus en beschrijven specifieke kenmerken van een product. De attributen van het product kunnen in [&#x200B; attributenreeksen &#x200B;](attribute-sets.md) worden georganiseerd, die dan als malplaatjes voor het creëren van producten worden gebruikt.

De attributen bepalen het type van inputcontrole dat voor productopties wordt gebruikt, en verstrekken extra informatie voor productpagina&#39;s. Ze worden ook gebruikt als zoekparameters en criteria voor gelaagde navigatie, productvergelijkingsrapporten en promoties. U kunt zoveel kenmerken en kenmerksets maken als nodig zijn om de producten in uw catalogus te beschrijven. Naast de kenmerken die u kunt maken, worden systeemkenmerken, zoals prijs, ingebouwd in het Commerce-kernplatform en kunnen deze niet worden gewijzigd.

![&#x200B; Creërend een nieuw attribuut terwijl het uitgeven van een product &#x200B;](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Gebruik de beste werkwijzen die in de volgende secties worden beschreven wanneer u productkenmerken plant en creeert.

## Kenmerknamen

Stel consistente conventies voor kenmerknaamgeving vast, inclusief lettertype en leestekens. `Color:Green` en `Color:green` kunnen bijvoorbeeld door verschillende systemen worden beschouwd als twee verschillende kenmerkwaarden. Dergelijke lawaai in de gegevens kan bedrijfsregels, onderzoeksresultaten, en gegevensfilters voor toepassingen beïnvloeden die producten aan regels aanpassen.

## Kenmerkgebruik

Bedenk hoe kenmerken moeten worden gebruikt bij het toewijzen van eigenschappen en waarden. Identificeer de kenmerken die worden gebruikt als labels voor presentatie, zoals een productnaam, afbeelding, prijs en beschrijving, en welke kenmerken worden gebruikt voor gegevensinvoer. Bedenk hoe de kenmerken op de verschillende pagina&#39;s op de hele site worden weergegeven en hoe ze op categoriepagina&#39;s, productdetailpagina&#39;s, categorierasters en miniatuurregelaars worden weergegeven.

## Kleur

Ad-hockleurbeschrijvingen kunnen een uitdaging vormen vanuit het oogpunt van databasebewerkingen. Kleurnamen zoals &quot;Azure Skies&quot; of &quot;Robin Egg Blue&quot; hebben een groot beroep, maar retourneren mogelijk niet de beste resultaten als ze als zoekcriteria worden gebruikt, of als u voor handelsdoeleinden `Color_Family:Blue` moet opgeven. Overweeg hoe kleuren worden vertegenwoordigd in zoekresultaten en gelaagde navigatie en stel enkele richtlijnen voor uw bedrijfsbehoeften vast. Zorg vervolgens voor consistentie bij het toewijzen van kleurkenmerkwaarden in de hele catalogus.

## Variatiebeheer

Het product van het gebruik [&#x200B; configuratieopties &#x200B;](product-configurations.md) en [&#x200B; configureerbare producten &#x200B;](product-create-configurable.md) om variaties in uw productdienstenaanbod te beheren. Deze functies maken het gemakkelijker om producten te categoriseren, regels voor de kartprijs en dynamische categorieregels tot stand te brengen, en een selectie van opties met diverse tekst, selectie, en datuminputtypes aan te bieden.

## Gewogen zoekopdracht

De attributen van het product die voor [&#x200B; catalogusonderzoek &#x200B;](search.md) worden toegelaten kunnen een gewicht worden toegewezen om hen een hogere waarde in onderzoeksresultaten te geven. Kenmerken met een groter gewicht worden geretourneerd vóór kenmerken met een lager gewicht. Bijvoorbeeld, overweeg twee attributen in het systeem, _kleur_ met een onderzoeksgewicht van 3 en _beschrijving_ met een onderzoeksgewicht van 1. Een onderzoek naar het woord _rood_ keert een lijst van producten met een waarde van kleurenattributen van `red` terug, maar keert geen producten met beschrijvingen terug die het woord _rood_ bevatten. In dit voorbeeld heeft het kenmerk `color` een grotere gedefinieerde dikte dan het kenmerk `description` .

## Ongebruikte eigenschappen

Verwijder ongebruikte producteigenschappen voor betere structurering en snellere indexering.


>[ NOTA!]
>
>Voor informatie bij het optimaliseren van de configuratie van de productattributen voor prestaties, zie [&#x200B; beste praktijken van het beheer van de Catalogus &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) in _Playbook van de Implementatie_.
