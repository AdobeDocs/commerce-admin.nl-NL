---
title: '[!DNL AR Viewer] voor Adobe Commerce'
description: Meer informatie over [!DNL AR Viewer] kan uw Adobe Commerce-exemplaar ten goede komen en de extensie met succes aan boord installeren en instellen.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] voor Adobe Commerce

De Augmented reality (AR) beschrijft gebruikerservaringen die 2D of 3D elementen aan het levende beeld van de camera van een apparaat op een bepaalde manier toevoegen die die elementen schijnen om de echte wereld te bewonen.

De [!DNL AR Viewer] voor Adobe Commerce-extensie maakt een naadloze ervaring mogelijk die is ontworpen om gerenderde 3D-afbeeldingen voor de gebruiker weer te geven.

De informatie in deze handleiding geeft een overzicht van de ervaring bij het aan boord nemen van de [!DNL AR Viewer] in Adobe Commerce en hoe [!DNL AR Viewer] de gebruiker ten goede komt, en beste praktijken om die reis te volgen.

Ontwikkeld door Pixar, [Universele beschrijving van scène (USD)](https://www.pixar.com/usd){target=_blank} is de eerste opensource-software die op robuuste en schaalbare wijze 3D-scènes kan uitwisselen die uit vele verschillende middelen, bronnen en animaties kunnen bestaan, en die tegelijkertijd zeer samenwerkingsworkflows stimuleert. Deze USD wordt gebruikt binnen `.USDZ` bestanden. Dit `.USDZ` AIR- en 3D-inhoud wordt geleverd aan de apparaten van de gebruiker.

>[!NOTE]
>
> De [!DNL AR Viewer] Alleen ondersteuning `.USDZ` bestanden.

## [!DNL AR Viewer] vereisten

De [!DNL AR Viewer] is compatibel met beide [!DNL Magento Open Source] en Adobe Commerce. Zie [Levenscyclusbeleid](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} voor meer informatie over ondersteunde versies.

Zie [Installeer de [!DNL AR Viewer] extension](../catalog/ar-viewer-setup.md) voor meer informatie .

Voor gebruik [!DNL AR Viewer], moet het volgende beschikbaar zijn voor uw instantie:

* PHP 8.1.0
* Adobe Commerce versie 2.4.4 en hoger
* Magento Open Source (CE) versie 2.4.x

## Compatibiliteitsbeperkingen

[!DNL AR Viewer] bestaande compatibiliteitsbeperkingen:

* `.USDZ` alleen: deze functie wordt alleen ondersteund `.USDZ` bestanden.
* `qr-code`: Vereist `endroid/qr-code` versie 4.5.
* `Catalog module`: Vereist `magento/module-catalog` versie 104.0.0.
