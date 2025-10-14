---
title: Enable  [!DNL Inventory Management]
description: Leer hoe te om  [!DNL Inventory Management]  op de globale opslag of productniveau toe te laten.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Inventory Management] inschakelen

Schakel [!DNL Inventory Management] in de winkel of op productniveau in om uw productvoorraad te beheren. Wanneer de _beheert de optie van de Voorraad_ wordt toegelaten, [!DNL Inventory Management] volgt automatisch producthoeveelheden beschikbaar voor de plaats door gevormde voorraden en bronnen. Elke functie en optie begint het volgen en het melden wanneer toegelaten, zonder extra configuratie.

Uw bedrijf loopt en inventarisupdates bij de snelheid van verkoop. Als klanten winkelen, ontvangt u nauwkeurige, bijgewerkte informatie voor beschikbare voorraad per verkoopkanaal en bron. Beschikbare verkoopbare hoeveelheden worden per voorraad bijgewerkt wanneer klanten producten aan winkelwagentjes toevoegen en aankopen voltooien, en wanneer en u bestellingen beheert, verzendingen maakt en terugbetalingen uitgeeft. Aanschaffen van nieuwe of overgedragen voorraad-update naar uw bronnen, direct beschikbaar voor online verkoop. Backorders voltooien tot gespecificeerde drempels zonder oneindige orden of extra configuraties. En u gaat en voltooit gedeeltelijke of volledige ladingen over één of meerdere bronnen met aanbevelingen in, die u volledige controle over ordenaleving en voorraad geven.

>[!NOTE]
>
>[!DNL Inventory Management] wordt standaard ingeschakeld wanneer u [!DNL Commerce] installeert of bijwerkt. Afhankelijk van uw bedrijfsbehoeften, kunt u volgen [!DNL Inventory Management] binnen [!DNL Commerce] toelaten of willen onbruikbaar maken.

Hoe deze instelling werkt in inventarissen van één en meerdere bronnen:

- Schakel _[!UICONTROL Manage Stock]_&#x200B;in als u [!DNL Inventory Management] wilt gebruiken.

- [!UICONTROL Manage Stock] de montages op de productconfiguratie treden de archiefconfiguratie met voeten.

- Schakel [!UICONTROL Manage Stock] uit als u Order Management of services van derden (zoals ERP) wilt gebruiken.

- Als de configuratie van het productniveau het systeemgebrek gebruikt, treedt de opslagconfiguratie met voeten.

Als [!DNL Inventory Management] is ingeschakeld, raadpleegt u het volgende om alle instellingen te configureren:

- [&#x200B; het Vormen Globale Opties &#x200B;](global-options.md) - Montages die uw volledige catalogus beïnvloeden, beschouwden de systeemstandaardmontages.

- [&#x200B; het Vormen de Opties van het Product &#x200B;](product-options.md) - Montages voor een specifiek product dat globale opties met voeten treedt.

## [!DNL Inventory Management] in- of uitschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Inventory]** .

1. Breid ![&#x200B; de selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) _Opties van de Voorraad van het Product_ uit en vorm:

   ![&#x200B; Opties van de Voorraad van het Product &#x200B;](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Als u een overzicht wilt beheren en alle [!DNL Commerce] -functies wilt gebruiken, stelt u **[!UICONTROL Manage Stock]** in op `Yes` (standaardwaarde).

   - Als u [!DNL Inventory Management] wilt uitschakelen, schakelt u het selectievakje **[!UICONTROL Use system value]** uit en stelt u **[!UICONTROL Manage Stock]** in op `No` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## De voorraad voor een winkel beheren

Zie [&#x200B; Globale Opties &#x200B;](global-options.md) vormen.

## De voorraad voor een product beheren

Zie [&#x200B; het Vormen de Opties van het Product &#x200B;](product-options.md).
