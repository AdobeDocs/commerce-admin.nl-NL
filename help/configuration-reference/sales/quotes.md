---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Sales] &gt; [!UICONTROL Quotes] pagina van Commerce Admin.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Met de installatie en activering van Adobe Commerce B2B kan de koopervaring worden gepersonaliseerd met bedrijfsspecifieke functies. Adobe Commerce B2B is een geïntegreerde oplossing die zowel B2B- als B2C-modellen ondersteunt. Voor meer informatie over de B2B-functies raadpleegt u de [Adobe Commerce B2B-gebruikershandleiding](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![Algemeen](./assets/quotes-general.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Website | Het minimumbedrag van het winkelwagentsubtotaal, na eventuele kortingen, dat vereist is voordat een klant een prijsaanvraag kan indienen. Standaardwaarde: `0` |
| [!UICONTROL Minimum Amount Message] | Winkelweergave | Het bericht dat in het winkelwagentje wordt weergegeven wanneer een klant een aanvraag voor een prijsopgave probeert in te dienen, maar er wordt niet voldaan aan het vereiste minimumbedrag. |
| [!UICONTROL Default Expiration Period] | Website | Hiermee wordt de standaardlevensduur van een [citeren](../../b2b/quote-price-negotiation.md) als periode vanaf de datum waarop het verzoek om een prijsopgave wordt ingediend. Opties: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Bijgevoegde bestanden](./assets/quotes-attached-files.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Algemeen | Hiermee bepaalt u de bestandsindelingen die aan een offerte kunnen worden gekoppeld. Ondersteunde standaardwaarden: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, en `jpeg` |
| [!UICONTROL Maximum file size] | Algemeen | Bepaalt de maximumgrootte voor een dossier dat aan een citaat wordt vastgemaakt. Deze instelling kan worden overschreven door de serverconfiguratie. |

{style="table-layout:auto"}
