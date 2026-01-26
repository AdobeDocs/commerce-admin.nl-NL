---
title: '[!DNL Page Builder] instellen'
description: Leer over  [!DNL Page Builder]  eigenschapconfiguratie in Admin voor Adobe Commerce en Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder] instellen

Als deze optie is ingeschakeld in de configuratie, is [!DNL Page Builder] het standaardprogramma voor het maken van inhoud voor CMS-pagina&#39;s, -blokken en -blokken. Daarnaast biedt de knop _[!UICONTROL Enable Advanced CMS]_[!DNL Page Builder] als optie voor Categorieën en Producten. U kunt de standaard [ paginalay-out ](../content-design/page-layout.md) ook kiezen die u voor producten, categorieën, en de pagina&#39;s van CMS wilt gebruiken. [!DNL Page Builder] is niet beschikbaar voor nieuwsbrief inhoud, die de redacteur van WYSIWYG [ ](../content-design/editor.md) gebruikt.

>[!NOTE]
>
>Als [!DNL Page Builder] is geïnstalleerd, wordt de standaardinstelling voor het configuratieveld van [!UICONTROL Mask for Meta Description] genegeerd. De waarde wordt gewijzigd van `{{name}} {{description}}` in `{{name}}` .
><br>
>U kunt deze instelling openen door naar [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration] te gaan, [!UICONTROL Catalog] uit te vouwen en [!UICONTROL Catalog] eronder te kiezen. Het veld [!UICONTROL Mask for Meta Description] bevindt zich in de sectie [!UICONTROL Product Fields Auto-generation] .

>[!NOTE]
>
>Een gebruiker Admin moet [!UICONTROL Content] toestemmingen voor hun [ rolwerkingsgebied ](../systems/permissions-user-roles.md) hebben om [!UICONTROL Edit with Page Builder] knopen te zien en de Bouwer van de Pagina te kunnen gebruiken.

Voor meer informatie over de de configuratieopties van Hulpmiddelen van het Beheer van de Inhoud Geavanceerde, zie de [_Gids van de Verwijzing van de Configuratie_](../configuration-reference/general/content-management.md).

## Configureren [!DNL Page Builder]

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_de optie **[!UICONTROL Content Management]**.

1. Vouw ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** uit en verifieer dat **[!UICONTROL Enable Page Builder]** aan `Yes` wordt geplaatst.

   ![ Geavanceerde Hulpmiddelen van de Inhoud ](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Ga als volgt te werk als u klaar bent om [!DNL Google Maps] in te stellen:

   - Indien nodig, volg [ krijg API Zeer belangrijke ](https://developers.google.com/maps/documentation/javascript/get-api-key) instructies, en kopieer en kleef dan uw **[!UICONTROL Google Maps API Key]**.

   - Om **[!UICONTROL Google Maps Style]** te veranderen, kleef de code JSON die door de [[!DNL Google Maps]  APIs het Stileren Tovenaar ](https://mapstyle.withgoogle.com/) wordt geproduceerd.

   >[!NOTE]
   >
   >Zie [ Media - Kaart ](map.md) voor meer informatie over het gebruiken van [!DNL Google Maps] in uw [!DNL Page Builder] inhoud.

1. Ga als volgt te werk om het aantal hulplijnen in het kolomraster [!DNL Page Builder] te configureren:

   - Voer bij **[!UICONTROL Default Column Grid Size]** het standaardaantal kolommen in dat u in het raster wilt weergeven.

   - Voer bij **[!UICONTROL Maximum Column Grid Size]** het grootste aantal kolommen in dat u beschikbaar wilt hebben in het raster.

   >[!NOTE]
   >
   >Zie [ Lay-out - Kolom ](column.md) voor meer informatie over het gebruiken van het kolomnet wanneer het werken met uw [!DNL Page Builder] inhoud.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Standaardschermindelingen configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_de optie **[!UICONTROL Web]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** uit en doe het volgende:

   ![ StandaardLay-outs ](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Voor meer informatie over de de configuratieopties van het Web, zie de [_Gids van de Verwijzing van de Configuratie_](../configuration-reference/general/web.md#default-layouts).

   - Kies de **[!UICONTROL Default Product Layout]** die u voor productpagina&#39;s wilt gebruiken.

   - Kies de **[!UICONTROL Default Category Layout]** die u voor categoriepagina&#39;s wilt gebruiken.

   - Kies de **[!UICONTROL Default Page Layout]** die u voor CMS-pagina&#39;s wilt gebruiken.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## [!DNL Page Builder] uitschakelen

>[!NOTE]
>
>Het onbruikbaar maken [!DNL Page Builder] vervangt de Geavanceerde Hulpmiddelen van de Inhoud met de redacteur van WYSIWYG [ ](../content-design/editor.md), en zou vertoningsfouten in de storefront kunnen veroorzaken. Inhoud die u eerder met [!DNL Page Builder] hebt gemaakt, kan mogelijk niet vanuit de beheerder worden bewerkt.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_de optie **[!UICONTROL Content Management]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** uit en reeks **[!UICONTROL Enable Page Builder]** aan `No`.

1. Klik op **[!UICONTROL Turn Off]** wanneer u wordt gevraagd om te bevestigen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Wanneer ertoe aangezet, [ verfrist zich ](../systems/cache-management.md) om het even welk ongeldig geheime voorgeheugen.
