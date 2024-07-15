---
title: Bedrijfskrediet beheren
description: Meer informatie over bedrijfskredietlijnen, parameters instellen en vooruitbetalingen verwerken.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Bedrijfskrediet beheren

Als [ Betaling op Rekening ](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) in de configuratie wordt toegelaten, kunnen de bedrijven aankopen op hun rekening tot de kredietgrens maken die aan het bedrijf wordt verleend. Wanneer deze optie is ingeschakeld, kunnen klanten de status van hun bedrijfskrediet controleren via het dashboard voor hun account.

![ Krediet van het Bedrijf ](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

U kunt de volgende kredietgerelateerde parameters instellen voor elk bedrijfsprofiel:

- Kredietvaluta
- Kredietlimiet
- Kredietlimiet overschrijden toestaan
- Reden voor wijziging

Als het bedrijf een openstaand saldo heeft, verschijnt een bericht aan de opslagbeheerder bij de bovenkant van de verkooporde wanneer het van Admin wordt bekeken. Meer leren, zie [ een bedrijfrekening ](account-company-create.md) creëren.

## Bedrijfskredietactiviteiten

In het gedeelte [!UICONTROL Company Credit] van het bedrijfsprofiel wordt een overzicht weergegeven van de activiteiten op het gebied van klantenkrediet, met een raster van de kredietgeschiedenis van het bedrijf.

![ activiteit van het Krediet van het Bedrijf ](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Date] | De datum van de transactie. Houd de muisaanwijzer boven de datum en tijd om de datum en tijd weer te geven. |
| [!UICONTROL Operation] | Het type activiteit dat aan de transactie is gekoppeld. Waarden: <br/>**[!UICONTROL Allocated]**- Aan het bedrijf toegewezen krediet.<br/>**[!UICONTROL Updated]** - Er is een wijziging toegepast op een van de volgende velden: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Er is een volgorde geplaatst.<br/>**[!UICONTROL Reimbursed]** - Het uitstaande saldo is vergoed. <br/>**[!UICONTROL Refunded]**- Er is een bedrag op creditnota terugbetaald.<br/>**[!UICONTROL Reverted]** - De bestelling is geannuleerd en het bedrag is geretourneerd naar het creditsaldo. |
| [!UICONTROL Amount] | Het bedrag van de transactie dat aan de volgende transactietypen is gekoppeld: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/> Voor aankoopbedragen wordt het bedrag weergegeven in de weergavevaluta van de winkel en in de notatie van de creditvalutaset, gevolgd door de huidige omrekeningskoers (indien van toepassing). Bijvoorbeeld: <br/> EUR 20.000.00 ($22.400.00) <br/> USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | Het terugbetaalde bedrag, verminderd met het totale verschuldigde bedrag van alle orders die zijn geplaatst met de betalingsmethode op rekening. De waarde kan positief of negatief zijn. <br/>**[!UICONTROL Positive value]**- Een vooruitbetaling wordt weergegeven als een positieve waarde.<br/>**[!UICONTROL Negative value]** - Een verschuldigd bedrag wordt weergegeven als een negatieve waarde. |
| [!UICONTROL Available Credit] | De som van de _[!UICONTROL Credit Limit]_en de_[!UICONTROL Outstanding Balance]_ . Als de onderneming de kredietlimiet heeft overschreden, wordt het bedrag weergegeven als een negatieve waarde. |
| [!UICONTROL Credit Limit] | Het bedrag van het aan de onderneming verstrekte krediet. |
| [!UICONTROL Updated By] | De naam van de persoon die de bewerking heeft gestart. |
| [!UICONTROL Custom Reference Number] | Het aangepaste referentienummer dat aan de transactie is gekoppeld. |
| [!UICONTROL Comment] | Een compilatie van de waarden van het `Reason for Change` gebied, volgens verrichtingstype. <br/>**[!UICONTROL Purchased]**- Bevat opmerkingen van de aankoop en het ordernummer en de koppeling naar de bestelling.<br/>**[!UICONTROL Reimbursed]** - Bevat opmerkingen van de vergoede transactie. |
| [!UICONTROL Action] | Alleen voor `Reimbursed` -bewerkingen. **[!UICONTROL Edit]** - Hiermee kan het restitutiebedrag worden bijgewerkt. |

{style="table-layout:auto"}

## De kredietgegevens bijwerken

Wanneer de klant de betaling voor het uitstaande krediet aan de handelaar verricht, moet een opslagbeheerder de informatie van het klantenkrediet in Admin dan bijwerken.

1. Op _Admin_ sidebar, ga naar **Klanten > Bedrijven**.

1. Vind het bedrijf in het net en open op _geef_ wijze uit.

1. Breid de **sectie van het Krediet van het Bedrijf** uit.

1. Voor **Kredietgrens**, ga de nieuwe waarde in.

1. Wijzig desgewenst de andere waarden.

1. Klik op **[!UICONTROL Save]** als de updates zijn voltooid.

## Betalingen ontvangen

Een vergoed saldo is een offline betaling die door een bedrijf wordt gedaan naar het saldo van hun rekening. De opslagbeheerder gaat het bedrag manueel in het bedrijfprofiel in, gebruikend de _knoop van het Saldo van de Terugbetaling_. Wanneer het bedrag wordt ingediend, herberekent het systeem het uitstaande saldo en het beschikbare bedrijfskrediet en registreert het de actie in de geschiedenis van het bedrijfskrediet. Het terugbetaalde bedrag wordt geboekt in de creditvaluta, zoals aangegeven in de configuratie.

### Betaling toepassen op een bedrijfsaccount

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek de bedrijfsrecord in de lijst en open in de modus **[!UICONTROL Edit]** .

1. Bij de bovenkant van de pagina, klik **vergoeden Saldo**.

1. Voeg in het dialoogvenster de betalingsgegevens toe:

   ![ Saldo van de Terugbetaling ](./assets/company-reimburse-balance.png){width="500"}

   - Ga het **Bedrag** van de betaling in.

     Het bedrag kan als positieve of negatieve waarde worden vermeld.

   - Indien van toepassing, ga het **Aantal van de Verwijzing van de Douane** voor verwijzing in.

     Per vergoeding kan slechts één aangepast referentienummer worden ingevoerd. Als u de betaling op meerdere inkooporder&#39;s wilt toepassen, maakt u voor elke PO een aparte vergoeding.

   - Zoals nodig, ga a **Commentaar** in om de terugbetaling te beschrijven.

1. Klik **Terugbetaling**.

   Het uitstaande saldo van de onderneming en het beschikbare krediet worden opnieuw berekend en de geschiedenis van het bedrijfskrediet wordt aangepast aan de terugbetaling.

### Een vergoeding bewerken

1. Open het bedrijfsprofiel in de modus **[!UICONTROL Edit]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **sectie van het Krediet van het Bedrijf**.

1. Zoek de terugbetalingstransactie in het raster en klik op **[!UICONTROL Edit]** .

1. Breng om het even welke veranderingen noodzakelijk aan **Aantal van de Verwijzing van de Douane** en **Commentaar** aan.

   Het terugbetalingsbedrag kan niet worden gewijzigd.

1. Klik op **[!UICONTROL Save]**.

## Winefront-kredietgegevens

Voor de bedrijfbeheerder, toont het rekendashboard de _sectie van het Krediet van het Bedrijf_. Het verstrekt het huidige uitstaande saldo, beschikbare krediet, en het kredietgrens dat aan hun bedrijfsrekening wordt toegewezen, gevolgd door een lijst van uitstaande facturen.

Als de handelaar een orde annuleert die aan bedrijfskrediet in rekening werd gebracht, is het bedrag van de orde teruggekeerd aan het bedrijfssaldo en de _Geschiedenis van de Toewijzing van de Krediet_ omvat een verslag van de actie.

![ Krediet van het Bedrijf ](./assets/company-credit.png){width="700" zoomable="yes"}

## Bedrijfskredietdemo

Bekijk deze demo-video voor meer informatie over het beheren van bedrijfskrediet:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
