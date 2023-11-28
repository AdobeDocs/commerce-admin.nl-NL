---
title: Categorie-URL herschrijft
description: Leer hoe u URL-codes voor categorieën kunt gebruiken om koppelingen om te leiden naar de URL van een andere categorie in uw winkel.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Categorie-URL herschrijft

Als een categorie uit uw catalogus wordt verwijderd, kunt u een categorie gebruiken herschrijft om verbindingen aan URL van een andere categorie in uw opslag om te leiden. Denk aan _target_ / _oorspronkelijke aanvraag_  of _omleiden naar_ / _omleiden van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

Indien [automatische omleidingen](url-redirect-product-automatic.md) zijn ingeschakeld voor uw winkel, hoeft u geen herschrijven te maken wanneer een categorie [URL-sleutel](../catalog/catalog-urls.md) is gewijzigd.

{{url-rewrite-skip}}

## Stap 1. Herschrijven plannen

Om fouten te voorkomen, noteer de _omleiden naar_ pad en _omleiden van_ en neemt u de URL-sleutel en het achtervoegsel op (indien van toepassing).

Als u niet zeker weet, opent u elke categoriepagina in uw winkel en kopieert u het pad van de adresbalk van uw browser.

**Voorbeeld:**

Omleiden naar: `gear/backpacks-and-bags.html`

Omleiden vanaf: `gear/bags.html`

## Stap 2. Herschrijven maken

{{url-rewrite-params}}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is:

   - In het zoekfilter boven aan het dialoogvenster **[!UICONTROL Request Path]** kolom, voert u de URL-sleutel in van de categorie die opnieuw moet worden omgeleid en klikt u **[!UICONTROL Search]**.

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke opslagweergave en opent u de omleidingsrecord in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]**. Klik op **[!UICONTROL OK]** ter bevestiging.

1. Wanneer u terugkeert naar de _[!UICONTROL URL Rewrites]_pagina, klikt u **[!UICONTROL Add URL Rewrite]**.

1. Set **[!UICONTROL Create URL Rewrite]** tot `For category` en kiest u de doelcategorie in de boomstructuur die het doel van de omleiding is.

   ![URL herschrijven - categorie kiezen](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. In de _URL herschrijven_ Ga als volgt te werk:

   - Als u meerdere winkels hebt, selecteert u de optie **[!UICONTROL Store]** waar de herschrijving van toepassing is.

   - Voor **[!UICONTROL Request Path]**, voert u de URL-sleutel in van de categorie die de klant aanvraagt. Dit is het _omleiden van_ categorie.

     >[!NOTE]
     >
     >Het aanvraagpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde verzoekweg gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Set **[!UICONTROL Redirect]** op een van de volgende wijzen:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte beschrijving in van het herschrijven.

   ![URL-herschrijven toevoegen voor categorie](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Lees het volgende voordat u de omleiding opslaat:

   - De koppeling in de linkerbovenhoek geeft de naam van de doelcategorie weer.
   - Het verzoekpad bevat het pad voor het origineel _omleiden van_ categorie.

1. Klik op **[!UICONTROL Save]** knop.

   De nieuwe categorie herschrijven wordt boven aan het raster URL herschrijft weergegeven.

## Stap 3. Het resultaat testen

1. Ga naar de homepage van je winkel.

1. Voer een van de volgende handelingen uit:

   - Naar origineel navigeren _omleiden van_ categorie.
   - Voer op de adresbalk van de browser het pad naar het origineel in _omleiden van_ categorie direct na de URL van de winkel en druk op **[!UICONTROL Enter]**.

   De nieuwe doelcategorie wordt weergegeven in plaats van het oorspronkelijke categorieverzoek.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Geeft het type herschrijven aan. Het type kan niet worden gewijzigd nadat het herschrijven is gemaakt. Opties: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | De categorie die moet worden omgeleid. Afhankelijk van uw configuratie kan het aanvraagpad het achtervoegsel .html of .htm en de bovenliggende categorie bevatten. Het aanvraagpad moet uniek zijn en kan niet worden gebruikt door een andere omleiding. Als er een fout optreedt in het aanvraagpad, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar de bestemming van de omleiding te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**[!UICONTROL No]**- Er is geen omleiding opgegeven. Vele verrichtingen leiden verzoeken van dit type tot omleiding. Elke keer dat u bijvoorbeeld producten aan een categorie toevoegt, wordt de opdracht `No` wordt er tekst gemaakt in elke winkelweergave.<br/>**[!UICONTROL Temporary (302)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen. <br/>**[!UICONTROL Permanent (301)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}
