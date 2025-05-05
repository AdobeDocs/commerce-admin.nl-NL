---
title: Valutaconfiguratie
description: Leer hoe u het bereik van de basisvaluta instelt en hoe u de valuta's opgeeft die u accepteert en de valuta die u wilt gebruiken voor de prijsweergave.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Valutaconfiguratie

Alvorens individuele munttarieven op te zetten, moet u het werkingsgebied van de [ basismunt ](../configuration-reference/general/currency-setup.md) eerst plaatsen. Het wordt geplaatst aan globaal door gebrek, dat de basismunt die op de volledige [ opslaghiërarchie ](../getting-started/websites-stores-views.md) plaatst toepast. Als u een Adobe Commerce- of Magento Open Source-installatie met meerdere sites hebt, kunt u meerdere basisvaluta&#39;s beheren door het bereik in te stellen op websiteniveau.

U specificeert ook de valuta die u goedkeurt en welke munt u voor de vertoning van [ prijzen ](../catalog/catalog-price-scope.md) in uw opslag wilt gebruiken. In het volgende diagram wordt het bereik van de basisvaluta ingesteld op websiteniveau, zodat elke website een andere basisvaluta kan hebben.

![ diagram van het werkingsgebied van de Valuta ](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Stap 1: Kies de geaccepteerde valuta&#39;s

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Stel in de linkerbovenhoek **[!UICONTROL Scope]** in op de winkelweergave waarop de configuratie van toepassing is.

1. In het linkerpaneel onder _Algemene_, kies **[!UICONTROL Currency Setup]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Currency Options]** sectie uit en plaats de volgende opties:

   - **[!UICONTROL Base Currency]** — Instellen op de primaire valuta die u gebruikt voor online transacties.

   - **[!UICONTROL Default Display Currency]** — Instellen op de valuta die u gebruikt om de prijsstelling in de winkelweergave weer te geven.

   - **[!UICONTROL Allowed Currencies]** — Selecteer alle valuta&#39;s die u als betaling accepteert in de winkelweergave. Selecteer ook de primaire valuta.

     Houd voor meerdere valuta&#39;s de Ctrl-toets (PC) of de Command-toets (Mac) ingedrukt en klik op elke optie.

   ![ Algemene configuratie - muntopties ](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Opties van de Valuta ](../configuration-reference/general/currency-setup.md) in de _Gids van de Verwijzing van de Configuratie_.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, klik _dicht_ ( ![ dicht doos ](../assets/icon-close-x.png)) in de hoger-juiste hoek van het systeembericht.

   U kunt [ het geheime voorgeheugen ](../systems/cache-management.md) later verfrissen.

1. Bepaal de reikwijdte van de basisvaluta:

   - Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

   - De rol neer en breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Price]** sectie. (Deze sectie verschijnt slechts als het werkingsgebied als **[!UICONTROL Store View:]** _Standaard config_ wordt geplaatst.)

   - Stel **[!UICONTROL Catalog Price Scope]** in op `Global` of `Website` .

   ![ configuratie van de Catalogus - prijsopties ](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Stap 2: De importverbinding configureren

1. Blader naar de bovenkant van de pagina.

1. Vouw in het linkerdeelvenster **[!UICONTROL General]** uit en kies **[!UICONTROL Currency Setup]** .

1. Configureer uw verbinding met de valutaservice:

   Er zijn drie serviceopties: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ en _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >Beginnend met versie 2.4.6, wordt de [[!DNL Fixer.io] ](https://fixer.io/) dienst afgekeurd en met de [[!DNL Fixer API]  vervangen (APILayer) ](https://apilayer.com/marketplace/fixer-api) dienst. Het wordt ten zeerste aanbevolen een APILayer-account te gebruiken in plaats van een afgekeurd [!DNL Fixer.io] -account.

   - _om met de {[&#128279;](https://fixer.io/) dienst 1} te verbinden fixer.io:_

      - Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Fixer.io]** sectie uit.

      - Voer het bestand fixer.io **[!UICONTROL API key]** in.

      - Voer bij **[!UICONTROL Connection Timeout in Seconds]** het aantal seconden inactiviteit in dat is toegestaan voordat de verbinding wordt verbroken.

     ![ Algemene configuratie - muntopstelling - opties Fixer.io ](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _om met de [[!DNL Fixer Api (APILayer)]  dienst ](https://apilayer.com/) te verbinden:_

      - Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Fixer Api (APILayer)]** sectie uit.

      - Voer uw [!DNL APILayer] **[!UICONTROL API key]** in.

      - Voer bij **[!UICONTROL Connection Timeout in Seconds]** het aantal seconden inactiviteit in dat is toegestaan voordat de verbinding wordt verbroken.

     ![ Algemene configuratie - muntopstelling - de opties van Fixer API (APILayer) ](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _om met de [[!DNL Currency Convertor API]  dienst ](https://free.currencyconverterapi.com/) te verbinden:_

      - Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Currency Convertor API]** sectie uit.

      - Voer de valutaconvertor in **[!UICONTROL API key]** .

      - Voer bij **[!UICONTROL Connection Timeout in Seconds]** het aantal seconden inactiviteit in dat is toegestaan voordat de verbinding wordt verbroken.

     ![ Algemene configuratie - muntopstelling - de opties van API van de Convertor van de Valuta ](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Stap 3: Configureer de geplande importinstellingen

1. Voortdurend met de Opstelling van de Valuta, breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL Scheduled Import Settings]** sectie.

   ![ Algemene configuratie - valuta geplande de invoermontages ](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Als u de valutakoersen automatisch wilt bijwerken, stelt u **[!UICONTROL Enabled]** in op `Yes` .

1. Stel de update-opties in:

   - **[!UICONTROL Service]** — Instellen op de tariefprovider. De standaardwaarde is `Fixer.io (legacy)` .

   - **[!UICONTROL Start Time]** — Stel dit in op het uur, de minuut en de seconde waarop de tarieven volgens het schema worden bijgewerkt.

   - **[!UICONTROL Frequency]** — Om te bepalen hoe vaak de tarieven worden bijgewerkt, plaats aan één van het volgende:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** — Voer het e-mailadres in van de persoon die de e-mailmelding moet ontvangen als zich tijdens het importeren een fout voordoet.

     Als u meerdere e-mailadressen wilt invoeren, scheidt u deze met een komma.

   - **[!UICONTROL Error Email Sender]** — Reeks aan het [ opslagcontact ](../getting-started/store-details.md#store-email-addresses) dat als afzender van het foutenmelding verschijnt.

   - **[!UICONTROL Error Email Template]** — Instellen op de e-mailsjabloon die wordt gebruikt voor de foutmelding.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Wanneer u wordt gevraagd de cache bij te werken, klikt u op de koppeling **[!UICONTROL Cache Management]** en vernieuwt u de ongeldige cache.

   ![ bericht van het Systeem - vernieuw het ongeldige geheime voorgeheugen ](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Stap 4: De wisselkoersen bijwerken

De wisselkoersen moeten met de huidige waarden worden bijgewerkt voordat ze in werking treden. [ werk de tarieven ](currency-update.md) manueel bij of om de tarieven automatisch in te voeren.

## Stap 5: Valutasymbolen aanpassen (optioneel)

Met behulp van Valutasymbolen kunt u het symbool aanpassen dat is gekoppeld aan elke valuta die als betaling in uw winkel wordt geaccepteerd.

![ de symbolen van de Valuta ](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Elke valuta die voor je winkel is ingeschakeld, wordt in de lijst _[!UICONTROL Currency]_&#x200B;weergegeven.

1. Wijzig desgewenst de instellingen in de lijst:

   - Voer een aangepast symbool in voor elke valuta die u wilt gebruiken of selecteer het selectievakje **[!UICONTROL Use Standard]** voor elke valuta.

   - Als u het standaardsymbool wilt overschrijven, schakelt u het selectievakje _[!UICONTROL Use Standard]_&#x200B;uit en voert u het symbool in dat u wilt gebruiken.

   >[!NOTE]
   >
   >Het is niet mogelijk de uitlijning van het valutasymbool van links naar rechts te wijzigen.

1. Klik op **[!UICONTROL Save Currency Symbols]** als de bewerking is voltooid.

1. Wanneer u wordt gevraagd de cache bij te werken, klikt u op de koppeling **[!UICONTROL Cache Management]** en vernieuwt u eventuele ongeldige cache.
