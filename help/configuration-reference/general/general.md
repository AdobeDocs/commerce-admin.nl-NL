---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL General] &gt; [!UICONTROL General] pagina van de Commerce Admin.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Zie [Landopties](../../getting-started/store-details.md#country-options) voor meer informatie over deze configuratiegebieden en opties.

![Algemeen > Landopties](./assets/general-country-options.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Default Country] | Winkelweergave | Het land waar je winkel zich bevindt. |
| [!UICONTROL Allow Countries] | Website | De landen waar je bestellingen accepteert. |
| [!UICONTROL Zip/Postal Code is Optional for] | Algemeen | Landen die geen postcode of postcode in het verzendadres nodig hebben. |
| [!UICONTROL European Union Countries] | Algemeen | Landen die lid zijn van de Europese Unie. |
| [!UICONTROL Top Destinations] | Winkelweergave | De primaire landen die u voor verkoop aanspreekt. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

Zie [Statusopties](../../getting-started/store-details.md#state-options) voor meer informatie over deze configuratiegebieden en opties.

![Algemeen > Statusopties](./assets/general-state-options.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL State is required for] | Algemeen | De landen (waar u zaken doet) die een regio of een staat vereisen om in het postadres worden omvat. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Algemeen | Voor landen waar dit niet vereist is, bepaalt u of de _Regio/staat_ wordt vermeld in het postadres van de klant.<br /> <br />**`Yes`**- Inclusief de _Regio/staat_ in het adres van de klant, zelfs als dit niet door het land wordt vereist.<br />**`No`** - Laat het gebied/van de Staat van het klantenadres weg als niet vereist door het land. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

Zie [Landinstellingen](../../getting-started/store-details.md#locale-options) voor meer informatie over deze configuratiegebieden en opties.

![Algemeen > Opties voor landinstelling](./assets/general-locale-options.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Timezone] | Website | De tijdzone van de primaire markt die door de website wordt bediend. Meestal is de tijdzone hetzelfde als de tijdzone die wordt gebruikt op de fysieke locatie van uw bedrijf. |
| [!UICONTROL Locale] | Winkelweergave | De taal, de valuta, en het systeem van meting die in de markt wordt gebruikt die door de archiefmening wordt gediend. |
| [!UICONTROL Weight Unit] | Winkelweergave | De maateenheid die doorgaans wordt gebruikt voor overbrengingen vanuit de landinstelling. Opties: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Winkelweergave | De dag die wordt beschouwd als de eerste dag van de week op de markt die door de winkelweergave wordt bediend. |
| [!UICONTROL Weekend Days] | Winkelweergave | De dagen die op het weekend in de markt vallen door de winkelmening worden gediend. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![Algemeen > Websitebeperkingen](./assets/general-website-restrictions.png)<!-- zoom -->

Zie voor meer informatie over het wijzigen van deze instellingen [Toegangsbeperkingen](../../merchandising-promotions/event-configure.md#access-restrictions) in de _Handleiding Handelsbemiddeling en speciale acties_.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Website | Hiermee bepaalt u of de website wordt uitgevoerd in de beperkte modus.<br /> <br />**`Yes`**- Toegang tot websites wordt beperkt op de manier die in de onderstaande velden is ingesteld.<br />**`No`** - Beperkingen zijn uitgeschakeld en de volgende instellingen hebben geen effect. |
| [!UICONTROL Restriction Mode] | Website | Bepaalt het type toegangsbeperking dat van toepassing is op de website.<br /> <br />**`Website Closed`**- Alle toegang tot de storefront is beperkt, en opslag URLs wordt tijdelijk opnieuw gericht aan de landende pagina. Deze instelling kan handig zijn tijdens het onderhoud van de site of voordat u de toepassing start.<br />**`Private Sales: Login Only`** - Alleen geregistreerde klanten kunnen zich aanmelden om toegang te krijgen tot de winkel. Alle URL&#39;s van de winkel worden tijdelijk omgeleid naar de opgegeven bestemmingspagina of het opgegeven aanmeldingsformulier. Gebruikers kunnen in deze modus geen account maken.<br />**`Private Sales: Login and Register`**- Gebruikers moeten zich aanmelden om toegang te krijgen tot de winkel. Alle URL&#39;s van de winkel worden tijdelijk doorgestuurd naar het aanmeldingsformulier totdat de gebruiker zich aanmeldt. Gebruikers kunnen zich registreren voor een account terwijl de site in deze modus is. |
| [!UICONTROL Startup Page] | Winkelweergave | Wanneer de website zich in de modus Privéverkoop bevindt, bepaalt deze instelling de pagina die wordt weergegeven totdat de klant zich aanmeldt.<br />  <br />**`To login form`**- Gebruikers worden omgeleid naar het aanmeldingsformulier totdat zij zich aanmelden.<br />**`To landing page`** - Gebruikers worden omgeleid naar de hieronder opgegeven statische pagina totdat ze zich aanmelden.<br /> <br />**_Belangrijk!_**Zorg ervoor dat u een koppeling naar de aanmeldingspagina opneemt vanaf de opgegeven bestemmingspagina, zodat klanten zich kunnen aanmelden voor toegang tot de volledige site. |
| [!UICONTROL Landing Page] | Winkelweergave | Hiermee bepaalt u de eerste pagina die wordt weergegeven wanneer de website zich in de modus Privéverkoop bevindt. |
| [!UICONTROL HTTP Response] | Website | Hiermee bepaalt u de HTTP-reactie die wordt verzonden wanneer de website wordt gesloten en een verbinding wordt geprobeerd door een bot, crawler of spin.<br /> <br />**`503 Service unavailable`**- De pagina is niet beschikbaar, maar de spin moet de index niet bijwerken.<br />**`200 OK`** - De landingspagina is correct en moet door de spin worden beschouwd als de enige pagina op de site. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Website | Hiermee bepaalt u of de velden op het tabblad _Aanmelden_ en _Wachtwoord vergeten_ formulieren worden automatisch ingevuld van vorige vermeldingen. Opties: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![Algemeen > Opslaggegevens](./assets/general-store-information.png)<!-- zoom -->

Zie voor meer informatie over het wijzigen van deze instellingen [Opslaggegevens](../../getting-started/store-details.md) in de _Aan de slag_.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Store Name] | Winkelweergave | De naam van de opslag die aan de archiefmening wordt geassocieerd. |
| [!UICONTROL Store Phone Number] | Winkelweergave | Het primaire telefoonnummer van de winkel (gekoppeld aan de winkelweergave) is open voor zakelijk gebruik. Bijvoorbeeld: ma - fri, 9-5, sat 9-middags PST |
| Land | Website | Het land van het bedrijf dat de website exploiteert. |
| [!UICONTROL Region/State] | Website | De regio of status van het bedrijf dat de website beheert. |
| [!UICONTROL ZIP/Postal Code] | Website | De postcode of postcode van het bedrijf dat de website exploiteert. |
| [!UICONTROL City] | Website | De locatie van de stad van het bedrijf dat de website beheert. |
| [!UICONTROL Street Address] | Website | De straat of het postadres van het bedrijf dat de website in werking stelt. |
| [!UICONTROL Street Address Line 2|]Website | De tweede regel van het adres van de zakenstraat, indien nodig. |
| [!UICONTROL VAT Number] | Website | Het btw-nummer van de onderneming die eigenaar is van de installatie van de handel, indien van toepassing. |
| [!UICONTROL Validate VAT Number] |  | Controleert het BTW-identificatienummer. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![Algemeen > Single-Store-modus](./assets/general-single-store-mode.png)<!-- zoom -->

Zie voor meer informatie over het wijzigen van deze instellingen [Single-store, modus](../../getting-started/websites-stores-views.md#single-store-mode) in de _Aan de slag_.

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Algemeen | Wanneer toegelaten voor enig-opslaginstallaties, verbergt het vakje van het configuratiebereik en verwante gebiedslabels Opties: `Yes` / `No` <br/>**_Opmerking:_**De modus Eén opslag wordt genegeerd voor winkels met meerdere weergaven. |

{style="table-layout:auto"}
