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

Een CAPTCHA is een visueel apparaat dat ervoor zorgt dat een mens, in plaats van een computer (of &#39;bot&#39;), communiceert met de site. CAPTCHA is een acroniem voor _Volledig geautomatiseerde openbare trainingstest om computers en mensen te informeren_. Het kan voor zowel toegang Admin als diverse storefront acties worden gebruikt die door geregistreerde klanten in werking worden gesteld. Adobe Commerce en Magento Open Source ondersteunen de standaard CAPTCHA die in dit onderwerp wordt beschreven en [Google reCAPTCHA](security-google-recaptcha.md).

U kunt de CAPTCHA zo vaak opnieuw laden als nodig is door op het pictogram Opnieuw laden in de rechterbovenhoek van de afbeelding te klikken. CAPTCHA is volledig configureerbaar en kan elke keer, of slechts na een bepaald aantal ontbroken login pogingen worden geplaatst.

![Aanmelden met CAPTCHA](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## CAPTCHA voor de beheerder configureren

Voor een extra beveiligingsniveau kunt u een CAPTCHA toevoegen aan de pagina Aanmelden bij beheerder en Wachtwoord vergeten. Gebruikers van Admin kunnen de weergegeven CAPTCHA opnieuw laden door op de knop _Opnieuw laden_ ![pictogram voor opnieuw laden](./assets/CAPTCHA-icon-reload.png) in de rechterbovenhoek van de afbeelding. Het aantal opnieuw laden is onbeperkt.

![Admin - Aanmelden met CAPTCHA](./assets/security-captcha-admin.png){width="300"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL Admin]**.

1. In de rechterbovenhoek stelt u **[!UICONTROL Store View]** tot `Default`.

   Als de [bereik](../getting-started/websites-stores-views.md#scope-settings) Kies de websites waarop u de CAPTCHA-configuratie wilt toepassen als uw Commerce-installatie meerdere websites bevat.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL CAPTCHA]** sectie.

1. Set **[!UICONTROL Enable CAPTCHA in Admin]** tot `Yes`. Voer vervolgens de resterende opties als volgt uit:

   ![Admin - CAPTCHA-configuratie](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Voer de naam in van de **[!UICONTROL Font]** te gebruiken voor CAPTCHA-symbolen (standaard: `LinLibertine`).

     Als u uw eigen lettertype wilt toevoegen, moet het lettertypebestand zich in dezelfde map bevinden als de Commerce-installatie en moet het worden gedeclareerd in het dialoogvenster `config.xml` bestand van de module Captcha op `app/code/Magento/Captcha/etc`.

   - Selecteer een van de volgende opties **[!UICONTROL Forms]** waar de CAPTCHA moet worden gebruikt. Houd Ctrl (PC) of Command (Mac) ingedrukt om meerdere formulieren te kiezen.

      - `Admin Login`
      - `Admin Forgot Password`

   - Set **[!UICONTROL Displaying Modes]** op een van de volgende wijzen:

      - `Always` — CAPTCHA is altijd vereist om u aan te melden bij de beheerder.
      - `After number of attempts to login` — Deze optie is alleen van toepassing op het aanmeldingsformulier voor beheerders. Als deze optie is geselecteerd, wordt _[!UICONTROL Number of Unsuccessful Attempts to Login]_wordt weergegeven. Voer het aantal aanmeldpogingen in dat u wilt toestaan. De waarde 0 (nul) komt overeen met het instellen van de weergavemodus op `Always`.

     Om het aantal mislukte aanmeldingspogingen bij te houden, wordt elke poging tot aanmelding onder één e-mailadres en van één IP-adres geteld. Het maximumaantal login pogingen die van het zelfde IP-adres worden toegestaan is 1.000. Deze beperking is alleen van toepassing wanneer CAPTCHA is ingeschakeld.

   - Voor **[!UICONTROL Number of Unsuccessful Attempts to Login]** Voer het aantal keren in dat de beheerder zich kan aanmelden voordat de CAPTCHA wordt weergegeven. Indien ingesteld op nul (`0`), is CAPTCHA altijd vereist.

   - Voor **[!UICONTROL CAPTCHA Timeout (minutes)]** Voer het aantal minuten in voordat de CAPTCHA verloopt. Wanneer de CAPTCHA verloopt, moet de beheerder de pagina opnieuw laden.

   - Voer de **[!UICONTROL Number of Symbols]** in de CAPTCHA. Maximaal acht (`8`) kunnen worden gebruikt. Voor een variabel aantal symbolen dat met elke CAPTCHA verandert, ga een waaier (zoals `5-8`).

   - Voor **[!UICONTROL Symbols Used in CAPTCHA]** Voer de letters (a-z en A-Z) en de cijfers (0-9) in die u willekeurig wilt weergeven in de CAPTCHA. Symbolen die moeilijk te onderscheiden zijn van andere symbolen, zoals `i`, `l`, of `1`, zijn niet opgenomen in de standaardset met CAPTCHA-symbolen.

   - Set **[!UICONTROL Case Sensitive]** tot `Yes` als u wilt dat beheerders de tekens in hoofdletters of kleine letters precies zo moeten invoeren als in de CAPTCHA wordt getoond.

1. Klik op **[!UICONTROL Save Config]**.

## CAPTCHA voor de storefront configureren

Klanten kunnen worden verplicht om een CAPTCHA in te voeren telkens wanneer zij zich aanmelden bij hun accounts of na verschillende mislukte aanmeldingspogingen. Bovendien kunnen vele vormen die door de storefront worden gebruikt worden gevormd om controle door CAPTCHA te vereisen.

![CAPTCHA tijdens uitchecken](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL CAPTCHA]** sectie.

![CAPTCHA-configuratie van klant](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable CAPTCHA on Storefront]** tot `Yes`. Voer vervolgens de resterende opties als volgt uit:

   - Voer de naam in van de **[!UICONTROL Font]** te gebruiken voor de CAPTCHA-symbolen (standaard: `LinLibertine`).

     Als u uw eigen lettertype wilt toevoegen, moet het lettertypebestand zich in dezelfde map bevinden als de Commerce-installatie en moet het worden gedeclareerd in het dialoogvenster `config.xml` bestand van de CAPTCHA-module.

   - Selecteer een van de volgende opties **[!UICONTROL Forms]** waar de CAPTCHA moet worden gebruikt. Houd Ctrl (PC) of Command (Mac) ingedrukt om meerdere formulieren te kiezen.

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (zie [beveiligingspatroon](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _Kennisbank_ artikel)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (alleen Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce)
      - `Create company` ![Adobe Commerce B2B](../assets/b2b.svg) (Alleen beschikbaar bij Adobe Commerce B2B)

   - Set **[!UICONTROL Displaying Mode]** op een van de volgende wijzen:

      - `Always` — CAPTCHA is altijd vereist voor toegang tot de geselecteerde formulieren.
      - `After number of attempts to login` — Voer het aantal aanmeldpogingen in voordat de CAPTCHA wordt weergegeven. De waarde 0 (nul) komt overeen met de waarde Altijd. Als deze optie is geselecteerd, wordt het aantal mislukte aanmeldingspogingen weergegeven. Deze optie is niet van toepassing op het formulier Wachtwoord vergeten, dat, indien ingeschakeld, altijd de CAPTCHA weergeeft.

   - Voor **[!UICONTROL Number of Unsuccessful Attempts to Login]** Voer het aantal keren in dat een klant zich zonder succes kan aanmelden voordat de CAPTCHA wordt weergegeven. Indien ingesteld op nul (`0`), wordt CAPTCHA altijd gebruikt.

   - Voor **[!UICONTROL CAPTCHA Timeout (minutes)]** Voer het aantal minuten in voordat de CAPTCHA verloopt. Wanneer de CAPTCHA verloopt, moet de klant de pagina opnieuw laden om een nieuwe CAPTCHA te produceren.

   - Voer de **[!UICONTROL Number of Symbols]** in de CAPTCHA. Maximaal acht (`8`) kunnen worden gebruikt. Voor een variabel aantal symbolen dat met elke CAPTCHA verandert, ga een waaier (zoals `5-8`).

   - Voor **[!UICONTROL Symbols Used in CAPTCHA]** Voer de letters (a-z en A-Z) en de cijfers (0-9) in die u willekeurig wilt weergeven in de CAPTCHA. De standaardset met tekens bevat geen vergelijkbare symbolen, zoals `I` of `1`. U bereikt de beste resultaten met symbolen die gebruikers gemakkelijk kunnen herkennen.

   - Set **[!UICONTROL Case Sensitive]** tot `Yes` als u wilt dat klanten de tekens in hoofdletters of kleine letters precies zo invoeren als in de CAPTCHA wordt getoond.

1. Klik op **[!UICONTROL Save Config]**.
