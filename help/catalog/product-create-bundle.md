---
title: Bundel
description: Leer hoe u een bundelproduct maakt waarmee kopers een aangepast product in uw winkel kunnen maken.
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1474'
ht-degree: 0%

---

# Bundel

Een bundel is een _uw eigen_, aanpasbaar product. Elk item in een bundel kan op een van de volgende producttypen worden gebaseerd:

- [Eenvoudig product](product-create-simple.md)
- [Virtueel product](product-create-virtual.md)

![Bundel](./assets/product-bundle.png){width="700" zoomable="yes"}

De opties verschijnen wanneer de klant of klikt **[!UICONTROL Customize]** of **[!UICONTROL Add to Cart]**. Omdat de producten die in de bundel inbegrepen zijn variëren, kan SKU, de Prijs, en het Gewicht aan of een dynamische of vaste waarde worden geplaatst.

>[!NOTE]
>
>De minimum Geadverteerde Prijs (MAP) is niet beschikbaar voor Bundelproducten die dynamische prijsstelling gebruiken.

Indien [Direct aanschaffen](../stores-purchase/checkout-instant-purchase.md) is beschikbaar, _Direct aanschaffen_ wordt onder de knop _Toevoegen aan winkelwagentje_ voor elk item in de bundel.

![Bundel aanpassen](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

De volgende instructies begeleiden u bij het maken van een bundelproduct met behulp van een [productsjabloon](attribute-sets.md), vereiste velden en basisinstellingen. Elk vereist veld is gemarkeerd met een rood sterretje (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

## Stap 1: Kies het producttype

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. In de rechterbovenhoek op het tabblad _[!UICONTROL Add Product]_( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ), kiest u **[!UICONTROL Bundle Product]**.

   ![Bundelproduct toevoegen](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## Stap 2: Kies de kenmerkset

Als u de optie [kenmerkset](attribute-sets.md) die als malplaatje voor het product wordt gebruikt, doe één van het volgende:

- Voor **[!UICONTROL Search]**, voert u de naam in van de kenmerkset,
- Kies in de lijst de kenmerkset die u wilt gebruiken.

Het formulier wordt bijgewerkt met de wijziging.

![Sjabloon kiezen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Stap 3: Voer de vereiste instellingen in

1. Voer het product in **[!UICONTROL Product Name]**.

1. Accepteer de standaardinstelling **[!UICONTROL SKU]** die is gebaseerd op de productnaam of een andere waarde invoert.

   Ga als volgt te werk om het type SKU te bepalen dat aan elk bundelitem is toegewezen:

   - A **[!UICONTROL Dynamic SKU]** kan automatisch aan elk bundelpunt worden toegewezen door een achtervoegsel aan standaardSKU toe te voegen. Standaard is deze ingesteld op `Yes`.

   - Als u verkiest unieke SKU voor elk bundelpunt toe te wijzen, plaats **[!UICONTROL Dynamic SKU]** tot `No`.

   ![Dynamische SKU en prijs](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit om de prijs van de bundel te bepalen:

   - Om de prijs de opties te laten weerspiegelen die de klant heeft gekozen, stelt u **[!UICONTROL Dynamic Price]** tot `Yes` en vertrekken **[!UICONTROL Price]** leeg.

   - Als u een vaste prijs voor de bundel wilt berekenen, stelt u **[!UICONTROL Dynamic Price]** tot `No` en voert u de **[!UICONTROL Price]** die u voor de bundel wilt opladen.

1. Aangezien het product nog niet gereed is om te publiceren, stelt u **[!UICONTROL Enable Product]** tot `No`.

1. Klikken **[!UICONTROL Save]** en doorgaan.

   Wanneer het product wordt opgeslagen, wordt [Winkelweergave](introduction.md#product-scope) wordt in de linkerbovenhoek weergegeven.

1. Kies de optie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![Winkelweergave kiezen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Stap 4: De basisinstellingen voltooien

1. Als de bundel vaste prijs heeft, stelt u **[!UICONTROL Tax Class]** op een van de volgende wijzen:

   - `None`
   - `Taxable Goods`

   Als de bundel Dynamische Prijsbepaling heeft, wordt de belasting bepaald voor **_elk_** bundelitem. Als de bundel vaste prijzen heeft, wordt de belasting bepaald voor de **_geheel_** bundelproduct.

1. Let op het volgende:

   - De **[!UICONTROL Quantity]** is niet beschikbaar omdat de waarde wordt bepaald voor elk bundelitem.

   - Standaard worden de **[!UICONTROL Stock Status]** is ingesteld op `In Stock`.

1. Voer een van de volgende handelingen uit om het gewicht van de bundel te bepalen:

   - Als u wilt dat het gewicht de door de klant gekozen opties weerspiegelt, stelt u **[!UICONTROL Dynamic Weight]** set `Yes` en vertrekken **[!UICONTROL Weight]** leeg.

   - Als u een vaste dikte aan de bundel wilt toewijzen, stelt u **[!UICONTROL Dynamic Weight]** tot `No` en voert u de **[!UICONTROL Weight]** van de bundel.

   ![Dynamische dikte](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. Het product plaatsen in de lijst met [nieuwe producten](../content-design/widget-new-products-list.md), selecteert u de **[!UICONTROL Set Product as New]** selectievakje.

1. De standaardinstelling accepteren **[!UICONTROL Visibility]** instellen van `Catalog, Search`.

1. Om _[!UICONTROL Categories]_voor het product klikt u op de knop **[!UICONTROL Select…]**en voer een van de volgende handelingen uit:

   **Kies een bestaande categorie:**

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van elke categorie die u wilt toewijzen.

   ![Selecteer een of meer categorieën voor het bundelproduct](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Een categorie maken:**

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** en kiest u **[!UICONTROL Parent Category]**, die de positie in de menustructuur bepaalt.

   - Klik op **[!UICONTROL Create Category]**.

1. Kies de optie **[!UICONTROL Country of Manufacture]**.

   Er kunnen aanvullende kenmerken zijn die het product beschrijven. De selectie varieert kenmerkset en u kunt deze later voltooien.

## Stap 5: Voeg de bundelitems toe

De _[!UICONTROL Bundle Items]_wordt gebruikt om items toe te voegen aan een bundel voor producttypen en om de huidige selectie van items te bewerken.

![Bundel items die zijn gedefinieerd voor een product](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}

1. Omlaag schuiven naar de _Bundel-items_ sectie en set **[!UICONTROL Ship Bundle Items]** op een van de volgende wijzen:

   - `Separately`
   - `Together`

   Als u `Together`moeten alle bundelitems op dezelfde manier worden toegewezen [bron](../inventory-management/sources-manage.md).

1. Klikken **[!UICONTROL Add Option]** en voer de volgende handelingen uit:

   - Voer een **[!UICONTROL Option Title]** als veldlabel te gebruiken.

   - Set **[!UICONTROL Input Type]** op een van de volgende wijzen:

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - Als u van het veld een verplicht item wilt maken, selecteert u de optie **[!UICONTROL Required]** selectievakje.

   - Klikken **[!UICONTROL Add Products to Option]** en schakelt u het selectievakje in van elk product dat u in deze optie wilt opnemen.

     Als er vele producten zijn, gebruik de lijstfilters en pagineringscontroles om de producten te vinden u nodig hebt.

   - Klik op **[!UICONTROL Add Selected Products]**.

     ![Geselecteerde producten toevoegen](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - Nadat de items in het deelvenster _Opties_ sectie, kies een punt om te zijn **[!UICONTROL Default]** selectie.

   - In de _Standaardhoeveelheid_ de hoeveelheid van elk item in die aan de bundel moet worden toegevoegd wanneer een klant het item kiest.

   - Als u klanten wilt toestaan de hoeveelheid van een bundelitem te wijzigen, selecteert u **[!UICONTROL User Defined]**.


     >[!NOTE]
     >
     >De hoeveelheid kan een vooraf ingestelde of door de gebruiker gedefinieerde waarde zijn. Wijs echter geen _[!UICONTROL User Defined]_eigenschap om het selectievakje in te schakelen of invoertypen te selecteren die meerdere malen zijn geselecteerd.

     Standaard kan de standaardhoeveelheid die in een bundelitem is opgenomen, niet door de klant worden gewijzigd. De klant kan echter de hoeveelheid van het item invoeren die in de bundel moet worden opgenomen.

     Als bijvoorbeeld de standaardhoeveelheid van de Sprite-statusbalk is ingesteld op `2` en de orders van de klant `4` van die bundeloptie is het totale aantal aangekochte ballen `8`.

     ![Itemdetails](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. Herhaal deze stappen voor elk item dat u aan de bundel wilt toevoegen.

1. Als u de volgorde van items in een bundelsectie wilt wijzigen, klikt u op de knop _Verplaatsen_ ( ![Pictogram Verplaatsen](../assets/icon-move.png) ) aan het begin van de rij en sleep het item naar de gewenste positie.

   ![De volgorde van bundelitems wijzigen](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   De volgorde van items kan ook worden gewijzigd in de gegevens van een geëxporteerd bundelproduct en vervolgens opnieuw worden geïmporteerd in de catalogus. Zie voor meer informatie [Bundelproducten importeren](../systems/data-transfer-bundle-products.md).

   Voor een betere weergave van de werkruimte, vouwt u eerst elke sectie samen en sleept u deze naar de gewenste positie.

1. Als u een item uit de bundel wilt verwijderen, klikt u op de knop **[!UICONTROL Delete]** ( ![Prullenbakpictogram](../assets/icon-delete-trashcan.png) ).

1. Klik op **[!UICONTROL Save]**.

## Stap 6: De productinformatie invullen

Schuif omlaag en voltooi indien nodig de informatie in de volgende secties:

- [Inhoud](product-content.md)
- [Afbeeldingen en video&#39;s](product-images-and-video.md)
- [Optimalisatie zoekmachine](product-search-engine-optimization.md)
- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)
- [Aanpasbare opties](settings-advanced-custom-options.md)
- [Producten op websites](settings-basic-websites.md)
- [Ontwerp](settings-advanced-design.md)
- [Cadeauopties](product-gift-options.md)

## Stap 7: Het product publiceren

1. Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** tot `Yes` ( ![Ja in-/uitschakelen](../assets/toggle-yes.png) ).

1. Voer een van de volgende handelingen uit:

   **Methode 1:** Opslaan en voorvertonen

   - Klik in de rechterbovenhoek op **[!UICONTROL Save]**.

   - Kies **[!UICONTROL Customer View]** op de _Beheerder_ ( ![Menupijl](../assets/icon-menu-down-arrow-black.png) ).

     De winkel wordt geopend in een nieuw browsertabblad.

   ![Klantenweergave](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Methode 2:** Opslaan en sluiten

   Op de _[!UICONTROL Save]_( ![Menupijl](../assets/icon-menu-down-arrow-red.png){width="25"} ), kiest u **[!UICONTROL Save & Close]**.

## Invoerbesturingselementen

| Besturing | Beschrijving | Voorbeeld |
|--- |--- |--- |
| [!UICONTROL Drop-down] | Hiermee geeft u een vervolgkeuzelijst met opties weer met de productnaam en de prijs. Er kan slechts één item worden geselecteerd. | ![Vervolgkeuzelijst](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | Hiermee geeft u een keuzerondje voor elke optie weer, gevolgd door de productnaam en -prijs. Er kan slechts één item worden geselecteerd. | ![Keuzerondjes](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | Hiermee wordt voor elke optie een selectievakje weergegeven, gevolgd door de productnaam en de prijs. U kunt meerdere items selecteren. | ![Selectievakje](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | Hiermee geeft u een lijst met opties weer met de productnaam en de prijs. Als u meerdere items wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elk item. | ![Meerdere selecties](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL SKU] | Hiermee wordt bepaald of aan elk item een variabele of dynamische SKU is toegewezen of of dat een vaste SKU voor de bundel wordt gebruikt. Opties: `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | Hiermee wordt opgegeven of het gewicht wordt berekend op basis van de geselecteerde items of een vast gewicht voor de hele bundel is. Opties: `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | Hiermee wordt bepaald of de prijs van het product wordt weergegeven als een bereik, van de goedkoopste prijs tot de duurste (prijsklasse) of met de goedkoopste prijs (Als laag als). Opties: `Price Range` / `As Low As` |
| Verzendbundelobjecten | Hiermee geeft u aan of afzonderlijke items afzonderlijk kunnen worden verzonden. |

{style="table-layout:auto"}

## Status van bundelproductvoorraad

De status van de bundelproductvoorraad is **_automatisch gewijzigd in Uit voorraad_** wanneer een van deze scenario&#39;s zich voordoet:

- Alle opties zijn optioneel en alle bijbehorende producten zijn _Uit voorraad_.

- Sommige opties zijn vereist en de producten die aan om het even welke vereiste opties worden geassocieerd _Uit voorraad_.

De status van de bundelproductvoorraad is **_niet automatisch gewijzigd in Uit voorraad_** wanneer een van deze scenario&#39;s zich voordoet:

- Alle opties zijn optioneel en ten minste één gekoppeld product is _In voorraad_.

- Sommige opties zijn vereist en ten minste één bijbehorend product in elke vereiste optie is _In voorraad_.

## Te onthouden zaken

![Selectievakje](../assets/checkbox.png) Klanten kunnen _hun eigen_ bundelproduct.

![Selectievakje](../assets/checkbox.png) Bundelitems kunnen eenvoudig zijn of virtuele producten zonder aangepaste opties.

![Selectievakje](../assets/checkbox.png) De prijsweergave kan worden ingesteld op `Price Range` of `As Low As`.

![Selectievakje](../assets/checkbox.png) SKU en Gewicht kunnen `Fixed` of `Dynamic`.

![Selectievakje](../assets/checkbox.png) De hoeveelheid kan een vooraf ingestelde of door de gebruiker gedefinieerde waarde zijn. Wijs echter geen _[!UICONTROL User Defined]_eigenschap om het selectievakje in te schakelen of invoertypen te selecteren die meerdere malen zijn geselecteerd.

![Selectievakje](../assets/checkbox.png) Bundelobjecten kunnen samen of afzonderlijk worden verzonden.
