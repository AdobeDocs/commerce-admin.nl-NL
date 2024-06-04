---
title: Inleiding tot [!DNL Adobe Commerce B2B]
description: Leer hoe u geïntegreerde B2B-functies kunt gebruiken voor wat u nodig hebt bij klanten die bedrijven zijn.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: 8e4e070f41f7d3bf872e81c9805e7c24779b812d
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 2%

---

# Inleiding tot [!DNL Adobe Commerce B2B]

In tegenstelling tot het standaard business-to-consumer model zijn geïntegreerde B2B-functies (Business to Business) ontworpen om te voldoen aan de behoeften van verkopers (Adobe Commerce-verkopers) die klanten hebben die bedrijven zijn. Het past bedrijven met complexe organisatorische structuren en veelvoudige gebruikers met diverse rollen en niveaus van koopvergunning aan. Een doorsnee B2B-klant kan de beheerder van een detailhandelswinkel zijn, of een koper die namens een bedrijf aankopen doet. In beide gevallen vindt de transactie plaats tussen uw bedrijf en hun bedrijf. Je kunt producten ook direct aan de consument verkopen. [!DNL Adobe Commerce B2B] is een geïntegreerde oplossing die zowel B2B- als B2C-modellen ondersteunt.

Met de [installatie](install.md) en [inschakelen](enable-basic-features.md) van de B2B-extensie in uw Adobe Commerce-winkel, kunt u uw aankopen aanpassen aan klantspecifieke catalogi en prijzen en aan doelgerichte inhoud en promoties.

## Bedrijfsrekeningen

De bedrijfsrekeningcomponent is een belangrijke entiteit binnen B2B waarvan alle andere kenmerken op een of andere manier afhankelijk zijn. Het maakt het mogelijk om meerdere kopers die deel uitmaken van één enkel bedrijf, tot één enkel bedrijfsaccount (of bedrijfsaccount) aan te sluiten. De bedrijfbeheerder kan een bedrijfsstructuur (afdelingen, onderverdelingen, en gebruikers) bouwen die op het operationele model voor het bedrijf wijst en verschillende gebruikersrollen en toestemmingen voor bedrijfsleden verstrekt. Deze structuur staat de bedrijfbeheerder toe om gebruikersactiviteit voor de bedrijfrekening te controleren: het opdracht geven, het citeren, het kopen, toegang tot de informatie of het profiel van het bedrijfskrediet, etc.

Vanuit de beheerder kan de Commerce-sitebeheerder configureren hoe het bedrijf op de website werkt. De configuratie bepaalt de B2B mogelijkheden beschikbaar voor bedrijfgebruikers, met inbegrip van betalingsmethodes, prijsniveaus, de capaciteit om prijzen te bespreken gebruikend noteringen, de capaciteit om vraaglijsten te creëren, en meer.

Zie voor meer informatie [Bedrijfsrekeningen](account-companies.md).

>[!NOTE]
>
>Als deze optie is ingeschakeld, kunnen bedrijven in uw winkel de optie krijgen om _Betalen op account_, hetgeen betekent dat aankopen op een kredietlijn van een onderneming worden verricht. Als handelaar, kunt u krediet voor een ondernemingsrekening toewijzen en kredietmontages voor een bedrijf, en kredietterugbetaling beheren.

## Bedrijfsbeheer

[!BADGE 1.5.0-bèta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"}

Bedrijfsbeheer helpt zakelijke beheerders het beheer en beheer van B2B-organisaties met complexe operationele modellen te stroomlijnen.

Vanuit de beheerder kunnen gebruikers met de juiste machtigingen een **[!UICONTROL Company Hierarchy]** dit weerspiegelt de organisatiestructuur van een onderneming die uit meerdere ondernemingen bestaat. Deze hiërarchie staat hen toe om bedrijven als groep te bekijken en te beheren. De beheerder kan bijvoorbeeld een moedermaatschappij aanwijzen en alle ondernemingen toewijzen die als dochterondernemingen van de moedermaatschappij opereren. Dan, kan de beheerder van het moederbedrijf bedrijfrekeningen voor alle toegewezen bedrijven bekijken en beheren.

Zie voor meer informatie [Bedrijfsbeheer](manage-companies.md).

## Services voor Adobe Commerce

Services voor Adobe Commerce zijn gehoste services die Adobe Commerce en Magento Open Source uitgebreide mogelijkheden bieden. De diensten die B2B werkstromen steunen zijn:

* [Catalogusservice](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Live zoeken](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Product Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Gedeelde catalogi

Gedeelde catalogi zijn de prijsniveaus waarmee aangepaste prijzen per product voor verschillende bedrijven op een of meerdere websites kunnen worden ingesteld. Door gedeelde catalogi te gebruiken, kunt u producten verkopen door verschillende prijsniveaus voor verschillende klantengroepen toe te passen. De steun voor Gedeelde catalogi is beschikbaar slechts voor de opslag van Commerce die wordt gevormd om de rekeningen van het Bedrijf te steunen.

Zie voor meer informatie [Werken met gedeelde catalogi](catalog-shared.md).

## Snelle bestelling

Vorm Snelle Orde om het ordeproces tot verscheidene kliks voor het programma geopende klanten te verminderen wanneer zij de productnaam of SKU van de producten kennen die zij willen hebben opdracht geven tot.

Zie voor meer informatie [Snelle bestellingen](quick-order.md).

## Onderhandelbare aanhalingstekens

Met de functie Aanhalingstekens kunt u prijsonderhandelingen starten tussen koper en verkoper van een bedrijf.

* Een geautoriseerde koper kan een prijsopgave op het winkelwagentje doen.

* Een verkoper kan een prijsopgave voor een koper starten vanuit Admin.

Kopers en verkopers gebruiken het citaat om onderhandelingsproces-zoals het toevoegen van punten, het bijwerken van hoeveelheden, het verzoeken en het toepassen van kortingen-tot zij een overeenkomst bereiken te leiden. De _Aanhalingen_ Het raster in de Admin geeft een overzicht van elke ontvangen offerte en houdt een geschiedenis bij van de communicatie tussen koper en verkoper.

De steun voor Negotiable Citaten is beschikbaar slechts voor de opslag van Commerce die wordt gevormd om de rekeningen van het Bedrijf te steunen.

Zie voor meer informatie [Onderhandelbare aanhalingstekens](quotes.md).

## Goedkeuring van inkooporders

Wanneer inkooporders voor een bedrijfsaccount worden geactiveerd, worden alle orders automatisch als inkooporders (inkooporder) gemaakt. De gebruikers van het bedrijf met de vereiste toestemmingen kunnen tot stand brengen, uitgeven en POs schrappen die zij creëren en POs die door ondergeschikte gebruikers worden gecreeerd. Afhankelijk van hun rol, en de orde, zouden de bedrijfgebruikers aan verscheidene goedkeuringsregels kunnen worden onderworpen.

Zie voor meer informatie [Aankooporders voor bedrijven](purchase-order-flow.md).

## Aanvraaglijsten

Klanten kunnen de aanvraaglijst gebruiken om tijd te besparen bij het aanschaffen van vaak bestelde producten, omdat ze artikelen rechtstreeks vanuit de lijst aan het winkelwagentje kunnen toevoegen. Ze kunnen meerdere lijsten bijhouden die zich richten op producten van verschillende leveranciers, kopers, teams, campagnes of iets anders dat hun workflow stroomlijnt.

Zie voor meer informatie [Aanvraaglijsten](requisition-lists.md).
