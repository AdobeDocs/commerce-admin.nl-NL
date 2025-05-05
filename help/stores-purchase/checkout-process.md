---
title: Afhandelingsproces en opties
description: Leer hoe het afhandelingsproces van Adobe Commerce en Magento Open Source de benodigde informatie verzamelt om de transactie te voltooien en de pagina Afhandeling leidt de klant door elke stap van het proces.
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Afhandelingsproces en opties

Wanneer het uitcheckproces begint, verschuift de transactie naar een veilig, gecodeerd kanaal. Er wordt een hangslotsymbool weergegeven in de adresbalk van de browser en de URL verandert van `http` in `https` .

## Proces

Het doel voor het afrekenen is de informatie te verzamelen noodzakelijk om de transactie te voltooien. De _pagina van de Controle_ leidt de klant door elke stap van het proces. Klanten die zijn aangemeld bij hun accounts kunnen de afhandeling snel voltooien, omdat veel van de gegevens al in hun accounts staan. Klanten die zijn gekoppeld aan een bedrijfsaccount dat kooporders gebruikt, hebben een iets andere workflow.

### Verzending

De eerste stap van het afrekenproces is dat de klant de verzendadresgegevens invult en de verzendmethode kiest. Als de klant een account heeft, wordt het verzendadres automatisch ingevoerd, maar kan het indien nodig worden gewijzigd.

![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) het formaat van het straatadres voor de ontvanger en de afzender wordt bepaald door de eigenschappen van het [ attribuut van het klantenadres ](../customers/address-attributes.md). De instelling voor invoervalidatie bepaalt de geldige tekens die in een verzendadres kunnen worden gebruikt.

De voortgangsbalk boven aan de pagina volgt elke stap van het uitcheckproces en het overzicht van de volgorde toont aan dat de informatie die u tot nu toe hebt ingevoerd.

![ Verzendpagina tijdens het controleproces ](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### Naar een ander adres verzenden

1. Als er extra ingangen in het adresboek zijn, vindt de klant het adres waar de orde moet worden verscheept.

1. Klik op **[!UICONTROL Ship Here]** om het adres te selecteren.

#### Een adres toevoegen

1. Onder aan de sectie _[!UICONTROL Shipping Address]_&#x200B;klikt de klant op **[!UICONTROL + New Address]**.

1. Voltooit het _[!UICONTROL Shipping Address]_-formulier.

   Standaard worden de voor- en achternaam van de klant in eerste instantie in het formulier weergegeven.

   ![ de Verzendvorm van het Adres omvat naam en adresinformatie ](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. Om het nieuwe adres in het adresboek te bewaren, selecteert de klant checkbox bij de bodem van de vorm.

1. Klik op **[!UICONTROL Save Address]** .

   Het nieuwe adres is nu geselecteerd als het verzendadres.

   ![ het bewaarde adres wordt automatisch geselecteerd in de Verzendpagina ](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### Kies de verzendmethode

1. In de lijst van [ het verschepen ](delivery.md) methodes, kiest de klant de optie die zij willen gebruiken.

   ![ Verzendpagina toont het verschepen methodopties ](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Next]** om door te gaan.

### Controle en betalingen - Regelmatige bestelling

Tijdens de tweede stap van het controleproces, kiest de klant de [ betalingsmethode ](payments.md), en past om het even welke coupons met promotionele codes op de aankoop toe. Alle informatie kan worden gecontroleerd en indien nodig worden bewerkt. Indien ingeschakeld, moet de klant akkoord gaan met de verkoopvoorwaarden voordat de bestelling wordt geplaatst.

>[!NOTE]
>
>Hoewel Commerce het configureren van meerdere couponcodes toestaat, kan een klant slechts één couponcode op de kaart toepassen. (Zie de [ Codes van de Coupon ](../merchandising-promotions/price-rules-cart-coupon.md) voor meer informatie.)

![ Overzicht en betalingspagina tijdens controle ](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### Controle en betalingen - Inkooporder

![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B slechts)

Wanneer een klant met een bedrijf wordt geassocieerd dat [ kooporden ](../b2b/purchase-order-flow.md) heeft toegelaten, worden alle orden verwerkt als kooporders. De beschikbare betalingsmethoden worden bepaald door de instellingen van de bedrijfsaccount.

1. De klant selecteert een betalingsmethode.

   Wanneer het gebruiken van de _Betaling op de methode van de Rekening_, kan het [!UICONTROL Custom Reference Number] gebied worden gebruikt om een factuuraantal van verwijzingen te voorzien.

1. De klant klikt op **[!UICONTROL Place Purchase Order]** .

   De kooporder wordt geplaatst.

Als het bedrijf opstelling [ goedkeuringsregels ](../b2b/account-dashboard-approval-rules.md) heeft, gaat de kooporder door het goedkeuringsproces. Anders wordt het onmiddellijk verwerkt.

![ overzicht en betaling van de inkooporder van de Aankoop ](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### Aantal items dat wordt weergegeven in het orderoverzicht

Gebruikers van Admin kunnen het maximumaantal items dat bij het uitchecken in het orderoverzicht wordt weergegeven, wijzigen om de weergave met minder producten te stroomlijnen. Deze waarde is standaard ingesteld op 10.

![ Aantal punten die in de Samenvatting van de Orde worden getoond ](./assets/order-summary.png){width="700" zoomable="yes"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Options]** sectie uit.

1. Voer bij **[!UICONTROL Maximum Number of Items to Display in Order Summary]** het maximumaantal items in dat moet worden weergegeven.

1. Klik op **[!UICONTROL Save Config]**.

   Met deze update is het tijdens het afrekenen weergegeven overzicht van de bestelling beperkt tot het opgegeven aantal items.

### Bevestiging van bestelling

De bevestiging van de bestelling wordt weergegeven nadat de bestelling is geplaatst. Voor geregistreerde klanten bevat de pagina het ordernummer met een koppeling naar de account van de klant en een koppeling om een ontvangstbewijs te genereren. Geregistreerde klanten wordt verteld dat ze per e-mail informatie over het bevestigen en volgen van bestellingen moeten ontvangen. Gasten worden aangeraden een account te maken om de bestelling te volgen. Geregistreerde klanten kunnen een ontvangstbewijs produceren door een verbinding te klikken.

De pagina van de ordesbevestiging wordt ook genoemd het _Succes_ pagina, en door analyseprogramma&#39;s gebruikt om omzettingen te volgen.

![ de vertoningen van de Bevestiging van de Orde een succesbericht en ordeaantal ](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## Opties voor uitchecken

De opties voor uitchecken bepalen verschillende kenmerken voor de uitcheckpagina, waaronder de lay-out. Er zijn opties die u kunt configureren om beperkingen op het afrekenen te plaatsen, waaronder het toestaan van uitchecken door gasten en het afdwingen van een overeenkomst met voorwaarden. Er zijn ook opties voor het beheren van de weergave van informatie tijdens het uitrekenen.

![ Configuratie - controleopties ](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Opties van de Controle ](../configuration-reference/sales/checkout.md#checkout-options) in de _Gids van de Verwijzing van de Configuratie_.

### De opties voor uitchecken wijzigen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .
1. Stel de volgende opties naar wens in.
1. Klik op **[!UICONTROL Save Config]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Options]** sectie uit.

1. Als de montages voor een specifieke opslagmening zijn, [ kies de opslagmening ](../configuration-reference/scope-change.md#set-the-scope) waar de configuratie van toepassing is.

   Klik op **[!UICONTROL OK]** als u daarom wordt gevraagd om door te gaan.

1. Stel de uitcheckopties in.

1. Klik op **[!UICONTROL Save Config]**.

### Beschikbare opties voor uitchecken

| Veld | [ Reikwijdte ](../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | Winkelweergave | Bepaalt als [ één-pagina controle ](checkout-one-page.md) het standaardcontrolemateriaal is. Opties: Ja/Nee |
| [!UICONTROL Allow Guest Checkout] | Winkelweergave | Bepaalt als de gasten door [ controle kunnen gaan zonder ](checkout-guest.md) voor een rekening met uw opslag te registreren. Opties: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Winkelweergave | Bepaalt als de klanten worden vereist om met de [ Voorwaarden ](terms-and-conditions.md) van de verkoop in te stemmen alvorens een aankoop te doen. Opties: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Winkelweergave | Hiermee bepaalt u de locatie van het factuuradres tijdens het afrekenen. Opties: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Winkelweergave | Hiermee bepaalt u het maximumaantal items dat tijdens het uitchecken in het overzicht van de volgorde kan worden weergegeven. De standaardwaarde is `10` . |
| [!UICONTROL Enable Address Search] | Website | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) bepaalt als de klanten [ functionaliteit van het adresonderzoek ](checkout-address-search.md) voor _het verschepen_ kunnen gebruiken, en de _Controle &amp; de stappen van de Betalingen_. Wanneer deze functie is ingeschakeld, gebruikt u _[!UICONTROL Number of Customer Addresses Limit]_&#x200B;om het aantal opgeslagen adressen in te stellen dat is vereist om deze functie te activeren tijdens het uitchecken. Opties: `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | Website | ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) wanneer het adresonderzoek **[!UICONTROL Enabled]** is, bepaalt het aantal bewaarde adressen die worden vereist om deze functionaliteit tijdens controle te activeren. Wanneer het aantal van de klant bewaarde adressen samenkomt of dit aantal overschrijdt, slechts wordt het standaardadres teruggegeven op de _Verschepende_ en _Controle &amp; de stappen van de Betalingen_. De klant kan een zoekfunctie gebruiken om het geselecteerde adres te wijzigen. De standaardwaarde is 10. |

{style="table-layout:auto"}
