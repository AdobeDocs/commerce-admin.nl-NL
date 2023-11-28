---
title: '[!DNL AR Viewer] voor Adobe Commerce setup'
description: Meer informatie over het beheren van 3D-modelelementen met de [!DNL AR Viewer] extensie voor je productaanbiedingen.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 3D-modellen van producten beheren met de [!DNL AR Viewer] voor Adobe Commerce

Voor elk product kunt u een `.USDZ` bestand waarmee AIR- en 3D-modellen kunnen worden gebruikt in de lijst met producten.

De [!DNL AR Viewer] alleen ondersteuning `.USDZ` bestanden.

## De extensie installeren

[!DNL AR Viewer] is geïnstalleerd als een extensie van [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Zie de [_Installatiehandleiding_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) voor meer informatie over het installatieproces van de extensie.

Na de [!DNL AR Viewer] Als de extensie is geïnstalleerd en geconfigureerd, kunnen Admin-gebruikers productlijsten zodanig instellen, aanpassen en beheren dat deze 3D-modellen bevatten.

## Een 3D-model toevoegen

1. Open het product in de bewerkingsmodus.

1. Als u met een specifieke winkelweergave wilt werken, stelt u de optie **[!UICONTROL Store View]** kiest u voor de toepasselijke weergave.

   >[!NOTE]
   >
   >3D-modellen voor nieuwe producten zijn _altijd_ geüpload en zichtbaar in _alles_ archiefweergaven, zelfs als de `All Store Views` bereik wordt niet gebruikt voor uploaden. <br/><br/>Als u 3D-modellen van een product wilt verbergen in een specifieke winkelweergave, moet u overschakelen naar die winkelweergave, de optie **[!UICONTROL Hide from Product Page]** selectievakje voor het 3D-model en klik op **[!UICONTROL Save]**.

1. Omlaag schuiven en de _[!UICONTROL Product 3D Model]_sectie.

   ![Pop-up Menu](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Het 3D-model toevoegen (`.USDZ` bestand) van het product.

1. Klik op **[!UICONTROL Save]**.

### Een 3D-model verwijderen

Een 3D-model verwijderen uit de productdetails:

1. Klik op **[!UICONTROL Delete]**.

1. Klik op **[!UICONTROL Save]**.

## 3D-modellen van producten weergeven

Wanneer de productgegevens worden bijgewerkt met het 3D-model:

1. De [!DNL AR Viewer] genereert een QR-code in de productbeschrijving die het AR-bestand codeert.

1. Een klant kan deze QR-code op de productpagina zien.

1. Wanneer klanten de QR-code scannen met hun mobiele apparaten, wordt een AIR-ervaring weergegeven op het mobiele apparaat.

>[!NOTE]
>
> Raadpleeg voor een aantal demonstratievideo&#39;s van gebruikers die een 3D-model aan een product toevoegen de [AR Viewer voor Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) pagina in _Commerciële video&#39;s en Tutorials_.
