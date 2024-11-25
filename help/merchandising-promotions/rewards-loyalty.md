---
title: Programma's voor beloningen en loyaliteit
description: Leer over het systeem van beloningspunten dat u kunt gebruiken om klantenovereenkomst te drijven en klantenloyaliteit te bevorderen.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1389'
ht-degree: 0%

---

# Programma&#39;s voor beloningen en loyaliteit

{{ee-feature}}

Het _beloningspunten_ systeem in Adobe Commerce geeft u de capaciteit om unieke programma&#39;s uit te voeren die klantenovereenkomst drijven en klantenloyaliteit bevorderen. Punten kunnen worden toegekend voor een breed scala aan transactie- en klantactiviteiten en de configuratie kan worden ingesteld om de punttoewijzing, het saldo en de vervaldatum te bepalen. Klanten kunnen punten in de richting van aankopen inwisselen op basis van de omrekeningskoers die u tussen bonuspunten en valuta instelt.

## Prijsregels voor winkelwagentjes

De punten kunnen aan klanten worden beloond die op de regel van het a [ winkelwagentje ](price-rules-cart.md) worden gebaseerd. Zij kunnen als enige actie van de prijsregel, of samen met een korting worden beloond.

## Klantenbalans

Retourpuntsaldi kunnen worden beheerd door Admin-gebruikers per klant. Indien ingeschakeld in de winkel, kunnen klanten ook de details van hun puntbalans bekijken.

## Punten opnieuw instellen

>[!NOTE]
>
>](reward-exchange-rates.md) de configuratie van de Tarieven van de Uitwisseling van 0} wordt de Winst {vereist voor terugbetaling van beloningspunten door klanten en gebruikers Admin tijdens controle.[

Punten kunnen tijdens het uitchecken worden terugbetaald door Admin-gebruikers en -klanten (indien ingeschakeld). In de sectie Betalingsmethode wordt het selectievakje Mijn betalingspunten gebruiken boven de toegestane betalingsmethoden weergegeven. De beschikbare punten en de monetaire wisselkoers zijn inbegrepen. Als het beschikbare saldo groter is dan het totaal-generaal van de bestelling, is geen aanvullende betalingsmethode vereist. Het aantal bonuspunten dat op de bestelling wordt toegepast, wordt weergegeven met de ordertotalen, afgetrokken van het totaal-generaal, vergelijkbaar met winkelkrediet of cadeaukaarten. Als bonuspunten samen met winkelkrediet of een cadeaukaart worden gebruikt, worden de bonuspunten eerst afgetrokken. Het winkelkrediet of de cadeaukaart wordt vervolgens afgetrokken als het totaal van de bestelling groter is dan het terugvorderbare aantal bonuspunten.

>[!NOTE]
>
>Retourpunten worden niet aanbevolen voor gebruik bij CZV-aankopen, omdat de ontvangst van de betaling pas kan worden bevestigd nadat de bestelling is gefactureerd.

## Restitutie voor bonuspunten

Orders die met een bonuspositie zijn geplaatst, kunnen tot het in de order afgeloste bedrag worden terugbetaald op de beloningspunten. Op het [_Nieuwe Memo van het Krediet_ pagina ](../stores-purchase/credit-memo-create.md), kan het aantal punten dat op het saldo van de klant moet worden toegepast worden ingegaan. Standaard bevat het veld het volledige aantal punten dat in de volgorde is gebruikt.

## Beloningspunten voor je winkel inschakelen

De configuratie van Punten van de Beloning bepaalt hoe de beloningspunten in de opslag worden voorgesteld en bepaalt de basiswerkende parameters.

![ configuratie van Klanten - beloningspunten ](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Stap 1. De bonuspunten configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Reward Points]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Reward Points]** sectie uit en doe het volgende:

   - Stel **[!UICONTROL Enable Reward Points Functionality]** in op `Yes` om bonuspunten te activeren.

   - Stel **[!UICONTROL Enable Reward Points Functionality on Storefront]** in op `Yes` om klanten toe te staan hun eigen bonuspunten te verdienen.

   - Stel **[!UICONTROL Customers May See Reward Point History]** in op `Yes` als u klanten een gedetailleerde geschiedenis van hun beloningen wilt laten zien.

1. Voer bij **[!UICONTROL Reward Points Balance Redemption Threshold]** het aantal punten in dat moet worden opgehaald voordat ze kunnen worden afgelost (leeg voor een minimum).

1. Voer bij **[!UICONTROL Cap Reward Points Balance At]** het maximumaantal punten in dat een klant mag bereiken (leeg laten voor geen limiet).

1. Voer voor **[!UICONTROL Reward Points Expire in (days)]** het aantal dagen in voordat de bonuspunten verlopen (leeg laten voor geen vervaldatum).

1. Stel **[!UICONTROL Reward Points Expiry Calculation]** in op een van de volgende opties:

   - `Static` - Bepaalt de resterende levensduur van beloningspunten die op het aantal dagen worden gebaseerd in de configuratie worden geplaatst. Als de vervallimiet in de configuratie verandert, verandert de vervaldatum van bestaande punten niet.

   - `Dynamic` - Berekent het resterende aantal dagen wanneer de evenwicht van het beloningspunt stijgt. Als de vervallimiet in de configuratie verandert, wordt de vervaldatum van alle bestaande punten dienovereenkomstig bijgewerkt.

1. Stel **[!UICONTROL Refund Reward Points Automatically]** in op `Yes` als u de beschikbare bonuspunten automatisch wilt terugbetalen.

1. Stel **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** in op `Yes` om te voorkomen dat bonuspunten die via aankopen worden verdiend, volledig of gedeeltelijk worden terugbetaald.

   >[!NOTE]
   >
   >Alleen de punten die zijn verdiend met de volgorde die wordt terugbetaald, worden beïnvloed.

1. Stel **[!UICONTROL Landing Page]** in op de inhoudspagina waarin uw bonuspuntprogramma wordt uitgelegd.

   Zorg ervoor dat u de standaardpagina Punten voor beloningen bijwerkt met uw eigen informatie.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Stap 2. Punten die zijn verdiend voor klantactiviteiten configureren

In deze stap wordt het aantal beloningspunten gespecificeerd dat voor diverse klantenactiviteiten kan worden verdiend. Wanneer klanten een actie voltooien die toegewezen punten heeft, verschijnt een bericht aan de klant die op hoeveel punten wijst zij hebben verdiend.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Actions for Acquiring Reward Points by Customer]** sectie uit.

   ![ configuratie van Klanten - acties voor het verwerven van beloningspunten door klant ](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Om beloningspunten toe te staan die voor de aankopen worden verdiend op de gevormde [ Winst Tarieven van de Uitwisseling ](reward-exchange-rates.md) worden gebaseerd, plaats **[!UICONTROL Purchase]** aan `Yes`.

   >[!NOTE]
   >
   >Om beloningspunten voor hun _eerste_ orde te verdienen, moet de klant _worden geregistreerd alvorens_ de transactie door de betalingsmethode wordt gevangen. De meeste betalingsmethodes zouden kunnen worden gevormd om transacties _automatisch_ te vangen wanneer de orde wordt geplaatst, maar _alvorens_ de registratie van de klantenrekening wordt gebeëindigd.

1. Voer bij **[!UICONTROL Registration]** het aantal punten in dat wordt verdiend voor het openen van een klantenaccount.

1. Voer voor **[!UICONTROL Newsletter Signup]** het aantal punten in dat wordt verdiend door geregistreerde klanten die zich abonneren op een nieuwsbrief.

1. Voer voor **[!UICONTROL Converting Invitation to Customer]** het aantal punten in dat een klant heeft verdiend die een uitnodiging verzendt en de ontvanger opent vervolgens een klantenaccount.

   U kunt het aantal uitnodigingsomzettingen beperken die kunnen worden gebruikt om punten voor de klant te verdienen die de uitnodiging (leeg voor geen grens) verzendt. Voer hiertoe een getal in het veld **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** in.

1. Voer voor **[!UICONTROL Converting Invitation to Order]** het aantal punten in dat wordt verdiend door een klant die een uitnodiging verzendt naar de ontvanger die vervolgens een bestelling plaatst en die het volgende doet:

   - Voor **Uitnodiging om de Limiet van de Hoeveelheid van de Omzetting van de Orde** in te orde, ga het aantal punten in die door de klant worden verdiend die de uitnodiging verzendt wanneer de ontvanger een aanvankelijke orde (leeg voor geen grens) plaatst.

   - Selecteer bij **[!UICONTROL Invitation Conversion to Order Reward]** de optie `Each` om punten te verdienen voor elke geplaatste volgorde van ontvangers of selecteer de optie `First` om alleen punten te verdienen voor de eerste geplaatste volgorde van de ontvanger.

1. Voer bij **[!UICONTROL Review Submission]** het aantal punten in dat een klant heeft verdiend die een revisie verzendt die is goedgekeurd voor publicatie.

1. Als u vervolgens het aantal revisies wilt beperken dat kan worden gebruikt om punten per klant te verdienen, voert u het nummer in het veld **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** in (leeg laten voor geen limiet).

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Stap 3. De instellingen voor e-mailmeldingen voltooien

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Email Notification Settings]** sectie uit.

   ![ configuratie van Klanten - beloningspunten e-mailberichten ](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Email Sender]** in op de contactpersoon van de winkel die wordt weergegeven als de afzender van balansupdates en vervalberichten.

1. Stel **[!UICONTROL Subscribe Customers by Default]** in op `Yes` als u klanten standaard wilt abonneren op het ontvangen van een melding over balansupdates en aanstaande vervaldatums.

1. Stel **[!UICONTROL Balance Update Email]** in op de sjabloon die wordt gebruikt voor het bericht dat naar klanten wordt verzonden wanneer hun puntbalans wordt bijgewerkt.

1. Stel **[!UICONTROL Reward Points Expiry Warning Email]** in op de sjabloon die wordt gebruikt voor het bericht dat naar klanten wordt verzonden wanneer de vervallimiet voor een batch punten is bereikt.

1. Voer voor **[!UICONTROL Expiry Warning Before (days)]** het aantal dagen in voordat de punten verlopen dat de melding wordt verzonden.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## De balans van de beloningspunten bijwerken

De balans tussen beloningspunten kan worden bijgewerkt via de beheerder.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klant in het raster en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Onder _Informatie van de Klant_, kies de **[!UICONTROL Reward Points]** sectie.

1. Voer het getal **[!UICONTROL Update Points]** in:

   - Als u het bedrag aan bonuspunten wilt bijwerken, voert u het getal in om het totale puntsaldo te verhogen.
   - Als u het bedrag aan bonuspunten wilt aftrekken, voert u het negatieve getal in dat u wilt gebruiken om het totale puntsaldo te verminderen.

1. Voer indien nodig **[!UICONTROL Comments]** in voor de aanpassing van de bonuspunten.

   ![ het Saldo van Punten van de Terugkeer ](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Naar keuze, abonneer de klant aan _de Berichten van Punten van de Beloning_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klik op **[!UICONTROL Save Customer]**.

Alle acties met betrekking tot bonuspunten worden weergegeven in het _[!UICONTROL Reward Points History]_-blok van de klant in hun account op de winkel.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Balance] | Huidig saldo van beloningspunten voor de cliënt |
| [!UICONTROL Amount Balance] | Het bedrag van het lopende kassaldo |
| [!UICONTROL Points] | Het aantal toegevoegde of afgetrokken punten |
| [!UICONTROL Amount] | Bedrag van toegevoegde of afgetrokken gelden |
| [!UICONTROL Rate] | De [ beloningswisselkoers ](reward-exchange-rates.md) |
| [!UICONTROL Website] | Website waaraan de geschiedenis van bonuspunten wordt toegewezen |
| [!UICONTROL Reason] | Redenen voor het toekennen van punten:<br>**[!UICONTROL Making purchases]**— Telkens als de klant een aankoop maakt, kunnen zij punten verdienen.<br>**[!UICONTROL Registering on the site]** - Wordt opgeladen bij registratie (eenmaal).<br>**[!UICONTROL Subscribing to a newsletter]**- Wordt opgevraagd voor het eerste abonnement (eenmaal).<br>**[!UICONTROL Sending Invitations]** — Verdien punten door hun vrienden uit te nodigen om zich bij de site aan te sluiten.<br>**[!UICONTROL Converting Invitations to Customer]**— Verdien punten voor elke uitnodiging die ze verzenden, en belangrijke vrienden die zich op de site registreren.<br>**[!UICONTROL Converting Invitations to Order]** — Verdien punten voor elke verkoop resulterend uit een verzonden uitnodiging.<br>**[!UICONTROL Review Submission]**— Verdien punten voor het indienen van productrevisies. |
| [!UICONTROL Created] | Datum en tijdstip van de update van bonuspunten |
| [!UICONTROL Expired] | Aantal verlopen bonuspunten |
| [!UICONTROL Comment] | Opmerkingen bij het toevoegen of verwijderen van punten |

{style="table-layout:auto"}

## Bronnen voor probleemoplossing

Raadpleeg de volgende artikelen in de Commerce Support Knowledge Base voor hulp bij het oplossen van problemen met beloningspunten:

- [ 404 fout - het verwijderen van beloningspunten op multi-verschepende controle ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
