---
title: Klantenaccounts beheren
description: Gebruik de [!UICONTROL Customers] netwerk om om het even welke klantenrekening en toegangsinformatie voor individuele klantenrekeningen te vinden.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Klantenaccounts beheren

Gebruik de _[!UICONTROL Customers]_raster om een klantenaccount te zoeken. U kunt de standaard [besturingselementen voor werkplek](../getting-started/admin-workspace.md) om de lijst te filteren, wijzigt u de [kolomindeling](../getting-started/admin-grid-controls.md), slaat weergaven op en exporteert gegevens. De [Handelingencontrole](../getting-started/admin-actions-control.md) boven het net kan worden gebruikt om een verrichting op veelvoudige klantenverslagen toe te passen.

![Alle klanten](assets/customers-all-customers.png){width="700" zoomable="yes"}

Zie [Klantprofiel bijwerken](update-account.md) voor informatie over het uitvoeren van handmatige updates voor een klantenaccount.

## Acties voor klantenaccounts

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Selecteer in de eerste kolom van het raster het selectievakje van elke record die u wilt bijwerken.

1. Volg de instructies voor de actie die u wilt toepassen.

   >[!INFO]
   >
   >De volgende handelingen kunnen op één of meerdere records worden toegepast.

1. Klik op **[!UICONTROL Save Config]**.

### Abonneren op nieuwsbrief

In meerdere winkels en meerdere sites met een wereldwijd [bereik van klantenaccount](../customers/customer-account-scope.md), kan een klantenrekening aan nieuwsbrieven veelvoudige plaatsen of opslag worden geabonneerd. Als u het _Abonneren_ activeert de toepassing voor een klantaccount het abonnement op de nieuwsbrief voor alleen de standaardweergave van de site of winkel.

* Stel de **[!UICONTROL Actions]** controle op `Subscribe to newsletter`.

Zie [Abonnees beheren](../merchandising-promotions/newsletter-subscribers.md) voor meer informatie over het beheren van nieuwsbrieven abonnementen voor een klant.

### Abonnement op nieuwsbrief opzeggen

In meerdere winkels en meerdere sites met een wereldwijd [bereik van klantenaccount](customer-account-scope.md), kan een klantenaccount worden geabonneerd op nieuwsbrieven voor meerdere sites/winkels. Als u het _Abonnement opzeggen_ actie aan een klantenrekening, worden alle actieve abonnementen geabonneerd.

1. Stel de **[!UICONTROL Actions]** controle op `Unsubscribe to newsletter`.

1. Klik wanneer u wordt gevraagd om te bevestigen **OK**.

### Een klantengroep toewijzen

1. Stel de **[!UICONTROL Actions]** controle op `Assign a customer group`.

1. Kies de klantengroep waaraan alle geselecteerde klantenverslagen moeten worden toegewezen.

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.

### Klantenaccounts verwijderen

Verwijderde klantaccounts kunnen niet worden hersteld. Informatie over klantactiviteiten en transacties wordt in het systeem bewaard.

1. Stel de **[!UICONTROL Actions]** controle op `Delete`.

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.

## Klantenaccounts exporteren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klik in het menu Tabelkop **[!UICONTROL Export]** en selecteer de gewenste indeling:

   * CSV
   * Excel XML

1. Klik op **[!UICONTROL OK]**.

   Het bestand gaat naar de standaardmap voor downloads.

De bovenstaande instructie exporteert alle klantenaccounts. Als u een beperkte set wilt exporteren, schakelt u de selectievakjes in voor de accounts die u wilt exporteren of gebruikt u filters in het configuratiescherm om een bereik met klantenaccounts te selecteren.

## Handelingen/besturingselementen

| Optie | Beschrijving |
|--- |--- |
| **[!UICONTROL Delete]** | Hiermee verwijdert u geselecteerde klantaccounts. Als de klantenrekening tot een bedrijfbeheerder voor een opslag B2B behoort, moet een andere bedrijfgebruiker als beheerder worden toegewezen alvorens de klantenrekening kan worden geschrapt. |
| **[!UICONTROL Subscribe to Newsletter]** | Abonneer geselecteerde klanten op nieuwsbrief. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Hiermee worden geselecteerde klanten afgemeld voor nieuwsbrief. |
| **[!UICONTROL Assign a Customer Group]** | Wijst geselecteerde klanten aan een klantengroep toe. |
| **[!UICONTROL Edit]** | Hiermee kunnen sommige waarden van één geselecteerde klantrecord worden bewerkt in het raster. Standaard zijn de volgende waarden beschikbaar voor een snelle bewerking: E-mail, Groep, Telefoon, ZIP, Website, BTW-nummer en Genderkwesties. |

{style="table-layout:auto"}

## Kolommen

| Kolom | Beschrijving |
|--- |--- |
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
| **[!UICONTROL Date of Birth]** | De geboortedatum van de klant. In overeenstemming met de huidige beste praktijken op het gebied van beveiliging en privacy, dient u zich bewust te zijn van mogelijke juridische en veiligheidsrisico&#39;s die verbonden zijn aan de opslag van de volledige geboortedatum van de klant (maand, dag, jaar) met andere persoonlijke identificatoren. U wordt aangeraden de opslag van de volledige geboortedatum van de klant te beperken en u aan te raden het geboortejaar van de klant als alternatief te gebruiken. |
| **[!UICONTROL Tax / VAT Number]** | Indien van toepassing, het belastingnummer of [belasting over toegevoegde waarde](../stores-purchase/vat.md) nummer dat aan de klant is toegewezen. <br/><br/> Dit veld is niet hetzelfde als het BTW-nummer. |
| **[!UICONTROL Gender]** | Het geslacht van de klant. |
| **[!UICONTROL Action]** | Bewerken - Opent het bedrijfsaccount in de bewerkingsmodus. |

{style="table-layout:auto"}

### Aanvullende kolommen

Deze kolommen zijn beschikbaar door de [kolomindeling](../getting-started/admin-grid-controls.md) van het raster.

| Kolom | Beschrijving |
|--- |--- |
| **[!UICONTROL Company]** | De bedrijfsnaam van de klant. |
| **[!UICONTROL Street Address]** | Het adres van de klant. |
| **[!UICONTROL City]** | De plaats waar de klant zich bevindt. |
| **[!UICONTROL Fax]** | Het faxnummer van de klant, indien van toepassing. |
| **[!UICONTROL Billing Firstname]** | De voornaam in het factureringsadres van de klant. |
| **[!UICONTROL Billing Lastname]** | De achternaam in het factureringsadres van de klant. |
| **[!UICONTROL Billing Address]** | Het adres waar factureringsinformatie moet worden verzonden. |
| **[!UICONTROL Shipping Address]** | Het adres waar bestellingen moeten worden verzonden. |
| **[!UICONTROL VAT Number]** | Het BTW-nummer dat aan het adres van de klant is gekoppeld. Voor [digitale goederen](../stores-purchase/taxes.md) in de EU wordt verkocht, is de btw gebaseerd op het factuuradres van de afnemer. <br/><br/> Dit veld is niet hetzelfde als het BTW-nummer. |
| **[!UICONTROL Account Lock]** | Geeft de status van de account aan. Als beveiligingsmaatregel kunnen klantenaccounts [vergrendeld](../customers/password-options.md) na te veel aanmeldpogingen. Waarden: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | De huidige gebruikersstatus. Opties: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Klantclassificatie. Opties: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | De verkoper die als contactpunt voor een bedrijfrekening wordt toegewezen en alle geautomatiseerde e-mailberichten ontvangt met betrekking tot het bedrijf. |

{style="table-layout:auto"}
