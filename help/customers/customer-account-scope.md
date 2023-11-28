---
title: Bereik van klantenaccount
description: Het bereik van klantenaccounts kan worden beperkt tot de website waar het account is gemaakt of wordt gedeeld met alle websites en winkels in de winkelhiërarchie.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 2541b2d55516e2a9c824825100c8348d81201ca9
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Bereik van klantenaccount

De koptekst van elke pagina in uw winkel breidt een uitnodiging voor kopers uit tot _Aanmelden of registreren_ voor een account bij je winkel. Klanten die een account openen, hebben een groot aantal voordelen, zoals:

* **Klantenaccount maken** - Bezoekers kunnen een klantenaccount maken zodat ze de winkel als geregistreerde klant kunnen gebruiken.
* **Een bedrijfsaccount maken** Afhankelijk van de configuratie kan een bezoeker van uw winkel desgewenst een bedrijfsaccount maken. Zie voor meer informatie [B2B voor Adobe Commerce](../b2b/introduction.md).
* **Snellere controle** — Geregistreerde klanten gaan sneller door met het afrekenen omdat veel van de gegevens al in hun accounts staan.
* **Zelfbediening** — Geregistreerde klanten kunnen hun gegevens bijwerken, de status van bestellingen controleren en zelfs van hun accounts opnieuw rangschikken.

Klanten hebben toegang tot hun account door op de knop **[!UICONTROL My Account]** in de koptekst van de winkel. Vanaf hun account kunnen klanten informatie weergeven en wijzigen, zoals oude en huidige adressen, facturerings- en verzendvoorkeuren, abonnementen op nieuwsbrieven, wenslijst en meer.

![Mijn account](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Bereik van klantenaccounts instellen

Het bereik van klantenaccounts kan worden beperkt tot de website waar het account is gemaakt of wordt gedeeld met alle websites en winkels in de winkelhiërarchie.

>[!NOTE]
>
>Als de website is uitgesloten van de klantengroep, mag de klant zich niet aanmelden bij de website wanneer het bereik van de klantenaccounts beperkt is tot de website of met alle websites wordt gedeeld. Zie [Een klantengroep maken](customer-groups.md#create-a-customer-group) voor meer informatie over het uitsluiten van websites van groepen .

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Vouw de sectie **[!UICONTROL Account Sharing Options]** uit.

   ![Opties voor het delen van accounts](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Share Customer Accounts]** op een van de volgende wijzen:

   | Optie | Beschrijving |
   | --- | --- |
   | `Global` | Deelt de informatie van de klantenrekening met elke website en opslag in de installatie. |
   | `Per Website` | Hiermee beperkt u de gegevens van de klantenaccount tot de website waar het account is gemaakt. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Indien nodig de **[!UICONTROL User system value]** Schakel het selectievakje in om de wijziging aan te brengen.

1. Klik op **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Wanneer `Global` is geselecteerd in **Mijn account** (adressen en accountgegevens zoals contactgegevens) worden gedeeld.
