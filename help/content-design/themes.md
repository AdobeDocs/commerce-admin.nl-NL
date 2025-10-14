---
title: Thema's
description: Leer over  [!DNL Commerce]  thema's, die lay-outdossiers, malplaatjedossiers, vertaaldossiers, en huiden omvatten die de blik en het gevoel van uw opslag bepalen.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Thema&#39;s

Een thema is een verzameling bestanden die de visuele presentatie van uw winkel bepaalt. Wanneer u eerst [!DNL Commerce] installeert, zijn de ontwerpelementen van de opslag gebaseerd op het _Standaard_ thema. Naast het aanvankelijke standaardthema dat met uw [!DNL Commerce] installatie komt, is er een grote verscheidenheid van beschikbare thema&#39;s die u _kunt gebruiken zoals_ is of voor uw behoeften wijzigt.

Met een responsief thema past u de paginalay-out aan de weergavepoort van het apparaat aan. Het steekproef _thema van de Luma_ heeft een flexibele, ontvankelijke lay-out die van de Desktop, de tablet, of het mobiele apparaat kan worden bekeken.

Tot de thema&#39;s van [!DNL Commerce] behoren lay-outbestanden, sjabloonbestanden, vertaalbestanden en skins. Een skin is een verzameling ondersteunende CSS-, afbeeldings- en JavaScript-bestanden die samen de visuele presentatie en interacties maken die uw klanten ervaren wanneer ze uw winkel bezoeken. Thema&#39;s en skins kunnen worden gewijzigd en aangepast door een ontwikkelaar of ontwerper die het Commerce-themaontwerp begrijpt en toegang heeft tot uw server. Meer leren, zie de [_Voorste Gids van de Ontwikkelaar_ &#x200B;](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![&#x200B; thema van de Luma &#x200B;](./assets/design-responsive.png){width="600" zoomable="yes"}

## Het standaardthema

Met het responsieve thema `Magento Blank` wordt de weergave van uw winkel voor verschillende apparaten weergegeven en worden de beste werkwijzen voor computers, tabellen en mobiele apparaten opgenomen. Sommige thema&#39;s zijn alleen ontworpen voor gebruik met specifieke apparaten. Wanneer [!DNL Commerce] een specifieke browser identiteitskaart, of gebruikersagent ontdekt, gebruikt het het thema dat voor specifieke browser wordt gevormd. De zoektekenreeks kan ook PCRE (Perl-Compatible Regular Expressions) bevatten.

![&#x200B; Thema&#39;s &#x200B;](./assets/themes.png){width="700" zoomable="yes"}

### Het themaraster filteren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Klik op **[!UICONTROL Filters]**.

1. Voer een ID-bereik, themanaam (of titel), mappad of bovenliggend thema in.

1. Klik op **[!UICONTROL Apply Filters]** om de lijst met onderwerpen bij te werken.

## Huidige thema-instellingen weergeven

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Zoek in de lijst met geïnstalleerde thema&#39;s het thema dat u wilt onderzoeken en klik op de rij om de instellingen weer te geven.

1. Klik op **[!UICONTROL Theme Preview Image]** om een voorbeeldpagina weer te geven.

![&#x200B; het thema van de Voorproef &#x200B;](./assets/theme-settings.png){width="600" zoomable="yes"}

## Een standaardthema toepassen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Stel onder _[!UICONTROL Default Theme]_&#x200B;**[!UICONTROL Applied Theme]**&#x200B;in op de waarde die u voor de huidige weergave wilt gebruiken.

   ![&#x200B; Toegepast Thema &#x200B;](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.

## Een gebruikersagentregel toevoegen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Klik onder _[!UICONTROL Design Rule]_&#x200B;op **[!UICONTROL Add New User Agent Rule]**.

   ![&#x200B; Regel van het Ontwerp &#x200B;](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Voer bij **[!UICONTROL Search String]** de browser-id voor het specifieke apparaat in.

   Zoektekenreeksen komen overeen in de volgorde waarin ze worden ingevoerd. Voer bijvoorbeeld voor Firefox het volgende in:

   `/^mozilla/i`

1. Herhaal het proces om extra apparaten in te voeren.

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.
