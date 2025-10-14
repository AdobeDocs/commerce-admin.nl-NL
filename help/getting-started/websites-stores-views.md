---
title: Reeks-, opslag- en weergavebereik
description: Leer over de hiërarchie van websites, winkels, en opslagmeningen die u kunt gebruiken om winkelervaringen voor uw klanten te leveren.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Reeks-, opslag- en weergavebereik

Elke installatie van Adobe Commerce en van de Magento Open Source heeft a [&#x200B; hiërarchie &#x200B;](../stores-purchase/stores.md) van websites, opslag, en opslagmeningen. Het termijn _werkingsgebied_ bepaalt waar in de hiërarchie een gegevensbestandentiteit - zoals een product, een attribuut, of een categorie - inhoudselement, of configuratie het plaatsen van toepassing is. Websites, winkels en winkelweergaven hebben een-op-een-relatie tussen bovenliggende en onderliggende sites. Eén installatie kan meerdere websites bevatten en elke website kan meerdere winkels en winkelweergaven hebben.

>[!NOTE]
>
>Meer leren, zie [&#x200B; Veelvoudige websites of opslag &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=nl-NL) in de [!DNL Commerce] ontwikkelaarsdocumentatie.

## Websites

De installaties beginnen met één enkele [&#x200B; website &#x200B;](../stores-purchase/stores.md#add-websites), die _Belangrijkste Website_ door gebrek wordt genoemd. U kunt ook meerdere websites instellen voor één installatie, elk met een eigen IP-adres en domein.

## Winkels

Één enkele website kan veelvoudige [&#x200B; opslag &#x200B;](../stores-purchase/stores.md#add-stores) hebben, elk met zijn eigen hoofdmenu. De winkels delen de productcatalogus, maar kunnen een verschillende selectie van producten en ontwerp hebben. Alle winkels onder dezelfde website delen de beheerder en het uitchecken.

## Winkelweergaven

Elke opslag die aan klanten beschikbaar is wordt voorgesteld volgens een specifieke _[mening](../stores-purchase/store-views.md)_. In eerste instantie heeft een winkel één standaardweergave. U kunt extra weergaven voor de winkel toevoegen om verschillende talen of voor andere doeleinden te ondersteunen. Klanten kunnen de taalkiezer in de koptekst gebruiken om de winkelweergave te wijzigen.

Houd rekening met het volgende wanneer u werkt met websites, winkels en winkelweergaven:

- Commerce-exemplaren hebben een trapsgewijs model: global → website → store → store view.
- Elke website heeft minimaal één standaardopslagweergave.
- Elke winkelweergave kan een andere basis-URL hebben.
- De primaire functie van een website is de configuratie van functies op hoofdniveau.
- De primaire functie van een opslag is de configuratie van de wortelcategorie.
- De primaire functie van een winkelweergave is de configuratie van vertaalgegevens en valutasymbolen.

## Bereik-instellingen

Als uw installatie van Adobe Commerce of van de Magento Open Source een hiërarchie van websites, opslag, of meningen heeft, kunt u de context, of _werkingsgebied_ van een configuratie plaatsen. De context van vele gegevensbestandentiteiten kan ook een specifiek werkingsgebied worden toegewezen om te bepalen hoe het in de opslaghiërarchie wordt gebruikt. Meer leren, zie {het werkingsgebied van het 0} Product [&#128279;](../catalog/introduction.md#product-scope) en [&#x200B; het werkingsgebied van de Prijs &#x200B;](../catalog/catalog-price-scope.md).

Sommige configuratiemontages zoals postcode, hebben een globaal werkingsgebied omdat de zelfde waarde door het systeem wordt gebruikt. Het [&#x200B; website &#x200B;](../stores-purchase/stores.md#add-websites) werkingsgebied is op om het even welke opslag onder dat niveau in de hiërarchie, met inbegrip van alle opslag en hun meningen van toepassing. Om het even welk punt met het werkingsgebied van [&#x200B; opslagmening &#x200B;](../stores-purchase/store-views.md) kan verschillend voor elke opslagmening worden geplaatst, die typisch wordt gebruikt om veelvoudige talen te steunen. Om de standaardwaarden van configuratiemontages met voeten te treden, zie [&#x200B; Plaats het werkingsgebied &#x200B;](../configuration-reference/scope-change.md#set-the-scope).

Tenzij de opslag op [&#x200B; enige opslagwijze &#x200B;](#single-store-mode) loopt, verschijnt het werkingsgebied van elke configuratie die in kleine tekst onder het gebiedsetiket plaatst. Als uw installatie veelvoudige websites, opslag, of meningen omvat, kies de [&#x200B; opslagmening &#x200B;](../stores-purchase/store-views.md) waar de montages van toepassing zijn alvorens om het even welke veranderingen aan te brengen.

![&#x200B; Hiërarchie van websites, opslag, en opslagmeningen &#x200B;](./assets/scope-multisite.svg){width="550"}

| Toepassingsgebied | Beschrijving |
|--- |--- |
| [!UICONTROL Global] | Instellingen en bronnen voor het hele systeem die beschikbaar zijn in de gehele installatie. |
| [!UICONTROL Website] | Instellingen en bronnen die beperkt zijn tot de huidige website. Elke website heeft een standaardopslag. |
| [!UICONTROL Store] | Instellingen en bronnen die beperkt zijn tot de huidige winkel. Elke winkel heeft een standaardhoofdcategorie (hoofdmenu) en een standaardwinkelweergave. |
| [!UICONTROL Store View] | Instelling en bronnen die beperkt zijn tot de huidige winkelweergave. |

{style="table-layout:auto"}

## Modus Eén winkel

Als uw Commerce-installatie slechts één winkel- en winkelweergave heeft, kunt u de weergave vereenvoudigen door alle opties voor de winkelweergave en bereikindicatoren uit te schakelen. De enige opslagwijze wordt met voeten getreden als u [&#x200B; meer opslagmeningen &#x200B;](../stores-purchase/store-views.md) later toevoegt.

![&#x200B; Reikwijdte - één enkele mening &#x200B;](./assets/scope-single-view.svg){width="550"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Blader onder **[!UICONTROL General]** omlaag naar de onderkant van de pagina en vouw de sectie **[!UICONTROL Single-Store Mode]** uit.

1. Stel **[!UICONTROL Enable Single-Store Mode]** in op `Yes` .

   ![&#x200B; Algemene configuratie - laat Enige-Opslagwijze &#x200B;](./assets/general-single-store-mode.png){width="400"} toe

1. Klik op **[!UICONTROL Save Config]**.

1. Ga als volgt te werk wanneer u wordt gevraagd de cache te vernieuwen:

   - Klik op de koppeling **[!UICONTROL Cache Management]** in het systeembericht boven aan de pagina.

     ![&#x200B; bericht van het Systeem - geheim voorgeheugenbeheer &#x200B;](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Schakel het selectievakje **[!UICONTROL Page Cache]** in.

   - Wanneer **[!UICONTROL Actions]** is ingesteld op `Refresh` , klikt u op **[!UICONTROL Submit]**
