---
title: Beheerdersdashboard
description: Leer meer over het dashboard Admin, dat gewoonlijk de eerste pagina is die wanneer u login verschijnt.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Beheerdersdashboard

Het dashboard is meestal de eerste pagina die wordt weergegeven wanneer u zich aanmeldt bij het _Beheerder_ en kan een overzicht in real time van verkoop en klantenactiviteit verstrekken. De gegevens van het dashboard verstrekken een momentopname van levenslange verkoop, gemiddelde ordehoeveelheid, recente orden, en onderzoekstermijnen. Het diagram toont voltooide orders en bedragen voor het geselecteerde datumbereik en kan worden gegenereerd op basis van dynamische gegevens, real-time gegevens of historische geaggregeerde gegevens. De tabbladen onderaan bieden snelle rapporten van uw best verkochte producten, de meeste bekeken producten, nieuwe klanten en klanten die het meest hebben aangeschaft.

Als u een aanzienlijke hoeveelheid gegevens hebt die moet worden verwerkt, kan het diagram worden uitgeschakeld om de prestaties te verbeteren. Het dashboard in het volgende voorbeeld wordt gevormd om gegevens in real time te gebruiken en toont voltooide orden tegen het uur voor de laatste 24 uren. De grafiek wordt bijgewerkt voor elke voltooide orde.

![Dashboard](./assets/dashboard-full.png){zoomable=&quot;yes&quot;}

[Geavanceerde rapportage](business-intelligence.md#advanced-reporting) toont een gepersonaliseerd dashboard dat op uw product, orde, en klantengegevens wordt gebaseerd.

![Geavanceerde rapportage](./assets/dashboard-advanced-reporting.png){zoomable=&quot;yes&quot;}

## Het dashboard configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**en voer een van de volgende instellingen in.

1. Wanneer de configuratie volledig is, klik **[!UICONTROL Save Config]**.

1. Klik op **[!UICONTROL Cache Management]** en vernieuw elke ongeldige cache.

### Grafieken inschakelen

Als u een grote hoeveelheid te verwerken gegevens hebt, kunt u de weergave van het diagram uitschakelen om de prestaties te verbeteren. Als deze optie niet is ingeschakeld, wordt het bericht &quot;Geen gegevens gevonden&quot; weergegeven in plaats van het diagram, hoewel de onderstaande overzichtstotalen nog steeds worden gegenereerd.

1. In het linkernavigatievenster onder **[!UICONTROL Advanced]**, kiest u **[!UICONTROL Admin]**.

1. Vouw indien nodig de **[!UICONTROL Dashboard]** sectie.

   ![Geavanceerde configuratie - Grafieken inschakelen](./assets/admin-dashboard-config.png){width="600"}

1. Als u de standaardwaarde wilt wijzigen, schakelt u de optie **[!UICONTROL Use system value]** selectievakje.

1. Set **Grafieken inschakelen** tot `Yes`.

Voor meer informatie over de configuratieopties van Admin raadpleegt u [Referentiehandleiding voor configuratie](../configuration-reference/advanced/admin.md).

### De startpagina wijzigen

Het dashboard is standaard [opstartpagina](../configuration-reference/advanced/admin.md) voor Admin, hoewel u een verschillende startpagina kunt vormen.

1. Als u nog niet de beheerdersconfiguratieopties hebt geopend, kiest u **[!UICONTROL Admin]** krachtens _[!UICONTROL Advanced]_in het linkernavigatievenster.

1. Klik om de **Opstartpagina** sectie.

   ![Beheerdersdashboard - instelling startpagina](./assets/admin-startup-page.png){width="600"}

1. Wis de **[!UICONTROL Use system value]** selectievakje en kies de **Opstartpagina** die u wilt weergeven wanneer u zich aanmeldt bij de beheerder.

### De begindatums kiezen

1. In het linkernavigatievenster onder **[!UICONTROL General]**, kiest u **Rapporten**.

1. Vouw op de pagina de **[!UICONTROL Dashboard]** sectie.

1. Wis de **[!UICONTROL Use system value]** Schakel de selectievakjes voor de datuminstellingen in en voer de volgende handelingen uit:

   - Set **Jaarlijks begin** aan de **Maand** en **Dag**.

   - Set **Huidige maand start** aan de **Dag**.

   ![Beheerdashboard - Datuminstellingen](./assets/reports-dashboard.png){width="600"}

Voor meer informatie over de [!UICONTROL Reports] configuratieopties, zie [_Referentiehandleiding voor configuratie_](../configuration-reference/general/reports.md).

### De gegevensbron configureren

Het dashboarddiagram kan in real time of door historische, samengevoegde gegevens te gebruiken worden geproduceerd. Als de prestaties van belang zijn, kunt u de prestaties versnellen door geaggregeerde gegevens te gebruiken.

1. Klik in het linkernavigatievenster om uit te vouwen **Verkoop** en kiest u **Verkoop** onder.

1. Vouw op de pagina de **[!UICONTROL Dashboard]** sectie.

   ![Admin dashboard - gegevensbroninstelling](./assets/config-sales-dashboard.png){width="600"}

1. Wis de **[!UICONTROL Use system value]** selectievakje en set **[!UICONTROL Use Aggregated Data]** op een van de volgende wijzen:

   - Kies bij historische, geaggregeerde gegevens de optie `Yes`.
   - Kies voor realtime gegevens de optie `No`.

## Grafieksecties

| Sectie | Beschrijving |
|--- |--- |
| [!UICONTROL Orders] | Dit lusje toont een grafiek in real time van alle voltooide orden voor de huidige archiefmening en gespecificeerde tijdspanne. |
| [!UICONTROL Amounts] | Dit lusje toont een grafiek in real time van alle voltooide ordebedragen voor de huidige archiefmening en de gespecificeerde tijdspanne. |
| [!UICONTROL Time Range] | Bepaalt de gegevens die in de grafiek en samenvattingstotalen hieronder worden vertegenwoordigd. Opties: `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | De totalen voor inkomsten, belastingen, verzendingen en hoeveelheden onder de grafiek zijn gebaseerd op de diagramgegevens en de instelling voor het huidige tijdbereik. |

{style="table-layout:auto"}

## Opnamegegevens

| Sectie | Beschrijving |
|--- |--- |
| [!UICONTROL Lifetime Sales] | De geaggregeerde totale verkoop tijdens de levensduur van de winkel. |
| [!UICONTROL Average Order] | Het gemiddelde orderbedrag tijdens de levensduur van de winkel. |
| [!UICONTROL Last Orders] | Een samenvatting van de laatste vijf geplaatste bestellingen. |
| [!UICONTROL Last Search Terms] | De laatste vijf zoektermen. |
| [!UICONTROL Top Search Terms] | De vijf meest gebruikte zoektermen. |

{style="table-layout:auto"}

## Tabbladen Rapport

| Sectie | Beschrijving |
|--- |--- |
| [!UICONTROL Bestsellers] | De vijf best verkochte producten gedurende de opgegeven periode. |
| [!UICONTROL Most Viewed Products] | De vijf producten werden het meest bekeken tijdens de opgegeven periode. |
| [!UICONTROL New Customers] | De meest recente vijf klanten die zich gedurende de opgegeven periode voor een account hebben geregistreerd. |
| [!UICONTROL Customers] | De laatste vijf klanten met een orde die verwerking tijdens de gespecificeerde tijdspanne voltooide. |

{style="table-layout:auto"}

## Dashboardknoppen

| Knop | Beschrijving |
|--- |--- |
| [!UICONTROL Reload Data] | Hiermee vernieuwt u de dashboardgegevens. |
| [!UICONTROL Go to Advanced Reporting] | Toont een gepersonaliseerd dashboard van dynamische grafieken en rapporten die op uw product, orde, en klantengegevens worden gebaseerd. Voor uitgebreidere analyse, zie [Geavanceerde rapportage](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
