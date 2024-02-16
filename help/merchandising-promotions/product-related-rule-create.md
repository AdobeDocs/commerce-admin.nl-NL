---
title: Een regel voor een verwant product maken
description: Leer hoe u een gerelateerde productregel maakt die kan worden geactiveerd voor het weergeven van verwante producten, upsells en cross-sells.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Een regel voor een verwant product maken

{{ee-feature}}

Het proces om een verwante productregel tot stand te brengen is gelijkaardig aan het opzetten van een prijsregel. Eerst definieert u de voorwaarden die moeten overeenkomen en vervolgens kiest u de producten die u wilt weergeven. Op elk moment kunnen er verschillende actieve regels zijn die kunnen worden geactiveerd om verwante producten, upsells en cross-sells weer te geven. De prioriteit van elke regel bepaalt de volgorde waarin het productblok op de pagina wordt weergegeven.

>[!NOTE]
>
>Voor een attribuut dat in een gerichte regel moet worden gebruikt, [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) eigenschap moet worden ingesteld op `Yes`.

>[!NOTE]
>
>De `All Store Views` bereikwaarde wordt altijd gebruikt voor beide [!UICONTROL Products to Match] en [!UICONTROL Products to Display] voorwaarden voor alle productkenmerken. Dit is ook van toepassing wanneer de productkenmerken verschillende waarden hebben voor verschillende winkelweergaven en websites.

## Een regel voor een verwant product maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Rule]**.

   ![Regel voor verwante producten - informatie](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Voltooi de **[!UICONTROL Rule Information]** als volgt:

   - Voer een **[!UICONTROL Rule Name]** om de regel te identificeren wanneer u in de Admin werkt.

   - Voor **[!UICONTROL Priority]** Voer een getal in dat de volgorde bepaalt waarin de resultaten op de pagina worden weergegeven wanneer de resultaten van andere regels op dezelfde locatie worden toegepast. Getal `1` is de hoogste prioriteit.

   - Om de regel toe te laten, reeks **[!UICONTROL Status]** tot `Active`.

   - Set **[!UICONTROL Apply To]** op een van de volgende wijzen:

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Als de regel voor een specifieke tijdspanne actief moet zijn, ga binnen **[!UICONTROL From]** en **[!UICONTROL To]** datums.

   - Voor **[!UICONTROL Result Limit]**, voert u het aantal records in dat in de resultatenlijst moet worden weergegeven. Het maximumaantal is 20.

   - Als de regel van toepassing is op een specifieke [klantensegment](../customers/customer-segments.md), set **[!UICONTROL Customer Segments]** tot `Specified` en kies het klantensegment van de lijst.

   - (**Beta**) Als de regel van toepassing is op een specifieke [Real-Time CDP-publiek](../customers/audience-activation.md), set **[!UICONTROL Real-Time CDP Audience]** tot `Specified` en kiest u het Real-Time CDP-publiek in de lijst. Deze functie is in bèta. Als u wilt deelnemen aan het bètaprogramma, verzendt u een aanvraag naar [dataconnection@adobe.com](mailto:dataconnection@adobe.com).

     ![Regel voor verwante producten - Real-Time CDP-publiek](./assets/rtcdp-related-products.png){width="500"}

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Products to Match]** en de voorwaarden te creëren zoals u zou willen [catalogusprijsregel](price-rules-catalog.md).

   ![Regel voor verwante producten - producten die met elkaar overeenkomen](./assets/catalog-related-products-match.png){width="500"}

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Products to Display]** en bouwt u de resultaten op zoals u voor een [catalogusprijsregel](price-rules-catalog.md).

   ![Regel voor verwante producten - weer te geven producten](./assets/catalog-related-products-to-display.png){width="500"}

   Voltooi de voorwaarde om de producten te beschrijven die u in de getoonde resultaten wilt omvatten.

1. Klik op **[!UICONTROL Save]**.

## Een regel voor een verwant product verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Zoek de regel met verwante producten die u wilt verwijderen.

1. Klik op de regel om de detailpagina te openen.

1. Klik in de rechterbovenhoek op **[!UICONTROL Delete]**.

1. Klik op **[!UICONTROL OK]**.

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
