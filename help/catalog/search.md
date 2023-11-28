---
title: Overzicht van zoeken in catalogus
description: Meer informatie over de gereedschappen Snel zoeken en Geavanceerd zoeken die klanten kunnen gebruiken om producten op de winkel te zoeken.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Overzicht van zoeken in catalogus

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) biedt een snelle, superrelevante en intuïtieve zoekervaring en is gratis beschikbaar voor Adobe Commerce. In deze sectie wordt de standaardzoekfunctionaliteit beschreven die afwijkt van [!DNL Live Search].

Uit onderzoek blijkt dat mensen die zoeken, meer geneigd zijn om een aankoop te doen dan klanten die alleen op navigatie vertrouwen. Volgens sommige studies zijn mensen die zoeken bijna twee keer zo vaak geneigd om een aankoop te doen.

In de volgende secties worden de basismogelijkheden voor het zoeken naar catalogi beschreven. Zie voor informatie over het configureren en aanpassen van de zoekmogelijkheden voor de native catalogus:

- [Cataloguszoekopdracht configureren](search-configuration.md)
- [Zoekresultaten](search-results.md)
- [Zoektermen beheren](search-terms.md)

>[!NOTE]
>
>De native zoekfunctionaliteit in Commerce biedt exact overeenkomende zoekresultaten. while [!DNL Live Search], wordt een optionele module die beschikbaar is voor installatie en activering in Adobe Commerce anders geïmplementeerd en het resultaat is niet beperkt tot de exacte zoekreeks. Als u bijvoorbeeld tien producten numeriek hebt gelabeld voor _Omega_: Een zoekopdracht naar `Omega 1` resulteert in één enkele gelijke voor _Omega 1_ met de native zoekfunctie. Maar dezelfde zoekreeks die wordt aangedreven door Live zoeken, resulteert in een overeenkomst voor meerdere items. _Omega 1_ en _Omega 10_.

## Snel zoeken

>[!NOTE]
>
>Wanneer [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) is geïnstalleerd, retourneert het zoekvak &quot;zoeken terwijl u typt&quot; resultaten in een pop-up.

Met het zoekvak in de koptekst van de winkel kunnen bezoekers producten zoeken in uw catalogus. De zoektekst kan de volledige of gedeeltelijke productnaam of een ander woord of zinsdeel zijn dat het product beschrijft. De zoektermen die mensen gebruiken om producten te zoeken, kunnen worden beheerd via de beheerder.

1. Voor **[!UICONTROL Search]**, voert de klant de eerste paar letters in van wat hij of zij wil zoeken.

   Alle overeenkomsten in de catalogus worden hieronder weergegeven, met het aantal gevonden resultaten.

1. De klant drukt op Enter of klikt op een resultaat in de lijst met overeenkomende producten.

   ![Zoeken](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Geavanceerd zoeken

>[!NOTE]
>
>De hier beschreven functionaliteit voor geavanceerd zoeken in formulieren is niet van toepassing op [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Met Geavanceerd zoeken kunnen kopers de catalogus doorzoeken op basis van waarden die in een formulier zijn ingevoerd. Omdat het formulier meerdere velden bevat, kan één zoekopdracht verschillende parameters bevatten. Het resultaat is een lijst van alle producten in de catalogus die aan de criteria voldoen. Een koppeling naar Geavanceerd zoeken vindt u in de voettekst van uw winkel.

![Geavanceerd zoeken](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Elk veld in het formulier komt overeen met een kenmerk uit de productcatalogus. Als u een veld wilt toevoegen, stelt u de eigenschappen frontend van het kenmerk in op `Include in Advanced Search`. Als beste praktijken, omvat slechts de gebieden die de klanten het meest waarschijnlijk om een product te vinden zullen gebruiken, omdat het hebben van teveel vertraagt het onderzoek.

1. In de voettekst van de winkel klikt de klant **[!UICONTROL Advanced Search]**.

1. In de _Geavanceerd zoeken_ voegt volledige of gedeeltelijke waarden toe in zoveel velden als nodig zijn.

1. Klikken **[!UICONTROL Search]** om de resultaten weer te geven.

   ![Zoekresultaten](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Als ze niet zien wat ze zoeken in de zoekresultaten, klikt de klant **[!UICONTROL Modify your search]** en probeert een andere combinatie van criteria.
