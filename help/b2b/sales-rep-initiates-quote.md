---
title: Aanhalingstekens voor een koper starten
description: Leer hoe een verkoper een prijsopgave kan maken voor een specifieke koper om het onderhandelingsproces te starten. De verkoper kan alleen offertes verzenden voor klanten die zijn gekoppeld aan een bedrijfsaccount op de geselecteerde website.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 69396421bae610ff02b12054bdea2278a8c0efe5
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Een prijsopgave voor een koper starten

Als de citaten in de [ configuratie van de Eigenschappen van de Verkoop ](configure-quotes.md) worden toegelaten, kan een verkoopvertegenwoordiger het onderhandelingsproces met een bedrijfkoper in werking stellen door een citaat van Admin te creëren.

- Concepten zijn alleen zichtbaar voor de verkoper.
- Conceptprijsopgaven kunnen pas worden ingediend nadat de verkoper items, relevante kortingen en opmerkingen heeft toegevoegd om de oorspronkelijke aanbieding voor de koper te maken.
- Een verkoper kan een aanhalingsteken maken op basis van de offertes of het klantenraster.

De verkoper stuurt de prijsopgave naar de koper om het onderhandelingsproces in gang te zetten. [](quote-price-negotiation.md)

## Sales representative quote creation experience

A Sales Representative can create a quote from the Quotes or Customer Grid.

>[!NOTE]
>
>[](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html)__

### Create a quote from the Quote grid

1. [](../systems/permissions.md)

1. Ga in Beheer naar het [!UICONTROL Quotes] -raster door **[!UICONTROL Sales]** te selecteren en selecteer vervolgens **[!UICONTROL Quotes]** .

1. Maak een prijsopgave voor een koper.

   - Selecteer **[!UICONTROL Create New Quote]** in het raster Aanhalingstekens.

     ![](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - [!UICONTROL Create New Quote]

     ![ Uitgezochte klant voor nieuw citaat ](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     Er wordt een nieuw aanhalingsteken weergegeven in de status `Draft` .

     ![ Nieuw ontwerp citaat dat door verkoper ](./assets/quote-create-by-seller.png){width="700" zoomable="yes"} wordt gecreeerd

   - Werk de citaatnaam bij en wijzig zo nodig de vervaldatum.

   - Sla het aanhalingsteken op als concept.

## De prijsopgave voor de koper voorbereiden

Nadat u het concept-aanhalingsteken hebt gemaakt, voegt u productitems toe, past u kortingen toe en communiceert u met de koper door opmerkingen en verwante bestanden aan het aanhalingsteken toe te voegen. Vervolgens stuurt u het aanhalingsteken ter controle naar de koper of slaat u het op als concept.

1. Voeg items aan het aanhalingsteken toe door **[!UICONTROL Add Product By SKU]** te selecteren. Voer het SKU-nummer en het aantal in en selecteer vervolgens **[!UICONTROL Add Product]** .

   ![ Verkoper die punten aan ontwerp citaat voor koper toevoegt ](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. Pas indien nodig kortingen voor regelobjecten toe op producten.

   - [!UICONTROL Select]**[!UICONTROL Discount Item]**

   - [!UICONTROL Discount Line item]**[!UICONTROL Discount Type]**

     ![](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - [!UICONTROL Discount] For example, if you selected a percentage discount, enter 10 to apply a 10% discount to the line item.

   - Optionally, lock the line item discount value so that the product price is not further reduced by any discounts applied at the quote level.

     Nadat de wijziging is bevestigd, worden de kenmerken van het regelitem in het productraster bijgewerkt om het toegepaste kortingsbedrag weer te geven. Als de korting is vergrendeld, wordt een vergrendelingspictogram weergegeven.

   Een vertegenwoordiger van de Verkoop kan om een korting van een specifiek lijnpunt in een citaat verzoeken.

   >[!NOTE]
   >
   >Voor een videodemo van hoe de kortingen bij het werk van het lijnpunt, zie [ de Vertegenwoordiger van de Verkoop korting op een punt van de citaatlijn ](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/quote-line-item-discount.html) in _Video&#39;s en Tutorials van Commerce_ toepast.

1. Apply a quote-level discount as needed:

   - [!UICONTROL Quote Totals - Negotiated Price]

     ![ Verkoper voegt de korting van het citaatniveau toe ](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   Het productraster wordt bijgewerkt om de korting weer te geven.

1. Voeg aanvullende informatie voor de koper toe.

   Voeg op het tabblad **[!UICONTROL Negotiation - Comments]** een notitie toe en voeg eventuele ondersteunende bestanden toe die vereist zijn voor de koper.

   ![ Verkoper voegt informatie voor koper ](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"} toe

   Door gebrek, kan een [ dossier in bijlage ](configure-quotes.md) tot 2 MB, in om het even welke volgende dossierformaten zijn: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG of JPEG, PNG.

1. Add shipping address during negotiations.

   A Sales Representative can make a shipping and delivery selection once the buyer has added a shipping address to the quote.

   Shipping options are locked on checkout.

   [](account-dashboard-my-quotes.md#adding-a-shipping-address)

1. Process the quote.

   Sla het aanhalingsteken op als concept of verzend het naar de koper.

   - Als u het aanhalingsteken opslaat als concept, wordt de status bijgewerkt naar `Draft` en wordt een bevestigingsbericht weergegeven.

   - Als je het aanhalingsteken naar de koper stuurt, verandert de status in `Submitted` . De koper ontvangt een e-mailbericht om de prijsopgave te bekijken. De prijsopgave is vergrendeld totdat de koper deze voor verdere onderhandelingen retourneert. De verkoper kan de prijsopgave bekijken in het Offertennet of het klantenraster.

## Aanhalingstekens weergeven en maken via het raster van de klant

1. Ga in Beheer naar het [!UICONTROL Customer] -raster door **[!UICONTROL Customers]** te selecteren en selecteer vervolgens **[!UICONTROL All Customers]** .

1. Selecteer de klant-id voor een bedrijfkoper.

   ![ Bevestigingsontwerp citaat dat aan koper wordt voorgelegd ](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Selecteer **[!UICONTROL Edit]** om de klantgegevens weer te geven.

1. Maak een aanhalingsteken voor de klant door het concept te selecteren, **[!UICONTROL Create Quote]** en het conceptprijsopgave bij te werken en naar de klant te verzenden.

1. Bestaande aanhalingstekens van klanten weergeven door **[!UICONTROL Quotes]** te selecteren.

   ![ Bevestigingsontwerp citaat dat aan koper wordt voorgelegd ](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Open een aanhalingsteken door **[!UICONTROL View]** te selecteren.

Voor details bij het beheren van het proces van de citaatonderhandeling, zie [ een citaat bespreken ](quote-price-negotiation.md)
