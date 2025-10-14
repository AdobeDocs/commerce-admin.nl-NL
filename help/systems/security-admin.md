---
title: Beveiliging van beheerder configureren
description: Leer hoe u beveiliging voor uw winkelbeheerder configureert.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Beveiliging van beheerder configureren

Wij adviseren dat u een veelzijdige benadering neemt om de veiligheid van uw opslag te beschermen. U kunt beginnen door a [&#x200B; douane Admin URL &#x200B;](../stores-purchase/store-urls.md#use-a-custom-admin-url) te gebruiken die niet gemakkelijk is te raden, eerder dan duidelijk &quot;Admin&quot;of &quot;Achterkant.&quot; Door gebrek, moeten de wachtwoorden die aan [&#x200B; login &#x200B;](../getting-started/admin-signin.md) aan Admin worden gebruikt zeven of meer lange karakters zijn en zowel brieven als aantallen omvatten. Als a [&#x200B; beste praktijken &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=nl-NL), gebruik slechts sterke wachtwoorden Admin die een combinatie brieven, aantallen, en symbolen omvatten. Adobe Commerce en Magento Open Source staan niet toe dat de laatste vier wachtwoorden die aan de account zijn toegewezen, opnieuw worden gebruikt.

Met de beveiligingsconfiguratie Admin kunt u:

- Een geheime sleutel toevoegen aan URL&#39;s
- Wachtwoorden zijn hoofdlettergevoelig
- De duur van beheerderssessies beperken
- De levensduur van wachtwoorden beperken
- Beperk het aantal login pogingen die kunnen worden gemaakt alvorens de Admin gebruikersrekening [&#x200B; wordt gesloten &#x200B;](permissions-users-all.md#locked-users).

Voor verhoogde veiligheid, kunt u de lengte van toetsenbordinactiviteit vormen alvorens de huidige zitting verloopt, en vereisen de gebruikersnaam en het wachtwoord om case-sensitive te zijn.

Naast de veiligheidsmontages in deze sectie, [&#x200B; wordt tweeledige authentificatie &#x200B;](security-two-factor-authentication.md) (2FA) vereist om de identiteit van gebruikers met een eenmalig wachtwoord te verifiëren dat door een app of een apparaat wordt geproduceerd. De eerste keer dat u zich aanmeldt bij de beheerder, wordt u gevraagd om 2FA in te stellen. Voor extra veiligheid, kan login Admin ook worden gevormd om a [&#x200B; CAPTCHA &#x200B;](security-captcha.md) te vereisen.

>[!NOTE]
>
>Voor opslagruimten die verificatie met [!DNL Adobe Identity Management Services] (IMS) hebben ingeschakeld, zijn Adobe Commerce en Magento Open Source 2FA uitgeschakeld. Admin-gebruikers die zich met hun Adobe-gegevens bij hun Commerce-exemplaar hebben aangemeld, hoeven voor veel beheertaken niet opnieuw te worden geverifieerd. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service]  (IMS) Overzicht van de Integratie &#x200B;](../getting-started/adobe-ims-integration-overview.md).

Voor technische informatie, zie [&#x200B; Overzicht van de Veiligheid &#x200B;](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} in de ontwikkelaardocumentatie.

![&#x200B; Admin veiligheid &#x200B;](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Beveiliging van beheerder configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL Advanced]_&#x200B;de optie **[!UICONTROL Admin]**.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Security]** sectie uit.

1. Stel **[!UICONTROL Admin Account Sharing]** in op `No` om te voorkomen dat Admin-gebruikers zich vanaf hetzelfde account aanmelden op verschillende apparaten.

1. Stel **[!UICONTROL Password Reset Protection Type]** in op een van de volgende opties om te bepalen welke methode wordt gebruikt voor het beheren van aanvragen voor het opnieuw instellen van wachtwoorden:

   - `By IP and Email` — Het wachtwoord kan online opnieuw worden ingesteld nadat een reactie is ontvangen van het bericht is verzonden naar het e-mailadres dat is gekoppeld aan het beheerdersaccount.
   - `By IP` — U kunt het wachtwoord online opnieuw instellen zonder extra bevestiging.
   - `By Email` — Het wachtwoord kan alleen opnieuw worden ingesteld door per e-mail te reageren op het bericht dat is verzonden naar het e-mailadres dat is gekoppeld aan het beheerdersaccount.
   - `None` — Het wachtwoord kan slechts door de archiefbeheerder worden teruggesteld.

1. Beveiligingsopties voor aanmelding instellen:

   - Voer voor **[!UICONTROL Recovery Link Expiration Period (hours)]** het aantal uren in dat een koppeling voor wachtwoordherstel geldig blijft.

   - Om het maximumaantal wachtwoordverzoeken te bepalen dat per uur kan worden ingediend, ga het aantal voor **[!UICONTROL Max Number of Password Reset Requests]** in.

   - Voer bij **[!UICONTROL Min Time Between Password Reset Requests]** het minimale aantal minuten in dat moet worden doorgestuurd tussen aanvragen voor het opnieuw instellen van wachtwoorden.

   - Stel **[!UICONTROL Add Secret Key to URLs]** in op `Yes` als u een geheime sleutel aan de URL van Admin wilt toevoegen als voorzorgsmaatregel tegen explosies. Deze instelling is standaard ingeschakeld.

   - Stel **[!UICONTROL Login is Case Sensitive]** in op `Yes` om te vereisen dat het gebruik van hoofdletters en kleine letters in aanmeldingsgegevens overeenkomt met wat in het systeem is opgeslagen.

   - Als u de lengte van een Admin-sessie wilt bepalen voordat deze wordt beëindigd, voert u de duur van de sessie in seconden in voor het veld **[!UICONTROL Admin Session Lifetime (seconds)]** . De waarde moet 60 seconden of langer zijn.

   - Voer bij **[!UICONTROL Maximum Login Failures to Lockout Account]** het aantal keren in dat een gebruiker zich kan aanmelden bij de beheerder voordat de account is vergrendeld. Standaard zijn zes pogingen toegestaan. Laat het veld leeg voor onbeperkte aanmeldpogingen.

   - Voer voor **[!UICONTROL Lockout Time (minutes)]** het aantal minuten in dat een beheerdersaccount is vergrendeld wanneer het maximumaantal pogingen is bereikt.

1. Stel wachtwoordopties in:

   - Als u de levensduur van beheerderswachtwoorden wilt beperken, voert u het aantal dagen in dat een wachtwoord geldig is voor **[!UICONTROL Password Lifetime (days)]** . Laat het veld leeg voor een onbeperkte levensduur.

   - Stel **[!UICONTROL Password Change]** in op een van de volgende opties:

      - `Forced` — Vereist dat Admin-gebruikers hun wachtwoorden wijzigen na het instellen van de account.
      - `Recommended` — Aanbevolen dat Admin-gebruikers hun wachtwoorden wijzigen na het instellen van de account.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Wachtwoordvereisten voor beheerders

Een beheerderswachtwoord moet standaard zeven of meer tekens lang zijn en zowel letters als cijfers bevatten.
