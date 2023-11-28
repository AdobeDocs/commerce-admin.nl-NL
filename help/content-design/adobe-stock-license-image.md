---
title: Een Adobe Stock-afbeelding in licentie geven
description: Als u juridische toegang wilt garanderen en het Adobe Stock-watermerk wilt verwijderen, moet u een licentie voor uw Adobe Stock-afbeeldingen aanschaffen.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Een Adobe Stock-afbeelding in licentie geven

Adobe Stock-middelen die u voor uw productie-Adobe Commerce en Magento Open Source-winkels wilt gebruiken, moeten een licentie hebben. Dankzij deze licentie hebt u juridische toegang tot het image en kunt u het Adobe Stock-watermerk dat op alle [voorvertoningen afbeeldingen][save-preview]. Als u afbeeldingen wilt licentiëren of afbeeldingen met een licentie wilt opslaan, moet u zijn aangemeld bij uw Adobe-account.

De nieuwe [[!DNL Media Gallery]](media-gallery.md) biedt een directe integratie met Adobe Stock, zodat u eenvoudig rechtstreeks vanaf de galeriepagina licenties voor uw afbeeldingen kunt maken.

## Vereisten

Voor deze functie is het [Adobe Stock-integratie][adobe-stock-integration] module en configuratie. Licentie [Adobe Stock][adobe-stock] voor afbeeldingen is een betaald Adobe Stock-abonnement en een [Adobe][adobe-signin].

## Een licentie geven voor een afbeelding uit het nieuwe [!DNL Media Gallery]

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Voer de volgende stappen uit [Adobe Stock-afbeeldingen gebruiken][using-adobe-stock] om u aan te melden en voorvertoningsafbeeldingen op te slaan in de [media-opslag][media-storage].

   ![Opgeslagen voorvertoningsafbeelding](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Klik op de drie stippen onder de afbeelding (![Pictogram van het menu Element](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) en klik vervolgens op **[!UICONTROL License]**.

   ![Handelingen voor Adobe Stock-afbeeldingen](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Als u niet bent aangemeld, wordt het aanmeldingsformulier weergegeven. Voor meer informatie over login, zie [Adobe Stock-afbeeldingen gebruiken][using-adobe-stock].

1. Klik in het dialoogvenster voor het bevestigen van licenties op **[!UICONTROL Confirm]** om de afbeelding in licentie te geven.

   ![Licentie bevestigen](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >U moet beschikken over [Adobe Stock credits][stock-credits] in uw account om een licentie voor de afbeelding te geven.

## Een licentie geven voor een afbeelding van de standaard opslagmedia

1. [Het Adobe Stock-zoekraster openen][access-search].

1. Naar [de details van de afbeelding weergeven][view-details]klikt u op een afbeelding in de gewenste volgorde in het zoekraster.

1. Voer afhankelijk van de huidige licentiestatus van de afbeelding een van de volgende handelingen uit:

   - Als voor de afbeelding al een licentie is verleend, klikt u op **[!UICONTROL Save]**.

   - Als de afbeelding _niet_ gelicentieerd, klik **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >U moet beschikken over [Adobe Stock credits][stock-credits] in uw account om een licentie voor de afbeelding te geven.

   Met deze handeling wordt u gevraagd een bestandsnaam op te geven waarmee de afbeelding in de [media-opslag][media-storage]. Er is een standaardbestandsnaam opgegeven, maar u kunt de naam aanpassen aan uw voorkeuren.

   ![Afbeelding met Adobe Stock-licentie opslaan](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Klik op **[!UICONTROL Confirm]**.

   De pagina wordt omgeleid naar de mediaopslag en de opgeslagen voorvertoning wordt weergegeven.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
