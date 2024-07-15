---
title: Twee-factor authentificatie opstelling voor gebruikersrekeningen
description: Leer hoe u verificatie met twee factoren instelt tijdens de eerste aanmelding bij Admin en uw identiteit verifieert met behulp van een ondersteunde apparaat-app.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Twee-factor authentificatie opstelling voor gebruikersrekeningen

In deze instructies ziet u hoe u verificatie met twee factoren instelt tijdens uw eerste aanmelding bij Adobe Commerce of Magento Open Source en hoe u uw identiteit verifieert met de volgende apps en apparaten.

Voor volledige instructies, zie [ binnen Teken Admin ](../getting-started/admin-signin.md).

>[!NOTE]
>
>Voor opslagruimten waarvoor verificatie met [!DNL Adobe Identity Management Services] (IMS) is ingeschakeld, zijn Adobe Commerce en Magento Open Source 2FA uitgeschakeld. Admin-gebruikers die zich bij hun Commerce-instantie hebben aangemeld met hun aanmeldingsgegevens voor de Adobe, hoeven niet opnieuw te worden geverifieerd voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service]  (IMS) Overzicht van de Integratie ](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Stap 1: Instellen [!DNL Google Authenticator]

1. Ga uw rekeningsgeloofsbrieven in en meld binnen aan _Admin_. Er wordt een nieuw verificatiescherm weergegeven met een QR-code.

1. Open de app **[!UICONTROL Google Authenticator]** op uw mobiele apparaat.

1. Klik op het plusteken ( **+** ) om een item toe te voegen en het rode vak in te stellen met de QR-code die u met de camera op uw smartphone wilt scannen.

1. Wanneer uw telefoon de QR code erkent en een ingang toevoegt, ga die code van 6 cijfers op het _Admin_ **[!UICONTROL Authenticator code]** gebied in.

1. Klik op **[!UICONTROL Confirm]** als de bewerking is voltooid.

   ![ QR van de Authenticator van Google code ](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Stap 2: Aanmelden met [!DNL Google Authenticator]

1. Ga uw rekeningsgeloofsbrieven in en meld binnen aan Commerce _Admin_.

   ![ de Authenticator van Google - teken ](./assets/storefront-2fa-google-code.png){width="300"}

1. Open [!DNL Google Authenticator] op uw mobiele apparaat.

1. Voer desgevraagd de 6-cijferige verificatiecode in.

1. Schakel het selectievakje **[!UICONTROL Trust this device, do not ask again]** in om de verificatie voor toekomstige aanmeldingen op te slaan.

1. Klik op **[!UICONTROL Confirm]** als de bewerking is voltooid.

## [!DNL Duo Security]

[!DNL Duo] biedt een gratis proefversie aan en brengt kosten in rekening op basis van het aantal gebruikers dat aan het account is gekoppeld. Volg hun [ instructies aan opstelling uw rekening en download app ](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Stap 1: Instellen [!DNL Duo Security]

1. Ga uw rekeningsgeloofsbrieven in en meld binnen aan _Admin_.

1. Wanneer de pagina [!DNL Duo] Setup wordt weergegeven, klikt u op **[!UICONTROL Start setup]** en voert u de volgende handelingen uit:

   ![ storefront van het Voorbeeld - duo opstelling ](./assets/storefront-2fa-duo-user1.png){width="300"}

1. Selecteer het apparaat.

1. Voer desgevraagd uw telefoonnummer in en klik op **[!UICONTROL Continue]** .

   In dit voorbeeld wordt om uw telefoonnummer gevraagd, omdat we een mobiel apparaat gebruiken.

1. Klik op **[!UICONTROL I have Duo Mobile]** wanneer u wordt gevraagd om [!DNL Duo Mobile] voor uw type telefoon te installeren.

1. Open [!DNL Duo Mobile] en scan de QR-code om de authenticator te synchroniseren met Adobe Commerce. Wanneer de activering is voltooid, wordt een vinkje weergegeven.

1. Om uw montages voor het apparaat te vormen, kies de actie die u wilt plaatsvinden wanneer u binnen ondertekent.

   - `Ask me to choose an authenticator method` — Staat de gebruiker toe om te selecteren wanneer het registreren en het voor authentiek verklaren in _Admin_.
   - `Automatically send this device a Duo Push` — Verstuurt een bericht naar het apparaat voor acceptatie of weigering van toegang.
   - `Automatically call this device` — Vraag en verstrekt een wachtwoord om voor toegang in te gaan.

   ![ Duo controleacties ](./assets/storefront-2fa-duo-user7.png){width="300"}

### Stap 2: Aanmelden met [!DNL Duo Security]

In het volgende voorbeeld worden de opties voor `Ask me to choose an authenticator method` getoond:

1. Wanneer ertoe aangezet, ga uw _Admin_ geloofsbrieven in om binnen te ondertekenen.

   ![ Duo - handtekening ](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Kies de methode die u wilt gebruiken voor verificatie:

   - `Send Me a Push` — Klik om een pushbericht te ontvangen aan [!DNL Duo Mobile] . Accepteren voor verificatie.
   - `Call Me` — Klik deze optie, ontvang een vraag met een code, en ga de pascode in.
   - `Enter a Passcode` — Klik op deze optie om een voldoende-code te ontvangen en in te voeren.

1. Voltooi duw of code om binnen aan _Admin_ volledig te ondertekenen.

## [!DNL Authy]

[!DNL Authy] biedt gebruikers gratis toegang tot hun app en service. Volg hun instructies om de app voor uw apparaat of browser te downloaden en in te stellen. Meer leren, zie de [[!DNL Authy]  documentatie ](https://authy.com/features/setup/).

### Stap 1: Auteur instellen

1. Ga uw rekeningsgeloofsbrieven in en meld binnen aan _Admin_.

   ![[!DNL Authy] registration ](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Ga als volgt te werk wanneer u wordt gevraagd uzelf te registreren bij Auteur:

   - Selecteer uw land.

   - Voer uw telefoonnummer in.

   - Selecteer **[!UICONTROL Verification method]**: `SMS` of `Call Me`

   Klik op **[!UICONTROL Continue]**. Een bericht wordt verzonden naar uw telefoon door de tekst van SMS of een vraag.

1. Voer de verificatiecode in die u ontvangt en klik op **[!UICONTROL Verify]** .

1. Klik op **[!UICONTROL Confirm]** als de bewerking is voltooid.

   ![[!DNL Authy] verificatiecode ](./assets/storefront-2fa-authy-verify.png){width="300"}

### Stap 2: Aanmelden met [!DNL Authy]

1. Ga uw rekeningsgeloofsbrieven in en meld binnen aan _Admin_.

   ![[!DNL Authy] - sign in ](./assets/storefront-2fa-authy-access.png){width="300"}

1. Kies een van de volgende methoden voor verificatie:

   - `Use one touch` — hiermee wordt een waarschuwing naar uw [!DNL Authy] -app verzonden. Accepteer de toegang in de app.
   - `Use authy token` — Prompts to enter a code from your [!DNL Authy] app.

1. Als u zich niet kunt aanmelden, kiest u de methode die u wilt gebruiken om de code te ontvangen. Dan, ga de code in die u ontvangt om tot _Admin_ toegang te hebben.

   De app bevat deze aanvullende noodmethoden.

   - `Send me a code via SMS` — Een SMS-bericht voor tekst wordt verzonden naar het geconfigureerde mobiele apparaat.
   - `Send me a code via phone call` — De gebruiker ontvangt een telefoongesprek met een code.

   Uw account is geverifieerd en wordt geopend.

## U2F ([!DNL Yubikey] en andere apparaten)

Volg de instructies van de leverancier van de oplossing om uw U2F apparaat te vormen. Zie de documentatie van de leverancier, bijvoorbeeld [[!DNL YubiKey] ](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) by [!UICONTROL Yubico] , voor meer informatie.

1. Ga uw rekeningsgeloofsbrieven in en meld binnen aan _Admin_.

   ![ U2F zeer belangrijke toegang ](./assets/storefront-2fa-u2f.png){width="300"}

1. Druk op de toets.

   De authentificatie brengt onmiddellijk teweeg en opent _Admin_.

1. Plaats de **[!UICONTROL U2F key]** in een USB-poort op uw computer.
