---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Customers] &gt; [!UICONTROL Invitations] van Commerce Admin.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![&#x200B; Algemeen &#x200B;](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Algemeen | Hiermee wordt bepaald of de module Uitnodigingen is ingeschakeld. Opties: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Website | Hiermee bepaalt u of uitnodigingen kunnen worden beheerd vanuit de storefront. Opties: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Winkelweergave | Bepaalt de klantengroep van invitee. Opties: <br/>**`Same as Inviter`**- genodigden worden automatisch toegewezen aan dezelfde klantengroep als de klanten die hen hebben uitgenodigd.<br/>**`Default Customer Group from Configuration`** - Invitees hebben automatisch de standaard [&#x200B; klantengroep &#x200B;](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | Winkelweergave | Hiermee bepaalt u hoe genodigden een account kunnen maken. Opties: <br/>**`By Invitation Only`**- genodigden moeten de koppeling in het e-mailbericht Uitnodiging volgen om een account te maken.<br/>**`Available to All`** - Genodigden kunnen het registratieformulier voor hun account gebruiken dat beschikbaar is in de winkel. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Winkelweergave | Hiermee wordt bepaald of het uitnodigingsformulier een veld bevat waarin de inviter een aangepast bericht kan toevoegen dat via e-mail naar de invitee wordt verzonden. Dit beïnvloedt niet de capaciteit van de beheerder om een bericht aan een Uitnodiging toe te voegen. Opties: `Yes` / `No` . |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Winkelweergave | Bepaalt het maximumaantal uitnodigingen dat de inviter tegelijk kan verzenden. Er wordt een andere uitnodiging verzonden naar elk e-mailadres dat de inviter in het formulier heeft opgenomen. Dit beschermt servermiddelen door grote aantallen Uitnodigingen te verhinderen tegelijkertijd worden verzonden, en maakt het minder waarschijnlijk voor uitnodigingen om als spam worden verzonden. |

{style="table-layout:auto"}

## [!UICONTROL Email]

![&#x200B; E-mail &#x200B;](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Veld | [&#x200B; Reikwijdte &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Winkelweergave | Bepaalt de afzender van de e-mail die invitees ontvangt wanneer een uitnodigings-e-mail wordt verzonden. Standaardwaarde: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Winkelweergave | Bepaalt de sjabloon van het e-mailbericht dat genodigden ontvangen wanneer een e-mailuitnodiging wordt verzonden. Standaardsjabloon: `Customer Invitation` |

{style="table-layout:auto"}
