---
title: Cadeauproduct
description: Leer hoe u een cadeaukaartproduct maakt dat een unieke code produceert die tijdens het afrekenen door een ontvanger kan worden ingewisseld.
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: e72977596c4479d2e94b1e066ee166d22cb12405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Cadeauproduct

{{ee-feature}}

Elke cadeaukaart heeft een unieke code die door slechts één klant kan worden afgelost tijdens het afrekenen. A [ codepool ](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) moet worden gevestigd alvorens de geschenkkaarten kunnen worden verkocht. Zie [ het werkschema van de Cadeaukaart ](../stores-purchase/product-gift-card-workflow.md) voor informatie over hoe de geschenkkaarten in het het winkelwagentje worden ingewisseld.

![ het productpagina van het kaartenproduct van de Gift ](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

Er zijn drie soorten cadeaukaartproducten:

- **Virtueel** - een virtuele geschenkkaart wordt verzonden naar het e-mailadres van de ontvanger, die tijdens de aankoop van de geschenkkaart wordt vereist. Een verzendadres is niet nodig.

- **Fysiek** - een fysieke geschenkkaart wordt verscheept aan het adres van de ontvanger, die tijdens de aankoop van de geschenkkaart wordt vereist.

- **Gecombineerd** - een gecombineerde geschenkkaart wordt verscheept en aan de ontvanger gemaild. Het e-mailadres en het verzendadres van de ontvanger zijn vereist tijdens de aankoop van de cadeaukaart.

## Een cadeaukaartproduct maken

De volgende instructies tonen het proces aan om een geschenkkaart te creëren gebruikend a [ productmalplaatje ](attribute-sets.md), vereiste gebieden, en basismontages. Elk vereist gebied is duidelijk met een rode asterisk (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

### Stap 1: Kies het producttype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. In de hoger-juiste hoek op _[!UICONTROL Add Product]_( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}  ), kiest u **[!UICONTROL Gift Card]**.

   ![ voeg de Kaart van het Cadeautje ](./assets/product-add-gift-card.png){width="700" zoomable="yes"} toe

### Stap 2: Kies de kenmerkset

U kunt de standaard `Gift Card` kenmerkset gebruiken of een andere set kiezen. Voer een van de volgende handelingen uit om de kenmerkset te kiezen die als sjabloon voor het product wordt gebruikt:

- Klik in het veld **[!UICONTROL Attribute Set]** en voer de naam van de kenmerkset geheel of gedeeltelijk in.

- Kies in de weergegeven lijst de kenmerkset die u wilt gebruiken.

![ kies Vastgestelde Attributen ](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### Stap 3: Voer de vereiste instellingen in

1. Voer een **[!UICONTROL Product Name]** in voor de cadeaukaart.

   U kunt ook het type cadeaukaart in de naam aangeven. Bijvoorbeeld, _de Virtuele Kaart van het Gift van de Luma_.

1. Voer een **[!UICONTROL SKU]** in voor het product.

   Door gebrek, wordt de Naam van het Product gebruikt als gebrek SKU.

1. Stel **[!UICONTROL Card Type]** in op een van de volgende opties:

   - `Virtual` - Virtuele cadeaukaarten worden via e-mail aan de ontvanger bezorgd.
   - `Physical` - Fysieke cadeaukaarten kunnen vooraf worden gemaakt en worden voorzien van unieke codes.
   - `Combined` - Een gecombineerde cadeaukaart heeft de kenmerken van zowel een virtuele als een fysieke cadeaukaart.

   ![ Type van Kaart van Cadeautje ](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. Als u de klant een keuze wilt bieden met vaste bedragen, klikt u op **[!UICONTROL Add Amount]** en voert u de eerste vaste waarde van de kaart in als een decimaal.

   Herhaal deze stap voor elke waarde om de selectie van vaste bedragen in te voeren.

1. Ga als volgt te werk om klanten de mogelijkheid te bieden de waarde van de cadeaukaart in te stellen:

   - Stel **[!UICONTROL Open Amount]** in op `Yes` .

   - Voer de waarden **[!UICONTROL Open Amount From]** en **[!UICONTROL To]** in om het bereik van de minimaal- en maximaal toegestane waarden te definiëren.

   U kunt cadeaukaarten maken met een vaste prijs, een open prijs of beide.

   >[!NOTE]
   >
   >Een cadeaukaartproduct heeft geen eigen prijs in de catalogus. De prijs van de cadeau-kaart wordt afgeleid van het geselecteerde bedrag van de cadeau-kaart tijdens de aankoop.

   ![ de Bedragen van de Kaart van het Cadeautje ](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### Stap 4: De basisinstellingen voltooien

1. Voer voor een fysieke of gecombineerde cadeaukaart de **[!UICONTROL Quantity]** in voorraad in.

1. Als de cadeaukaart die moet worden verzonden, voert u de **[!UICONTROL Weight]** van het pakket in.

1. Kies in het veld **[!UICONTROL Categories]** de optie `Gift Card` .

Er kunnen aanvullende individuele kenmerken zijn die het product beschrijven. De selectie varieert kenmerkset en u kunt deze later voltooien.

### Stap 5: De kaartgegevens van de cadeau invullen

De _[!UICONTROL Gift Card Information]_&#x200B;sectie van de productmontages kan worden gebruikt om de [ configuratie van de giftekaart ](../configuration-reference/sales/gift-cards.md) montages met voeten te treden die bepalen hoe de kaart wordt beheerd.

1. Schuif omlaag naar de sectie _[!UICONTROL Gift Card Information]_.

   De standaardinstellingen in deze sectie worden bepaald door de systeemconfiguratie.

   ![ de Informatie van de Kaart van het Cadeautje ](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. Wijzig aanvullende velden op basis van de manier waarop de cadeaukaart moet werken:

   - **[!UICONTROL Treat Balance as Store Credit]** - Hiermee bepaalt u of de houder van de cadeau-kaart het saldo kan inwisselen als winkelkrediet.

   - **[!UICONTROL Lifetime (days)]** - Hiermee bepaalt u het aantal dagen na aanschaf tot de cadeaukaart verloopt. Als u geen limiet wilt instellen voor de levensduur van de kaart, laat u dit veld leeg.

   - **[!UICONTROL Allow Message]** - Hiermee wordt bepaald of de koper van de cadeaukaart een bericht voor aan de ontvanger kan invoeren. Een cadeaubericht kan worden opgenomen voor zowel virtuele (e-mail) als fysieke (verzonden) cadeaukaarten.

   - **[!UICONTROL Email Template]** - Bepaalt de e-mailsjabloon die wordt gebruikt voor het bericht dat naar de ontvanger van een cadeaukaart wordt verzonden.

### Stap 6: De productinformatie invullen

Voer de benodigde gegevens in de volgende secties in:

- [Inhoud](product-content.md)
- [Afbeeldingen en video&#39;s](product-images-and-video.md)
- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)
- [Optimalisatie zoekmachine](product-search-engine-optimization.md)
- [Aanpasbare opties](settings-advanced-custom-options.md)
- [Producten op websites](settings-basic-websites.md)
- [Ontwerp](settings-advanced-design.md)
- [Cadeauopties](product-gift-options.md)

### Stap 7: Publish het product

1. Als u bereid bent om het product in de catalogus te publiceren, plaats **laat de schakelaar van het Product** `Yes` toe.

1. Voer een van de volgende handelingen uit:

   **Methode 1:** sparen en Voorproef

   - Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

   - Om het product in uw opslag te bekijken, verkies **[!UICONTROL Customer View]** op _Admin_ ( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-black.png)) menu,

   ![ Mening van de Klant ](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Methode 2:** sparen en sluit

   Voor _[!UICONTROL Save]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu, kies **[!UICONTROL Save & Close]**.

## Te onthouden zaken

- A _codepool_ van unieke aantallen moet worden geproduceerd alvorens een geschenkkaart voor verkoop kan worden aangeboden.

- Cadeaukaarten kunnen worden ingesteld op `Redeemable` of `Non-Redeemable` .

- De belastingen worden **_niet toegepast_** op geschenkkaarten tijdens de geschenkkaartaankoop. Belastingen worden alleen op producten toegepast wanneer een aangeschafte cadeaukaart wordt gebruikt om producten te kopen.

- De levensduur van een cadeaukaart kan onbeperkt zijn of op een opgegeven aantal dagen worden ingesteld.

- De waarde van een cadeaukaart kan worden ingesteld op een vast bedrag of worden ingesteld op een open bedrag met een minimum- en maximumwaarde.

- Een cadeaukaartproduct heeft geen eigen prijs in de catalogus. De prijs van de cadeau-kaart wordt afgeleid van het geselecteerde bedrag van de cadeau-kaart tijdens de aankoop.

- Een kaartenaccount voor de klant kan worden gemaakt wanneer de bestelling wordt geplaatst of op het moment van de factuur.
