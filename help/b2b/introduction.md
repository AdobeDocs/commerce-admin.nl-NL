---
title: Inleiding tot  [!DNL Adobe Commerce B2B]
description: Leer hoe u geïntegreerde B2B-functies kunt gebruiken voor wat u nodig hebt bij klanten die bedrijven zijn.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: c3a54d4574ec6aaf580d97563165c63c55711f15
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 2%

---

# Inleiding tot [!DNL Adobe Commerce B2B]

In tegenstelling tot het standaard business-to-consumer model zijn geïntegreerde B2B-functies (Business to Business) ontworpen om te voldoen aan de behoeften van verkopers (Adobe Commerce-verkopers) die klanten hebben die bedrijven zijn. Het past bedrijven met complexe organisatorische structuren en veelvoudige gebruikers met diverse rollen en niveaus van koopvergunning aan. Een doorsnee B2B-klant kan de beheerder van een detailhandelswinkel zijn, of een koper die namens een bedrijf aankopen doet. In beide gevallen vindt de transactie plaats tussen uw bedrijf en hun bedrijf. Je kunt producten ook direct aan de consument verkopen. [!DNL Adobe Commerce B2B] is een geïntegreerde oplossing die zowel B2B als B2C modellen steunt.

Met de [ installatie ](install.md) en [ enablement ](enable-basic-features.md) van de B2B uitbreiding in uw opslag van Adobe Commerce, kan de het kopen ervaring met klant-specifieke catalogi en tarifering, en gerichte inhoud en bevorderingen worden gepersonaliseerd.

## Bedrijfsrekeningen

De bedrijfsaccountcomponent is een belangrijke entiteit binnen B2B, waarvan alle andere functies in zekere zin afhankelijk zijn. Hiermee kunt u meerdere kopers die binnen één bedrijf horen, samenvoegen tot één bedrijfsaccount (of bedrijfsaccount). De bedrijfsbeheerder kan een bedrijfsstructuur (afdelingen, onderverdelingen en gebruikers) bouwen die het operationele model voor het bedrijf weerspiegelt en verschillende gebruikersrollen en toestemmingen voor bedrijfsleden verstrekt. Met deze structuur kan de bedrijfsbeheerder de gebruikersactiviteiten voor het bedrijfsaccount beheren: bestellen, citeren, aanschaffen, toegang tot bedrijfskredietinformatie of -profiel, enzovoort.

Vanuit de beheerder kan de Commerce-sitebeheerder configureren hoe het bedrijf op de website werkt. De configuratie bepaalt de B2B mogelijkheden beschikbaar voor bedrijfgebruikers, met inbegrip van betalingsmethodes, prijsniveaus, de capaciteit om prijzen te bespreken gebruikend noteringen, de capaciteit om vraaglijsten te creëren, en meer.

Voor meer informatie, zie [ Rekeningen van het Bedrijf ](account-companies.md).

>[!NOTE]
>
>Wanneer toegelaten, kan uw opslag bedrijven de optie aan _betalen op Rekening_ geven, wat betekent om aankopen op een lijn van het bedrijfkrediet te maken. Als verkoper kunt u krediet toewijzen aan een bedrijfsaccount en de kredietinstellingen voor een bedrijf en de terugbetaling van tegoeden beheren.

## Bedrijfsbeheer

Bedrijfsbeheer helpt zakelijke beheerders om het beheer en beheer van B2B-organisaties met complexe operationele modellen te stroomlijnen.

Vanuit de beheerder kunnen gebruikers met de juiste machtigingen een **[!UICONTROL Company Hierarchy]** maken die de organisatiestructuur weerspiegelt van een onderneming die uit meerdere bedrijven bestaat. Met deze hiërarchie kunnen ze bedrijven als een groep bekijken en beheren. De beheerder kan bijvoorbeeld een moedermaatschappij aanwijzen en alle ondernemingen toewijzen die als dochterondernemingen van de moedermaatschappij opereren. Dan, kan de beheerder van het moederbedrijf bedrijfrekeningen voor alle toegewezen bedrijven bekijken en beheren.

Voor meer informatie, zie [ Beheer van het Bedrijf ](manage-companies.md).

## Services voor Adobe Commerce

Services voor Adobe Commerce zijn gehoste services die Adobe Commerce en Magento Open Source uitgebreide mogelijkheden bieden. De diensten die B2B werkstromen steunen zijn:

* [ de Dienst van de Catalogus ](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [ Levend Onderzoek ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [ Product Recommendations ](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Gedeelde catalogi

Gedeelde catalogi zijn de prijsniveaus waarmee aangepaste prijzen per product voor verschillende bedrijven op een of meerdere websites kunnen worden ingesteld. Door gedeelde catalogi te gebruiken, kunt u producten verkopen door verschillende prijsniveaus voor verschillende klantengroepen toe te passen. De steun voor Gedeelde catalogi is beschikbaar slechts voor de opslag van Commerce die wordt gevormd om de rekeningen van het Bedrijf te steunen.

Voor meer informatie, zie [ Werken met Gedeelde Catalogi ](catalog-shared.md).

## Snelle volgorde

Vorm Snelle Orde om het ordeproces tot verscheidene kliks voor het programma geopende klanten te verminderen wanneer zij de productnaam of SKU van de producten kennen die zij willen hebben opdracht geven tot.

Voor meer informatie, zie [ Snelle Orden ](quick-order.md).

## Onderhandelbare aanhalingstekens

Met de functie Aanhalingstekens kunt u prijsonderhandelingen starten tussen koper en verkoper van een bedrijf.

* Een geautoriseerde koper kan een offerte uit het winkelwagentje initiëren.

* Een verkoper kan een offerte voor een koper initiëren vanuit de beheerder.

Kopers en verkopers gebruiken de offerte om het onderhandelingsproces te beheren, zoals items toevoegen, hoeveelheden bijwerken, kortingen aanvragen en toepassen, totdat ze een overeenkomst bereiken. Het _citaten_ net in Admin maakt een lijst van elk ontvangen citaat, en handhaaft een geschiedenis van de communicatie tussen koper en verkoper.

Ondersteuning voor onderhandelbare offertes is alleen beschikbaar voor Commerce-winkels die zijn geconfigureerd om bedrijfsaccounts te ondersteunen.

Voor meer informatie, zie [ Negotiable Citaten ](quotes.md).

## Goedkeuring van inkooporders

Wanneer inkooporders voor een bedrijfsaccount worden geactiveerd, worden alle orders automatisch als inkooporders (inkooporder) gemaakt. De gebruikers van het bedrijf met de vereiste toestemmingen kunnen tot stand brengen, uitgeven en POs schrappen die zij creëren en POs die door ondergeschikte gebruikers worden gecreeerd. Afhankelijk van hun rol, en de orde, zouden de bedrijfgebruikers aan verscheidene goedkeuringsregels kunnen worden onderworpen.

Voor meer informatie, zie [ Orders van de Koop voor Bedrijven ](purchase-order-flow.md).

## Aanvraaglijsten

Klanten kunnen de aanvraaglijst gebruiken om tijd te besparen bij het aanschaffen van vaak bestelde producten, omdat ze artikelen rechtstreeks vanuit de lijst aan het winkelwagentje kunnen toevoegen. Ze kunnen meerdere lijsten bijhouden die zich richten op producten van verschillende leveranciers, kopers, teams, campagnes of andere producten die hun workflow stroomlijnen.

Voor meer informatie, zie [ Lijsten van de Vereiste ](requisition-lists.md).
