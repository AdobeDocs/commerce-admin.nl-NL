---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Customers] &gt; [!UICONTROL Promotions] pagina van de Commerce Admin.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Regels voor automatische e-mailherinnering](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Algemeen | Hiermee schakelt u automatische e-mailherinneringen in. Als deze optie is ingesteld op Nee, worden de overige instellingen genegeerd. Opties: `Yes` / `No` |
| [!UICONTROL Frequency] | Algemeen | Hiermee geeft u de frequentie aan waarmee de Handel nieuwe klanten moet controleren die in aanmerking komen voor de automatische e-mailherinneringen. Opties: <br/>**`Minute Intervals`**- Hiermee verzendt u het e-mailbericht volgens het geselecteerde interval. (5 minuten, 10 minuten, 15 minuten, 20 minuten of 30 minuten)<br/>**`Hourly`** - verzendt het e-mailbericht per uur, op de minuut na het opgegeven uur. Voer een waarde in tussen 0 en 59. <br/>**`Daily`**- Verzendt dagelijks e-mail, vanaf de Tijd van het Begin. |
| [!UICONTROL Interval] | Algemeen | Het interval moet gelijk zijn aan of groter zijn dan de startperiode van cron.php. Opties: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Algemeen | Hiermee stelt u de dag, de minuut en de seconde in waarop de e-mail wordt verzonden. Opgegeven in 24-uursnotatie, gebaseerd op de systeemtijd op uw server. |
| [!UICONTROL Maximum Emails per One Run] | Algemeen | Hiermee beperkt u het aantal e-mailberichten dat in een gepland blok wordt verzonden. |
| [!UICONTROL Email Send Failure Threshold] | Algemeen | Het aantal keren dat de herinnering probeert meldingen naar een specifiek e-mailadres te verzenden en is mislukt. Wanneer de waarde is ingesteld op 0, is er geen drempel en worden ondanks eventuele fouten nog steeds meldingen verzonden. |
| [!UICONTROL Reminder Email Sender] | Winkelweergave | De opslagidentiteit die wordt weergegeven als de afzender van de e-mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Automatisch gegenereerde specifieke couponcodes](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Code Length] | Algemeen | Definieert de lengte van de waardeboncode, exclusief het voor- en achtervoegsel en de scheidingstekens. |
| [!UICONTROL Code Format] | Algemeen | Definieert de notatie van de couponcode. U kunt onder andere de volgende opties kiezen: <br/>**`Alphanumeric`**- Elke combinatie van letters en cijfers.<br/>**`Alphabetical`** - alleen letters. <br/>**`Numeric`**- Alleen nummers. |
| [!UICONTROL Code Prefix] | Algemeen | Een waarde die aan het begin van alle couponcodes wordt toegevoegd. Laat het veld leeg als u geen voorvoegsel wilt gebruiken. |
| [!UICONTROL Code Suffix] | Algemeen | Een waarde die aan het einde van alle codes wordt toegevoegd. Laat het veld leeg als u geen achtervoegsel wilt gebruiken. |
| [!UICONTROL Dash Every X Characters] | Algemeen | Het interval voor het invoegen van een streepje (-) in alle couponcodes. Laat het veld leeg als u geen streepje wilt gebruiken. <br/>_**Opmerking:**_ Couponcodes die alleen door een streepje verschillen, worden als verschillende codes beschouwd. |

{:style=&quot;table-layout:auto&quot;}
