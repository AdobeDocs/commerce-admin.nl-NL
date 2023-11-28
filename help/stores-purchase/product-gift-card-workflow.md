---
title: Aankoop en terugbetaling van creditcard
description: Meer informatie over de levenscyclus voor aankopen en terugbetalen van cadeaukaarten wanneer u cadeaukaarten opneemt in uw winkelcatalogus.
exl-id: ecaa39aa-f504-4bfd-874b-12b44093c2a9
feature: Products, Gift
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Aankoop en terugbetaling van creditcard

{{ee-feature}}

Cadeaukaarten worden in het winkelwagentje afgelost, net zoals bij een bestelling een coupon wordt gebruikt. Tijdens het afrekenen voert de verkoper de code van de cadeaukaart in om een bedrag van de cadeaukaart op de aankoop toe te passen. Cadeauhouders die een klantenaccount hebben, kunnen de status en het resterende saldo controleren vanaf het dashboard van hun account. Enkelvoudige en meervoudige cadeaukaarten kunnen worden gebruikt om een bestelling geheel of gedeeltelijk te betalen.

De toegepaste kaartencode kan worden weergegeven door de volgorde in de _Beheerder_, zodat u de code zo nodig kunt ophalen en op een fysieke cadeaukaart kunt plaatsen. Als een kaartopdracht voor cadeautjes wordt geannuleerd of terugbetaald, moet u het bijbehorende kaartenaccount handmatig annuleren. U kunt het account volledig verwijderen of deactiveren.

![Cadeaudetails in winkelwagen](./assets/storefront-gift-card-order-customer-account.png){width="700" zoomable="yes"}

Zo kan een klant die in de demo Luma-winkel winkelt, een virtuele of fysieke cadeaukaart kopen.

**Virtuele cadeaukaart** - Een virtuele cadeaukaart voor een luminantie wordt per e-mail verzonden met een optioneel bericht aan de ontvanger. Het kan op om het even welke familie van Luma van websites worden terugbetaald en nooit verlopen.

**Fysieke cadeaukaart** - Een cadeaukaart voor een luminantie wordt verpakt in een aangepaste illustratiemailer en wordt kosteloos naar de ontvanger verzonden. Het kan vooraf worden geproduceerd, geëtiketteerd met unieke codes, en in opslag, telefonisch, of op om het even welke familie van Luma van websites worden ingewisseld. Het vervalt nooit.

**Gecombineerde cadeaukaart** - Een gecombineerde cadeaukaart heeft de kenmerken van zowel een virtuele als een fysieke cadeaukaart. Een Luma-gecombineerde cadeaukaart wordt verzonden en naar de ontvanger gemaild. Het e-mailadres en het verzendadres zijn vereist tijdens de aankoop van de cadeaukaart. Het vervalt nooit.

## Levenscyclus van creditcard

1. **De klant bepaalt de waarde van de cadeau-kaart**.

   De klant bepaalt de waarde van de cadeaukaart op de productpagina. Afhankelijk van de configuratie is er een vast prijsveld, een lijst met prijsopties of beide. Alle bedragen worden weergegeven in de valuta die in de winkel wordt gebruikt.

1. **De klant voltooit de creditcardgegevens**.

   Voor een fysieke cadeaukaart voert de klant de **Naam afzender** en **Naam ontvanger**. Voor virtuele of gecombineerde cadeaukaarten voert de klant ook de **E-mail afzender** en **E-mail ontvanger**. Als de klant is aangemeld, wordt de naam van de afzender (en, indien van toepassing, de e-mail van de afzender) automatisch van hun account ingevoerd. Afhankelijk van de configuratie, zou de klant een bericht aan de ontvanger ook kunnen ingaan.

1. **Klant voltooit afhandeling**.

   De cadeaukaart wordt weergegeven als een lijstitem in het winkelwagentje met details waarop de naam van de afzender, de ontvanger en het bericht wordt weergegeven, indien van toepassing. Het bedrag dat aan de cadeaukaart is gekoppeld, wordt omgezet in de basisvaluta van de winkel wanneer deze aan de winkelwagen wordt toegevoegd.

1. **De klant ontvangt bevestiging van de bestelling**.

   De koper van de cadeau-kaart kan op de koppeling in de bevestiging klikken om de bestelling van het dashboard van de account bij te houden.

1. **De ontvanger ontvangt de cadeaukaart**.

   Voor virtuele of gecombineerde cadeaukaarten ontvangt de ontvanger een e-mail met de code van de cadeau-kaart, de naam van de afzender en, indien van toepassing, het bericht. Als meerdere cadeaukaarten in één bestelling worden aangeschaft en het type virtueel of gecombineerd is, worden alle overeenkomende kaartcodes in één e-mail naar de ontvanger verzonden. Fysieke cadeaukaarten kunnen rechtstreeks naar de ontvanger of naar de klant worden verzonden, die de kaartje vervolgens persoonlijk aan de ontvanger kan afgeven.

1. **Ontvanger past cadeaukaart toe op aankoop**.

   De ontvanger koopt een object in je winkel en past de code van de cadeau-kaart toe tijdens het afrekenen. Telkens wanneer een cadeaukaart wordt toegepast tijdens het afrekenen, wordt het bedrag weergegeven in het vak met de totalen van de bestelling en wordt het bedrag afgetrokken van het totaal-generaal. Het volledige saldo van elke cadeaukaart wordt afgetrokken van het totaal van de winkelwagentjes. Als voor een aankoop meerdere cadeaukaarten worden gebruikt, worden deze in oplopende volgorde toegepast, te beginnen met de kaart met het kleinst resterende saldo, totdat alles wordt toegepast of het totaal-generaal nul is. Wanneer het totaal van de cadeaus nul bereikt, wordt het laatste geschenkkaartaccount dat op het winkelwagentje is toegepast, gedeeltelijk afgetrokken. Kaarten die niet op de wagen zijn aangebracht, worden niet in mindering gebracht op het saldo. De bedragen worden pas afgetrokken van de rekeningen van de cadeau-kaart nadat de bestelling is geplaatst.

## Storefront-ervaring

Hoe cadeaukaarten werken op de winkel:

- De code van de cadeau-kaart kan worden toegepast in het winkelwagentje of bij de kassa om het totale bedrag van de bestelling te dekken.

- In de catalogus wordt een cadeaukaart weergegeven als een afzonderlijk type product.

- De code van de cadeaukaart wordt geactiveerd nadat de bestelling is gefactureerd. Als de bestelling niet wordt betaald, kan de ontvangende klant de kaartje niet gebruiken.

- Accounts voor cadeaucodes worden gemaakt om de balans van een specifieke voucher bij te houden. Een opslagbeheerder kan de balans handmatig aanpassen.

De ontvangende klant kan de _[!UICONTROL Gift Card]_afdeling van hun rekeningdashboard om het saldo van hun [kaartenaccount](product-gift-card-accounts.md) en cadeaukaarten inwisselen voor [winkelkrediet](../customers/store-credit-using.md).

![Cadeaukaart](./assets/account-dashboard-gift-card.png){width="700" zoomable="yes"}

### De status en balans van de cadeaukaart controleren

1. Vanuit de winkel, meldt de klant zich aan en opent hij zijn pagina van de klantenrekening.

1. De klant opent de **[!UICONTROL Gift Card]** pagina en voert code van cadeaukaart in.

1. De klant klikt **[!UICONTROL Check status and balance]**.

![Balans kaartje](./assets/gift-balance.png){width="700" zoomable="yes"}

De balans van de cadeaukaart wordt weergegeven.

### Activering van creditcard

1. Op de _[!UICONTROL Gift Card]_pagina, voert de klant code voor cadeaukaarten in.

1. De klant klikt **[!UICONTROL Redeem Gift Card]**.

![Bericht over geslaagde activering van de cadeaukaart](./assets/gift-redeemed-balance.png){width="700" zoomable="yes"}

Het bedrag van de creditcard wordt geactiveerd en toegevoegd aan het totale creditsaldo van de winkel.

![Winkelcreditsaldo](./assets/store-credit.png){width="700" zoomable="yes"}

Alle bewerkingen voor het saldo van de cadeau-kaart zijn beschikbaar op het tabblad _[!UICONTROL Store Credit]_pagina.

### Een cadeaukaart toepassen tijdens het afrekenen

Als de cadeaukaart niet kan worden terugbetaald, kan een klant de code van de cadeau-kaart tijdens het afrekenen toepassen.

1. Tijdens de _Reviseren en betalen_ stap, de klant klikt **[!UICONTROL Apply Gift Card]**.

1. Voer de code voor de cadeau-kaart in en klik vervolgens op **[!UICONTROL Apply]**.

   De korting moet in de _[!UICONTROL Order Summary]_.

1. Klikken **[!UICONTROL Place Order]** om de bestelling af te ronden.
