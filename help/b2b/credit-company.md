---
title: Bedrijfskrediet beheren
description: Meer informatie over bedrijfskredietlijnen, parameters instellen en vooruitbetalingen verwerken.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Bedrijfskrediet beheren

Indien [Betaling op rekening](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) in de configuratie is ingeschakeld, kunnen bedrijven aankopen op hun rekening doen tot het aan het bedrijf toegekende kredietplafond. Wanneer deze optie is ingeschakeld, kunnen klanten de status van hun bedrijfskrediet controleren via het dashboard voor hun account.

![Bedrijfskrediet](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

U kunt de volgende kredietgerelateerde parameters instellen voor elk bedrijfsprofiel:

- Kredietvaluta
- Kredietlimiet
- Kredietlimiet overschrijden toestaan
- Reden voor wijziging

Als het bedrijf een openstaand saldo heeft, verschijnt een bericht aan de opslagbeheerder bij de bovenkant van de verkooporde wanneer het van Admin wordt bekeken. Zie voor meer informatie [Een bedrijfsaccount maken](account-company-create.md).

## Bedrijfskredietactiviteiten

De [!UICONTROL Company Credit] het gedeelte van het bedrijfsprofiel bevat een overzicht van de activiteiten op het gebied van klantenkrediet , met een overzicht van de kredietgeschiedenis van het bedrijf .

![Bedrijfskredietactiviteiten](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Date] | De datum van de transactie. Houd de muisaanwijzer boven de datum en tijd om de datum en tijd weer te geven. |
| [!UICONTROL Operation] | Het type activiteit dat aan de transactie is gekoppeld. Waarden: <br/>**[!UICONTROL Allocated]**- Aan de onderneming toegekende kredieten.<br/>**[!UICONTROL Updated]** - Een wijziging is toegepast op een van de volgende velden: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Er is een bestelling geplaatst.<br/>**[!UICONTROL Reimbursed]** - Het uitstaande saldo is terugbetaald. <br/>**[!UICONTROL Refunded]**- Er is een bedrag op creditnota terugbetaald.<br/>**[!UICONTROL Reverted]** - De bestelling werd geannuleerd en het bedrag werd teruggeboekt naar het creditsaldo. |
| [!UICONTROL Amount] | Het bedrag van de transactie die aan de volgende transactietypen wordt geassocieerd: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Voor aankoopbedragen wordt het bedrag weergegeven in de weergavevaluta van de opslagplaats en in de notatie van de kredietvaluta-instelling, gevolgd door de huidige omrekeningskoers (indien van toepassing). Bijvoorbeeld: <br/>EUR 20.000,00 ($ 22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Het terugbetaalde bedrag, verminderd met het totale verschuldigde bedrag van alle orders die zijn geplaatst met de betalingsmethode op rekening. De waarde kan positief of negatief zijn. <br/>**[!UICONTROL Positive value]**- Een voorschot wordt als een positieve waarde weergegeven.<br/>**[!UICONTROL Negative value]** - Een verschuldigd bedrag wordt weergegeven als een negatieve waarde. |
| [!UICONTROL Available Credit] | De som van de _[!UICONTROL Credit Limit]_en de_[!UICONTROL Outstanding Balance]_. Als de onderneming de kredietlimiet heeft overschreden, wordt het bedrag weergegeven als een negatieve waarde. |
| [!UICONTROL Credit Limit] | Het bedrag van het aan de onderneming verstrekte krediet. |
| [!UICONTROL Updated By] | De naam van de persoon die de bewerking heeft gestart. |
| [!UICONTROL Custom Reference Number] | Het aangepaste referentienummer dat aan de transactie is gekoppeld. |
| [!UICONTROL Comment] | Een compilatie van de waarden uit de `Reason for Change` veld, afhankelijk van het type bewerking. <br/>**[!UICONTROL Purchased]**- Bevat opmerkingen van de aankoop en het ordernummer en de koppeling naar de bestelling.<br/>**[!UICONTROL Reimbursed]** - Bevat opmerkingen van de terugbetaalde transactie. |
| [!UICONTROL Action] | Voor `Reimbursed` alleen bewerkingen. **[!UICONTROL Edit]** - Het terugbetalingsbedrag kan worden bijgewerkt. |

{style="table-layout:auto"}

## De kredietgegevens bijwerken

Wanneer de klant de betaling voor het uitstaande krediet aan de handelaar verricht, moet een opslagbeheerder de informatie van het klantenkrediet in Admin dan bijwerken.

1. Op de _Beheerder_ zijbalk, ga naar **Klanten > Bedrijven**.

1. Zoek het bedrijf in het raster en open het in _Bewerken_ -modus.

1. Breid uit **Bedrijfskrediet** sectie.

1. Voor **Kredietlimiet** Voer de nieuwe waarde in.

1. Wijzig desgewenst de andere waarden.

1. Wanneer de updates zijn voltooid, klikt u op **[!UICONTROL Save]**.

## Betalingen ontvangen

Een vergoed saldo is een offline betaling die door een bedrijf wordt gedaan naar het saldo van hun rekening. De opslagbeheerder gaat het bedrag in het bedrijfsprofiel manueel in, gebruikend _Terugbetalingssaldo_ knop. Wanneer het bedrag wordt ingediend, herberekent het systeem het uitstaande saldo en het beschikbare bedrijfskrediet en registreert het de actie in de geschiedenis van het bedrijfskrediet. Het terugbetaalde bedrag wordt geboekt in de creditvaluta, zoals aangegeven in de configuratie.

### Betaling toepassen op een bedrijfsaccount

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek de bedrijfsrecord in de lijst en open in **[!UICONTROL Edit]** -modus.

1. Klik boven aan de pagina op **Terugbetalingssaldo**.

1. Voeg in het dialoogvenster de betalingsgegevens toe:

   ![Terugbetalingssaldo](./assets/company-reimburse-balance.png){width="500"}

   - Voer de **Hoeveelheid** van de betaling.

     Het bedrag kan als positieve of negatieve waarde worden vermeld.

   - Voer, indien van toepassing, de **Aangepast referentienummer** ter referentie.

     Per vergoeding kan slechts één aangepast referentienummer worden ingevoerd. Als u de betaling op meerdere inkooporder&#39;s wilt toepassen, maakt u voor elke PO een aparte vergoeding.

   - Voer zo nodig een **Opmerking** om de terugbetaling te beschrijven.

1. Klikken **Terugbetaling**.

   Het uitstaande saldo van de onderneming en het beschikbare krediet worden opnieuw berekend en de geschiedenis van het bedrijfskrediet wordt aangepast aan de terugbetaling.

### Een vergoeding bewerken

1. Open het bedrijfsprofiel in **[!UICONTROL Edit]** -modus.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **Bedrijfskrediet** sectie.

1. Zoek de terugbetalingstransactie in het raster en klik op **[!UICONTROL Edit]**.

1. Breng de benodigde wijzigingen aan om **Aangepast referentienummer** en **Opmerking**.

   Het terugbetalingsbedrag kan niet worden gewijzigd.

1. Klik op **[!UICONTROL Save]**.

## Winefront-kredietgegevens

Voor de bedrijfsbeheerder, toont het rekeningsdashboard _Bedrijfskrediet_ sectie. Het verstrekt het huidige uitstaande saldo, beschikbare krediet, en het kredietgrens dat aan hun bedrijfsrekening wordt toegewezen, gevolgd door een lijst van uitstaande facturen.

Als de handelaar een bestelling annuleert die op bedrijfskrediet in rekening werd gebracht, wordt het bedrag van de bestelling teruggeboekt naar het bedrijfssaldo en de _Crediteringsgeschiedenis_ bevat een record van de handeling.

![Bedrijfskrediet](./assets/company-credit.png){width="700" zoomable="yes"}

## Bedrijfskredietdemo

Bekijk deze demo-video voor meer informatie over het beheren van bedrijfskrediet:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
