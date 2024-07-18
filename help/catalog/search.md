---
title: Overzicht van zoeken in catalogus
description: Meer informatie over de gereedschappen Snel zoeken en Geavanceerd zoeken die klanten kunnen gebruiken om producten op de winkel te zoeken.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 65d295694e13be2e0a0de29b8b396faa9f2c9cd4
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Overzicht van zoeken in catalogus

>[!TIP]
>
>[[!DNL Live Search] ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) levert een snelle, super-relevante, en intuïtieve onderzoekservaring en is beschikbaar voor Adobe Commerce zonder extra kosten. In deze sectie wordt de standaardzoekfunctionaliteit beschreven die kan verschillen van [!DNL Live Search] .

Uit onderzoek blijkt dat mensen die zoeken, meer geneigd zijn om een aankoop te doen dan klanten die alleen op navigatie vertrouwen. Volgens sommige studies zijn mensen die zoeken bijna twee keer zo vaak geneigd om een aankoop te doen.

In de volgende secties worden de basismogelijkheden voor het zoeken naar catalogi beschreven. Zie voor informatie over het configureren en aanpassen van de zoekmogelijkheden voor de native catalogus:

- [Cataloguszoekopdracht configureren](search-configuration.md)
- [Zoekresultaten](search-results.md)
- [Zoektermen beheren](search-terms.md)

>[!NOTE]
>
>De native zoekfunctie in Commerce biedt exacte zoekresultaten die overeenkomen. Hoewel [!DNL Live Search] een optionele module die beschikbaar is voor installatie en activering in Adobe Commerce anders wordt geïmplementeerd en het resultaat niet beperkt is tot de exacte zoekreeks. Bijvoorbeeld, waar u tien producten numeriek voor _Omega_ geëtiketteerd hebt: Een onderzoek naar `Omega 1` resultaten in één enkele gelijke voor _Omega 1_ met het inheemse onderzoeksvermogen. Maar het zelfde onderzoekskoord dat door Levend Onderzoek wordt aangedreven resulteert in een gelijke voor veelvoudige punten, _Omega 1_ en _Omega 10_.

## Snel zoeken

>[!NOTE]
>
>Wanneer [[!DNL Live Search] ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) wordt geïnstalleerd en [[!DNL Storefront Popover] ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/storefront-popover) widget wordt toegelaten, keert het onderzoeksvakje &quot;onderzoek terug aangezien u&quot;resultaten in een pop over typt.

Met het zoekvak in de koptekst van de winkel kunnen bezoekers producten zoeken in uw catalogus. De zoektekst kan de volledige of gedeeltelijke productnaam of een ander woord of zinsdeel zijn dat het product beschrijft. De zoektermen die mensen gebruiken om producten te zoeken, kunnen worden beheerd via de beheerder.

1. Voor **[!UICONTROL Search]** voert de klant de eerste paar letters in van wat hij of zij wil zoeken.

   Alle overeenkomsten in de catalogus worden hieronder weergegeven, met het aantal gevonden resultaten.

1. De klant drukt op Enter of klikt op een resultaat in de lijst met overeenkomende producten.

   ![ Onderzoek ](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Geavanceerd zoeken

>[!NOTE]
>
>De hier beschreven geavanceerde functionaliteit voor het zoeken van formulieren is niet van toepassing op [[!DNL Live Search] ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) .

Met Geavanceerd zoeken kunnen kopers de catalogus doorzoeken op basis van waarden die in een formulier zijn ingevoerd. Omdat het formulier meerdere velden bevat, kan één zoekopdracht verschillende parameters bevatten. Het resultaat is een lijst van alle producten in de catalogus die aan de criteria voldoen. Een koppeling naar Geavanceerd zoeken vindt u in de voettekst van uw winkel.

![ Geavanceerd Onderzoek ](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Elk veld in het formulier komt overeen met een kenmerk uit de productcatalogus. Als u een veld wilt toevoegen, stelt u de eigenschappen frontend van het kenmerk in op `Include in Advanced Search` . Als beste praktijken, omvat slechts de gebieden die de klanten het meest waarschijnlijk om een product te vinden zullen gebruiken, omdat het hebben van teveel vertraagt het onderzoek.

1. In de voettekst van de winkel klikt de klant op **[!UICONTROL Advanced Search]** .

1. In de _Geavanceerde vorm van het Onderzoek_, voegt volledige of gedeeltelijke waarden op zo vele gebieden zonodig toe.

1. Klik op **[!UICONTROL Search]** om de resultaten weer te geven.

   ![ Resultaten van het Onderzoek ](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Als de klant niet ziet wat hij of zij zoekt in de zoekresultaten, klikt de klant op **[!UICONTROL Modify your search]** en probeert hij of zij een andere combinatie van criteria.
