---
title: '[!DNL AR Viewer] voor Adobe Commerce'
description: Leer hoe  [!DNL AR Viewer]  uw instantie van Adobe Commerce kon bevoordelen en hoe te met succes aan boord te gaan en de uitbreiding te plaatsen.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] voor Adobe Commerce

De Augmented reality (AR) beschrijft gebruikerservaringen die 2D of 3D elementen aan het levende beeld van de camera van een apparaat op een bepaalde manier toevoegen die die elementen schijnen om de echte wereld te bewonen.

Met de extensie [!DNL AR Viewer] for Adobe Commerce beschikt u over een naadloze ervaring die is ontworpen om gerenderde 3D-afbeeldingen voor de gebruiker weer te geven.

De informatie in deze handleiding biedt een overzicht van de instapervaring voor de [!DNL AR Viewer] -gebruiker in Adobe Commerce en van de voordelen die [!DNL AR Viewer] biedt voor de gebruiker. Ook bevat deze handleiding tips en trucs voor het volgen van deze reis.

Ontwikkeld door Pixar, [ Universele Beschrijving van de Scène (USD) ](https://www.pixar.com/usd) {target=_blank} is de eerste open-bronsoftware die robuust en scalable 3D scènes kan ruilen die uit vele verschillende activa, bronnen, en animaties kunnen bestaan, terwijl het bevorderen van hoogst samenwerkingswerkschema&#39;s. Deze USD wordt gebruikt in `.USDZ` -bestanden. Dit `.USDZ` -bestand levert AIR- en 3D-inhoud aan de apparaten van de gebruiker.

>[!NOTE]
>
> [!DNL AR Viewer] ondersteunt alleen `.USDZ` -bestanden.

## [!DNL AR Viewer] vereisten

[!DNL AR Viewer] is zowel compatibel met [!DNL Magento Open Source] als met Adobe Commerce. Zie {het Beleid van de Levenscyclus 0} ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html) {target=_blank} voor meer informatie over gesteunde versies.[

Zie [ installeren de  [!DNL AR Viewer]  uitbreiding ](../catalog/ar-viewer-setup.md) voor meer informatie.

Als u [!DNL AR Viewer] wilt gebruiken, moet u het volgende beschikbaar hebben voor uw instantie:

* PHP 8.1.0
* Adobe Commerce versie 2.4.4 en hoger
* Magento Open Source (CE) versie 2.4.x

## Compatibiliteitsbeperkingen

[!DNL AR Viewer] bestaande compatibiliteitsbeperkingen:

* `.USDZ` alleen: deze functie ondersteunt alleen `.USDZ` -bestanden.
* `qr-code`: vereist `endroid/qr-code` versie 4.5.
* `Catalog module`: vereist `magento/module-catalog` versie 104.0.0.
