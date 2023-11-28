---
title: "Configureren [!DNL Inventory Management] productopties"
description: Leer hoe u de [!DNL Inventory Management] productconfiguratieopties.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Configureren [!DNL Inventory Management] productopties

Deze configuraties zijn alleen van toepassing op het bewerkte product en overschrijven alle configuraties op algemeen websiteniveau. Wijzig deze instellingen tijdens het bewerken van een product via het dialoogvenster _[!UICONTROL Sources]_en_[!UICONTROL Advanced Inventory]_ pagina.

- Productopties configureren per bron
- Productopties configureren voor geavanceerde inventarisatie

## Productopties per bron

De hoeveelheden en extra instellingen configureren per [toegevoegde bron](sources-add.md) voor het product.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de bewerkingsmodus.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** sectie en vorm productmontages voor elke bron:

   - Voer een **[!UICONTROL Qty]** (hoeveelheid).

   - Stel de **[!UICONTROL Source Item Status]** als `In Stock` of `Out of Stock`.

   - Als u de optie Waarschuwen voor hoeveelheid onder per bron wilt wijzigen, schakelt u de optie **[!UICONTROL Notify Quantity Use Default]** selectievakje.

     Indien gecleard, voer het bedrag van het voorraadniveau in dat de kennisgeving van het item buiten de balans brengt. Het opgegeven bedrag wordt afgetrokken van de verkoopbare hoeveelheid van het artikel op voorraadniveau.

     `Select to use Default` - [!DNL Commerce] controleert de opties van de product Geavanceerde Inventaris voor configuratiemontages.
     `Clear to Modify` - Geef een waarde op voor Hoeveelheid bericht, waarbij de configuratie-instellingen voor Geavanceerde voorraad en Winkel worden genegeerd.

   ![Bronsectie voor een product](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Klik op **[!UICONTROL Done]** vervolgens **[!UICONTROL Save]**.

### Veldomschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--|--|--|
| [!UICONTROL Source Code] | Algemeen | De unieke code voor een [bron](sources-manage.md). |
| [!UICONTROL Name] | Algemeen | De unieke naam voor een bron. |
| [!UICONTROL Status] | Algemeen | Product is in- of uitgeschakeld in de catalogus. |
| [!UICONTROL Source Item Status] | Algemeen | Bepaalt de huidige beschikbaarheid van het product. Opties:<br />`In Stock` - Maakt het product beschikbaar voor aankoop.<br />`Out of Stock` - Als u geen backorders activeert, kan het product niet worden aangeschaft en wordt de aanbieding uit de catalogus verwijderd. |
| [!UICONTROL Qty] | Algemeen | Aandelen voor elke bron of locatie. |
| [!UICONTROL Notify Quantity] | Algemeen | Een bedrag voor de _[!UICONTROL Notify for Quantity Below]_voor deze specifieke bron als_[!UICONTROL Notify Quantity Use Default]_ is niet geselecteerd. |
| [!UICONTROL Notify Quantity Use Default] | Algemeen | Geeft aan dat de standaardinstelling voor _[!UICONTROL Notify for Quantity Below]_in het product_[!UICONTROL Advanced Inventory]_ of globale instelling in de winkelconfiguratie. |

## Geavanceerde productopties

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de bewerkingsmodus.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** sectie en klik op **[!UICONTROL Advanced Inventory]**.

1. Inschakelen [inventariscontrole](enable.md) voor uw catalogus, set **[!UICONTROL Manage Stock]** tot `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] de montages in kindproducten treden een configureerbaar product met voeten.

   ![Geavanceerde voorraad voor een product](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Voer een bedrag in voor de **[!UICONTROL Out-of-Stock Threshold]**:

   | Waarde | Beschrijving |
   | ----- | ----- |
   | Positief bedrag | Met _[!UICONTROL Backorders]_uitgeschakeld, geeft u een positieve waarde op. |
   | Nul | Met _[!UICONTROL Backorders]_ingeschakeld, invoeren `0` staat voor oneindige achterorden toe. |
   | Negatief bedrag | Met _[!UICONTROL Backorders]_wordt aangeraden een negatieve waarde in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` om opdrachten tot dit bedrag toe te staan. |

1. Voer de **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Voer de **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Set **[!UICONTROL Qty uses Decimals]** tot `Yes` als klanten een decimale waarde in plaats van een geheel getal kunnen gebruiken bij het invoeren van de geordende hoeveelheid.

1. Set **[!UICONTROL Allow Multiple Boxes for Shipping]** tot `Yes` als het product afzonderlijk kan worden verkocht, in veel dozen. Deze optie is zichtbaar wanneer **[!UICONTROL Qty Uses Decimals]** is ingesteld op `Yes` alleen.

1. Set **[!UICONTROL Backorders]** op een van de volgende wijzen:

   | Optie | Beschrijving |
   | ----- | ----- |
   | `No Backorders` | Achtergronden niet accepteren wanneer het product uit voorraad is. |
   | `Allow Qty Below 0` | Achtergronden accepteren wanneer het aantal minder dan nul is. |
   | `Allow Qty Below 0 and Notify Customer` | Achterorden accepteren wanneer het aantal minder is dan nul en de klant ervan op de hoogte stellen dat de bestelling nog steeds kan worden geplaatst. |

   Zie voor meer informatie [Backorders configureren](backorders.md).

1. Als u de hoeveelheid wilt verhogen voor het product, stelt u **[!UICONTROL Enable Qty Increments]** tot `Yes` en voert u het nummer in van de items die moeten worden aangeschaft om te voldoen aan de vereisten van het dialoogvenster **[!UICONTROL Qty Increments]** veld.

   Een artikel dat in stappen van zes wordt verkocht, kan bijvoorbeeld worden aangeschaft in hoeveelheden van 6, 12, 18 enzovoort.

1. Klik op **[!UICONTROL Done]** en vervolgens **[!UICONTROL Save]**.

### Veldomschrijvingen

| Veld | Toepassingsgebied | Beschrijving |
|--|--|--|
| [!UICONTROL Manage Stock] | Algemeen | Hiermee bepaalt u of voorraadbeheer wordt gebruikt voor het beheer van dit product in uw catalogus. Instellen op inschakelen of uitschakelen van alles [!DNL Inventory Management] functies. Wanneer u een retour- of creditnota voltooit, wordt de producthoeveelheid automatisch teruggestuurd naar de desbetreffende bronhoeveelheid. U kunt desgewenst uitschakelen bij gebruik van een ERP-systeem van derden. |
| [!UICONTROL Out-of-Stock Threshold] | Algemeen | Hiermee wordt bepaald op welk voorraadniveau een product als niet in voorraad wordt beschouwd. Opties:<br />Positieve waarde - Voer een positieve waarde in als achtergronden zijn uitgeschakeld.<br />Nul (0) - Als Achterorden toegelaten, staat het ingaan van nul voor oneindige achterorden toe.<br />Negatieve waarde - Als backorders zijn ingeschakeld, wordt u aangeraden een negatief bedrag in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` om opdrachten tot dit bedrag toe te staan. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Algemeen | Hiermee bepaalt u het minimumaantal producten dat in één bestelling kan worden aangeschaft. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Algemeen | Hiermee bepaalt u het maximumaantal producten dat in één bestelling kan worden aangeschaft. |
| [!UICONTROL Qty Uses Decimals] | Algemeen | Hiermee bepaalt u of klanten een decimale waarde in plaats van een geheel getal kunnen gebruiken bij het invoeren van de geordende hoeveelheid. Opties:<br />`Yes` - Laat waarden toe om als decimalen in plaats van als hele getallen te worden ingegaan. Decimalen zijn geschikt voor producten die worden verkocht in gewicht, volume of lengte.<br />`No` - Vereist dat de kwantitatieve waarden als gehele getallen worden ingevoerd. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Algemeen | Hiermee wordt bepaald of onderdelen van het product afzonderlijk kunnen worden verzonden. Deze optie is zichtbaar wanneer **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Algemeen | Hiermee bepaalt u hoe achterorden worden beheerd. De achterorden veranderen niet de verwerkingsstatus van de orde. Geldmiddelen worden nog steeds onmiddellijk toegestaan of vastgelegd wanneer de bestelling wordt geplaatst, ongeacht of het product in voorraad is. De producten worden verzonden zodra ze beschikbaar zijn. Als deze optie is ingeschakeld, kunt u het beste een negatief bedrag voor de drempelwaarde voor de uit-of-voorraad invoeren. Opties:<br/>`No Backorders` - Accepteert geen backorders wanneer het product uit voorraad is.<br />`Allow Qty Below 0` - Accepteert backorders als de hoeveelheid onder nul daalt.<br />`Allow Qty Below 0 and Notify Customer` - Accepteert backorders wanneer het aantal onder nul daalt, maar waarschuwt klanten dat de orders nog kunnen worden geplaatst. |
| [!UICONTROL Enable Qty Increments] | Algemeen | Hiermee wordt bepaald of het product in hoeveelheden kan worden verkocht. |

>[!NOTE]
>
>De eenvoudige productconfiguratie treedt configureerbare productconfiguraties voor een specifiek product met voeten.
