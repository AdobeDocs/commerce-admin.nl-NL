---
title: "Vorm  [!DNL Inventory Management]  achterorden"
description: Leer hoe te om backorders te vormen om verkoop van uit-van-voorraad producten te steunen.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# [!DNL Inventory Management] backorders configureren

Met backorders kan je winkel producten blijven verkopen nadat de hoeveelheid nul is bereikt of de voorraad is uitgeput. Wanneer een order van een klant een backorder is, worden de fondsen onmiddellijk geautoriseerd en vastgelegd, verandert de verwerkingsstatus van de order niet en blijft de verzending in voorraad totdat de voorraad beschikbaar is.

Afhankelijk van uw opslag en verkoop, kunt u backorders op de volgende niveaus willen toelaten of onbruikbaar maken:

- **[!UICONTROL Global]** - Alle producten in uw catalogus op siteniveau

- **[!UICONTROL Product]** - Specifieke producten die instellingen voor site, bron en voorraad overschrijven

## Instellingen voor achtergrondvolgorde begrijpen

Het wordt hoogst geadviseerd dat u specifieke drempels en montages vormt om backorders het best te steunen.

### Drempel voor voorraadoverschrijding

Gebruik een negatieve waarde voor deze drempel om de maximumhoeveelheid producten te bepalen die kan worden teruggeordend alvorens het product werkelijk als out van voorraad wordt beschouwd. Dit bedrag komt bij de verkoopbare hoeveelheid. De waarde die op het productniveau is ingesteld, heeft voorrang op alle waarden die op algemeen niveau zijn ingesteld.

De formule voor de verkoopbare hoeveelheid is `(Quantity - (Out-of-Stock Threshold))` .

Hieronder ziet u een voorbeeld:

- Hoeveelheid: 25
- Melden voor hoeveelheid onder: 10
- Alleen X linkerdrempel: 5
- Drempel voor voorraadverlies: -50

De verkoopbare hoeveelheid voor dit product is `75 (25 - (-50))` .

![ Aanpasbare Hoeveelheid van het Voorbeeld vóór toegelaten backorders ](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![ Aanpasbare Aantal van het Voorbeeld na toegelaten backorders ](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Wanneer klanten de beschikbare 25 producten aanschaffen, worden nieuwe bestellingen ingevoerd als backorders. Aangezien het Aankoopbare Aantal van het product tot 5 (70 punten zijn verkocht) vermindert, toont de _pagina van het Product_ een bericht `Only 5 left` op de winkel. Wanneer het Aankoopbare Aantal `0` bereikt, wordt het product weergegeven als `Out of Stock` in de winkel.

>[!NOTE]
>
>Wanneer een klant een bestelling plaatst met _[!UICONTROL backorder qty]_, trekt [!DNL Inventory Management] automatisch de hoeveelheid af van de verkoopbare hoeveelheid. Als een bestelling niet wordt verzonden en wordt geannuleerd, wordt de hoeveelheid teruggezet naar de geaggregeerde virtuele verkoopbare hoeveelheid. De **_geannuleerde ordehoeveelheid wordt niet toegewezen aan om het even welke bronnen_**, maar is teruggekeerd aan het totale aantal producten beschikbaar voor verkoop (_[!UICONTROL Salable Quantity]_ kolom op het productnet).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### Status van voorraad

Producten moeten de status `In Stock` hebben wanneer ze backorders inschakelen. U kunt deze waarde van de _pagina van het Product_ plaatsen. Voor multisource-producten moet ten minste één bron zijn gemarkeerd als `In Stock` . De toegang en plaatsen de status door de _pagina van het 0} Product {en toegewezen_ Bronnen _net._

## Globaal randapparatuur configureren

Deze stappen laten backorders voor alle producten op het plaatniveau toe.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Stel **[!UICONTROL Store View]** in op `Default Config` .

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Inventory]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]** uit.

1. Schakel voor **[!UICONTROL Backorders]** het selectievakje **[!UICONTROL Use system value]** uit en selecteer een optie:

   | Optie | Beschrijving |
   | -- | -- |
   | `No Backorders` | Achtergronden niet accepteren wanneer het product uit voorraad is. |
   | `Allow Qty Below 0` | Achtergronden accepteren wanneer het aantal minder dan nul is. |
   | `Allow Qty Below 0 and Notify Customer` | Achterorden accepteren wanneer het aantal minder is dan nul en de klant laten weten dat de bestelling nog steeds kan worden geplaatst. |

1. Schakel bij **[!UICONTROL Out-of-Stock Threshold]** het selectievakje **[!UICONTROL Use system value]** uit en voer een andere waarde in.

   | Waarde | Beschrijving |
   | -- | -- |
   | Positief bedrag | Voer een positieve waarde in als Achterorden uitgeschakeld is. |
   | Nul | Als Achterorden ingeschakeld is en u `0` invoert, zijn oneindige achterorden mogelijk. |
   | Negatief bedrag | Als Achterorden ingeschakeld, wordt u aangeraden een negatieve waarde in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` in om bestellingen tot dit bedrag toe te staan. |

1. Klik op **[!UICONTROL Save Config]**.

## Achterorden voor een product configureren

Configuraties op productniveau overschrijven algemene configuraties. U kunt backorders op productniveau willen vormen om de montages op het globale opslag of bronniveau met voeten te treden. Uw winkel biedt bijvoorbeeld wereldwijd ondersteuning voor backorders. Met productmontages, kunt u achterorden onbruikbaar maken of de drempel veranderen uit-van-voorraad zonder andere producten en bronnen te beïnvloeden.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open een product in de modus **[!UICONTROL Edit]** en schuif de pagina omlaag naar het gebied _[!UICONTROL Sources]_.

   Voor producten die zonder [!DNL Inventory Management] zijn geconfigureerd, wordt het tabblad niet weergegeven. De knop `Advanced Inventory` wordt weergegeven onder het veld _[!UICONTROL Quantity]_.

1. Klik op **[!UICONTROL Advanced Inventory]**.

   Deze actie toont een pagina van product-specifieke configuraties. Bij elke instelling die als `global` wordt vermeld, wordt de huidige algemene instelling voor de winkel weergegeven.

1. Schakel voor **[!UICONTROL Backorders]** het selectievakje **[!UICONTROL Use Config Setting]** uit en selecteer een optie:

   | Optie | Beschrijving |
   | -- | -- |
   | `No Backorders` | Achtergronden niet accepteren wanneer het product uit voorraad is. |
   | `Allow Qty Below 0` | Achtergronden accepteren wanneer het aantal minder dan nul is. |
   | `Allow Qty Below 0 and Notify Customer` | Achterorden accepteren wanneer het aantal minder is dan nul en de klant laten weten dat de bestelling nog steeds kan worden geplaatst. |

1. Schakel voor **[!UICONTROL Out-of-Stock Threshold]** het selectievakje **[!UICONTROL Use Config Setting]** uit en voer een waarde in:

   | Waarde | Beschrijving |
   | -- | -- |
   | Positief bedrag | Voer een positieve waarde in als Achterorden uitgeschakeld is. |
   | Nul | Als Achterorden ingeschakeld is en u `0` invoert, zijn oneindige achterorden mogelijk. |
   | Negatief bedrag | Als Achterorden ingeschakeld, wordt u aangeraden een negatieve waarde in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` in om bestellingen tot dat bedrag toe te staan. |

   ![ Geavanceerde die Inventaris voor Achterorden ](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"} wordt gevormd

1. Klik op **[!UICONTROL Done]** en vervolgens op **[!UICONTROL Save]** .
