---
title: Configureren  [!DNL Inventory Management]
description: Leer over de configuratie van  [!DNL Inventory Management]  opties die bronbeschikbaarheid, storefront producten, en ordeverzending bepalen.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Configureren [!DNL Inventory Management]

De module [!DNL Inventory Management] ondersteunt de configuratie-instellingen voor voorraden op product- en globaal niveau en biedt ook extra instellingen die de beschikbaarheid van de bron, de winkelproducten en de verzending van bestellingen beïnvloeden. De configuratie-instellingen gelden voor:

- De hele catalogus: Ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Vouw vervolgens **[!UICONTROL Catalog]**&#x200B;in het linkerdeelvenster uit en selecteer **[!UICONTROL Inventory]**.

- Specifieke producten: Ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]** . Open vervolgens het product in de bewerkingsmodus en klik op **[!UICONTROL Advanced Inventory]** in de sectie _[!UICONTROL Sources]_.

Uw catalogus kan worden geconfigureerd om inventarisgegevens weer te geven in uw winkel, actieve winkelwagentjes te beheren en nog veel meer. Toon de beschikbaarheid van elk punt als _in Voorraad_ of _uit Voorraad_ en de beschikbare inventaris wanneer de voorraad laag is.

De drempel voor het niet-bestand geeft aan wanneer een product opnieuw moet worden geordend, wordt afgetrokken van de Salable Quantity voor een voorraad en kan worden ingesteld op ondersteuning van in- of uitgeschakeld backorders. Geef uw winkel een backorder en stel een maximale hoeveelheid bestellingen in voor alle of voor bepaalde producten.

Een andere manier u de drempel van de voorraadbeschikbaarheid kunt gebruiken is producten te beheren die in hoge vraag zijn. Als je nieuwe klanten wilt vastleggen in plaats van ze aan kopers met een grote hoeveelheid te verkopen, kun je een maximumhoeveelheid instellen om te voorkomen dat één koper je hele voorraad opneemt.

![ Voorbeeld van in Voorraad, slechts 1 verlaten ](assets/storefront-stock-options-1-left.png)

## Configuratieopties

[!DNL Commerce] biedt ondersteuning voor de volgende configuraties voor het beheer van producten, voorraden, meldingen en meer. [!DNL Commerce] biedt aanvullende configuratie-instellingen voor bulkacties en het algoritme voor de prioriteit Afstand.

| Optie | Beschrijving |
|--|--|
| [!UICONTROL Manage Stock] | Hiermee kan [!DNL Commerce] alle voorraad beheren. Stel in of voorraadbeheer wordt gebruikt voor dit product of voor alle producten in [!DNL Commerce] . Hiermee geeft u meer opties weer wanneer u deze instelt op `Yes` . |
| [!UICONTROL Only X left Threshold] | Hiermee stelt u een hoeveelheid in die wordt gemeld wanneer een bepaald bedrag beschikbaar blijft voor aankoop. Dit bedrag wordt bijgehouden op voorraadniveau. |
| [!UICONTROL Out-of-Stock Threshold] | Uw veiligheidsvoorraad, Hoeveelheid om een kennisgeving uit de voorraad op te roepen en het risico van voorraadvorming te beperken. Deze waarde is van invloed op de backorders. Opties:<br />**[!UICONTROL No Backorders]**: Accepteert geen backorders wanneer het product uit voorraad is.<br />**[!UICONTROL Allow Qty Below 0]**: accepteert backorders wanneer het aantal kleiner is dan nul.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: accepteert backorders wanneer het aantal kleiner is dan nul, maar waarschuwt klanten dat orders nog steeds kunnen worden geplaatst.<br /><br />**[!UICONTROL Backorders disabled]**: u kunt het beste een positieve waarde groter dan 0 invoeren, zoals 5 of 25. <br/>**[!UICONTROL Backorders enabled]**: voer een negatieve drempelwaarde in voor de maximale hoeveelheid toegestane backorders, zoals -5 of -25. De waarde 0 fungeert als oneindige voorraad. Een positieve waarde wordt genegeerd en behandeld als 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Hiermee stelt u de minimale hoeveelheid van het product in die in één bestelling kan worden aangeschaft. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Hiermee stelt u de maximale hoeveelheid van het product in die in één bestelling kan worden aangeschaft. |
| [!UICONTROL Qty Uses Decimals] | Staat decimale hoeveelheden toe in plaats van hele getallen voor de hoeveelheid van een product. Deze instelling is handig voor producten die worden verkocht op basis van gewicht, volume of lengte. Opgegeven op het niveau van Source, berekend op het voorraadniveau op basis van toegewezen bronnen. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Hiermee wordt bepaald of onderdelen van een product afzonderlijk kunnen worden verzonden. Deze optie is zichtbaar wanneer **[!UICONTROL Qty Uses Decimals]** = `Yes` . |
| [!UICONTROL Backorders] | Hiermee geeft u aan of Achterorden zijn toegestaan. Opgegeven op het niveau van Source, berekend op het voorraadniveau op basis van toegewezen bronnen. Als toegelaten om backorders toe te staan, wordt het plaatsen van een negatieve waarde voor de Drempel uit-van-voorraad (zie [ het Vormen Achterorden ](backorders.md)) geadviseerd. Opties:<br />**[!UICONTROL No Backorders]**: Accepteert geen backorders wanneer het product uit voorraad is.<br />**[!UICONTROL Allow Qty Below 0]**: accepteert backorders wanneer het aantal kleiner is dan nul.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: accepteert backorders wanneer het aantal kleiner is dan nul, maar waarschuwt klanten dat orders nog steeds kunnen worden geplaatst. |
| [!UICONTROL Notify for Quantity Below] | Hiermee stelt u de hoeveelheid in die een melding Hoeveelheid onder activeert, met waarschuwing voor een lage voorraad. Dit bedrag wordt in mindering gebracht op de verkoopbare hoeveelheid en niet op de voorraadhoeveelheid. |
| [!UICONTROL Enable Qty Increments] | Hiermee wordt bepaald of het product in hoeveelheden kan worden verkocht. Indien ingeschakeld, voert u de hoeveelheid producten in die u in stappen wilt aanschaffen. De verhogingen plaatsen hoeveel productpunten als één enkel product, en als kind van configureerbare, gegroepeerde en bundelproducten moeten worden gekocht. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] gebruikt deze waarde niet. Wanneer u een retour- of creditnota voltooit, wordt de producthoeveelheid automatisch teruggestuurd naar de desbetreffende bronhoeveelheid. Zie [ het Vormen de Opties van het Product ](product-options.md). |

## De daling van de configuratie en overerving

Configuraties overschrijven of toepassen in het volgende overervingspad: de sectie Product _[!UICONTROL Sources]_&#x200B;heeft voorrang op de&#x200B;_[!UICONTROL Advanced Options]_ algemene _[!UICONTROL Inventory]_&#x200B;winkelconfiguratie van Product.

Wanneer [!DNL Commerce] controleert of er aangepaste instellingen worden toegepast, volgt deze volgorde:

1. Controleert op aangepaste instellingen op productniveau in de sectie _[!UICONTROL Sources]_. Er zijn enkele instellingen beschikbaar.

1. Controleert de productinstellingen _[!UICONTROL Advanced Inventory]_.

1. Als `Use Config Settings` voor de productmontages wordt geselecteerd, controleert het een waarde van de globale _pagina van de de opslagconfiguratie van de Inventaris_.

Bijvoorbeeld, kon u backorders verschillend over uw opslag vormen met een configuratie gelijkend op het volgende:

- _globaal:_ laat backorders voor de opslag toe, plaats de Drempel uit-van-voorraad aan `-50`

- _Product:_ maak backorders voor een specifiek product onbruikbaar, de vastgestelde Drempel uit-van-voorraad aan `10`
