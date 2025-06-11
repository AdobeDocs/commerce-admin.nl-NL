---
title: Optimalisatie van afbeeldingen in mediagalerie
description: Leer hoe te om beeldoptimalisering voor uw  [!DNL Commerce]  media activa te gebruiken.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Optimalisatie van afbeeldingen in mediagalerie

De nieuwe [ Galerij van Media ](media-gallery.md) verstrekt een _beeldoptimalisering_ eigenschap, die prestaties verbetert en media dossiergrootte op de opslag vermindert. Deze optimalisatie is standaard ingeschakeld en kan worden gewijzigd in de configuratie-instellingen van de winkel.

## Optimalisatie van afbeeldingen configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** uit en doe het volgende:

   - Stel **[!UICONTROL Enable Image Optimization]** in op `Yes` .
   - Voer de waarden **[!UICONTROL Maximum Width]** en **[!UICONTROL Maximum Height]** (in pixels) naar wens in.

## Gedrag

Wanneer de het beeldoptimaliseringsfunctionaliteit van de Galerij van Media wordt toegelaten, wordt een geoptimaliseerde kopie van een beeld automatisch opgenomen in de inhoud van de [ Galerie van Media ](media-gallery.md) in plaats van het originele dossier.

Wanneer de _Maximale waarden van de Breedte_ en _Maximale Hoogte_ in de configuratie worden veranderd, werkt het alle bestaande geoptimaliseerde beelden bij die eerder werden opgenomen.

Voor de optimalisatie van afbeeldingen in de medialalerie is het vereist dat de gebruikers in de wachtrij van `media.gallery.renditions.update` de geoptimaliseerde afbeeldingen opnieuw genereren wanneer de configuratie wordt gewijzigd. Zie [ berichtrijen ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) beheren in de _Gids van de Configuratie_ voor meer details.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
