---
title: Lijst met klanten
description: In het raster Klanten worden alle klanten weergegeven die zich voor een account bij uw winkel hebben geregistreerd of die door de beheerder zijn toegevoegd.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Lijst met klanten

In de Admin [!UICONTROL Customers] In het raster worden alle klanten weergegeven die zich voor een account bij uw winkel hebben geregistreerd of die door de beheerder zijn toegevoegd. De standaard gebruiken [rasterbesturingselementen](../getting-started/admin-grid-controls.md) om de lijst te filteren en de kolomlay-out aan te passen. Zie voor meer informatie [Klantenaccounts beheren](../customers/manage-account.md).

![Lijst met klanten](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Klantgegevens bijwerken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klantrecord en klik op [!UICONTROL **Bewerken**] in de _[!UICONTROL Action]_kolom.

1. Kies in het linkerdeelvenster de informatie die u wilt bewerken en breng de benodigde wijzigingen aan.

   >[!NOTE]
   >
   >Zie voor meer informatie [Klantenaccounts bijwerken](../customers/update-account.md).

1. Klik op **[!UICONTROL Save Customer]**.

## Besturingselementen werkruimte

| Besturing | Beschrijving |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Maakt een klantenaccount. |
| **[!UICONTROL Search]** | Hiermee wordt een zoekopdracht naar klanten gestart op basis van de huidige filters. |
| **[!UICONTROL Filters]** | Definieert een set zoekparameters die wordt gebruikt om de records te filteren die in het dialoogvenster [raster](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Default View]** | Hiermee bepaalt u de standaardkolom [layout](../getting-started/admin-grid-controls.md) van het raster. |
| **[!UICONTROL Columns]** | Hiermee bepaalt u de selectie van [kolommen](../getting-started/admin-grid-controls.md) en hun rekeningen op het net. De kolomlay-out kan worden gewijzigd en opgeslagen als een _weergave_. Standaard worden slechts enkele kolommen in het raster opgenomen. |
| **[!UICONTROL Export]** | Hiermee exporteert u de geselecteerde records als een CSV- of Excel XML-bestand. |

{style="table-layout:auto"}

## Kolommen

| Kolom | Beschrijving |
| --- | --- |
| **[!UICONTROL Select]** | Beheert de checkbox selections for the customer records for applying an action. U kunt ook het selectiekader in de kolomkop gebruiken om alles in of uit te schakelen. |
| **[!UICONTROL ID]** | Een unieke numerieke id die wordt toegewezen wanneer de klantenaccount wordt gemaakt. |
| **[!UICONTROL Name]** | De voornaam en achternaam van de klant. |
| **[!UICONTROL Email]** | Het e-mailadres van de klant |
| **[!UICONTROL Group]** | De klantengroep waaraan de klant wordt toegewezen. |
| **[!UICONTROL Phone]** | Het telefoonnummer van de klant. |
| **[!UICONTROL ZIP]** | De postcode of postcode van de klant. |
| **[!UICONTROL Country]** | Het land waar de klant zich bevindt. |
| **[!UICONTROL State/Province]** | De staat of provincie waar de klant zich bevindt. |
| **[!UICONTROL Customer Since]** | De datum en tijd waarop de klantenaccount is gemaakt. |
| **[!UICONTROL Web Site]** | De website in de opslaghiërarchie waaraan het klantenaccount is gekoppeld. |
| **[!UICONTROL Confirmed Email]** | Hiermee geeft u aan of een bevestigingsbericht vereist is. |
| **[!UICONTROL Account Created In]** | Geeft de winkelweergave aan waaruit de klantenaccount is gemaakt. |
| **[!UICONTROL Date of Birth]** | De geboortedatum van de klant. <br><br>**_Belangrijk:_**In overeenstemming met de huidige beste praktijken op het gebied van beveiliging en privacy, dient u zich bewust te zijn van mogelijke juridische en veiligheidsrisico&#39;s die verbonden zijn aan de opslag van de volledige geboortedatum van de klant (maand, dag, jaar) met andere persoonlijke identificatoren. U wordt aangeraden de opslag van de volledige geboortedatum van de klant te beperken en u aan te raden het geboortejaar van de klant als alternatief te gebruiken. |
| **[!UICONTROL Tax / VAT Number]** | Indien van toepassing, het belastingnummer of [belasting over toegevoegde waarde](../stores-purchase/vat.md) nummer dat aan de klant is toegewezen. <br/><br/>Dit veld is niet hetzelfde als het BTW-nummer. |
| **[!UICONTROL Gender]** | Het geslacht van de klant. |
| **[!UICONTROL Action]** | Bewerken - Opent het bedrijfsaccount in de bewerkingsmodus. |

{style="table-layout:auto"}

### Aanvullende kolommen

Deze kolommen zijn beschikbaar door de [kolomindeling](../getting-started/admin-grid-controls.md) van het raster.

| Kolom | Beschrijving |
| --- | --- |
| **[!UICONTROL Company]** | De bedrijfsnaam van de klant. |
| **[!UICONTROL Street Address]** | Het adres van de klant. |
| **[!UICONTROL City]** | De plaats waar de klant zich bevindt. |
| **[!UICONTROL Fax]** | Het faxnummer van de klant, indien van toepassing. |
| **[!UICONTROL Billing Firstname]** | De voornaam in het factureringsadres van de klant. |
| **[!UICONTROL Billing Lastname]** | De achternaam in het factureringsadres van de klant. |
| **[!UICONTROL Billing Address]** | Het adres waar factureringsinformatie moet worden verzonden. |
| **[!UICONTROL Shipping Address]** | Het adres waar bestellingen moeten worden verzonden. |
| **[!UICONTROL VAT Number]** | Het BTW-nummer dat aan het adres van de klant is gekoppeld. Voor [digitale goederen](../stores-purchase/taxes.md) in de EU wordt verkocht, is de btw gebaseerd op het factuuradres van de afnemer. <br/><br/>Dit veld is niet hetzelfde als het BTW-nummer. |
| **[!UICONTROL Account Lock]** | Geeft de status van de account aan. Als beveiligingsmaatregel kunnen klantenaccounts [vergrendeld](../customers/password-options.md) na te veel aanmeldpogingen. Waarden: `Locked` / `Unlocked` |

{style="table-layout:auto"}
