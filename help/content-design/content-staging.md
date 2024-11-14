---
title: Inhoud stapelen
description: Met Inhoud stapelen kan uw bedrijfsteam eenvoudig een groot aantal inhoudsupdates voor uw winkel maken, voorvertonen en plannen, rechtstreeks vanuit de beheerder.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Inhoud stapelen

{{ee-feature}}

Inhoud het opvoeren geeft uw bedrijfsteam de capaciteit om, een brede waaier van inhoudsupdates voor uw opslag direct van _te creëren voor te vertonen en te plannen Admin_. Bijvoorbeeld, eerder dan het denken in termen van een statische pagina, overweeg een pagina om een inzameling van verschillende elementen te zijn die _kunnen worden aangezet_ of _weg_ gebaseerd op een programma. U kunt inhoud die opneemt gebruiken om een pagina te maken die het hele jaar volgens een schema automatisch verandert.

De termijn _campagne_ verwijst naar het verslag van een geplande verandering, of een inzameling van veranderingen die van het het Opvoeren Dashboard worden beheerd. De wijzigingen kunnen worden weergegeven op een kalender of tijdlijn. De termijnen _geplande verandering_ en _geplande update_ zijn onderling verwisselbaar en verwijzen naar één enkele verandering.

Wanneer u een inhoudswijziging voor een specifieke tijdsperiode plant, keert de inhoud terug naar de vorige versie wanneer de geplande wijziging verloopt. U kunt meerdere versies maken van dezelfde basislijninhoud die u kunt gebruiken voor toekomstige updates. U kunt ook de tijdlijn doorlopen om vorige versies van de inhoud weer te geven. Als u een conceptversie wilt opslaan, wijst u gewoon een datum op de tijdlijn toe die zo ver in de toekomst ligt dat deze nooit in productie wordt genomen.

## Objecten en campagnes voor het opvoeren van inhoud

Velden met betrekking tot de begindatum en einddatum zijn uit Adobe Commerce verwijderd en kunnen niet rechtstreeks worden gewijzigd op de winkelprijregel, catalogusprijsregel, product, categorie en CMS-pagina. U moet een geplande update maken voor deze activeringen.

Alle geplande updates worden opeenvolgend toegepast, wat betekent dat elke entiteit slechts één geplande update tegelijk kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit geen verschillende geplande update voor verschillende opslagmeningen tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

Wanneer een nieuwe geplande update wordt gemaakt voor een van de volgende objecten, wordt een corresponderende campagne gemaakt als tijdelijke aanduiding en wordt het vak _[!UICONTROL Scheduled Changes]_boven aan de pagina weergegeven. De plaatsaanduidingscampagne heeft een begindatum, maar geen einddatum. U kunt updates van de inhoud plannen als deel van een campagne, en dan voorproef en de veranderingen door datum, tijd, of opslagmening delen. Nadat een nieuwe campagne voor één voorwerp wordt gecreeerd, kunt u het als geplande update voor andere voorwerpen toewijzen.

- [Producten](../catalog/product-scheduled-changes.md)
- [Categorieën](../catalog/category-scheduled-changes.md)
- [Catalogusprijsregels](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Lijnen met winkelprijzen](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS-pagina&#39;s](pages-workspace.md#scheduled-changes)
- [CMS-blokken](blocks.md)

## Workflow voor het opslaan van inhoud

1. **creeer de basislijninhoud**

   De basislijn is de inhoud van een element zonder campagne en bevat alles onder de sectie _[!UICONTROL Scheduled Changes]_boven aan de pagina. De basislijninhoud wordt altijd gebruikt, tenzij er een actieve campagne is met veranderingen die voor die plaats op de chronologie worden gepland.

1. **creeer de eerste campagne**

   Maak waar nodig uw eerste campagne met de begin- en einddatum. Laat de einddatum leeg om de campagne open te maken. Wanneer de eerste campagne is beëindigd, wordt de oorspronkelijke basislijninhoud hersteld.

   De Datum van het Begin van de campagne en de Datum van het Eind moeten worden bepaald door de **_gebrek_** tijdzone Admin te gebruiken, die van de lokale tijdzone van elke website wordt omgezet. Bekijk een voorbeeld van meerdere websites in verschillende tijdzones, maar u wilt een campagne starten op basis van een Amerikaanse tijdzone. In dit geval moet u een afzonderlijke update voor elke lokale tijdzone plannen en **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** instellen in geconverteerde tijdzone van elke lokale website naar de standaardtijdzone van Admin.

1. **voeg een tweede campagne** toe

   Maak de tweede campagne met de begin- en einddatum naar wens. De tweede campagne kan worden toegewezen aan een heel andere periode. Wanneer u meerdere campagnes voor hetzelfde middel maakt, kunnen de campagnes elkaar niet overlappen. U kunt zoveel campagnes maken als u nodig hebt.

   Meerdere elementen kunnen worden toegewezen aan een bestaande campagne die nog niet is gestart. Zo kunnen twee verschillende productprijzen in het kader van dezelfde campagne worden bijgewerkt met een toekomstige begindatum.

   >[!NOTE]
   >
   >Als een campagne met meer dan één entiteit verbonden is, kan de campagne slechts van het [ Inhoud Staging Dashboard ](content-staging-dashboard.md) worden uitgegeven.

1. **herstel de basislijninhoud**

   Als alle campagnes einddata hebben, wordt de basislijninhoud hersteld wanneer alle actieve campagnes beëindigen.

   >[!NOTE]
   >
   >Als een actieve campagne in eerste instantie zonder einddatum wordt gemaakt, kan de campagne later niet worden bewerkt om een einddatum op te nemen. In dat geval moet een dubbele campagne worden gemaakt en moet de gewenste einddatum worden ingevoerd.

>[!NOTE]
>
>Terwijl een testupdate actief is voor een entiteit, bewerkt de entiteit de huidige actieve testupdate. Dit heeft geen invloed op de basislijninhoud, die wordt hersteld wanneer de gefaseerde update eindigt.

## [!UICONTROL Content Staging] dashboard

Het [!UICONTROL Content Staging] [ dashboard ](content-staging-dashboard.md) verstrekt zicht in alle geplande plaatsveranderingen en updates. Elke dag, elk datumbereik of elke tijdsperiode van een campagne kan vooraf worden bekeken en met anderen worden gedeeld.

![ het Opvoeren dashboard ](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demo voor inhoudstaging

Bekijk de volgende video voor meer informatie over het staging van inhoud:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12&learn=on)

## Bronnen voor probleemoplossing

Raadpleeg de volgende [!DNL Commerce] artikelen in de Support Knowledge Base voor hulp bij het oplossen van problemen met betrekking tot het staging van inhoud:

- [ Fout 404 op alle pagina&#39;s toe te schrijven aan inhoud die kwestie opneemt ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [ Geplande die updates van het Staging van de Inhoud niet met het oude Fastly geheime voorgeheugen worden getoond ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [ Kan ik de updates van het Staging van de Inhoud voor prijzen in een gedeelde catalogus plannen?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
