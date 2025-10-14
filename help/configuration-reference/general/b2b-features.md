---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL General] &gt; [!UICONTROL B2B Features] van Commerce Admin.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Met de installatie en activering van Adobe Commerce B2B kan de koopervaring worden gepersonaliseerd met bedrijfsspecifieke functies. Adobe Commerce B2B is een geïntegreerde oplossing die zowel B2B- als B2C-modellen ondersteunt. Voor meer informatie over de eigenschappen B2B, zie de [_Gids van de Gebruiker van Adobe Commerce B2B_ &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=nl-NL).

## [!UICONTROL B2B Features]

![&#x200B; B2B Eigenschappen &#x200B;](./assets/b2b-features.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Website | Wanneer toegelaten, staat klanten toe om hun bedrijfstoewijzing van hun rekeningsdashboard te beheren, en laat ook de Gedeelde eigenschappen van de Catalogus en van het Aanhalingsteken B2B door gebrek toe. Opties: `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Website | Wanneer toegelaten, staat klanten en gasten toe om orden snel te plaatsen die op SKU of productnaam worden gebaseerd. Opties: `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Website | Als deze optie is ingeschakeld, kunnen klanten aanvraaglijsten maken en beheren vanaf het dashboard van hun account. |

{style="table-layout:auto"}

![&#x200B; B2B Eigenschappen met bedrijven en gedeelde toegelaten catalogi &#x200B;](./assets/b2b-features-company-enabled.png)<!-- zoom -->

Wanneer de eigenschap van het Bedrijf wordt toegelaten, zijn de extra gebieden beschikbaar voor Gedeelde Catalogus en B2B Citaat.

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Website | Wanneer toegelaten, maakt het mogelijk om gekrulde catalogi met douaneprijzen tot stand te brengen die of globaal, of beperkt tot specifieke bedrijven beschikbaar zijn. Opties: `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Website | Wanneer het veld _[!UICONTROL Enable Shared Catalog]_&#x200B;is ingesteld op `Yes` , is deze optie beschikbaar. Wanneer toegelaten, slechts worden de producten die aan een gedeelde catalogus worden toegewezen opgeslagen in de prijsindex. Producten die niet aan de gedeelde catalogus zijn toegewezen, worden niet in de winkel weergegeven. Opties: `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Website | Als deze optie is ingeschakeld, kunnen kopers van bedrijven een prijsaanvraag indienen via het winkelwagentje. Opties: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![&#x200B; B2B configuratie - de montages van de standaard betalingsmethode &#x200B;](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | Algemeen | Bepaalt de selectie van betalingsmethoden die beschikbaar zijn voor B2B-kopers. Opties: `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | Algemeen | Geeft elke betalingsmethode aan die beschikbaar is voor B2B-kopers. |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![&#x200B; B2B configuratie - standaard verschepende methodes &#x200B;](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | Algemeen | Bepaalt de selectie van verzendmethoden die standaard beschikbaar zijn voor B2B-kopers. Opties: `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | Algemeen | Geeft elke verzendmethode aan die standaard beschikbaar is voor B2B-kopers. <br/>**_Nota:_**&#x200B;u kunt de het verschepen methodes voor een specifieke [&#x200B; bedrijfrekening &#x200B;](../../b2b/account-companies.md) ook beperken. |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![&#x200B; B2B Eigenschappen - de Configuratie van de Goedkeuring van de Orde &#x200B;](./assets/b2b-features-order-approval.png)<!-- zoom -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Website | Als deze optie is ingeschakeld, kunnen bedrijven kooporders maken. Opties: `Yes` / `No` |

{style="table-layout:auto"}


