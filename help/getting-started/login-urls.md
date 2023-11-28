---
title: Aanmeldingsgegevens en URL's
description: Meer informatie over de URL's van de Handel en accountgegevens die worden gebruikt om toegang te krijgen tot uw beheerder en uw winkel.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Aanmeldingsgegevens en URL&#39;s

Alvorens u met opstelling en configuratie te werk gaat, zorg ervoor dat u de informatie hebt die wordt vereist om tot Admin van uw opslag en uw rekening van de Handel toegang te hebben.

## Storefront-URL

Het adres voor uw [storefront](storefront.md) is gewoonlijk het domein dat aan uw IP adres wordt toegewezen. Sommige opslagruimten zijn geïnstalleerd bij de wortel, of hoogste folder. Andere bestanden worden geïnstalleerd in een map onder de hoofdmap. De opslag zou binnen subdomain kunnen verblijven die met een primair domein wordt geassocieerd. De URL voor uw winkel kan er als volgt uitzien:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Als u nog geen domein hebt, bevat de URL van uw winkel een reeks van vier getallen, die elk worden gescheiden door een punt in _gestippeld vierhoekig_ notatie.

## URL van beheerder

Het adres voor je winkel [Beheerder](admin.md) wordt ingesteld tijdens de installatie. Het standaardadres is hetzelfde als in je winkel, maar met `/admin` aan het einde. Hoewel de voorbeelden in deze handleiding de standaardmap gebruiken, is het verstandig om uw beheerder uit te voeren vanaf een locatie die uniek is voor uw winkel.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

Uw [Handelsrekening](commerce-account-create.md) biedt toegang tot informatie over uw producten en services, accountinstellingen, factureringsgeschiedenis en ondersteuningsbronnen. Ga voor toegang tot je account naar de belangrijkste site voor Handel en klik op **[!UICONTROL My Account]** in de rechterbovenhoek.

## Klantenaccount

Zorg dat u tijdens het leren door de winkel een test instelt [klantenaccount](../customers/account-dashboard.md), zodat u het winkel- en uitcheckproces vanuit het perspectief van de klant kunt ervaren.

## Voorbeeldgegevens

De Adobe verstrekt een reeks steekproefgegevens die een steekproefopslag met meer dan 250 producten omvat (ongeveer 200 van hen zijn configureerbare producten), categorieën, promotieprijsregels, CMS pagina&#39;s, banners, etc. Voorbeeldgegevens gebruiken de _Luminantie_ thema op de winkel. [Deze voorbeeldgegevens installeren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) is optioneel, maar kan nuttig zijn voor het testen en ontwikkelen van aanpassingen voor uw eCommerce-bedrijf.
