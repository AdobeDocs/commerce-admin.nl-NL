---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Customers] &gt; [!UICONTROL Invitations] pagina van de Commerce Admin.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![Algemeen](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Algemeen | Hiermee wordt bepaald of de module Uitnodigingen is ingeschakeld. Opties: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Website | Hiermee bepaalt u of uitnodigingen kunnen worden beheerd vanuit de storefront. Opties: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Winkelweergave | Bepaalt de klantengroep van invitee. Opties: <br/>**`Same as Inviter`**- Genodigden worden automatisch toegewezen aan dezelfde klantengroep als de klanten die hen hebben uitgenodigd.<br/>**`Default Customer Group from Configuration`** - Genodigden hebben automatisch de standaardwaarde [klantengroep](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | Winkelweergave | Hiermee bepaalt u hoe genodigden een account kunnen maken. Opties: <br/>**`By Invitation Only`**- Genodigden moeten de koppeling in de e-mail met uitnodiging volgen om een account te maken.<br/>**`Available to All`** - Genodigden kunnen het registratieformulier voor hun account gebruiken dat beschikbaar is in de winkel. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Winkelweergave | Hiermee wordt bepaald of het uitnodigingsformulier een veld bevat waarin de inviter een aangepast bericht kan toevoegen dat via e-mail naar de invitee wordt verzonden. Dit beïnvloedt niet de capaciteit van de beheerder om een bericht aan een Uitnodiging toe te voegen. Opties: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Winkelweergave | Bepaalt het maximumaantal uitnodigingen dat de inviter tegelijk kan verzenden. Er wordt een andere uitnodiging verzonden naar elk e-mailadres dat de inviter in het formulier heeft opgenomen. Dit beschermt servermiddelen door grote aantallen Uitnodigingen te verhinderen tegelijkertijd worden verzonden, en maakt het minder waarschijnlijk voor uitnodigingen om als spam worden verzonden. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Email]

![E-mail](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Winkelweergave | Bepaalt de afzender van de e-mail die invitees ontvangt wanneer een uitnodigings-e-mail wordt verzonden. Standaardwaarde: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Winkelweergave | Bepaalt de sjabloon van het e-mailbericht dat genodigden ontvangen wanneer een e-mailuitnodiging wordt verzonden. Standaardsjabloon: `Customer Invitation` |

{:style=&quot;table-layout:auto&quot;}
