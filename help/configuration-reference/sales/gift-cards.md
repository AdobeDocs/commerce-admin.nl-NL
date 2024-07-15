---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] van Commerce Admin.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![ E-mailmontages van de Kaart van het Cadeautje ](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Winkelweergave | Identificeert het [ opslagcontact ](../../getting-started/store-details.md#store-email-addresses) dat als afzender van het e-mailbericht van het cadeaukaartbericht verschijnt. Standaardwaarde: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Winkelweergave | Bepaalt het [ malplaatje ](../../systems/email-templates.md) dat voor het bericht e-mail van de cadeaukaart wordt gebruikt. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![ Algemene Montages van de Kaart van het Cadeautje ](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Algemeen | Hiermee bepaalt u of de houder van de cadeau-kaart zijn waarde voor contant geld kan inwisselen. Opties: `Yes` / `No` . |
| [!UICONTROL Lifetime (days)] | Algemeen | Hiermee bepaalt u hoeveel dagen de kaart geldig is. Als de kaart leeg blijft, verloopt deze niet. <br/><br/>**_Belangrijk:_**in sommige plaatsen, is het illegaal om een vervalsingsgegevens op giftekaarten te plaatsen. Controleer uw lokale wetten voordat u een leven instelt voor uw cadeaukaarten. |
| [!UICONTROL Allow Gift Message] | Winkelweergave | Bepaalt of de optie om een cadeaubericht op te nemen beschikbaar is voor klanten die een cadeaukaart aanschaffen. Opties: `Yes` / `No` . |
| [!UICONTROL Gift Message Maximum Length] | Winkelweergave | Hiermee bepaalt u het maximum aantal tekens dat is toegestaan in een cadeaukaartbericht. Standaardwaarde: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Algemeen | Hiermee bepaalt u of een rekening met een cadeaukaart wordt gegenereerd wanneer een klant een bestelling plaatst of wanneer de bestelling wordt gefactureerd. Opties: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![ E-mail die van het Beheer van de Rekening van de Kaart van de Kaart wordt verzonden ](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Winkelweergave | Identificeert het [ opslagcontact ](../../getting-started/store-details.md#store-email-addresses) dat als afzender van het e-mailbericht van de giftekaart verschijnt. Standaardwaarde: `General Contact` |
| [!UICONTROL Gift Card Template] | Winkelweergave | Bepaalt het [ malplaatje ](../../systems/email-templates.md) dat voor het e-mailbericht van de cadeaukaart wordt gebruikt. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![ de Algemene Montages van de Rekening van de Kaart van het Cadeautje ](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Code Length] | Algemeen | Hiermee bepaalt u de lengte van de code van de cadeau-kaart. |
| [!UICONTROL Code Format] | Algemeen | Bepaalt de opmaak van de code van de cadeau-kaart. Opties: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Algemeen | Hiermee definieert u een voorvoegsel dat aan het begin van de code wordt toegevoegd. |
| [!UICONTROL Code Suffix] | Algemeen | Bepaalt om het even welk achtervoegsel dat aan het eind van de code wordt toegevoegd. |
| [!UICONTROL Dash Every X Characters] | Algemeen | Als u streepjes in de code wilt opnemen, bepaalt u het aantal tekens tussen de streepjes. |
| [!UICONTROL New Pool Size] | Algemeen | Hiermee bepaalt u de grootte van de nieuwe codepool die moet worden gegenereerd. |
| [!UICONTROL Low Code Pool Threshold] | Algemeen | Bepaalt het aantal verslagen in de codepool die een alarm teweegbrengt dat de pool moet worden aangevuld. |
| [!UICONTROL Generate] | Algemeen | Klik om de lijst met kaartcodes voor cadeaus te genereren. |

{style="table-layout:auto"}
