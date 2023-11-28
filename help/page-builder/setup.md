---
title: '[!DNL Page Builder] instellen'
description: Meer informatie over [!DNL Page Builder] configuratie van functies in Admin voor Adobe Commerce en Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] instellen

Wanneer toegelaten in de configuratie, [!DNL Page Builder] is het standaardgereedschap voor het maken van inhoud voor CMS-pagina&#39;s, -blokken en dynamische blokken. Bovendien _[!UICONTROL Enable Advanced CMS]_knopaanbiedingen [!DNL Page Builder] als optie voor Categorieën en Producten. U kunt ook de standaardinstelling kiezen [pagina-indeling](../content-design/page-layout.md) die u wilt gebruiken voor producten, categorieën en CMS-pagina&#39;s. [!DNL Page Builder] is niet beschikbaar voor nieuwsbrief-inhoud, die WYSIWYG gebruikt [editor](../content-design/editor.md).

>[!NOTE]
>
>Wanneer geïnstalleerd, [!DNL Page Builder] Hiermee overschrijft u de standaardinstelling voor de [!UICONTROL Mask for Meta Description] configuratieveld. De waarde wordt gewijzigd van `{{name}} {{description}}` tot `{{name}}`.
><br>
>U hebt toegang tot deze instelling wanneer u naar [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], uitbreiden [!UICONTROL Catalog]en kiest u [!UICONTROL Catalog] onder. De [!UICONTROL Mask for Meta Description] veld bevindt zich in [!UICONTROL Product Fields Auto-generation] sectie.

>[!NOTE]
>
>Een Admin-gebruiker moet [!UICONTROL Content] machtigingen voor [rolbereik](../systems/permissions-user-roles.md) om te zien [!UICONTROL Edit with Page Builder] knoppen gebruiken en in staat zijn om Page Builder te gebruiken.

Voor meer informatie over de configuratieopties van Geavanceerde hulpmiddelen van het Beheer van de Inhoud, zie [_Referentiehandleiding voor configuratie_](../configuration-reference/general/content-management.md).

## Configureren [!DNL Page Builder]

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Content Management]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** en verifieert dat **[!UICONTROL Enable Page Builder]** is ingesteld op `Yes`.

   ![Geavanceerde gereedschappen voor inhoud](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Als u klaar bent om op te zetten [!DNL Google Maps]Ga als volgt te werk:

   - Indien nodig, volg de [API-sleutel ophalen][1] instructies, en kopieer en plak vervolgens uw **[!UICONTROL Google Maps API Key]**.

   - Als u het dialoogvenster **[!UICONTROL Google Maps Style]** plakt u de JSON-code die is gegenereerd door de [[!DNL Google Maps] Wizard API&#39;s opmaken][2].

   >[!NOTE]
   >
   >Zie [Media - toewijzen](map.md) voor meer informatie over het gebruik [!DNL Google Maps] in uw [!DNL Page Builder] inhoud.

1. Om het aantal richtlijnen in te vormen [!DNL Page Builder] Voer de volgende handelingen uit in het kolomraster:

   - Voor **[!UICONTROL Default Column Grid Size]** voert u het standaardaantal kolommen in dat u in het raster wilt weergeven.

   - Voor **[!UICONTROL Maximum Column Grid Size]** Voer het grootste aantal kolommen in dat u beschikbaar wilt hebben in het raster.

   >[!NOTE]
   >
   >Zie [Layout - kolom](column.md) voor meer informatie over het gebruiken van het kolomnet wanneer het werken met uw [!DNL Page Builder] inhoud.

1. Klik op **[!UICONTROL Save Config]**.

## Standaardschermindelingen configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Web]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** en voer de volgende handelingen uit:

   ![Standaardindelingen](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Voor meer informatie over de de configuratieopties van het Web, zie [_Referentiehandleiding voor configuratie_](../configuration-reference/general/web.md#default-layouts).

   - Kies de optie **[!UICONTROL Default Product Layout]** die u wilt gebruiken voor productpagina&#39;s.

   - Kies de optie **[!UICONTROL Default Category Layout]** die u wilt gebruiken voor categoriepagina&#39;s.

   - Kies de optie **[!UICONTROL Default Page Layout]** die u wilt gebruiken voor CMS-pagina&#39;s.

1. Klik op **[!UICONTROL Save Config]**.

## Uitschakelen [!DNL Page Builder]

>[!NOTE]
>
>Uitschakelen [!DNL Page Builder] vervangt de Geavanceerde Hulpmiddelen van de Inhoud met WYSIWYG [editor](../content-design/editor.md)en kunnen weergavefouten in de winkel veroorzaken. Inhoud die u eerder hebt gemaakt met [!DNL Page Builder] kan niet vanuit de beheerder worden bewerkt.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Content Management]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** en instellen **[!UICONTROL Enable Page Builder]** tot `No`.

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL Turn Off]**.

1. Klik op **[!UICONTROL Save Config]**.

1. Als hierom wordt gevraagd, [vernieuwen](../systems/cache-management.md) elke ongeldige cache.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
