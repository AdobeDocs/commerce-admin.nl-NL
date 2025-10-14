---
title: Een klantengroep toewijzen aan een bedrijf
description: Meer informatie over het toewijzen van een klantengroep aan een bedrijfsaccount in uw Adobe Commerce-winkel.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Een klantengroep toewijzen aan een bedrijf

Het toewijzen van een klantengroep aan een bedrijf is in wezen het zelfde als het toewijzen van een gedeelde catalogus. Als de Gedeelde Catalogus niet [&#x200B; in de configuratie &#x200B;](enable-basic-features.md) wordt toegelaten, wordt een Groep van de Klant — eerder dan een Gedeelde Catalogus — toegewezen aan een bedrijf.

- Er kan slechts één klantengroep of gedeelde catalogus tegelijk aan een bedrijf worden toegewezen. Een klantengroep die is gekoppeld aan een gedeelde catalogus, kan niet worden verwijderd.
- Als u de klantengroep wijzigt die aan het bedrijf is toegewezen, worden de profielen van alle leden van het bedrijf bijgewerkt.
- Als de toewijzing van de klantengroep van een gedeelde catalogus in een regelmatige klantengroep wordt veranderd, verliezen de bedrijfsleden toegang tot de gedeelde catalogus en de primaire catalogus wordt beschikbaar aan hen van de winkel.
- Nadat het veranderen van de bedrijvengroep, moet een bedrijfgebruiker zich afmelden en op Storefront aanmelden om nieuwe prijzen in de catalogus te zien.

## De klantengroep wijzigen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek het bedrijf in het raster en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

   ![&#x200B; geef Bedrijf &#x200B;](./assets/companies-grid-edit.png){width="700" zoomable="yes"} uit

1. Voor de bedrijfpagina, scrol neer en breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Advanced Settings]** sectie.

1. Stel de juiste **[!UICONTROL Customer Group]** in.

   De lijst [!UICONTROL Customer Group] bevat alle bestaande gedeelde catalogi, zelfs als Gedeelde catalogi is uitgeschakeld in de configuratie.

   ![&#x200B; de klantengroep van de Verandering of gedeelde catalogus &#x200B;](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Klik op **[!UICONTROL Proceed]** wanneer u wordt gevraagd om te bevestigen.

1. Klik op **[!UICONTROL Save]**.
