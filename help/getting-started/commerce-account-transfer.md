---
title: Een Commerce-account overmaken
description: Leer hoe u uw Commerce-account naar een andere eigenaar of een ander e-mailadres kunt overbrengen.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 9daf227e52c8f225e957ee5009d0d0a02815d835
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---

# Een Commerce-account overmaken

Als uw zakelijke verantwoordelijkheden veranderen, moet u mogelijk het eigendom van uw bestaande Commerce-account overdragen aan een nieuwe eigenaar of een ander e-mailadres. Voor deze overdracht moet de e-mail voor de primaire gebruiker die aan het account is gekoppeld, worden gewijzigd.

De volgende informatie beschrijft het proces voor het overdragen van een Commerce (MAGEID) rekening. Wijzigingen voor eigendom van Cloud-account (Cloud-project of New Relic) zijn hier niet in inbegrepen. Voor meer informatie over de toegang van het wolkenproject, zie [ gebruikerstoegang ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) in _Commerce op de Gids van de Infrastructuur van de Wolk beheren_.

>[!IMPORTANT]
>
>Als de nieuwe accounteigenaar oorspronkelijk extensies had aangeschaft met Gedeelde toegang, gaan deze extensies verloren zodra het proces Account Transfer is gestart. Alvorens om de rekeningsoverdracht te verzoeken, zorg ervoor dat de nieuwe eigenaar identiteitskaarts van de Orde voor de aankopen van [ terugwint hun rekening van de Marketplace ](https://commercemarketplace.adobe.com/sales/order/history/) en om een terugbetaling voor die uitbreidingen van het [ team van de Marketplace ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) verzoekt. Het is niet mogelijk om extensieaankopen naar een andere account over te maken.

## Identificeer uw overdrachtstype

Hoe u deze overdracht voltooit, hangt af van welke van de volgende scenario&#39;s uw situatie als huidige eigenaar van de rekening en de nieuwe eigenaar (e-mailadres) beschrijft aan wie u de rekening wilt overbrengen:

| Overdrachtstype | Huidige eigenaar | Nieuwe eigenaar |
| ------------- | ------------- | --------- |
| [ Nieuwe Adobe ID en e-mailverandering ](#new-adobe-id-and-email-change) | Heeft een MAGEID die **_niet_** met een Adobe login rekening verbonden is. | Heeft geen MAGEID en is niet verbonden met een Adobe-aanmeldingsaccount. |
| [ E-mailverandering ](#email-change) | Heeft een MAGEID die **__** met een Adobe login rekening wordt verbonden. | Heeft geen MAGEID en is niet verbonden met een Adobe-aanmeldingsaccount. |
| [ de schakelaar van Adobe ID ](#adobe-id-account-switch) | Heeft een MAGEID die **__** met een Adobe login rekening wordt verbonden. | Heeft een MAGEID en is verbonden met een Adobe-aanmeldingsaccount waarbij geen andere Adobe-producten of -services zijn gekoppeld. |

{style="table-layout:auto"}

>[!NOTE]
>
>Aangezien Adobe Commerce zich blijft integreren met andere Adobe-oplossingen, is voor een Commerce-account (MAGEID) nu een koppeling met een Adobe-aanmelding vereist. Deze Adobe ID gebruikt hetzelfde e-mailadres als dat van uw Commerce-account.

## Nieuwe Adobe ID en e-mailwijziging

>[!IMPORTANT]
>
>Herzie de [ overdrachtstypes ](#identify-your-transfer-type) en zorg ervoor dat u aan de voorwaarden voor deze opeenvolging van stappen voldoet.

Voor dit type overdracht moet u eerst een gekoppelde Adobe ID maken en die account vervolgens wijzigen in het e-mailadres voor de nieuwe eigenaar.

1. Ga naar uw [ rekening van Commerce ](https://account.magento.com/customer/account/login/).

1. Klik op **[!UICONTROL Sign in with Adobe ID]**.

1. Klik op **[!UICONTROL Create an account]**.

1. Voer het e-mailadres van de huidige eigenaar en een wachtwoord in.

1. Klik op **[!UICONTROL Continue]**.

   Hiermee wordt een Adobe ID gemaakt en gekoppeld aan de huidige Commerce-account (MAGEID). Met deze accountkoppeling wordt het veld _[!UICONTROL Email]_geblokkeerd zodat er geen wijzigingen kunnen worden aangebracht. Het bijbehorende e-mailadres wordt beheerd door de Adobe ID-account.

1. Navigeer aan [ account.adobe.com ](https://account.adobe.com/).

1. Klik op **[!UICONTROL Change Email]**.

1. Voer het e-mailadres van de nieuwe eigenaar in.

1. Klik op **[!UICONTROL Change]**.

   Hiermee wordt een verificatiebericht gegenereerd dat naar het nieuwe e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het nieuwe e-mailadres is verzonden.

1. Klik op **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## E-mailwijziging

>[!IMPORTANT]
>
>Herzie de [ overdrachtstypes ](#identify-your-transfer-type) en zorg ervoor dat u aan de voorwaarden voor deze opeenvolging van stappen voldoet.

1. Navigeer aan [ account.adobe.com ](https://account.adobe.com/) en voltooi login van Adobe.

1. Klik onder uw accountnaam en avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster het e-mailadres van de nieuwe eigenaar in.

1. Klik op **[!UICONTROL Change]**.

   Hiermee wordt een verificatiebericht gegenereerd dat naar het nieuwe e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het nieuwe e-mailadres is verzonden.

1. Klik op **[!UICONTROL Verify]**.

## Adobe ID-accountschakelaar

>[!IMPORTANT]
>
>Herzie de [ overdrachtstypes ](#identify-your-transfer-type) en zorg ervoor dat u aan de voorwaarden voor deze opeenvolging van stappen voldoet.

Als de huidige eigenaar en de nieuwe eigenaar over bestaande Adobe-id&#39;s beschikken, moeten beide accounts behouden blijven, maar moeten de e-mailadressen van de andere accounts worden gewijzigd. Dit vereist het gebruik van a _tijdelijk_ e-mailadres dat geldig is, maar niet met en Adobe ID wordt geassocieerd.

### Wijzigen in een tijdelijke account

De huidige eigenaar voert deze stappen uit om zijn Adobe ID te koppelen aan een ander tijdelijk e-mailadres.

1. Navigeer aan [ account.adobe.com ](https://account.adobe.com/) en voltooi login van Adobe.

1. Klik onder uw accountnaam en avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster een geldig tijdelijk e-mailadres in dat niet wordt gebruikt door een Adobe ID.

   U moet toegang hebben tot het e-mailadres, zodat u het e-mailbericht met de bevestigingscode kunt ophalen.

1. Klik op **[!UICONTROL Change]**.

   Hiermee wordt een verificatiebericht gegenereerd dat naar het tijdelijke e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar het tijdelijke e-mailadres is verzonden.

1. Klik op **[!UICONTROL Verify]**.

1. Afmelden bij Adobe-account.

### Nieuwe stappen voor eigenaars

Nadat de huidige eigenaar de overdracht naar een tijdelijk e-mailadres heeft voltooid, voert u de volgende stappen uit om uw account over te wijzigen naar de huidige eigenaar.

1. Navigeer aan [ account.adobe.com ](https://account.adobe.com/) en voltooi login van Adobe.

1. Klik onder uw accountnaam en avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster het oorspronkelijke e-mailadres van de huidige eigenaar in.

1. Klik op **[!UICONTROL Change]**.

   Hiermee wordt een verificatiebericht gegenereerd dat naar dat e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar de huidige eigenaar is verzonden.

1. Klik op **[!UICONTROL Verify]**.

1. Afmelden bij Adobe-account.

### Follow-upstappen

Nadat de nieuwe eigenaar zijn Adobe-account naar de huidige (nu vorige) eigenaar heeft overgebracht, voert u de volgende stappen uit om de eigendom over te dragen.

1. Navigeer aan [ account.adobe.com ](https://account.adobe.com/) (eerste rekening die in de reeks stappen wordt gebruikt) en voltooi login van Adobe.

   Voor deze aanmelding moet het tijdelijke e-mailadres worden gebruikt.

1. Klik onder de naam van de account en de avatar op **[!UICONTROL Change Email]** .

1. Voer in het dialoogvenster het e-mailadres van de nieuwe eigenaar in.

1. Klik op **[!UICONTROL Change]**.

   Hiermee wordt een verificatiebericht gegenereerd dat naar dat e-mailadres wordt verzonden. Het e-mailbericht bevat een bevestigingscode die vereist is om de wijziging van het e-mailadres te voltooien.

1. Voer de bevestigingscode in die naar de nieuwe eigenaar is verzonden.

1. Klik op **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Verzend een ondersteuningsverzoek om het ondersteuningsteam mee te delen dat u het e-mailadres van de eigenaar van de account hebt bijgewerkt. Het team moet extra stappen uitvoeren om de update zoals het bijwerken van het e-mailadres op uw [ Commerce Marketplace ](https://commercemarketplace.adobe.com/) profiel te voltooien. Neem het e-mailadres van de vorige rekeninghouder op in uw aanvraag.
