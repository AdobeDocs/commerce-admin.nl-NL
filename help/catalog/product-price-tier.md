---
title: Tier-prijsstelling
description: Leer hoe u de prijzen op de laag gebruikt om een korting op de hoeveelheid van een productaanbieding of productpagina aan te bieden.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Tier-prijsstelling

Met de prijzen voor Tier kunt u een korting bieden op de hoeveelheid van een productaanbieding of productpagina in de winkel. De korting kan worden toegepast op een specifieke opslagweergave of een klantgroep of gedeelde catalogus.

Als u veel producten hebt om bij te werken, is het het meest efficiënt om de prijsveranderingen van de lijst in plaats van hen individueel in te voeren. Voor meer informatie, zie [&#x200B; de laagprijzen van de Invoer &#x200B;](../systems/data-import-price-tier.md).

![&#x200B; de prijs van de Rij op een storefront productpagina &#x200B;](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

Op de productpagina wordt de kwantumkorting berekend en wordt een bericht weergegeven, zoals:

`Buy 6 for $5.95 each and save 15%`

De prijzen in de winkel hebben voorrang van de hoogste naar de laagste hoeveelheid. Als u een prijs op de laag hebt voor het aantal `5` en één voor `10` en een klant vijf, zes, zeven, acht of negen items aan het winkelwagentje toevoegt, ontvangt de klant de verlaagde prijs voor de laag voor het aantal `5` . Wanneer de klant het tiende item toevoegt, vervangt de gedisconteerde prijs die voor de kwantiteit `10` is opgegeven de laag voor een hoeveelheid `5` en geldt de gedisconteerde prijs voor `10` .

## Een prijsniveau toevoegen voor een product

1. Open het product in de bewerkingsmodus.

1. Klik onder het veld _[!UICONTROL Price]_&#x200B;op **[!UICONTROL Advanced Pricing]**.

1. Klik in de sectie _[!UICONTROL Tier Price]_&#x200B;op **[!UICONTROL Add]**.

   Als u een laag van verscheidene prijzen creeert, klik **[!UICONTROL Add]** voor elk extra niveau, zodat kunt u alle rijen tezelfdertijd werken. Elke laag in de groep heeft dezelfde website en dezelfde klantengroep of dezelfde gedeelde catalogustoewijzing, maar een ander aantal en een andere prijs.

## Prijsniveau configureren

1. Als uw winkel meerdere websites heeft, kiest u de **[!UICONTROL Website]** waarvoor de prijzen op de laag van toepassing zijn.

1. Indien nodig, beperk de beschikbaarheid van de het tarief rij door **[!UICONTROL Customer Group]** of **[!UICONTROL Shared Catalog]** te selecteren (![&#x200B; Adobe Commerce B2B &#x200B;](../assets/b2b.svg) Beschikbaar met [&#x200B; Adobe Commerce B2B &#x200B;](./b2b/../introduction.md) slechts).

1. Voer bij **[!UICONTROL Qty]** de hoeveelheid in die moet worden besteld om de korting te ontvangen.

   - **Methode 1:** ga prijs als vast bedrag in

     Stel **[!UICONTROL Price]** in op `Fixed` en voer de aangepaste prijs voor één eenheid op die laag in.

     ![&#x200B; Prijs van de Rij als Vast Bedrag &#x200B;](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Methode 2:** ga prijs als percentage in

     Stel **[!UICONTROL Price]** in op `Discount` en voer de gedisconteerde prijs in als een percentage van de basisprijs van het product.

     Voer bijvoorbeeld voor een korting van 15 procent het getal `15` in. (De prijs wordt opgeslagen met twee decimale posities, zoals `15.00` .)

     >[!NOTE]
     >
     >Om de gedisconteerde prijs op te halen, wordt het gedefinieerde percentage berekend aan de hand van de waarde die is gedefinieerd in het veld _[!UICONTROL Price]_, niet in het veld&#x200B;_[!UICONTROL Special Price]_ .

     ![&#x200B; Prijs van de Rij als Percentage &#x200B;](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Voltooi de prijsconfiguratie

1. Herhaal de vorige stappen om nog een reeks prijzen voor een andere website of klantengroep toe te voegen.

1. Klik na voltooiing op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** .

>[!NOTE]
>
>De **_definitieve_** productprijs wordt berekend als **_minimum_** relevante prijs, gebruikend de volgende formule: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_product Aanpasbare Opties van de Prijs van de Vaste Prijs_** &lbrace;worden _niet_ beïnvloed door de Prijs van de Groep, de Prijs van de Rij, de Speciale Prijs, of de regels van de Prijs van de Catalogus.

## Laagprijzen inschakelen voor catalogusprijsregels

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service-projecten (door Adobe beheerde SaaS-infrastructuur)."}

In eerdere versies van Commerce kon de prijzen op de laag niet worden gebruikt in combinatie met de prijsregels voor catalogi. De catalogusregels negeerden de configuratie van de laagprijs en berekende kortingen slechts van de oorspronkelijke basisprijs. Met Adobe Commerce as a Cloud Service kunt u nu laagprijzen opnemen in de berekening van catalogusprijsregels.

U schakelt deze functionaliteit als volgt in:

1. Navigeer naar **[!UICONTROL Stores]** > *[!UICONTROL Settings]* > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Promotions]** en stel het veld **[!UICONTROL Apply Catalog Price Rule on Grouped Price]** in op **[!UICONTROL Yes]** .

   ![&#x200B; laat rij het tarief voor de catalogusprijs toe regels &#x200B;](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. Definieer een laagprijs met een hoeveelheid van `1` voor elke specifieke klantengroep of gedeelde catalogus (zoals `Wholesale` , `Retail` of door de handelaar gedefinieerde groep) die u wilt gebruiken met de prijsregels voor de catalogus. De gedeelde `ALL GROUPS` klantengroep en `Default` catalogus kunnen niet voor dit doel worden gebruikt. Prijsniveau is niet ingeschakeld voor een groep waarvoor geen laagprijs is gedefinieerd met een hoeveelheid `1` .

1. Definieer zo nodig extra laagprijzen met hoeveelheden groter dan `1`. Deze aanvullende prijzen op de markt worden op de gebruikelijke wijze toegepast wanneer de klant extra hoeveelheden van het product aan het winkelwagentje toevoegt. De catalogusprijsregels zijn niet van toepassing op deze extra laagprijzen.

Om te illustreren hoe de prijsverhoging met catalogusprijsregels werkt wanneer het kopen van één enkel product, overweeg het volgende voorbeeld:

- De standaardbasisprijs van een product is 100 USD.
- Een laagprijs wordt gedefinieerd voor de `Wholesale` klantengroep met een hoeveelheid `1` en een vaste prijs van 90 USD.
- Een regel voor catalogusprijzen biedt een korting van 10% voor de klantengroep van `Wholesale` .

Wanneer de prijsverhoging voor catalogusprijzen wordt toegelaten, gebruikt het systeem de volgende stroom om de definitieve prijs te berekenen:

1. Voordat de klant zich aanmeldt, wordt de productprijs weergegeven als 100 USD (de standaardbasisprijs).

1. Nadat de klant zich heeft aangemeld als lid van de `Wholesale` -groep, wordt de productprijs aangepast aan 90 USD (de laagprijs voor de `Wholesale` -groep).

1. De prijsregel voor catalogi wordt toegepast, waarbij een korting van 10% wordt toegepast op de op de lijst opgenomen prijs van 90 USD, wat resulteert in een uiteindelijke prijs van 81 USD.

In de volgende tabel worden prijsberekeningen samengevat wanneer de prijsopgave voor catalogusprijzen is ingeschakeld en een regel voor catalogusprijzen biedt een korting van 10% voor alle klantengroepen:

Product: standaardprijs $100 (aankoop van één object)

| Klantengroep | Tier-prijs (Qty=1) | Nieuwe basisprijs | Uiteindelijke prijs |
|---|---|---|---|
| ALLE GROEP | Niet geconfigureerd | $ 100 | $ 100 - 10% = $ 90 |
| Groothandel | Vast: $85 | $ 85 | $ 85 - 10% = $ 76,50 |
| Retailer | 20% korting | $ 80 | $ 80 - 10% = $ 72,00 |
| VIP | 15% korting | $ 85 | $ 85 - 10% = $ 76,50 |
