---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Security] &gt; [!UICONTROL Security.txt] van Commerce Admin.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Voor meer informatie over het veranderen van deze configuratiemontages, zie [ kwestie van de Veiligheid die ](../../systems/security-issue-reporting.md) meldt.

{{config}}

## [!UICONTROL General]

![ Algemeen ](./assets/txt-general.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable] | Website | Als deze optie is ingeschakeld, wordt een `security.txt` -bestand opgeslagen dat informatie bevat die beveiligingsonderzoekers nodig hebben om potentiële kwetsbaarheden aan u te melden. Opties:<br />**`Yes`**- creeert het `security.txt` dossier dat op informatie wordt gebaseerd in de _informatie van het Contact_ wordt ingegaan en _Andere informatie_ secties.<br />**`No`** - (standaardwaarde) Maakt het `security.txt` -bestand niet. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![ de informatie van het Contact ](./assets/txt-contact-info.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email] | Website | Het e-mailadres waar beveiligingsrapporten kunnen worden verzonden. |
| [!UICONTROL Phone] | Website | Een telefoonnummer dat kan worden gebruikt om beveiligingsproblemen te melden. |
| [!UICONTROL Contact Page] | Website | URL van een pagina op uw plaats die van veiligheidscontacten, of uw _pagina van het Contact van ons_ een lijst maakt. Voorbeelden: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![ Andere informatie ](./assets/txt-other-info.png)<!-- zoom -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Encryption] | Website | Een URL die wijst naar de locatie van een coderingssleutel die beveiligingsonderzoekers kunnen gebruiken om gecodeerde communicatie te verzenden. _**ga niet de encryptiesleutel op dit gebied in.**_ <br/><br/> Het is de verantwoordelijkheid van de onderzoeker om te verifiëren dat de sleutel van een betrouwbare bron is. Onderzoekers mogen er niet van uitgaan dat de sleutel gelijk is aan de sleutel waarmee de digitale handtekening is gegenereerd. Voorbeeld:<br /> OpenPGP sleutel van Webserver - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Website | Een URL die naar een pagina in uw opslag wijst waar de veiligheidsonderzoekers, zoals `https://mystore.com/hall-of-fame.html` worden erkend. Als u toekomstige aanvallen wilt voorkomen, neemt u alleen een algemene beschrijving op zonder specifieke informatie over kwetsbaarheidsproblemen te onthullen. Voorbeeld:<br /> wij zouden de volgende onderzoekers willen bedanken:<br /> (yyyy/mm/dd) Justin Thyme - SQL injectie |
| [!UICONTROL Preferred Languages] | Website | Geeft minstens één voorkeurstaal voor beveiligingsrapporten op. Scheid veelvoudige twee karakter [ taalcodes ](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) met een komma. Alle opgegeven talen hebben dezelfde prioriteit. Als u bijvoorbeeld Engels, Spaans en Frans wilt opgeven, voert u `en, es, fr` in. |
| [!UICONTROL Hiring] | Website | De URL van een pagina op de site die een lijst bevat met beveiliginggerelateerde taakposities. Voorbeeld: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Website | De URL van de pagina die uw beveiligingsbeleid en praktijken voor het melden van kwetsbaarheden beschrijft. Voorbeeld: `https://mystore.com/security-reporting.html` Default: `https://mystore.com/security` |
| [!UICONTROL Signature] | Website | Een koppeling naar het digitale handtekeningbestand. De digitale handtekening moet worden gegenereerd via de opdrachtregel en wordt opgeslagen in de map `.well-known` op de server. Voor meer informatie, zie [ Security.txt ](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) op GitHub. Voorbeeld: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
