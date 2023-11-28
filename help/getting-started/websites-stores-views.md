---
title: Reeks-, opslag- en weergavebereik
description: Leer over de hiërarchie van websites, winkels, en opslagmeningen die u kunt gebruiken om winkelervaringen voor uw klanten te leveren.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Reeks-, opslag- en weergavebereik

Elke Adobe Commerce- en Magento Open Source-installatie heeft een [hiërarchie](../stores-purchase/stores.md) van websites, winkels en winkelweergaven. De term _bereik_ bepaalt waar in de hiërarchie een gegevensbestandentiteit — zoals een product, een attribuut, of een categorie — inhoudselement, of configuratie het plaatsen van toepassing is. Websites, winkels en winkelweergaven hebben een-op-een-relatie tussen bovenliggende en onderliggende sites. Eén installatie kan meerdere websites bevatten en elke website kan meerdere winkels en winkelweergaven hebben.

>[!NOTE]
>
>Zie voor meer informatie [Meerdere websites of winkels](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) in de [!DNL Commerce] ontwikkelaarsdocumentatie.

## Websites

Installaties beginnen met één installatie [website](../stores-purchase/stores.md#add-websites), die _Hoofdwebsite_ standaard. U kunt ook meerdere websites instellen voor één installatie, elk met een eigen IP-adres en domein.

## Winkels

Eén website kan meerdere [winkelen](../stores-purchase/stores.md#add-stores), elk met een eigen hoofdmenu. De winkels delen de productcatalogus, maar kunnen een verschillende selectie van producten en ontwerp hebben. Alle winkels onder dezelfde website delen de beheerder en het uitchecken.

## Winkelweergaven

Elke winkel die voor klanten beschikbaar is, wordt gepresenteerd volgens een specifieke _[weergave](../stores-purchase/store-views.md)_. In eerste instantie heeft een winkel één standaardweergave. U kunt extra weergaven voor de winkel toevoegen om verschillende talen of voor andere doeleinden te ondersteunen. Klanten kunnen de taalkiezer in de koptekst gebruiken om de winkelweergave te wijzigen.

Houd rekening met het volgende wanneer u werkt met websites, winkels en winkelweergaven:

- Commerciële instanties hebben een trapsgewijs model: global → website → store → store view.
- Elke website heeft minimaal één standaardopslagweergave.
- Elke winkelweergave kan een andere basis-URL hebben.
- De primaire functie van een website is de configuratie van functies op hoofdniveau.
- De primaire functie van een opslag is de configuratie van de wortelcategorie.
- De primaire functie van een winkelweergave is de configuratie van vertaalgegevens en valutasymbolen.

## Bereik-instellingen

Als uw Adobe Commerce- of Magento Open Source-installatie een hiërarchie heeft van websites, winkels of weergaven, kunt u de context instellen, of _bereik_ van een configuratie-instelling. De context van vele gegevensbestandentiteiten kan ook een specifiek werkingsgebied worden toegewezen om te bepalen hoe het in de opslaghiërarchie wordt gebruikt. Zie voor meer informatie [Productbereik](../catalog/introduction.md#product-scope) en [Prijsbereik](../catalog/catalog-price-scope.md).

Sommige configuratiemontages zoals postcode, hebben een globaal werkingsgebied omdat de zelfde waarde door het systeem wordt gebruikt. De [website](../stores-purchase/stores.md#add-websites) het toepassingsgebied is van toepassing op alle winkels onder dat niveau in de hiërarchie , met inbegrip van alle winkels en hun weergaven . Elk item met het toepassingsgebied van [winkelweergave](../stores-purchase/store-views.md) kan voor elke archiefweergave anders worden ingesteld. Deze wordt doorgaans gebruikt om meerdere talen te ondersteunen. Als u de standaardwaarden van configuratie-instellingen wilt overschrijven, raadpleegt u [Bereik instellen](../configuration-reference/scope-change.md#set-the-scope).

Tenzij de opslag wordt uitgevoerd in [Single Store-modus](#single-store-mode), wordt het bereik van elke configuratie-instelling weergegeven in kleine tekst onder het veldlabel. Kies de optie [winkelweergave](../stores-purchase/store-views.md) waar de instellingen van toepassing zijn voordat er wijzigingen worden aangebracht.

![Hiërarchie van websites, winkels en winkelweergaven](./assets/scope-multisite.svg){width="550"}

| Toepassingsgebied | Beschrijving |
|--- |--- |
| [!UICONTROL Global] | Instellingen en bronnen voor het hele systeem die beschikbaar zijn in de gehele installatie. |
| [!UICONTROL Website] | Instellingen en bronnen die beperkt zijn tot de huidige website. Elke website heeft een standaardopslag. |
| [!UICONTROL Store] | Instellingen en bronnen die beperkt zijn tot de huidige winkel. Elke winkel heeft een standaardhoofdcategorie (hoofdmenu) en een standaardwinkelweergave. |
| [!UICONTROL Store View] | Instelling en bronnen die beperkt zijn tot de huidige winkelweergave. |

{style="table-layout:auto"}

## Modus Eén winkel

Als uw installatie van de Handel slechts één enkele opslag en opslagmening heeft, kunt u de vertoning vereenvoudigen door alle opties van de opslagmening en werkingsgebiedindicatoren uit te zetten. De modus Eén winkel wordt genegeerd als u [meer winkelweergaven toevoegen](../stores-purchase/store-views.md) later.

![Toepassingsgebied - één weergave](./assets/scope-single-view.svg){width="550"}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Onder **[!UICONTROL General]** schuift u omlaag naar de onderkant van de pagina en vouwt u de **[!UICONTROL Single-Store Mode]** sectie.

1. Set **[!UICONTROL Enable Single-Store Mode]** tot `Yes`.

   ![Algemene configuratie - Modus Single Store inschakelen](./assets/general-single-store-mode.png){width="400"}

1. Klik op **[!UICONTROL Save Config]**.

1. Ga als volgt te werk wanneer u wordt gevraagd de cache te vernieuwen:

   - Klik op de knop **[!UICONTROL Cache Management]** koppeling in het systeembericht boven aan de pagina.

     ![Systeembericht - cachebeheer](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Selecteer de **[!UICONTROL Page Cache]** selectievakje.

   - Met **[!UICONTROL Actions]** instellen op `Refresh`, klikt u op **[!UICONTROL Submit]**
