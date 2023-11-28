---
title: Twee-factor authentificatie opstelling voor gebruikersrekeningen
description: Leer hoe u verificatie met twee factoren instelt tijdens de eerste aanmelding bij Admin en uw identiteit verifieert met behulp van een ondersteunde apparaat-app.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Twee-factor authentificatie opstelling voor gebruikersrekeningen

In deze instructies ziet u hoe u verificatie met twee factoren instelt tijdens uw eerste aanmelding bij Adobe Commerce of Magento Open Source en hoe u uw identiteit verifieert met de volgende apps en apparaten.

Voor volledige instructies, zie [Aanmelden bij beheerder](../getting-started/admin-signin.md).

>[!NOTE]
>
>Winkels die zijn ingeschakeld [!DNL Adobe Identity Management Services] (IMS)-verificatie heeft native Adobe Commerce en Magento Open Source 2FA uitgeschakeld. De gebruikers Admin die in hun instantie van de Handel met hun geloofsbrieven van de Adobe worden geregistreerd hoeven niet voor vele Admin taken opnieuw voor authentiek te verklaren. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service] (IMS) Overzicht van integratie](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Stap 1: Instellen [!DNL Google Authenticator]

1. Voer uw accountgegevens in en meld u aan bij de _Beheerder_. Er wordt een nieuw verificatiescherm weergegeven met een QR-code.

1. Open de **[!UICONTROL Google Authenticator]** op uw mobiele apparaat.

1. Klik op het plusteken ( **+** ) om een ingang toe te voegen en de rode doos met de QR code op te zetten met de camera op uw slimme telefoon af te tasten.

1. Wanneer uw telefoon de code QR erkent en een ingang toevoegt, ga die code van 6 cijfers in _Beheerder_ **[!UICONTROL Authenticator code]** veld.

1. Klik op **[!UICONTROL Confirm]**.

   ![QR-code Google Authenticator](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Stap 2: aanmelden met [!DNL Google Authenticator]

1. Voer uw accountgegevens in en meld u aan bij de Handel _Beheerder_.

   ![Google Authenticator - aanmelden](./assets/storefront-2fa-google-code.png){width="300"}

1. Openen [!DNL Google Authenticator] op uw mobiele apparaat.

1. Voer desgevraagd de 6-cijferige verificatiecode in.

1. Als u de verificatie wilt opslaan voor toekomstige aanmeldingen, selecteert u de optie **[!UICONTROL Trust this device, do not ask again]** selectievakje.

1. Klik op **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] biedt een gratis proefversie aan en brengt kosten in rekening op basis van het aantal gebruikers dat aan de account is gekoppeld. Volg hun [instructies voor het instellen van uw account en het downloaden van de app](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Stap 1: Instellen [!DNL Duo Security]

1. Voer uw accountgegevens in en meld u aan bij de _Beheerder_.

1. Wanneer de [!DNL Duo] De pagina van de opstelling verschijnt, klikt **[!UICONTROL Start setup]** en voer de volgende handelingen uit:

   ![Voorbeeld van storefront - Duo instellen](./assets/storefront-2fa-duo-user1.png){width="300"}

1. Selecteer het apparaat.

1. Voer uw telefoonnummer in en klik op **[!UICONTROL Continue]**.

   In dit voorbeeld wordt om uw telefoonnummer gevraagd, omdat we een mobiel apparaat gebruiken.

1. Wanneer wordt gevraagd om te installeren [!DNL Duo Mobile] voor uw telefoontype, klik **[!UICONTROL I have Duo Mobile]**.

1. Openen [!DNL Duo Mobile] en scan de QR-code om de authenticator te synchroniseren met Adobe Commerce. Wanneer de activering is voltooid, wordt een vinkje weergegeven.

1. Om uw montages voor het apparaat te vormen, kies de actie die u wilt plaatsvinden wanneer u binnen ondertekent.

   - `Ask me to choose an authenticator method` — Hiermee kan de gebruiker selecteren bij het aanmelden en verifiëren in het dialoogvenster _Beheerder_.
   - `Automatically send this device a Duo Push` — Verstuurt een bericht naar het apparaat voor acceptatie of weigering van toegang.
   - `Automatically call this device` — Roept en verstrekt een wachtwoord om voor toegang in te gaan.

   ![Duo-verificaties](./assets/storefront-2fa-duo-user7.png){width="300"}

### Stap 2: aanmelden met [!DNL Duo Security]

In het volgende voorbeeld worden de opties getoond voor `Ask me to choose an authenticator method`:

1. Voer desgevraagd uw _Beheerder_ aanmeldingsgegevens.

   ![Duo - signin](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Kies de methode die u wilt gebruiken voor verificatie:

   - `Send Me a Push` — Klik om een pushbericht te ontvangen aan [!DNL Duo Mobile]. Accepteren voor verificatie.
   - `Call Me` — Klik deze optie, ontvang een vraag met een code, en ga de pascode in.
   - `Enter a Passcode` — Klik op deze optie om een voldoende-code te ontvangen en in te voeren.

1. Voltooi de push- of code om u volledig aan te melden bij de _Beheerder_.

## [!DNL Authy]

[!DNL Authy] biedt gebruikers gratis toegang tot hun app en service. Volg hun instructies om de app voor uw apparaat of browser te downloaden en in te stellen. Zie voor meer informatie de [[!DNL Authy] documentatie](https://authy.com/features/setup/).

### Stap 1: Auteur instellen

1. Voer uw accountgegevens in en meld u aan bij de _Beheerder_.

   ![[!DNL Authy] registratie](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Ga als volgt te werk wanneer u wordt gevraagd uzelf te registreren bij Auteur:

   - Selecteer uw land.

   - Voer uw telefoonnummer in.

   - Selecteer de **[!UICONTROL Verification method]**: `SMS` of `Call Me`

   Klik op **[!UICONTROL Continue]**. Een bericht wordt verzonden naar uw telefoon door de tekst van SMS of een vraag.

1. Voer de verificatiecode in die u ontvangt en klik op **[!UICONTROL Verify]**.

1. Klik op **[!UICONTROL Confirm]**.

   ![[!DNL Authy] verificatiecode](./assets/storefront-2fa-authy-verify.png){width="300"}

### Stap 2: aanmelden met [!DNL Authy]

1. Voer uw accountgegevens in en meld u aan bij de _Beheerder_.

   ![[!DNL Authy] - handtekening](./assets/storefront-2fa-authy-access.png){width="300"}

1. Kies een van de volgende methoden voor verificatie:

   - `Use one touch` — Verstuurt een waarschuwing naar uw [!DNL Authy] app. Accepteer de toegang in de app.
   - `Use authy token` — Vragen om een code in te voeren vanuit uw [!DNL Authy] app.

1. Als u zich niet kunt aanmelden, kiest u de methode die u wilt gebruiken om de code te ontvangen. Voer vervolgens de code in die u ontvangt voor toegang tot de _Beheerder_.

   De app bevat deze aanvullende noodmethoden.

   - `Send me a code via SMS` — Er wordt een SMS-bericht naar het geconfigureerde mobiele apparaat verzonden.
   - `Send me a code via phone call` — De gebruiker ontvangt een telefoongesprek met een code.

   Uw account is geverifieerd en wordt geopend.

## U2F ([!DNL Yubikey] en andere apparaten)

Volg de instructies van de leverancier van de oplossing om uw U2F apparaat te vormen. Raadpleeg de documentatie van de leverancier voor meer informatie, zoals [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) door [!UICONTROL Yubico].

1. Voer uw accountgegevens in en meld u aan bij de _Beheerder_.

   ![U2F-sleuteltoegang](./assets/storefront-2fa-u2f.png){width="300"}

1. Druk op de toets.

   Verificatie activeert en opent de _Beheerder_.

1. Voeg de **[!UICONTROL U2F key]** naar een USB-poort op uw computer.
