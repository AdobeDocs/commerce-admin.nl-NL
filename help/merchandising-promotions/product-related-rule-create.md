---
title: Een regel voor een verwant product maken
description: Leer hoe u een gerelateerde productregel maakt die kan worden geactiveerd voor het weergeven van verwante producten, upsells en cross-sells.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: cea943cd7f4d148c885fbd113c3bc08bfdf63ea0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Een regel voor een verwant product maken

{{ee-feature}}

Het proces om een verwante productregel tot stand te brengen is gelijkaardig aan het opzetten van een prijsregel. Eerst definieert u de voorwaarden die moeten overeenkomen en vervolgens kiest u de producten die u wilt weergeven. Op elk moment kunnen er verschillende actieve regels zijn die kunnen worden geactiveerd om verwante producten, upsells en cross-sells weer te geven. De prioriteit van elke regel bepaalt de volgorde waarin het productblok op de pagina wordt weergegeven.

>[!NOTE]
>
>Voor een kenmerk dat in een doelregel moet worden gebruikt, moet de eigenschap [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) op `Yes` worden ingesteld.

>[!NOTE]
>
>De waarde `All Store Views` scope wordt altijd gebruikt voor zowel [!UICONTROL Products to Match] als [!UICONTROL Products to Display] -voorwaarden voor alle productkenmerken. Dit is ook van toepassing wanneer de productkenmerken verschillende waarden hebben voor verschillende winkelweergaven en websites.

## Een regel voor een verwant product maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Rule]** .

   ![ Verwante productregel - informatie ](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Voltooi **[!UICONTROL Rule Information]** als volgt:

   - Voer een **[!UICONTROL Rule Name]** in om de regel te identificeren wanneer u in Beheer werkt.

   - Voer bij **[!UICONTROL Priority]** een getal in dat de volgorde bepaalt waarin de resultaten op de pagina worden weergegeven wanneer de resultaten van andere regels op dezelfde locatie betrekking hebben. Number `1` is top priority.

   - Stel **[!UICONTROL Status]** in op `Active` om de regel in te schakelen.

   - Stel **[!UICONTROL Apply To]** in op een van de volgende opties:

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Als de regel voor een bepaald tijdsbereik actief moet zijn, voert u de **[!UICONTROL From]** - en **[!UICONTROL To]** -datums in.

   - Voer bij **[!UICONTROL Result Limit]** het aantal records in dat in de resultatenlijst moet worden weergegeven. Het maximumaantal is 20.

   - Als de regel op een specifiek [ klantensegment ](../customers/customer-segments.md) van toepassing is, plaats **[!UICONTROL Customer Segments]** aan `Specified` en kies het klantensegment van de lijst.

   - Als de regel op een specifiek [ publiek van Real-Time CDP ](../customers/audience-activation.md) van toepassing is, plaats **[!UICONTROL Real-Time CDP Audience]** aan `Specified` en kies het publiek van Real-Time CDP van de lijst. Deze functie is in bèta. Als u zich bij het bètaprogramma zou willen aansluiten, verzend een verzoek aan [ dataconnection@adobe.com ](mailto:dataconnection@adobe.com).

     ![ Verwante productregel - het publiek van Real-Time CDP ](./assets/rtcdp-related-products.png){width="500"}

1. In het linkerpaneel, kies **[!UICONTROL Products to Match]** en bouw de voorwaarden zoals u voor de regel van de a [ catalogusprijs ](price-rules-catalog.md) zou.

   ![ Verwante productregel - producten om ](./assets/catalog-related-products-match.png){width="500"} aan te passen

1. In het linkerpaneel, kies **[!UICONTROL Products to Display]** en bouw de resultaatvoorwaarden zoals u voor de regel van de a [ catalogusprijs ](price-rules-catalog.md) zou.

   ![ Verwante productregel - producten aan vertoning ](./assets/catalog-related-products-to-display.png){width="500"}

   Voltooi de voorwaarde om de producten te beschrijven die u in de getoonde resultaten wilt omvatten.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Een regel voor een verwant product verwijderen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Zoek de regel met verwante producten die u wilt verwijderen.

1. Klik op de regel om de detailpagina te openen.

1. Klik in de rechterbovenhoek op **[!UICONTROL Delete]** .

1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

## Demo van regel voor verwante producten

Bekijk deze video voor meer informatie over het maken van verwante productregels:

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Rule Name] | Een naam die de regel voor intern gebruik identificeert. |
| [!UICONTROL Priority] | Bepaalt de opeenvolging waarin de resultaten van de regel verschijnen wanneer getoond met andere reeksen resultaten die de zelfde plaats op de pagina richten. De waarde kan aan om het even welk geheel aantal, met de hoogste prioriteit van 1 worden geplaatst. Als er bijvoorbeeld meerdere Up-sell-regels van toepassing zijn, wordt de regel met de hoogste prioriteit vóór de andere regels weergegeven. De sorteervolgorde van de producten binnen elke set resultaten is willekeurig. Alle up-sell, dwars-verkoop, en verwante producten die manueel werden gevormd verschijnen altijd op de pagina vóór om het even welke op regel-gebaseerde productpromoties. |
| [!UICONTROL Status] | Controls the active status of the rule. Opties: `Active` / `Inactive` |
| [!UICONTROL Apply To] | Identificeert het type van productverhouding die met de regel wordt geassocieerd. Opties: `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | Als de regel voor een waaier van tijd actief is, bepaalt dit het plaatsen de eerste datum de regel actief is. |
| [!UICONTROL To Date] | Als de regel voor een waaier van tijd actief is, bepaalt dit het plaatsen de laatste datum de regel actief is. |
| [!UICONTROL Result Limit] | Hiermee bepaalt u het aantal producten dat in één keer in de resultaten wordt weergegeven. Het maximumaantal is 20. Als er meer overeenkomende resultaten worden gevonden, roteren de producten door het blok telkens wanneer de pagina wordt vernieuwd. |
| [!UICONTROL Customer Segments] | Identificeert de klantensegmenten waarop de regel van toepassing is. Opties: `All` / `Specified` |

{style="table-layout:auto"}
