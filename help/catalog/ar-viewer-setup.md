---
title: '[!DNL AR Viewer] voor Adobe Commerce instellen'
description: Leer over het beheren van 3D modelactiva gebruikend de  [!DNL AR Viewer]  uitbreiding voor uw productlijsten.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# 3D-modellen van producten beheren met de [!DNL AR Viewer] voor Adobe Commerce

Voor elk product kunt u een `.USDZ` -bestand uploaden waarmee AIR- en 3D-modellen kunnen worden gebruikt in de lijst met producten.

[!DNL AR Viewer] ondersteunt alleen `.USDZ` -bestanden.

## De extensie installeren

[!DNL AR Viewer] is geïnstalleerd als uitbreiding van de [&#x200B; Marketplace van Adobe Commerce &#x200B;](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank} .

Zie de [_Gids van de Installatie_ &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=nl-NL) voor meer informatie over het proces van de uitbreidingsinstallatie.

Nadat de extensie [!DNL AR Viewer] is geïnstalleerd en geconfigureerd, kunnen Admin-gebruikers productlijsten instellen, aanpassen en beheren om 3D-modellen op te nemen.

## Een 3D-model toevoegen

1. Open het product in de bewerkingsmodus.

1. Als u met een specifieke winkelweergave wilt werken, stelt u de **[!UICONTROL Store View]** -kiezer in op de toepasselijke weergave.

   >[!NOTE]
   >
   >De nieuwe product 3D modellen zijn altijd _geupload en zichtbaar in_ alle _opslagmeningen, zelfs als het `All Store Views` werkingsgebied niet voor upload wordt gebruikt._ <br/><br/> om het even welke product 3D modellen van een specifieke opslagmening te verbergen, moet u aan die Mening van de Opslag overschakelen, **[!UICONTROL Hide from Product Page]** checkbox voor het 3D model selecteren, en klikken **[!UICONTROL Save]**.

1. Schuif omlaag en vouw de sectie _[!UICONTROL Product 3D Model]_&#x200B;uit.

   ![&#x200B; Pop-up van het Menu &#x200B;](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Voeg het 3D model (`.USDZ` dossier) van het product toe.

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
> Voor een reeks demonstratievideo&#39;s van een gebruiker die een 3d model aan een product toevoegen, zie de [&#x200B; AR Kijker voor Adobe Commerce &#x200B;](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html?lang=nl-NL) pagina in _de Video&#39;s en Tutorials van Commerce_.
