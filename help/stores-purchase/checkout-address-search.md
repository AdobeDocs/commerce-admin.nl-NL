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

Wanneer deze eigenschap wordt toegelaten en het aantal van de klant bewaarde adressen ontmoet of overschrijdt de gevormde grens, _Verzending_ en _Reviseren en betalen_ de stappen tonen slechts één adres (het gebrek). De klant kan het geselecteerde adres veranderen door te klikken **Adres wijzigen** en zoek vervolgens naar het juiste adres per plaats, staat, straat of postcode. Deze functie ondersteunt ook adresselectie voor uitchecken van cadeauregisters.

![Afhandeling met opgeslagen verzendadressen weergegeven](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Als de klant geen standaard verzendadres heeft, _Verzending_ paginaweergaven _Geen adres geselecteerd_. In dit geval moet de klant op **Adres wijzigen** om een opgeslagen adres te selecteren of klik op **Nieuw adres** om een adres toe te voegen en te selecteren voordat u verdergaat met het afrekenen. Als de klant geen standaard factureringsadres heeft, _Reviseren en betalen_ op de pagina wordt het adres weergegeven dat is geselecteerd voor verzending samen met het _Adres wijzigen_ -optie.

![Afhandeling zonder adres geselecteerd bericht](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Zoeken naar aanhalingstekens met vergrendeld adres

![Adobe Commerce B2B](../assets/b2b.svg) (Alleen beschikbaar bij Adobe Commerce B2B)

Het toelaten van adresonderzoek beïnvloedt ook de controle voor orden die van citaten worden gecreeerd waar het aantal van de klant bewaarde adressen of de gevormde grens ontmoet overschrijdt. Wanneer de prijsopgave is voltooid en de klant doorgaat naar de kassa, wordt alleen het geselecteerde verzendadres weergegeven. Op de pagina wordt ook een bericht weergegeven dat het verzendadres vergrendeld is en alleen in de prijsopgave kan worden gewijzigd.

![Verzendadres vergrendeld voor een prijsopgave](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Zoeken naar adressen inschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Checkout]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Options]** sectie.

   ![Configuratie - Afhandelingsopties](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [Afhandelingsopties](../configuration-reference/sales/checkout.md#checkout-options) in de _Referentiehandleiding voor configuratie_.

1. Set **[!UICONTROL Enable Address Search]** tot `Yes`.

1. Als u de drempel voor het opnemen van de zoekfunctie voor adressen wilt opgeven, stelt u de optie **[!UICONTROL Number of Customer Addresses Limit]** -optie.

   Indien nodig de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze wijziging aan te brengen.

   Wanneer het aantal opgeslagen adressen van de klant aan deze grens voldoet of overschrijdt, toont de pagina of het standaardadres (als de klant heeft) of _Geen adres geselecteerd_ met de _Adres wijzigen_ -optie. De standaardlimiet is `10`.

1. Klik op **[!UICONTROL Save Config]**.
