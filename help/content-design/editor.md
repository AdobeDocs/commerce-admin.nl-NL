---
title: WYSIWYG Editor
description: Leer hoe u de editor gebruikt en met inhoud werkt in een weergave _What You See is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# WYSIWYG Editor

De redacteur geeft u de capaciteit in te gaan en te formatteren terwijl het werken in een _Wat je ziet is wat je krijgt_ (WYSIWYG) weergave van de inhoud. Als u liever rechtstreeks met de onderliggende HTML-code werkt, kunt u de modi eenvoudig wijzigen. De editor kan worden gebruikt om inhoud te maken voor [pagina&#39;s](pages.md), [blokken](blocks.md), en [productbeschrijvingen](../catalog/product-content.md). Als u werkt met productdetails, klikt u op **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 is de standaard redacteur WYSIWYG. Een update van de TinyMCE 5.10-bibliotheek in Adobe Commerce en Magento Open Source 2.4.5 verhelpt een kwetsbaarheid die willekeurige JavaScript-uitvoering toestaat bij het bijwerken van een afbeelding of koppeling met bepaalde typen URL&#39;s. TinyMCE 3 is afgekeurd in de release 2.4.0 en verwijderd uit de release 2.4.3. TinyMCE 4 is verwijderd uit de release 2.4.4.

![Editor, werkbalk](./assets/editor-toolbar.png){width="700" zoomable="yes"}

De volgende onderwerpen verstrekken gedetailleerde informatie over het gebruiken van de redacteur:

- [Een koppeling invoegen](editor-insert-link.md)
- [Een afbeelding invoegen](editor-insert-image.md)
- [Een widget invoegen](editor-widget.md)
- [Een variabele invoegen](editor-insert-variable.md)

## De Editor configureren

De redacteur WYSIWYG wordt toegelaten door gebrek, en kan worden gebruikt om inhoud op CMS pagina&#39;s en blokken, en in producten en categorieën uit te geven. Vanuit de configuratie kunt u de editor activeren of deactiveren en ervoor kiezen om de statische editor te gebruiken in plaats van [dynamic](../catalog/catalog-urls.md#dynamic-url), URL&#39;s voor media-inhoud in product- en categoriebeschrijvingen.

![WYSIWYG-opties](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Zie voor een gedetailleerde beschrijving van alle WYSIWYG-opties [Inhoud beheren](../configuration-reference/general/content-management.md) in de _Configuratieverwijzing_.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Content Management]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Set **[!UICONTROL Enable WYSIWYG Editor]** naar uw voorkeur.

   De editor is standaard ingeschakeld.

1. Set **[!UICONTROL Static URLs for Media Content in WYSIWYG]** naar uw voorkeur voor iedereen [media-inhoud](../catalog/catalog-urls.md#static-url) die met de redacteur WYSIWYG is ingegaan.

1. Klik op **[!UICONTROL Save Config]**.
