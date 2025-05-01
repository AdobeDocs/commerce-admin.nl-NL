---
title: Aangepaste URL wordt opnieuw geschreven
description: Leer hoe u aangepaste URL-herschriften kunt gebruiken om diverse omleidingen in uw Commerce-winkel te beheren.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Aangepaste URL wordt opnieuw geschreven

Een aangepaste rewrite kan worden gebruikt om diverse omleidingen te beheren, zoals het omleiden van een pagina van uw winkel naar een externe website. U hebt bijvoorbeeld twee Commerce-websites, elk met een eigen domein. U kunt een aangepaste omleiding gebruiken om aanvragen voor een product, categorie of pagina om te leiden naar de andere website. In tegenstelling tot andere omleidingstypen wordt het doel van een aangepaste omleiding niet gekozen uit een lijst met bestaande pagina&#39;s in uw winkel.

Voordat u begint, moet u controleren of u precies begrijpt wat omleiding precies inhoudt. Denk in termen van _doel_ / _bron_ of _opnieuw richt aan_ / _opnieuw richt van_. Hoewel mensen nog steeds vanuit zoekmachines of verouderde koppelingen naar de vorige pagina kunnen navigeren, zorgt de omleiding ervoor dat de winkel naar het nieuwe doel overschakelt.

## Stap 1. Herschrijven plannen

Om fouten te vermijden, schrijf URL van _omleiding aan_ pagina en de sleutel URL van _om van_ pagina.

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

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Ga als volgt te werk voordat u verdergaat om te controleren of het aanvraagpad beschikbaar is:

   - Voer in het zoekfilter boven aan de kolom **[!UICONTROL Request Path]** de URL-sleutel in van de pagina die omgeleid moet worden en klik op **[!UICONTROL Search]** .

   - Als er meerdere omleidingsrecords voor de pagina zijn, zoekt u de record die overeenkomt met de toepasselijke winkelweergave en opent u deze in de bewerkingsmodus.

   - Klik in de rechterbovenhoek op **[!UICONTROL Delete]** . Klik op **[!UICONTROL OK]** om te bevestigen wanneer hierom wordt gevraagd.

1. Klik op **[!UICONTROL Add URL Rewrite]** wanneer u terugkeert naar de pagina URL herschrijft.

1. Stel **[!UICONTROL Create URL Rewrite]** in op `Custom` .

   ![ URL herschrijft - douane ](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. Voer onder Informatie voor herschrijven van URL de volgende handelingen uit:

   - Als u meerdere winkelweergaven hebt, selecteert u de **[!UICONTROL Store]** waar het herschrijven van toepassing is.

   - Voer bij **[!UICONTROL Request Path]** de URL-sleutel en het pad (indien van toepassing) in van het product, de categorie of de CMS-pagina die omgeleid moet worden.

     >[!NOTE]
     >
     >Het aanvraagpad moet uniek zijn voor de opgegeven opslag. Als er al een omleiding is die het zelfde verzoekweg gebruikt, ontvangt u een fout wanneer u probeert om omleiding te bewaren. De vorige omleiding moet worden verwijderd voordat u een omleiding kunt maken.

   - Voer bij **[!UICONTROL Target Path]** de URL van het doel in. Als het doel zich op een andere website bevindt, voert u de volledig gekwalificeerde URL in.

   - Plaats **opnieuw richt** aan één van het volgende:

      - `Temporary (302)`
      - `Permanent (301)`

   - Voer ter referentie een korte beschrijving in van het herschrijven.

1. Lees het volgende voordat u de omleiding opslaat:

   - [!UICONTROL Request Path] bevat de sleutel URL of de weg van originele _opnieuw richt van_ pagina.
   - [!UICONTROL Target Path] bevat URL van _opnieuw richt aan_ pagina.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   Het nieuwe herschrijven verschijnt in het net bij de bovenkant van de lijst.

## Stap 3. Het resultaat testen

1. Ga naar de homepage van je winkel.

1. Voer een van de volgende handelingen uit:

   - Navigeer aan origineel _opnieuw richt van_ pagina.
   - In de adresbar van browser, ga de naam van originele _omleiding van_ pagina onmiddellijk na opslag URL in en druk **gaat** binnen.

   De nieuwe doelpagina wordt weergegeven in plaats van de oorspronkelijke paginaaanvraag.

## Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Geeft het type herschrijven aan. Het type kan niet worden gewijzigd nadat het herschrijven is gemaakt. Opties: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | De pagina die moet worden omgeleid. Het aanvraagpad moet uniek zijn en kan niet worden gebruikt door een andere omleiding. Als u een foutbericht ontvangt dat het aanvraagpad bestaat, verwijdert u de bestaande omleiding en probeert u het opnieuw. |
| [!UICONTROL Target Path] | Het interne pad dat door het systeem wordt gebruikt om naar het doel te wijzen. Het doelpad wordt grijs weergegeven en kan niet worden bewerkt. |
| [!UICONTROL Redirect] | Bepaalt het type omleiding. Opties: <br/>**Nr** - Geen wordt omleiding gespecificeerd. <br/>**[!UICONTROL Temporary (302)]**- Geeft aan zoekprogramma&#39;s aan dat het herschrijven een beperkte tijd duurt. Zoekprogramma&#39;s behouden de paginarangtelgegevens meestal niet voor tijdelijke herschrijvingen.<br/>**[!UICONTROL Permanent (301)]** - Geeft aan zoekprogramma&#39;s aan dat het herschrijven permanent is. Zoekprogramma&#39;s behouden doorgaans de rangtelgegevens van de pagina voor permanente herschrijvingen. |
| [!UICONTROL Description] | Beschrijft het doel van herschrijven voor interne verwijzing. |

{style="table-layout:auto"}
