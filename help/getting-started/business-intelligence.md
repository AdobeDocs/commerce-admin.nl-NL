---
title: '''[!DNL Business Intelligence] gereedschappen'
description: Leer hoe handelaars van Adobe Commerce en van de Magento Open Source bedrijfsintelligentiegereedschappen kunnen gebruiken om het inzicht te verkrijgen dat wordt gebruikt om correcte bedrijfsbesluiten te nemen.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# [!DNL Business Intelligence] gereedschappen

De bedrijfsintelligentiegereedschappen van het gebruik om het inzicht te verkrijgen dat wordt gebruikt om correcte bedrijfsbesluiten te nemen.

## [!DNL Business Intelligence] account

Wanneer u een [!DNL Business Intelligence] via Adobe hebt u toegang tot vijf dashboards met ongeveer 70 rapporten. Deze rapporten zijn ontworpen om inzicht te verschaffen in uw gegevens en vragen te beantwoorden zoals &quot;Hoe worden mijn bestellingen maandelijks gegroeid?&quot;, &quot;Wie zijn mijn meest loyale klanten?&quot;, en &quot;Werkt mijn couponstrategie?&quot; Voor gedetailleerde informatie over deze gereedschapsset raadpleegt u de [MBI-gebruikershandleiding][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] wordt opgenomen in Adobe Commerce en Magento Open Source. Deze functie biedt u toegang tot een reeks dynamische rapporten die op uw product, orde, en klantengegevens gebaseerd zijn, met een gepersonaliseerd dashboard dat aan uw bedrijfsbehoeften wordt aangepast. while [!DNL Advanced Reporting] gebruik [!DNL Business Intelligence] voor analyses hebt u geen Business Intelligence-account nodig om te gebruiken [!DNL Advanced Reporting].

Zie voor technische informatie de [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} in de ontwikkelaarsdocumentatie.

>[!NOTE]
>
>[!DNL Business Intelligence] accounts maken gebruik van ingebouwde rapportage in plaats van de [!DNL Advanced Reporting] gebruiken.

![Geavanceerd rapportdashboard](./assets/reporting-advanced.png){width="700"}

### Vereisten

* De website moet worden uitgevoerd op een openbare webserver.

* Het domein moet een geldig beveiligingscertificaat (SSL) hebben.

* [!DNL Commerce] moet zonder fout geïnstalleerd of bevorderd zijn.

* In de [!DNL Commerce] configuratie voor [opslag-URL&#39;s](../stores-purchase/store-urls.md)de **[!UICONTROL Base URL (Secure)]** het plaatsen voor de archiefmening moet aan veilige URL richten. Bijvoorbeeld: `https://yourdomain.com`.

* In de [!DNL Commerce] configuratie voor opslag-URL&#39;s, **[!UICONTROL Use Secure URLs on Storefront]** en **[!UICONTROL Use Secure URLs in Admin]** moet worden ingesteld op `Yes`.

* [[!DNL Commerce] crontab][3] wordt gemaakt en er worden snijtaken uitgevoerd op de geïnstalleerde server.

>[!NOTE]
>
>[!DNL Advanced Reporting] kan alleen worden gebruikt met [!DNL Commerce] installaties die voortdurend één installatie hebben gebruikt [basisvaluta](../stores-purchase/currency-configuration.md).


### Stap 1: Inschakelen [!DNL Advanced Reporting]

In de [!DNL Commerce] configuratie, [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) is standaard ingeschakeld en wordt automatisch gestart als de uitsnede is [geconfigureerd](../configuration-reference/advanced/system.md) en wordt uitgevoerd. Een poging om het abonnement te vestigen wordt begonnen aan het begin van elk uur over de volgende 24 uur tot succesvol. De status van het abonnement is in behandeling totdat het abonnement is ingesteld.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkernavigatievenster waar **[!UICONTROL General]** wordt uitgebreid, kiest u **[!UICONTROL Advanced Reporting]** en voer de volgende handelingen uit:

   * Controleren of **[!UICONTROL Advanced Reporting Service]** is ingesteld op `Enable` (de standaardinstelling).

   * Stel de **[!UICONTROL Time of day to send data]** tot het uur, de minuut, en de tweede, volgens een klok van 24 uur, dat u de dienst bijgewerkte gegevens van uw opslag wilt ontvangen. Standaard worden gegevens verzonden om 2:00 uur.

   * Onder **[!UICONTROL Industry Data]**, kiest u de **[!UICONTROL Industry]** dat het beste uw zaken beschrijft.

   ![Geavanceerde rapportconfiguratie](./assets/advanced-reporting-config.png){width="400"}

1. Klik op **[!UICONTROL Save Config]**.

1. Klik op **[[!UICONTROL Cache Management]](../systems/cache-management.md)** in het bericht boven aan de pagina en vernieuw eventuele ongeldige caches.

1. Wacht een nacht of tot na de tijd van de volgende geplande update. Controleer vervolgens de status van uw abonnement. Als de status nog steeds _hangend_, moet u controleren of de installatie aan alle vereisten voldoet.

### Stap 2: Toegang [!DNL Advanced Reporting]

1. Voer een van de volgende handelingen uit:

   * Op de _Beheerder_ zijbalk, kies **[!UICONTROL Dashboard]**. Klik vervolgens op **[!UICONTROL Go to Advanced Reporting]**.
   * Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   De [!DNL Advanced Reporting] dashboard geeft een snel overzicht van uw bestellingen, klanten en producten. Schuif omlaag om het volledige dashboard weer te geven.

1. Als u een betere weergave van de gegevens wilt, stelt u de **[!UICONTROL Filters]** in de hoger-juiste hoek aan de periode en opslagmening die u in het rapport wilt omvatten. Voer vervolgens de volgende handelingen uit:

   * Houd de muisaanwijzer boven een gegevenspunt voor meer informatie.
   * Klik op elk tabblad om alle dashboardrapporten weer te geven.

   ![Gegevenspunt](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Toegang [!DNL Advanced Reporting] gegevensbronnen

Klik in de rechterbovenhoek van het dashboard Geavanceerde rapporten op **[!UICONTROL Additional Resources]**.

![Geavanceerde gegevensbronnen voor rapporten](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Problemen oplossen

Als je het bericht &quot;Pagina niet gevonden&quot; van 404 ontvangt, controleer dan of je winkel voldoet aan de vereisten voor [!DNL Advanced Reporting]. Volg vervolgens de instructies om te controleren of de integratie is geïnstalleerd.

### Controleren of de integratie actief is

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Controleer of de **[!UICONTROL Magento Analytics user]** de integratie wordt weergegeven in de lijst en de **[!UICONTROL Status]** is `Active`.

1. Als u de gebruiker opnieuw wilt instellen, klikt u op **[!UICONTROL Reauthorize]** en voer de volgende handelingen uit:

   ![Opnieuw goedkeuren](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Klik op **[!UICONTROL Reauthorize]** de toegang tot de API-bronnen goedkeuren.

     ![Toegang tot API-bronnen opnieuw toestaan](./assets/advanced-reporting-integration-api.png){width="600"}

   * Verifieer dat de lijst van de Tokens van de Integratie voor Uitbreidingen volledig is. Klik vervolgens op **Gereed**.

     ![Integratietokens](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Zoek het bericht dat op de integratie wijst `Magento Analytics user` opnieuw is toegestaan.

1. Wacht een nacht of tot na het tijdstip van de volgende geplande update.

### Eén basisvaluta verifiëren

[!DNL Advanced Reporting] kan alleen worden gebruikt met [!DNL Commerce] installaties die slechts één installatie hebben gebruikt [basisvaluta](../stores-purchase/currency-configuration.md) sinds het tijdstip van installatie. Het resultaat is dat in de geschiedenis alle orders dezelfde basisvaluta gebruiken. [!DNL Advanced Reporting] werkt niet als u op enig moment uw basisvaluta hebt gewijzigd en bestellingen in uw geschiedenis hebt die met verschillende basisvaluta&#39;s zijn verwerkt.

Als je winkel meerdere basisvaluta&#39;s heeft, kun je je vragen [!DNL Commerce] gegevensbestand van de bevellijn gebruikend het volgende voorbeeld MySQL. Mogelijk moet u de tabelnamen aanpassen aan de gegevensstructuur:

```sql
select distinct base_currency_code from sales_order;
```

### Gegevensafwijking

Als u merkt dat de `Data last updated...` het bijschrift toont de datum van gisteren en niet van vandaag, er zou een vertraging van tot een dag in de Geavanceerde updates van het Rapporteren kunnen zijn. Deze vertraging is te wijten aan een groter dan verwachte wachtrijgrootte.

## Dashboardrapporten

**[!UICONTROL Orders]**

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Revenue] | Toont alle opbrengst die door de archiefmening tijdens de bepaalde tijdspanne wordt ontvangen. |
| [!UICONTROL Orders] | Toont alle orden die door de archiefmening tijdens de bepaalde tijdspanne worden geplaatst. |
| [!UICONTROL AOV] | Toont de gemiddelde die ordewaarde door de archiefmening tijdens de bepaalde tijdspanne wordt geplaatst. |
| [!UICONTROL Refunds] | Toont alle terugbetalingen die door de archiefmening tijdens de bepaalde tijdspanne worden verwerkt. |
| [!UICONTROL Tax Collected] | Toont alle belasting die door de archiefmening tijdens de bepaalde tijdspanne wordt verzameld. |
| [!UICONTROL Shipping Collected] | Hiermee worden alle verzendkosten weergegeven die tijdens de opgegeven periode via de winkelweergave zijn geïnd. |
| [!UICONTROL Orders by Status] | Toont het aantal orden door status, voor de archiefmening tijdens de bepaalde tijdspanne. |
| [!UICONTROL Orders by Status] | Hiermee geeft u een overzicht van het aantal bestellingen per status. |
| [!UICONTROL Coupon Usage] | Hiermee geeft u alle couponcodes en het aantal gebruikers voor elke code weer, die gedurende de gedefinieerde periode via de winkelweergave zijn afgelost. |
| [!UICONTROL Orders and Revenue by Billing Region] | Vermeldt het aantal orders en de opbrengst per gebied voor de archiefmening tijdens de bepaalde tijdspanne. |
| [!UICONTROL Tax Collected by Billing Region] | Hier wordt het bedrag aan belasting weergegeven dat per regio is geïnd voor de winkelweergave tijdens de gedefinieerde tijdsperiode. |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | Hier worden de verzendkosten weergegeven die per regio zijn geïnd voor de winkelweergave tijdens de gedefinieerde periode. |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Unique Customers] | Toont het aantal unieke klantenrekeningen verbonden aan de archiefmening tijdens de bepaalde tijdspanne. |
| [!UICONTROL New Registered Accounts] | Toont het aantal nieuwe die klantenrekeningen bij de archiefmening tijdens de bepaalde tijdspanne worden geregistreerd. |
| [!UICONTROL Top Coupon Users] | Hiermee geeft u de hoogste gebruikers van de coupon weer op basis van de klant-id en het aantal orders met coupons voor de winkelweergave tijdens de gedefinieerde periode. |
| [!UICONTROL Customer KPI Table] | Vermeldt het aantal bestellingen, de omzet en de gemiddelde orderwaarde per klant-id voor de winkelweergave tijdens de gedefinieerde periode. |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | Hier wordt het aantal producten weergegeven dat tijdens de gedefinieerde periode via de winkelweergave is verkocht. |
| [!UICONTROL Products Added to Wishlists] | Hiermee geeft u alle producten weer die tijdens de gedefinieerde tijdsperiode aan verlanglijsten zijn toegevoegd via de winkelweergave. |
| [!UICONTROL Best Selling Products by Quantity] | Hier worden de best verkochte producten en de hoeveelheid weergegeven die tijdens de gedefinieerde periode via de winkelweergave zijn verkocht. |
| [!UICONTROL Best Selling Products by Revenue] | Hier worden de best verkochte producten en inkomsten weergegeven die worden gegenereerd door de verkoop van het product via de winkelweergave tijdens de gedefinieerde periode. |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
