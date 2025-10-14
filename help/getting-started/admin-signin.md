---
title: Uw beheerdersaccount
description: Meer informatie over uw beheerdersaccount en over het gebruik van tweeledige verificatie voor aanmelding bij de beheerder.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: 54fdc97156c602337c983de5fddfafd7c50a67e1
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Uw beheerdersaccount

Het primaire beheerdersaccount is oorspronkelijk ingesteld tijdens de installatie en bevat mogelijk initiële plaatsaanduidingsgegevens of voorbeeldgegevens. De aangewezen eigenaar van dit account kan de gebruikersnaam en het wachtwoord aanpassen en de voornaam, achternaam en het e-mailadres op elk gewenst moment bijwerken. Deze rekening, a _super gebruiker_ met alle toestemmingen door gebrek, leidt typisch tot de Admin gebruikersrekeningen nodig voor de zaken.

- Zie [&#x200B; een gebruiker &#x200B;](../systems/permissions-users-all.md#create-a-user) voor informatie creëren bij het toevoegen van of het uitgeven van gebruikers.

- Zie [&#x200B; Toestemmingen &#x200B;](../systems/permissions.md) en [&#x200B; Rollen van de Gebruiker &#x200B;](../systems/permissions-user-roles.md) voor informatie over Admin en gebruikersrollen.

{{ims-admin-note}}

## Aanmelden bij beheerder

[!DNL Commerce] _Admin_ wordt beschermd door veelvoudige lagen van veiligheidsmaatregelen om onbevoegde toegang tot uw opslag, orde, en klantengegevens te verhinderen. De eerste keer u binnen aan _Admin_ ondertekent, moet u uw gebruikersbenaming en wachtwoord ingaan en aan opstelling [&#x200B; tweefaste authentificatie &#x200B;](../systems/security-two-factor-authentication.md) (2FA).

Afhankelijk van de configuratie van uw opslag, kan er a [&#x200B; CAPTCHA &#x200B;](../systems/security-google-recaptcha.md) uitdaging zijn op te lossen, zoals het ingaan van een reeks toetsenbordkarakters, het oplossen van een raadsel, of het klikken van een reeks beelden met een gemeenschappelijk thema. Deze tests zijn ontworpen om je te identificeren als mens, in plaats van als een geautomatiseerde bot.

Voor extra veiligheid, kunt u bepalen welke delen van _Admin_ elke gebruiker [&#x200B; toestemming &#x200B;](../systems/permissions.md) heeft om toegang te hebben, en ook het aantal [&#x200B; login pogingen &#x200B;](../configuration-reference/advanced/admin.md) te beperken. Standaard is het account na zes pogingen vergrendeld en moet de gebruiker een paar minuten wachten voordat hij het opnieuw probeert. [&#x200B; Vergrendelde rekeningen &#x200B;](../systems/permissions-users-all.md#locked-users) kunnen ook van _Admin_ worden teruggesteld.

>[!NOTE]
>
>De eerste keer u binnen aan _Admin_ ondertekent, wordt u ertoe aangezet om _de inzameling van admin gebruiksgegevens_ toe te staan. Zie [&#x200B; de gegevensinzameling van het Gebruik &#x200B;](admin.md#usage-data-collection) voor meer informatie.

![&#x200B; binnen teken Admin &#x200B;](./assets/admin-login.png){width="400"}

### Stap 1: Opstelling tweefasenauthentificatie

Alvorens u binnen aan _Admin_ van uw opslag kunt ondertekenen, moet u een twee-factor opstelling van de authentificatieoplossing hebben en klaar te gebruiken. Meer over het authentificatieproces leren dat door elke oplossing wordt gebruikt, zie [&#x200B; Gebruikend Two-Factor Authentificatie &#x200B;](../systems/security-two-factor-authentication-use.md). Door gebrek, [!DNL Commerce] steunt [ de Authenticator van Google ][1].

Vraag aan de systeembeheerder van [!DNL Commerce] welke 2FA-oplossingen worden ondersteund voor de winkel. Voer vervolgens de installatie van de gewenste 2FA-oplossing uit volgens de instructies van de provider.

### Stap 2: Aanmelden bij de beheerder

1. Ga _Admin_ URL in die tijdens de [!DNL Commerce] installatie werd gespecificeerd.

   Het gebrek _Admin_ URL kijkt iets als `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >Hoewel deze documentatie `admin` als basis URL in de meeste voorbeelden gebruikt, wordt het geadviseerd dat u een uniek en hard-aan-gok [&#x200B; douane URL &#x200B;](../stores-purchase/store-urls.md) voor _Admin_ van uw opslag kiest.

   U kunt een bladwijzer voor de pagina toevoegen of een sneltoets op uw bureaublad opslaan, zodat u deze gemakkelijk kunt openen.

1. Ga uw _Admin_ **[!UICONTROL Username]** en **[!UICONTROL Password]** in.

1. (Optioneel) Als een CAPTCHA voor uw winkel is ingeschakeld, volgt u de aanwijzingen op het scherm om de uitdaging op te lossen.

   Meer leren, zie [&#x200B; CAPTCHA &#x200B;](../systems/security-captcha.md) en [&#x200B; reCAPTCHA &#x200B;](../systems/security-google-recaptcha.md).

1. Klik op **[!UICONTROL Sign in]**.

   Als het de eerste keer is u binnen aan _Admin_ van de rekening hebt ondertekend, zou u een e-mail met een verbinding aan configuratieinstructies moeten ontvangen.

### Stap 3: Voltooi de 2FA-configuratie

Het volgende voorbeeld toont hoe te om uw _Admin_ rekening met de Authenticator van Google te koppelen.

1. Wanneer de QR code verschijnt, gebruik één van de volgende methodes om de code en paarGoogle Authenticator met uw _Admin_ rekening te vangen.

   ![&#x200B; de Authenticator van Google van de opstelling &#x200B;](./assets/admin-login-google-auth-setup.png){width="400"}

   - QR-code vastleggen met een smartphone

     Start Google Authenticator op uw smartphone. Tik het _plusteken_ (+) in de hoger-juiste hoek van app. Tik vervolgens onder aan het scherm op **[!UICONTROL Scan Barcode]** en maak een foto van de QR-code.

   - QR-code vastleggen vanuit browser

     Als de Authenticator van Google als uitbreiding in uw browser wordt geïnstalleerd, klik het **Authenticator** pictogram in de toolbar en vang de pagina.

   - Voer handmatig de QR-code in

     Kopieer de tekstreeks onder de QR-code. Start Google Authenticator met uw smartphone of browser en klik op het plusteken (+). Kies vervolgens **[!UICONTROL Manual Entry]** . Onder **[!UICONTROL Account]**, ga het e-mailadres in dat met uw _Admin_ rekening wordt geassocieerd en kleef het QR codekoord in het **[!UICONTROL Key]** gebied.

1. Om binnen aan _Admin_ met twee-factor authentificatie te ondertekenen, ga de code van zes cijfers in die door de Authenticator van Google in het **[!UICONTROL Authenticator code]** gebied wordt geproduceerd, en klik dan **[!UICONTROL Confirm]**.

   ![&#x200B; ga de code van Authenticator &#x200B;](./assets/admin-login-2fa-google.png){width="400"} in

## Wachtwoord opnieuw instellen

Hergebruik van de laatste vier wachtwoorden die aan de account zijn toegewezen, is niet toegestaan.

1. Ga **[!UICONTROL Email Address]** in dat met de _Admin_ rekening wordt geassocieerd.

   ![&#x200B; vergeten wachtwoord &#x200B;](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Klik op **[!UICONTROL Retrieve Password]**.

   Als een account aan het e-mailadres is gekoppeld, wordt een e-mail verzonden om uw wachtwoord opnieuw in te stellen.

   >[!NOTE]
   >
   >Een _Admin_ wachtwoord moet zeven of meer lange karakters zijn en zowel brieven als aantallen omvatten. Zie [&#x200B; Vormend _Admin_ Veiligheid &#x200B;](../systems/security-admin.md) voor informatie over wachtwoordopties.

## Afmelden bij de beheerder

1. In de hoger-juiste hoek, klik het _pictogram van de Rekening_ (![&#x200B; Rekening &#x200B;](../assets/icon-admin-user.png)).

1. Klik op **[!UICONTROL Sign Out]**.

   ![&#x200B; Teken uit &#x200B;](./assets/admin-sign-out.png){width="700" zoomable="yes"}

Op de pagina _[!UICONTROL Sign In]_&#x200B;wordt een bericht weergegeven dat u bent afgemeld. Teken uit_ Admin _wanneer u uw computer onbeheerd verlaat.

## Accountgegevens bewerken

1. Klik het _pictogram van de Rekening_ (![&#x200B; het pictogram van de Rekening &#x200B;](../assets/icon-admin-user.png)).

1. Klik op **[!UICONTROL Account Setting]**.

   ![&#x200B; de Informatie van de Rekening &#x200B;](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Breng de benodigde wijzigingen aan in uw accountgegevens.

   Als u uw aanmeldingsgegevens wijzigt, moet u ervoor zorgen dat u deze op een veilige locatie opslaat.

1. Voer het wachtwoord voor uw huidige account in.

1. Klik op **[!UICONTROL Save Account]**.

## Meerdere Admin-aanmeldingen toestaan

De beheerder biedt toegang om de functies voor bestellingen, klanten, producten, verzending en betalingen te beheren. De standaardconfiguratie wordt geplaatst om veelvoudige logins voor een Admin gebruikersrekening als veiligheids beste praktijken niet toe te staan. U kunt deze instelling echter wijzigen zodat Admin-gebruikers zich vanaf meerdere apparaten kunnen aanmelden voor uw zakelijke workflows.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het navigatievenster aan de linkerkant **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Admin]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Security]** sectie uit.

1. Voor **het Delen van de Rekening Admin**, uitgezochte `Yes`.

   ![&#x200B; staat Admin rekening het delen &#x200B;](./assets/multiple-admin-login.png){width="700" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save Config]**.

## Aanmeldingsnamen van Admin-gebruikers instellen als hoofdlettergevoelig

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het navigatievenster aan de linkerkant **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Admin]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Security]** sectie uit.

1. Stel het veld **[!UICONTROL Login is Case Sensitive]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_US

## Veilige toegang tot de beheerder

Om de veiligheid van uw admin te verzekeren, voer regelmatige controles van gebruikers en rollen met admintoegang uit.

Bovendien, overweeg [&#x200B; het bijwerken van de configuratie Admin Basis URL &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce-admin/config/advanced/admin#admin-base-url) om het standaard `/admin` eindpunt in een douanepad te veranderen. Het vormen van een douanepad verstrekt de volgende veiligheidsvoordelen:

**Verbeterde Veiligheid**: De standaard &quot;admin&quot;weg is wijd gekend en vaak gericht door kwaadwillige acteurs die brute krachtaanvallen proberen. Door het in een unieke, douanewaarde te veranderen, vermindert u beduidend het risico van ongeoorloofde toegangspogingen.

**Verminderde Vulnerability**: De geautomatiseerde bots scannen vaak voor gemeenschappelijke wegen zoals &quot;admin&quot;om kwetsbaarheid te exploiteren. Een douanepad maakt het voor deze bots moeilijker om van uw admin login pagina de plaats te bepalen, daardoor verminderend de waarschijnlijkheid van aanvallen.

**Verbeterde Privacy**: Een weg van douane admin voegt een extra laag van onveiligheid toe, makend het voor potentiële aanvallers moeilijker om uw admin login pagina te identificeren en te richten.

**Naleving met Beste praktijken**: Na veiligheids beste praktijken, zoals het aanpassen van uw admin weg, toont een pro-actieve benadering aan om uw e-commercesite en klantengegevens te beschermen.

>[!NOTE]
>
>Als een breuk wordt vermoed, zorg ervoor om alle onbekende gebruikers Admin te verwijderen en alle wachtwoorden Admin terug te stellen en het [&#x200B; actieplan van de Veiligheid &#x200B;](https://experienceleague.adobe.com/nl/docs/commerce-admin/systems/security/security) voor verdere stappen te herzien.
