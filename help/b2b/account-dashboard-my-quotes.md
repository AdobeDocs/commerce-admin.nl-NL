---
title: '[!UICONTROL My Quotes]'
description: Meer informatie over de ervaring van klanten met prijsopgaven, die beschikbaar is op het dashboard van hun account.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Als aanhalingstekens zijn ingeschakeld, wordt de _[!UICONTROL My Quotes]_in het gedeelte van het dashboard voor de klantenaccount worden alle aanhalingstekens weergegeven die door de klant zijn ingediend. Afhankelijk van hun machtigingen kunnen alleen kopers die namens een bedrijf aankopen doen, verzoeken om over de prijs van een aankoop te onderhandelen.

![Mijn aanhalingstekens](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

De koper begint de procedure met [indiening van een verzoek](quote-request.md) voor een citaat uit het winkelwagentje . E-mail wordt uitgewisseld tussen koper en verkoper tijdens de [onderhandelingsproces](quote-price-negotiation.md). Voor de koper [!UICONTROL My Quotes] Deze pagina is het centrale punt voor alle communicatie tussen koper en verkoper tijdens het onderhandelingsproces. Een koper die de door de verkoper geboden onderhandelingsprijs accepteert, kan direct vanaf de prijsopgave naar de betalingspagina gaan. Er kunnen geen extra kortingen aan het onderhandelde prijsopgave worden toegevoegd.

Een koper kan de volgende handelingen uitvoeren bij het onderhandelen over een prijsopgave:

* Prijsbepaling en updates van objecten controleren
* Houd het onderhandelingsproces bij van [!UICONTROL Comments] en [!UICONTROL History] secties
* Het aanhalingsteken wijzigen om items te verwijderen
* Communiceren en onderhandelen met de verkoper door opmerkingen toe te voegen op het niveau van het regelobject en de prijsopgave
* Aanhalingsteken ter controle naar verkoper sturen
* Zet het citaat in een orde om als de termijnen aanvaardbaar zijn
* Het aanhalingsteken sluiten
* Het aanhalingsteken verwijderen
* [!BADGE 1.5.0 bètamogelijkheden]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"}

In het volgende voorbeeld wordt een prijsopgave getoond die door de koper is bijgewerkt en ter controle naar de verkoper is teruggestuurd.


![Weergave koper van prijsopgave](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Aanhalingstekens met de `Updated` status zijn vergrendeld totdat de verkoper de prijsopgave retourneert.

## Aanhalingstekens tonen

Met de vereiste [machtigingen voor hun rol](account-company-roles-permissions.md)kunnen klanten die zijn gekoppeld aan een bedrijfsaccount, de door [ondergeschikte gebruikers](account-company-structure.md). De beheerders van het bedrijf kunnen alle citaten voor de bedrijfrekening zien.

1. De klant meldt zich aan bij zijn account op de winkel.

1. Klikken **[!UICONTROL My Quotes]** in de linkernavigatie.

1. Om alle citaten te zien die zij hebben gecreeerd, klik **[!UICONTROL Show My Quotes]** koppeling (wordt alleen weergegeven voor de systeembeheerder van het bedrijf of de account met onderliggende gebruikers).

1. Om alle citaten van alle bedrijfgebruikers te zien, klik **[!UICONTROL Show All Quotes]**.

## Een aanhalingsteken weergeven

1. De klant meldt zich aan bij zijn account.

1. Kies in het linkerdeelvenster de optie **[!UICONTROL My Quotes]**.

1. Hiermee zoekt u het aanhalingsteken in de lijst en klikt u **[!UICONTROL View]** in de _[!UICONTROL Action]_kolom.

## Een aanhalingsteken afdrukken

1. In het open citaat rechts van _[!UICONTROL Items Quoted]_sectie, klikt de klant **[!UICONTROL Print]**.

1. Controleert de **[!UICONTROL Destination]** als printer of PDF.

1. Klikken **[!UICONTROL Print]**.

## Een prijsaanvraag annuleren

1. Klik in het open aanhalingsteken net boven de sectie Items genoemd op **[!UICONTROL Close quote]**.

   Het verzoek wordt geannuleerd en de status van het citaat verandert in `Closed`. Het gesloten citaat blijft in uw lijst van citaten, en blijft vermeld in _[!UICONTROL Quotes]_raster van de beheerder.

1. Om het geannuleerde citaat uit de lijst van citaten te verwijderen, klikt **[!UICONTROL Delete]**.

1. Wanneer ertoe aangezet om te bevestigen, klikt **[!UICONTROL OK]**.

   Het gesloten citaat wordt verwijderd uit hun lijst van citaten. Het bestand blijft echter in de lijst _[!UICONTROL Quotes]_het raster in Admin, met `Closed` status.

## Offertehandelingen

| Handeling | Beschrijving |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naam wijzigen | [!BADGE 1.5.0 bètamogelijkheden]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"} |
| Een kopie maken | [!BADGE 1.5.0 bètamogelijkheden]{type=Informative url="/help/b2b/release-notes.md" tooltip="Alleen beschikbaar voor deelnemers aan het bètaprogramma"} |
| Aanhalingsteken sluiten | Nadat een koper een prijsopgave heeft gesloten, kan deze niet opnieuw worden geopend. Indien nodig kan de koper het opnieuw maken met de [!UICONTROL Create Copy] handeling. Deze optie is niet beschikbaar als de status van de offerte `Draft`. |
| Aanhalingsteken verwijderen | Wanneer een koper een prijsopgave verwijdert, wordt deze uit het systeem verwijderd en is deze niet meer beschikbaar. |
| Afdrukken | Hiermee opent u een afdrukformulier waarin u het aanhalingsteken kunt opslaan als een PDF, bestand of afdrukbestand naar een geconfigureerde printer. |

## Kolombeschrijvingen

| Kolom | Beschrijving |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | De naam die door de koper is toegewezen aan de prijsaanvraag. |
| [!UICONTROL Created] | De datum waarop de prijsaanvraag voor het eerst is ingediend. |
| [!UICONTROL Created By] | De voornaam en achternaam van de koper die de prijsaanvraag heeft ingediend. |
| [!UICONTROL Status] | Geeft de status van het aanhalingsteken aan. De status van een prijsopgave kan alleen worden gewijzigd door actie van de koper of de verkoper. <br/>**[!UICONTROL Submitted]**- De aanvraag van de koper voor een prijsopgave is nog niet geopend door de verkoper. In deze status kan de koper nog steeds de aanvraag voor een prijsopgave wijzigen. Beschikbare acties: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - De verkoper heeft het verzoek geopend en is bezig het te bekijken en een reactie voor te bereiden. Beschikbare acties: `View` / `Close` <br/>**[!UICONTROL Updated]**- De verkoper heeft een reactie gestuurd naar de koper en de _[!UICONTROL Proceed to Checkout]_wordt ingeschakeld. In deze status kan de koper doorgaan met het wijzigen van de prijsopgave. Beschikbare acties: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- De koper werkt de prijsopgave nog steeds bij en de_[!UICONTROL Proceed to Checkout]_ is uitgeschakeld. Beschikbare acties: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- De koper heeft een bestelling ingediend op basis van de onderhandelde prijsopgave. Het aanhalingsteken is vergrendeld en kan niet worden bewerkt. Beschikbare actie: Weergeven<br/>**[!UICONTROL Closed]** - De koper heeft de onderhandeling beëindigd en annuleert de prijsopgave. De prijsopgave is vergrendeld en kan niet door de koper of de verkoper worden bewerkt. Beschikbare acties: `View` / `Delete` <br/>**[!UICONTROL Declined]**- De verkoper heeft het verzoek om een prijsopgave afgewezen of heeft tijdens het onderhandelingsproces een voorgestelde wijziging voorgesteld. Een citaat kan in om het even welk stadium van het werkschema worden verworpen. Eventuele aangepaste prijzen worden uit de prijsopgave verwijderd. De koper kan de prijsopgave blijven bewerken en opnieuw indienen, of de aanschaf uitvoeren met standaardcatalogusprijzen. Beschikbare acties: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - De levensduur van de prijsopgave is verlopen. Alle voorgestelde prijzen worden opnieuw vastgesteld. De koper kan de aankoop voltooien op basis van standaardcatalogusprijzen of een andere onderhandelingsronde starten. Beschikbare acties: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
