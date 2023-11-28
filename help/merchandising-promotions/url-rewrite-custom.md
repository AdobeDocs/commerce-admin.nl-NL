---
title: Aangepaste URL wordt opnieuw geschreven
description: Leer hoe u aangepaste URL-herschriften kunt gebruiken om diverse omleidingen in uw winkel te beheren.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Aangepaste URL wordt opnieuw geschreven

Een aangepaste rewrite kan worden gebruikt om diverse omleidingen te beheren, zoals het omleiden van een pagina van uw winkel naar een externe website. U hebt bijvoorbeeld twee Commerce-websites, elk met een eigen domein. U kunt een aangepaste omleiding gebruiken om aanvragen voor een product, categorie of pagina om te leiden naar de andere website. In tegenstelling tot andere omleidingstypen wordt het doel van een aangepaste omleiding niet gekozen uit een lijst met bestaande pagina&#39;s in uw winkel.

Voordat u begint, moet u controleren of u precies begrijpt wat omleiding precies inhoudt. Denk aan _target_ / _bron_ of _omleiden naar_ / _omleiden van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

## Stap 1. Herschrijven plannen

Als u fouten wilt voorkomen, noteert u de URL van het dialoogvenster _omleiden naar_ pagina en de URL-sleutel van de _omleiden van_ pagina.

Als u niet zeker weet, opent u elke pagina en kopieert u de URL vanuit de adresbalk van uw browser.

**Voorbeeld**

Omleiden naar:

    http://www.different-website.com/page.html

Omleiden vanaf:

    cms-pagina
    category.html
    category/subcategory.html
    product.html
    category/product.html

## Stap 2. Herschrijven maken

{{url-rewrite-params}}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is:

   - In het zoekfilter boven aan het dialoogvenster **[!UICONTROL Request Path]** voert u de URL-sleutel in van de pagina die opnieuw moet worden omgeleid en klikt u op **[!UICONTROL Search]**.

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke winkelweergave en opent u deze in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]**. Klik op **[!UICONTROL OK]** ter bevestiging.

1. Als u terugkeert naar de pagina URL herschrijft, klikt u op **[!UICONTROL Add URL Rewrite]**.

1. Set **[!UICONTROL Create URL Rewrite]** tot `Custom`.

   ![URL herschrijft - aangepast](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. Voer onder Informatie voor herschrijven van URL de volgende handelingen uit:

   - Als u meerdere winkelweergaven hebt, selecteert u de **[!UICONTROL Store]** waar de herschrijving van toepassing is.

   - Voor **[!UICONTROL Request Path]** Voer de URL-sleutel en het pad (indien van toepassing) in van de product-, categorie- of CMS-pagina die omgeleid moet worden.

     >[!NOTE]
     >
     >Het aanvraagpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde verzoekweg gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Voor **[!UICONTROL Target Path]** Voer de URL van het doel in. Als het doel zich op een andere website bevindt, voert u de volledig gekwalificeerde URL in.

   - Set **Omleiden** op een van de volgende wijzen:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte beschrijving in van het herschrijven.

1. Lees het volgende voordat u de omleiding opslaat:

   - De [!UICONTROL Request Path] bevat de URL-sleutel of het oorspronkelijke pad _omleiden van_ pagina.
   - De [!UICONTROL Target Path] bevat de URL van het dialoogvenster _omleiden naar_ pagina.

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
| [!UICONTROL Request Path] | De pagina die moet worden omgeleid. Het aanvraagpad moet uniek zijn en kan niet worden gebruikt door een andere omleiding. Als u een foutbericht ontvangt dat het aanvraagpad bestaat, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar het doel te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**Nee** - Er is geen omleiding opgegeven. <br/>**[!UICONTROL Temporary (302)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen.<br/>**[!UICONTROL Permanent (301)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}
