---
title: Beveiliging van beheerder configureren
description: Leer hoe u beveiliging voor uw winkelbeheerder configureert.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Beveiliging van beheerder configureren

Wij adviseren dat u een veelzijdige benadering neemt om de veiligheid van uw opslag te beschermen. U kunt beginnen met het gebruik van een [aangepaste Admin-URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) Dat is niet gemakkelijk te raden, maar de duidelijke &quot;Admin&quot; of &quot;Backend&quot;. Door gebrek, wachtwoorden die worden gebruikt aan [aanmelden](../getting-started/admin-signin.md) naar de beheerder moet uit minimaal zeven tekens bestaan en zowel letters als cijfers bevatten. Als [beste praktijken](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)Gebruik alleen sterke beheerderswachtwoorden die een combinatie van letters, cijfers en symbolen bevatten. Adobe Commerce en Magento Open Source staan niet toe dat de laatste vier wachtwoorden die aan de account zijn toegewezen, opnieuw worden gebruikt.

Met de beveiligingsconfiguratie Admin kunt u:

- Een geheime sleutel toevoegen aan URL&#39;s
- Wachtwoorden zijn hoofdlettergevoelig
- De duur van beheerderssessies beperken
- De levensduur van wachtwoorden beperken
- Beperk het aantal aanmeldpogingen dat kan worden uitgevoerd voordat de Admin-gebruikersaccount is ingesteld [vergrendeld](permissions-users-all.md#locked-users).

Voor verhoogde veiligheid, kunt u de lengte van toetsenbordinactiviteit vormen alvorens de huidige zitting verloopt, en vereisen de gebruikersnaam en het wachtwoord om case-sensitive te zijn.

Naast de beveiligingsinstellingen in deze sectie, [tweeledige verificatie](security-two-factor-authentication.md) (2FA) is vereist om de identiteit van gebruikers te verifiëren met een eenmalig wachtwoord dat door een app of apparaat wordt gegenereerd. De eerste keer dat u zich aanmeldt bij de beheerder, wordt u gevraagd om 2FA in te stellen. Voor extra beveiliging kan de beheerdersaanmelding ook zo worden geconfigureerd dat een [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Winkels die zijn ingeschakeld [!DNL Adobe Identity Management Services] (IMS)-verificatie heeft native Adobe Commerce en Magento Open Source 2FA uitgeschakeld. De gebruikers Admin die in hun instantie van de Handel met hun geloofsbrieven van de Adobe worden geregistreerd hoeven niet voor vele Admin taken opnieuw voor authentiek te verklaren. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service] (IMS) Overzicht van integratie](../getting-started/adobe-ims-integration-overview.md).

Voor technische informatie, zie [Beveiligingsoverzicht](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} in de ontwikkelaarsdocumentatie.

![Beveiliging beheerder](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Beveiliging van beheerder configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL Advanced]_, kiest u **[!UICONTROL Admin]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Security]** sectie.

1. Als u wilt voorkomen dat Admin-gebruikers zich aanmelden bij hetzelfde account op verschillende apparaten, stelt u **[!UICONTROL Admin Account Sharing]** tot `No`.

1. Om de methode te bepalen die wordt gebruikt om verzoeken om opnieuw instellen van wachtwoorden te beheren, plaatst **[!UICONTROL Password Reset Protection Type]** op een van de volgende wijzen:

   - `By IP and Email` — Het wachtwoord kan online opnieuw worden ingesteld nadat een reactie is ontvangen van het bericht is verzonden naar het e-mailadres dat is gekoppeld aan de beheerdersaccount.
   - `By IP` — Het wachtwoord kan online opnieuw worden ingesteld zonder extra bevestiging.
   - `By Email` — Het wachtwoord kan alleen opnieuw worden ingesteld door per e-mail te reageren op het bericht dat is verzonden naar het e-mailadres dat is gekoppeld aan de beheerdersaccount.
   - `None` — Het wachtwoord kan slechts door de opslagbeheerder worden teruggesteld.

1. Beveiligingsopties voor aanmelding instellen:

   - Voor **[!UICONTROL Recovery Link Expiration Period (hours)]** Voer het aantal uren in dat een koppeling voor wachtwoordherstel geldig blijft.

   - Om het maximumaantal wachtwoordverzoeken te bepalen dat per uur kan worden ingediend, ga het aantal voor **[!UICONTROL Max Number of Password Reset Requests]**.

   - Voor **[!UICONTROL Min Time Between Password Reset Requests]** Voer het minimale aantal minuten in dat moet worden doorgestuurd tussen aanvragen voor het opnieuw instellen van wachtwoorden.

   - Als u een geheime sleutel als voorzorgsmaatregel tegen misbruik wilt toevoegen aan de URL van Admin, stelt u **[!UICONTROL Add Secret Key to URLs]** tot `Yes`. Deze instelling is standaard ingeschakeld.

   - Om te vereisen dat het gebruik van hogere en kleine letters in om het even welke login ingegaan geloofsbrieven aanpast wat in het systeem wordt opgeslagen, plaats **[!UICONTROL Login is Case Sensitive]** tot `Yes`.

   - Voer de duur van de sessie in seconden in voor u de duur van een beheersessie voor time-out kunt bepalen **[!UICONTROL Admin Session Lifetime (seconds)]** veld. De waarde moet 60 seconden of langer zijn.

   - Voor **[!UICONTROL Maximum Login Failures to Lockout Account]** Voer het aantal keren in dat een gebruiker zich kan aanmelden bij de beheerder voordat de account is vergrendeld. Standaard zijn zes pogingen toegestaan. Laat het veld leeg voor onbeperkte aanmeldpogingen.

   - Voor **[!UICONTROL Lockout Time (minutes)]** Voer het aantal minuten in dat een beheerdersaccount is vergrendeld wanneer aan het maximumaantal pogingen is voldaan.

1. Stel wachtwoordopties in:

   - Voer het aantal dagen in waarop een wachtwoord geldig is om de levensduur van beheerderswachtwoorden te beperken **[!UICONTROL Password Lifetime (days)]**. Laat het veld leeg voor een onbeperkte levensduur.

   - Set **[!UICONTROL Password Change]** op een van de volgende wijzen:

      - `Forced` — Vereist dat Admin-gebruikers hun wachtwoorden wijzigen na het instellen van de account.
      - `Recommended` — Aanbevolen dat Admin-gebruikers hun wachtwoorden wijzigen na het instellen van de account.

1. Klik op **[!UICONTROL Save Config]**.

## Wachtwoordvereisten voor beheerders

Een beheerderswachtwoord moet standaard zeven of meer tekens lang zijn en zowel letters als cijfers bevatten.
