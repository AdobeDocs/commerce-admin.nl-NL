---
title: Regels inzake catalogusprijzen
description: Meer informatie over de prijsregels voor catalogi die kunnen worden gebruikt om producten aan kopers aan te bieden tegen een verlaagde prijs op basis van een aantal gedefinieerde voorwaarden.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Regels inzake catalogusprijzen

De catalogusprijsregels kunnen worden gebruikt om producten tegen een verlaagde prijs aan kopers aan te bieden, op basis van een aantal gedefinieerde voorwaarden. De catalogusprijsregels worden niet gebruikt [couponcodes](price-rules-cart-coupon.md), omdat ze worden geactiveerd voordat een product in de winkelwagentje wordt geplaatst.

U kunt bijvoorbeeld de voorwaarden definiëren en instellen voor een prijsregel waarbij producten automatisch worden weergegeven met een speciale prijs of een speciale promotieprijs. De bepaalde regeleigenschappen zouden klantengroepen, productcategorieën, een kortingsbedrag of een percentage, productkleur, productgrootte, of enkel over om het even welk productattribuut kunnen omvatten opstelling in uw opslag. U kunt begin- en einddatums instellen voor een prijsregel die automatisch een aanbieding start en stopt op de datums die u in de regel definieert. De eigenschappen van een opgeslagen regel kunnen zo nodig worden bijgewerkt of gewijzigd.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) U kunt een gedefinieerde regel ook koppelen aan een [dynamisch blok](../content-design/dynamic-blocks.md) om het evenement of het product in uw winkel te helpen promoten.

- ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Voor terugkerende aanbiedingen kunt u handmatig een opgeslagen regel instellen op _Actief_ of _Inactief_ status iedere keer dat je de speciale actie wilt uitvoeren.

## Regels voor catalogusprijzen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Regels inzake catalogusprijzen](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Eigenschappen voor een regel bijwerken:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Klik op **[!UICONTROL Edit]** om de _Regelinformatie_ pagina.

   - ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Klik op de regel in de lijst om de pagina Regelgegevens weer te geven.

   Hier kunt u de instellingen voor de regel wijzigen (vergelijkbaar met [regel maken](price-rules-catalog-create.md)).

## Filteropties

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Voer tekst in om de lijst voor een specifiek regel-id-nummer te filteren. |
| [!UICONTROL Rule] | Voer tekst in om de lijst te filteren op basis van de regelnaam die is gedefinieerd toen de regel werd gemaakt. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Typ tekst in dit veld om de lijst te filteren op basis van de prioriteit die voor een regel is gedefinieerd. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Gebruik deze optie om de lijst te filteren op basis van websites die voor een regel zijn gedefinieerd. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Klik op **[!UICONTROL Edit]** om de Informatie van de Regel te tonen en de regelmontages bij te werken (gelijkend op het creëren van een regel). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Gebruik de dynamische kalendervelden (Aan: en Van:) om de lijst te filteren op basis van de begindatum voor de regel zoals die is gedefinieerd toen de regel werd gemaakt. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Gebruik de dynamische kalendervelden (Aan: en Van:) om de lijst te filteren op basis van de einddatum voor de regel zoals die is gedefinieerd toen de regel werd gemaakt. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Gebruik deze optie om de lijst te filteren op basis van de regelstatus (`Active` of `Inactive`). |

{style="table-layout:auto"}

## Bronnen voor probleemoplossing

Raadpleeg de volgende artikelen in de Knowledge Base van Commerce Support voor hulp bij het oplossen van problemen met catalogusprijsregels:

- [404 Fout op winkelfront zodra de update van de catalogusprijsregelschema&#39;s is uitgevoerd](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [Verbeterde prestaties van de productpagina met verwante producten en doelregels](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [Catalogusprijsregels werken niet](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [Berekening van GraphQL-prijzen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
