---
title: CAPTCHA
description: Leer hoe u CAPTCHA configureert voor beheerdersrechten en verschillende storefront-acties die door geregistreerde klanten worden geïnitieerd.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# CAPTCHA

Een CAPTCHA is een visueel apparaat dat ervoor zorgt dat een mens, in plaats van een computer (of &#39;bot&#39;), communiceert met de site. CAPTCHA is een acroniem voor _volledig Geautomatiseerde Openbare Turing test om Computers en Humans te vertellen over_. Het kan voor zowel toegang Admin als diverse storefront acties worden gebruikt die door geregistreerde klanten in werking worden gesteld. Adobe Commerce en de Magento Open Source steunen standaardCAPTCHA die in dit onderwerp en [ Google reCAPTCHA ](security-google-recaptcha.md) wordt beschreven.

U kunt de CAPTCHA zo vaak opnieuw laden als nodig is door op het pictogram Opnieuw laden in de rechterbovenhoek van de afbeelding te klikken. CAPTCHA is volledig configureerbaar en kan elke keer, of slechts na een bepaald aantal ontbroken login pogingen worden geplaatst.

![ Login met CAPTCHA ](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## CAPTCHA voor de beheerder configureren

Voor een extra beveiligingsniveau kunt u een CAPTCHA toevoegen aan de pagina Aanmelden bij beheerder en Wachtwoord vergeten. De gebruikers van Admin kunnen de getoonde CAPTCHA opnieuw laden door _te klikken herlaadt_ ![ pictogram opnieuw laden ](./assets/CAPTCHA-icon-reload.png) in de hoger-juiste hoek van het beeld. Het aantal opnieuw laden is onbeperkt.

![ Admin - Teken binnen met CAPTCHA ](./assets/security-captcha-admin.png){width="300"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Admin]** .

1. Stel in de rechterbovenhoek **[!UICONTROL Store View]** in op `Default` .

   Als het [ werkingsgebied ](../getting-started/websites-stores-views.md#scope-settings) van uw installatie van Commerce veelvoudige websites omvat, kies de websites waar u de configuratie CAPTCHA wilt toepassen.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL CAPTCHA]** sectie uit.

1. Stel **[!UICONTROL Enable CAPTCHA in Admin]** in op `Yes` . Voer vervolgens de resterende opties als volgt uit:

   ![ Admin - configuratie CAPTCHA ](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Voer de naam in van de **[!UICONTROL Font]** die voor CAPTCHA-symbolen moet worden gebruikt (standaard: `LinLibertine`).

     Als u uw eigen lettertype wilt toevoegen, moet het lettertypebestand zich in dezelfde map bevinden als de Commerce-installatie en moet het worden gedeclareerd in het `config.xml` -bestand van de Captcha-module op `app/code/Magento/Captcha/etc` .

   - Selecteer een van de volgende opties **[!UICONTROL Forms]** waar de CAPTCHA moet worden gebruikt. Houd Ctrl (PC) of Command (Mac) ingedrukt om meerdere formulieren te kiezen.

      - `Admin Login`
      - `Admin Forgot Password`

   - Stel **[!UICONTROL Displaying Modes]** in op een van de volgende opties:

      - `Always` — CAPTCHA is altijd vereist om u aan te melden bij de beheerder.
      - `After number of attempts to login` — Deze optie is alleen van toepassing op het aanmeldingsformulier voor beheerders. Als deze optie is geselecteerd, wordt het veld _[!UICONTROL Number of Unsuccessful Attempts to Login]_weergegeven. Voer het aantal aanmeldpogingen in dat u wilt toestaan. De waarde 0 (nul) komt overeen met het instellen van de weergavemodus op `Always` .

     Om het aantal mislukte aanmeldingspogingen bij te houden, wordt elke poging tot aanmelding onder één e-mailadres en van één IP-adres geteld. Het maximumaantal login pogingen die van het zelfde IP-adres worden toegestaan is 1.000. Deze beperking is alleen van toepassing wanneer CAPTCHA is ingeschakeld.

   - Voer bij **[!UICONTROL Number of Unsuccessful Attempts to Login]** het aantal keren in dat de beheerder zich kan aanmelden voordat de CAPTCHA wordt weergegeven. Indien ingesteld op nul (`0`), is CAPTCHA altijd vereist.

   - Voer bij **[!UICONTROL CAPTCHA Timeout (minutes)]** het aantal minuten in voordat de CAPTCHA verloopt. Wanneer de CAPTCHA verloopt, moet de beheerder de pagina opnieuw laden.

   - Voer de **[!UICONTROL Number of Symbols]** in die u in de CAPTCHA wilt weergeven. U kunt maximaal acht (`8`) symbolen gebruiken. Voor een variabel aantal symbolen dat met elke CAPTCHA verandert, ga een waaier (zoals `5-8`) in.

   - Voer bij **[!UICONTROL Symbols Used in CAPTCHA]** de letters (a-z en A-Z) en de cijfers (0-9) in die u willekeurig in de CAPTCHA wilt weergeven. Symbolen die moeilijk te onderscheiden zijn van andere symbolen, zoals `i` , `l` of `1` , worden niet opgenomen in de standaardset met CAPTCHA-symbolen.

   - Stel **[!UICONTROL Case Sensitive]** in op `Yes` als u wilt dat beheerders de tekens in hoofdletters of kleine letters precies zo moeten invoeren als in de CAPTCHA wordt getoond.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## CAPTCHA voor de storefront configureren

Klanten kunnen worden verplicht om een CAPTCHA in te voeren telkens wanneer zij zich aanmelden bij hun accounts of na verschillende mislukte aanmeldingspogingen. Bovendien kunnen vele vormen die door de storefront worden gebruikt worden gevormd om controle door CAPTCHA te vereisen.

![ CAPTCHA tijdens controle ](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL CAPTCHA]** sectie uit.

![ KLANT CAPTCHA configuratie ](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable CAPTCHA on Storefront]** in op `Yes` . Voer vervolgens de resterende opties als volgt uit:

   - Voer de naam in van de **[!UICONTROL Font]** die voor de CAPTCHA-symbolen moet worden gebruikt (standaard: `LinLibertine`).

     Als u uw eigen lettertype wilt toevoegen, moet het lettertypebestand zich in dezelfde map bevinden als de Commerce-installatie en moet het worden gedeclareerd in het `config.xml` -bestand van de CAPTCHA-module.

   - Selecteer een van de volgende opties **[!UICONTROL Forms]** waar de CAPTCHA moet worden gebruikt. Houd Ctrl (PC) of Command (Mac) ingedrukt om meerdere formulieren te kiezen.

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (zie [ veiligheidspatch ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _artikel van de Kennisbank_)
      - `Send to Friend Form` ![ Magento Open Source ](../assets/open-source.svg) (Magento Open Source slechts)
      - `Add Gift Card Code` ![ Adobe Commerce ](../assets/adobe-logo.svg) (slechts Adobe Commerce)
      - `Create company` ![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B slechts)

   - Stel **[!UICONTROL Displaying Mode]** in op een van de volgende opties:

      - `Always` — CAPTCHA is altijd vereist voor toegang tot de geselecteerde formulieren.
      - `After number of attempts to login` — Voer het aantal aanmeldpogingen in voordat de CAPTCHA wordt weergegeven. De waarde 0 (nul) komt overeen met de waarde Altijd. Als deze optie is geselecteerd, wordt het aantal mislukte aanmeldingspogingen weergegeven. Deze optie is niet van toepassing op het formulier Wachtwoord vergeten, dat, indien ingeschakeld, altijd de CAPTCHA weergeeft.

   - Voer bij **[!UICONTROL Number of Unsuccessful Attempts to Login]** het aantal keren in dat een klant zich zonder succes kan aanmelden voordat de CAPTCHA wordt weergegeven. Indien ingesteld op nul (`0`), wordt CAPTCHA altijd gebruikt.

   - Voer bij **[!UICONTROL CAPTCHA Timeout (minutes)]** het aantal minuten in voordat de CAPTCHA verloopt. Wanneer de CAPTCHA verloopt, moet de klant de pagina opnieuw laden om een nieuwe CAPTCHA te produceren.

   - Voer de **[!UICONTROL Number of Symbols]** in die u in de CAPTCHA wilt weergeven. U kunt maximaal acht (`8`) symbolen gebruiken. Voor een variabel aantal symbolen dat met elke CAPTCHA verandert, ga een waaier (zoals `5-8`) in.

   - Voer bij **[!UICONTROL Symbols Used in CAPTCHA]** de letters (a-z en A-Z) en de cijfers (0-9) in die u willekeurig in de CAPTCHA wilt weergeven. De standaardset met tekens bevat geen vergelijkbare symbolen, zoals `I` of `1` . U bereikt de beste resultaten met symbolen die gebruikers gemakkelijk kunnen herkennen.

   - Stel **[!UICONTROL Case Sensitive]** in op `Yes` als u wilt dat klanten de tekens in hoofdletters of kleine letters precies zo moeten invoeren als in de CAPTCHA wordt getoond.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
