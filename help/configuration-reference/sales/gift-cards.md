---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] pagina van de Commerce Admin.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![E-mailinstellingen creditcard](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Winkelweergave | Identificeert de [contactpersoon voor winkel](../../getting-started/store-details.md#store-email-addresses) die wordt weergegeven als de afzender van het e-mailbericht voor een cadeaukaart. Standaardwaarde: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Winkelweergave | Hiermee bepaalt u de [template](../../systems/email-templates.md) die wordt gebruikt voor het e-mailbericht voor een cadeaukaart. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Gift Card General Settings]

![Algemene instellingen voor creditcard](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Algemeen | Hiermee bepaalt u of de houder van de cadeau-kaart zijn waarde voor contant geld kan inwisselen. Opties: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Algemeen | Hiermee bepaalt u hoeveel dagen de kaart geldig is. Als de kaart leeg blijft, verloopt deze niet. <br/><br/>**_Belangrijk:_**Op sommige plaatsen is het illegaal om vervalgegevens in te stellen voor cadeaukaarten. Controleer uw lokale wetten voordat u een leven instelt voor uw cadeaukaarten. |
| [!UICONTROL Allow Gift Message] | Winkelweergave | Bepaalt of de optie om een cadeaubericht op te nemen beschikbaar is voor klanten die een cadeaukaart aanschaffen. Opties: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Winkelweergave | Hiermee bepaalt u het maximum aantal tekens dat is toegestaan in een cadeaukaartbericht. Standaardwaarde: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Algemeen | Hiermee bepaalt u of een rekening met een cadeaukaart wordt gegenereerd wanneer een klant een bestelling plaatst of wanneer de bestelling wordt gefactureerd. Opties: `Ordered` / `Invoiced` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Email Sent from Gift Card Account Management]

![E-mail verzonden vanuit accountbeheer voor creditcard](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Winkelweergave | Identificeert de [contactpersoon voor winkel](../../getting-started/store-details.md#store-email-addresses) die wordt weergegeven als de afzender van de e-mail met de cadeaukaart. Standaardwaarde: `General Contact` |
| [!UICONTROL Gift Card Template] | Winkelweergave | Hiermee bepaalt u de [template](../../systems/email-templates.md) wordt gebruikt voor het e-mailadres van de cadeaukaart. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Gift Card Account General Settings]

![Algemene instellingen Cadeaukaartaccount](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Code Length] | Algemeen | Hiermee bepaalt u de lengte van de code van de cadeau-kaart. |
| [!UICONTROL Code Format] | Algemeen | Bepaalt de opmaak van de code van de cadeau-kaart. Opties: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Algemeen | Hiermee definieert u een voorvoegsel dat aan het begin van de code wordt toegevoegd. |
| [!UICONTROL Code Suffix] | Algemeen | Bepaalt om het even welk achtervoegsel dat aan het eind van de code wordt toegevoegd. |
| [!UICONTROL Dash Every X Characters] | Algemeen | Als u streepjes in de code wilt opnemen, bepaalt u het aantal tekens tussen de streepjes. |
| [!UICONTROL New Pool Size] | Algemeen | Hiermee bepaalt u de grootte van de nieuwe codepool die moet worden gegenereerd. |
| [!UICONTROL Low Code Pool Threshold] | Algemeen | Bepaalt het aantal verslagen in de codepool die een alarm teweegbrengt dat de pool moet worden aangevuld. |
| [!UICONTROL Generate] | Algemeen | Klik om de lijst met kaartcodes voor cadeaus te genereren. |

{:style=&quot;table-layout:auto&quot;}
