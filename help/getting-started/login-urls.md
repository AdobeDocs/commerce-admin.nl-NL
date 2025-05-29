---
title: Aanmeldingsgegevens en URL's
description: Meer informatie over de Commerce-URL's en accountgegevens die worden gebruikt om toegang te krijgen tot uw beheerder en winkelcentrum.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Aanmeldingsgegevens en URL&#39;s

Voordat u verdergaat met instellen en configureren, moet u controleren of u beschikt over de benodigde informatie voor toegang tot de beheerder van uw winkel en uw Commerce-account.

## Storefront-URL

Het adres voor uw [ storefront ](storefront.md) is gewoonlijk het domein dat aan uw IP adres wordt toegewezen. Sommige opslagruimten zijn geïnstalleerd bij de wortel, of hoogste folder. Andere bestanden worden geïnstalleerd in een map onder de hoofdmap. De opslag zou binnen subdomain kunnen verblijven die met een primair domein wordt geassocieerd. De URL voor uw winkel kan er als volgt uitzien:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx` s

Als u nog geen domein hebt, omvat uw opslag URL een reeks van vier aantallen, elk die door een periode in _gestippelde vierhoekige_ aantekening worden gescheiden.

## URL van beheerder

Het adres voor uw opslag [ Admin ](admin.md) wordt opstelling tijdens de installatie. Het standaardadres is hetzelfde als in uw winkel, maar met `/admin` aan het einde. Hoewel de voorbeelden in deze handleiding de standaardmap gebruiken, is het verstandig om uw beheerder uit te voeren vanaf een locatie die uniek is voor uw winkel.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

Uw [ rekening van Commerce ](commerce-account-create.md) verleent toegang tot informatie over uw producten en de diensten, rekeningsmontages, het factureren geschiedenis, en steunmiddelen. Ga naar de Commerce-hoofdsite en klik op **[!UICONTROL My Account]** in de rechterbovenhoek om uw account te openen.

## Klantenaccount

Terwijl u uw manier rond de opslag leert, zorg ervoor aan opstelling een test [ klantenrekening ](../customers/account-dashboard.md), zodat kunt u de opslag en het controleproces vanuit het perspectief van de klant ervaren.

## Voorbeeldgegevens

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

Adobe biedt een set voorbeeldgegevens die een voorbeeldwinkel bevat met meer dan 250 producten (ongeveer 200 daarvan zijn configureerbare producten), categorieën, promotieprijsregels, CMS-pagina&#39;s, banners enzovoort. De gegevens van de steekproef gebruiken het _thema 0&rbrace; Luma op de storefront._ [ Installing this sample data ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) is facultatief, maar kan voor het testen en het ontwikkelen van aanpassingen voor uw eCommerce zaken nuttig zijn.
