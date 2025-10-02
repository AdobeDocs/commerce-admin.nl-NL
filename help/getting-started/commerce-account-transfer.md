---
title: Een Commerce-account overmaken
description: Leer hoe u uw Commerce-account naar een andere eigenaar of een ander e-mailadres kunt overbrengen.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 7d1a086b4c5443e88029fb6f151f41f9926d41ae
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%

---

# Een Commerce-account overmaken

Als de zakelijke verantwoordelijkheden veranderen, moet u mogelijk uw Commerce-account overdragen naar een nieuwe eigenaar of naar een ander e-mailadres. Voor deze overdracht moet de e-mail voor de primaire gebruiker die aan het account is gekoppeld, worden gewijzigd.

De volgende informatie beschrijft het proces voor het overdragen van een Commerce (MAGEID) rekening. Wijzigingen voor eigendom van Cloud-account (Cloud-project of New Relic) zijn hier niet in inbegrepen. Voor meer informatie over de toegang van het wolkenproject, zie [&#x200B; gebruikerstoegang &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) in _Commerce op de Gids van de Infrastructuur van de Wolk beheren_.

>[!IMPORTANT]
>
>Als de nieuwe accounteigenaar extensies heeft aangeschaft met Gedeelde toegang, gaat de toegang tot deze extensies verloren zodra het proces Account Transfer is gestart. Alvorens om de rekeningsoverdracht te verzoeken, zorg ervoor dat de nieuwe eigenaar identiteitskaarts van de Orde voor de aankopen van [&#x200B; terugwint hun rekening van de Marketplace &#x200B;](https://commercemarketplace.adobe.com/sales/order/history/) en om een terugbetaling voor die uitbreidingen van het [&#x200B; team van de Marketplace &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) verzoekt. Het is niet mogelijk om extensieaankopen naar een andere account over te maken.

## Identificeer uw overdrachtstype

Het type Commerce-accountoverdracht is afhankelijk van de Commerce-accountgegevens die beschikbaar zijn voor de huidige eigenaar en de nieuwe eigenaar. De volgende scenario&#39;s beschrijven de verschillende overdrachtstypes die op deze geloofsbrieven worden gebaseerd.

| Overdrachtstype | Huidige eigenaar | Nieuwe eigenaar |
| ------------- | ------------- | --------- |
| [&#x200B; Nieuwe Adobe ID en e-mailverandering &#x200B;](#new-adobe-id-and-email-change) | Heeft MAGEID dat **_niet_** met een Adobe login rekening is verbonden | Heeft geen MAGEID en is niet verbonden met een Adobe-aanmeldingsaccount. |
| [&#x200B; E-mailverandering &#x200B;](#email-change) | Heeft een MAGEID die **__** met een Adobe login rekening wordt verbonden. | Heeft een Adobe login rekening, maar **_heeft geen MAGEID_** verbonden met een Adobe login rekening. |
| [&#x200B; de rekeningsschakelaar van Adobe ID &#x200B;](#adobe-id-account-switch) | Heeft een MAGEID die **__** met een Adobe login rekening wordt verbonden. | Heeft een MAGEID en is verbonden met een Adobe-aanmeldingsaccount. |

{style="table-layout:auto"}

>[!NOTE]
>
>Aangezien Adobe Commerce zich blijft integreren met andere Adobe-oplossingen, is voor een Commerce-account (MAGEID) nu een koppeling met een Adobe-aanmelding vereist. Deze Adobe ID gebruikt hetzelfde e-mailadres als dat van uw Commerce-account.

## Nieuwe Adobe ID en e-mailwijziging

>[!IMPORTANT]
>
>Herzie de [&#x200B; overdrachtstypes &#x200B;](#identify-your-transfer-type) en zorg ervoor dat u aan de voorwaarden voor deze opeenvolging van stappen voldoet.

Voor dit type overschrijving hebt u een Adobe ID nodig die is gekoppeld aan de bestaande Commerce-account. Vervolgens wijzigt u die account in het e-mailadres voor de nieuwe eigenaar.

1. Ga naar de [&#x200B; de rekeningslogin van Commerce &#x200B;](https://account.magento.com/customer/account/login/) pagina.

1. Klik op **[!UICONTROL Sign in with Adobe ID]**.

1. Klik op **[!UICONTROL Create an account]**.

1. Voer het e-mailadres van de huidige eigenaar en een wachtwoord in.

1. Klik op **[!UICONTROL Continue]**.

   Met deze stap wordt een Adobe ID gemaakt en gekoppeld aan de huidige Commerce-account (MAGEID). Met deze accountkoppeling wordt het veld _[!UICONTROL Email]_&#x200B;geblokkeerd zodat er geen wijzigingen kunnen worden aangebracht. De configuratie van het bijbehorende e-mailadres wordt beheerd via de Adobe ID-account.

1. Navigeer aan [&#x200B; account.adobe.com &#x200B;](https://account.adobe.com/).

1. Klik op **[!UICONTROL Change Email]**.

1. Voer het e-mailadres van de nieuwe eigenaar in.

   Als het nieuwe e-mailadres al is gekoppeld aan een andere account in het systeem, kan het niet rechtstreeks worden gebruikt voor de overdracht. In plaats daarvan, vereist het proces het gebruiken van a [&#x200B; tijdelijk e-mailadres &#x200B;](#change-to-a-temporary-account) om de verandering te vergemakkelijken.

1. Klik op **[!UICONTROL Change]**.

   Met deze stap wordt een verificatiebericht gegenereerd dat naar het nieuwe e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het nieuwe e-mailadres is verzonden.

1. Klik op **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## E-mailwijziging

>[!IMPORTANT]
>
>Herzie de [&#x200B; overdrachtstypes &#x200B;](#identify-your-transfer-type) en zorg ervoor dat u aan de voorwaarden voor deze opeenvolging van stappen voldoet.

Dit type overschrijving heeft tot gevolg dat de huidige rekeninghouder de toegang tot andere Adobe-producten verliest.

1. Navigeer aan [&#x200B; account.adobe.com &#x200B;](https://account.adobe.com/) en voltooi login van Adobe.

1. Klik onder uw accountnaam en avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster het e-mailadres van de nieuwe eigenaar in.

   Als het nieuwe e-mailadres al is gekoppeld aan een andere account in het systeem, kan het niet rechtstreeks worden gebruikt voor de overdracht. In plaats daarvan, vereist het proces het gebruiken van a [&#x200B; tijdelijk e-mailadres &#x200B;](#change-to-a-temporary-account) om de verandering te vergemakkelijken.

1. Klik op **[!UICONTROL Change]**.

   Met deze stap wordt een verificatiebericht gegenereerd dat naar het nieuwe e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het nieuwe e-mailadres is verzonden.

1. Klik op **[!UICONTROL Verify]**.

## Adobe ID-accountschakelaar

>[!IMPORTANT]
>
>Herzie de [&#x200B; overdrachtstypes &#x200B;](#identify-your-transfer-type) en zorg ervoor dat u aan de voorwaarden voor deze opeenvolging van stappen voldoet.

Dit overdrachtstype gebruikt een tijdelijk e-mailadres om over te schakelen naar het eigendom van een account wanneer zowel de huidige eigenaar als de nieuwe eigenaar bestaande Adobe-id&#39;s hebben en u beide accounts wilt behouden. Als u de eigendomsoverdracht wilt voltooien, moet u een tijdelijk e-mailadres gebruiken dat niet aan een Adobe ID is gekoppeld.

### Wijzigen in een tijdelijke account

De huidige eigenaar voert deze stappen uit om zijn Adobe ID te koppelen aan een ander tijdelijk e-mailadres.

1. Navigeer aan [&#x200B; account.adobe.com &#x200B;](https://account.adobe.com/) en voltooi login van Adobe.

1. Klik onder uw accountnaam en avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster een geldig tijdelijk e-mailadres in dat niet wordt gebruikt door een Adobe ID.

   U moet toegang hebben tot het e-mailadres, zodat u het e-mailbericht met de bevestigingscode kunt ophalen.

1. Klik op **[!UICONTROL Change]**.

   Met deze stap wordt een verificatiebericht gegenereerd dat naar het tijdelijke e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het tijdelijke e-mailadres is verzonden.

1. Klik op **[!UICONTROL Verify]**.

1. Afmelden bij Adobe-account.

### Nieuwe stappen voor eigenaars

Nadat de huidige eigenaar de overdracht naar een tijdelijk e-mailadres heeft voltooid, moet de nieuwe eigenaar deze stappen voltooien om de configuratie van zijn account te wijzigen zodat deze het oorspronkelijke e-mailadres van de huidige eigenaar aanwijst.

1. Navigeer aan [&#x200B; account.adobe.com &#x200B;](https://account.adobe.com/) en voltooi login van Adobe.

1. Klik onder uw accountnaam en avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster het oorspronkelijke e-mailadres van de huidige eigenaar in.

1. Klik op **[!UICONTROL Change]**.

   Met deze stap wordt een verificatiebericht gegenereerd dat naar het oorspronkelijke e-mailadres van de huidige eigenaar is verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het oorspronkelijke e-mailadres van de huidige eigenaar is verzonden.

1. Klik op **[!UICONTROL Verify]**.

1. Afmelden bij Adobe-account.

### Follow-upstappen

Nadat de nieuwe eigenaar zijn Adobe-account heeft geconfigureerd met het oorspronkelijke e-mailadres van de huidige eigenaar, voert u de volgende stappen uit om de eigendom over te dragen.

1. Navigeer aan [&#x200B; account.adobe.com &#x200B;](https://account.adobe.com/), en voltooi login van Adobe gebruikend het e-mailadres voor de [&#x200B; tijdelijke rekening &#x200B;](#change-to-a-temporary-account).

1. Klik onder de naam van de account en de avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster het e-mailadres van de nieuwe eigenaar in.

1. Klik op **[!UICONTROL Change]**.

   Met deze stap wordt een verificatiebericht gegenereerd dat naar het e-mailadres van de nieuwe eigenaar wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het e-mailadres van de nieuwe eigenaar is verzonden.

1. Klik op **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Verzend een ondersteuningsverzoek om het ondersteuningsteam mee te delen dat u het e-mailadres van de eigenaar van de account hebt bijgewerkt. Het team moet extra stappen uitvoeren om de update zoals het bijwerken van het e-mailadres op uw [&#x200B; Commerce Marketplace &#x200B;](https://commercemarketplace.adobe.com/) profiel te voltooien. Neem het e-mailadres van de vorige rekeninghouder op in uw aanvraag.
