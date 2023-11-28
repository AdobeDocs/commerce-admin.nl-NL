---
title: Een voorraadblok toevoegen
description: Leer hoe u een voorraad toevoegt en bronnen toewijst aan verkoopkanalen (websites) en een directe koppeling biedt naar verkoopbare hoeveelheden en productinventarissen.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# Een voorraad toevoegen

De voorraden wijzen uw bronnen aan verkoopkanalen (of websites) toe, die een directe verbinding aan verkoopbare hoeveelheden en productinventarissen verstrekken.

Wanneer u een aangepaste voorraad maakt, wijst u websites en bronnen toe. De bronnen kunnen toegelaten en gehandicapte bronnen omvatten. U kunt bijvoorbeeld een opslagplaats aan uw voorraad toevoegen en de locatie voorbereiden voor het beheer van de voorraad en het voltooien van de verzendingen.

Nadat u bronnen hebt toegevoegd, moet u de volgorde voor de bronnen van boven (eerst) tot onder (laatst) als prioriteit instellen. Deze bestelling is van invloed op aanbevelingen tijdens de verzending van orders.

![Nieuwe voorraad](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## De voorraad toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Klik op **[!UICONTROL Add New Stock]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL General]** en voer een unieke **[!UICONTROL Name]** de identificatie van het nieuwe bestand.

   ![Algemene aandelenopties](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Sales Channels]** en selecteert u de **[!UICONTROL Websites]** wanneer dit bestand beschikbaar is.

   Houd voor een installatie op meerdere sites de Ctrl-toets (PC) of de Command-toets (Mac) ingedrukt en klik op elke website.

   >[!NOTE]
   >
   >Als u een website of verkoopkanaal selecteert dat aan een andere voorraad is toegewezen, wordt de toewijzing ongedaan gemaakt. Alle Sales Channel die niet aan een aangepaste voorraad zijn toegewezen, worden toegewezen aan de standaardvoorraad.

   ![Sales Channel-opties voor voorraden](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Sources]** en voer de volgende handelingen uit voor alle andere bestanden dan de standaardinstelling:

   - Klik op **[!UICONTROL Assign Sources]**.

   ![Toegewezen bronnen](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Schakel selectievakjes in voor alle bronnen die u aan de voorraad wilt toewijzen.

   >[!IMPORTANT]
   >
   >Als u dezelfde bron aan meerdere voorraden toewijst, kan dit ertoe leiden dat de producten die aan die bron zijn toegewezen, worden oververkocht.

   - Klik op **[!UICONTROL Done]**.

     De toegevoegde bronnen tonen in Toegewezen Bronnen.

     ![Bronnen toewijzen aan voorraad](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Gebruiken ![Pictogram Sorteren](assets/icon-sort.png) om de bronnen naar een prioriteit van boven (eerste) naar onder (laatste) te slepen.

   De bronvolgorde is belangrijk bij verzendopdrachten.

   ![Voorbeeld van toegewezen bronnen](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Op de _[!UICONTROL Save]_(![Menupijl](../assets/icon-menu-down-arrow-red.png)), kiest u **[!UICONTROL Save & Close]**.

## Veldomschrijvingen

| Veld | Beschrijving |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Naam van het bestand. Bijvoorbeeld: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Definieert de [bereik](../getting-started/websites-stores-views.md#scope-settings) van de voorraad door de voorraad toe te wijzen aan specifieke websites als _verkoopkanalen_. Selecteer een of meer websites per bestand. Elke website kan slechts aan één bestand worden toegewezen. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Hiermee wijst u inventarisbronnen toe aan dit bestand. Aangepaste bronnen kunnen niet worden toegewezen aan standaardvoorraad. |
| [!UICONTROL Assigned Sources] | Lijst met toegewezen bronnen. Bronnen slepen en neerzetten met ![Pictogram Sorteren](assets/icon-sort.png) in een geprioriteerde volgorde voor het uitvoeren van bestellingen en het verzenden van bestellingen.<br/><br/>**[!UICONTROL Code]**- Unieke code-id voor de bron.<br/>**[!UICONTROL Name]** - Beschrijving van naam voor de bron.<br/>**[!UICONTROL Unassign]**- Verwijder de toegewezen bron uit het bestand met ![Prullenbakpictogram](../assets/icon-delete-trashcan-solid.png). |
