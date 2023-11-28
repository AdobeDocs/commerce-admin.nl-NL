---
title: Couponcodes
description: Leer hoe u couponcodes met de regels voor winkelprijzen kunt gebruiken om een korting toe te passen wanneer aan een aantal voorwaarden wordt voldaan.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---

# Couponcodes

Coupons-codes worden gebruikt met [regels betreffende de kartonprijs](price-rules-cart.md) om een korting toe te passen wanneer aan een reeks voorwaarden wordt voldaan. U kunt bijvoorbeeld een couponcode maken voor een specifieke klantengroep of voor iedereen die een aankoop voor een bepaald bedrag doet. Als u de coupon op een aankoop wilt toepassen, kan de klant de couponcode in het winkelwagentje of mogelijk in het kasregister van uw _baksteen en mortel_ opslaan. Hier volgen enkele manieren waarop je coupons kunt gebruiken in je winkel:

- E-mailcoupons naar klanten
- Afgedrukte coupons maken
- In-store coupons maken voor mobiele gebruikers

Couponcodes kunnen via e-mail worden verzonden of worden opgenomen in nieuwsbrieven, catalogi en advertenties. De lijst met couponcodes kan worden geëxporteerd en naar een commerciële drukker worden verzonden. U kunt ook in-store coupons maken met een snelle antwoordcode die kopers kunnen scannen met hun smartphones. De QR-code kan worden gekoppeld aan een pagina op uw site met meer informatie over de aanbieding.

## couponcodes configureren

De lengte en opmaak van automatisch gegenereerde couponcodes worden bepaald door de configuratie. De tekens kunnen op alle getallen, alle letters of een combinatie worden ingesteld. U kunt een streepje invoegen met ingestelde intervallen, zodat u het gemakkelijk kunt lezen, en een voor- en achtervoegsel toevoegen om de code aan een specifieke campagne of een bepaald initiatief te koppelen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Promotions]**.

   ![Configuratie van klanten - automatisch gegenereerde specifieke couponcodes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Vouw de sectie **[!UICONTROL Auto Generated Specific Coupon Codes]** uit.

   ![Configuratie van klanten - automatisch gegenereerde specifieke couponcodes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Voer de **[!UICONTROL Code Length]**, inclusief voor- en achtervoegsel en scheidingstekens.

1. Stel de **[!UICONTROL Code Format]** op een van de volgende wijzen:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Voor **[!UICONTROL Code Prefix]** Voer de waarde in die u aan het begin van alle couponcodes wilt weergeven.

1. Voor **[!UICONTROL Code Suffix]** Voer de waarde in die u aan het einde van alle couponcodes wilt weergeven.

1. Voor **[!UICONTROL Dash Every X Characters]**, voert u het aantal tekens tussen elk streepje in.

   Couponcodes met verschillende streepjespatronen worden als verschillende codes beschouwd, zelfs als de getallen gelijk zijn.

1. Klik op **[!UICONTROL Save Config]**.

## coupons maken

>[!NOTE]
>
>Voordat u coupons maakt, gebruikt u de `bin/magento cron:run` om te controleren of de uitsnede wordt uitgevoerd. Zie [Uitsnijden uitvoeren vanaf de opdrachtregel](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) in de _Configuratiegids_ voor meer informatie .

### Methode 1: Een specifieke coupon maken

1. Volg de instructies om een [kartonnen prijsregel](price-rules-cart.md).

1. In de **[!UICONTROL Rule Information]** sectie, set **[!UICONTROL Coupon]** tot `Specific Coupon`.

1. Voer een **[!UICONTROL Coupon Code]** worden gebruikt voor de promotie.

   De notatie van de code (numeriek, alfanumeriek of alfabetisch) wordt bepaald door de instelling [configuratie](#configure-coupon-codes).

1. Ga als volgt te werk om het aantal keren dat de coupon kan worden gebruikt te beperken:

   - Voer het aantal van **[!UICONTROL Uses per Coupon]**.
   - Voer het aantal van **[!UICONTROL Uses per Customer]**.

   Voor onbeperkt gebruik, verlaat deze gebieden leeg.

   ![Winkelprijsregel - couponinformatie](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Als meerdere klanten tegelijkertijd dezelfde coupon gebruiken, is het mogelijk dat de vastgestelde gebruikslimiet wordt overschreden als gevolg van vertraagde couponverwerking.

1. Ga als volgt te werk om de coupon geldig te maken voor een tijdsperiode:

   - ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Voltooi de **Van** en **Naar** datums. Klik op de knop **Kalender** (![Kalenderpictogram](../assets/icon-calendar.png)) naast elk veld. Als u het datumbereik leeg laat, verloopt de regel niet.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Voer een van de volgende handelingen uit:

     **Optie 1:** Een nieuwe update plannen

      - Klikken **[!UICONTROL Schedule New Update]** rechtsboven op de pagina.

        ![Update plannen](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Voer de **[!UICONTROL Update Name]** en **[!UICONTROL Description]**.

      - Kies de optie **Begindatum** en **[!UICONTROL End Date]** van de kalender ( ![Kalenderpictogram](../assets/icon-calendar.png) ). Als u het datumbereik leeg laat, verloopt de regel niet.

      - Klik op **[!UICONTROL Save]**.

        ![Prijsregel voor winkelwagentjes - geplande wijziging](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Optie 2:** Toewijzen aan een bestaande update:

      - Selecteren **[!UICONTROL Assign to Another Update]**.

      - Zoek de update in de lijst en klik op **[!UICONTROL Select]**.

1. Voltooi de [kartonnen prijsregel](price-rules-cart.md) indien nodig.

### Methode 2: Een batch coupons genereren

Het genereren van kortingscoupons is een asynchrone bewerking die op de achtergrond wordt uitgevoerd, zodat u in de beheerder kunt blijven werken zonder te wachten tot de bewerking is voltooid. Het systeem geeft een bericht weer wanneer de taak is voltooid.

1. Volg de instructies om een [kartonnen prijsregel](price-rules-cart.md).

1. Onder **[!UICONTROL Coupon Code]**, selecteert u de **[!UICONTROL Use Auto Generation]** selectievakje.

1. Als u het aantal keren wilt beperken dat elke klant de coupon mag gebruiken, voert u het aantal **[!UICONTROL Uses per Customer]**.

   ![Regel voor winkelprijzen - automatisch genummerde coupons genereren](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Als meerdere klanten tegelijkertijd dezelfde coupon gebruiken, is het mogelijk dat de vastgestelde gebruikslimiet wordt overschreden als gevolg van vertraagde couponverwerking.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Manage Coupon Codes]** en voer de volgende handelingen uit:

   ![Winkelprijsregel - couponcodes beheren](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Voor **[!UICONTROL Coupons Qty]** Voer het aantal coupons in dat u wilt genereren.

   - Voer de **[!UICONTROL Code Length]**, exclusief het voorvoegsel, achtervoegsel of scheidingstekens.

   - Stel de **[!UICONTROL Code Format]** op een van de volgende wijzen:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Optioneel) Voer een **[!UICONTROL Code Prefix]** toe te voegen aan het begin van de code.

   - (Optioneel) Voer een **[!UICONTROL Code Suffix]** toe te voegen aan het einde van de code.

   - (Optioneel) Voor **[!UICONTROL Dash Every X Characters]**, voert u het aantal tekens tussen elk streepje in. Als de code bijvoorbeeld 12 tekens lang is en er om de vier tekens een streepje staat, ziet het er als volgt uit `xxxx-xxxx-xxxx`. Met streepjes kunt u codes beter lezen en invoeren.

1. Klik op **[!UICONTROL Generate]**.

   Het systeem wordt weergegeven `Message is added to queue, wait to get your coupons soon`.

   Nadat de uitsnijdtaak is voltooid, wordt de lijst met gegenereerde codes weergegeven.

   | Veld | Beschrijving |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Een unieke couponcode die is gemaakt en kan worden gebruikt voor het ontvangen van speciale voorwaarden. |
   | [!UICONTROL Created] | De datum waarop de couponcode is gemaakt. |
   | [!UICONTROL Used] | Geeft aan of de coupon is gebruikt. |
   | [!UICONTROL Times Used] | Geeft aan hoe vaak de couponcode is gebruikt. |

   {style="table-layout:auto"}

U kunt couponcodes exporteren naar een CSV- of Excel XML-bestand door de bestandsindeling te selecteren en op **[!UICONTROL Export]**.

Als u couponcodes wilt verwijderen, selecteert u een of meer codes in de lijst. Selecteren `Delete` van de **[!UICONTROL Actions]**  en klik vervolgens op **[!UICONTROL Submit]**.

>[!NOTE]
>
>Hoewel de Handel het vormen van veelvoudige couponcodes toestaat, kan een klant slechts één couponcode in de kar gebruiken. Als u het gebruik van meer dan één couponcode in het winkelwagentje tegelijk wilt toestaan, kunt u overwegen een overeenkomstige verlenging te gebruiken van [Commerce Marketplace](https://marketplace.magento.com/).

## Coupons-rapport

De _Coupons_ rapporteren aggregaatgegevens van elke coupon die wordt gebruikt gedurende een specifiek datumbereik. Omdat coupons worden toegepast vanaf het winkelwagentje, bevat het rapport gegevens van alle terugbetaalde coupons, ongeacht [orderstatus](../stores-purchase/order-status.md). Bijgevolg kan het verslag zowel de geraamde als de werkelijke totalen bevatten. Het rapport kan voor een specifieke opslagmening, tijdspanne, ordestatus, en de kartprijsregel worden gefiltreerd.

In het volgende voorbeeld werd de couponcode &quot;H20&quot; door twee klanten gebruikt. Een van de orders wordt gefactureerd, maar de andere is nog steeds _hangend_. In de kolommen Subtotaal voor verkoop, Verkoop en Totaal voor verkoop worden de geaggregeerde bedragen van beide bestellingen weergegeven, maar in de kolommen Subtotaal, Korting en Totaal wordt alleen de werkelijk gefactureerde volgorde weergegeven. Elke rij in het rapport vertegenwoordigt één enkele couponbevordering.

![Coupons-rapport](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Het rapport uitvoeren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Als u meerdere winkelweergaven hebt, stelt u **[!DNL Store View]** in de linkerbovenhoek om het bereik van het rapport vast te stellen.

1. De verkoop vernieuwen [statistieken](../getting-started/sales-reports.md#refresh-statistics) voor de dag klikt u op _Laatst bijgewerkt_ bericht boven aan de werkruimte.

   Klik vervolgens om het **[!UICONTROL Coupons]** selectievakje en klik op **[!UICONTROL Refresh]**.

   ![Coupons-rapport - verfrissingsstatistieken](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Ga als volgt te werk om de gegevens te filteren:

   ![Couponrapport - filters](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Date Used]** op een van de volgende wijzen:

      - `Order Created`
      - `Order Updated`

     De _Bestelling bijgewerkt_ het rapport wordt gecreeerd in echt - tijd en vereist niet verfrist.

   - Om de in het verslag bestreken periode te bepalen, stelt u **[!UICONTROL Period]** op een van de volgende wijzen:

      - `Day`
      - `Month`
      - `Year`

   - Om de datumwaaier van het rapport te bepalen, ga in **Van** en **Naar** datums in de notatie M/D/YY.

   - Een rapport afdrukken voor een specifieke [orderstatus](../stores-purchase/order-status.md), set **[!UICONTROL Order Status]** tot `Specified` en kiest u de orderstatus in de lijst.

   - Als u rijen zonder gegevens uit het rapport wilt weglaten, stelt u **[!UICONTROL Empty Rows]** tot `No`.

   - Voer een van de volgende handelingen uit om de couponactiviteit in het rapport te definiëren:

      - Om alle couponactiviteiten van alle prijsregels op te nemen, stelt u **[!UICONTROL Cart Price Rule]** tot `Any`.
      - Om alleen activiteiten op te nemen die verband houden met een specifieke prijsregel **[!UICONTROL Cart Price Rule]** tot `Specified` en selecteer de regel voor de winkelwagenprijs in de lijst.

1. Wanneer klaar om het rapport in werking te stellen, klik **[!UICONTROL Show Report]**.

   Het rapport wordt onder aan de pagina weergegeven.

### Filteropties

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Date Used] | Identificeert het datumgebied dat als basis van het rapport wordt gebruikt. Opties:<br/>**[!UICONTROL Order Created]**: Genereert het rapport dat op de datum wordt gebaseerd dat de orde door de klant werd geplaatst. Om ervoor te zorgen dat de huidigste gegevens worden omvat, klik de verbinding in het bericht om statistieken te verfrissen.<br/>**[!UICONTROL Order Updated]**: Genereert het rapport op basis van de datum waarop de bestellingen voor het laatst zijn bijgewerkt. Dit rapport gebruikt gegevens in real time en vereist geen statistieken om worden vernieuwd. |
| [!UICONTROL Period] | Bepaalt het type van datumwaaier die voor het rapport wordt gebruikt. Opties: `Day` / `Month` / `Year` |
| [!UICONTROL From] | Geeft de eerste datum in het bereik van ordergegevens aan die in het rapport is opgenomen. |
| [!UICONTROL To] | Geeft de laatste datum in het bereik van ordergegevens aan die in het rapport is opgenomen. |
| [!UICONTROL Order Status] | Filtert het rapport op ordestatus. Het rapport kan voor alle orders worden gegenereerd of worden beperkt tot een specifieke orderstatus. Opties: <br/>**[!UICONTROL Any]**: Bevat alle opdrachten, ongeacht de status.<br/>**[!UICONTROL Specified]**: Neemt alleen orders met de opgegeven status op. Geannuleerde orders worden niet in het rapport opgenomen. |
| [!UICONTROL Empty Rows] | Hiermee bepaalt u of het rapport rijen lege gegevens bevat die kunnen worden opgehaald. Opties: `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Hiermee bepaalt u welke couponpromoties worden opgenomen in het rapport. Opties:<br/>**[!UICONTROL Any]**: Deze groep bevat ordergegevens voor alle couponpromoties die zijn gebruikt tijdens het opgegeven datumbereik.<br/>**[!UICONTROL Specified]**: Bevat alleen bestelgegevens voor de geselecteerde couponbevordering tijdens het opgegeven datumbereik. |

{style="table-layout:auto"}

### Kolommen rapporteren

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Interval] | Geeft het datumbereik van het gebruik van coupons aan dat in het rapport moet worden opgenomen. Het interval kan een specifieke dag, maand, of jaar, of waaier van data zijn. De intervaldatum wordt volgens de waarde die is ingesteld in **[!UICONTROL Period]** instellen:<br/>`Day`21-6-19<br/>`Month`Debat : 6 juni 2019<br/>`Year`2019 |
| [!UICONTROL Coupon Code] | De code van de Korting die door klanten in het winkelwagentje wordt ingegaan om de korting te ontvangen. |
| [!UICONTROL Price Rule] | De naam van de prijsregel die aan de coupon is gekoppeld. |
| [!UICONTROL Uses] | Het aantal keren dat de coupon is gebruikt gedurende het datumbereik dat voor het rapport is opgegeven. |
| [!UICONTROL Sales Subtotal] | Het geprojecteerde Subtotaal van alle orders die met de coupon zijn geplaatst. <br/>Het Subtotaal van de Verkoop vertegenwoordigt het geaggregeerde Subtotaal van alle in aanmerking komende orders en omvat `Pending` verkooporders die nog niet zijn gefactureerd. |
| [!UICONTROL Sales Discount] | Het geprojecteerde kortingsbedrag van alle orders die met de coupon zijn geplaatst. <br/>De korting vertegenwoordigt het geaggregeerde disagio van alle in aanmerking komende orders en omvat `Pending` verkooporders die nog niet zijn gefactureerd. |
| [!UICONTROL Sales Total] | Het geprojecteerde Grand Total van alle orders die met de coupon zijn geplaatst. Het verkooptotaal bevat verzendkosten, verminderd met het bedrag van de korting. <br/>Het totaal van de verkopen vertegenwoordigt het geaggregeerde totaal van alle in aanmerking komende orders en omvat `Pending` verkooporders die nog niet zijn gefactureerd. De waarde omvat het subtotaal plus verzendkosten, minus de korting plus btw. <br/> Berekend door: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Het geaggregeerde subtotaal van alle gefactureerde orders die van de coupon gebruikten. |
| [!UICONTROL Discount] | De geaggregeerde korting van alle gefactureerde orders die de coupon hebben gebruikt. |
| [!UICONTROL Total] | Het geaggregeerde ordertotaal van alle gefactureerde orders die de coupon hebben gebruikt. |

{style="table-layout:auto"}
