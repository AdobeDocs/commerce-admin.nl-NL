---
title: Groepsprijzen
description: Leer hoe je groepsprijzen kunt gebruiken om prijzen voor objecten met korting in te stellen op basis van klantgroepen in je winkel.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Groepsprijzen

U kunt de instellingen voor productconfiguratie in de Admin gebruiken om prijzen voor gedisconteerde objecten in te stellen op basis van klantgroepen in uw winkel. Dit strategische het tariferen model wordt genoemd _groep tarifering_.

De gedisconteerde prijs van om het even welk product kan aan leden van een specifieke klantengroep worden aangeboden wanneer de verkoopster aan hun rekening wordt het programma geopend. De prijs van de klantengroep wordt samen met de normale prijs op de productpagina weergegeven, zodat een winkelier de prijzen gemakkelijk kan vergelijken en dienovereenkomstig kan handelen. Nadat zij het product aan het winkelwagentje hebben toegevoegd, wordt de normale prijs vervangen door de groepsprijs op basis van hun klantengroep.

Het tarief voor klantengroepen is een component van [&#x200B; gelaagde tarifering &#x200B;](product-price-tier.md) en op een gelijkaardige manier geplaatst. Het enige verschil is dat de prijzen van de klantengroep een hoeveelheid van 1 hebben.

![&#x200B; Korting van de Groep van de Klant &#x200B;](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Voordelen van het gebruik van groepsprijzen

- Geschikt voor groothandelaars

- Stimulering voor klanten om hun klantengroep te bevorderen om uit kortingen voordeel te halen

- Gerichte marketingcampagnes

- Vertrouwen en geloofwaardigheid opbouwen door loyale klanten te belonen

## Een groepsprijs instellen

1. Open het product in de bewerkingsmodus.

1. Klik onder het veld _[!UICONTROL Price]_&#x200B;op **[!UICONTROL Advanced Pricing]**.

1. Klik in de sectie _[!UICONTROL Customer Group Price]_&#x200B;op **[!UICONTROL Add]**.

   Als uw opslag [&#x200B; Adobe Commerce B2B &#x200B;](../b2b/introduction.md) omvat en [&#x200B; gedeelde toegelaten catalogi &#x200B;](../b2b/catalog-shared.md) heeft, wordt deze sectie geëtiketteerd _[!UICONTROL Catalog and Tier Price]_.

   ![&#x200B; Geavanceerde Prijsverhoging &#x200B;](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configureer de groepsprijs:

   - Kies voor een installatie met meerdere sites de **[!UICONTROL Website]** waar de groepsprijs van toepassing is.

   - Kies de **[!UICONTROL Customer Group]** die de korting moet ontvangen.

   - Voer een **[!UICONTROL Quantity]** van `1` in.

   - Stel voor **[!UICONTROL Price]** het type en het bedrag van de prijs in:

      - `Fixed` - Voer de gedisconteerde productprijs in.

      - `Discount` - Voer de gedisconteerde prijs in als een percentage van de productprijs.

     ![&#x200B; Prijzen van de Groep van de Klant &#x200B;](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Als u nog een groepsprijs wilt toevoegen, klikt u op **[!UICONTROL Add]** en herhaalt u de vorige stap.

1. Klik na voltooiing op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** .

>[!NOTE]
>
>De **_definitieve_** productprijs wordt berekend als **_minimum_** relevante prijs, gebruikend de volgende formule: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>_&#x200B;**product Aanpasbare Opties van de Prijs van de Vaste Prijs**&#x200B;_ &lbrace;worden _niet_ beïnvloed door de Prijs van de Groep, de Prijs van de Rij, de Speciale Prijs, of de regels van de Prijs van de Catalogus.
