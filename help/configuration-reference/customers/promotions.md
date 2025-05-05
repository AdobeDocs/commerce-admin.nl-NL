---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Customers] &gt; [!UICONTROL Promotions] van Commerce Admin.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![ Geautomatiseerde Regels van de Herinnering E-mail ](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Algemeen | Hiermee schakelt u automatische e-mailherinneringen in. Als deze optie is ingesteld op Nee, worden de overige instellingen genegeerd. Opties: `Yes` / `No` |
| [!UICONTROL Frequency] | Algemeen | Geeft aan hoe vaak Commerce moet controleren op nieuwe klanten die in aanmerking komen voor de automatische e-mailherinneringen. Opties: <br/>**`Minute Intervals`**- verzendt het e-mailbericht volgens het geselecteerde interval. (5 minuten, 10 minuten, 15 minuten, 20 minuten of 30 minuten)<br/>**`Hourly`** - verzendt het e-mailbericht per uur, op de minuut na het opgegeven uur. Voer een waarde in tussen 0 en 59. <br/>**`Daily`**- verzendt dagelijks e-mail, van de Tijd van het Begin. |
| [!UICONTROL Interval] | Algemeen | Het interval moet gelijk zijn aan of groter zijn dan de startperiode van cron.php. Opties: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Algemeen | Hiermee stelt u de dag, de minuut en de seconde in waarop de e-mail wordt verzonden. Opgegeven in 24-uursnotatie, gebaseerd op de systeemtijd op uw server. |
| [!UICONTROL Maximum Emails per One Run] | Algemeen | Hiermee beperkt u het aantal e-mailberichten dat in een gepland blok wordt verzonden. |
| [!UICONTROL Email Send Failure Threshold] | Algemeen | Het aantal keren dat de herinnering probeert meldingen naar een specifiek e-mailadres te verzenden en is mislukt. Wanneer de waarde is ingesteld op 0, is er geen drempel en worden ondanks eventuele fouten nog steeds meldingen verzonden. |
| [!UICONTROL Reminder Email Sender] | Winkelweergave | De opslagidentiteit die wordt weergegeven als de afzender van de e-mail. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![ Auto Gegenereerde Specifieke Codes van de Coupon ](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/nl/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Code Length] | Algemeen | Definieert de lengte van de waardeboncode, exclusief het voor- en achtervoegsel en de scheidingstekens. |
| [!UICONTROL Code Format] | Algemeen | Definieert de notatie van de couponcode. Opties zijn: <br/>**`Alphanumeric`**- Een willekeurige combinatie van letters en cijfers.<br/>**`Alphabetical`** - Alleen letters. <br/>**`Numeric`**- Alleen nummers. |
| [!UICONTROL Code Prefix] | Algemeen | Een waarde die aan het begin van alle couponcodes wordt toegevoegd. Laat het veld leeg als u geen voorvoegsel wilt gebruiken. |
| [!UICONTROL Code Suffix] | Algemeen | Een waarde die aan het einde van alle codes wordt toegevoegd. Laat het veld leeg als u geen achtervoegsel wilt gebruiken. |
| [!UICONTROL Dash Every X Characters] | Algemeen | Het interval voor het invoegen van een streepje (-) in alle couponcodes. Laat het veld leeg als u geen streepje wilt gebruiken. <br/>_&#x200B;**Nota:**&#x200B;_ de codes van de coupon die door slechts een streepje verschillen worden beschouwd als verschillende codes. |

{style="table-layout:auto"}
