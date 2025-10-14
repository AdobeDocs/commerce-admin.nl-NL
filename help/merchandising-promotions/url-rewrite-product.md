---
title: URL van product herschrijft
description: Leer hoe u de URL van het product kunt gebruiken om koppelingen om te leiden naar de URL van een ander product in uw Commerce-winkel.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# URL van product herschrijft

Zorg voordat u begint dat u precies begrijpt wat omleiding moet doen. Denk in termen van _doel_ / _origineel verzoek_ of _opnieuw richt aan_ / _opnieuw richt van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

Als [&#x200B; automatische redirects &#x200B;](url-redirect-product-automatic.md) voor uw opslag worden toegelaten, is er geen behoefte om tot rewrite te leiden wanneer een product [&#x200B; Sleutel URL &#x200B;](../catalog/catalog-urls.md) wordt veranderd.

{{url-rewrite-skip}}

## Stap 1. Herschrijven plannen

Om fouten te vermijden, schrijf _omleiding aan_ weg en _omleiding van_ weg neer en omvat de Sleutel URL en het achtervoegsel (als toepasselijk).

Als u niet zeker bent, open elke productpagina in uw opslag, en kopieer de weg van de adresbar van uw browser. Wanneer het creëren van een product redirect, kunt u of de [&#x200B; categorieweg &#x200B;](../catalog/catalog-urls.md) omvatten of uitsluiten. In dit voorbeeld maken we een omleiding van een product zonder categoriepad.

### Product met categoriepad

Omleiden naar: `gear/bags/impulse-duffle.html`

Omleiden vanaf: `gear/bags/overnight-duffle.html`

### Product zonder categoriepad

Omleiden naar: `impulse-duffle.html`

Omleiden vanaf: `overnight-duffle.html`

## Stap 2. Herschrijven maken

{{url-rewrite-params}}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is.

   - Voer in het zoekfilter boven aan de kolom **[!UICONTROL Request Path]** de URL-sleutel in van de pagina die u wilt omleiden en klik op **[!UICONTROL Search]** .

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke winkelweergave en opent u deze in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]** . Klik op **[!UICONTROL OK]** om te bevestigen wanneer hierom wordt gevraagd.

1. In de hoger-juiste hoek van URL herschrijft pagina, voegt de klik **URL toe herschrijft**.

1. Stel **[!UICONTROL Create URL Rewrite]** in op `For product` .

1. Zoek in het raster het product dat het doel (doel) van de omleiding is en klik op de rij.

   ![&#x200B; URL herschrijft - product &#x200B;](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Klik onder de categoriestructuur op **[!UICONTROL Skip Category Selection]** .

   In dit voorbeeld bevat de omleiding geen categorie.

   ![&#x200B; het product URL herschrijft - overslaat categorieselectie &#x200B;](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   Met URL toevoegen voor herschrijven van productpagina wordt een koppeling naar het doel in de linkerbovenhoek weergegeven en in het veld Doelpad wordt de systeemversie van het pad weergegeven, die niet kan worden gewijzigd. In eerste instantie wordt in het veld Pad omleiden ook het doelpad weergegeven.

   - Als u meerdere winkelweergaven hebt, stelt u **[!UICONTROL Store]** in op de weergave waarop het herschrijven van toepassing is. Anders wordt voor elke weergave een rewrite gemaakt.

   - Vervang voor **[!UICONTROL Request Path]** de standaardinstelling door de URL-sleutel en het achtervoegsel (indien van toepassing) van de oorspronkelijke productaanvraag in te voeren. Dit is het _opnieuw richten van_ product dat u in de planningsstap identificeerde.

     >[!NOTE]
     >
     >Het aanvraagpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde verzoekweg gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Stel **[!UICONTROL Redirect Type]** in op een van de volgende opties:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte **[!UICONTROL Description]** van het herschrijven in.

   ![&#x200B; het product URL herschrijft - informatie &#x200B;](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Lees het volgende voordat u de omleiding opslaat:

   - De koppeling in de linkerbovenhoek geeft de naam van het doelproduct weer.
   - Het Weg van het Verzoek bevat de weg voor originele _omleiding van_ product.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   Het nieuwe product herschrijven verschijnt nu bij de bovenkant van URL herschrijft net.

## Stap 3. Het resultaat testen

1. Ga naar de homepage van je winkel.

1. Voer een van de volgende handelingen uit:

   - Navigeer aan origineel _omleiding van_ pagina van het productverzoek.
   - In de adresbar van browser, ga de weg aan origineel _in opnieuw richt van_ product onmiddellijk na opslag URL en druk **&#x200B;**&#x200B;binnengaan.

   Het nieuwe doelproduct wordt weergegeven in plaats van het oorspronkelijke productverzoek.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Geeft het type herschrijven aan. Het type kan niet worden gewijzigd nadat het herschrijven is gemaakt. Opties: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Het product dat moet worden omgeleid. Afhankelijk van uw configuratie bevat het aanvraagpad mogelijk het achtervoegsel `.html` of `.htm` en de categorie. Het verzoekpad moet uniek zijn en kan niet door een andere omleiding worden gebruikt. Als er een fout optreedt in het aanvraagpad, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar de bestemming van de omleiding te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**[!UICONTROL No]**- Er is geen omleiding opgegeven. Vele verrichtingen leiden verzoeken van dit type tot omleiding. Elke keer dat u bijvoorbeeld producten aan een categorie toevoegt, wordt een omleiding van het type `No` gemaakt in elke winkelweergave.<br/>**[!UICONTROL Temporary (302)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen. <br/>**[!UICONTROL Permanent (301)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}

## Meerdere URL&#39;s worden herschreven

U kunt URL herschrijvingen voor veelvoudige of alle producten snel bijwerken gelijktijdig gebruikend de volgende stappen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer alle producten waarvoor u URL wilt bijwerken herschrijft.

1. Kies onder _[!UICONTROL Actions]_&#x200B;de optie **[!UICONTROL Update attributes]**&#x200B;om meerdere of alle herschrijvingen bij te werken.

1. Klik onder _[!UICONTROL PRODUCTS INFORMATION]_&#x200B;op de tab **[!UICONTROL Websites]**.

1. Selecteer in de sectie _[!UICONTROL Add Product To Websites]_&#x200B;alle websites waarvan u de URL wilt herstellen.

1. Klik op **[!UICONTROL Save]** als u klaar bent om bij te werken.

>[!NOTE]
>
>Alle geselecteerde producten worden opnieuw aan de geselecteerde websites gelezen en URL-herboekingen worden opnieuw gegenereerd.

![&#x200B; de Attributen van de Update - werk veelvoudige URL herschrijft &#x200B;](./assets/url-rewrites-update.png){width="600" zoomable="yes"} bij
