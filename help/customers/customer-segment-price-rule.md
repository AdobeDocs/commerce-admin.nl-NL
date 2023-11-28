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

Een klantensegment kan voor gerichte bevorderingen worden gebruikt door het met een [kartonnen prijsregel](../merchandising-promotions/price-rules-cart.md).

![Winkelprijsregel - gericht klantensegment](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_**Een segment aan een regel voor de winkelwagenprijs koppelen:**_

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _Aanbiedingen_ > **[!UICONTROL Cart Price Rules]**.

1. Open een nieuwe of bestaande regel:

   * Klik op **[!UICONTROL Add New Rule]** in de rechterbovenhoek.
   * Als u een bestaande regel wilt gebruiken, klikt u op de regel in de lijst om deze te openen in de bewerkingsmodus.

1. Omlaag schuiven en de **[!UICONTROL Conditions]** sectie.

1. Voeg de voorwaarde toe.

   * Klik op de knop _Toevoegen_ (![Lijstpictogram](../assets/icon-add-green-circle.png)), waarmee de lijst met voorwaarden wordt weergegeven. Kies vervolgens **[!UICONTROL Customer Segment]**.

   ![Prijsregel voor winkelwagentjes - voorwaarde voor klantensegment toevoegen](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Standaard wordt bij deze voorwaarde een overeenkomende voorwaarde gevonden. Klik indien nodig op de knop **[!UICONTROL matches]** koppelen en de operator wijzigen in een van de volgende:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Condition, operator](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Als u een specifiek segment wilt instellen, klikt u op Meer **...** voor het weergeven van extra opties. Klik vervolgens op de knop _Kiezer_ (![Lijstpictogram](../assets/icon-list-chooser.png)) om de lijst met klantsegmenten weer te geven.

1. In de lijst, selecteer checkbox van elk segment dat u met de voorwaarde wilt richten.

   ![Regel voor winkelprijzen - voorwaarden kiezen](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Klikken **[!UICONTROL Select]** om de geselecteerde klantsegmenten in de voorwaarde te plaatsen.

1. Voltooi zo nodig de rest van de prijsregel.

1. Klik op **[!UICONTROL Save]**.
