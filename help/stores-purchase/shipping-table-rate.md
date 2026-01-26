---
title: Verzending van tabeltarieven
description: Leer hoe je een verzendoptie voor tabeltarieven instelt voor je winkel.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 3%

---

# Verzending van tabeltarieven

Het _tarief van de lijst_ verschepende methodeverwijzingen een lijst van gegevens om het verschepen tarieven te berekenen die op een combinatie voorwaarden worden gebaseerd, die omvatten:

- Gewicht v. bestemming
- Prijs v. bestemming
- Aantal objecten v. Doel

Als je pakhuis bijvoorbeeld in Los Angeles is, kost het minder om naar San Diego te verzenden dan naar Vermont. U kunt de verzending van tabeltarieven gebruiken om de besparingen door te geven aan uw klanten.

De gegevens die worden gebruikt om tabelsnelheden te berekenen, worden in een spreadsheet voorbereid en in uw winkel geïmporteerd. Wanneer de klant een prijsopgave aanvraagt, worden de resultaten weergegeven in de sectie met verzendramingen van het winkelwagentje.

>[!NOTE]
>
>Er kan slechts één set tabelsnelheidsgegevens tegelijk actief zijn.

![&#x200B; de verschepende optie van het Tarief van de Lijst in het winkelwagentordoverzicht &#x200B;](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## Stap 1: De standaardinstellingen voltooien

De eerste stap bestaat uit het voltooien van de standaardinstellingen voor tabelsnelheden. U kunt deze stap voltooien zonder het werkingsgebied van de configuratie te veranderen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies _[!UICONTROL Sales]_&#x200B;in de sectie **[!UICONTROL Delivery Methods]**&#x200B;van het linkerdeelvenster.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Table Rates]** sectie uit.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om de volgende instellingen te wijzigen zoals beschreven.

   ![&#x200B; Tarieven van de Lijst &#x200B;](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enabled]** in op `Yes` .

1. Voer de **[!UICONTROL Title]** in die u tijdens het uitchecken voor de sectie met tabelsnelheden wilt weergeven.

   De standaardtitel is `Best Way` .

1. Voer de **[!UICONTROL Method Name]** in die u als label naast de berekende frequentie in het winkelwagentje wilt weergeven.

1. Stel **[!UICONTROL Condition]** in op een van de volgende berekeningsmethoden:

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Voor orders die virtuele producten bevatten, stelt u **[!UICONTROL Include Virtual Products in Price Calculation]** in op `Yes` als u de virtuele producten wilt opnemen in de berekening.

   >[!NOTE]
   >
   >Omdat de virtuele producten-zulke als dienst-geen gewicht hebben, kunnen zij niet het resultaat van een berekening veranderen die op de voorwaarde van de Waarde v. van de Bestemming gebaseerd is. Virtuele producten kunnen echter het resultaat wijzigen van een berekening die is gebaseerd op de voorwaarde Prijs v. Doel of # van items vs. Doel.

1. Configureer de opties voor de behandelingskosten naar wens.

   De verpakkingskosten zijn optioneel en worden weergegeven als extra kosten die bij de verzendkosten worden opgeteld. Voer de volgende handelingen uit als u verpakkingskosten wilt opnemen:

   - Instellen **[!UICONTROL Calculate Handling Fee]** :

      - `Fixed`
      - `Percent`

   - Voer de **[!UICONTROL Handling Fee]** -rente in volgens de methode die wordt gebruikt om de kosten te berekenen.

     Als de kosten bijvoorbeeld zijn gebaseerd op een vaste vergoeding, voert u het bedrag in als een decimaal, bijvoorbeeld `4.90` . Als de behandelingskosten echter zijn gebaseerd op een percentage van de bestelling, voert u het bedrag in als een percentage. Als u bijvoorbeeld zes procent van de volgorde in rekening brengt, voert u de waarde in als `.06` .

1. Wijzig indien nodig de **[!UICONTROL Displayed Error Message]** .

   Dit tekstvak is vooraf ingesteld met een standaardbericht, maar u kunt een ander bericht invoeren dat u wilt weergeven als deze leveringsmethode niet meer beschikbaar is.

1. Instellen **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - de klanten van alle [&#x200B; landen &#x200B;](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze leveringsmethode gebruiken.
   - `Specific Countries` - Wanneer u deze optie kiest, wordt de lijst _[!UICONTROL Ship to Specific Countries]_&#x200B;weergegeven. Selecteer elk land in de lijst waar deze leveringsmethode kan worden gebruikt.

1. Stel **[!UICONTROL Show Method if Not Applicable]** in op `Yes` als u de Tabelpercentages altijd wilt weergeven

1. Voer bij **[!UICONTROL Sort Order]** een getal in om de volgorde te bepalen waarin Verzending tabelsnelheid wordt weergegeven wanneer deze bij andere leveringsmethoden tijdens het afrekenen wordt vermeld.

   `0` = first, `1` = second, `2` = third, enzovoort.

1. Klik op **[!UICONTROL Save Config]**.

## Stap 2: De tabelsnelheidsgegevens voorbereiden

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op `Main Website` of op een andere website waarop de configuratie van toepassing is.

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om de volgende instellingen te wijzigen zoals beschreven.

1. Wijzig de **[!UICONTROL Condition]** indien nodig.

1. Klik op **[!UICONTROL Export CSV]**.

   ![&#x200B; Uitvoer CSV &#x200B;](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Sla het `tablerates.csv` -bestand op uw systeem op.

1. Open het bestand in een spreadsheettoepassing.

1. Vul de tabel in met de juiste waarden voor de verzendberekeningsvoorwaarde.

   - Gebruik een asterisk (*) als vervanging die alle mogelijke waarden in om het even welke categorie vertegenwoordigt.
   - De _[!UICONTROL Country]_&#x200B;kolom moet a [&#x200B; geldige code van drie tekens &#x200B;](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) voor elke rij bevatten.
   - Sorteer de gegevens op _[!UICONTROL Region/State]_, zodat de specifieke locaties zich boven aan de lijst bevinden en de jokertekenlocaties onderaan. Het gebruiken van deze methode verwerkt eerst de regels met de absolute waarden, en later de vervangingswaarden.
   - Postcodes worden niet ondersteund. Gebruik een asterisk (*) om alle codes binnen het gebied/de staat toe te staan, of specificeer één enkele code voor een specifieke plaats in de _[!UICONTROL Zip/Postal Code]_&#x200B;kolom.
   - Waarden in de kolom _[!UICONTROL Weight (and above)]_&#x200B;kunnen maximaal vier decimalen hebben (zoals `2.5075` ). Wanneer meer decimalen in de gegevens worden gebruikt, mislukt het importeren.

   ![&#x200B; Gewicht vs. Doel (Australië) &#x200B;](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Sla het `tablerates.csv` -bestand op.

## Stap 3: De tabelsnelheidsgegevens importeren

1. Ga terug naar de sectie **[!UICONTROL Table Rates]** van uw winkelconfiguratie.

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op de website waar deze methode wordt gebruikt.

1. Voor **[!UICONTROL Import]** klikt u op **[!UICONTROL Choose File]** en selecteert u het voltooide `tablerates.csv` bestand om de tarieven te importeren.

   ![&#x200B; de Tarieven van de Lijst van de Invoer &#x200B;](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Stap 4: De tarieven verifiëren

Om ervoor te zorgen dat de gegevens van het lijsttarief correct zijn, ga het betalingsproces met verscheidene verschillende adressen door om ervoor te zorgen dat de verschepings en behandelende tarieven correct worden berekend.

### Voorbeeld 1: Prijs en bestemming

In dit voorbeeld wordt de voorwaarde Prijs v. bestemming gebruikt om een set van drie verschillende verzendtarieven te maken op basis van de hoeveelheid van het subtotaal voor bestellingen voor het Amerikaanse continent, Alaska en Hawaii. Het sterretje (*) is een jokerteken dat alle waarden vertegenwoordigt.

| LAND | REGIO/STAAT | ZIP/POSTCODE | SUBTOTAAL BESTELLEN (en hoger) | VERZENDPRIJS |
|--- |--- |--- |--- |--- |
| VS | HI | * | 100 | 10 |
| VS | HI | * | 50 | 15 |
| VS | HI | * | 0 | 20 |
| VS | AK | * | 100 | 10 |
| VS | AK | * | 50 | 15 |
| VS | AK | * | 0 | 20 |
| VS | * | * | 100 | 5 |
| VS | * | * | 50 | 10 |
| VS | * | * | 0 | 15 |

{style="table-layout:auto"}

### Voorbeeld 2: Gewicht en bestemming

In dit voorbeeld wordt de voorwaarde Dikte v. bestemming gebruikt om verschillende verzendkosten te maken op basis van het gewicht van de bestelling.

| LAND | REGIO/STAAT | ZIP/POSTCODE | GEWICHT (en hoger) | VERZENDPRIJS |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39,95 |
| AUS | NT | * | 0 | 19,95 |
| AUS | VIC | * | 9 | 19,95 |
| AUS | VIC | * | 0 | 5,95 |
| AUS | WA | * | 9 | 39,95 |
| AUS | WA | * | 0 | 19,95 |
| AUS | * | * | 9 | 29,95 |
| AUS | * | * | 0 | 9,95 |

{style="table-layout:auto"}

### Voorbeeld 3: Beperking van de gratis verzending naar het Amerikaanse vasteland

1. Maak een `tablerates.csv` -bestand dat alle statusdoelen bevat waarvoor u gratis verzending wilt aanbieden.

1. Voltooi de configuratie van de tabelsnelheid met de volgende instellingen:

   | Instelling | Waarde |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op `Main Website` of op een andere website waarop de configuratie van toepassing is.

1. Voor **[!UICONTROL Import]** klikt u op **[!UICONTROL Choose File]** en selecteert u het voltooide `tablerates.csv` bestand om de tarieven te importeren.
