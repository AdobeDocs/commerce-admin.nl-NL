---
title: URL van inhoudspagina herschrijft
description: Leer hoe u URL van inhoudspagina gebruikt om koppelingen om te leiden naar de URL van een andere inhoudspagina in uw winkel van de Handel.
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# URL van inhoudspagina herschrijft

Voordat u begint, moet u controleren of u precies begrijpt wat omleiding precies inhoudt. Denk aan _target_ / _bron_ of _omleiden naar_ / _omleiden van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

![URL herschrijft - CMS-pagina](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## Stap 1. Herschrijven plannen

Als u fouten wilt voorkomen, noteert u de URL-sleutel van het dialoogvenster _omleiden naar_ pagina en _omleiden van_ pagina.

Als u niet zeker bent, open elke pagina in uw opslag, en kopieer de weg van de adresbar van uw browser.

### CMS-paginapad

Omleiden naar: `new-page`

Omleiden vanaf: `old-page`

## Stap 2. Herschrijven maken

{{url-rewrite-params}}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is.

   - In het zoekfilter boven aan het dialoogvenster **[!UICONTROL Request Path]** voert u de URL-sleutel in van de pagina die opnieuw moet worden omgeleid en klikt u op **[!UICONTROL Search]**.

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke winkelweergave en opent u deze in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]**. Klik op **[!UICONTROL OK]** ter bevestiging.

1. Als u terugkeert naar de pagina URL herschrijft, klikt u op **[!UICONTROL Add URL Rewrite]**.

1. Set **[!UICONTROL Create URL Rewrite]** tot `for CMS page`.

1. Zoek de nieuwe doelpagina in het raster en open de bewerkingsmodus.

   ![URL-herschrijven toevoegen - voor CMS-pagina](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. Voer onder Informatie voor herschrijven van URL de volgende handelingen uit:

   - Als u meerdere winkelweergaven hebt, selecteert u de **[!UICONTROL Store]** waar de herschrijving van toepassing is.

   - Voor **[!UICONTROL Request Path]**, voert u de URL-sleutel in van de oorspronkelijke pagina die de klant aanvraagt. Dit is het _omleiden van_ pagina.

     >[!NOTE]
     >
     >Het verzoekpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde Weg van het Verzoek gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Set **[!UICONTROL Redirect]** op een van de volgende wijzen:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte beschrijving in van het herschrijven.

   ![URL-herschrijfgegevens](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. Lees het volgende voordat u de omleiding opslaat:

   - De koppeling in de linkerbovenhoek geeft de naam van de doelpagina weer.
   - Het verzoekpad bevat het pad voor het origineel _omleiden van_ pagina.

1. Klik op **[!UICONTROL Save]**.

   Het nieuwe herschrijven verschijnt in het net bij de bovenkant van de lijst.

## Stap 3. Het resultaat testen

1. Ga naar de homepage van je winkel.

1. Voer een van de volgende handelingen uit:

   - Naar origineel navigeren _omleiden van_ pagina.
   - Voer in de adresbalk van de browser de naam in van het origineel _omleiden van_ pagina direct na de winkel-URL en druk op **Enter**.

   De nieuwe doelpagina wordt weergegeven in plaats van de oorspronkelijke paginaaanvraag.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Geeft het type herschrijven aan. Het type kan niet worden gewijzigd nadat het herschrijven is gemaakt. Opties: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | De CMS-pagina die moet worden omgeleid. Het aanvraagpad moet uniek zijn en kan niet worden gebruikt door een andere omleiding. Als u een foutbericht ontvangt dat het aanvraagpad bestaat, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar het doel te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**[!UICONTROL No]**- Er is geen omleiding opgegeven.<br/>**[!UICONTROL Temporary (302)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen. <br/>**[!UICONTROL Permanent (301)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}
