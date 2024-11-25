---
title: Belastingrichtsnoeren per land
description: Bekijk de aanbevolen belastinginstellingen per land.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Belastingrichtsnoeren per land

## Amerikaanse belastingconfiguratie

Deze aanbevolen instellingen kunnen worden gebruikt voor de meeste belastingconfiguraties voor winkels in de Verenigde Staten.

| Belastingoptie | Aanbeveling |
|--- |--- |
| Catalogusprijzen laden | Exclusief belasting |
| FPT | Nee, omdat FPT niet wordt belast. |
| Belasting op basis van | Oorsprong verzending |
| Belastingberekening | Totaal |
| Belasting op verzendkosten? | Nee |
| Korting toepassen | Voor belasting |
| Opmerking | Alle belastingzones hebben dezelfde prioriteit, idealiter een zone voor de staat en een of meer zones voor het opzoeken van postcodes. |

{style="table-layout:auto"}

### Belastingklassen

| Belastingklasse | Aanbevolen instelling |
|--- |--- |
| Belastingklasse voor verzending | Geen |

{style="table-layout:auto"}

### Instellingen voor berekening

| Optie | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Berekening van de standaardbelastingbestemming

| Optie | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | Staat waar het bedrijf gevestigd is. |
| [!UICONTROL Default Post Code] | De postcode die in je belastingzones wordt gebruikt. |

{style="table-layout:auto"}

### Instellingen voor prijsweergave

| Optie | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Weergave-instellingen winkelwagentje

| Optie | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Orders, facturen, creditnota&#39;s en weergave-instellingen

| Optie | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Vaste productbelastingen (FPT)

| Optie | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Enable FPT] | `No` , behalve in Californië. |

{style="table-layout:auto"}

## VK-belastingconfiguratie

Deze aanbevolen instellingen kunnen worden gebruikt voor de meeste belastingconfiguraties voor winkels in het Verenigd Koninkrijk.

### B2C-belastingconfiguratie van het Verenigd Koninkrijk

| Belastingoptie | Aanbeveling |
|--- |--- |
| Catalogusprijzen laden | Exclusief belasting |
| FPT | Ja, inclusief FPT en beschrijving |
| Belasting op basis van | [!UICONTROL Shipping Address] |
| Belastingberekening | Totaal |
| Belasting op verzendkosten? | Ja |
| Korting toepassen | Vóór belasting, korting op prijzen, inclusief belasting. |
| Opmerking | Voor handelaren die leveranciersfacturen (inclusief btw) aangeven. |

{style="table-layout:auto"}

### U.K. B2B belastingconfiguratie

| Belastingoptie | Aanbeveling |
|--- |--- |
| Catalogusprijzen laden | Exclusief belasting |
| FPT | Ja, inclusief FPT en beschrijving |
| Belasting op basis van | [!UICONTROL Shipping Address] |
| Belastingberekening | Op object |
| Belasting op verzendkosten? | Ja |
| Korting toepassen | Vóór belasting, korting op prijzen, inclusief belasting. |
| Opmerking | Voor B2B-handelaren om eenvoudigere overwegingen met betrekking tot de btw-toeleveringsketen te bieden. De berekening van de belasting op rij is ook geldig; nochtans, controleer met uw het belasten jurisdictie. Er wordt vanuit gegaan dat een handelaar zich in de toeleveringsketen bevindt en dat verkochte goederen door andere verkopers worden gebruikt voor btw-kortingen, enzovoort. Deze definitie maakt het gemakkelijk om belasting door punt voor snellere kortingsgeneratie te onderscheiden. <br/><br/>**_Nota:_**sommige jurisdicties vereisen verschillende het afronden strategieën momenteel niet die door Commerce worden gesteund, en dat niet alle jurisdicties punt of rijniveaubelasting toestaan. |

{style="table-layout:auto"}

## belastingconfiguratie van Canada

>[!IMPORTANT]
>
>Handelaren in de provincie GST/PST (Montreal) moeten één belastingregel opstellen en een gecombineerd belastingbedrag laten zien. Raadpleeg een bevoegde belastingautoriteit als u vragen hebt.

| Belastingoptie | Aanbeveling |
|--- |--- |
| Catalogusprijzen laden | Exclusief belasting |
| FPT | Ja, inclusief FPT, beschrijving en pas belasting toe op FPT. |
| Belasting op basis van | Oorsprong verzending |
| Belastingberekening | Totaal |
| Belasting op verzendkosten? | Ja |
| Korting toepassen | Voor belasting |

{style="table-layout:auto"}

In het volgende voorbeeld ziet u hoe u GST-belastingtarieven voor Canada en PST-belastingtarieven voor Saskatchewan kunt instellen, met belastingregels die de twee belastingtarieven berekenen en weergeven. Deze informatie schetst een voorbeeldconfiguratie; ben zeker om de correcte belastingtarieven en de regels voor uw belastingjurisdicties te verifiëren. Stel bij het instellen van belastingen het bereik van de winkel in om de configuratie toe te passen op alle toepasselijke winkels en websites.

- Vaste productbelasting wordt voor relevante goederen als productkenmerk opgenomen.
- In Quebec wordt PST aangeduid als TVQ. Als u een tarief voor Quebec wilt opstelling, zorg ervoor TVQ als herkenningsteken te gebruiken.

### Stap 1: Volledige instellingen voor belastingberekening

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Voor een configuratie met meerdere sites stelt u **[!UICONTROL Store View]** in op de website en slaat u die configuratie als doel heeft.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Tax]** .

1. Klik om elke sectie op de pagina uit te vouwen en de volgende instellingen in te vullen:

#### Instellingen voor belastingberekening

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (indien beschikbaar) |

{style="table-layout:auto"}

#### Belastingklassen

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (verzending wordt belast) |

{style="table-layout:auto"}

#### Berekening standaardbelastingbestemming

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (in voorkomend geval) |
| [!UICONTROL Default Postal Code] | `*` (sterretje) |

{style="table-layout:auto"}

#### Weergave-instellingen winkelwagentje

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### Vaste productbelastingen

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| Alle instellingen voor FPT-weergave | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Stap 2: Canadese belasting op goederen en diensten (GST) instellen

Als u het GST-nummer op facturen en andere verkoopdocumenten wilt afdrukken, moet u het ook in de naam van de toepasselijke belastingtarieven vermelden. De GST wordt weergegeven als onderdeel van de GST-hoeveelheid in een willekeurige ordersamenvatting.

#### Belastingzones en -tarieven beheren

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (sterretje) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (sterretje) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Stap 3: Canadese provinciale BTW instellen

Stel een ander belastingtarief in voor de betreffende provincie.

#### Informatie over belastingtarieven

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (sterretje) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Stap 4: Een GST-belastingregel maken

Vermijd het samenstellen van de belasting en de berekende belasting correct te tonen als afzonderlijke lijnpunten voor GST en PST, plaats verschillende prioriteiten voor elke regel en selecteer **Berekenen van subtotaal slechts** checkbox. Elke belasting wordt weergegeven als een afzonderlijke post, maar de belastingbedragen worden niet samengevoegd.

#### Informatie over belastingregels

| Veld | Aanbevolen instelling |
|--- |--- |
| Naam | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Schakel dit selectievakje in. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Stap 5: Maak een PST-belastingregel voor Saskatchewan

Voor deze belastingregel, zorg ervoor om de prioriteit aan 0 te plaatsen en **te selecteren berekent van subtotal slechts** checkbox. Elke belasting wordt weergegeven als een afzonderlijke post, maar de belastingbedragen worden niet samengevoegd.

#### Informatie over belastingregels

| Veld | Aanbevolen instelling |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | Schakel dit selectievakje in. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Stap 6: Sla de resultaten op en test deze

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Ga terug naar de winkel en maak een voorbeeldvolgorde om de resultaten te testen.

## EU-belastingconfiguratie

In het volgende voorbeeld ziet u een winkel in Frankrijk die 100 k+ euro in Frankrijk en 100 k+ euro in Duitsland verkoopt.

- Belastingberekeningen worden op het niveau van de website beheerd.
- De opties voor het converteren van valuta&#39;s en belastingweergave worden afzonderlijk beheerd in de winkelweergave (schakel het selectievakje Website gebruiken in om de standaardinstelling te overschrijven).
- Door het standaard belastingland in te stellen, kunt u dynamisch de juiste belasting voor het rechtsgebied tonen.
- Vaste productbelasting wordt voor relevante goederen als productkenmerk opgenomen.
- Het kan nodig zijn de catalogus te bewerken om ervoor te zorgen dat deze wordt weergegeven in de juiste categorie-/website-/winkelweergave.

### Stap 1: drie productbelastingklassen maken

In dit voorbeeld wordt aangenomen dat er geen meervoudige btw-verlaging voor productbelastingklassen nodig is.

1. Maak een btw-standaard productbelastingklasse.

1. Creëer een btw-verlaging voor de categorie productbelasting.

1. Maak een btw-vrije productbelastingklasse.

### Stap 2: Vaststelling van belastingtarieven voor Frankrijk en Duitsland

Maak de volgende belastingtarieven:

| Belastingtarieven | Instellingen |
|--- |--- |
| Frankrijk-NormVAT | Land: Frankrijk <br/> Staat/Gebied: * <br/> ZIP/Postcode: * <br/> Tarief: 20% |
| Verlaagde btw door Frankrijk | Land: Frankrijk <br/> Staat/Gebied: * <br/> ZIP/Postcode: * <br/> Tarief: 5% |
| Duitsland-standaardBTW | Land: Duitsland <br/> Staat/Regio: * <br/> ZIP/Postcode: * Tarief: 19% |
| Verlaagde btw voor Duitsland | Land: Duitsland <br/> Staat/Gebied: * <br/> ZIP/Postcode: * <br/> Tarief: 7% |

{style="table-layout:auto"}

### Stap 3: Instellen van de belastingregels

Maak de volgende belastingregels:

| Belastingregels | Instellingen |
|--- |--- |
| Retail-France-StandardVAT | Klant Klasse: de Belastingsklasse van de Klant van de kleinhandel <br/>: BTW-Standaard <br/> Tarief: Frankrijk-NormVAT <br/> Prioriteit: 0 <br/> Sorteervolgorde: 0 |
| Retail-France-ReducedVAT | Klant Klasse: de Belastingsklasse van de Klant van de Kleinhandels <br/>: BTW verminderd <br/> Tarief: Frankrijk-ReducedVAT <br/> Prioriteit: 0 <br/> Sorteervolgorde: 0 |
| Retail-Germany-StandardVAT | Klant Klasse: de Belastingsklasse van de Klant van de kleinhandel <br/>: BTW-Standaard <br/> Tarief: Duitsland-NormVAT <br/> Prioriteit: 0 <br/> Orde van de Soort: 0 |
| Retail-Germany-ReducedVAT | Klant Klasse: de Belastingsklasse van de Klant van de kleinhandel <br/>: BTW-verminderd <br/> Tarief: Duitsland-GereduceerdeBTW <br/> Prioriteit: 0 <br/> Orde van de Sortering: 0 |

{style="table-layout:auto"}

### Stap 4: Een winkelweergave instellen voor Duitsland

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Maak onder de standaardwebsite een winkelweergave voor **[!UICONTROL Germany]** .

1. Ga als volgt te werk:

   - Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Stel in de linkerbovenhoek **[!UICONTROL Default Config]** in op de Franse opslag.

   - Voor de Algemene pagina, breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Countries Options]** sectie uit, en plaats het standaardland aan `France`.

   - Vul de gewenste landinstellingen in.

1. Kies in de linkerbovenhoek de optie Duits **[!UICONTROL Store View]** .

1. Voor de _Algemene_ pagina, breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** uit en plaats het standaardland aan `Germany`.

1. Vul de gewenste landinstellingen in.

### Stap 5: belastinginstellingen configureren voor Frankrijk

Voer de volgende algemene belastinginstellingen in:

| Veld | Aanbevolen instelling |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (verzending wordt belast) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (sterretje) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### Stap 6: De belastinginstellingen voor Duitsland configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In de rechterbovenhoek stelt u **[!UICONTROL Store View]** in op de weergave in de Duitse winkel en klikt u op **[!UICONTROL OK]** om te bevestigen.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Tax]** .

1. Ga als volgt te werk in de sectie **[!UICONTROL Default Tax Destination Calculation]** :

   - Schakel het selectievakje **[!UICONTROL Use Website]** na elk veld uit.

   - Om het Verschepende Punt van Montages van uw plaats [ van oorsprong ](shipping-settings.md#point-of-origin) aan te passen, werk de volgende waarden bij:

      - Standaardland
      - Standaardstatus
      - Standaardpostcode

     Deze instelling zorgt ervoor dat de belasting correct wordt berekend wanneer de productprijzen belasting bevatten.

     ![ Berekening van de StandaardBelastingbestemming ](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
