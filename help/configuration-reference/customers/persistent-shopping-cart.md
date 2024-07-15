---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] van Commerce Admin.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [ Persistent het Vormen Kart ](../../stores-purchase/cart-persistent.md) staat behoud van niet gekochte punten toe die in de kar worden verlaten en bewaart hen voor een periode die in _het Levensduur van de Persistentie_ wordt gevormd. Cookies moeten in de browser van de klant worden toegestaan om een hardnekkig winkelwagentje te gebruiken.

## [!UICONTROL General Options]

![ Algemene Opties ](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Website | Hiermee wordt bepaald of de persistentie is ingeschakeld. |
| [!UICONTROL Persistence Lifetime (seconds)] | Website | Definieert de levensduur van de permanente cookie in seconden. De maximaal toegestane waarde is 3153600000 seconden (100 jaar). |
| [!UICONTROL Enable "Remember Me"] | Website | Bepaalt of _me_ checkbox herinnert verschijnt op login en registratiepagina&#39;s van de opslag. Opties: <br/>**`Yes`**- toont _me_ checkbox herinnert.<br/>**`No`** - toont niet _me_ checkbox herinnert, en het blijvende koekje wordt gebruikt slechts voor klanten die het reeds hebben. |
| [!UICONTROL "Remember Me" Default Value] | Website | Bepaalt de standaardstaat voor _me_ checkbox herinneren. |
| [!UICONTROL Clear Persistence on Log Out] | Website | Bepaalt of het blijvende koekje wordt geschrapt wanneer een winkelklant zich uitlogt. Ongeacht hoe dit wordt gevormd, als een klant niet logout, maar het zittingskoekje verloopt, wordt het blijvende koekje nog gebruikt. |
| [!UICONTROL Persist Shopping Cart] | Website | Hiermee bepaalt u of het gebruik van de permanente cookie toegang geeft tot de gegevens van het winkelwagentje van de correspondentaccount. Opties: <br/>**`Yes`**- De inhoud van het winkelwagentje wordt opgeslagen nadat de sessie is beëindigd.<br/>**`No`** - De inhoud van het winkelwagentje wordt niet opgeslagen nadat de sessie is beëindigd. |
| [!UICONTROL Persist Wish List] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de staat van klant wenst lijsten wordt behouden wanneer de zitting beëindigt. Opties: <br/>**`Yes`**- De inhoud van de wensenlijst wordt opgeslagen wanneer de sessie wordt beëindigd.<br/>**`No`** - De lijst met wensen wordt niet opgeslagen wanneer de sessie wordt beëindigd. |
| [!UICONTROL Persist Recently Ordered Items] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de staat van onlangs bevolen punten wordt behouden wanneer de zitting beëindigt. Opties: <br/>**`Yes`**- De status van onlangs geordende items wordt opgeslagen wanneer de sessie wordt beëindigd.<br/>**`No`** - De status van recent bestelde items wordt niet opgeslagen wanneer de sessie wordt beëindigd. |
| [!UICONTROL Persist Currently Compared Products] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de staat van momenteel vergeleken producten wordt behouden wanneer de zitting beëindigt. Opties: <br/>**`Yes`**- De status van de momenteel vergeleken producten wordt opgeslagen wanneer de sessie wordt beëindigd.<br/>**`No`** - De status van de momenteel vergeleken producten wordt niet opgeslagen wanneer de sessie wordt beëindigd. |
| [!UICONTROL Persist Comparison History] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de staat van vergelijkingsgeschiedenis wordt behouden wanneer de zitting beëindigt. Opties: <br/>**`Yes`**- De vergelijkingsgeschiedenis wordt opgeslagen wanneer de sessie wordt beëindigd.<br/>**`No`** - De vergelijkingsgeschiedenis wordt niet opgeslagen wanneer de sessie wordt beëindigd. |
| [!UICONTROL Persist Recently Viewed Products] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de staat van onlangs bekeken producten wordt behouden wanneer de zitting beëindigt. Opties: <br/>**`Yes`**- De status van onlangs bekeken producten wordt opgeslagen wanneer de sessie wordt beëindigd.<br/>**`No`** - De status van onlangs bekeken producten wordt niet opgeslagen wanneer de sessie wordt beëindigd. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Website | ![ Adobe Commerce ](../../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de staat van de groepslidmaatschap van klanten en de segmenteringscriteria worden behouden wanneer de zitting beëindigt. Opties: <br/>**`Yes`**- De status van het groepslidmaatschap van de klant en de segmentatiegegevens worden opgeslagen wanneer de sessie wordt beëindigd.<br/>**`No`** - De status van het groepslidmaatschap van de klant en de segmentatiegegevens worden niet opgeslagen wanneer de sessie wordt beëindigd. |

{style="table-layout:auto"}
