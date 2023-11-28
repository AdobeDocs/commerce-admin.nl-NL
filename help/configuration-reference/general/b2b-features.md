---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL General] &gt; [!UICONTROL B2B Features] pagina van de Commerce Admin.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 4f4ddb6da9bbf3bc07efb3b8518ee71323d43b49
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Met de installatie en activering van B2B voor Adobe Commerce, kan de koopervaring met bedrijf-specifieke eigenschappen worden gepersonaliseerd. B2B voor Adobe Commerce is een geïntegreerde oplossing die zowel B2B- als B2C-modellen ondersteunt. Voor meer informatie over de B2B-functies raadpleegt u de [_B2B voor Adobe Commerce-gebruikershandleiding_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![B2B-functies](./assets/b2b-features.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Website | Wanneer toegelaten, staat klanten toe om hun bedrijfstoewijzing van hun rekeningsdashboard te beheren, en laat ook de Gedeelde eigenschappen van de Catalogus en van het Aanhalingsteken B2B door gebrek toe. Opties: `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Website | Wanneer toegelaten, staat klanten en gasten toe om orden snel te plaatsen die op SKU of productnaam worden gebaseerd. Opties: `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Website | Als deze optie is ingeschakeld, kunnen klanten aanvraaglijsten maken en beheren vanaf het dashboard van hun account. |

{:style=&quot;table-layout:auto&quot;}

![B2B-functies met bedrijven en gedeelde catalogi ingeschakeld](./assets/b2b-features-company-enabled.png)<!-- zoom -->

Wanneer de eigenschap van het Bedrijf wordt toegelaten, zijn de extra gebieden beschikbaar voor Gedeelde Catalogus en B2B Citaat.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Website | Wanneer toegelaten, maakt het mogelijk om gekrulde catalogi met douaneprijzen tot stand te brengen die of globaal, of beperkt tot specifieke bedrijven beschikbaar zijn. Opties: `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Website | Wanneer de _[!UICONTROL Enable Shared Catalog]_veld is ingesteld op `Yes`, is deze optie beschikbaar. Wanneer toegelaten, slechts worden de producten die aan een gedeelde catalogus worden toegewezen opgeslagen in de prijsindex. Producten die niet aan de gedeelde catalogus zijn toegewezen, worden niet in de winkel weergegeven. Opties: `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Website | Als deze optie is ingeschakeld, kunnen kopers van bedrijven een prijsaanvraag indienen via het winkelwagentje. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Default B2B Payment Methods]

![B2B-configuratie - betalingsmethode-instellingen voor wanbetaling](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | Algemeen | Bepaalt de selectie van betalingsmethoden die beschikbaar zijn voor B2B-kopers. Opties: `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | Algemeen | Geeft elke betalingsmethode aan die beschikbaar is voor B2B-kopers. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Default B2B Shipping Methods]

![B2B-configuratie - standaardverzendmethoden](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | Algemeen | Bepaalt de selectie van verzendmethoden die standaard beschikbaar zijn voor B2B-kopers. Opties: `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | Algemeen | Geeft elke verzendmethode aan die standaard beschikbaar is voor B2B-kopers. <br/>**_Opmerking:_**U kunt ook de verzendmethoden beperken voor een specifieke [bedrijfsaccount](../../b2b/account-companies.md). |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order Approval Configuration]

![B2B-functies - Configuratie voor goedkeuring van bestellingen](./assets/b2b-features-order-approval.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Website | Als deze optie is ingeschakeld, kunnen bedrijven kooporders maken. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}


