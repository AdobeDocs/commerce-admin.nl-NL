---
title: "Configureren [!DNL Inventory Management]"
description: Meer informatie over de configuratie van [!DNL Inventory Management] opties die bronbeschikbaarheid, opslagproducten, en ordeverzending bepalen.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# Configureren [!DNL Inventory Management]

De [!DNL Inventory Management] de module steunt de montages van de inventarisconfiguratie op het product en globaal niveau en verstrekt ook extra montages die bronbeschikbaarheid, opslagproducten, en ordeverzending beïnvloeden. De configuratie-instellingen gelden voor:

- De hele catalogus: Ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Vouw vervolgens uit **[!UICONTROL Catalog]**in het linkerdeelvenster en selecteer **[!UICONTROL Inventory]**.

- Specifieke producten: Ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Open vervolgens het product in de bewerkingsmodus en klik op **[!UICONTROL Advanced Inventory]** in de _[!UICONTROL Sources]_sectie.

Uw catalogus kan worden geconfigureerd om inventarisgegevens weer te geven in uw winkel, actieve winkelwagentjes te beheren en nog veel meer. De beschikbaarheid van elk item weergeven als _In voorraad_ of _Uit voorraad_ en de beschikbare voorraad wanneer de voorraad laag is.

De drempel voor het niet-bestand geeft aan wanneer een product opnieuw moet worden geordend, wordt afgetrokken van de Salable Quantity voor een voorraad en kan worden ingesteld op ondersteuning van in- of uitgeschakeld backorders. Geef uw winkel een backorder en stel een maximale hoeveelheid bestellingen in voor alle of voor bepaalde producten.

Een andere manier u de drempel van de voorraadbeschikbaarheid kunt gebruiken is producten te beheren die in hoge vraag zijn. Als je nieuwe klanten wilt vastleggen in plaats van ze aan kopers met een grote hoeveelheid te verkopen, kun je een maximumhoeveelheid instellen om te voorkomen dat één koper je hele voorraad opneemt.

![Voorbeeld van In voorraad, slechts 1 links](assets/storefront-stock-options-1-left.png)

## Configuratieopties

[!DNL Commerce] winkels en producten ondersteunen de volgende configuraties voor het beheer van producten, voorraden, meldingen en meer. [!DNL Commerce] verstrekt extra configuratiemontages voor bulkacties en het algoritme van de Prioriteit van de Afstand.

| Optie | Beschrijving |
|--|--|
| [!UICONTROL Manage Stock] | Inschakelen [!DNL Commerce] om alle voorraad te beheren. Instellen of voorraadbeheer wordt gebruikt voor dit product of voor alle producten in [!DNL Commerce]. Hiermee geeft u meer opties weer als ingesteld op `Yes`. |
| [!UICONTROL Only X left Threshold] | Hiermee stelt u een hoeveelheid in die wordt gemeld wanneer een bepaald bedrag beschikbaar blijft voor aankoop. Dit bedrag wordt bijgehouden op voorraadniveau. |
| [!UICONTROL Out-of-Stock Threshold] | Uw veiligheidsvoorraad, Hoeveelheid om een kennisgeving uit de voorraad op te roepen en het risico van voorraadvorming te beperken. Deze waarde is van invloed op de backorders. Opties:<br />**[!UICONTROL No Backorders]**: accepteert geen backorders wanneer het product uit voorraad is.<br />**[!UICONTROL Allow Qty Below 0]**: Accepteert backorders als de hoeveelheid onder nul daalt.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Accepteert backorders wanneer het aantal onder nul daalt, maar waarschuwt klanten dat de orden nog kunnen worden geplaatst.<br /><br />**[!UICONTROL Backorders disabled]**: U wordt aangeraden een positieve waarde groter dan 0 in te voeren, zoals 5 of 25. <br/>**[!UICONTROL Backorders enabled]**: Voer een negatieve drempelwaarde in voor de maximale hoeveelheid toegestane backorders, zoals -5 of -25. De waarde 0 fungeert als oneindige voorraad. Een positieve waarde wordt genegeerd en behandeld als 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Hiermee stelt u de minimale hoeveelheid van het product in die in één bestelling kan worden aangeschaft. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Hiermee stelt u de maximale hoeveelheid van het product in die in één bestelling kan worden aangeschaft. |
| [!UICONTROL Qty Uses Decimals] | Staat decimale hoeveelheden toe in plaats van hele getallen voor de hoeveelheid van een product. Deze instelling is handig voor producten die worden verkocht op basis van gewicht, volume of lengte. Gespecificeerd op het niveau van de bron, berekend op het niveau van de voorraad op basis van toegewezen bronnen. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Hiermee wordt bepaald of onderdelen van een product afzonderlijk kunnen worden verzonden. Deze optie is zichtbaar wanneer **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Hiermee geeft u aan of Achterorden zijn toegestaan. Gespecificeerd op het niveau van de bron, berekend op het niveau van de voorraad op basis van toegewezen bronnen. Indien ingeschakeld om achtergronden toe te staan, wordt een negatieve waarde voor de drempel voor Uit-van-voorraad ingesteld (zie [Backorders configureren](backorders.md)) wordt aanbevolen. Opties:<br />**[!UICONTROL No Backorders]**: accepteert geen backorders wanneer het product uit voorraad is.<br />**[!UICONTROL Allow Qty Below 0]**: Accepteert backorders als de hoeveelheid onder nul daalt.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Accepteert backorders wanneer het aantal onder nul daalt, maar waarschuwt klanten dat de orden nog kunnen worden geplaatst. |
| [!UICONTROL Notify for Quantity Below] | Hiermee stelt u de hoeveelheid in die een melding Hoeveelheid onder activeert, met waarschuwing voor een lage voorraad. Dit bedrag wordt in mindering gebracht op de verkoopbare hoeveelheid en niet op de voorraadhoeveelheid. |
| [!UICONTROL Enable Qty Increments] | Hiermee wordt bepaald of het product in hoeveelheden kan worden verkocht. Indien ingeschakeld, voert u de hoeveelheid producten in die u in stappen wilt aanschaffen. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] gebruikt deze waarde niet. Wanneer u een retour- of creditnota voltooit, wordt de producthoeveelheid automatisch teruggestuurd naar de desbetreffende bronhoeveelheid. Zie [Productopties configureren](product-options.md). |

## De daling van de configuratie en overerving

Configuraties overschrijven of toepassen in het volgende overervingspad: Product _[!UICONTROL Sources]_sectie overschrijft product_[!UICONTROL Advanced Options]_ overschrijvingen van algemeen _[!UICONTROL Inventory]_winkelconfiguratie.

Wanneer [!DNL Commerce] de controles voor douanemontages om toe te passen, volgt het deze orde:

1. Controleert op aangepaste instellingen op productniveau in het dialoogvenster _[!UICONTROL Sources]_sectie. Er zijn enkele instellingen beschikbaar.

1. Controleert het product _[!UICONTROL Advanced Inventory]_instellingen.

1. Indien `Use Config Settings` is geselecteerd voor de productinstellingen, wordt gecontroleerd op een waarde van de algemene _Inventaris_ opslagconfiguratiepagina.

Bijvoorbeeld, kon u backorders verschillend over uw opslag vormen met een configuratie gelijkend op het volgende:

- _Globaal:_ Achterorden voor de winkel inschakelen: Drempel voor out van voorraad instellen op `-50`

- _Product:_ Schakel backorders voor een specifiek product uit, stel Drempel voor out-of-stock in op `10`
