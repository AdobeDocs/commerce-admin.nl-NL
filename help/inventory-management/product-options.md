---
title: Vorm  [!DNL Inventory Management]  productopties
description: Leer hoe te om de  [!DNL Inventory Management]  opties van de productconfiguratie te vormen.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# [!DNL Inventory Management] productopties configureren

Deze configuraties zijn alleen van toepassing op het bewerkte product en overschrijven alle configuraties op algemeen websiteniveau. Wijzig deze instellingen tijdens het bewerken van een product via de secties _[!UICONTROL Sources]_&#x200B;en&#x200B;_[!UICONTROL Advanced Inventory]_ .

- Productopties configureren per bron
- Productopties configureren voor geavanceerde inventarisatie

## Productopties per bron

Vorm de hoeveelheden en de extra montages per [&#x200B; toegevoegde bron &#x200B;](sources-add.md) voor het product.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de bewerkingsmodus.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** sectie uit en vorm productmontages voor elke bron:

   - Voer een hoeveelheid **[!UICONTROL Qty]** (hoeveelheid) in.

   - Stel de **[!UICONTROL Source Item Status]** in op `In Stock` of `Out of Stock` .

   - Schakel het selectievakje **[!UICONTROL Notify Quantity Use Default]** uit of selecteer dit als u het vak Waarschuwen voor hoeveelheid onder per bron wilt wijzigen.

     Indien gecleard, voer het bedrag van het voorraadniveau in dat de kennisgeving van het item buiten de balans brengt. Het opgegeven bedrag wordt afgetrokken van de verkoopbare hoeveelheid van het artikel op voorraadniveau.

     `Select to use Default` - [!DNL Commerce] controleert de product Geavanceerde opties van de Inventaris voor configuratiemontages.
     `Clear to Modify` - Voer een waarde in voor Hoeveelheid bericht, waarbij de instellingen voor Geavanceerde voorraad en winkelconfiguratie worden genegeerd.

   ![&#x200B; Bronsectie voor een product &#x200B;](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Klik op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** als de bewerking is voltooid.

### Veldomschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--|--|--|
| [!UICONTROL Source Code] | Algemeen | De unieke code voor a [&#x200B; bron &#x200B;](sources-manage.md). |
| [!UICONTROL Name] | Algemeen | De unieke naam voor een bron. |
| [!UICONTROL Status] | Algemeen | Product is in- of uitgeschakeld in de catalogus. |
| [!UICONTROL Source Item Status] | Algemeen | Bepaalt de huidige beschikbaarheid van het product. Opties:<br />`In Stock` - maakt het product beschikbaar voor aankoop.<br />`Out of Stock` - Als u geen achtergrondbestanden activeert, kan het product niet worden aangeschaft en wordt de aanbieding uit de catalogus verwijderd. |
| [!UICONTROL Qty] | Algemeen | Aandelen voor elke bron of locatie. |
| [!UICONTROL Notify Quantity] | Algemeen | Een hoeveelheid voor de _[!UICONTROL Notify for Quantity Below]_&#x200B;voor deze specifieke bron als&#x200B;_[!UICONTROL Notify Quantity Use Default]_ niet is geselecteerd. |
| [!UICONTROL Notify Quantity Use Default] | Algemeen | Geeft aan dat de standaardinstelling voor _[!UICONTROL Notify for Quantity Below]_&#x200B;moet worden gebruikt in het product&#x200B;_[!UICONTROL Advanced Inventory]_ of de globale instelling in de winkelconfiguratie. |

## Geavanceerde productopties

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de bewerkingsmodus.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** sectie uit en klik **[!UICONTROL Advanced Inventory]**.

1. Om [&#x200B; inventariscontrole &#x200B;](enable.md) voor uw catalogus toe te laten, plaats **[!UICONTROL Manage Stock]** aan `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] -instellingen in onderliggende producten hebben voorrang op een configureerbaar product.

   ![&#x200B; Geavanceerde Inventaris voor een Product &#x200B;](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Voer een bedrag in voor de **[!UICONTROL Out-of-Stock Threshold]** :

   | Waarde | Beschrijving |
   | ----- | ----- |
   | Positief bedrag | Voer een positieve waarde in als _[!UICONTROL Backorders]_&#x200B;is uitgeschakeld. |
   | Nul | Als _[!UICONTROL Backorders]_&#x200B;is ingeschakeld, kunt u met het invoeren van `0` oneindige backorders invoeren. |
   | Negatief bedrag | Als _[!UICONTROL Backorders]_&#x200B;is ingeschakeld, wordt u aangeraden een negatieve waarde in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` in om bestellingen tot dit bedrag toe te staan. |

1. Voer de **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** in.

1. Voer de **[!UICONTROL Maximum Qty Allowed in Shopping Cart]** in.

1. Stel **[!UICONTROL Qty uses Decimals]** in op `Yes` als klanten een decimale waarde in plaats van een geheel getal kunnen gebruiken bij het invoeren van de geordende hoeveelheid.

1. Stel **[!UICONTROL Allow Multiple Boxes for Shipping]** in op `Yes` als het product afzonderlijk in veel vakken kan worden verkocht. Deze optie is zichtbaar wanneer **[!UICONTROL Qty Uses Decimals]** is ingesteld op `Yes` only.

1. Stel **[!UICONTROL Backorders]** in op een van de volgende opties:

   | Optie | Beschrijving |
   | ----- | ----- |
   | `No Backorders` | Achtergronden niet accepteren wanneer het product uit voorraad is. |
   | `Allow Qty Below 0` | Achtergronden accepteren wanneer het aantal minder dan nul is. |
   | `Allow Qty Below 0 and Notify Customer` | Achterorden accepteren wanneer het aantal minder is dan nul en de klant ervan op de hoogte stellen dat de bestelling nog steeds kan worden geplaatst. |

   Voor meer informatie, zie [&#x200B; het Vormen Achterorden &#x200B;](backorders.md).

1. Als u de hoeveelheid wilt verhogen voor het product, stelt u **[!UICONTROL Enable Qty Increments]** in op `Yes` en voert u in het veld **[!UICONTROL Qty Increments]** het aantal items in dat moet worden aangeschaft om aan de vereisten te voldoen.

   Een artikel dat in stappen van zes wordt verkocht, kan bijvoorbeeld worden aangeschaft in hoeveelheden van 6, 12, 18 enzovoort.

   In het veld **[!UICONTROL Qty Increments]** wordt ingesteld hoeveel productitems moeten worden aangeschaft als één product en als onderliggend product van configureerbare, gegroepeerde en bundelproducten.

1. Klik na voltooiing op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** .

### Veldomschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--|--|--|
| [!UICONTROL Manage Stock] | Algemeen | Hiermee bepaalt u of voorraadbeheer wordt gebruikt voor het beheer van dit product in uw catalogus. Instellen op inschakelen of uitschakelen van alle [!DNL Inventory Management] -functies. Wanneer u een retour- of creditnota voltooit, wordt de producthoeveelheid automatisch teruggestuurd naar de desbetreffende bronhoeveelheid. U kunt desgewenst uitschakelen bij gebruik van een ERP-systeem van derden. |
| [!UICONTROL Out-of-Stock Threshold] | Algemeen | Hiermee wordt bepaald op welk voorraadniveau een product als niet in voorraad wordt beschouwd. Opties:<br /> Positieve waarde - met gehandicapte backorders, ga een positieve hoeveelheid in.<br /> Nul (0) - met toegelaten Achterorden, staat het ingaan van nul voor oneindige achterorden toe.<br /> Negatieve waarde - met toegelaten backorders, wordt het ingaan van een negatief bedrag geadviseerd. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` in om bestellingen tot dit bedrag toe te staan. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Algemeen | Hiermee bepaalt u het minimumaantal producten dat in één bestelling kan worden aangeschaft. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Algemeen | Hiermee bepaalt u het maximumaantal producten dat in één bestelling kan worden aangeschaft. |
| [!UICONTROL Qty Uses Decimals] | Algemeen | Hiermee bepaalt u of klanten een decimale waarde in plaats van een geheel getal kunnen gebruiken bij het invoeren van de geordende hoeveelheid. Opties:<br />`Yes` - laat waarden toe om als decimalen, eerder dan volledige aantallen worden ingegaan. Decimalen zijn geschikt voor producten die worden verkocht in gewicht, volume of lengte.<br />`No` - Vereist kwantitatieve waarden dat deze als hele getallen worden ingevoerd. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Algemeen | Hiermee wordt bepaald of onderdelen van het product afzonderlijk kunnen worden verzonden. Deze optie is zichtbaar wanneer **[!UICONTROL Qty Uses Decimals]** = `Yes` . |
| [!UICONTROL Backorders] | Algemeen | Hiermee bepaalt u hoe achterorden worden beheerd. De achterorden veranderen niet de verwerkingsstatus van de orde. Geldmiddelen worden nog steeds onmiddellijk toegestaan of vastgelegd wanneer de bestelling wordt geplaatst, ongeacht of het product in voorraad is. De producten worden verzonden zodra ze beschikbaar zijn. Als deze optie is ingeschakeld, kunt u het beste een negatief bedrag voor de drempelwaarde voor de uit-of-voorraad invoeren. Opties:<br/>`No Backorders` - Accepteert geen backorders wanneer het product uit voorraad is.<br />`Allow Qty Below 0` - Accepteert backorders als het aantal minder dan nul is.<br />`Allow Qty Below 0 and Notify Customer` - Accepteert backorders wanneer het aantal onder nul daalt, maar waarschuwt klanten dat de orders nog kunnen worden geplaatst. |
| [!UICONTROL Enable Qty Increments] | Algemeen | Hiermee wordt bepaald of het product in hoeveelheden kan worden verkocht. De verhogingen plaatsen hoeveel productpunten als één enkel product, en als kind van configureerbare, gegroepeerde en bundelproducten moeten worden gekocht. |

>[!NOTE]
>
>De eenvoudige productconfiguratie treedt configureerbare productconfiguraties voor een specifiek product met voeten.
