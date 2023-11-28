---
title: Belastingrichtsnoeren per land
description: Bekijk de aanbevolen belastinginstellingen per land.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1324'
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
| [!UICONTROL Enable FPT] | `No`, behalve in Californië. |

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
| Opmerking | Voor B2B-handelaren om eenvoudigere overwegingen met betrekking tot de btw-toeleveringsketen te bieden. De berekening van de belasting op rij is ook geldig; nochtans, controleer met uw het belasten jurisdictie. Er wordt vanuit gegaan dat een handelaar zich in de toeleveringsketen bevindt en dat verkochte goederen door andere verkopers worden gebruikt voor btw-kortingen, enzovoort. Deze definitie maakt het gemakkelijk om belasting door punt voor snellere kortingsgeneratie te onderscheiden. <br/><br/>**_Opmerking:_**Sommige rechtsgebieden vereisen verschillende afrondingsstrategieën die momenteel niet door de Handel worden ondersteund en die niet in alle rechtsgebieden de belasting op item- of rijniveau toestaan. |

{style="table-layout:auto"}

## belastingconfiguratie van Canada

>[!IMPORTANT]
>
>Handelaren in de provincie GST/PST (Montreal) moeten één belastingregel opstellen en een gecombineerd belastingbedrag laten zien. Raadpleeg een bevoegde belastingautoriteit als u vragen hebt. Zie voor meer informatie over de belastingvereisten van specifieke provincies het volgende: [Revenu Québec][1], [Regering van Saskatchewan][2], en [Manitoba-informatie voor leveranciers][3]

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

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Voor een configuratie met meerdere sites stelt u **[!UICONTROL Store View]** naar de website en opslag die het doel van de configuratie is.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Tax]**.

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

Als u wilt voorkomen dat de belasting wordt samengeperst en de berekende belasting correct als afzonderlijke posten voor GST en PST wilt weergeven, stelt u verschillende prioriteiten voor elke regel in en selecteert u de **Alleen subtotaal berekenen** selectievakje. Elke belasting wordt weergegeven als een afzonderlijke post, maar de belastingbedragen worden niet samengevoegd.

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

Voor deze belastingregel moet u de prioriteit instellen op 0 en de optie **Alleen subtotaal berekenen** selectievakje. Elke belasting wordt weergegeven als een afzonderlijke post, maar de belastingbedragen worden niet samengevoegd.

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

1. Klik op **[!UICONTROL Save Config]**.

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
| Frankrijk-NormVAT | Land: Frankrijk <br/>Staat/regio: * <br/>Postcode: * <br/>Percentage: 20% |
| Verlaagde btw door Frankrijk | Land: Frankrijk <br/>Staat/regio: * <br/>Postcode: * <br/>Frequentie: 5% |
| Duitsland-standaardBTW | Land: Duitsland <br/>Staat/regio: * <br/>Postcode: * Tarief: 19% |
| Verlaagde btw voor Duitsland | Land: Duitsland <br/>Staat/regio: * <br/>Postcode: * <br/>Percentage: 7% |

{style="table-layout:auto"}

### Stap 3: Instellen van de belastingregels

Maak de volgende belastingregels:

| Belastingregels | Instellingen |
|--- |--- |
| Retail-France-StandardVAT | Klantklasse: Retail Customer <br/>Belastingklasse: BTW-standaard <br/>Belastingtarief: Frankrijk-StandaardBTW <br/>Prioriteit: 0 <br/>Sorteervolgorde: 0 |
| Retail-France-ReducedVAT | Klantklasse: Retail Customer <br/>Belastingklasse: btw verlaagd <br/>Belastingtarief: door Frankrijk verlaagd BTW <br/>Prioriteit: 0 <br/>Sorteervolgorde: 0 |
| Retail-Germany-StandardVAT | Klantklasse: Retail Customer <br/>Belastingklasse: BTW-standaard <br/>Belastingtarief: Duitsland-Standaardbtw <br/>Prioriteit: 0 <br/>Sorteervolgorde: 0 |
| Retail-Germany-ReducedVAT | Klantklasse: Retail Customer <br/>Belastingklasse: verlaagd btw <br/>Belastingtarief: door Duitsland verlaagd BTW <br/>Prioriteit: 0 <br/>Sorteervolgorde: 0 |

{style="table-layout:auto"}

### Stap 4: Een winkelweergave instellen voor Duitsland

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Onder de standaardwebsite maakt u een winkelweergave voor **[!UICONTROL Germany]**.

1. Ga als volgt te werk:

   - Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - In de linkerbovenhoek, plaats **[!UICONTROL Default Config]** naar de Franse opslagplaats.

   - Vouw op de pagina Algemeen de tekst uit ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Countries Options]** en het standaardland instellen op `France`.

   - Vul de gewenste landinstellingen in.

1. Kies in de linkerbovenhoek de optie Duits **[!UICONTROL Store View]**.

1. Op de _Algemeen_ pagina, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** en stelt het standaardland in op `Germany`.

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

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In de rechterbovenhoek stelt u **[!UICONTROL Store View]** naar de Duitse winkel en klik op **[!UICONTROL OK]** ter bevestiging.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Tax]**.

1. In de **[!UICONTROL Default Tax Destination Calculation]** Ga als volgt te werk:

   - Wis de **[!UICONTROL Use Website]** selectievakje na elk veld,

   - Aanpassen aan de verzendinstellingen van uw site [punt van oorsprong](shipping-settings.md#point-of-origin)Werk de volgende waarden bij:

      - Standaardland
      - Standaardstatus
      - Standaardpostcode

     Deze instelling zorgt ervoor dat de belasting correct wordt berekend wanneer de productprijzen belasting bevatten.

     ![Berekening standaardbelastingbestemming](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf
