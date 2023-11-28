---
title: Rapport Action Logs
description: Leer hoe te om het rapport van het Logboek van Acties te bekijken, te filtreren en uit te voeren, dat een gedetailleerd verslag van alle logboek-toegelaten acties Admin verstrekt.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Rapport Action Logs

{{ee-feature}}

De _Handelingenlogboeken_ het rapport toont een gedetailleerd verslag van alle acties Admin die voor registreren worden toegelaten. Elk verslag is tijdstempels, en registreert het IP adres en de naam van de gebruiker. Het logboekgegeven omvat admin gebruikersgegevens en verwante veranderingen die tijdens de actie werden aangebracht.

De acties die u in het rapport wilt tonen moeten in worden toegelaten [Logboekregistratie van beheerhandelingen](action-log.md) in de opslaginstellingen. Als het actietype wordt gecontroleerd (toegelaten), worden die types van acties Admin getoond in het Logs van de Actie rapport.

Het rapport kan worden gefilterd gebruikend de opties in elke kolom. U kunt één filteroptie instellen of filteropties voor meerdere kolommen instellen om het rapport te beperken tot een lijst met specifieke handelingen. U kunt rapportgegevens in of Csv of formaat van XML van Excel ook uitvoeren.

Het rapport Action Logs bevat de volgende informatie:

- **[!UICONTROL Time]** - De datum en tijd waarop de handeling is uitgevoerd
- **[!UICONTROL Action Group]** - Hiermee geeft u het actietype weer. Het correleert de acties die zijn ingeschakeld _Logboekregistratie van beheerhandelingen_ scherm in uw winkelinstellingen
- **[!UICONTROL Action]** - Geeft de handeling weer die is vastgelegd
- **[!UICONTROL IP Address]** - Geeft het IP-adres weer van de computer waarop de handeling is uitgevoerd
- **[!UICONTROL Username]** - Hiermee wordt de aanmeldings-id weergegeven voor de gebruiker die de handeling heeft uitgevoerd
- **[!UICONTROL Result]** - Geeft aan of de handeling van de gebruiker is gelukt of mislukt
- **[!UICONTROL Full Action Name]** - Geeft de naam van de achterste handeling weer
- **[!UICONTROL Details]** - Geeft de categorie voor achterste acties weer
- **[!UICONTROL Full Details]** - Toont alle geregistreerde details van de admin actie

## Het rapport Handelingenlogboeken weergeven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Handelingenlogboeken](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL View]**.

   ![Gegevens van het handelingenlogboek](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Het rapport Handelingenlogboeken filteren

U kunt de gebieden van filteropties bepalen en dan klikken **[!UICONTROL Search]** om de weergegeven acties te beperken.

Klik op **[!UICONTROL Reset Filter]**.

![Rapportfilters van het handelingenlogboek](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Veld | beschrijving |
|--- |--- |
| [!UICONTROL Time] | In **[!UICONTROL From]**, klikt u om een datum in de dynamische kalender te selecteren om de begindatum voor het filter te definiëren. In **[!UICONTROL To]** klikt u om een datum te selecteren waarop de einddatum voor het filter moet worden gedefinieerd. |
| [!UICONTROL Action Group] | Kies een actiegroep. |
| [!UICONTROL Action] | Kies een handeling. |
| [!UICONTROL IP Address] | Voer het IP-adres in van de computer die voor een handeling wordt gebruikt. |
| [!UICONTROL Username] | Kies een gebruikersnaam. Standaard is `All Users`. |
| [!UICONTROL Result] | Kies Succes of Fout. |
| [!UICONTROL Full Action Name] | Voer tekst in die overeenkomt met de zoekopdracht in het veld. |
| [!UICONTROL Details] | Voer tekst in die overeenkomt met de zoekopdracht in het veld. |

{style="table-layout:auto"}

## Het rapport Handelingenlogboeken exporteren

1. Voor **[!UICONTROL Export to]** kiest u een exportindeling:

   - `CSV` - Een bestand met door komma&#39;s gescheiden waarden dat normale tekstgegevens bevat
   - `Excel XML` - Een op XML gebaseerde indeling voor spreadsheetgegevens

1. Klik op **[!UICONTROL Export]**.

   Het gegenereerde bestand wordt automatisch voor downloads opgeslagen in de door u aangewezen map.

   ![Rapport met handelingenlogboeken exporteren](./assets/action-log-report-export.png){width="200"}
