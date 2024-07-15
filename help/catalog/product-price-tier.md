---
title: Tier-prijsstelling
description: Leer hoe u de prijzen op de laag gebruikt om een korting op de hoeveelheid van een productaanbieding of productpagina aan te bieden.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Tier-prijsstelling

Met de prijzen voor Tier kunt u een korting bieden op de hoeveelheid van een productaanbieding of productpagina in de winkel. De korting kan worden toegepast op een specifieke opslagweergave of een klantgroep of gedeelde catalogus.

Als u veel producten hebt om bij te werken, is het het meest efficiënt om de prijsveranderingen van de lijst in plaats van hen individueel in te voeren. Voor meer informatie, zie [ de laagprijzen van de Invoer ](../systems/data-import-price-tier.md).

![ de prijs van de Rij op een storefront productpagina ](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

Op de productpagina wordt de kwantumkorting berekend en wordt een bericht weergegeven, zoals:

`Buy 6 for $5.95 each and save 15%`

De prijzen in de winkel hebben voorrang van de hoogste naar de laagste hoeveelheid. Als u een prijs op de laag hebt voor het aantal `5` en één voor `10` en een klant vijf, zes, zeven, acht of negen items aan het winkelwagentje toevoegt, ontvangt de klant de verlaagde prijs voor de laag voor het aantal `5` . Wanneer de klant het tiende item toevoegt, vervangt de gedisconteerde prijs die voor de kwantiteit `10` is opgegeven de laag voor een hoeveelheid `5` en geldt de gedisconteerde prijs voor `10` .

## Een prijsniveau toevoegen voor een product

1. Open het product in de bewerkingsmodus.

1. Klik onder het veld _[!UICONTROL Price]_op **[!UICONTROL Advanced Pricing]**.

1. Klik in de sectie _[!UICONTROL Tier Price]_op **[!UICONTROL Add]**.

   Als u een laag van verscheidene prijzen creeert, klik **[!UICONTROL Add]** voor elk extra niveau, zodat kunt u alle rijen tezelfdertijd werken. Elke laag in de groep heeft dezelfde website en dezelfde klantengroep of dezelfde gedeelde catalogustoewijzing, maar een ander aantal en een andere prijs.

## Prijsniveau configureren

1. Als uw winkel meerdere websites heeft, kiest u de **[!UICONTROL Website]** waarvoor de prijzen op de laag van toepassing zijn.

1. Indien nodig, beperk de beschikbaarheid van de het tarief rij door **[!UICONTROL Customer Group]** of **[!UICONTROL Shared Catalog]** te selecteren (![ Adobe Commerce B2B ](../assets/b2b.svg) Beschikbaar met [ Adobe Commerce B2B ](./b2b/../introduction.md) slechts).

1. Voer bij **[!UICONTROL Qty]** de hoeveelheid in die moet worden besteld om de korting te ontvangen.

   - **Methode 1:** ga prijs als vast bedrag in

     Stel **[!UICONTROL Price]** in op `Fixed` en voer de aangepaste prijs voor één eenheid op die laag in.

     ![ Prijs van de Rij als Vast Bedrag ](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Methode 2:** ga prijs als percentage in

     Stel **[!UICONTROL Price]** in op `Discount` en voer de gedisconteerde prijs in als een percentage van de basisprijs van het product.

     Voer bijvoorbeeld voor een korting van 15 procent het getal `15` in. (De prijs wordt opgeslagen met twee decimale posities, zoals `15.00` .)

     >[!NOTE]
     >
     >Om de gedisconteerde prijs op te halen, wordt het gedefinieerde percentage berekend aan de hand van de waarde die is gedefinieerd in het veld _[!UICONTROL Price]_, niet in het veld_[!UICONTROL Special Price]_ .

     ![ Prijs van de Rij als Percentage ](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Voltooi de prijsconfiguratie

1. Herhaal de vorige stappen om nog een reeks prijzen voor een andere website of klantengroep toe te voegen.

1. Klik na voltooiing op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** .

>[!NOTE]
>
>De **_definitieve_** productprijs wordt berekend als **_minimum_** relevante prijs, gebruikend de volgende formule: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>_**product Aanpasbare Opties van de Prijs van de Vaste Prijs**_ {worden _niet_ beïnvloed door de Prijs van de Groep, de Prijs van de Rij, de Speciale Prijs, of de regels van de Prijs van de Catalogus.
