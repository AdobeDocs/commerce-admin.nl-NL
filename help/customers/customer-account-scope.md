---
title: Bereik van klantenaccount
description: Het bereik van klantenaccounts kan worden beperkt tot de website waar het account is gemaakt of wordt gedeeld met alle websites en winkels in de winkelhiërarchie.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Bereik van klantenaccount

De kopbal van elke pagina in uw opslag breidt een uitnodiging voor kopers tot _Login of register_ voor een rekening met uw opslag uit. Klanten die een account openen, hebben een groot aantal voordelen, zoals:

* **creeer klantenrekening** - de Bezoekers kunnen een klantenrekening tot stand brengen zodat zij de opslag als geregistreerde klant kunnen gebruiken.
* **creeer een bedrijfrekening** Afhankelijk van de configuratie, kan een bezoeker aan uw opslag verkiezen om een bedrijfrekening tot stand te brengen. Voor meer informatie, zie [ Adobe Commerce B2B ](../b2b/introduction.md).
* **Snellere controle** - de geregistreerde klanten bewegen zich door controle sneller omdat veel van de informatie reeds in hun rekeningen is.
* **Zelfbediening** — Geregistreerde klanten kunnen hun informatie bijwerken, het statuut van orden controleren, en zelfs van hun rekeningen opnieuw rangschikken.

Klanten hebben toegang tot hun account door op de koppeling **[!UICONTROL My Account]** in de koptekst van de winkel te klikken. Vanaf hun account kunnen klanten informatie weergeven en wijzigen, zoals oude en huidige adressen, facturerings- en verzendvoorkeuren, abonnementen op nieuwsbrieven, wenslijst en meer.

![ Mijn Rekening ](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Bereik van klantenaccounts instellen

Het bereik van klantenaccounts kan worden beperkt tot de website waar het account is gemaakt of wordt gedeeld met alle websites en winkels in de winkelhiërarchie.

>[!NOTE]
>
>Als de website is uitgesloten van de klantengroep, mag de klant zich niet aanmelden bij de website wanneer het bereik van de klantenaccounts beperkt is tot de website of met alle websites wordt gedeeld. Zie [ een klantengroep ](customer-groups.md#create-a-customer-group) voor meer informatie over het uitsluiten van websites van groepen tot stand brengen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Account Sharing Options]** uit.

   ![ de Opties van het Delen van de Rekening ](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Share Customer Accounts]** in op een van de volgende opties:

   | Optie | Beschrijving |
   | --- | --- |
   | `Global` | Deelt de informatie van de klantenrekening met elke website en opslag in de installatie. |
   | `Per Website` | Hiermee beperkt u de gegevens van de klantenaccount tot de website waar het account is gemaakt. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Schakel indien nodig het selectievakje **[!UICONTROL User system value]** uit om de wijziging aan te brengen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

   >[!NOTE]
   >
   >Wanneer `Global` wordt geselecteerd wordt de klanteninformatie in **Mijn Rekening** (adressen en rekeningsinformatie zoals contactdetails) gedeeld.
