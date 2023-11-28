---
title: Een gedeelde catalogus maken
description: Leer hoe u gedeelde catalogi maakt en bestaande gedeelde catalogi dupliceert.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Een gedeelde catalogus maken

Wanneer een [gedeelde catalogus](catalog-shared.md) wordt gemaakt, maakt het systeem automatisch een [klantengroep](account-company-customer-group.md) met dezelfde naam. Als u bijvoorbeeld een gedeelde catalogus maakt met de naam _ABC-catalogus_, maakt het systeem ook een overeenkomstige _ABC-catalogus_ klantgroep. Het toewijzen van een bedrijf aan de gedeelde douanecatalogus is hoofdzakelijk het zelfde als het toewijzen van hen aan een klantengroep.

Een nieuwe gedeelde catalogus bevat geen producten, aangepaste prijzen of bedrijfskoppelingen. Een openbare catalogus, de standaard gedeelde catalogus die wordt gemaakt wanneer gedeelde catalogi worden ingeschakeld, wordt automatisch toegewezen aan gasten en aan klanten die niet aan een bedrijf zijn gekoppeld.

![Gedeelde catalogi](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Voordat een gedeelde catalogus kan worden gebruikt, moet u de volgende aspecten instellen:

- Catalogusbereik
- Productselectie
- Aangepaste prijzen
- Bedrijfstoewijzingen

## Prijsbereik

Als u een installatie met meerdere sites hebt, moet u het prijsbereik configureren voordat u gedeelde catalogi maakt. De [prijsbereik](../catalog/catalog-price-scope.md) kan worden ingesteld op `Global` of `Website`. Deze kan echter alleen aan het begin van het installatieproces worden ingesteld. De websitekiezer wordt weergegeven tijdens stap 2 van het dialoogvenster [gedeelde catalogusinstelling](catalog-shared-pricing-structure.md).

![Websitekiezer](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **Catalogus** en kiest u **Catalogus** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **Prijs** sectie.

1. Set **Bereik catalogusprijs** tot `Website`.

   ![Bereik catalogusprijs](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Stap 1: De gedeelde catalogus maken

Er zijn twee manieren om een gedeelde catalogus te maken. U kunt een gedeelde catalogus van elk type maken of een bestaande gedeelde catalogus dupliceren. Een nieuwe gedeelde catalogus bevat geen producten en is nog niet toegewezen aan een bedrijf.

### Methode 1: Een nieuwe gedeelde catalogus toevoegen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Shared Catalog]** en voer de volgende handelingen uit:

   - Voer een **[!UICONTROL Name]** voor de gedeelde catalogus.

     De naam die u toewijst, wordt in het hele dashboard voor beheerders en klanten gebruikt, indien van toepassing, om naar de gedeelde catalogus te verwijzen. Het wordt ook de naam van de overeenkomstige klantengroep.

   - Selecteren **[!UICONTROL Type]** : `Custom` of `Public`.

   - Kies de juiste **[!UICONTROL Customer Tax Class]** dat van toepassing is op aankopen uit de gedeelde catalogus.

     Voor meer informatie over de opstelling en de definitie van de belastingklasse, zie [Belastingklassen](../stores-purchase/tax-class.md).

     Het volgende voorbeeld toont een nieuwe douanecatalogus voor een specifieke groothandelsklant.

     ![Nieuwe gedeelde catalogus](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Enter **[!UICONTROL Description]**

1. Klik op **[!UICONTROL Save]**.

   De nieuwe catalogus wordt weergegeven in de _[!UICONTROL Shared Catalogs]_raster.

### Methode 2: Een bestaande gedeelde catalogus dupliceren

In een dubbele aangepaste catalogus blijven het prijsmodel en de structuur van het origineel behouden, maar niet die van de bedrijfsverenigingen. Er wordt ook een overeenkomende klantengroep gemaakt met dezelfde naam als de gedupliceerde catalogus. Standaard krijgt een gedupliceerde catalogus de naam _Dupliceren van_ de oorspronkelijke catalogus.

Als een openbare gedeelde catalogus wordt gedupliceerd, verandert het type van de gedupliceerde catalogus in `custom`.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Ga voor de gedeelde catalogus in het raster die u wilt dupliceren naar de **[!UICONTROL Action]** kolom en selecteer **[!UICONTROL General Settings]**.

1. Klik in de opties boven aan de pagina op **[!UICONTROL Duplicate]**.

   ![Gedeelde catalogus dupliceren](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Werk de volgende velden voor de nieuwe catalogus bij:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Klik op **[!UICONTROL Save]**.

   Het duplicaat wordt weergegeven in het dialoogvenster _[!UICONTROL Shared Catalogs]_raster, met een unieke id.

## Stap 2: De installatie voltooien

Nadat u een nieuwe gedeelde catalogus hebt gemaakt, moet deze zijn geconfigureerd met de juiste productselectie, [bedrijfstoewijzingen](catalog-shared-assign-companies.md), en [categoriemachtigingen](../catalog/category-permissions.md). Ga als volgt te werk [Prijs en structuur instellen](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[B2B-release 1.3.0](release-notes.md#b2b-v130) en hoger** — Wanneer u een gedeelde catalogus maakt, moet u elk [categorietoestemming](../catalog/category-permissions.md) voor de catalogus is ingesteld op _[!UICONTROL Allow for the Display Product Prices]_en_[!UICONTROL Add to Cart]_ voor klantengroepen die deze toegang in de montages van de catalogustoestemming worden toegewezen. Eerder werden deze instellingen automatisch ingesteld op `Deny` zelfs wanneer catalogusmachtigingen zijn ingesteld op `Allow`.

## Demo van gedeelde catalogus

Bekijk deze video voor een demonstratie van gedeeld catalogusbeheer:

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## Verwijzing naar gedeelde cataloguspagina

### Knopbalk

| Knop | Beschrijving |
|--- |--- |
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Gedeelde catalogi zonder de nieuwe gedeelde catalogus op te slaan. |
| [!UICONTROL Reset] | Hiermee wist u de vorm van niet-opgeslagen wijzigingen en herstelt u de oorspronkelijke details van de catalogus. |
| [!UICONTROL Save and Continue Edit] | Hiermee slaat u alle wijzigingen op en het formulier blijft geopend in de bewerkingsmodus. |
| [!UICONTROL Save] | Hiermee slaat u wijzigingen op, sluit u het formulier en keert u terug naar de pagina Gedeelde catalogi. |

{style="table-layout:auto"}

### Catalogusdetails

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Name] | Identificeert de gedeelde catalogus door Admin, en in de klantenrekeningen waar het beschikbaar is. De catalogusnaam moet beschrijvend zijn en mag niet langer zijn dan 32 tekens. U kunt geen twee gedeelde catalogi met dezelfde naam hebben. Maximum aantal tekens: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identificeert een catalogus met aangepaste prijzen die alleen beschikbaar is voor de specifieke ondernemingen waaraan deze is toegewezen.<br/>**[!UICONTROL Public]**- Identificeert de gedeelde catalogus die beschikbaar is voor alle gastbezoekers en voor aangemelde klanten die niet aan een bedrijf zijn gekoppeld. Een standaard openbare gedeelde catalogus wordt gemaakt wanneer [!DNL B2B for Adobe Commerce] is geïnstalleerd, maar moet door een opslagbeheerder worden gevormd. Er kan slechts één openbare gedeelde catalogus tegelijk bestaan. |
| [!UICONTROL Customer Tax Class] | Bepaalt de belastingklasse die wordt gebruikt voor aankopen uit de catalogus. De opties omvatten alle beschikbare belastingklassen. |
| [!UICONTROL Description] | Een korte uitleg van de manier waarop de catalogus moet worden gebruikt. |

{style="table-layout:auto"}

### Rasterkolommen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke id die is toegewezen aan een gedeelde catalogusentiteit. |
| [!UICONTROL Name] | De naam van de gedeelde catalogus. |
| [!UICONTROL Type] | Geeft het type gedeelde catalogus aan. Kan `Public` of `Custom`. |
| [!UICONTROL Created At] | De datum waarop de gedeelde catalogus in het systeem is gemaakt. |
| [!UICONTROL Created By] | De naam van de beheerder die een gedeelde catalogus heeft gemaakt. |
| [!UICONTROL Action] | De lijst met handelingen. Opties: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
