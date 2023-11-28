---
title: Verkooprapporten
description: De [!DNL Commerce] Met verkooprapporten kunt u bestellingen, belastingen, facturen, verzendingen, terugbetalingen, coupons en PayPal-betalingen bijhouden.
exl-id: 928a407f-cbed-4114-ad0b-ee227383bf36
feature: Reporting, Orders
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 1%

---

# Verkooprapporten

De selectie van verkooprapporten omvat Bestellingen, Belasting, Facturering, Verzending, Terugbetalingen, Coupons, en Afwikkeling PayPal.

## Rapportfilters

U kunt een verkooprapport genereren voor een hele website of voor één winkel. De verkooprapporten kunnen door tijdsinterval, datum, en status worden gefiltreerd.

![Verkooprapportfilters](./assets/tax-report.png){width="600"}

Als u een verkooprapport wilt filteren, stelt u de volgende opties in:

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Date Used] | Hiermee stelt u de gegevens in die voor het rapport moeten worden gebruikt. |
| [!UICONTROL Period] | De periode waarvoor de gegevens worden gebruikt: Dag/Maand/Jaar. |
| [!UICONTROL From/To] | Hiermee definieert u de zoekgegevens op begin- en einddatum. |
| [!UICONTROL Order Status] | Hiermee wordt de status van de volgorde aangegeven |
| [!UICONTROL Empty Rows] | Geeft aan of lege rijen moeten worden toegevoegd aan het rapport. |

## [!UICONTROL Orders Report]

De [!UICONTROL Orders Report] bevat het aantal geplaatste en geannuleerde orders, met de totalen voor verkopen, gefactureerde bedragen, terugbetaalde bedragen, geïnde belasting, in rekening gebrachte verzendkosten en kortingen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Orders]**.

1. In de **[!UICONTROL Filter]** selecteert u de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport in te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![Orderrapport-records](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

De [!UICONTROL Tax Report] omvat de toegepaste belastingregel, het belastingtarief, het aantal bestellingen en het bedrag van de geheven belasting.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Tax]**.

1. In de **[!UICONTROL Filter]** selecteert u de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport in te vullen.


1. Klik op **[!UICONTROL Show Report]**.

![Belastingrapport](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

De [!UICONTROL Invoice Report] bevat het aantal orders en facturen gedurende de periode, met bedragen die gefactureerd, betaald en onbetaald zijn.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Invoiced]**.

1. In de **[!UICONTROL Filter]** selecteert u de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport in te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![Factuurrapport](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

De [!UICONTROL Shipping Report] bevat het aantal bestellingen voor de gebruikte vervoerder of verzendmethode, inclusief de bedragen voor de totale verkoop en de totale verzending.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Shipping]**.

1. In de **[!UICONTROL Filter]** selecteert u de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport in te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![Verzendrapport](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

De [!UICONTROL Refunds Report] bevat het aantal terugbetaalde bestellingen en het totale bedrag dat online en offline is terugbetaald.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Refunds]**.

1. In de **[!UICONTROL Filter]** selecteert u de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport in te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![Restitutierapport](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

De [!UICONTROL Coupons Report] omvat elke couponcode die tijdens het opgegeven tijdsinterval wordt gebruikt, de desbetreffende prijsregel en het aantal gebruikte tijdstippen, met totalen en subtotalen voor verkopen en kortingen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. In de **[!UICONTROL Filter]** selecteert u de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport in te vullen.

1. Klik op **[!UICONTROL Show Report]**.

Voor meer informatie over het gebruik van de [!UICONTROL Coupons Report] om gegevens voor je promotiecampagnes te verzamelen, zie [Coupons rapporteren](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) in de _Handleiding Handelsbemiddeling en speciale acties_.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

De [PayPal-afwikkelingsrapporten] De pagina bevat het type gebeurtenis, zoals een debitcardtransactie, de begin- en einddatum, het brutobedrag en de bijbehorende kosten. Het rapport kan automatisch worden bijgewerkt met de meest recente gegevens van PayPal. Er zijn filteropties voor datumbereik, zakelijke account, transactie-id, factuur-id of PayPal-referentie-id.

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

![PayPal-afwikkelingsrapport](./assets/reports-sales-paypal-settlement.png){width="600"}

Voor meer informatie over het gebruik van de [!UICONTROL PayPal Settlement Reports] voor informatie over elke PayPal-transactie die de afwikkeling van fondsen beïnvloedt, raadpleegt u [PayPal-afwikkelingsrapporten](../stores-purchase/paypal-settlement-reports.md) in de _Handleiding voor winkels en aanschaf_.

## [!UICONTROL Braintree Settlement Report]

De [Braintree](../stores-purchase/braintree.md) Afwikkelingsrapport kan worden gefilterd op aanmaakdatum, bedrag, status, type transactie, betalingstype, transactie-id, bestellings-id, PayPal-betalings-id, type, handels-account-id of transactie-batch-id. Het rapport bevat de transactie-id, de bestellings-id, de PayPal-betalings-id, het type, de aanmaakdatum, het bedrag, de afwikkelingscode, de status, de tekst van de afwikkelingsreactie, de terugbetaling-ID&#39;s, de handelaarrekening-id, de partij-ID van de afwikkeling en de valuta.

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## Rapporten exporteren

1. Als u het rapport wilt exporteren, selecteert u het bestandstype: `Excel XML` of `CSV`

1. Klik op **[!UICONTROL Export]**.

## Statistieken vernieuwen

Om het prestatieseffect van het produceren van verkooprapporten te verminderen, [!DNL Commerce] berekent en slaat de vereiste statistieken voor elk rapport op. In plaats van de statistieken opnieuw te berekenen telkens als een rapport wordt geproduceerd, worden de opgeslagen statistieken gebruikt, tenzij u de statistieken vernieuwt. Om de meest recente gegevens op te nemen, moeten de rapportstatistieken worden vernieuwd alvorens een verkooprapport wordt geproduceerd.

![Statistieken vernieuwen](./assets/refresh-stats.png){width="700"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Statistics]_>**[!UICONTROL Refresh Statistics]**.

1. Selecteer in de lijst het selectievakje voor elk rapport dat moet worden vernieuwd.

1. Stel de **[!UICONTROL Actions]** de controle op een van de volgende punten:

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. Klik op **[!UICONTROL Submit]**.
