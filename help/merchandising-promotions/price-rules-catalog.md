---
title: Regels inzake catalogusprijzen
description: Meer informatie over de prijsregels voor catalogi die kunnen worden gebruikt om producten aan kopers aan te bieden tegen een verlaagde prijs op basis van een aantal gedefinieerde voorwaarden.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Regels inzake catalogusprijzen

De catalogusprijsregels kunnen worden gebruikt om producten tegen een verlaagde prijs aan kopers aan te bieden, op basis van een aantal gedefinieerde voorwaarden. De de prijsregels van de catalogus gebruiken niet [ couponcodes ](price-rules-cart-coupon.md), omdat zij worden teweeggebracht alvorens een product in het winkelwagentje wordt geplaatst.

U kunt bijvoorbeeld de voorwaarden definiëren en instellen voor een prijsregel waarbij producten automatisch worden weergegeven met een speciale prijs of een speciale promotieprijs. De bepaalde regeleigenschappen zouden klantengroepen, productcategorieën, een kortingsbedrag of een percentage, productkleur, productgrootte, of enkel over om het even welk productattribuut kunnen omvatten opstelling in uw opslag. U kunt begin- en einddatums instellen voor een prijsregel die automatisch een aanbieding start en stopt op de datums die u in de regel definieert. De eigenschappen van een opgeslagen regel kunnen zo nodig worden bijgewerkt of gewijzigd.

- ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) U kunt een bepaalde regel aan a [ dynamisch blok ](../content-design/dynamic-blocks.md) ook verbinden helpen de gebeurtenis of het product in uw opslag bevorderen.

- ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) voor terugkomende bevorderingen, kunt u een bewaarde regel aan _Actieve_ of _Inactieve_ status manueel plaatsen telkens als u de bevordering wilt in werking stellen.

## Regels voor catalogusprijzen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![ de prijsregels van de Catalogus ](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Eigenschappen voor een regel bijwerken:

   - ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) klik **[!UICONTROL Edit]** om de _pagina van de Informatie van de Regel_ te tonen.

   - ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) klik de regel in de lijst om de pagina van de Informatie van de Regel te tonen.

   Daar kunt u de montages voor de regel (gelijkend op [ veranderen creërend een regel ](price-rules-catalog-create.md)).

## Filteropties

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Voer tekst in om de lijst voor een specifiek regel-id-nummer te filteren. |
| [!UICONTROL Rule] | Voer tekst in om de lijst te filteren op basis van de regelnaam die is gedefinieerd toen de regel werd gemaakt. |
| [!UICONTROL Priority] | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) gaat tekst op dit gebied in om de lijst te filtreren die op de prioriteit wordt gebaseerd die voor een regel wordt bepaald. |
| [!UICONTROL Web Site] | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Gebruik deze optie om de lijst te filtreren die op websites wordt gebaseerd die voor een regel worden bepaald. |
| [!UICONTROL Action] | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) klik **[!UICONTROL Edit]** om de Informatie van de Regel te tonen en de regelmontages (gelijkend op het creëren van een regel) bij te werken. |
| [!UICONTROL Start] | ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) Gebruik de dynamische kalendergebieden (aan: en van:) om de lijst te filtreren die op de begindatum voor de regel wordt gebaseerd zoals die werd bepaald toen de regel werd gecreeerd. |
| [!UICONTROL End] | ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) Gebruik de dynamische kalendergebieden (aan: en van:) om de lijst te filtreren die op de einddatum voor de regel wordt gebaseerd zoals die toen de regel werd gecreeerd. |
| [!UICONTROL Status] | ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) Gebruik deze optie om de lijst te filtreren die op regelstatus (`Active` of `Inactive` wordt gebaseerd). |

{style="table-layout:auto"}

## Bronnen voor probleemoplossing

Raadpleeg de volgende artikelen in de Commerce Support Knowledge Base voor hulp bij het oplossen van problemen met catalogusprijsregels:

- [ 404 Fout op archiefvoorzijde zodra de update van de de regelschema&#39;s van de catalogusprijs wordt uitgevoerd ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [ Verbeterde prestaties van productpagina met verwante producten en doelregels ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [ de prijsregels van de Catalogus werken niet ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [ de prijsberekeningen van GraphQL ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
