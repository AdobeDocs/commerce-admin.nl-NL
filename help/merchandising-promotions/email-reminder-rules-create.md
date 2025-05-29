---
title: E-mailherinneringen maken
description: Leer hoe u een regel voor e-mailherinneringen instelt die gebruikmaakt van een bestaande regel voor de prijs van winkelwagentjes.
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# E-mailherinneringen maken

Alvorens vestiging een e-mailherinneringsregel, moet u eerst [ opstelling een regel van de kartprijs ](price-rules-cart-create.md) om de bevordering te bepalen die wordt aangeboden. De voorwaarden van de regel die een e-mailherinnering teweegbrengen kunnen op karteleigenschappen, vorkvermelde eigenschappen, of allebei worden gebaseerd.

>[!NOTE]
>
>E-mailherinneringen kunnen een regel voor winkelprijzen promoten met of zonder coupon. Een kaartprijsregel die een automatisch gegenereerde coupon definieert, genereert een willekeurige couponcode voor elke klant.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Rule]** .

1. Voltooi _[!UICONTROL Rule Information]_als volgt:

   ![ E-mailreminder regel ](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - Voer een **[!UICONTROL Rule Name]** in om de regel intern te identificeren.

   - Voer een korte **[!UICONTROL Description]** van de regel in.

   - Als u de **[!UICONTROL Cart Price Rule]** -promotie wilt kiezen die deze herinnering moet adverteren, klikt u op **[!UICONTROL Select Rule…]** en selecteert u de regel.

     ![ de regel van de Kar - uitgezocht ](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Status]** in op `Active` als u wilt dat de regel direct van kracht wordt.

   - Als u een datumbereik wilt instellen waarop de regel actief moet zijn, voert u de datums **[!UICONTROL From]** en **[!UICONTROL To]** in.

     U kunt de datum van de Kalender ( ![ pictogram van de Kalender ](../assets/icon-calendar.png) ook kiezen).

   - Als u de herinnering meerdere keren wilt verzenden, voert u in het veld **[!UICONTROL Repeat Schedule]** het aantal dagen voor de volgende e-mailexplosie in.

1. Kies **[!UICONTROL Conditions]** in het deelvenster aan de linkerkant.

   Voor de regel moet ten minste één voorwaarde worden gedefinieerd. Het proces is gelijkaardig aan het bouwen van de regel van de a [ catalogusprijs.](price-rules-catalog.md)

   ![ E-mailherinneringsvoorwaarden ](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   Klik _toevoegen_ ( ![ voeg pictogram ](../assets/icon-add-green-circle.png) toe) om de lijst van opties te tonen en dan één van de volgende voorwaarden te kiezen:

   - Gewenste lijst
   - Winkelwagentje

   >[!NOTE]
   >
   >Als een klant meer dan één geëvenaard karretje, verlanglijst, of combinatie van beide heeft, wordt de e-mailherinnering slechts eenmaal geactiveerd voor die klant. Als u dezelfde e-mailherinnering opnieuw wilt activeren, gebruikt u het veld _[!UICONTROL Repeat Schedule]_om het aantal dagen tussen de e-mailberichten in te stellen. <br/>
   >
   >De zelfde e-mailherinnering wordt **_niet opnieuw teweeggebracht_** voor de zelfde klant voor **_nieuwe_** verlaten wortels en wenst lijsten **_na_** de _[!UICONTROL Repeat Schedule]_periode is over.

   Voltooi de voorwaarde om het scenario te beschrijven dat de e-mailherinnering teweegbrengt.

   ![ voorbeeld van de e-mailherinneringsvoorwaarden ](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. Kies **[!UICONTROL Emails and Labels]** in het deelvenster aan de linkerkant.

   ![ Regel voor e-mailherinnering - e-mails en labels ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. In de **[!UICONTROL Email Templates]** sectie, kies het e-mailmalplaatje dat voor elke website en opslagmening in uw [ opslaghiërarchie ](../getting-started/websites-stores-views.md) moet worden gebruikt.

   Als u de herinnering niet per e-mail naar klanten van een winkelweergave wilt verzenden, laat u de waarde `Not Selected` ongewijzigd.

1. In de _Standaard Titels en de sectie van de Beschrijving_, doe het volgende:

   - Voer de **[!UICONTROL Rule Title for All Store Views]** in.

     >[!NOTE]
     >
     >Deze waarde kan in e-mailsjablonen worden opgenomen met de variabele `promotion_name` .

   - Voer de **[!UICONTROL Rule Description for All Store Views]** in.

     ![ E-mailherinneringen - titels en beschrijvingen ](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - In de _[!UICONTROL Titles and Descriptions Per Store View]_sectie, ga **[!UICONTROL Rule Title]**en **[!UICONTROL Description]**voor de_ StandaardMening van de Opslag _in. Voer voor meerdere winkelweergaven de juiste titel en beschrijving voor elke weergave in.

     >[!NOTE]
     >
     >De beschrijving kan in e-mailmalplaatjes worden opgenomen door de bevordering_beschrijvingsvariabele te gebruiken.

     ![ Titels en beschrijvingen - opslagmening ](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Trigingvoorwaarden

| Source | Trigger |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Rule Name] | De naam van de geautomatiseerde herinneringsregel identificeert intern de regel. |
| [!UICONTROL Description] | Een beschrijving van de regel voor interne verwijzing. |
| [!UICONTROL Shopping Cart Price Rule] | De winkelwagentregel die aan deze e-mailherinnering is gekoppeld. E-mails met herinneringen kunnen een winkelprijregel met of zonder coupon promoten. Als een winkelwagenprijsregel een automatisch gegenereerde coupon bevat, genereert de herinneringsregel een willekeurige, unieke couponcode voor elke klant. |
| [!UICONTROL Assigned to Website] | De websites die op basis van deze regel automatische e-mail met herinneringen ontvangen. |
| [!UICONTROL Status] | Hiermee activeert u de regel. Als status inactief is, worden alle andere instellingen genegeerd en wordt de regel niet geactiveerd. Opties: `Active` / `Inactive` |
| [!UICONTROL From Date] | De begindatum voor deze regel voor automatische herinnering. Als geen datum wordt gespecificeerd, wordt de regel onmiddellijk actief. |
| [!UICONTROL To Date] | De einddatum voor deze automatische herinneringsregel. Als geen datum wordt gespecificeerd, wordt de regel voor onbepaalde tijd actief. |
| [!UICONTROL Repeat Schedule] | Het aantal dagen voordat de regel wordt geactiveerd en het e-mailbericht voor de herinnering wordt opnieuw verzonden, mits aan de voorwaarden is voldaan. Als u de regel meerdere keren wilt activeren, voert u het aantal dagen voor de volgende e-mailexplosie in, gescheiden door een komma. Voer bijvoorbeeld `7` in om de regel zeven dagen later opnieuw te laten activeren. Voer `7,14` in om de regel binnen zeven dagen, en nogmaals 14 dagen later, te laten activeren. |
| [!UICONTROL Email Templates] | Bepaalt de e-mailsjabloon die voor elke winkelweergave moet worden gebruikt. |
| [!UICONTROL Rule Title for All Store Views] | Bepaalt de titel van de regel voor elke archiefmening. |
| [!UICONTROL Rule Description for All Store Views] | Bepaalt de beschrijving van de regel voor elke archiefmening. |

{style="table-layout:auto"}
