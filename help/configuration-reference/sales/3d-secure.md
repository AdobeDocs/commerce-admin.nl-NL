---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] van Commerce Admin.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] is ontwikkeld door [!DNL Visa] om veilige online transacties te promoten. Voorbeelden van [!DNL 3-D Secure] -oplossingen die door kaartnetwerken worden gemaakt, worden geverifieerd door [!DNL Visa] , [!DNL Mastercard SecureCode] , [!DNL American Express SafeKey] en [!DNL CardinalCommerce Consumer Authentication] . [!DNL CardinalCommerce] is wereldwijd marktleider op het gebied van digitale transactieverificatie en een volledige dochteronderneming van [!DNL Visa] .

[!DNL 3-D Secure] versie 2.0 ondersteunt talrijke verbeteringen, zoals geavanceerde verificatiemethoden en verificatiestroom, en verbeterde gegevensuitwisseling tussen leverancier en leverancier.

>[!NOTE]
>
>De ](../../stores-purchase/braintree.md) betaalgateway van de Braintree [ {steunt ook [!DNL 3-D Secure] controle.

{{config}}

## [!UICONTROL CardinalCommerce]

![ CardinalCommerce ](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Environment] | Website | Geeft de werkingsmodus van uw [!DNL CardinalCommerce] -account aan. Als u in een testomgeving werkt, kiest u &#39;Sandbox&#39;. Opties: zandbak/productie (standaard) |
| [!UICONTROL Org Unit ID] | Website | De organisatie-eenheid-id van uw [!DNL CardinalCommerce] -zakelijke account. |
| [!UICONTROL API Key] | Website | De API-sleutel van uw [!DNL CardinalCommerce] -zakelijke account. |
| [!UICONTROL API Identifier] | Website | De API-id van uw [!DNL CardinalCommerce] -zakelijke account. |
| [!UICONTROL Debug] | Website | Opties: `Yes` / `No` |

{style="table-layout:auto"}
