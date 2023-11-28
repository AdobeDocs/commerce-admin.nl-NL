---
title: URL van product herschrijft
description: Leer hoe u de URL van het product kunt gebruiken om koppelingen om te leiden naar de URL van een ander product in uw winkel.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# URL van product herschrijft

Zorg voordat u begint dat u precies begrijpt wat omleiding moet doen. Denk aan _target_ / _oorspronkelijke aanvraag_ of _omleiden naar_ / _omleiden van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

Indien [automatische omleidingen](url-redirect-product-automatic.md) zijn ingeschakeld voor uw winkel, hoeft u het product niet opnieuw te schrijven [URL-sleutel](../catalog/catalog-urls.md) is gewijzigd.

{{url-rewrite-skip}}

## Stap 1. Herschrijven plannen

Om fouten te voorkomen, noteer de _omleiden naar_ pad en _omleiden van_ en neemt u de URL-sleutel en het achtervoegsel op (indien van toepassing).

Als u niet zeker bent, open elke productpagina in uw opslag, en kopieer de weg van de adresbar van uw browser. Wanneer u een omleiding van een product maakt, kunt u de opdracht [categoriepad](../catalog/catalog-urls.md). In dit voorbeeld maken we een omleiding van een product zonder categoriepad.

### Product met categoriepad

Omleiden naar: `gear/bags/impulse-duffle.html`

Omleiden vanaf: `gear/bags/overnight-duffle.html`

### Product zonder categoriepad

Omleiden naar: `impulse-duffle.html`

Omleiden vanaf: `overnight-duffle.html`

## Stap 2. Herschrijven maken

{{url-rewrite-params}}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is.

   - In het zoekfilter boven aan het dialoogvenster **[!UICONTROL Request Path]** voert u de URL-sleutel in van de pagina die u wilt omleiden en klikt u op **[!UICONTROL Search]**.

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke winkelweergave en opent u deze in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]**. Klik op **[!UICONTROL OK]** ter bevestiging.

1. Klik in de rechterbovenhoek van de pagina URL herschrijft op **URL-herschrijven toevoegen**.

1. Set **[!UICONTROL Create URL Rewrite]** tot `For product`.

1. Zoek in het raster het product dat het doel (doel) van de omleiding is en klik op de rij.

   ![URL herschrijft - product](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Klik onder de categoriestructuur op **[!UICONTROL Skip Category Selection]**.

   In dit voorbeeld bevat de omleiding geen categorie.

   ![URL van product herschrijven - categorieselectie overslaan](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   Met URL toevoegen voor herschrijven van productpagina wordt een koppeling naar het doel in de linkerbovenhoek weergegeven en in het veld Doelpad wordt de systeemversie van het pad weergegeven, die niet kan worden gewijzigd. In eerste instantie wordt in het veld Pad omleiden ook het doelpad weergegeven.

   - Als u meerdere winkelweergaven hebt, stelt u **[!UICONTROL Store]** op de weergave waarop de herschrijven van toepassing is. Anders wordt voor elke weergave een rewrite gemaakt.

   - Voor **[!UICONTROL Request Path]**, vervangt u de standaardinstelling door de URL-sleutel en het achtervoegsel (indien van toepassing) van de oorspronkelijke productaanvraag in te voeren. Dit is het _omleiden van_ product dat u in de planningsstap hebt geïdentificeerd.

     >[!NOTE]
     >
     >Het aanvraagpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde verzoekweg gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Set **[!UICONTROL Redirect Type]** op een van de volgende wijzen:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte beschrijving in **[!UICONTROL Description]** van de herschrijving.

   ![URL van product herschrijven - informatie](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Lees het volgende voordat u de omleiding opslaat:

   - De koppeling in de linkerbovenhoek geeft de naam van het doelproduct weer.
   - Het verzoekpad bevat het pad voor het origineel _omleiden van_ product.

1. Klik op **[!UICONTROL Save]**.

   Het nieuwe product herschrijven verschijnt nu bij de bovenkant van URL herschrijft net.

## Stap 3. Het resultaat testen

1. Ga naar de homepage van je winkel.

1. Voer een van de volgende handelingen uit:

   - Naar origineel navigeren _omleiden van_ pagina met productaanvragen.
   - Voer op de adresbalk van de browser het pad naar het origineel in _omleiden van_ product direct na de winkel-URL en druk op **Enter**.

   Het nieuwe doelproduct wordt weergegeven in plaats van het oorspronkelijke productverzoek.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Geeft het type herschrijven aan. Het type kan niet worden gewijzigd nadat het herschrijven is gemaakt. Opties: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Het product dat moet worden omgeleid. Afhankelijk van uw configuratie, zou de Weg van het Verzoek kunnen omvatten `.html` of `.htm` achtervoegsel en categorie. Het verzoekpad moet uniek zijn en kan niet door een andere omleiding worden gebruikt. Als er een fout optreedt in het aanvraagpad, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar de bestemming van de omleiding te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**[!UICONTROL No]**- Er is geen omleiding opgegeven. Vele verrichtingen leiden verzoeken van dit type tot omleiding. Elke keer dat u bijvoorbeeld producten aan een categorie toevoegt, wordt de opdracht `No` wordt er tekst gemaakt in elke winkelweergave.<br/>**[!UICONTROL Temporary (302)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen. <br/>**[!UICONTROL Permanent (301)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}

## Meerdere URL&#39;s worden herschreven

U kunt URL herschrijvingen voor veelvoudige of alle producten snel bijwerken gelijktijdig gebruikend de volgende stappen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer alle producten waarvoor u URL wilt bijwerken herschrijft.

1. Onder _[!UICONTROL Actions]_, kiest u **[!UICONTROL Update attributes]**om meerdere of alle herschrijvingen bij te werken.

1. Onder _[!UICONTROL PRODUCTS INFORMATION]_klikt u op de knop **[!UICONTROL Websites]**tab.

1. In de _[!UICONTROL Add Product To Websites]_selecteert u alle websites waarvan u de URL wilt herstellen.

1. Als u wilt bijwerken, klikt u op **[!UICONTROL Save]**.

>[!NOTE]
>
>Alle geselecteerde producten worden opnieuw aan de geselecteerde websites gelezen en URL-herboekingen worden opnieuw gegenereerd.

![Kenmerken bijwerken - meerdere URL-herschrijvingen bijwerken](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
