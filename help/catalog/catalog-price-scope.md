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

Het toepassingsgebied van de [basisvaluta](../stores-purchase/currency-configuration.md) die voor productprijzen wordt gebruikt, kan worden geconfigureerd om op globaal niveau of op het niveau van de website van toepassing te zijn. Indien toegepast op het algemene niveau, wordt dezelfde prijs gebruikt in de hele winkelhiërarchie. Als hetzelfde product wordt toegepast op het niveau van de website, kan het voor verschillende prijzen beschikbaar zijn dan in winkels die bij verschillende websites horen. Standaard is het bereik van productprijzen wereldwijd.

Verschillende factoren kunnen van invloed zijn op de prijs van hetzelfde product op de ene locatie en niet op een andere. Er kunnen bijvoorbeeld extra distributiekosten voor het product zijn en andere overwegingen die van invloed zijn op de prijs van producten die in een specifieke winkel worden verkocht. In het volgende diagram ziet u een installatie op meerdere locaties met de basisvaluta ingesteld op websiteniveau. De winkels en winkelweergaven die aan elke website zijn gekoppeld, weerspiegelen de productprijzen die op websiteniveau zijn ingesteld.

![Adobe Commerce B2B](../assets/b2b.svg) Als u gedeelde catalogi gebruikt, raadpleegt u ook [Prijsbepaling en structuur van gedeelde catalogus instellen](../b2b/catalog-shared-pricing-structure.md) in de _Adobe Commerce B2B-gids_.

![Prijsbereikdiagram](./assets/catalog-price-scope.svg){width="550"}

## Prijsbereik configureren

1. Op de _Beheerder_ menu, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. Omlaag schuiven naar de **[!UICONTROL Price]** sectie en set **[!UICONTROL Catalog Price Scope]** op een van de volgende wijzen:

   - `Global`
   - `Website`

   De gekozen bereikinstelling wordt weergegeven onder prijsvelden in de catalogus.

   ![Omvang catalogusprijs](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Bereik gebruiken om productprijzen in te stellen

Commerce staat het niet toe dat voor elke winkel een productprijs wordt vastgesteld. Maar u kunt de prijs per website wijzigen:

1. Op de _Beheerder_ menu, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Catalog]** onder.

1. In de **[!UICONTROL Price]** tab, prijsbereik instellen op `Website` in plaats van wereldwijd.

1. Stel de prijs in door de productbewerkingspagina te openen, het bereik linksboven te selecteren en vervolgens een nieuwe prijs per website in te voeren.
