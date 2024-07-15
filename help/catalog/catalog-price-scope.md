---
title: Prijsbereik
description: Leer over de werkingsfeer die voor productprijzen wordt gebruikt, die kan worden gevormd om op of globaal of websiteniveau van toepassing te zijn.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Prijsbereik

Het werkingsgebied van de [ basismunt ](../stores-purchase/currency-configuration.md) die voor productprijzen wordt gebruikt kan worden gevormd om op of globaal of websiteniveau van toepassing te zijn. Indien toegepast op het algemene niveau, wordt dezelfde prijs gebruikt in de hele winkelhiërarchie. Als hetzelfde product wordt toegepast op het niveau van de website, kan het voor verschillende prijzen beschikbaar zijn dan in winkels die bij verschillende websites horen. Standaard is het bereik van productprijzen wereldwijd.

Verschillende factoren kunnen van invloed zijn op de prijs van hetzelfde product op de ene locatie en niet op een andere. Er kunnen bijvoorbeeld extra distributiekosten voor het product zijn en andere overwegingen die van invloed zijn op de prijs van producten die in een specifieke winkel worden verkocht. In het volgende diagram ziet u een installatie op meerdere locaties met de basisvaluta ingesteld op websiteniveau. De winkels en winkelweergaven die aan elke website zijn gekoppeld, weerspiegelen de productprijzen die op websiteniveau zijn ingesteld.

![ Adobe Commerce B2B ](../assets/b2b.svg) als u gedeelde catalogi gebruikt, verwijs ook naar [ Vastgestelde gedeelde catalogusprijs en structuur ](../b2b/catalog-shared-pricing-structure.md) in de _B2B Gids van Adobe Commerce_.

![ diagram van het werkingsgebied van de Prijs ](./assets/catalog-price-scope.svg){width="550"}

## Prijsbereik configureren

1. Voor het _Admin_ menu, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Blader omlaag naar de sectie **[!UICONTROL Price]** en stel **[!UICONTROL Catalog Price Scope]** in op een van de volgende opties:

   - `Global`
   - `Website`

   De gekozen bereikinstelling wordt weergegeven onder prijsvelden in de catalogus.

   ![ het prijswerkingsgebied van de Catalogus ](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Bereik gebruiken om productprijzen in te stellen

Commerce staat het niet toe dat voor elke winkel een productprijs wordt vastgesteld. Maar u kunt de prijs per website wijzigen:

1. Voor het _Admin_ menu, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Stel op het tabblad **[!UICONTROL Price]** het prijsbereik in op `Website` in plaats van op global.

1. Stel de prijs in door de productbewerkingspagina te openen, het bereik linksboven te selecteren en vervolgens een nieuwe prijs per website in te voeren.
