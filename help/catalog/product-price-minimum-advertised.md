---
title: Minimale geadverteerde prijs
description: Leer hoe u de functie voor minimale geadverteerde prijzen (MAP) kunt gebruiken om te blijven voldoen aan de vereisten van de fabrikant met betrekking tot speciale prijzen.
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# Minimale geadverteerde prijs

Het is handelaren soms verboden een prijs weer te geven die lager is dan de door de fabrikant voorgestelde detailhandelsprijs (MSRP). Met de MAP (Minimum Adverted Price) kunt u voldoen aan de vereisten van de fabrikant en uw klanten een betere prijs bieden. Omdat de vereisten per fabrikant verschillen, kunt u uw winkel zo configureren dat de werkelijke prijs niet wordt weergegeven op pagina&#39;s waarvoor dit niet is toegestaan.

De functie MAP voegt een speciale functie toe _Klik voor prijs_ koppeling in plaats van de normale productprijs. Als de prijs in uw winkel lager is dan de minimumprijs die voor dat product is ingesteld, zijn er twee manieren waarop de prijsgegevens op de winkel kunnen worden verwerkt. De eerste manier is dat de prijs niet wordt weergegeven. Als de koper op de knop _Klik voor prijs_ wordt alleen dan de werkelijke prijs zichtbaar waarvoor je het product verkoopt. De tweede manier is dat de lijst/marktprijs doorgehaald wordt weergegeven om te benadrukken dat je prijs lager is.

Bovendien kunt u met de functie MAP enkele verbeteringen voorstellen. Wanneer een klant bijvoorbeeld een dergelijk product aan zijn winkelwagentje toevoegt, wordt het niet naar de winkelwagentje omgeleid en worden er aanbiedingen weergegeven die de koper in staat stellen:

- Een object uit het winkelwagentje verwijderen (kan worden uitgevoerd als de koper alleen de prijs wil verduidelijken en nog geen aankoopbeslissing heeft genomen)

- Laat het in hun winkelwagentje liggen en blijf winkelen

- Doorgaan naar afhandeling

## MAP-logica

Sommige producten hebben prijzen die afhankelijk zijn van een geselecteerde optie, zoals aangepaste opties of eenvoudige producten met hun eigen SKU&#39;s en voorraadbeheer). Voor deze producten wordt de volgende logica toegepast, afhankelijk van de productsoort en de prijsstelling. De werkelijke prijs wordt gebruikt door orderbeheer, tools voor klantenbeheer en rapporten.

## MAP gebruiken met producttypen

| Producttype | Beschrijving |
|--- |--- |
| [eenvoudig](product-create-simple.md), [Virtueel](product-create-virtual.md) | De werkelijke prijs wordt niet automatisch weergegeven in de cataloguslijst en de productpagina&#39;s, maar wordt alleen opgenomen op basis van de [!UICONTROL Display Actual Price] instellen. Aangepaste optieprijzen worden normaal weergegeven. |
| [Gegroepeerd](product-create-grouped.md) | De prijzen van de bijbehorende eenvoudige producten worden niet automatisch weergegeven op de cataloguslijst en productpagina&#39;s, maar worden alleen opgenomen volgens de [!UICONTROL Display Actual Price] instellen. |
| [Configureerbaar](product-create-configurable.md) | De werkelijke prijs wordt niet automatisch weergegeven in de cataloguslijst en de productpagina&#39;s, maar wordt alleen opgenomen op basis van de [!UICONTROL Display Actual Price] instellen. Optieprijzen worden normaal weergegeven. |
| [Bundel](product-create-bundle.md) (met vaste prijs) | De werkelijke prijs wordt niet automatisch weergegeven op cataloguspagina&#39;s, maar wordt alleen opgenomen op basis van de [!UICONTROL Display Actual Price] instellen. De prijzen van bundelitems worden normaal weergegeven. MAP is niet beschikbaar voor bundelproducten met dynamische prijzen. |
| [Downloadbaar](product-create-downloadable.md) | De werkelijke prijs wordt niet automatisch weergegeven in de cataloguslijst en de productpagina&#39;s, maar wordt alleen opgenomen op basis van de [!UICONTROL Display Actual Price] instellen. De prijs voor elke downloadkoppeling wordt normaal weergegeven. |

{style="table-layout:auto"}

## KAART gebruiken met prijsinstellingen

| Prijsinstelling | Beschrijving |
|--- |--- |
| Voornaamste prijs | Wanneer MAP wordt toegepast op de hoofdprijs, worden de prijzen van opties, bundelitems en bijbehorende producten (die de hoofdprijs verhogen of verlagen) normaal weergegeven. |
| Gekoppelde productprijs | Als een product geen hoofdprijs heeft en de prijs ervan wordt afgeleid van de bijbehorende productprijzen (zoals in een gegroepeerd product), worden de MAP-instellingen van de bijbehorende producten toegepast. |
| [MSRP](product-price-minimum-advertised.md) | Als voor een product in het winkelwagentje de door de fabrikant voorgestelde detailhandelsprijs (MSRP) is opgegeven, wordt de prijs niet doorberekend. |
| [Tier-prijs](product-price-tier.md) | Als de prijsstelling voor lagen is ingesteld, wordt het prijsbericht voor lagen niet weergegeven in de catalogus. Op de productpagina wordt een bericht weergegeven dat aangeeft dat de prijs lager kan zijn wanneer u meer dan een bepaalde hoeveelheid bestelt, maar dat de korting alleen in percentages wordt weergegeven. Voor gekoppelde producten van een gegroepeerd product worden de kortingen niet weergegeven op de productpagina. De laagprijs wordt weergegeven volgens de instelling Ware prijs weergeven. |
| [Speciale prijs](product-price-special.md) | Als de speciale prijs is opgegeven, wordt de speciale prijs weergegeven volgens de instelling Ware prijs weergeven. |

## MAP-configuratie

De functie Minimale geadverteerde prijs (MAP) is niet standaard ingeschakeld. Als u dit vermogen aan uw opslag wilt toevoegen, moet u het toelaten en de montages van de KAART voor uw producten vormen. De montages van de KAART kunnen op alle producten in uw catalogus worden toegepast of voor specifieke producten worden gevormd. Als MAP wereldwijd is ingeschakeld, zijn alle productprijzen in de winkels verborgen. Er zijn verschillende configuratieopties die u kunt gebruiken om in overeenstemming te blijven met de bepalingen van uw overeenkomst met de fabrikant, terwijl u uw klanten toch een betere prijs aanbiedt.

![De werkelijke prijs wordt weergegeven &quot;Op beweging&quot;](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"}

Op het globale niveau, kunt u MAP toelaten of onbruikbaar maken, het op alle producten toepassen, bepalen hoe de daadwerkelijke prijs wordt getoond. U kunt ook de tekst van de gerelateerde berichten en informatieterminfo in de winkel bewerken.

Als MAP is ingeschakeld, worden de MAP-instellingen op productniveau beschikbaar. U kunt KAART op een individueel product toepassen door MSRP in te gaan en te kiezen hoe u de daadwerkelijke prijs in de opslag wilt verschijnen. De MAP-instellingen op productniveau overschrijven de algemene MAP-instellingen.

![Klik voor prijs](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### Stap 1: Enable MAP for the store view

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Indien van toepassing, instellen **[!UICONTROL Store View]** in de rechterbovenhoek van de weergave waarop de configuratie van toepassing is.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Sales]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Minimum Advertised Price]_sectie.

1. Indien nodig, instellen **KAART inschakelen** tot `Yes`.

   ![MAP-configuratie](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}

   Voor een gedetailleerde lijst van deze configuratieopties, zie [_Minimale geadverteerde prijs_](../configuration-reference/sales/sales.md#minimum-advertised-price) in de _Configuratieverwijzing_.

### Stap 2: De MAP-instellingen configureren

Gebruik één van de volgende methodes om de montages van de KAART te vormen:

#### Methode 1: MAP configureren voor alle producten

1. Ga als volgt te werk om te bepalen wanneer en waar de werkelijke prijs zichtbaar moet zijn voor klanten:

   - Als u de standaardwaarde wilt wijzigen, schakelt u de optie **[!UICONTROL Use system value]** selectievakje.

   - Set **Werkelijke prijs weergeven** op een van de volgende wijzen:
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. Voer de tekst in die u in het dialoogvenster **[!UICONTROL Default Popup Text Message]**.

1. Voer een aanvullende uitleg in die u wilt weergeven in het dialoogvenster **[!UICONTROL Default "What's This" Text Message]**.

1. Klik op **[!UICONTROL Save Config]**.

#### Methode 2: MAP configureren voor één product

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. Open het product in **[!UICONTROL Edit]** -modus.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced Settings]** en kiest u **[!UICONTROL Advanced Pricing]**.

   >[!NOTE]
   >
   >De [!UICONTROL Manufacturer's Suggested Retail Price] en [!UICONTROL Display Actual Price] velden worden alleen weergegeven als [Minimale geadverteerde prijs](../configuration-reference/sales/sales.md#minimum-advertised-price) wordt toegelaten in de configuratie.

1. Voer de **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP).

   In dit voorbeeld, is de productprijs $54.00, en MSRP is 59.95.

   ![Door fabrikant voorgestelde detailhandelsprijs](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Display Actual Price]** op een van de volgende wijzen:

   - `Use config` - (Standaard) Hiermee worden de weergave-instellingen toegepast [geconfigureerd](../configuration-reference/sales/sales.md#minimum-advertised-price) voor de winkel. |
   - `On Gesture` - Geeft de werkelijke productprijs weer in een pop-up wanneer de klant op de knop _Klik voor prijs_ of _Wat is dit?_ koppeling.
   - `In Cart` - Geeft de werkelijke productprijs weer in het winkelwagentje.
   - `Before Order Confirmation` - Geeft de werkelijke productprijs weer aan het einde van het afrekenproces, vlak voordat de bestelling wordt bevestigd.

1. Klik op **[!UICONTROL Done]** en vervolgens **[!UICONTROL Save]**.
