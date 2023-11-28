---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Security] &gt; [!UICONTROL Security.txt] pagina van de Commerce Admin.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Voor meer informatie over het veranderen van deze configuratiemontages, zie [Melding van beveiligingsproblemen](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Algemeen](./assets/txt-general.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable] | Website | Indien ingeschakeld, wordt een `security.txt` bestand wordt opgeslagen dat informatie bevat die beveiligingsonderzoekers nodig hebben om potentiële kwetsbaarheden aan u te melden. Opties:<br />**`Yes`**- Creeert `security.txt` bestand op basis van informatie die is ingevoerd in het _Contactgegevens_ en _Overige informatie_ secties.<br />**`No`** - (standaard) Er wordt geen `security.txt` bestand. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Contact information]

![Contactgegevens](./assets/txt-contact-info.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email] | Website | Het e-mailadres waar beveiligingsrapporten kunnen worden verzonden. |
| [!UICONTROL Phone] | Website | Een telefoonnummer dat kan worden gebruikt om beveiligingsproblemen te melden. |
| [!UICONTROL Contact Page] | Website | De URL van een pagina op uw site die beveiligingscontactpersonen bevat, of uw _Contact opnemen_ pagina. Voorbeelden: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Other information]

![Overige informatie](./assets/txt-other-info.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Encryption] | Website | Een URL die wijst naar de locatie van een coderingssleutel die beveiligingsonderzoekers kunnen gebruiken om gecodeerde communicatie te verzenden. _**Voer in dit veld geen coderingssleutel in.**_ <br/><br/>Het is de verantwoordelijkheid van de onderzoeker om te controleren of de sleutel uit een betrouwbare bron afkomstig is. Onderzoekers mogen er niet van uitgaan dat de sleutel gelijk is aan de sleutel waarmee de digitale handtekening is gegenereerd. Voorbeeld:<br />OpenPGP-sleutel van webserver - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Website | Een URL die verwijst naar een pagina in uw winkel waar beveiligingsonderzoekers worden erkend, zoals`https://mystore.com/hall-of-fame.html`. Als u toekomstige aanvallen wilt voorkomen, neemt u alleen een algemene beschrijving op zonder specifieke informatie over kwetsbaarheidsproblemen te onthullen. Voorbeeld:<br />Wij willen de volgende onderzoekers bedanken:<br />(jjjj/mm/dd) Justin Thyme - SQL-injectie |
| [!UICONTROL Preferred Languages] | Website | Geeft minstens één voorkeurstaal voor beveiligingsrapporten op. Meerdere tekens scheiden [taalcodes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) met een komma. Alle opgegeven talen hebben dezelfde prioriteit. Als u bijvoorbeeld Engels, Spaans en Frans wilt opgeven, voert u `en, es, fr`. |
| [!UICONTROL Hiring] | Website | De URL van een pagina op de site die een lijst bevat met beveiliginggerelateerde taakposities. Voorbeeld: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Website | De URL van de pagina die uw beveiligingsbeleid en praktijken voor het melden van kwetsbaarheden beschrijft. Voorbeeld: `https://mystore.com/security-reporting.html` Standaard: `https://mystore.com/security` |
| [!UICONTROL Signature] | Website | Een koppeling naar het digitale handtekeningbestand. De digitale handtekening moet worden gegenereerd via de opdrachtregel en wordt opgeslagen in de `.well-known` op de server. Zie voor meer informatie [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) op GitHub. Voorbeeld: `https://mystore.com/.well-known/security.txt.sig` |

{:style=&quot;table-layout:auto&quot;}
