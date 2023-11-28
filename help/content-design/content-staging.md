---
title: Inhoud stapelen
description: Met Inhoud stapelen kan uw bedrijfsteam eenvoudig een groot aantal inhoudsupdates voor uw winkel maken, voorvertonen en plannen, rechtstreeks vanuit de beheerder.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Inhoud stapelen

{{ee-feature}}

Met inhoudstaging kan uw bedrijfsteam eenvoudig een groot aantal inhoudsupdates voor uw winkel maken, bekijken en plannen, rechtstreeks vanuit de _Beheerder_. Neem bijvoorbeeld, in plaats van te denken aan een statische pagina, een pagina als een verzameling verschillende elementen die kunnen worden omgedraaid _op_ of _uit_ op basis van een schema. U kunt inhoud die opneemt gebruiken om een pagina te maken die het hele jaar volgens een schema automatisch verandert.

De term _campagne_ verwijst naar het verslag van een geplande verandering, of een inzameling van veranderingen die van het het Opvoeren Dashboard worden beheerd. De wijzigingen kunnen worden weergegeven op een kalender of tijdlijn. De voorwaarden _geplande wijziging_ en _geplande update_ zijn onderling verwisselbaar en hebben betrekking op één enkele wijziging.

Wanneer u een inhoudswijziging voor een specifieke tijdsperiode plant, keert de inhoud terug naar de vorige versie wanneer de geplande wijziging verloopt. U kunt meerdere versies maken van dezelfde basislijninhoud die u kunt gebruiken voor toekomstige updates. U kunt ook de tijdlijn doorlopen om vorige versies van de inhoud weer te geven. Als u een conceptversie wilt opslaan, wijst u gewoon een datum op de tijdlijn toe die zo ver in de toekomst ligt dat deze nooit in productie wordt genomen.

## Objecten en campagnes voor het opvoeren van inhoud

Wanneer een nieuwe geplande update wordt gemaakt voor een van de volgende objecten, wordt een corresponderende campagne gemaakt als tijdelijke aanduiding en wordt de opdracht _[!UICONTROL Scheduled Changes]_wordt boven aan de pagina weergegeven. De plaatsaanduidingscampagne heeft een begindatum, maar geen einddatum. U kunt updates van de inhoud plannen als deel van een campagne, en dan voorproef en de veranderingen door datum, tijd, of opslagmening delen. Nadat een nieuwe campagne voor één voorwerp wordt gecreeerd, kunt u het als geplande update voor andere voorwerpen toewijzen.

- [Producten](../catalog/product-scheduled-changes.md)
- [Categorieën](../catalog/category-scheduled-changes.md)
- [Catalogusprijsregels](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Lijnen met winkelprijzen](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS-pagina&#39;s](pages-workspace.md#scheduled-changes)
- [CMS-blokken](blocks.md)

## Workflow voor het opslaan van inhoud

1. **De basislijninhoud maken**

   De basislijn is de inhoud van een middel zonder een campagne en omvat alles onder de _[!UICONTROL Scheduled Changes]_boven aan de pagina. De basislijninhoud wordt altijd gebruikt, tenzij er een actieve campagne is met veranderingen die voor die plaats op de chronologie worden gepland.

1. **De eerste campagne maken**

   Maak waar nodig uw eerste campagne met de begin- en einddatum. Laat de einddatum leeg om de campagne open te maken. Wanneer de eerste campagne is beëindigd, wordt de oorspronkelijke basislijninhoud hersteld.

   >[!NOTE]
   >
   >Begindatum en Einddatum van campagne moeten worden gedefinieerd met de instelling **_default_** Tijdzone voor beheerders, die wordt omgezet vanuit de lokale tijdzone van elke website. Bekijk een voorbeeld van meerdere websites in verschillende tijdzones, maar u wilt een campagne starten op basis van een Amerikaanse tijdzone. In dit geval moet u een afzonderlijke update voor elke lokale tijdzone plannen, en reeks **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** in omgezet van elke lokale tijdzone van de websitetijd in de standaardtijdzone van Admin.

1. **Een tweede campagne toevoegen**

   Maak de tweede campagne met de begin- en einddatum naar wens. De tweede campagne kan worden toegewezen aan een heel andere periode. Wanneer u meerdere campagnes voor hetzelfde middel maakt, kunnen de campagnes elkaar niet overlappen. U kunt zoveel campagnes maken als u nodig hebt.

   >[!NOTE]
   >
   >Alle geplande updates worden opeenvolgend toegepast, wat betekent dat elke entiteit slechts één geplande update tegelijk kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit geen verschillende geplande update voor verschillende opslagmeningen tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

1. **De basislijninhoud herstellen**

   Als alle campagnes einddata hebben, wordt de basislijninhoud hersteld wanneer alle actieve campagnes beëindigen.

>[!NOTE]
>
>Terwijl een testupdate actief is voor een entiteit, bewerkt de entiteit de huidige actieve testupdate. Dit heeft geen invloed op de basislijninhoud, die wordt hersteld wanneer de gefaseerde update eindigt.

## [!UICONTROL Content Staging] dashboard

De [!UICONTROL Content Staging] [dashboard](content-staging-dashboard.md) biedt zichtbaarheid in alle geplande wijzigingen en updates voor de site. Elke dag, elk datumbereik of elke tijdsperiode van een campagne kan vooraf worden bekeken en met anderen worden gedeeld.

![Staging-dashboard](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demo voor inhoudstaging

Bekijk de volgende video voor meer informatie over het staging van inhoud:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## Bronnen voor probleemoplossing

Raadpleeg de volgende bronnen voor hulp bij het oplossen van problemen met inhoud-staging [!DNL Commerce] Kennisbank-artikelen ondersteunen:

- [Fout 404 op alle pagina&#39;s vanwege probleem met inhoudstaging](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [Geplande updates voor het bijhouden van inhoud worden niet weergegeven met een verouderde snelcache](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [Kan ik updates voor het opslaan van inhoud plannen voor prijzen in een gedeelde catalogus?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
