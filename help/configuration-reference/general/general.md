---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL General] &gt; [!UICONTROL General] van Commerce Admin.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Zie [ Opties van het Land ](../../getting-started/store-details.md#country-options) voor meer details over deze configuratiegebieden en opties.

![ Algemeen > de Opties van het Land ](./assets/general-country-options.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Default Country] | Winkelweergave | Het land waar je winkel zich bevindt. |
| [!UICONTROL Allow Countries] | Website | De landen waar je bestellingen accepteert. |
| [!UICONTROL Zip/Postal Code is Optional for] | Algemeen | Landen die geen postcode of postcode in het verzendadres nodig hebben. |
| [!UICONTROL European Union Countries] | Algemeen | Landen die lid zijn van de Europese Unie. |
| [!UICONTROL Top Destinations] | Winkelweergave | De primaire landen die u voor verkoop aanspreekt. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

Zie [ Opties van de Staat ](../../getting-started/store-details.md#state-options) voor meer details over deze configuratiegebieden en opties.

![ Algemeen > de Opties van de Staat ](./assets/general-state-options.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL State is required for] | Algemeen | De landen (waar u zaken doet) die een regio of een staat vereisen om in het postadres worden omvat. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Algemeen | Voor landen waar het niet wordt vereist, bepaalt als het _gebied 0&rbrace; Gebied/Staat &lbrace;in het postadres van de klant inbegrepen is.<br />_ <br />**`Yes`**- omvat het _Gebied/Staat_ gebied in het klantenadres, zelfs als niet vereist door het land.<br />**`No`** - Laat het gebied/van de Staat van het klantenadres weg als niet vereist door het land. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

Zie [ Opties van de Landinstelling ](../../getting-started/store-details.md#locale-options) voor meer details over deze configuratiegebieden en opties.

![ Algemeen > de Opties van de Landinstelling ](./assets/general-locale-options.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Timezone] | Website | De tijdzone van de primaire markt die door de website wordt bediend. Meestal is de tijdzone hetzelfde als de tijdzone die wordt gebruikt op de fysieke locatie van uw bedrijf. |
| [!UICONTROL Locale] | Winkelweergave | De taal, de valuta, en het systeem van meting die in de markt wordt gebruikt die door de archiefmening wordt gediend. |
| [!UICONTROL Weight Unit] | Winkelweergave | De maateenheid die doorgaans wordt gebruikt voor overbrengingen vanuit de landinstelling. Opties: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Winkelweergave | De dag die wordt beschouwd als de eerste dag van de week op de markt die door de winkelweergave wordt bediend. |
| [!UICONTROL Weekend Days] | Winkelweergave | De dagen die op het weekend in de markt vallen door de winkelmening worden gediend. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![ Algemeen > de Beperkingen van de Website ](./assets/general-website-restrictions.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [ de beperkingen van de Toegang ](../../merchandising-promotions/event-configure.md#access-restrictions) in de _Gids van de Verkoop en van Bevorderingen_.

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Website | Bepaalt of de website op beperkte wijze werkt.<br /> <br />**`Yes`**- Toegang tot de website wordt beperkt op de manier die is ingesteld in de onderstaande velden.<br />**`No`** - Beperkingen zijn uitgeschakeld en de volgende instellingen hebben geen effect. |
| [!UICONTROL Restriction Mode] | Website | Bepaalt het type van toegangsbeperking dat op de website van toepassing is.<br /> <br />**`Website Closed`**- Alle toegang tot de storefront is beperkt, en opslag-URL&#39;s worden tijdelijk doorgestuurd naar de landingspagina. Deze instelling kan handig zijn tijdens het onderhoud van de site of voordat u de toepassing start.<br />**`Private Sales: Login Only`** - Alleen geregistreerde klanten kunnen zich aanmelden om toegang te krijgen tot de winkel. Alle URL&#39;s van de winkel worden tijdelijk omgeleid naar de opgegeven bestemmingspagina of het opgegeven aanmeldingsformulier. Gebruikers kunnen in deze modus geen account maken.<br />**`Private Sales: Login and Register`**- Gebruikers moeten zich aanmelden om toegang te krijgen tot de winkel. Alle URL&#39;s van de winkel worden tijdelijk doorgestuurd naar het aanmeldingsformulier totdat de gebruiker zich aanmeldt. Gebruikers kunnen zich registreren voor een account terwijl de site in deze modus is. |
| [!UICONTROL Startup Page] | Winkelweergave | Wanneer de website op Privé wijze van de Verkoop is, bepaalt dit het plaatsen de pagina die tot de klant login verschijnt.<br />  <br />**`To login form`**- Gebruikers worden omgeleid naar het aanmeldingsformulier totdat ze zich aanmelden.<br />**`To landing page`** - Gebruikers worden omgeleid naar de hieronder opgegeven statische pagina totdat zij zich aanmelden.<br /> <br />**_Belangrijk!_**&#x200B;Zorg ervoor dat u een koppeling naar de aanmeldingspagina opneemt vanaf de opgegeven bestemmingspagina, zodat klanten zich kunnen aanmelden voor toegang tot de volledige site. |
| [!UICONTROL Landing Page] | Winkelweergave | Hiermee bepaalt u de eerste pagina die wordt weergegeven wanneer de website zich in de modus Privéverkoop bevindt. |
| [!UICONTROL HTTP Response] | Website | Bepaalt de reactie van HTTP die wordt verzonden wanneer de website wordt gesloten en een verbinding door zowel een kruipper, als een spin wordt geprobeerd.<br /> <br />**`503 Service unavailable`**- De pagina is niet beschikbaar, maar de spin moet de index niet bijwerken.<br />**`200 OK`** - De landingspagina is correct en moet door de spin worden beschouwd als de enige pagina op de site. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Website | Bepaalt als de gebieden op de _Login_ en _vergeten Vorm van het Wachtwoord_ automatisch van vorige ingangen worden gevuld. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![ Algemeen > de Informatie van de Opslag ](./assets/general-store-information.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [ Informatie van de Opslag ](../../getting-started/store-details.md) in de _Begonnen Gids_.

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Store Name] | Winkelweergave | De naam van de opslag die aan de archiefmening wordt geassocieerd. |
| [!UICONTROL Store Phone Number] | Winkelweergave | Het primaire telefoonnummer van de winkel (gekoppeld aan de winkelweergave) is open voor zakelijk gebruik. Bijvoorbeeld: ma - fri, 9-5, sat 9-middags PST |
| Land | Website | Het land van het bedrijf dat de website exploiteert. |
| [!UICONTROL Region/State] | Website | De regio of status van het bedrijf dat de website beheert. |
| [!UICONTROL ZIP/Postal Code] | Website | De postcode of postcode van het bedrijf dat de website exploiteert. |
| [!UICONTROL City] | Website | De locatie van de stad van het bedrijf dat de website beheert. |
| [!UICONTROL Street Address] | Website | De straat of het postadres van het bedrijf dat de website in werking stelt. |
| [!UICONTROL Street Address Line 2|] Website | De tweede regel van het adres van de zakenstraat, indien nodig. |
| [!UICONTROL VAT Number] | Website | Het BTW-nummer van de onderneming die eigenaar is van de installatie van Commerce, indien van toepassing. |
| [!UICONTROL Validate VAT Number] |  | Controleert het BTW-identificatienummer. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![ Algemeen > Enige-Opslagwijze ](./assets/general-single-store-mode.png)<!-- zoom -->

Voor meer informatie over het veranderen van deze montages, zie [ enig-opslagwijze ](../../getting-started/websites-stores-views.md#single-store-mode) in _Begonnen Gids_ krijgen.

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Algemeen | Wanneer toegelaten voor enig-opslaginstallaties, verbergt het vakje van het configuratiebereik en verwante gebiedslabels Opties: `Yes` / `No` <br/>**_Nota:_**&#x200B;de enig-opslagwijze wordt genegeerd voor opslag met meer dan één mening.<br/> Als u de modus Eén winkel inschakelt, worden alle specifieke gegevens van de catalogus en de productopslag gekopieerd van de standaardwinkelweergave naar het volledige weergavebereik van de winkel. De catalogus- en productgegevens worden alleen gekopieerd als de winkel slechts over één voorvertoning beschikt. Als de opslag één gehandicapte opslagmening en één toegelaten opslagvoorproef heeft zal het geen catalogus en productgegevens kopiëren.<br/> Als u de modus Eén winkel inschakelt, worden de specifieke configuratie-instellingen voor de opslag genegeerd voor gegevens die specifiek zijn voor de inhoud. In plaats daarvan, gebruikt het configuratiemontages die op het globale niveauwerkingsgebied worden bepaald om consistentie tussen Admin UI en opslag te verzekeren. |

{style="table-layout:auto"}

## [!UICONTROL Data Services]

![ Algemeen > de Diensten van Gegevens ](./assets/general-data-services.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Commerce Events Enabled] | Algemeen | Deze configuratie wordt uitgezet door gebrek als u een gezondheidszorgklant bent en de [&#128279;](https://experienceleague.adobe.com/nl/docs/commerce/data-connection/hipaa-readiness) uitbreiding van HIPAA  van de Diensten van Gegevens &lbrace;geïnstalleerd. Hierdoor worden gegevens over opslaggebeurtenissen die worden gebruikt door Live zoeken en productaanbevelingen niet meer vastgelegd. Dit komt doordat gebeurtenisgegevens voor storefront op de client worden gegenereerd. Om storefront gebeurtenisgegevens voor gebruik door het [ Levende Onderzoek ](https://experienceleague.adobe.com/nl/docs/commerce/live-search/overview) en de [ diensten van de Aanbevelingen van het Product ](https://experienceleague.adobe.com/nl/docs/commerce/product-recommendations/guide-overview) verder te vangen en te verzenden, plaatste **Gebeurtenissen van Commerce Toegelaten** aan `Yes`. |

{style="table-layout:auto"}
