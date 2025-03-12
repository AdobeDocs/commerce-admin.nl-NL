---
title: Direct aanschaffen
description: Klik hier als je wilt weten hoe je direct kunt kopen en hoe je een snelle afhandeling voor geregistreerde klantenaccounts kunt aanbieden.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Direct aanschaffen

_Onmiddellijke Aankoop_ staat klanten toe om door het controleproces te versnellen gebruikend informatie die in hun rekening wordt bewaard. Wanneer toegelaten, verschijnt de _Onmiddellijke knoop van de Aankoop_ onder _toevoegt aan Kaart_ knoop op de productpagina voor klanten die aan de vereisten voldoen.

![ pagina van het Product met de Onmiddellijke getoonde optie van de Aankoop ](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Klantvereisten

- De klant wordt [ binnen ondertekend ](../customers/customer-sign-in.md) aan hun rekening.

- De rekening van de klant heeft a [ standaard het factureren en het verschepen adres ](../customers/account-dashboard-address-book.md).

- Minstens één [ verschepende methode ](delivery.md) is beschikbaar voor het land dat in het standaard verschepende adres wordt gespecificeerd.

- De rekening van de klant heeft a [ opgeslagen betalings ](../stores-purchase/stored-payment-methods.md) methode met toegelaten kluis.

  De volgende betalingsmethoden kunnen worden gebruikt om beveiligde toegang tot opgeslagen creditcardgegevens te bieden:

   - [ de Kredietkaarten van Braintree ](braintree.md) (De Onmiddellijke Aankoop kan niet met de Kredietkaarten van Braintree worden gebruikt als 3D Veilig wordt toegelaten.)
   - [Braintree met PayPal ingeschakeld](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Directe aankoop op de winkel

1. In de winkel gaat de klant naar de productpagina van het aan te schaffen object.

1. Hiermee selecteert u de gewenste opties en klikt u op **[!UICONTROL Instant Purchase]** .

   ![ de dialoog van de Bevestiging om de onmiddellijke aankoop te bevestigen ](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Hiermee controleert u de **[!UICONTROL Instant Purchase Confirmation]** informatie en klikt u op **[!UICONTROL OK]** om de transactie te voltooien.

   Boven aan de productpagina worden een bevestigingsbericht en een bestelnummer weergegeven.

## Directe aankoop configureren

### Stap 1: Open de configuratiepagina

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Stap 2: De vault van de betalingsmethode configureren

U kunt Direct aanschaffen met Braintree of Betalingsservices voor Adobe Commerce en Magento Open Source gebruiken. Vaulting moet zijn ingeschakeld voordat een winkelier de functie Onmiddellijk kopen kan gebruiken.

Leer hoe u de betalingsmethode configureert en archivering voor Braintree of Betalingsservices inschakelt:

- [Braintree](braintree.md)
- [ documentatie van de Diensten van de Betaling ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)

### Stap 3: Directe aankoop inschakelen

1. Kies **[!UICONTROL Sales]** in het linkerdeelvenster onder de sectie _[!UICONTROL Sales]_.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Instant Purchase]** sectie uit.

1. Als deze verandering voor een specifieke opslagmening is, [ kies de opslagmening ](../configuration-reference/scope-change.md#set-the-scope) waar de configuratie van toepassing is.

   Klik op **[!UICONTROL OK]** als u daarom wordt gevraagd om door te gaan.

1. Stel **[!UICONTROL Enabled]** in op `Yes` .

1. Voer de **[!UICONTROL Button Text]** in die u op de knop wilt weergeven.

   De knoptekst kan voor elke winkelweergave of taal worden gewijzigd. Standaard is de knoptekst `Instant Purchase` .

   ![ Configuratie - onmiddellijke aankoopopties ](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Onmiddellijke Aankoop ](../configuration-reference/sales/sales.md#instant-purchase) in de _Gids van de Verwijzing van de Configuratie_.

1. Klik op **[!UICONTROL Save Config]**.

1. Wanneer u wordt gevraagd de cache bij te werken, klikt u op **[!UICONTROL Cache Management]** in het systeembericht en volgt u de instructies om de cache leeg te maken.
