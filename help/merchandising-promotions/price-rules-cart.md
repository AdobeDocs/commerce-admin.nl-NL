---
title: Prijsregels voor winkelwagentjes
description: Meer informatie over de regels voor winkelprijzen die kortingen toepassen op objecten in het winkelwagentje op basis van een aantal voorwaarden.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Prijsregels voor winkelwagentjes

Met de prijsregels voor winkelwagentjes worden op basis van een aantal voorwaarden kortingen toegepast op objecten in het winkelwagentje. De korting kan automatisch worden toegepast wanneer aan de voorwaarden wordt voldaan of wanneer de klant een geldige couponcode invoert. Als deze korting wordt toegepast, wordt deze in het winkelwagentje weergegeven onder het subtotaal. Een prijsregel voor winkelwagentjes kan worden gebruikt wanneer dat nodig is voor een seizoen of promotie door de status en het datumbereik ervan te wijzigen.

>[!NOTE]
>
>Als de regel voor het couponwinkelwagentje voorwaarden bevat die afhandelingsopties specificeren, zoals bepaalde verzend- of betalingsmethoden, wordt alleen aan de voorwaarden voldaan bij afhandeling nadat de specifieke verzend-/betalingsmethoden zijn geselecteerd. In dit geval kan de coupon worden toegepast bij afhandeling in de laatste stap.

![ Voorbeeld storefront - kart past coupon toe ](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Toegangsprijsregels

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![ de prijsregel van de Kar ](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Als u veel regels hebt, gebruikt u de filteropties boven aan elke kolom om de lijst te stroomlijnen en klikt u op **[!UICONTROL Search]** om de filters toe te passen.

1. Als u alle filteropties wilt wissen en de volledige lijst wilt weergeven, klikt u op **[!UICONTROL Reset Filter]** .

1. Eigenschappen voor een regel bijwerken:

   - ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) klik **[!UICONTROL Edit]** om de pagina van de Informatie van de Regel te tonen.

   - ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) klik de regel in de lijst om de pagina van de Informatie van de Regel te tonen.

   Daar kunt u de montages voor de regel (gelijkend op het creëren van een regel) veranderen.

## Filteropties per kolom

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Voer tekst in om de lijst voor een specifiek regel-id-nummer te filteren. |
| [!UICONTROL Rule] | Voer tekst in om de lijst te filteren op basis van de regelnaam die is gedefinieerd toen de regel werd gemaakt. |
| [!UICONTROL Coupon Code] | Voer tekst in om de lijst te filteren op basis van de codenaam die is gedefinieerd toen de regel werd gemaakt. |
| [!UICONTROL Priority] | Vrije-tekstveld dat de lijst filtert op basis van de prioriteit die voor een regel is gedefinieerd. |
| [!UICONTROL Status] | Gebruik deze optie om de lijst te filteren op regelstatus (`Active` of `Inactive`). |
| [!UICONTROL Web Site] | Met deze optie filtert u de lijst op basis van websites die voor een regel zijn gedefinieerd. |
| [!UICONTROL Action] | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) klik **[!UICONTROL Edit]** om de _[!UICONTROL Rule Information]_pagina te tonen en de regelmontages (gelijkend op het creëren van een regel) bij te werken. |
| [!UICONTROL Start] | ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) Gebruik de dynamische kalendergebieden (_[!UICONTROL To:]_en_[!UICONTROL From:]_) om de lijst te filtreren die op de begindatum voor de regel wordt gebaseerd zoals die werd bepaald toen de regel werd gecreeerd. |
| [!UICONTROL End] | ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts) Gebruik de dynamische kalendergebieden (_[!UICONTROL To:]_en_[!UICONTROL From:]_) om de lijst te filtreren die op de einddatum voor de regel wordt gebaseerd zoals die toen de regel werd gecreeerd. |

{style="table-layout:auto"}

## Real-Time CDP-publiek gebruiken om regels voor de kartprijs te informeren

Leer hoe te [ ](../customers/audience-activation.md) het publiek van Real-Time CDP in uw instantie van Adobe Commerce te activeren om de regels van de wortelprijs te informeren.
