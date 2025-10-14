---
title: Configuratiebereik
description: Meer informatie over het instellen van het bereik voor configuratie-instellingen in Commerce Admin.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Configuratiebereik

De keuze van de Mening van de Opslag in de upper-left hoek van vele configuratiepagina&#39;s filtert de mening van de pagina voor een specifiek werkingsgebied, en plaatst de waarde van sommige entiteiten die door Commerce worden gebruikt. Het maakt een lijst van elk niveau in de hiërarchie door naam, en wordt gebruikt om het werkingsgebied in een ander niveau te veranderen. Alle instellingen die het huidige bereik vertegenwoordigen, worden grijs weergegeven. Alleen de instellingen die de huidige bereikinstelling vertegenwoordigen, zijn dus beschikbaar. Het werkingsgebied wordt aanvankelijk geplaatst aan _StandaardConfig_. Voor Admin gebruikers met beperkte toegang, omvat de lijst van beschikbare opslagmeningen slechts die tot wie de gebruiker [&#x200B; toestemming &#x200B;](../systems/permissions.md) heeft om toegang te hebben.

| Niveau | Beschrijving |
|--- |--- |
| [!UICONTROL Default Config] | De standaardsysteemconfiguratie. |
| [!UICONTROL Main Website] | De naam van de website boven in de hiërarchie. |
| [!UICONTROL Main Website Store] | De naam van de standaardwinkel die aan de bovenliggende website is gekoppeld. |
| [!UICONTROL Default Store View] | De naam van de standaardopslagweergave die aan de bovenliggende opslag is gekoppeld. |
| [!UICONTROL Stores Configuration] | Springt naar het raster Opslagruimten en is hetzelfde als [!UICONTROL Stores] > [!UICONTROL All Stores] kiezen in het zijpaneel Beheer. |

{style="table-layout:auto"}

![&#x200B; geselecteerde checkboxes van de Waarde van het Systeem van het Gebruik &#x200B;](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

Het selectievakje _[!UICONTROL Use System Value]_&#x200B;rechts van veel configuratie-instellingen wordt gebruikt om de standaardwaarde voor het veld binnen het huidige configuratiebereik toe te passen of te overschrijven. De standaardwaarde voor het veld kan niet worden gewijzigd wanneer het selectievakje is ingeschakeld. Als u de waarde wilt wijzigen, schakelt u het selectievakje uit en voert u de nieuwe waarde in. U wordt gevraagd te bevestigen wanneer u de systeemwaarde wijzigt.

Het label van het selectievakje verandert afhankelijk van het huidige bereik en verwijst altijd naar het bovenliggende niveau dat één stap hoger in de hiërarchie van het bereik is. Omdat het ouderniveau een container voor alle punten onder dat niveau is, wordt het werkingsgebied dat van het ouderniveau plaatst geërft tenzij het wordt met voeten getreden.

## Standaardopties voor waarden

| Selectievakje | Beschrijving |
|--- |--- |
| [!UICONTROL Use system value] | Dit selectievakje wordt weergegeven wanneer het configuratiebereik is ingesteld op `Default Config` . |
| [!UICONTROL Use Default] | Dit selectievakje wordt weergegeven wanneer het configuratiebereik is ingesteld op Main `Website` en verwijst naar de standaardwinkel die aan de website is toegewezen. |
| [!UICONTROL Use Website] | Dit checkbox verschijnt wanneer het configuratiewerkingsgebied aan een specifieke opslagmening wordt geplaatst. Als deze optie is geselecteerd, wordt de instelling gebruikt van de bovenliggende website die is gekoppeld aan de winkelweergave. In dit geval wordt het opslagniveau overgeslagen omdat het van toepassing is op de standaardwinkel die aan de website is gekoppeld. |

{style="table-layout:auto"}

## Bereik instellen

Ga als volgt te werk voordat u een configuratie-instelling maakt die alleen van toepassing is op een specifieke website, op een specifieke opslagweergave of op een specifieke opslagweergave:

1. Op _Admin_ sidebar, doe één van het volgende:

   - Ga voor de meeste configuratie-instellingen naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Voor [&#x200B; ontwerp-verwante montages &#x200B;](../content-design/configuration.md), ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Kies vervolgens in het raster de toepasselijke winkelweergave.

1. Navigeer naar de configuratie die u wilt wijzigen en voer de volgende handelingen uit:

   - Stel in de linkerbovenhoek **[!UICONTROL Store View]** in op de specifieke weergave waarop de configuratie van toepassing is. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd het schakelen tussen bereik en bereik te bevestigen.

     Na elk veld wordt een selectievakje weergegeven en er kunnen extra velden beschikbaar komen.

   - Schakel het selectievakje **[!UICONTROL Use system value]** uit na de velden die u wilt bewerken. Werk vervolgens de waarde voor de weergave bij.

   - Herhaal dit proces voor elk veld dat op de pagina moet worden bijgewerkt.

   ![&#x200B; plaatsend de opties van het Land van de Franse opslagmening &#x200B;](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Snelle naslaggids voor bereik

| Toepassingsgebied | Beschrijving |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Beheerder | Alle websites, winkels en winkelweergaven in de installatie worden beheerd vanuit dezelfde beheerder. |
| Standaardconfiguratie | De globale [&#x200B; standaardconfiguratie &#x200B;](../getting-started/websites-stores-views.md#scope-settings) montages worden gebruikt door de opslaghiërarchie, tenzij zij op een lager niveau worden met voeten getreden. |
| Catalogus | De termijn _catalogus_ verwijst naar het productgegevensbestand als geheel, en is beschikbaar door de installatie. |
| Productprijzen | Productprijzen kunnen globaal of op websiteniveau worden geconfigureerd voor toepassing. |
| Productconfiguraties | Attributen die als [&#x200B; configureerbare product &#x200B;](../catalog/product-create-configurable.md) opties worden gebruikt moeten een globaal werkingsgebied hebben. |
| Klanten | Klantenaccounts kunnen worden geconfigureerd voor toepassing op algemeen niveau of op de website. Elke website kan een afzonderlijke reeks [&#x200B; klantenrekeningen &#x200B;](../customers/customer-account-scope.md) hebben of klantenrekeningen met andere websites in de installatie delen. |
| **[!UICONTROL Website]** |  |
| Domein | De extra [&#x200B; websites &#x200B;](../stores-purchase/introduction.md#store-structure) kunnen opstelling als subdomeinen van het primaire domein zijn, of afzonderlijke IP adressen en specifieke domeinen hebben. |
| Klanten | Klantenaccounts kunnen worden geconfigureerd voor toepassing op algemeen niveau of op de website. Elke website kan een afzonderlijke reeks [&#x200B; klantenrekeningen &#x200B;](../customers/customer-account-scope.md) hebben of klantenrekeningen met andere websites in de installatie delen. |
| Valuta | Elke website kan een verschillende [&#x200B; basismunt &#x200B;](../stores-purchase/currency-configuration.md) worden toegewezen. De basisvaluta wordt gebruikt om alle transacties te verwerken, hoewel de klant een andere weergavevaluta kan zien, afhankelijk van de landinstelling van de winkelweergave. |
| Producten | Afzonderlijke producten worden op websiteniveau aan de hiërarchie toegewezen. Het raster Producten bevat een lijst met alle producten in de catalogus en de websites waar deze beschikbaar zijn. Het [&#x200B; Product in Websites &#x200B;](../catalog/settings-basic-websites.md) plaatsen identificeert elke website waar het product beschikbaar is. |
| Productprijzen | [&#x200B; de prijzen van het Product &#x200B;](../catalog/catalog-price-scope.md) kunnen voor toepassing op of een globaal of websiteniveau worden gevormd. |
| Betalingsmethoden | [&#x200B; de methodes van de Betaling &#x200B;](../stores-purchase/payments.md) worden gevormd op het websiteniveau, hoewel de titel en de instructies voor elke archiefmening kunnen worden gevormd. |
| Afhandeling | Het [&#x200B; controleproces &#x200B;](../stores-purchase/checkout-process.md) vindt op het websiteniveau plaats, hoewel sommige vertoningsopties voor elke archiefmening kunnen worden gevormd. Alle opslag verbonden aan een website hebben de zelfde [&#x200B; controleconfiguratie &#x200B;](../stores-purchase/checkout-process.md#checkout-options). |
| Toegestane landen | Toegestane landen kunnen op websiteniveau worden geconfigureerd. De [&#x200B; toegestane landen &#x200B;](../getting-started/store-details.md#country-options) montages worden gebruikt in de controle om te beperken waar een klant uit kan komen. |
| **[!UICONTROL Store]** |  |
| Domein | Met veelvoudige opslag, kan elke opslag het zelfde domein, subdomain, of duidelijk verschillende domeinen hebben. Voor meer informatie, verwijs naar [&#x200B; het Toevoegen van Opslag &#x200B;](../stores-purchase/stores.md#add-stores). |
| Basiscategorie | Elke winkel kan een aparte set producten en een hoofdmenu hebben dat is gebaseerd op een categorie en subcategorieën van het type &quot;root&quot;. Elke catalogus heeft a [&#x200B; wortelcategorie &#x200B;](../catalog/category-root.md) die op het opslagniveau wordt toegewezen. |
| **[!UICONTROL Store View]** |  |
| Subcategorieën | De [&#x200B; subcategorieën &#x200B;](../catalog/category-create.md#category-structure) die omhoog het belangrijkste menu (onder de wortel) maken worden toegewezen op het niveau van de opslagmening. |
| Landinstelling | Elke opslagmening kan een verschillende [&#x200B; scène &#x200B;](../getting-started/store-details.md#locale-options) worden toegewezen. De weergaverevaluta, maateenheden en beheerinterface zijn specifiek voor de landinstelling. |
| Talen | Om veelvoudige talen te steunen, moet al inhoud, met inbegrip van productbeschrijvingen, [&#x200B; vertaald &#x200B;](../stores-purchase/store-localize.md#localize-products) voor elke archiefmening zijn. |
| Valuta weergeven | Een verschillende [&#x200B; vertoningsmunt &#x200B;](../stores-purchase/currency-configuration.md) kan voor elke opslagmening worden gebruikt, hoewel de transacties op het websiteniveau gebruikend de basismunt worden verwerkt. |

{style="table-layout:auto"}
