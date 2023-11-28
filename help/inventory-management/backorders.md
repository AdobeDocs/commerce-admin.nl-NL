---
title: "Configureren [!DNL Inventory Management] backorders"
description: Leer hoe te om backorders te vormen om verkoop van uit-van-voorraad producten te steunen.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Configureren [!DNL Inventory Management] achtergronden

Met backorders kan je winkel producten blijven verkopen nadat de hoeveelheid nul is bereikt of de voorraad is uitgeput. Wanneer een order van een klant een backorder is, worden de fondsen onmiddellijk geautoriseerd en vastgelegd, verandert de verwerkingsstatus van de order niet en blijft de verzending in voorraad totdat de voorraad beschikbaar is.

Afhankelijk van uw opslag en verkoop, kunt u backorders op de volgende niveaus willen toelaten of onbruikbaar maken:

- **[!UICONTROL Global]** - Alle producten in uw catalogus op siteniveau

- **[!UICONTROL Product]** - Specifieke producten die de instellingen voor site, bron en voorraad overschrijven

## Instellingen voor achtergrondvolgorde begrijpen

Het wordt hoogst geadviseerd dat u specifieke drempels en montages vormt om backorders het best te steunen.

### Drempel voor voorraadoverschrijding

Gebruik een negatieve waarde voor deze drempel om de maximumhoeveelheid producten te bepalen die kan worden teruggeordend alvorens het product werkelijk als out van voorraad wordt beschouwd. Dit bedrag komt bij de verkoopbare hoeveelheid. De waarde die op het productniveau is ingesteld, heeft voorrang op alle waarden die op algemeen niveau zijn ingesteld.

De formule voor de verkoopbare hoeveelheid is `(Quantity - (Out-of-Stock Threshold))`.

Hieronder ziet u een voorbeeld:

- Hoeveelheid: 25
- Melden voor hoeveelheid onder: 10
- Alleen X linkerdrempel: 5
- Drempel voor voorraadverlies: -50

De verkoopbare hoeveelheid voor dit product is `75 (25 - (-50))`.

![Voorbeeld van aanpasbare hoeveelheid voordat backorders zijn ingeschakeld](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![Voorbeeld van aanpasbare hoeveelheid na ingeschakelde backorders](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Wanneer klanten de beschikbare 25 producten aanschaffen, worden nieuwe bestellingen ingevoerd als backorders. Aangezien de verkoopbare hoeveelheid van het product tot 5 (er zijn 70 objecten verkocht) daalt, wordt de _Product_ pagina toont een bericht `Only 5 left` op de opslagplaats. Wanneer de verkoopbare hoeveelheid `0`, wordt het product weergegeven als `Out of Stock` in de winkel.

>[!NOTE]
>
>Wanneer een klant een order plaatst met _[!UICONTROL backorder qty]_, [!DNL Inventory Management] wordt de hoeveelheid automatisch afgetrokken van de verkoopbare hoeveelheid. Als een bestelling niet wordt verzonden en wordt geannuleerd, wordt de hoeveelheid teruggezet naar de geaggregeerde virtuele verkoopbare hoeveelheid. De **_hoeveelheid geannuleerde bestelling wordt niet toegewezen aan een van de bronnen_**, maar wordt teruggegeven aan het totale aantal te koop aangeboden producten (_[!UICONTROL Salable Quantity]_ kolom op het productraster).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### Status van voorraad

Producten moeten worden ingesteld op `In Stock` status bij het inschakelen van backorders. U kunt deze waarde instellen in het menu _Product_ pagina. Voor uit meerdere bronnen bestaande handelaren moet u ten minste één bron hebben die is gemarkeerd als `In Stock`. Toegang tot de status en stel deze in via de _Product_ pagina en toegewezen _Bronnen_ raster.

## Globaal randapparatuur configureren

Deze stappen laten backorders voor alle producten op het plaatniveau toe.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Set **[!UICONTROL Store View]** tot `Default Config`.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Inventory]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. Voor **[!UICONTROL Backorders]** schakelt u de optie **[!UICONTROL Use system value]** Schakel het selectievakje in en selecteer een optie:

   | Optie | Beschrijving |
   | -- | -- |
   | `No Backorders` | Achtergronden niet accepteren wanneer het product uit voorraad is. |
   | `Allow Qty Below 0` | Achtergronden accepteren wanneer het aantal minder dan nul is. |
   | `Allow Qty Below 0 and Notify Customer` | Achterorden accepteren wanneer het aantal minder is dan nul en de klant laten weten dat de bestelling nog steeds kan worden geplaatst. |

1. Voor **[!UICONTROL Out-of-Stock Threshold]** schakelt u de optie **[!UICONTROL Use system value]** en voer een ander bedrag in.

   | Waarde | Beschrijving |
   | -- | -- |
   | Positief bedrag | Voer een positieve waarde in als Achterorden uitgeschakeld is. |
   | Nul | Als Achterorden ingeschakeld, voert u `0` staat voor oneindige achterorden toe. |
   | Negatief bedrag | Als Achterorden ingeschakeld, wordt u aangeraden een negatieve waarde in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` om opdrachten tot dit bedrag toe te staan. |

1. Klik op **[!UICONTROL Save Config]**.

## Achterorden voor een product configureren

Configuraties op productniveau overschrijven algemene configuraties. U kunt backorders op productniveau willen vormen om de montages op het globale opslag of bronniveau met voeten te treden. Uw winkel biedt bijvoorbeeld wereldwijd ondersteuning voor backorders. Met productmontages, kunt u achterorden onbruikbaar maken of de drempel veranderen uit-van-voorraad zonder andere producten en bronnen te beïnvloeden.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Een product openen in **[!UICONTROL Edit]** en de pagina omlaag naar de _[!UICONTROL Sources]_gebied.

   Voor producten die zonder [!DNL Inventory Management], wordt de tab niet weergegeven. De `Advanced Inventory` wordt weergegeven onder de _[!UICONTROL Quantity]_veld.

1. Klik op **[!UICONTROL Advanced Inventory]**.

   Deze actie toont een pagina van product-specifieke configuraties. Elke instelling die wordt vermeld als `global` geeft de huidige algemene instelling voor de winkel weer.

1. Voor **[!UICONTROL Backorders]** schakelt u de optie **[!UICONTROL Use Config Setting]** Schakel het selectievakje in en selecteer een optie:

   | Optie | Beschrijving |
   | -- | -- |
   | `No Backorders` | Achtergronden niet accepteren wanneer het product uit voorraad is. |
   | `Allow Qty Below 0` | Achtergronden accepteren wanneer het aantal minder dan nul is. |
   | `Allow Qty Below 0 and Notify Customer` | Achterorden accepteren wanneer het aantal minder is dan nul en de klant laten weten dat de bestelling nog steeds kan worden geplaatst. |

1. Voor **[!UICONTROL Out-of-Stock Threshold]** schakelt u de optie **[!UICONTROL Use Config Setting]** en voer een bedrag in:

   | Waarde | Beschrijving |
   | -- | -- |
   | Positief bedrag | Voer een positieve waarde in als Achterorden uitgeschakeld is. |
   | Nul | Als Achterorden ingeschakeld, voert u `0` staat voor oneindige achterorden toe. |
   | Negatief bedrag | Als Achterorden ingeschakeld, wordt u aangeraden een negatieve waarde in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` om opdrachten tot dat bedrag toe te staan. |

   ![Geavanceerde inventarisatie geconfigureerd voor backorders](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Klikken **[!UICONTROL Done]** en vervolgens **[!UICONTROL Save]**.
