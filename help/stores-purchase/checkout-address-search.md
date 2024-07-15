---
title: Adreszoekopdracht bij afhandeling
description: Leer hoe je adreszoekopdrachten kunt opnemen bij het afrekenen in je winkel.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Adreszoekopdracht bij afhandeling

{{ee-feature}}

Uw klanten zouden vele bewaarde adressen en informatie in hun adresboek kunnen hebben, vooral regelmatige, terugkerende klanten of bedrijven die veelvoudige orden en verzendplaatsen ingaan. Het weergeven van vele adressen kan het laden van de kassa en de processen aanzienlijk vertragen en tot een negatieve het winkelervaring leiden. Om de responsiviteit van het afrekenen te helpen verhogen, wordt aanbevolen om adreszoekopdrachten voor uw site te activeren en te configureren.

>[!NOTE]
>
>Adreszoekopdracht is niet standaard ingeschakeld. U kunt deze functie zo configureren dat deze de functionaliteit op uw site bevat.

Wanneer deze eigenschap wordt toegelaten en het aantal van de klant bewaarde adressen samenkomt of de gevormde grens overschrijdt, _het verschepen_ en _Controle &amp; de stappen van de Betalingen_ tonen slechts één adres (het gebrek). De klant kan het geselecteerde adres veranderen door **Adres van de Verandering** te klikken en dan het zoeken naar het correcte adres door stad, staat, straat, of zip. Deze functie ondersteunt ook adresselectie voor uitchecken van cadeauregisters.

![ Afhandeling met bewaarde verschepende getoonde adressen ](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Als de klant geen standaard verschepend adres heeft, _het verschepen_ paginasvertoningen _Geen geselecteerd adres_. In dit geval, moet de klant **Adres van de Verandering** klikken om een bewaard adres te selecteren of **Nieuw Adres** te klikken om een adres toe te voegen en te selecteren alvorens met de controle te werk te gaan. Als de klant geen standaard facturerend adres heeft, toont de _Overzicht &amp; van betalingen_ pagina het adres dat voor het verschepen samen met de _optie van het Adres van de Verandering_ wordt geselecteerd.

![ Controle met geen adres geselecteerd bericht ](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Zoeken naar aanhalingstekens met vergrendeld adres

![ Adobe Commerce B2B ](../assets/b2b.svg) (Beschikbaar met Adobe Commerce B2B slechts)

Het toelaten van adresonderzoek beïnvloedt ook de controle voor orden die van citaten worden gecreeerd waar het aantal van de klant bewaarde adressen of de gevormde grens ontmoet overschrijdt. Wanneer de prijsopgave is voltooid en de klant doorgaat naar de kassa, wordt alleen het geselecteerde verzendadres weergegeven. Op de pagina wordt ook een bericht weergegeven dat het verzendadres vergrendeld is en alleen in de prijsopgave kan worden gewijzigd.

![ Verzendadres dat voor een citaat wordt gesloten ](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Zoeken naar adressen inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Options]** sectie uit.

   ![ Configuratie - de Opties van de Controle ](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [ Opties van de Controle ](../configuration-reference/sales/checkout.md#checkout-options) in de _Gids van de Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Enable Address Search]** in op `Yes` .

1. Stel de optie **[!UICONTROL Number of Customer Addresses Limit]** in om de drempel voor het opnemen van de zoekfunctie voor adressen op te geven.

   Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om deze wijziging aan te brengen.

   Wanneer het aantal van de klant bewaarde adressen samenkomt of deze grens overschrijdt, toont de pagina of het standaardadres (als de klant één) heeft of _Geen adres dat_ met de _optie van het Adres van de Verandering_ wordt geselecteerd. De standaardlimiet is `10` .

1. Klik op **[!UICONTROL Save Config]**.
