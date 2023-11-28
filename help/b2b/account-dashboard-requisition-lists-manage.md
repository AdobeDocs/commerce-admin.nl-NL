---
title: '[!UICONTROL My Requisition Lists]'
description: Meer informatie over de ervaring van klanten met aanvraaglijsten, die beschikbaar is in het dashboard van hun account.
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL My Requisition Lists]

De belangrijkste reden om een aanvraaglijst te handhaven is het gemakkelijk te maken om producten opnieuw in orde te brengen. Geautoriseerde klanten kunnen de volgorde van items in een aanvraaglijst eenvoudig wijzigen door ze aan het winkelwagentje toe te voegen en items van de ene lijst naar de andere te verplaatsen of te kopiëren.

![Mijn aanvraaglijsten](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## Een aanvraaglijst openen

1. Van hun rekeningdashboard, kiest de klant **[!UICONTROL My Requisition Lists]**.

1. Hiermee wordt de lijst met aanvragen gezocht die ze willen openen en klikt u op deze lijst **[!UICONTROL View]** en voer een van de volgende handelingen uit:

### Producten aan winkelwagentje toevoegen

1. De klant voert een van de volgende handelingen uit om de producten te selecteren die moeten worden toegevoegd:

   - Selecteert checkbox van elk punt.
   - Klikken **[!UICONTROL Select All]**.

1. Hiermee wordt het dialoogvenster **[!UICONTROL Qty]** aan het winkelwagentje toe te voegen.

1. Ga als volgt te werk om de productopties te wijzigen:

   - Klik in het regelitem op de knop _Bewerken_ (![Pictogram Potlood](../assets/icon-edit-pencil.png)).
   - Hiermee wijzigt u de benodigde opties.
   - Klikken **[!UICONTROL Update Requisition List]**.

1. Klikken **[!UICONTROL Add to Cart]**.

   ![Details aanvraaglijst](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### Items naar een andere lijst kopiëren

1. De klant selecteert het selectievakje van elk item dat moet worden verplaatst.

1. Klikken **[!UICONTROL Copy Selected]** en voert een van de volgende handelingen uit:

   - Kies een bestaande aanvraaglijst.
   - Klikken **[!UICONTROL Create New Requisition List]**.

### Een lijst exporteren

1. De klant opent de aanvraaglijst die u wilt exporteren.

1. Klik op de knop **[!UICONTROL Export]** koppeling.

Adobe Commerce genereert en downloadt een CSV-lijst met `sku` en `qty` waarden.

### Items naar een andere lijst verplaatsen

1. De klant selecteert het selectievakje van elk item dat moet worden verplaatst.

1. Klikken **[!UICONTROL Move Selected]** en voer een van de volgende handelingen uit:

   - Kies een bestaande aanvraaglijst.
   - Klikken **[!UICONTROL Create New Requisition List]**.

### Een lijst afdrukken

1. In de rechterbovenhoek van de lijst klikt de klant **[!UICONTROL Print]**.

1. Controleert het uitvoerapparaat en klikt **[!UICONTROL Print]**.

   ![Aanvraaglijst afdrukken](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### Productopties bewerken

De klant doet het volgende om de productopties in de lijst te bewerken:

1. Klik op de knop _Potlood_ (![Pictogram Potlood](../assets/icon-edit-pencil.png)) om de productpagina te openen.

1. Hiermee wijzigt u de benodigde opties.

1. Klikken **[!UICONTROL Update Requisition List]**.

   ![Aanvraaglijst bijwerken](./assets/requisition-list-update.png){width="700" zoomable="yes"}

Een product in de aanvraaglijst kan worden bewerkt als:

- Het product heeft **[!UICONTROL all options set]** (wanneer het een [geconfigureerd product](../catalog/product-create-configurable.md) in de aanvraaglijst).

  Het product is **[!UICONTROL added to this Requisition List]**.

- Het product is [een eenvoudig product met opties](../catalog/settings-advanced-custom-options.md)

- Bewerken is toegestaan voor het producttype.

### Items verwijderen

1. De klant selecteert het selectievakje van elk item dat moet worden verwijderd.

1. Klikken **[!UICONTROL Remove Selected]**.

1. Wanneer ertoe aangezet om te bevestigen, klikt **[!UICONTROL Delete]**.

### De naam van een lijst wijzigen

1. Na de lijsttitel, klikt de klant **[!UICONTROL Rename]**.

1. Hiermee wordt een andere waarde ingevoerd **[!UICONTROL Requisition List Name]**.

1. Klikken **[!UICONTROL Save]**.

   ![Naam aanvraaglijst wijzigen](./assets/requisition-list-rename.png){width="300"}


### Een aanvraaglijst verwijderen

1. De klant opent de aanvraaglijst die moet worden verwijderd.

1. Klikken **[!UICONTROL Delete Requisition List]**.

1. Wanneer ertoe aangezet om te bevestigen, klikt **[!UICONTROL Delete]**.

>[!NOTE]
>
>Deze handeling kan niet ongedaan worden gemaakt.

## Handelingen

| Handeling | Beschrijving |
|--- |--- |
| [!UICONTROL Rename] | Hiermee kunt u de naam van de aanvraaglijst wijzigen en de beschrijving bijwerken. |
| [!UICONTROL Export] | Exporteert de aanvraaglijst naar een CSV-bestand. |
| [!UICONTROL Print] | Hiermee wordt de huidige aanvraaglijst afgedrukt. |
| [!UICONTROL Select] | Beheert de itemselecties die het onderwerp van een handeling moeten zijn. <br/>**[!UICONTROL Select All]**- Hiermee selecteert u alle items in de aanvraaglijst.<br/>**[!UICONTROL Remove Selected]** - Hiermee verwijdert u alle geselecteerde items uit de aanvraaglijst. <br/>**[!UICONTROL Copy Selected]**- Hiermee worden alle geselecteerde items naar een andere aanvraaglijst gekopieerd. |
| [!UICONTROL Add to Cart] | Hiermee voegt u geselecteerde items toe aan het winkelwagentje. |
| [!UICONTROL Update List] | Hiermee herberekent u het subtotaal aan de hand van een wijziging in de hoeveelheid. |
| [!UICONTROL Delete Requisition List] | Verwijdert de aanvraaglijst uit de account van de bedrijfsgebruiker. |

{style="table-layout:auto"}
