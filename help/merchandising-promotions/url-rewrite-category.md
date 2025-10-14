---
title: Categorie-URL herschrijft
description: Leer hoe je de rubriek URL herschrijft om links om te leiden naar de URL van een andere categorie in je Commerce-winkel.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Categorie-URL herschrijft

Als een categorie uit uw catalogus wordt verwijderd, kunt u een categorie gebruiken herschrijft om verbindingen aan URL van een andere categorie in uw opslag om te leiden. Denk in termen van _doel_ / _origineel verzoek_ of _opnieuw richt aan_ / _opnieuw richt van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

Als [&#x200B; automatische redirects &#x200B;](url-redirect-product-automatic.md) voor uw opslag worden toegelaten, is er geen behoefte om tot rewrite te leiden wanneer een sleutel van categorie [&#x200B; URL &#x200B;](../catalog/catalog-urls.md) wordt veranderd.

{{url-rewrite-skip}}

## Stap 1. Herschrijven plannen

Om fouten te vermijden, schrijf _omleiding aan_ weg en _omleiding van_ weg neer en omvat de Sleutel URL en het achtervoegsel (als toepasselijk).

Als u niet zeker weet, opent u elke categoriepagina in uw winkel en kopieert u het pad van de adresbalk van uw browser.

**Voorbeeld:**

Omleiden naar: `gear/backpacks-and-bags.html`

Omleiden vanaf: `gear/bags.html`

## Stap 2. Herschrijven maken

{{url-rewrite-params}}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is:

   - Voer in het zoekfilter boven aan de kolom **[!UICONTROL Request Path]** de URL-sleutel in van de categorie die u wilt omleiden en klik op **[!UICONTROL Search]** .

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke opslagweergave en opent u de omleidingsrecord in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]** . Klik op **[!UICONTROL OK]** om te bevestigen wanneer hierom wordt gevraagd.

1. Wanneer u terugkeert naar de _[!UICONTROL URL Rewrites]_&#x200B;pagina, klikt u op **[!UICONTROL Add URL Rewrite]**.

1. Stel **[!UICONTROL Create URL Rewrite]** in op `For category` en kies de doelcategorie in de boomstructuur die het doel van de omleiding is.

   ![&#x200B; URL herschrijft - kies categorie &#x200B;](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. In _URL herschrijft_ sectie, doe het volgende:

   - Als u meerdere winkels hebt, selecteert u de **[!UICONTROL Store]** waar het herschrijven van toepassing is.

   - Voer bij **[!UICONTROL Request Path]** de URL-sleutel in van de categorie die de klant aanvraagt. Dit is _opnieuw richt van_ categorie.

     >[!NOTE]
     >
     >Het aanvraagpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde verzoekweg gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Stel **[!UICONTROL Redirect]** in op een van de volgende opties:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte beschrijving in van het herschrijven.

   ![&#x200B; voeg URL herschrijven voor categorie &#x200B;](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"} toe

1. Lees het volgende voordat u de omleiding opslaat:

   - De koppeling in de linkerbovenhoek geeft de naam van de doelcategorie weer.
   - Het Weg van het Verzoek bevat de weg voor originele _omleiding van_ categorie.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   De nieuwe categorie herschrijven wordt boven aan het raster URL herschrijft weergegeven.

## Stap 3. Het resultaat testen

1. Ga naar de homepage van je winkel.

1. Voer een van de volgende handelingen uit:

   - Navigeer aan origineel _opnieuw richt van_ categorie.
   - In de adresbar van browser, ga de weg aan originele _omleiding van_ categorie onmiddellijk na opslag URL in en druk **[!UICONTROL Enter]**.

   De nieuwe doelcategorie wordt weergegeven in plaats van het oorspronkelijke categorieverzoek.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Geeft het type herschrijven aan. Het type kan niet worden gewijzigd nadat het herschrijven is gemaakt. Opties: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | De categorie die moet worden omgeleid. Afhankelijk van uw configuratie kan het aanvraagpad het achtervoegsel .html of .htm en de bovenliggende categorie bevatten. Het aanvraagpad moet uniek zijn en kan niet worden gebruikt door een andere omleiding. Als er een fout optreedt in het aanvraagpad, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar de bestemming van de omleiding te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**[!UICONTROL No]**- Er is geen omleiding opgegeven. Vele verrichtingen leiden verzoeken van dit type tot omleiding. Elke keer dat u bijvoorbeeld producten aan een categorie toevoegt, wordt een omleiding van het type `No` gemaakt in elke winkelweergave.<br/>**[!UICONTROL Temporary (302)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen. <br/>**[!UICONTROL Permanent (301)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}
