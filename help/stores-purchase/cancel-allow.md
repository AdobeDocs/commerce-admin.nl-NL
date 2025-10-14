---
title: Annuleren van bestelling toestaan
description: Leer hoe u uw klanten annuleringsmogelijkheden biedt.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Annuleren van bestelling toestaan

Als deze optie is ingeschakeld, kunt u een bestelling rechtstreeks vanaf de account van de klant annuleren. Annuleren is standaard uitgeschakeld.

## Criteria voor annulering die moeten worden ingeschakeld voor een bestelling

- _toestaat annuleer de configuratieoptie van de Orde_ moet worden toegelaten.

- Als de volgorde de status `Hold`, `Canceled`, `Complete` of `Closed` heeft, wordt de optie Annuleren uitgeschakeld in de winkel.

- Als een van de items in de bestelling is verzonden, is de optie Annuleren uitgeschakeld in de winkel.

- Als er een object is betaald, is de optie Annuleren ingeschakeld en wordt de restitutie voor dat object gemaakt.

- Als de volgorde de status `Pending` of `Processing` heeft, wordt de optie Annuleren ingeschakeld in de winkel.

## Configureren om annulering door klanten toe te staan en de annuleringsredenen aan te passen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en selecteer **[!UICONTROL Sales]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Order cancellation]** sectie uit.

   ![&#x200B; de annuleringsopties van de Orde &#x200B;](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Order cancellation through GraphQL]** in op `Yes` .

   Met deze instelling wordt de functionaliteit voor annuleren ingeschakeld vanuit de klantenaccount in de winkel.

1. In **[!UICONTROL Order Order cancellation reasons]** kunt u annuleringsredenen toevoegen, verwijderen of wijzigen.

   Met deze instelling worden annuleringsredenen weergegeven in de winkel aan de klant wanneer deze een bestelling annuleert.
Zorg ervoor dat u ten minste één reden hebt opgegeven.

1. Klik op **[!UICONTROL Save Config]**.

## Annuleren vanuit de winkel

Een klant kan de functie voor annuleren voor een specifieke bestelling starten op drie pagina&#39;s:

- _Mijn Orden_ pagina

- _de Mening van de Orde_ pagina

- _Mijn Rekening_ pagina

### Mijn bestellingen

_annuleert de knoop van de Orde_ wordt getoond in de Mijn pagina van Orden als de orde kan worden geannuleerd.

![&#x200B; storefront van het Voorbeeld - Mijn pagina van Orden &#x200B;](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Weergavepagina Volgorde

_annuleert de knoop van de Orde_ wordt getoond in de pagina van de Orde van de Mening als de orde kan worden geannuleerd.

![&#x200B; de detailpagina van de Orde &#x200B;](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mijn account

_annuleert de knoop van de Orde_ wordt getoond in de Recente sectie van Orden van de Mijn pagina van de Rekening, als de orde kan worden geannuleerd.

![&#x200B; Mijn pagina van de Rekening &#x200B;](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
