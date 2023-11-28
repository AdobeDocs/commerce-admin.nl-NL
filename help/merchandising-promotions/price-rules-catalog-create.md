---
title: Een regel voor catalogusprijzen maken
description: Leer hoe u een regel voor catalogusprijzen maakt die een korting toepast op specifieke producten wanneer aan een bepaalde voorwaarde wordt voldaan.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Een regel voor catalogusprijzen maken

Volg deze instructies om een korting op specifieke producten toe te passen wanneer aan een reeks voorwaarden wordt voldaan. Kortingen op catalogusprijzen worden van kracht voordat het product in het winkelwagentje wordt geplaatst.

## Stap 1: Een regel toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add New Rule]**.

   De _[!UICONTROL Rule Information]_sectie bevat uitbreidbare secties voor **[!UICONTROL Conditions]**en **[!UICONTROL Actions]**.

   ![Catalogusprijsregel - informatie](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Voltooi de **[!UICONTROL Rule Name]** en **[!UICONTROL Description]** velden.

   Deze velden zijn alleen bedoeld voor uw interne referentie.

1. Stel de **[!UICONTROL Status]** van de prijsregel indien nodig.

   Standaard is de status `Inactive`.

   >[!NOTE]
   >
   >Nadat de regel is gemaakt, kan de status worden bijgewerkt door de status te wijzigen in `Active` of `Inactive` indien nodig.

1. Selecteer de **[!UICONTROL Websites]** waar de regel beschikbaar moet zijn.

1. Selecteer de **[!UICONTROL Customer Groups]** waarop deze regel van toepassing is.

   Als u meerdere groepen wilt kiezen, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   >[!NOTE]
   >
   >De opties in deze lijst hangen van de klantengroepen af die binnen worden gecreeerd en worden geleid _Klanten_ > _Klantengroepen_.

1. ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Voer de optie **[!UICONTROL From]** en **[!UICONTROL To]** data waarop moet worden bepaald wanneer de prijsregel van kracht is.

   U kunt de datums invoeren of de **[!UICONTROL Calendar]** (![Kalenderpictogram](../assets/icon-calendar.png)) om de datums te kiezen. Als u de datums leeg laat, wordt de regel ingeschakeld wanneer de prijsregel wordt opgeslagen.

1. Voer een getal in om de **[!UICONTROL Priority]** van deze regel met betrekking tot andere regels.

   >[!NOTE]
   >
   >De _[!UICONTROL Priority]_het is belangrijk dat een catalogusproduct voldoet aan de voorwaarden die voor meer dan één prijsregel zijn vastgesteld . De regel met de hoogste prioriteit (1 is het hoogste) wordt actief voor het product.

## Stap 2: De voorwaarden definiëren

De meeste beschikbare voorwaarden zijn gebaseerd op bestaande kenmerkwaarden. Laat de voorwaarden leeg als u de regel op alle producten wilt toepassen.

>[!NOTE]
>
>Als ten minste één voorwaardelijk productkenmerk een lege waarde heeft, wordt de regel voor catalogusprijzen niet op het product toegepast.

>[!NOTE]
>
>Als u een `Category` productkenmerkvoorwaarde voor elke [bundelen](../catalog/product-create-bundle.md) of [gegroepeerd](../catalog/product-create-grouped.md) , moeten alle onderliggende producten aan dezelfde categorie worden toegewezen om de regel correct toe te passen. Zo niet, dan kunt u een [Regel voor winkelprijs](price-rules-cart-create.md) in plaats daarvan.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Conditions]** sectie.

   De eerste voorwaarde wordt standaard weergegeven en de volgende statussen:

   `If **ALL** of these conditions are **TRUE**:`

   ![Catalogusprijsregel - voorwaardenregel 1](./assets/catalog-condition1.png){width="400"}

   De instructie heeft twee vette koppelingen waarop u kunt klikken om de opties voor dat gedeelte van de instructie weer te geven. U kunt verschillende voorwaarden maken door de combinatie van deze waarden te wijzigen.

1. Wijzig de instructie op een van de volgende manieren:

   - Klikken **[!UICONTROL ALL]** en selecteert u `ALL` of `ANY`.
   - Klikken **[!UICONTROL TRUE]** en selecteert u `TRUE` of `FALSE`.
   - Laat de voorwaarde ongewijzigd om de regel op alle producten toe te passen.

   U kunt verschillende voorwaarden maken door de combinatie van deze waarden te wijzigen. In dit voorbeeld wordt de standaardvoorwaarde gebruikt.

1. Klik op de knop _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) aan het begin van de volgende regel en selecteer een optie voor de voorwaarde, zoals een productkenmerk of combinatie.

1. In de lijst onder **[!UICONTROL Product Attribute]** kiest u het kenmerk dat u als basis voor de voorwaarde wilt gebruiken.

   In dit voorbeeld is de voorwaarde: `Attribute Set`.

   ![Catalogusprijsregel - voorwaardenregel 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Voor een attribuut om in de lijst te verschijnen, moet het voor gebruik in promotionele regelvoorwaarden worden gevormd. Zie voor meer informatie [Productkenmerken](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Wanneer u de opdracht `is not one of` voorwaarde met een _SKU_ productkenmerk en configureerbaar product, zowel de SKU&#39;s van het bovenliggende product als het onderliggende product moeten worden geselecteerd. Als u wilt voorkomen dat alle onderliggende SKU&#39;s in de regel worden vermeld, kunt u de opdracht `does not contain` voorwaarde met gemeenschappelijke delen van SKU van een configureerbaar product en zijn kindproducten.

   De geselecteerde voorwaarde wordt weergegeven in de instructie, gevolgd door nog twee vette koppelingen. Welke opties beschikbaar zijn, is afhankelijk van het kenmerk condition dat u selecteert. In de verklaring staat nu:

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Klikken **[!UICONTROL is]** en kiest u de vergelijkingsoperator die de voorwaarde beschrijft waaraan moet worden voldaan.

   Deze opties kunnen een optie voor verschillende vergelijkingen omvatten. In dit voorbeeld zijn de opties: `is` en `is not`.

1. Selecteer of typ waarden voor de voorwaarde.

   Afhankelijk van de voorwaarde, kunt u producten van een net of een lijst selecteren, een numerieke waarde ingaan, etc.

   ![Catalogusprijsregel - voorwaardenregel 2](./assets/catalog-condition3.png){width="400"}

   Het geselecteerde item wordt weergegeven in de instructie om de voorwaarde te voltooien.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Als u nog een voorwaardelijn aan de instructie wilt toevoegen, klikt u op de knop _Toevoegen_ (![Pictogram toevoegen](../assets/icon-add-green-circle.png)) en kiest u een van de volgende opties:

   - `Conditions Combination`
   - `Product Attribute`

   Herhaal het proces totdat alle gewenste voorwaarden zijn voltooid.

   Als u op een bepaald moment een deel van de instructie condition wilt verwijderen, klikt u op de knop **[!UICONTROL Delete]** (![Pictogram Verwijderen](../assets/icon-delete-red-circle.png) aan het einde van de regel.

## Stap 3: De acties definiëren

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png)de **[!UICONTROL Actions]** en voer de volgende handelingen uit:

   ![Catalogusprijsregel - handelingen](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. Onder **[!UICONTROL Pricing Structure Rules]**, set **[!UICONTROL Apply]** op een van de volgende wijzen:

   - `Apply as percentage of original` - Kortingen op object door een percentage van de normale prijs af te trekken. Bijvoorbeeld: geef 10 op in het kortingsbedrag voor een uiteindelijke prijs die 10% lager is dan de normale prijs.
   - `Apply as fixed amount` - Kortingen op object door een vast bedrag af te trekken van de normale prijs. Bijvoorbeeld: voer 10 in Korting Bedrag in voor een definitieve prijs die $10 minder dan de normale prijs is.
   - `Adjust final price to this percentage` - Past de definitieve prijs aan met een percentage van de normale prijs. Bijvoorbeeld: Voer 25 in Korting Bedrag in voor een uiteindelijke prijs die 75% lager is dan de normale prijs.
   - `Adjust final price to discount value` - Stelt de uiteindelijke prijs in op een vast, gedisconteerd bedrag. Bijvoorbeeld: voer 20 in het bedrag voor korting in voor een uiteindelijke prijs van $20,00.

   >[!NOTE]
   >
   >_Normale prijs_ heeft betrekking op de basisprijs van het product zonder geavanceerde prijzen (special/tier/group) of promotionele kortingen. _Definitieve prijs_ verwijst naar de verlaagde prijs die in het winkelwagentje wordt weergegeven. <br/>De **_final_** de productprijs wordt berekend als **_minimum_** relevante prijs, met gebruikmaking van de volgende formule: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Vaste prijs_** Aanpasbare opties voor producten zijn _niet_ worden beïnvloed door de regels voor groepsprijs, Tier-prijs, Speciale prijs of Catalogusprijs.

1. Voer de **[!UICONTROL Discount Amount]**.

1. Als u de verwerking van andere regels wilt stoppen nadat deze regel is toegepast, stelt u **[!UICONTROL Discard Subsequent Rules]** tot `Yes`.

   >[!NOTE]
   >
   >Deze instellen op `Yes` is een garantie om te voorkomen dat het systeem meerdere kortingen (regels) op hetzelfde product toepast.

## Stap 4: verwante dynamische blokken toevoegen

{{ee-feature}}

[Dynamische blokken](../content-design/dynamic-blocks.md) die aan een regel van de catalogusprijs worden geassocieerd verschijnen in de opslagruimte wanneer de voorwaarden worden voldaan. Dit is een optionele stap.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png)de **[!UICONTROL Related Dynamic Blocks]** sectie.

1. Gebruik de [zoekfilters](../getting-started/admin-workspace.md) om van de dynamische blokken de plaats te bepalen die u met de regel wilt associëren.

1. Schakel het selectievakje in de eerste kolom in om het dynamische blok aan de regel te koppelen.

   ![Regels voor catalogusprijzen - gerelateerde dynamische blokken](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save and Continue Edit]**.

## Stap 5: Plan de regel

{{ee-feature}}

>[!NOTE]
>
>Het plaatsen van de regel aan actief moet als geplande update worden toegevoegd. Zie voor meer informatie [Geplande wijzigingen](price-rule-catalog-scheduled-changes.md).

1. In de _Geplande wijzigingen_ vak, klikt u op **[!UICONTROL Schedule New Update]** boven aan de doos).

   Als de regel een bestaande geplande update heeft, kunt u klikken **[!UICONTROL View/Edit]** rechts van de vermelde wijziging.

   U kunt de bestaande update bewerken of de regel voor catalogusprijzen toewijzen aan een andere campagne. De **Bestaande update bewerken** is standaard geselecteerd.

1. Om de regel te plannen, ga in **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** dat de prijsregel actief moet zijn.

   U kunt de datums invoeren of de datums kiezen in het menu _Kalender_ (![Kalenderpictogram](../assets/icon-calendar.png)).

   ![Catalogusprijsregel - update-schema](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

1. In de _Regelinformatie_ in, stelt u de **[!UICONTROL Status]** tot `active`.

## Stap 6: Sla de regel op en test deze

1. Sla de regel op wanneer deze is voltooid.

   - ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Klik op **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Klik op **[!UICONTROL Save]**.

     De pagina van de Informatie van de Regel toont een bijgewerkte chronologie in de Geplande Veranderingen voor de regel.

     ![Catalogusprijsregels - geplande wijzigingen](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Eigenschappen voor een regel bijwerken:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Alleen Adobe Commerce) Klik op **[!UICONTROL Edit]** om de _[!UICONTROL Rule Information]_pagina.

   - ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Klik op de regel in de lijst om het dialoogvenster _[!UICONTROL Rule Information]_pagina.

1. Test de regel om er zeker van te zijn dat deze correct werkt.

   Prijsregels worden elke avond automatisch met andere systeemregels verwerkt. Wanneer u een prijsregel creeert, laat genoeg tijd voor het in het systeem alvorens u de regel test om ervoor te zorgen dat het correct werkt. Aangezien nieuwe regels worden toegevoegd, herberekent de Handel de prijzen en de prioriteiten dienovereenkomstig.

## Demo van catalogusprijsregel

Bekijk deze video voor meer informatie over het maken van prijsregels voor catalogi:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## Veldomschrijvingen

### [!UICONTROL Rule Information]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Rule name] | (Vereist) De naam van de regel is voor interne verwijzing. |
| [!UICONTROL Description] | Een beschrijving van de regel moet het doel van de regel bevatten en uitleggen hoe deze wordt gebruikt. |
| [!UICONTROL Websites] | (Vereist) Hiermee worden de websites geïdentificeerd waarop de regel kan worden gebruikt. |
| [!UICONTROL Customer Groups] | (Vereist) Identificeert de klantengroepen waarop de regel van toepassing is. |
| [!UICONTROL Priority] | Een getal dat de prioriteit van deze regel ten opzichte van andere regels aangeeft. De hoogste prioriteit is nummer 1. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Hiermee wordt bepaald of de regel actief is in de winkel. Opties: `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Hiermee geeft u de eerste dag op waarop de prijsregel van kracht is. Als deze optie leeg blijft, wordt de prijsregel toegepast wanneer deze wordt opgeslagen. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Alleen Magento Open Source) Hiermee geeft u de laatste dag op waarop de prijsregel van kracht is. Als je niets invult, gaat de prijsregel eindeloos door. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Hiermee geeft u de voorwaarden op waaraan moet worden voldaan voordat de regel voor catalogusprijzen in werking treedt. Als deze optie niet wordt opgegeven, geldt de regel voor alle producten.

### [!UICONTROL Actions]

| Veld | Beschrijving |
|-----|-----------|
| [!UICONTROL Apply] | Bepaalt het type berekening dat op de aankoop wordt toegepast. Opties: <br/>**[!UICONTROL Apply as percentage of original]**- Kortingen op object door een percentage van de normale prijs af te trekken.<br/>**[!UICONTROL Apply as fixed amount]** - Kortingen op object door een vast bedrag af te trekken van de normale prijs. <br/>**[!UICONTROL Adjust final price to this percentage]**- Past de definitieve prijs aan met een percentage van de normale prijs.<br/>**[!UICONTROL Adjust final price to discount value]** - Stelt de uiteindelijke prijs in op een vast, gedisconteerd bedrag. <br/><br/>**_Opmerking:_**De normale prijs heeft betrekking op de basisprijs van het product zonder geavanceerde prijzen (speciale prijzen/tier/groep) of promotionele kortingen. De uiteindelijke prijs heeft betrekking op de verlaagde prijs die in het winkelwagentje wordt weergegeven. <br/>De**_final _**de productprijs wordt berekend als**_minimum _**relevante prijs, met gebruikmaking van de volgende formule: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Vereist) Het bedrag van korting dat wordt aangeboden. |
| [!UICONTROL Discard Subsequent Rules] | Hiermee bepaalt u of er aanvullende regels kunnen worden toegepast op deze aankoop. Als u wilt voorkomen dat meerdere kortingen op dezelfde aankoop worden toegepast, selecteert u `Yes`. Opties: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identificeert alle [dynamische blokken](../content-design/dynamic-blocks.md) die aan de regel worden geassocieerd.
