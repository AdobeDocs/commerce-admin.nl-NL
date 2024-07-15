---
title: Verkooprapporten
description: De  [!DNL Commerce]  verkooprapporten helpen u om orden, belastingen, facturen, verzending, terugbetalingen, coupons, en PayPal regeling te volgen.
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

![ het rapportfilters van de Verkoop ](./assets/tax-report.png){width="600"}

Als u een verkooprapport wilt filteren, stelt u de volgende opties in:

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Date Used] | Hiermee stelt u de gegevens in die voor het rapport moeten worden gebruikt. |
| [!UICONTROL Period] | De periode waarvoor de gegevens worden gebruikt: Dag/Maand/Jaar. |
| [!UICONTROL From/To] | Hiermee definieert u de zoekgegevens op begin- en einddatum. |
| [!UICONTROL Order Status] | Hiermee wordt de status van de volgorde aangegeven |
| [!UICONTROL Empty Rows] | Geeft aan of lege rijen moeten worden toegevoegd aan het rapport. |

## [!UICONTROL Orders Report]

[!UICONTROL Orders Report] bevat het aantal geplaatste en geannuleerde orders, met totalen voor verkopen, gefactureerde bedragen, terugbetaalde bedragen, geïnde belasting, in rekening gebrachte verzendkosten en kortingen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Orders]**.

1. Selecteer in de sectie **[!UICONTROL Filter]** de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![ de verslagen van het Rapport van Orden ](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

[!UICONTROL Tax Report] bevat de toegepaste belastingregel, het belastingtarief, het aantal bestellingen en het bedrag aan belasting.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Tax]**.

1. Selecteer in de sectie **[!UICONTROL Filter]** de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport te vullen.


1. Klik op **[!UICONTROL Show Report]**.

![ Belastingrapport ](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

[!UICONTROL Invoice Report] bevat het aantal orders en facturen tijdens de periode, met bedragen gefactureerd, betaald en onbetaald.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Invoiced]**.

1. Selecteer in de sectie **[!UICONTROL Filter]** de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![ Factuurrapport ](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

[!UICONTROL Shipping Report] bevat het aantal bestellingen voor de gebruikte vervoerder of verzendmethode, inclusief de bedragen voor de totale verkoop en de totale verzending.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Shipping]**.

1. Selecteer in de sectie **[!UICONTROL Filter]** de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![ Verzendrapport ](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

[!UICONTROL Refunds Report] bevat het aantal terugbetaalde bestellingen en het totale bedrag dat online en offline is terugbetaald.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Refunds]**.

1. Selecteer in de sectie **[!UICONTROL Filter]** de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport te vullen.

1. Klik op **[!UICONTROL Show Report]**.

![ Rapport van Terugbetalingen ](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

De [!UICONTROL Coupons Report] bevat elke couponcode die tijdens het opgegeven tijdsinterval wordt gebruikt, de gerelateerde prijsregel en het aantal gebruikte tijdstippen, met totalen en subtotalen voor verkopen en kortingen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Selecteer in de sectie **[!UICONTROL Filter]** de opties voor de rapportageperiode en de orderstatus die worden gebruikt om het rapport te vullen.

1. Klik op **[!UICONTROL Show Report]**.

Voor meer informatie over het gebruiken van [!UICONTROL Coupons Report] om gegevens voor uw promotiecampagnes te verzamelen, zie [ Waarden die ](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) in de _Gids van de Verkoop en van Bevorderingen_ melden.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

De [ pagina van de Rapporten van de Afrekening van PayPal ] omvat het type van gebeurtenis, zoals een debitcardtransactie, de begin en einddata, brutobedrag, en verwante kosten. Het rapport kan automatisch worden bijgewerkt met de meest recente gegevens van PayPal. Er zijn filteropties voor datumbereik, zakelijke account, transactie-id, factuur-id of PayPal-referentie-id.

Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

![ PayPal Rapport van de Afwikkeling ](./assets/reports-sales-paypal-settlement.png){width="600"}

Voor meer informatie over het gebruiken van [!UICONTROL PayPal Settlement Reports] om informatie over elke transactie terug te winnen PayPal die de regeling van middelen beïnvloedt, zie [ de rapporten van de Afrekening van PayPal ](../stores-purchase/paypal-settlement-reports.md) in de _Gids van de Opslag en van de Ervaring van de Aankoop_.

## [!UICONTROL Braintree Settlement Report]

Het ](../stores-purchase/braintree.md) Rapport van de Afwikkeling van de Braintree [ kan volgens aanmaakdatum, bedrag, status, transactietype, betalingstype, transactie identiteitskaart, orde ID, PayPal betalings identiteitskaart, type, handels rekening ID, of identiteitskaart van de afwikkelingspartij worden gefiltreerd. Het rapport bevat de transactie-id, de bestellings-id, de PayPal-betalings-id, het type, de aanmaakdatum, het bedrag, de afwikkelingscode, de status, de tekst van de afwikkelingsreactie, de terugbetaling-ID&#39;s, de handelaarrekening-id, de partij-ID van de afwikkeling en de valuta.

Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## Rapporten exporteren

1. Selecteer het bestandstype: `Excel XML` of `CSV` om het rapport te exporteren

1. Klik op **[!UICONTROL Export]**.

## Statistieken vernieuwen

Om het prestatieseffect van het produceren van verkooprapporten te verminderen, berekent [!DNL Commerce] en slaat de vereiste statistieken voor elk rapport op. In plaats van de statistieken opnieuw te berekenen telkens als een rapport wordt geproduceerd, worden de opgeslagen statistieken gebruikt, tenzij u de statistieken vernieuwt. Om de meest recente gegevens op te nemen, moeten de rapportstatistieken worden vernieuwd alvorens een verkooprapport wordt geproduceerd.

![ verfrist Statistieken ](./assets/refresh-stats.png){width="700"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Statistics]_>**[!UICONTROL Refresh Statistics]**.

1. Selecteer in de lijst het selectievakje voor elk rapport dat moet worden vernieuwd.

1. Stel het besturingselement **[!UICONTROL Actions]** in op een van de volgende opties:

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. Klik op **[!UICONTROL Submit]**.
