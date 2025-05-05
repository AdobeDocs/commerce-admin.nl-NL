---
title: Klantsegmenten in prijsregels
description: Leer over het associëren van klantensegmenten met een de prijsregel van de winkelwagentje zodat u gerichte bevorderingen voor uw opslag kunt bepalen.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Klantsegmenten in prijsregels

{{ee-feature}}

Een klantensegment kan voor gerichte bevorderingen worden gebruikt door het met de regel van de a [ kartprijs ](../merchandising-promotions/price-rules-cart.md) te associëren.

![ de prijsregel van het Kart - gericht klantensegment ](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**om een segment met een regel van de wortelprijs te associëren:**&#x200B;_

1. Op _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _Bevorderingen_ > **[!UICONTROL Cart Price Rules]**.

1. Open een nieuwe of bestaande regel:

   * Als u een nieuwe regel wilt gebruiken, klikt u op **[!UICONTROL Add New Rule]** in de rechterbovenhoek.
   * Als u een bestaande regel wilt gebruiken, klikt u op de regel in de lijst om deze te openen in de bewerkingsmodus.

1. Schuif omlaag en vouw de sectie **[!UICONTROL Conditions]** uit.

1. Voeg de voorwaarde toe.

   * Klik _toevoegen_ (![ pictogram van de Lijst ](../assets/icon-add-green-circle.png)) pictogram, dat de lijst van voorwaarden toont. Kies vervolgens **[!UICONTROL Customer Segment]** .

   ![ de prijsregel van het Kart - voeg de voorwaarde van het klantensegment toe ](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Standaard wordt bij deze voorwaarde een overeenkomende voorwaarde gevonden. Klik zo nodig op de koppeling **[!UICONTROL matches]** en wijzig de operator in een van de volgende:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![ de exploitant van de Voorwaarde ](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Als u een specifiek segment wilt instellen, klikt u op de koppeling Meer **..** om extra opties weer te geven. Dan, klik het _pictogram van de Kiezer_ (![ pictogram van de Lijst ](../assets/icon-list-chooser.png)) om de lijst van klantensegmenten te tonen.

1. In de lijst, selecteer checkbox van elk segment dat u met de voorwaarde wilt richten.

   ![ de prijsregel van de Kar - lijst van de voorwaardenselecteur ](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Select]** om de geselecteerde klantsegmenten in de voorwaarde te plaatsen.

1. Voltooi zo nodig de rest van de prijsregel.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.
