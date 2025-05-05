---
title: Verwante productregels
description: Leer over verwante productregels en hoe zij worden gebruikt om verwante producten dynamisch voor te stellen, omhoog-verkoopt, en dwars-verkoopt aan uw klanten.
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Regels voor verwante producten (doelregels)

{{ee-feature}}

De verwante productregels geven u de capaciteit om de selectie van producten te richten die aan klanten als verwante producten worden voorgesteld, omhoog-verkoopt, en dwars-verkoopt. Elke productregel kan met a [ klantensegment ](../customers/customer-segments.md) worden geassocieerd om een dynamische vertoning van gerichte handel te veroorzaken.

Aangezien verscheidene actieve regels tezelfdertijd kunnen worden teweeggebracht, kunt u een prioriteit voor elke regel plaatsen. Het bepaalt de orde waarin de regels worden toegepast en de producten op de pagina worden getoond.

Ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**&#x200B;om de verwante productregels te openen.

![ Verwante lijst van productregels ](./assets/related-products-rules.png){width="700" zoomable="yes"}

## Kolombeschrijvingen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke id die aan elke gerelateerde productregel is toegewezen |
| [!UICONTROL Rule] | De naam van de verwante productregel |
| [!UICONTROL Start] | Gebruik de dynamische kalendergebieden (_[!UICONTROL To:]_&#x200B;en&#x200B;_[!UICONTROL From:]_) om de lijst te filtreren die op de begindatum voor de regel wordt gebaseerd zoals die werd bepaald toen de regel werd gecreeerd. |
| [!UICONTROL End] | Gebruik de dynamische kalendergebieden (_[!UICONTROL To:]_&#x200B;en&#x200B;_[!UICONTROL From:]_) om de lijst te filtreren die op de einddatum voor de regel wordt gebaseerd zoals die werd bepaald toen de regel werd gecreeerd. |
| [!UICONTROL Priority] | Typ tekst in dit veld om de lijst te filteren op basis van de prioriteit die voor een regel is gedefinieerd. |
| [!UICONTROL Applies To] | Met deze optie filtert u de lijst met regels die van toepassing zijn op `Related Products` , `Up-sells` en `Cross-sells` . |
| [!UICONTROL Status] | Gebruik deze optie om de lijst te filteren op regelstatus (`Active` of `Inactive`). |

{style="table-layout:auto"}

## Prioriteit regel

Op elk moment kunnen er verschillende actieve regels zijn die kunnen worden geactiveerd om verwante producten, upsells en cross-sells weer te geven. De prioriteit van elke regel bepaalt de volgorde waarin de producten op de pagina worden weergegeven. De waarde kan op elk geheel getal worden ingesteld, waarbij `1` de hoogste prioriteit heeft.

Het aantal product-id&#39;s dat in een regel voor productrelaties kan worden opgenomen, wordt bepaald door de `Result Limit` -waarde, die maximaal 20 is. De `Result Limit` -waarde, in combinatie met de `Configurable Maximum` voor de specifieke op regels gebaseerde productbevordering, wordt de `Real Limit` -waarde en bepaalt het werkelijke aantal overeenkomende producten dat in de lijst kan worden weergegeven.

[ Resultaatgrens ] + [ configureerbare Maximum ] = [ Echte Grens ]

Stel dat u bijvoorbeeld drie regels hebt met een prioriteit `1` , `2` en `3` .

- Er zijn twee passende producten die voor _Regel 1_ zijn teruggekeerd, zes passende producten voor _Regel 2_, en 20 passende producten voor _Regel 3_.
- In de configuratie wordt _[!UICONTROL Maximum Number of Products for Related Products List]_&#x200B;ingesteld op `6` .

  | Regels | Prioriteit | Overeenkomende producten |
  |---|---|-----|
  | Artikel 1 | `1` | `2` |
  | Artikel 2 | `2` | `6` |
  | Artikel 3 | `3` | `20` |

Als de eerste regel meer passende producten terugkeert dan toegestaan door de _configureerbare maximumgrens_, maar minder dan de _echte grens_, worden de passende producten van de andere regels gebruikt (in volgorde van prioriteit) tot de _echte grens_ wordt bereikt.

Door prioriteit, kunnen de passende producten die van _worden teruggekeerd Regel 1_ eerst worden gebruikt om alle 26 beschikbare groeven te vullen. Omdat Regel 1 slechts twee passende producten terugbracht, is er nog ruimte voor 24 meer. _Regel 2_ heeft de volgende hoogste prioriteit, en keert zes meer passende producten terug. Er zijn nu 18 beschikbare sleuven die moeten worden ingevuld. _Regel 3_ heeft het volgende niveau van prioriteit, met genoeg passende producten om de resterende 18 groeven te vullen. Wanneer alle beschikbare groeven worden gevuld, en afhankelijk van de omwentelingswijze die wordt geplaatst, zouden de producten door identiteitskaart binnen elke prioriteit kunnen worden willekeurige volgorde geplaatst of worden bevolen en dan tot de configureerbare maximumgrens worden verminderd. In dit geval worden de resterende zes producten in de winkel weergegeven.

>[!NOTE]
>
>De geselecteerde producten worden altijd getoond vóór de op regel-gebaseerde producten ongeacht de omwentelingswijze.

## Op regels gebaseerde productrelaties configureren

Het gedrag van de regels van de productverhouding en de vertoning van aangepaste producten worden bepaald door de configuratiemontages. Deze montages bepalen hoeveel van de producten die de regel aanpassen kunnen worden getoond en de orde waarin zij verschijnen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het deelvenster aan de linkerkant **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** onder.

1. Breid ![ Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Rules-Based Product Relations]** sectie.

   ![ configuratie van de Catalogus - op regel-gebaseerde productbetrekkingen ](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. Voer de **[!UICONTROL Maximum Number of Products in the Related Products List]** in.

1. Stel **[!UICONTROL Show Related Products]** in op een van de volgende opties:

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. Stel **[!UICONTROL Rotation Mode for Products in Related Product List]** in op een van de volgende opties:

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. Ga als volgt te werk om de instellingen voor cross-sell-producten te voltooien:

   - Voer de **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]** in.

   - Stel **[!UICONTROL Show Cross-Sell Products]** in op een van de volgende opties:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Stel **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** in op een van de volgende opties:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Ga als volgt te werk om de up-sell-productinstellingen te voltooien:

   - Voer de **[!UICONTROL Maximum Number of Products in the Upsell Product List]** in.

   - Stel **[!UICONTROL Show Upsell Products]** in op een van de volgende opties:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Stel **[!UICONTROL Rotation Mode for Products in Upsell Product List]** in op een van de volgende opties:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Rotatiemodi

| Modus | Beschrijving |
|---|---|
| [!UICONTROL By Priority, Then by ID] | De producten worden gesorteerd door prioriteit en dan opnieuw geordend door identiteitskaart binnen elke prioriteit. De producten van lagere prioritaire regel verschijnen slechts wanneer zij geen producten van hogere prioritaire regel worden verlaten om de beschikbare groeven te vullen. |
| [!UICONTROL By Priority, Then Random] | De producten worden gesorteerd door prioriteit en dan gerandomiseerd binnen elke prioriteit. De producten van lagere prioritaire regel verschijnen slechts wanneer zij geen producten van hogere prioritaire regel worden verlaten om de beschikbare groeven te vullen. |
| [!UICONTROL Weighted Random] | De producten worden gerandomiseerd zodat producten die tot een regel met een hogere prioriteit behoren, een grotere kans hebben om te verschijnen dan producten die tot een regel met een lagere prioriteit behoren. De producten worden dan verminderd tot de configureerbare maximumgrens en door prioriteit opnieuw gegroepeerd. Deze wijze geeft een kans aan producten van lagere prioriteit om soms te verschijnen zelfs als de resterende groeven met producten van regel met hogere prioriteit konden worden gevuld |

{style="table-layout:auto"}

## Real-Time CDP-publiek gebruiken om gerelateerde productregels te informeren

>[!NOTE]
>
>Deze functie is in bèta. Als u zich bij het bètaprogramma zou willen aansluiten, verzend een verzoek aan [ dataconnection@adobe.com ](mailto:dataconnection@adobe.com).


Leer hoe te [&#128279;](../customers/audience-activation.md) publiek van Real-Time CDP in uw instantie van Adobe Commerce te activeren om verwante productregels mee te delen.
