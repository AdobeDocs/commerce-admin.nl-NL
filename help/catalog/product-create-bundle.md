---
title: Bundel
description: Leer hoe u een bundelproduct maakt waarmee kopers een aangepast product in uw winkel kunnen maken.
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '1603'
ht-degree: 0%

---

# Bundel

Een bundel is a _bouwt uw eigen_, aanpasbaar product. Elk item in een bundel kan op een van de volgende producttypen worden gebaseerd:

- [Eenvoudig product](product-create-simple.md)
- [Virtueel product](product-create-virtual.md)

![ Bundel product ](./assets/product-bundle.png){width="700" zoomable="yes"}

De opties worden weergegeven wanneer de klant op **[!UICONTROL Customize]** of **[!UICONTROL Add to Cart]** klikt. Omdat de producten die in de bundel inbegrepen zijn variëren, kan SKU, de Prijs, en het Gewicht aan of een dynamische of vaste waarde worden geplaatst.

>[!NOTE]
>
>De minimum Geadverteerde Prijs (MAP) is niet beschikbaar voor Bundelproducten die dynamische prijsstelling gebruiken.

>[!NOTE]
>
>Het bovenliggende bundelproduct wordt altijd automatisch weergegeven als een up-sell-product voor alle onderliggende producten.

Als [ Onmiddellijke Aankoop ](../stores-purchase/checkout-instant-purchase.md) beschikbaar is, verschijnt de _Onmiddellijke knoop van de Aankoop_ onder _toevoegt aan Kar_ knoop voor elk punt in de bundel.

![ pas Bundel ](./assets/product-bundle-customize.png){width="600" zoomable="yes"} aan

De volgende instructies nemen u door het proces om een bundelproduct tot stand te brengen gebruikend a [ productmalplaatje ](attribute-sets.md), vereiste gebieden, en basismontages. Elk vereist gebied is duidelijk met een rode asterisk (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

## Stap 1: Kies het producttype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. In de hoger-juiste hoek op het _[!UICONTROL Add Product]_( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"} ) menu, kies **[!UICONTROL Bundle Product]**.

   ![ voeg Bundelproduct ](./assets/product-add-bundle.png){width="700" zoomable="yes"} toe

## Stap 2: Kies de kenmerkset

Om de [ geplaatste attributen ](attribute-sets.md) te kiezen die als malplaatje voor het product wordt gebruikt, doe één van het volgende:

- Voer bij **[!UICONTROL Search]** de naam in van de kenmerkset,
- Kies in de lijst de kenmerkset die u wilt gebruiken.

Het formulier wordt bijgewerkt met de wijziging.

![ kies malplaatje ](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Stap 3: Voer de vereiste instellingen in

1. Voer het product **[!UICONTROL Product Name]** in.

1. Accepteer de standaardwaarde **[!UICONTROL SKU]** die is gebaseerd op de productnaam of voer een andere waarde in.

   Ga als volgt te werk om het type SKU te bepalen dat aan elk bundelitem is toegewezen:

   - Een **[!UICONTROL Dynamic SKU]** kan automatisch worden toegewezen aan elk bundelitem door een achtervoegsel toe te voegen aan de standaard-SKU. Standaard is dit ingesteld op `Yes` .

   - Als u liever een unieke SKU voor elk bundelitem wilt toewijzen, stelt u **[!UICONTROL Dynamic SKU]** in op `No` .

   ![ Dynamische SKU en prijs ](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit om de prijs van de bundel te bepalen:

   - Als u wilt dat de prijs de door de klant gekozen opties weerspiegelt, stelt u **[!UICONTROL Dynamic Price]** in op `Yes` en laat u **[!UICONTROL Price]** leeg. In dit geval heeft een bundelproduct geen eigen prijs uit de catalogus en wordt de productprijs afgeleid van de prijs van de afzonderlijke producten in de bundel.

   - Als u een vaste prijs voor de bundel wilt berekenen, stelt u **[!UICONTROL Dynamic Price]** in op `No` en voert u de **[!UICONTROL Price]** in die u voor de bundel wilt laden.

   >[!NOTE]
   >
   >[!UICONTROL Special Price] en [!UICONTROL Customer Group Price] (Tier-prijs) worden altijd ingesteld als het kortingspercentage voor alle typen bundelproducten.

1. Stel **[!UICONTROL Enable Product]** in op `No` omdat het product nog niet kan worden gepubliceerd.

1. Klik op **[!UICONTROL Save]** en ga verder.

   Wanneer het product wordt bewaard, verschijnt de [ verkiesster van de Mening van de Opslag ](introduction.md#product-scope) in de upper-left hoek.

1. Kies de locatie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![ kies de Mening van de Opslag ](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Stap 4: De basisinstellingen voltooien

1. Als de bundel Vaste Prijsbepaling heeft, plaats **[!UICONTROL Tax Class]** aan één van het volgende:

   - `None`
   - `Taxable Goods`

   Als de bundel Dynamische Prijsbepaling heeft, wordt de belasting bepaald voor **_elk_** bundelpunt. Als de bundel Vaste Prijsbepaling heeft, wordt de belasting bepaald voor het **_volledige_** bundelproduct.

1. Let op het volgende:

   - **[!UICONTROL Quantity]** is niet beschikbaar omdat de waarde wordt bepaald voor elk bundelitem.

   - Standaard is de waarde van **[!UICONTROL Stock Status]** ingesteld op `In Stock` .

1. Voer een van de volgende handelingen uit om het gewicht van de bundel te bepalen:

   - Als u wilt dat het gewicht de door de klant gekozen opties weerspiegelt, stelt u **[!UICONTROL Dynamic Weight]** set `Yes` in en laat u **[!UICONTROL Weight]** leeg.

   - Als u een vaste dikte aan de bundel wilt toewijzen, stelt u **[!UICONTROL Dynamic Weight]** in op `No` en voert u de **[!UICONTROL Weight]** van de bundel in.

   ![ Dynamisch Gewicht ](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. Om het product in de lijst van [ nieuwe producten ](../content-design/widget-new-products-list.md) te voorzien, selecteer **[!UICONTROL Set Product as New]** checkbox.

1. Accepteer de standaardinstelling **[!UICONTROL Visibility]** van `Catalog, Search` .

1. Als u _[!UICONTROL Categories]_aan het product wilt toewijzen, klikt u op het vak **[!UICONTROL Select…]**en voert u een van de volgende handelingen uit:

   **kies een bestaande categorie:**

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van elke categorie die u wilt toewijzen.

   ![ selecteer één of meerdere categorieën voor het bundelproduct ](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **creeer een categorie:**

   - Klik op **[!UICONTROL New Category]**.

   - Voer de **[!UICONTROL Category Name]** in en kies de **[!UICONTROL Parent Category]** die de positie in de menustructuur bepaalt.

   - Klik op **[!UICONTROL Create Category]**.

1. Kies de **[!UICONTROL Country of Manufacture]** .

   Er kunnen aanvullende kenmerken zijn die het product beschrijven. De selectie varieert kenmerkset en u kunt deze later voltooien.

## Stap 5: Voeg de bundelitems toe

De sectie _[!UICONTROL Bundle Items]_wordt gebruikt om items toe te voegen aan een bundelproducttype en om de huidige selectie van items te bewerken.

![ Bundel punten die voor een product ](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"} worden bepaald

1. De rol neer aan de _sectie van de Punten van de Bundel_ en reeks **[!UICONTROL Ship Bundle Items]** aan één van het volgende:

   - `Separately`
   - `Together`

   Als u `Together` selecteert, moeten alle bundelpunten de zelfde [ bron ](../inventory-management/sources-manage.md) worden toegewezen.

1. Klik op **[!UICONTROL Add Option]** en voer de volgende handelingen uit:

   - Voer een **[!UICONTROL Option Title]** in dat als veldlabel moet worden gebruikt.

   - Stel **[!UICONTROL Input Type]** in op een van de volgende opties:

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - Schakel het selectievakje **[!UICONTROL Required]** in om van het veld een verplicht item te maken.

   - Klik op **[!UICONTROL Add Products to Option]** en schakel het selectievakje in van elk product dat u in deze optie wilt opnemen.

     Als er vele producten zijn, gebruik de lijstfilters en pagineringscontroles om de producten te vinden u nodig hebt.

   - Klik op **[!UICONTROL Add Selected Products]**.

     ![ voeg Geselecteerde Producten ](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"} toe

   - Nadat de punten in de _sectie van Opties_ verschijnen, kies een punt om de **[!UICONTROL Default]** selectie te zijn.

   - In de _StandaardHoeveelheid_ kolom, ga de hoeveelheid van elk punt in dat aan de bundel moet worden toegevoegd wanneer een klant het punt kiest.

   - Selecteer **[!UICONTROL User Defined]** als u klanten wilt toestaan de hoeveelheid van een bundelitem te wijzigen.


     >[!NOTE]
     >
     >De hoeveelheid kan een vooraf ingestelde of door de gebruiker gedefinieerde waarde zijn. Wijs de eigenschap _[!UICONTROL User Defined]_echter niet toe aan een selectievakje of aan invoertypen die een meervoudige selectie bevatten.

     Standaard kan de standaardhoeveelheid die in een bundelitem is opgenomen, niet door de klant worden gewijzigd. De klant kan echter de hoeveelheid van het item invoeren die in de bundel moet worden opgenomen.

     Als de Standaardhoeveelheid van de Sprite-statusbalk bijvoorbeeld is ingesteld op `2` en de klant geeft `4` van die bundeloptie de opdracht, is het totale aantal gekochte ballen `8` .

     ![ Detail van het Punt ](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. Herhaal deze stappen voor elk item dat u aan de bundel wilt toevoegen.

1. Om de orde van punten in een bundelsectie te veranderen, klik de _Beweging_ ( ![ pictogram van de Beweging ](../assets/icon-move.png) ) aan het begin van de rij en sleep het punt in positie.

   ![ verander de orde van de Punten van de Bundel ](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   De volgorde van items kan ook worden gewijzigd in de gegevens van een geëxporteerd bundelproduct en vervolgens opnieuw worden geïmporteerd in de catalogus. Voor meer informatie, zie [ het Invoeren van de Producten van de Bundel ](../systems/data-transfer-bundle-products.md).

   Voor een betere weergave van de werkruimte, vouwt u eerst elke sectie samen en sleept u deze naar de gewenste positie.

1. Om om het even welk punt uit de bundel te verwijderen, klik het **[!UICONTROL Delete]** ( ![ pictogram van het Afval ](../assets/icon-delete-trashcan.png)) pictogram.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

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

## Stap 7: Publish het product

1. Als u bereid bent om het product in de catalogus te publiceren, plaats **[!UICONTROL Enable Product]** aan `Yes` ( ![ Wissel ja ](../assets/toggle-yes.png)).

1. Voer een van de volgende handelingen uit:

   **Methode 1:** sparen en voorproef

   - Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

   - Om het product in uw opslag te bekijken, verkies **[!UICONTROL Customer View]** op _Admin_ ( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-black.png)) menu.

     De winkel wordt geopend in een nieuw browsertabblad.

   ![ Mening van de Klant ](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Methode 2:** sparen en sluit

   Voor _[!UICONTROL Save]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu, kies **[!UICONTROL Save & Close]**.

## Invoerbesturingselementen

| Besturing | Beschrijving | Voorbeeld |
|--- |--- |--- |
| [!UICONTROL Drop-down] | Hiermee geeft u een vervolgkeuzelijst met opties weer met de productnaam en de prijs. Er kan slechts één item worden geselecteerd. | ![ drop-down ](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | Hiermee geeft u een keuzerondje voor elke optie weer, gevolgd door de productnaam en -prijs. Er kan slechts één item worden geselecteerd. | ![ Keuzerondjes ](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | Hiermee wordt voor elke optie een selectievakje weergegeven, gevolgd door de productnaam en de prijs. U kunt meerdere items selecteren. | ![ Checkbox ](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | Hiermee geeft u een lijst met opties weer met de productnaam en de prijs. Als u meerdere items wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elk item. | ![ Veelvoudige Uitgezochte ](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

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

De status van de de productvoorraad van de bundel wordt **_automatisch veranderd in uit Voorraad_** wanneer één van beiden van deze scenario&#39;s voorkomt:

- Alle opties zijn facultatief en alle bijbehorende producten zijn _uit Voorraad_.

- Sommige opties worden vereist en de producten die aan om het even welke vereiste opties worden geassocieerd zijn _uit Voorraad_.

De status van de de productvoorraad van de bundel is **_niet automatisch veranderd in uit voorraad_** wanneer één van beiden van deze scenario&#39;s voorkomt:

- Alle opties zijn facultatief en minstens één geassocieerd product is _in Voorraad_.

- Sommige opties worden vereist en minstens één geassocieerd product in elke vereiste optie is _in Voorraad_.

## Te onthouden zaken

![ Checkbox ](../assets/checkbox.png) Klanten kunnen _hun eigen_ bundelproduct bouwen.

![ Checkbox ](../assets/checkbox.png) Alle kindproducten worden toegewezen en unassigned van het bundelproduct **_globaal_** voor alle websites, opslag, en opslagmeningen tezelfdertijd.

![ checkbox ](../assets/checkbox.png) de punten van de Bundel kunnen eenvoudige of virtuele producten zonder douaneopties zijn.

![ Checkbox ](../assets/checkbox.png) de Mening van de Prijs kan aan of `Price Range` of `As Low As` worden geplaatst.

![ Checkbox ](../assets/checkbox.png) SKU en Gewicht kunnen of `Fixed` of `Dynamic` zijn.

![ Checkbox ](../assets/checkbox.png) de hoeveelheid kan een vooraf ingestelde of user-defined waarde zijn. Wijs de eigenschap _[!UICONTROL User Defined]_echter niet toe aan een selectievakje of aan invoertypen die een meervoudige selectie bevatten.

](../assets/checkbox.png) de punten van de Bundel van 0} Checkbox {kunnen samen of afzonderlijk worden verscheept.![

![ CheckBox ](../assets/checkbox.png) de bundelproduct van de Ouder wordt altijd getoond als omhoog-verkoopproduct voor al zijn kindproducten automatisch.

![ Checkbox ](../assets/checkbox.png) [!UICONTROL Special Price] en [!UICONTROL Customer Group Price] (de Prijs van de Rij) worden altijd geplaatst als disconteringspercentage voor alle types van bundelproduct.
