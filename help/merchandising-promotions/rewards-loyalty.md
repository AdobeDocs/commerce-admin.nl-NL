---
title: Programma's voor beloningen en loyaliteit
description: Leer over het systeem van beloningspunten dat u kunt gebruiken om klantenovereenkomst te drijven en klantenloyaliteit te bevorderen.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---

# Programma&#39;s voor beloningen en loyaliteit

{{ee-feature}}

De _beloningspunten_ -systeem in Adobe Commerce biedt u de mogelijkheid unieke programma&#39;s te implementeren die de betrokkenheid van klanten stimuleren en klantenloyaliteit bevorderen. Punten kunnen worden toegekend voor een breed scala aan transactie- en klantactiviteiten en de configuratie kan worden ingesteld om de punttoewijzing, het saldo en de vervaldatum te bepalen. Klanten kunnen punten in de richting van aankopen inwisselen op basis van de omrekeningskoers die u tussen bonuspunten en valuta instelt.

## Prijsregels voor winkelwagentjes

Punten kunnen aan klanten worden beloond op basis van een [winkelwagentje](price-rules-cart.md). Zij kunnen als enige actie van de prijsregel, of samen met een korting worden beloond.

## Klantenbalans

Retourpuntsaldi kunnen worden beheerd door Admin-gebruikers per klant. Indien ingeschakeld in de winkel, kunnen klanten ook de details van hun puntbalans bekijken.

## Punten opnieuw instellen

>[!NOTE]
>
>[Reward Exchange Rates](reward-exchange-rates.md) configuratie is vereist voor de terugbetaling van bonuspunten door klanten en Admin-gebruikers tijdens het afrekenen.

Punten kunnen tijdens het uitchecken worden terugbetaald door Admin-gebruikers en -klanten (indien ingeschakeld). In de sectie Betalingsmethode wordt het selectievakje Mijn betalingspunten gebruiken boven de toegestane betalingsmethoden weergegeven. De beschikbare punten en de monetaire wisselkoers zijn inbegrepen. Als het beschikbare saldo groter is dan het totaal-generaal van de bestelling, is geen aanvullende betalingsmethode vereist. Het aantal bonuspunten dat op de bestelling wordt toegepast, wordt weergegeven met de ordertotalen, afgetrokken van het totaal-generaal, vergelijkbaar met winkelkrediet of cadeaukaarten. Als bonuspunten samen met winkelkrediet of een cadeaukaart worden gebruikt, worden de bonuspunten eerst afgetrokken. Het winkelkrediet of de cadeaukaart wordt vervolgens afgetrokken als het totaal van de bestelling groter is dan het terugvorderbare aantal bonuspunten.

>[!NOTE]
>
>Retourpunten worden niet aanbevolen voor gebruik bij CZV-aankopen, omdat de ontvangst van de betaling pas kan worden bevestigd nadat de bestelling is gefactureerd.

## Restitutie voor bonuspunten

Orders die met een bonuspositie zijn geplaatst, kunnen tot het in de order afgeloste bedrag worden terugbetaald op de beloningspunten. Op de [_Nieuwe creditnota_ page](../stores-purchase/credit-memo-create.md), kan het aantal punten worden vermeld dat op het saldo van de klant moet worden toegepast. Standaard bevat het veld het volledige aantal punten dat in de volgorde is gebruikt.

## Beloningspunten voor je winkel inschakelen

De configuratie van Punten van de Beloning bepaalt hoe de beloningspunten in de opslag worden voorgesteld en bepaalt de basiswerkende parameters.

![Configuratie van klanten - beloningspunten](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Stap 1. De bonuspunten configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Reward Points]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Reward Points]** en voer de volgende handelingen uit:

   - Als u bonuspunten wilt activeren, stelt u **[!UICONTROL Enable Reward Points Functionality]** tot `Yes`.

   - Om klanten toe te staan om hun eigen beloningspunten te verdienen, reeks **[!UICONTROL Enable Reward Points Functionality on Storefront]** tot `Yes`.

   - Om klanten toe te staan om een gedetailleerde geschiedenis van hun beloningen te zien, reeks **[!UICONTROL Customers May See Reward Point History]** tot `Yes`.

1. Voor **[!UICONTROL Reward Points Balance Redemption Threshold]**, voert u het aantal punten in dat moet worden opgebouwd voordat ze kunnen worden afgelost (minimaal leeg).

1. Voor **[!UICONTROL Cap Reward Points Balance At]**, voert u het maximum aantal punten in dat een klant mag bereiken (leeg laten voor geen limiet).

1. Voor **[!UICONTROL Reward Points Expire in (days)]** Voer het aantal dagen in voordat de bonuspunten verlopen (leeg laten voor niet verlopen).

1. Set **[!UICONTROL Reward Points Expiry Calculation]** op een van de volgende wijzen:

   - `Static` - Hiermee wordt de resterende levensduur van bonuspunten bepaald op basis van het aantal dagen dat is ingesteld in de configuratie. Als de vervallimiet in de configuratie verandert, verandert de vervaldatum van bestaande punten niet.

   - `Dynamic` - Berekent het resterende aantal dagen wanneer de beloningspunten stijgen. Als de vervallimiet in de configuratie verandert, wordt de vervaldatum van alle bestaande punten dienovereenkomstig bijgewerkt.

1. Als je de beschikbare bonuspunten automatisch wilt terugbetalen, stelt u **[!UICONTROL Refund Reward Points Automatically]** tot `Yes`.

1. Als u bonuspunten automatisch wilt aftrekken, stelt u **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** tot `Yes`.

1. Set **[!UICONTROL Landing Page]** op de inhoudspagina die uw beloningspunten programma verklaart.

   Zorg ervoor dat u de standaardpagina Punten voor beloningen bijwerkt met uw eigen informatie.

1. Klik op **[!UICONTROL Save Config]**.

### Stap 2. Punten die zijn verdiend voor klantactiviteiten configureren

In deze stap wordt het aantal beloningspunten gespecificeerd dat voor diverse klantenactiviteiten kan worden verdiend. Wanneer klanten een actie voltooien die toegewezen punten heeft, verschijnt een bericht aan de klant die op hoeveel punten wijst zij hebben verdiend.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Actions for Acquiring Reward Points by Customer]** sectie.

   ![Configuratie van klanten - acties voor het verwerven van bonuspunten door klant](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Om een bericht in het winkelwagentje te tonen dat de beloningspunten die voor de aankoop worden verdiend en de huidige beloningspunten van de klant omvatten, reeks **[!UICONTROL Purchase]** tot `Yes`.

   >[!NOTE]
   >
   >Om beloningspunten te verdienen voor hun _first_ bestelling, de klant moet worden geregistreerd _voor_ de transactie wordt door de betalingsmethode afgewikkeld. De meeste betalingsmethoden zouden kunnen worden geconfigureerd om transacties vast te leggen _automatisch_ wanneer de order is geplaatst, maar _voor_ de registratie van de klantenaccount is voltooid.

1. Voor **[!UICONTROL Registration]**, voert u het aantal punten in dat wordt verdiend voor het openen van een klantenaccount.

1. Voor **[!UICONTROL Newsletter Signup]**, voert u het aantal punten in dat wordt verdiend door geregistreerde klanten die zich op een nieuwsbrief abonneren.

1. Voor **[!UICONTROL Converting Invitation to Customer]**, ga het aantal punten in die door een klant worden verdiend die een uitnodiging verzendt en de ontvanger dan een klantenrekening opent.

   U kunt het aantal uitnodigingsomzettingen beperken die kunnen worden gebruikt om punten voor de klant te verdienen die de uitnodiging (leeg voor geen grens) verzendt. Voer hiertoe een getal in het dialoogvenster **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** veld.

1. Voor **[!UICONTROL Converting Invitation to Order]**, ga het aantal punten in die door een klant worden verdiend die een uitnodiging naar de ontvanger verzendt die dan een orde plaatst en het volgende doet:

   - Voor **Limiet voor aantal aanvragen voor omzetting van bestellingen**, ga het aantal punten in die door de klant worden verdiend die de uitnodiging verzendt wanneer de ontvanger een aanvankelijke orde (leeg voor geen grens) plaatst.

   - Voor **[!UICONTROL Invitation Conversion to Order Reward]**, selecteert u de `Each` optie om punten te verdienen voor elke geplaatst door ontvankelijke orde, of selecteer `First` optie om alleen punten te verdienen voor de eerste geplaatste order van de ontvanger.

1. Voor **[!UICONTROL Review Submission]** Voer het aantal punten in dat wordt verdiend door een klant die een revisie indient die is goedgekeurd voor publicatie.

1. Als u vervolgens het aantal beoordelingen wilt beperken dat kan worden gebruikt om punten per klant te verdienen, voert u het aantal in het dialoogvenster **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** veld (leeg laten voor geen limiet).

1. Klik op **[!UICONTROL Save Config]**.

### Stap 3. De instellingen voor e-mailmeldingen voltooien

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Email Notification Settings]** sectie.

   ![Configuratie van klanten - e-mailmeldingen met bonuspunten](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Email Sender]** aan de opslagcontactpersoon die wordt weergegeven als de afzender van balansupdates en vervalberichten.

1. Als u standaard klanten wilt abonneren om op de hoogte te worden gesteld van de balansupdates en de komende vervaldatums, stelt u **[!UICONTROL Subscribe Customers by Default]** tot `Yes`.

1. Set **[!UICONTROL Balance Update Email]** aan het malplaatje wordt gebruikt voor het bericht dat wordt verzonden naar klanten wanneer hun puntsaldo wordt bijgewerkt.

1. Set **[!UICONTROL Reward Points Expiry Warning Email]** aan het malplaatje voor het bericht wordt gebruikt dat naar klanten wordt verzonden wanneer de vervalgrens voor een partij van punten wordt bereikt.

1. Voor **[!UICONTROL Expiry Warning Before (days)]** Voer het aantal dagen in voordat de punten verlopen dat de melding is verzonden.

1. Klik op **[!UICONTROL Save Config]**.

## De balans van de beloningspunten bijwerken

De balans tussen beloningspunten kan worden bijgewerkt via de beheerder.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klant in het raster en klik op **[!UICONTROL Edit]** in de _[!UICONTROL Action]_kolom.

1. Onder _Klantgegevens_, kiest u de **[!UICONTROL Reward Points]** sectie.

1. Voer het aantal van **[!UICONTROL Update Points]**:

   - Als u het bedrag aan bonuspunten wilt bijwerken, voert u het getal in om het totale puntsaldo te verhogen.
   - Als u het bedrag aan bonuspunten wilt aftrekken, voert u het negatieve getal in dat u wilt gebruiken om het totale puntsaldo te verminderen.

1. Enter **[!UICONTROL Comments]** in verband met de correctie van de beloningspunten, indien nodig.

   ![Balans uitkeringspunten](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Abonneer de klant op _Punten terugsturen_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klik op **[!UICONTROL Save Customer]**.

Alle handelingen met betrekking tot bonuspunten worden weergegeven in de _[!UICONTROL Reward Points History]_blokkeren in hun account op de winkel.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Balance] | Huidig saldo van beloningspunten voor de cliënt |
| [!UICONTROL Amount Balance] | Het bedrag van het lopende kassaldo |
| [!UICONTROL Points] | Het aantal toegevoegde of afgetrokken punten |
| [!UICONTROL Amount] | Bedrag van toegevoegde of afgetrokken gelden |
| [!UICONTROL Rate] | De [wisselkoers](reward-exchange-rates.md) |
| [!UICONTROL Website] | Website waaraan de geschiedenis van bonuspunten wordt toegewezen |
| [!UICONTROL Reason] | Redenen voor de toekenning van punten:<br>**[!UICONTROL Making purchases]**— Telkens wanneer de klant een aankoop doet, kunnen ze punten verdienen.<br>**[!UICONTROL Registering on the site]** - Opgelopen bij registratie (eenmaal).<br>**[!UICONTROL Subscribing to a newsletter]**- Wordt opgebouwd voor het eerste abonnement (eenmaal).<br>**[!UICONTROL Sending Invitations]** — Verdien punten door hun vrienden uit te nodigen om zich bij de site aan te sluiten.<br>**[!UICONTROL Converting Invitations to Customer]**— Verdien punten voor elke uitnodiging die ze sturen, en belangrijke vrienden die zich op de site registreren.<br>**[!UICONTROL Converting Invitations to Order]** — Verdien punten voor elke verkoop die voortvloeien uit een verzonden uitnodiging.<br>**[!UICONTROL Review Submission]**— Verdien punten voor het indienen van productevaluaties. |
| [!UICONTROL Created] | Datum en tijdstip van de update van bonuspunten |
| [!UICONTROL Expired] | Aantal verlopen bonuspunten |
| [!UICONTROL Comment] | Opmerkingen bij het toevoegen of verwijderen van punten |

{style="table-layout:auto"}

## Bronnen voor probleemoplossing

Voor hulp bij het oplossen van problemen van beloningspunten, zie de volgende artikelen van de Kennisbank van de Steun van de Handel:

- [Loyalty&#39;s op gedeeltelijke orders](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404 fout - beloningspunten verwijderen bij afhandeling via meerdere verzendingen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
