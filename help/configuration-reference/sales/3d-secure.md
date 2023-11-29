---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] pagina van de Commerce Admin.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] is ontwikkeld door [!DNL Visa] veilige onlinetransacties bevorderen. Voorbeelden van [!DNL 3-D Secure] oplossingen die door kaartnetwerken worden gecreeerd worden geverifieerd door [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey], en [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] is wereldwijd marktleider op het gebied van authenticatie van digitale transacties en een volledige dochteronderneming van [!DNL Visa].

[!DNL 3-D Secure] versie 2.0 steunt talrijke verhogingen, met inbegrip van geavanceerde authentificatiemethodes en authentificatiestroom, en betere gegevens het delen tussen handelaars en uitgever.

>[!NOTE]
>
>De [Braintree](../../stores-purchase/braintree.md) betaalgateway ondersteunt ook [!DNL 3-D Secure] verificatie.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Environment] | Website | Geeft de besturingsmodus van uw [!DNL CardinalCommerce] account. Als u in een testomgeving werkt, kiest u &#39;Sandbox&#39;. Opties: zandbak/productie (standaard) |
| [!UICONTROL Org Unit ID] | Website | De eenheid-id van uw organisatie [!DNL CardinalCommerce] zakelijke rekening. |
| [!UICONTROL API Key] | Website | De API-sleutel van uw [!DNL CardinalCommerce] zakelijke rekening. |
| [!UICONTROL API Identifier] | Website | De API-id van uw [!DNL CardinalCommerce] zakelijke rekening. |
| [!UICONTROL Debug] | Website | Opties: `Yes` / `No` |

{style="table-layout:auto"}
