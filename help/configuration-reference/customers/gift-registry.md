---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] pagina van de Commerce Admin.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Ga voor gedetailleerde informatie over het gebruik van deze instellingen naar [Cadeauregisters configureren](../../merchandising-promotions/gift-registry-configure.md). Ga voor meer informatie over het opnemen van gegevens in het register naar [Zoeken naar cadeauregister toevoegen](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Algemene opties](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Winkelweergave | Hiermee wordt bepaald of cadeauregisters beschikbaar zijn. Opties: <br/>**`Yes`**- Schakelt cadeauregisters in voor de geselecteerde winkelweergave. Het tabblad Cadeauregister wordt weergegeven in het dashboard van de account van geregistreerde klanten.<br/>**`No`** - Cadeauregisters zijn niet beschikbaar voor de winkelweergave. |
| [!UICONTROL Maximum Registrants] | Winkelweergave | Hiermee stelt u het aantal personen in dat een klant kan toevoegen aan een cadeauregister. De klant deelt het cadeauregister met elke registrant. In de winkel _Registrant toevoegen_ is beschikbaar voor klanten tot het maximumaantal wordt bereikt. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Eigenaarbericht](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Template] | Winkelweergave | Bepaalt het malplaatje voor de e-mail van het Bericht van de Eigenaar wordt gebruikt die wordt verzonden wanneer een geschenkregister wordt gecreeerd. Standaardsjabloon: bericht eigenaar van cadeauregister |
| [!UICONTROL Email Sender] | Winkelweergave | Identificeert de [contactpersoon voor winkel](../../getting-started/store-details.md#store-email-addresses) die wordt weergegeven als de afzender van het e-mailbericht van eigenaar van cadeauregister. Standaardwaarde: `General Contact` |

{style="table-layout:auto"}

## Cadeauregister delen

![Cadeauregister delen](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Template] | Winkelweergave | Bepaalt het malplaatje voor het Gedeelde e-mail van het Registratie van het Cadeautje wordt gebruikt dat wordt verzonden wanneer een geschenkregister wordt gecreeerd. Wanneer de eigenaar klikt _Cadeauregister delen_, wordt de e-mail verzonden naar elke ontvanger. Standaardsjabloon: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Winkelweergave | Identificeert de [contactpersoon voor winkel](../../getting-started/store-details.md#store-email-addresses) die wordt weergegeven als de afzender van de e-mail voor het delen van het cadeauregister. Standaardwaarde: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Winkelweergave | Het maximumaantal berichten dat via e-mailberichten kan worden verzonden bij het delen van een cadeauregister. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Bijwerken register van geschenk](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Template] | Winkelweergave | Bepaalt het malplaatje voor de e-mail van de Update van de Registratie van het Cadeautje wordt gebruikt die wordt verzonden naar de eigenaar van het cadeauregister wanneer een aankoop van het cadeauregister wordt gemaakt dat. De update bevat informatie over het aangeschafte item en het aangeschafte aantal, maar bevat niet de naam van de persoon die de order heeft geplaatst. Standaardsjabloon: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Winkelweergave | Identificeert de [contactpersoon voor winkel](../../getting-started/store-details.md#store-email-addresses) die wordt weergegeven als de afzender van de e-mail met de update van het Cadeauregister. Standaardwaarde: `General Contact` |

{style="table-layout:auto"}
